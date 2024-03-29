#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

A [[2-category equipped with proarrows]] is a 2-category together with a 2-category of "proarrows" which are intended to generalize the arrows of $K$ in the same way that [[profunctors]] generalize the [[functors]] in [[Cat]].  Since profunctors are a [[categorification]] of [[relations]], it is natural to think of decategorifying such equipments to give a structure on a 1-category that equips it with "relations".  We call this structure a *1-category equipped with relations*.


## Definition ##

### (1,2)-categories equipped with proarrows

Recall that a *2-category equipped with proarrows* (aka "proarrow equipment" or "equipment") can be defined as a certain sort of [[double category]], with $\mathcal{V}(\underline{K}) = K$.  If, in such a double category, any two squares with the same boundary are equal, we say that it is is a **(1,2)-category equipped with proarrows**, or a **(1,2)-category proarrow equipment**.  This is equivalent to requiring that the 2-category of proarrows (and hence also the underlying 2-category of arrows) is [[locally posetal 2-category|locally posetal]], i.e. a (1,2)-category.

For example, if $V$ is any [[quantale]], then $V Cat$ is naturally a (1,2)-category equipped with proarrows.  In particular, taking $V=\mathbb{2}$, we have a (1,2)-category proarrow equipment whose objects are [[preorders]].


### 1-categories equipped with relations

A **1-category equipped with relations** is a (1,2)-category equipped with proarrows, regarded as a double category $\underline{K}$, together with an [[involution]] $\underline{K}^{h op} \cong \underline{K}$ which is (isomorphic to) the identity on objects and (vertical) arrows.  Here $\underline{K}^{h op}$ denotes the horizontal opposite of a double category obtained by reversing the horizontal (pro-)arrows but not the vertical ones.  We also call this structure a **relation equipment** or a **1-category proarrow equipment**.

In particular, the definition implies that we have an involution $K \cong K^{co}$ which is the identity on objects and arrows, which for a (1,2)-category means that $K$ is actually (equivalent to) a 1-category.  Note though that the 2-category of proarrows (which we now call "relations") is still (like [[Rel]]) a (1,2)-category, not necessarily a 1-category.

For example, for any quantale $V$, the sub-2-category of $V Cat$ consisting of the *symmetric* $V$-categories (those where $A(x,y) = A(y,x)$) is a 1-category equipped with relations.  In particular, for $V=\mathbb{2}$, we have the relation equipment $\underline{Rel}$ of sets, functions, and binary relations.

In general, we can think of a relation equipment as generalizing some of the properties of $\underline{Rel}$.  For instance, internal relations in any [[regular category]] also form a relation equipment.


## Cartesian 1-categories equipped with relations ##

It is proven in

* Carboni, Kelly, Wood, "A 2-categorical approach to change of base and geometric morphisms, I" ([PDF](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1991__32_1/CTGDC_1991__32_1_47_0/CTGDC_1991__32_1_47_0.pdf))

that a (1,2)-category is a [[cartesian bicategory]] precisely when it is a [[cartesian object]] in a suitable 2-category of proarrow equipments (where we make a bicategory $M$ into an equipment by taking the proarrows to be those of $M$ and the arrows to be the "maps" in $M$, i.e. the morphisms having right adjoints).  Here is a rough sketch of the argument, using the double-category description of equipments.

+-- {: .un_theorem}
###### Theorem
Let $\underline{K}$ be a 1-category equipped with relations, which is a [[cartesian object]] in the 2-category of relation equipments (that is, it is a **cartesian relation equipment**).  Then $\mathcal{H}(\underline{K})$ is a cartesian bicategory.
=--
+-- {: .proof}
###### Proof
That $\underline{K}$ is a cartesian object means, in particular, that it is a [[pseudomonoid]] in the 2-category of equipments.  By lifting the coherence data from arrows to representable proarrows, it follows that $\mathcal{H}(\underline{K})$ is a monoidal 2-category.  Being a cartesian object also gives a cartesian product on objects and proarrows, with diagonals $\Delta\colon X\to X\times X$, and lifting these arrows to representable proarrows $\Delta_\bullet$ and $\Delta^\bullet$ gives each object a commutative monoid and comonoid structure.  Now for any proarrow $\phi\colon X\to Y$, the square
$$\array{X & \overset{\phi}{\to} & Y\\
  ^\Delta \downarrow & \Downarrow & \downarrow^\Delta\\
  X\times X& \underset{\phi\times \phi}{\to} & Y\times Y}$$
in $\underline{K}$ induces 2-cells, i.e. inequalities, $\Delta_\bullet \phi \le (\phi\times\phi)\Delta_\bullet$ and $\phi \Delta^\bullet  \le \Delta^\bullet(\phi\times\phi)$.
=--

A [[bicategory of relations]] is a (1,2)-category which is a cartesian bicategory, and which also satisfies some additional conditions.  We can also construct this structure starting from a relation equipment.

+-- {: .un_theorem}
###### Theorem
Let $\underline{K}$ be a relation equipment satisfying the hypotheses of the previous theorem, and suppose in addition that every proarrow $\phi\colon x\nrightarrow y$ in $\underline{K}$ can be written as $f_\bullet g^\bullet$ for some (vertical) arrows $f$ and $g$.  (That is, "tabulations" in a certain sense exist.)  Then $\mathcal{H}(\underline{K})$ is a [[bicategory of relations]].
=--
+-- {: .proof}
###### Sketch of Proof
We first verify the axiom $\Delta^\bullet \Delta_\bullet = 1$.  Since $\Delta^\bullet \Delta_\bullet$ is the restriction of $1_{X\times X}$ along $\Delta$ on both sides, it suffices to show that
$$\array{X & \overset{1_X}{\to} & X\\
  ^\Delta\downarrow &\Downarrow& \downarrow^\Delta\\
  X\times X& \underset{1_{X\times X}}{\to} & X\times X}$$
is a cartesian 2-cell in $\underline{K}$.  But if we have any other square
$$\array{A & \overset{\phi}{\to} & B\\
  ^{(f,g)}\downarrow &\Downarrow& \downarrow^{(h,k)}\\
  X\times X& \underset{1_{X\times X}}{\to} & X\times X}$$
then $(f,g)$ factoring through $\Delta$ means that $f=g$, and likewise $h=k$.  Composing the given square  with the projection
$$\array{X\times X & \overset{1_{X\times X}}{\to} & X\times X\\
  \downarrow &\Downarrow & \downarrow\\
  X& \underset{1_X}{\to} & X}$$
(which comes from being a cartesian object in $Equipments$), we obtain a square
$$\array{A & \overset{\phi}{\to} & B \\
  ^f\downarrow &\Downarrow & \downarrow^g\\
  X& \underset{1_X}{\to} & X}$$
which factors the given square through the putative cartesian one.  The factorization is unique since all 2-cells are unique.

We now verify the Frobenius axiom $\Delta^\bullet \Delta_\bullet = (1\times \Delta_\bullet)(\Delta^\bullet \times 1)$.  Since $\Delta$ is associative, we have a square
$$\array{X & \overset{1_X}{\to} & X\\
  ^\Delta\downarrow && \downarrow^\Delta\\
  X\times X & \Downarrow & X\times X\\
  ^{1\times \Delta}\downarrow && \downarrow^{\Delta\times 1}\\
  X\times X\times X & \underset{1_{X\times X\times X}}{\to} & X\times X\times X}$$
and therefore a square
$$\array{X\times X & \overset{\Delta^\bullet \Delta_\bullet}{\to} & X\times  X\\
  ^{1\times \Delta}\downarrow && \downarrow^{\Delta\times 1}\\
  X\times X\times X & \underset{1_{X\times X\times X}}{\to} & X\times X\times X}$$
and it suffices to show that this is a cartesian 2-cell.  So suppose given a square
$$\array{A & \overset{\phi}{\to} & B\\
  ^{(f,g,g)}\downarrow & \Downarrow & \downarrow^{(h,h,k)}\\
  X\times X\times X & \underset{1_{X\times X\times X}}{\to} & X\times X\times X.}$$
The fact that $g$ and $h$ appear twice is equivalent to saying that the left and right boundaries of this square factor through $1\times\Delta$ and $\Delta\times 1$, respectively.  Now by assumption, $\phi = u_\bullet v^\bullet$ for some $u\colon C\to B$ and $v\colon C\to A$.  Thus our square is equivalent to one
$$\array{C & \overset{1_C}{\to} & C\\
  ^{(f v,g v,g v)}\downarrow & \Downarrow & \downarrow^{(h u,h u,k u)}\\
  X\times X\times X & \underset{1_{X\times X\times X}}{\to} & X\times X\times X.}$$
But this is just a 2-cell in the vertical category $K$, which is a 1-category; hence we have $(f v,g v, g v) = (h u, h u, k u)$ and thus $f v = h u = g v = k u$.  Calling their common value $m$, we thus have a composite square
$$\array{C & = & C & = & C\\
  ^{(m,m)}\downarrow && \downarrow^{m} && \downarrow^{(m,m)}\\
  X\times X & \underset{\Delta^\bullet }{\to} & X & \underset{\Delta_\bullet}{\to} & X\times X}$$
(since $\Delta m = (m,m)$) which gives us the desired factorization.  The other Frobenius axiom is, of course, dual.
=--

+-- {: .un_corollary}
###### Corollary
If $\underline{K}$ is a relation equipment satisfying the hypotheses of the theorem, then $\mathcal{H}(\underline{K})$ is an [[allegory]].
=--
+-- {: .proof}
###### Proof
It is shown [here](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html) that any bicategory of relations is an allegory.
=--

## See also ##

Other attempted axiomatizations of the same idea "something that acts like the category of relations in a regular category" include:

* [[allegory]]

* [[bicategory of relations]]

## References

A comparison of "regular proarrow equipments" with "regular [[fibrations]] of [[subobjects]]" is in

* [[Finn Lawler]], *Fibrations of predicates and bicategories of relations*, [arXiv](http://arxiv.org/abs/1502.08017)

A study of equipments of relations from a double-categorical viewpoint, and a characterization of those that arise from some [[factorization system]], is in

* [[Michael Lambert]], *Double categories of relations*, [arxiv](https://arxiv.org/abs/2107.07621) 2021

[[!redirects (1,2)-category equipment]]
[[!redirects (1,2)-category equipped with proarrows]]
[[!redirects 1-category equipped with proarrows]]
[[!redirects relation equipment]]
[[!redirects relation equipments]]
[[!redirects 1-category relation equipment]]
[[!redirects 1-category equipment]]
[[!redirects 1-category equipments]]
[[!redirects 1-category proarrow equipment]]
[[!redirects (1,2)-category proarrow equipment]]