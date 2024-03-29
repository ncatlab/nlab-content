#Contents#
* table of contents
{:toc}

## Ideas and objectives

The motivation of generalized global analytic geometry is to define analytic spaces associated to rig categories, and to use their relations with classical [[global analytic geometry|global analytic spaces]] in order to properly define [[Arakelov geometry|Arakelov models]] of [[arithmetic varieties]] in an analytic setting.

Since rig categories are categorical analogs of associative and commutative semi-rings, a proper theory for them can only be given in the setting of $\infty$-categories.

One will thus need to define [[overconvergent global analytic geometry|overconvergent global analytic spaces]] over a given rig $\infty$-category, rational domains in them, and compare the associated $G$-topology with the usual $G$-topology of overconvergent analytic geometry. Generalizing directly Haran's definition of the rig of integers of $(\mathbb{R},|\cdot|_\infty)$, we will then give examples of rig $\infty$-category with a well defined notion of rig $\infty$-category of analytic functions, and use them to define natural Arakelov-type compactifications of strict overconvergent global analytic spaces over $(\mathbb{Z},|\cdot|_\infty)$.

To be able to complete non-additive rig categories, we will have to replace seminorms by rig metrics (metrics on morphism spaces that are compatible with the rig category structure). There are rig categories associated to rings, but also to Banach rings, and for the last ones, there may be various natural choices, based on the type of modules in use. The notion of morphism will be imposed by the necessity of having a natural morphism
$$
(\Z_\eta,\|\cdot \|_2)\to (\Z_\eta,\|\cdot\|_2)^t
$$
for every $t\geq 1$.
We will then define a category of rational domain rig categories that will be the building blocks of analytic ring categories and analytic ringed spaces. The definitions proposed in the coming Sections is not clearly adapted to the setting of Banach rings, because the metric enrichment should be done on the full infinity groupoid of morphisms in a rig category (and this last point is yet a problematic issue; one should probably use simplicial Cauchy spaces or metric spaces with Cauchy maps, to make an $\infty$-category adapted to the enrichment). All these constructions will be compatible with the standard flow on metrics and absolute value given by taking $t$-th power for $t\in \mathbb{R}_+^*$.

## Seminormed and metrized ring $\infty$-categories

A ring $\infty$-category is a model of the Lawvere theory of rings (given by the category with finite products opposite to the category of finitely generated polynomial semirings over the initial ring $\mathbb{Z}$) with values in the category with products of $\infty$-categories. If we give such a rig $\infty$-category
$$\mathcal{A}:(T_{Rings},\times)\longrightarrow ({}^\infty Cat,\times),$$
we may associate to it a classical ring-category $h(\mathcal{A})$. A multiplicative seminorm on $\mathcal{A}$ will be a multiplicative seminorm on $h(\mathcal{A})$ in the sense of the article cited on this page. If $\mathcal{A}$ is a rig category in the classical sense, one may extend it by a kind of nerve construction to a rig $\infty$-category. Indeed, the nerve $N(\mathcal{A})$ of $\mathcal{A}$ gives an $\infty$-category. By sending $\mathbb{A}^n$ to $N(\mathcal{A})^n$, one defines a functor
$$N_{\oplus,\otimes}(\mathcal{A}):T_{SRings}\to {}^\infty Cat$$
given by sending a polynomial map
$f=\sum a_\alpha X^\alpha:\mathbb{A}^n\to \mathbb{A}^1$
to the corresponding functor
$$
N_{\oplus,\otimes}(f):=
(M_1,\dots,M_n)\mapsto \bigoplus_\alpha\oplus_{a_\alpha}(M_1,\dots,M_n)^{\otimes \alpha}.
$$

There is a natural functor from the category of (commutative) rings to the category of ring $\infty$-categories given by sending a ring $A$ to its category $FMod(A)$ of free finitely generated modules, together with their usual direct sum and tensor product. This functor is fully faithful.

Recall that the Berkovich spectrum of $FMod(\mathbb{Z})$ projects on the space of "Artin" seminorms, that fulfill a weak triangle inequality of the form
$$|a+b|\leq C\,\max(|a|,|b|).$$

A stable symmetric monoidal $\infty$-category is also a natural example of a ring $\infty$-category, with additive homotopy category (since the direct sum monoidal structure is given by the product, or equivalently coproduct, of the given $\infty$-category).

One may define the Berkovich spectrum of a ring $\infty$-category by setting
$$\mathcal{M}(\mathcal{A})=\mathcal{M}(h(\mathcal{A})).$$
This means that the Berkovich spectrum doesn't really encode the homotopy information. However, it is quite practical to work with rig $\infty$-categories because they have nice categorical properties such as (at least finite) limits and colimits.

We will also work with the notion of a ring metric on a ring category,
given by a ring norm on its homotopy category.

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

## Classical approach: the metrized spectrum

If $(\mathcal{A},d_{\mathcal{A}})$ is a metrized pointed ring category,
we may define its Berkovich spectrum as the set $X=\mathcal{M}(\mathcal{A},d_{\mathcal{A}}(0,\cdot))$ of multiplicative seminorms such that
$|\cdot|\leq d_\mathcal{A}(0,\cdot)$. One may define the presheaf of uniform limits (i.e., the completion) of rational functions without poles, and then germs $\mathcal{O}_x$ at a point $x\in X$ as equivalence classes of pairs $(V,(f_n))$ composed of an open neighborhood $V$ of $x$ and a Cauchy sequence of rational functions without poles $f_n\in \mathcal{K}(V)$.

We then define analytic functions as maps
$$f:U\to \coprod_{x\in U} \Hom_{\mathcal{O}_x}(M,N)$$
($M$ and $N$ are objects of $\mathcal{A}$, seen as objects of $\mathcal{O}_x$)
such that for every point $x\in U$, there is a neighborhood $V$ of $x$ such
that $f$ comes from the completion of rational functions without poles on $V$. The obtained sheaf $\mathcal{O}_X$ has a map from rational functions $\mathcal{K}_X$ by definition.

Morphisms of analytic spaces will be those induced by morphisms of
metrized ring categories.

Remark that the point $d_\infty^\infty$ doesn't even make sense in $\mathcal{D}(\mathbb{Z}_\eta,d_\infty)$, because $d_\infty^t(-1,1)$ tends to infinity.
However, the associated norm makes sense. Inspired by this remark,
we define the rig category of analytic functions on $\mathcal{M}(\mathcal{A},d_\mathcal{A}(0,-))$
as the direct image along
$$\phi:\mathcal{D}(\mathcal{A},d_\mathcal{A})\to \mathcal{M}(\mathcal{A},d_\mathcal{A}(0,-))$$
of the structural sheaf we just defined on the space of metrics.

## Functorial approach: derived stacks over metrized ringed categories

One may define a natural class of ind-metrized ring categories
by the following process: first, one defines
the category of metrized power series ring categories over
$\mathbb{Z}$ in the usual way, using the $L^2$-norm and its real powers.
Then one defines power series ring categories over $\mathbb{Z}_\eta$ as
valuation ring categories of power series ring categories over $\mathbb{R}$.
Then we define rational domain algebras over both types of
power series rings, as coequalizers of morphisms such as $fX$ and $g$
with $fX,g\in \mathrm{End}(\mathbb{1})$. This is where we need the metric
structure (because the norm will not allow completion) on morphism spaces.
This gives a subcategory of ind-metrized ring categories called
rational domain algebra categories.

One then gets inspiration from Dubuc's work on synthetic analytic geometry and Lurie's work on general pre-geometries to define general analytic ring categories
as arbitrary colimits (in the category of ind-metrized ring categories) of rational domain algebra categories, or maybe, as functors of functions that commute with products and standard pullbacks along rational domain embeddings. One may then define a Grothendieck topology on analytic ring categories and use it to define sheaves (functors of points) that will extend (in a sense to be explained) global analytic spaces (in the sense of the paper cited down this page) to a wider class of spaces.

In this new category $\An^\dagger_{\mathbb{F}_{\{\pm 1\}}}$, we may define,
for example
$$
\overline{\mathcal{M}(\mathbb{Z})}:=
\{|2|\geq 3/2\}\coprod_{\{2\geq |2|\geq 3/2\}}\{2\geq |2|\},
$$
where the left domain is from $\mathcal{M}(\mathbb{Z}_\eta)$ and the two other domains are from $\mathcal{M}(\mathbb{Z})$.

The gives a category $An^{\dagger,s}_\overline{\mathcal{M}(\mathbb{Z})}$ of Arakelov-type varieties.

## Adelic description of principal $\GL_n$-bundles on $\overline{\mathcal{M}(\mathbb{Z})}$

The main motivation for compactifying global analytic spaces using the ring categories approach is to get a geometric interpretation of the standard
adelic quotient
$$
\GL_n(\mathbb{Q})\backslash\GL_n(\mathbb{A})/K,
$$
where $K$ is the maximal compact subgroup of the adelic group,
as a moduli space of bundles.

An $F$-rig category is a rig category whose objects are all isomorphic
to objects of the form $\mathbb{1}^{\oplus n}$ for $n\in \N$, with
the convention that $\mathbb{1}^{\oplus 0}:=0$.

Let $\GL_n$ be the functor on rig categories that sends
$(\mathcal{A},\oplus,\otimes)$ to
$$\GL_n(\mathcal{A}):=\Isom_\mathcal{A}(\mathbb{1}^{\oplus n},\mathbb{1}^{\oplus n}).$$
A principal $\GL_n$-bundle on a generalized analytic space $X$ is a space
$F\to X$ that is isomorphic, locally on $X$, to the space $\GL_n$.
One may actually define an $\infty$-stack $B\GL_n$ by sheafifying the nerve
of the groupoid $B\GL_n$.

We denote $\Bun_n(\cdot):=\Hom_{St}(\cdot,B\GL_n)$
the $\infty$-stack of $\GL_n$-bundles on generalized analytic spaces.

By construction, we will have
$$
\pi_0(\Bun_n(\overline{\mathcal{M}(\mathbb{Z})}))\cong \GL_n(\mathbb{Q})\backslash\GL_n(\mathbb{A})/K,
$$
where $K$ is the maximal compact subgroup of the adelic group.
## References

[[Frédéric Paugam]] _Analytic spectrum of rig categories_ [TAC](http://www.tac.mta.ca/tac/volumes/29/6/29-06abs.html)

[[Frédéric Paugam]] _Overconvergent global analytic geometry_ [arXiv](http://arxiv.org/abs/1410.7971)