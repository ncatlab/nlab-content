
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $E_1, E_2 \to X$ two [[vector bundles]], their [[direct sum]] over $X$, also called their **Whitney sum**, is the vector bundle $E_1 \oplus E_2 \to X$ whose [[fiber]] over any $x \in X$ is the [[direct sum]] of vector spaces of the fibers of $E_1$ and $E_2$ (the [fiber-wise](topological+vector+bundle#FiberwiseOperations) direct sum).

## Definition

+-- {: .num_defn #DirectSumOfTopologicalVectorBundlesViaTotalspaces}
###### Definition
**([[direct sum]] of [[topological vector bundles]] via total spaces)**

Let 

1. $X$ be a [[topological space]],

1. $E_1 \overset{\pi_1}{\to} X$ and $E_2 \overset{\pi_2}{\to} X$ two [[topological vector bundles]] over $X$.

Then the _direct sum of vector bundles_ $E_1 \oplus_X E_2 \to E$ is the [[topological vector bundle]] whose total space is the [[topological subspace]]

$$
  E_1 \oplus_X E_2
  \;\coloneqq\;
  \left\{
    (v_1, v_2)
    \in 
    E_1 \times E_2
    \,\vert\,
    \pi_1(v_1) = \pi_2(v_2)
  \right\}
  \;\subset\;
  E_1 \times E_2
$$

of the [[product topological space]] of the two total spaces, and whose projection map is

$$
  \array{
    E_1 \oplus_X E_2 
      &\overset{\phantom{AA}\pi\phantom{AA}}{\longrightarrow}&
    X
    \\
    (v_1,v_2) &\overset{\phantom{AAA}}{\mapsto}& \pi_1(v_1) = \pi_2(v_2)
  }
  \,.
$$

For $x \in X$ the vector space structure on the [[fibers]] 

$$
  (E_1 \oplus E_2)_x \simeq (E_1)_x \oplus (E_2)_x
$$

is the one on the [[direct sum]] of [[vector spaces]].


=--

+-- {: .num_defn #DirectSumOfTopologicalVectorBundlesViaTransitionFunctions}
###### Definition
**([[direct sum]] of [[topological vector bundles]] via [[transition functions]])**

Let $X$ be a [[topological space]], and let $E_1 \to X$ and $E_2 \to X$ be two [[topological vector bundles]] over $X$. 

Let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]] with respect to which both vector bundles locally trivialize (this always exists: pick a [[local trivialization]] of either bundle and form the joint [[refinement]] of the respective [[open covers]] by [[intersection]] of their patches). Let 

$$
  \left\{
    (g_1)_{i j}
    \colon U_i \cap U_j \to GL(n_1)
  \right\}
  \phantom{AAA}
  \text{and}  
  \phantom{AAA}
  \left\{
    (g_2)_{i j}
    \colon
     U_i \cap U_j \longrightarrow GL(n_2)
  \right\}
$$

be the [[transition functions]] of these two bundles with respect to this cover.

For $i, j \in I$ write

$$
  \array{
    (g_1)_{i j} \oplus (g_2)_{i j}
    &\colon&
    U_i \cap U_j
      &\longrightarrow&
    GL(n_1 + n_2)
    \\
    &&
    x 
      &\overset{\phantom{AAA}}{\mapsto}&
    \left(
      \array{
         (g_1)_{i j}(x) & 0
         \\
         0 & (g_2)_{i j}(x)
      }
    \right)
  }
$$

be the pointwise [[direct sum]] of these transition functions

Then the _direct sum bundle_ $E_1 \oplus E_2$ is the one glued from this direct sum of the transition functions (by [this construction](topological+vector+bundle#TopologicalVectorBundleFromCechCocycle)):

$$
  E_1 \oplus E_2
  \;\coloneqq\;
  \left(
    \left( \underset{i}{\sqcup} U_i \right)
    \times 
    \left(
      \mathbb{R}^{n_1 + n_2}
    \right)
  \right)/ \left( \left\{ (g_1)_{i j} \oplus (g_2)_{i j} \right\}_{i,j \in I} \right)
  \,.
$$
 

=--

## Examples

+-- {: .num_example #DirectSumOnDisjointUnionSpace}
###### Example

Let $X$ and $Y$ be [[topological spaces]], and write  $X \sqcup Y$
for their [[disjoint union space]]. 

Then every [[topological vector bundle]] on $X \sqcup Y$ is the direct sum of a vector bundle that has [[rank of a vector bundle|rank]] zero on $Y$ and one that has rank zero on $X$. 

More explicitiy: let

$$
  i_X \colon Vect(X) \longrightarrow Vect(X \sqcup Y)
$$

and

$$
  i_Y \colon Vect(Y) \longrightarrow Vect(X \times Y)
$$

be the operations of extending a vector bundle on the other [[connected component]] by a rank-0 vector bundle, then 

$$
  Vect(X) \times Vect(Y)
    \underoverset{\simeq}{ i_X \oplus_{(X \sqcup Y)} i_Y }{\longrightarrow}
  Vect(X \sqcup Y)
$$

is an [[isomorphism]] of [[isomorphism classes]] of vector bundles (and an [[equivalence of categories]] of [[Vect(X)|categories of vector bundles]] before passing to isomorphism classes).


=--

## Properties

### Whitney summands of trivial vector bundles

+-- {: .num_prop #TopologicalSubBundlesOverParacompactHausdorffSpacesAreDirectSummands}
###### Proposition
**(sub-bundles over [[paracompact spaces]] are [[direct sum of vector bundles|direct summands]])**

Let 

1. $X$ be a [[paracompact Hausdorff space]],

1. $E \to X$ a [[topological vector bundle]]. 

Then every vector subbundle $E_1 \hookrightarrow E$ is a direct vector bundle summand, in that there exists another vector subbundle $E_2 \hookrightarrow E$ such that their direct sum of vector bundles (def. \ref{DirectSumOfTopologicalVectorBundlesViaTotalspaces}) is $E$

$$
  E_1 \oplus E_2 \simeq E
  \,.
$$

=--

([e.g. Hatcher, prop. 1.3](#Hatcher))

+-- {: .proof}
###### Proof

Since $X$ is assumed to be paracompact Hausdorff, there exists a [[inner product on vector bundles]]

$$
  \langle -,-\rangle
  \;\colon\;
  E \oplus_X E 
    \longrightarrow
  X \times \mathbb{R}
$$

(by [this prop.](inner+product+of+vector+bundles#ExistenceOfInnerProductOfTopologicalVectorBundlesOverParacompactHausdorffSpaces)). This defines at each $x \in X$ the [[orthogonal complement]] $(E'_x)^\perp \subset E_x$ of $E'_x \hookrightarrow E$. The [[subspace]] of these orthogonal complements is readily checked to be a [[topological vector bundle]] $(E')^\perp \to X$. Hence by construction we have

$$
  E \;\simeq\; E' \oplus_X (E')^\perp
  \,.
$$

=--

+-- {: .num_prop #OverCompactHausdorffSpacesEveryTopologicalVectorBundleIsDirectSummandOfATrivialBundle}
###### Proposition
**(over [[compact Hausdorff spaces]] every vector bundle is [[direct sum of vector bundles|direct summand]] of a trivial bundle)**

Let 

1. $X$ be a [[compact Hausdorff space]];

1. $E \to X$ a [[topological vector bundle]].

Then there exists another topological vector bundle $\tilde E \to X$ such that the direct sum of vector bundles (def. \ref{DirectSumOfTopologicalVectorBundlesViaTotalspaces}) of the two is a trivial vector $X \times \mathbb{R}^n$:

$$
  E \oplus \tilde E
   \;\simeq\;
  X \times \mathbb{R}^n
  \,.
$$

=--

(e.g. [Hatcher, prop. 1.4](#Hatcher), [Friedlander, ptop. 3.1](#Friedlander))

+-- {: .proof}
###### Proof

Let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]] of $X$ over which $E \to X$ has a [[local trivialization]]

$$
  \left\{
    \phi_i
      \;\colon\;
     U_i \times \mathbb{R}^n
       \overset{\simeq}{\longrightarrow}
     E\vert_{U_i}
  \right\}_{i \in I}
  \,.
$$

By compactness of $X$, there is a [[finite cover|finite sub-cover]], hence a [[finite set]] $J \subset I$ such tat 

$$
  \{U_i \subset X\}_{i \in J \subset I}
$$

is still an open cover over which $E$ trivializes.

Since [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]] there exists a [[partition of unity]]

$$
  \left\{
    f_i \;\colon\; X \to [0,1]
  \right\}_{i \in J}
$$

with [[support]] $supp(f_i) \subset U_i$. Hence the functions

$$
  \array{
    E\vert_{U_i} 
     &\overset{\phantom{AAAA}}{\longrightarrow}&
    U_i \times \mathbb{R}^n
    \\
    v 
       &\overset{\phantom{AAA}}{\mapsto}&
    f_i(x) \cdot \phi_i^{-1}(v)
  }
$$

extend by 0 to vector bundle homomorphism of the form

$$
  f_i \cdot \phi^{-1}_i
  \;\colon\;
  E
    \longrightarrow
  X \times \mathbb{R}^n
  \,.
$$

The finite pointwise [[direct sum]] of these yields a vector bundle homomorphism
of the form

$$
  \underset{i \in J}{\oplus} f_i \cdot \phi_i
  \;\colon\;
  E
    \longrightarrow
  X \times \left( 
    \underset{i \in J}{\oplus}
       \mathbb{R}^n
  \right)
  \simeq
  X \times \mathbb{R}^{n \dot {\vert J\vert}}
  \,.
$$

Observe that, as opposed to the single $f_i \cdot \phi^{-1}_i$, this is a fiber-wise injective, because at each point at least one of the $f_i$ is non-vanishing. Hence this is an injection of $E$ into a trivial vector bundle. 

With this the statement follows by prop. \ref{TopologicalSubBundlesOverParacompactHausdorffSpacesAreDirectSummands}.

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{OverCompactHausdorffSpacesEveryTopologicalVectorBundleIsDirectSummandOfATrivialBundle} is key for the construction of [[topological K-theory]] groups on compact Hausdorff spaces.

=--

Remark : Let $E_1\rightarrow M$ and $E_2\rightarrow M$ be vector bundles over $M$. This gives product map $E_1\times E_2\rightarrow M\times M$ which is still a vector bundle. Consider diagonal map $d:M\rightarrow M\times M$ given by $m\mapsto (m,m)$. The Whitney sum of $E_1\rightarrow M$ and $E_2\rightarrow M$ is the pull back of $E_1\times E_2\rightarrow M\times  M$ along the diagonal map $d:M\rightarrow M\times M$ which is denoted by $E_1\oplus E_2\rightarrow M$.  


### Characteristic classes of Whitney sums

+-- {: .num_prop #EulerClassOfWhitneySumIsCupProductOfEulerClasses}
###### Proposition
**([[Euler class]] takes [[Whitney sum]] to [[cup product]])**

The Euler class of the [[Whitney sum]] of two [[orthogonal group|oriented]] [[real vector bundles]] to the [[cup product]] of the separate Euler classes:

$$
  \chi( E \oplus F )
  \;=\;
  \chi(E)  \smile \chi(F)
  \,.
$$

=--

For details see at [[Euler class]], [this Prop.](Euler+class#EulerClassOfWhitneySumIsCupProductOfEulerClasses).




## Related concepts

* [[inner product on vector bundles]]

* [[tensor product of vector bundles]], [[external tensor product of vector bundles]], [[dual vector bundle]], 

* [[tensor category]]

* [[Stiefel-Whitney class]]

* [[virtual vector bundle]], [[topological K-theory]]

* [[framed manifold]], [[Thom spectrum]]

## References

Discussion with an eye towards [[topological K-theory]] is in

* [[Max Karoubi]], _K-theory. An introduction_, Grundlehren der Mathematischen Wissenschaften __226__, Springer 1978. xviii+308 pp.


* {#Hatcher} [[Allen Hatcher]], section 1.1 of _Vector bundles and K-Theory_, (partly finished book) [web](http://www.math.cornell.edu/~hatcher/VBKT/VBpage.html)

and with an eye towards [[algebraic K-theory]] in

* {#Friedlander} [[Eric Friedlander]], _An introduction to K-theory_ (emphasis on [[algebraic K-theory]]), 2007 ([pdf](http://users.ictp.it/~pub_off/lectures/lns023/Friedlander/Friedlander.pdf))



[[!redirects Whitney sum]]

[[!redirects direct sums of vector bundles]]
