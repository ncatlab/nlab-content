
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

In [[topology]], the notion of *properness* is that of [[compact topological space|compactness]], but generalized from [[topological spaces]] to [[continuous functions]] between them.

A continuous map $X \to Y$ is proper when “$X$ is compact, relative to $Y$”.

## Definitions

There are three inequivalent definitions of a proper map in the literature.

The first one is the oldest definition, still found in some analysis books.

\begin{definition}
A continuous map $f\colon X\to Y$ of [[topological spaces]] is __proper__ (or __quasi-proper__) if for every [[compact]] subset $K\subset Y$, the preimage $f^{-1}K$ is a compact subset of $X$.
\end{definition}

The second definition was introduced by [[Bourbaki]] to make proper maps closed under [[base changes]].

\begin{definition}
A continuous map $f\colon X\to Y$ of [[topological spaces]] is __proper__ if it is __universally closed__: every [[base change]] of $f$ is a [[closed map]] of topological spaces.
\end{definition}

Other equivalent characterizations include the following:

* For every [[topological space]] $Z$ the map $f\times id_Z\colon X\times Z\to Y\times Z$ is a [[closed map]].  (The original formulation used by Bourbaki.)

* The map $f$ is quasi-proper and closed.

* The map $f$ is closed and every fiber of $f$ is [[compact]].

The third definition was introduced by [[Grothendieck]].  It is in the same relation to the previous definition as [[compact Hausdorff spaces]] are to [[compact spaces]].

\begin{definition}
A continuous map $f\colon X\to Y$ of [[topological spaces]] is __proper__ if it is universally closed and [[separated map|separated]].
\end{definition}

Recall that $f$ is [[separated map|separated]] if its relative diagonal $X\to X\times_Y X$ is a [[closed map]].

If $Y=\{*\}$ is the terminal [[topological space]], then the first two definitions amount to saying $X$ is [[compact]], whereas the last definition makes $X$ compact and [[Hausdorff]].

## Definition

Just like there are various equivalent ways of characterizing [[compact topological spaces]], there are also various equivalent ways of characterizing proper functions.

In the following we discuss:

* [characterization via nets](#UsingNets);

* [characterization via intersection of closed sets](#UsingClosedSets);

* [characterization via closedness](#UsingClosedness);

* [characterization as a continuous family of compact fibres](#AsAContinousFamilyOfCompactSpaces);

* [further characterizations](#FurtherCharacterizations).

### Via nets
 {#UsingNets}

Recall that for a [[topological space]] $X$ to be [[compact topological space|compact]] means for every [[ net ]] $x_\bullet$ in $X$ to have a [[cluster point]] in $X$; hence for every net to admits a [[convergence of a net|convergent]] subnet.

A generalisation of this characterisation to a [[continuous map]] $f \colon X \to Y$ is the following:

\begin{definition}
\label{PropernessViaNets}

A [[continuous map]] $f \,\colon\, X \to Y$ is *proper* iff for every [[net]] $x_\bullet$ in $X$ and for every [[cluster point]] $y$ of $f(x_\bullet)$ in $Y$, the net $x_\bullet$ has a [[cluster point]] $x \in X$ with $f(x) = y$.

Equivalently:

Such $f$ is proper iff for every net $x_\bullet \in X$ and every $y \in Y$, if $f(x_\bullet)$ [[convergence of a net|converges]] to $y$ then $x_\bullet$ admits a subnet [[convergence of a net|converging]] to $x \in X$ with $f(x) = y$.

\end{definition}

### Via intersection of closed sets
 {#UsingClosedSets}

Recall that, equivalently, a [[topological space]] $X$ is [[compact topological space|compact]] if and only if for every cofiltered set of non-empty closed subsets $F_i \subset X$, their intersection $\cap_i F_i$ is also non-empty.

\begin{definition}
\label{PropernessViaClosedSets}

A [[continuous map]]  $f \,\colon\, X \to Y$  is *proper* iff

1. $f$ is closed;

1. for every cofiltered set of closed subsets $\{F_i\}_{i \in I}$ of $X$, one has

$$
  f(\cap_{i \in I} F_i) = \cap_{i \in I}f(F_i)
$$

\end{definition}

### Via closedness
 {#UsingClosedness}


Recall that, equivalently, a [[topological space]] $X$ is [[compact topological space|compact]] if and only if the [[projection map]] 

$$
  X \times Z \longrightarrow Z
$$

out of the [[product topological space]] with some $Z$
is a [[closed map]], for every [[topological space]] $Z$.

\begin{definition}
\label{PropernessViaClosedness}

A [[continuous map]]  $f \,\colon\, X \to Y$  is *proper* iff its image under the [[Cartesian product]]-[[functor]]

$$ 
  f \times \mathrm{Id}_Z 
   \;\colon\; 
  X \times Z 
   \;\longrightarrow\; 
  Y \times Z
$$

is a [[closed map]] for every [[topological space]] $Z$.

\end{definition}

### As a continuous family of compact spaces
 {#AsAContinousFamilyOfCompactSpaces}

With every function $f \colon X \to Y$, the space $X$ can be described as the union of the fibres $f^{-1}(y)$ with $y \in Y$. The map $f$ is proper when each fibre is compact and the family is continuous in the sense that: for every net $y_\bullet$ converging to $y \in Y$, we ask that the net of sets $f^{-1}(y_\bullet)$ converges to $f^{-1}(y)$. This is equivalent to ask that $f$ be closed.

\begin{definition}
\label{PropernessAsAContinuousFamilyOfCompactFibres}

A [[continuous map]]  $f \,\colon\, X \to Y$  is *proper* if:

1. $f^{-1}(\{y\})$ is compact for every $y \in Y$;

1. $f$ is closed.

\end{definition}

### Further characterizations
 {#FurtherCharacterizations}

\begin{proposition}
\label{EquivalenceOfCharacterization}
Given a [[continuous map]] $f \colon X \to Y$, the following properties are all equivalent:

1. (Def. \ref{PropernessViaNets}) 

   For every [[net]] $x_\bullet$ in $X$ and every [[cluster point]] $y$ of $f(x_\bullet)$, the net $x_\bullet$ admits a cluster point $x$ with $f(x) = y$;

1. If $\mathcal{F}$ is a [[filter]] on $X$ and if $y$ is a [[cluster point]] of $f(\mathcal{F})$, then $\mathcal{F}$ has a cluster point $x \in X$ with $f(x) = y$;

1. (Def. \ref{PropernessViaClosedSets}) 

   $f$ is a [[closed map]] and for every cofiltered family $\{F_i\}_{i \in I}$ of
closed subsets of $X$, one has $f(\cap_{i \in I} F_i) = \cap_{i \in I}f(F_i)$;

1. (Def. \ref{PropernessViaClosedness}) 

   The image $f \times \mathrm{Id}_Z \,\colon\, X \times Z \to Y \times Z$ under the [[Cartesian product]]-[[functor]] is a [[closed map]] for every topological space $Z$;


1. ([[universally closed morphism|universally closed]]) 
   
   For every [[continuous map]] $g \colon Z \to Y$, the resulting [[pullback]] map

   \[
      g^\ast(f) 
        \;\colon\; 
      X \times_Y Z \to Z
   \]

   is a [[closed map]];

1. (Def. \ref{PropernessAsAContinuousFamilyOfCompactFibres})

   $f$ is a [[closed map]] and the [[inverse image]] $f^{-1}\big(\{y\}\big)$ of every $y \in Y$ is [[compact topological space|compact]];

1. $f$ is a [[closed map]] and the [[inverse image]] $f^{-1}(K)$ of every [[compact subspace]] $K \subset Y$ is [[compact topological space|compact]].

\end{proposition}

(cf. [Bourbaki 1971](#Bourbaki71): Thm. 1 on p. 1 with Def. 1 on p. 97)

\begin{definition}
\label{ProperContinuous}
**([[proper maps]])**
\linebreak
A [[continuous function]] $f  \colon X \to Y$
is called _[[proper map|proper]]_ if it satisfies one of the equivalent properties listed in Prop. \ref{EquivalenceOfCharacterization}.

\end{definition}


\begin{remark} 
**(Ambiguous terminology)**
\linebreak
The notion of compact space is subject to naming ambiguity. For the same notion, some authors will use the term _quasi-compact_, using _compact_ only when the space is also separated.

For _properness_ the situation is _worse_ as there are three competing definitions. We have defined the one similar to _quasi-compact_ spaces.

In addition one could require $f$ to be [[separated map|separated]], that is to require that if a net $x_\bullet$ converges to both $x_1$ and $x_2$ with $f(x_1) = f(x_2)$, then $x_1 = x_2$. This definition of properness resembles the one used in algebraic geometry: see [[ proper morphism ]]. It is also the one to be used in the proper base change theorem.

Finally, some authors use a weaker version of properness, where $f \colon X \to Y$ is proper when $f^{-1}(K)$ is compact for every compact $K \subset Y$. But as explained below, this definition is usually used in situations where these maps are always closed.
\end{remark} 

## Further criteria

A continuous map $f \colon X \to Y$ such that $f^{-1}(K)$ is compact for every compact $K \subset Y$ may not be closed; even when both $X$ and $Y$ are very nice spaces like $\mathbf{T}_5$ spaces.

\begin{example}
Let $X$ be an uncountable set and let $p \in X$. Let's still write $X$ for the discrete topological space associated to it. Let $X_p$ denote the topological space whose underlying set is $X$ but whose opens sets are either all the sets not containing $p$ or the sets containing $p$ with countable complement in $X$.

Then $X_p$ is a $\mathbf{T}_5$ topological space and its compact subsets are all finite.
But the identity map
$$ X \longrightarrow X_p$$
 is not closed.
\end{example}

However this is very often the case in practice: for example when $Y$ is a metric space or a locally compact separated space.

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


Proper maps enjoy analogous properties as [[compact topological spaces]] do, for example the product of proper maps is again proper:

\begin{theorem}
Let $\{f_i \colon X_i \to Y_i\}_{i \in I}$ be a small [[indexed family]] of continuous proper maps (Def. \ref{ProperContinuous}), then their [[functor|functorial]] [[product topological space|product]]

$$
  \prod_{i \in I} \,f_i 
    \;\colon\; 
  \prod_{i \in I} \, X_i 
  \longrightarrow 
  \prod_{i \in I} Y_i
$$
is also a proper map.
\end{theorem}

Further properties:

* [[proper maps to locally compact spaces are closed]]


## Comparison with proper maps of locales

\begin{proposition}
Every proper map $f\,:\, X \to Y$ between two topological spaces induces a
proper map $\mathrm{Loc}(f)\,:\, \mathrm{Loc}(X) \to \mathrm{Loc}(Y)$ between the associated locales.

Conversely, if $\mathrm{Loc}(f)\,:\, \mathrm{Loc}(X) \to \mathrm{Loc}(Y)$ is proper and $Y$ is a $\mathrm{T}_\mathrm{D}$-space, then $f\,:\, X \to Y$ is proper.
\end{proposition}

## Related concepts

* [[locally proper map]]

* [[proper morphism]]

* [[open map]], [[closed map]]

* [[proper group action]]

* [[proper homotopy]]

* [[proper equivariant homotopy theory]]

## References

All three definitions are presented in

* [[Stacks Project]], Tag 005M, <https://stacks.math.columbia.edu/tag/005M>.

One of the early reference on proper maps is

* [[Nicolas Bourbaki]], _Topologie Générale_ (Éléments de Mathématique, Livre III), Chapitres 1 à 2.  Second Edition, 1951.  Actualites Sci. Ind. 1142, Hermann, Paris.

A considerable expanded treatment is given in the third edition, see Chapter I, Section 10:

* [[Nicolas Bourbaki]], _Topologie Générale_ (Éléments de Mathématique, Livre III), Chapitres 1 à 2.  Third Edition, 1961.  Actualites Sci. Ind. 1142, Hermann, Paris.

English translation of the 1971 edition:

* {#Bourbaki71} [[Nicolas Bourbaki]], *General topology*, Elements of Mathematics III, Springer (1971, 1990, 1995) &lbrack;[doi:10.1007/978-3-642-61701-0](https://doi.org/10.1007/978-3-642-61701-0)&rbrack;


{#LocaliVersionReferences} The [[locale|localic]] version of proper maps was introduced in:

* [[Peter Johnstone]], §1 of: _The Gleason cover of a topos, II_, Journal of Pure and Applied Algebra **22** 3 (1981) 229–247 &lbrack;<a href="http://dx.doi.org/10.1016/0022-4049(81)90100-6">doi:10.1016/0022-4049(81)90100-6</a>&rbrack;

where it is attributed to this "preliminary" (and apparently unpublished) account:

* [[Peter Johnstone]], _Factorization and pullback theorems for localic geometric morphisms_, Univ. Cath. de Louvain, Sem. de math, pure, Rapport no. 79 (1979)



[[!redirects proper maps]]
[[!redirects proper continuous map]]
[[!redirects proper continuous maps]]

[[!redirects proper continuous function]]
[[!redirects proper continuous functions]]