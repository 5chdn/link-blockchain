# Link Blockchain Testnet

[![Join the chat at https://gitter.im/link-blockchain/link-blockchain](https://badges.gitter.im/link-blockchain/link-blockchain.svg)](https://gitter.im/link-blockchain/link-blockchain?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

The purpose of Link Blockchain is to permanently store semantic linked data. Mainnet has not been activated yet.

## Cryptofuel

Name: Link

Code: LINK

Symbol: `🔗`

BIP44 coin type (once live): 76 / 0x8000004c

## Ethereum configuration

Network ID: 13919287

Port: 30313

RPC Port: 8645

WS Port: 8646

## Parity instructions

    parity --chain link.json --db-path ~/.link-parity --port 30313 --jsonrpc-port 8645 --geth

## Geth instructions

    geth --datadir ~/.link-geth init genesis.json
    cp static-nodes.json ~/.link-geth
    geth --datadir ~/.link-geth --networkid 13919287 --port 30313 --rpcport 8645 --wsport 8646
    # In a separate terminal launch the console.
    geth attach ~/.link-geth/geth.ipc
