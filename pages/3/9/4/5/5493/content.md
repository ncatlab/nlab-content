
# Contents
* contents
{: toc}

## Idea

A **sesquicategory** is a (strict) [[2-category]] except for the fact that the [[interchange law]] need not hold.


## Definition

Sesquicategories can be straightforwardly defined just as for strict [[2-categories]] except with the interchange law left out.  (In order for this to make sense, one has to spell out the definition explicitly enough that the interchange law is a separate axiom.)  This means that composition in a sesquicategory cannot be [[functor]] $\hom(y,z)\times \hom(x,y)\to\hom(x,z)$.  So sesquicategories are more usually defined as categories [[enriched category|enriched in]] [[Cat]], where the monoidal structure for the enrichment is not the usual cartesian product but the [[funny tensor product]], i.e. the tensor adjoint to the 'unnatural' hom, in which the hom-category $[C,D]$ has morphisms given by $C$-indexed families of arrows of $D$ _without_ any naturality requirement.

Alternatively, a sesquicategory may be given as a category $C$ together with a functor $H \colon C^{op} \times C \to Cat$ whose composite $ob \circ H \colon C^{op} \times C \to Cat \to Set$ with the underlying-set functor is equal to the hom functor of $C$.  Because of the equivalence $[C, Cat(D)] \simeq Cat [C,D]$ (for [[finitely complete category|finitely complete]] $D$), this is the same as saying that a sesquicategory is given by a category $C$ together with an internal category $H$ in $[C^{op} \times C, Set]$ whose object $H_0$ of objects is the [[hom functor]] $hom_C$ of $C$.

## Remarks

A strict [[premonoidal category]] is the same as a sesquicategory with exactly one object.

A [[Gray-category]] does not have an underlying [[strict 2-category]], but it does have an underlying strict sesquicategory.  Thus, if one wants to define Gray-[[computads]], it is natural to work with "sesqui-computads" as a partway stage; see for instance [[toddtrimble:Surface diagrams]]

The name 'sesquicategory' literally means $1\frac{1}{2}$-category, although strictly speaking they are actually *more* general than $2$-categories (which are of course more general than $1$-categories).  However, one can also view a $2$-category or sesquicategory as a $1$-category with [[extra structure]] or stuff (the $2$-cells and their composition), and in this way sesquicategories are partway between $1$-categories and $2$-categories, with only one axiom left out.  (A [[strict 2-category]] can be considered directly as a 1-category with additional 2-cells added; for a weak 2-category one has instead to consider its "underlying" 1-category to be its [[homotopy category]] obtained by identifying isomorphic 1-morphisms.)

The paper [Stell (1994)](#Stell) shows the relation with rewriting. 

The paper [Brown (2010)](#Brown) shows how a sesquicategory arises from a whiskered category. 


## References

* [this discussion](http://www.mta.ca/~cat-dist/catlist/1999/2-cats-without) on the categories list.
{#catlist}

* {#Stell} [[John Stell]], _Modelling Term Rewriting Systems by Sesqui-Categories_, Proc. Catégories, Algèbres, Esquisses et Néo-Esquisses (1994). &lbrack;<a href='/nlab/files/Stell.pdf' title='Modelling Term Rewriting Systems by Sesqui-Categories'>pdf</a>&rbrack;

* {#Street} [[Ross Street]], _Categorical Structures_, Handbook of Algebra, Vol. 1, 1996, pp. 531-577. &lbrack;<a href="https://doi.org/10.1016/S1570-7954(96)80019-2">doi:10.1016/S1570-7954(96)80019-2</a>, [[Street-CategoricalStructures.pdf:file]]&rbrack;

* {#Brown} [[Ronnie Brown]], Possible connections between whiskered categories and groupoids, Leibniz algebras, automorphism structures and local-to-global questions. J. Homotopy Relat. Struct., 5(1) (2010) 305--318.
&lbrack; [arXiv:0708.1677](https://arxiv.org/abs/0708.1677) [PDF](https://tcms.org.ge/Journals/JHRS/xvolumes/2010/n1a15/v5n1a15hl.pdf) &rbrack;

* [[Nelson Martins-Ferreira]], _Low-dimensional internal categorial structures in weakly Mal'cev sesquicategories_, PhD thesis, University of Cape Town (2008). &lbrack; [url](http://hdl.handle.net/11427/4907) &rbrack;


[[!redirects sesquicategory]]
[[!redirects sesquicategories]]
