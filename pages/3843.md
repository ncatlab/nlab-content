
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

### Raising the index of accessibility

If $\lambda\le\kappa$, then every $\kappa$-filtered colimit is also $\lambda$-filtered, and thus if $F$ preserves $\lambda$-filtered colimits then it also preserves $\kappa$-filtered ones.  Therefore, if $F$ is $\lambda$-accessible and $C$ and $D$ are $\kappa$-accessible, then $F$ is $\kappa$-accessible.  Two conditions under which this happens are:

1. $C$ and $D$ are [[locally presentable categories]].

2. $\lambda$ is [[sharply smaller cardinal|sharply smaller]] than $\kappa$, i.e. $\lambda\lhd\kappa$.

In particular, for any accessible functor $F$ there are arbitrarily large cardinals $\kappa$ such that $F$ is $\kappa$-accessible, and if the domain and codomain of $F$ are locally presentable then $F$ is $\kappa$-accessible for all sufficiently large $\kappa$.

### Preserving presentable objects

For any accessible functor $F$, there are arbitrarily large cardinals $\kappa$ such that $F$ is $\kappa$-accessible and preserves $\kappa$-[[presentable objects]].  Indeed, this can be achieved simultaneously for any set of accessible functors.  See [Adamek-Rosicky, Theorem 2.19](#AdamekRosicky).

### Images of accessible functors

\begin{theorem}
Assuming the existence of a [[proper class]] of [[strongly compact cardinals]],
the following are equivalent for the image $K$ of an accessible functor:

* $K$ is [[complete]];
* $K$ is [[cocomplete]];
* $K$ is [[locally presentable]].

\end{theorem}


## Related concepts


* [[accessible (∞,1)-functor]].

* [[accessible monad]]



## References

The theory of accessible 1-categories is described in 

* [[Michael Makkai]], [[Robert Paré]], _Accessible categories: The foundations of categorical model theory_ Contemporary Mathematics 104. American Mathematical Society, Rhode Island, 1989. 
{#MakkaiPare}

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AdamekRosicky}

Images of accessible functors are considered in

* [[Jiří Rosický]], _More on directed colimits of models_.

The theory of accessible $(\infty,1)$-categories is the topic of section 5.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects accessible functors]]
