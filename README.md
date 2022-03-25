# SDDP.jl with compromise policy
The repository contains the code for the compromise policy in multi-stage stochastic programming (MSLP).
The compromise policy is constructed based on stochastic dual dynamic programming or online dual dynamic programming. The single replication SDDP code is based on the [SDDP.jl](https://github.com/odow/SDDP.jl) package by [Oscar Dowson](https://odow.github.io/). Thanks Oscar.

This repository is a developping version of the official SDDP.jl package, which is able to run multiple replications and construct the compromise policy.
In order to run the compromise policy, please first download this package. 
Then, 
```
dev path_to_the_package
```
which will switch the SDDP.jl to our package in Julia. If you have any question, please check [Developing packages in Julia](https://pkgdocs.julialang.org/v1/managing-packages/#developing). 

## CompromiseSDDP
In order to run the compromiseSDDP algorithm, please check out the compromiseSDDP branch.
CompromiseSDDP solves the MSLP problems with mulitple replications, where each replication is solved by SDDP. 
After solving each replication independently and parallelly, CompromiseSDDP formulates the compromise policy as the final policy.

## CompromiseODDP
To run compromiseODDP, please check out the compromiseODDP branch.
CompromiseODDP solves the MSLP problems with mulitple replications, where each replication is solved by ODDP. 
ODDP algorithm generates the sample on-the-fly, and applys sequential sampling scheme to iteratively update the function approximation.
After solving each replication independently and parallelly, CompromiseS`ODDP formulates the compromise policy as the final policy.
