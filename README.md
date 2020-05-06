# mclpif
Maximal Covering Location Problem with Interconnected facilities

Detailed results of our computational experiments for the manuscript "Continuous maximal covering location problems\\with interconnected facilities" by Víctor Blanco y Ricardo Gázquez.

In particular:

- Instances: based on the 50-points data set in (Eilon, S., Watson-Gandy, C. D.~T., and Christofides, N. (1971).
Distribution management : mathematical modelling and practical analysis. Folder "instances" in the form eilonN_i.csv where N is the number of demand points (N in {10, 20, 30, 40, 50} and i the instance (i in {1,2,3,4,5}).
- Results: Organized by graph structure. GraphType in {Cycle, Line, Complete, Matching, Ring, RingStar} in files GraphType_Results.csv with columns:
  * instance: file
  * GraphType
  * n: number of demand points
  * p: centers to be located
  * R: Coverage radius
  * r: limit radius between facilities
  * obj_NL: Objective value for the MINLP formulation.
  * Time_NL: CPU Time for the MINLP formulation.
  * Relax_NL: Root node relaxation of the MINLP formulation.
  * Gap_NL: MIPGap for the MINLP formulation within the time limit (3600 secs)
  * C_NL: Clusters of points obtained with the MINLP formulation.
  * obj_IP1: Objective value for the Incomplete formulation (INC1).
  * Time_IP1: CPU Time for solving the IP problem with the Incomplete formulation (INC1).
  * Relax_IP1: Root notde relaxation for the Incomplete formulation (INC1).
  * LC_IP1: # of Linear constraints  for the Incomplete formulation (INC1).
  * numcuts_IP1: # of Cuts in the B-&-C skeme for the Incomplete formulation (INC1).
  * TConstrGen_IP1: CPU time required to generate constraints for the Incomplete formulation (INC1).
  * TotalT_IP1: Total CPU time for the Incomplete formulation (INC1) to solve the problem.
  * GapIP1: MIPGap  for the Incomplete formulation (INC1) within the time limit (3600 secs).
  * C_IP1: Clusters of points obtained with formulation (INC1).
  * obj_IP2: Objective value for the Incomplete formulation (INC2).
  * Time_IP2: CPU Time for solving the IP problem with the Incomplete formulation (INC2).
  * Relax_IP2: Root notde relaxation for the Incomplete formulation (IN2).
  * LC_IP2: # of Linear constraints  for the Incomplete formulation (INC2).
  * numcuts_IP2: # of Cuts in the B-&-C skeme for the Incomplete formulation (INC2).
  * TConstrGen_IP2: CPU time required to generate constraints for the Incomplete formulation (INC2).
  * TotalT_IP2: Total CPU time for the Incomplete formulation (INC1) to solve the problem.
  * GapIP2: MIPGap  for the Incomplete formulation (INC2) within the time limit (3600 secs).
  * C_IP2: Clusters of points obtained with formulation (INC2).


We also report a file with the results obtained with the compact formulation (file ovals.csv) with the following information:
  
  * obj_IP: objective value.
  * IP_Time: CPU time required to solve the IP problem.
  * COntrGen_Time: CPU Time required to incorporate the constraints to the model. 
  * Tot_Time: Total CPU time (IP_Time + COnctr_Time)
  * #Ball_Ctrs: Number of ball-type constraints.
  * #O_Ctrs: Number of O-sets constraints.
  * #All_Ctrs: Total number of constraints.
  * Gap: MIP Gap for the IP formulation within the time limit (3600 secs)
  * NonComputed: 1 if  and 0 otherwise
  * OoM: 1 if the problem got a Out Of Memory Flag in Gurobi; 0 otherwise.
