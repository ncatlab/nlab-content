
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##


What is called _topological_ [[K-theory]] is a collection of  [[generalized (Eilenberg-Steenrod) cohomology]] theories whose cocycles in degree 0 on a [[topological space]] $X$ may be represented by pairs of [[vector bundles]], real or complex ones, on $X$ modulo a certain equivalence relation.

First, recall that for $k$ a [[field]] then a $k$-[[vector bundle]] over a [[topological space]] $X$ is a map $V \to X$ whose [[fibers]] are [[vector spaces]] which vary over $X$ in a controlled way. Explicitly this means that there exits an [[open cover]] $\{U_i \to X\}$ of $X$, a [[natural number]] $n \in \mathbb{N}$ (the _[[rank of a vector bundle|rank]]_ of the vector bundle) and a [[homeomorphism]] $U_i \times k^n \to V|_{U_i}$ over $U_i$ which is fiberwise a $k$-[[linear map]]. 

Vector bundles are of central interest in large parts of [[mathematics]] and [[physics]], for instance in [[Chern-Weil theory]] and [[cobordism theory]]. But the collection $Vect(X)_{/\sim}$ of [[isomorphism classes]] of vector bundles over a given space is in general hard to analyze. One reason for this is that these are classified in degree-1 _[[nonabelian cohomology]]_ with [[coefficients]] in the ([[nonabelian group|nonabelian]]) [[general linear group]] $GL(n,k)$. K-theory may roughly be thought of as the result of forcing vector bundles to be classified by an abelian [[cohomology theory]].

To that end, observe that all natural operations on [[vector spaces]] generalize to vector bundles by applying them [[fiber]]-wise. Notably there is the fiberwise [[direct sum of vector bundles]], also called the _[[nLab:Whitney sum]]_ operation. This operation gives the set $Vect(X)_{/\sim}$ of [[nLab:isomorphism classes]] of vector bundles the structure of an [[semi-group]] ([[monoid]]) $(Vect(X)_{/\sim},\oplus)$.

Now as under direct sum, the [[nLab:dimension]] of vector spaces adds, similarly under [[nLab:direct sum of vector bundles]] their [[nLab:rank]] adds.  Hence in analogy to how one passes from the  additive [[semi-group]] ([[monoid]]) of  [[natural numbers]] to the addtitive [[group]] of [[integers]] by adjoining formal additive inverses, so one may adjoin formal additive inverses to $(Vect(X)_{/\sim},\oplus)$. By a general prescription ("[[Grothendieck group]]") this is achieved by first passing to the larger class of [[pairs]] $(V_+,V_-)$ of vector bundles ("[[virtual vector bundles]]"), and then [[quotient|quotienting]] out the [[equivalence relation]] given by

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

This [[abelian group]] obtained from $(Vect(X)_{/\sim}, \oplus)$ is denoted $K(X)$ and often called _the K-theory_ of the space $X$. Here the letter "K" (due to [[Alexander Grothendieck]]) originates as a shorthand for the German word _Klasse_, referring to the above process of forming [[equivalence classes]] of ([[isomorphism classes]]) of vector bundles.

This simple construction turns out to yield remarkably useful groups of [[homotopy]] [[invariants]]. 
A variety of deep facts in [[algebraic topology]] have fairly elementary proofs in terms of topolgical K-theory, for instance the [[Hopf invariant one]] problem ([Adams-Atiyah 66](#AdamsAtiyah66)). 

One defines the "higher" K-groups of a topological space to be those of its higher [[suspensions]] 

$$
  K^{-n}(X) = K(\Sigma^n X)
  \,.
$$

The assignment $X \mapsto K^\bullet(X)$ turns out to share many properties of the assignment of [[ordinary cohomology]] groups $X \mapsto H^n(X,\mathbb{Z})$. One says that topological K-theory is a [[generalized (Eilenberg-Steenrod) cohomology]] theory. As such it is [[Brown representability theorem|represented]] by a [[spectrum]]. For $k = \mathbb{C}$ this is called [[KU]], for $k = \mathbb{R}$ this is called [[KR]].

One of the basic facts about topological K-theory, rather unexpected from the definition, is that these higher K-groups repeat _periodically_ in the degree $n$. For $k = \mathbb{R}$ the periodicity is 8, for $k = \mathbb{C}$ it is 2. This is called _[[Bott periodicity]]_.


It turns out that an important source of [[virtual vector bundles]] representing classes in [[K-theory]] are [[index bundles]]: Given a [[Riemannian manifold|Riemannian]] [[spin structure|spin]] [[manifold]] $B$, then there is a [[vector bundle]] $S \to B$ called the _[[spin bundle]]_ of $B$, which carries a [[differential operator]], called the [[Dirac operator]] $D$. The [[index of a Dirac operator]] is the formal difference of its [[kernel]] by its [[cokernel]] $[ker D, coker D]$. Now given a continuous family $D_x$ of Dirac operators/Fredholm operators, parameterized by some topological space $X$, then these indices combine to a class in $K(X)$.

It is via this construction that topological K-theory connects to [[spin geometry]] (see e.g. [[Karoubi K-theory]]) and [[index theory]].

As the terminology indicates, both [[spin geometry]] and [[Dirac operator]] originate in [[physics]]. Accordingly, K-theory plays a central role in various areas of theoretic physics, for instance in the theory of [[geometric quantization]] ("[[spin^c quantization]]") in the theory of [[D-branes]] (where it models [[D-brane charge]] and [[RR-fields]]).

All these geometric constructions have an [[operator algebra|operator algebraic]] incarnation: by the topological [[Serre-Swan theorem]] then [[vector bundles]] of finite rank are equivalently [[modules]] over the [[C*-algebra]] of [[continuous functions]] on the base space. Using this relation one may express K-theory classes entirely operator algebraically, this is called _[[operator K-theory]]_. Now [[Dirac operators]] are generalized to [[Fredholm operators]].

There are more [[C*-algebras]] than arising as [[algebras of functions]] of [[topological space]], namely non-commutative C*-algebras. One may think of these as defining [[non-commutative geometry]], but the definition of [[operator K-theory]] immediately generalizes to this situation (see also at _[[KK-theory]]_).

While the [[C*-algebra]] of a [[Riemannian manifold|Riemannian]] [[spin structure|spin]] [[manifold]] remembers only the underlying [[topological space]], one may algebraically encode the [[smooth structure]] and [[Riemannian structure]] by passing from [[Fredholm modules]] to "[[spectral triples]]". This may for instance be used to algebraically encode the spin physics underlying the [[standard model of particle physics]] and [[operator K-theory]] plays a crucial role in this.



### Motivational example: "nonabelian K-cohomology" ###

To see how this works, first consider the task of generalizing the "[[nonabelian cohomology]]" or [[cohomotopy]] theory given by the coefficient object $\mathbb{N}$, the additive semi-group of  $\mathbb{N}$ of [[natural number]]s.

This does have arbitrarily high [[delooping]]s in the context of [[omega-category|omega-categories]], but not in the context of [[infinity-groupoid]]s. So, for the purposes of [[cohomology]], $\mathbb{N}$ is just the [[monoid]]al [[0-groupoid]] $\mathbb{N}$, which as a coefficient object induces a very boring [[cohomology]] theory: the $\mathbb{N}$-cohomology of anything connected is just the monoidal set $\mathbb{N}$ itself. While we cannot [[delooping|deloop]] it, we can [[vertical categorification|categorify]] it and do obtain an interesting [[nonabelian cohomology]] theory:
 
Namely the [[category]] $Core(Vect)$ of finite dimensional vector spaces with invertible linear maps between them would serve as a [[vertical categorification|categorification]] of $\mathbb{N}$: isomorphism classes of finite dimensional vector spaces $V$ are given by their dimension $d(V) \in \mathbb{N}$, and [[direct sum]] of vector spaces corresponds to addition of these numbers.

If we want to use the category $Core(Vect)$ as the coefficient for a [[cohomology]] theory, for greater applicability we should equip it with its natural topological or smooth structure,  so that it makes sense to ask what the $Vect$-cohomology of a [[topological space]] or a [[smooth space]] would be. The canonical way to do this is to regard $Vect$ as a [[generalized smooth space]] called a [[smooth infinity-stack]] and consider it as the assignment

$$
  \mathbf{Vect} : Diff \to \infty Grpd
$$

$$
  U \mapsto Core(VectBund(U))
$$

that sends each smooth test space $U$ (a smooth manifold, say) to the [[groupoid]] of smooth [[vector bundle]]s over $U$ with [[bundle]] [[isomorphism]]s betweem them. We regard here a vector bundle $V \to U$ as a smooth $U$-parametrized family of vector spaces (the [[fiber]]s over each point) and thus as a smooth _probe_ or _plot_  of the category $Core(Vect)$.

The [[nonabelian cohomology]] theory with coefficients in $\mathbf{Vect}$ has no [[cohomology group]]s, but at least cohomology [[monoids]]

$$
  H(X,\mathbf{Vect}) := \pi_0 \mathbf{H}_{diff}(X, \mathbf{Vect})
  \,.
$$

It is equivalent to the [[nonabelian cohomology]] with coefficients the [[delooping]] $\mathbf{B} U$ of the stable unitary group $U := colim_n U(n)$.

To get actual topological K-theory from this, one applies [[geometric realization]] ([[fundamental infinity-groupoid]]) of the [[K-theory of a symmetric monoidal (∞,1)-category|infinity-group completion]] of  $\mathbf{Vect}$ or $\mathbf{B}U$ ([Bunke-Nikolaus-Voelkl 13](#BunkeNikolausVoelkl13)). See at _[[differential cohomology hexagon]]_ the section _[Algebraic K-theory of smooth manifolds](differential+cohomology+diagram#SoothVectorBundlesWithConnectionAndEInvariant)_.

Note: Topological complex K-theory is defined on pairs of spaces $K(X,U)$, such that the section of the complex bundle over $U$ is trivial (we might choose a trivialization). If no second space is listed, we assumed that K-theory of our manifold $X$ is taken with respect to the empty set -- $K(X) \equiv K(X, \emptyset)$ -- in this case, the bundle can be nowhere trivial. 

### K-theory as a groupoidification of $\mathbf{Vect}$ ###

The integers $\mathbb{Z}$ are obtained from the natural numbers $\mathbb{N}$ by including "formal inverses" to all elements under the additive operation. Another way to think of this is that the [[delooping|delooped]] [[groupoid]] $\mathbf{B} \mathbb{Z}$ is obtained from $\mathbf{B} \mathbb{N}$ by groupoidification (under the [[nerve]] operation this is fibrant replacement in the [[model structure on simplicial sets]]).

The idea of K-cohomology is essentially to apply this groupoidification process to not just to $\mathbb{N}$, but to its [[vertical categorification|categorification]] $\mathbf{Vect}$.

Just as an integer $k = n-m \in \mathbb{Z}$  may be regarded as an equivalence class of natural numbers $(n,m) \in \mathbb{N} \times \mathbb{N}$  under the relation

$$
  [(n,m)] = [(n+r, m+r)] \;\; \forall r \in \mathbb{N}
$$

one can similarly look at equivalence classes of pairs $(V,W) \in \mathbf{Vect}(U) \times \mathbf{Vect}(U)$ of [[vector bundle]]s.

This perspective on K-theory was originally realized by Atiyah and Hirzebruch. The resulting cohomology theory is usually called [[topological K-theory]].

As one of several variations, it is useful to regard a pair of [[vector bundle]]s as a single $\mathbb{Z}_2$-[[graded vector space|graded vector bundle]].

One version of $\mathbb{Z}_2$-graded vector bundles, which lead to a description of [[twisted cohomology|twisted]] $K$-theory are [[vectorial bundle]]s.

## Definition

Let $X$ be a [[compact space|compact]] [[Hausdorff space|Hausdorff]] [[topological space]]. Write $k$ for either the [[field]] of [[real number]]s $\mathbb{R}$ or of [[complex number]]s $C$ . By a [[vector space]] we here mean a vector space over $k$ of finite [[dimension]]. By a [[vector bundle]] we mean a topological $k$-vector bundle.  We write $I^n \to X$ for the trivial vector bundle $I^n = k^n \times X$ over $X$ of [[rank]] $n \in \mathbb{N}$.

+-- {: .num_lemma #DirectSumHasInverseUpToTrivialBundle}
###### Lemma

For every vector bundle $E \to X$ (with $X$ [[compact space|compact]] [[Hausdorff space|Hausdorff]]) there exists a [[vector bundle]] $E' \to X$ such that 

$$
  E \oplus E' \simeq I^{rank E + rank E'}
  \,.
$$

=--


+-- {: .proof}
###### Proof

One invokes a [[partition of unity]] relative to an [[open cover]] on which $E$ trivializes, constructs $E'$ locally and glues.

=--

For details see for instance ([Hatcher, prop. 1.4](#Hatcher)) or ([Friedlander, prop. 3.1](#Friedlander)).



+-- {: .num_defn #DefinitionOfKClasses}
###### Definition

Define an [[equivalence relation]] on the [[set]] of finite-[[rank]] [[vector bundle]]s $E \to X$ over $X$ by declaring that $E_1 \sim E_2$ if there exists $k,l \in \mathbb{N}$ such that there is an [[isomorphism]] of vector bundles between the (fiberwise) [[direct sum]] of $E_1$ with $I^k$ and of $E_2$ with $I^l$

$$
  (E_1 \sim E_2)
  :\Leftrightarrow
  \exists (E_1 \oplus I^k \simeq E_2 \oplus I^l)
  \,.
$$

Write 

$$
  \tilde K(X) := Vect(X)/\sim
$$

for the [[quotient set]] of [[equivalence class|equivalence classes]]. We also define the slightly coarser equivalence relation $E_1 \sim_s E_2$ where in the above definition of $\sim$ we force $k=l$. The set of equivalence classes for this equivalence relation is denoted
$$
K(X) := Vect(X)/{\sim_s}.
$$

=--

+-- {: .num_prop #KGroupIsIndeedAGroup}
###### Proposition

With $X$ compact Hausdorff as in the assumption, we have that fiberwise [[direct sum]] of vector bundles equips $\tilde K(X)$ and $K(X)$ with the structure of an [[abelian group]]. Together with the fiberwise [[tensor product]] of vector bundles this makes $K(X)$ a [[ring]] and $\tilde K(X)$ a nonunital ring.  

=--

Therefore $K(X)$ is called the **topological K-theory ring** of $X$ or just the **K-theory group** or even just the **K-theory** of $X$, for short. The smaller ring $\tilde K(X)$ is called the **reduced K-theory** of $X$.

+-- {: .proof}
###### Proof

The non-trivial part of the statement is that in $\tilde K(X)$ and $K(X)$ there is an [[inverse]] to the operation of direct sum of vector bundles. Because in $Vect(X)$ direct sum acts by addition of the ranks of vector bundles, it clearly has no inverse in $Vect(X)$.

On the other hand, clearly the K-class $[I^n]$ of any trivial bundle $I^n$ is the neutral element in $\tilde K(X)$

$$
  [I^n] = 0
$$

for all $n \in \mathbb{N}$, because by definition $I^n \sim I^0$. Therefore an inverse of a class $[E_1]$ is given by a vector bundle $E_2$ with the property that the direct sum

$$
  E_1 \oplus E_2 \simeq I^n
$$

is isomorphic to a trivial bundle for some $n$. This is the case by lemma \ref{DirectSumHasInverseUpToTrivialBundle}.


=--

+-- {: .num_prop #EquivalenceToGrothendieckGroup}
###### Proposition

$\tilde K(X)$ is isomorphic to the [[Grothendieck group]] of $(Vect(X), \oplus)$.

=--

However, def. \ref{DefinitionOfKClasses} is more directly related to the definition of K-theory by a classifying space, hence by a [[spectrum]]. This we discuss [below](#ClassifyingSpace).


## Properties

### Classifying space
 {#ClassifyingSpace}

We discuss how the [[classifying space]] for $K^0$ is the [[delooping]] of the [[stable unitary group]].

+-- {: .num_defn #BUn}
###### Definition

For $n \in \mathbb{N}$ write $U(n)$ for the [[unitary group]] in dimension $n$ and $O(n)$ for the [[orthogonal group]] in dimension $n$, both regarded as [[topological group]]s in the standard way. Write $B U(n) , B O(n)\in$ [[Top]] $ for the corresponding [[classifying space]].

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

### As a generalized cohomology theory

That topological K-theory satisfies the axioms of a [[generalized (Eilenberg-Steenrod) cohomology theory]] was shown (at least) in (Atiyah-Hirzebruch 61, 1.8](#AtiyahHirzebruch61))

### Spectrum 

Being a [[generalized (Eilenberg-Steenrod) cohomology]] theory, topological K-theory is represented by a [[spectrum]]: the _[[K-theory spectrum]]_.

The degree-0 part of this spectrum, i.e. the classifying space for degree 0 topological $K$-theory is modeled in particular by the space $Fred$ of [[Fredholm operator]]s.

### Chromatic filtration

[[!include chromatic tower examples - table]]

### As the shape of the smooth K-theory spectrum

See at _[[differential cohomology diagram]]_.

### Relation to algebraic K-theory
 {#RelationToAlgebraicKTheory}

The topological K-theory over a space $X$ is not
identical with the _[[algebraic K-theory]]_ of the
ring of functions on $X$, but the two are closely related. See for instance ([Paluch](#Paluch), [Rosenberg](#Rosenberg)). See at _[[comparison map between algebraic and topological K-theory]]_.




## Related concepts

* [[virtual vector bundle]]

* [[K-theory]]

* **topological K-theory

  * [[Atiyah-Bott-Shapiro isomorphism]]

  * [[topological index]]

  * [[KR-theory]]

* [[groupoid K-theory]]

* [[twisted K-theory]]

* [[differential K-theory]]

* [[twisted differential K-theory]]

[[!include orientations in higher quantization - table]]

[[!include string theory and cohomology theory -- table]]


## References 

The "ring of complex vector bundles" $K(X)$ was introduced in

* {#AtiyahHirzebruch61} [[M. F. Atiyah]], [[F. Hirzebruch]], _Riemann-Roch theorems for differentiable manifolds_, Bull.  Amer. Math Soc. vol. 65 (1959) pp. 276-281. 

and shown to give a [[generalized (Eilenberg-Steenrod) cohomology]] theory in

* {#AtiyahHirzebruch61} [[M. F. Atiyah]], [[F. Hirzebruch]], _Vector bundles and homogeneous spaces_, 1961, Proc. Sympos. Pure Math., Vol. III pp. 7&#8211;38 American Mathematical Society, Providence, R.I. ([web](http://hirzebruch.mpim-bonn.mpg.de/87/), [MR 0139181](http://www.ams.org/mathscinet-getitem?mr=0139181))


Early lecture notes on topological K-theory in a general context of [[stable homotopy theory]] and [[generalized cohomology theory]] includes

* {#Adams74} [[Frank Adams]], part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

Textbook accounts on topological K-theory include

* [[M. F. Atiyah]], _K-theory_, Benjamin New-York (1967)

* {#Karoubi} [[Max Karoubi]], _K-theory: an introduction_, Grundlehren der Math. Wissen. 226 Springer 1978, Reprinted in Classics in Mathematics (2008)

* {#Hatcher} [[Allen Hatcher]], _Vector bundles and K-theory_, 2003/2009 ([web](http://www.math.cornell.edu/~hatcher/VBKT/VBpage.html))


Further introductions include

* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], _[[Spin geometry]]_, Princeton University Press (1989)

* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 9 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* {#Karoubi06} [[Max Karoubi]], _K-theory. An elementary introduction_, lectures given at the Clay Mathematics Academy ([arXiv:math/0602082](https://arxiv.org/abs/math/0602082)) 

* {#Friedlander} [[Eric Friedlander]], _An introduction to K-theory_ (emphasis on [[algebraic K-theory]]), 2007 ([pdf](http://users.ictp.it/~pub_off/lectures/lns023/Friedlander/Friedlander.pdf))
 
* {#Karpova09} [[Varvara Karpova]], _Complex topological K-theory_, 2009  ([pdf](http://infoscience.epfl.ch/record/162450/files/karpova.semestre.hess2.pdf))

* {#Wirthmuller12} [[Klaus Wirthmüller]], _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))

* Aderemi Kuku, _Introduction to K-theory and some applcations_ ([pdf](https://www.math.ksu.edu/~zlin/kuku/Intro-Kthy.pdf))

A textbook account of topological K-theory with an eye towards [[operator K-theory]] is section 1 of

* [[Bruce Blackadar]], _[[K-Theory for Operator Algebras]]_

A discussion of the topological K-theory of [[classifying spaces]] of [[Lie groups]] is in 

* {#JackowskiOliver} Stefan Jackowski and Bob Oliver, _Vector bundles over classifying spaces of compact Lie groups_ ([pdf](http://hopf.math.purdue.edu/Jackowski-Oliver/bg-bu.pdf))
 

The [[comparison map between algebraic and topological K-theory]] is discussed for instance in

* {#Paluch} Michael Paluch, _Algebraic $K$-theory and topological spaces_ K-theory 0471 ([web](http://www.math.uiuc.edu/K-theory/0471/))
 

* {#Rosenberg} [[Jonathan Rosenberg]], _Comparison Between Algebraic and Topological K-Theory for Banach Algebras and $C^*$-Algebras_, ([pdf](http://www2.math.umd.edu/~jmr/algtopK.pdf))
 
Discussion from the point of view of [[smooth stacks]] and [[differential K-theory]] is in 

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_, Journal of Homotopy and Related Structures October 2014 ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

The proof of the [[Hopf invariant one]] theorem in terms of topological K-theory is due to

* {#AdamsAtiyah66} [[Frank Adams]], [[Michael Atiyah]], _K-theory and the Hopf invariant_, Quart. J. Math. Oxford (2), 17 (1966), 31-38 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/adamatiy.pdf))


[[!redirects complex K-theory]]

[[!redirects periodic complex K-theory]]

[[!redirects complex topological K-theory]]