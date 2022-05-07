
## Idea

We would like a general procedure to determine when a [[topos]] can be a category of models of homotopy types of CW-complexes, the same way simplicial sets, cubical sets, or any other category of presheaves on a [[test category]] do. In particular, given a sheaf $X$ on a site $C$, we would like that the [[shape theory | shape]] of the topos $Sh(C)_{/X}$ to be strongly related with the (weak) homotopy type of $X$. Typical examples coming from geometry should be sheaves of sets on suitable categories of manifolds. Grothendieck never mentioned the concept of test topoi themselves, but the idea of `test topologies' on test categories is expressed from time to time in Pursuing Stacks. As in the case of test categories, the natural (i.e most robust) notion is in fact local: it is worth looking at models of homotopy types over a given homotopy type. In other terms, given a topos $T$, a natural question will be to formulate how the objects of $T$ are models of homotopy types over the homotopy type of $T$ (defined through shape theory).

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

There is an analogue of (a relative version of) Quillen's Theorem A which is a direct application of (hyper)[[descent]] (e.g. see Thm. 3.4.25 in ([Cisinski03](#Cisinski03]))):

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
This follows right away from Prop. 3.4.22 in ([Cisinski03](#Cisinski03])).
=--

## Related concepts

* [[test category]]

## References

 
* {#Artin-Mazur69} [[Michael Artin]] and [[Barry Mazur]], _Etale homotopy_, Lecture Notes in Mathematics 100, Springer (1969).

* {#Cisinski03} [[Denis-Charles Cisinski]], _Faisceaux localement asph&#233;riques|Faisceaux localement asph&#233;riques_, preprint (2003) ([pdf](http://www.mathematik.uni-regensburg.de/cisinski/mtest2.pdf))

* {#Hoyois18} [[Marc Hoyois]], _Higher Galois theory_, J. Pure Appl. Algebra 222, no. 7 (2018), ([arXiv](http://arxiv.org/abs/1506.07155))

* {#Moerdijk95} [[Ieke Moerdijk]], _Classifying spaces and classifying topoi_, Lecture Notes in Mathematics 1616, Springer (1995). 

[[!redirects test toposes]]

[[!redirects topos test]]