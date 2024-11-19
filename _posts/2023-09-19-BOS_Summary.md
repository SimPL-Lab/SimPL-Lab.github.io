---
title:  "Bayesian optimization for the vehicle dwelling policy in a semiconductor wafer fab"
header:
    teaser: "/assets/images/BOS.jpg"
excerpt: "New paper has been published in IEEE Transactions on Automation Science and Engineering."
author: "Hyunjung"
categories:
  - Paper summary
tags:
  - Simulation
  - Bayesian optimization
  - FAB
last_modified_at: 2023-09-19
---
<img align="center" width="900" height="900" style="border: 1px solid white" src="/assets/images/BOS.jpg">

Journal : IEEE Transactions on Automation Science and Engineering

Title : Bayesian optimization for the vehicle dwelling policy in a semiconductor wafer fab

Authors : Bonggwon Kang, Chiwoo Park, Haejoong Kim, and Soondo Hong

Abstract : Many semiconductor fabrication plants (fabs) prefer simulation-based decision making for vehicle dwelling policies because it can capture a fab’s scalability and complexity. Vehicle dwelling policies assign idle vehicles to intra-bay and outer loops in automated material handling systems (AMHSs) to respond quickly to transportation demands. Fabs are motivated to control vehicle dwelling policies when fabs experience significant fluctuations, i.e., changes in product mix. Fab operators evaluate manually designed candidate solutions because it is time-intensive to run a large-scale simulation with numerous potential solutions. To determine a vehicle dwelling policy, we propose a simulation optimization approach based on Bayesian optimization (BO) with class-based clustering. BO adaptively traces efficient vehicle dwelling policies based on a surrogate model and an acquisition function. Class-based clustering alleviates the high dimensionality of the design space by grouping bays into a small number of classes. By striking a balance between the complexity of the design space and the quality of the solutions, our proposed policy significantly reduces the number of simulation runs required to determine efficient vehicle dwelling policies. We conclude that BO with class-based clustering is more advantageous than using a genetic algorithm (GA) and using heuristics. 


[http://doi.org/10.1109/TASE.2023.3320189](http://doi.org/10.1109/TASE.2023.3320189)