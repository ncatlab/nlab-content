[[!redirects Schlessinger's criterion]]
[[!redirects schlessinger's criterion]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea and Motivation

One motivation for studying deformations over Artin rings is that one may wish to classify/parameterize or create a [[moduli space]] of some particular type of object. Often it is very easy to write down a [[functor of points]] for the space. For instance, curves of genus $g$, vector bundles on some fixed variety, maps between varieties, closed subschemes, quotients of a coherent sheaf, and the list goes on.

But then one must ask, is this really a space? In other words, is it [[representable functor| representable]]? This rarely happens, but even if you don't have a legitimate space, you can see what the "points" are formally locally. If everything in your original problem was noetherian, then [[completion]] of the [[local ring]] at a point gives rise to the Artin rings we consider. The deformations of the object over infinitesimal thickenings gives us a way to tell what the points near our given point look like on the original [[moduli space]].

This reduces us to now asking for a given deformation problem to be representable, but this is almost always too much to hope for as well. Schlessinger's criterion refers to two weaker notions of representability, namely that of hulls and that of [[prorepresentable functor| prorepresentability]]. The criterion gives a beautifully simple necessary and sufficient way to determine when we get each.

Once we determine these formal local points, we must then go backwards and see if these correspond to actually points in the original space. This is known as effectivization.



## Definitions

$\Lambda$ will denote a complete [[noetherian ring]].

Unless otherwise specified, everything will be in the category of local Artin $\Lambda$-algebras with residue field $k$ and will be denoted $_\Lambda Art_k$.

Define $_\Lambda Noeth_k$ to be the category of complete noetherian local $\Lambda$-algebras with residue field $k$.

A *thickening* is a surjection $A' \stackrel{f}{\to} A\to 0$ such that $I=ker(f)$ satisfies $m_{A'}I=0$. 

A *small thickening* is a thickening in which $I$ is principal. Note that in our category any surjection can be factored as a sequence of small thickenings.

A *predeformation functor* is a functor $F: _\Lambda Art_k \to \text{Set}$ such that $F(k)=\{*\}$ is a singleton. This condition is the notion that we are really over a "point", and so any deformation must be the trivial one.

The functor $\widehat{F}: _\Lambda Noeth_k\to \text{Set}$ is defined to be $\displaystyle \widehat{F}(A)= \lim_n F(R/\mathfrak{m}^n)$.

A predeformation functor is [[prorepresentable functor| prorepresentable]] if $\widehat{F}$ is representable.

A hull for $F$ is a pair $(R, \eta)$ where $R\in _\Lambda Noeth_k$ and $\eta\in \widehat{F}(R)$ such that $h_R\to F$ is formally smooth and we have a bijection on tangent spaces $T_{h_R}\to T_F$.

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


## Deformation Functors

We call a predeformation functor a *deformation functor* if it satisfies (H1) and (H2). Here we make precise what was meant in the motivation section. Suppose you have a moduli functor $\tilde{F}: \text{Sch}\to \text{Set}$ and you would like to know what the [[moduli space]] looks like in a neighborhood of some point say $\eta_0\in \overline{F}(\text{Spec} k)$. Then if we consider the functor of deformations of $\eta_0$, we get $F: _\Lambda Art_k \to \text{Set}$ by the following prescription $F(A)=\{ \eta \in \overline{F}(\text{Spec} A): \eta|_{\text{Spec} k}=\eta_0\}$. This $F$ can be seen to be a deformation functor.

Of course, this doesn't *always* work if we're parametrizing objects with automorphisms, but this general approach does work for most of the examples in the motivation section and explains why this class of functors is what we consider.


## Schlessinger's Criterion

The main theorem of Schlessinger's [paper](#Schless) says that  (H1), (H2), and (H3) are satisfied if and only if $F$ has a hull. The second part of the theorem is that $F$ is prorepresentable if and only if in addition (H4) is satisfied.




## Examples

Let $Def_X$ be the predeformation functor parametrizing flat deformations of $X$. Then (H1) and (H2) are always satisfied and hence it is a deformation functor. If $X$ is proper, then (H3) is satisfied and it has a hull. $Def_X$ is prorepresentable if and only if every automorphism extends over a small thickening.

Consider the node $X=\text{Spec} k[ [ x,y ] ] /(xy)$. Then the pair $(k[ [ t ] ], \text{Spec} k [ [ x,y,t ] ] /(xy - t))$ is a hull for $Def_X$. Note that this functor is not prorepresentable.


*Several more can be added.


## Tangent and Obstruction Theories

I haven't come up with a nice succinct way to do this yet. I think there is a nice streamlined gerbe/stacky way to think about it in the Brian Osserman article cited below.


## Effectivization

Given a deformation functor, $F$, that came from a moduli problem and some object $\eta\in \widehat{F}(R)$, we'd like to tell when it corresponds to a point on the original moduli space over $\text{Spec}R$, or if $(R,\eta)$ is a hull for $F$ does there exist a universal object over $\text{Spec}R$?

An example where we do have effectivization is Grothendieck's existence theorem for coherent sheaves. Let $f:X\to \text{Spec}A$ be proper and $A$ complete, local, [[noetherian ring]]. Let $A_n=A/m^n$ and $X_n=X\otimes_A A_n$ the thickenings over $A_n$. If $\mathcal{F}_n$ is a compatible collection of coherent sheaves on $X_n$, then there exists a coherent sheaf $\mathcal{F}$ on $X$ whose restriction to each $X_n$ is $\mathcal{F}_n$.





## References

See also [[deformation theory]] and references therein.

* B. Osserman, _Deformations and automorphisms: a framework for globalizing local tangent and obstruction spaces_, Annali della Scuola Normale Superiore di Pisa, Classe di Scienze, IX (2010), no. 3, 581-633.

* M. Schlessinger, _Functors of Artin rings_, Trans. AMS 130, 208-222 (1968) 
{#Schless}

this was a groundbreaking article at the time, still much cited. 

