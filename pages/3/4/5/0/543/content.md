+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--





#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

An _$A_\infty$-category_ is a kind of [[category]] in which the associativity condition on the [[composition]] of [[morphism]]s is relaxed "up to higher coherent homotopy".

The "A" is for Associative and the "${}_\infty$" indicates that associativity is relaxed up to higher homotopies without bound on the degree of the homotopies.

In the most wide-spread use of the word $A_\infty$-categories are _linear_ categories in that they have [[hom-object]]s that are [[chain complex]]es. These are really models/presentations for [[stable (∞,1)-category|stable (∞,1)-categories]].

If the composition in the linear $A_\infty$-category does happen to be strictly associative it becomes the same as a [[dg-category]]. In fact, every linear $A_\infty$-category is $A_\infty$-equivalent to a [[dg-category]]. In this way, we have that $A_\infty$-categories related to [[dg-category|dg-categories]] as models for [[stable (∞,1)-category|stable (∞,1)-categories]] in roughly the same way as [[quasi-category|quasi-categories]] relate to [[simplicially enriched category|simplicially enriched categories]] as models for [[(∞,1)-category|(∞,1)-categories]]: the former is the general incarnation, while the latter is a [[semi-strict infinity-category|semi-strictified]] version.



## Ordinary linear $A_\infty$-categories ##

In what is strictly speaking a restrictive sense -- which is however widely and conventionally understood in [[homological algebra]] as the standard notion of $A_\infty$-category (see references below) -- the [[hom-space]]s of an $A_\infty$-category are taken to be linear spaces, i.e. [[module]]s over some [[ring]] or [[field]], and in fact [[chain complex]]es of such modules.

Therefore an $A_\infty$-category in this standard sense of [[homological algebra]] is a category which is in some way [[homotopical enrichment|homotopically enriched]] over a [[category of chain complexes]] $Ch$. Since a category which is [[enriched category|enriched]] in the ordinary ?dg? sense of [[enriched category theory]] is a [[dg-category]], there is a close relation between $A_\infty$-categories and [[dg-category|dg-categories]].


$A_\infty$-categories in this linear sense are a [[horizontal categorification]] of the notion of [[A-infinity-algebra]]. As such they are to [[A-infinity-algebra]]s as [[Lie infinity-algebroid]]s are to [[L-infinity-algebra]]s. For this point of view see the Kontsevich--Soibelman reference below.

+-- {: .un_defn}
###### Definition

A category $C$ such that

1. for all $X,Y$ in $Ob(C)$ the [[hom-set|Hom-set]]s $Hom_C(X,Y)$ are finite dimensional [[chain complex]]es of $\mathbf{Z}$-graded modules

2. for all objects $X_1,...,X_n$ in $Ob(C)$ there is a family of linear composition maps (the higher compositions)
$m_n : Hom_C(X_0,X_1) \otimes Hom_C(X_1,X_2) \otimes \cdots \otimes Hom_C(X_{n-1},X_n) \to Hom_C(X_0,X_n)$ of degree $n-2$ (homological grading convention is used) for $n\geq1$

3. $m_1$ is the differential on the chain complex $Hom_C(X,Y)$

4. $m_n$ satisfy the quadratic $A_\infty$-associativity equation for all $n\geq0$.
=--

$m_1$ and $m_2$ will be [[chain complex|chain map]]s but the compositions $m_i$ of higher order are not chain maps, nevertheless they are [[Massey product]]s.
 
The framework of dg-categories and dg-functors is too narrow for many problems, and it is preferable to consider the wider class of $A_\infty$-categories and $A_\infty$-functors. Many features of $A_\infty$-categories and $A_\infty$-functors come from the fact that they form a symmetric closed [[multicategory]], which is revealed in the language of [[comonad|comonads]].

From a higher dimensional perspective $A_\infty$-categories are weak $\omega$-categories with all morphisms invertible. $A_\infty$-categories can also be viewed as noncommutative formal dg-manifolds with a closed marked subscheme of objects.


## Examples and remarks ##

* Every [[dg-category]] may be regarded as a special case when there are no higher maps (trivial homotopies) of an $A_\infty$-category.

* Every $A_\infty$-category is $A_\infty$-equivalent to a [[dg-category]].

  * This is a corollary of the $A_\infty$-categorical [[Yoneda lemma]].
  
  * beware that this statement does not imply that the notion of 
  $A_\infty$-categories is obsolete (see section 1.8 in Bespalov et al.):
  in practice it is often easier to work with a given naturally
  arising $A_\infty$-category than constructing its equivalent [[dg-category]]
  
    * for instance when dealing with a [[Fukaya A-infinity-category|Fukaya]] $A_\infty$-category;
  
    * or when dealing with various constructions on dg-categories, for instance certain quotients,
that naturally yield directly $A_\infty$-categories instead of dg-categories.

* The [[path space ]] of a topological space $X$

* The [[Fukaya category]] $Fuk(X)$ of a topological space $X$ -- a [[Calabi-Yau A-∞ category]]

* $A_\infty$-[[A-infinity-algebra|algebras]] as $A_\infty$-categories with one object.

* The [[loop space]] $\Omega{X}$ of a topological space $X$



## More general $A_\infty$-categories ##

In the widest sense, "$A_\infty$-category" may be used as a term for a category in which the [[composition]] operation constitutes an algebra over an [[operad]] which resolves in some sense the associative operad $Ass$.

One should be aware, though, that this use of the term is not understood by default in the large body of literature concerned with the above linear notion.

A less general but non-linear definition is fairly straight forward in any category in which there is a notion of _homotopy_ with the usual properties.
+-- {: .un_defn}
###### Definition

An $A_\infty$-category is a [[category over an operad|category over]]
the $A_\infty$-[[A-infinity operad|operad]]: e.g. the free resolution 
in the context of dg-operads of the linear associative operad.
=--

+-- {: .un_example}
###### Examples

* [[Trimble n-category|Trimble n-categories]];

* also the classical notion of [[bicategory]] can be interpreted as an $A_\infty$-category in [[Cat]] for a suitable Cat-operad.
=--


# References #

## For $A_\infty$-categories in the sense of homological algebra ##

For a short and precise introduction see

* B. Keller, _Introduction to $A_\infty$-algebras and modules_ (<a href="http://people.math.jussieu.fr/~keller/publ/ioan.dvi">dvi</a>, <a href="http://people.math.jussieu.fr/~keller/publ/ioan.ps">ps</a>) and Addendum (<a href="http://people.math.jussieu.fr/~keller/publ/addendum.ps">ps</a>), Homology, Homotopy and Applications 3 (2001), 1-35; 

* B. Keller, _$A_\infty$ algebras, modules and functor categories_, (<a href="http://people.math.jussieu.fr/~keller/publ/ainffun.dvi">pdf</a>, <a href="http://people.math.jussieu.fr/~keller/publ/ainffun.ps">ps</a>).

and for a [[Fukaya category]]-oriented introduction see chapter 1 in 

* P. Seidel,  _Fukaya category and Picard-Lefschetz theory_,
<a href="http://web.archive.org/web/20070807231549/http://www.math.uchicago.edu/~seidel">draft version</a>

A very detailed treatment of $A_\infty$-categories is a recent book 

* Yu. Bespalov, V. Lyubashenko, O. Manzyuk, _Pretriangulated $A_\infty$-categories_, Proceedings of the Institute of Mathematics of NAS of Ukraine, vol. 76, Institute of Mathematics of NAS of Ukraine, Kyiv, 2008, 598 ([ps.gz](http://www.math.ksu.edu/~lub/cmcMonad.gz))

  * notice: the ps.gz file has different page numbers than the printed version, but the numbering of sections and formulae is final. Errata to published version are [here](http://www.math.ksu.edu/~lub/cmcMoCor.pdf).

The relation of $A_\infty$-categories to [[differential graded algebra]]s is emphasized in the introduction of

* Maxim Kontsevich, Yan Soibelman, _Notes on A-infinity algebras, A-infinity categories and non-commutative geometry. I_ ([arXiv](http://arxiv.org/abs/math/0606241))

which mostly discusses just [[A-infinity-algebra]]s, but points out a generalizations to $A_\infty$-categories, see the overview on [p. 3](http://arxiv.org/PS_cache/math/pdf/0606/0606241v2.pdf#page=3)

Essentially the authors say that an $A_\infty$-category should be a non(-graded-)commutative [[NQ-supermanifold]]. Recall that a graded-commutative [[NQ-supermanifold]] is a [[L-infinity-algebroid]]. From this perspective one would want to think of a non-graded commutative [[NQ-supermanifold]] as an _$A_\infty$-algebroid_.


## For $A_\infty$-categories in the wider sense ##

If one understands $A_\infty$-category as "operadically defined higher category", then relevant references would include:

* Eugenia Cheng, _Comparing operadic definitions of $n$-category_ ([arXiv](http://arxiv.org/abs/0809.2070))


[[!redirects A-infinity category]]
[[!redirects A-infinity categories]]
[[!redirects A-∞ category]]
[[!redirects A-∞ categories]]
[[!redirects A? category]]
[[!redirects A? categories]]
[[!redirects A∞-category]]
[[!redirects A∞-categories]]
[[!redirects A-∞-category]]
[[!redirects A-∞-categories]]
