
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion often called an _enriched bicategory_ is that of an [[enriched category]], but where the enriching context $\mathcal{V}$ is allowed to be generalized from a [[monoidal category]] to a [[monoidal bicategory]], while suitably weakening the [[associativity]] any [[unitality]] conditions on the enrichment.

So for $\mathcal{V}$ a [[monoidal bicategory]], a  $\mathcal{V}$-enriched (bi)category $C$ is

* a collection of [[object]]s;

* for every ordered pair $(x,y)$ of objects a [[hom-object]] $C(x,y) \in \mathcal{V}$

* for every ordered triple $(x,y,z)$ a [[composition]] morphism of the form

  $$
    comp_{x,y,z} : C(x,y)\otimes C(y,z) \to C(x,z)
  $$ 

  in $\mathcal{V}$

* for every object $x$ an [[identity]] morphism

  $$
    i_x : I \to C(x,x) 
  $$

  from the tensor unit of $\mathcal{V}$;

* a [[natural isomorphism|natural 2-ismorphism]]

  $$
    \alpha : comp(Id \otimes comp) \Rightarrow comp(comp \otimes Id)
  $$
 
  called the [[associator]]

* similarly left and right [[unitor]]s

* such that some more or less evident [[coherence]] conditions hold.

## References

The definition first appeared in 

* S. M. Carmody, _Cobordism Categories_ , PhD thesis, University of Cambridge,
1995.

A definition also appeared in 

* [[Steve Lack]], _The algebra of distributive and extensive categories_ , PhD thesis, University of Cambridge, 1995.

Forcey has studied the combinatorics of [[polytope]]s associated to enrichment and [[higher category theory|higher categories]] in detail. See for example

* S. Forcey, _Quotients of the Multiplihedron as Categoried Associahedra_ ,  ([arXiv:0803.2694]()).

The definition is reviewed in 

* [[Alex Hoffnung]], _Notes on enrichment_ ([pdf](http://mysite.science.uottawa.ca/hoffnung/notes_files/enrichment_notes.pdf))

[[!redirects enriched 2-category]]