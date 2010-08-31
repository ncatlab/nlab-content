
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Freyd--Mitchell embedding theorem_ says that every [[abelian category]] is a [[full subcategory]] of a [[category of modules]] over some [[ring]] $R$ and that the embedding is an [[exact functor]].

## Details

First of all, it's easy to see that not every abelian category is equivalent to $R Mod$ for some ring $R$.  The reason is that $R Mod$ has all [[small category]] [[limits]] and [[colimits]].  The category of [[finitely generated module|finitely generated]] $R$-modules is an abelian category that lacks these properties.

However, we have

+-- {: .un_thm}
###### Mitchell's Embedding Theorem
Every small [[abelian category]] admits a [[full functor|full]], [[faithful functor|faithful]] and [[exact functor|exact]] functor to the category $R Mod$ for some ring $R$.
=--

+-- {: .proof}
###### Proof
This result can be found as Theorem 7.34 on page 150 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=176).  His terminology is a bit outdated, in that he calls an abelian category "fully abelian" if admits a full and faithful exact functor to a category of $R$-modules.  See also the [Wikipedia article](http://en.wikipedia.org/wiki/Mitchell%27s_embedding_theorem) for the idea of the proof.
=--


We can also characterize which abelian categories _are_ equivalent to a category of $R$-modules:

+-- {: .un_thm}
###### Theorem
Let $C$ be an abelian category.  If $C$ has all [[small category|small]] [[coproducts]] and has a [[compact object|compact]] [[projective object|projective]] [[generator]], then $C \simeq R Mod$ for some ring $R$.  In fact, in this situation we can take $R = C(x,x)^{op}$ where $x$ is any compact projective generator.   Conversely, if $C \simeq R Mod$, then $C$ has all small coproducts and $x = R$ is a compact projective generator.
=--

+-- {: .proof}
###### Proof
This theorem, minus the explicit description of $R$, can be found as Exercise F on page 103 of Peter Freyd's book [Abelian Categories](http://www.emis.de/journals/TAC/reprints/articles/3/tr3.pdf#page=132).
The first part of this theorem can also be found as Prop. 2.1.7. of Victor Ginzburg's [Lectures on noncommutative geometry](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=4).  Conversely, it is easy to see that $R$ is a compact projective generator of $R Mod$. 
=--

Going further, we can try to characterize functors between categories of $R$-modules that come from tensoring with bimodules.  Here we have

+-- {: .un_thm}
###### Watts' Theorem
If $B$ is an an $S$-$R$-bimodule, the functor

$$ B \otimes_R -\colon R Mod \to S Mod $$

is [[right exact functor|right exact]] and preserves [[small category|small]] [[coproducts]].  Conversely, if $F\colon Mod_R \to Mod_S$ is right exact and that preserves small coproducts, it is naturally isomorphic to $B \otimes_R -$ where $B$ is the $S$-$R$-bimodule $F R$.  
=--

+-- {: .proof}
###### Proof
This theorem was more or less simultaneously proved by Watts and Eilenberg; a generalization is proved in A. Nyman and S. Paul Smith's paper [A generalization of Watts's Theorem: Right exact functors on module categories](http://arxiv.org/abs/0806.0832), and references to the original papers can be found there.
=--

Going still further we should be able to obtain a nice theorem describing the image of the embedding of the weak 2-category of

* rings
* bimodules
* bimodule homomorphisms

into the strict 2-category of 

* abelian categories
* right exact functors
* natural transformations.

For more discussion see the [$n$-Cafe](http://golem.ph.utexas.edu/category/2007/08/questions_about_modules.html).


## References

Apart from the above references...

...an introductory survey is for instance also in section 3 of 

* Geillan Aly, _Abelian Categories and the Freyd-Mitchell Embedding Theorem_ ([pdf](http://math.arizona.edu/~galy/research/ab_categories.pdf))


[[!redirects Freyd-Mitchell embedding theorem]]
[[!redirects Freyd–Mitchell embedding theorem]]
[[!redirects Freyd--Mitchell embedding theorem]]
[[!redirects Freyd-Mitchell embedding]]
[[!redirects Freyd–Mitchell embedding]]
[[!redirects Freyd--Mitchell embedding]]
[[!redirects Freyd-Mitchell theorem]]
[[!redirects Freyd–Mitchell theorem]]
[[!redirects Freyd--Mitchell theorem]]

[[!redirects Mitchell theorem]]
[[!redirects Mitchell's theorem]]
[[!redirects Mitchell's theorem]]
