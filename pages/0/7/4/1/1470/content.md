
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#

* automatic table of contents goes here
{:toc}

## Idea

An **algebraic stack** is essentially a [[geometric stack]] on the [[étale site]]. 

Depending on details, this is a [[Deligne-Mumford stack]] or a more general [[Artin stack]] in the traditional setup of [[algebraic space]]s.

## Definition

An **algebraic stack** $X \in Sh_{(2,1)}(Et)$ is 

* a [[stack]] on the [[étale site]] $Et$ 

* such that 

  * $X$ has an [[atlas]] $A\to X$ from an [[algebraic space]] (or in a stronger version a [[scheme]]) which is  

    * surjective representable and [[étale morphism|étale]] (for a [[Deligne-Mumford stack]]);

    * surjective representable and [[smooth morphism|smooth]] (for an [[Artin stack]]).

  * the diagonal morphism $\Delta : X \to X \times_S X$ is a

    * [[representable morphism of stacks]], 
 
    * separated, 

    * quasi compact.

This appears for instance as ([Laumont, Moret-Bailly, def (4.1)](#LaumontMoret-Bailly)).

Here we used the following definition.  A map $f:X\to Y$ of 1-stacks on the &#233;tale site is a *[[representable morphism of stacks]]* if for any scheme $S$ the [[fiber product]] $S\times_Y X$ is a stack associated to a scheme. 

Let $P$ be a property stable under composition and pullback. A representable map $f:X\to Y$ of stacks is said to have a property $P$ if for any scheme $S$ and a morphism of 1-stacks $S\to Y$ the pullback $S\times_Y X\to X$ has property $P$.  


## Examples

[[orbifold|Orbifolds]] are an example of an Artin stack. For orbifolds the stabilizer groups are [[finite group]]s, while for Artin stacks in general they are [[algebraic group]]s. 


## Properties

* [[Tannaka duality for geometric stacks]].

## Generalizations

### Noncommutative spaces 

A noncommutative generalization for [[Q-category|Q-categories]] instead of [[Grothendieck topology|Grothendieck topologies]], hence applicable in noncommutative geometry of Deligne--Mumford and Artin stacks can be found in ([KontsevichRosenberg](#KontsevichRosenberg)).


## Examples

* [[projective stack]]

## Related concepts

* [[geometric stack]]

  * **algebraic stack**

  * [[topological stack]]

  * [[differentiable stack]]

* [[geometric ∞-stack]]

## References

A standard textbook reference is

* G. Laumon, L. Moret-Bailly, _Champs alg&#233;briques_ , Ergebn. der Mathematik und ihrer Grenzgebiete 39 , Springer-Verlag, Berlin, 2000
{#LaumontMoret-Bailly}

An account is given in [chapter 47](http://www.math.columbia.edu/algebraic_geometry/stacks-git/book.pdf#page=2103) of 

* [[Aise Johan de Jong]],  _[[The Stacks Project]]_ ([pdf](http://www.math.columbia.edu/algebraic_geometry/stacks-git/book.pdf)) ([project website](http://www.math.columbia.edu/algebraic_geometry/stacks-git/))


The noncommutative version is discussed in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative stacks_ , preprint MPIM2004-37 ([dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305) [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333))
{#KontsevichRosenberg}

[[!redirects algebraic stack]]
[[!redirects algebraic stacks]]
