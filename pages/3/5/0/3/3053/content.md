
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

A **bifibration** of [[category|categories]] is a [[functor]]

$$
  E \to B
$$

that is both a [[Grothendieck fibration]] as well as an [[opfibration]].

Therefore every morphism $f \colon b_1 \to b_2$ in a bifibration has both a push-forward $f_* : E_{b_1} \to E_{b_2}$ as well as a pullback $f^* : E_{b_2} \to E_{b_1}$.


## Examples

* For $C$ any [[category]] with [[pullback]]s, the [[codomain fibration]] $cod : [I,C] \to C$ is a bifibration.

* Dually, for $C$ any [[category]] with [[pushout]]s, the [[domain opfibration]] $dom : [I,C] \to C$ is a bifibration.

* The canonical functor [[Mod]] $\to $ [[CRing]] is a bifibration.

* The [[forgetful functor]] [[Top]] $\to$ [[Set]] is a bifibration. See also [[topological concrete category]].

* The [[forgetful functor]] [[Grpd]] $\to$ [[Set]] is a bifibration.

* The [[forgetful functor]] [[Cat]] $\to$ [[Set]] is a bifibration.

## Properties

### Relation to pseudofunctors in adjoints
 {#RelationToPseudofunctors}

\begin{proposition}
  Under the [[Grothendieck construction]], the [[Grothendieck fibrations]] which arise from [[pseudofunctors]] $\mathcal{B} \longrightarrow Cat$ that factor through [[CatAdj|$Cat_{Adj}$]] are equivalently the [[bifibrations]].
\end{proposition}
This may be [[category theory]] [[folklore]]; a proof has been spelled out in [Harpaz & Prasma (2015), Prop. 2.2.1](#HarpazPrasma15).

\begin{remark}
\label{BifibrationsOfModelCategories}
Further factoring through [[ModCat]] $ \longrightarrow Cat_{Ajd}$ hence yields bifibrations of [[model categories]] &lbrack;[Harpaz & Prasma (2015), Sec. 3](#HarpazPrasma15); [Cagne & Melliès (2020)](#CagneMelliès20)&rbrack;. See at *[[model structures on Grothendieck constructions]]* for more on this.
\end{remark}



### Relation to monadic descent
 {#RelationToMonadicDescent}

Ordinary [[Grothendieck fibrations]] correspond to [[pseudofunctors]] to [[Cat]], by the [[Grothendieck construction]] and hence to [[stack|prestacks]]. For these one may consider [[descent]].

If the fibration is a bifibration, there is a particularly elegant algebraic way to encode its descent properties; this is [[monadic descent]]. The [[Benabou–Roubaud theorem]] characterizes descent properties for bifibrations.

### Relation to distributive laws

Fibrations and opfibrations on a category $C$ (or more generally an object of a suitable 2-category) are the algebras for a pair of pseudomonads.  If $C$ has pullbacks, there is a [[pseudo-distributive law]] between these pseudomonads, whose joint algebras are the bifibrations satisfying the [[Beck-Chevalley condition]]; see [(von Glehn)](#vonGlehn).



## Bifibration of bicategories

The basic theory of [[2-fibrations]], fibrations of bicategories, is developed in ([Buckley](#Buckley)). One (unpublished) proposal by Buckley and Shulman, for a "2-bifibration", a bifibration of [[bicategories]], is a functor of bicategories that is both a 2-fibration and a 2-opfibration. This should correspond to a pseudofunctor into $2 Cat_{adj}$, just as for 1-categories.  There is a difference from this case, however, in that although a 2-fibration (corresponding to a "doubly contravariant" pseudofunctor $B^{coop} \to 2Cat$) has both cartesian lifts of 2-cells and 1-cells, a 2-opfibration (corresponding to a totally *covariant* pseudofunctor $B\to 2Cat$) has opcartesian lifts of 1-cells but still *cartesian* lifts of 2-cells.

## Related concepts

* [[Grothendieck fibration]]

* [[Beck-Chevalley condition]]

* [[hyperdoctrine]]

* A bifibration $F:E\to B$ such that the transition functors also have *right* adjoints is sometimes called a [[trifibration]] (cf. Pavlovi&#263; 1990, p.315) or $\ast$-bifibration.


## References

* [[Dusko Pavlovic|Duško Pavlović]], _Categorical Interpolation: Descent and the Beck-Chevalley Condition without Direct Images_ in:_Category theory Como 1990_, LNM **1488** Springer (1991) 306-325 

* {#Buckley} Mitchell Buckley, _Fibred 2-categories and bicategories_, ([arXiv:1212.6283](https://arxiv.org/abs/1212.6283)) 

* {#Stanculesu12} [[Alexandru E. Stanculescu]], *Bifibrations and weak factorisation systems*, Applied Categorical Structures **20** 1 (2012) 19–30 &lbrack;<a href="https://link.springer.com/article/10.1007/s10485-009-9214-3">doi:10.1007/s10485-009-9214-3</a>&rbrack;

* [[Paul-André Melliès]], [[Noam Zeilberger]], _Type refinement and monoidal closed bifibrations_, ([arXiv.1310.0263](http://arxiv.org/abs/1310.0263v1)).

* {#vonGlehn} [[Tamara von Glehn]], *Polynomials and models of type theory*, PhD thesis &lbrack;[1810/254394](https://www.repository.cam.ac.uk/handle/1810/254394)&rbrack;

Relation to [[pseudofunctors]] with values in [[CatAdj|$Cat_{Adj}$]] and [[ModCat|$ModCat$]] (cf. [[model structures on Grothendieck constructions]]): 

* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], Section 2.2. of: _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

* {#CagneMelliès20} [[Pierre Cagne]], [[Paul-André Melliès]], *On bifibrations of model categories*, Advances in Mathematics **370** (2020) 107205 &lbrack;[arXiv:1709.10484](https://arxiv.org/abs/1709.10484), [doi:10.1016/j.aim.2020.107205](https://doi.org/10.1016/j.aim.2020.107205)&rbrack;







[[!redirects bifibrations]]