#Contents#
* table of contents
{:toc}

## Idea

The motivation of generalized global analytic geometry is to define analytic spaces associated to rig categories, and to use their relations with classical [[global analytic geometry|global analytic spaces]] in order to properly define [[Arakelov models]] of [[arithmetic varieties]] in an analytic setting.

Since rig categories are categorical analogs of associative and commutative semi-rings, a proper theory for them can only be given in the setting of $\infty$-categories.

One will thus define [[overconvergent global analytic geometry|overconvergent global analytic spaces]] of power series over a given stable rig $\infty$-category, rational domains in them, and compare the associated $G$-topology with the usual $G$-topology of overconvergent analytic geometry. Generalizing directly Haran's definition of the rig of integers of $(\mathbb{R},|\cdot|_\infty)$, we will then give examples of non-stable rig $\infty$-category with a well defined notion of rig $\infty$-category of analytic functions, and use them to define natural Arakelov-type compactifications of strict overconvergent global analytic spaces over $(\mathbb{Z},|\cdot|_\infty)$.

There are two possibities to get a sensible notion of analytic rig $\infty$-category:

* The first one is to use Banach stable $\infty$-categories, which may be seen as the categorical analogs of classical Banach rings, and to define general Banach rig $\infty$-categories as being either being the stable ones or their rig of integers in the sense of Haran. This approach has the advantage of giving a very concrete description of the objects in play, but the drawback of having bad $\infty$-categorical properties (no clear notions of limits and colimits in general). One should however keep in mind this concrete approach, even if one works with the other one, because they should not be incompatible.

* The second one is to remark that the Lawvere theory of commutative unitary rings, given by the category with finite products opposite to the category of polynomial rings, may be extended to a bigger category of strict rational domains over the trivially normed ring $(\mathbb{Z},|\cdot|_0)$. Using the localization of rig categories, one may easily extend a usual rig-category to a functor on such rational domains that commutes with pullbacks along rational (i.e., standard Zariski open) embeddings. One may instead work with any other commutative Banach ring $(R,|\cdot|)$, and define overconvergent ring $\infty$-categories (be careful, we have in particular a minus functor, here, i.e., all this is over $\mathbb{F}_{\{\pm 1\}}$) over $R$ simply as overconvergent analytic algebras over $R$ with values in the [[infinity-category]] of infinity categories. These are given by product preserving functors from the category $\texsc{RatAlg}^\dagger_R$ of overconvergent rational domain algebras to the $\infty$-category of $\infty$-categories, that further commute with pullbacks along rational domain embeddings. If we are given a usual dagger algebra, $A$, we may send it to the ring $\infty$-category $\mathcal{A}$ of free modules finitely generated modules over $A$. One should however be careful, in this approach, to check that points of the hypercompletion of the corresponding topos give exactly multiplicative seminorms on the underlying rig category. In particular, one should check that it is possible to get back the $L^2$-norm at infinity.

In the particular case of $\mathcal{M}(\mathbb{Z})$, we will get a natural proper $G$-topological space $\overline{\mathcal{M}(\mathbb{Z})}$ together with an analytic rig category $\mathcal{O}$ of overconvergent analytic functions, whose global sections are given by the rig category $\mathbb{F}_{\{\pm 1\}}$. This gives convincing indications that strict global analytic spaces may be naturally thought of as Arakelov models of the corresponding schemes over $\mathbb{Z}$. Since these new compactified spectra are stable by the natural power flow $|\cdot|\mapsto |\cdot|^t$ for $t\in [0,+\infty]$, they may be useful to better understand the relations between overconvergent global analytic geometry and analytic number theory (in the adelic sense of Tate's thesis).

## References

[[Frédéric Paugam]] _Analytic spectrum of rig categories_ [TAC](http://www.tac.mta.ca/tac/volumes/29/6/29-06abs.html)