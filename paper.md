---
title: 'Autarky: A Modular Optimization Platform for Distributed Energy Systems under Uncertainty'
tags:
  - energy systems
  - optimization
  - Julia
  - JuMP
  - mini-grids
  - chance constraints
  - decentralized electrification
authors:
  - name: XXXX
    orcid: XXXX
    affiliation: '1'
affiliations:
  - index: 1
    name: XXX
    ror: XXX
date: XXX
bibliography: paper.bib
---

# Summary

Autarky is a modular, open-source modeling platform for the techno-economic optimization of distributed energy systems under uncertainty. Built in Julia using the JuMP modeling language, Autarky allows users to define, simulate, and optimize hybrid mini-grid architectures with configurable levels of modeling complexity, including deterministic and probabilistic formulations. It supports linear programming (LP), expected value models, and individual and joint chance constraints (ICC/JCC) to account for forecast uncertainty and reliability targets.

Designed for flexibility and accessibility, Autarky features a front-end web interface for parameter input, result visualization, and comparative analysis of planning scenarios. The backend implements a suite of optimization models that are easily extendable and tailored for energy access planning, particularly in Sub-Saharan Africa and other contexts with unreliable or no main grid access.

# Statement of need

Energy system planning tools are essential for designing affordable and reliable electrification solutions in areas with constrained infrastructure and high uncertainty in demand and renewable supply. Existing tools often either (i) lack probabilistic reliability modeling, (ii) are not open source, or (iii) do not scale well to decentralized, modular energy systems. Autarky addresses these gaps by:

- Enabling high-resolution, long-term optimization of off-grid systems with seasonality and uncertainty.
- Supporting multiple formulations (LP, EV, ICC, JCC) to balance computational cost and system robustness.
- Including JCC formulations using the JointChance.jl package, enabling power system planners to specify reliability levels over outage durations.
- Offering an integrated user interface to facilitate adoption by policy-makers, planners, and non-programmers.

Autarky is already used in ongoing research projects and educational contexts, including the iDesignRES EU project and EMP-A 2025 training in Addis Ababa.

# Functionality

Autarky allows users to:

- Configure decentralized energy systems with solar, batteries, diesel gensets, and grid connection options.
- Upload time series data or use APIs (e.g., PVGIS) for renewable potential.
- Define seasonal representative periods for long-term simulations.
- Solve deterministic, expected value, and probabilistic optimization problems.
- Visualize key outputs such as dispatch, capacity sizing, and costs.
- Compare scenarios (e.g., low-cost vs. high-reliability solutions) via a web dashboard.

All formulations share a common YAML-based input schema and JSON result format for interoperability and reproducibility.

# Research applications

Autarky has enabled:

- Probabilistic analysis of mini-grid islanding during main-grid outages, using ICC and JCC constraints with Gaussian error distributions.
- Optimal sizing and dispatch of systems for informal settlements (e.g., Kingstone in Mukuru, Nairobi), revealing cost-robustness tradeoffs in marginalized urban contexts.
- Comparative analysis of grid-tied vs. stand-alone planning scenarios across diverse geographies and regulatory assumptions.

Ongoing work includes extending the platform to swarm-grids and tariff design using complementarity constraints under uncertainty.

# Acknowledgements

XXXX

# References
