
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _stable model category_ is a 1-[[category]] structure used to present a [[stable (∞,1)-category]] in analogy to how a general [[model category]] encodes a general [[(∞,1)-category]].

## Defintion

A **stable model category** $C$ is

* a [[pointed category|pointed]]

* [[model category]]

* such that the [[loop space object]] functor $\Omega$ and the suspension functor $\Sigma$, are inverse [[equivalence of categories|equivalences]] on the [[homotopy category]] $Ho(C)$:

  $$ \Omega : Ho(C) \stackrel{\leftarrow^\simeq}{\to^\simeq} : 
   Ho(C) : \Sigma
  $$

## Properties


**Proposition**

Let $C$ be a _stable model category_ that is in addition

* a [[simplicial model category]];

* a [[cofibrantly generated model category]];

* a [[proper model category]];

* with a [[set]] $S$ of [[compact object|compact]] generators;

then there is a chain of [[SSet]] [[Quillen equivalence]]s 
linking $C$ to the the [[spectrum]]-[[enriched functor category]] 

$$
  C \simeq Sp Cat(\mathcal{E}(S), Sp)
$$

equipped with the [[global model structure on functors]],
where $\mathcal{E}(S)$ is the $Sp$-[[enriched category]] given by...
  
This is theorem 3.3.3 in [ClassStabMod](http://hopf.math.purdue.edu/Schwede-Shipley/class.final.pdf).


**Remark** Notice the similarity (but superficial difference: $SSet$/$Sp$-enrichment localization/no-localization) to the **stable Giraud theorem** discussed at [[stable (∞,1)-category]].


## References

* [[Stefan Schwede]], [[Brooke Shipley]], _Classification of stable model categories_ ([pdf](http://hopf.math.purdue.edu/Schwede-Shipley/class.final.pdf))
