
> This page is about [[Grothendieck fibrations]] that are also [[opfibrations]]. Not to be confused with [[two-sided fibrations]] nor with [[fibration of 2-categories|fibrations of 2-categories]] (both of which some authors also refer to as "bifibrations").


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

A **bifibration** of [[categories]] is a [[functor]]

$$
  \array{
    E
    \\
    \big\downarrow
    \\
    B
  }
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
 \label{BifibrationsAreTheGrothConstrOnCatAdjValuedPseudofunctors}
  Under the [[Grothendieck construction]], the [[Grothendieck fibrations]] which arise from [[pseudofunctors]] $\mathcal{B} \longrightarrow Cat$ that factor through [[CatAdj|$Cat_{Adj}$]] are equivalently the [[bifibrations]].
\end{proposition}
\begin{proof}
A Grothendieck construction on a pseudofunctor yielding a bifibration is fairly immediately equivalent to all base change functors having an adjoint on the respective side (e.g. [Jacobs (1998), Lem. 9.1.2](#Jacobs98)). By the fact that $Cat_{adj} \to Cat$ is a [[locally full sub-2-category]] ([this Prop.](transformation+of+adjoints#UniqueConjugateMate)) this already means that the given pseudofunctor factors through  $Cat_adj$, and essentially uniquely so.
\end{proof}
See also [Harpaz & Prasma (2015), Prop. 2.2.1](#HarpazPrasma15).



\begin{remark}
\label{BifibrationsOfModelCategories}
Further factoring through [[ModCat]] $ \longrightarrow Cat_{Ajd}$ hence yields bifibrations of [[model categories]] &lbrack;[Harpaz & Prasma (2015), Sec. 3](#HarpazPrasma15); [Cagne & Melliès (2020)](#CagneMelliès20)&rbrack;. See at *[[model structures on Grothendieck constructions]]* for more on this.
\end{remark}



### Relation to monadic descent
 {#RelationToMonadicDescent}

Ordinary [[Grothendieck fibrations]] correspond to [[pseudofunctors]] to [[Cat]], by the [[Grothendieck construction]] and hence to [[stack|prestacks]]. For these one may consider [[descent]].

If the fibration is a bifibration, there is a particularly elegant algebraic way to encode its descent properties; this is [[monadic descent]]. The [[Benabou–Roubaud theorem]] characterizes descent properties for bifibrations.




## Bifibration of bicategories

The basic theory of [[2-fibrations]], fibrations of bicategories, is developed in ([Buckley](#Buckley)). One (unpublished) proposal by Buckley and Shulman, for a "2-bifibration", a bifibration of [[bicategories]], is a functor of bicategories that is both a 2-fibration and a 2-opfibration. This should correspond to a pseudofunctor into $2 Cat_{adj}$, just as for 1-categories.  There is a difference from this case, however, in that although a 2-fibration (corresponding to a "doubly contravariant" pseudofunctor $B^{coop} \to 2Cat$) has both cartesian lifts of 2-cells and 1-cells, a 2-opfibration (corresponding to a totally *covariant* pseudofunctor $B\to 2Cat$) has opcartesian lifts of 1-cells but still *cartesian* lifts of 2-cells.

## Related concepts

* [[Grothendieck fibration]]

* [[Beck-Chevalley condition]]

* [[hyperdoctrine]]

* A bifibration $F:E\to B$ such that the transition functors also have *right* adjoints is sometimes called a [[trifibration]] (cf. Pavlovi&#263; 1990, p.315) or $\ast$-bifibration.


## References
 {#References}

Original notion and terminology of "bifibration":

* [[Alexander Grothendieck]], *Catégories co-fibrées, catégories bi-fibrées.*, Section 10 in exposé VI of: _Revêtements Etales et Groupe Fondamental - Séminaire de Géometrie Algébrique du Bois Marie 1960/61_ ([[SGA 1]]), LNM **224** Springer (1971) &lbrack;updated version with comments by M. Raynaud: [arxiv.0206203](http://arxiv.org/abs/math/0206203)&rbrack;

Further early discussion (not using the terminology "bifibration", though):

* {#Gray66} [[John W. Gray]], pp. 59 of: *Fibred and Cofibred Categories*,  in: [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 21-83 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

Discussion in the context of the [[Beck-Chevalley condition]]:

* [[Duško Pavlović]], _Categorical Interpolation: Descent and the Beck-Chevalley Condition without Direct Images_ in:_Category theory Como 1990_, LNM **1488** Springer (1991) 306-325 &lbrack;[doi:10.1007/BFb0084229](https://doi.org/10.1007/BFb0084229), [pdf](http://dusko.org/wp-content/uploads/2020/03/1990-Como-BCDE.pdf)&rbrack;


In the context of [[categorical semantics for dependent types]]:

* {#Jacobs98} [[Bart Jacobs]], pp. 511 of: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;


* [[Paul-André Melliès]], [[Noam Zeilberger]], _Type refinement and monoidal closed bifibrations_, ([arXiv.1310.0263](http://arxiv.org/abs/1310.0263v1)).


Relation to [[pseudofunctors]] with values in [[CatAdj|$Cat_{Adj}$]] and [[ModCat|$ModCat$]] (cf. [[model structures on Grothendieck constructions]]): 

* {#Stanculesu12} [[Alexandru E. Stanculescu]], *Bifibrations and weak factorisation systems*, Applied Categorical Structures **20** 1 (2012) 19–30 &lbrack;<a href="https://link.springer.com/article/10.1007/s10485-009-9214-3">doi:10.1007/s10485-009-9214-3</a>&rbrack;

* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], Section 2.2. of: _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

* {#CagneMelliès20} [[Pierre Cagne]], [[Paul-André Melliès]], *On bifibrations of model categories*, Advances in Mathematics **370** (2020) 107205 &lbrack;[arXiv:1709.10484](https://arxiv.org/abs/1709.10484), [doi:10.1016/j.aim.2020.107205](https://doi.org/10.1016/j.aim.2020.107205)&rbrack;

Discrete bifibrations (i.e. functors that are both [[discrete fibrations]] and [[discrete opfibrations]]) are termed **coverings** in:

* Samantha Parle, _A note on Robert Paré's notion of universal covering category_, [[TAC]] (2025), ([url](http://www.tac.mta.ca/tac/volumes/44/34/44-34abs.html))


[[!redirects bifibrations]]
[[!redirects discrete bifibration]]
[[!redirects discrete bifibrations]]