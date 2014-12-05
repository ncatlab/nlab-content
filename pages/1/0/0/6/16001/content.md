#Contents#
* table of contents
{:toc}

## Ideas and objectives

The motivation of generalized global analytic geometry is to define analytic spaces associated to rig categories, and to use their relations with classical [[global analytic geometry|global analytic spaces]] in order to properly define [[Arakelov models]] of [[arithmetic varieties]] in an analytic setting.

Since rig categories are categorical analogs of associative and commutative semi-rings, a proper theory for them can only be given in the setting of $\infty$-categories.

One will thus define [[overconvergent global analytic geometry|overconvergent global analytic spaces]] of power series over a given stable rig $\infty$-category, rational domains in them, and compare the associated $G$-topology with the usual $G$-topology of overconvergent analytic geometry. Generalizing directly Haran's definition of the rig of integers of $(\mathbb{R},|\cdot|_\infty)$, we will then give examples of non-stable rig $\infty$-category with a well defined notion of rig $\infty$-category of analytic functions, and use them to define natural Arakelov-type compactifications of strict overconvergent global analytic spaces over $(\mathbb{Z},|\cdot|_\infty)$.

There are two possibities to get a sensible notion of analytic rig $\infty$-category:

* The first one is to use Banach stable $\infty$-categories, which may be seen as the categorical analogs of classical Banach rings, and to define general Banach rig $\infty$-categories as being either the stable ones or their rig of integers in the sense of Haran. This approach has the advantage of giving a very concrete description of the objects in play, but the drawback of having bad $\infty$-categorical properties (no clear notions of limits and colimits in general). One should however keep in mind this concrete approach, even if one works with the other one, because they should not be incompatible.

* The second one is to remark that the Lawvere theory of commutative unitary rings, given by the category with finite products opposite to the category of polynomial rings, may be extended to a bigger category of strict rational domains over the trivially normed ring $(\mathbb{Z},|\cdot|_0)$. Using the localization of rig categories, one may easily extend a usual rig-category to a functor on such rational domains that commutes with pullbacks along rational (i.e., standard Zariski open) embeddings. One may instead work with any other commutative Banach ring $(R,|\cdot|)$, and define overconvergent ring $\infty$-categories (be careful, we have in particular a minus functor, here, i.e., all this is over $\mathbb{F}_{\{\pm 1\}}$) over $R$ simply as overconvergent analytic algebras over $R$ with values in the [[infinity-category]] of infinity categories. These are given by product preserving functors from the category $RatAlg^\dagger_R$ of overconvergent rational domain algebras to the $\infty$-category of $\infty$-categories, that further commute with pullbacks along rational domain embeddings. If we are given a usual dagger algebra, $A$, we may send it to the ring $\infty$-category $\mathcal{A}$ of free modules finitely generated modules over $A$. One should however be careful, in this approach, to check that points of the hypercompletion of the corresponding topos give exactly multiplicative seminorms on the underlying rig category. In particular, one should check that it is possible to get back the $L^2$-norm at infinity.

In the particular case of $\mathcal{M}(\mathbb{Z})$, we will get a natural proper $G$-topological space $\overline{\mathcal{M}(\mathbb{Z})}$ together with an analytic rig category $\mathcal{O}$ of overconvergent analytic functions, whose global sections are given by the rig category $\mathbb{F}_{\{\pm 1\}}$. This gives convincing indications that strict global analytic spaces may be naturally thought of as Arakelov models of the corresponding schemes over $\mathbb{Z}$. Since these new compactified spectra are stable by the natural power flow $|\cdot|\mapsto |\cdot|^t$ for $t\in [0,+\infty]$, they may be useful to better understand the relations between overconvergent global analytic geometry and analytic number theory (in the adelic sense of Tate's thesis).

## The Banach rig $\infty$-categories approach

A rig $\infty$-category is a model of the Lawvere theory of semirings (given by the category with finite products opposite to the category of finitely generated polynomial semirings over the initial semiring $\mathbb{N}$) with values in the category with products of $\infty$-categories. If we give such a rig $\infty$-category
$$\mathcal{A}:(T_{SRings},\times)\longrightarrow ({}^\infty Cat,\times),$$
we may associate to it a classical rig-category $h(\mathcal{A})$. A multiplicative seminorm on $\mathcal{A}$ will be a multiplicative seminorm on $h(\mathcal{A})$ in the sense of the article cited on this page. If $\mathcal{A}$ is a rig category in the classical sense, one may extend it by a kind of nerve construction to a rig $\infty$-category.

There is a natural functor from the category of (commutative) rings to the category of rig $\infty$-categories given by sending a ring $A$ to its category $FMod(A)$ of free finitely generated modules, together with their usual direct sum and tensor product. This functor is fully faithful.

A stable symmetric monoidal $\infty$-category is also a natural example of a rig $\infty$-category, with additive homotopy category (since the direct sum monoidal structure is given by the product, or equivalently coproduct, of the given $\infty$-category).

One may define the Berkovich spectrum of a rig $\infty$-category by setting
$$\mathcal{M}(\mathcal{A})=\mathcal{M}(h(\mathcal{A})).$$
This means that the Berkovich spectrum doesn't really encode the homotopy information. However, it is quite practical to work with rig $\infty$-categories because they have nice categorical properties such as (at least finite) limits and colimits.

Given a multiplicative seminorm $|\cdot|$ on a rig $\infty$-category $\mathcal{A}$, one may define the associated generalized valuation ring as the rig $\infty$-category $O_\mathcal{A}$ whose homotopy category is given by
$$h(O_\mathcal{A}):=\{f\in h(\mathcal{A}),\;|f|\leq 1\}.$$
For example, Haran's definition of the ring of integers of $\mathbb{R}$ is given by
$$\mathbb{Z}_\eta:=O_{(FMod(\mathbb{R}),\|\cdot\|_2)}.$$
Remark that the $L^2$ norm $\|\cdot\|_2$ on the rig category $FMod(\mathbb{R})$ may be extended to a family of norms on the rig category $FMod(\mathbb{R}\{X\}^\dagger)$, by putting on the free module $(\mathbb{R}\{X\}^\dagger)^n$ the norms given by
$$
\|(\sum a_{i,1} X^i,\dots,\sum a_{i,n} X^i)\|_{\rho,2}:=
\|(\sum |a_{i,1}|_\infty\rho^i,\dots,\sum |a_{i,n}|_\infty\rho^i)\|_2.
$$
This seminorm is only sub-multiplicative for the tensor product operation.
One may then give a construction of the rig $\infty$-category
$$
\mathbb{Z}_\eta\{X\}^\dagger:=O_{FMod(\mathbb{R}\{X\}^\dagger)}.
$$
There may also be other interesting ways to define converging power series over $\mathbb{Z}_\eta$ (without forgetting that this generalized ring is not additive, i.e., not a usual ring), and these may be used to define Arakelov compactifications of strict dagger analytic spaces over $(\Z,|\cdot|_\infty)$, using a by hand approach to paste
the overconvergent spectrum of the seminormed rig category $(\mathbb{Z}_\eta,\|\cdot\|_2)$ and the overconvergent spectrum of the seminormed rig category $(FMod(\mathbb{Z}),\|\cdot\|_2)$ at the point $\|\cdot\|_2$, which corresponds to the archimedean norm $|\cdot|_\infty$ on $\mathbb{Z}$.

Recall that the Berkovich spectrum of $FMod(\mathbb{Z})$ projects on the space of "Artin" seminorms, that fulfill a weak triangle inequality of the form
$$|a+b|\leq C\,\max(|a|,|b|).$$


## The analytic ringed $\infty$-categories approach


## Complex generalized analytic geometry

**Careful: some corrections to be done here: there is no minus functor**

Before describing the general overconvergent theory, we will discuss the case of complex analytic generalized geometry, that will play an inspiring role in the forthcoming generalizations. We base our considerations on Lurie's notion of analytic rings and on Porta's description of modules over them.

Let $AnOpen_\mathbb{C}$ be the category of open subsets in finite dimensional affine spaces $\mathbb{C}^n$. It is equipped with two classes of limits, given by finite products and pullbacks along open immersions. A complex analytic ring is a functor
$$A:AnOpen_\mathbb{C}\to Sets$$
that commutes with the two given classes of limits on open subsets of affine spaces.
We will thus also define a complex analytic $\infty$-category as a functor
$$\mathcal{A}:AnOpen_\mathbb{C}\to {}^\infty Cat$$
that commutes with the two given classes of limits on open subsets of affine spaces.
We will denote $AnRings$ and ${}^\infty AnCat$ the categories of analytic rings and analytic infinity categories.

One may define a natural "free module" functor
$$FMod:AnRings\to {}^\infty AnCat$$
by sending an analytic ring $A$ to the functor that sends $\mathbb{C}$ to the
category
$$FMod(A)(\mathbb{C}):=FMod(A(\mathbb{C}))$$
of free modules over $A$ (which are the same as free modules over the underlying algebraic complex algebra $A(\mathbb{C})$).
One must of course have
$$FMod(A)(\mathbb{C}^n)\cong FMod(A)(\mathbb{C})^n.$$
Now one has to define the value of $FMod(A)$ on an open subset
$U$ of $\mathbb{C}^n$. Can you guess by yourself?
The answer seems quite hard to find, a priori.

However, one may get inspiration by going back to the algebraic situation: recall that a rig-$\infty$-category is a model of the [[Lawvere theory]] $T_{Rings}$ of rings. If $A$ is a usual (commutative unitary ring), one may extend it to such a model by sending a function on the affine space in n variables to the functor on the product of $n$ copies of the category $FMod(A)$ of free modules to $FMod(A)$ that sends $(M_1,\dots,M_n)$ to $f(M_1,\dots,M_n)$ in the sense of the given monoidal structures $\oplus$ and $\otimes$. A tricky point here is that one would like to extend this model of the [[Lawvere theory]] of rings to the Zariski [[pre-geometry]] $T_{Zar}$  of Lurie by saying what should the definition of the localization of $FMod(A)(\mathbb{C}[x_1,\dots,x_n])$ at a given $f\in \mathbb{C}[x_1,\dots,x_n]$ be (say we work over the complex numbers). This should be the localization $FMod(A)(\mathbb{C}[x_1,\dots,x_n])[f^{-1}]$, in some sense. Since $f$ is a function form $\mathbb{A}^n$ to $\mathbb{A}^1$, what could we do? The inspiration comes from the definition of the localization in the theory of smooth (or analytic rings): it is not given by inverting naively elements of the ring (Zariski open subset) but by taking the corresponding equation in a space that is of one dimension higher:
$C^\infty(\R^n)[f^{-1}]:=C^\infty(\R^n\times \R)/(Xf-1)$. We can do the same in the categorical framework (because the $\infty$-category of $\infty$-categories is presentable). So we define
$$FMod(A)(\mathbb{C}[x_1,\dots,x_n])[f^{-1}]$$
by
$$FMod(A)(\mathbb{C}[x_1,\dots,x_n])[X]/(X\otimes f-1).$$
One now needs to give a correct definition for the last expression.
Let's see if you can do that.

## Overconvergent generalized analytic geometry

One may easily extend the above complex analytic results to define overconvergent analytic $\infty$-categories over a given Banach ring. If $A$ is an dagger analytic ring, one may send the unit disc $D^1$ to the category $FMod(A)(D^1)$ of free modules of finite rank on $A$. Now one must send $D^n$ to $FMod(A)(D^1)^n$, and an overconvergent function $f:D^n\to D^1$ to a functor $f:FMod(A)(D^n)\to FMod(A)(D^1)$. One may then send a rational domain $U=\{|f|\leq |g|\}$ in $D^n$ to the quotient category
$$FMod(A)(U):=FMod(A)(D^{n+1})/(X\otimes g-f).$$
This will extend to the complex analytic situation by using compact Stein exhautions.

One must be very careful here with the fact that the unit disc and the affine line are very different on a non-trivially normed ring, so that it may also be interesting to consider a non-strict version of the above construction using the affine line instead of the unit disc.

## References

[[Frédéric Paugam]] _Analytic spectrum of rig categories_ [TAC](http://www.tac.mta.ca/tac/volumes/29/6/29-06abs.html)