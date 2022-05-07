
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea ##


What is called _topological_ [[K-theory]] is a collection of  [[generalized (Eilenberg-Steenrod) cohomology]] theories whose cocycles in degree 0 on a [[topological space]] $X$ may be represented by pairs of [[vector bundles]], real or complex ones, on $X$ modulo a certain equivalence relation.

The following is the quick idea. For a detailed introduction see _[[Introduction to Topological K-Theory]]_.

First, recall that for $k$ a [[field]] then a $k$-[[vector bundle]] over a [[topological space]] $X$ is a map $V \to X$ whose [[fibers]] are [[vector spaces]] which vary over $X$ in a controlled way. Explicitly this means that there exits an [[open cover]] $\{U_i \to X\}$ of $X$, a [[natural number]] $n \in \mathbb{N}$ (the _[[rank of a vector bundle|rank]]_ of the vector bundle) and a [[homeomorphism]] $U_i \times k^n \to V|_{U_i}$ over $U_i$ which is fiberwise a $k$-[[linear map]].

Vector bundles are of central interest in large parts of [[mathematics]] and [[physics]], for instance in [[Chern-Weil theory]] and [[cobordism theory]]. But the collection $Vect(X)_{/\sim}$ of [[isomorphism classes]] of vector bundles over a given space is in general hard to analyze. One reason for this is that these are classified in degree-1 _[[nonabelian cohomology]]_ with [[coefficients]] in the ([[nonabelian group|nonabelian]]) [[general linear group]] $GL(n,k)$. K-theory may roughly be thought of as the result of forcing vector bundles to be classified by an abelian [[cohomology theory]].

To that end, observe that all natural operations on [[vector spaces]] generalize to vector bundles by applying them [[fiber]]-wise. Notably there is the fiberwise [[direct sum of vector bundles]], also called the _[[nLab:Whitney sum]]_ operation. This operation gives the set $Vect(X)_{/\sim}$ of [[nLab:isomorphism classes]] of vector bundles the structure of an [[semi-group]] ([[monoid]]) $(Vect(X)_{/\sim},\oplus)$.

Now as under direct sum the [[nLab:dimension]] of vector spaces adds, similarly under [[nLab:direct sum of vector bundles]] their [[nLab:rank]] adds.  Hence in analogy to how one passes from the  additive [[semi-group]] ([[monoid]]) of  [[natural numbers]] to the addtitive [[group]] of [[integers]] by adjoining formal additive inverses, so one may adjoin formal additive inverses to $(Vect(X)_{/\sim},\oplus)$. By a general prescription ("[[Grothendieck group of a commutative monoid]]") this is achieved by first passing to the larger class of [[pairs]] $(V_+,V_-)$ of vector bundles ("[[virtual vector bundles]]"), and then [[quotient|quotienting]] out the [[equivalence relation]] given by

$$
  (V_+, V_-) \sim (V_+ \oplus W , V_- \oplus W)
$$

for all $W \in Vect(X)_{/\sim}$. The resulting set of [[equivalence classes]] is an [[abelian group]] with group operation given on representatives by

$$
  [V_+, V_-] \oplus [V'_+, V'_-] \coloneqq (V_+ \oplus V'_+, V_- \oplus V'_-)
$$

and with the [[inverse]] of $[V_+,V_-]$ given by

$$
  -[V_+, V_-] = [V_-, V_+]
  \,.
$$

This [[abelian group]] obtained from $(Vect(X)_{/\sim}, \oplus)$ is denoted $K(X)$ and often called _the K-theory_ of the space $X$. Here the letter "K" (due to [[Alexander Grothendieck]]) originates as a shorthand for the German word _Klasse_, referring to the above process of forming [[equivalence classes]] of ([[isomorphism classes]] of) vector bundles.

This simple construction turns out to yield remarkably useful groups of [[homotopy]] [[invariants]].
A variety of deep facts in [[algebraic topology]] have fairly elementary proofs in terms of topological K-theory, for instance the [[Hopf invariant one]] problem ([Adams-Atiyah 66](#AdamsAtiyah66)).

One defines the "higher" K-groups of a topological space to be those of its higher [[reduced suspensions]]

$$
  K^{-n}(X) = K(\Sigma^n X)
  \,.
$$

The assignment $X \mapsto K^\bullet(X)$ turns out to share many properties of the assignment of [[ordinary cohomology]] groups $X \mapsto H^n(X,\mathbb{Z})$. One says that topological K-theory is a [[generalized (Eilenberg-Steenrod) cohomology]] theory. As such it is [[Brown representability theorem|represented]] by a [[spectrum]]. For $k = \mathbb{C}$ this is called [[KU]], for $k = \mathbb{R}$ this is called [[KO]]. (There is also the unification of both in [[KR]]-theory.)

One of the basic facts about topological K-theory, rather unexpected from the definition, is that these higher K-groups repeat _periodically_ in the degree $n$. For $k = \mathbb{R}$ the periodicity is 8, for $k = \mathbb{C}$ it is 2. This is called _[[Bott periodicity]]_.


It turns out that an important source of [[virtual vector bundles]] representing classes in [[K-theory]] are [[index bundles]]: Given a [[Riemannian manifold|Riemannian]] [[spin structure|spin]] [[manifold]] $B$, then there is a [[vector bundle]] $S \to B$ called the _[[spin bundle]]_ of $B$, which carries a [[differential operator]], called the [[Dirac operator]] $D$. The [[index of a Dirac operator]] is the formal difference of its [[kernel]] by its [[cokernel]] $[ker D, coker D]$. Now given a continuous family $D_x$ of Dirac operators/Fredholm operators, parameterized by some topological space $X$, then these indices combine to a class in $K(X)$.

It is via this construction that topological K-theory connects to [[spin geometry]] (see e.g. [[Karoubi K-theory]]) and [[index theory]].

As the terminology indicates, both [[spin geometry]] and [[Dirac operator]] originate in [[physics]]. Accordingly, K-theory plays a central role in various areas of [[mathematical physics]], for instance in the theory of [[geometric quantization]] ("[[spin^c quantization]]") in the theory of [[D-branes]] (where it models [[D-brane charge]] and [[RR-fields]]) and in the theory of [[Kaluza-Klein compactification]] via [[spectral triples]] (see below).

All these geometric constructions have an [[operator algebra|operator algebraic]] incarnation: by the topological [[Serre-Swan theorem]] then [[vector bundles]] of finite rank are equivalently [[modules]] over the [[C*-algebra]] of [[continuous functions]] on the base space. Using this relation one may express K-theory classes entirely operator algebraically, this is called _[[operator K-theory]]_. Now [[Dirac operators]] are generalized to [[Fredholm operators]].

There are more [[C*-algebras]] than arising as [[algebras of functions]] of [[topological space]], namely non-commutative C*-algebras. One may think of these as defining [[non-commutative geometry]], but the definition of [[operator K-theory]] immediately generalizes to this situation (see also at _[[KK-theory]]_).

While the [[C*-algebra]] of a [[Riemannian manifold|Riemannian]] [[spin structure|spin]] [[manifold]] remembers only the underlying [[topological space]], one may algebraically encode the [[smooth structure]] and [[Riemannian structure]] by passing from [[Fredholm modules]] to "[[spectral triples]]". This may for instance be used to algebraically encode the spin physics underlying the [[standard model of particle physics]] and [[operator K-theory]] plays a crucial role in this.



## Definition
 {#Definition}

The following discussion of topological K-theory in terms of [[point-set topology]].
For more abstract perspectives see for instance _[[Snaith's theorem]]_ and other pointers at _[[K-theory]]_.

Assumed background for the following is the content of

* _[[topological vector bundles]]_

* _[[Grothendieck group of a commutative monoid]]_

* _[[pointed topological spaces]]_


Throughout, let $k$ be a [[topological field]], usually the [[real numbers]] $\mathbb{R}$ or of [[complex numbers]] $\mathbb{C}$.

In the following we take

1. _[[vector space]]_ to mean _[[finite dimensional vector space]]_ over $k$.

1. _[[vector bundle]]_ to mean _[[topological vector bundle]] over $k$ of finite [[rank of a vector bundle|rank]]_.

We say _[[monoid]]_ for _[[semigroup]] with [[unitality|unit]]_.


For the most part below we will invoke the assumption that the base [[topological space]] $X$ is a [[compact Hausdorff space]].
Because then the following statement holds, which is crucial in some places:

+-- {: .num_lemma #DirectSumHasInverseUpToTrivialBundle}
###### Lemma
**(over [[compact Hausdorff space]] every [[topological vector bundle]] is [[direct sum of vector bundles|direct summand]] of a [[trivial vector bundle]])**

For every [[topological vector bundle]] $E \to X$ over the [[compact Hausdorff space]] $X$ there exists a [[topological vector bundle]] $\tilde E \to X$ such that the [[direct sum of vector bundles]]

$$
  E \oplus_X \tilde E \simeq X \times \mathbb{R}^{n}
$$

is a [[trivial vector bundle]].

=--

For **proof** see [this prop.](topological+vector+bundle#TopologicalVectorbundleOverCompactHausdorffSpaceIsDirectSummandOfTrivialBundle) at _[[topological vector bundle]]_.


### The K-group

The starting point is the simple observation that the operation of [[direct sum of vector bundles]] yields a [[monoid]] structure ([[semi-group]] with [[unitality|unit]]) on [[isomorphism classes]] of [[topological vector bundles]], which however is lacking [[inverse elements]] and hence is not an actual [[group]].

+-- {: .num_defn #SemigroupOfIsomorphismClassesOfTopologicalVectorBundlesOnX}
###### Definition
**([[monoid]] of [[isomorphism classes]] of [[topological vector bundles]] on $X$)

For $X$ a [[topological space]], write $Vect(X)_{/\sim}$ for the [[set]] of [[isomorphism classes]] of [[topological vector bundles]] over $X$. The operation of [[direct sum of vector bundles]]

$$
  (-)\oplus_X (-)
  \;\colon\;
  Vect(X) \times Vect(X)
    \longrightarrow
  Vect(X)
$$

descends to this [[quotient]] by [[isomorphism]]

$$
  [E_1] + [E_2]
  \;\coloneqq\;
  [E_1 \oplus_X E_2]
$$

to yield the structure of a [[monoid]] ([[semi-group]] with [[unitality|unit]])

$$
  \left(
     Vect(X)_{/\sim}, +
  \right)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The operation of [[direct sum of vector bundles]] on [[isomorphism classes]] in def. \ref{SemigroupOfIsomorphismClassesOfTopologicalVectorBundlesOnX} is indeed not a [[group]]:

Let $x \in X$ be a chosen point of $x$ and write

$$
  rk_x
    \;\colon\;
  Vect(X)_{/\sim}
    \longrightarrow
  \mathbb{N}
$$

for the [[function]] which takes a [[topological vector bundle]] to the [[rank of a vector bundle|rank]] over the [[connected component]] of the point $x$.

Then under [[direct sum of vector bundles]] the rank is additive

$$
  rk_x(E_1 \oplus_X E_2)
   \,=\,
  rk_x(E_1) + rk_x(E_1)
  \,.
$$

Now since the [[natural numbers]] under [[addition]] are just a [[monoid]] ([[semi-group]] with [[unitality|unit]]), with no element except zero having an [[inverse element]] under the additive operation, it follows immediately that a necessary condition for the [[isomorphism class]] of a [[topological vector bundle]] to be invertible under [[direct sum of vector bundles]] is that its [[rank of a vector bundle]] be zero. But there is only one such class of vector bundles, in fact there is only one such vector bundle,
namely the unique rank-zero bundle $X \times k^0$, necessarily a [[trivial vector bundle]].

Now for the [[monoid]] of [[natural numbers]] $(\mathbb{N},+)$ it is a time honored fact that it is interesting and useful to rectify its failure of being a [[group]] by [[universal construction|universally]] forcing it to become one. This is a process called _[[group completion]]_ and the group completion of the natural numbers is the additive group of [[integers]] $(\mathbb{Z},+)$.

The idea is hence to apply group completion also to the monoid $(Vect(X)_{/\sim}, +)$, and so that the [[rank of a vector bundle|rank]] operation above becomes a [[homomorphism]] of [[abelian groups]].

=--

An explicit construction of [[group completion]] of a [[commutative monoid]] is called the _[[Grothendieck group of a commutative monoid]]_.



+-- {: .num_defn #KGroupByGrothendieckGroup}
###### Definition
**(K-group as the [[Grothendieck group of a commutative monoid|Grothendieck group]] of [[isomorphism classes]] of [[topological vector bundles]])

For $X$ a [[topological space]], write

$$
  K(X) \;\coloneqq\; K(Vect(X)_{/\sim}, +)
$$

for the [[Grothendieck group of a commutative monoid|Grothendieck group]] of the [[commutative monoid]] (abelian [[semi-group]] with [[unitality|unit]]) of [[isomorphism classes]] of [[topological vector bundles]] on $X$
from def. \ref{SemigroupOfIsomorphismClassesOfTopologicalVectorBundlesOnX}.

This means that $K(X)$ is the [[group]] whose elements are [[equivalence classes]] of pairs

$$
  ([E_+], [E_-]) \; \in Vect(X)_{/\sim} \times Vect(X)_{/\sim}
$$

of [[isomorphism classes]] of [[topological vector bundles]] on $X$, with respect to the [[equivalence relation]]

\[
  \label{DefiningEquivalenceRelation}
  \big(
  \left(
    [E_+], [E_-]
  \right)
   \;\sim\;
  \left(
    [F_+, F_-]
  \right)
  \big)
   \;\Leftrightarrow\;
  \left(
    \underset{[G],[H] \in Vect(X)_{/\sim}}{\exists}
    \left(
      \left([E_+ \oplus_X G] , [E_- \oplus_X G]\right)
        \,=\,
      \left([F_+ \oplus_X H] , [F_- \oplus_X H]\right)
    \right)
  \right)
  \,.
\]

Here a pair $([E_+], [E_-])$ is also called a _[[virtual vector bundle]]_, and its equivalence class under the
above equivalence relation is also denoted

$$
  [E_+] - [E_-] \;\;\in K(X)
  \,.
$$

If $X$ is a [[pointed topological space]], hence equipped with a choice of point $x \in X$
then the difference of [[rank of a vector bundle|ranks]] $rk_x(-)$ of the representing vector bundles
over the [[connected component]] of $x \in X$

$$
  rk_x( [E_+] - [E_-] )
    \;\coloneqq\;
  rk_x(E_+) -  rk_x(E_-) \in \mathbb{Z}
$$

is called the _virtual rank_ of the virtual vector bundle.

=--

+-- {: .num_example #KGroupOfThePoint}
###### Example
**(K-group of the point is the [[integers]])**

Let $X = \ast$ be the [[point]]. Then a [[topological vector bundle]] on $X$ is just a [[vector space]]

$$
  Vect(\ast) \simeq Vect
$$

and an isomorphism of vector bundles is just a bijective [[linear map]].

Since [[finite dimensional vector spaces]] are [[isomorphism|isomorphic]] precisely if they have the same
[[dimension]], the [[monoid]] ([[semi-group]] with [[unitality|unit]]) of isomorphism classes of vector bundles over the point (def. \ref{SemigroupOfIsomorphismClassesOfTopologicalVectorBundlesOnX})
is the [[natural numbers]]:

$$
  \left(
    Vect(\ast)_{/\sim}, +
  \right)
    \;\simeq\;
  \left(
    \mathbb{N}, +
  \right)
  \,.
$$

Accordingly the K-group of the point is the [[Grothendieck group of a commutative monoid|Grothendieck group]] of the [[natural numbers]], which is the additive group of [[integers]] ([this example](Grothendieck+group+of+a+commutative+monoid#GrothendieckGroupOfNaturalNumbersUnderAdditionIsTheIntegers)):

$$
  K(\ast) \simeq (\mathbb{Z}, +)
$$

and this identification is the assignment of _virtual rank_ (def. \ref{KGroupByGrothendieckGroup}).

=--

+-- {: .num_prop #OnCompactHausdorffVirtualVectorBundlesAreFormalDifferentcesWithATrivialBundle}
###### Proposition
**(on [[compact Hausdorff spaces]] all [[virtual vector bundles]] are formal difference by a [[trivial vector bundle]])**

If $X$ is a [[compact Hausdorff space]], then every [[virtual vector bundle]] on $X$ (def. \ref{KGroupByGrothendieckGroup})
is of the form

$$
  [E] - [X \times k^n]
$$

(i.e. with negative  component represented by a [[trivial vector bundle]]).

=--

+-- {: .proof}
###### Proof

For $X$ compact Hausdorff then lemma \ref{DirectSumHasInverseUpToTrivialBundle} implies
that for every [[topological vector bundle]] $E_-$ there exists a topological vector bundle $\tilde E_-$
with $E_- \oplus_X \tilde E_- \simeq X \times k^n$, and hence

$$
  [E_+] - [E_-]
  =
  \underset{[E]}{\underbrace{[E_+] + [\tilde E_-]}}
    -
  \underset{[X \times k^n]}{\underbrace{ \left( [E_-] + [\tilde E_-] \right) } }
  =
  [E] - [X \times k^n]
  \,.
$$

=--

+-- {: .num_remark #KTheoryRing}
###### Remark
**([[commutative ring]] structure on $K(X)$ from [[tensor product of vector bundles]])**

Also the operation of [[tensor product of vector bundles]] over $X$ descends to
[[isomorphism classes]] of [[topological vector bundles]] and makes $(Vect(X)_{\sim}, \oplus, \otimes )$
a [[semi-ring]] ([[rig]]).

(This is the shadow under passing to isomorphism classes of the fact that the [[category]] $Vect(X)$
is a [[distributive monoidal category]] under [[tensor product of vector bundles]].)

This  multiplicative structure passes to the K-group (def. \ref{KGroupByGrothendieckGroup}) by the formula

$$
  [E_+, E_-] \cdot [F_+, F_-]
    \;\coloneqq\;
  [ (E_+ \otimes_X F_+) \oplus_X (E_- \otimes_X F_-) \,,\, (E_+ \otimes_X F_-) \oplus_X (E_- \otimes_X F_+)  ]
  \,.
$$

Accordingly the ring $(K(X), +,\cdot)$ is also called the _K-theory ring_ of $X$.

=--


+-- {: .num_remark #FunctorialityOfKGroup}
###### Remark
**([[functor|functoriality]] of the K-theory ring assignment)

Let $f \colon X \longrightarrow Y$ be a [[continuous function]] between [[topological spaces]].
The operation of [[pullback of vector bundles]]

$$
  f^\ast \;\colon\; Vect(Y) \longrightarrow Vect(X)
$$

is compatible with [[direct sum of vector bundles]] as well as with [[tensor product of vector bundles]]
and hence descends to a [[homomorphism]] of [[commutative rings]]

$$
  f^\ast \;\colon\; K(Y) \longrightarrow K(X)
$$

between the K-theory rings from remark \ref{KTheoryRing}. Moreover, for

$$
  X \overset{f}{\longrightarrow} Y \overset{g}{\longrightarrow} Z
$$

two consecutive [[continuous functions]], then the consecutive pullback
of the vector bundle is isomorphic to the pullback along the composite map, which
means that on K-group pullback preserves composition

$$
  (g \circ f)^\ast = f^\ast \circ g^\ast \;\colon\; K(Z) \longrightarrow K(X)
  \,.
$$

Finally, of course pullback along an [[identity function]] $id_X \colon X \to X$ is the identity group
homomorphism.

In summary this says that the assignment of K-groups to topological spaces is a [[functor]]

$$
  K(-)
   \;\colon\;
  Top^{op}
    \longrightarrow
  CRing
$$

from the [[opposite category]] of the [[category]] [[Top]] of [[topological space]] to the category [[CRing]] of [[commutative rings]].

=--

We consider next the image of plain vector bundles in [[virtual vector bundles]]:

+-- {: .num_prop #StableEquivalenceOfVectorBundles}
###### Definition
**([[stable equivalence of vector bundles]])**

Let $X$ be a [[topological space]]. Define an [[equivalence relation]] $\sim_{stable}$ on [[topological vector bundles]]
over $X$ by declaring two vector bundles $E_1 E_2 \in Vect(X)$ to be equivalent if there exists a
[[trivial vector bundle]] $X \times k^n$ of some [[rank]] $n$ such that after [[direct sum of vector bundles]]
with this [[trivial vector bundle]], both bundles become [[isomorphism|isomorphic]]

$$
  \left(
    E_1
      \sim_{stable}
    E_2
  \right)
    \;\Leftrightarrow\;
  \underset{n \in \mathbb{N}}{\exists}
  \left(
     E_1 \oplus_X (X \times k^n)
       \;\simeq\;
     E_2 \oplus_X (X \times k^n)
  \right)
  \,.
$$

If $E_1 \sim_{stable} E_2$ we say that $E_1$ and $E_2$ are _stably equivalent vector bundles_.

=--


+-- {: .num_prop }
###### Proposition
**([[image]] of plain [[vector bundles]] in [[virtual vector bundles]])**

Let $X$ be a [[topological space]]. There is a [[homomorphism]] of [[semigroups]]

$$
  \array{
    Vect(X)_{/\sim}
      & \longrightarrow &
    K(X)
    \\
    [E_1] &\overset{\phantom{AAA}}{\mapsto}& \left( [E_1], [X \times k^0] \right)
  }
$$

from the [[isomorphism classes]] of [[topological vector bundles]] (def. \ref{SemigroupOfIsomorphismClassesOfTopologicalVectorBundlesOnX})
to the K-group of $X$ (def. \ref{KGroupByGrothendieckGroup} ).

If $X$ is a [[compact Hausdorff space]],
then the [[image]] of this function is the [[stable equivalence classes of vector bundles]] (def. \ref{StableEquivalenceOfVectorBundles}),
hence this function factors as an [[epimorphism]] onto $Vect(X)_{/\sim_{stable}}$ followed by an [[injection]]

$$
  Vect(X)_{/\sim}
    \longrightarrow
  Vect(X)_{/\sim_{stable}}
    \hookrightarrow
  K(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The homomorphism of [[commutative monoids]] $Vect(X)_{/\sim} \to K(X)$ is the one given by the [[universal property]] of the [[Grothendieck group of a commutative monoid|Grothendieck group]] construction ([this prop.](Grothendieck+group+of+a+commutative+monoid#UniversalProperty)).

By definition of the [[Grothendieck group of a commutative monoid|Grothendieck group]] ([this def.](Grothendieck+group+of+a+commutative+monoid#GrothendieckGroupViaQuotientOfCartesianProduct)), two elements of the form

$$
  \left(
    [E_1], [X \times k^0]
  \right)
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \left(
    [E_2], [X \times k^0]
  \right)
$$

are equivalent precisely if there exist vector bundles $F_1$ and $F_2$ such that

$$
  \left(
     [ E_1 \oplus_X F_1 ], [ F_1]
  \right)
   \;=\;
  \left(
    [E_2 \oplus_X F_2], [F_2]
  \right)
  \,.
$$

First of all this means that $F_1 \simeq F_2$, hence is equivalent to the existence of a vector
bundle $F$ such that


$$
  [E_1 \oplus F] \;=\; [E_2 \oplus F]
  \,.
$$

Now, by the assumption that $X$ is compact Hausdorff, lemma \ref{DirectSumHasInverseUpToTrivialBundle}
implies that there exists a vector bundle $\tilde F$ such that

$$
  F \oplus_X \tilde F \simeq X \times k^n
$$

is the [[trivial vector bundle]] of some [[rank of a vector bundle|rank]] $n \in \mathbb{N}$. This means that the above is equivalent already to the existence of an
$n \in \mathbb{N}$ such that

$$
 [E_1 \oplus (X \times k^n)]
   \;=\;
 [E_2 \oplus (X \times k^n)]
 \,.
$$

This is the definition of stable equivalence from def. \ref{StableEquivalenceOfVectorBundles}.

=--




### The reduced K-group
 {#ReducedKGroup}

+-- {: .num_defn #KernelReducedKGroup}
###### Definition
**([[reduced K-theory]])**

Let $X$ be a [[pointed topological space]], hence a [[topological space]] equipped with a choice of
point $x \in X$, hence with a [[continuous function]] $const_x \colon \ast  \to X$ from the [[point space]].

By the functoriality of the K-groups (remark \ref{FunctorialityOfKGroup}) this induces a group homomorphism

$$
  const_x^\ast \;\colon\; K(X) \longrightarrow K(\ast)
$$

given by restricting a virtual vector bundle to the basepoint.

The [[kernel]] of this map is called the _[[reduced K-theory]] group_ of $(X,x)$, denoted

$$
  \tilde K(X) \;\coloneqq\; ker(const_x^\ast)
  \,.
$$

=--



+-- {: .num_example #ExpressingPlainKTHeoryGroupInTermsOfReducedKTheoryGroup}
###### Example
**(expressing plain K-groups as reduced K-groups)**

Let $X$ be a [[topological space]]. Write  $X_* \coloneqq X \sqcup \ast$ for its [[disjoint union space]]
with the [[point space]], and regard this as a [[pointed topological space]] with base point the adjoined point.

Then the reduced K-theory of $X_+$ is the plain K-theory of $X$:

$$
  \tilde K(X_+)
    \simeq
  K(X)
  \,.
$$

Because every [[topological vector bundle]] on $X \sqcup \ast$ is the [[direct sum of vector bundles]]
of one that has [[rank of a vector bundle|rank]] zero on $\ast$
and one that has rank zero on $X$ ([this example.](direct+sum+of+vector+bundles#DirectSumOnDisjointUnionSpace))

=--


+-- {: .num_remark #RestrictionInKTheoryToPointComputesVirtualRank}
###### Remark
**(restriction in K-theory to the point computes virtual rank)**

By example \ref{KGroupOfThePoint} we have that

1. $K(\ast) \simeq \mathbb{Z}$;

1. under this identification the function $const_x^\ast$ is the assignment of _virtual rank_

   $$
     \array{
        K(X) &\overset{const_x^\ast}{\longrightarrow}& K(\ast) &\overset{\simeq}{\to}& \mathbb{Z}
        \\
        [E]- [F] &\overset{\phantom{AAA}}{\mapsto}& [E_x] - [F_x] &\mapsto& rk_x(E) - rk_x(F)
     }
   $$

=--


+-- {: .num_defn #VanishingAtInfinity}
###### Remark
**([[vanishing at infinity]])

If $X$ is a [[locally compact topological space|locally compact]] [[Hausdorff space]], then a [[continuous function]]

$$
  f \;\colon\; X \longrightarrow \mathbb{R}
$$

is said to [[vanishing at infinity|vanish at infinity]] if it [[extension|extends]] by zero
to the [[one-point compactification]] $X^* \coloneqq (X \sqcup \{\infty\}, \tau_{cpt})$

$$
  \array{
    X &\overset{f}{\longrightarrow}& \mathbb{R}
    \\
    \downarrow & \nearrow_{\mathrlap{ x \mapsto \left\{ \array{ f(x) &\vert& x \in X \\ 0 &\vert& x = \infty }  \right. }}
    \\
    X^\ast
  }
$$

Now the [[one-point compactification]] $X^\ast$ is a [[compact Hausdorff space]]
(by [this prop. ](one-point+compactification#OnePointExtensionIsCompact) and [this prop.](one-point+compactification#HausdorffOnePointCompactification))
and canonically a [[pointed topological space]] with basepoint the element $\infty \in X^\ast$.

Moreover, every [[compact Hausdorff space]] $X$ arises this way as the [[one-point compactification]]
of the [[complement]] [[subspace]] of any of its points: $X \simeq (X \setminus \{x\})^\ast$
(by [this remark](one-point+compactification#CompactHausdorffSpaceIsCompactificationOfComplementOfAnyPoint)).

Since [[open subspaces of compact Hausdorff spaces are locally compact]],
this complement [[subspace]] $X \setminus \{x\} \subset X$ is a [[locally compact topological space|locally compact]]
[[Hausdorff space]], and every locally compact Hausdorff spaces arises
this way (by [this prop.](one-point+compactification#InclusionIntoOnePointExtensionIsOpenEmbedding)).

Therefore one may think of the [[reduced K-groups]] $\tilde K(X)$ (def. \ref{KernelReducedKGroup})
of compact Hausdorff spaces as the those K-groups of locally compact Hausdorff spaces which
"vanish at infinity".

=--


+-- {: .num_remark #FunctorialityOfReducedKGroups}
###### Remark
**([[functor|functoriality]] of the reduced K-groups)**

By the functoriality of the unreduced K-groups (remark \ref{FunctorialityOfKGroup})
on (the [[opposite category|opposite]] of) the [[category]] [[Top]] of all topological spaces,
the reduced K-groups (def. \ref{KernelReducedKGroup}) becomes functorial
on the category $Top^{\ast/}$ of _[[pointed topological spaces]]_
(whose [[morphisms]] are the [[continuous functions]] that preserve the base-point):

$$
  \tilde K \;\colon\; (Top^{\ast/})^{op} \longrightarrow Ab
  \,.
$$

This follows by the functoriality of the [[kernel]] construction
(which in turn follows by the [[universal property]] of the kernel):

For $(X,x)$ and $(Y,y)$ [[pointed topological spaces]]
and  $f \colon X \longrightarrow Y$ a continuous function which preserves basepoints
$f(x) = y$ then

$$
  \array{
     ker(const_x^\ast)
       &\longrightarrow&
     K(X)
       &\overset{const_x^\ast}{\longrightarrow}&
     K(\{x\})
     \\
     \uparrow^{\mathrlap{\exists !}} && \uparrow^{\mathrlap{f^\ast}} && \uparrow^{\mathrlap{f^\ast}}
     \\
     ker(const_y^\ast)
       &\longrightarrow&
     K(Y)
       &\overset{const_x^\ast}{\longrightarrow}&
     K(\{y\})
  }
  \,.
$$

=--




+-- {: .num_prop #KGrupDirectSummandReducedKGroup}
###### Proposition
**(over [[compact Hausdorff spaces]] $\tilde K(X)$ is a [[direct sum|direct summand]] of $K(X)$)

If $(X,x)$ is a [[pointed topological space|pointed]] [[compact Hausdorff space]] then the defining [[short exact sequence]]
of [[reduced K-theory]] groups (def. \ref{KernelReducedKGroup})

$$
  0 \to \tilde K(X) \overset{\phantom{AAA}}{\hookrightarrow} K(X) \overset{const_x^\ast}{\longrightarrow} K(\ast) \simeq \mathbb{Z}
   \to 0
$$

[[split exact sequence|splits]] and thus yields an [[isomorphism]], which is given by

$$
  \array{
    K(X)
      &\overset{\phantom{A}\simeq \phantom{A}}{\longrightarrow}&
    \tilde K(X) \oplus \mathbb{Z}
    \\
    [E] - [X \times k^n]
      &\overset{\phantom{AAA}}{\mapsto}&
    ([E], rk_x(E) - n)
  }
  \,.
$$

Here on the left we are using prop. \ref{OnCompactHausdorffVirtualVectorBundlesAreFormalDifferentcesWithATrivialBundle}
to represent any element of the K-group as a [[virtual vector bundle|virtual]] difference of a vector bundle $E$ by
a [[trivial vector bundle]],
and $rk_x(E) \in \mathbb{N}$ denotes the [[rank of a vector bundle|rank]] of this vector bundle over the [[connected component]]
of $x \in X$.

Equivalently this means that every element of $K(X)$ decomposes as follows into a
piece that has vanishing virtual rank over the connected component of $x$ and a virtual [[trivial vector bundle]].

$$
  [E]- [X \times k^n]
    =
  \underset{\in \tilde K(X) \subset K(X)}{\underbrace{\left( [E] - [X \times k^{rk_x(E)}] \right)}}
    -
  \underset{\in \mathbb{Z} \subset K(X) }{\underbrace{[X \times k^{n-rk_x(E)}]}}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By remark \ref{RestrictionInKTheoryToPointComputesVirtualRank} the kernel of
$const_x^\ast$ is identified with the [[virtual vector bundles]] of
vanishing virtual rank.
By prop. \ref{OnCompactHausdorffVirtualVectorBundlesAreFormalDifferentcesWithATrivialBundle}
this kernel is identified with the elements of the form
$$
  [E] - [X \times k^{rk_x(E)}]
  \,.
$$

=--

+-- {: .num_example #BottElement}
###### Example
**([[Bott element]])**

For $S^2$ the [[Euclidean space|Euclidean]] [[2-sphere]], write

$$
  h \in Vect_{\mathbb{C}}(S^2) \longrightarrow K_{\mathbb{C}}(S^2)
$$

for the complex topological K-theory class of the [[basic complex line bundle on the 2-sphere]].
By prop. \ref{KGrupDirectSummandReducedKGroup} its image in [[reduced K-theory]]
is the [[virtual vector bundle]]

$$
  \beta \;\coloneqq \; h-1 \in \tilde K_{\mathbb{C}}(S^2)
  \,.
$$

This is known as the _[[Bott element]]_, due to its key role in the [[Bott periodicity]]
of complex topological K-theory, discussed [below](#BottPeriodicities).

=--

In order to describe $\tilde K(X)$ itself as an equivalence class, we consider the followign refinement
of [[stable equivalence of vector bundles]] (def. \ref{StableEquivalenceOfVectorBundles}):

+-- {: .num_defn #EquivalenceRelationForReducedKTheory}
###### Definition
**([[equivalence relation]] for [[reduced K-theory]] on [[compact Hausdorff spaces]])**

For $X$ a [[topological space]], define an [[equivalence relation]] on the [[set]] of  [[topological vector bundles]] $E \to X$ over $X$ by declaring that $E_1 \sim E_2$ if there exists $k_1, k_2 \in \mathbb{N}$ such that there is an [[isomorphism]] of [[topological vector bundles]] between the [[direct sum of vector bundles]] of $E_1$ with the [[trivial vector bundle]] $X \times \mathbb{R}^{k_1}$ and of $E_2$ with $X \times \mathbb{R}^{k_2}$

$$
  (E_1 \sim_{red} E_2)
   \Leftrightarrow
  \left(
    \underset{k_1,k_2 \in \mathbb{N}}{\exists}
      \left(
         (E_1 \oplus_X (X \times \mathbb{R}^{k_1})
           \;\simeq\;
         (E_2 \oplus_X (X \times \mathbb{R}^{k_2})
      \right)
  \right)
  \,.
$$


The operation of [[direct sum of vector bundles]] descends to these quotients

$$
  [E_1] + [E_2]
  \;\coloneqq\;
  [ E_1 \oplus_X E_2 ]
$$

to yield a commutative [[semi-group]]

$$
  \left(Vect(X)_{/\sim_{red}}, +\right)
  \,.
$$

=--

+-- {: .num_prop #ReducedKEquivalenceRelationVerified}
###### Proposition


For $X$ a [[compact Hausdorff space]] then the commutative [[monoid]] $(Vect(X)_{/\sim_{red}}, +)$
from def. \ref{EquivalenceRelationForReducedKTheory} is already an [[abelian group]] and is
in fact [[natural isomorphism|naturally isomorphic]]
to the [[reduced K-theory]] group $\tilde K(X)$ (def. \ref{KernelReducedKGroup}):

$$
  \tilde K(X) \simeq (Vect(X)_{/\sim_{red}}, +)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{KGrupDirectSummandReducedKGroup} $\tilde K(X)$ is the subgroup of the [[Grothendieck group of a commutative monoid|Grothendieck group]] $K(X)$
on the elements of the form $[E]- [X \times k^{rk_x(E)}]$, which are clearly entirely determined by
$[E] \in Vect(X)_{/\sim}$. Hence we need to check if the equivalence relation of the Gorthendieck
goup coincides with $\sim_{red}$ on these representatives.

The relation in the Grothendieck group is given by

$$
  \left(
    [E_1]
      \sim
    [E_2]
  \right)
    \Leftrightarrow
  \left(
    \underset{[G], [H] \in Vect(X)_{/\sim}}{\exists}
    \left(
      ( [E_1]+ [G], [X \times k^{rk_x(E_1)}] + [G] )
      \;=\;
      ( [E_2] + [H], [X \times k^{rk_x(E_2)}] + [H] )
    \right)
  \right)
$$

As before, in prop. \ref{OnCompactHausdorffVirtualVectorBundlesAreFormalDifferentcesWithATrivialBundle}
we may assume without restriction that $G = X \times k^{n_1}$ and $H = X \times k^{n_2}$ are [[trivial vector bundles]]. Then
the above equality on the first component

$$
  [E_1] + [X \times k^{n_1}]
  =
  [E_2] + [X \times k^{n_2}]
$$

is the one that defines $\sim_{red}$, and since isomorphic vector bundles
necessarily have the same rank, it implies the equality of the second component.

=--


+-- {: .num_remark}
###### Remark
**([[non-unital ring|non-unital]] [[commutative ring]]-structure on $\tilde K(X)$)**

In view of the [[commutative ring]] structure on the K-group $K(X)$ from remark \ref{KTheoryRing},
the reduced K-group $\tilde K(X)$ from def. \ref{KernelReducedKGroup}, being the [[kernel]]
of a ring [[homomorphism]] (remark \ref{FunctorialityOfKGroup}) is an ideal in $K(X)$,
hence itself a [[non-unital ring|non-unital]] [[commutative ring]].

(The ring unit of $K(X)$ is the class $[X \times k^1, X \times k^0]$ of the [[trivial vector bundle|trivial]]
[[line bundle]] on $X$, which has virtual rank 1, and hence is not in $\tilde K(x)$.)


=--



### The relative K-group
 {#TheRelativeKGroup}


+-- {: .num_defn #RelativeKTheory}
###### Definition
**([[relative K-theory]])**

Let

1. $X$ be a [[compact Hausdorff space]];

1. $A \subset X$ a [[closed subspace]].

Then the _[[relative K-theory]] group of the pair $(X,A)$_, denoted $K(X,A)$ is the [[reduced K-theory]] group (def. \ref{KernelReducedKGroup})
of the [[quotient space]] $X/A$ ([this def.](quotient+space#QuotientBySubspace)):

$$
  K(X,A)
   \;\coloneqq\;
  \tilde K(X/A)
  \,.
$$

=--

+-- {: .num_defn #RelatveKTheoryReducesToBareKTheoryAndToReducedKTheory}
###### Example
**(expressing plain and reduced K-theory in terms of relative K-theory)**

The [[relative K-theory]] construction from def. \ref{RelativeKTheory}
reduces in special cases to the plain K-theory group and to the [[reduced K-theory]] group.

Recall  that for the case that $A = \emptyset \subset X$ then $X/\emptyset = X_+ = X \sqcup \ast$
(by [this example](quotient+space#QuotientBySubspace)). Therefore:

1. for $A = \emptyset \subset X$ we have $K(X,\emptyset) = \tilde K(X \sqcup \ast) \simeq K(X)$ (example \ref{ExpressingPlainKTHeoryGroupInTermsOfReducedKTheoryGroup});

1. for $A = \{x\} \subset X$ we have $K(X, \{x\}) = \tilde K(X/\{x\}) = \tilde K(X)$.


=--


### The graded K-groups
 {#TheGradedKGroups}

The (reduced) K-theory groups of reduced suspensions of pointed space are called the
"K-group in degree 1":

+-- {: .num_defn #GradedKGroups}
###### Definition
**(graded K-groups)**

For $X$ a [[pointed topological space]] write

$$
  \tilde K^1(X)
    \;\coloneqq\;
  \tilde K(\Sigma X)
$$

for the [[reduced K-theory]] of the [[reduced suspension]] of $X$.

For $X$ a [[compact Hausdorff space]] and $A \subset X$ a [[closed subspace]], write

$$
  K^1(X,A)
    \coloneqq
  \tilde K( \Sigma(X/A) )
$$

for the [[reduced K-theory]] of the [[reduced suspension]] of the [[quotient space]].

We say these are the K(-cohomology)-groups in degree 1. For emphasis one says that the original K-groups
are in degree zero and writes

$$
  K^0(X) \coloneqq K(X)
  \phantom{AAAA}
  \tilde K^0(X) \coloneqq \tilde K(X)
    \phantom{AAA}
  K^0(X,A) \coloneqq K(X,A)
  \,.
$$

The groups are collected to the _graded K-groups_, which are the [[direct sums]]

$$
  \tilde K^\bullet(X)
    \coloneqq
  \tilde K^0(X) \oplus \tilde K^1(X)
$$

and

$$
  K^\bullet(X,A)
    \coloneqq
  K^0(X,A) \oplus K^1(X.A)
$$

regarded as $\mathbb{Z}/2$-graded groups.

Under [[tensor product of vector bundles]] this becomes a non-unital $\mathbb{Z}/2$-
[[graded-commutative ring]] (discussed [below](#GradedRingStructure)).

=--



Recall from
example \ref{ExpressingPlainKTHeoryGroupInTermsOfReducedKTheoryGroup}
and from example \ref{RelatveKTheoryReducesToBareKTheoryAndToReducedKTheory} the identifications
of plain, reduced and relative K-groups, which with the degree-zero notation from def. \ref{GradedKGroups}
read:

$$
  K^0(X, \emptyset)
    \simeq
  \tilde K^0(X_+)
    \simeq
  K^0(X)
$$

The analogue is true for the K-groups in degree 1 from def. \ref{GradedKGroups},
though this is no longer completely trivial:


### For non-compact spaces
 {#ForNonCompactSpaces}

By prop. \ref{OnCompactHausdorffVirtualVectorBundlesAreFormalDifferentcesWithATrivialBundle} the
topological K-theory groups of [[compact topological spaces]] are [[representable functor|represended]]
by [[homotopy classes]] of [[continuous functions]] into the [[classifying spaces]] $B O \times \mathbb{Z}$
and $B U \times \mathbb{Z}$, respectively (def. \ref{BUn}).

$$
  \left(
    X \text{compact}
  \right)
    \;\Rightarrow\;
  \left(
    K_{\mathbb{C}}(X)
      \simeq
    [X \to B U \times \mathbb{Z}]
    \phantom{AAAAA}
    K_{\mathbb{R}}(X)
      \simeq
    [X, B O \times \mathbb{Z}]
  \right)
  \,.
$$

There are various ways of generalizing this situation to non-compact spaces:

+-- {: .num_defn #GrothendieckGroupKTheory}
###### Definition
**(Grothendieck group topological K-theory)**

   The [[Grothendieck group]] construction on the [[monoid]] $(Vect(X)/_\sim, \oplus)$
   of [[isomorphism classes]] of [[topological vector bundles]] makes sense for every
   [[topological space]] $X$. For non-compact $X$ this is usually just called that
   "the Grothendieck group of vector bundles on $X$", sometimes denoted

   $$
     \mathbb{K}(X) \coloneqq GrothGroup( Vect(X)/_\sim, \oplus )
     \,.
   $$

=--

+-- {: .num_defn #RepresntableTopologicalKTheory}
###### Definition
**(representable topological K-theory)

   The group of [[homotopy classes]] of [[continuous functions]] into a (classifying) space
   is of course well defined for any domain space, hence for any topological space $X$ one may set

   $$
     K_{\mathbb{C}}(X)_{rep}
      \;\coloneqq\;
     [X,B U \times \mathbb{Z}]
     \phantom{AAAAA}
     K_{\mathbb{R}}(X)_{rep}
      \;\coloneqq\;
     [X,B O \times \mathbb{Z}]
   $$

   This is called _representable K-theory_.

=--

Representable K-theory over [[paracompact topological spaces]] was discussed in ([Karoubi 70](#Karoubi70)).

+-- {: .num_defn #InverseLimitTopologicalKTheory}
###### Definition
**(inverse limit topological K-theory)

   Let $X$ be a [[topological space]] with the structure of a [[CW-complex]],
   hence a [[colimit]] ("[[direct limit]]") $X \simeq \underset{\longrightarrow}{\lim}_n X_n$
   such that each $X_n$ is a [[finite cell complex]], hence in particular a [[compact topological space]].
   Then the [[limit]] ([[inverse limit]])
   of the corresponding K-group

   $$
     K(X)_{invl} \coloneqq \underset{\longleftarrow}{\lim}_n K(X_n)
   $$

   is called the _inverse limit K-theory_ of $X$.

=--

$\,$

No two of these definitions are equivalent to each other on all of their domain of defintion
(e.g. [Anderson-Hodgkin 68](#AndersonHodgkin68), [Jackowski-Oliver](#JackowskiOliver)).

Representable and direct limit K-theory of spaces that are [[sequential colimits]] of [[compact spaces]]
differ in general by a [[lim^1]]-term ([Segal-Atiyah 69, prop. 4.1](#SegalAtiyah69)).




## Examples
 {#Examples}

+-- {: .num_example}
###### Example
**(topological K-theory ring of the [[point space]])**

We have already seen in example \ref{KGroupOfThePoint} that

$$
  K(\ast) \simeq \mathbb{Z}
  \,.
$$

=--

+-- {: .num_example #ComplexTopologicalKTheoryOfTheCircle}
###### Example
**(complex topological K-theory ring of the [[circle]])

Since the complex [[general linear group]] $GL(n,\mathbb{C})$ is [[path-connected topological space|path-connected]]
([this prop.](general+linear+group#ConnectednessOfGeneralLinearGroup)) and hence the [[classifying space]]
$B GL(n,\mathbb{C})$ is [[simply connected topological space|simply]]-connected, hence its
[[fundamental group]] is trivial $\pi_1(B GL(n,\mathbb{C})) \simeq [S^1, B GL(n,\mathbb{C})] = 1$.
Accordingly, all [[complex vector bundles]] on $S^1$ are [[isomorphism|isomorphic]] to a [[trivial vector bundle]].

It follows that

$$
  K_{\mathbb{C}}(S^1) \simeq \mathbb{Z}
  \phantom{AA} \text{and} \phantom{AA}
  \tilde K_{ \mathbb{C} }(S^1) \simeq 0
  \,.
$$


=--

+-- {: .num_example #TopologicalKTheoryRingOfThe2Sphere}
###### Example
**(complex topological K-theory ring of the [[2-sphere]])

For $X = \ast$ the [[point space]], the [[fundamental product theorem in topological K-theory]] \ref{FundamentalProductTheorem} states that the homomorphism

$$
  \array{
    \mathbb{Z}[h]/((h-1)^2)
      &\longrightarrow&
    K_{\mathbb{C}}(S^2)
    \\
    h &\mapsto& h
  }
$$

is an [[isomorphism]].

This means that the relation $(h-1)^2 = 0$ satisfied by the [[basic complex line bundle on the 2-sphere]] ([this prop.](basic+complex+line+bundle+on+the+2-sphere#TensorRelationForBasicLineBundleOn2Sphere)) is the _only_ relation is satisfies in topological K-theory.

Notice that the underlying [[abelian group]] of $\mathbb{Z}[h]/((h-1)^2)$ is two [[direct sum]] copies of the [[integers]],

$$
  K_{\mathbb{C}}(S^2) \simeq \mathbb{Z} \oplus \mathbb{Z} = \langle 1, h\rangle
$$

one copy spanned by the [[trivial vector bundle|trivial]] [[complex line bundle]] on the 2-sphere, the other spanned by the [[basic complex line bundle on the 2-sphere]]. (In contrast, the underlying abelian group of the [[polynomial ring]] $\mathbb{R}[h]$ has infinitely many copies of $\mathbb{Z}$, one for each $h^n$, for $n \in \mathbb{N}$).

It follows (by [this prop.](topological+K-theory#KGrupDirectSummandReducedKGroup)) that the [[reduced K-theory]] group of the 2-sphere is

$$
  \tilde K_{\mathbb{C}}(S^2) \simeq \mathbb{Z}
  \,.
$$

=--

+-- {: .num_example}
###### Example
**(complex topological K-theory of the [[torus]])**

Consider the [[torus]] $S^1 \times S^1$, the [[product topological space]] of the [[circle]] with itself
(with the [[Euclidean space|Euclidean]] [[subspace topology]]).

By example \ref{ReducedKTheoryOfProductSpace} we have

$$
  \tilde K(S^1 \times S^1)
    \simeq
  \tilde K(\underset{S^2}{\underbrace{S^1 \wedge S^1}})
    \oplus
  \underset{= 0}{
  \underbrace{
  \tilde K(S^1)
    \oplus
  \tilde K(S^1)
  }}
  \,.
$$

Since the [[smash product]] of the circle with itself is the  [[2-sphere]], and
since, the complex K-theory of the circle vanishes by example \ref{ComplexTopologicalKTheoryOfTheCircle},
this shows that the topological K-theory of the torus coincides with that of the 2-sphere:

$$
  K(S^1 \times S^1) \simeq K(S^2)
  \,.
$$

=--




## Properties

### Homotopy invariance

+-- {: .num_prop #KGroupsHomotopyInvariance}
###### Proposition
**([[homotopy invariance]] of K-groups)

Let $X$ and $Y$ be [[paracompact Hausdorff spaces]], and let

$$
  f \;\colon\; X \longrightarrow Y
$$

be a [[continuous function]] which is a [[homotopy equivalence]].
Then the pullback operation on (reduced) K-groups along $f$ (remark \ref{FunctorialityOfKGroup}, remark \ref{FunctorialityOfReducedKGroups}) is an
[[isomorphism]]:

$$
  f^\ast
  \;\colon\;
  K(Y)
    \overset{\simeq}{\longrightarrow}
  K(X)
$$

and

$$
  f^\ast
  \;\colon\;
  \tilde K(Y)
    \overset{\simeq}{\longrightarrow}
  \tilde K(X)
  \,.
$$


=--

+-- {: .proof}
###### Proof

This is an immediate consequence of the fact that over paracompact Hausdorff spaces
isomorphism classes of topological vector bundles are homotopy invariant ([this example.](topological+vector+bundle#HomotopyInvarianceOfIsomorphismClassesOfVectorBundles))

=--


### Exact sequences
 {#ExactSequences}

We discuss the [[long exact sequences in cohomology]] for topological K-theory.

What makes these work in prop. \ref{ExactSequenceInReducedTopologicalKTheory} below, turns out to be the following property of [[topological vector bundles]]:

+-- {: .num_lemma #VectorBundleOnClosedSubsetOfCompactHausdorffSpaceIsPullbackOfBundeOnQuotientSpace}
###### Lemma
**([[topological vector bundle]] [[trivial vector bundle|trivial]] over [[closed subspace]] of [[compact Hausdorff space]] is [[pullback bundle|pullback]] of bundle on [[quotient space]])**

Let $X$ be a [[compact Hausdorff space]] and let $A \subset X$ be a [[closed subspace]].

If a [[topological vector bundle]] $E \overset{p}{\to} X$ is such that its restriction $E\vert_A$
is [[trivializable vector bundle|trivializable]], then $E$ is [[isomorphism|isomorphic]] to
the [[pullback bundle]] $q^\ast E'$ of a topological vector bundle $E' \to X/A$
over the [[quotient space]]..

=--

The **proof** of lemma \ref{VectorBundleOnClosedSubsetOfCompactHausdorffSpaceIsPullbackOfBundeOnQuotientSpace} is
given at _[[topological vector bundle]]_
[here](topological+vector+bundle+VectorBundleOnClosedSubsetOfCompactHausdorffSpaceIsPullbackOfBundeOnQuotientSpace).
What makes that proof work, in turn, is the [[Tietze extension theorem]], via
[this lemma](topological+vector+bundle#IsomorphismOfVectorBundlesOnClosedSubsetOfCompactHausdorffSpaceExtendsToOpenNeighbourhoods).

+-- {: .num_prop #ExactSequenceInReducedTopologicalKTheory}
###### Proposition
**(exact sequence in reduced topological K-theory)**

Let

* $X$ be a [[pointed topological space|pointed]] [[compact Hausdorff space]];

* $A \subset X$ a [[pointed topological space|pointed]] [[closed subset|closed]] [[subspace]]

Write $X/A$ for the corresponding [[quotient space]] ([this def.](quotient+space#QuotientBySubspace)).
Denote the [[continuous functions]] of [[subspace]] inclusion and of  [[quotient space]] co-projection  by

$$
  A
    \overset{i}{\longrightarrow}
  X
    \overset{q}{\longrightarrow}
  X/A
  \,,
$$

respectively.
Then the induced sequence of [[reduced K-theory]] groups (def. \ref{KernelReducedKGroup}, remark \ref{FunctorialityOfReducedKGroups})

$$
  \tilde K_{\mathbb{C}}(X/A)
    \overset{q^\ast}{\longrightarrow}
  \tilde K_{\mathbb{C}}(X)
    \overset{i^\ast}{\longrightarrow}
  \tilde K_{\mathbb{C}}(A)
$$

is [[exact sequence|exact]], meaning that they induce an [[isomorphism]]

$$
  im(q^\ast) \simeq ker(i^\ast)
$$

between the [[image]] of $g^\ast$ and the [[kernel]] of $i^\ast$.

Similarly the sequence of unreduced and [[relative K-groups]] (def. \ref{RelativeKTheory}) is exact:

$$
  \tilde K_{\mathbb{C}}(X/A)
    \overset{q^\ast}{\longrightarrow}
  K_{\mathbb{C}}(X)
    \overset{i^\ast}{\longrightarrow}
  K_{\mathbb{C}}(A)
$$

=--

(e.g. [Wirthmuller 12, p. 32 (34 of 67)](#Wirthmuller12), [Hatcher, prop. 2.9](#Hatcher))

+-- {: .proof}
###### Proof

First observe that both statements are equivalent to each other: By
[[natural transformation|naturality]] of the construction of [[kernels]] the following
[[commuting diagram|diagram commutes]]:

$$
  \array{
    \tilde K_{\mathbb{C}}(X/A)
      &\overset{q^\ast}{\longrightarrow}&
    \tilde K_{\mathbb{C}}(X)
      &\overset{i^\ast}{\longrightarrow}&
    \tilde K_{\mathbb{C}}(A)
    \\
    {}^{\mathllap{id}}\downarrow && \downarrow && \downarrow
    \\
    \tilde K_{\mathbb{C}}(X/A)
      &\overset{q^\ast}{\longrightarrow}&
    K_{\mathbb{C}}(X)
      &\overset{i^\ast}{\longrightarrow}&
    K_{\mathbb{C}}(A)
    \\
    &&
    \downarrow && \downarrow
    \\
    && K_{\mathbb{C}}(\ast) &\underset{id}{\longrightarrow}& K_{\mathbb{C}}(\ast)
  }
  \,.
$$

Here the top vertical morphisms, the [[kernel]] inclusions, are [[monomorphisms]], and
hence the top horizonal row is exact precisely if the middle horizontal row is.

Hence it is sufficient to consider the top row. First of all
the composite function $A \overset{i}{\to} X \overset{q}{\to} X/A$ is a [[constant function]],
constant on the basepoint,
and hence $i^\ast \circ q^\ast$ is a constant function, constant on zero. This says that
we have an inclusion

$$
  im(q^\ast) \subset ker(i^\ast)
  \,.
$$

Hence it only remains to see for $x \in \tilde K(X)$ a class with $i^\ast(x) = 0$
that $x = q^\ast(y)$ comes from a class on the quotient $X/A$. But by compactness, the class
$x$ is given by a [[virtual vector bundle]] of the form $E - rk(E)$
(prop. \ref{OnCompactHausdorffVirtualVectorBundlesAreFormalDifferentcesWithATrivialBundle}, prop. \ref{KGrupDirectSummandReducedKGroup}).
and by prop. \ref{ReducedKEquivalenceRelationVerified} the triviality of $i^\ast(E- rk(E))$ means that
there is $n \in \mathbb{N}$ such that  $i \ast(E) \oplus_A (A \times \mathbb{C}^n)$
is a [[trivializable vector bundle]].
Therefore lemma \ref{VectorBundleOnClosedSubsetOfCompactHausdorffSpaceIsPullbackOfBundeOnQuotientSpace} gives
that $E \oplus_X (X \times \mathbb{C}^n)$
is isomorphic to the [[pullback bundle]] of a vector bundle $E'$ on $X/A$. This proves the claim.

=--


+-- {: .num_cor #LongExactSequenceInReducedTopologicalKTheory}
###### Corollary
**([[long exact sequence]] in [[reduced K-theory|reduced topological K-theory]])**

For $X$ a [[compact Hausdorff space]] and for $A \subset X$ a [[closed subset|closed]] [[subspace]] inclusion,
there is a [[long exact sequence]] of [[reduced K-theory]] groups of the form

$$
  \cdots
    \longrightarrow
  \tilde K_{\mathbb{C}}(\Sigma (X/A))
    \longrightarrow
  \tilde K_{\mathbb{C}}(\Sigma X)
    \longrightarrow
  \tilde K_{\mathbb{C}}( \Sigma A )
    \longrightarrow
  \tilde K_{\mathbb{C}}(X/A)
   \longrightarrow
  \tilde K_{\mathbb{C}}(X)
    \longrightarrow
  \tilde K_{\mathbb{C}}(A)
  \,,
$$

where $\Sigma(-)$ denotes [[reduced suspension]].

=--

+-- {: .proof}
###### Proof

The sequence is induced by functoriality (remark \ref{FunctorialityOfReducedKGroups}) from the long [[cofiber sequence]]

$$
  A
    \overset{i}{\longrightarrow}
  X
    \longrightarrow
  X \cup Cone(A)
    \longrightarrow
  (X \cup Cone(A)) \cup Cone(X)
    \longrightarrow
  ((X \cup Cone(A)) \cup Cone(X)) \cup (X \cup Cone(A))
    \longrightarrow
  \cdots
$$

obtained by consecutively forming [[mapping cones]].
By the discussion at _[[topological cofiber sequence]]_ this may be rearranged as

$$
  \array{
    A
      &\overset{i}{\longrightarrow}&
    X
      &\overset{j}{\longrightarrow}&
    Cone(i)
      &\longrightarrow&
    Cone(j)
    \\
    && &&
    \downarrow {\mathrlap{\text{homotopy} \atop \text{equivalence}}}
    &&
    \downarrow^{\mathrlap{\text{homotopy} \atop \text{equivalence}}}
    \\
    && &&
    X/A
    &&
    S A
      &\overset{S i}{\longrightarrow}&
    S X
      &\longrightarrow& \cdots
  }
$$

([this prop.](topological+cofiber+sequence#HomotopyEquivalenceSuspensionWithMappingConeOfMappingCone)
and [this](topological+cofiber+sequence)).

The claim hence follows by the [[homotopy invariance]] of the K-groups (prop. \ref{KGroupsHomotopyInvariance}).

=--


$\,$

We discuss some useful consequences of the [[long exact sequences in cohomology]].

+-- {: .num_prop #DirectSumOfKTheoryGroupsOverRetracts}
###### Proposition
**([[direct sum]] decomposition of K-theory groups over [[retractions]])**

Let $X$ be a ([[pointed topological space|pointed]]) [[compact topological space]]
and $A \subset X$ a ([[pointed topological space|pointed]]) [[closed subspace]], such that the
[[subspace]] inclusion $A \overset{i}{\to}$ X as a [[retraction]], i.e. a [[continuous function]]
$r \colon X \to A$ such that the [[composition|composite]]

$$
  id_A
    \;\colon\;
  A
    \overset{i}{\longrightarrow}
  X
    \overset{r}{\longrightarrow}
  A
$$

is the [[identity function]].

Then there is a splitting of the K-theory group of $X$ as a [[direct sum]] of the K-theory of $A$
and the [[relative K-theory]] of the [[quotient space]] $X/A$:

$$
  K(X)
    \;\simeq\;
  K(A)
    \oplus
  K(X,A)
$$

and in the pointed case a splitting of the [[reduced K-theory]] groups

$$
  \tilde K(X)
    \;\simeq\;
  \tilde K(A)
    \oplus
  K(X,A)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The long exact sequence from cor \ref{LongExactSequenceInReducedTopologicalKTheory} together
with the retraction yields

$$
  \tilde K(A)
    \underoverset
      {\underset{r^\ast}{\longrightarrow}}
      {\overset{i^\ast}{\longleftarrow}}
      {}
  \tilde K(X)
    \overset{}{\longleftarrow}
  K(X,A)
    \longleftarrow
  \tilde K(\Sigma A)
    \underoverset
      {\underset{}{\longrightarrow}}
      {\overset{}{\longleftarrow}}
      {}
  \tilde K(\Sigma X)
  \,.
$$

The splitting makes the morphisms $i^\ast$ and its suspension be [[surjections]], so that the
long exact sequence decomposes into [[short exact sequences]] which are [[split exact sequence|split exact]]:

$$
  0
    \longleftarrow
  \tilde K(A)
    \underoverset
     {\underset{r^\ast}{\longrightarrow}}
     {\overset{i^\ast}{\longleftarrow}}
     {}
  \tilde K(X)
    \longleftarrow
  K(X,A)
    \longleftarrow
  0
  \,.
$$

=--


+-- {: .num_example #FiniteWedgePropertyForReducedTopologicalKTheory}
###### Example
**(finite [[wedge axiom]])**

Let $(X,x)$ and $(Y,y)$ be two [[pointed topological space|pointed]] [[compact Hausdorff spaces]]
with [[wedge sum]]

$$
  X \vee Y \;\coloneqq\; (X \sqcup Y)/(x \sim y)
$$

(i.e. the [[quotient topological space|quotient]] of their [[disjoint union space]] by re-identifying the base points).

Then there is an [[isomorphism]]

$$
  \tilde K(X \vee Y) \simeq \tilde K(X) \oplus \tilde K(Y)
  \,.
$$

=--

+-- {: .proof}
###### Proof

We have [[retracts]]

$$
  X = X \times \{y\} \hookrightarrow X \times Y
$$

and

$$
  Y = \{x\} \times Y \hookrightarrow (X \times Y) / (X \times \{y\})
  \,.
$$

Applying prop. \ref{DirectSumOfKTheoryGroupsOverRetracts} to each of these consecutively yields an
isomorphism that establishes the claim:

$$
  \tilde K(X \times Y)
    \simeq
  \tilde K(X)
    \oplus
  \tilde K( (X \times Y)/(X \times \{y\}) )
    \simeq
  \tilde K(X) \oplus \tilde K(Y) \oplus \tilde K(X \wedge Y)
  \,.
$$

This proves the claim.

Alternatively, we may again argue directly from the long exact sequence:

Consider the subspace inclusion

$$
  X \subset X \vee Y
  \,.
$$

This is a [[closed subspace]] because its [[complement]] is $(X \vee Y) \setminus X = Y \setminus \{y\}$ which is
open because all points in a [[Hausdorff space]] (which is in particular $T_1$-[[separation axiom|separated]]) are closed.
Moreover, by definition of [[wedge sum]] the corresponding [[quotient space]] is $Y$:

$$
  (X \vee Y) / X \simeq Y
  \,.
$$

Similary for the inclusion of $Y$. Hence in particular these inclusions and quotients are [[retractions]] in that they factor the [[identity maps]]
as

$$
  id_X \;\colon\; X \longrightarrow X \vee Y \longrightarrow X
  \phantom{AA}
    \text{and}
  \phantom{AA}
  id_Y \;\colon\; Y \longrightarrow X \vee Y \longrightarrow Y
  \,.
$$

By functoriality (remark \ref{FunctorialityOfReducedKGroups}) this implies that similarly

$$
  id_{\tilde K(X)}
    \;\colon\;
  \tilde K(X) \longrightarrow \tilde K(X \vee Y) \longrightarrow \tilde K(X)
  \phantom{AA}
   \text{and}
  \phantom{AA}
  id_{\tilde K(Y)}
    \;\colon\;
  \tilde K(Y) \longrightarrow \tilde K(X \vee Y) \longrightarrow \tilde K(Y)
  \,.
$$

In particular these maps are [[injective function|injections]] and [[surjective function|surjections]],
respectively.

Therefore by prop. \ref{ExactSequenceInReducedTopologicalKTheory} there are [[short exact sequences]] of the form

$$
  0
    \to
  \tilde K(X)
    \longrightarrow
  \tilde K(X \vee Y)
    \longrightarrow
  \tilde K(Y)
    \to
  0
$$

which are [[split exact sequences|split exact]]. This implies the claim.

=--


### External product
 {#ExternalProducts}

+-- {: .num_defn #ExternalTensorProductInKTheory}
###### Definition
**(external product in K-theory)**

Let $X$ and $Y$ be [[topological spaces]]. Then the [[external tensor product of vector bundles|external tensor product]]
of [[topological vector bundles]] over $X$ and $Y$

$$
  \boxtimes
    \;\colon\;
  Vect(X) \times Vect(Y)
    \longrightarrow
  Vect(X \times Y)
$$

induces on K-groups an _external product_

$$
  \boxtimes
    \;\colon\;
  K(X) \oplus K(Y)
    \longrightarrow
  K(X \times Y)
$$


=--

We want to see that this restricts to an operation on [[reduced K-theory]].
To this end we need the following proposition:


+-- {: .num_prop #ReducedKTheoryOfProductSpace}
###### Proposition
**(reduced K-theory of product space)**

Let $(X,x_0)$ $(Y,y_0)$ be two [[pointed topological space|pointed]] [[compact Hausdorff spaces]] with
$X \times Y$ their [[product topological space]] and
$X \wedge Y$ their [[smash product]]. Then there is an isomorphism of [[reduced K-theory]] groups

$$
  \tilde K(X \times Y)
    \;\simeq\;
  \tilde K(X \wedge Y)
    \oplus
  \tilde K(X)
    \oplus
  \tilde K(Y)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Be definition, the [[smash product]] is the [[quotient topological space]] of the [[product topological space]]
by the [[wedge sum]]:

$$
  X \wedge Y
  \;=\;
  (X \times Y) / (X \vee Y)
$$

for the inclusion

$$
  \array{
    X \vee Y &\overset{i}{\longrightarrow}& X \times Y
    \\
    x &\mapsto& (x, y_0)
    \\
    y &\mapsto& (x_0, y)
  }
  \,.
$$

This quotient is still a [[compact topological space]] because [[continuous images of compact spaces are compact]]
and and it is still [[Hausdorff topological space]]
because [[compact subspaces in Hausdorff spaces are separated by neighbourhoods from points]], so that
the point $(X \vee Y)/ (X \vee Y) \in (X \times Y)/(X \vee Y)$ is separated by open neighbourhoods from points
in $(X \times Y) \setminus (X \vee Y)$.

Hence corollary \ref{LongExactSequenceInReducedTopologicalKTheory} yields a [[long exact sequence]] of the form

$$
  \tilde K(\Sigma(X \times Y))
    \overset{\Sigma i^\ast}{\longrightarrow}
  \tilde K( (\Sigma X) \vee (\Sigma Y))
    \longrightarrow
  \tilde K( X \wedge Y )
    \longrightarrow
  \tilde K( X \times Y )
    \overset{i^\ast}{\longrightarrow}
  \tilde K(X \vee Y)
  \,.
$$

By example \ref{FiniteWedgePropertyForReducedTopologicalKTheory} the two terms involving
reduced topological K-theory of a wedge sum are direct sums of the reduced K-theory of the wedge summands:

$$
  \tilde K(\Sigma(X \times Y))
    \overset{\Sigma i^\ast}{\longrightarrow}
  \tilde K(\Sigma X) \oplus \tilde K(\Sigma Y)
    \longrightarrow
  \tilde K( X \wedge Y )
    \longrightarrow
  \tilde K( X \times Y )
    \overset{i^\ast}{\longrightarrow}
  \tilde K(X) \oplus \tilde K(Y)
  \,.
$$

Now observe that, via example \ref{FiniteWedgePropertyForReducedTopologicalKTheory}, the morphisms $i^\ast$ and $\Sigma i^\ast$ are [[split epimorphisms]],
with [[section]] given by "external direct sum"

$$
  \array{
    \tilde K(X) \oplus \tilde K(Y)
      &\longrightarrow&
    \tilde K(X \times Y)
    \\
    (E_X, E_Y)
      &\mapsto&
    p_X^\ast(E_X) + p_Y^\ast(E_Y)
  }
  \,.
$$

This means that the long exact sequence decomposes into [[short exact sequences]]

$$
  0
   \to
  \tilde K(X \wedge Y)
    \longrightarrow
  \tilde K(X \times Y)
    \overset{i^\ast}{\longrightarrow}
  \tilde K(X) \oplus \tilde K(Y)
    \to
  0
$$

which moreover are [[split exact sequence|split exact]]. This yields the claim.


=--

It follows that:

+-- {: .num_prop #ExternalTensorProductOnReducedKGroups}
###### Proposition
**(external product on reduced K-groups)**

Let $X$ and $Y$ be [[pointed topological space|pointed]] [[compact Hausdorff spaces]].
Then the external product on K-groups (def. \ref{ExternalTensorProductInKTheory})
restricts to [[reduced K-groups]] under the inclusion $\tilde K(-) \hookrightarrow K(-)$
from prop. \ref{KGrupDirectSummandReducedKGroup} and the inclusion $\tilde K(-\wedge -) \hookrightarrow K(-\times -)$
from prop. \ref{ReducedKTheoryOfProductSpace}, in that there is a morphism $\tilde \boxtimes$
that makes the following [[commuting diagram|diagram commute]]:

$$
  \array{
    \tilde K(X) \oplus \tilde K(Y)
      &\hookrightarrow&
    K(X) \oplus K(Y)
    \\
    {}^{\mathllap{\tilde \boxtimes}}\downarrow && \downarrow^{\mathrlap{\boxtimes}}
    \\
    \tilde K(X \wedge Y) &\hookrightarrow& K(X \times Y)
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{KGrupDirectSummandReducedKGroup} the elements in $\tilde K(X)$ and $\tilde K(Y)$
are represented by [[virtual vector bundles]] which vanish when restricted to the base points
$x \in X$ and $y \in Y$, respectively. But this implies that their [[external tensor product of vector bundles]]
vanishes over $X \times \{y\}$ and $\{x\} \times Y$. From the proof of prop. \ref{ReducedKTheoryOfProductSpace}
it is the restriction of the product to to these subspaces that gives the map


$$
  K(X \times Y) \simeq \tilde K(X \times Y) \oplus \tilde K(X) \oplus \tilde K(Y)
    \longrightarrow
  \tilde K(X) \oplus \tilde K(Y)
$$

and hence on these element this component vanishes.

=--





### Fundamental product theorem

In order to compute K-classes, one needs the computation of some basic cases, such as that of the K-theory groups
of [[n-spheres]] and of [[product spaces]] with $n$-spheres. The _[[fundamental product theorem in K-theory]]_
determines these K-theory groups. Its result is most succinctly summarized by the statement of _[[Bott periodicity]]_,
to which we turn [below](#BottPeriodicities).

Before discussing the product theorem, it is useful to recall the analogous
situation in [[ordinary cohomology]] $H^\bullet(-) \coloneqq H^\bullet(\mathbb{Z})$.
Here it is immediate to determine the cohomology groups of the [[n-spheres]], in particular one finds that
for the [[2-sphere]] is $H^\bullet(S^2) = \mathbb{Z}\langle e\rangle \oplus \mathbb{Z}\langle h\rangle $,
for $h \in \tilde H^2(S^2)$ the [[first Chern class]] of the
[[basic complex line bundle on the 2-sphere]]. As  a ring this has the trivial product $h^2 = 0$,
since by degree-reasons the [[cup product]] goes $H^2(S^2) \otimes H^2(S^2) \to H^4(S^2) = 0$.

Therefore me may write the ordinary [[cohomology ring]] of the 2-sphere as the following [[quotient ring]] of the [[polynomial ring]]
in the generator $h$:

$$
  H^\bullet(S^2) \simeq \mathbb{Z}[h]/\left( (h)^2 \right)
  \,.
$$

Notice that in ordinary cohomology $h$ is also the generator of the [[reduced cohomology]] group $\tilde H^\bullet(S^2) \simeq \mathbb{Z}\langle h\rangle$.
Now as an element of $K_{\mathbb{C}}(S^2)$ the [[basic complex line bundle on the 2-sphere]] is not reduced, but its image in
[[reduced K-theory]] is the [[Bott element]] [[virtual vector bundle]] $\beta = h-1$ (def. \ref{BottElement}).
The [[fundamental product theorem in topological K-theory]] says, in particular, that the complex topological K-theory
of the 2-sphere behaves in just the same way as the ordinary cohomology, if only one replaces the generator $h$ by $\beta = h-1$.

First of all, the Bott element also squares to zero:

+-- {: .num_prop #BottElementNilotentcy}
###### Proposition
**(nilpotency of the [[Bott element]])**

For $S^2 \subset \mathbb{R}^3$ the [[2-sphere]] with its [[Euclidean space|Euclidean]] [[subspace topology]],
write $h \in Vect_{\mathbb{C}}(S^2)_{/\sim}$ for the [[basic complex line bundle on the 2-sphere]]. Its image in the [[topological K-theory]] ring $K(S^2)$ satisfies the relation

$$
  2 h = h^2 + 1
  \;\;\Leftrightarrow\;\;
  (h-1)^2 = 0
$$

=--

A **proof** of this may be obtained by analysis of the
relevant [[clutching function]], see _[here](basic+complex+line+bundle+on+the+2-sphere#TensorRelationForBasicLineBundleOn2Sphere)_.

Notice that $h-1$ is the image of $h$ in the [[reduced K-theory]] $\tilde K(X)$ of $S^2$ under the splitting $K(X) \simeq \tilde K(X) \oplus \mathbb{Z}$ (by [this prop.](topological+K-theory#KGrupDirectSummandReducedKGroup)). This element

$$
  h - 1 \in \tilde K_{\mathbb{C}}(S^2)
$$

is the _[[Bott element]]_ of complex [[topological K-theory]] (def. \ref{BottElement}).

It follows from prop. \ref{BottElementNilotentcy} that there is a [[ring homomorphism]] of the form

$$
  \array{
    \mathbb{Z}[h]/\left( (h-1)^2 \right)
      &\overset{}{\longrightarrow}&
    K(S^2)
    \\
    h &\overset{\phantom{AAA}}{\mapsto}& h
  }
$$

from the [[polynomial ring]] in one abstract generator, [[quotient ring|quotiented]] by this relation, to the [[topological K-theory]] ring.

More generally, for $X$ a [[topological space]], then this induces the composite ring homomorphism

$$
  \array{
    K(X) \otimes \mathbb{Z}[h]/\left((h-1)^2 \right)
      & \longrightarrow &
    K(X) \otimes K(S^2)
      & \overset{\boxtimes}{\longrightarrow} &
    K(X \times S^2)
    \\
    (E, h)
      &\overset{\phantom{AAA} }{\mapsto}&
    (E,H)
      &\overset{\phantom{AAA}}{\mapsto}&
    (\pi_{X}^\ast E) \cdot (\pi_{S^2}^\ast H)
  }
$$

to the topological K-theory ring of the [[product topological space]] $X \times S^2$,
where the second map $\boxtimes$ is the external product from def. \ref{ExternalTensorProductInKTheory}.

+-- {: .num_prop #FundamentalProductTheorem}
###### Proposition
**([[fundamental product theorem in topological K-theory]])**

For $X$ a [[compact Hausdorff space]], then this ring homomorphism is an [[isomorphism]].

=--

(e.g. [Hatcher, theorem 2.2](#Hatcher))

+-- {: .num_remark}
###### Remark

More generally, for $L\to X$ a [[complex line bundle]] with class $l \in K(X)$ and with $P(1 \oplus L)$ denoting its [[projective bundle]] then

$$
  K(X)[h]/((h-1)(l \cdot h -1))
   \simeq
  K(P(1 \oplus L))
$$

=--

(e.g. [Wirthmuller 12, p. 17](#Wirthmuller12))

As a special case this implies the first statement above:


For $X = \ast$ the product theorem prop. \ref{FundamentalProductTheorem} says in particular that the first of the two morphisms in the composite is an [[isomorphism]] (example \ref{TopologicalKTheoryRingOfThe2Sphere} below)  and
hence by the [[two-out-of-three]]-property for [[isomorphisms]] it follows that:

+-- {: .num_cor #ExternalProductTheorem}
###### Corollary
**([[external product theorem in topological K-theory]])**

For $X$ a [[compact Hausdorff space]] we have that the external product in K-theory $\boxtimes$ (def. \ref{ExternalTensorProductInKTheory})
with vector bundles on the [[2-sphere]]

$$
  \boxtimes
    \;\colon\;
  K(X) \otimes K(S^2) \overset{\simeq}{\longrightarrow} K(X \times S^2)
$$

is an [[isomorphism]] in [[topological K-theory]].

=--




### Bott periodicity
 {#BottPeriodicities}


When restricted to [[reduced K-theory]] then the external product theorem (cor. \ref{ExternalProductTheorem}) yields the statement of [[Bott periodicity]] of topological K-theory:

+-- {: .num_prop #BottPeriodicity}
###### Proposition
**([[Bott periodicity]])

Let $X$ be a  [[pointed topological space|pointed]] [[compact Hausdorff space]].

Then the external product $\tilde X$ in reduced K-theory (prop. \ref{ExternalTensorProductInKTheory})
with the image of the [[basic complex line bundle on the 2-sphere]] in reduced K-theory yields an [[isomorphism]] of [[reduced K-groups]]

$$
  (h-1)
    \widetilde \boxtimes
  (-)
    \;\colon\;
  \tilde K(X) \overset{\simeq}{\longrightarrow} \tilde K(\Sigma^2 X)
$$

from that of $X$ to that of its double [[suspension]] $\Sigma^2 X$.

=--

[e.g. Wirthmuller 12, p. 34 (36 of 67)](#Wirthmuller12)

+-- {: .proof}
###### Proof

By [this example](topologica+K-theory#ReducedKTheoryOfProductSpace)
there is for any two pointed compact Hausdorff spaces $X$ and $Y$ an [[isomorphism]]

$$
  \tilde K(Y \times X)
    \simeq
  \tilde K(Y \wedge X)
    \oplus
  \tilde K(Y)
    \oplus
  \tilde K(X)
$$

relating the reduced K-theory of the [[product topological space]]
with that of the [[smash product]].

Using this and the fact that for any pointed compact Hausdorff space $Z$ we have
$K(Z) \simeq \tilde K(Z) \oplus \mathbb{Z}$ ([this prop.](topological+K-theory#KGrupDirectSummandReducedKGroup)) the isomorphism of the external product theorem (cor. \ref{ExternalProductTheorem})

$$
  K(S^2) \otimes K(X)
   \underoverset{\simeq}{\boxtimes}{\longrightarrow}
  K(S^2 \times X)
$$

becomes

$$
  \left(
    \tilde K(S^2) \oplus \mathbb{Z}
  \right)
    \otimes
  \left(
     \tilde K(X) \oplus \mathbb{Z}
  \right)
   \;\simeq\;
  \left(
    \tilde K(S^2 \times X)
     \oplus
     \mathbb{Z}
  \right)
   \simeq
  \left(
    \tilde K(S^2 \wedge X)
      \oplus
    \tilde K(S^2)
      \oplus
    \tilde K(X)
      \oplus
    \mathbb{Z}
  \right)
  \,.
$$

Multiplying out and chasing through the constructions to see that this reduces to an isomorphism on the common summand $\tilde K(S^2) \oplus \tilde K(X) \oplus \mathbb{Z}$, this yields an isomorphism of the form

$$
  \tilde K(S^2) \otimes \tilde K(X)
    \underoverset{\simeq}{\widetilde \boxtimes}{\longrightarrow}
  \tilde K(S^2 \wedge X)
    =
  \tilde K(\Sigma^2 X)
  \,,
$$

where on the right we used that [[smash product]] with the 2-sphere is the same as double [[suspension]].

Finally there is an [[isomorphism]]

$$
  \array{
    \mathbb{Z}
      &\underoverset{\simeq}{ \beta }{\longrightarrow}&
    \tilde K_{\mathbb{C}}(S^2)
    \\
    1 &\overset{\phantom{AAA}}{\mapsto}& (h-1)
  }
$$

(example \ref{TopologicalKTheoryRingOfThe2Sphere}). The composite

$$
  \array{
    \tilde K_{\mathbb{C}}(X)
      &
      \simeq
    \mathbb{Z} \otimes \tilde K_{\mathbb{C}}(X)
      \overset{ \beta \otimes id }{\longrightarrow}
    \tilde K_{\mathbb{C}}(S^2) \otimes \tilde K_{\mathbb{C}}(X)
      \underoverset{\simeq}{\widetilde \boxtimes}{\longrightarrow}
      &
    \tilde K_{\mathbb{C}}(S^2 \wedge X)
      =
    \tilde K_{\mathbb{C}}(\Sigma^2 X)
    \\
    E - rk_x(E) &\overset{\phantom{AAAA}}{\mapsto}& (h-1) \widetilde \boxtimes (E - rk_x(E))
  }
$$

is the isomorphism to be established.

=--



### Graded-commutative ring structure
 {#GradedRingStructure}

The external product on reduced K-groups from
prop. \ref{ExternalTensorProductOnReducedKGroups}
allows to extend the [[commutative ring]] structure from the plain K-groups (remark \ref{KTheoryRing})
to a ring structure on the graded K-groups from def. \ref{GradedKGroups}. This is def. \ref{ProductOnGradedKGroups} below.

To state this definition, recall that

1. for $X$ a [[pointed topological space]] then the [[diagonal]] map to its [[product topological space]] $X \times X$
   induced a diagonal to the [[smash product]] $X \wedge X = (X \times X)/(X \vee X)$

   $$
     X \overset{\Delta_X}{\longrightarrow} X \times X \overset{q}{\longrightarrow} X\wedge X
   $$

1. since [[reduced suspension]] is equivalently [[smash product]] with the [[circle]] $\Sigma X \simeq S^1 \wedge X$,
   there are induced "partial diagonal maps" of the form

   $$
     \Sigma (q \circ \Delta_X)
      \;\colon\;
     \Sigma X \simeq S^1 \wedge X \overset{S^1 \wedge (q\circ \Delta_X)}{\longrightarrow} S^1 \wedge X \wedge X \simeq (\Sigma X) \wedge X
   $$

   etc.

+-- {: .num_defn #ProductOnGradedKGroups}
###### Definition
**(product on graded K-groups)**

For $X$ a [[pointed topological space|pointed]] [[compact Hausdorff space]], the _product on graded K-groups_

$$
  (-)\cdot (-)
    \;\colon\;
  K^\bullet(X) \otimes K^\bullet(X)
    \longrightarrow
  K^\bullet(X)
$$

is the [[linear map]] which on the direct summands $\tilde K^0(X) \coloneqq \tilde K(X)$ and $\tilde K^1(X) \coloneqq \tilde K(\Sigma X)$
is given by the following morphisms, which are [[composition|composites]] of the external product $\tilde \boxtimes$ on reduced K-groups
from prop. \ref{ExternalTensorProductOnReducedKGroups} with pullbacks along the above suspended diagonal maps:

$$
  \tilde K(X) \otimes \tilde K(X)
    \overset{\tilde \boxtimes}{\longrightarrow}
  \tilde K(X)
$$

$$
  \tilde K(X) \otimes \tilde K(\Sigma X)
    \overset{\tilde \boxtimes}{\longrightarrow}
  \tilde K(X \wedge (\Sigma X))
    \overset{ (\Sigma(q \circ \Delta_X))^\ast }{\longrightarrow}
  \tilde K(\Sigma X)
$$

$$
  \tilde K(\Sigma X) \otimes \tilde K(\Sigma X)
    \overset{\tilde \boxtimes}{\longrightarrow}
  \tilde K( (\Sigma X) \wedge (\Sigma X))
    \overset{ (\Sigma^2(q \circ \Delta_X))^\ast }{\longrightarrow}
  \tilde K(\Sigma^2 X)
    \simeq
  \tilde K(X)
  \,,
$$

where the last isomorphism on the right is [[Bott periodicity]] isomorphism (prop. \ref{BottPeriodicity}).

=--




### Classifying space
 {#ClassifyingSpace}

We discuss how the [[classifying space]] for $\tilde K^0$ is the [[delooping]] of the [[stable unitary group]].

+-- {: .num_defn #BUn}
###### Definition
**([[classifying space]] of the [[stable unitary group]])**

For $n \in \mathbb{N}$ write $U(n)$ for the [[unitary group]] in dimension $n$ and $O(n)$ for the [[orthogonal group]]
in dimension $n$, both regarded as [[topological groups]] in the standard way. Write $B U(n) , B O(n)\in $ [[Top]] for the corresponding [[classifying space]].

Write

$$
  [X, B O(n)] := \pi_0 Top(X, B O(n))
$$

and

$$
  [X, B U(n)] := \pi_0 Top(X, B U(n))
$$

for the set of [[homotopy]]-classes of [[continuous function]]s $X \to B U(n)$.

=--

+-- {: .num_prop #BUnClassifyingSpace}
###### Proposition

This is equivalently the set of [[isomorphism]] classes of $O(n)$- or $U(n)$-[[principal bundle]]s  on $X$ as well as of rank-$n$ real or complex [[vector bundle]]s on $X$, respectively:

$$
  [X, B O(n)] \simeq O(n) Bund(X) \simeq Vect_{\mathbb{R}}(X,n)
  \,,
$$

$$
  [X, B U(n)] \simeq U(n) Bund(X) \simeq Vect_{\mathbb{C}}(X,n)
  \,.
$$

=--

+-- {: .num_defn #InclusionOfUns}
###### Definition

For each $n$ let

$$
  U(n) \to U(n+1)
$$

be the inclusion of [[topological group]]s given by inclusion of $n \times n$ [[matrices]] into $(n+1) \times (n+1)$-matrices given by the block-diagonal form

$$
  \left[g\right] \mapsto
  \left[
    \array{
      1 & [0]
      \\
      [0] & [g]
    }
  \right]
  \,.
$$

This induces a corresponding sequence of morphisms of classifying spaces, def. \ref{BUn}, in [[Top]]

$$
  B U(0) \hookrightarrow B U(1) \hookrightarrow B U(2) \hookrightarrow \cdots
  \,.
$$

Write

$$
  B U := {\lim_{\to}}_{n \in \mathbb{N}} B U(n)
$$

for the [[homotopy colimit]] (the "homotopy [[direct limit]]") over this diagram (see at _[[homotopy colimit]]_ the section _[Sequential homotopy colimits](homotopy+limit#SequentialHocolims)_).

=--

+-- {: .num_remark }
###### Remark

The [[topological space]] $B U$ is **not** equivalent to $B U(\mathcal{H}) $, where $U(\mathcal{H})$ is the [[unitary group]] on a separable infinite-dimensional [[Hilbert space]] $\mathcal{H}$. In fact the latter is [[contractible]], hence has a  [[weak homotopy equivalence]] to the point

$$
  B U(\mathcal{H}) \simeq *
$$

while $B U$ has nontrivial [[homotopy group]]s in arbitrary higher degree (by [[Kuiper's theorem]]).

But there is the group $U(\mathcal{H})_{\mathcal{K}} \subset U(\mathcal{H})$ of unitary operators that differ from the [[identity]] by a [[compact operator]]. This is essentially $U = \Omega B U$. See [below](#Uk).

=--

+-- {: .num_prop }
###### Proposition

Write $\mathbb{Z}$ for the set of [[integer]]s regarded as a [[discrete topological space]].

The product spaces

$$
  B O \times \mathbb{Z}\,,\;\;\;\;\;B U \times \mathbb{Z}
$$

are [[classifying spaces]] for real and complex $K$-theory, respectively: for every compact Hausdorff topological space $X$, we have an isomorphism of groups

$$
  \tilde K(X)
  \simeq
  [X, B U ]
  \,.
$$


$$
  K(X)
  \simeq
  [X, B U \times \mathbb{Z}]
  \,.
$$

=--

See for instance ([Friedlander, prop. 3.2](#Friedlander)) or ([Karoubi, prop. 1.32, theorem 1.33](#Karoubi)).

+-- {: .proof}
###### Proof

First consider the statement for reduced cohomology $\tilde K(X)$:

Since a [[compact topological space]] is a [[compact object]] in [[Top]] (and using that the [[classifying spaces]] $B U(n)$ are (see there) [[paracompact topological space]]s, hence normal, and since the inclusion morphisms are closed inclusions (...)) the [[hom-functor]] out of it commutes with the [[filtered colimit]]

$$
  \begin{aligned}
    Top(X, B U)
    &=
    Top(X, {\lim_\to}_n B U(n))
    \\
    & \simeq {\lim_\to}_n Top(X, B U (n))
  \end{aligned}
  \,.
$$

Since $[X, B U(n)] \simeq U(n) Bund(X)$, in the last line the colimit is over [[vector bundle]]s of all ranks and identifies two if they become isomorphic after adding a trivial bundle of some finite rank.

For the full statement use that by prop. \ref{missing} we have

$$
  K(X) \simeq H^0(X, \mathbb{Z}) \oplus \tilde K(X)
  \,.
$$

Because $H^0(X,\mathbb{Z}) \simeq [X, \mathbb{Z}]$ it follows that

$$
  H^0(X, \mathbb{Z}) \oplus \tilde K(X)
  \simeq
  [X, \mathbb{Z}] \times [X, B U]
  \simeq
  [X, B U \times \mathbb{Z}]
  \,.
$$

=--

There is another variant on the classifying space

+-- {: .num_defn #Uk}
###### Definition

Let

$$
  U_{\mathcal{K}}
  =
  \left\{
    g \in U(\mathcal{H}) | g - id \in \mathcal{K}
  \right\}
$$

be the group of unitary operators on a [[separable Hilbert space]] $\mathcal{H}$ which differ from the identity by a [[compact operator]].

=--

Palais showed that


+-- {: .num_prop }
###### Proposition

$U_\mathcal{K}$ is a [[homotopy equivalence|homotopy equivalent]] model for $B U$. It is in fact the [[norm closure]] of the evident model of $B U$ in $U(\mathcal{H})$.

Moreover $U_{\mathcal{K}} \subset U(\mathcal{H})$ is a [[Banach Lie group|Banach Lie]] [[normal subgroup]].

=--

Since $U(\mathcal{H})$ is [[contractible]], it follows that

$$
  B U_{\mathcal{K}} \coloneqq U(\mathcal{H})/U_{\mathcal{K}}
$$

is a model for the [[classifying space]] of reduced K-theory.


### Of non-compact spaces

For $G$ a compact Lie group with [[classifying space]] $B G$ (in general non-compact)
then the map from the [[Grothendieck group]] $\mathbb{K}(B G) \coloneqq Grp(Vect(B G)/_\sim, \oplus)$
(def. \ref{GrothendieckGroupKTheory})
to the representable K-theory $K(B G)_{rep} \coloneqq [X, B U \times\mathbb{Z}]$
(def. \ref{RepresntableTopologicalKTheory}) is
[[injective function|injective]]

$$
   \mathbb{K}(B G) \hookrightarrow K(B G)_{rep}
   \,.
$$

[Jackowski-Oliver](#JackowskiOliver)


### As a generalized cohomology theory
 {#AsAGeneralizedCohomologyTheory}

Topological K-theory satisfies the axioms of a [[generalized (Eilenberg-Steenrod) cohomology theory]]
([Atiyah-Hirzebruch 61, 1.8](#AtiyahHirzebruch61)).

This is essentially the statement of the long exact sequences [above](#ExactSequences).


### Complex orientation and formal group law
 {#ComplexOrientationAndFormalGroupLaw}

A [[multiplicative cohomology theory|multiplicative]] [[generalized (Eilenberg-Steenrod) cohomology]] theory $E$ is called _[[complex oriented cohomology|complex orientable]]_
if the element $1 \in E(\ast) \simeq \tilde E(S^0)$ is in the image of the pullback morphism

$$
  \tilde i^\ast \;\colon\; \tilde E^2(B U(1)) \longrightarrow \tilde E^2(S^2) \simeq \tilde E^0(S^0)
  \,.
$$

If so, then a choice of pre-image $c^E_1 \in E^2(B U(1))$ is a choice of _complex orientation_ ([this def.](complex+oriented+cohomology+theory#ComplexOrientedCohomologyTheory)).

Now for $E = K_{\mathbb{C}}$ being complex topological K-theory regarded as a generalized cohomology theory
as [above](#AsAGeneralizedCohomologyTheory), then by [[Bott periodicity]] (prop. \ref{BottPeriodicity})
and by $\tilde K_{\mathbb{Z}}(S^2) \simeq \mathbb{Z} \cdot (h-1)$ (example \ref{ComplexTopologicalKTheoryOfTheCircle})
this reduces to the statement that there is an element $c^K_1 \in \tilde K_{\mathbb{C}}(B U(1))$ such that its image
under

$$
  \tilde i^\ast
    \;\colon\;
  \tilde K_{\mathbb{C}}(B U(1))
    \longrightarrow
  \tilde K_{\mathbb{C}}(S^2)
    \simeq
  \mathbb{Z} \cdot (h-1)
$$

is the [[Bott element]] $h-1$, the [[virtual vector bundle]] difference between the [[basic complex line bundle on the 2-sphere]]
and the [[trivial vector bundle|trivial]] [[complex line bundle]].

By the very nature of the [[basic complex line bundle on the 2-sphere]] $h$, it is the restriction of the [[universal complex line bundle|universal]]/[[tautological line bundle|tautological]] [[complex line bundle]] $\mathcal{O}(1)$ on $B U(1) \simeq \mathbb{C}P^\infty$ along the defining cell inclusion $i \colon S^2 \hookrightarrow \mathbb{C}P^\infty \simeq B U(1)$.
Hence if we set

$$
  c_K^1 \;\coloneqq\; \mathcal{O}(1)-1 \; \in \tilde K_{\mathbb{C}}(B U(1))
$$

then this is a [[complex oriented cohomology|complex orientation]] for complex topological K-theory.

From this we obtain the [[formal group law]] associated with topological K-theory (from [this prop.](complex+oriented+cohomology+theory#ComplexOrientedCohomologyTheoryFormalGroupLaw)):

By the nature of the [[classifying space]] $B U(1)$ we have that for

$$
  \mu \;\colon\; B U(1) \times B U(1) \longrightarrow B U(1)
$$

the group product operation, which classifies the [[tensor product of vector bundles|tensor product of line bundles]], that

$$
  \mu^\ast \mathcal{O}(1) \simeq pr_1^\ast \mathcal{O}(1) \otimes_{B U(1)} pr_2^\ast \mathcal{O}(1)
  \,,
$$

where

$$
  pr_i\colon B U(1) \times B U(1) \to B U(1)
$$

are the two [[projections]] out of the [[Cartesian product]]. Hence

$$
  \begin{aligned}
    \mu^\ast c_1^K
    &\coloneqq
    \mu^\ast (\mathcal{O}(1) - 1)
    \\
      & =
    \left(pr_1^\ast \mathcal{O}(1)\right)  \cdot  \left(pr_2^\ast \mathcal{O}(1)\right) - 1
    \\
      &  =
    \left(pr_1^\ast (\mathcal{O}(1) -1)\right) \cdot \left(pr_2^\ast( \mathcal{O}(1) -1)\right)
    + pr_1^\ast \mathcal{O}(1)
    + pr_2^\ast \mathcal{O}(2)
    - 2
    \\
     & =
    \left(pr_1^\ast (\mathcal{O}(1) -1)\right) \cdot \left(pr_2^\ast( \mathcal{O}(1) -1)\right)
     +
    \left(pr_1^\ast \mathcal{O}(1) - 1\right)
     +
    \left(pr_2^\ast \mathcal{O}(1) - 1\right)
  \end{aligned}
$$

This shows that the [[formal group law]] associated with the complex orientation of complex topological K-theory
is that of the _[[formal multiplicative group]]_ given by

$$
  f(x,y) = x + y + x y
  \,.
$$


### Spectrum

Being a [[generalized (Eilenberg-Steenrod) cohomology]] theory, topological K-theory is represented by a [[spectrum]]: the _[[K-theory spectrum]]_.

e.g. [Switzer 75, p. 216](#Switzer75)

The degree-0 part of this spectrum, i.e. the classifying space for degree 0 topological $K$-theory is modeled in particular by the space $Fred$ of [[Fredholm operator]]s.

### Ring spectrum

This [[K-theory]] spectrum has the structure of a [[ring spectrum]]

(e.g. [Switzer 75, section 13.90, around p. 300](#Switzer75),

see also p. 205 (213 of 251) in _[[A Concise Course in Algebraic Topology]]_)

(...)


### Chromatic filtration

[[!include chromatic tower examples - table]]

### As the shape of the smooth K-theory spectrum

See at _[[differential cohomology diagram]]_.

### Relation to algebraic K-theory
 {#RelationToAlgebraicKTheory}

The topological K-theory over a space $X$ is not
identical with the _[[algebraic K-theory]]_ of the
ring of functions on $X$, but the two are closely related. See for instance ([Paluch](#Paluch), [Rosenberg](#Rosenberg)).
See at _[[comparison map between algebraic and topological K-theory]]_.




## Related concepts

* [[virtual vector bundle]]

* [[K-theory]]

* **topological K-theory

  * [[Atiyah-Bott-Shapiro isomorphism]]

  * [[topological index]]

  * [[KR-theory]]

  * [[vectorial bundle]]

* [[groupoid K-theory]]

* [[twisted K-theory]]

* [[differential K-theory]]

* [[twisted differential K-theory]]

* [[equivariant K-theory]], [[orbifold K-theory]]

* [[equivariant differential K-theory]], [[orbifold differential K-theory]]

* [[semi-topological K-theory]]

* [[algebraic K-theory]]

* [[iterated K-theory]]

* [[Tate K-theory]]

* [[KU-local stable homotopy theory]]


[[!include orientations in higher quantization - table]]

[[!include string theory and cohomology theory -- table]]


## References

### General

The "ring of complex vector bundles" $K(X)$ was introduced in

* {#AtiyahHirzebruch61} [[M. F. Atiyah]], [[F. Hirzebruch]], _Riemann-Roch theorems for differentiable manifolds_, Bull.  Amer. Math Soc. vol. 65 (1959) pp. 276-281 ([euclid:bams/1183523205](https://projecteuclid.org/euclid.bams/1183523205))

and shown to give a [[Whitehead-generalized cohomology]] theory in

* {#AtiyahHirzebruch61} [[M. F. Atiyah]], [[F. Hirzebruch]], _Vector bundles and homogeneous spaces_, 1961, Proc. Sympos. Pure Math., Vol. III pp. 7&#8211;38 American Mathematical Society, Providence, R.I. (<a href="https://doi.org/10.1142/9789814401319_0008">doi:10.1142/9789814401319_0008</a>, [web](http://hirzebruch.mpim-bonn.mpg.de/87/), [MR 0139181](http://www.ams.org/mathscinet-getitem?mr=0139181))


Early review:

*  {#Atiyah67}  [[Michael Atiyah]], _K-theory_, Harvard Lecture 1964 (notes by D. W. Anderson), Benjamin 1967 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahk.pdf), [[AtiyahKTheory.pdf:file]])

Representable K-theory over non-compact spaces was considered in

* {#Karoubi70} [[Max Karoubi]], _Espaces Classifiants en K-Th&#233;orie_, Transactions of the American Mathematical Society Vol. 147, No. 1 (Jan., 1970), pp. 75-115  ([jstor](http://www.jstor.org/stable/1995218))

and (over [[classifying spaces]] in the context of [[equivariant K-theory]]) in

* {#SegalAtiyah69} [[Graeme Segal]], [[Michael Atiyah]], section 4 of _Equivariant K-theory and completion_, J. Differential Geometry 3 (1969), 1&#8211;18. MR 0259946 


Early lecture notes on topological K-theory in a general context of [[stable homotopy theory]] and [[generalized cohomology theory]] includes

* {#Adams74} [[Frank Adams]], part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

Textbook accounts:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

  > (in view of [[U-bordism theory]] and the [[e-invariant]])

* {#Switzer75} [[Robert Switzer]], sections 11 and 13.90 of _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975.

* {#Karoubi} [[Max Karoubi]], _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften 226, Springer 1978 ([pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3))

* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-theory_, 2003/2009 ([web](http://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))

* [[Dai Tamaki]], [[Akira Kono]], Section 4.1 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))

Further introductions include

* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], _[[Spin geometry]]_, Princeton University Press (1989)

* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 9 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* {#Courtney04} Dennis Courtney, _A brief glance atK-theory_, 2004 ([pdf](https://math.berkeley.edu/~hutching/teach/215b-2004/courtney.pdf))

* {#Karoubi06} [[Max Karoubi]], _K-theory. An elementary introduction_, lectures given at the Clay Mathematics Academy ([arXiv:math/0602082](https://arxiv.org/abs/math/0602082))

* {#Friedlander} [[Eric Friedlander]], _An introduction to K-theory_ (emphasis on [[algebraic K-theory]]), 2007 ([pdf](http://users.ictp.it/~pub_off/lectures/lns023/Friedlander/Friedlander.pdf))

* {#Karpova09} [[Varvara Karpova]], _Complex topological K-theory_, 2009  ([pdf](http://infoscience.epfl.ch/record/162450/files/karpova.semestre.hess2.pdf), [[KarpovaTopologicalKTheory.pdf:file]])

* {#Blair09} Chris Blair, _Some K-theory examples_, 2009 ([pdf](http://www.maths.tcd.ie/~cblair/notes/kex.pdf))

* {#Wirthmuller12} [[Klaus Wirthmüller]], _Vector bundles and K-theory_, 2012 ([[wirthmueller-vector-bundles-and-k-theory.pdf:file]])

* Aderemi Kuku, _Introduction to K-theory and some applications_ ([pdf](https://www.math.ksu.edu/~zlin/kuku/Intro-Kthy.pdf))

A textbook account of topological K-theory with an eye towards [[operator K-theory]] is section 1 of

* [[Bruce Blackadar]], _[[K-Theory for Operator Algebras]]_


The [[comparison map between algebraic and topological K-theory]] is discussed for instance in

* {#Paluch} Michael Paluch, _Algebraic $K$-theory and topological spaces_ K-theory 0471 ([web](http://www.math.uiuc.edu/K-theory/0471/))


* {#Rosenberg} [[Jonathan Rosenberg]], _Comparison Between Algebraic and Topological K-Theory for Banach Algebras and $C^*$-Algebras_, ([pdf](http://www2.math.umd.edu/~jmr/algtopK.pdf))

Discussion from the point of view of [[smooth stacks]] and [[differential K-theory]] is in

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_, Journal of Homotopy and Related Structures October 2014 ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

The proof of the [[Hopf invariant one]] theorem in terms of topological K-theory is due to

* {#AdamsAtiyah66} [[Frank Adams]], [[Michael Atiyah]], _K-theory and the Hopf invariant_, Quart. J. Math. Oxford (2), 17 (1966), 31-38 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/adamatiy.pdf))

On [[Hopf rings]] of [[ordinary homology]] of topological K-theories:

* [[Neil Strickland]], _Bott periodicity and Hopf rings_, 1992 ([pdf](https://neil-strickland.staff.shef.ac.uk/research/thesis.pdf), [[StricklandHopfRings.pdf:file]])


### For non-compact spaces

Topological K-theory of [[Eilenberg-MacLane spaces]] is discussed in

* {#AndersonHodgkin68} [[Donald W. Anderson]], Luke Hodgkin _The K-theory of Eilenberg-Maclane complexes_, Topology, Volume 7, Issue 3, August 1968, Pages 317-329 ([doi:10.1016/0040-9383(68)90009-8](https://doi.org/10.1016/0040-9383(68)90009-8))

Topological topological K-theory of [[classifying spaces]] of [[Lie groups]] is in

* {#JackowskiOliver} Stefan Jackowski and Bob Oliver, _Vector bundles over classifying spaces of compact Lie groups_ ([pdf](http://hopf.math.purdue.edu/Jackowski-Oliver/bg-bu.pdf))


### D-brane charge

For more see at _[[K-theory classification of D-brane charge]]_.

Discussion of [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type II string theory]] (see also [there](D-brane#ReferencesKTheoryDescription)):

* {#GradySati19a} [[Daniel Grady]], [[Hisham Sati]], _Ramond-Ramond fields and twisted differential K-theory_ ([arXiv:1903.08843](https://arxiv.org/abs/1903.08843))

Discussion of [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[KO-theory|orthogonal]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type I string theory]] (on [[orientifolds]]):

* {#GradySati19b} Daniel Grady, [[Hisham Sati]], _Twisted differential KO-theory_ ([arXiv:1905.09085](https://arxiv.org/abs/1905.09085))

### Topological phases of matter

For more see at _[[K-theory classification of topological phases of matter]]_.


[[!redirects complex K-theory]]

[[!redirects periodic complex K-theory]]


[[!redirects complex topological K-theory]] 
[[!redirects topological complex K-theory]] 

[[!redirects KU-theory]]
[[!redirects KU-cohomology]]
