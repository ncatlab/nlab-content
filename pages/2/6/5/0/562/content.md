* toc
{:toc}

# Idea #

A **[[Alexander Grothendieck|Grothendieck]] fibration** (also called a **cartesian fibration** or [[fibered category]] or just a **fibration**) is a [[functor]] $p:E\to B$ such that the fibers $E_b = p^{-1}(b)$ depend (contravariantly) pseudofunctorially on $b\in B$.  One also says that $E$ is a **fibered category** over $B$. Dually, in a (Grothendieck) **opfibration** the dependence is covariant.

There is an [[equivalence of categories|equivalence]] of [[strict 2-category|2-categories]] between the 2-category of fibrations over $B$ and the 2-category $[B^{op},Cat]$ of contravariant [[pseudofunctor]]s from $B$ to [[Cat]], also called _$B$-indexed categories_.  The construction of a fibration from a pseudofunctor is sometimes called the _Grothendieck construction_, although fortunately (or unfortunately) Grothendieck performed many constructions.  Less ambiguous terms are the [[category of elements]] and the [[2-limit|lax colimit]].

# Definition #

Let $\phi:e'\to e$ be an arrow in $E$.  We say that $\phi$ is **[[cartesian morphism|cartesian]]** if for any arrow $\psi:e''\to e$ in $E$ and $g:p(e'')\to p(e')$ in $B$ such that $p(\phi)\circ g = p(\psi)$, there exists a unique $\chi:e''\to e'$ such that $\psi = \phi\circ \chi$ and $p(\chi) =g$.  We say that $p:E\to B$ is a **fibration** if for any $e\in E$ and $f:b\to p(e)$, there is a cartesian arrow $\phi:e'\to e$ with $p(\phi)=f$.

As a side note, we say that $\phi$ is _weakly cartesian_ if it has the property described above only when $g$ is an identity.  One can prove that $p$ is a fibration if and only if firstly, it has the above property with "cartesian" replaced by "weakly cartesian," and secondly, the composite of weakly cartesian arrows is weakly cartesian.  In a fibration, every weakly cartesian arrow is cartesian, but this is not true in general.  Some sources say "cartesian" and "strongly cartesian" instead of "weakly cartesian" and "cartesian," respectively.

We say that $p$ is an **opfibration** if $p^{op}:E^{op}\to B^{op}$ is a fibration.  Grothendieck originally called these "cofibrations," but that term has fallen out of favor because an opfibration still has a _lifting_ property, as is characteristic of other notions of [[fibration]], as opposed to the _extension_ property exhibited by [[cofibration]]s in [[homotopy theory]].  (Unfortunately, however, using the internal notion of fibration in a 2-category mentioned below, opfibrations are fibrations in the 2-cell dual $Cat^{co}$ while the fibrations in the 1-cell dual $Cat^{op}$ are more deserving of the name "cofibration.")

A square
$$\array{E' & \to & E \\ \downarrow && \downarrow \\ B' &\to  & B}$$
is a **morphism of fibrations** if the top arrow takes cartesian arrows to cartesian arrows.  Most frequently when considering morphisms of fibrations, the bottom arrow $B'\to B$ is an identity.  A 2-cell between morphisms of fibrations is a pair of 2-cells, one lying over the other.  Again frequently the bottom one is an identity, so that the condition is just that the top 2-cell is "vertical" (its components lie in fibers).

Given a fibration $p:E\to B$, we obtain a pseudofunctor $B^{op}\to Cat$ by sending each $b\in B$ to the category $E_b = p^{-1}(b)$ of objects mapping onto $b$ and morphisms mapping onto $1_b$.  To obtain the action on morphisms, given an $f:a\to b$ in $B$ and an object $e\in E_b$, we choose a cartesian arrow $\phi:e'\to e$ over $f$ and call its [[source]] $f^*(e)$.  The universal factorization property of cartesian arrows then makes $f^*$ into a functor $E_b \to E_a$, and it is easy to verify that it is a pseudofunctor.  The construction in the other direction is left as an exercise for the reader (or future contributor to this page).

Important special cases include when each fiber is a [[groupoid]], corresponding to pseudofunctors $B^{op}\to Grpd$, and when each fiber is a [[discrete category]], corresponding to functors $B^{op}\to Set$.  The latter case is called a **[[discrete fibration]]**.


# Remarks #

* If $p:E\to B$ is a fibration, then it is also an opfibration if and only if each functor $f^*$ has a left adjoint, written $f_!$ or $\Sigma_f$.  Such a fibration-and-opfibration is sometimes called a **bifibration**.  In many cases $f^*$ also has a right adjoint, written $f_*$ or $\Pi_f$, but this is not as easily expressible in fibrational language.

* A functor $B^{op}\to Cat$ can be represented both by a fibration $E_1\to B$ and by an opfibration $E_2\to B^{op}$.  However $E_2$ is _not_ the opposite category of $E_1$.

* It is easy to verify that fibrations are closed under pullback in [[Cat]], and that the composite of fibrations is a fibration.  This latter property is notably difficult to express in the language of pseudofunctors.

* Fibrations are a "nonalgebraic" structure, since the base change functors $f^*$ are determined by universal properties, hence uniquely up to isomorphism.  By contrast, pseudofunctors are an "algebraic" structure, since the functors $f^*$ are specified, together with the necessary coherence data and axioms; the latter come for free in a fibration because of the universal property.

* A [[stack]], being a particular type of pseudofunctor, can also be described as a particular sort of fibration.  This was the original application for which Grothendieck introduced the notion.


# Examples #

* Let $Ring$ be the category of [[ring|rings]], and $Mod$ the category of pairs $(R,M)$ where $R$ is a ring and $M$ is a (left) $R$-module.  Then the evident forgetful functor $Mod\to Ring$ is a fibration and an opfibration.  The functors $f^*$ are given by restriction of scalars, $f_!$ is extension of scalars, and the right adjoint $f_*$ is coextension of scalars.

* Let $C$ be any category with pullbacks and $\mathbf{2}$ the free-living arrow, so that $C^{\mathbf{2}}$ is the category of arrows and commutative squares in $C$.  Then the "codomain" functor $C^{\mathbf{2}} \to C$ is a fibration and opfibration.  The cartesian arrows are precisely the pullback squares, and the functors $f_!$ are just given by composition.  The right adjoints $f_*$ exist iff $C$ is [[locally cartesian closed category|locally cartesian closed]].  The term "cartesian" is motivated by this example.

* Let $C$ be any category and let $Fam(C)$ be the category of set-indexed families of objects of $C$.  The forgetful functor $Fam(C)\to Set$ taking a family to its indexing set is a fibration; the functors $f^*$ are given by reindexing.  They have left adjoints iff $C$ has small coproducts, and right adjoints iff $C$ has small products.

# Variations #

## Non-evil version ##

There is something [[evil]] about the notion of fibration, namely the requirement that for every $f:a\to b$ and $e\in E_b$ there exists a $\phi:e'\to e$ such that $p(e')$ is _[[equality|equal]]_, rather than merely [[isomorphism|isomorphic]], to $a$.  This is connected with the fact that we use strict fibers, rather than [[essential fiber]]s, and that fibrations and pseudofunctors can be recovered from each other up to isomorphism rather than merely equivalence.

While almost any fibration between "concrete" categories that arises in practice does satisfy this evil property, it is sometimes useful to have a non-evil version, for instance when working internally in a [[bicategory]] where equality of objects doesn't even really make sense.  The correct modification, first given by Street, is simply to require that for any $f:a\to b$ and $e\in E_b$ there exists a cartesian $\phi:e'\to e$ and an _isomorphism_ $h:p(e') \cong a$ such that $f\circ h = p(\phi)$; the definition of "cartesian" is unchanged.

+--{: .query}
[[David Roberts]]: Couldn't we also say that it is evil to say that the target of the cartesian arrow $\phi$ is equal to the given object $e$? I'm thinking from the point of view of [[Dold fibration|Dold fibrations]], where the initial point of a lifted path can only be specified up to homotopy. The resulting functor between fundamental groupoids is then not a fibration in the above 'evil' sense as it would be if we were dealing with a [[Serre fibration]].

[[Mike Shulman]]: Two answers: (1) I don't think that part of the definition is evil.  It's just like saying, in the definition of a [[product]] of two objects $A$ and $B$, that the target of the two projections $A\times B\to A$ and $A\times B \to B$ are *equal* to $A$ and $B$.  Defining the source and target of an arrow is just a typing assertion.

(2) I think any weakening along those lines would actually be equivalent to the version above, and moreover a Dold fibration really does induce an actual fibration (even an evil one) between fundamental groupoids.  The categorical version of a Dold fibration would say that for any $f\colon a\to b$ in $B$ and $e\in E_b$, there exists a cartesian $\phi\colon e' \to \hat{e}$ with $p(\phi)=f$ and an isomorphism $\hat{e}\cong e$ in the fiber $E_b$.  But in that case you can just compose $\phi$ with the isomorphism $\hat{e}\cong e$ to get a cartesian arrow $\hat{\phi}\colon e'\to e$ with $p(\phi)=f$ still.  The reason this doesn't work in topology is that paths come with parametrizations, and requiring the lower triangle (in the square drawn at [[Dold fibration]]) to commute strictly prevents the reparametrization necessary to compose with a vertical homotopy.

[[David Roberts]]: Duh, of course. The interesting bit of course comes when thinking about fundamental bigroupoids, where the parameterisations on the paths are preserved. I'd like to talk to you about some ideas on this line, but obviously on a more appropriate page, such as [[fibration of bigroupoids]].
=--

## Internal version ##

In a [[strict 2-category]] $K$, a morphism $p:E\to B$ is called a fibration if for every object $X$, $K(X,E)\to K(X,B)$ is a fibration of categories, and for every morphism $f:Y\to X$, the square
$$\array{ K(X,E) & \to & K(Y,E) \\ \downarrow && \downarrow \\ K(X,B) & \to & K(Y,B)}$$
is a morphism of fibrations.  There is an alternate characterization in terms of [[comma object]]s and adjoints, see [[fibration in a 2-category]].  The same definition works in a [[bicategory]], as long as we use the non-evil version above.  Interpreted in [[Cat]] we obtain the explicit notion we started with.

## Two-sided version ##

A **two-sided fibration**, or a **fibration from $B$ to $A$**, is a span $A \leftarrow E \rightarrow B$ such that $E\to A$ is a fibration, $E\to B$ is an opfibration, and the structure "commutes" in a natural way.  Such two-sided fibrations correspond to pseudofunctors $A^{op}\times B \to Cat$.

Note that such a pseudofunctor can also be represented by an opfibration $E_1\to A^{op}\times B$ and by a fibration $E_2\to A\times B^{op}$, but there is no simple relationship between the three categories $E$, $E_1$, and $E_2$.

## Higher categorical versions ##

There is a notion of Grothendieck fibration for [[quasi-category|quasicategories]] defined using lifting of fillers for certain simplicial spheres, used in work of Joyal and Lurie.  Applied to [[nerve|nerves]] of categories, it generalizes the original notion.

There is also a notion of fibration for 2-categories that has been studied by Hermida.  See [[n-fibration]] for a general version.

For [[(infinity,1)-category|(∞,1)-categories]] the notion of fibered category is modeled by the notion of [[Cartesian fibration]] of simplicial sets.

# References #

There are lots of references on fibrations; feel free to add your favorites!

* Part B of the [[Elephant]] contains a lot of basic information and some good intuition, although he uses the non-standard words "prone" and "supine" where most people say "cartesian" and "opcartesian" morphism.

*  Notes by Streicher: "Fibred Categories &#224; l&#224; Jean B&#233;nabou" are available online  &lt;http://www.mathematik.tu-darmstadt.de/~streicher>.


* "Categorical logic and type theory" by B. Jacobs

* The Wikipedia entry on [Fibred category](http://en.wikipedia.org/wiki/Fibred_category) is okay, and contains a number of other references.

[[!redirects Grothendieck fibrations]]
