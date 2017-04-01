.. _configuration:

#############
Configuration
#############

Network ID: 13919287

Port: 30313

RPC Port: 8645

WS Port: 8646

.. code::

    git clone https://github.com/link-blockchain/link-blockchain.git

Parity
------

Install Parity as described here: https://parity.io/parity.html

.. code::

    parity --chain link.json --db-path ~/.link-parity --port 30313 --jsonrpc-port 8645 --geth

Geth
----

Install Geth as described here: https://github.com/ethereum/go-ethereum/wiki/Building-Ethereum

.. code::

    geth --datadir ~/.link-geth init genesis.json
    cp static-nodes.json ~/.link-geth
    geth --datadir ~/.link-geth --networkid 13919287 --port 30313 --rpcport 8645 --wsport 8646 --fast
    # In a separate terminal launch the console.
    geth attach ~/.link-geth/geth.ipc

Netstats
--------

To have your node listed on http://stats.link-blockchain.org/ do the following (requires `Node.js <https://nodejs.org/en/>`_):

.. code::

    git clone https://github.com/cubedro/eth-net-intelligence-api
    cd eth-net-intelligence-api
    npm install
    sudo npm install pm2

Edit app.json::

         {
           "NODE_ENV"        : "production",
           "RPC_HOST"        : "localhost",
    -      "RPC_PORT"        : "8545",
    -      "LISTENING_PORT"  : "30303",
    -      "INSTANCE_NAME"   : "",
    +      "RPC_PORT"        : "8645",
    +      "LISTENING_PORT"  : "30313",
    +      "INSTANCE_NAME"   : "MY_NODE_NAME",      // Customize this.
           "CONTACT_DETAILS" : "",
    -      "WS_SERVER"       : "wss://rpc.ethstats.net",
    -      "WS_SECRET"       : "see http://forum.ethereum.org/discussion/2112/how-to-add-yourself-to-the-stats-dashboard-its-not-automatic",
    +      "WS_SERVER"       : "ws://stats.link-blockchain.org:3000",
    +      "WS_SECRET"       : "welcometothelinkedworld",
           "VERBOSITY"       : 2
         }

Then::

    pm2 start app.json
