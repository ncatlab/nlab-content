#Contents#
* table of contents
{:toc}

## Ideas and objectives

The motivation of generalized global analytic geometry is to define analytic spaces associated to rig categories, and to use their relations with classical [[global analytic geometry|global analytic spaces]] in order to properly define [[Arakelov models]] of [[arithmetic varieties]] in an analytic setting.

Since rig categories are categorical analogs of associative and commutative semi-rings, a proper theory for them can only be given in the setting of $\infty$-categories.

One will thus define [[overconvergent global analytic geometry|overconvergent global analytic spaces]] of power series over a given stable rig $\infty$-category, rational domains in them, and compare the associated $G$-topology with the usual $G$-topology of overconvergent analytic geometry. Generalizing directly Haran's definition of the rig of integers of $(\mathbb{R},|\cdot|_\infty)$, we will then give examples of non-stable rig $\infty$-category with a well defined notion of rig $\infty$-category of analytic functions, and use them to define natural Arakelov-type compactifications of strict overconvergent global analytic spaces over $(\mathbb{Z},|\cdot|_\infty)$.

We will use Banach stable $\infty$-categories, which may be seen as the categorical analogs of classical Banach rings, and define general Banach rig $\infty$-categories as either the stable ones or their rig of integers in the sense of Haran. This approach has the advantage of giving a very concrete description of the objects in play, but the drawback of having bad $\infty$-categorical properties (no clear notions of limits and colimits in general). One should however keep in mind this concrete approach, even if one works with another one, because they should not be incompatible.

In the particular case of $\mathcal{M}(\mathbb{Z})$, we will get a natural proper $G$-topological space $\overline{\mathcal{M}(\mathbb{Z})}$ together with an analytic rig category $\mathcal{O}$ of overconvergent analytic functions, whose global sections are given by the rig category $\mathbb{F}_{\{\pm 1\}}$. This gives convincing indications that strict global analytic spaces may be naturally thought of as Arakelov models of the corresponding schemes over $\mathbb{Z}$. Since these new compactified spectra are stable by the natural power flow $|\cdot|\mapsto |\cdot|^t$ for $t\in [0,+\infty]$, they may be useful to better understand the relations between overconvergent global analytic geometry and analytic number theory (in the adelic sense of Tate's thesis).

## Seminorm rig $\infty$-categories

A rig $\infty$-category is a model of the Lawvere theory of semirings (given by the category with finite products opposite to the category of finitely generated polynomial semirings over the initial semiring $\mathbb{N}$) with values in the category with products of $\infty$-categories. If we give such a rig $\infty$-category
$$\mathcal{A}:(T_{SRings},\times)\longrightarrow ({}^\infty Cat,\times),$$
we may associate to it a classical rig-category $h(\mathcal{A})$. A multiplicative seminorm on $\mathcal{A}$ will be a multiplicative seminorm on $h(\mathcal{A})$ in the sense of the article cited on this page. If $\mathcal{A}$ is a rig category in the classical sense, one may extend it by a kind of nerve construction to a rig $\infty$-category. Indeed, the nerve $N(\mathcal{A})$ of $\mathcal{A}$ gives an $\infty$-category. By sending $\mathbb{A}^n$ to $N(\mathcal{A})^n$, one defines a functor
$$N_{\oplus,\otimes}(\mathcal{A}):T_{SRings}\to {}^\infty Cat$$
given by sending a polynomial map
$f=\sum a_\alpha X^\alpha:\mathbb{A}^n\to \mathbb{A}^1$
to the corresponding functor
$$
N_{\oplus,\otimes}(f):=
(M_1,\dots,M_n)\mapsto \bigoplus_\alpha\oplus_{a_\alpha}(M_1,\dots,M_n)^{\otimes \alpha}.
$$

There is a natural functor from the category of (commutative) rings to the category of rig $\infty$-categories given by sending a ring $A$ to its category $FMod(A)$ of free finitely generated modules, together with their usual direct sum and tensor product. This functor is fully faithful.

Recall that the Berkovich spectrum of $FMod(\mathbb{Z})$ projects on the space of "Artin" seminorms, that fulfill a weak triangle inequality of the form
$$|a+b|\leq C\,\max(|a|,|b|).$$

A stable symmetric monoidal $\infty$-category is also a natural example of a rig $\infty$-category, with additive homotopy category (since the direct sum monoidal structure is given by the product, or equivalently coproduct, of the given $\infty$-category).

One may define the Berkovich spectrum of a rig $\infty$-category by setting
$$\mathcal{M}(\mathcal{A})=\mathcal{M}(h(\mathcal{A})).$$
This means that the Berkovich spectrum doesn't really encode the homotopy information. However, it is quite practical to work with rig $\infty$-categories because they have nice categorical properties such as (at least finite) limits and colimits.

Remark that one may be tempted to work with a refined definition of multiplicative seminorm on a rig $\infty$-category, by using enrichment over the (multiplicative) symmetric monoidal category of simplicial $\R_+$-graded sets together with contracting (or simply bounded) maps. The notion of stable $\R_+$-graded rig category may then be given by using $\R_+$-graded spectra, described in the reference on overconvergent global analytic geometry down this page.

## Valuation rig $\infty$-categories

Given a multiplicative seminorm $|\cdot|$ on a rig $\infty$-category $\mathcal{A}$, one may define the associated generalized valuation ring as the rig $\infty$-category $O_\mathcal{A}$ whose homotopy category is given by
$$h(O_\mathcal{A}):=\{f\in h(\mathcal{A}),\;|f|\leq 1\}.$$
For example, Haran's definition of the ring of integers of $\mathbb{R}$ is given by
$$\mathbb{Z}_\eta:=O_{(FMod(\mathbb{R}),\|\cdot\|_2)}.$$
One may also define an ind-seminormed rig $\infty$-category
$$
\mathbb{Z}^\dagger_\eta:=\colim_{\rho\to 1}
O_{(FMod(\mathbb{R}),\|\cdot\|^\rho_2)}.
$$

Remark that the $L^2$ norm $\|\cdot\|_2$ on the rig category $FMod(\mathbb{R})$ may be extended to a family of norms on the rig category $FMod(\mathbb{R}\{X\}^\dagger)$, by putting on the free module $(\mathbb{R}\{X\}^\dagger)^n$ the norms given by
$$
\|(\sum a_{i,1} X^i,\dots,\sum a_{i,n} X^i)\|_{\rho,2}:=
\|(\sum |a_{i,1}|_\infty\rho^i,\dots,\sum |a_{i,n}|_\infty\rho^i)\|_2.
$$
This seminorm is only sub-multiplicative for the tensor product operation.
One may then give a construction of the ind-seminormed rig $\infty$-category
$$
\mathbb{Z}_\eta\{X\}^\dagger:=O_{FMod(\mathbb{R}\{X\}^\dagger)}.
$$

## A natural class of ind-seminormed rig categories

One may define a natural class of ind-seminormed rig categories by using ind-Banach rings given by algebras of functions $\mathcal{O}^\dagger(R)$ on non-strict compact rational domains
$R=D(f_0,\rho_0|f_1,\rho_1,\dots,f_n,\rho_n)$ in the affine space $\mathbb{A}^{n,an}_\mathbb{Z}$,
given by all (Artin-type) multiplicative seminorms on the polynomial ring.
We will work with the associated ind-seminormed topological rig categories.

In addition to the above rig categories, we may also use the valuation rig categories $\mathcal{V}^\dagger(R)$ of algebras of functions $\mathcal{O}^\dagger(R)$ on non-strict (not necessarily compact) rational domains
$R=D(f_0,\rho_0|f_1,\rho_1,\dots,f_n,\rho_n)$ in the (Artin type) affine space $\mathbb{A}^{n,an}_\mathbb{Z}$
such that the fiber $R_{(\mathbb{Z},|\cdot|_\infty)}$ is compact.
These domains are either bounded on the archimedean branch of $\mathcal{M}(\mathbb{Z})$ or project surjectively on an interval
$$\{|2|\geq 2^t\}\cong[|\cdot|_\infty^t,|\cdot|_\infty^\infty[$$
of the archimedean branch of $\mathcal{M}(\mathbb{Z})$.
The valuation rig category $\mathcal{V}^\dagger(R)$ is defined concretely as the sub-rig category of $\mathcal{O}^\dagger(R_{(\mathbb{Z},|\cdot|_\infty)})$ given by functions $f$ such that for every $x\in \mathcal{M}(FMod(\mathcal{O}^\dagger(R_{(\mathbb{Z},|\cdot|_\infty)})))$, $|f(x)|\leq 1$. Here, we use the set of seminorms on free modules that are continuous and bounded on $\End(\mathbb{1})$ by the given seminorms on $\mathcal{O}^\dagger(R_{(\mathbb{Z},|\cdot|_\infty)})$.

It would be nice to check that $\bar{R}:=\mathcal{M}(\mathcal{V}^\dagger(R))$ is a natural compactification of $R\cong \mathcal{M}(\mathcal{O}^\dagger(R))$.

## Analytic geometry over $\mathbb{F}_{\{\pm 1\}}$

One defines rational embeddings $R\to S$ of usual rational domains as usual,
and this defines also the notion of rational embedding
$\bar{R}\to \bar{S}$.
We consider the category $\mathcal{T}$ whose objects are of the form $R$ or $\bar{R}$ (remark that there may exist $S$ such that $S\cong \bar{R}$; one may make an easy example with $\mathbb{Q}_p$), and whose morphisms correspond to morphisms of topological ind-seminormed rig $\infty$-categories. One may try to show that it defines a pre-geometry in the sense of Lurie, with admissible morphisms given by rational embeddings. One may think of $\mathcal{T}$-schemes as analytic spaces over $\mathcal{M}(\mathbb{F}_{\{\pm 1\}})$, where
$$\mathbb{F}_{\{\pm 1\}}:=\mathcal{V}^\dagger(\{|2|\leq 2\})$$
(with $\{|2|\leq 2\}\subset \mathcal{M}(FMod(\mathbb{Z}))$)
is in some sense the initial valuation rig category.

In this new category $\An^\dagger_{\mathbb{F}_{\{\pm 1\}}}$, we may define,
for example
$$
\overline{\mathcal{M}(\mathbb{Z})}:=
\overline{\{|2|\geq 3/2\}}\coprod_{\{2\geq |2|\geq 3/2\}}\{2\geq |2|\},
$$
where all rational domains are from $\mathcal{M}(\mathbb{Z})$.

One may define $D^1_\overline{\mathcal{M}(\mathbb{Z})}$ (resp. more generally $R_\overline{\mathcal{M}(\mathbb{Z})}$ for $R$ a rational domain over $(\mathbb{Z},|\cdot|_\infty)$) exactly by the same formula but with rational domains from $D^1$ (resp. from $R$). If we start from a strict analytic space, this compactification process will be called the arithmetic compactification.
The gives a category $An^{\dagger,s}_\overline{\mathcal{M}(\mathbb{Z})}$ of Arakelov-type varieties, whose base extension to $(\mathbb{Z},|\cdot|_0)$ give schemes. It seems reasonable to conjecture that the base extension functor
$$
An^{\dagger,s}_\overline{\mathcal{M}(\mathbb{Z})}\longrightarrow
An^{\dagger,s}_{(\mathbb{Z},|\cdot|_\infty)}
$$
is an equivalence of categories.


## References

[[Frédéric Paugam]] _Analytic spectrum of rig categories_ [TAC](http://www.tac.mta.ca/tac/volumes/29/6/29-06abs.html)

[[Frédéric Paugam]] _Overconvergent global analytic geometry_ [arXiv](http://arxiv.org/abs/1410.7971)