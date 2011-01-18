[[!redirects schlessinger's criterion]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

One might wish for a given deformation problem to be representable, but this is almost always too much to hope for. Schlessinger's criterion refers to two weaker notions of representability, namely that of hulls and that of prorepresentability.

The criterion gives a beautifully simple necessary and sufficient way to determine when we get each.



## Definitions

$\Lambda$ will denote a complete [[noetherian ring]].

Unless otherwise specified, everything will be in the category of local Artin $\Lambda$-algebras with residue field $k$ and will be denoted $_\Lambda Art_k$.

Define $_\Lambda Noeth_k$ to be the category of complete noetherian local $\Lambda$-algebras with residue field $k$.

A *small thickening* is a surjection $A' \stackrel{f}{\to} A\to 0$ such that $I=ker(f)$ is principal and $m_{A'}I=0$. Note that in our category any surjection can be factored as a sequence of small thickenings.

A *predeformation functor* is a functor $F: _\Lambda Art_k \to \text{Set}$ such that $F(k)=\{*\}$ is a singleton.

The functor $\overhat{F}: _\Lambda Noeth_k\to \text{Set}$ is defined to be $\displaystyle \overhat{F}(A)= \lim_n F(R/\mathfrak{m}^n)$.

A predeformation functor is [[prorepresentable functor| prorepresentable]] if $\overhat{F}$ is representable.

A hull for $F$ is a pair $(R, \eta)$ where $R\in _\Lambda Noeth_k$ and $\eta\in \overhat{F}(R)$ such that $h_R\to F$ is formally smooth and we have a bijection on tangent spaces $T_{h_R}\to T_F$.

$k[\epsilon]$ is defined to be the ring $k[\epsilon]/(\epsilon^2)$ with the trivial $\Lambda$-algebra structure.


## The Conditions

Note that whenever we are given a predeformation functor $F$, and two maps of rings: $A'\to A$ and $A''\to A$ we get an induced map $F(A'\times_A A'')\to F(A')\times_{F(A)} F(A'')$ by functoriality of $F$ and the universal property of a [[pullback]]. Call this map (\*).

Schlessinger gives four conditions in his [paper](#Schless) called (H1) - (H4).

(H1) If $A''\to A$ is a small thickening then (\*) is surjective.

(H2) If $A=k$ and $A''=k[\epsilon]$, then (\*) is bijective.

(H3) $T_F$ is finite-dimensional

(H4) If $A''=A'$ and $A'\to A$ is a small thickening, then (\*) is bijective


Geometrically the conditions can informally be thought of as follows:

One can think of (H1) as being able to "glue".

One can think of (H2) as gluing being unique over infinitesimal neighborhoods.

(H3) is having a finite dimensional tangent space

One can think of (H4) as gluing being unique on a small thickening over itself.


## The Theorem

The main theorem of Schlessinger's [paper](#Schless) says that  (H1), (H2), and (H3) are satisfied if and only if $F$ has a hull. The second part of the theorem is that $F$ is prorepresentable if and only if in addition (H4) is satisfied.

We call a predeformation functor a *deformation functor* if it satisfies (H1) and (H2).



## Examples

Let $Def_X$ be the predeformation functor parametrizing flat deformations of $X$. Then (H1) and (H2) are always satisfied and hence it is a deformation functor. If $X$ is proper, then (H3) is satisfied and it has a hull. $Def_X$ is prorepresentable if and only if every automorphism extends over a small thickening.

Consider the node $X=\text{Spec} k[ [ x,y ] ] /(xy)$. Then the pair $(k[ [ t ] ], \text{Spec} k [ [ x,y,t ] ] /(xy - t))$ is a hull for $Def_X$. Note that this functor is not prorepresentable.


*Several more can be added.





## References

See also [[deformation theory]] and references therein.

* M. Schlessinger, _Functors of Artin rings_, Trans. AMS 130, 208-222 (1968) 
{#Schless}

this was a groundbreaking article at the time, still much cited. 

