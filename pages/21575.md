+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

We would like a general procedure to determine when a [[topos]] can be a category of models of homotopy types of CW-complexes, the same way simplicial sets, cubical sets, or any other category of presheaves on a [[test category]] do. In particular, given a sheaf $X$ on a site $C$, we would like that the [[shape theory | shape]] of the topos $Sh(C)_{/X}$ to be strongly related with the (weak) homotopy type of $X$. Typical examples coming from geometry should be sheaves of sets on suitable categories of manifolds. Grothendieck never mentioned the concept of test topoi themselves, but the idea of `test topologies' on test categories is expressed from time to time in Pursuing Stacks. As in the case of test categories, the natural (i.e most robust) notion is in fact local: it is worth looking at models of homotopy types over a given homotopy type.

In other terms, given a topos $X$, a natural question will be to formulate how the objects of $X$ are models of homotopy types over the homotopy type of $X$ (defined through shape theory). The following is a summary of part of ([Cisinski03](#Cisinski03])).

## Artin-Mazur weak equivalences

A morphism of Grothendieck topoi $f\colon X\to Y$ is an **Artin-Mazur weak equivalence** if, for any integer $n\geq 0$ and any locally constant sheaf $F$ on $Y$, the induced map 
\[
f^*\colon H^n(Y,F)\to H^n(X,F)
\]

is bijective, with $n=0$ if $F$ is a sheaf of sets, $n=1$ if $F$ is a sheaf of groups, and $n$ is arbitrary if $F$ is a sheaf of abelian groups. These are simply called **weak homotopy equivalences** of topoi in ([Moerdijk95](#Moerdijk95)).
In particular, any morphism inducing an equivalence of [[shape theory | shapes]] of the associated hypercomplete $\infty$-topoi is
Artin-Mazur weak equivalence; see ([Hoyois18](#Hoyois18)). 

Given a [[Grothendieck topos]] $T$, a morphism $\colon x\to y$ in $T$ is an **Artin-Mazur weak equivalence** if the induced morphism of topoi $T_{/x}\to T_{/y}$ (whose pull-back functor is defined via the assignment $(t\to y)\mapsto (t\times_y x\to x)$) is an Artin-Mazur weak equivalence.

+-- {: .num_remark}
###### Remark
If $f\colon C\to D$ is a functor between small categories, it induces a morphism of topoi $f\colon PSh(C)\to PSh(D)$ whose pull-back functor is defined by precomposition with $u$. The nerve of the functor $f$ is a weak homotopy equivalence of simplicial sets if and only if the corresponding morphism of topoi is an Artin-Mazur weak equivalence. This is a reformulation of a well known theorem of Whitehead asserting that one can detect weak homotopy equivalences through cohomology with coefficients in local systems.

=--

There is an analogue of (a relative version of) Quillen's Theorem A which is a direct application of (hyper)[[descent]] (e.g. see Thm. 3.4.25 in ([Cisinski03](#Cisinski03))):

+-- {: .num_prop #theorem A for topoi}
###### Proposition
_Let_
\[
\array{ X & & \overset{f}{\to} & & Y\\ & _p \searrow & & \swarrow_q \\ & & S }
\]
_be a commutative triangle of Grothendieck topoi.
Let $(S_i)_{i\in I}$ be a small family of maps in $S$ which is a covering, i.e. so that the induced map from $\coprod_i S_i$ to the terminal object of $S$ is an epimorphism. If, for each index $i$ the induced map $X_{/p^*(S_i)}\to Y_{/q^*(S_i)}$ is an Artin-Mazur weak equivalence, then the map $f:X\to Y$ is
an Artin-Mazur weak equivalence as well._
=--

A particular case is the following.

+-- {: .num_prop #theorem A in topoi}
###### Corollary
_Let_
\[
\array{ X & & \overset{f}{\to} & & Y\\ & _p \searrow & & \swarrow_q \\ & & S }
\]
_be a commutative triangle in a Grothendieck topos $T$.
Let $(S_i\to S)_{i\in I}$ be a small family of maps in $T$ which is a covering, i.e. so that the induced map $\coprod_i S_i\to S$ is an epimorphism.
If, for each index $i$ the induced map $S_i\times_S X\to S_i\times_SY$ is an Artin-Mazur weak equivalence, then the map $f:X\to Y$ is
an Artin-Mazur weak equivalence as well._
=--

+-- {: .num_prop #saturation}
###### Proposition
_Let $T$ be a Grothendieck topos. The class of monomorphisms which are Artin-Mazur weak equivalences is [[saturated class of maps | saturated]] and stable under small filtered colimits._
=--

+-- {: .proof}
###### Proof
This follows right away from Prop. 3.4.22 in ([Cisinski03](#Cisinski03)).
=--

+-- {: .num_defn #asphtopos}
###### Definition
A Grothendieck topos $T$ is **aspherical** if the map $T\to pt$ to the terminal topos is an Artin-Mazur weak equivalence.

An object $x$ of a topos $T$ is **aspherical** if the corresponding topos $T_{/x}$ is aspherical.

A Grothendieck topos $T$ is **locally aspherical** there is a generating family of $T$ which consists of aspherical objects.
=--

+-- {: .num_example #ex1}
###### Example
If $C$ is a small category, the corresponding topos of presheaves of sets $PSh(C)$ is locally aspherical.
Indeed, representable presheaves generate $PSh(C)$, and, for any presheaf $x$ on $C$ represented by an object $c$ of $C$, we have a canonical equivalence
$$PSh(C)_{/x}\cong PSh(C_{/c})$$
with $PSh(C_{/c})$ aspherical because the slice category $C_{/c}$ has a terminal object.
=--

+-- {: .num_example #ex3}
###### Example
A topos $T$ is locally aspherical if and only if $T\cong Sh(C)$ where $C$ is a small site such that, for any representable presheaf $U$ on $C$, with associated sheaf $U^{\wedge}$,
the topos $T_{/U^{\wedge}}$ is aspherical. Equivalently (using the toposic analogue of Quillen's Theorem A above), for any presheaf $F$ on $C$ with associated sheaf $F^{\wedge}$, the induced morphism of topoi
$T_{/F^{\wedge}}\to PSh(C)_{/F}$ is an Artin-Mazur weak equivalence.
=--

## Characterization and examples

+-- {: .num_defn #interval}
###### Definition
An **interval** in a topos $T$ is an object $I$ with the following properties: 

* it has two disjoint global sections: there is a monomorphism from the disjoint union of two copies of the terminal object to $I$;

* for any object $X$ in $T$, the projection $I\times X\to X$ is an Artin-Mazur weak equivalence (equivalently, there exists
a small family $(S_i)_{i\in I}$ which covers $T$ such that the projection $I\times S_i\to S_i$ is an Artin-Mazur weak equivalence).
=--

+-- {: .num_prop #characterization of local pretest topoi}
###### Proposition

Let $T$ be a Grothendieck topos. The following conditions are equivalent:

* Any morphism of $T$ with the right ligting property with respect to monomorphisms is an Artin-Mazur weak equivalence;

* There exists an interval in $T$;

=--

+-- {: .proof}
###### Proof
Since the class of Artin-Mazur weak equivalences has the 2-out-of-3 property and is saturated, this follows from Lemma 3.3 in ([Cisinski02](#Cisinski02)).
=--

+-- {: .num_defn #testtopos}
###### Definition

A **local test topos** is a topos which is locally aspherical and which has an interval.

A **test topos** is a local test topos which is aspherical.

=--

+-- {: .num_example #ex4}
###### Example

A small category $A$ is a (local) [[test category]] if and only if the associated topos $PSh(A)=Fun(A^{op},Set)$ is a (local) test topos:
this follows from the proposition right above and from the characterization of local test categories provided by Thm. 1.5.6 in ([Maltsiniotis05](#Maltsin05)).

=--

+-- {: .num_example #ex5}
###### Example

Let $T$ be a topos and $C$ a small site such that $T\cong Sh(C)$. We assume that $C$ is a local [[test category]] and that,
for any representable presheaf $F$ on $C$ with associated sheaf $F^\wedge$, the topos $T_{/U^{\wedge}}$ is aspherical.
Then $T$ is a local test topos: any interval of $PSh(C)$ is then an interval of $T$, and $T$ is clearly
locally aspherical; see Thm. 4.2.8 in ([Cisinski03](#Cisinski03)).

=--

+-- {: .num_theorem #toposic local test model structure}
###### Theorem

Let $T$ be a local test topos. Then there is a proper [[combinatorial model category]] structure on $T$ whose
cofibrations are the monomorphisms, and whose weak equivalences are the Artin-Mazur weak equivalences.
Futhermore, this model structure provides models for homotopy types over the homotopy type of $T$.
More precisely, if $C$ is any small site whose underlying category is a local test category, such that
$T\cong Sh(C)$, and such that, for any representable presheaf $F$ on $C$ with associated sheaf $F^\wedge$,
the topos $T_{/F^{\wedge}}$ is aspherical, then the sheafification functor is a left Quillen equivalence
$PSh(C)\to T$, and there is a left Quillen equivalence $PSh(C)\to SSet_{/N(C)}$ which sends any presheaf
$F$ to the nerve of its category of elements $C_{/F}$.

=--

+-- {: .proof}
###### Proof
The first assertion on the existence of a combinatorial proper model structure comes from Cor. 4.2.12 in ([Cisinski03](#Cisinski03))
and is an example of a [[Cisinski model structure]] provided by Thm. 3.9 in ([Cisinski02](#Cisinski02)).
For the second part, it is obvious that the sheafification functor is a left Quillen equivalence from $PSh(C)$ to $T$
and an Artin-Mazur weak equivalence. Therefore, it is sufficient to prove the case where $T=PSh(C)$. This is then a particular
case of Proposition 4.4.28 in ([Cisinski06](#Cisinski06)).

=--

+-- {: .num_prop #toposic test model structure}
###### Corollary

Let $T$ be a test topos. Then there is a proper combinatorial model category structure on $T$ whose
cofibrations are the monomorphisms, and whose weak equivalences are the Artin-Mazur weak equivalences which
models homotopy types of CW-complexes.

=--

+-- {: .num_example #ex6}
###### Example

Let $T$ be a local test topos and $C$ an internal category of $T$. On can then consider the topos $PSh(C)$ of internal
presheaves on $C$ (which only depends on the stack associated to $C$). Then, by virtue of Thm. 6.2.7
in ([Cisinski03](#Cisinski03])), $PSh(C)$ is a local test topos as well.
In particular, if $G$ is a sheaf of groups on $T$, then $Rep(G)=PSh(BG)$ is the category of representations of $G$ (i.e.
the objects of $T$ equipped with an action of $G$). If the Artin-Mazur weak equivalences are stable under finite products in $T$,
then one can show that the Artin-Mazur weak equivalences of $Rep(G)$
simply are the $G$-equivariant maps $X\to Y$ which are Artin-Mazur weak equivalences in $T$ when we forget the action
of $G$; to see this, one reduces easily to the case where $T$ is a category of presheaves on a local test category,
and this follows then from Prop. 7.3.8 in ([Cisinski02](#Cisinski02])).

=--

+-- {: .num_example #ex7}
###### Example

Let us consider a full subcatogry $C$ of the category of locally ringed spaces with the following properties:

* for any space $X$ in $C$, there is a basis of contractible open subsets of $X$ which are $C$;

* for any locally ringed space $X$, if each point of $X$ admits an open neighborhood in $C$, then $X$ belong to $X$;

* the forgetful functor from $C$ to the category of topological spaces commutes with products (up to weak equivalence);

* there exists a contractible space with two distinct closed points in $C$.

We consider $C$ as site with the Grothendieck topology induced by open coverings.
Then, for any $X$ in $C$, the topos $Sh(C)_{/X}$ is aspherical because there is an adjunction between $Sh(X)$ and $Sh(C)_{/X}$ in the $2$-category of topoi.
Therefore, since $C$ is a [[strict test category]], we see that $Sh(C)$
is a test topos in which the Artin-Mazur weak equivalencesne are stable under finite products; see Thm. 6.1.8 in ([Cisinski03](#Cisinski03])).
If $X$ is a locally ringed space which has a covering by spaces in $C$, then the sheaf on $C$ represented by $X$ corresponds
in the test model structure on $Sh(C)$ to the classical weak homotopy type of $X$ (this follows by hyperdescent in shape theory). In practice, all objects of $C$
admit CW-structures, so that we even get the classical homotopy type of $X$ characterized by the sheaf represented by $X$ on $C$.
Such geometric models of weak homotopy types of manifolds are used for instance by Madsen and Weiss ([Madsen-Weiss07](#Madsen-Weiss07)) and Kupers ([Kupers19](#Kupers19)).

Examples of such 'test sites' $C$ are given by: euclidian spaces (seen as $C^\infty$-manifolds), or contractible Stein complex manifolds.
If $G$ is a real (or complex) Lie group, then representations of $G$ in the topos of sheaves on differentiable (or complex analytic) manifolds
is a local test topos. One may also replace $G$ by any orbifold, presented as an internal groupoid in the category of manifolds.

=--

## Related concepts

* [[test category]]

## References

 
* {#Artin-Mazur69} [[Michael Artin]] and [[Barry Mazur]], _Etale homotopy_, Lecture Notes in Mathematics 100, Springer (1969).

* {#Cisinski02} [[Denis-Charles Cisinski]], _Théories homotopiques dans les topos_, J. Pure Appl. Algebra 174, No. 1 (2002). ([doi](https://www.sciencedirect.com/science/article/pii/S0022404901001761))

* {#Cisinski03} [[Denis-Charles Cisinski]], _Faisceaux localement asph&#233;riques_, preprint (2003) ([pdf](http://www.mathematik.uni-regensburg.de/cisinski/mtest2.pdf))

* {#Hoyois18} [[Marc Hoyois]], _Higher Galois theory_, J. Pure Appl. Algebra 222, no. 7 (2018), ([arXiv](http://arxiv.org/abs/1506.07155))

* {#Kupers19} Alexander Kupers, _Three applications of delooping to h-principles_, Geom. Dedicata 202 (2019), pp. 103–151. ([journal](https://link.springer.com/article/10.1007/s10711-018-0405-7), [arXiv](https://arxiv.org/abs/1701.06788))

* {#Madsen-Weiss07} [[Ib Madsen]] and [[Michael Weiss]], _The stable moduli space of Riemann surfaces: Mumford’s conjecture_, Ann. of Math. (2)165(2007), no. 3, 843–941. ([journal](http://doi.org/10.4007/annals.2007.165.843), [arXiv](https://arxiv.org/abs/math/0212321))

* {#Maltsin05} [[Georges Maltsiniotis]], _La th&#233;orie de l'homotopie de Grothendieck_, Ast&#233;risque 301 (2005) (see
[html](http://people.math.jussieu.fr/~maltsin/textes.html))

* {#Moerdijk95} [[Ieke Moerdijk]], _Classifying spaces and classifying topoi_, Lecture Notes in Mathematics 1616, Springer (1995). 

[[!redirects test toposes]]

[[!redirects topos test]]

[[!redirects local test toposes]]