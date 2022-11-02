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





#### Allocations

The allocation process works to broadcast/advertise which subgraphs an indexer is indexing, so it helps to build a “state of the world” on-chain. But particularly is part of the game indexers play to compete for indexing rewards, they need to optimize what they stake into what subgraph using their available stake.&#x20;

An allocation can last for more than 28 days, but after the 28 days anyone can close it. The motivation for this rule was to prevent indexers from withholding rewards for a long time rather than distributing them to delegators.&#x20;

Getting rid of the allocation process if we ever find a better mechanism would hugely reduce on-chain traffic. We may always want a process by which indexers tell what they serve, but this may be moved off-chain by querying them about it through endpoints (_e.g._ via the GraphCast gossip network). As long as indexers must play the stake to subgraph allocation game for indexing rewards, this information will be on-chain because the on-chain protocol is the gatekeeper to distribute those rewards.



(INSERT DETAILED VERSION OF DISTRIBUTION VIA SNAPSHOTTING LIKE [HERE](https://forum.thegraph.com/t/gip-0034-the-graph-arbitrum-deployment-with-a-new-rewards-issuance-and-distribution-mechanism/3418))

