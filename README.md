# NPBMZ.jl

This is an experimental implementation of the multizone versions of the simulated applications __SP__, __BT__, and __LU__, from the [NAS Parallel Benchmarks (NPB)](https://www.nas.nasa.gov/software/npb.html) in Julia, developed to be a case study of multicluster computations using an extended version of [Distributed.jl](https://github.com/PlatformAwareProgramming/Distributed.jl) with multilevel parallelism. 

The zones are workload units that are distributed from a _driver process_, using Distributed.jl, across the _entry processes_ running in the access node of one or more clusters. Then, using [MPI.jl](https://github.com/JuliaParallel/MPI.jl), the entry processes divide the zones into cells to be distributed across _worker processes_ distributed over the cluster nodes. 

## Reference ##
Francisco Carvalho Junior and Tiago Carneiro. 2024. Towards multicluster computations with Julia. In Anais do XXV Simpósio em Sistemas Computacionais de Alto Desempenho, outubro 23, 2024, São Carlos/SP, Brasil. SBC, Porto Alegre, Brasil, 276-287. DOI: https://doi.org/10.5753/sscad.2024.244307.
