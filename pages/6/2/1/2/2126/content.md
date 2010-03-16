
> under construction

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

The **singular cohomology** of a [[topological space]] $X$ is the [[chain homology and cohomology|cochain cohomology]] of the [[cochains on simplicial sets|cochains on the simplicial set]] $X^{\Delta^\bullet_{Top}}$ of "singular simplices" in $X$, i.e. of images of the standard topological simplices in $X$.

Write

$$
  \Delta_{Top} : \Delta \to Top
$$

for the canonical [[cosimplicial object]] in [[Top]], induced from the standard [[interval object]] $\Delta_{Top}^1 = [0,1]$.:

$$
  \Delta_{Top}^n = \{ 0 \leq x_1 \leq x_2 \cdots \leq x_n  \leq 1 \} \subset \mathbb{R}^n
  \,.
$$

For $X$ a [[topological space]], let $\Pi(X)_\bullet := X^{\Delta_{Top}^\bullet}$ be the [[simplicial set]] of $n$-[[simplex|simplices]] in $X$ -- the [[fundamental ∞-groupoid]] of $X$.

For $R$ some [[ring]], let $Maps(\Pi(X),R)^{\bullet}$ be the [[cosimplicial object|cosimplicial]] [[ring]] of $R$-valued functions on the spaces of $n$-simplices. The corresponding [[Moore complex|Moore cochain complex]] $C^\bullet(X)$ of normalized cochains is the cochain complex whose [[chain homology and cohomology|cochain cohomology]] is the __singular cohomology__ of the space $X$:


A homogeneous element $\omega_p \in C^p(X)$ is a function on $p$-simplices in $X$.

These form a ring themselves under the [[cup product]].

## Properties

* [[de Rham theorem]]

...

## Discussion

A previous version of this entry led to the following discussion, which later led to extensive discussion by email. Partly as a result of this and similar discussions, there is now more information on how Kan complexes _are_ $\infty$-groupoids at 

* [[Kan complex]]

* [[∞-groupoid]].

+-- {: .query}

_[[RonnieBrown]]_ Query: Why is the notation $\Pi(X)$ used here? The old notation $S(X)$ or $S^\Delta(X)$ is perfectly clear. The notation $\Pi(X)$ suggests it is some kind of $\infty$-groupoid, but the precise statement of such properties are unclear, and it conflicts with older use of $\Pi$ where some homotopy classes are taken in a more structured situation (filtered spaces, $n$-cubes of spaces) to give well defined strict structures closely related to classical construtions (relative homotopy groups, $n$-adic homotopy groups). 

There should also be some analysis of why globular or simplicial constructions are used rather than cubical ones. 
The case needs to be made, as this analysis of aims is useful. 

[[Urs Schreiber]]: I believe that [[Toby Bartels|Toby]] copied material which I typed elsewhere, so this is my fault. But I have adopted the habit of writing $\Pi(X)$ instead of $S(X)$, because the singular complex $S(X)$ _is_ the fundamental $\infty$-groupoid in its Kan complex incarnation. I find it conceptually very useful to make that explicit and I felt like here on the $n$Lab I can allow myself to do this. But I am prepared to be outvoted. In any case, we should certainly have a discussion of the notation and certainly of the different models: globular, simplicial, cubical. 

I'd do it myself if I had the time right now, but I have to run. Sorry.

=--

