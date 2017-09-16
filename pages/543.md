# Idea #

An _$A_\infty$-category_ is a kind of [[category]] in which the associativity condition on the [[composition]] of [[morphism]]s is relaxed "up to higher coherent homotopy".

The "A" is for Associative and the "${}_\infty$" indicates that associativity is relaxed up to higher homotopies without bound on the degree of the homotopies.

## ordinary linear $A_\infty$-categories ##

In what is strictly speaking a restrictive sense -- which is however widely and conventionally understood in [[homological algebra]] as the standard notion of $A_\infty$-category (see references below) -- the [[hom-space]]s of an $A_\infty$-category are taken to be linear spaces, i.e. [[module]]s over some [[ring]] or [[field]], and in fact [[chain complex]]es of such modules.

Therefore an $A_\infty$-category in this standard sense of [[homological algebra]] is a category which is in some way [[homotopical enrichment|homotopically enriched]] over a [[category of chain complexes]] $Ch$. Since a category which is [[enriched category|enriched]] in the ordinary sense of [[enriched category theory]] is a [[dg-category]], there is a close relation between $A_\infty$-categories and [[dg-category|dg-categories]].


$A_\infty$-categories in this linear sense are a [[horizontal categorification]] of the notion of [[A-infinity-algebra]]. As such they are to [[A-infinity-algebra]]s as [[Lie infinity-algebroid]]s are to [[L-infinity-algebra]]s. For this point of view see the Kontsevich-Soibelman reference below.

**Definition**

An $A_\infty$-category is a [[category over an operad]]
for the [[A-infinity operad]]: the free resolution 
in the context of dg-operads of the linear associative operad.


##Examples and remarks##

* Every [[dg-category]] may be regarded as a special case of an  [[A-infinity category]].

* Every $A_\infty$-category is $A_\infty$-equivalent to a [[dg-category]].

  * This is a corollary of the $A_\infty$-categorical [[Yoneda lemma]].
  
  * beware that this statement does not imply that the notion of 
  $A_\infty$-categories is obsolete (see section 1.8 in Bespalov et al.):
  in practice it is often easier to work with a given naturally
  arising $A_\infty$-category than constructing its equivalent [[dg-category]]
  
    * for instance when dealing with a [[Fukaya A_infinity-category]];
  
    * or when dealing with various constructions on dg-categories, for instance certain quotients,
that naturally yield directly $A_\infty$-categories instead of dg-categories.



## more general $A_\infty$-categories

In the widest sense, "$A_\infty$-category" may be used as a term for a category in which the [[composition]] operation constitutes an algebra over an [[operad]] which resolves in some sense the associative operad $Ass$.

One should be aware, though, that this use of the term is not understood by default in the large body of literature concerned with the above linear notion.

Examples for this are

* [[Trimble n-category|Trimble n-categories]];

* also the classical notion of [[bicategory]] can be interpreted as an $A_\infty$-category in [[Cat]] for a suitable Cat-operad.



# References #

## for $A_\infty$-categories in the sense of homological algebra ##

For a short and precise introduction see

* B. Keller, _Introduction to $A_\infty$-algebras and modules_ (<a href="http://people.math.jussieu.fr/~keller/publ/ioan.dvi">dvi</a>, <a href="http://people.math.jussieu.fr/~keller/publ/ioan.ps">ps</a>) and Addendum (<a href="http://people.math.jussieu.fr/~keller/publ/addendum.ps">ps</a>), Homology, Homotopy and Applications 3 (2001), 1-35; 

* B. Keller, _$A_\infty$ algebras, modules and functor categories_, (<a href="http://people.math.jussieu.fr/~keller/publ/ainffun.dvi">pdf</a>, <a href="http://people.math.jussieu.fr/~keller/publ/ainffun.ps">ps</a>).

and for a [[Fukaya category]]-oriented introduction see chapter 1 in 

* P. Seidel,  _Fukaya category and Picard-Lefschetz theory_,
<a href="http://web.archive.org/web/20070807231549/http://www.math.uchicago.edu/~seidel">draft version</a>


A very detailed treatment of $A_\infty$-categories is a recent book 

* Yu. Bespalov, V. Lyubashenko, O. Manzyuk, _Pretriangulated $A_\infty$-categories_, Proceedings of the Institute of Mathematics of NAS of Ukraine, vol. 76, Institute of Mathematics of NAS of Ukraine, Kyiv, 2008, 598 ([ps.gz](http://www.math.ksu.edu/~lub/cmcMonad.gz))

  * notice: the ps.gz file has different page numbers than the printed version, but the numbering of sections and formulae is final. Errata to published version are [here](http://www.math.ksu.edu/~lub/cmcMoCor.pdf).


The relation of $A_\infty$-categories to [[differential graded algebra]] is emphasized in the introduction of

* Maxim Kontsevich, Yan Soibelman, _Notes on A-infinity algebras, A-infinity categories and non-commutative geometry. I_ ([arXiv](http://arxiv.org/abs/math/0606241))

which mostly discusses just [[A-infinity-algebra]]s, but points out a generalizations to $A_\infty$-categories, see the overview on [p. 3](http://arxiv.org/PS_cache/math/pdf/0606/0606241v2.pdf#page=3)

Essentially the authors say that an $A_\infty$-category should be a non(-graded-)commutative [[NQ-supermanifold]]. Recall that a graded-commutative [[NQ-supermanifold]] is a [[L-infinity-algebroid]]. From this perspective one would want to think of a non-graded commutative [[NQ-supermanifold]] as an _$A_\infty$-algebroid_.


## for $A_\infty$-categories in the wider sense ##


If one understands $A_\infty$-category as "operadically defined higher category", then relevant references would include:

* Eugenia Cheng, _Comparing operadic definitions of $n$-category_ ([arXiv](http://arxiv.org/abs/0809.2070))


[[!redirects A-infinity category]]