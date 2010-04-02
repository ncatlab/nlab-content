<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>


This entry is about the general properties and characterization of [[(∞,1)-categories]] of [[(∞,1)-sheaves]] -- also known as [[∞-stack]] [[(∞,1)-topos]]es.

The 1-categorical analog of the discussion is this entry is at [[category of sheaves]].

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For any [[(∞,1)-category]] $C$ every [[(∞,1)-functor]] $\bar {(-)} : C \to D$ which admits a [[(infinity,1)-fully faithful functor|fully faithful]] [[adjoint (infinity,1)-functor|right adjoint]] -- equivalently every [[(∞,1)-functor]] $L : C \to C$ which is 
[[adjoint (infinity,1)-functor|left adjoint]] to the inclusion $L C \hookrightarrow C$ of its [[essential image|essential image]] $L C$ into $C$ -- is a [[localization of an (∞,1)-category]] onto a [[reflective (∞,1)-subcategory]] characterized by the collection $W$ of [[morphisms]] which it sends to [[(infinity,1)-equivalence|equivalences]]. One can think of it 

* as _inverting_ these morphisms;

* as projecting onto those objects of $C$ which are [[local object|local]] with respect to these morphsims: those objects which sees $W$ as a collection of equivalences.

Using the familiar characterization of the [[category of sheaves]] in the 1-categorical context, this straightforwardly suggests to characterize 
_$(\infinity,1)$-categories $Sh(S)$ of $(\infty,1)$-sheaves_ -- also called (Grothendieck-Rezk-Lurie) [[(∞,1)-topoi]] as essential images of [[exact (infinity,1)-functor|left exact]] $(\infty,1)$-functors from [[(infinity,1)-category of (infinity,1)-functors|(∞,1)-categories of (∞,1)-presheaves]]

$$
 \bar{(-)} : PSh(S) \to Sh(S)
$$ 

(called [[∞-stackification]], analogous to [[sheafification]])

that have a 
[[(infinity,1)-fully faithful functor|fully faithful]] [[adjoint (infinity,1)-functor|right adjoint]] [[stuff, structure, property|forgetful]] functor

$$
  Sh(S) \hookrightarrow PSh(S)
  \,.
$$


## Definition

In the strict sense of the word, an [[(∞,1)-category]] of **$(\infty,1)$-sheaves** is a [[topological localization]] of an [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\incfty,1)}(C)$ on some small [[(∞,1)-category]] $C$

$$
  Sh_{(\infty,1)}(C) \hookrightarrow PSh_{(\infty,1)}(C)
  \,.
$$

Notice that by the facts recalled there, every such topological localization corresponds uniquely, up to equivalence, to a choice of [[Grothendieck topology]] on $C$: the objects of $Sh_{(\infty,1)}(C)$ are those $(\infty,1)$-presheaves that satisfy [[descent]] with respect to [[Cech cover]]s of covering [[sieve]]s.

Often such $(\infty,1)$-sheaves are called **[[∞-stack]]**s. The counting is

* [[sheaf]] = 0-stack

* (2,1)-sheaf = [[stack]]

* (3,1)-sheaf = 2-stack

* etc

* $(\infty,1)$-sheaf = [[∞-stack]].

Notice also that [[topological localization]]s are usually not [[hypercomplete (∞,1)-topos]]es. With slight abouse of language, the objects of the [[hypercompletion]] may still be called "$\infty$-stack"s around here.


## Models 


The topological localizations of an [[(∞,1)-category of (∞,1)-presheaves]] are [[presentable (∞,1)-category|presented]] by the [[Bousfield localization of model categories|left Bousfield localization]] of the global [[model structure on simplicial presheaves]] at the set of [[Cech cover]]s.

The [[hypercompletion|hypercomplete]] $(\infty,1)$-sheaf toposes are [[presentable (infinity,1)-category|presented]] by the local Joyal-Jardine [[model structure on simplicial presheaves]]. 

Detailed discussion of this [[model category]] presentation is at 

* [[models for infinity-stack (infinity,1)-toposes|models for (infinity,1)-category of (infinity,1)-sheaves]] .

## References

The study of simplicial presheaves apparently goes back to 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

which considers locally [[Kan complex|Kan]] [[simplicial presheaf|simplicial presheaves]] as a [[category of fibrant objects]].

This was later conceived in terms of a [[model structure on simplicial presheaves]] and on simplicial sheaves by Joyal and Jardine. To&#235; summarizes the situation and emphasizes the interpretation in terms of [[∞-stacks]] living in $(\infty,1)$-categories for instance in

B. To&euml;n, _Higher and derived stacks: a global overview_   ([arXiv](http://arxiv.org/abs/math/0604504)) .

The full picture in terms of Grothendieck-$(\infty,1)$-topoi of $(\infty,1)$-sheaves is the topic of

J. Lurie, [[Higher Topos Theory]].

* localization $(\infty,1)$-functors ($(\infty,1)$-sheafification for the present purpose) are discussed in section 5.2.7;

* local objects ($(\infty,1)$-sheaves for the present purpose) and [[local isomorphism]]s are discussed in section 5.5.4;

* the definition of $(\infty,1)$-topoi of $(\infty,1)$-sheaves is then definition 6.1.0.4 in section 6.1;

* the characterization of $(\infty,1)$-sheaves in terms of [[descent|descent and codescent]] is in section 6.1.3 

* the relation between the [[model structure on simplicial presheaves|Brown?Joyal?Jardine model]] and the general story is discussed at length in section 6.5.4


[[!redirects (infinity,1)-category of (infinity,1)-sheaves]]
[[!redirects (∞,1)-category of (∞,1)-sheaves]]
[[!redirects (infinity,1)-categories of (infinity,1)-sheaves]]
[[!redirects (∞,1)-categories of (∞,1)-sheaves]]
