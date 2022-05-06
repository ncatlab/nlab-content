+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--



# Hypergraph categories

* table of contents
{: toc}

## Idea

A *hypergraph category* is a [[monoidal category]] whose [[string diagrams]] are [[hypergraphs]].  Recall that in general the [[vertices]] of a string diagram correspond to [[morphisms]] in a [[category]], and its [[edges]] to [[objects]].  An ordinary string diagram is a [[directed graph]], where the inputs and outputs of a vertex describe objects appearing in a [[tensor product]]-decomposition of the [[domain]] and [[codomain]] of a morphism; each edge is connected to only one vertex as input and one vertex as output because of how morphisms in a category are composed.  A hypergraph category allows edges to connect to many vertices as input and many vertices as output, which [[category theory|category theoretically]] means that we may [[composition|compose]] many morphisms containing an object in their [[codomain]] with many morphisms containing that object in their [[domain]].

Hypergraph categories have been reinvented many times and given many different names, such as "well-supported compact closed categories" ([Carboni](#Carboni) and [RSW](#RSW)), "dgs-monoidal categories" ([GH](#GH)), and "spidered/dungeon categories" ([Morton](#Morton)).  The name "hypergraph category" is more recent ([Kissinger](#Kissinger) and [Fong](#FongDC)).

## Definition

A **hypergraph category** is:

* a [[symmetric monoidal category]] in which
* each object is equipped with the structure of a special commutative [[Frobenius algebra]], such that
* the Frobenius algebra structure of any tensor product $X\otimes Y$ is induced in the canonical way from those of $X$ and $Y$.

Note in particular that we do *not* require the morphisms of the category to be Frobenius algebra morphisms.

## Examples

* The category [[Rel]] of sets and relations (with cartesian product of sets as the monoidal product) is a hypergraph category, with the Frobenius algebra on $X$ given by the "deleting and copying" [[comonoid]] $\{ (x, *) \mid x \in X \}$, $\{ (x, (x, x)) | x \in X \}$ together with its [[opposite relation|opposite]].

* More generally, categories of [[span|spans]], [[cospan|cospans]], [[relation|relations]] and [[corelation|corelations]] in any category (with the appropriate structure) can be made into hypergraph categories by choosing the correct monoidal structure.  For example, the category [[FinRel]] is hypergraph when this category is given the $\times$ monoidal structure (beware: this is not the categorical product in $FinRel$; it comes from cartesian product in [[FinSet]]).  The same is probably true of relations in any [[regular category]].    The category $FinRel$ is not hypergraph when given the $+$ monoidal structure.   The category [[FinCorel]] is hypergraph when this category is given the $+$ monoidal structure (coming from disjoint unions).

* Categories of [[decorated cospan|decorated cospans]] and decorated corelations are hypergraph categories.

## Remarks

* The reason for the definition is that if $X$ is a special commutative Frobenius algebra, then there is a unique morphism $X^{\otimes m}\to X^{\otimes n} $ induced by the Frobenius algebra structure.  It can of course be defined as the $m$-ary multiplication followed by the $n$-ary comultiplication; the real point is that the special commutative Frobenius axioms ensure that any composite of two such morphisms is again another such morphism.  This is what enables the hypergraph string diagrams described informally above. (Some authors refer to these morphisms as "spiders" due to their appearance in [[string diagram|string diagrams]], as a black node with $m + n$ legs.)

* The free hypergraph category on one object is the category of finite sets and isomorphism classes of cospans.  This is a decategorification of the fact that the free monoidal category containing a (non-special) commutative Frobenius algebra is the category of 1-dimensional [[manifolds]] and isomorphism classes of 2-dimensional [[cobordisms]].  More general free hypergraph categories can be constructed using labeled cospans.

* Note that the special commutative Frobenius algebras are not required to be "extra-special", meaning that the morphism $I = X^{\otimes 0} \to X^{\otimes 0} = I$ need not be the identity.  Thus, the relevant sort of "hypergraphs" can contain "edges not incident to any vertices".  If we add the extra-special condition, the cospans are replaced by "co-relations", i.e. jointly surjective cospans.

## Properties

### As monoids in a presheaf category

Let $\mathbf{Cospan}_\Delta$ be the free hypergraph category on [[generators and relations|generators]] $\Delta$. The objects are [[lists]] of [[elements]] of $\Delta$, or equivalently [[pairs]] $(m,l)$ of a [[natural number]] $m$ and a labelling $l\colon \big[ m \big] \to \Delta$. The morphisms are compatible [[cospans]] of [[functions]] (up to [[isomorphism]]). 

+-- {: .un_prop}
###### Theorem 
[Fong, Spivak](#FongSpivak).
To give a hypergraph category with chosen objects $\Delta$ that generate it is to give a lax monoidal functor $\mathbf{Cospan}_\Delta\to \mathbf{Set}$. 
=--
(Formally, this can be made into an equivalence between the category of objectwise-free hypergraph categories and the lax monoidal functors; and every hypergraph category is in some sense equivalent to an objectwise-free one.)

A hypergraph category is thus a [presheaf](https://ncatlab.org/nlab/show/presheaf) $H\colon \mathbf{Cospan}_\Delta\to \mathbf{Set}$ that has lax monoidal structure 
\[
1\to H()\qquad H(\vec a)\times H(\vec b)\to H(\vec a,\vec b)
\]
which is strongly reminiscent of the [mix rule](https://ncatlab.org/nlab/show/mix%20rule). 
A lax monoidal functor is the same thing as a [monoid for the Day convolution](https://ncatlab.org/nlab/show/Day+convolution#Monoids). Thus hypergraph categories are monoids in the presheaf category $[\mathbf{Cospan}_\Delta, \mathbf{Set}]$.

## References

* {#Kissinger} [[Aleks Kissinger]], *Finite matrices are complete for (dagger-)hypergraph categories*. ([arxiv:1406.5942](https://arxiv.org/abs/1406.5942))
 
* {#FongDC} [[Brendan Fong]], *Decorated cospans*, Theory and Applications of Categories, Vol. 30, 2015, No. 33, 1096-1120. ([arxiv:1502.00872](https://arxiv.org/abs/1502.00872))

* {#FongThesis} [[Brendan Fong]], *The Algebra of Open and Interconnected Systems*, Ph.D. Thesis, Department of Computer Science, University of Oxford, 2016. ([arxiv:1609.05382](https://arxiv.org/abs/1609.05382))

* {#Carboni} [[Aurelio Carboni]], _Matrices, relations and group representations_ J. Algebra, 138(2):497&#8211;529, 1991.

* {#RSW} [[Robert Rosebrugh]], N. Sabadini, and R. F. C. Walters. *Generic commutative separable algebras and cospans of graphs*. Th. App. Cat. 15(6):164&#8211;177, 2005. [online](http://www.tac.mta.ca/tac/volumes/15/6/15-06abs.html).
 

* {#GH} F. Gadducci, R. Heckel. *An inductive view of graph transformation*. In "Recent Trends in Algebraic Development Techniques", Lecture Notes in
Computer Science 1376:223&#8211;237. Springer&#8211;Verlag, Berlin Heidelberg, 1998.
 

* {#Morton} [[Jason Morton]], _Belief propagation in monoidal categories_ In [[Bob Coecke]], I. Hasuo, P. Panangaden (eds.) _Quantum Physics and Logic_ 2014 (QPL 2014), EPTCS 172:262&#8211;269.
 

* {#FongSpivak} [[Brendan Fong]] and [[David Spivak]], *Hypergraph categories*. ([arxiv:1806.08304](https://arxiv.org/abs/1806.08304)) 
 

[[!redirects hypergraph categories]]
[[!redirects well-supported compact closed category]]
[[!redirects well-supported compact closed categories]]
[[!redirects dgs-monoidal category]]
[[!redirects dgs-monoidal categories]]
[[!redirects spidered category]]
[[!redirects spidered categories]]
[[!redirects dungeon category]]
[[!redirects dungeon categories]]
