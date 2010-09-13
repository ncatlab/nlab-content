
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## In the definition of $(n,r)$-categories

In the definition of [[(n,r)-categories]] in [[higher category theory]] the **coherence laws** assert that:

+-- {: .un_defn}
###### Semi-formal Definition
**(Coherence)** 

While [[associativity]] and [[uniticity]] of [[composition]] of [[k-morphism]]s holds only up to choices of higher morphisms, **coherence** is the demand that the collection of these choices forms a _[[contractible]]_ [[∞-groupoid]].

A **[[coherence theorem]]** is an assertion that with a given definition of [[n-category]]-structure, coherence is satisfied.

=--


+-- {: .un_remark}
###### Remark

It is the fact that this condition makes recourse among all [[(n,r)-categories]] to [[(∞,0)-categories]]  = [[∞-groupoid]]s that it is easier to define and handle an [[(∞,n)-category|(∞,r)-category]] than an [[(n,r)-category]] for finite $n$: in the former case one just needs that certain spaces are [[contractible]] without necessarily being _equal_ to the point, while in the latter case one demands some of these to be exactly _equal_ to the point, which is a condition much harder to get under control. Accordingly, a _coherence law_ in an [[(n,n)-category]] such as a [[bicategory]] ($n = 2$) or a [[tricategory]] ($n=3$) or a [[tetracategory]] ($n = 4$) is in degree $n+1$ a complicated _equation_ that asserts that a certain contractible space of higher morphisms is exactly equal to the point. 

=--



### Examples

We start the list of examples with a warning on how not to misunderstand the above definition.

+-- {: .un_remark}
###### Warning

The demand for contractible spaces of choices of [[associator]]s and [[unitor]]s is not to be confused with asserting contractible [[hom-space]]s in general (which would make the theory of $(n,r)$-categories trivial, anyqay!) 

For instance in a [[braided monoidal category]] there is, in general, a non-contractible space of morphisms $x \otimes y \to x \otimes y$ for any two objects , because the double braiding $B_{y \otimes x}\circ B_{x \otimes y}$ will not in general be equal to the identity morphism. But the braiding morphisms also is not the kind of structural morphism that the above definition refers to. In the definition of braided monoidal category it may look as if it is on par with the [[associator]], but this is in fact not so: 

in the context of $(n,r)$-categories we may use the [[periodic table of higher categories]] to identify the braided monoidal category with a one-object-one-morphism [[3-category]]. In this, the non-trivial double braiding $B_{y \otimes x}\circ B_{x \otimes y}$ is a nontrivial [[3-morphism]] that represents a nontrivial element of the 3rd [[homotopy group]] of the 3-category. Demanding this to be trivial would be demanding the 3-caztegory to be trivial!

But the role of the associator, which now is a 3-morphism witnessing the non-associativitiy of 2-morphisms under [[horizontal composition]] is quite different. This is best seen by looking at a [[geometric definition of higher categories]], such as an  [[(∞,n)-category]] for $n = 3$: here the associator is a _choice_ of [[horn]]-filler, and this choice by construction happens in a contractible space and by construction cannot contain nontrivial cells like the double braiding. This is also amplified by the following example

=--

+-- {: .un_example}
###### Example
**(monoidal categories)**

The [[coherence theorem for monoidal categories]] asserts that the with the standar definition of [[monoidal category]], there is a unique composite of [[associators]] that re-bracket any sequence of [[tensor product]]s.

=--


+-- {: .un_example}
###### Example
**(quasi-categories)**


For $C$ a [[simplicial set]] that is a [[quasi-category]] we have (as discussed there) that the canonical morphism

$$
  sSet(\Delta[2], C) \to sSet(\Lambda^1[2], C)
$$

is an acyclic [[Kan fibration]]. This means that its [[fiber]]s are [[contractible]] [[∞-groupoid]]s. But these fibers are exactly the spaces whose points are choices of [[composition]] rules, whose morphisms are comparison maps between these, and so on

(...)

=--

+-- {: .un_example}
###### Example
**(Trimbe $\omega$-categories)**

In a [[Trimble n-category]] the space of choices of composing a sequence of $n$ morphisms is explicitly the [[topological space]] $Top_{0,1}(I, I^{\vee n})$ of surjections from the unit interval $[0,1]$ onto the length $n$-interval $[0,n]$. The coherence law of composition in a Trimble $n$-category is the fact that these spaces are [[contractible]].

=--



## For other algebraic structures

One can consider coherence laws for algebraic structures other than $(n,r)$-cagtegories. See [[coherence theorem]] for more.


[[!redirects coherence laws]]
[[!redirects coherent]]
[[!redirects coherence]]

[[!redirects coherence condition]]
