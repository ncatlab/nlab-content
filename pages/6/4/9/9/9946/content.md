


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Semicontinuous maps
* table of contents
{: toc}

## Idea

Recall that a (say [[real number|real]]-valued) [[function]] $f$ is [[continuous map|continuous]] at a [[point]] $x$ if, roughly speaking, $f(x) \approx f(y)$ (meaning that $f(x)$ is close to $f(y)$) whenever $x \approx y$.  For a _lower_ semicontinuous map, we require only $f(x) \lesssim f(y)$ (meaning that $f(x)$ is close to or less than $f(y)$); for an _upper_ semicontinuous map, we require only $f(x) \gtrsim f(y)$.


## Definitions

Let $X$ be a [[topological space]], let $R$ be a [[linearly ordered set]], and let $f$ be a [[function]] from $X$ to $R$.

In [[nonstandard analysis]], the vague idea above becomes a precise definition, so long as we use the appropriate [[quantification|quantifiers]] for $x$ and $y$.
+-- {: .num_defn #nonstandard}
###### Definition

The function $f$ is __lower semicontinuous__ if, for each [[standard point]] $x$ of $X$ and each [[hyperpoint]] $y$ in the [[infinitesimal neighbourhood]] of $x$, $f(y)$ is either greater than or in the infinitesimal neighbourhood of $f(x)$.  Similarly, $f$ is __upper semicontinuous__ if, for each standard point $x$ of $X$ and each hyperpoint $y$ in the [[infinitesimal neighbourhood]] of $x$, $f(y)$ is either less than or in the infinitesimal neighbourhood of $f(x)$.
=--

In [[classical analysis]], we must phrase this another way:
+-- {: .num_defn #standard}
###### Definition

The function $f$ is __lower semicontinuous__ if, for each [[point]] $x$ of $X$ and each $a \lt f(x)$ in $R$, there is some [[neighbourhood]] $U$ of $x$ such that, for each $y \in U$, $f(y) \gt a$.  Similarly, $f$ is __upper semicontinuous__ if, for each point $x$ of $X$ and each $b \gt f(x)$ in $L$, there is some neighbourhood $U$ of $x$ such that, for each $y \in U$, $f(y) \lt b$.
=--

We can also refer to an appropriate [[topological structure]] on $R$:
+-- {: .num_defn #continuous}
###### Definition

The function $f$ is __lower semicontinuous__ if it is [[continuous function|continuous]] from $X$ to $R$ with the [[semicontinuous topology|lower semicontinuous topology]].  Similarly, $f$ is __upper semicontinuous__ if it is continuous from $X$ to $R$ with the [[semicontinuous topology|upper semicontinuous topology]].
=--
Of course, this doesn\'t really say anything if you don\'t know what those topologies on $R$ are, and the easiest way to figure that out is to refer to Definition \ref{standard} (or to Definition \ref{nonstandard} if you know enough nonstandard analysis to interpret it).


## Examples

A function is [[continuous function|continuous]] (with respect to the usual [[order topology]] on $R$) iff it is both upper and lower semicontinuous.

The [[characteristic function]] of a [[subset]] $A$ (either valued in the [[poset]] of [[truth values]] with its usual order or valued in the [[real numbers]] with $1$ for true and $0$ for false) is lower semicontinuous iff $A$ is [[open subset|open]], and upper semicontinuous iff $A$ is [[closed subset|closed]] (hence continuous iff $A$ is [[clopen subset|clopen]]).

## Semicontinuity for multi-valued maps

We define the __small__ and __large preimages__ of a subset $V \subset Y$ under a [[multi-valued function]] $F\colon X \to Y$ by
$$\begin{aligned}
  F^{*s}(V) &\coloneqq \{ x \in X \mid F(x) \subset V \} \;\text{and} \\
  F^{*l}(V) &\coloneqq \{ x \in X \mid F(x) \cap V \neq \emptyset \}.
\end{aligned}$$
A [[multi-valued function]] $F\colon X \to Y $ is said to be __upper semicontinuous__ if the small preimage of all open sets are open and is said to be __lower semicontinuous__ if the large preimages of all open sets are open. Both properties have also a point-wise variant. The map $F$ is __upper semicontinuous at $x$__ for some $ x \in X$ if for every open neighborhood $V$ of $F(x)$ there is a neighborhood $U$ of $x$ such that for all $x'\in U$ the set $F(x')$ is contained in $V$. Likewise, $F$ is __lower semicontinuous at $x$__ for some $ x \in X$ if for every open neighborhood $V$ intersecting $F(x)$ (i.e. $ V \cap F(x) \neq \emptyset $) there is a neighborhood $U$ of $x$ such that for all $x'\in U$ the set $F(x')$ intersects $V$.

## Generalizations

We need to say something about when $R$ is a [[dcpo]] or something like that (involving the [[Scott topology]]), as well as semicontinuity in [[constructive mathematics]] involving [[locales]].  Compare also the [[one-sided real numbers]].

## Related concepts

* [[selection theorem]]


## References

To read later:

* {#LiWang} Li Yong-ming and Wang Guo-jun, Localic Kat&#283;tov&#8211;Tong insertion theorem and localic Tietze extension theorem, [pdf](http://www.kurims.kyoto-u.ac.jp/EMIS/journals/CMUC/pdf/cmuc9704/yong.pdf).
  

* {#GarciaPicado} Guti&#233;rrez Garc&#237;a and Jorge Picado, On the algebraic representation of semicontinuity, [doi](http://dx.doi.org/10.1016/j.jpaa.2006.09.004).
  


[[!redirects semicontinuous map]]
[[!redirects semicontinuous maps]]
[[!redirects semi-continuous map]]
[[!redirects semi-continuous maps]]
[[!redirects semicontinuous function]]
[[!redirects semicontinuous functions]]
[[!redirects semi-continuous function]]
[[!redirects semi-continuous functions]]

[[!redirects semicontinuity]]
[[!redirects semi-continuity]]
[[!redirects semicontinuous]]
[[!redirects semi-continuous]]

[[!redirects lower semicontinuous map]]
[[!redirects lower semicontinuous maps]]
[[!redirects lower semi-continuous map]]
[[!redirects lower semi-continuous maps]]
[[!redirects lower semicontinuous function]]
[[!redirects lower semicontinuous functions]]
[[!redirects lower semi-continuous function]]
[[!redirects lower semi-continuous functions]]

[[!redirects lower semicontinuity]]
[[!redirects lower semi-continuity]]
[[!redirects lower semicontinuous]]
[[!redirects lower semi-continuous]]

[[!redirects upper semicontinuous map]]
[[!redirects upper semicontinuous maps]]
[[!redirects upper semi-continuous map]]
[[!redirects upper semi-continuous maps]]
[[!redirects upper semicontinuous function]]
[[!redirects upper semicontinuous functions]]
[[!redirects upper semi-continuous function]]
[[!redirects upper semi-continuous functions]]

[[!redirects upper semicontinuity]]
[[!redirects upper semi-continuity]]
[[!redirects upper semicontinuous]]
[[!redirects upper semi-continuous]]
