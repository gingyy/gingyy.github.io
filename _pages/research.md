---
layout: page
title: research
permalink: /research/
subtitle: 
nav: true
nav_order: 2
---

---
### NTT Research, Inc.

Most recently, I was at [NTT Research](https://ntt-research.com/) in the [Physics & Informatics Laboratory](https://phi.ntt-research.com/). Working with [Adil Gangat](https://scholar.google.com/citations?user=BAvEYIUAAAAJ&hl=en), I developed methods for a new combinatorial optimization metaheuristic competitive with current state-of-the-art classical and quantum heuristics such as Memetic Tabu Search and QAOA. This was a very fun opportunity to return to discrete optimization problems, which first captured my interest during undergrad.

The problem I worked on is called [Low Autocorrelation Binary Sequences (LABS)](https://arxiv.org/abs/1512.02475), an NP-hard combinatorial optimization problem. It is a hard benchmarking problem which has practical applications in signal processing and communications engineering. In LABS, we aim to determine a sequence of binary variables in which the values correlate the least with itself when the sequence is delayed. This is particularly helpful when designing signals to minimize interference with itself.

LABS can be formulated as the Bernasconi spin glass model, with long-range 4-spin interactions. While existing methods generally involve optimizing the entire sequence (of length $N$), our method involves instead only optimizing very small *subsystems* (of $n=4$ spins at a time) and is still capable of obtaining the full optimal sequence for at least up to $N=60$.

See the details of our method and scaling results in our new [preprint](https://arxiv.org/abs/2610.14361).
Our work also belongs to the broader discussion on the role of specialized optimization hardware. Since we are able to decompose the LABS problem and still obtain global optimization with good scaling, specialized hardware with only a few logical variables could potentially see real practical value in large-scale discrete variable optimization problems.



---
### Emory University

It's always fun to tell people that spin glasses neither spin nor are they made of glass. Through working with [Stefan Boettcher](https://faculty.college.emory.edu/sites/boettcher/), I developed my interest in spin glass models and their connections to combinatorial optimization.

[Extremal Optimization (EO)](https://en.wikipedia.org/wiki/Extremal_optimization) is a local search heuristic inspired by self-organization in nature. In ecosystems, a small change in one species can cascade through its interactions with other species, reshaping the ecosystem as a whole. Regardless of whether this change is "good" or "bad," the ecosystem will rearrange into an equilibrium either way.

In each step of the EO heuristic, the worst-performing spin is identified and its value is randomly changed (for better or for worse). Through this simple mechanism, the search alternates between converging toward local minima and triggering large cascades of change, enabling it to quickly explore many local minima in search of the global optimum.


In my project, I implemented EO for a spin glass with 3-spin connections, an extension of the 2-spin Sherrington-Kirkpatrick model. In adapting EO for higher-order problems, we developed parallelization methods. I wrote my [undergraduate thesis](https://etd.library.emory.edu/concern/etds/rb68xd344) on this topic, and my work also contributed to a characterization of ground state behavior in this $p=3$ mean field spin glass, described in this *Physical Review Letters* [paper](https://arxiv.org/abs/2501.13205).




---
### Fulbright Germany

I was very fortunate to spend one year abroad in Stuttgart, Germany through the [Fulbright Study/Research Award](https://us.fulbrightonline.org/). I was at the [Stuttgart Center for Simulation Science (SimTech)](https://www.simtech.uni-stuttgart.de/sc/) in the group of [Miriam Klopotek](https://www.simtech.uni-stuttgart.de/career/junior-research-groups/many-body-simulations/). Alongside increasing my foreign language skills and enjoying a new culture, I worked on oscillators that synchronize and swarm, also known as [swarmalators](https://www.complexity-explorables.org/explorables/swarmalators/). Swarming (e.g., flocks of birds) and synchronization (e.g., fireflies flashing) are both self-organizational behaviors in systems. 

In this project, I further explored how principles of self-organization in nature can inspire new approaches to computing. First, I added a leader agent into a system of swarmalators, controlling only the leader's position and phase. Response of the swarmalator system was governed by internal equations linking spatial proximity to internal phase update and phase similarity to attraction/repulsion between swarmalators. 


The presence of a leader agent gives rise to rich swarmalator dynamics, with well-defined phase boundaries between self-organized states. I presented a characterization of these dynamics in a talk at the [German Physical Society (DPG) Spring Meeting](https://www.dpg-verhandlungen.de/year/2025/conference/regensburg/part/dy/session/3/contribution/8?lang=en). This work can have potential applications in distributed systems, such as robotic swarms and other autonomous systems of many agents. 

It is also an excellent candidate system for [reservoir computing](https://arxiv.org/html/2412.13212v1). Reservoir computing is a machine learning framework where rather than training many layers of neurons, a high-dimensional system (reservoir) is used as the black box instead. Only the readout layer is trained to link the reservoir to prediction outputs. Major benefits include faster training and the future possibility to use physical systems as the reservoir, inspiring novel energy-efficient hardware implementations. Initial tests using simulations of swarmalators for reservoir computing are promising.



---
### Lawrence Livermore National Laboratory

I spent one summer at [LLNL](https://www.llnl.gov/) in the [Defense Science and Technology Internship](https://sd.llnl.gov/students) program, working on shock compression modeling using multi-physics simulation codes.


---
### REU at Brigham Young University

Through the national [Research Experiences for Undergraduates](https://www.nsf.gov/funding/initiatives/reu) summer internship program, I worked with [Traci Neilsen](https://hydroacoustics.byu.edu/) on machine learning for hydroacoustics applications. 

Determining the composition of the ocean floor is of interest to both science and industry. While collecting physical samples from the seafloor is costly and time-consuming, sediment types can also be determined using acoustics. Different sediments reflect sound waves differently, and the resulting acoustical signals encode information about the seafloor within. 



In my project, I worked on a [residual neural network](https://en.wikipedia.org/wiki/Residual_neural_network) to predict on sound signals recorded at multiple depths underwater. We used methods in physics-based synthetic data generation and trained a model which made predictions consistent with results from the [SBCEX 2017](https://wwwext.arlut.utexas.edu/sbcex/).

After the summer, I continued working virtually with Dr. Neilsen, presented my first [conference talk](https://doi.org/10.1121/2.0001971), and published a first-author [paper](https://doi.org/10.1121/10.0036221).


---
---
*Bonus: click [here](https://gingyy.github.io/research/spin-glass) for a non-technical explanation of spin glasses.*
