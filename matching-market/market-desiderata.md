# Market Desiderata

### Introduction

This pages discusses properties that help markets operate "successfully." First high-level properties are covered, which are then expanded upon in the context of The Graph.

### Desiderata

> Each of these ubiquitous marketplaces has found a way to succeed not only in making markets thick, uncongested, and safe, but also in making them _simple to use_.\
> ****\
> ****-Alvin Roth

The core properties for a market are concisely summarized by Roth in the quote above. Below we overview relevant market properties and their interpretation in our context. In addition to Roth's list, note we strive for computationally efficiency in order to obtain practical gas costs in blockchain environments.

{% hint style="info" %}
**Safe**\
****The single most important aspect of marketplace design is safety. Here this is measured in two respects. The first is participants can reveal their true preferences, without running a risk that by doing so they will receive a worse outcome than if they had behaved strategically and stated some other preferences (_e.g._ consider high school matching, matching for medical residencies, and auctions). Since curation markets have optional participation, we must also ensure folks are not worse off by truthful participation. These two properties are, respectively, called dominant strategy incentive compatible (DSIC) and individual rationality (IR).&#x20;
{% endhint %}

{% hint style="info" %}
**Simple**

We consider simplicity along two dimensions: actions and their consequences are simple to understand (low cognitive overhead) and tasks are simple to perform (efficient workflows). As Roth concisely notes, "being easy to describe isn't the same as being easy to navigate." In fact, markets may use complex algorithms "under the hood" to execute transactions for simple strategies. This is the case for various matching markets (_e.g._ medical residencies).
{% endhint %}

{% hint style="info" %}
**Thick**

A market is _thick_ provided it brings together enough potential buyers and sellers to produce satisfactory outcomes for both sides of transactions. For example, a farmer may be unable to sell sufficient produce at the entrance to their farm (_e.g._ due to limited passersby). Thus, the farmer may find it favorable to instead sell their produce at a local farmers' market alongside other farmers and many interested consumers.
{% endhint %}

{% hint style="info" %}
**Uncongested**

Thick markets can tend toward congestion, which can make it impossible for participants to assess the most promising choices available. Formally, a market is _uncongested_ if it provides enough time (and makes transactions fast enough) for market participants to consider enough alternative possible transactions to arrive at satisfactory ones. In other words, uncongested markets provide participants ample time for due diligence.
{% endhint %}

{% hint style="info" %}
**Tractable**

The Graph's permissionless markets are deployed on blockchains (_e.g._ Ethereum) in smart contracts. These contracts define computations and variables that must be updated to enable the market to operate. However, the execution of smart contracts is extremely expensive with respect to the computation and the mathematical operations available are often limited; for example, in Ethereum smart contract are written in the Solidity programming language, which uses unsigned integers. Thus, standard algorithms (_e.g._ sorting and matrix multiplication) can be prohibitively costly. For this reason, all aspects of the market must be with few variables and simple/cheap mathematical operations.
{% endhint %}

### Concrete Properties in The Graph

(Explain how the above properties are realized in The Graph.)

#### Simple

The tasks ought to aptly modeled by way of convex optimization. This can then be automated...

#### Uncongested

* Rank
* Rate
* Allocate

#### Thick

* permissionless - Anyone can participate on either side
* Gateway matching and pricing experiences are satisfactory for both developers and indexers
* Subgraphs are straightforward to create for dapps
* Indexing tools are standardized and accessible

#### Safe

* Folks are not worse off by participating truthfully (_**e.g.**_ no surprise “rugpulling” and no benefits to “free riding”)
* Folks obtain the optimal outcomes by acting truthfully (**i.e.** not “gaming the system”)







### References

