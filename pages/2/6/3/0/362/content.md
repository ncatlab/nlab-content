
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

The **Gray tensor product** is a "better" replacement for the cartesian product of [[strict 2-category|strict 2-categories]] with respect to pseudonatural transformations.  To get the idea it suffices to consider the 2-category $\mathbf{2}$ which has two objects, 0 and 1, one non-identity morphism $0\to 1$, and no nonidentity 2-cells. Then the cartesian product $\mathbf{2}\times\mathbf{2}$ is a commuting square, while the Gray tensor product $\mathbf{2}\otimes\mathbf{2}$ is a square which commutes up to isomorphism.

More generally, given [[2-categories]] $C$ and $D$, a [[2-functor]] $C\times\mathbf{2} \to D$ consists of two 2-functors $C\to D$ and a strict 2-natural transformation between them, while a 2-functor $C\otimes\mathbf{2} \to D$ consists of two 2-functors $C\to D$ and a *[[pseudonatural transformation]]* between them.

## Definition 

Following up on the last comment, $B\otimes C$ can be defined by
$$ 
  2Cat(B\otimes C, D)   
   \cong 
  2Cat\big(B, Ps(C,D)\big) 
  \,,
$$
where $Ps(C,D)$ is the 2-category of [[2-functors]], [[pseudonatural transformations]], and [[modifications]] between $C$ and $D$. In other words, the category $2Cat$ of strict 2-categories  and strict 2-functors becomes a [[closed monoidal category|closed]] [[symmetric monoidal category]] with tensor product guven by the Gray tensor $\otimes$ and [[internal hom]] given by $Ps(-,-)$.

## Remarks 

* When considered with this monoidal structure, $2Cat$ is often called $Gray$.  [[Gray-category|Gray-categories]], or categories [[enriched category|enriched]] over $Gray$, are a model for [[semi-strict infinity-category|semi-strict]] 3-categories.  Categories enriched over $2Cat$ with its cartesian product are _strict_ 3-categories, which are not as useful.  This is one precise sense in which the Gray tensor product is "more correct" than the cartesian product.

* $Gray$ is an example of a [[semicartesian monoidal category]], i.e. a non-[[cartesian monoidal category|cartesian]] monoidal category whose unit object is nevertheless the terminal object.

* There are also versions of the Gray tensor product in which pseudonatural transformations are replaced by lax or oplax ones.  (In fact, these were the ones originally defined by Gray.)

* $Gray$ is actually a monoidal [[model category]] (that is, a model category with a monoidal structure that interacts well with the model structure), which $2Cat$ with the cartesian product is not.  In particular, the cartesian product of two cofibrant 2-categories need not be cofibrant.  This is another precise sense in which the Gray tensor product is "more correct" than the cartesian product.

* The cartesian monoidal structure is sometimes called the "black"  product, since the square $2\times 2$ is "completely filled in" (i.e. it commutes).  There is another "white" tensor product in which the square $2\Box 2$ is "not filled in at all" (doesn't commute at all), and the "gray" tensor product is in between the two (the square commutes up to an isomorphism).  This is a pun on the name of John Gray, for whom the Gray tensor product is named.  The "white" tensor product is also called the [[funny tensor product]].

* There are generalizations to [[higher category theory|higher categories]] of the Gray tensor product. In particular there is a tensor product on [[strict omega-category|strict omega-categories]] -- the [[Crans-Gray tensor product]] -- which is such that restricted to strict 2-categories it reproduces the Gray tensor product.

* A  [[closed monoidal category|closed monoidal structure]] on [[strict omega-category|strict omega-categories]] is introduced by Al-Agl, Brown and Steiner. This uses an equivalence between the categories of strict (globular) omega categories and of strict  cubical omega categories with connections; the construction of the closed  monoidal  structure on the latter category is direct and generalises that for strict cubical omega groupoids with connections established by Brown and Higgins.

* The Gray tensor product cannot be extended to a [[2-functor]] (or 3-functor) on the [[2-category]] of 2-categories, 2-functors, [[2-natural transformations]], and [[modifications]]. See [this MathOverflow answer](https://mathoverflow.net/a/459360).

## Related entries

* [[Crans-Gray tensor product]]

* [[generalized Gray tensor product]]

* [[Verity-Gray tensor product]]

## References

### In 2-category theory

Original discussion of the Gray tensor product in [[2-category theory]]:

* [[John W. Gray]], Theorem 1,4.14 of: _Formal category theory: adjointness for 2-categories_, Lecture Notes in Mathematics, Vol. 391. Springer-Verlag, Berlin-New York, 1974. xii+282 pp doi:[10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280) (see also [[Adjointness for 2-Categories]])

* [[John W. Gray]], _Coherence for the Tensor Product of 2-Categories, and Braid Groups_ , pp.62-76 in Heller, [[Myles Tierney|Tierney]] (eds.), _Algebra, Topology, and Category Theory_ , Academic Press New York 1976.

* [[Robert Gordon]], [[John Power]], [[Ross Street]]:  _Coherence for tricategories_, Mem. Amer. Math. Soc. **117** 558 (1995) &lbrack;[doi:10.1090/memo/0558](http://dx.doi.org/10.1090/memo/0558), [ams:memo-117-558](https://bookstore.ams.org/memo-117-558/)&rbrack;

* [[Stephen Lack]], _A Quillen model structure for 2-categories_, K-Theory, 26(2) (2002) pp171-205, ([gzipped .ps](http://maths.mq.edu.au/~slack/papers/qmc2cat.ps.gz)) (doi:[10.1023/A:1020305604826](https://doi.org/10.1023/A:1020305604826) - requires Portico subscription)

* [[Stephen Lack]], _A Quillen model structure for bicategories_, K-theory, 33(3) (2004) pp185-197, ([gzipped .ps](http://maths.mq.edu.au/~slack/papers/qmcbicat.ps.gz)) (doi:[10.1007/s10977-004-6757-9](https://doi.org/10.1007/s10977-004-6757-9) - requires Portico subscription)

* [[Ronnie Brown]] and P.J. Higgins, Tensor products and homotopies for $\omega$-groupoids and crossed complexes,  J. Pure Appl. Alg. 47 (1987) 1-33. doi:[10.1016/0022-4049(87)90099-5](https://doi.org/10.1016/0022-4049(87%2990099-5), ([pdf](https://pdfs.semanticscholar.org/3323/d82ed1effb1953a6af573aab2e3fb0b02394.pdf))

* F.A. Al-Agl, R. Brown and   R. Steiner, _Multiple categories: the equivalence between a globular and cubical approach_, Advances in Mathematics, 170 (2002) 71-118. doi:[10.1006/aima.2001.2069](https://doi.org/10.1006/aima.2001.2069), arXiv:[math/0007009](https://arxiv.org/abs/math/0007009)

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], section 12.2 of: *2-Dimensional Categories*, Oxford University Press (2021) &lbrack;[arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378)&rbrack;


On the Gray tensor product as the [[left Kan extension]] of a tensor product on the full subcategory $Cu$ of $2Cat$:

* [[Ross Street]], p. 16 of: _Gray's tensor product of 2-categories_, 22-page handwritten note, (1988) &lbrack;[pdf](http://maths.mq.edu.au/~street/GrayTensor.pdf)&rbrack;

A general theory of lax tensor products, unifying Gray tensor products with the [[Crans-Gray tensor product]] is in 

* [[Michael Batanin]], [[Denis-Charles Cisinski]], [[Mark Weber]], _Multitensor lifting and strictly unital higher category theory_ ([arXiv:1209.2776](http://arxiv.org/abs/1209.2776))

A proof that the Gray tensor product does form a monoidal structure, based only on its universal property, is in

* [[John Bourke]], [[Nick Gurski]], _The Gray tensor product via factorisation_, Appl Categor Struct **25** (2017) p603-624, doi:[10.1007/s10485-016-9467-6](https://doi.org/10.1007/s10485-016-9467-6), arXiv:[1508.07789](http://arxiv.org/abs/1508.07789)

On its generalization to [[Gray-category|Gray-categories]]

* [[Sjoerd Crans]]. "A tensor product for $Gray$-categories". *Theory and applications of categories*, 5(2), 12-69. ([tac](http://www.tac.mta.ca/tac/volumes/1999/n2/5-02abs.html)) ([pdf](http://www.tac.mta.ca/tac/volumes/1999/n2/n2.pdf))

### In [[enhanced 2-category]] theory

* [[Nathanael Arkor]], [[John Bourke]], and [[Joanna Ko]], _Enhanced 2-categorical structures, two-dimensional limit sketches and the symmetry of internalisation_, [arXiv:2412.07475](https://arxiv.org/abs/2412.07475) (2024).

### In $(\infty,2)$-category theory
 {#ReferencesInInfinity2CategoryTheory}

Discussion of the Gray tensor product in [[(infinity,2)-category|$(\infty,2)$-category]] theory:

* {#GaitsgoryRozenblyum17} [[Dennis Gaitsgory]], [[Nick Rozenblyum]]: *Lax functors and the Gray product*, Chapter 10.3 in the Appendix of: *[[A study in derived algebraic geometry]]*, Mathematical Surveys and Monographs **221**, Americal Mathematical Society (2017) &lbrack;[ams:SURV/221](https://bookstore.ams.org/view?ProductCode=SURV/221), [book webpage](https://people.mpim-bonn.mpg.de/gaitsgde/Book/)&rbrack;

* [[Félix Loubaton]], [[Jaco Ruit]]: *On the squares functor and the Gaitsgory-Rozenblyum conjectures* &lbrack;[arXiv:2507.07807](https://arxiv.org/abs/2507.07807)&rbrack;

* {#Loubaton25} [[Félix Loubaton]], answer to: *The missing proofs in Gaitsgory–Rozenblyum's derived algebraic geometry book* (Jul 2025) &lbrack;[MO:a/497541](https://mathoverflow.net/a/497541/)&rbrack;


[[!redirects Gray tensor products]]

[[!redirects Gray]]




