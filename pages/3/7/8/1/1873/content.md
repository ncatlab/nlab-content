#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $G$ a [[Lie group]], its [[delooping]] $\mathbf{B}G$ is a smooth [[groupoid]], which we may think of as a [[groupoid]] [[internal category|internal to]] [[smooth spaces]].

According to the theory of [[models for ∞-stack (∞,1)-toposes]] this is to be thought of as modeling the corresponding [[smooth ∞-stack]] $G Bund(-)$ of smooth $G$-[[principal bundles]] obtained after [[∞-stackification]].

The [[cohomology]] with coefficients in $\mathbf{B}G$ is degree 1 smooth [[nonabelian cohomology]].

Let $g := Lie(G)$ be the [[Lie algebra]] of $G$.

The _groupoid of $g$-valued differential forms_ , denoted here $\bar \mathbf{B}G$, is the refinement of $\mathbf{B}G$ in [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].


## Definition 

+-- {: .un_defn}
###### Definition

For $G$ a [[Lie group]] the **groupoid of $Lie(G)$-valued differential forms** is as a [[groupoid]] [[internal category|internal to]] [[smooth spaces]], the [[sheaf]] of groupoids
$$
  \bar \mathbf{B}G := [P_1(-), \mathbf{B}G]
$$
that to a smooth test space $U \in Diff$ assigns the [[functor category]] $[P_1(U),\mathbf{B}G]$ of smooth functors (functors internal to [[smooth spaces]]) from the [[path groupoid]] $P_1(U)$ of $U$ to the one-object [[delooping]] groupoid $\mathbf{B}G$.
=--

+-- {: .un_theorem}
###### Theorem

The groupoid $\bar \mathbf{B}G$ is canonically equivalent to the smooth groupoid where
* objects are smooth $g$-valued 1-forms $A \in \Omega^1(U, g)$;
* morphisms $h : A \to A'$ are given by smooth $G$-valued functions $h \in C^\infty(U,G)$ such that
  $$
    A' = Ad_h(A) - h^* \bar \theta
  $$

Here $\bar \theta$ is the right invariant canonical $g$-valued 1-form on $G$. A more sloppy but common way to write this is   $A' = Ad_h(A) + h d h^{-1}$.
=--


## Differential nonabelian cohomology 

+-- {: .un_theorem}
###### Theorem

The [[cohomology]] with coefficients in $\bar \mathbf{B}G$ classifies $G$-[[principal bundles]] [[connection on a bundle]] with connection.

More is true: there is a natural canonical equivalence of groupoids
$$
  \mathbf{H}_{Diff}(X, \bar \mathbf{B}G)
  \simeq
  G Bund_\nabla(X)
  \,.
$$
=--


## Remarks 

* There is the obvious projection
  $$
    \bar \mathbf{B}G \to \mathbf{B}G
    \,.
  $$

* Lifting a $G$-cocycle through this projection to a differential $G$-cocycle means equipping it with a [[connection on a bundle|connection]].

For $G = U(n)$ these differential cocycles model the [[Yang-Mills field]] in physics.

* For $G = U(1)$ the sheaf $\bar \mathbf{B}U(1)(-)$ coincides with the the [[Deligne cohomology|Deligne complex]] in degree 2, $\bar \mathbf{B}U(1)\simeq \mathbb{Z}(2)_D^\infty$, as described there. 

  * This corresponds to the [[electromagnetic field]].


## References

The idea goes back to [[John Baez]]. For a detailed history see the discussion at [[schreiber:Differential Nonabelian Cohomology]].

The details are in

* U. Schreiber, Konrad Waldorf, _Parallel Transport and Functors_ ([arXiv](http://arxiv.org/abs/0705.0452))


The definition in terms of differential forms is def 4.6 there. The equivalence to $[P_1(-), \mathbf{B}G]$ is proposition 4.7.


[[Note on Formatting|?]]