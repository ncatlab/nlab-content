

> Some overlap with [[PU(ℋ)]]. Needs to be disentangled.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #PUH}
###### Definition


For $\mathcal{H}$ a [[Hilbert space]], the _projective unitary group_ $P U(\mathcal{H})$ is the [[quotient]] of the [[unitary group]] $U(\mathcal{H})$ by its [[center]] $Z U(\mathcal{H}) \simeq U(1)$, the [[circle group]]

$$
 P U(\mathcal{H}) \coloneqq U(\mathcal{H})/U(1)
  \,.
$$


=--

This is naturally a [[topological group]]. For $\mathcal{H}$ of finite-[[dimension]] $n$ $P U(n) := P U(\mathcal{H})$ is also naturally a [[Lie group]].


## Properties

### Homotopy type
 {#HomotopyType}

\begin{proposition}\label{KZ2}
If $\mathcal{H}$ is an infinite-[[dimension]]al [[separable Hilbert space]] the underlying [[topological space]] of its projective unitary group has the [[homotopy type]] of an [[Eilenberg-MacLane space]] $K(\mathbb{Z}, 2)$.
\end{proposition}


\begin{proof}
The [[unitary group]] $U(\mathcal{H})$ in this case is [[contractible]] (by [[Kuiper's theorem]]) and the [[circle group]] $U(1)$ [[action|acts]] free and faithfully on it. Therefore the quotient map $U(\mathcal{H}) \to P U(\mathcal{H})$ is a model for the [[circle group]]-[[universal principal bundle]] and in particular the topological space underlying $P U(\mathcal{H})$ is equivalent to the [[classifying space]] $B U(1) \simeq B^2 \mathbb{Z} \simeq K(\mathbb{Z},2)$.
\end{proof}


\begin{proposition}\label{ClassesOfPUHBundles}
For $\mathcal{H}$ an infinite-dimensional separable Hilbert space $P U(\mathcal{H})$-[[principal bundle]]s over a [[topological space]] $X$ are classidied by third [[integral cohomology]] of $X$

$$
  P U(\mathcal{H}) Bund(X) \simeq H^3(X, \mathbb{Z})
  \,.
$$
\end{proposition}

\begin{proof}
By prop. \ref{KZ2} we have that the [[classifying space]] of $P U(\mathcal{H})$ itself is an [[Eilenberg-MacLane space]]

$$
 B P U(\mathcal{H})
  \simeq
  B B U(1)
  \simeq
  B^3 \mathbb{Z}
  \simeq
  K(\mathbb{Z}, 3)
  \,.
$$

This is the classifying space for degree-3 integral cohomology (see [[Eilenberg-MacLane spectrum]] for more on this).
\end{proof}


\begin{prop}\label{ClassesOfPUHBundles}
Every [[circle n-bundle with connection|circle 2-bundle]]/[[bundle gerbe]] on $X$ is equivalent to the [[lifting gerbe]] of some $P U(\mathcal{H})$-principal bundle to a $U(\mathcal{H})$-bundle, and the equivalence classes of these structures correspond uniquely.
\end{prop}

\begin{proof}
The [[twisted bundles]] of a given bundle gerbe are given by the [[twisted cohomology]] relative to the morphism $\mathbf{B} P U(\mathcal{H}) \to \mathbf{B}^2 U(1)$ that is part of the long [[fiber sequence]]

$$
  \mathbf{B} U(1) \to \mathbf{B} U(\mathcal{H}) \to B \mathbf{P} U(\mathcal{H}) \to \mathbf{B}^2 U(1)
  \,.
$$

Since the topological space underlying $U(\mathcal{H})$ is contractible, on the underlying topological spaces this is

$$
  K(\mathbb{Z},2) 
   \to 
  * 
   \to 
  K(\mathbb{Z},3) 
    \stackrel{\simeq}{\to} 
  K(\mathbb{Z}, 3)
  \,.
$$

This means that the morphism that sends $P U(\mathcal{H})$-bundles to the twist that they induce is an isomorphism.
\end{proof}

> (Somebody should force me to say this in more detail).


For more on this see also [[twisted K-theory]].

### Action on Fredholm operators

Let $\mathcal{H}$ be an infinite-dimensional separable Hilbert space.

Since by the above $PU(\mathcal{H}) \simeq B U(1)$ and since there is a canonical action of [[line bundles]] on complex vector bundles, hence on the [[topological K-theory]] of a manifold $X$, there must also be a natural action of $PU(\mathcal{H}) \times Fred \to Fred$ of $PU(\mathcal{H})$ on the space of [[Fredholm operators]] (on connected components).

This is given by letting a projective unitary act by conjugation on a Fredholm operator: $(g, F) \mapsto g F g^{-1}$.

## Related concepts

* [[PU(ℋ)]], [[universal equivariant PU(H)-bundle|universal equivariant $PU(\mathcal{H})$-bundle]]

* [[projective linear group]]

* [[unitary group]]

  * [[special unitary group]], **projective unitary group**

* [[orthogonal group]]

  * [[special orthogonal group]]

  * [[spin group]]

## References

On the [[cohomology]] of the [[classifying spaces]] $B PU(n)$:

* Xing Gu, _On the Cohomology of the Classifying Spaces of Projective Unitary Groups_,  Journal of Topology and AnalysisVol. **13** 02 (2021)  535-573 ([arXiv:1612.00506](https://arxiv.org/abs/1612.00506), [doi:10.1142/S1793525320500211](https://doi.org/10.1142/S1793525320500211))

On the spaces of [[group homomorphisms]] into $PU(\mathcal{H})$ (with an eye towards the [[universal equivariant PU(H)-bundle|universal equivariant $PU(\mathcal{H})$-bundle]]):

* {#BEJU14} [[Noé Bárcenas Torres|Noé Bárcenas]], [[Jesús Francisco Espinoza Fierro|Jesús Espinoza]], [[Michael Joachim]], [[Bernardo Uribe]], Section 1 of: _Universal twist in Equivariant K-theory for proper and discrete actions_, Proceedings of the London Mathematical Society, Volume 108, Issue 5 (2014) ([arXiv:1202.1880](https://arxiv.org/abs/1202.1880), [doi:10.1112/plms/pdt061](https://doi.org/10.1112/plms/pdt061))


[[!redirects projective unitary groups]]

[[!redirects PU(n)]]




