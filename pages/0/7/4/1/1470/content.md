
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Geometry
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

Let $C_{fppf}$ be the [[fppf-site]] and $\mathcal{E} = Sh_{(2,1)}(C_{fppf})$
the [[(2,1)-topos]] of [[stack]]s over it.


+-- {: .un_defn}
###### Definition

An **algebraic stack** is

* an object $\mathcal{X}\in Sh_{(2,1)}(C_{fppf})$;

* such that 

  1. the [[diagonal]] $\mathcal{X} \to \mathcal{X} \times \mathcal{X}$
  is [[representable morphism of stacks|representable]] by [[algebraic space]]s;

  1. there exists a [[scheme]] $U \in Sh(C_{fppf}) \hookrightarrow Sh_{(2,1)}(C_{fppf})$ and a morphism $U \to \mathcal{X}$ which is a surjective and
     [[smooth morphism of schemes|smooth morphism]]. 

=--

This appears in this form as ([deJong, def. 47.12.1](#deJong)).

+-- {: .un_defn}
###### Definition

A **smooth algebraic groupoid** is an [[internal groupoid]] in [[algebraic space]]s such that source and target maps are [[smooth morphism of schemes|smooth morphisms]].

=--

This appears as ([deJong, def. 47.16.2](#deJong)).

Notice that every [[internal groupoid]] in [[algebraic spaces]] represents a [[(2,1)-presheaf]] on the [[fppf-site]]. We shall not distinguish between the groupoid and the [[stackification]] of this presheaf, called the **quotient stack** of the groupoid.

+-- {: .un_theorem}
###### Theorem

Every algebraic stack is equivalent to a smooth algebraic groupoid and every smooth algebraic groupoid is an algebraic stack.

=--

This appears as ([deJong, lemma 47.16.2, theorem 47.17.3](#deJong)).



## Properties

* [[Tannaka duality for geometric stacks]].


## Examples

[[orbifold|Orbifolds]] are an example of an [[Artin stack]]. For orbifolds the stabilizer groups are [[finite group]]s, while for Artin stacks in general they are [[algebraic group]]s. 

## Generalizations

### Noncommutative spaces 

A noncommutative generalization for [[Q-category|Q-categories]] instead of [[Grothendieck topology|Grothendieck topologies]], hence applicable in noncommutative geometry of Deligne--Mumford and Artin stacks can be found in ([KontsevichRosenberg](#KontsevichRosenberg)).


## Examples

* [[projective stack]]

## Related concepts

* [[lisse-étale site]]

* [[geometric stack]]

  * **algebraic stack**

  * [[topological stack]]

  * [[differentiable stack]]

  * [[complex analytic stack]]

* [[geometric ∞-stack]]

## References

A standard textbook reference is

* G. Laumon, L. Moret-Bailly, _Champs alg&#233;briques_ , Ergebn. der Mathematik und ihrer Grenzgebiete 39 , Springer-Verlag, Berlin, 2000
{#LaumontMoret-Bailly}

An account is given in [chapter 47](http://www.math.columbia.edu/algebraic_geometry/stacks-git/book.pdf#page=2103) of 

* [[Aise Johan de Jong]],  _[[The Stacks Project]]_ ([pdf](http://www.math.columbia.edu/algebraic_geometry/stacks-git/book.pdf)) ([project website](http://www.math.columbia.edu/algebraic_geometry/stacks-git/))
{#deJong}

The noncommutative version is discussed in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative stacks_ , preprint MPIM2004-37 ([dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305) [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333))
{#KontsevichRosenberg}

[[!redirects algebraic stack]]
[[!redirects algebraic stacks]]
