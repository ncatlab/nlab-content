
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[algebraic topology]] one defines and uses [[functor]]s from some category of [[topological space]]s to some category of algebraic objects to help solve some existence or uniqueness problem for spaces or maps. 

There are 4 basic problems of algebraic topology for the existence of maps: extension problems, retraction problems, lifting problems and section problems.

Regarding that these problems make sense in any [[category]], we will talk about objects and morphisms and not spaces and maps. 

+-- {: .un_example}
###### Extension problem
Given morphisms $i:A\to X$, $f:A\to Y$ find an [[extension]] of $f$ to $X$, i.e. a morphism $\tilde{f}:X\to Y$ such that $i\circ\tilde{f}=f$. Notice that if $i:A\hookrightarrow X$ is a [[subobject]], then $i\circ\tilde{f}$ is the [[restriction]] $\tilde{f}{|_A}$, and the condition is $\tilde{f}{|_A} = f$. 
=--

+-- {: .un_example}
###### Retraction problem
Let $i:A\to X$ be a morphism. Find a [[retraction]] of $i$, that is a morphism $r:X\to A$ such that $r\circ i = id_A$.
=--

The retraction problem is a special case of the extension problem for $Y=A$ and $f=id_A$. Conversely, the general extension problem may (in [[Top]] and many other categories) be reduced to a retraction problem:

+-- {: .un_prop}
###### Proposition (Reducing an extension to a retraction)
If the [[pushout]] $Y\coprod_A X$ exists (for $i$, $f$ as above) then the extensions $\tilde{f}$ of $f$ along $i$ are in 1--1 correspondence with the retractions of $i_*(f) : Y\to Y\coprod_A X$. 
=--

+-- {: .un_example}
###### Lifting problem
Given morphisms $p:E\to B$ and $g:Z\to B$, find a [[lifting]] of $g$ to $E$, i.e. a morphism $\tilde{g}:Z\to E$ such that $p\circ\tilde{g}=g$.
=--

+-- {: .un_example}
###### Section problem
For any $p:E\to B$ find a [[section]] $s: B\to E$, i.e. a morphism $s$ such that $p\circ s = id_B$.
=--

The section problem is a special case of a lifting problem where $g = id_B : B\to B$. Then the lifting is the section: $\tilde{g} = s$.  A converse is true in the sense

+-- {: .un_prop}
###### Proposition (Reducing a lifting to a section)

If the [[pullback]] $Z\times_B E$ exists then the general liftings for of $G$ along $p$ as above are in a bijection with the section of $g^*(p)=Z\times_B p : Z\times_B E\to Z$. 
=--




