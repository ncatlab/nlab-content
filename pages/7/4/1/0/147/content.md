#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

The structure of a _site_ on a [[category]] $C$ is a structure that regards each [[object]] $c$ of $C$ as a [[space and quantity|space]] and determines which [[morphisms]] $\pi : d \to c$ from collections $d := \{\sqcup_i d_i\}$ of [[objects]] of $C$ to $c$ behave as [[cover|covers]] of spaces.

One says a site is a [[category]] equipped with a [[topology]], called a [[Grothendieck topology]]. The structure of a site on a category allows to characterize those [[presheaf|presheaves]] on the category which are "continuous" with respect to this topology in that they send covering morphisms to [[equivalences]]. 

Such presheaves are [[sheaf|sheaves]]. Or, in [[higher category theory|higher categorical contexts]], [[stacks]], and further [[∞-stacks]].

## Definition ##

+-- {: .un_defn}
###### Definition
A _site_ is a category $C$ equipped with a [[Grothendieck topology]] $J$.
=--

##Remarks##

* Sometimes it is useful to define a site to be a category equipped merely with a [[coverage]].

* Notice also that there are many equivalent ways to define a [[Grothendieck topology]], for instance in terms of a system of [[local isomorphisms]], or in terms of a system of [[dense monomorphisms]] in the [[presheaf]] category $PSh(S)$.

## Examples ##

* The archetypical class of examples is the [[category of open subsets]] $S = Op(X)$ of a [[topological space]] $X$. Notice that a morphism $f : X \to Y$ of topological spaces induces naturally a [[functor]] $f^t : Op(Y) \to Op(X)$ going the other way around, sending an open subset $U \in Y$ to the open subset $f^{-1}(U)$ in $X$.




## Definition: morphisms of sites ##

Motivated from the archetypical example of [[category of open subsets|categories of open subsets]], one says that 

* a **presite** is the same as a [[category]] $S$;

* a **morphism of presites** $S \to S'$ is a [[functor]] going the other way round, $S' \to S$. 

Hence the **category of presites** is just the [[opposite category]] of the category [[Cat]] of categoris, 

$$
  PSit := Cat^{op}
  \,.
$$

This is just terminology, but supposedly suggestive for working with presheaf categories. For instance one would denote a presite by $X$ and the same entity regarded as a category as $S_X$ and write

$$
  PSh(X) := [S_X^{op}, Set]
$$

and thus have notation entirely analogous to the familiar notation for presheaves on a topological space $X$.


In this notation a **site** $X$ is a pair consisting of a category $S_X$ and a [[coverage]] on $S_X$. 

Then a **morphism of sites** $f : X \to Y$ is

* a [[functor]] $f^t : S_Y \to S_X$

* such that the [[Yoneda extension]] $\hat f^t : [S_Y^\op, Set] \to [S_X^{op}, Set]$ (of $Y_X \circ f^t : S_Y \to [S_X^{op}, Set]$) sends [[local isomorphisms]] to local isomorphisms.


**Proposition**

A morphism of sites $f : X \to Y$ as above induces a morphism of [[category of sheaves|categories of sheaves]] $Sh(X) \to Sh(Y)$ and this morphism is a [[geometric morphism]] of [[topos|topoi]].


### Sub-sites ###

Moreover, for $X$ a presite and $U \in S_X$ an object in the corresponding category, the [[comma category]] $(Y_{S_X} / U)$ is naturally regarded as the presite defined by $U$, which by convenient abuse of notation one would just write $U$ itself, so that $S_U = S_X \downarrow U$. 

For instance for $X$ a topological space and $U \in Op(X)$ an open subset, $U$ regarded as a topological space in its own right has corresponding to it the site $U$ with $S_U = Op(U) = Op(X) \downarrow U$.

The [[stuff, structure, property|forgetful]] [[functor]]
$$
  j^t_{U \to X} : (S_U = (Y_{S_X} / U)) \to S_X
$$
therefore constitutes a canonical morphism of pre-sites
$$
  j_{U \to X} : X \to U  
  \,.
$$
This induces a [[Grothendieck topology]] on the site $U$ whose [[local epimorphisms]] $(Y \to U) \in [S_U^{op}, Set]$ are precisely those morphisms for which
$$
  \hat j^t_{U \to X}(Y \to U)
  \in 
  [S_X^{op}, Set]
$$
is a [[local epimorphism]].

There are natural operations for [[restriction and extension of sheaves]] from a sub-site $U$ to $X$ and back.


### Direct and inverse image ###

So for $f : X \to Y$ a morphisms of sites, coming from a functor $f^t : S_Y \to S_X$, the [[direct image]] functor is the functor may be denoted
$$
  f_* : Sh(X) \to Sh(Y)
$$
and the [[inverse image]] functor 
$$
  f^{-1} : Sh(Y) \to Sh(X)
  \,.
$$




## References ##

Morphisms between sites are discussed for instance

in section 17.2 of 

* Kashiwara-Schapira, [[Categories and Sheaves]]

(in terms of [[local isomorphisms]])

as well as in section VII. 10 of

* [[Saunders MacLane]] [[Ieke Moerdijk]], [[Sheaves in Geometry and Logic]] 

(in terms of covering [[sieves]]), where also the relation to [[geometric morphisms]] is discussed.

[[!redirects sites]]