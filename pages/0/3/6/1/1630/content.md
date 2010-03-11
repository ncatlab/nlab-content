<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Definition

The **$\omega$-nerve** functor

$$
  N : \omega Cat \to sSet
$$

$$
  C \mapsto N(C)
$$

from [[∞-categories]] to [[simplicial sets]] is the functor induced by the general logic of [[nerve and realization]] from the [[orientals]]: the [[cosimplicial object|cosimplicial]] $\omega$-category

$$
  O : \Delta \to \omega Cat
  \,.
$$

So for $C$ an $\omega$-category, its $\omega$-nerve is the [[simplicial set]] whose $k$-[[simplex|simplices]] are precisely all possible images of the $k$-[[oriental]] in $C$:

$$
  N(C)_k := \omega Cat(O[k], C)
  \,.
$$

Where the $\omega$-category itself provided rules for how exactly to compose [[k-morphism]]s, its $\omega$-nerve just records all possible ways of how $(k+1)$-morphisms connect pasting diagrams of $k$-morphisms in $C$. This is however precisely the same information.

## Characterization of $\omega$-categories by their $\omega$-nerves

Accordingly, omega-nerves may be used to _define_ and identify $\omega$-categories. For instance

* the $\omega$-nerve $N(C)$ is a simplicial set in wich _all_  [[horn]]s have _unique_ fillers precisely if $C$ is a 1-[[groupoid]];

* the $\omega$-nerve $N(C)$ is a simplicial set in wich all _inner_ [[horn]]s have _unique_ fillers precisely if $C$ is an ordinary [[category]];

* the $\omega$-nerve $N(C)$ is a simplicial set in wich _all_ [[horn]]s have any fillers precisely if $C$ is an [[∞-groupoid]] (see [[Kan complex]] for more on this);

* the $\omega$-nerve $N(C)$ is a simplicial set in wich all _inner_ [[horn]]s have any fillers precisely if $C$ is an [[(∞,1)-category]].

* in full generality, a simplicial set is the $\omega$-nerve of an $\omega$-category if it is a [[weak complicial set]].


[[!redirects omega-nerves]]
[[!redirects ∞-nerve]]
[[!redirects ∞-nerves]]