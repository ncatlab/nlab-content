
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

A _modular tensor category_ is, roughly, a [[braided monoidal category]] that encodes the _topological_ structure underlying a [[rational CFT|rational]] 2-dimensional [[conformal field theory]]. In other words, it is a basis-independent formulation of _Moore-Seiberg data_.

It is in particular a [[fusion category]] that is also a [[ribbon category]] such that the "modularity operation" is non-degenerate (this is what the name "modular tensor category" comes from):

this means that for $i,j \in I$ indices for representatives of simple objects $U_i$, $U_j$, the matrix 
$$
  (s^{i j}) = (U_i\text{-circle threading through the} \, U_j\text{ -circle})
$$
is non-degenerate.

Here on the right what is meant is the diagram in the modular tensor category made from the identity morphisms, the duality morphisms and the braiding morphism on the objects $U_i$ and $U_j$ that looks like a figure-eight with one circle threading through the other, and this diagram is interpreted as an element in the endomorphism space of the tensor unit object, which in turn is canonically identified with the [[ground field]].

In the description of 2-dimensional [[conformal field theory]] in the [[FFRS-formalism]] it is manifestly this kind of modular diagram that encodes the torus partition function of the CFT. This explains the relevance of modular tensor categories in the description of [[conformal field theory]].

Since 2-dimensional conformal field theory is related by a [[holographic principle]] to 3-dimensional [[TQFT]], modular tensor categories also play a role there, which was in fact understood before the full application in conformal field theory was: in the [[Reshetikhin-Turaev model]].


## Definition ##

A **modular tensor category** is a [[category]] with the following long list of extra structure.

> needs to be put in more coherent form, just a stub

* it is an [[abelian category]], $\mathbb{C}$-linear (i.e. $Vect_{\mathbb{C}}$ [[enriched category]]), [[semisimple category]] [[monoidal category]] ([[tensor category]])

* the tensor unit is a simple object, $I$ 
  a finite set of representatives of isomorphism classes of simple objects

* [[fusion category]]

* [[braided monoidal category]]

* [[ribbon category]], in particular objects have [[dual objects|duals]]

* **modularity** a non-degeneracy condition on the [[braiding]] given by an [[isomorphism]] of algebras
  $$
    K(C) \otimes_{\mathbb{Z}} \stackrel{\simeq}{\to} End(Id_C)
  $$
  where
  $$
    [U] \mapsto \alpha_U
  $$
  where the transformation $\alpha_U$ is given on the simple object $V$ by
  $$
    \alpha_U(V) = \text{straight } V\text{-line encircled by } U\text{-loop}
  $$
  (on the right we use string diagram notation)

## Examples

### Rep categories of VOAs
 {#RepCategoriesOfVOAs}

#### General

Many modular tensor categories arise as [[representation]] categories of [[vertex operator algebras]] ([Huang 2005, Sec. 1](#Huang05); [Huang 2008](#Huang08); [Huang, Lepowski & Zhang 2014](#HuangLepowskiZhang14) see [EGNO 15, Sec. 8.27.6](#EGNO15)), hence of chiral [[field (physics)|fields]] of [[2d conformal field theories]]. 

(For [[logarithmic CFTs]] one still gets [[braided monoidal category|braided]] [[tensor categories]], see [Creutzig, Lentner & Rupert 2021](#CreutzigLentnerRupert21)).



#### Relation to conformal blocks
{#RelationToConformalBlocks}

 In this case the [[monoidal category|monoidal]]- and the [[braided monoidal category|braided]] [[structure]] (hence the modular tensor structure) on the underlying [[representation category]] is entirely fixed by the space of [[conformal blocks]] of the [[2d CFT]] on the [[Riemann sphere]] (the "genus zero conformal blocks"). 

This may be found highlighted in [EGNO 15, p. 266](#EGNO15), [Runkel, Sec. 4.3](#Runkel). The essentially equivalent fact that the genus=0 conformal blocks already determine the [[modular functor]] of the CFT is proven in [Andersen & Ueno 2012](modular+functor#AndersenUeno12).


#### Examples

A database of examples is given by ([Gannon & Höhn](#GannonHoehn)).

## Related concepts

* [[tensor category]]


## References

### General

Original article:

* [[Vladimir Turaev]], *Modular categories and 3-manifold invariants*,  International Journal of Modern Physics B Vol. 06, No. 11n12, pp. 1807-1824 (1992) ([doi:10.1142/S0217979292000876](https://doi.org/10.1142/S0217979292000876))

Review in the context of the [[Reshetikhin-Turaev construction]] of [[modular functors]]:

* [[Bojko Bakalov]], [[Alexander Kirillov]], *Modular Tensor Categories*, Ch. 3 in: *Lectures on tensor categories and modular functors*, University Lecture Series **21**, Amer. Math. Soc. (2001) &lbrack;[[BakalovKirillov-Ch3-ModularTensorCategories.pdf:file]],[web](http://www.math.stonybrook.edu/~kirillov/tensor/tensor.html), [ams:ulect/21](https://bookstore.ams.org/view?ProductCode=ULECT/21)&rbrack;

Review in the context of [[2d CFT]]/[[VOA]]

* [Fuchs-Runkel-Schweigert 02, Sec. 2.1](#FuchsRunkelSchweigert02)

* {#Runkel} [[Ingo Runkel]], *Algebra in Braided Tensor Categories and Conformal Field Theory* ([pdf](https://www.math.uni-hamburg.de/home/runkel/PDF/alg.pdf), [[Runkel-AlgebraInBTCAndCFT.pdf:file]])

and with focus on relation to [[braid representations]]:

* [[Colleen Delaney]], *Lecture notes on modular tensor categories and braid group representations*, 2019 ([pdf](http://web.math.ucsb.edu/~cdelaney/MTC_Notes.pdf), [[DelaneyModularTensorCategories.pdf:file]])


Construction of modular tensor categories from [[vertex operator algebras]]:

* {#Huang05} [[Yi-Zhi Huang]], *Vertex operator algebras, the Verlinde conjecture and modular tensor categories*, Proc. Nat. Acad. Sci. **102** (2005) 5352-5356 $[$[arXiv:math/0412261](http://arxiv.org/abs/math/0412261), [doi:10.1073/pnas.0409901102](https://doi.org/10.1073/pnas.0409901102)$]$

* {#Huang08} [[Yi-Zhi Huang]], *Rigidity and modularity of vertex tensor categories*,  Communications in Contemporary Mathematics **10** supp01 (2008) 871-911   $[$[arXiv:math/0502533](https://arxiv.org/abs/math/0502533), [doi:10.1142/S0219199708003083](https://doi.org/10.1142/S0219199708003083)$]$

* {#HuangLepowskiZhang14} [[Yi-Zhi Huang]], [[James Lepowsky]], Lin Zhang, *Logarithmic tensor category theory for generalized modules for a conformal vertex algebra, I: Introduction and strongly graded algebras and their generalized modules*,  In: Bai, Fuchs, Huang, Kong, Runkel, Schweigert (eds.), *Conformal Field Theories and Tensor Categories* Mathematical Lectures from Peking University. Springer (2014) $[$[arXiv:1012.4193](https://arxiv.org/abs/1012.4193), [doi:10.1007/978-3-642-39383-9_5](https://doi.org/10.1007/978-3-642-39383-9_5)$]$

* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], Section 8.27.6 of: *Tensor Categories*, AMS Mathematical Surveys and Monographs **205** (2015) &lbrack;[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205)&rbrack;

brief survey:

* [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Simon Wood]], [[Yang Yang]], pp. 5 of: *Algebraic structures in two-dimensional conformal field theory*, Encyclopedia of Mathematical Physics &lbrack;[arXiv:2305.02773](https://arxiv.org/abs/2305.02773)&rbrack;


and generalization to [[logarithmic CFT|logarithmic]] VOAs:

* {#CreutzigLentnerRupert21} [[Thomas Creutzig]], [[Simon Lentner]], [[Matthew Rupert]], *Characterizing braided tensor categories associated to logarithmic vertex operator algebras* $[$[arXiv:2104.13262](https://arxiv.org/abs/2104.13262)$]$


A list of examples (with an emphasis on [[representation categories]] of rational [[vertex operator algebras]]) is in

* {#GannonHoehn} [[Terry Gannon]], [[Gerald Höhn]], Hiroshi Yamauchi, _[The online database of Vertex Operator Algebras and Modular Categories](http://www.math.ksu.edu/~gerald/voas/)_

Classification results

* [[Eric Rowell]], [[Richard Stong]], [[Zhenghan Wang]], *On classification of modular tensor categories*, Comm. Math. Phys. **292** 2 (2009) 343--389 &lbrack;[arXiv:0712.1377](https://arxiv.org/abs/0712.1377), [doi:10.1007/s00220-009-0908-z](https://doi.org/10.1007/s00220-009-0908-z)&rbrack;

On [[number theory|number theoretic]] aspects of modular tensor categories:

* {#DavidovichHaggeWang2013} [[Orit Davidovich]], [[Tobias Hagge]], [[Zhenghan Wang]], _On Arithmetic Modular Categories_, arXiv preprit, 2013 &lbrack;[arXiv:1305.2229](https://arxiv.org/abs/1305.2229)&rbrack;



### Relation to 3dCS/2dWZW quantum field theory

Discussion of modular tensor categories in [[quantum field theory]] ([[3d TQFT]] and [[2d CFT]], as well as their relation via the [[AdS3-CFT2 and CS-WZW correspondence|CS/WZW correspondence]]) includes the following.

A general survey of the literature is in 

* [[Eric Rowell]], _From quantum groups to Unitary modular tensor categories_, Contemporary Mathematics 2005 ([arXiv:math/0503226](http://arxiv.org/abs/math/0503226))

See also

* [[Victor Ostrik]], _Tensor categories in conformal field theory_, talk notes 2011  ([pdf slides](http://pages.uoregon.edu/vostrik/talks/beijing.pdf))

More specific discussion in the context of [[2d CFT]] is in

* {#FuchsRunkelSchweigert02} [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _TFT construction of RCFT correlators I: partition functions_ ([arXiv:hep-th/0204148](http://arxiv.org/abs/hep-th/0204148))

  (for more along these lines see at _[[FRS formalism]]_)

Review of construction of MTCs from [[vertex operator algebras]] is in

* [[James Lepowsky]], _From the representation theory of vertex operator algebras to modular tensor categories in conformal field theory_ ([pdf](http://www.pnas.org/content/102/15/5304.full.pdf))

Discussion from the point of view of the [[cobordism hypothesis]] (see also the discussion at [[fusion category]]) is in 

* [[Bruce Bartlett]], [[Christopher Douglas]], [[Chris Schommer-Pries]], [[Jamie Vicary]], _Modular categories as representations of the 3-dimensional bordism 2-category_ ([arXiv:1509.06811](http://arxiv.org/abs/1509.06811))

On the [[Drinfeld center]]:

* {#GuuTham21} [[Jin-Cheng Guu]], [[Ying Hong Tham]]: *Explicit Factorization of a Categorical Center* &lbrack;[arXiv:2111.06919](https://arxiv.org/abs/2111.06919)&rbrack;



[[!include anyonic topological order via braided fusion categories -- references]]





  



[[!redirects modular tensor categories]]