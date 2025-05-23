# Contents
* table of contents
{: toc}

## Idea

A **category of cubes** is a category of [[geometric shapes for higher structures]] in which the basic shapes are cubes of all dimensions.
There are actually many different categories of cubes, depending on what sorts of operations are permitted between cubes.
In general, we expect the following of a category of cubes:

* It is a [[monoidal category]] $(\Box,\otimes,I^0)$: the monoidal product of the "$n$-cube" and "$m$-cube" is the "$(n+m)$-cube", and the monoidal unit is the "$0$-cube" $I^{0}$.
* It contains an [[interval object]], the "1-cube", which is to say an object $I^{1}$ with two "faces" $\delta_0, \delta_1 \colon I^{0} \to I^{1}$ and a "degeneracy" $\epsilon \colon I^{1} \to I^{0}$ fitting in the diagram below.
\begin{tikzcd}
I^{0} \ar[dr,"id"{below left}] \ar[r,"\delta_0"] & I^{1} \ar[d,"\epsilon"] & \ar[l,"\delta_1"{above}] I^{0} \ar[dl,"id"{below right}] \\
& I^{0}
\end{tikzcd}
* Every object can be written as a monoidal product of $n \ge 0$ copies of the "$1$-cube".

Often one asks that the monoidal structure is [[strict monoidal category|strict]], in which case any cube category is a [[PRO]].
Besides the faces and degeneracies, a cube category might also include

* automorphisms of cubes, such as _permutations/symmetries_ or _reversals_;
* additional face-like maps, such as _diagonals_;
* additional degeneracy-like maps, such as [[connection on a cubical set|_connections_]].

Often we describe a cube category as generated by some subset of these morphisms.
Typically there is a functor from $\Box$ to [[Top]] sending the $n$-cube to the topological $n$-cube $[0,1]^n$.

A presheaf on a category of cubes is a [[cubical set]].

## Definitions

A uniform way to present many cube categories is as free (strict) monoidal categories with some structure, i.e., as classifying categories for monoidal theories ([Mauri 2005](#Mauri2005)).
This approach is described by [Grandis and Mauri (2003)](#GrandisMauri2003) and expanded upon by [Buchholtz and Morehouse (2017)](#BuchholtzMorehouse2017).
In these descriptions, some morphisms between cubes play the role of [[structural rule|structural rules]], reflecting additional requirements on the monoidal structure:

* Degeneracies (always included) correspond to [[semicartesian monoidal category|requiring the monoidal unit to be terminal]].
* Permutations correspond to requiring the monoidal product to be [[symmetric monoidal category|symmetric]].
* Diagonals correspond to requiring a [[monoidal category with diagonals]].

Including permutations thus makes the cube category a [[PROP]], while including all structural rules makes it a [[Lawvere theory]].
Other morphisms, such as connections or reversals, are instead "operations".

The construction of the classifying category can be unpacked into an explicit description of a cube category $\Box$ in terms of generating morphisms and relations (the "cubical identities").
Most cube categories can also be described as wide subcategories of the full subcategory of [[Set]] consisting of $\{0,1\}^n$ for $n \ge 0$: a morphism between cubes is determined by its behavior on vertices.

At least in the cartesian case, the classifying category description implies that $\Box$ is equivalent to the opposite of the category of free finitely-generated algebras for the theory.
The 1-cube $I^1$ can often be cast as a [[dualizing object]], yielding another description of the cube category.

### The ordered cube category

The **ordered cube category** or **restricted cube category** ([Grandis & Mauri 2003, Section 4](#GrandisMauri2003)) is the minimal cube category, generated by face and degeneracy maps.
When unqualified, **cube category** usually refers to this category, which historically was the first to be defined.

+-- {: .num_defn}
###### Definition

The **ordered cube category** is the free strict monoidal category with terminal unit $(\Box,\otimes,I^0)$ equipped with an object $I^{1}$ and two maps $\delta_0,\delta_1 : I^{0} \to I^{1}$.

=--

+-- {: .num_defn}
###### Notation

Let $n \geq 0$ be an integer. We denote the object $\underset{n}{\underbrace{I^{1} \otimes \cdots \otimes I^{1}}}$ of $\Box$ by $I^{n}$. 

=--

+-- {: .num_defn}
###### Terminology

In addition to the maps $\delta_0$ and $\delta_1$, maps of the form $I^n \otimes \delta_\alpha \otimes I^m$ for $n,m \ge 0$ are also called *faces*.
Finite composites of such maps may also be called faces.
Likewise, maps of the form $I^n \otimes \epsilon \otimes I^m$ for $n,m \ge 0$ are also called degeneracies.

=--

See ([Grandis & Mauri 2003, Section 4](#GrandisMauri2003)) for the following two propositions.

+-- {: .num_defn}
###### Proposition

The ordered cube category is the classifying category of the monoidal theory of bipointed objects with the weakening structural rule.

=--

+-- {: .num_defn #OrderedCubesInSet}
###### Proposition

The ordered cube category is isomorphic to the subcategory of $Set$ whose objects are powers $2^n$ of $2 = \{0, 1\}$, $n \geq 0$, and whose morphisms are generated by degeneracy maps $2^{n} \to 2^{n-1}$ which delete a coordinate and face maps $2^{n} \to 2^{n+1}$ which insert a 0 or 1 without modifying the order of coordinates.
The monoidal product is the restriction of the cartesian product on $Set$.
The basic face maps are the two inclusions $\delta^0, \delta^1 \colon 1 \to 2$ and the basic degeneracy is the map $\epsilon \colon 2 \to 1$.

=--

+-- {: .num_defn}
###### Remark

It follows from Proposition \ref{OrderedCubesInSet} that every morphism in $\Box$ can be written as a finite composite of maps of the form $I^n \otimes \delta_\alpha \otimes I^m$ and $I^n \otimes \epsilon \otimes I^m$.
An explicit description of the ordered cube category by [[presentation of a category by generators and relations|generators and relations]] is in section 2 of

  * Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega-Cat$_ ([web](http://crans.fol.nl/papers/thten.html), [ps](http://crans.fol.nl/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

=--

+-- {: .num_defn}
###### Definition

Write $\Box_{\leq 1}$ for the full subcategory of $\Box$ consisting of $I^0$ and $I^1$.

=--

+-- {: .num_defn}
###### Remark

The category $\Box_{\leq 1}$ is isomorphic to the category $\Delta_{\leq 1}$, i.e. it may also be described as

 * The full subcategory of the [[simplex category]] $\Delta$ on the objects $[0]$ and $[1]$.

 * (A skeleton of) the category of linearly ordered sets of cardinality 1 or 2.

 * The indexing category for [[reflexive coequalizer|reflexive equalizers]].

$\Box$ itself can be recovered as the [[free strict monoidal category]] on $\square_{\leq 1}$ whose unit object is $I^{0}$.
Note that $\Box$ is _not_ the free strict monoidal category on $\square_{\leq 1}$, but the free strict monoidal category _with specified unit_ on $\square_{\leq 1}$, where the unit is specified to be $I^{0}$.

=--

### Cubes with connections

For $\alpha \in \{0,1\}$, an **$\alpha$-connection** in a cube category is a morphism $\gamma_\alpha \colon I^1 \otimes I^1 \to I^1$ such that $(I^1,\delta_\alpha,\gamma_\alpha)$ defines a [[monoid in a monoidal category]] and additionally the equations
$$
\gamma_\alpha \circ (\delta_{1-\alpha} \otimes I^1) = \gamma_\alpha \circ (\delta_{1-\alpha} \otimes I^1) = \delta_{1-\alpha} \circ \epsilon
$$
hold.
Often these are called negative and positive connections rather than $0$- and $1$-connections respectively.
We can think of the negative connection as the morphism of topological spaces $[0,1]^2 \to [0,1]$ sending a pair of points $(x,y)$ to their maximum, likewise the positive connection as the minimum.
We may more generally refer to maps of the form $I^n \otimes \gamma_\alpha \otimes I^m$ as connections.

+-- {: .num_defn}
###### Definition

The **ordered cube category with an $\alpha$-connection** is the free strict monoidal category with terminal unit $(\Box,\otimes,I^0)$ equipped with an object $I^{1}$, two maps $\delta_0,\delta_1 : I^{0} \to I^{1}$, and an $\alpha$-connection.

=--

We can also consider the cube category with both negative and positive connections.
The cube category has several advantages over the minimal cube category as a shape for higher structures; see [[connection on a cubical set]] for more information.

### Symmetric cube categories

+-- {: .num_defn}
###### Definition

The **symmetric cube category** is the free strict _symmetric_ monoidal category with terminal unit $(\Box,\otimes,I^0)$ equipped with an object $I^{1}$ and two maps $\delta_0,\delta_1 : I^{0} \to I^{1}$.

=--

The symmetric cube category is also called the [[semicartesian monoidal category|semicartesian]] cube category, as well as the "BCH" cube category after its use by [Bezem, Coquand, & Huber (2013)](#BezemCoquandHuber2013) to interpret [[homotopy type theory]] constructively.
It is also used in the semantics of [[parametric dependent type theory|internally parametric dependent type theory]].

The symmetric monoidal structure induces an automorphism $I^{\sigma} \colon I^n \cong I^n$ for each element $\sigma \in \Sigma_n$ of the [[symmetric group]] on $n$ elements.
The symmetric cube category can be compared with the [[symmetric simplicial set|symmetric simplex category]] and [[cyclic category]], which similarly add symmetries to the [[simplex category]].
Note that while the symmetric simplex category includes all the natural symmetries of an $n$-simplex, the symmetric cube category only includes the symmetries of the $n$-cube coming from permutations of the axes.

The symmetric cube category admits the following alternative description, used by Bezem, Coquand, and Huber:

+-- {: .num_defn}
###### Proposition

The symmetric cube category is equivalent to the category whose objects are finite sets and whose morphisms $f \colon I \to J$ are set functions $f \colon J \to I \sqcup \{0,1\}$ such that the restriction of $f$ to the preimage of $I$ is injective.

=--

+-- {: .num_defn}
###### Remark

A [[cubical set]] over the symmetric cube category can also be seen as a [[nominal set]] with additional structure; see [Pitts (2015)](#Pitts2015).

=--

+-- {: .num_defn}
###### Remark

[Isaacson (2011)](#Isaacson2011) uses a cube category with symmetries and a positive connection, while [Grandis and Mauri (2003)](#GrandisMauri2003) describe a cube category $\mathbb{K}$ with symmetries and both positive and negative connections.
Grandis and Mauri also take the connections to be symmetric, making $(I^1,\delta_\alpha,\gamma_\alpha)$ are _commutative_ monoids for $\alpha \in \{0,1\}$, while Isaacson does not.

=--

+-- {: .num_defn}
###### Remark

[Krishnan and Rudman (2025)](#KrishnanRudman2025) consider the subcategory of [[Pos]] whose objects are $\{0 \lt 1\}^n$ for $n \ge 0$ and whose morphisms are the monotone maps that preserve [[intervals]] (in the sense of [[order theory]]).
This cube category has symmetries and connections but also contains maps not generated by these, such as the poset map $(x,y,z) \mapsto (x \wedge y) \vee (x \wedge z) \vee (y \wedge z)$ [(Krishnan and Rudman 2025, Example 3.13)](#KrishnanRudman2025).

=--

### Cubes with reversals

A **reversal** or **reversion** in a cube category is a involution $\rho \colon I^1 \to I^1$ such that $\rho \circ \delta_{\alpha} = \delta_{1-\alpha}$ for $\alpha \in \{0,1\}$.
Topologically, we think of a reversal as the automorphism of the topological 1-cube $[0,1]$ sending $t$ to $1 - t$.

+-- {: .num_defn}
###### Remark

[Grandis and Mauri (2003, Section 9)](#GrandisMauri2003) consider a cube category $!\mathbb{K}$ generated by connections, symmetries, and reversals (on top of faces and degeneracies).
They also impose laws governing the interaction between reversals and connections, $\gamma_\alpha \circ (\rho \otimes \rho) = \rho \circ \gamma_{1-\alpha}$, which reflect the equations satisfied by the topological $min$, $max$, and reversal.

=--

### Cartesian cube categories

By adding diagonal morphisms $I^n \to I^n \otimes I^n$ on top of the symmetric cube category, we arrive at the cartesian cube category.

+-- {: .num_defn}
###### Remark

Symmetries can already be derived from the combination of degeneracies and diagonals $I^n \to I^n \otimes I^n$ [(Mauri 2005, Corollary 5.5)](#Mauri2005), though not if one only assumes a diagonal $I^1 \to I^1 \otimes I^1$.

=--

+-- {: .num_defn #CartesianCubes}
###### Definition

The **cartesian cube category** is the free strict _cartesian_ monoidal category $(\Box,\otimes,I^0)$ equipped with an object $I^{1}$ and two maps $\delta_0,\delta_1 : I^{0} \to I^{1}$.

=--

The cartesian cube category is thus the [[Lawvere theory]] of [[bi-pointed object|bi-pointed objects]].
In particular, it is dual to the category of free finite bi-pointed sets.
By a [[Stone duality|Stone-type duality]] with $I^1$ as a [[dualizing object]], $\Box$ itself admits an algebraic description:


+-- {: .num_defn}
###### Proposition

The cartesian cube category is isomorphic to the subcategory of [[Set]] consisting of maps $\{0 \lt 1\}^{n} \to \{0 \lt 1\}^{m}$ preserving binary $max$ and $min$.

=--

Cartesian cube categories (with or without additional structure) are used in the semantics of [[homotopy type theory]] and [[cubical type theory]].
The use of a cube category with diagonals for this purpose was proposed by [Coquand (2014)](#CoquandDiagonals2014).
The first constructed model of this kind used the De Morgan cube category ([Cohen, Coquand, Huber & Mörtberg, 2015](#CohenCoquandHuberMoertberg2017)) (see below), but the construction can be (non-trivially) modified to work for the cartesian cubes of Definition \ref{CartesianCubes} [(Angiuli, Brunerie, Coquand, Harper, Favonia & Licata 2021)](#ABCFHL).
Various cartesian cube categories are categorized by [Buchholtz and Morehouse (2017)](#BuchholtzMorehouse2017).

#### Cartesian cubes with connections

In the cartesian regime, there is a proliferation of options for the laws governing the interaction of operations such as connections or reversals. For example, one may ask that the positive and negative connections distribute over each other, a condition which only makes sense in the presence of diagonals.
The following two choices, for one and two connections respectively, reflect the equational theory of the topological $n$-cubes when we interpret diagonals by geometric diagonals and connections by $min$ and $max$.

+-- {: .num_defn}
###### Definition

The **join (resp. meet) semilattice category** is the Lawvere theory of [[01-bounded]] join (resp. meet) [[semilattice|semilattices]].
(The join and meet variants are of course isomorphic.)

=--

+-- {: .num_defn}
###### Definition

The **distributive lattice cube category** (or **Dedekind cube category**) is the Lawvere theory of bounded [[distributive lattice|distributive lattices]].

=--

Like the cartesian cube category, these have alternate characterizations via [[Stone duality|Stone-type dualities]] (and in particular [[Birkhoff duality]]) mediated by $I^1$.

+-- {: .num_defn}
###### Proposition

The distributive lattice cube category is isomorphic to the full subcategory of [[Pos]] consisting of the powers $\{0 \lt 1\}^n$ for $n \ge 0$.
The join semilattice cube category is isomorphic to the wide subcategory thereof consisting of maps $\{0 \lt 1\}^n \to \{0 \lt 1\}^m$ preserving binary joins.

=--

Unlike the previously discussed cube categories, the cartesian cube categories with one or more connections are not [[Cauchy complete category|Cauchy complete]].
For applications using presheaves on the cube category, it is often convenient to work with their Cauchy completions.

+-- {: .num_defn #CartesianConnectionCauchyCompletion}
###### Proposition

The Cauchy completion of the distributive lattice cube category is equivalent to the full subcategory of [[Pos]] consisting of finite (bounded) lattices.
The Cauchy completion of the join semilattice cube category is equivalent to the subcategory of [[Pos]] consisting of finite (bounded) distributive lattices and morphisms preserving binary joins.

=--

+-- {: .proof}
###### Proof

([Sattler 2019](#Sattler2019)) and ([Cavallo & Sattler (2022), Theorem 4.46](#CavalloSattler2022)).

=--

+-- {: .num_defn}
###### Remark

There is a [[fully faithful functor]] $\Delta \to \overline{\Box}$ from the [[simplex category]] into the Cauchy completions of the semilattice and distributive lattice cube categories, corresponding to the inclusion of linear orders in the categories of Proposition \ref{CartesianConnectionCauchyCompletion}.

=--

#### Cartesian cubes with connections and reversals

[Buchholtz and Morehouse (2017)](#BuchholtzMorehouse2017) consider the cube categories with symmetries, diagonals, connections, and reversals (on top of faces and degenerecies) given by the Lawvere theories of [[De Morgan algebras]], [[Kleene algebras]], and [[Boolean algebras]], the differences between them being in the equational theory of morphisms.

The Kleene cube category is the choice that makes the evident functor $\Box \to Top$ faithful.
The De Morgan cube category is used in the model of [[cubical type theory]] of [Cohen, Coquand, Huber & Mörtberg (2015)](#CohenCoquandHuberMoertberg2017), but the construction also works with Kleene and Boolean cubes.
The Cauchy completion of the Boolean cube category is the category [[FinSet]]$_+$ of nonempty finite sets, so the category of Boolean cubical sets is equivalent to the category of [[symmetric sets]].

## As shapes for higher structures

### As test categories

Many (perhaps all) of the cube categories described above are [[test categories]] ([Buchholtz & Morehouse 2017](#BuchholtzMorehouse2017)).
Hence their categories of [[cubical sets]] model [[homotopy types]].
Cube categories with connections or diagonals are generally [[strict test categories]], while the ordered and symmetric cube categories are not.
See _[[model structure on cubical sets]]_ and _[[connection on a cubical set]]_ for more details.

### Tensor products

Among all [[geometric shapes for higher structures]] cubes are best suited for describing Gray-like [[tensor product|tensor products]] of higher structures: there is geometrically obvious way in which to combine the $n$-cube $I^{n}$ and the $m$-cube $I^{m}$ to the $(n+m)$-cube $I^{n} \otimes I^m := I^{n+m}$. The monoidal structure on the ordered cube category induces the canonical monoidal structure on [[cubical set|cubical sets]] and then on [[strict omega-category|strict omega-categories]]: the [[Crans-Gray tensor product]].

## Reedy and Eilenberg--Zilber structures

Many (but not all) cube categories can be seen as [[Reedy categories]] (or [[generalized Reedy categories]] if they contain non-trivial automorphisms), with the degree of an cube given by its dimension.
The Reedy face maps are the cubical faces and diagonals (if present), while the Reedy degeneracy maps are the cubical degeneracies and connections (if present).

Those cube categories which are Reedy categories are generally also [[elegant Reedy categories]], or [[Eilenberg-Zilber categories]] if they contain automorphisms.
[Campion (2023)](#Campion2023) enumerates a collection of cube categories and determines which of them are Eilenberg--Zilber categories.

+-- {: .num_defn}
###### Proposition

The cube categories without diagonals (i.e., having possibly symmetries, connections, or reversals on top of faces and degeneracies) are Eilenberg--Zilber categories.

=--

+-- {: .proof}
###### Proof

([Campion 2023, Corollary 7.10](#Campion2023)).

=--

One should check Campion for the precise definition of cube category used there.
The cube category of [Krishnan and Rudman (2025)](#KrishnanRudman2025) is the largest Eilenberg--Zilber category among the concrete (i.e., given by a subcategory of [[Set]] with objects $\{0,1\}^n$) cube categories not including diagonals or reversals.

Cube categories with diagonals are more delicate.

+-- {: .num_defn}
###### Proposition

The cartesian cube category (of \ref{CartesianCubes}) is an Eilenberg--Zilber category, as is the cartesian cube category with reversals.

=--

+-- {: .proof}
###### Proof

([Campion 2023, Theorem 8.12(1)](#Campion2023)).

=--

A Reedy category is always [[Cauchy complete category|Cauchy complete]], so for cube categories with diagonals and connections we may need to consider their Cauchy completions.

+-- {: .num_defn}
###### Proposition

The Cauchy completion of the semilattice cube category admits no Reedy structure.

=--

+-- {: .proof}
###### Proof

([Cavallo & Sattler 2022, Proposition A.1](#CavalloSattler2022)).

=--

+-- {: .num_defn}
###### Proposition

The Cauchy completion of the distributive lattice cube category is not an Eilenberg--Zilber category.

=--

+-- {: .proof}
###### Proof

([Campion 2023, Theorem 8.12(2)](#Campion2023)).

=--

+-- {: .num_defn}
###### Remark

([Cavallo & Sattler 2022](#CavalloSattler2022)) develops a generalization of the theory of EZ-categories which can be used to work with the semilattice cube category, but this theory does not apply to the distributive lattice cube category ([Cavallo & Sattler 2022, Appendix A.2](#CavalloSattler2022)).

=--

+-- {: .num_defn}
###### Proposition

The Cauchy completion of the Boolean cube category is an Eilenberg--Zilber category.

=--

+-- {: .proof}
###### Proof

([Campion 2023, Theorem 8.12(3)](#Campion2023)).

=--

## Related entries

* [[simplex category]], [[globe category]], [[cell category]]

See also the related entries at [[cubical set]].

## References

* {#Mauri2005} Luca Mauri, _Algebraic theories in monoidal categories_ (2005) &lbrack;[arXiv:1705.09202](https://arxiv.org/abs/1705.09202)&rbrack;

Zoologies of cube categories:

* {#GrandisMauri2003} [[Marco Grandis]] and Luca Mauri, _Cubical sets and their site_, Theory Applic. Categories **11** (2003) 185--201 &lbrack;[tac](http://www.tac.mta.ca/tac/volumes/11/8/11-08abs.html)&rbrack;

* {#BuchholtzMorehouse2017} [[Ulrik Buchholtz]], [[Edward Morehouse]], _Varieties of Cubical Sets_, Relational and Algebraic Methods in Computer Science (RAMICS 2017), Lecture Notes in Computer Science **10226** (2017) 77--92 &lbrack;[arXiv:1701.08189](https://arxiv.org/abs/1701.08189), [doi:10.1007/978-3-319-57418-9_5](https://dx.doi.org/10.1007/978-3-319-57418-9_5)&rbrack;

For the semicartesian cube category:

* {#BezemCoquandHuber13} [[Marc Bezem]], [[Thierry Coquand]], [[Simon Huber]], _A Model of Type Theory in Cubical Sets_,  19th International Conference on Types for Proofs and Programs (TYPES 2013). ([doi:10.4230/LIPIcs.TYPES.2013.107](https://dx.doi.org/10.4230/LIPIcs.TYPES.2013.107))

* {#Pitts2015} [[Andrew Pitts]], *Nominal Presentation of Cubical Sets Models of Type Theory*, Proceedings of the 20th International Conference on Types for Proofs and Programs (TYPES 2014). ([doi:10.4230/LIPIcs.TYPES.2014.202](https://dx.doi.org/10.4230/LIPIcs.TYPES.2014.202))

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 3* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-12.pdf), [video](https://www.youtube.com/watch?v=9pDddxB7LbE))

Cubes with symmetries and a connection:

* {#Isaacson2011} [[Samuel Isaacson]], _Symmetric cubical sets_, Journal of Pure and Applied Algebra **215**(6) (2011) 1146--1173 &lbrack;[doi:10.1016/j.jpaa.2010.08.001](https://dx.doi.org/10.1016/j.jpaa.2010.08.001)&rbrack;

Cubes with diagonals:

* {#ABCFHL} [[Carlo Angiuli]], [[Guillaume Brunerie]], [[Thierry Coquand]], [[Kuen-Bang Hou (Favonia)]], [[Robert Harper]], and [[Daniel R. Licata]], _Syntax and models of Cartesian cubical type theory_, Mathematical Structures in Computer Science **31**(4) (2021). ([doi:10.1017/S0960129521000347](https://dx.doi.org/10.1017/S0960129521000347))

* {#CohenCoquandHuberMoertberg17} [[Cyril Cohen]], [[Thierry Coquand]], [[Simon Huber]], [[Anders Mörtberg]], _Cubical Type Theory: a constructive interpretation of the univalence axiom_,  21st International Conference on Types for Proofs and Programs (TYPES) (2015). ([doi:10.4230/LIPIcs.TYPES.2015.5](https://dx.doi.org/10.4230/LIPIcs.TYPES.2015.5), [arXiv:1611.02108](https://arxiv.org/abs/1611.02108))

* {#CoquandDiagonals2014} [[Thierry Coquand]], _Variation on Cubical sets_ (2014) &lbrack;[pdf](http://www.cse.chalmers.se/~coquand/diag.pdf)&rbrack;

* {#Sattler2019} [[Christian Sattler]], _Idempotent completion of cubes in posets_ (2019) &lbrack;[arXiv:1805.04126](https://arxiv.org/abs/1805.04126)&rbrack;

* {#CavalloSattler2022} [[Evan Cavallo]] and [[Christian Sattler]], _Relative elegance and cartesian cubes with one connection_ (2022). &lbrack;[arXiv:2211.14801](https://arxiv.org/abs/2211.14801)&rbrack;

On Eilenberg--Zilber structures:

* {#Campion2023} [[Tim Campion]], _Cubical sites as Eilenberg-Zilber categories_, 2023, [arXiv:2303.06206](https://arxiv.org/abs/2303.06206)

Cubes with monotone interval-preserving maps:

* {#KrishnanRudman2025} [[Sanjeevi Krishnan]], Emily Rudman: _A convenient category of cubes_ (2025) &lbrack;[arXiv:2503.13663](https://arxiv.org/abs/2503.13663)&rbrack;

A [[constructive mathematics|constructive]] model of [[homotopy type theory]] in a [[Quillen model category]] of equivariant [[cartesian cube category|cartesian]] [[cubical sets]] that [[classical mathematics|classically]] presents the usual [[homotopy theory]] of [[spaces]]:

* [[Steve Awodey]], [[Evan Cavallo]], [[Thierry Coquand]], [[Emily Riehl]], [[Christian Sattler]], *The equivariant model structure on cartesian cubical sets* ([arXiv:2406.18497](https://arxiv.org/abs/2406.18497))

[[!redirects symmetric cube category]]
[[!redirects semicartesian cube category]]
[[!redirects cartesian cube category]]
[[!redirects semilattice cube category]]
[[!redirects de Morgan cube category]]
[[!redirects Dedekind cube category]]
[[!redirects category of cubes - exposition]]
[[!redirects cube category - exposition]]
[[!redirects cube category]]