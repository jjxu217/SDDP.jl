# SDDP.jl with compromise policy
The repository contains the code for the compromise policy in multi-stage stochastic programming (MSLP).
The compromise policy is constructed on top of Stochastic Dual Dynamic Programming. The single replication SDDP code is based on the SDDP.jl package by Oscar Dowson.

## CompromiseSDDP
In order to run the compromiseSDDP algorithm, please check out the compromiseSDDP branch.
CompromiseSDDP solves the MSLP problems with mulitple replications, where each replication is solved by SDDP. 
After solving each replication independently and parallelly, CompromiseSDDP formulates the compromise policy as the final policy.

## CompromiseODDP
To run compromiseODDP, please check out the compromiseODDP branch.
CompromiseODDP solves the MSLP problems with mulitple replications, where each replication is solved by ODDP. 
ODDP algorithm generates the sample on-the-fly, and applys sequential sampling scheme to iteratively update the function approximation.
After solving each replication independently and parallelly, CompromiseS`ODDP formulates the compromise policy as the final policy.
