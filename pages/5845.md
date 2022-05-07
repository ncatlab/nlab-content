
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

> This entry is about the notion of _adjoint triple_ involving three functors. This is not to be confused with the notion of [[adjoint monads]], which were also sometimes called adjoint triples, with "triple" then being a synonym for "monad". However, an adjoint triple in the sense here does induce an [[adjoint monad]]!

#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn #Defn}
###### Definition

An __adjoint triple__ (of [[functors]] between [[categories]] or generally of [[1-morphisms]] in a [[2-category]])

$$
  (F \dashv G \dashv H) \colon C \to D 
$$

is a [[triple]] of [[functors]]/morphisms $F,H \colon C \to D$ and $G \colon D \to C$ together with [[adjunction]] data $F\dashv G$ and $G\dashv H$.   That is, it is an [[adjoint string]] of length 3.

=--

+-- {: .num_prop #AsAdjunctionOfAdjunctions}
###### Proposition

An adjoint triple $(F\dashv G\dashv H)$, def. \ref{Defn} is equivalently an [[adjoint pair]] in the 2-category whose morphisms are adjoint pairs in the original 2-category, hence an adjunction of adjunctions

$$
  (F \dashv G) \dashv (G \dashv H)
  \,.
$$

=--

This fact plays an important role in [Licata--Shulman, 5.1](#LicataShulman).  Relatedly, it also appears in the characterization of certain kinds of [[geometric morphism]] (e.g. the [[local geometric morphism|local]] ones) in terms of adjunctions in the 2-category [[Topos]].

It may be suggestive to denote this like so

$$
  \array{
     F &\dashv& G
     \\
     \bot && \bot
     \\
     G &\dashv& H
  }
$$

such that the two adjoint pairs appear horizontally, while the second order adjunction between them runs vertically.

## Properties
 {#Properties}

+-- {: .num_note #GIsBicontinuous}
###### Note

The two adjunctions imply of course that $G$ preserves all [[limit]]s and [[colimit]]s that exist in $D$.

=--

+-- {: .num_note #AdjointPairFromAdjointTriple}
###### Note


Every adjoint triple 

$$
  (F \dashv G \dashv H) \colon C \to D
$$ 

gives rise to an [[adjunction|adjoint pair]] 

$$
  (G F \dashv G H) \colon C \to C
$$ 

consisting of the [[monad]] $G F$ [[left adjoint]] to the [[comonad]] $G H$ on $C$;
as well as to an adjoint pair

$$
   (F G \dashv H G) \colon D \to D
$$

consisting of the comonad $F G$ left adjoint to the monad $H G$ on $D$.

=--

See [[adjoint monad]] for more.

In general there is a duality (an [[dual equivalence|antiequivalence of categories]]) between the categories of monads having right adjoints and of comonads having left adjoints.  Note also that the [[algebra over a monad|algebras]] for a left-adjoint monad can be identified with the coalgebras for its right-adjoint comonad. ([SGL, Theorems V.8.1 and V.8.2](#SGL))

### Fully faithful adjoint triples
 {#FullyFaithFulAdjointTriples}

+-- {: .num_prop #FullyFaithful}
###### Proposition

For an adjoint triple $F\dashv G\dashv H$ we have that $F$ is [[full and faithful functor|fully faithful]] precisely if $H$ is fully faithful. 

=--

+-- {: .proof}
###### Proof

By a basic [[adjoint functor#FullyFaithfulAndInvertibleAdjoints|property]] of [[adjoint functor]]s, we have that 

* the [[left adjoint]] $F$ being full and faithful is equivalent to the [[unit of an adjunction|unit]] $Id \to G F$ being a [[natural isomorphism]];

* the [[right adjoint]] $H$ being full and faithful is equivalent to the counit $G H \to Id$ being a [[natural isomorphism]].

Moreover, by Note \ref{AdjointPairFromAdjointTriple} and the fact that adjoints are unique up to isomorphism, we have that $G F$ is isomorphic to the identity precisely if $G H$ is. 

Finally, by a standard fact about [[adjoint functor]]s (see for instance ([Elephant, Lemma A1.1.1](#Elephant))), we have that $G H$ is isomorphic to the identity precisely if it is so by the [[unit of an adjunction|counit]].

=--

The preceeding proposition is [[folklore]]; perhaps its earliest appearance in print is ([DT, Lemma 1.3](#DyckhoffTholen)).  A slightly shorter proof is in ([KL, Prop. 2.3](#KellyLawvere)).  Both proofs explicitly exhibit an inverse to the counit $G H \to Id$ or the unit $Id \to G F$ given an inverse to the other (which could be extracted by [[beta-reduction|beta-reducing]] the above, slightly more abstract argument). It also appears in ([SGL, Lemma 7.4.1](#SGL)).

In the situation of Proposition \ref{FullyFaithful}, we say that $F\dashv G \dashv H$ is a **fully faithful adjoint triple**.  This is often the case when $D$ is a category of "spaces" structured over $C$, where $F$ and $H$ construct "discrete" and "codiscrete" spaces respectively.

For instance, if $G\colon D\to C$ is a [[topological concrete category]], then it has both a left and right adjoint which are fully faithful.  Not every fully faithful adjoint triple is a topological concrete category (among other things, $G$ need not be [[faithful functor|faithful]]), but they do exhibit certain similar phenomena.  In particular, we have the following.

+-- {: .num_prop #FinalLifts}
###### Proposition
Suppose $(F \dashv G \dashv H) \colon C \to D$ is an adjoint triple in which $F$ and $H$ are fully faithful, and suppose that $C$ is [[cocomplete category|cocomplete]].  Then $G$ admits [[final lift|final lifts]] for [[small category|small]] $G$-structured [[sinks]].
=--
+-- {: .proof}
###### Proof
Let $\{G(S_i) \to X\}$ be a small sink in $C$, and consider the diagram in $D$ consisting of all the $S_i$, all the counits $\varepsilon\colon F G(S_i) \to S_i$ (where $F$ is the left adjoint of $G$), and all the images $F G(S_i) \to F(X)$ of the morphisms making up the sink.  The colimit of this diagram is preserved by $G$ (since it has a right adjoint as well).  But the image of the diagram consists essentially of just the sink itself (since $F$ is fully faithful, $G(\varepsilon)$ is an isomorphism), and its colimit is $X$; hence the colimit of the original diagram is a lifting of $X$ to $D$ (up to isomorphism).  It is easy to verify that this lifting has the correct universal property.
=--

Thus, we can talk about objects of $D$ having the [[weak structure]] or [[strong structure]] induced by any small collection of maps.

+-- {: .num_cor #Fibration}
###### Corollary
In the situation of Proposition \ref{FinalLifts}, $G$ is a ([[Street fibration|Street]]) [[Grothendieck fibration|opfibration]].  If it is also an [[isofibration]], then it is a Grothendieck opfibration.
=--
+-- {: .proof}
###### Proof
A final lift of a singleton sink is precisely an opcartesian arrow.
=--

Dually, of course, if $C$ is complete, then $G$ admits initial lifts for small $G$-structured cosinks and is a fibration.

In particular, the proposition and its corollary apply to a [[cohesive topos]], and (suitably categorified) to a [[cohesive (∞,1)-topos]].

### Idempotent adjoint triples

+-- {: .num_prop #Idempotent}
###### Proposition
For an adjoint triple $F\dashv G\dashv H$, the adjunction $F\dashv G$ is an [[idempotent adjunction]] if and only if the adjunction $G\dashv H$ is so.
=--
+-- {: .proof}
###### Proof
The monad $G F$ is left adjoint to the comonad $H G$, with the structure maps being [[mates]].  Therefore, by a standard fact, the category of $G F$-algebras and the category of $H G$-coalgebras are isomorphic over their common base.  However, $F\dashv G$ is idempotent precisely when $G F$ is an [[idempotent monad]], hence precisely when the forgetful functor of the category of $G F$-algebras is fully faithful, and dually for $G\dashv H$.  Since the categories of algebras are isomorphic respecting their forgetful functors, one forgetful functor is fully faithful if and only if the other is.
=--


## Examples

### Special cases

* If one of the two [[adjoint pairs]] induced from an adjoint triple involving identities, then the other exhibits an _[[adjoint cylinder]]_ / _[[unity of opposites]]_.

* An adjoint triple $F\dashv G\dashv H$ is **Frobenius** if $F$ is naturally isomorphic to $H$. See [[Frobenius functor]].

* An *[[affine morphism]]* is an adjoint triple of functors in which the middle term is [[conservative functor|conservative]]. For example, any [[affine morphism of schemes]] induce an affine triples of functors among the categories of [[quasicoherent module]]s.

* An adjoint triple of functors among $A_\infty$- or [[triangulated functor]]s with certain additional structure is called **spherical** . See e.g. ([Anno](#Anno)). The main examples come from [[Serre functor]]s in a [[Calabi-Yau category]] context. 

* A context of [[six operations]] $(f_! \dashv f^!)$, $(f^\ast \dashv f_\ast)$ induces an adjoint triple when either $f^! \simeq f^\ast$ or $f_! = f_\ast$. This is called a  _[[Wirthmüller context]]_ or a  _[[Grothendieck context]]_, respectively.


### Specific examples

* Given any [[ring]] [[homomorphism]] $f^\circ: R\to S$ (in commutative case dual to an [[affine morphism]] $f: Spec S\to Spec R$ of [[affine schemes]]), there is an adjoint triple $f^!\dashv f_*\dashv f^*$ where $f^*: {}_R Mod\to {}_S Mod$ is an [[extension of scalars]], $f_*: {}_S Mod\to {}_R Mod$ the restriction of scalars and $f^! : M\mapsto Hom_R ({}_R S, {}_R M)$ its [[coextension of scalars|right adjoint]]. This triple is affine in the above sense.

* If $T$ is a [[lax-idempotent 2-monad]], then a $T$-algebra $A$ has an adjunction $a : T A \rightleftarrows A : \eta_A$.  If this extends to an adjoint triple with a further left adjoint to $a$, then $A$ is called a [[continuous algebra]].


## Related concepts

* [[adjoint quadruple]], [[adjoint string]]

* [[cohesive topos]]

* [[ambidextrous adjunction]]

* [[affine morphism]], [[affine localization]] 

* [[Quillen adjoint triple]]

## References

Some remarks on adjoint triples are in

* {#Johnstone} [[Peter Johnstone]], _Remarks on punctual local connectedness_, [tac/25-03](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html).


The [[modal type theory]] of adjoint triples is discussed in

* {#LicataShulman} [[Dan Licata]] and [[Mike Shulman]], _Adjoint logic with a 2-category of modes_ ([pdf](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint.pdf)).


On spherical triples see

* {#Anno} Rina Anno, _Spherical functors_, [arxiv/0711.4409](https://arxiv.org/abs/0711.4409).


Generalities are in

* {#Elephant} [[Peter Johnstone]], _[[Sketches of an Elephant]]_.


Proofs of the folklore Proposition \ref{FullyFaithful} can be found in

* {#DyckhoffTholen} Roy Dyckhoff and [[Walter Tholen]], "Exponentiable morphisms, partial products, and pullback complements", JPAA 49 (1987), 103--116.

* {#KellyLawvere} [[G.M. Kelly]] and [[F.W. Lawvere]], "On the complete lattice of essential localizations", Bulletin de la Soci&#233;t&#233; Math&#233;matique de Belgique, S&#233;rie A, v. 41 no 2 (1989) 289--319.

* {#SGL} [[Saunders Mac Lane]] and [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic|Sheaves in Geometry and Logic --- A First Introduction to Topos Theory]]_, Springer (1992), [doi](https://dx.doi.org/10.1007/978-1-4612-0927-0).


Several lemmas concerning adjoint pairs and adjoint triples are included in

* [[Alexander Rosenberg]], _Noncommutative schemes_, Compos. Math. __112__ (1998) 93--125, [doi](https://dx.doi.org/10.1023/A:1000479824211)

together with geometric consequences. Note a somewhat nonstandard usage of terminology continuous functor (also flatness in the paper includes having right adjoint).

[[!redirects adjoint triples]]
[[!redirects fully faithful adjoint triple]]
[[!redirects fully faithful adjoint triples]]
[[!redirects adjunction of adjunctions]]
[[!redirects adjunction between adjunctions]]