
> This entry is about the concept in  [[topology]]. For variants see at _[[proper morphism]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Properness is compactness, but for continuous functions.
Compactness for topological spaces can described in multiple ways; the same applies to properness. Let us see two lines of intuition for the definition of proper maps, following two equivalent definitions of compact spaces.

### Using nets

A topological space $X$ is compact when every [[ net ]] $x_\bullet$ has a cluster point in $X$. Equivalently, it is compact when every net admits a convergent subnet.

A generalisation of this characterisation to a continuous map $f \colon X \to Y$ would then be:

$f$ is proper when for every net $x_\bullet$ in $X$ and for every cluster point $y$ of $f(x_\bullet)$, $x_\bullet$ has a cluster point $x \in X$ with $f(x) = y$.

Or equivalently, $f$ is proper when for every net $x_\bullet \in X$ and every $y \in Y$, if $f(x_\bullet)$ converges to $y$ then $x_\bullet$ admits a subnet converging to $x \in X$ with $f(x) = y$.

### Using closeness

A topological space $X$ is compact if and only if the projection map
$$X \times Z \longrightarrow Z$$
is closed for every topological space $Z$.

Then one can extend this property by defining a proper map $f \colon X \to Y$ to be a continuous map such that
$$ f \times \mathrm{Id}_Z \colon X \times Z \longrightarrow Y \times Z$$
is closed for every topological space $Z$.

## Definitions

\begin{theorem}
Given a continuous function $f \colon X \to Y$, the following properties are
equivalent:

1. For every net $x_\bullet$ in $X$ and every cluster point $y$ of $f(x_\bullet)$, $x_\bullet$ admits a cluster point $x$ with $f(x) = y$;

1. If $\mathcal{F}$ is a [[ filter ]] on $X$ and if $y$ is a cluster point of $f(\mathcal{F})$, then $\mathcal{F}$ has a cluster point $x \in X$ with $f(x) = y$;

1. $f \times \mathrm{Id}_Z \colon X \times Z \to Y \times Z$ is closed for every topological space $Z$;

1. __([[ universally closed morphism | universally closed ]])__ For every continuous map $g \colon Z \to Y$, the resulting pullback map
\[g^\ast(f) \colon X \times_Y Z \to Z\]
is closed;

1. $f$ is closed and $f^{-1}(y)$ is compact for every $y \in Y$;

1. $f$ is closed and $f^{-1}(K)$ is compact for every compact $K \subset Y$.

\end{theorem}



+-- {: .num_defn #ProperContinuous}
###### Definition
**([[proper maps]])**

A [[continuous function]] $f  \colon X \to Y$
is called _[[proper map|proper]]_ if it satisfies one of the equivalent properties listed above.

=--

\begin{remark} __(Ambiguous terminology)__
The notion of compact space is subject to naming ambiguity. For the same notion, some authors will use the term _quasi-compact_, using _compact_ only when the space is also separated.

For _properness_ the situation is _worse_ as there are three competing definitions. We have defined the one similar to _quasi-compact_ spaces.

In addition one could require $f$ to be separated, that is to require that if a net $x_\bullet$ converges to both $x_1$ and $x_2$ with $f(x_1) = f(x_2)$, then $x_1 = x_2$. This definition of properness ressembles the one used in algebraic geometry: see [[ proper morphism ]]. It is also the one to be used in the proper base change theorem.

Finally, some authors use a weaker version of properness, where $f \colon X \to Y$ is proper when $f^{-1}(K)$ is compact for every compact $K \subset Y$. But as explained below, this definition is usually used in situations where these maps are always closed.
\end{remark} 

## Criterions for properness

A continuous map $f \colon X \to Y$ such that $f^{-1}(K)$ is compact for every compact $K \subset Y$ may not be closed. However this is very often the case in practice: for example when $Y$ is a metric space or a locally compact separated space.

\begin{proposition}
Let $f \colon X \to Y$ be a continuous map such that

1. $f^{-1}(K)$ is compact for every compact $K \subset Y$;

1. $Y$ is a [[ compactly generated topological space | $k$-space ]]

then $f$ is closed and thus proper.
\end{proposition}

Also,

+-- {: .num_prop #MapsFromCompactSpacesToHausdorffSpacesAreClosed}
###### Proposition
**(maps from compact spaces to separated spaces are proper)**

Let $f \colon X \longrightarrow Y$ be a [[continuous function]] between [[topological spaces]] such that

1. $X$ is [[compact topological space|compact]];

1. $Y$ is [[Hausdorff topological space | separated]],

then $f$ is proper.

=--

## Properties

Proper maps enjoy similar properties as compact spaces do, for example their product is proper.

\begin{theorem}
Let $\{f_i \colon X_i \to Y_i\}_{i \in I}$ be a small family of continuous proper maps, then their product
$$
\prod_{i \in I}f_i \colon \prod_{i \in I} X_i \longrightarrow \prod_{i \in I} Y_i
$$
is proper.
\end{theorem}


## Related concepts

* [[locally proper map]]

* [[proper morphism]]

* [[open map]], [[closed map]]

* [[proper group action]]

* [[proper homotopy]]

* [[proper equivariant homotopy theory]]

[[!redirects proper maps]]
[[!redirects proper continuous map]]
[[!redirects proper continuous maps]]

[[!redirects proper continuous function]]
[[!redirects proper continuous functions]]

