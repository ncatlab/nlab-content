
<div class="rightHandSide toc" markdown="1">
[[!include (infinity,1)-topos - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In the [[(∞,1)-topos]] [[Top]] to every object -- every [[topological space]] -- $X$ is associated 
the set $\pi_0(X)$ of connected components and the [[homotopy group]]s $\pi_n(X,x)$ for $x \in X$ and $n \in \mathbb{N}$, $n\gt 0$.

By the general logic of [[space]], we may think of the objects in an arbitrary [[∞-stack]] [[(∞,1)-topos]] as generalized spaces of sorts. Accordingly, there is a notion of **homotopy groups of an $\infty$-stack** .

But care has to be taken. It turns out that there are actually _two_ different notions of homotopy groups in an arbitrary $(\infty,1)$-topos, two notions that accidentally coincide for [[Top]]:

* there is a notion of **categorical homotopy group**: 

  every $(\infty,1)$-topos $\mathbf{H}$ is [[power]]ed over [[∞Grpd]] [[model structure on simplicial sets|usually modeled]] as [[SSet]], hence for every object $X \in \mathbf{H}$ there is the **categorical $n$-sphere object** $X^{S^n_c}$, where $S^n_c = \Delta^n/\partial \Delta^n$. 

* there should be a notion of **geometric homotopy group**, induced from the [[monodromy]] of [[locally constant ∞-stack]]s on objects $X \in \mathbf{H}$.

For instance let $\mathbf{H} = Sh_{(\infty,1)}(Diff)$ be the $(\infty,1)$-topos of [[Lie ∞-groupoid]]s. An ordinary smooth [[manifold]] $X$ is represented in $\mathbf{H}$ by a [[sheaf]] of [[set]]s on [[Diff]]. This has no higher nontrivial categorical homotopy groups -- $\pi_{n \gt 0}^{cat}(X) = 0$ -- reflecting the fact regarded as a smooth [[∞-groupoid]], $X$ is a categorically [[discrete groupoid]].

But of course the manifold $X$ may have nontrivial [[homotopy group]]s in terms of its underlying [[topological space]]. For instance if $X = S^1$ is the circle, then the _geometric_ first homotopy group is nontrivial, $\pi_1^{geom}(X) = \mathbb{Z}$.

We discuss below both cases. The case of categorical homotopy groups is fully understood, for the case of geometric homotopy groups at the moment only a few aspects are in the literature, more is in the making. Some authors of this page ([[Urs Schreiber|U.S.]]) thank [[Richard Williamson]] for pointing this out.

## Categorical homotopy groups

See [[categorical homotopy groups in an (∞,1)-topos]].

## Geometric homotopy groups

See [[geometric homotopy groups in an (∞,1)-topos]].


[[!redirects homotopy group of an infinity-stack]]
[[!redirects homotopy group of an ∞-stack]]
[[!redirects homotopy groups of an infinity-stack]]
[[!redirects homotopy groups of an ∞-stack]]
[[!redirects homotopy groups of infinity-stacks]]
[[!redirects homotopy groups of ∞-stacks]]
[[!redirects homotopy group (of an infinity-stack)]]
[[!redirects homotopy group (of an ∞-stack)]]
[[!redirects homotopy groups (of an infinity-stack)]]
[[!redirects homotopy groups (of an ∞-stack)]]
[[!redirects homotopy groups (of infinity-stacks)]]
[[!redirects homotopy groups (of ∞-stacks)]]

[[!redirects fundamental group of an infinity-stack]]
[[!redirects fundamental group of an ∞-stack]]
[[!redirects fundamental groups of infinity-stacks]]
[[!redirects fundamental groups of ∞-stacks]]

[[!redirects homotopy group of an infinity-stack]]

[[!redirects homotopy groups in an (∞,1)-topos]]
[[!redirects homotopy group in an (∞,1)-topos]]
[[!redirects homotopy group in an (infinity,1)-topos]]
