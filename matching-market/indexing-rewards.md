---
description: (under construction)
---

# Indexing Rewards

(write some high-level stuff like in blogs - tech writer will excel here)



The Graph introduced indexing rewards as a bootstrapping mechanism. The supply of GRT increases continuously. In a nutshell, the indexing rewards during a period of time (_e.g._ a day) equal the increase in GRT supply. These rewards are paid to indexers for indexing subgraphs. Specifically, the indexing rewards $$R_i$$​ obtained by the $$i$$-th indexer equal the issuance rate $$\Phi$$​ multiplied by the sum over of all subgraphs $$j\in\mathcal{S}$$ of the products of the indexer's relative portion $$\omega_{ij}$$ of allocated stake $$\Omega_j$$ on each subgraph and the relative amount of signal $$\psi_j$$ on each subgraph of total signal $$\Psi$$. That is,

| $$\displaystyle R_i = \Phi\cdot\sum_{j\in \mathcal{S}} \dfrac{\omega_{ij}}{\Omega_j}\cdot\dfrac{\psi_j}{\Psi}$$ |
| :-------------------------------------------------------------------------------------------------------------: |

{% hint style="danger" %}
Indexing rewards form the majority of indexer income in The Graph today. This is problematic as it hinders the adoption of serving queries, the core purpose of this protocol. Ongoing work aims to address these misaligned incentives.
{% endhint %}





