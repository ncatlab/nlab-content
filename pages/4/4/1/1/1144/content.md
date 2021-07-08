 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea
  {#LieModels}

Rational homotopy theory is the [[homotopy theory]] of [[rational topological spaces]], hence of rational [[homotopy types]]: [[simply connected topological space|simply connected]] [[topological spaces]] whose [[homotopy groups]] are [[vector spaces]] over the [[rational numbers]] ([[rational vector spaces]]).

Much of the theory is concerned with [[rationalization]], the process that sends a general homotopy type to its closest rational approximation, in a precise sense. On the level of [[homotopy groups]] this means to retain precisely the non-[[torsion subgroups]] of the homotopy groups.

Two algebraic models of rational homotopy types exist, via [[differential graded-commutative algebras]] (Sullivan model) and via [[dg-Lie algebras]] (Quillen model).

This way rational homotopy theory connects [[homotopy theory]] and [[differential graded algebra]]. Akin to the [[Dold-Kan correspondence]], the [[Sullivan construction]] in rational homotopy theory connects the conceptually powerful perspective of [[homotopy theory]] with the computationally powerful perspective of [[differential graded algebra]].

Moreover, via the [[homotopy hypothesis]] the study of [[topological spaces]] is connected to that of [[∞-groupoids]], so that rational homotopy theory induces a bridge (the [[Sullivan construction]]) between [[∞-groupoids]] and [[differential graded algebra]]. It was observed essentially by ([Henriques 08](Lie+integration#Henriques), [Getzler 09](Lie+integration#Getzler04)) that this bridge is [[Lie integration]] (see there) in the [[∞-Lie theory]] of [[L-∞ algebras]].

$\,$

There are two established approaches in rational homotopy theory for encoding rational homotopy types in terms of [[Lie theory|Lie theoretic data]]:

1. In the **Sullivan approach** ([Sullivan 77](#Sullivan77)) a 1-connected rational space, in its incarnation as a [[simplicial set]],
is turned into something like a piecewise smooth space by [[nerve and realization|realizing]] each abstract $n$-[[simplex]] by the standard $n$-simplex in $\mathbb{R}^n$; and then a [[dg-algebra]] of [[differential form]]s on this piecewise smooth space
is formed by taking on each simplex the dg-algebra of ordinary rational [[polynomial differential forms]] and gluing these dg-algebras all together.

1. In the **Quillen approach** ([Quillen 69](#Quillen69)) the [[loop space]] of the rational space/simplicial set is formed and its [[H-space]] structure strictified to a [[simplicial group]], of which then a [[dg-Lie algebra]] (a strict [[L-infinity-algebra]]) is formed by mimicking the construction of the Lie algebra of a [[Lie group]] from the [[primitive element]]s of its completed [[group ring]]: the group ring of the simplicial group here is a simplicial ring, whose degreewise primitive elements hence yield a [[simplicial Lie algebra]]. The [[Moore complex]] functor maps this to the [[dg-Lie algebra]] functor that models the rational homotopy type in the Quillen approach.


The connection between these two appoaches is discussed in ([Majewski 00](#Majewski00)): The Sullivan dg-algebra of forms is the [[formal dual]] (the [[Chevalley-Eilenberg algebra]]) of an [[L-infinity algebra]] that may be rectified (see at _[[model structure for L-infinity algebras]]_) to a [[dg-Lie algebra]], and that is the one from Quillen's construction.

(Beware that --  while both rational homotopy types as well as $L_\infty$-algebras are presented by [[formal duals]] of [[dg-algebras]] (via [[Sullivan construction]] and via forming [[Chevalley-Eilenberg algebras]], respectively) -- the class of [[weak equivalences]] in the former case strictly includes that in the latter. See [this remark](model+structure+for+L-infinity+algebras#OndgCoAlgWEs) at _[[model structure for L-∞ algebras]]_.)

$\,$

{#ClassifyingSpacesOfAcyclicGroups} Rational homotopy theory is mostly restricted to [[simply connected topological spaces]]. This is due to the existence of [[acyclic groups]] $\Gamma$ whose [[classifying space]] $B \Gamma$ is an "acyclic space" in that its [[ordinary cohomology]] vanishes in positive degrees. This means that [[Sullivan algebras]] do not distinguish classifying spaces of acyclic groups from [[contractible spaces]]. But by [[Hurewicz theorem]] asking that all spaces be [[simply connected topological space|simply connected]] precisely makes all "acyclic spaces" be [[contractible topological space|contractible]].


## Generalities

+-- {: .num_prop #RationalHomotopyEquivalenceCoincidesWithRationalHomologyEquivalence}
###### Proposition

Let $X$ and $Y$ by [[simply connected topological spaces]]. Then a [[continuous function]] $f \colon X \to Y$ is a [[isomorphism]] on [[homotopy groups]] after [[tensor product of abelian groups|tensor product]] with the [[rational numbers]] $\mathbb{Q}$

$$
  \pi_\bullet(f) \otimes \mathbb{Q}
    \;\colon\;
  \pi_\bullet(X) \otimes \mathbb{Q}
    \overset{\simeq}{\longrightarrow}
  \pi_\bullet(Y) \otimes \mathbb{Q}
$$

precisely if it induces an [[isomorphism]] on [[ordinary homology]] with [[rational numbers]] [[coefficients]]:

$$
  H_\bullet(f,\mathbb{Q})
    \;\colon\;
  H_\bullet(X,\mathbb{Q})
    \overset{\simeq}{\longrightarrow}
  H_\bullet(Y,\mathbb{Q})
  \,.
$$


=--

This is due to ([Serre 53](#Serre53)).

+-- {: .num_defn }
###### Definition

A map $f$ satisfying the equivalent conditions of def. \ref{RationalHomotopyEquivalenceCoincidesWithRationalHomologyEquivalence} is called a _[[rational homotopy equivalence]]_.

=--

## Sullivan approach
 {#SullivanApproach}

We review here the Sullivan approach to rational homotopy theory, where rational topological spaces are modeled by [[differential graded-commutative algebras]] over the [[rational numbers]] with good (cofibrant) representatives being [[Sullivan algebras]] which are [[formal duals]] to [[L-infinity algebras]].

First we discuss how to define an analog of the construction of the [[de Rham dg-algebra]] of a [[smooth manifold]] for [[topological spaces]]:

* _[Differential forms on topological spaces](#FormsOnTopSpaces)_.

These dg-algebras of "[[piecewise polynomial differential forms|piecewise polynomial]]" differential forms on a topological space are typically extremely large and unwieldy. Much more tractable dg-algebras are the [[minimal Sullivan algebra]], which we discuss next:

* _[Sullivan models](#SullivanModels)_.

The relation between these algebras is that the Sullivan algebras are the cofibrant resolutions of the larger dg-algebras. In order to make this precise, we next recall some basics of topological and algebraic [[homotopy theory]] in

* _[Homotopy theory](#HomotopyTheory)_

Finally we state and discuss the main theorem, that the construction of dg-algebras of [piecewise polynomial differential forms]] on a topological space exhibits an [[equivalence of categories|equivalence]] between the [[homotopy theory]] of [[simply connected topological space|simply connected]] [[rational topological spaces]] [[of finite type]] and that of [[minimal Sullivan algebras]]:

* _[The rationalization adjunction](#SullivanRationalizationAdjunction)_


### Differential forms on topological spaces
  {#FormsOnTopSpaces}

A central tool in the study of rational topological spaces is an assignment that sends each [[topological space]]/[[simplicial set]] $X$ to a [[dg-algebra]] $\Omega^\bullet_{poly}(X)$ that behaves like the [[deRham complex|deRham dg-algebra]] of a smooth [[manifold]]. Instead of consisting of smooth [[differential forms]], $\Omega^\bullet_{poly}(X)$ consists of _piecewise linear polynomial differential forms_ , in a way described in detail now.

We first discuss this semi-formally in

* _[Idea](#DifferentialFormsOnSpacesIdea)_

and then in more detail in

* _[Details](#FormsOnSpacesDetails)_.


#### Idea
 {#DifferentialFormsOnSpacesIdea}

The construction of $\Omega^\bullet_{poly}$ is a special case of the following general construction:

Let $C$ be any [[small category]], write $PSh(C) = [C^{op}, Set]$ for its category of [[presheaf|presheaves]] and let

$$
  \Omega^\bullet_C : C^{op} \to dgcAlg
$$

be _any_ functor to the category of [[dg-algebra]]s. Following the logic of [[space and quantity]], we may think of the objects of $C$ as being _test spaces_ and the functor $\Omega^\bullet_C$ as assigning to each test space its [[deRham complex|deRham dg-algebra]].

An example of this construction that is natural from the point of view of [[differential geometry]] appears in the study of [[diffeological space]]s, where $C$ is some subcategory of the category [[Diff]] of smooth [[manifold]]s, and $\Omega^\bullet_C$ is the restriction of the ordinary assignment of [[differential form]]s to this. But in the application to topological spaces, in the following, we need a choice for $C$ and $\Omega^\bullet_C$ that is non-standard from the point of view of [[differential geometry]]. Still, it follows the same general pattern.

After postcomposing with the [[forgetful functor]] that sends each [[dg-algebra]] to its underlying [[set]], the functor $\Omega^\bullet_C$ becomes itself a [[presheaf]] on $C$. For $X \in PSh(C)$ any other presheaf, we extend the notation and write

$$
  \Omega^\bullet_C(X) := Hom_{PSh(C)}(X, \Omega^\bullet_C)
$$

for the [[hom-set]] of presheaves. One checks that this set naturally inherits the structure of a [[dg-algebra]] itself, where all operations are given by applying "pointwise" for each $p : U \to X$ with $U \in C$ the operations in $\Omega^\bullet_C(U)$. This way we get a functor

$$
  \Omega^\bullet_C : PSh(C) \to dgcAlg^{op}
$$

to the [[opposite category]] of that of [[dg-algebra]]s. We may think of $\Omega^\bullet_C(X)$ as the deRham complex of the presheaf $X$ as seen by the functor $\Omega^\bullet_C : C \to dgcAlg^{op}$.

By the general discussion at  _[[nerve and realization]]_ this functor has a [[right adjoint]] $K_C : dgcAlg^{op} \to PSh(C)$, that sends a dg-algebra $A$ to the [[presheaf]]

$$
  K_C(A) : U \mapsto Hom_{dgcAlg}(\Omega^\bullet_C(U), A)
  \,.
$$

The [[adjunction]]

$$
  \Omega^\bullet_C : PSh(C) \stackrel{\leftarrow}{\to} : dgcAlg^{op} : K_C
$$

is an example for the adjunction induced from a [[dualizing object]].

See [[differential forms on presheaves]] for more.


For the purpose of rational homotopy theory, consider the following special case of the above general discussion of differential forms on presheaves.

Recall that by the [[homotopy hypothesis]] theorem, [[Top]] is equivalent to [[sSet]]. In the sense of [[space and quantity]], a [[simplicial set]] is a "generalized space modeled on the [[simplex category]]": a [[presheaf]] on $\Delta$.

Therefore set in the above $C \coloneqq \Delta$.

Now, a simplicial set has no smooth structure in terms of which one could define differential forms globally, but of course each abstract  $k$-[[simplex]] $\Delta[k]$ may be regarded as the standard $k$-simplex $\Delta^k_{Diff}$ in [[Diff]], and as such it supports smooth differential forms $\Omega^\bullet_{deRham}(\Delta^k_{Diff})$.

The functor $\Omega^\bullet_{deRham}( \Delta_{Diff}^{(-)} ) : \Delta^{op} \to dgcAlg$ obtained this way is _almost_ the one that -- after fed into the above procedure -- is used in rational homotopy theory.

The only difference is that for the purposes needed here, it is useful to cut down the smooth differential forms to something smaller. Let $\Omega^\bullet_{poly}(\Delta^k_{Diff})$ be the [[dg-algebra]] of **polynomial differential forms** on the standard $k$-simplex. Notice that this recovers all differential forms after tensoring with smooth functions:

$$
  \Omega^\bullet(\Delta^k_{Diff}) =
  C^\infty(\Delta^k_{Diff}) \otimes_{\Omega^0_{poly}(\Delta^k_{Diff})} \Omega^\bullet_{poly}(\Delta^k_{Diff})
  \,.
$$

For more details see at [[differential forms on simplices]].

#### Details
  {#FormsOnSpacesDetails}

We discuss the definition of polynomial differential forms on topological spaces in more detail.

+-- {: .num_defn #SmoothnSimplex}
###### Definition
**(smooth $n$-simplex)**

For $n \in \mathbb{N}$ the _smooth [[n-simplex]]_ $\Delta^n_{smth}$ is the [[smooth manifold]] with [[manifold with boundary|boundary]] and [[manifold with corners|corners]] defined, up to [[isomorphism]], as the following locus inside the [[Cartesian space]] $\mathbb{R}^{n+1}$:

$$
  \Delta^n_{smth}
  \;\coloneqq\;
  \left\{
    (x_0, x_1, \cdots, x_n)
    \in
    \mathbb{R}^{n+1}
     \;\vert\;
     0 \leq x_i \leq 1
     \;\text{and}\;
     \underoverset{i = 0}{n}{\sum}
     x_i
     \; = 0
  \right\}
  \hookrightarrow
  \mathbb{R}^{n+1}
  \,.
$$

For $0 \leq i \leq n$ the [[function]]

$$
  x_i \;\colon\; \Delta^n_{smth} \to \mathbb{R}
$$

which picks the $i$th component in the above definition is called the $i$th _barycentric coordinate function_.

For

$$
  f \;\colon\; [n_1] \longrightarrow [n_2]
$$

a morphism of finite non-empty [[linear orders]] $[n] \coloneqq \{0 \lt 1 \lt \cdots \lt n\}$, let

$$
  \Delta_{smth}(f)
     \;\colon\;
  \Delta^{n_1}_{smth}
    \longrightarrow
  \Delta^{n_2}_{smth}
$$

be the [[smooth function]] defined by $x_i \mapsto x_{f(i)}$.



=--

+-- {: .num_defn #dgcAlgebras}
###### Definition

For definiteness, we write

$$
  dgcAlg_{\mathbb{Q}, \geq 0}
$$

for the [[category]] of [[differential graded-commutative algebras]] over the [[complex numbers]] in non-negative $\mathbb{Z}$-degree, i.e. $\mathbb{N}$-graded.

=--


+-- {: .num_defn #SmoothDifferentialFormsOnSmoothnSimplex}
###### Definition
**(smooth differential forms on the smooth $n$-simplex)

For $k \in \mathbb{N}$ then a [[smooth differential k-form]] on the smooth $n$-simplex (def. \ref{SmoothnSimplex}) is a smooth differential form in the sense of [[smooth manifolds]] with [[manifold with boundary|boundary]] and [[manifold with corners|corners]]. Explicitly this means the following.

Let

$$
  F^n
  \;\coloneqq\;
  \left\{
    (x_0, x_1, \cdots, x_n)
    \in
    \mathbb{R}^{n+1}
     \;\vert\;
     \underoverset{i = 0}{n}{\sum}
     x_i
     \; = 0
  \right\}
  \hookrightarrow
  \mathbb{R}^{n+1}
$$

be the affine plane in $\mathbb{R}^{n+1}$ that contains $\Delta^n_{smth}$ in its defining inclusion from def. \ref{SmoothnSimplex}. This is a [[smooth manifold]] [[diffeomorphism|diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^{n}$.

A smooth differential form on $\Delta^n_{smth}$ of degree $k$ is a collection of [[linear functions]]

$$
  \wedge^k T_x F^n \longrightarrow \mathbb{R}
$$

out of the $k$-fold skew-symmetric [[tensor power]] of the [[tangent space]] of $F^n$ at some point $x$ to the [[real numbers]], for all $x \in \Delta^n_{smth}$ such that this extends to a smooth differential $k$-form on $F^n$.

Write $\Omega^\bullet(\Delta^n_{smth})$ for the graded [[real vector space]] defined this way. By definition there is then a canonical linear map

$$
  \Omega^\bullet(F^n) \longrightarrow \Omega^\bullet(\Delta^n_{smth})
$$

from the [[de Rham complex]] of $F^n$ and there is a unique structure of a [[differential graded-commutative algebra]] on $\Omega^\bullet(\Delta^n_{smth})$ that makes is a [[homomorphism]] of [[dg-algebras]] form the [[de Rham algebra]] of $F^n$. This is the de Rham algebra of smooth differential forms on the smooth $n$-simplex.

For $f \colon [n_1] \to [n_2]$ a homomorphism of finite non-empty [[linear orders]] with $\Delta_{smth}(f) \colon \Delta^{n_1}_{smth} \to \Delta^{n_2}_{smth}$ the corresponding smooth function according to def. \ref{SmoothnSimplex}, there is the induced [[homomorphism]] of [[differential graded-commutative algebras]]

$$
  (\Delta_{smth}(f))^\ast
    \;\colon\;
  \Omega^\bullet(\Delta^{n_2}_{smth})
    \longrightarrow
  \Omega^\bullet(\Delta^{n_1}_{smth})
$$

induced from the usual [[pullback of differential forms]] on $F^n$. This makes smooth differential forms on smooth simplices be a [[simplicial object]] in [[differential graded-commutative algebras]] (def. \ref{dgcAlgebras}):

$$
  \Omega^\bullet(\Delta^{(-)}_{smth})
    \;\colon\;
   \Delta^{op}
     \longrightarrow
   dgcAlg_{\mathbb{R}, \geq 0}
  \,.
$$

=--

+-- {: .num_defn #PolynomialDifferentialForms}
###### Definition

For $n \in \mathbb{N}$ write

$$
  \Omega_{poly}^{\bullet}(\Delta^n)
   \;\coloneqq\;
  Sym^\bullet_{\mathbb{Q}}
   \langle t_0, \cdots, t_n, d t_0, \cdots, d t_n\rangle/\left(\sum t_i -1, \sum d t_i \right)
$$

for the [[quotient]] of the $\mathbb{Z}$-graded [[symmetric algebra]] over the [[rational numbers]] on $n+1$ generators $t_i$ in degree 0 and $n+1$ generators $d t_i$ of degree 1.

In particular in degree 0 this are called the _polynomial functions_

$$
  \Omega^0_{poly}(\Delta^n)
  \;=\;
  \mathbb{Q}[t_0, t_1, \cdots t_n]/\left( \underset{i}{\sum} t_i = 0 \right)
$$

due to the canonical inclusion

$$
  \Omega^0_{poly}(\Delta^n)
    \hookrightarrow
  C^\infty(\Delta^n_{smth})
$$

into the [[smooth functions]] on the $n$-simplex according to def. \ref{SmoothDifferentialFormsOnSmoothnSimplex}, obtained by regarding the generator $t_i$ as the $i$th barycentric coordinate function.

Observe that the [[tensor product]] of the polynomial differential forms over these polynomial functions with the [[smooth functions]] on the $n$-simplex, is canonically [[isomorphism|isomorphic]] to the space $\Omega^\bullet(\Delta^n_{smth})$ of smooth [[differential forms]], according to def. \ref{SmoothDifferentialFormsOnSmoothnSimplex}:

$$
  \Omega^\bullet(\Delta^n_{smth})
    \simeq
  C^\infty(\Delta^n_{smth}) \otimes_{\Omega^0_{poly}(\Delta^n)}
  \Omega^\bullet_{poly}(\Delta^n)
$$

where moreover the generators $d t_i$ are identified with the de Rham differential of the $i$th barycentric coordinate functions.

This defines a canonical inclusion

$$
  \Omega^\bullet_{poly}(\Delta^n)
    \hookrightarrow
  \Omega^\bullet(\Delta^n_{smth})
$$

and there is uniquely the structure of a [[differential graded-commutative algebra]] on $\Omega^\bullet_{poly}(\Delta^n)$ that makes this a [[homomorphism]] of [[dg-algebras]]. This is the _dg-algebra of polynomial differential forms_.


For $f \colon [n_1] \to [n_1]$ a [[morphism]] of finite non-empty [[linear orders]], let

$$
  \Omega^\bullet_{poly}(f)
   \;\colon\;
  \Omega^\bullet_{poly}(\Delta^{n_2}) \to \Omega^\bullet_{poly}(\Delta^{n_1})
$$

be the morphism of dg-algebras given on generators by

$$
  \Omega^\bullet_{poly}(f) : t_i \mapsto \sum_{f(j) = i} t_j
  \,.
$$

This yields a [[simplicial object|simplicial]] [[differential graded-commutative algebra]]

$$
  \Omega^\bullet_{poly}(\Delta^{(-)}) : \Delta^{op} \to cdgcAlg_k
$$

which is a sub-simplicial object of that of smooth differential form

$$
  \Omega^\bullet_{poly}(\Delta^{(-)})
    \hookrightarrow
  \Omega^\bullet(\Delta_{smth}^{(-)})
  \,.
$$

=--


+-- {: .num_defn #AdjunctionBetweenSimplicialSetAnddgcAlgebras}
###### Definition

Consider the [[simplicial object|simplicial]] [[differential graded-commutative algebra]] of [[polynomial differential forms]] from def. \ref{PolynomialDifferentialForms}, equivalently a [[cosimplicial object]] in the [[opposite category]] of [[differential graded-commutative algebras]] (def. \ref{dgcAlgebras}):

$$
  \Omega^\bullet_{poly}
    \;\colon\;
  \Delta
    \longrightarrow
  dgcAlg_{\mathbb{Q}, \geq 0}^{op}
  \,.
$$

By the general discussion at _[[nerve and realization]]_, this induces a pair of [[adjoint functors]] between the [[opposite category]] of [[differential graded-commutative algebras]] $(dgcAlg_{\mathbb{Q}, \geq 0})^{op}$ (def. \ref{dgcAlgebras}) and the category [[sSet]] of [[simplicial sets]]:

$$
  (\Omega^\bullet_{poly} \dashv \mathcal{K}_{poly})
    \;\colon\;
  (dgcAlg_{\mathbb{Q}, \geq 0})^{op}
    \underoverset
      {\underset{K_{poly}}{\longrightarrow}}
      {\overset{\Omega^\bullet_{poly}}{\longleftarrow}}
      {\bot}
  sSet
  \,.
$$

Here the [[left adjoint]] is the [[left Kan extension]] of $\Omega \bullet_{poly}$ along the [[Yoneda embedding]] $\Delta \hookrightarrow sSet$, which we denote by the same symbols.

=--

This adjunction is an algebraic analog of the [[singular simplicial complex]] construction, which we briefly recall (for detailed exposition see at _[[geometry of physics -- homotopy types]]_):

+-- {: .num_defn #SingluarNerveAndRealization}
###### Definition

For $n \on \mathbb{N}$, write $\Delta^n_{top}$ for the [[n-simplex]] canonically regarded as a [[topological space]], i.e. the topological space underlying the smooth simplex $\Delta^n_{smth}$ from def. \ref{SmoothnSimplex}.  As in def. \ref{PolynomialDifferentialForms} this is a [[cosimplicial object]]

$$
  \Delta^{(-)}_{top}
  \;\colon\;
  \Delta \longrightarrow Top
$$

now in the [[category]] [[Top]] of [[topological spaces]].

This also induces a [[nerve and realization]] [[adjunction]]

$$
  ({\vert -\vert} \dashv Sing)
  \;\colon\;
  Top
    \underoverset
      {\underset{Sing}{\longrightarrow}}
      {\overset{{\vert -\vert}}{\longleftarrow}}
      {\bot}
  sSet
$$

where the [[left adjoint]] $Sing$ is the [[singular simplicial complex]] functor and the [[right adjoint]] ${\vert- \vert}$ is the [[geometric realization]] functor.

=--

+-- {: .num_defn #AdjunctionBetweenTopopologicalSpacesAnddgcAlgebras}
###### Definition


Combining the [[functors]] from def. \ref{AdjunctionBetweenSimplicialSetAnddgcAlgebras} and def. \ref{SingluarNerveAndRealization} we finally obtain a functorial association of differential forms to a topological space


$$
  \Omega^\bullet_{pwpoly}
   \;\colon\;
  Top
   \overset{Sing}{\longrightarrow}
  sSet
   \overset{\Omega^\bullet_{poly}}{\longrightarrow}
  (dgcAlg_{\mathbb{Q}, \geq 0})^{op}
$$

(foring "[[piecewise polynomial differential forms]]") and a functorial operation that turns every [[differential graded-commutative algebra]] into a topological space

$$
  Spec
   \;\colon\;
  (dgcAlg_{\mathbb{Q}, \geq 0})^{op}
    \overset{K_{poly}}{\longrightarrow}
  sSet
    \overset{\vert - \vert}{\longrightarrow}
  Top
  \,.
$$


=--



### Sullivan models
  {#SullivanModels}


+-- {: .num_defn #SullivanAlgebra}
###### Definition
**(Sullivan algebras)**

A **relative Sullivan algebra** is a [[homomorphism]] of [[differential graded-commutative algebras]] in non-negative degrees, hence a [[morphism]] in $dgcAlg_{\geq 0}$, that is an inclusion of the form

$$
  (A,d) \hookrightarrow (A \otimes_k \wedge^\bullet V, d')
$$

$$
  a \mapsto a \otimes 1
$$

for $(A,d) \in dgcAlg_{\geq 0}$ any [[dgc-algebra]]  and for $V$ some [[graded vector space]], such that

1. there is a [[well ordered set]] $J$ indexing a [[linear basis]] $\{v_\alpha \in V| \alpha \in J\}$ of $V$;

1. writing $V_{\lt \beta} \coloneqq span(v_\alpha | \alpha \lt \beta)$ we have for all basis elements $v_\beta$ that

  $$
    d' v_\beta \in A \otimes \wedge^\bullet V_{\lt \beta}
    \,.
  $$

(See remark \ref{MeaningOfOrderingCondition} below for what this means.)

Such a relative Sullivan algebra if called **minimal** if in addition the degrees of these basis elements increase [[monotone function|monotonicly]]:

$$
  (\alpha \lt \beta) \Rightarrow (deg v_\alpha  \leq deg v_\beta)
$$

If $A \in dgcAlg_{\geq 0}$ is such that the unique homomorphism

$$
  (\mathbb{Q}, d = 0) \hookrightarrow A
$$

is a (minimal) relative Sullivan algebra in the above sense, then $A$ is simply called a _(minimal) Sullivan algebra_. In particular this means that $A = (\wedge^\bullet, d)$ is a [[semifree dgc-algebra]].

=--

+-- {: .num_example}
###### Example

Let $\mathfrak{g}$ be a [[finite number|finite]] [[dimension|dimensional]] [[Lie algebra]] and write

$$
  CE(\mathfrak{g})
   \coloneqq
  (\wedge^\bullet \mathfrak{g}^\ast, d_\mathfrak{g} = [-,-]^\ast)
$$

for its [[Chevalley-Eilenberg algebra]]. This CE-algebra is a [[Sullivan algebra]] in the sense of def. \ref{SullivanAlgebra}, precisely if $\mathfrak{g}$ is a [[nilpotent Lie algebra]].


=--

+-- {: .num_example #GeneratingRelativeSullivanAlgebras}
###### Example

For $n \in \mathbb{N}$ let

$$
  S(n) \coloneqq (\wedge^\bullet \langle c \rangle, d = 0)
$$

be the dgc-algebra on a single generator in degree $n$ with vanishing differential.

For $n \geq 1$ let

$$
  D(n)
   \coloneqq
  (\wedge^\bullet (\langle b \rangle \oplus \langle c \rangle), d b = c, d c = 0)
$$

be the dgc-algebra generated by an additional generator in degree $n-1$ such that the differential takes this to the previous generator.

Then the canonical inclusions

$$
  i_0 \;\colon\; (\mathbb{Q},d = 0) \hookrightarrow S(0)
$$

and for $n \geq 1$

$$
  i_n \;\colon\; S(n) \hookrightarrow D(n)
$$

are relative Sullivan algebras according to \ref{SullivanAlgebra}.

These are to be called the _[[cofibrantly generated model category|generating cofibrations]]_ for the [[projective model structure on dgc-algebras]] below in theorem \ref{ProjectiveModelStructureOndgcAgebras}.

Moreover, the inclusions

$$
  (\mathbb{Q},d = 0) \hookrightarrow D(n)
$$

for $n \geq 1$ are relative Sullivan algebras.

These are to be called the _[[cofibrantly generated model category|generating acyclic cofibrations]]_ for the [[projective model structure on dgc-algebras]] below in theorem \ref{ProjectiveModelStructureOndgcAgebras}.


=--

([Hess 06, p. 6](#Hess06))

The examples in \ref{GeneratingRelativeSullivanAlgebras} are trivial, but they generate all examples of relative Sullivan algebras:


+-- {: .num_remark #MeaningOfOrderingCondition}
###### Remark

The special condition on the ordering in the relative Sullivan algebra in def. \ref{SullivanAlgebra} says that these morphisms are [[transfinite compositions]] of [[pushouts]] of the generating cofibrations in def. \ref{GeneratingRelativeSullivanAlgebras}:


For $A \in dgcAlg_{\geq 0}$ any [[dgc-algebra]], then a [[pushout]] of the form

$$
  \array{
     S(n) &\stackrel{\phi}{\longrightarrow}& A
     \\
     {}^{\mathllap{i_n}}\downarrow && \downarrow
     \\
     D(n)
       &\longrightarrow&
    (A \otimes \wedge^\bullet \langle b \rangle, d b = \phi)
  }
$$

is precisely a choice $\phi \in A$ of a $d_A$-closed element in degree $n$
and results in adjoining to $A$ the element $b$ whose differential is
$d b = \phi$.

This gives the condition in the above definition: the differential of any new element has to be a sum of wedge products of the old elements.


=--

+-- {: .num_defn #SullivanModel}
###### Definition
**(Sullivan models)**

For $X$ a [[simply connected]] [[topological space]] $X$, a **Sullivan (minimal) model** for $X$ is a Sullivan (minimal) algebra $(\wedge^\bullet V^\ast, d_V)$ equipped with a [[quasi-isomorphism]]

  $$
    (\wedge^\bullet V^*, d_V)
      \stackrel{\simeq}{\longrightarrow}
    \Omega^\bullet_{pwpoly}(X)
  $$

  to the dg-algebra of [[piecewise polynomial differential forms]].

=--

+-- {: .num_prop }
###### Proposition

Minimal Sullivan models (def. \ref{SullivanModel}) are unique up to [[isomorphism]].

=--

e.g [Hess 06, prop 1.18](#Hess06).


[[!include Sullivan models -- examples]]



### Homotopy theory
 {#HomotopyTheory}


#### Topological homotopy theory

We briefly recall classical statement of the equivalene of the [[homotopy theories]] of [[topological spaces]] and of [[simplicial sets]] ([[simplicial homotopy theory]]), i.e. the "[[homotopy hypothesis]]". For full exposition see at _[[geometry of physics -- homotopy types]]_.

+-- {: .num_theorem #TopQuillen}
###### Theorem

Say that a [[continuous function]], hence a [[morphism]] in the [[category]] [[Top]] of [[topological spaces]] is

* a _[[weak equivalence]]_ if it is a [[weak homotopy equivalence]];

* a _[[fibration]]_ if it is a [[Serre fibration]]

* a _[[cofibration]]_ if it is the [[retract]] of a [[relative cell complex]] inclusion.

These classes of morphisms make the category [[Top]] into a [[model category]], the _[[classical model structure on topological spaces]]_, to be denoted $Top_{Quillen}$.

=--


+-- {: .num_theorem #sSetQuillen}
###### Theorem

Say that a [[morphism]] of [[simplicial sets]] is

* a _[[weak equivalence]]_ if its [[geometric realization]] (def. \ref{SingluarNerveAndRealization}) is a [[weak homotopy equivalence]] of [[topological spaces]];

* a _[[fibration]]_ if it is a [[Kan fibration]];

* a _[[cofibration]]_ if it is a [[monomorphism]] (hence degreewise an [[injection]]).

These classes of morphisms make the [[category]] [[sSet]] of [[simplicial sets]] into a [[model category]], the _[[classical model structure on simplicial sets]]_, to be denoted $sSet_{Quillen}$.

=--

+-- {: .num_theorem}
###### Theorem

The [[singular simplicial complex|singular]] [[nerve and realization]] adjunction from def. \ref{SingluarNerveAndRealization} is a [[Quillen equivalence]] between the [[classical model structure on topological spaces]] (theorem \ref{TopQuillen}) and the [[classical model structure on simplicial sets]] (theore \ref{sSetQuillen}):

$$
  Top_{Quillen}
    \underoverset
      {\underset{Sing}{\longrightarrow}}
      {\overset{{\vert -\vert}}{\longleftarrow}}
      {\simeq_{Quillen}}
  sSet_{Quillen}
$$

=--



#### Algebraic homotopy theory

+-- {: .num_theorem #ProjectiveModelStructureOndgcAgebras}
###### Theorem

Say that a [[homomorphism]] of [[differential graded-commutative algebras]] in non-negative degrees is

* a _[[weak equivalence]]_ if its underlying [[chain map]] is a [[quasi-isomorphism]];

* a _[[fibration]]_ if it is degreewise a surjection

* a _[[cofibration]]_ if it is the [[retract]] of a [[relative Sullivan algebra]] inclusion (def. \ref{SullivanAlgebra}).

These classes of morphisms make the category of [[differential graded-commutative algebras]] over the [[rational numbers]] and in non-negative degree into a [[model category]], to be called the [[projective model structure on differential graded-commutative algebras]], $(dcgAlg_{\mathbb{Q} ,\geq 0})_{proj}$.

This is a [[cofibrantly generated model category]], with generating (acyclic) cofibrations the morphisms from example \ref{GeneratingRelativeSullivanAlgebras}.


=--

([Hess 06, p. 6](#Hess06))


### The rationalization adjunction
 {#SullivanRationalizationAdjunction}


+-- {: .num_theorem #SullivanRationalizationAdjunction}
###### Theorem

The [[adjunction]] of def. \ref{AdjunctionBetweenSimplicialSetAnddgcAlgebras} is a [[Quillen adjunction]] with respect to the [[classical model structure on simplicial sets]] on the left (theorem \ref{TopQuillen}), and the [[opposite model structure]] of the [[projective model structure on differential graded-commutative algebras]] on the right (theorem \ref{ProjectiveModelStructureOndgcAgebras}):

$$
  (dgcAlg_{\mathbb{Q}, \geq 0}_{proj})^{op}
    \underoverset
      {\underset{K_{poly}}{\longrightarrow}}
      {\overset{\Omega^\bullet_{poly}}{\longleftarrow}}
      {\phantom{\phantom{AA}{}_{Qu}}\bot_{Qu}\phantom{AA}}
  sSet_{Quillen}
$$

=--

This is due to ([Bousfield-Gugenheim 76, section 8](#BousfieldGugenheim76)) Review includes ([Hess 06, p. 9](#Hess06)).

+-- {: .num_defn #NilpotentObjects}
###### Definition
**(subcategories of nilpotent objects of finite type)**

Write

1. $Ho(Top_{\mathbb{Q},nil,fin}) \hookrightarrow Ho(Top)$ for the [[full subcategory]] on those [[topological spaces]] $X$ which are

   1. [[rational topological space|rational]]: their [[homotopy groups]] are uniquely divisible;

   1. [[nilpotent topological space|nilpotent]]: their [[fundamental group]] is a [[nilpotent group]];

   1. [[finite type]]: the $\mathbb{Q}$-vector space $H_\bullet(X,\mathbb{Q})$ are of [[finite number|finite]] [[dimension]].

1. $Ho(dgcAlg^{fin}_{\mathbb{Q},nil})$ for the [[full subcategory]] on the [[differential graded-commutative algebras]] which are equivalent to [[minimal Sullivan models]] $(\wedge^\bullet V, d)$ (def. \ref{SullivanAlgebra}) for which the [[graded vector space]] $V$ is of [[finite type]], i.e. is degreewise of [[finite number|finite]] [[dimension]] over $\mathbb{Q}$.

[Bousfield-Gugenheim 76, p. viii](#BousfieldGugenheim76)


=--

+-- {: .num_theorem #SullivanRationalizationEquivalence}
###### Theorem

Consider the [[adjunction]] of [[derived functors]]

$$
  Ho(Top)
   \simeq
  Ho(sSet)
   \underoverset
     {\underset{\mathbb{R} \Omega^\bullet_{poly}}{\longrightarrow}}
     {\overset{\mathbb{L} K_{poly} }{\longleftarrow}}
     {\bot}
  Ho( (dgcAlg_{\mathbb{Q}, \geq 0})^{op} )
$$

induced on [[homotopy category of a model category|homotopy categories]] (via [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) from the [[Quillen adjunction]] from theorem \ref{SullivanRationalizationAdjunction}.

On the [[full subcategories]] of [[nilpotent homotopy types]] of [[finite type]], def. \ref{NilpotentObjects}, this adjunction restricts to an [[equivalence of categories]]

$$
  Ho(Top)_{\mathbb{Q}, nil}^{fin}
   \underoverset
     {\underset{\mathbb{R} \Omega^\bullet_{poly}}{\longrightarrow}}
     {\overset{\mathbb{L} K_{poly} }{\longleftarrow}}
     {\simeq}
  Ho( (dgcAlg^{op}_\mathbb{Q})_{conn}^{fin}
  \,.
$$


In particular for such spaces the [[adjunction unit]]

$$
  X \longrightarrow K_{poly}(\Omega^\bullet_{pwpoly}(X))
$$

exhibits the [[rationalization]] of $X$.

=--


[Bousfield-Gugenheim 76, p. viii](#BousfieldGugenheim76)

e. g. [Hess 06, corollary 1.26](#Hess06).


+-- {: .num_cor #RationalCohomologyFromSullivanModel}
###### Corollary

It follows that the [[cochain cohomology]] of the cochain complex of [[piecewise polynomial differential forms]] on any topological, hence equivalently that of any of its [[Sullivan models]], coincides with its [[ordinary cohomology]] with coefficients in the [[rational numbers]]:

$$
  H^\bullet(X,\mathbb{Q})
    \;\simeq\;
  H^\bullet( \Omega^\bullet_{pwpoly}(X), d_{dR} )
  \,.
$$

=--

But more is true, also the rationalization of the [[homotopy groups]] may be read off from any [[minimal Sullivan model]]:

+-- {: .num_theorem #HomotopyGroupsFromSullivanGenerators}
###### Theorem

Let $(\wedge^\bullet V^*, d_V)$ be a minimal Sullivan model of a simply connected rational topological space $X$. Then there is an [[isomorphism]]

$$
  \pi_\bullet(X)
    \simeq
  V
$$

between the [[homotopy groups]] of $X$ and the generators of the minimal Sullivan model.

=--


e.g. [Hess 06, theorem 1.24](#Hess06).


+-- {: .num_remark}
###### Remark

The need to restrict to [[simply connected topological spaces]] in theorem \ref{SullivanRationalizationEquivalence} is due to the existence of [[acyclic groups]]. This are [[discrete groups]] $\Gamma$ such that their [[classifying space]] $B \Gamma$ has trival [[ordinary cohomology]] in positive degree

$$
  H^\bullet(B \Gamma, \mathbb{Q}) \simeq \mathbb{Q}
  \,.
$$

Therefore, by corollary \ref{RationalCohomologyFromSullivanModel}, its dg-algebra of [[piecewise polynomial differential forms]] do not distinguish such spaces from [[contractible topological spaces]]. But, unless $\Gamma = 1$ is in fact the trivial group,  $B \Gamma$ is not contractible, instead it is the [[Eilenberg-MacLane space]] $K(\Gamma,1)$ with nontrivial [[fundamental group]] $\pi_1(B \Gamma) \simeq \Gamma$.
However, by the [[Hurewicz theorem]], this fundamental group is the only obstruction to contractibility.


=--








### Examples
 {#SullivanModelExamples}


#### Rational $n$-spheres
  {#SullivanModelRationalSpheres}

We discuss the minimal Sullivan models of [[rational n-spheres]].

The minimal [[Sullivan model]] of a [[sphere]] $S^{2k+1}$ of odd [[dimension]] is the dg-algebra with a single generator $\omega_{2k+1}$ in degre $2k+1$ and vanishing differential

$$
  d \omega_{2k+1} = 0
  \,.
$$


The minimal [[Sullivan model]] of a sphere $S^{2k}$ of even dimension, for $k \geq 1$. is the dg-algeba with a generator $\omega_{2k}$ in degree $2k$ and another generator $\omega_{4k-1}$ in degree $4k+1$ with the differential defined by

$$
  d \omega_{2k}= 0
$$
$$
  d \omega_{4k+1} = \omega_{2k}\wedge \omega_{2k}
  \,.
$$

One may understand this form theorem \ref{HomotopyGroupsFromSullivanGenerators}: an $n$-sphere has rational cohomology concentrated in degree $n$. Hence its Sullivan model needs at least one closed generator in that degree. In the odd dimensional case one such is already sufficient, since the wedge square of that generator vanishes and hence produces no higher degree cohomology classes. But in the even degree case the wedge square $\omega_{2k}\wedge \omega_{2k}$ needs to be canceled in cohomology. That is accomplished by the second generator $\omega_{4k-1}$.

Again by theorem \ref{HomotopyGroupsFromSullivanGenerators}, this now implies that the rational [[homotopy groups of spheres]] are concentrated, in degree $2k+1$ for the odd $(2k+1)$-dimensional spheres, and in degrees $2k$ and $4k-1$ in for the even $2k$-dimensional spheres.

For instance the [[4-sphere]] has rational homotopy in degree 4 and 7. The one in degree 7 being represented by the [[quaternionic Hopf fibration]].


## Quillen approach
 {#QuillenApproach}


We briefly review Quillen's approach to rational homotopy theory ([Quillen 69](#Quillen69)), see for instance ([Griffith-Morgan 13, chapter 17](#GriffithMorgan13)) .

The following sequence of six consecutive functors, each of which is a [[Quillen equivalence]], takes one from a [[n-connected space|1-connected]] rational space $X$ to a [[dg-Lie algebra]].

One starts with the [[fundamental infinity-groupoid|singular simplicial set]]

$$
  S(X)
$$


and throws away all the simplices except the basepoint in degrees $0$ and $1$, to get a [[reduced simplicial set]].  Then one applies the Kan loop group functor (the simplicial analogue of the based [[loop space]] functor, see [here](simplicial+group#AsInfinityGroups)) to $S(X)$, obtaining an a [[simplicial group]]

$$
  G S(X).
$$

Then one forms its [[group ring]]

$$
  \mathbb{Q}[G S(X)]
$$

and completes it with respect to powers of its [[augmentation ideal]], obtaining a "reduced, complete simplicial [[Hopf algebra]]",

$$
  \hat \mathbb{Q}[G S(X)],
$$

which happens to be cocommutative, since the group ring is cocommutative. Taking degreewise [[primitive element|primitives]], one then gets a reduced simplicial Lie algebra

$$
  Prim(\hat \mathbb{Q}[G  S(X)]).
$$

At the next stage, the [[Moore complex|normalized chains functor]] is applied, to get Quillen's [[dg-Lie algebra]] model of $X$:

$$
  N^\bullet(Prim(\hat \mathbb{Q}[G S(X)])).
$$

Finally, to get a cocommutative dg [[coalgebra]] model for $X$, one uses a slight generalization of a functor first defined by Koszul for computing the homology of a Lie algebra, which always gives rise to a cocommutative dg coalgebra.


One may think of this procedure as doing the following: we are taking the [[Lie algebra]] of the "group" $\Omega X$ which is the [[loop space]] of $X$. From a group we pass to the enveloping algebra, i.e. the algebra of [[distribution]]s supported at the identity, completed. The topological analog of distributions are chains (dual to functions = cochains), so Quillen's completed chains construction is exactly the completed enveloping algebra. From the (completed) enveloping algebra we recover the Lie algebra as its primitive elements.


## Properties

### Preservation of homotopy pullbacks

+-- {: .num_theorem}
###### Theorem

The left [[derived functor]] of the [[Quillen functor|Quillen left adjoint]] $\Omega^\bullet_{poly} \colon sSet \to dgcAlg^{\geq 0}_{\mathbb{Q}}$ (thorem \ref{SullivanRationalizationAdjunction}) preserves [[homotopy pullbacks]] of objects of [[finite type]] (each rational homotopy group is a [[finite dimensional vector space]] over the [[ground field]]).

In other words in the induced pair of [[adjoint (∞,1)-functors]]

$$
  (\Omega^\bullet_{poly} \dashv {\vert -\vert_{poly}})
   :
  (dgcAlg^{\geq 0}_\mathbb{Q}^{op})^\circ
   \stackrel{\overset{}{\leftarrow}}{\underset{}{\to}}
  \infty Grpd
$$

the left adjoint preserves [[limit in a quasi-category|(∞,1)-categorical pullbacks]] of objects of finite type.

=--

+-- {: .proof}
###### Proof

This is effectively a restatement of a result that appears effectively below proposition 15.8 in HalperinThomas and is reproduced in some repackaged form as [Hess 06, theorem 2.2](#Hess06). We recall the [[model category|model category-theoretic]] context that allows to rephrase this result in the above form.

Let $C = \{a \to c \leftarrow b\}$ be the pullback [[diagram]] category.

The [[homotopy limit]] functor is the right [[derived functor]] $\mathbb{R} lim_C$ for the [[Quillen adjunction]] (described in detail at [[homotopy Kan extension]])

$$
  [C,sSet]_{inj} \stackrel{\overset{const}{\leftarrow}}{\underset{lim_C}{\to}}
  sSet
  \,.
$$

At [[model structure on functors]] it is discussed that composition with the Quillen pair $\Omega^\bullet \dashv K$ induces a Quillen adjunction

$$
  ([C,\Omega^bullet] \dashv [C,K])
  :
  [C, dgcAlg^{op}]
  \stackrel{\overset{[C,\Omega^\bullet]}{\leftarrow}}{\underset{[C,K]}{\to}}
  [C,sSet]
  \,.
$$

We need to show that for every fibrant and cofibrant pullback diagram $F \in [C,sSet]$ there exists a weak equivalence

$$
  \Omega^\bullet \circ lim_C F
  \;\;
  \simeq
  \;\;
  lim_C   \widehat{\Omega^\bullet(F)}
  \,,
$$

here $\widehat{\Omega^\bullet(F)}$ is a fibrant replacement of $\Omega^\bullet(F)$ in $dgcAlg^{op}$.

Every object $f \in [C,sSet]_{inj}$ is cofibrant. It is fibrant if all three objects $F(a)$, $F(b)$ and $F(c)$ are fibrant and one of the two morphisms is a fibration. Let us assume without restriction of generality that it is the morphism $F(a) \to F(c)$ that is a fibration. So we assume that $F(a), F(b)$ and $F(c)$ are three [[Kan complex]]es and that $F(a) \to F(b)$ is a [[Kan fibration]]. Then $lim_C$ sends $F$ to the ordinary [[pullback]]  $lim_C F = F(a) \times_{F(c)} F(b)$ in $sSet$, and so the left hand side of the above equivalence is

$$
  \Omega^\bullet(F(a) \times_{F(c)} F(b))
  \,.
$$


Recall that the [[Sullivan algebra]]s are the cofibrant objects in $dgcAlg$, hence the fibrant objects of $dgcAlg^{op}$. Therefore a fibrant replacement of $\Omega^\bullet(F)$ may be obtained by

* first choosing a [[Sullivan model]] $(\wedge^\bullet V, d_V) \stackrel{\simeq}{\to} \Omega^\bullet(c)$

* then choosing factorizations in $dgcAlg$ of the composites of this with $\Omega^\bullet(F(c)) \to \Omega^\bullet(F(a)) $ and $\Omega^\bullet(F(c)) \to \Omega^\bullet(F(b))$ into cofibrations follows by weak equivalences.

The result is a diagram

$$
  \array{
    (\wedge^\bullet U^*, d_U)
    &\leftarrow&
    (\wedge^\bullet V^*, d_V)
    &\hookrightarrow&
    (\wedge^\bullet W^* , d_W)
    \\
    \downarrow^{\simeq}
    &&
    \downarrow^{\simeq}
    &&
    \downarrow^{\simeq}
    \\
    \Omega^\bullet(F(a))
    &\stackrel{}{\leftarrow}&
    \Omega^\bullet(F(c))
    &\stackrel{}{\to}&
    \Omega^\bullet(F(b))
  }
$$

that in $dgcAlg^{op}$ exhibits a fibrant replacement of $\Omega^\bullet(F)$. The limit over that in $dgcAlg^{op}$ is the colimit

$$
  (\wedge^\bullet U^* , d_U)
  \otimes_{(\wedge^\bullet V^* , d_V)}
  (\wedge^\bullet W^* , d_W)
$$

in $dgcAlg$. So the statement to be proven is that there exists a weak equivalence

$$
  (\wedge^\bullet U^* , d_U)
  \otimes_{(\wedge^\bullet V^* , d_V)}
  (\wedge^\bullet W^* , d_W)
  \simeq
  \Omega^\bullet(F(a) \times_{F(c)} F(b))
  \,.
$$

This is precisely the statement of that quoted result [Hess 06, theorem 2.2](#Hess06).

=--


### Preservation of homotopy fibers

See at _[[rational fibration lemma]]_.



## Further variants of rational homotopy theory

There are various variants of [[homotopy theory]], such as [[stable homotopy theory]] or [[equivariant homotopy theory]]. Several of these have their coresponding rational models in terms of rational [[chain complexes]] equipped with extra structure. This includes the following:

* [[rational stable homotopy theory]]

* [[rational equivariant homotopy theory]]

* [[rational equivariant stable homotopy theory]]

* [[rational parametrized homotopy theory]]

* [[rational parameterized stable homotopy theory]]


## Related concepts

* [[PL de Rham complex]]

* [[rational cohomology]]

* [[rational Cohomotopy]]

* [[fundamental theorem of dg-algebraic rational homotopy theory]]

* from the [[nPOV]]: [[rational homotopy theory in an (infinity,1)-topos]].

* [[rational equivariant homotopy theory]], [[rational equivariant stable homotopy theory]]

* [[p-adic homotopy theory]]

* [[real homotopy theory]]

* [[fracture theorem]]

* [[integral chains homotopy theory]]

## References

### General

Precursors include

* {#Serre53} [[Jean-Pierre Serre]], _Groupes d'homotopy et classes de groupes abelians_, Ann. of Math. 58 (1953) 258-294

The original articles are

* {#Quillen69} [[Dan Quillen]], _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf))

* {#Sullivan77} [[Dennis Sullivan]], _Infinitesimal computations in topology_, Publications math&#233;matiques de l' I.H.&#201;.S. tome 47 (1977), p. 269-331. ([numdam:PMIHES_1977__47__269_0](http://www.numdam.org/item?id=PMIHES_1977__47__269_0), [pdf](http://archive.numdam.org/article/PMIHES_1977__47__269_0.pdf))

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

* {#Neisendorfer78} [[Joseph Neisendorfer]], _Lie algebras, coalgebras and rational homotopy theory for nilpotent spaces_, Pacific J. Math. Volume 74, Number 2 (1978), 429-460. ([euclid](http://projecteuclid.org/euclid.pjm/1102810284))

* {#Silveira84} [[Flavio da Silveira]], _Rational homotopy theory of fibrations_, Pacific Journal of Mathematics, Vol. 113, No. 1 (1984) ([pdf](http://msp.org/pjm/1984/113-1/pjm-v113-n1-p01-s.pdf))

* {#GriffithMorgan13} [[Phillip Griffiths]], [[John Morgan]], _Rational Homotopy Theory and Differential Forms_,  Progress in Mathematics Volume 16, Birkhauser (2013) ([doi:10.1007/978-1-4614-8468-4](https://doi.org/10.1007/978-1-4614-8468-4))


Survey and review includes

* {#FelixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000 ([doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9))

* {#FelixHalperinThomas15} [[Yves Félix]], [[Steve Halperin]], [[Jean-Claude Thomas]], _Rational Homotopy Theory II_, World Scientific 2015 ([doi:10.1142/9473](https://doi.org/10.1142/9473))

  (this second volume generalizes to the case of non-[[simply connected topological spaces]])

* {#Majewski00} Martin Majewski, _Rational homotopy models and uniqueness_ , AMS Memoir (2000):

* {#Hess06} [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_, contribution to _[Summer School on Interactions between Homotopy Theory and Algebra](https://jdc.math.uwo.ca/summerschool/)_, University of Chicago, July 26-August 6, 2004, Chicago ([arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626)), chapter in Luchezar Lavramov, [[Dan Christensen]], [[William Dwyer]], [[Michael Mandell]], [[Brooke Shipley]] (eds.), _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007 ([doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))

* [[Yves Félix]], [[John Oprea]], [[Daniel Tanré]], _Algebraic models in geometry_, Oxford University Press 2008 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/tanre.pdf), [ISBN:9780199206520](https://global.oup.com/academic/product/algebraic-models-in-geometry-9780199206520))


* {#Moerman15} [[Joshua Moerman]], _Rational Homotopy Theory_, 2015 ([pdf](https://www.ru.nl/publish/pages/813282/rational_homotopy_theory.pdf), [[MoermanRationalHomotopyTheory.pdf:file]])

* {#FelixHalperin} [[Yves Félix]], [[Steve Halperin]], _Rational homotopy theory via Sullivan models: a survey_,  Notices of the International Congress of Chinese Mathematicians Volume 5 (2017) Number 2 ([arXiv:1708.05245](https://arxiv.org/abs/1708.05245), [doi:10.4310/ICCM.2017.v5.n2.a3](https://dx.doi.org/10.4310/ICCM.2017.v5.n2.a3))



Review that makes the [[L-infinity algebra]] aspect completely manifest is in

* {#BuijsFelixMurillo12} [[Urtzi Buijs]], [[Yves Félix]], [[Aniceto Murillo]], _$L_\infty$-rational homotopy of mapping spaces_,  published as _$L_\infty$-models of based mapping spaces_,  J. Math. Soc. Japan Volume 63, Number 2 (2011), 503-524 ([arXiv:1209.4756](https://arxiv.org/abs/1209.4756), [doi:10.2969/jmsj/06320503](https://doi.org/10.2969/jmsj/06320503))


(which otherwise is about [[Sullivan models of mapping spaces]]).


More on the relation to Lie theory is in:

* [[Ezra Getzler]], _Lie theory for nilpotent $L_\infty$-algebras_ ([arXiv](http://arxiv.org/abs/math.AT/0404003))


The above description of the Quillen approach draws on blog comments by [[Kathryn Hess]] [here](http://golem.ph.utexas.edu/category/2010/01/this_weeks_finds_in_mathematic_50.html#c030961) and by [[David Ben-Zvi]] [here](http://golem.ph.utexas.edu/category/2010/01/this_weeks_finds_in_mathematic_50.html#c031038).

Discussion from the point of view of [[(∞,1)-category theory]] and [[E-∞ algebras]] is in

* [[Jacob Lurie]], Section 1 of: _Rational and $p$-adic homotopy theory_, 2011 ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-XIII.pdf), [[Lurie_RationalHomotopyTheory.pdf:file]])

An extension of rational homotopy theory to describe (some) non-[[simply connected spaces]] is given, using [[derived algebraic geometry]], in

* [[B. Toën]], _Champs affines_, Selecta Math. (N.S.) 12 (2006), no. 1, 39-135.

  See in particular Cor. 2.4.11, Cor. 2.5.3 and Cor. 2.5.4, and the MathOverflow answer [MO/79309](http://mathoverflow.net/a/79309) by [[Denis-Charles Cisinski]].

Generalization to non-[[connected spaces]] is discussed in

* {#BuijsMurillo12} [[Urtzi Buijs]], [[Aniceto Murillo]], _Algebraic models of non-connected spaces and homotopy theory of $L_\infty$-algebras_, Advances in Mathematics 236 (2013): 60-91. ([arXiv:1204.4999](https://arxiv.org/abs/1204.4999))

### Relation to Whitehead products

Relation to [[Whitehead products]]:

* {#Quillen69} [[Daniel Quillen]], section I.5 of _Rational Homotopy Theory_, Annals of Mathematics Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](https://www.jstor.org/stable/1970725))


* Christopher Allday, _Rational Whitehead products and a spectral sequence of Quillen_, Pacific J. Math. Volume 46, Number 2 (1973), 313-323 ([euclid:1102946308](https://projecteuclid.org/euclid.pjm/1102946308))

* Christopher Allday, _Rational Whitehead product and a spectral sequence of Quillen, II_, Houston Journal of Mathematics, Volume 3, No. 3, 1977 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.434.8821&rep=rep1&type=pdf))

* [[Pierre Deligne]], [[Phillip Griffiths]], [[John Morgan]], [[Dennis Sullivan]], _Real homotopy theory of Kähler manifolds_, Invent Math (1975) 29: 245 ([doi:10.1007/BF01389853](https://doi.org/10.1007/BF01389853))

* Peter Andrews, Martin Arkowitz, _Sullivan's Minimal Models and Higher Order Whitehead Products_, Canadian Journal of Mathematics, 30(5), 961-982, 1978 ([doi:10.4153/CJM-1978-083-6](https://doi.org/10.4153/CJM-1978-083-6))

* Francisco Belchí, [[Urtzi Buijs]], José M. Moreno-Fernández, Aniceto Murillo, _Higher order Whitehead products and $L_\infty$ structures on the homology of a DGL_, Linear Algebra and its Applications, Volume 520 (2017), pages 16-31 ([arXiv:1604.01478](https://arxiv.org/abs/1604.01478))
    


* Takahito Naito, _A model for the Whitehead product in rational mapping spaces_ ([arXiv:1106.4080](https://arxiv.org/abs/1106.4080))

### Generalization to arbitrary fundamental groups

Generalization to arbitrary [[fundamental groups]]:

* Antonio Gómez-Tato, [[Stephen Halperin]], [[Daniel Tanré]], _Rational Homotopy Theory for Non-Simply Connected Spaces_, Transactions of the American Mathematical Society, Transactions of the American Mathematical Society Vol. 352, No. 4 (Apr., 2000), pp. 1493-1525 (33 pages) ([jstor:118074](https://www.jstor.org/stable/118074))

* Syunji Moriya, _Rational homotopy theory and differential graded category_, Journal of Pure and Applied Algebra, Volume 214, Issue 4, April 2010, Pages 422-439 ([doi:10.1016/j.jpaa.2009.06.015](https://doi.org/10.1016/j.jpaa.2009.06.015))

* [Felix-Halperin-Thomas 15](#FelixHalperinThomas15)

* [[Urtzi Buijs]], [[Yves Félix]], [[Aniceto Murillo]], [[Daniel Tanré]], _Homotopy theory of complete Lie algebras and Lie models of simplicial sets_, Journal of Topology (2018) 799-825 ([arXiv:1601.05331](https://arxiv.org/abs/1601.05331), [doi:10.1112/topo.12073](https://doi.org/10.1112/topo.12073))



[[!redirects rational homotopy type]]
[[!redirects rational homotopy types]]
