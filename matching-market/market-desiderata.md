# Market Desiderata

### Introduction

This pages discusses properties that help markets operate "successfully." First high-level properties are covered, which are then expanded upon in the context of The Graph.

### Desiderata

> Each of these ubiquitous marketplaces has found a way to succeed not only in making markets thick, uncongested, and safe, but also in making them _simple to use_.\
> ****\
> ****-Alvin Roth

The essential properties of matching market are concisely summarized by Roth in the quote above. Below we these market properties and their interpretation. In addition to Roth's list, we strive for computationally efficiency as to obtain practical gas costs in blockchain environments.

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

### Implementation

The above properties are helpful for general-purpose descriptions. This section describes how each property is "measured" in The Graph. In each bulleted list, blue items are handled externally to the protocol (_i.e._ are not verifiable via on-chain transactions) whereas the other items are handled in the protocol (_i.e._ via smart contracts on Ethereum).

#### Simple

* UX experience on the studio is clean and intuitive
* Decision problems are aptly modeled via convex optimization / games
* Indexing tools are standardized and accessible
* Subgraphs are straightforward to create for dapps

#### Uncongested

The properties are presently understood to contribute to whether the market is congested.

* Possible to rank subgraphs in terms of expected indexer revenue per subgraph
* Possible to deduce typical rates indexers are paid to serve queries/index subgraphs
* <mark style="color:blue;">Possible to know if indexers are competing to index subgraph</mark>
* <mark style="color:blue;">Gateways are able to quickly process and route queries between developers and indexers</mark>.

Ranking of subgraphs is important for indexers to be able to easily identify which subgraphs are valuable (_i.e._ "follow the money"). Using statistics (_e.g._ dashboard compiling usage data), developers should be able to easily estimate typical costs for subgraphs. The particular costs to index their subgraph are (often) unknown, but typical ranges can be known for attracting a particular number of indexers (corresponding to a desired quality of service).&#x20;

We next consider factors that are external to the protocol. Indexers may not have time to make decisions about which subgraphs to allocate on if it is unclear whether other indexers have already started indexing efforts on the subgraph of interest. This matter is expected to be resolved by GraphCast, where indexers can broadcast their intent to index and sign communications with their ETH wallet. Lastly, the final item ought hold in order for indexers to be able to provide the quality of service (_e.g._ with respect to latency) desired by consumers.



#### Thick

* permissionless - Anyone can participate on either side
* stable - Matching and pricing experiences are satisfactory for both developers and indexers

#### Safe

* Folks are not worse off by participating truthfully (_**e.g.**_ no surprise “rugpulling” and no benefits to “free riding”)
* Folks obtain the optimal outcomes by acting truthfully (**i.e.** not “gaming the system”)







### References

