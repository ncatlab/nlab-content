[[!redirects lifts and sections]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


Given any [[morphism]] in some [[category]] a basic question is to ask for [[lifts]]/[[extensions]] along it (which are [[formal duality|dual]] notions), and in particular for [[retracts]]/[[sections]]. 

We survey how these concepts relate to each other. See the respective entries for more details and pointers.

## Definitions


+-- {: .num_example}
###### Extension problem

Given morphisms $i:A\to X$, $f:A\to Y$ find an [[extension]] of $f$ to $X$, i.e. a morphism $\tilde{f}:X\to Y$ such that $i\circ\tilde{f}=f$. Notice that if $i:A\hookrightarrow X$ is a [[subobject]], then $i\circ\tilde{f}$ is the [[restriction]] $\tilde{f}{|_A}$, and the condition is $\tilde{f}{|_A} = f$. 

=--

+-- {: .num_example}
###### Retraction problem

Let $i:A\to X$ be a morphism. Find a [[retraction]] of $i$, that is a morphism $r:X\to A$ such that $r\circ i = id_A$.

=--

The retraction problem is a special case of the extension problem for $Y=A$ and $f=id_A$. Conversely, the general extension problem may (in [[Top]] and many other categories) be reduced to a retraction problem:

+-- {: .num_prop}
###### Proposition (Reducing an extension to a retraction)

If the [[pushout]] $Y\coprod_A X$ exists (for $i$, $f$ as above) then the extensions $\tilde{f}$ of $f$ along $i$ are in 1--1 correspondence with the retractions of $i_*(f) : Y\to Y\coprod_A X$. 

=--

+-- {: .num_example}
###### Lifting problem

Given morphisms $p:E\to B$ and $g:Z\to B$, find a [[lifting]] of $g$ to $E$, i.e. a morphism $\tilde{g}:Z\to E$ such that $p\circ\tilde{g}=g$.

=--

+-- {: .num_example}
###### Section problem

For any $p:E\to B$ find a [[section]] $s: B\to E$, i.e. a morphism $s$ such that $p\circ s = id_B$.

=--

The section problem is a special case of a lifting problem where $g = id_B : B\to B$. Then the lifting is the section: $\tilde{g} = s$.  A converse is true in the sense

+-- {: .num_prop}
###### Proposition (Reducing a lifting to a section)

If the [[pullback]] $Z\times_B E$ exists then the general liftings for of $G$ along $p$ as above are in a bijection with the section of $g^*(p)=Z\times_B p : Z\times_B E\to Z$. 

=--



## Related concepts

* [[lift]]/[[extension]]

* [[retract]]/[[section]]



category: disambiguation


