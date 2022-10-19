# Market Desiderata

> Each of these ubiquitous marketplaces has found a way to succeed not only in making markets thick, uncongested, and safe, but also in making them simple to use.\
> ****\
> ****-Alvin Roth

### Desiderata

The core properties for a market are concisely summarized by Roth in the quote above. Below we overview relevant market properties and their interpretation in our context. In addition to Roth's list, note we strive for computationally efficiency in order to obtain practical gas costs in blockchain environments.

{% hint style="info" %}
**Safe**\
****The single most important aspect of marketplace design is safety. Here this is measured in two respects. The first is participants can reveal their true preferences, without running a risk that by doing so they will receive a worse outcome than if they had behaved strategically and stated some other preferences (_e.g._ consider high school matching, matching for medical residencies, and auctions). Since curation markets have optional participation, we must also ensure folks are not worse off by truthful participation. These two properties are, respectively, called dominant strategy incentive compatible (DSIC) and individual rationality (IR).&#x20;
{% endhint %}

{% hint style="info" %}
**Simple**

We consider simplicity along two dimensions: actions and their consequences are simple to understand (low cognitive overhead) and tasks are simple to perform (efficient workflows). As Roth concisely notes, "`being easy to describe isn't the same as being easy to navigate." In fact, markets may use complex algorithms` under the hood'' to execute transactions for simple strategies. This is the case for various matching markets (_e.g._ medical residencies).
{% endhint %}

{% hint style="info" %}
**Uncongested**

****
{% endhint %}

{% hint style="info" %}
**Thick**

****
{% endhint %}

{% hint style="info" %}
**Tractable**

****
{% endhint %}

### References

