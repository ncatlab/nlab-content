
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Definition

### In components

A ($\mathbb{Z}$-graded) **chain complex** in a [[category]] $C$ with a notion of [[zero morphism]] is a sequence of [[object]]s $V_n$, $n\in\mathbb{Z}$, and [[morphism]]s $\partial_n:V_n \to V_{n-1}$ called [[differential|codifferentials]] or _boundary maps_:

$$ 
\cdots \overset{\partial_3}{\to} V_2 \overset{\partial_2}{\to} V_1 \overset{\partial_1}{\to} V_0 \overset{\partial_0}{\to} V_{-1} \overset{\partial_{-1}}{\to} \cdots
$$

such that $\partial_n  \circ \partial_{n+1} = 0$ (the [[zero morphism]]) for each $n$.  

More precisely, this is a _homologically graded_ chain complex, in which the differentials lower degree; if we rename $V_n$ to $V_{-n}$ so that the differentials raise degree, it becomes a _cohomologically graded_ chain complex or a **[[cochain complex]]**.  Common choices for $C$ include [[Ab]], [[Vect]], or $R Mod$, in which case we obtain the familiar definition of an (unbounded) chain complex of abelian groups, vector spaces, or modules.

Frequently one also considers $\mathbb{N}$-graded (or _nonnegatively graded_) chain complexes, which can be identified with $\mathbb{Z}$-graded ones for which $V_n=0$ when $n\lt 0$.  Similarly, an $\mathbb{N}$-graded _cochain_ complex is a cochain complex for which $V_n=0$ when $n\lt 0$, or equivalently a chain complex for which $V_n=0$ when $n\gt 0$.

### In terms of translations

Note that in particular, a chain complex is a [[graded object]] with extra structure.  This extra structure can be codified as a map of graded objects $\partial:V\to T V$, where $T$ is the 'shift' endofunctor of the category $Gr(V)$ of graded objects in $C$, such that $T(\partial) \circ \partial = 0$.  More generally, in any pre-additive category $G$ [[category with translation|with translation]] $T : G \to G$, we can define a **chain complex** to be a [[differential object]] $\partial_V : V \to T V$ such that $V \stackrel{\partial_V}{\to} T V \stackrel{T(\partial_V)}{\to} T T V$ is the [[zero morphism]].  When $G= Gr(C)$ this recovers the original definition.

## Examples

In $C =$ [[Vect]] a chain complex is also called a [[differential graded vector space]], consistent with other terminology such as [[differential graded algebra]]. 

## Properties

### Model structure 

There is a [[model category]] structure on the category $Ch(A)$ of chain complexes in an [[abelian category]]. Its [[homotopy category]] is the [[derived category]] of $A$.

See [[model structure on chain complexes]].

[[!redirects chain complexes]]