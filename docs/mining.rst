.. _mining:

######
Mining
######

Link livenet has not been launched yet, so any mined Link will be worthless.

You need to have a Link account to receive the mining reward. If you do not have one already, go to the Link console and run ``personal.newAccount();``.

CPU mining
##########

Parity
------
Parity needs to be run with the address to receive the mining rewards specified with ``--author``. Then run ``ethminer -F http://127.0.0.1:8645``. ``-t`` can be specified to set the number of cores to be used. It defaults to using all cores.

Geth
----
CPU mining with Geth is very easy. Run the regular Geth command, but add the ``--autodag --mine`` options. Use ``--etherbase`` to specify which account will receive the mining rewards. It defaults to using all processor cores. This can be changed using the ``--minerthreads`` option.
