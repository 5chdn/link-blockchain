.. _configuration:

#############
Configuration
#############

Network ID: 13919287

Port: 30313

RPC Port: 8645

WS Port: 8646

Parity instructions
-------------------
.. code::

    parity --chain link.json --db-path ~/.link-parity --port 30313 --jsonrpc-port 8645 --geth

Geth instructions
-----------------
.. code::

    geth --datadir ~/.link-geth init genesis.json
    cp static-nodes.json ~/.link-geth
    geth --datadir ~/.link-geth --networkid 13919287 --port 30313 --rpcport 8645 --wsport 8646
    # In a separate terminal launch the console.
    geth attach ~/.link-geth/geth.ipc
