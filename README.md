This source code repository contains a python implementation of an algorithm for bounding the synchronization threshold of directed networks of diffusively-coupled nonlinear oscillators.  The method is described in detail in [1]  and implemented in the routine gcg() in file gcg.py.  The novel optimization procedure described in [1] for the selection of a choice of paths between connected node pairs which minimizes the bound is likewise implemented in the same routine.

The routine gcg() accepts two default parameters:  A, the adjacency matrix of the directed network, and a, which is double the minimum strength of coupling required for globally asymptotically stable synchrony in the network of two mutually and symmetrically coupled nodes.  Another optional parameter alpha determines the "greediness" of the optimization procedure; alpha=0 disables this optimization, while alpha<1 does not allow the procedure to backtrack; the computational complexity is therefore dependent on alpha.  Usually, setting alpha to 1 yields an acceptable bound.

The source code for gcg() is heavily documented and several worked examples of the computation are given in [1].  If the python file is run as a standalone program, the first commandline argument is interpreted as a tab-separated text file containing the adjacency matrix of the network on which to perform computation.  The default value of a is 7.79 which is associated with the chaotic Lorenz system with standard parameters (10,28,8/3).

You may use this code for any purpose; however, please cite the following paper:

[1] "Synchronizability in directed networks: The power of nonexistent ties."  Kevin Daley, Kun Zhao, and Igor Belykh.  Manuscript submitted (2019).
