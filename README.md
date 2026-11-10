# Steiner Topology Cluster: Unsupervised Instance Profiling

This repository provides an unsupervised machine learning pipeline designed to classify the topological complexity of Steiner Forest Problem (SFP) instances. By automatically grouping graphs based on their structural difficulty, this tool creates reliable blocking factors for statistical analysis.

### Dataset and Original Sources

The graphs and network instances processed by this pipeline are originally part of the SteinForestLib collection.

* **Instance Repository:** All instances utilized in this project can be accessed at [https://github.com/lalehghalami/SteinForestProblem](https://github.com/lalehghalami/SteinForestProblem)
* **Original Reference:** foundational study:
> Ghalami L, Grosu D. Approximation algorithms for Steiner forest: An experimental study. *Networks*. (2022), 164–188. [https://doi.org/10.1002/net.22046](https://doi.org/10.1002/net.22046)

### Theoretical Background

The Steiner Forest Problem (SFP) is a classic NP-hard combinatorial optimization challenge with critical real-world applications in VLSI circuit routing and large-scale network survivability design. It requires finding a minimum-cost subgraph that interconnects specific subsets of terminal nodes, allowing the use of auxiliary Steiner nodes to optimize the global structure.

### Methodology

Instead of forcing instances into rigid, predefined partitions, the model builds a similarity hierarchy. The grouping is based on the characteristics of the instances (graph topology + terminal pairs + node characteristics).

### Experimental Impact

The discovery of these conglomerates solves the problem of extremely high variance in performance analysis. The discovered clusters act directly as a Blocking Factor in subsequent Analysis of Variance (ANOVA) models.

By comparing computational performance within groups that share the same level of structural difficulty, the model reduces the noise and Experimental Error (SSE) that occurs when mixing incomparable topologies. This ensures complete statistical rigor and independence in the results when evaluating disruption metaheuristics, neutralizing execution time bias and revealing in which complexity scenarios the optimization truly excels.
