.. _mining:

######
Mining
######

You need to have a Link account to receive the mining reward. If you do not have one already, go to the Link console and run ``personal.newAccount();``.

CPU mining
##########

Geth
----
CPU mining with Geth is very easy. Run the regular Geth command, but add the ``--autodag --mine`` options. It will mine into the first account that it knows about. This can be overridden with ``--etherbase``. It defaults to using all cores. This can be changed using the ``--minerthreads`` option.
