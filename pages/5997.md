
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The $n$-connected/$n$-truncated factorization system is an [[orthogonal factorization system in an (∞,1)-category]],  specifically in an [[(∞,1)-topos]], that generalizes the _relative [[Postnikov systems]]_ of [[∞Grpd]]: it factors any morphism through its _[[n-image|(n+2)-image]]_ by an _[[n-epimorphism|(n+2)-epimorphism]]_ followed by an _[[n-monomorphism|(n+2)-monomorphism]]_.

As $n$ ranges through $(-1), 0, 1, 2, 3, \cdots$ these factorization systems form an [[k-ary factorization system|∞-ary factorization system]].

## Definitions

+-- {: .num_prop}
###### Proposition

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. For all $(-2) \leq n \leq \infty$ the [[class]] of [[n-truncated morphisms in an infinity,1-category|n-truncated morphisms]]  in $\mathbf{H}$ forms the right class in a [[orthogonal factorization system in an (∞,1)-category]]. The left class is that of [[n-truncated morphisms in an infinity,1-category|n-connected morphisms]]  in $\mathbf{H}$.

=--

This appears as a remark in [[Higher Topos Theory|HTT, Example 5.2.8.16]]. A construction of the factorization in terms of a [[model category]] [[presentable (∞,1)-category|presentation]] is in ([Rezk, prop. 8.5](#Rezk)). 

+-- {: .num_remark}
###### Remark

For $n = -1$ this says that [[effective epimorphisms in an (∞,1)-category]] have the [[left lifting property]] against [[monomorphisms in an (∞,1)-category]]. Therefore one may say that the effective epimorphisms in an $(\infty,1)$-topos are the [[strong epimorphisms]].

=--

## Properties

### Stability

\begin{prop}\label{nConnectedTruncatedIsStable}
For all $n$, the $n$-connected/$n$-truncated factorization system is [[stable factorization system|stable]]: the class of [[n-connected]] morphisms is preserved under [[(∞,1)-pullback]].

\end{prop}

This appears as ([Lurie, prop. 6.5.1.16(6)](#Lurie)).

It follows that:
\begin{prop}\label{HomotopyPullbackPreservesNImageFactorization}
For all $n$, [[n-images]] are preserved by [[(∞,1)-pullback]]
\end{prop}
\begin{proof}
Let $X \xrightarrow{f} Y$ with $n$-image $im_n(f)$.
By the [[pasting law]] its [[(infinity,1)-pullback|$\infty$-pullback]] along any $g \,\colon\, X' \xrightarrow{\;} X$ may be decomposed as two consecutive $\infty$-pullbacks:

\begin{tikzcd}
  g^\ast X
  \ar[r]
  \ar[d]
  \ar[dr, phantom, "{\mbox{\tiny(pb)}}"]
  \ar[
    dd,
    bend right=50,
    "{g^\ast f}"{swap}
  ]
  &
  X
  \ar[d, "{\mbox{\tiny $n$-cnct}}"{description}]
  \ar[
    dd,
    bend left=50,
    "{f}"
  ]
  \\
  \mathrm{im}_n(g^\ast f)
  \ar[r]
  \ar[d]
  \ar[dr, phantom, "{\mbox{\tiny(pb)}}"]
  &
  \mathrm{im}_n(f)
  \ar[d, "{\mbox{\tiny $n$-trnct}}"{description}]
  \\
  Y'
  \ar[
    r,
    "g"{swap} 
  ]
  &
  Y
\end{tikzcd}

Here the pullback of the $n$-truncated map in again $n$-truncated since the right class of any orthogonal factorization system is stable under pullback. The analogous statement holds also for the $n$-connected map by Prop. \ref{nConnectedTruncatedIsStable}. Therefore the pullback of $im_n(f)$ along $g$ is indeed $im_n(g^\ast f)$, as shown.

\end{proof}


## Examples

### The case $n = -2$

A [[(-2)-truncated]] [[morphism]] is precisely an [[equivalence in an (∞,1)-category]] (see there or [[Higher Topos Theory|HTT, example 5.5.6.13]]).

Moreover, every morphism is [[(-2)-connected]]. 

Therefore for $n = -2$ the $n$-connected/$n$-truncated factorization system says (only) that equivalences have inverses, unique up to coherent homotopy.

### The case $n = -1$

A [[(-1)-truncated]] morphism is precisely a [[monomorphism in an (∞,1)-category|full and faithful morphism]].

A [[(-1)-connected]] morphism is one whose [[homotopy fiber]]s are [[inhabited]].

In [[∞Grpd]] a morphism between _[[0-truncated]]_ [[object]]s ([[set]]s) 

* is full and faithful precisely if it is an [[injection]];

* has non-empty fibers precisely if it is an [[epimorphism]].

Therefore between 0-truncated objects the (-1)-connected/(-1)-truncated factorization system is the [[epi/mono factorization system]] and hence [[image]] factorization.

Generally, the (-1)-connected/(-1)-truncated factorization is through the **$\infty$-categorical [[1-image]]**, the _[[homotopy image]]_ (see there for more details).


### The case $n = 0$

Let $X,Y$ be two [[groupoid]]s ([[homotopy n-type|homotopy 1-types]]) in [[∞Grpd]]. 

A morphism $X \to Y$ is [[0-truncated]] precisely if it is a [[faithful functor]]. 

A morphism $X \to Y$ is [[0-connected]] precisely if it is a [[full functor]] and an [[essentially surjective functor]]: a [[essentially surjective and full functor]]

Therefore on homotopy 1-types the 0-connected/0-truncated factorization system is the [[(eso+full, faithful) factorization system]].

## References

The general abstract statement is in 

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_
 

A [[model category]]-theoretic discussion is in section 8 of

* {#Rezk} [[Charles Rezk]], _Toposes and homotopy toposes_ ([pdf](http://www.math.uiuc.edu/~rezk/homotopy-topos-sketch.pdf))
 

Discussion in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], section 7.6 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_


[[!redirects n-connected/n-truncated factorization system]]
[[!redirects (n-connected, n-truncated) factorization system]]

[[!redirects (n-epi, n-mono) factorization system]]
[[!redirects (n-epi, n-mono) factorization systems]]

