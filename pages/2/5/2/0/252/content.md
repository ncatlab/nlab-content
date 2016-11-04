+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An ordinary [[locally small category]] $\mathcal{C}$ has for any ordered pair of  [[object]]s $x,y$ a [[hom-set]] $\mathcal{C}(x,y)$&#8212;an object in the category [[Set]].

For $\mathcal{C}$ more generally an [[enriched category]] over a [[closed monoidal category]] $\mathcal{V}$, there is --  by definition -- for all $x,y$ an _object_ $\mathcal{C}(x,y) \in obj V$ that plays the role of the "collection of morphisms" from $x$ to $y$.

Accordingly, if here $\mathcal{V}$ is a category of "spaces" of sorts, then one also speaks of a _hom space_. 
For instance if $\mathcal{V}$ =[[vector spaces]] such that $\mathcal{C}$ is a [[linear category]], then hom-spaces are vector spaces.


Or if $\mathcal{V}$=[[topological spaces]] such that $\mathcal{C}$ is [[topologically enriched category]], then hom-spaces are [[topological spaces]]. If this last example is regarded in the context of [[homotopy theory]], then one may consider just the [[homotopy type]] of these topological spaces, which is equivalently modeled as a [[simplicial set]] ([[Kan complex]]) and thought of as an [[infinity-groupoid]]. In all these cases people still often speak of "hom spaces", but see at _[[derived hom space]]_.


## Examples

* The category [[Grpd]] of [[groupoid]]s is a enriched over itself. Hence for any two groupoids $A,B$, there is a [[hom-groupoid]] $Grpd(A,B)$. This is the [[functor category]] $Func(A,B)$.


## Related concepts


* **hom-object**

* [[hom-set]], [[hom-functor]]

* [[hom-category]]

* [[derived hom-space]]



[[!include homotopy-homology-cohomology]]


[[!redirects hom-objects]]
[[!redirects hom object]]
[[!redirects hom objects]]

[[!redirects enriched hom]]

[[!redirects hom space]]
[[!redirects hom spaces]]


[[!redirects hom-space]]
[[!redirects hom-spaces]]
