---
description: A brief overview of query components.
---

# Query Properties

(high level description of what sorts of queries are made - GraphQL, the kinds of things that can be queried for non-technical folks)



Queries in The Graph consist of three ingredients. Below we list these and some consequences.

{% hint style="info" %}
**Query Contents**

Each query has three components:

* Block hash
* GraphQL Query
* SubgraphID
{% endhint %}

First, the three properties uniquely identify an appropriate response (assuming determinism and well-formed query properties hold). Additionally, anyone can serve a query, but consumers (_e.g._ a gateway) make each request to a specific Indexer. The indexer serves the query and provides both the query response and an attestation. The attestation is used to verify faithful query service, which can be used to slash the indexer if the response is incorrect.&#x20;



Allocations identify which subgraphs the Indexer intends to serve queries for, and any Indexer can allocate to any subgraph.

