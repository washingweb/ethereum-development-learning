## install
```bash
sudo apt-get update
sudo apt-get install -y software-properties-common
sudo add-apt-repository -y ppa:ethereum/ethereum
sudo apt-get update
sudo apt-get install -y ethereum
```

## create a private chain
```bash
# do it once
geth --datadir=~/.ethereum/net102216 init genesis102216.json

# run every time
geth --datadir=~/.ethereum/net102216 --networkid 102216
```

