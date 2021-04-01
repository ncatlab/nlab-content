[[!redirects inner product of vector bundles]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles#
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

The concept of _inner product on vector bundles_ is the evident generalization of that of [[inner product]] on [[vector spaces]] to [[vector bundles]]: a [[fiber]]-wise inner product of vector spaces.

## Definition

+-- {: .num_defn #InnerProductOnTopologicalVectorBundles}
###### Definition
**(inner product on [[topological vector bundles]])**

Let 

1. $k$ be a [[topological field]] (such as the [[real numbers]] or [[complex numbers]] with their [[Euclidean space|Euclidean]] [[metric topology]] ),

1. $X$ be a [[topological space]],

1. $E \to X$ a [[topological vector bundle]] over $X$ (over $\mathbb{R}$, say).

Then an _inner product_ on $E$ is 

* a vector bundle [[homomorphism]]

  $$
    \langle -,-\rangle
    \;\colon\;
    E \otimes_X E 
     \longrightarrow
    X \times \mathbb{R}
  $$

  from the [[tensor product of vector bundles]] of $E$ with itself to the trivial [[line bundle]]

such that

* for each point $x \in X$ the function

  $$
    \langle -,-\rangle|_x \colon E_x \otimes E_x \to \mathbb{R}
  $$

  is an [[inner product]] on the [[fiber]] [[vector space]], hence a positive-definite symmetric [[bilinear form]].

=--

## Properties

### Existence

+-- {: .num_prop #ExistenceOfInnerProductOfTopologicalVectorBundlesOverParacompactHausdorffSpaces}
###### Proposition

Let $X$ be a [[paracompact Hausdorff space]]. Then on every [[topological vector bundle]] $E \to X$ on $X$ there exists an inner product of topological vector bundles (def. \ref{InnerProductOnTopologicalVectorBundles})

=--

(e.g. [Hatcher, prop. 1.2](#Hatcher))

+-- {: .proof}
###### Proof

Let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]] of $X$ over which $E \to X$ admits a [[local trivialization]]

$$
  \left\{
    \phi_i \;\colon\;
    U_i \times \mathbb{R}^n
      \overset{\simeq}{\longrightarrow}
    E|_{U_i}
  \right\}_{i \in I}
  \,.
$$


Since [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]] we may choose a [[partition of unity]]

$$
  \{f_i \;\colon\; X \to [0,1]\}_{i \in I}
  \,.
$$

Write

$$
  \langle -,-\rangle_{\mathbb{R}^n}
  \;\colon\;
  \mathbb{R}^n 
    \otimes
  \mathbb{R}^n
    \longrightarrow
  \mathbb{R}
$$

for the standard inner product on $\mathbb{R}^n$.

By the [[compact support]] of $f_i$ inside $U_i \subset X$, the functions

$$
  \array{
    \langle -,-\rangle_i
    &\colon&
    E|_{U_i} \otimes_X E|_{U_i}
      &\overset{ \phi_i^{-1} \otimes_{U_i} \phi_i^{-1} }{\longrightarrow}&
    (U_i \times \mathbb{R}^n ) \otimes_{U_i} (U_i \times \mathbb{R}^n)
      &\overset{\simeq}{\to}&
    U_i \times (\mathbb{R}^n \otimes \mathbb{R}^n)
      &\overset{}{\longrightarrow}&
    U_i \times \mathbb{R}
    \\
    && && &&
    ((x,i),(v_1,v_2))
      & \overset{\phantom{AAA}}{\mapsto} &
    ((x,i), f_i(x) \cdot \langle v_1, v_2\rangle_{\mathbb{R}^n} )
  }
  \,.
$$

extend by zero to continuous functions on all of $E \otimes_X E$, which we denote by the same symbol $\langle -,-\rangle_i \colon E \otimes_X E \to X \times \mathbb{R}$.

We then claim that the sum

$$
  \langle -,-\rangle
    \;\colon\;
  \underset{i \in I}{\sum} \langle -,-\rangle_i
  \;\colon\;
  E \otimes_X E
  \longrightarrow
  X \times \mathbb{R}
$$

is an inner product as required.  Notice that the sum is well defined by [[locally finite cover|local finiteness]] of the supports of the partition functions $f_i$. Hence it is pointwise a finite sum of positive definite symmetic bilinear forms on $E_x$, and as such itself pointwise a positive definite symmetric bilinear form.

=--


## Related concepts

* [[vector bundle]] 
   
  * [[real vector bundle]]

  * [[complex vector bundle]]

    * [[holomorphic vector bundle]], [[pseudoholomorphic vector bundle]]

  * [[universal vector bundle]]

  * [[dual vector bundle]]

  * [[module bundle]]

  * [[direct sum of vector bundles]]

  * [[short exact sequence of vector bundles]]
 
  * [[connection on a vector bundle]]

  * [[flat vector bundle]]

  * [[real vector bundle]], [[complex vector bundle]]

  * [[super vector bundle]]



## References

* Glenys Luke, Alexander S. Mishchenko, _Vector bundles and their applications_, Math. and its Appl. __447__, Kluwer 1998. viii+254 pp. [MR99m:55019](http://www.ams.org/mathscinet-getitem?mr=99m:55019)

Discussion with an eye towards [[topological K-theory]] is in

* [[Max Karoubi]], _K-theory. An introduction_, Grundlehren der Mathematischen Wissenschaften __226__, Springer 1978. xviii+308 pp.

* {#Hatcher} [[Allen Hatcher]], section 1.1 of: _Vector bundles and K-Theory_ ([webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf))


[[!redirects inner products on vector bundles]]

[[!redirects inner products of vector bundles]]

