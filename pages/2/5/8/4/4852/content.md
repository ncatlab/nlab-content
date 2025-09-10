> This page is about the generalisation of an [[adjunction]] to [[bicategories]]. Instead, for functors $L$ which are both left and right adjoints see *[[ambidextrous adjunction]]*.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

_Biadjunctions_ are the "maximally weak" kind of [[2-adjunctions]]: a [[categorification|higher generalization]] of the notion of [[adjunction]] from [[category theory]] to [[2-category theory]], and specifically to [[bicategories]] (or more generally internally in a [[tricategory]].  See [[2-adjunction]] for other kinds of 2-adjunction.

## Definition

### Incoherent versions

Given (possibly weak) [[2-categories]], $A$ and $C$, and (possibly weak) [[2-functors]] $F:A\to C$ and $U:C\to A$, a __biadjunction__ is given by specifying for each object $a$ in $A$ and each object $c$ in $C$ an [[equivalence of categories]] $C(F a,c)\cong A(a,U c)$, which is [[pseudonatural transformation|pseudonatural]] both in $a$ and in $c$. 

By the [[Yoneda lemma for bicategories]], this is equivalent to giving pseudonatural transformations $\eta : Id_A \to U F$ and $\varepsilon : F U \to Id_C$ satisfying the [[triangle identities]] up to invertible [[modifications]].  This latter definition can be internalized in any (weak) [[3-category]], such as a [[Gray-category]] or a [[tricategory]].

### Coherent versions

Both the "equivalence of hom-categories" definition and the "unit and counit" definition have stronger "coherent" versions:  We can ask the equivalences $C(F a,c)\cong A(a,U c)$ to be [[adjoint equivalences]], or for the "triangulator" modifications to satisfy the [[lax 2-adjunction#definition|swallowtail equations]].  These two conditions are roughly equivalent, and any "incoherent" biadjunction can be improved to a coherent one by altering one of the triangulators; see [Gurski](#Gurski12), [Riehl-Verity](#RV15), [Pstr&#261;gowski](#Pstr&#261;gowski14), [Riehl-Shulman](#RS17), and [this proof](http://globular.science/1512.006) in [[Globular]].


## Related concepts

* [[adjoint functor]], [[adjoint triple]], [[adjoint quadruple]]

* [[proadjoint]], [[Hopf adjunction]]

* [[2-adjunction]]
  
  **biadjunction**, [[lax 2-adjunction]], [[pseudoadjunction]]

* [[pseudoadjunction]]

* [[biequivalence]], [[biadjoint biequivalence]]

* [[adjoint (infinity,1)-functor]]


## References

* [[John Gray]], _[[Gray-adjointness-for-2-categories|Formal category theory: Adjointness for 2-categories]]_, Lecture Notes in Mathematics __391__, Springer, Berlin, 1974.

* [[Thomas M. Fiore]], _Pseudo limits, biadjoints, and pseudo algebras: categorical foundations of conformal field theory_, Memoirs of the American Mathematical Society __182__ (2006), no. 860. 171 pages, [MR2007f:18006](http://www.ams.org/mathscinet-getitem?mr=2007f:18006),  [math.CT/0408298](http://arxiv.org/abs/math.CT/0408298)

* {#Gurski12} [[Nick Gurski]], _Biequivalences in tricategories_, Theory and applications of categories 2012, [journal web site](http://www.tac.mta.ca/tac/volumes/26/14/26-14abs.html), [arxiv](https://arxiv.org/abs/1102.0979)


* {#RV15} [[Emily Riehl]] and [[Dominic Verity]], _Homotopy coherent adjunctions and the formal theory of monads_, 2015, [arxiv](https://arxiv.org/abs/1310.8279)

* 
{#Pstr&#261;gowski14} [[Piotr Pstrągowski]]: *On dualizable objects in monoidal bicategories, framed surfaces and the Cobordism Hypothesis*, Theory and Applications of Categories **38** 9 (2022)  257-310.  &lbrack;[tac:38-09](http://www.tac.mta.ca/tac/volumes/38/9/38-09abs.html) ,[arXiv:1411.6691](https://arxiv.org/abs/1411.6691)&rbrack;

* {#RS17} [[Emily Riehl]] and [[Mike Shulman]], _A type theory for synthetic ∞-categories_, 2017, [arxiv](https://arxiv.org/abs/1705.07442)



[[!redirects biadjunctions]]
[[!redirects biadjoint]]
[[!redirects biadjoints]]

