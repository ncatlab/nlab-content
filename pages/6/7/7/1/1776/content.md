
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of __co-H-space__ is the [[Eckmann-Hilton duality|Eckmann-Hilton dual]] of that of [[H-spaces]].

They are [[co-H-object]]s in the [[category]] of [[pointed object|pointed]] [[topological spaces]]. Thus a co-H-space $(X, \phi)$ is a pointed space, $X$, together with a map $\phi: X \to X \vee X$ (the [[wedge sum]]), such that $p_i \circ \phi$ is homotopic to $1_X$, where $p_i, i = 1, 2$, are the projections $X \vee X \to X$. Alternatively, $(X, \phi)$ is a co-H-space if and only if $j \circ \phi$ is homotopic to $\Delta$, where $j: X \vee X \to X \times X$ is the inclusion and $\Delta: X \to X \times X$ is the [[diagonal map]].

The importance of the notion is that $X$ is a co-H-space if and only if for every space $Y$, $[X, Y]$ has a binary operation with unit. Further properties of $\phi$ are of interest, in particular being (co)associative and having right and left (co)inverses. In this case $X$ is a [[cogroup]]. The [[suspension]] of a topological space is a cogroup. 

Every co-H-space is [[path-connected space|path-connected]], and its [[fundamental group]] is [[free group|free]].


##Reference##

* [[Martin Arkowitz]], _Co-H-spaces_, chapter 23 of [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_


[[!redirects co-H-spaces]]
