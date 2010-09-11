
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

## Idea

In the definition of [[(n,r)-categories]] in [[higher category theory]] the **coherence laws** assert that:

+-- {: .un_defn}
###### Semi-formal Definition
**(Coherence)** 

While [[associativity]] and [[uniticity]] of [[composition]] of [[k-morphism]]s holds only up to choices of higher morphisms, **coherence** is the demand that the collection of these choices forms a _[[contractible]]_ [[∞-groupoid]].

A **[[coherence theorem]]** is an assertion that with a given definition of [[n-category]]-structure, coherence is satisfied.

=--

+--{.query}
Todd: I'm sorry, that formulation of coherence theorem seems to go overboard. A full coherence theorem for symmetric monoidal closed categories asserts nothing of the sort, and to say that the coherence theorem for braided monoidal categories or for tortile categories asserts a statement of this form is either wrong or highly questionable. 
=-- 

+-- {: .un_remark}
###### Remark

It is the fact that this condition makes recourse among all [[(n,r)-categories]] to [[(∞,0)-categories]]  = [[∞-groupoid]]s that it is easier to define and handle an [[(∞,n)-category|(∞,r)-category]] than an [[(n,r)-category]] for finite $n$: in the former case one just needs that certain spaces are [[contractible]] without necessarily being _equal_ to the point, while in the latter case one demands some of these to be exactly _equal_ to the point, which is a condition much harder to get under control. Accordingly, a _coherence law_ in an [[(n,n)-category]] such as a [[bicategory]] ($n = 2$) or a [[tricategory]] ($n=3$) or a [[tetracategory]] ($n = 4$) is in degree $n+1$ a complicated _equation_ that asserts that a certain contractible space of higher morphisms is exactly equal to the point. 

=--



## Examples

* The [[coherence theorem for monoidal categories]] asserts that the with the standar definition of [[monoidal category]], there is a unique composite of [[associators]] that re-bracket any sequence of [[tensor product]]s.

[[!redirects coherence laws]]
[[!redirects coherent]]
[[!redirects coherence]]

[[!redirects coherence condition]]
