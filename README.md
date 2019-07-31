# SimulatorWaterNetworkLoopMethod
Simulator algorithm for water networks based on loop method


Simulation of water networks by using the loop method and Newton-Raphson numerical method  (wat_dem1.m)
 
There are given the nodal consumptions, the characteristics of the pipes, head value of reference main head node, inflows/outflows. 

sim_demo_pb.m   - simulation of water networks by using the loop method and Newton-Raphson numerical method.

determine_flowsi_pb.m - this function uses Depth First search to calculate the following variables: the loop incidence matrix Mlp, the topological incidence matrix Anp, initial pipe flows flows_i, chord/co-tree pipes.

shortest_path.m  - This function calculated shortest path between two nodes in the spanning tree.

This simulator can be applied to any water network not containing non-linear controlling hydraulic elements although some “minor modifications” would be necessary in the various Matlab files such as :
- in sim_demo_pb.m at line 98 the number of loops l is 28, so for a different water network the number of loops would be different so it is better to change the number 28 with the letter l which stands for the number of loops.  
- other “minor modifications” would be for example in the file determine_flowsi_pb.m at line 408, to remove nodes 65, 61, 62, 35, 34 and node 33 which are fixed head nodes but in a different water network these numbers may not mean anything.
- other similar “minor modifications”.  

This algorithm would benefit also from the addition of non-linear controlling elements based for example on the paper Alvarruiz et al. (2018) “Efficient modeling of active control valves in water distribution systems using the loop method”, J. Water Resour. Plann. Manage.  

The project has also a DoI: 

The license for this software is a Creative Commons Attribution 4.0 International License (CCL). 

