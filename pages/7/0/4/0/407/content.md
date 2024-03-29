# The globe category
* table of contents
{: toc}

## Idea

The **globe category** $G$ encodes one of the main [[geometric shapes for higher structures]].  Its objects are the standard cellular $n$-[[globe|globes]], and presheaves on it are [[globular sets]].

It may also be called the [[globular category]], although that term has other interpretations.


## Definition

The **globe category** $G$ is
the category whose objects are the non-negative integers and
whose morphisms are generated from
$$
  \sigma_n : [n] \to [n+1]
$$
$$
  \tau_n : [n] \to [n+1]
$$
for all $n \in \mathbb{N}$ subject to the relations (dropping obvious subscripts)
$$
  \sigma\circ \sigma = \tau \circ \sigma
$$
$$
  \sigma\circ \tau = \tau \circ \tau
$$

### The reflexive globe category

If we add the generating morphisms
$$
  \iota_n : [n+1] \to [n]
$$
subject to the relations
$$
  \iota \circ \sigma = \mathrm{Id}
$$
$$
  \iota \circ \tau = \mathrm{Id}
  \,.
$$
we obtain the **reflexive globe category**.

## Remarks

* The globe category is used to define [[globular set|globular sets]].

* M. Roy has studied [[level of a topos|levels]] in the topos of [[globular set#ReflexiveGlobularSets|reflexive globular sets]] in the context of [[Bill Lawvere|F. W. Lawvere]]'s concept of [[Aufhebung]] (cf. [Kennett-Riehl-Roy-Zaks(2011)](#KRRZ11)).

## Related concepts

* [[globular set]]

* [[simplex category]]

* [[cube category]]

* [[cell category]]

## Reference

* {#KRRZ11} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no.5 (2011) pp.949-961. ([preprint](http://arxiv.org/abs/1003.5944))

category: category
