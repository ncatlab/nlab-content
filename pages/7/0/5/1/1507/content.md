
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition 

A **split idempotent** in a [[category]] $C$ is a [[morphism]] $e: A \to A$ which has a [[retract]], meaning there exists an [[object]] $B$ and morphisms $r: A \to B$ and $s: B \to A$ such that $s \circ r = e$ but $r \circ s = 1_B$. 

In an [[abelian category|abelian]] or [[semi-abelian category]], a _splitting_ of an [[exact sequence]] 

$$1 \to A \stackrel{i}{\to} B \stackrel{q}{\to} C \to 1$$

is given by a [[section]] $j: C \to B$ of $q$. This yields an idempotent $\pi = j \circ q$; in the abelian category case, this yields a further idempotent $1_B - \pi$ which is canonically split by a further retraction of $i: A \to B$, thus yielding a [[biproduct]] diagram. 

## Properties 

* Any split idempotent is an [[idempotent]], since
   $$ e \circ e = (s \circ r) \circ (s \circ r) = s \circ (r \circ s) \circ r = s \circ 1_B \circ r = s \circ r = e .$$

*  The splitting of an idempotent $e$ is both the [[limit]] and the [[colimit]] of the diagram containing only two [[parallel morphisms|parallel]] [[endomorphisms]] of $A$, namely $e$ and the identity.  Splittings of idempotents are preserved by any functor, making them [[absolute limit|absolute]] (co)limits.  In ordinary (i.e. [[enriched category|unenriched]]) categories, every absolute (co)limit can be constructed from split idempotents.  Thus, the [[Cauchy complete category|Cauchy completion]] of an ordinary ([[Set]]-enriched) category is just its completion under split idempotents.

* A category in which all idempotents split is called [[idempotent complete (infinity,1)-category|idempotent complete]]. The free completion of a category under split idempotents is also called its [[Karoubi envelope]].

## Examples

+-- {: .num_prop #InTrinagulatedCategoryWithDirectSumsOfTrianglesAllIdempotentsSplit}
###### Proposition

Let $\mathcal{T}$ be a [[triangulated category]] such that in addition to the existence of small [[direct sums]] the objectwise direct sum of any small family of distinguished triangles is itself a distinguished triangle ([B&#246;kstedt-Neeman 93, def. 1.2](#BokstedtNeeman93)).

Then in $\mathcal{T}$ all idempotents split.

=--

([B&#246;kstedt-Neeman 93, prop. 3.2](#BokstedtNeeman93))

+-- {: .num_remark #SchnurerCounterexample}
###### Remark

Prop. \ref{InTrinagulatedCategoryWithDirectSumsOfTrianglesAllIdempotentsSplit} is false under the weaker hypothesis of only binary/finite [[direct sums]]. 
A counter-example is in [Schnürer 11, Remark 3.2](#Schnurer11)

=--

## Related concepts

* [[Cauchy complete category]]

* [[idempotent completion]]

* [[pseudo-abelian category]]

## References

* [[Francis Borceux]], Section 6.5 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory* &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;

In [[triangulated categories]]:

* {#BokstedtNeeman93} [[Marcel Bökstedt]], [[Amnon Neeman]], _Homotopy limits in triangulated categories_, Compositio Mathematica, tome 86, no 2 (1993) p. 209-234 ([numdam](http://www.numdam.org/item?id=CM_1993__86_2_209_0))

* {#Schnurer11} Olaf M. Schnürer, _Homotopy categories and idempotent completeness, weight structures and weight complex functors_ ([arXiv:1107.1227](https://arxiv.org/abs/1107.1227))

On split idempotents in [[Kleisli categories]]:

* [[Rene Guitart]] and J. Riguet. _Enveloppe Karoubienne de catégories de Kleisli_, Cahiers de topologie et géometrie différentielle catégoriques 33.3 (1992): 261-266. ([Numdam](http://www.numdam.org/item/CTGDC_1992__33_3_261_0/))

* [[Robert Rosebrugh]] and [[Richard Wood]], _Split structures_, [[TAC]] 13.12 (2004): 172-183. ([TAC](https://www.tac.mta.ca/tac/volumes/13/12/13-12abs.html))

* {#Menni09}[[Matías Menni]], _Algebraic categories whose projectives are explicitly free_ , TAC **22** no.20 (2009) pp.509-541. ([abstract](http://www.tac.mta.ca/tac/volumes/22/20/22-20abs.html))

* [[Dusko Pavlovic]] and Peter-Michael Seidel. _Quotients in monadic programming: Projective algebras are equivalent to coalgebras_, 2017 32nd Annual ACM/IEEE Symposium on Logic in Computer Science (LICS). IEEE, 2017.

[[!redirects split idempotents]]
[[!redirects splitting]]
[[!redirects splittings]]
[[!redirects splitting of idempotents]]
[[!redirects idempotent splitting]]
