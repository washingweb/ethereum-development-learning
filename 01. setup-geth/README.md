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
## console
```bash
geth --datadir=~/.etherem/net102216 --networkid 102216 console
```
## commands
network
```javascript
net.version
net.peerCount
```
accounts
```javascript
eth.accounts
personal.newAccount()
personal.unlockAccount(eth.accounts[0])
eth.getBalance(eth.accounts[0])
```
mining
```javascript
// status
eth.mining
eth.blockNumber
txpool.content.pending

// start/stop
minter.start(1)
minter.stop()

// Minning rewards will goto coinbase account, which defaults to eth.accounts[0]
eth.coinbase

// get balance
eth.getBalance(eth.coinbase)
web3.fromWei(eth.getBalance(eth.coinbase), "ether")

// block
var block = eth.getBlock(0)
block.transactions.length

// transaction
var txHash = eth.sendTransaction({from: eth.accounts[0], to: eth.accounts[1], value: web3.toWei(5, "ether")})
eth.getTransaction(txHash)
eth.getTransactionFromBlock(blockNumber, transactionIndex)
eth.getTransactionReceipt(txHash)
```

```javascript
admin.nodeInfo.enode
```

Tick to list initial commands
> type 2 spaces and hit TAB twice

## backup private key
```bash
ls ~/.ethereum/net42/keystore/
```

## reference
[Private network](https://github.com/ethereum/go-ethereum/wiki/Private-network)
