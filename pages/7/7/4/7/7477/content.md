
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **completely distributive lattice** is a [[complete lattice]] in which arbitrary [[joins]] and arbitrary meets [[distributive lattice|distribute]] over each other.

## Properties

### Algebraic lattices

+-- {: .num_prop}
###### Proposition

The category of [[Alexandroff locales]] is equivalent to that of completely distributive [[algebraic lattice|algebraic lattices]]. 
=--

This appears as remark 4.3 in ([Caramello 2011](#Caramello11)).

### Constructive complete distributivity

A complete lattice $A$ is called **constructively completely distributive** (CCD) if the join-assigning morphism $D A \to A$ has a left adjoint, with $D A$ the poset of [[downsets]]. 

_Constructive complete distributivity is equivalent to complete distributivity if and only if the [[axiom of choice]] holds_ ([Wood&Fawcett (1990)](#WoodFawcett)).

Constructively completely distributive lattices are an example of [[continuous algebras]] for a [[lax-idempotent 2-monad]].

### Remark

Completely distributive lattices correspond to tight [[Galois connections]] (Raney 1953). This generalizes to a correspondence between totally distributive toposes and [[essential geometric morphism|essential localizations]] (Lucyshyn-Wright 2011).

CCD lattices are precisely the [[nuclear objects]] in the category of complete lattices. 

The (bi-) category $\mathfrak{CCD}$ with CCD lattices and sup-preserving maps is the [[Karoubi envelope|idempotent splitting]] of the (bi-) category of relations $\mathfrak{Rel}$. This plays an important role in _[[domain]]-theoretical_ approaches to the semantics of [[linear logic]].

## Related concepts

* [[continuous lattice]]

* [[totally distributive category]]

## Links

* wikipedia-entry: [completely distributive lattice](http://en.wikipedia.org/wiki/Completely_distributive_lattice)

## References

* [[Olivia Caramello]], _A topos-theoretic approach to Stone-type dualities_  , ms. 2011. ([arXiv:1103.3493](http://arxiv.org/abs/1103.3493))
 {#Caramello11}

* B. Fawcett, R. J. Wood, _Constructive complete distributivity I_ , Math. Proc. Camb. Phil. Soc. **107** (1990)  pp.81-89.
 {#WoodFawcett}

* R. Guitart, J. Riguet, _Enveloppe Karoubienne de Cat&#233;gories de Kleisli_ , Cah. Top. Geom. Diff. Cat. **XXXIII** no.3 (1992) pp.261-266. ([pdf](http://archive.numdam.org/article/CTGDC_1992__33_3_261_0.pdf))

* {#LW11}[[Rory Lucyshyn-Wright|R. Lucyshyn-Wright]], _Totally Distributive Toposes_ , arXiv.1108.4032 (2011). ([pdf](http://arxiv.org/pdf/1108.4032v3))

* G. N. Raney, _Tight Galois Connections and Complete Distributivity_ , Trans.Amer.Math.Soc **97** (1960) pp.418-426. ([pdf](http://www.ams.org/journals/tran/1960-097-03/S0002-9947-1960-0120171-3/S0002-9947-1960-0120171-3.pdf))

* R. Rosebrugh, R. J. Wood, _Constructive complete distributivity IV_ , App. Cat. Struc. **2** (1994) pp.119-144. ([preprint](http://www.mta.ca/~rrosebru/articles/ccd4.pdf))

* [[Isar Stubbe|I. Stubbe]], _Towards "Dynamic Domains": Totally Continuous Complete Q-Categories_ , Theo. Comp. Sci. **373** no.1-2 (2007) pp.142-160.

[[!redirects completely distributive lattices]]
[[!redirects constructive completely distributive lattice]]
[[!redirects constructively completely distributive lattice]]
[[!redirects constructively completely distributive lattices]]
[[!redirects constructive completely distributive lattices]]
[[!redirects CCD lattice]]