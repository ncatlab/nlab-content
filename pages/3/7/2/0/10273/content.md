
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

> This page contains, or is going to contain, notes to go with a seminar of the [String Geometry Network meeting in October 2013](http://www-app.uni-regensburg.de/Fakultaeten/MAT/waldorf/Stringgeometry/index.php?show=events). 

#Contents#
* table of contents
{:toc}

## Introduction and survey

These notes concern the generalization of the notion of _[[gerbes]]_, of _[[principal 2-bundles]] with [[principal 2-connections]]_ and generally of _[[principal ∞-bundles]] with [[principal ∞-connection]]_ from [[higher differential geometry]] modeled on [[smooth manifolds]] to _[[higher supergeometry]]_ modeled on [[supermanifolds]].

A key motivation for this comes from applications to [[string theory]] and the induced [[higher geometry]]-analog of traditional [[spin geometry]] called _[[string geometry]]_:

Since early observations in the 1980s ([Gaw&#281;dzki 87](#Gawedzki87)) and then more prominently since ([Freed-Witten 99](FreedWitten99), [Carey-Johnson-Murray 02](#CareyJohnsonMurray02))), it is known that the [[B-field]] in [[string theory]] is mathematically a [[circle 2-bundle with connection]] and that the _[[WZW term]]_ in the [[action functional]] of the 2-dimensional [[string]] [[sigma-model]] with such a [[background gauge field]] is the [[surface holonomy]] of this 2-connection, in higher analogy of how the gauge [[interaction]] term of the [[electromagnetic field|electromagnetically]] [[charged particle]] is the line [[holonomy]] of a [[circle bundle with connection]] over the [[worldline]] of the [[particle]]. 

While this is well-explored by now, it has almost exclusively been applied to the [[bosonic string]], or else to the bosonic sector of the [[superstring]]. Notably the [[anomaly cancellation]] between the contributions of the [[B-field]] and of the [[fermions]] (on the [[string]]'s [[worldsheet]] and/or in [[spacetime]]) is typically considered in two independent steps: a computation in [[index theory]] gives the fermionic anomaly incarnated as a [[Pfaffian line bundle]], and then the contribution of the [[B-field]] to the anomaly is adjusted such as to cancel the class of this anomaly bundle. The main examples of this are the [[Freed-Witten-Kapustin anomaly]] in [[type II string theory]] (incarnated as [[spin^c structure]] serving as [[orientation in generalized cohomology|orientation]] in [[complex K-theory]]) and the [[Green-Schwarz anomaly]] in [[heterotic string theory]] (incarnated as [[string^c structure]] serving as [[orientation in generalized cohomology|orientation]] in [[tmf]]-[[cohomology theory]]).

However, since in [[string theory]] all the [[fermion|fermionic]] contributions are connected by ([[supergravity|local]]!) [[supersymmetry]] to the bosonic contributions, it is to be expected that on a more fundamental level there are not two independent contributions -- one in [[spin geometry]] (the [[fermions]]) and one [[higher differential geometry]] (the [[B-field]]) -- that happen to cancel each other, but that instead the [[field (physics)|fields]] arrange into one single structure ("supermultiplet") in the _[[higher supergeometry]]_.

By general principles of [[higher geometry]] it is clear what [[higher supergeometry]] is to be: the theory of [[∞-stacks]] over a [[site]] of [[supermanifolds]], hence of _[[smooth super ∞-groupoids]]_. The general notions of [[principal ∞-bundles]] and of [[principal ∞-connections]] apply to this ([[cohesive (∞,1)-topos|cohesive]]) [[(∞,1)-topos]] as to any other and hence in principle provide all the relevant structure.

It remains to work out more examples and applications. A good testing ground is the [[infinitesimal object|infinitesimal]] approximation of [[smooth super ∞-groupoids]] by their _[[super L-∞ algebras]]_. It turns out ([SSS 09](#SSS09)) that that these have _implicitly_ been recognized and used in the study of higher [[supergravity]] for a long time, starting with ([D'Auria-Fr&#233;-Regge 80](#DAuriaFre80)) and fully developed in ([Castellani-D'Auria-Fr&#233; 91](CastellaniDAuriaFre91)), namely in their dual incarnation via their [[Chevalley-Eilenberg algebras]]. In ([Nieuwenhuizen 83](#Nieuwenhuizen83)) these super-dg-algebras have been called "free differential algebras", abbreviated "FDA", referring to the fact that their underlying graded superalgebra is free on a [[super vector space]], hence is a super-[[Grassmann algebra]]. Since the [[differential]] on these [[Chevalley-Eilenberg algebras]] is crucially _not_ [[free construction|free]], in general, this is an unfortunate misnomer, but it did stick and is used ever since in the [[supergravity]] literature, see the references at _[[D'Auria-Fré formulation of supergravity]]_ and at _[[Green-Schwarz action functional]]_.

If however one does make the [[homotopy theory of L-∞ algebras]] explicit that is hidden in the "FDA"-formulation of [[supergravity]], then one sees that a large part of the literature has secretly been describing the infinitesimal approximation to [[supergeometry|supergeometric]] [[schreiber:∞-Wess-Zumino-Witten theory|higher WZW terms]] all along ([FSS 13b](#FSS13b)), namely in form of the [[Green-Schwarz action functionals]] for [[sigma-models]] of higher-dimensional [[branes]] propagating in a [[super spacetime]] [[target space]]. By ([FSS 13b, last section](#FSS13b)), each of these [[perturbation theory|perturbative]] action functionals formulated (implicitly) in terms of [[super L-∞ algebra|super L-∞ algebraic data]] [[Lie integration|Lie integrates]] to a genuine ([[non-perturbative field theory|non-perturbative]]) [[schreiber:∞-Wess-Zumino-Witten theory|∞-WZW model]] in [[higher supergeometry]]. 

The present notes are aimed at spelling out class of examples of "super [[∞-gerbes]]", but for the most part they apply more generally and only take their motivation from this example.

$\,$

We start with traditional basics, first introducing [[superpoints]] and [[supermanifolds]], then recalling the [[spin group]] and the classification of its [[spin representations]], and then combining both to build $N$-[[supersymmetry|supersymmetric]] [[super Minkowski spacetimes]] as [[coset spaces]] of the [[super Poincaré group]] of $N$ [[supersymmetries]].

Then we introduce [[higher supergeometry]] in terms of [[super stacks]]/[[smooth super ∞-groupoids]] and finally discuss how all the exceptional [[L-∞ cocycles]] of [[super Minkowski spacetime]] and its higher [[L-∞ extensions]] yield the [[Green-Schwarz sigma models]] of the [[brane scan]] of [[string theory]]/[[M-theory]], and in fact the whole [[schreiber:The brane bouquet|brane bouquet]] of branes with "tensor multiplet" fields, such as the [[D-branes]] and notably the [[M5-brane]].

## **1)** Superpoints and supermanifolds

### Summary

Where ordinary [[differential geometry]] is modeled on the [[Cartesian spaces]] $\mathbb{R}^d$ with [[smooth functions]] between them,
[[supergeometry]] is modeled on the [[super Cartesian spaces]] that are denoted $\mathbb{R}^{p|q}$, for $p,q \in \mathbb{N}$, where the _[[superpoints]]_ $\mathbb{R}^{0|q}$ are characterized by the fact that their [[function algebra]] is a [[Grassmann algebra]] on $q$ [[generators]]. A _[[supermanifold]]_ of [[dimension]] $(p|q)$ is a [[space]] locally modeled on $\mathbb{R}^{p|q}$.

Introductions to traditional discussion of supermanifolds include 
([Varadarajan 04, chapter 4](#Varadarajan04), [Hohnhold-Stolz-Teichner 11](#HohnholdStolzTeichner11)). A more detailed discussion with an eye to serious applications to [[super Riemann surfaces]] and with an emphasis on [[integration over supermanifolds]] is in ([Witten 12](#Witten12)). See also at _[[signs in supergeometry]]_.

In some accounts of [[supergeometry]], going back to the influential textbook [DeWitt 92](#supermanifold#DeWitt), one fixes once and for all an infinite-dimensional [[Grassmann algebra]] to model the idea that one can arbitrarily probe any [[supermanifold]] by [[superpoints]]. 

That fixing such an algebra is unnatural, and that the natural formulation rather is to probe by _all_ finite-dimensional Grassmann algebras/superpoints in a way that is respects "change of odd coordinates" was realized in 1984 by [[Albert Schwarz]] and others, see ([Konechny-Schwarz 98, appendix](#KonechnySchwarz98)) for a review. In more abstract language this insight says that supergeometry happens in the [[topos]] over the [[site]] of [[superpoints]], see at _[[super infinity-groupoid|topos over superpoints]]_. Besides nicely clarifying what is really going on, this perspective immediately generalizes to yield the [[higher supergeometry]] that we come to [below](#HigherSupergeometry).

The [[topos theory|topos-theoretic]] perspective on supergeometry can be further enhanced by invoking the supergeometric analog of _[[synthetic differential geometry]]_. This [[synthetic differential supergeometry]] is developed in ([Carchedi-Roytenberg 12](#CarchediRoytenberg12)).


## **2)** Super Lie algebras and super Lie groups 
 {#SuperLieAlgebrasAndSuperLieGroups}

### Summary

By [[internalization]] all the standard notions of [[algebra]] and [[geometry]] are implemented in the super-context to yield [[superalgebra]] and [[supergeometry]]. Here we notably need some [[Lie theory]] in the super context.

By the above [[super infinity-groupoid|super-topos]]-perspective, one simply has that a _[[super Lie algebra]]_ $\mathfrak{g} \in SuperLieAlg$ is a collection $(\mathfrak{g}\otimes \Lambda^q)_{even} \in LieAlg$ of ordinary [[Lie algebras]], one for each finite dimensional [[Grassmann algebra]] $\Lambda^q$, together with compatible Lie algebra homomorphisms $(\mathfrak{g}\otimes \Lambda^{q_2})_{even} \longrightarrow (\mathfrak{g}\otimes \Lambda^{q_1})_{even}$ for each change of Grassmann coordinates $\Lambda^{q_2} \longrightarrow \Lambda^{q_1}$, hence a _[[presheaf]]_ of ordinary Lie algebras over the [[site]] of [[superpoints]]. Via the [[Yoneda lemma]] this is equivalently [[super vector space]] equipped with a [[Lie bracket]] which is _symmetric_ on two odd-graded elements and skew-symmetric otherwise, and which satisfies a [[Jacobi identity]] with signs depending suitably on the degree of the elements. 

In precisely the same fashion one finds all super-algebraic structures such as for instance also [[super L-∞ algebras]], which become important [below](#HigherSupergeometry) in the discussion of [[higher supergeometry]].
 
Similarly a _[[super Lie group]]_ $G$ is just a system $G(\mathbb{R}^{0|q})$ of ordinary Lie groups, equipped with compatible Lie group [[homomorphisms]] $G(\mathbb{R}^{0|q_2}) \longrightarrow G(\mathbb{R}^{0|q_1})$ for each algebra homomorphisms $\Lambda^{q_2} \longrightarrow \Lambda^{q_1}$, hence a [[presheaf]] of [[Lie groups]] on the [[site]] of [[superpoints]].

A decent exposition of this general principle of super Lie algebras and super Lie groups is for instance in ([Varadarajan 04, chapter 7.1](#Varadarajan04)). 
Discussion of the classical examples is in ([Varadarajan 04, chapter 7.3](#Varadarajan04)).

## **3)** Spin group and spin representations
 {#SpinGroupAndSpinRepresentations}

### History
[[Clifford algebra]]s, the [[spin group]] and its [[representation]]s made its first appearance in Physics in 1928 when Dirac tried to describe relativistic particles moving through [[Minkowski spacetime]]: Such a particle should be described by a [[wave function]] $\psi \colon \mathbb{R}^4 \to \mathbb{C}$ (we choose $x_0$ to be the time coordinate). The dynamics of the system obeys the [[Schrödinger equation]], which takes the form 
$$
	i\partial_0\psi	= H\,\psi
$$
where $H$ is the [[Hamilton operator]] measuring the energy. Now let $P_i$ be the $i$th momentum and let $m$ be the mass of the particle. Note that the above equation is of first order whereas the relativistic energy condition, $E^2 = \sum_{i=1}^3 P_i^2 + m^2$, turns out to be quadratic. Therefore, one way of obtaining a version of the above compatible with relativity is squaring the [[Schrödinger equation]], i.e.
$$
	(i\partial_0)^2\psi = H^2\,\psi = \left[ \sum_{j=1}^3 (-i\partial_j)^2 + m^2 \right]\,\psi
$$
The resulting [[Klein-Gordon equation]] describes the kinematics of spinless scalar particles. Dirac asked the question, whether it is possible to write down a relativistically covariant first order equation. The ansatz 
$$
	H = \sum_{j=1}^3 \alpha_j\,(-i\partial_j) + \alpha_0\,m
$$
yields the conditions $\alpha_j\alpha_k + \alpha_k\alpha_j = \delta_{jk}\,1$, which of course cannot be satisfied, if $\alpha_j$ are complex numbers. Dirac's conclusion was that the particle had some inner degree of freedom - the [[spin]] - which forces the wave functions $\psi$ to be vector-valued and transforming under a [[representation]] of the above algebra, which was already known as the [[Clifford algebra]].  

### Clifford algebras
Let $V$ be a finite dimensional vector space over a field $k$ of characteristic $0$ and denote by $Q$ a non-degenerate quadratic form on $V$, i.e. $Q(v) = \phi(v,v)$ for some non-degenerate symmetric bilinear form $\phi \colon V \otimes V \to k$. The pair $(V,Q)$ will be called a *quadratic vector space*.

+-- {: .un_defn}
###### Definition
The *Clifford algebra* $Cl(V,Q)$ associated to a quadratic vector space $(V,Q)$ is the quotient of the tensor algebra  $T(V) = \oplus_{r \geq 0} V^{\otimes r}$ of $V$ by the ideal $I$ generated by elements of the form $t_{x,y} = x \otimes y + y \otimes x - 2\phi(x,y)\cdot 1$. Equivalently $I$ is the ideal generated by elements $x \otimes x - Q(x) \cdot 1$. 
=-- 

The tensor algebra $T(V)$ is $\mathbb{Z}$-graded. Since $I$ is not homogeneous, this grading does not descend to the quotient. However, $Cl(V,Q)$ is still $\mathbb{Z}/2\mathbb{Z}$-graded and *filtered* by the length of tensors. This filtration leads to an important connection between the [[Clifford algebra]] associated to a quadratic vector space and its [[exterior algebra]]: The associated graded algebra of the former is isomorphic to the latter, i.e.
\[
	Cl(V,Q)^{gr} \cong \Lambda(V)
\] 
An isomorphism is induced by the linear map $\lambda \colon \Lambda(V) \to Cl(V)$ with $\lambda(v_1 \wedge \dots \wedge v_r) = \frac{1}{r!}\sum_{\sigma \in \Sigma_r} sign(\sigma)v_{\sigma(1)}\,\dots\,v_{\sigma(r)}$.

The following theorem is the key to all structural results about [[Clifford algebra]]s. Note that tensor products are taken in the category of *[[superalgebras]]*. 

+-- {: .num_theorem}
###### Theorem
Let $(V,Q)$ and $(V',Q')$ be two quadratic vector spaces. Then 
$$
\begin{aligned}
	Cl((V,Q) \oplus (V',Q')) & \cong Cl(V,Q) \otimes Cl(V',Q') \\
	Cl(V,-Q) & \cong Cl(V,Q)^{op}
\end{aligned}
$$
Moreover, we have $\dim(Cl(V,Q)) = 2^{\dim(V)}$.
=-- 

+-- {: .proof}
###### Proof
We drop the quadratic forms from the notation and just sketch the proof. The $k$-linear map $L \colon V \oplus V' \to Cl(V) \otimes Cl(V)$ satisfies $L(v,v')^2 = Q(v)\,1 + Q'(v')\,1$. Therefore it extends to an algebra homomorphism $Cl(V \oplus V') \to Cl(V) \otimes Cl(V')$. To construct the inverse note that the algebra inclusions $Cl(V) \to Cl(V \oplus V')$ and $Cl(V') \to Cl(V \oplus V')$ yield $Cl(V) \otimes Cl(V') \to Cl(V \oplus V')$, which is easily seen to be an algebra homomorphism inverse to the first one. By induction we obtain the formula for the dimension of $Cl(V,Q)$.

For the second statement consider the homomorphism $T(V) \to Cl(V,Q)^{op}$ sending $x_1 \otimes \dots \otimes x_k$ to $[x_k \otimes \dots \otimes x_1]$. Due to the definition of the opposite of a [[superalgebra]], it sends $x \otimes x + Q(x)\,1$ to $0$ and the kernel is generated by these elements. Therefore it descends to a surjective map $Cl(V,-Q) \to Cl(V,Q)$. Since both sides have the same dimension, it is an isomorphism.
=--

From this we can completely classify all complex Clifford algebras, i.e. $Cl(V,Q)$ for a complex vector space $V$. Note that in this case there is up to similarity just one quadratic form $Q(z) = \sum_{j=1}^n z_i^2$. We denote $Cl(V,Q)$ by $\mathbb{C}l(V)$ in this case. 

+-- {: .num_theorem}
###### Theorem
If $V$ is a complex vector space with $\dim(V) = 2m$, then $\mathbb{C}l(V) \cong End(S)$ for $\dim(S) = 2^{m-1}|2^{m-1}$ as graded algebras. 

If $V$ is a complex vector space with $\dim(V) = 2m+1$, then $\mathbb{C}l(V) \cong \mathbb{C}l(V)^+ \otimes D$, where $D = \mathbb{C}[\epsilon] \cong \mathbb{C}l(\mathbb{C}^1)$ with $\epsilon^2 = 1$. Moreover, $\mathbb{C}l(V)^+ \cong End(S_0)$ where $\dim(S_0) = 2^m$.
=-- 

+-- {: .proof}
###### Proof
We can check directly that $\mathbb{C}l(\mathbb{C}^2) \cong M_2(\mathbb{C})$: Let $e_1, e_2$ be two orthogonal basis vectors of $\mathbb{C}^2$. The map $e_1 \mapsto \begin{pmatrix}0 & 1 \\ 1 & 0 \end{pmatrix}$, $e_2 \mapsto \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}$ defines an isomorphism of [[superalgebras]]. By induction we then have $\mathbb{C}l(\mathbb{C}^{2m}) \cong \mathbb{C}l(\mathbb{C}^{2m-2}) \otimes \mathbb{C}l(\mathbb{C}^{2})$. The odd dimensional case is similar.
=--

From the above theorem we deduce that $\mathbb{C}l(V)$ has exactly two (graded) simple modules $S$ and $\Pi S$ ($S$ with the reversed grading) in the even-dimensional case and exactly one graded simple module $S = S_0 \otimes D$ in case the dimension is odd. 

The classification of Clifford algebras is a little more intricate in the case of real vector spaces. Here we can without loss of generality assume that $V$ is the [[super vector space]] $\mathbb{R}^{s|t}$. The structure of the real Clifford algebras is dictated by the super Brauer group.

+-- {: .un_defn}
###### Definition
A [[superalgebra]] is called a *super division algebra* if all nonzero homogeneous elements are invertible. A real [[superalgebra]] $A$ is called *central simple* if $A \otimes_{\mathbb{R}} \mathbb{C} \cong M_{s|t}(\mathbb{C})$ or $A \otimes_{\mathbb{R}} \mathbb{C} \cong M_n(\mathbb{C}) \otimes_{\mathbb{C}} D$ (with $D$ as above) as superalgebras. We will write *CS superalgebra* for short. 
=-- 

There are a lot of different characterizations of CS [[superalgebras]], see [Varadarajan 04, Theorem 6.2.5](#Varadarajan04). For example, each CS [[superalgebra]] over a field $k$ of characteristic $0$ is isomorphic to $M_{s|t}(k) \otimes K$ for some super division algebra $K$ over $k$ such that its supercenter is $k$. 

+-- {: .un_defn}
###### Definition
Two CS [[superalgebras]] $A_1$ and $A_2$ are called *similar* if their associated super division algebras are isomorphic, i.e. if $A_i \cong M_{s_i|t_i}(k) \otimes K$ for some super division algebra $K$ over $k$. The monoid of similarity classes of CS [[superalgebras]] *$sBr(k)$* with respect to the graded tensor product $\otimes_k$ turns out to be a group and is called the *super Brauer group* of $k$.
=-- 

The following is proven in [Varadarajan 04, Theorem 6.4.1](#Varadarajan04).
+-- {: .num_theorem}
###### Theorem
The super Brauer group $sBr(\mathbb{R})$ is isomorphic to $\mathbb{Z}/8\mathbb{Z}$. Let $D_{\mathbb{R}}=\mathbb{R}[\epsilon]$ be the [[superalgebra]] with $\epsilon$ odd and $\epsilon^2 = 1$. If $(V,Q)$ is a quadratic vector space, then $[Cl(V,Q)] = [D_{\mathbb{R}}]^{sign(Q)}$. 
=-- 

This result explains the $8$-fold periodicity found in real Clifford algebras as can be seen from the following table in which $V= \mathbb{R}^{s|t}$ with dimension $d = s+t$:

| $(t-s)$ mod $8$ | $Cl(s,t)$ | $N$ |
|--|--|--|
|$0,6$|$M_N(\mathbb{R})$|$2^{d/2}$|
|$2,4$|$M_N(\mathbb{H})$|$2^{(d-2)/2}$|
|$1,5$|$M_N(\mathbb{C})$|$2^{(d-1)/2}$|
|$3$|$M_N(\mathbb{H}) \oplus M_N(\mathbb{H})$|$2^{(d-3)/2}$|
|$7$|$M_N(\mathbb{R}) \oplus M_N(\mathbb{R})$|$2^{(d-1)/2}$|

### Spin group, spin representations and invariant forms
With this background about Clifford algebras at hand, we can finally define the [[spin group]]:
+-- {: .un_defn}
###### Definition
Let $(V,Q)$ be a quadratic vector space. The *[[spin group]]* $Spin(V,Q)$ is defined as
\[
	Spin(V,Q) = \left\{ v_1\,\dots\,v_{2k} | Q(v_i) = \pm 1 \forall i \right\} \subset Cl(V,Q)^+
\]
The irreducible [[representations]] of $Spin(V,Q)$ that arise from simple $Cl(V,Q)^+$-modules are called *[[spin representations]]*.
=-- 

Note that this definition of the [[spin group]] differs from the one given in [Varadarajan 04, Proposition 5.4.8](#Varadarajan04), but agrees with the one from [Lawson-Michelsohn 89, page 18](#LawsonMichelsohn89). More precisely, the former is the connected component of the identity of the latter, i.e. for $V = \mathbb{R}^{p|q}$ we have
\[
	Spin(p,q)^0 = \left\{ v_1\,\dots\,v_{2k}w_1\,\dots\,w_{2l} | Q(v_i) = 1, Q(w_j) = -1 \forall i,j \right\}
\]
$Spin(p,q)$ is a double cover of $SO(p,q)$ in the sense that
\[
	0 \to \mathbb{Z}/2\mathbb{Z} \to Spin(p,q) \to SO(p,q) \to 1
\]
is exact ([Lawson-Michelsohn 89, Theorem 2.10](#LawsonMichelsohn89)). If $\min(p,q) = 1$ and $\max(p,q) \geq 3$, then $SO(p,q)$ and $Spin(p,q)$ have two connected components and the above restricts to a double cover of $SO(p,q)^0$ by $Spin(p,q)^0$. Hidden in the above definition is the statement that simple $Cl(V,Q)^+$-modules yield *irreducible* [[representations]] when restricted to the group $Spin(V,Q)$.

We have $Cl(r,s)^+ \cong Cl(r,s-1)$ as ungraded algebras. Therefore we can read off the spin representations from the above classification table. Consider for example the group $Spin(3,1) \subset Cl(3,1)^+ \cong Cl(3,0) \cong M_2(\mathbb{C})$. This has *two* simple modules as a real algebra, $\mathbb{C}^2$ and its conjugate. 

#### Invariant forms and Super Lie Algebras
The symmetries of $d$-dimensional [[Minkowski space]] $\mathbb{R}^{d-1|1}$ are given by the [[Poincaré group]], which has the [[Lie algebra]]
\[
	\mathfrak{g}_0 = \mathbb{R}^{d-1|d} \ltimes \mathfrak{so}(d-1,1)
\]
To get the [[super Poincaré Lie algebra]] from this, we would like to extend it by an odd part $\mathfrak{g}_1$ given by a spin representation $S$. In general, a [[super Lie algebra]] can be obtained from the following data:

* an ordinary [[Lie algebra]] $(\mathfrak{g}_0, [\,\cdot\,, \,\cdot\,])$, 
* a $\mathfrak{g}_0$-module $\mathfrak{g}_1$,
* a symmetric $\mathfrak{g}_0$-module map $\kappa \colon \mathfrak{g}_1 \otimes \mathfrak{g}_1 \to \mathfrak{g}_0$ such that $a \cdot \kappa(a,a) = 0$ for all $a \in \mathfrak{g}_1$, where the dot denotes the action of $\mathfrak{g}_0$ on $\mathfrak{g}_1$. 

We know what $\mathfrak{g}_0$ and $\mathfrak{g}_1$ should be in our case. Note that $\mathfrak{so}(d-1,1) = \mathfrak{spin}(d-1,1)$, therefore $\mathfrak{g}_0$ acts on $S$ (where the translations act trivially). Therefore we need to concentrate on invariant symmetric forms $\kappa$. 

One way to easily satisfy the last condition for $\kappa$ is to just look at those symmetric forms that take values in the translation part of $\mathfrak{g}_0$, i.e. the underlying vector space $\mathbb{R}^{d-1|1}$. More generally, we will summarize below the results about the existence of symmetric bilinear forms $S \otimes S \to \Lambda V$ for a quadratic vector space $(V,Q)$ and an irreducible [[spin representation]] $S$ of $Spin(V,Q)$. 

We will again spell out the case of complex vector spaces in more detail and just state the results in the real case. Since we would like to use duality results to classify invariant vector-valued forms, we first need to think about scalar-valued ones. Surprisingly enough, their existence in the *complex* case shows an $8$-fold periodicity, depending on the dimension $d$ of the underlying *complex vector space* $V$:

| $d$ mod $8$ | type of invariant scalar form |
|--|--|
|$0$| symmetric forms on $S^{+}$ and on $S^{-}$ |
|$1,7$| symmetric form on $S$ |
|$2,6$| $S^+$ dual to $S^-$ |
|$3,5$| skew-symmetric form on $S$ |
|$4$| skew-symmetric form on $S^{+}$ and on $S^{-}$ |

This can be found in [Varadarajan 04, Table 6.4](#Varadarajan04). 

+-- {: .num_theorem}
###### Theorem
Let $V$ be a complex vector space. If $d = \dim(V)$ is even, then $\mathbb{C}l(V) \cong End(S)$ with $S = S^+ \oplus S^-$ for irreducible spin representations $S^{\pm}$. Let $0 \leq r \leq \frac{d}{2}-1$. Then
\[
	\dim(Hom_{Spin(V)}(S \otimes S, \Lambda^r(V))) = 2.
\]

If $d$ is odd, then $\mathbb{C}l(V)^+ \cong End(S_0)$ for an irreducible spin representation $S_0$ and
\[
	\dim(Hom_{Spin(V)}(S_0 \otimes S_0, \Lambda^r(V))) = 1.	
\]
=-- 

+-- {: .proof}
###### Proof
We just prove the even case: By the above table we have $S^* \cong S$ via an equivariant isomorphism. Therefore $S \otimes S \cong S^* \otimes S \cong End(S) \cong \mathbb{C}l(V) \cong \Lambda(V)$ as $Spin(V)$-modules. Now we have
\[
	Hom_{Spin(V)}(S \otimes S, \Lambda^r(V)) \cong Hom_{Spin(V)}(\Lambda(V), \Lambda^r(V))
\]
and $\Lambda^r(V)$ is irreducible as $SO(V)$-module. Moreover, observe that $\Lambda^r(V) \cong \Lambda^{d-r}(V)$. The proof for the odd dimensional case is similar.
=--

The basis in both cases is obtained from $\kappa$ defined via duality by $(\kappa(x \otimes y), v)_{\Lambda^r(V)} = (\lambda(v)x, y)_S$, where the brackets denote the invariant scalar forms on $\Lambda^r(V)$ and $S$ respectively. We can read off the parity and the symmetry of $\kappa$ from this definition and we have to restrict to $S^+ \otimes S^+$, $S^- \otimes S^-$ or $S^+ \otimes S^-$ depending on the dimension and on $r$. 

This time the results are much more complex in the real case. Aside from the fact that the dimension of $V$, the signature of $Q$ and the parity of $r$ enter, the invariant forms need not be projectively unique anymore. The case most important for us, however, is that of Minkowski signature. And here - quite magically - all the ambiguities disappear and we have ([Varadarajan 04, Theorem 6.7.1](#Varadarajan04)):

+-- {: .num_theorem}
###### Theorem
Let $V$ be a real quadratic vector space of dimension $d$ and with Minkowski signature, let $S$ be a real irreducible spin representation, then there is a projectively unique nontrivial invariant symmetric form 
\[
	\kappa \colon S \otimes S \to V.
\]  
=-- 

### Summary

A class of examples of [[super Lie algebras]] of particular interest in applications to [[physics]] in general and [[quantum field theory]] in particular are super-[[Lie algebra extensions]] of the Lie algebra of infinitesimal [[isometries]] of [[Minkowski spacetime]]: the "[[supersymmetry]]" [[super Lie algebras]] that appear as [[local symmetries]] in [[supergravity]] and [[superstring theory]] and, more speculatively, as [[global symmetries]] in the [[MSSM]].

These we turn to [below](#SuperMinkowskiSpacetime), where we see that these [[supersymmetry]] [[super Lie algebras]] crucially contain [[spin representations]] and crucially depend on the subtleties of the [[representation theory]] of the [[spin group]]. Therefore here we first recall the classification and properties of _[[spin representations]]_ in general.

A standard mathematical textbook account for this is ([Lawson-Michelsohn 89, I.2, I.3, I.5](#LawsonMichelsohn89)), but for actual computations and notably for comparison with the bulk of the literature, it is useful to also make explicit the standard [[bases]] and [[matrix]] representations, as summarized neatly for instance in ([Polchinski 01, volume II, appendix B](#Polchinski01)). Decent accounts that are both mathematically satisfactory as well as geared towards the applications to [[supersymmetry]] in [[physics]] are ([Varadarajan 04, chapters 5 and 6](#Varadarajan04)) and ([Freed 99, lecture 3](#Freed99)).

The main point of interest here is that a [[supersymmetry]] [[super Lie algebra]] for $d$-dimensional [[Minkowski space]] requires precisely a [[spin representation]] $S$ which is equipped with a linear map

$$
  \Gamma \;\colon\; S \otimes S \longrightarrow \mathbb{R}^{d-1,1}
$$

which is 

1. symmetric;

1. $Spin(d-1,1)$-equivariant.

(Precisely these two properties will make $\Gamma$ the odd/odd component of a [[super Lie algebra|super]] [[Lie bracket]]).

In ([Varadarajan 04, section 6.6](#Varadarajan04)) these bilinear pairings are classified in full generality, for arbitrary [[spacetime]] [[signature of a quadratic form|signature]]. However it turns out that for [[Minkowski spacetime|Minkowski]] [[signature of a quadratic form|signature]] all _real_ spinor representations ("[[Majorana representations]]") carry an essentially unique such pairing and at the same time are the representations relevant in most applications. Therefore we concentrate [below](#ClassificationAndPropertiesOfMajoranaRepresentations) on the classification and properties of [[Majorana representations]] of the Lorentzian [[spin groups]] $Spin(d-1,1)$.

### Classification and properties of Majorana representations

 {#ClassificationAndPropertiesOfMajoranaRepresentations}

The following table lists the irreducible real representations of $Spin(V)$ ([Freed 99, page 48](#Freed99)).

| $d$ | $Spin(d-1,1)$ | minimal real spin representation $S$ | $dim_{\mathbb{R}} S\;\;$ |  $V$ in terms of $S^\ast$ |  [[supergravity]] | 
|--|--|--|--|--|--|
| 1 | $\mathbb{Z}_2$ | $S$ real | 1 | $V \simeq (S^\ast)^{\otimes}^2$ |  |
| 2 | $\mathbb{R}^{\gt 0} \times \mathbb{Z}_2$ | $S^+, S^-$ real | 1 | $V \simeq ({S^+}^\ast)^{\otimes^2} \oplus ({S^-}^\ast)^{\otimes 2}$ |  |
| 3 | $SL(2,\mathbb{R})$ | $S$ real | 2 |  $V \simeq Sym^2 S^\ast$ |  |
| 4 | $SL(2,\mathbb{C})$ | $S_{\mathbb{C}} \simeq S' \oplus S''$ | 4 | $V_{\mathbb{C}} \simeq {S'}^\ast \oplus {S''}^\ast$ |  |
| 5 | $Sp(1,1)$ | $S_{\mathbb{C}} \simeq S_0 \otimes_{\mathbb{C}} W$ | 8 |  $\wedge^2 S_0^\ast \simeq \mathbb{C} \oplus V_{\mathbb{C}}$ |  |
| 6 | $SL(2,\mathbb{H})$ | $S^\pm_{\mathbb{C}} \simeq S_0^\pm  \otimes_{\mathbb{C}} W$ | 8 | $V_{\mathbb{C}} \simeq \wedge^2 {S_0^+}^\ast \simeq (\wedge^2 {S_0^-}^\ast)^\ast$ |  |
| 7 |  |  $S_{\mathbb{C}} \simeq S_0 \otimes_{\mathbb{C}} W$ | 16 |  $\wedge^2 S_0^\ast \simeq V_{\mathbb{C}} \oplus \wedge^2 V_{\mathbb{C}}$ |  |
| 8 |  | $S_{\mathbb{C}} \simeq S' \oplus S^{\prime\prime}$ | 16 | ${S'}^\ast {S''}^\ast \simeq V_{\mathbb{C}} \oplus \wedge^3 V_{\mathbb{C}}$ |  |
| 9 |  | $S$ real | 16 |  $Sym^2 S^\ast \simeq \mathbb{R} \oplus V \wedge^4 V$ |  |
| 10 |   | $S^+ , S^-$ real | 16 | $Sym^2(S^\pm)^\ast \simeq V  \oplus \wedge_\pm^5 V$ | [[type II supergravity]] |
| 11 |   | $S$ real | 32 | $Sym^2 S^\ast \simeq V \oplus \wedge^2 V \oplus \wedge^5 V$ | [[11-dimensional supergravity]] |

Here $W$ is the 2-dimensional [[complex vector space]] on which the [[quaternions]] naturally act. 

+-- {: .num_remark}
###### Remark

The last column implies that in each dimension there exists a [[linear map]]

$$
  \Gamma \;\colon\; S^\ast \otimes S^\ast \longrightarrow \mathbb{R}^{d-1,1}
$$

which is 

1. symmetric;

1. $Spin(V)$-equivariant.

This allows to form the [[super Poincaré Lie algebra]] in each of these cases. See there and see _[Spinor bilinear forms](#SpinorBilinearForms)_ below for more.

=--


## **4)** Super Poincar&#233; group and super Minkowski spacetime
 {#SuperMinkowskiSpacetime}


### Summary

Ordinary [[Minkowski space]] $\mathbb{R}^{d-1,1}$ happens to be [[coset space]] which is the quotient of (the double cover of) its own Lie group of oriented [[isometries]], the [[Poincaré group]] $Iso(d-1,1)$ by (the [[spin group|spin]] [[double cover]] of) the [[Lorentz group]] $SO(d-1,1)$ of rotations and boosts:

$$
  \mathbb{R}^{d-1,1} \simeq Iso(d-1,1)/SO(d-1,1)
  \,.
$$

The same is true already for the corresponding [[Lie algebras]]:

$$
  \mathbb{R}^{d-1,1} \simeq \mathfrak{iso}(d-1,1)/\mathfrak{so}(d-1,1)
  \,.
$$

While for ordinary [[differential geometry]] this identification is maybe not very deep, for [[supergeometry]] it becomes crucial:


for a [[super Lie algebra]] [[Lie algebra extension|extension]] $\mathfrak{siso}_N(d-1,1)$ of the [[Poincaré Lie algebra]] by a [[spin representation]] in odd degree -- a [[super Poincaré Lie algebra]] -- one _defines_ the corresponding [[super Minkowski spacetime]] as the quotient

$$
  \mathbb{R}^{d;N} \coloneqq \mathfrak{siso}_N(d-1,1)/\mathfrak{so}(d-1,1)
  \,.
$$

Good mathematical discussion of this construction is in  ([Deligne-Freed 99, section 1.1](#DeligneFreed99), [Freed 99, lecture 3](#Freed99), [Varadarajan 04, chapter 7](#Varadarajan04)). A decent summary of the standard component expressions of this construction as used in [[physics]] is in ([Polchinski 01, volume II, appendix B](#Polchinski01)).



Since the [[special orthogonal Lie algebra]] $\mathfrak{so}(d-1,1)$ is [[normal sub Lie algebra|normal]] in $\mathfrak{iso}(d-1,1)$, this exhibits [[super Minkowski spacetime]] itself as a [[super Lie algebra]], namely the [[super translation Lie algebra]] over itself. 
Accordingly one can ask for the [[Lie algebra cohomology]] of [[super Minkowski spacetime]]. And while that of ordinary Minkowski spacetime, regarded as the abelian [[translation Lie algebra]], is uninteresting, super-Minkowski spacetimes -- which are mildly non-abelian!, the nontrivial bracket being just the pairing $\Gamma$ from above -- happen to admit a finite number of exceptional [[super Lie algebra|super]] [[Lie algebra cohomology|Lie cocycles]]. For reasons that will become clear below, the classification of these is known as the _[[brane scan]]_. A decent discussion of this is in ([Azc&#225;rraga-Izqierdo 95](#AzcarragaIzqierdo95), [Chrysso&#8204;malakos-Azc&#225;rraga-Izquierdo-Bueno 99](#CAIP99)). This analysis of the [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]] super-dg-algebra of the [[super Poincaré Lie algebra]] goes back to ([Nieuwenhuizen 83](#Nieuwenhuizen83)).

Since by above, [[super Minkowski spacetime]] is defined as a [[coset space]] in [[supergeometry]], the [[mechanics]] of [[particles]] and more generally [[branes]] propagating in super Minkowski spacetimes are naturally given by super-[[coset models]]. On the Lie-algebraic level this is discussed nicely in [Azcarraga-Izqierdo 95, section 8](#AzcarragaIzqierdo95). On the other hand, this means that the geometry of _curved_ [[super spacetime]] is most naturally thought of in terms of super-[[Cartan geometry]]. This is (somewhat implicitly) the approach to [[supergravity]] in ([Castellani-D'Auria-Fr&#233;](#CastellaniDAuriaFre91)).


## **5)** Higher supergeometry
 {#HigherSupergeometry}

### Summary

In order to pass from [[supergeometry]] to [[higher supergeometry]], we proceed by the canonical route.

Above we already mentioned that ordinary [[supergeometry]] takes place in the [[topos]] $Sh(SuperPoints)$ of "super sets". In order to model [[super ∞-groupoids]] we hence naturally pass to the [[(∞,1)-topos]] over the [[site]] of [[superpoints]]. In order to equip these with [[smooth structure]] such as to yield [[smooth super ∞-groupoids]] we form the [[(∞,1)-sheaf (∞,1)-topos]]

[[SmoothSuper∞Grpd]] $\coloneqq Sh_\infty\left(\left\{\mathbb{R}^{p|q}\right\}_{p,q \in \mathbb{N}}\right) \simeq Sh_\infty\left(SuperManifolds\right)$

over [[supermanifolds]] (see for instance [FSS 13a](#FSS13a)). 


As in any [[(∞,1)-topos]], there is a canonical notion of [[principal ∞-bundles]], of [[associated ∞-bundles]] and of [[∞-gerbes]] in [[SmoothSuper∞Grpd]] ([NSS 12](#NSS12)).
The basic fact of relevance here is that [[SmoothSuper∞Grpd]] is  _[[cohesive (∞,1)-topos|cohesive]]_ ([S](#S)) and hence also admits refinements of these structures to [[differential cohomology]]. 

In particular, due to [[cohesion]] every [[super ∞-group]] $G \in Grp(SmoothSuper\infty Grpd)$ naturally has a canonical higher [[Maurer-Cartan form]] exhibited by a [[cocycle]]

$$
  \theta_G \;\colon\; G \longrightarrow \flat_{dR}\mathbf{B}G
$$

with [[coefficients]] in non-abelian de Rham hypercohomology. Since the ordinary [[WZW gerbe]] is characterized by a 3-cocycle $\mu$ in [[Lie algebra cohomology]] such that $\mu(\theta_Q) \colon G \to \Omega^3_{cl}$ is its [[curvature]] 3-form, this is a crucial ingredient for the definition of [[schreiber:∞-Wess-Zumino-Witten theory]] models. This we come to [below](#SuperWZWBundles).




## **6)** Super Wess-Zumino-Witten gerbes / $n$-connections
 {#SuperWZWBundles}


We discuss how to construct [[circle n-bundles with connection]] ("bundle (n-1)-gerbes") on [[super Lie groups]] and on [[smooth super ∞-groupoid|super ∞-groups]] which generalize the familiar [[WZW model|Wess-Zumino-Witten term]] that serves as the [[action functional]] for the [[sigma-model]] that describes a [[string]]  propagating on a [[Lie group]]. Following the "[[holographic principle]]" we construct these [[schreiber:∞-Wess-Zumino-Witten theory|∞-Wess-Zumino-Witten theories]] as [[boundary field theories]] for [[schreiber:∞-Chern-Simons theories]] (which in turn are realized as [[boundary field theories]] for higher [[topological Yang-Mills theories]]).

Finally we apply this general construction of supergeometric [[schreiber:∞-Wess-Zumino-Witten theory|∞-Wess-Zumino-Witten theories]] to the exceptional [[super L-∞ algebra]] [[extended supersymmetry]] algebras and thus find the [[non-perturbative field theory|non-pertrubative]] formulation of the $p$-[[brane]] [[sigma-models]] in [[string theory]]/[[M-theory]] which constitute the [[brane scan]]/[[schreiber:The brane bouquet]].


### Introduction

A [[classical field theory]]/[[prequantum field theory]]
is traditionally defined by an [[action functional]]: given a [[smooth space]] $\mathbf{Fields}_{traj}$ "of [[trajectories]]" of a given [[physical system]], then the [[action functional]] is a [[smooth function]]

$$
  \array{
    \mathbf{Fields}_{traj}
    \\
    \downarrow^{\mathrlap{\exp(i S)}}
    \\
    U(1)
  }
$$

to the [[circle group]]. The idea of producing a [[quantum field theory]] from this is to 

1. choose a linearization in the form of the group [[homomorphism]] 
$U(1) \longrightarrow GL_1(\mathbb{C})$ to the [[group of units]] of the complex numbers, 

1. choose a [[measure]] $d\mu$ on $\mathbf{Fields}_{traj}$ 

and then declare that the [[integral]] ("[[path integral]]")

$$
  \underset{\phi \in \mathbf{Fields}_{traj}}{\int} \exp(i S(\phi))\, d\mu \in \mathbb{C}
$$ 

is the [[partition function]] of the theory a kind of [[expectation value]] with [[probabilities]] replaced by [[probability amplitudes]].

In order to make sense of this (for a full discussion of "[[motivic quantization]]" in this sense see ([Nuiten 13](#Nuiten13)), here we concentrate on the [[prequantum field theory|pre-quantum aspects]]), it is useful to allow some more conceptual wiggling room by passing to [[higher differential geometry]]. Notice that if we write $\mathbf{B}U(1)$ for the [[smooth groupoid|smooth]] universal [[moduli stack]] of [[circle group]]-[[principal bundles]], then an [[action functional]] as above is equivalently a [[homotopy]] of the form

$$
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{0}}
    \\
    && \mathbf{B}U(1)
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow &\downarrow^{\mathrlap{\exp(i S)}}& \searrow
    \\
    \ast &\leftarrow& U(1) &\rightarrow& \ast
    \\
    & {}_{\mathllap{0}}\searrow &{}^{(pb)}& \swarrow_{\mathrlap{0}}
    \\
    && \mathbf{B}U(1)
  }
  \,,
$$

where on the right we used the [[universal property]] of the [[homotopy pullback]] [[diagram]] which exhibits the smooth [[circle group]] $U(1)$ as the [[loop space object]] of $\mathbf{B}U(1)$.

For instance for $X$ a [[smooth manifold]] ("[[spacetime]]") and $\nabla \;\colon\; X \longrightarrow \mathbf{B}U(1)_{conn}$ a [[circle group]]-[[principal connection]] ("[[electromagnetic field]] on [[spacetime]]") then for [[trajectories]] in $X$ of shape the [[circle]], the canonical [[action functional]] ("[[Lorentz force]] gauge [[interaction]]") is the [[holonomy]] [[nonlinear functional|functional]]

$$
  \exp(i S_{Lor})
  \coloneqq
  \exp(i \int_{S^1} [S^1, \nabla])
  \;\colon\;
  [S^1, X]
  \stackrel{[S^1, X]}{\longrightarrow}
  [S^1, \mathbf{B}U(1)_{conn}]
  \stackrel{\exp(i \int_{S^1}(-))}{\longrightarrow}
  U(1)
  \,.
$$

But more generally, if the [[trajectories]] have a [[boundary]], hence if they are of the shape of an [[interval]] $I \coloneqq [0,1]$, then the [[holonomy]] functional on [[smooth loop space]] $[S^1, X]$ generalizes to the [[parallel transport]] on the [[path space]] $[I,X]$ and there it is no longer a function, but exists only as a [[homotopy]] of the form

$$
  \array{
    && [I,X]
    \\
    & {}^{(-)|_0}\swarrow && \searrow^{\mathrlap{(-)|_1}}
    \\
    X && \swArrow_{\exp(i \int_{I}[I,\nabla])} && X
    \\
    & {}_{\mathllap{\chi_\nabla}}\searrow && \swarrow_{\mathrlap{\chi_\nabla}}
    \\
    && \mathbf{B}U(1)
  }
  \,.
$$
 
Notice that this is a "local" description of the action functional: the data that determines it is the boundary

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{\nabla}}
    \\
    \mathbf{B}U(1)_{conn}
  }
$$

and from this the rest is induced by [[transgression]]. 

A related class of examples are [[prequantized Lagrangian correspondences]]: Let 

$$
  \array{
     X
     \\
     \downarrow^{\mathrlap{\omega}}
     \\
     \mathbf{\Omega}^2
  }
$$

be a [[symplectic manifold]]. Then a [[symplectomorphism]] $f \;\colon\; X \longrightarrow X$ is a [[correspondence]] of the form

$$
  \array{
    && graph(f)
    \\
    & \swarrow && \searrow
    \\
    X && && X
    \\
    & {}_{\mathllap{\omega}}\searrow && \swarrow_{\mathrlap{\omega}}
    \\
    && \mathbf{\Omega}^2
  }
  \,.
$$

A [[prequantization]] of $(X,\omega)$ is a lift $\nabla$ in

$$
  \array{
    X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}U(1)_{conn}
    \\
    & \searrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    && \mathbf{\Omega}^2
  }
$$

and so a [[prequantized Lagrangian correspondence]] is

$$
  \array{
    && graph(f)
    \\
    & \swarrow && \searrow
    \\
    X && \swArrow && X
    \\
    & _{\mathllap{\nabla}}\searrow && \swarrow_{\mathrlap{\nabla}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \,.
$$

To conceptualize all this, write

$$
  \mathbf{H} \coloneqq SmoothGrpd \coloneqq
  Func(SmoothMfd^{op}, Grpd)[\{stalkwise\;equivalences\}^{-1}]
$$

for the [[homotopy theory]] obtained from the [[category]] of [[groupoid]]-valued [[presheaves]] on the [[category]] of all [[smooth manifolds]] by universally turning [[stalk|stalkwise]] [[equivalences of groupoids]] into genuine [[homotopy equivalences]] ("[[simplicial localization]]").

This is the [[(2,1)-topos]] of [[smooth groupoids]]/smooth ([[moduli stacks|moduli]]) [[stacks]].

Write 

$$
  Corr_1(\mathbf{H})
  \in 
  (2,1)Cat
$$ 

for the [[(2,1)-category]] of [[correspondences]] in $\mathbf{H}$. Write $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$ for the [[slice (infinity,1)-topos|slice]] [[(2,1)-topos]] over the smooth [[moduli stack]] of [[circle n-bundles with connection|circle bundles with connection]]. Then the abovve diagrams are morphisms in $Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}})$.

+-- {: .num_prop}
###### Proposition 

The [[automorphism group]] of $\nabla \in Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}})$ is the [[quantomorphism group]] of $(X,\omega)$, hence the [[smooth group]] which is the [[Lie integration]] of the [[Poisson bracket]] [[Lie algebra]] of $(X,\omega)$.

A [[concrete object|concrete]] smooth 1-parameter subgroup

$$
  \mathbf{B}\mathbb{R} \longrightarrow
  \mathbf{B}\mathbf{Aut}_{/\mathbf{B}U(1)_{conn}}(\nabla)
  \hookrightarrow
  \mathbf{H}_{/\mathbf{B}U(1)_{conn}}
$$

is equivalently a choice $H \in C^\infty(X)$ of a smooth function and sends

$$
  t
  \;\;
   \mapsto
  \;\;
  \left(
  \array{
    X &&\stackrel{\exp(t \{H,-\})}{\longrightarrow}&& X
    \\
    & {}_{\mathllap{\nabla}}\searrow &\swArrow_{\mathrlap{\exp(i S_t)}}& \swarrow_{\mathrlap{\nabla}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \right)
  \,,
$$

where

1. $\exp(t \{H,-\})$ is the [[Hamiltonian flow]] induced by $H$;

1. $S_t = \int_0^t L$ is the [[Hamilton-Jacobi theory|Hamilton-Jacobi]] [[action functional]], the [[integral]] of the [[Lagrangian]] of $H$, hence of its [[Legendre transform]].  

=--


(see [Schreiber 13](#SchreiberClassical)).

It is now clear how to pass from this to [[local prequantum field theory]] of higher dimension.

Let now more generally



$$
  \mathbf{H} \coloneqq 
  Smooth\infty Grpd
  \coloneqq
  Func(SuperMfd^{op}, KanCplx)[\{stalkwise\;homotopy\;equivalences\}^{-1}]
$$

be the [[homotopy theory]] obtained from the [[category]] of [[Kan complex]]-valued [[presheaves]] on the category of all [[supermanifolds]] by universally turning [[stalk|stalkwise]] [[homotopy equivalences]] into actual [[homotopy equivalences]].

We say that this is the [[(∞,1)-topos]] of _[[smooth super ∞-groupoids]]_/_[[supergeometry|supergeometric]] [[moduli ∞-stacks]]_.

Let 

$$
  Corr_n(\mathbf{H}) \in (\infty,n)Cat
$$

be the [[(∞,n)-category]] of $n$-fold [[correspondences]] in $\mathbf{H}$. This is a [[symmetric monoidal (∞,n)-category]] under the objectwise [[Cartesian product]] in $\mathbf{H}$.



[[Smooth∞Grpd]] has the special property that it is [[cohesive (∞,1)-topos|cohesive]] in that it is equipped with an [[adjoint quadruple]] of [[adjoint (∞,1)-functors]]

$$
  \mathbf{H}
  \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  \infty Grpd
$$

which induce an [[adjoint triple]] of [[idempotent monad|idempotent]] [[(∞,1)-monads]]/comonads


$$
  \left(
    \Pi \dashv \flat \dashv \sharp
  \right)
  \;\colon\;
  \mathbf{H} 
  \longrightarrow
  \mathbf{H}
$$

with $\Pi$ [[Cartesian product|product]]-preserving, called

* _[[shape modality]]_ $\dashv$ _[[flat modality]]_ $\dashv$ _[[sharp modality]]_ .

Here the [[shape modality]] $\Pi$ sends a [[simplicial manifold]] to the [[homotopy type]] of the [[geometric realization of simplicial topological spaces|fat geometric realization]] of the underlying [[simplicial topological space]], hence in particular sends a [[smooth manifold]] to its [[homotopy type]].
 
Write $Bord_n$ for the [[(∞,n)-category of cobordisms|(∞,n)-category of framed n-dimensional cobordisms]].

+-- {: .num_prop}
###### Proposition 

A [[monoidal (∞,n)-functor]] 

$$
  \mathbf{Fields}
  \;\colon\;
  Bord_n
  \longrightarrow
  Corr_n(\mathbf{H})
$$

is equivalently a choice of object $\mathbf{Fields} \in \mathbf{H}$. It sends a [[cobordism]] $\Sigma$ to the [[internal hom]] of its [[shape]] into the [[higher moduli stack]] $\mathbf{Fields}$:


$$
  \left(
    \array{
      && \Sigma
      \\
      & \nearrow && \nwarrow
      \\
      \Sigma_{in}
      && &&
      \Sigma_{out}
    }
  \right)
  \;\;
   \mapsto
  \;\;
  \left(
    \array{
       && [\Pi\Sigma, \mathbf{Fields}]
       \\
       & {}^{(-)|_{\Sigma_{in}}}\swarrow
       &&
       \searrow^{(-)|_{\Sigma_{out}}}
       \\
       [\Pi(\Sigma_{in}), \mathbf{Fields}]
       && &&
       [\Pi(\Sigma_{out}), \mathbf{Fields}]
    }
  \right)
  \,.
$$

=--

([lpqft](#lpqft))


+-- {: .num_prop}
###### Proposition 

Under the [[Dold-Kan correspondence]] 

$$
  DK \colon ChainComplexes \stackrel{\simeq}{\longrightarrow}
  SimplicialAbelianGroups
  \stackrel{forget}{\longrightarrow}
  KanComplexes
$$


we have for all $n \in \mathbb{N}$ an [[equivalence]]

$$
  \flat \mathbf{B}^{n+1}U(1)
   \simeq
  DK
  \left(
    \underline{U}(1)
    \stackrel{\mathbf{d}}{\longrightarrow}
    \mathbf{\Omega}^1 
    \stackrel{\mathbf{d}}{\longrightarrow}
    \mathbf{\Omega}^2
    \stackrel{\mathbf{d}}{\longrightarrow}
    \cdots  
   \stackrel{\mathbf{d}}{\longrightarrow}
    \mathbf{\Omega}^{n+1}_{cl}   
  \right)
$$

in $\mathbf{H}$.

=--

+-- {: .num_example #tYM}
###### Example

Consider the induced canonical inclusion

$$
  \mathbf{\Omega}^{n+1}
  \longrightarrow
  \flat \mathbf{B}^{n+1}U(1)
  \,.
$$

By the above we may regard this as an [[action functional]] for an $(n+1)$-dimensional [[prequantum field theory]] with [[moduli stack]] of [[field (physics)|fields]] being $\mathbf{\Omega}^{n+1}_{cl}$. As such we denote it

$$
  \array{
     \mathbf{\Omega}^{n+1}_{cl}
     \\
     \downarrow^{\mathrlap{\exp(i S_{tYM})}}
     \\
     \flat \mathbf{B}^{n+1}U(1)
  }
  \,,
$$

where the subscript is supposed to refer to "universal higher [[topological Yang-Mills theory]]".

=--

+-- {: .num_prop}
###### Proposition 

[[monoidal (∞,n)-functors]]

$$
  \array{
     Bord_n
     &\stackrel{\exp(i S)}{\longrightarrow}&
     Corr_n(\mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)})
     \\
     & {}_{\mathbf{Fields}} \searrow & \downarrow
     \\
     && Corr_n(\mathbf{H})
  }
$$

are equivalent to objects

$$
  \left(
  \array{
    \mathbf{Fields}
    \\
     \downarrow^{\mathrlap{\exp(i S)}}
    \\
    \flat \mathbf{B}^{n+1}U(1)
  }
  \right)
  \;\;\;
    \in
  \;\;\;
  \mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)}
  \hookrightarrow
  Corr_n(\mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)})
  \,.
$$

This sends the dual point to $\exp(- i S)$
and sends the $k$-[[sphere]] to the [[transgression]]
of $\exp(i S)$ to the mapping space $[S^k , \mathbf{Fields}]$.

=--

([lpqft](#lpqft))

+-- {: .num_example}
###### Example

Consider the induced canonical inclusion

$$
  \mathbf{\Omega}^{n+1}
  \longrightarrow
  \flat \mathbf{B}^{n+1}U(1)
  \,.
$$

By the above we may regard this as an [[action functional]] for an $(n+1)$-dimensional [[prequantum field theory]] with [[moduli stack]] of [[field (physics)|fields]] being $\mathbf{\Omega}^{n+1}_{cl}$. As such we denote it

$$
  \array{
     \mathbf{\Omega}^{n+1}_{cl}
     \\
     \downarrow^{\mathrlap{\exp(i S_{tYM})}}
     \\
     \flat \mathbf{B}^{n+1}U(1)
  }
  \,,
$$

where the subscript is supposed to refer to "universal higher [[topological Yang-Mills theory]]".

=--


Observe that by the [[cobordism hypothesis]] $Bord_n$ is the [[free construction|free]] [[symmetric monoidal (∞,n)-category]] with [[fully dualizable objects]] generated from a single object $\ast$. 

$$
  Bord_n \simeq FreeSMwD(\{\ast\})
  \,.
$$

Let then

$$
  Bord_n^{\partial} \coloneqq FreeSMwD(\{\emptyset \longrightarrow \ast\})
$$

the free [[symmetric monoidal (∞,n)-category]] with [[fully dualizable objects]] generated from a single object $\ast$ and a single [[morphism]] $\emptyset \longrightarrow \ast$ from the [[tensor unit]] to the generating object. By the [[boundary field theory]]/[[defect field theory|defect]] version of the [[cobordism hypothesis]], this is equivalently the [[(∞,n)-category of cobordisms]] with possibly a [[boundary]] component of [[codimension]] $(n-1)$.

Hence a [[boundary field theory]] is

$$
  \array{
     Bord_n^\partial
     &\stackrel{\exp(i S)}{\longrightarrow}&
     Corr_n(\mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)})
     \\
     & {}_{\mathbf{Fields}^\partial} \searrow & \downarrow
     \\
     && Corr_n(\mathbf{H})
  }
$$

+-- {: .num_remark}
###### Remark

A [[boundary field theory]] as above is equivalently a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    && \mathbf{Fields}_{bdr}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \mathbf{Fields}
    \\
    & \searrow && \swarrow_{\mathrlap{\exp(i S)}}
    \\
    && \flat \mathbf{B}^{n+1}U(1)
  }
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The _universal_ [[boundary field theory|boundary condition]] for
the universal higher topological Yang-Mills theory of example \ref{tYM} is the [[higher moduli stack]]
$\mathbf{B}^n U(1)_{conn}$ of [[circle n-bundle with connection]],
hence a general boundary condition for this 
higher [[topological Yang-Mills theory]] is a
[[schreiber:∞-Chern-Simons theory]]].



=--

The [[schreiber:∞-Wess-Zumino-Witten theory]] that we are after are boundaries of these boundary field theories, hence "corner field theories" ([Sati 11](#Sati11), [lpqft](#lpqft)) of the higher universal topological Yang-Mills theory. This we turn to now.


+-- {: .num_remark}
###### Remark


The earliest and the only rigorously understood example of the [[holographic principle]] is the [[AdS3-CFT2 and CS-WZW correspondence]] between the [[WZW model]] on a [[Lie group]] $G$ and 3d $G$-[[Chern-Simons theory]].

In ([Witten 98](7d+Chern-Simons+theory#Witten98)) it is argued that all examples of the [[AdS-CFT duality]] are governed by the [[schreiber:infinity-Chern-Simons theory|higher Chern-Simons theory]] terms in the [[supergravity]] [[Lagrangian]] on one side of the correspondence, hence that the corresponding [[conformal field theories] are higher dimensional analogs of the traditional [[WZW model]]: that they are "[[schreiber:∞-Wess-Zumino-Witten theory]]"-type models.

In particular for [[AdS7-CFT6]] this means that the [[6d (2,0)-superconformal QFT]] on the [[M5-brane]] [[worldvolume]] should be a 6d-dimensional WZW model holographically related to the [[7d Chern-Simons theory]] which appears when [[11-dimensional supergravity]] is [[KK-reduction|KK-reduced]] on a 4-[[sphere]]:

| [[schreiber:∞-Chern-Simons theory]] | $\leftarrow$[[holographic principle]]$\rightarrow$ | [[schreiber:∞-Wess-Zumino-Witten theory]] |
|---|---|---|
| 3d [[Chern-Simons theory]] |  | 2d [[Wess-Zumino-Witten model]] |
| [[7d Chern-Simons theory]] from [[11-dimensional supergravity]] |  | [[6d (2,0)-superconformal QFT]] on [[M5-brane]] |

In ([Witten 96](http://ncatlab.org/nlab/show/7d+Chern-Simons+theory#WittenI)) this is argued, by [[geometric quantization]] after [[transgression]] to [[codimension]] 1, for the _bosonic and abelian_  contribution in [[7d Chern-Simons theory]]. (The subtle [[theta characteristic]] involved was later formalized in [[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]].) 


In order to formalize this in generality, one needs a general formalization of [[holography]] for [[local prequantum field theory]] as these. How are [[schreiber:∞-Wess-Zumino-Witten theory]]-models higher holographic boundaries of [[schreiber:∞-Chern-Simons theory]]? This we are dealing with now.


=--



### Lie integration of $L_\infty$-cocycles

The datum going into [[schreiber:∞-Wess-Zumino-Witten theory]] is  [[smooth super ∞-group]] $G$ which is the [[Lie integration]] of a given [[super L-∞ algebra]] $\mathfrak{g}$, and is a [[L-∞ algebra cohomology|cocycle]] $\mu$ on $\mathfrak{g}$.

We discuss here how [[Lie integration]] relates $\mathfrak{g}$ to $G$ and how the Lie integration of the cocycle $\mu$ induces a smooth universal [[characteristic map]] $\exp(\mu) \colon \mathbf{B}G \longrightarrow \mathbf{B}^n (\mathbb{R}/\Gamma)$ ([Fiorenza-Schreiber-Stasheff 12](#FiorenzaSchreiberStasheff12)).

+-- {: .num_defn}
###### Definition


Given a ([[super L-∞ algebra|super]]-)[[L-∞ algebra]] $\mathfrak{g}$, its [[Lie integration]] is the [[∞-stack]]

$$
  \exp(\mathfrak{g})
  \colon
  U \mapsto
  \left(
   \Delta[k] \maptso
   \Omega^\bullet_{flat,vert,si}(U \times \Delta^k, \mathfrak{g})
  \right)
$$

which assigns to a test ([[super Cartesian space]]-)[[Cartesian space]] $U$ the [[Kan complex]] whose $k$-[[simplices]] are smooth [[L-∞ algebra valued differential forms]] on $U \times \Delta^k$ which are

1. flat

1. vertical, this means that all their "legs" are along $\Delta^k$

1. have [[sitting instants]]: such that the [[boundary]] of the [[simplex]] has a [[neighbourhood]] such that in this neighbourhood the differential form is constant in the direction perpendicular to the boundary (this condition makes the [[simplicial set]] indeed by a [[Kan complex]]).


=--

+-- {: .num_example}
###### Example

Let $\mathfrak{g}$ be an  ordinary [[Lie algebra]] then the [[truncated|1-truncation]] of $\exp(\mathfrak{g})$ is the [[delooping]] of the simply connected [[Lie group]] $G$ corresponding to $\mathfrak{g}$ under traditional [[Lie theory]]:

$$
  \tau_1 \exp(\mathfrak{g}) \simeq \mathbf{B}G
  \,.
$$

In fact also 

$$
  \tau_2 \exp(\mathfrak{g}) \simeq \mathbf{B}G
$$

but $\tau_3 \exp(\mathfrak{g})$ is different from $\mathbf{B}G$ if $\pi_3(G) $ is non-trivial.


=--

+-- {: .num_example}
###### Example

For $\mathfrak{g}$ a [[semisimple Lie algebra]] and 
$\mathfrak{string}(\mathfrak{g})$ its [[string Lie 2-algebra]], then

$$
  \tau_2 \exp(\mathfrak{string}(\mathfrak{g}))
  \simeq
  \mathbf{B}String(G)

  \,,
$$

where $String(G)$ is the smooth [[string 2-group]].

=--

+-- {: .num_remark}
###### Remark

The $\exp$-construction clearly extends to a [[functor]]

$$
  s L_\infty Alg
  \longrightarrow
  Func(sCartSp^{op}, KanCplx)
  \longrightarrow
  \mathbf{H}
$$

=--

+-- {: .num_defn}
###### Definition

An [[L-∞ algebra cohomology|L-∞ cocycle]] of degree $n+1$ on $\mathfrak{g}$ is a [[homomorphism]] of [[L-∞ algebras]] of the form

$$
  \mu
  \;\colon\;
  \mathfrak{g}
   \longrightarrow
  \mathbb{R}[n]
  \,.
$$

=--


Hence given a cocycle $\mu$, universal [[Lie integration]] produces a morphism of [[smooth super ∞-groupoids]] of the form

$$
  \exp(\mu)
  \;\colon\;
  \exp(\mathfrak{g})
  \longrightarrow
  \exp(\mathbb{R}[n])
  \simeq
  \mathbf{B}^{n+1}\mathbb{R}
  \,.
$$

+-- {: .num_defn}
###### Definition

Say that the [[periods]] of $\mu$ are all values in $\mathbb{R}$ obtained by [[integration]] of the $(n+1)$-form on an $(n+1)$-[[sphere]] in the image of the biundary of an $(n+1)$-simplex under this map. Write $\Gamma_\mu \hookrightarrow \mathbb{R}$ for the [[subgroup]] of such [[periods]]

=--



+-- {: .num_defn}
###### Definition

Under [[truncated|truncation]] the universal [[Lie integration]] above descents to an $(n+1)$-[[∞-group cohomology|∞-group cocycle]] with [[coefficients]] in $\mathbb{R}/\Gamma_{\mu}$:


$$
  \array{
    \exp(\mathfrak{g})
    &\stackrel{\exp(\mu)}{\longrightarrow}&
    \mathbf{B}^{n+1}\mathbb{R}
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G
    &\stackrel{}{\longrightarrow}&
    \mathbf{B}^{n+1}(\mathbb{R}/\Gamma_\mu)
  }
$$

where

$$
  \mathbf{B}G \coloneqq \tau_n \exp(\mathfrak{g})
  \,.
$$

=--

Proof: Use the standard [[coskeleton|simplicial (n+1)-coskeleton]] model for the $n$-truncation.


+-- {: .num_example}
###### Example

For $\mathfrak{g}$ a [[semisimple Lie algebra]]
with its canonical 3-cocycle $\mu = \langle -,[-,-]\rangle$, 
then 

$$
  \exp(\langle -,[-,-]\rangle)
  \simeq
  \mathbf{c}_2
  \;\colon\;
  \mathbf{B}G
  \longrightarrow
  \mathbf{B}^3 U(1)
$$

is the smooth refinement of the [[fractional first Pontryagin class]]/[[second Chern class]] whose [[homotopy fiber]] is the [[delooping]] of the [[string 2-group]]

$$
  \array{
    \mathbf{B}String(G)
    \\
    \downarrow
    \\

    \mathbf{B}G &\stackrel{\mathbf{c}_2}{\longrightarrow}&
    \mathbf{B}^3 U(1)
  }
$$

=--



### WZW $n$-bundles
 {#WZWnBundle}

+-- {: .num_remark}
###### Remark

Observe that the ordinary [[WZW term]] 

$$
  \mathcal{L}_{WZW} \;\colon\; G \longrightarrow \mathbf{B}^2 U(1)_{conn}
$$

on a [[compact Lie group]] is characterized (e.g. [Schweigert-Waldorf 07](#SchweigertWaldorf07)) in terms of  the corresponding [[universal Chern-Simons circle 3-connection]]

$$
  \mathcal{L}_{CS} \;\colon\; \mathbf{B}G_{conn} \longrightarrow \mathbf{B}^3 U(1)_{conn}
$$

by two pieces (the two ingredients in the [[homotopy fiber product]]-definition of [[ordinary differential cohomology]]):

1. the [[curvature]] of $\mathcal{L}_{WZW}$ is the value of the [[Chern-Simons form]] on the canonical [[Maurer-Cartan form]] on $G$;

1. the [[Dixmier-Douady class]] $\chi(\mathcal{L}_{WZW})$ is the [[looping]] of the class of the Chern-Simons circle 3-bundle.

=--

We discuss now how this construction generalizes to [[higher differential geometry]] in general, and to [[higher supergeometry]] in particular. Then in _[The brane bouquet of higher super WZW terms](#TheBraneBouquet)_ we discuss a class of examples of this construction arising from the tower of [[super L-∞ algebra|super]] [[L-∞ algebra cohomology|L-∞ extensions]] of [[super Minkowski spacetime]]. ([FSS 13b](#FSS13b))



Let 

$$
  \mu \colon \mathfrak{g} \longrightarrow \mathbb{R}[n]
$$

be a [[super L-∞ algebra]] [[L-∞ cocycle]] of degree $(n+1)$. Let 

$$
  \mathbf{c} \;\colon\; \mathbf{B}G \longrightarrow \mathbf{B}^{n+1}(\mathbb{R}/\Gamma)
$$

be its [[Lie integration]] in [[smooth super ∞-groupoids]], according to ([[schreiber:Cech Cocycles for Differential characteristic Classes|FSS 10]]). 

Observe that the [[smooth ∞-group]] $G$ has, by [[cohesion]], a canonical higher [[Maurer-Cartan form]]

$$
  \theta \;\colon \; G \longrightarrow \flat_{dR}\mathbf{B}G
  \,. 
$$

This is a [[cocycle]] in the nonabelian de Rham [[hypercohomology]] of $G$. We want an [[schreiber:∞-Wess-Zumino-Witten theory]] model with a _globally defined_ [[curvature]] $(n+1)$-form. Therefore consider the [[universal construction|universal]] solution $\tilde G$ of making $\theta$ globally well defined, hence the [[homotopy pullback]]

$$
  \array{
    \tilde G &\stackrel{\theta_{global}}{\to}& \Omega_{flat}(-,\mathfrak{g})
    \\
    \downarrow && \downarrow
    \\
    G &\stackrel{\theta_G}{\to}& \flat_{dR} \mathbf{B}G
  }
  \,.
$$

Then one observes that by [[cohesion]] the [[pasting]] diagram on the right of the following exists, and hence defines a [[local action functional]] $\exp(i S_{WZW})$ by the universal factorization on the left. This is the [[schreiber:∞-Wess-Zumino-Witten theory]] induced by the [[L-∞ cocycle]] $\mu$:

$$
  \array{
    && \tilde G
    \\
    & \swarrow &\downarrow^{\exp(i S_{WZW})}& \searrow^{\mathrlap{\mu(\theta_{global})}}
    \\
    \ast &\leftarrow& \mathbf{B}^n U(1)_{conn} &\rightarrow& \Omega_{cl}^{n+1}
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow
    \\
    && \flat \mathbf{B}^{n+1}U(1)
  }
  \;\;\;\;\coloneqq\;\;\;\;
  \array{
    && && \tilde G
    \\
    && & \swarrow && \searrow^{\mathrlap{\theta_{global}}}
    \\
    && G && && \Omega_{flat}(-,\mathfrak{g})
    \\
    & \swarrow && \searrow^{\mathrlap{\theta_G}} && \swarrow && \searrow^{\mathrlap{\mu}}
    \\
    \ast && && \flat_{dR}\mathbf{B}G && && \Omega^{n+1}_{cl}
    \\
    & \searrow && \swarrow && \searrow^{\mathrlap{\flat_{dR}\mathbf{c}}} && \swarrow
    \\
    && \flat \mathbf{B}G && &&\flat_{dR} \mathbf{B}^{n+1}U(1)
    \\
    && & {}_{\mathllap{\exp(i S_{CS}^{flat})}}\searrow^{\mathrlap{\flat \mathbf{c}}} && \swarrow
    \\
    && && \flat \mathbf{B}^{n+1}U(1)
  }
  \,.
$$

This uses the following general fact about how [[local action functionals]] $\mathbf{Fields} \longrightarrow \mathbf{B}^n U(1)_{conn}$ are themselves boundary conditions for what one might call _universal higher [[topological Yang-Mills theory]]_ ([[schreiber:Local prequantum field theory|lpqft]]), the theory given by the local action functional

$$
  \exp(i S_{tYM})
  \;\colon\;
  \mathbf{Fields}_{tYM} = \Omega^{n+1}_{cl}
  \longrightarrow 
  \flat \mathbf{B}^{n+1}U(1)
  \,,
$$

which is just the canonical inclusion of closed differential $(n+1)$-forms into the universal moduli stack of flat [[circle n-bundle with connection|circle (n+1)-bundles with connection]]. By the [[universal property]] of [[ordinary differential cohomology]] one finds that boundary conditions for this somewhat degenerate theory are precisely differential cocycles:

$$
  \array{   
    && \mathbf{Fields}_{boundary}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \Omega_{cl}^{n+1}
    \\
    & \searrow && \swarrow
    \\
   && \flat \mathbf{B}^{n+1}U(1)
  }
  \;\;\;
  \simeq
  \;\;\;
  \array{   
    && \mathbf{Fields}_{boundary}
    \\
    & \swarrow &\downarrow^{\exp(i S_{bdr})}& \searrow
    \\
    \ast &\leftarrow& \mathbf{B}^n U(1)_{conn} &\stackrel{F_{(-)}}{\to}& \Omega_{cl}^{n+1}
    \\
    & \searrow && \swarrow
    \\
   && \flat \mathbf{B}^{n+1}U(1)
  }
  \,.
$$



### The brane bouquet of super WZW $n$-bundles
 {#TheBraneBouquet}

* [[brane scan]]

  [[supergravity Lie 3-algebra]], [[supergravity Lie 6-algebra]]

  [[M-theory super Lie algebra]]

* [[schreiber:The brane bouquet]]

(...)

## References

* {#DAuriaFre80} [[Riccardo D'Auria]], [[Pietro Fré]] [[Tullio Regge]], _Graded Lie algebra, cohomology and supergravity_, Riv. Nuov. Cim. 3, fasc. 12 (1980) ([spire](http://inspirehep.net/record/156191))
  

* {#AzcarragaIzqierdo95} [[José de Azcárraga]], Izqierdo, _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_, Cambridge monographs of mathematical physics, (1995)
 



* {#CarchediRoytenberg12} [[David Carchedi]], [[Dmitry Roytenberg]], _On theories of superalgebras of differentiable functions_ ([arxiv:1211.6134](http://arxiv.org/abs/1211.6134))
  

* [[David Carchedi]], [[Dmitry Roytenberg]], _Homological Algebra for Superalgebras of Differentiable Functions_ ([arXiv:1212.3745](http://arxiv.org/abs/1212.3745))

* {#CareyJohnsonMurray02} [[Alan Carey]], Stuart Johnson, [[Michael Murray]], _Holonomy on D-Branes_ ([arXiv:hep-th/0204199](http://arxiv.org/abs/hep-th/0204199))
 

* {#CastellaniDAuriaFre91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)
  


* {#CAIB99} C. Chrysso&#8204;malakos, [[José de Azcárraga]], J. M. Izquierdo and C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nuclear Physics B Volume 567, Issues 1&#8211;2, 14 February 2000, Pages 293&#8211;330 ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))
 


* {#DeligneFreed99} [[Pierre Deligne]], [[Daniel Freed]], _Supersolutions_ ([arXiv:hep-th/9901094](http://arxiv.org/abs/hep-th/9901094))

  in [[Pierre Deligne]], [[Pavel Etingof]], [[Dan Freed]], L. Jeffrey, [[David Kazhdan]], [[John Morgan]], D.R. Morrison and [[Edward Witten]], (eds.), _[[Quantum Fields and Strings]]_
  


* {#FiorenzaSchreiberStasheff12} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_, Advances in Theoretical and Mathematical Phyiscs, Volume 16 Issue 1 (2012) ([arXiv:1011.4735](http://arxiv.org/abs/1011.4735))
  

* {#FSS13a} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_ ([arXiv:1301.2580](http://arxiv.org/abs/1301.2580))
  

* {#FSS13b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))
 


* {#Freed99} [[Daniel Freed]], _[[Five lectures on supersymmetry]]_, American Mathematical Society (1999)
  


* {#FreedWitten99} [[Dan Freed]], [[Edward Witten]], _Anomalies in String Theory with D-Branes_, Asian J. Math.3:819,1999 ([arXiv:hep-th/9907189](http://arxiv.org/abs/hep-th/9907189))
  


* {#Gawedzki87} [[Krzysztof Gaw?dzki]], _Topological Actions in two-dimensional Quantum Field Theories_, in [[Gerard 't Hooft]] et. al (eds.) _Nonperturbative quantum field theory_ Cargese 1987 proceedings,  ([web](http://inspirehep.net/record/257658?ln=de))
  

* {#HohnholdSolzTeichner11} [[Henning Hohnhold]], [[Stephan Stolz]], [[Peter Teichner]], _Super manifolds: an incomplete survey_, Bulletin of the Manifold Atlas (2011) 1&#8211;6 ([pdf](http://people.mpim-bonn.mpg.de/teichner/Papers/Survey-Journal.pdf))
  

* {#KonechnySchwarz98} Anatoly Konechny and [[Albert Schwarz]], 

  _On $(k \oplus l|q)$-dimensional supermanifolds_, in: [[Julius Wess]], V. Akulov (eds.) _Supersymmetry and Quantum Field Theory_ (D. Volkov memorial volume) Springer-Verlag, 1998 ,
Lecture Notes in Physics, 509 ([arXiv:hep-th/9706003](http://arxiv.org/abs/hep-th/9706003))

  _Theory of $(k \oplus l|q)$-dimensional supermanifolds_ Sel. math., New ser. 6 (2000) 471 - 486
  



* {#LawsonMichelsohn89} [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], _[[Spin geometry]]_, Princeton University Press (1989)
  


* {#Nieuwenhuizen83} [[Peter van Nieuwenhuizen]], _Free graded differential superalgebras_, in Lect. Notes in Phys. 180, 228-245, Springer-Verlag (1983) ([pdf](http://cds.cern.ch/record/142062/files/198302065.pdf))
  

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles]]_ 

  _Part I -- General theory_ ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

  _Part II -- Presentations_ ([arXiv:1207.0249](http://arxiv.org/abs/1207.0249))
  

* {#Nuiten13} [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, Thesis 2013
  

* {#Polchinski01} [[Joseph Polchinski]], _[[String theory|String theory volume II: Superstring theory and beyond]]_, Cambridge Monographs on Mathematical Physics (2001)
  

* {#Sati11} [[Hisham Sati]], _Corners in M-theory_, J. Phys. A44:255402, 2011 ([arXiv:1101.2793](http://arxiv.org/abs/1101.2793))
  

* {#SSS09} [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:L-∞ algebra connections|L ∞-algebra connections and applications to String- and Chern-Simons n-transport]]_, in _Quantum Field Theory_, Birkh&#228;user (2009), 303-424, DOI: 10.1007/978-3-7643-8736-5_17 ([arXiv:0801.3480](http://arxiv.org/abs/0801.3480)) 
 

* {#S} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_
  

* {#SchreiberClassical} [[Urs Schreiber]], _[[schreiber:Classical field theory via Cohesive homotopy types]]_
  

* {#lpqft} [[Urs Schreiber]] et al. _[[schreiber:Local prequantum field theory]]_
  

* {#SchweigertWaldorf07}[[Christoph Schweigert]], [[Konrad Waldorf]], _Gerbes and Lie Groups_, in _Trends and Developments in Lie Theory_, Progress in Math., Birkh&#228;user ([arXiv:0710.5467](http://arxiv.org/abs/0710.5467))
  

* {#Varadarajan04} [[Veeravalli Varadarajan]], _[[Supersymmetry for mathematicians]]: An introduction_, Courant lecture notes in mathematics, American Mathematical Society Providence, R.I 2004
 


* {#Witten12} [[Edward Witten]], _Notes On Supermanifolds and Integration_ ([arXiv:1209.2199](http://arxiv.org/abs/1209.2199))
 

For more see also

* [[Urs Schreiber]], _[[schreiber:Structure Theory for Higher WZW Terms]]_
