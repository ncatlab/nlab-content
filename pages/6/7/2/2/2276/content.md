
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### Discrete case

Given an [[action]] $G\times X\to X$ of a ([[discrete group|discrete]]) [[group]] $G$ on a set $X$, any [[set]] of the form $G x = \{g x|g\in G\}$ for a fixed $x\in X$ is called an __orbit__ of the action, or the __$G$-orbit through the point $x$__.  The set $X$ is a [[disjoint union]] of its orbits.


### Category of orbits

The _category of orbits_ of a [[group]] $G$ is the full subcategory
of the category of sets with an action of $G$.

Since any orbit of $G$ is isomorphic to the orbit $G/H$
for some group $H$, the category of $G$-orbits admits the following
alternative description: its objects are subgroups $H$ of $G$
and morphisms $H_1\to H_2$ are elements $[g]\in G/H_2$
such that $H_1\subset g H_2g^{-1}$.

In particular, the group of automorphisms of a $G$-orbit $G/H$
is $N_G(H)/H$, where $N_G(H)$ is the [[normalizer]] of $H$ in $G$.


### Topological case

If $G$ is a [[topological group]], $X$ a [[topological space]] and the action [[continuous map|continuous]], then one can distinguish [[closed subset|closed]] orbits from those which are not. Even when one starts with $G,X$ [[Hausdorff space|Hausdorff]], the space of orbits is typically non-Hausdorff. 
(This problem is one of the motivations of the [[noncommutative geometry]] of Connes' school.)

If the original space is [[paracompact space|paracompact]] Hausdorff, then every orbit $G x$ as a topological $G$-space is isomorphic to $G/H$, where $H$ is the [[stabilizer subgroup]] of $x$. 


## Examples

* An orbit of a [[cyclic group|cyclic]] [[subgroup]] of a [[permutation group]] is called a *[[permutation cycle]]*.


## Related concepts

* [[orbit category]], [[orbit type]]

* [[coadjoint orbit]]

* [[coinvariant]]

* [[coset space]]

* [[orbit method]]

* [[slice theorem]]



## References

Textbook accounts:

* {#Bredon72} [[Glen Bredon]], Sections I.3, I.4 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))



[[!redirects orbits]]

[[!redirects orbit space]]
[[!redirects orbit spaces]]
