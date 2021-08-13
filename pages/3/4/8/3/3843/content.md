
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A [[functor]]
$$
  F\colon C\to D
$$ 
is a **$\kappa$-accessible functor** (for $\kappa$ a [[regular cardinal]]) if $C$ and $D$ are both $\kappa$-[[accessible categories]] and $F$ preserves $\kappa$-[[filtered colimit]]s.  $F$ is an **accessible functor** if it is $\kappa$-accessible for some regular cardinal $\kappa$.

## Properties

It is immediate from the definition that accessible functors are closed under composition.

### Raising the index of accessibility

If $\lambda\le\kappa$, then every $\kappa$-filtered colimit is also $\lambda$-filtered, and thus if $F$ preserves $\lambda$-filtered colimits then it also preserves $\kappa$-filtered ones.  Therefore, if $F$ is $\lambda$-accessible and $C$ and $D$ are $\kappa$-accessible, then $F$ is $\kappa$-accessible.  Two conditions under which this happens are:

1. $C$ and $D$ are [[locally presentable categories]].

2. $\lambda$ is [[sharply smaller cardinal|sharply smaller]] than $\kappa$, i.e. $\lambda\lhd\kappa$.

In particular, for any accessible functor $F$ there are arbitrarily large cardinals $\kappa$ such that $F$ is $\kappa$-accessible, and if the domain and codomain of $F$ are locally presentable then $F$ is $\kappa$-accessible for all sufficiently large $\kappa$.

### Preserving presentable objects

For any accessible functor $F$, there are arbitrarily large cardinals $\kappa$ such that $F$ is $\kappa$-accessible and preserves $\kappa$-[[presentable objects]].  Indeed, this can be achieved simultaneously for any set of accessible functors.  See [Adamek-Rosicky, Theorem 2.19](#AdamekRosicky).

### Essential images of accessible functors

\begin{theorem}
Assuming the existence of a [[proper class]] of [[strongly compact cardinals]],
the following are equivalent for the [[essential image]] $K$ of an accessible functor:

* $K$ is [[complete]];
* $K$ is [[cocomplete]];
* $K$ is [[locally presentable]].

\end{theorem}

\begin{theorem}
Assuming the existence of a [[proper class]] of [[strongly compact cardinals]],
the closure of the image of an accessible functor under passage to subobjects is an accessible subcategory.
\end{theorem}

The existence of a [[proper class]] of [[strongly compact cardinals]]
can be weakened, see the paper of [Brooke-Taylor and Rosický](#BrookeTaylorRosicky).

## Examples

\begin{example}\label{AdjointsAreAccecible}
Given [[locally presentable categories]] $C$ and $D$ and a [[functor]] $F\colon C\to D$, if $F$ has a [[left adjoint|left]] or [[right adjoint]], then it is an accessible functor.
\end{example}

\begin{example}
By Example \ref{AdjointsAreAccecible} it follows that [[polynomial endofunctors]] of [[Set|$Set$]] are accessible, as they are [[composition|composites]] of [[adjoint functors]].
\end{example}


## Related concepts


* [[accessible (∞,1)-functor]].

* [[accessible monad]]



## References

The theory of accessible 1-categories is described in 

* [[Michael Makkai]], [[Robert Paré]], _Accessible categories: The foundations of categorical model theory_ Contemporary Mathematics 104. American Mathematical Society, Rhode Island, 1989. 
{#MakkaiPare}

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AdamekRosicky}

Essential images of accessible functors are considered in

* [[Jiří Rosický]], _More on directed colimits of models_, Applied Categorical Structures volume 2 (1994) pages 71–76, doi:[10.1007/BF00878503](https://doi.org/10.1007/BF00878503)

An improvement of Rosický's result is in

* {#BrookeTaylorRosicky} Andrew Brooke-Taylor, [[Jiří Rosický]], _Accessible images revisited_ ([arXiv:1506.01986](https://arxiv.org/abs/1506.01986)).

The theory of accessible $(\infty,1)$-categories is the topic of section 5.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects accessible functors]]
