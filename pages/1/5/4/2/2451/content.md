
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


\tableofcontents


## Idea

The _free groupoid_ on a [[directed graph]] is the [[groupoid]] whose [[objects]] are the vertices of the graph and whose morphisms are finite concatenations of the edges in the graph and formal inverses to them. 

This construction is the [[left adjoint]] [[free construction]] to the [[forgetful functor]] that sends a groupoid to its underlying [[directed graph]].

{#FreeGroupoidOnACategory} More generally, there is a free groupoid construction on ([[small category|small]]) [[strict categories]], given by freely adjoining [[inverse morphisms]] to all existing non-invertible morphisms, and the free groupoid on a directed graph is the pre-composition of that operation with the [[free category]]-construction on the graph:

$$
  Grpd^{strct}_{smll}
  \underoverset
    {\underset{U_{Grpd}}{\longrightarrow}}
    {\overset{F_{Grpd}}{\longleftarrow}}
    {\;\;\bot\;\;\;}
  Cat^{strct}_{smll}
  \underoverset
    {\underset{U_{Cat}}{\longrightarrow}}
    {\overset{F_{Cat}}{\longleftarrow}}
    {\;\;\bot\;\;\;}
  DiGrph
$$

(Incidentally, the [[forgetful functor]] $U_{Grpd} \,\colon\, Grpd^{strct}_{smll} \longrightarrow Cat^{strct}_{smll}$ also has a [[right adjoint]], known as the *[[core]]*-construction).


## Definition

Given a [[graph]] $D$, that is, a collection of vertices and of labeled arrows between them, the **free groupoid $G(D)$ on $D$** is the [[groupoid]] that has the vertices of $D$ as [[objects]], and whose [[morphisms]] are constructed recursively by formal composition (i.e., juxtaposition) from identity maps, the arrows of $D$ and formal [[inverses]] for the arrows of $D$. 

The only relations between morphisms of $G(D)$ are the necessary ones defining the [[identity]] of each object, the [[inverse]] of each arrow in $D$ and the associativity of composition. This is clearly a groupoid, which comes with an evident morphism $D \to G(D)$ of quivers. 

The above sketched construction could be made more precise, but what really matters is the [[universal property]] it enjoys: the free groupoid $G(D)$ is the universal ([[initial object|initial]]) [[groupoid]] mapping out of $D$. By varying $D$, the free groupoid yields a [[functor]] $G$ from [[directed graph]]s to [[groupoid]]s, [[left adjoint]] to the forgetful functor. 

This last conceptual characterization is best taken as the definition. Similarly, it is possible to construct the left adjoint to the forgetful functor from groupoids to categories, that is the **free groupoid over a category**.

The construction of free groupoids in "Topology and Groupoids" is by taking a disjoint union of copies of the unit interval groupoid $\mathbf I$ and then identifying the vertices according to the scheme given by the directed graph. 

See the paper by Crisp and Paris for an application of free groupoids. 

## Properties

### Fundamental group
 {#FundamentalGroup}

+-- {: .num_prop}
###### Proposition

The [[fundamental group]] of a free groupoid on a [[countable set|countable]] [[directed graph]] (for any basepoint) is a [[free group]].

=--

For instance ([Cote, theorem 2.3](#Cote)).

+-- {: .num_example}
###### Example

The [[fundamental group]] of the free groupoid of a graph with a single vertex is the [[free group]] on the set of edges of the graph. A result relevant to the Jordan Curve Theorem and the Phragmen-Brouwer Property  is given in the Corrigendum referenced below. It gives conditions on a pushout of groupoids to contain a free groupoid as a retract. 

=--

## Related concepts

* [[free category]], [[core groupoid]]

* [[Nielsen-Schreier theorem]]

* [[Dwyer-Kan simplicial path groupoid]]



## References

On the construction of free groupoids on a graph:

* [[Philip Higgins]], §4 of: *Categories and groupoids*, Van Nostrand Reinhold (1971); Reprints in Theory and Applications of Categories **7** (2005) 1-195 &lbrack;[tac:tr7] (http://www.tac.mta.ca/tac/reprints/articles/7/tr7abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/7/tr7-2l.pdf)&rbrack;

* {#MacLane} [[Saunders MacLane]], p. 51 Ex. 3 in: *[[Categories for the Working Mathematician]]*, Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

On the construction of free groupoids on a category ([[localization]] at all morphisms):

* [[Pierre Gabriel]], [[Michel Zisman]], §1.5.4 of: *[[Calculus of fractions and homotopy theory]]*, Ergebnisse der Mathematik und ihrer Grenzgebiete **35**, Springer (1967) &lbrack;[doi:10.1007/978-3-642-85844-4](https://link.springer.com/book/10.1007/978-3-642-85844-4), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf)&rbrack;

and in the generality of [[sSet-enriched categories]] and [[sSet]]-[[enriched groupoids]] ("[[simplicial groupoids]]"):

* {#DwyerKan80} [[William Dwyer]], [[Daniel Kan]], §5.5 of: *Simplicial localizations of categories*, J. Pure Appl. Algebra **17** 3 (1980), 267-284 &lbrack;<a href="https://doi.org/10.1016/0022-4049(80)90049-3">doi:10.1016/0022-4049(80)90049-3</a>&rbrack;

* [[André Joyal]], [[Myles Tierney]], pp. 75 of: *On the theory of path groupoids*, Journal of Pure and Applied Algebra **149** 1 (2000) 69-100 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(98)00164-9">doi:10.1016/S0022-4049(98)00164-9</a>&rbrack;

* [Goerss & Jardine (2009), V.7](Dwyer-Kan+loop+groupoid#GoerssJardine09)

  > (highlighting relation to the [[Milnor construction]])



See also:

* {#Cote} Lauren Cote, _Free groups and graphs: the Hanna Neumann theorem_ (2008) &lbrack;[pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2008/REUPapers/Cote.pdf)&rbrack;
 
* [[Ronnie Brown]]: _Topology and Groupoids_ (2006)  &lbrack;[web] (http://pages.bangor.ac.uk/~mas010/topgpds.html)&rbrack;

* [[Omar Antolín-Camarena]], [[Ronnie Brown]]: *Corrigendum to "Groupoids, the Phragmen-Brouwer Property, and the Jordan Curve Theorem", J. Homotopy and Related Structures 1 (2006) 175-183* &lbrack;[arXiv:1404.0556](https://arxiv.org/abs/1404.0556), [pdf] (http://pages.bangor.ac.uk/~mas010/pdffiles/brouwer-cor-fin.pdf)&rbrack;

* J. Crisp, L. Paris, *The solution to a conjecture of Tits on the subgroup generated by the squares of the generators of an Artin group*, Invent. math. 145, 19&#8211;36 (2001). 


[[!redirects free groupoids]]
