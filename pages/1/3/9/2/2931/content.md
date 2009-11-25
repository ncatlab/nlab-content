# Idea

If $K$ is a [[2-category]], an [[equipment]] on $K$ gives it the structure of "proarrows" which are intended to generalize the arrows of $K$ in the same way that [[profunctors]] generalize the [[functors]] in [[Cat]].  Since profunctors are a [[categorification]] of [[relations]], it is natural to think of decategorifying equipments to give a structure on a 1-category that equips it with "relations".  We call this structure a *1-category equipment*.

# Definition

Recall that a *2-category equipment* (the usual meaning of "equipment") on a 2-category $K$ can be defined as a certain sort of [[double category]], with $\mathcal{V}(\underline{K}) = K$.  If any two squares of such a double category with the same boundary are equal, we say that it is is a **(1,2)-category equipment**.  Note that if we write an equipment as a special sort of functor $(-)_\bullet\colon K\to M$, this is equivalent to saying that $M$ (and hence also $K$) is [[locally posetal 2-category|locally posetal]], i.e. a (1,2)-category.

If $V$ is any [[quantale]], then $V$-$Prof$ is a (1,2)-category equipment.  In particular, taking $V=\mathbb{2}$, we have a (1,2)-category equipment whose objects are [[preorders]].

A **1-category equipment** is a (1,2)-category equipment, regarded as a double category $\underline{K}$, together with an [[involution]] $\underline{K}^{h-op} \cong \underline{K}$ which is (isomorphic to) the identity on objects and (vertical) arrows.  Here $\underline{K}^{h-op}$ denotes the horizontal opposite of a double category obtained by reversing the horizontal (pro-)arrows but not the vertical ones.  In particular, this implies an involution $K \cong K^{co}$ which is the identity on objects and arrows, which for a (1,2)-category means that $K$ is actually (equivalent to) a 1-category.  Note though that $M$ is still a (1,2)-category, not necessarily a 1-category.

For any quantale $V$, the sub-equipment of $V$-$Prof$ consisting of the *symmetric* $V$-categories (those where $A(x,y) = A(y,x)$) is a 1-category equipment.  In particular, for $V=\mathbb{2}$, we have the 1-category equipment $\underline{Rel}$ of sets, functions, and binary relations.

In general, we can think of a 1-category equipment as generalizing some of the properties of $\underline{Rel}$.  For instance, internal relations in any [[regular category]] also form a 1-category equipment.


# See also

Other attempted axiomatizations of the same idea "something that acts like the category of relations in a regular category" include:

* [[allegory]]

* [[bicategory of relations]]


# Cartesian 1-category equipments

The following is a very rough sketch, with lots remaining to be made precise.

+-- {: .un_theorem}
###### Theorem
Let $\underline{K}$ be a 1-category equipment, and assume the following.

1. $\underline{K}$ is a [[cartesian object]] in the 2-category of 1-category equipments (that is, it is a **cartesian equipment**).

1. Every proarrow $\phi\colon x\nrightarrow y$ in $\underline{K}$ can be written as $f_\bullet g^\bullet$ for some (vertical) arrows $f$ and $g$.  (That is, "tabulations" in a certain sense exist.)

Then $\mathcal{H}(\underline{K})$ is a [[bicategory of relations]].
=--
+-- {: .proof}
###### Sketch of Proof
That $\underline{K}$ is a cartesian object means, in particular, that it is a [[pseudomonoid]] in the 2-category of equipments.  By lifting the coherence data from arrows to representable proarrows, it follows that $\mathcal{H}(\underline{K})$ is a monoidal 2-category.  Being a cartesian object also gives a cartesian product on objects and proarrows, with diagonals $\Delta\colon X\to X\times X$, and lifting these arrows to representable proarrows $\Delta_\bullet$ and $\Delta^\bullet$ gives each object a commutative monoid and comonoid structure.  Now for any proarrow $\phi\colon X\to Y$, the square
$$\array{X & \overset{\phi}{\to} & Y\\
  ^\Delta \downarrow & \Downarrow & \downarrow^\Delta\\
  X\times X& \underset{\phi\times \phi}{\to} & Y\times Y}$$
in $\underline{K}$ induces 2-cells, i.e. inequalities, $\Delta_\bullet \phi \le (\phi\times\phi)\Delta_\bullet$ and $\phi \Delta^\bullet  \le \Delta^\bullet(\phi\times\phi)$.  The details to check here depend on the precise definition of "bicategory of relations," which depends on the definition of "cartesian bicategory" of which there seem to be several versions, but we skip ahead to verifying the more interesting conditions.

We now verify the axiom $\Delta^\bullet \Delta_\bullet = 1$.  Since $\Delta^\bullet \Delta_\bullet$ is the restriction of $1_{X\times X}$ along $\Delta$ on both sides, it suffices to show that
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

Finally, we verify the Frobenius axiom $\Delta^\bullet \Delta_\bullet = (1\times \Delta_\bullet)(\Delta^\bullet \times 1)$.  Since $\Delta$ is associative, we have a square
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
If $\underline{K}$ is a 1-category equipment satisfying the hypotheses of the theorem, then $\mathcal{H}(\underline{K})$ is an [[allegory]].
=--
+-- {: .proof}
###### Proof
It is shown [here](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html) that any bicategory of relations is an allegory.
=--


[[!redirects (1,2)-category equipment]]
[[!redirects 1-category equipments]]