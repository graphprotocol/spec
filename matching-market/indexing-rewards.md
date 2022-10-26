---
description: (under construction)
---

# Indexing Rewards

(Copy some high-level stuff from blogs)



The Graph introduced indexing rewards as a bootstrapping mechanism. The supply of GRT increases continuously. In a nutshell, the indexing rewards during a period of time (_e.g._ a day) equal the increase in GRT supply. This increase in supply is paid to indexers for indexing subgraphs.

The indexing rewards $$R_i$$​ obtained by the $$i$$-th indexer equal the issuance rate $$\Phi$$​ multiplied by the sum over of all subgraphs $$j\in\mathcal{S}$$ of the products of the indexer's relative portion $$\omega_{ij}$$ of allocated stake $$\Omega_j$$ on each subgraph and the relative amount of signal $$\psi_j$$ on each subgraph of total signal $$\Psi$$. That is,

| $$\displaystyle R_i = \Phi\cdot\sum_{j\in \mathcal{S}} \dfrac{\omega_{ij}}{\Omega_j}\cdot\dfrac{\psi_j}{\Psi}$$ |
| :-------------------------------------------------------------------------------------------------------------: |







