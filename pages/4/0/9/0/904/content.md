
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea 

The fundamental group $\pi_1(X,a)$ of a [[pointed object|pointed]] [[topological space]] $(X,a)$ is the group of [[homotopy]] classes of [[loops]] at $x$, with multiplication defined by concatenation (following one path by another).  

This is the first [[homotopy group]] of $X$.




## Properties

For a (path)-[[connected space]], all of the fundamental groups are isomorphic, no matter which point is chosen as 'base point', so one sometimes speaks of 'the' fundamental group of a connected space.  However, this does not follow the yoga of the [[generalized the]], so careful description of the functors involved still requires using a pointed space.

The fundamental group $\pi_1(X,a)$ generalises in one direction to the [[fundamental groupoid]] $\Pi_1(X)$, or in another direction to the [[homotopy group]]s $\pi_n(X,a)$.  (Ultimately, all of this is contained within the [[fundamental infinity-groupoid]] $\Pi(X)$.)

### Relation to universal covers

There is a relation to [[universal cover|universal covers]]: The group of cover automorphisms of a universal cover is isomorphic to the fundamental group of the covered space. This is used to establish a [[the fundamental group and Galois theory|link between Galois theory and fundamental groups]]. This version of the fundamental group is sometimes called the Chevalley or algebraic fundamental group of the space. In [[Grothendieck's Galois theory]], the role of the basepoint is replaced by considering a 'fibre functor' $F:\mathcal{C}\to Sets$ or to $FinSets$, where $\mathcal{C}$ is the category of coverings of the given space.


## Generalizations

### Non-locally 'nice' spaces and 'generalised' spaces

The definition of fundamental group in terms of homotopy classes of loops at a base point does not work well for the spaces that occur in algebraic geometry, nor for many spaces considered in analysis as there may be very few loops.  For instance, for a [[scheme]] there are in general very few paths, and [[Grothendieck]] gave a definition of a fundamental group in SGA1 which is closely related to the [[Galois group|Galois groups]] of number theory, but in cases where both the path-based group and this [[algebraic fundamental group]] make sense, the algebraic form tends to be related to the [[profinite completion of a group|profinite completion]] of the topological fundamental group; see the example in that entry.

A similar type of construction gives the [[fundamental group of a topos]]. Other related forms include a &#268;ech version of the fundamental group used in shape theory, and linked to &#268;ech homology groups of a compact space.

The notion of fundamental group generalizes to that of [[fundamental groupoid]] in both the loop based theory and in [[Grothendieck's Galois theory]] as described in [[SGA1]]. In this form it has been used to give generalisations for simplicial profinite spaces in work by Quick and to [[pro-spaces]] in work of Isaksen.
  

### Proper fundamental groups

In the context of [[proper homotopy theory]] there are two related fundamental groups for single ended spaces. 

## References

Discussion from the point of view of [[Galois theory]] is in 

* [[Luis Javier Hernández-Paricio]], _Fundamental pro-groupoids and covering projections_([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm156/fm15611.pdf))

Isaksen's work is 

* [[D. C. Isaksen]], _A model structure on the category of pro-simplicial sets_, 
Trans. Amer. Math. Soc., 353, (2001), 2805&#8211;2841

whilst Quick's is in

* [[G. Quick]], _Profinite homotopy theory_, Documenta Mathematica, 13, (2008), 585&#8211;612. 
 

[[!redirects fundamental group]]
[[!redirects fundamental groups]]
