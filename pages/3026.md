.
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

The _one-point compactification_ of a [[topological space]] $X$ is a new [[compact space]] $X^* = X \cup \{\infty\}$ obtained by adding a single new point "$\infty$" to the original space and declaring in $X^*$ the [[complements]] of the original [[closed subspace|closed]] [[compact space|compact]] [[subspaces]] to be [[open subspace|open]].

One may think of the new point added as the "point at infinity" of the original space. A [[continuous function]] on $X$ _[[vanishing at infinity|vanishes at infinity]]_ precisely if it extends to a continuous function on $X^*$ and literally takes the value zero at the point "$\infty$".

This one-point compactification is also known as the _Alexandroff compactification_ after a 1924 paper by [[Pavel Aleksandrov|Павел Сергеевич Александров]] (then transliterated 'P.S. Aleksandroff'). 

The one-point compactification is usually applied to a non-[[compact space|compact]] [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] space.  In the more general situation, it may not really be a [[compactification]] and hence is called the _one-point extension_ or _Alexandroff extension_.


## Definition

### For topological spaces

+-- {: .num_defn #OnePointExtension}
###### Definition
**(one-point extension)**

Let $X$ be any [[topological space]]. Its **one-point extension** $X^*$ is the topological space 

* whose underlying [[set]] is the [[disjoint union]] $X \cup \{\infty\}$ of that of $X$ with a [[singleton set]] $\{\infty\}$;

* and whose [[open subsets]] are 

  1. the [[open subsets]] of $X \,\subset\, X^*$ ;

  2. the [[complements]] $X^\ast \setminus CK = (X \setminus CK) \cup \{\infty\}$ of the [[closed subspace|closed]] [[compact space|compact]] subsets $CK \subset X$.

=--

([Aleksandrov 24](#Aleksandrov24), see [Kelly 75, p. 150](#Kelly75))

+-- {: .num_remark}
###### Remark

If $X$ is [[Hausdorff space|Hausdorff]], then it is sufficient to speak of compact subsets in def. \ref{OnePointExtension}, since [[compact subspaces of Hausdorff spaces are closed]].

=--

+-- {: .num_lemma #OnePointExtensionWellDefined}
###### Lemma
**(one-point extension is well-defined)**

The [[topological space|topology]] on the one-point extension in def. \ref{OnePointExtension} is indeed well defined in that the given set of subsets is indeed closed under arbitrary unions and finite intersections.

=--

+-- {: .proof}
###### Proof

The unions and finite intersections of the open subsets inherited from $X$ are closed among themselves by the assumption that $X$ is a topological space.

It is hence sufficient to see that 

1. the unions and finite intersection of the $(X \backslash CK) \cup \{\infty\}$ are closed among themselves,

1. the union and intersection of a subset of the form $U \underset{\text{open}}{\subset} X \subset X^\ast$ with one of the form $(X \backslash CK) \cup \{\infty\}$ is again of one of the two kinds.

Regarding the first statement: Under [[de Morgan duality]] 

$$  
  \underset{i \in \underset{\text{finite}}{J}}{\bigcap} (X \backslash CK_i \cup \{\infty\})
  = 
  \left( X \backslash \left(\underset{i \in \underset{\text{finite}}{J}}{\bigcup} CK_i \right)\right) \cup \{\infty\}
$$

and

$$
  \underset{i \in I}{\bigcup} ( X \backslash CK_i \cup \{\infty\} )
  = 
  \left(X \backslash \left(\underset{i \in I}{\bigcap} CK_i \right)\right) \cup \{\infty\}
$$

and so the first statement follows from the fact that finite unions of compact subspaces and arbitrary intersections of closed compact subspaces are themselves again compact ([this prop.](compact+space#UnionsAndIntersectionOfCompactSubspaces)).

Regarding the second statement: That $U \subset X$ is open means that there exists a closed subset $C \subset X$ with $U = X\backslash C$. Now using [[de Morgan duality]] we find

1. for intersections:

   $$
     \begin{aligned}
       U \cap ( (X\backslash CK) \cup \{\infty\} )
       & = 
       (X \backslash C) \cap (X \backslash CK)
       \\
       & =
       X \backslash (C \cup CK).
     \end{aligned}
   $$

   Since finite unions of closed subsets are closed, this is again an open subset of $X$;

2. for unions:

   $$
     \begin{aligned}
       U \cup (X \backslash CK) \cup \{\infty\}
       & = 
       (X \backslash C) \cup (X \backslash CK) \cup \{\infty\}
       \\
       & =
       (X \backslash (C \cap CK)) \cup \{\infty\} .
     \end{aligned}
   $$ 

   For this to be open in $X^\ast$ we need that $C \cap CK$ is again compact. This follows because [[subsets are closed in a closed subspace precisely if they are closed in the ambient space]] and because [[closed subsets of compact spaces are compact]].


=--



### For non-commutative topological spaces ($C^\ast$-algebras)

Dually in [[non-commutative topology]] the one-point compactification corresponds to the [[unitisation of C*-algebras]].


## Properties

### Basic properties
 {#BasicProperties}

We discuss the basic properties of the construction $X^\ast$ in def. \ref{OnePointExtension}, in particular that it always yields a [[compact topological space]] (prop. \ref{OnePointExtensionIsCompact} below) and the ingredients needed to see its [[universal property]] in the Hausdorff case [below](#OnePointExtensionIsCompact).

+-- {: .num_prop #OnePointExtensionIsCompact}
###### Proposition
**(one-point extension is compact)**

For $X$ any [[topological space]], we have that its one-point extension $X^\ast$ (def. \ref{OnePointExtension}) is a [[compact topological space]].

=--

+-- {: .proof}
###### Proof

Let $\{U_i \subset X^\ast\}_{i \in I}$ be an [[open cover]].  We need to show that this has a finite subcover.

That we have a cover means that 

1. there must exist $i_\infty \in I$ such that $U_{i \infty} \supset \{\infty\}$ is an [[open neighbourhood]] of the extra point. But since, by construction, the only open subsets containing that point are of the form $(X \backslash CK) \cup \{\infty\}$, it follows that there is a compact closed subset $CK \subset X$ with $X \backslash CK \subset U_{i \infty}$. 

1. $\{U_i \subset X\}_{i \in i}$ is in particular an open cover of that closed compact subset $CK \subset X$. This being compact means that there is a finite subset $J \subset I$ so that $\{U_i \subset X\}_{i \in \J \subset X}$ is still a cover of $CK$. 

Together this implies that 

$$
  \{U_i \subset X\}_{i \in J \subset I}
  \cup
  \{ U_{i_\infty} \}
$$

is a finite subcover of the original cover.


=--

+-- {: .num_prop #HausdorffOnePointCompactification}
###### Proposition
**(one-point extension of locally compact space is Hausdorff precisely if original space is)

Let $X$ be a [[locally compact topological space]]. Then its one-point extension $X^\ast$ (def. \ref{OnePointExtension}) is a [[Hausdorff topological space]] precisely if $X$ is. 

=--

+-- {: .proof}
###### Proof

It is clear that if $X$ is not Hausdorff then $X^\ast$ is not.

For the converse, assume that $X$ is Hausdorff.  

Since $X^\ast = X \cup \{\infty\}$ as underlying sets, we only need to check that for $x \in X$ any point, then there is an open neighbourhood $U_x \subset X \subset X^\ast$ and an open neighbourhood $V_\infty \subset X^\ast$ of the extra point which are disjoint.

That $X$ is locally compact implies by definition that there exists an open neighbourhood $U_k \supset \{x\}$ whose [[topological closure]] $CK \coloneqq Cl(U_x)$ is a closed compact neighbourhood $CK \supset \{x\}$. Hence 

$$
  V_\infty \coloneqq (X \backslash CK ) \cup \{\infty\} \subset X^\ast
$$

is an open neighbourhood of $\{\infty\}$ and the two are disjoint 

$$
  U_x \cap V_\infty = \emptyset
$$

by construction.


=--


+-- {: .num_prop #InclusionIntoOnePointExtensionIsOpenEmbedding}
###### Proposition
**(inclusion into one-point extension is open embedding)**

Let $X$ be a [[topological space]]. Then the evident inclusion function

$$
  i \;\colon\; X \longrightarrow X^\ast
$$

into its one-point extension (def. \ref{OnePointExtension}) is 

1. a [[continuous function]] 

1. an [[open map]]

1. an [[embedding of topological spaces]].

=--

+-- {: .proof}
###### Proof

Regarding the first point: For $U \subset X$ open and $CK \subset X$ closed and compact, the preimages of the corresponding open subsets in $X^\ast$ are

$$
  i^{-1}(U) = U
  \phantom{AAAA}
  i^{-1}( (X \backslash CK) \cup \infty ) = X \backslash CK
$$

which are open in $X$.


Regarding the second point:  The image of an open subset $U \subset X$ is $i(U) = U \subset X^\ast$, which is open by definition.

Regarding the third point: We need to show that $i \colon X \to i(X) \subset X^\ast$ is a [[homeomorphism]]. This is immediate from the definition of $X^\ast$.

=--



+-- {: .num_prop #CompactHausdorffSpaceIsCompactificationOfComplementOfAnyPoint}
###### Proposition

If $X$ is a [[compact Hausdorff space]] and $x_0 \in X$ any point, then $X$ is [[homeomorphism|homeomorphic]] to the one-point compactification (Def. \ref{OnePointExtension}) of its [[complement]] [[subspace]] $X \setminus \{x_0\} \subset X$:

$$
  X \simeq (X \setminus \{x_0\})^\ast
  \,.
$$

Observe also that $X \setminus \{x_0\}$, being an [[open subspace]] of a [[compact Hausdorff space]], is a [[locally compact topological space]], since [[open subspaces of compact Hausdorff spaces are locally compact]], and of course it is Hausdorff, since $X$ is.

=--

+-- {: .proof}
###### Proof

Since [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]], the open neighbourhoods of $x \in X$ are equivalently the
complements of closed, and hence compact closed, subsets in $X \setminus \{x\}$. By def. \ref{OnePointExtension} this means that the function

$$
  \array{
     X &\longrightarrow& (X \setminus \{x_0\})^\ast
  }
$$

which is the identity on $X \setminus \{x_0\}$ and sends $x_0 \mapsto \infty$ (hence which is just the identity on the underlying sets) is a [[homeomorphism]].

=--


### Universal property
  {#UniversalProperty}

As a [[pointed topological space|pointed]] [[locally compact topological space|locally compact]] [[Hausdorff space]], the one-point compactification of $X$ may be described by a [[universal property]]: 

For every [[pointed topological space|pointed]] [[locally compact topological space|locally compact]] [[Hausdorff space]] $(Y, y_0)$ and every [[continuous map]] $f \colon X \to Y$ such that the [[pre-image]] $f^{-1}(K)$ is compact for all compact sets $K$ not containing $y_0$, there is a unique basepoint-preserving continuous map $X^\ast \to Y$ that extends $f$. 

This property characterizes $X^\ast$ in an [[essentially unique]] manner.

$X$ is [[dense subspace|dense]] in $X^*$ precisely if $X$ is not already compact.  Note that $X^*$ is technically a [[compactification]] of $X$ only in this case.

$X^*$ is [[Hausdorff space|Hausdorff]] (hence a [[compactum]]) if and only if $X$ is already both Hausdorff and [[locally compact space|locally compact]] (see prop. \ref{HausdorffOnePointCompactification}).

### Monoidal functoriality
  {#MonoidalFunctoriality}


+-- {: .num_prop #OnePointCompactificationFunctor}
###### Proposition

The operation of one-point compactification (Def. \ref{OnePointExtension}) does not extend to a [[functor]] on the whole [[category]] of [[topological spaces]]. But it does extend to a [[functor]] on [[locally compact Hausdorff spaces]] with [[proper maps]] between them.

=--

(e.g. [Cutler 20, Prop. 1.6](#Cutler20))

+-- {: .num_prop #OnePointCompactificationAndSmashProduct}
###### Proposition
**([[one-point compactification intertwines Cartesian product with smash product]])

On the [[subcategory]] $Top_{LCHaus}$ in [[Top]] of [[locally compact Hausdorff spaces]] with [[proper maps]] between them, the [[functor]] of [[one-point compactification]] (Prop. \ref{OnePointCompactificationFunctor})

$$
  (-)^{cpt}
  \;\colon\;
  Top_{LCHaus}
  \longrightarrow 
  Top^{\ast/}
$$


1. sends [[coproducts]], hence [[disjoint union topological spaces]], to [[wedge sums]] of [[pointed topological spaces]];

1. sends [[Cartesian products]], hence [[product topological spaces]], to [[smash products]] of [[pointed topological spaces]];

hence constitutes a [[strong monoidal functor]] for both [[monoidal category|monoidal]] structures of these [[distributive monoidal categories]] in that there are [[natural transformation|natural]] [[homeomorphisms]]

$$
  \big(
    X \sqcup Y 
  \big)^{cpt}
  \;\simeq\;
  X^{cpt} \vee Y^{cpt}
  \,,
$$

and

$$
  \big(
    X \times Y 
  \big)^{cpt}
  \;\simeq\;
  X^{cpt} \wedge Y^{cpt}
  \,.
$$

=--

This is briefly mentioned in [Bredon 93, p. 199](#Bredon93).
The argument is spelled out in: [MO:a/1645794](https://math.stackexchange.com/a/1645794/58526), [Cutler 20, Prop. 1.6](#Cutler20).



## Examples

### Eculidean spaces compactify to Spheres
 {#ExamplesSpheres}

We discuss how the [[one-point compactification]] of [[Euclidean space]] of [[dimension]] $n$ is the [[n-sphere]].

+-- {: .num_example #nSphereIsOnePointCompactificationOfRn}
###### Example
**([[one-point compactification]] of [[Euclidean space|Euclidean n-space]] si the [[n-sphere]])

For $n \in \mathbb{N}$ the [[n-sphere]] with its standard [[topological space|topology]] (e.g. as a [[subspace]] of the [[Euclidean space]] $\mathbb{R}^{n+1}$ with its [[metric topology]]) is [[homeomorphism|homeomorphic]] to the one-point compactification (def. \ref{OnePointExtension}) of the [[Euclidean space]] $\mathbb{R}^n$

$$
  S^n \simeq (\mathbb{R}^n)^\ast
  \,.
$$

=--

+-- {: .proof}
###### Proof

Pick a point $\infty \in S^n$. By [[stereographic projection]] we have a [[homeomorphism]]

$$
  S^n \setminus \{\infty\} \simeq \mathbb{R}^n
  \,.
$$

With this it only remains to see that for $U_\infty \supset \{\infty\}$ an open neighbourhood of $\infty$ in $S^n$ then the complement $S^n \setminus U_\infty$ is compact closed, and conversely that the complement of every compact closed subset of $S^n \setminus \{\infty\}$ is an open neighbourhood of $\{\infty\}$.

Observe that under [[stereographic projection]] the open subspaces $U_\infty \setminus \{\infty\} \subset S^n \setminus \{\infty\}$ are identified precisely with the [[closed subset|closed]] and [[bounded subsets]] of $\mathbb{R}^n$. (Closure is immediate, boundedness follows because an open neighbourhood of $\{\infty\} \in S^n$ needs to contain an open ball around $0 \in \mathbb{R}^n \simeq S^n \setminus \{-\infty\}$ in the _other_ stereographic projection, which under change of chart gives a bounded subset. )

By the [[Heine-Borel theorem]] the closed and bounded subsets of $\mathbb{R}^n$ are precisely the compact, and hence the compact closed, subsets of $\mathbb{R}^n \simeq S^n \setminus \{\infty\}$.

=--

+-- {: .num_remark #RelevanceForMonopolesAndInstantons}
###### Remark
**(relevance for [[monopoles]] and [[instantons]] in [[gauge theory]])**

In [[physics]], Example \ref{nSphereIsOnePointCompactificationOfRn} governs the phenomenon of [[monopoles]] and [[instantons]] for [[gauge theory]] on [[Minkowski spacetime]] or [[Euclidean space]]: While such spaces themselves are not [[compact topological space|compact]], the consistency condition that any [[field history|field configuration]] carries a [[finite number|finite]] [[energy]] requires that [[gauge fields]] _[[vanishing at infinity|vanish at infinity]]_. 

This means that if $A$ is the [[classifying space]] for the corresponding gauge field --  e.g. $A = B G$ for [[Yang-Mills theory]] with [[gauge group]] $G$ -- and if $a_\infty \in A$ denotes the [[pointed topological space|base point]] witnessing vanishing fields, then a [[field configuration]]/[[cocycle]]

$$
  \mathbb{R}^n
  \overset{c}{\longrightarrow}
  A
$$

on $\mathbb{R}^n$ in $A$-[[generalized cohomology theory|cohomology]] _[[vanishing at infinity|vanishes at infinity]]_ if outside any [[compact topological space|compact]] [[subset]] its value is the vanishing field configuration $a_\infty$.

But by Def. \ref{OnePointExtension} this is equivalent to the cocycle [[extension|extends]] to the [[one-point compactification]] as a [[morphism]] of [[pointed topological space]]:

$$ 
  \array{
    \big(
      \mathbb{R}^n
    \big)
    \simeq S^n
    &
    \overset{c}{\longrightarrow}
    &
    A
    \\
    \infty &\mapsto& a_\infty
  }
$$

The following graphics illustrates this for $A = S^n$ an [[n-sphere]] itself, hence for charges in [[Cohomotopy cohomology theory]]:

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=9">
<img src="https://ncatlab.org/schreiber/files/CohomotopyOfEuclideanNSpaceVanishingAtInfinity.jpg" width="640">
</a>
</center>

> graphics grabbed from [SS 19](cohomotopy+charge#SatiSchreiber19)
 

For more see at _[Yang-Mills instanton -- SU(2)-instantons from the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)_.

=--

### Linear representations compactify to representation spheres

Via the presentation of example \ref{nSphereIsOnePointCompactificationOfRn}, the canonical [[action]] of the [[orthogonal group]] $O(N)$ on $\mathbb{R}^n$ induces an action of $O(n)$ on $S^n$, which preserves the basepoint $\infty$ (the "point at infinity").

This construction presents the [[J-homomorphism]] in [[stable homotopy theory]] and is encoded for instance in the definition of [[orthogonal spectra]].

Slightly more generally, for $V$ any real [[vector space]] of [[dimension]] $n$ one has $S^n \simeq (V)^\ast$. In this context and in view of the previous case, one usually writes

$$
  S^V \coloneqq (V)^\ast
$$

for the $n$-[[sphere]] obtained as the one-point compactification of the vector space $V$.


As a special case of Prop. \ref{OnePointCompactificationAndSmashProduct} we have:

+-- {: .num_prop }
###### Proposition

For $V,W \in Vect_{\mathbb{R}}$ two real [[vector spaces]], there is a [[natural transformation|natural]] [[homeomorphism]]

$$
  S^V \wedge S^W \simeq S^{V\oplus W}
$$

between the [[smash product]] of their one-point compactifications and the one-point compactification of the [[direct sum]].

=--

+-- {: .num_remark }
###### Remark

In particular, it follows directly from this that the [[suspension]] $\Sigma(-) \simeq S^1 \wedge (-)$ of the $n$-sphere is the $(n+1)$-sphere, up to [[homeomorphism]]:

$$
  \begin{aligned}
    \Sigma S^n 
    & \simeq S^{\mathbb{R}^1} \wedge S^{\mathbb{R}^n}
    \\
    & \simeq S^{\mathbb{R}^1 \oplus \mathbb{R}^n}
    \\
    & \simeq S^{\mathbb{R}^{n+1}}
    \\
    & \simeq S^{n+1}
  \end{aligned}
  \,.
$$

=--

\linebreak

### Thom spaces

For $X$ a [[compact topological space]] and $V \to X$
a [[vector bundle]], then the ([[homotopy type]] of the) one-point compactification of 
the total space $V$ is the [[Thom space]] of $V$, equivalent to $D(V)/S(V)$. 

For a simple example: the real [[projective plane]] $\mathbb{RP}^2$ is the one-point compactification of the 'open' [[Moebius strip|Möbius strip]], as line bundle over $S^1$. This is a special case of the more general observation that $\mathbb{RP}^{n+1}$ is the Thom space of the [[tautological line bundle]] over $\mathbb{RP}^n$. 

### Locally compact Hausdorff spaces

+-- {: .num_example #LocallyCompatcHausdorffSpaceIsOpenSubspaceOfCompactHausdorffSpace}
###### Example
**(every [[locally compact topological space|locally compact]] [[Hausdorff space]] is an [[open subset|open]] [[subspace]] of a [[compact Hausdorff space]])**

Every [[locally compact topological space|locally compact]] [[Hausdorff space]]  is [[homeomorphism|homemorphic]] to a [[open subset|open]] [[topological subspace]] of a [[compact topological space]].

=--

+-- {: .proof}
###### Proof

In one direction the statement is that [[open subspaces of compact Hausdorff spaces are locally compact]] (see there for the proof). What we need to show is that every locally compact Hausdorff spaces arises this way.

So let $X$ be a locally compact Hausdorff space. By prop. \ref{OnePointExtensionIsCompact} and prop. \ref{HausdorffOnePointCompactification} its one-point extension $X^\ast$ (def. \ref{OnePointExtension}) is a [[compact Hausdorff space]]. By prop. \ref{InclusionIntoOnePointExtensionIsOpenEmbedding} the canonical inclusion $X \to X^\ast$ is an [[open map|open]] [[embedding of topological spaces]].

=--




## Related concepts

* [[Thom space]]

* [[compactification]] 

  * [[Stone-Cech compactification]]

  * [[end compactification]]

  * [[Bohr compactification]]

  * [[Kaluza-Klein compactification]]

* [[configuration space (mathematics)]]

* [Yang-Mills instanton -- SU(2)-instantons from the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)_


## References

The concept goes back to 

* {#Aleksandrov24} [[Pavel Aleksandrov]], _Über die Metrisation der im Kleinen kompakten topologischen Räume_, Mathematische Annalen (1924) Volume: 92, page 294-301 ([dml:159072](https://eudml.org/doc/159072))

Textbook accounts:

* {#Kelly75} John Kelly, [p. 150](https://archive.org/details/GeneralTopology/page/n167) of: _General Topology_, van Nostrand 1955 ([archive:GeneralTopology](https://archive.org/details/GeneralTopology))

* {#Bredon93} [[Glen Bredon]], p. 199 of: _Topology and Geometry_, Graduate Texts in Mathematics 139, Springer 1993 ([doi:10.1007/978-1-4757-6848-0](https://link.springer.com/book/10.1007/978-1-4757-6848-0), [pdf](http://virtualmath1.stanford.edu/~ralph/math215b/Bredon.pdf))

Review:

* {#Cutler20} Tyrone Cutler, _The category of pointed topological spaces_, 2020 ([pdf](https://www.math.uni-bielefeld.de/~tcutler/pdf/Elementary%20Homotopy%20Theory%20II%20-%20The%20Pointed%20Category.pdf), [[CutlerPointedTopologicalSpaces.pdf:file]])


See also 

* Wikipedia, _[Alexandroff extension](https://en.wikipedia.org/wiki/Alexandroff_extension)_

[[!redirects one-point compactification]]
[[!redirects one-point compactifications]]
[[!redirects One-point compactification]]
[[!redirects Alexandroff compactification]]
[[!redirects Alexandroff compactifications]]
[[!redirects Alexandrov compactification]]
[[!redirects Alexandrov compactifications]]
[[!redirects Aleksandrov compactification]]
[[!redirects Aleksandrov compactifications]]
[[!redirects Александров compactification]]
[[!redirects Александров compactifications]]

[[!redirects one-point extension]]
[[!redirects one-point extensions]]
[[!redirects Alexandroff extension]]
[[!redirects Alexandroff extensions]]
[[!redirects Alexandrov extension]]
[[!redirects Alexandrov extensions]]
[[!redirects Aleksandrov extension]]
[[!redirects Aleksandrov extensions]]
[[!redirects Александров extension]]
[[!redirects Александров extensions]]

[[!redirects point at infinity]]
