
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* toc
{:toc}

## Idea 

A **[[Alexander Grothendieck|Grothendieck]] fibration** (also called a **cartesian fibration** or **fibered category** or just a **fibration**) is a [[functor]] $p:E\to B$ such that the [[fiber]]s $E_b = p^{-1}(b)$ depend (contravariantly) [[pseudofunctor|pseudofunctorially]] on $b\in B$.  One also says that $E$ is a **fibered category** over $B$. Dually, in a (Grothendieck) **opfibration** the dependence is covariant.

There is an [[equivalence of categories|equivalence]] of [[strict 2-category|2-categories]] 

$$
  Fib(B) \stackrel{\simeq}{\leftrightarrow} [B^{op}, Cat] : 
  \int
$$

between the 2-category of fibrations over $B$ and the 2-category $[B^{op},Cat]$ of contravariant [[pseudofunctor]]s from $B$ to [[Cat]], also called _$B$-indexed categories_.  

The construction $\int : [B^{op}, Cat] \to Fib(B) : F \mapsto \int F$ of a fibration from a pseudofunctor is sometimes called the _[[Grothendieck construction]]_, although fortunately (or unfortunately) Grothendieck performed many constructions.  Less ambiguous terms for $\int F$ are the [[category of elements]] and the [[2-limit|lax colimit]] of $F$.

Those fibrations corresponding to pseudofunctors that factor through [[Grpd]] are called **[[categories fibered in groupoids]]**.


## Definition 

Let $\phi:e'\to e$ be an arrow in $E$.  We say that $\phi$ is **[[cartesian morphism|cartesian]]** if for any arrow $\psi:e''\to e$ in $E$ and $g:p(e'')\to p(e')$ in $B$ such that $p(\phi)\circ g = p(\psi)$, there exists a unique $\chi:e''\to e'$ such that $\psi = \phi\circ \chi$ and $p(\chi) =g$.

We say that $p:E\to B$ is a **fibration** if for any $e\in E$ and $f:b\to p(e)$, there is a cartesian arrow $\phi:e'\to e$ with $p(\phi)=f$.  A choice of such a cartesian arrow for every $e$ and $f$ is called a [[cleavage]].  Thus, assuming the [[axiom of choice]], a functor is a fibration iff it admits some cleavage.

As a side note, we say that $\phi$ is _weakly cartesian_ if it has the property described above only when $g$ is an identity.  One can prove that $p$ is a fibration if and only if firstly, it has the above property with "cartesian" replaced by "weakly cartesian," and secondly, the composite of weakly cartesian arrows is weakly cartesian.  In a fibration, every weakly cartesian arrow is cartesian, but this is not true in general.  Some sources say "cartesian" and "strongly cartesian" instead of "weakly cartesian" and "cartesian," respectively.

A square
$$\array{E' & \to & E \\ \downarrow && \downarrow \\ B' &\to  & B}$$
is a **cartesian morphism** or *morphism of fibrations* if the top arrow takes cartesian arrows to cartesian arrows.  Most frequently when considering morphisms of fibrations, the bottom arrow $B'\to B$ is an identity.  A 2-cell between morphisms of fibrations is a pair of 2-cells, one lying over the other.  If the bottom arrow is an identity, this means that the top 2-cell is "vertical" (its components lie in fibers).

## Fibrations versus pseudofunctors

Given a fibration $p:E\to B$, we obtain a pseudofunctor $B^{op}\to Cat$ by sending each $b\in B$ to the category $E_b = p^{-1}(b)$ of objects mapping onto $b$ and morphisms mapping onto $1_b$.  To obtain the action on morphisms, given an $f:a\to b$ in $B$ and an object $e\in E_b$, we choose a cartesian arrow $\phi:e'\to e$ over $f$ and call its [[source]] $f^*(e)$.  The universal factorization property of cartesian arrows then makes $f^*$ into a functor $E_b \to E_a$, and it is easy to verify that it is a pseudofunctor.  The functor in the other direction is called the [[Grothendieck construction]].  This yields a [[strict 2-equivalence of 2-categories]] between

* fibrations over $B$, morphisms of fibrations over $Id_B$, and 2-cells over $id_{Id_B}$, and

* [[pseudofunctors]] $B^{op}\to Cat$, [[pseudonatural transformations]], and [[modifications]].

In fact, this is an instance of the general theory of representability for [[generalized multicategories]].  There is a monad $T$ whose pseudoalgebras are pseudofunctors $B^{op}\to Cat$, and whose "generalized multicategories" are functors $E\to B$.  Such a multicategory is "representable" precisely when it is a fibration, and moreover there is an induced monad $\hat{T}$ on $Cat/B$ which is [[lax-idempotent 2-monad|colax-idempotent]] and whose pseudoalgebras are precisely the fibrations.


## Remarks

* It is easy to verify that fibrations are closed under pullback in [[Cat]], and that the composite of fibrations is a fibration.  This latter property is notably difficult to even express in the language of pseudofunctors.

* Every fibration (or opfibration) is a [[Conduché functor]], and therefore an [[exponentiable morphism]] in [[Cat]].

* Fibrations are a "nonalgebraic" structure, since the base change functors $f^*$ are determined by universal properties, hence uniquely up to isomorphism.  By contrast, pseudofunctors are an "algebraic" structure, since the functors $f^*$ are specified, together with the necessary coherence data and axioms; the latter come for free in a fibration because of the universal property.

* A [[stack]], being a particular type of pseudofunctor, can also be described as a particular sort of fibration.  This was the original application for which Grothendieck introduced the notion.


## Examples 

* Let $Ring$ be the category of [[ring|rings]], and $Mod$ the category of pairs $(R,M)$ where $R$ is a ring and $M$ is a (left) $R$-module.  Then the evident forgetful functor $Mod\to Ring$ is a fibration and an opfibration.  The functors $f^*$ are given by restriction of scalars, $f_!$ is extension of scalars, and the right adjoint $f_*$ is coextension of scalars.

* Let $C$ be any category with pullbacks and $\mathbf{2}$ the free-living arrow, so that $C^{\mathbf{2}}$ is the category of arrows and commutative squares in $C$.  Then the "codomain" functor $C^{\mathbf{2}} \to C$ is a fibration and opfibration.  The cartesian arrows are precisely the pullback squares, and the functors $f_!$ are just given by composition.  The right adjoints $f_*$ exist iff $C$ is [[locally cartesian closed category|locally cartesian closed]].  The term "cartesian" is motivated by this example, which is usually called the **[[codomain fibration]]** over $C$.

* Let $C$ be any category and let $Fam(C)$ be the category of set-indexed families of objects of $C$.  The forgetful functor $Fam(C)\to Set$ taking a family to its indexing set is a fibration; the functors $f^*$ are given by reindexing.  They have left adjoints iff $C$ has small coproducts, and right adjoints iff $C$ has small products.

## Variations 

### Discrete and groupoidal fibrations

One important special case of a fibration is when each fiber is a [[groupoid]]; these correspond to pseudofunctors $B^{op}\to Grpd$.  These are also called *categories fibered in groupoids*.  A fibration $E\to B$ is fibered in groupoids precisely when *every* morphism in $E$ is cartesian.

Another important special case is when each fiber is a [[discrete category]]; these correspond to functors $B^{op}\to Set$.  These are also called *[[discrete fibrations]]*.  A functor $p\colon E\to B$ is a discrete fibration precisely when for every $e\in E$ and $f\colon b\to p(e)$ there is a *unique* lifting of $f$ to a morphism $e'\to e$.


### Opfibrations and bifibrations

We say that $p\colon E\to B$ is an **opfibration** if $p^{op}:E^{op}\to B^{op}$ is a fibration.  These correspond to covariant pseudofunctors $B\to Cat$.  A functor that is both a fibration and an opfibration is called a **[[bifibration]]**.  It is not hard to see that a fibration is a bifibration iff each functor $f^*$ has a left adjoint, written $f_!$ or $\Sigma_f$.  In many cases $f^*$ also has a right adjoint, written $f_*$ or $\Pi_f$, but this is not as easily expressible in fibrational language.

Grothendieck originally called an opfibration a *cofibered category*, and if the fibers are groupoids a [[category cofibered in groupoids]] (SGA I, [[Higher Topos Theory]]).  However, that term has fallen out of favor in the homotopy-theory and category-theory communities (though still used sometimes in algebraic geometry), because an opfibration still has a _lifting_ property, as is characteristic of other notions of [[fibration]], as opposed to the _extension_ property exhibited by [[cofibration]]s in [[homotopy theory]].

Note that an opfibration is the same as an internal fibration in the 2-category $Cat^{co}$, while it is the fibrations in the 2-category $Cat^{op}$ which are more deserving of the name "cofibration."

Note also that a given pseudofunctor $B^{op}\to Cat$ can be represented both by a fibration $E_1\to B$ and by an opfibration $E_2\to B^{op}$.  However $E_2$ is _not_ the opposite category of $E_1$.


### Non-evil version {#StreetFibration}

There is something [[evil]] about the notion of fibration, namely the requirement that for every $f:a\to b$ and $e\in E_b$ there exists a $\phi:e'\to e$ such that $p(e')$ is _[[equality|equal]]_, rather than merely [[isomorphism|isomorphic]], to $a$.  This is connected with the fact that we use strict fibers, rather than [[essential fiber]]s, and that fibrations and pseudofunctors can be recovered from each other up to isomorphism rather than merely equivalence.

While almost any fibration between "concrete" categories that arises in practice does satisfy this evil property, it is sometimes useful to have a non-evil version, for instance when working internally in a [[bicategory]] where equality of objects doesn't even really make sense.  The correct modification, first given by [[Ross Street]], is simply to require that for any $f:a\to b$ and $e\in E_b$ there exists a cartesian $\phi:e'\to e$ and an _isomorphism_ $h:p(e') \cong a$ such that $f\circ h = p(\phi)$; the definition of "cartesian" is unchanged; this gives the notion of [[Street fibration]].  Every [[equivalence of categories]] is a Street fibration, which is not true for the "evil" Grothendieck fibrations, but every Street fibration can be factored as an equivalence of categories followed by a Grothendieck fibration.

We might also think that it is evil to say that the target of the cartesian arrow $\phi$ is equal to the given object $e$, akin to the topological distinction between [[Serre fibrations]] and [[Dold fibrations]], where the initial point of a lifted path can only be specified up to homotopy.  However, this part of the definition is really better regarded as a typing assertion, akin to saying, in the definition of a [[product]] of two objects $A$ and $B$, that the target of the two projections $A\times B\to A$ and $A\times B \to B$ are *equal* to $A$ and $B$.  Moreover, any weakening along these lines would actually be equivalent to the version above: if we demand only that for any $f\colon a\to b$ in $B$ and $e\in E_b$, there exists a cartesian $\phi\colon e' \to \hat{e}$ with $p(\phi)=f$ and an isomorphism $\hat{e}\cong e$ in the fiber $E_b$, then you can just compose $\phi$ with the isomorphism $\hat{e}\cong e$ to get a cartesian arrow $\hat{\phi}\colon e'\to e$ with $p(\phi)=f$ still.  The reason this doesn't work in topology is that paths come with parametrizations, and requiring the lower triangle (in the square drawn at [[Dold fibration]]) to commute strictly prevents the reparametrization necessary to compose with a vertical homotopy.

The idea of [[proto-fibration]] is closely related to this.

### Internal version 

In a [[strict 2-category]] $K$, a morphism $p:E\to B$ is called a fibration if for every object $X$, $K(X,E)\to K(X,B)$ is a fibration of categories, and for every morphism $f:Y\to X$, the square
$$\array{ K(X,E) & \to & K(Y,E) \\ \downarrow && \downarrow \\ K(X,B) & \to & K(Y,B)}$$
is a morphism of fibrations.  There is an alternate characterization in terms of [[comma object]]s and adjoints, see [[fibration in a 2-category]].  The same definition works in a [[bicategory]], as long as we use the non-evil version above.  Interpreted in [[Cat]] we obtain the explicit notion we started with.


### Two-sided version 

A **two-sided fibration**, or a **fibration from $B$ to $A$**, is a span $A \leftarrow E \rightarrow B$ such that $E\to A$ is a fibration, $E\to B$ is an opfibration, and the structure "commutes" in a natural way.  Such two-sided fibrations correspond to pseudofunctors $A^{op}\times B \to Cat$.  If they are discrete, they correspond to functors $A^{op}\times B\to Set$, i.e. to [[profunctors]] from $B$ to $A$.

Explicitly, a **two-sided discrete fibration** is a span $q \colon E \to A$, $p \colon E \to B$ such that 
1. each $b \to pe$ in $B$ has a unique lift in $E$ that has codomain $e$ and is in the fiber over $qe$
1. each $qe \to a$ in $A$ has a unique lift in $E$ that has domain $e$ and is in the fiber over $pe$
1. for each $f\colon e \to e'$ in $E$, the codomain of the lift of $qf$ equals the domain of the lift of $pf$ and their composite is $f$.

A **two-sided fibration** is a span $q \colon E \to A$, $p \colon E \to B$ such that
1. each $b \to pe$ in $B$ has a cartesian lift in $E$ with codomain $e$ and lying in the fiber over the identity at $qe$
1. each $qe \to a$ in $A$ has an opcartesian lift in $E$ with domain $e$ and lying in the fiber over the identity at $pe$
1. for each $f \colon e \to e'$ in $E$ the canonical arrow between the codomain of any opcartesian lift of $qf$ as in (2) and the domain of the cartesian lift of $pf$ as in (1) is an isomorphism.

Note that a pseudofunctor $A^{op}\times B \to Cat$ can also be represented by an opfibration $E_1\to A^{op}\times B$ and by a fibration $E_2\to A\times B^{op}$, but there is no simple relationship between the three categories $E$, $E_1$, and $E_2$.


### Higher categorical versions 

There is also a notion of fibration for 2-categories that has been studied by Hermida.  See [[n-fibration]] for a general version.

For [[(∞,1)-category|(∞,1)-categories]] the notion of fibered category is modeled by the notion of [[Cartesian fibration]] of simplicial sets. The corresponding analog of the Grothendieck construction is discussed at [[(∞,1)-Grothendieck construction]].

## Alternate definitions

There are several alternate characterizations of when a functor is a fibration, some of which are more convenient for [[fibration in a 2-category|internalization]].  Here we mention a few.

### In terms of adjoints

Since Grothendieck fibrations are a strict notion, in what follows we denote by $E/p$ the strict [[comma category]] (i.e. determined up to isomorphism, not merely up to equivalence) and by $Cat/B$ the [[strict slice 2-category]] (elsewhere denoted $Cat/_s B$).

+--{: .un_lemma}
###### Lemma
A functor $p \colon E \to B$ is a cloven fibration if and only if the canonical functor $i \colon B \to E/p$ has a right adjoint $r$ in $Cat / B$.
=--
+-- {: .proof }
###### Proof
First, recall that the strict slice 2-category $Cat/X$ has objects the functors $C \to X$, as morphisms the commuting triangles
$$\array{C & \stackrel{h}{\to} & C' \\ & f \searrow \swarrow g &  \\  & X,  & }$$
and as 2-cells the natural transformations $\alpha : h_1 \to h_2$ such that $g\alpha = id_f$.

Next, recall that the [[comma category]] $B/p$ has objects the triples $(x, e, k)$, with $k \colon x \to p e$.  Let $\pi \colon B/p \to B$ denote the projection $(x, e, k) \mapsto x$.

The canonical morphism $p \to B/p$ is simply the inclusion functor of identity maps $i b = 1 \colon p b \to p b$.

Somewhat imprecisely, seeing both categories $E$ and $B/p$ as sitting over $B$ means that functors between those should be the identity on the $b$ component, and natural transformations should have the identity as their $b$ component.

To give an adjunction $i \dashv r$ it suffices to give, for each $k \colon x \to p e$ in $B/p$, an object $r k$ in $E$ such that $p r k = x$ and an arrow $i r k = 1_x \to k$ in $B/p$ that is [[universal arrow|universal]] from $i$ to $k$.  For the adjunction to live in $Cat/B$ we must have that $\pi \circ i r k = 1_{p r k} = 1_x$, so the universal arrow must be of the form
$$
\array{
  x & \overset{1}{\to} & x \\
  \mathllap{1} \downarrow & & \downarrow \mathrlap{p \epsilon_k} \\
  x & \underset{k}{\to} & p e
}
$$
and thus amounts to a choice of $\epsilon_k \colon r k \to e$ in $E$ such that $p \epsilon_k = k$.

The universal property of $\epsilon_k$ tells us that for any other morphism in $B/p$ from some $i y$ to $k$, i.e., for any $y$ and any pair $(f,g)$ making the square
$$
\array{
  p y & \stackrel{1}{\to} & p y \\
  \mathllap{f} \downarrow & & \downarrow \mathrlap{p g} \\
  x & \underset{k}{\to} & p e
}
$$
commute, there is a unique map $h \colon y \to r k$ in $B$ such that the above square factors in $B/p$ as
$$
\array{
  p y & \stackrel{1}{\to} & p y \\
  \mathllap{p h} \downarrow &  & \downarrow \mathrlap{p h} \\
  \mathllap{p r k =} x & \stackrel{1}{\to} & x \mathrlap{= p r k}\\
  \mathllap{1} \downarrow & & \downarrow \mathrlap{p \epsilon_k} \\
  x & \underset{k}{\to} & p e.
}
$$

In other words, the universal property provides a unique $h$ such that $\epsilon_k h = g$ and $p h = f$, which exactly asserts that $\epsilon_k$ is a cartesian lift of $k$.

So the existence of a right adjoint to $i$ means precisely that for each morphism $k \colon x \to p e$ a choice is given of a cartesian lift of $k$, which means in turn that $p$ is a cloven fibration.
=--

## Discussions

The following discussion brings out some interesting points about the equivalence between fibrations and pseudofunctors.

+--{: .query}
[[Sridhar Ramesh]]: I have a (possibly stupid) question about the nature of this equivalence. I assume the idea here is that moving from a cloven fibration to the corresponding pseudofunctor is in some sense "inverse" to carrying out the Grothendieck construction in the other direction. But, in trying to get a good intuition for the nuances of non-splittable fibrations, I seem to be stumbling upon just in what sense this is so. For example, consider the nontrivial group homomorphism from Z (integer addition) to Z_2 (integer addition modulo 2); this gives us a non-splittable fibration (and, for that matter, an opfibration), for which a cleavage can be readily selected. No matter what cleavage is selected, the corresponding (contravariant) pseudofunctor from Z_2 to Cat, it would appear to me, is the one which sends the unique object in Z_2 to the subcategory of Z containing only even integers (let us call this 2Z), and which sends both of Z_2's morphisms to identity; thus, it is actually a genuine functor, and indeed, a "constant" functor. Applying the Grothendieck construction now, I would seem to get back the projection from Z_2 X 2Z onto Z_2. But can this really be equivalent to the fibration I started with? After all, Z and Z_2 X 2Z are very different groups. So either "equivalence" means something trickier here than I realize, or I keep making a mistake somewhere along the line. Either way, it'd be great if someone could help me see the light.

[[Mike Shulman]]: Good question!  I think the missing subtlety is that a pseudofunctor is not uniquely determined by its action on objects and morphisms, even if its domain is a mere category (or a mere group); there are also natural coherence isomorphisms $g^* f^* \cong (g f)^*$ to take into account.  For instance, if $g$ is the nonidentity element of $\mathbb{Z}/2$, then $g g = 1$, so even if $g$ acts by the identity on $2\mathbb{Z}$, a pseudofunctor also contains the additional data of a natural automorphism of the identity of $2\mathbb{Z}$, i.e. a (central) element of $2\mathbb{Z}$.  If you start from $\mathbb{Z}$, then depending on your cleavage your element can be anything that's 2 mod 4, while if you start from $\mathbb{Z}/2\times 2\mathbb{Z}$, your element can be anything that's 0 mod 4.  Finally, there is a pseudonatural equivalence between two such pseudofunctors just when their corresponding elements differ by a multiple of 4, so you get exactly two equivalence classes of pseudofunctors, corresponding to the two groups $\mathbb{Z}$ and $\mathbb{Z}/2\times 2\mathbb{Z}$.  Of course we are reproducing the classification of group extensions via group cohomology.

By the way, this sort of thing (by which I mean, the cohomology class that classifies some categorical structure arising as the trace of a coherence isomorphism) happens in lots of other places too.  For instance, a [[2-group]] is classified by a group $G$, an abelian group $H$, an action of $G$ on $H$, and an element in $H^3(G;H)$.  If you replace a 2-group by a [[skeleton|skeletal]] one, then $G$ is the group of objects (which is strictly associative and unital, by skeletality), $H$ is the group of endomorphisms of the unit, and the action is defined by "whiskering".  The cohomology class comes from the [[associator]] isomorphism, which can (and often must) still be nontrivial even though the multiplication is "strictly associative" at the level of objects (by skeletality).

_Toby_:  So the multiplication is strictly associative, but the $2$-group itself is not a strict $2$-group, since it uses a different associator than the identity.  As in the example of the pseudofunctor from $Z_2$ to $Cat$, there is some additional structure here which is not trivial, even though it seems like it could be.

[[Sridhar Ramesh]]: Ah, of course, that's what I was missing. Thanks, both of you; that clears it all up.
=--

## References 

* Part B of [[Sketches of an Elephant]] (by [[Peter Johnstone]]) contains a lot of basic information and some good intuition, although he uses the non-standard words "prone" and "supine" where most people say "cartesian" and "opcartesian" morphism.

* [[Andre Joyal]], _[[joyalscatlab:Grothendieck fibrations]]_

* [[Angelo Vistoli]], _Notes on Grothendieck topologies, fibered categories and descent theory_ ([pdf](http://homepage.sns.it/vistoli/descent.pdf))

*  Notes by Streicher: "Fibred Categories &#224; l&#224; Jean B&#233;nabou" are available online  &lt;http://www.mathematik.tu-darmstadt.de/~streicher>.

* "Categorical logic and type theory" by B. Jacobs

* The Wikipedia entry on [Fibred category](http://en.wikipedia.org/wiki/Fibred_category) is okay, and contains a number of other references.

[[!redirects Grothendieck fibrations]]
[[!redirects Grothendieck opfibration]]
[[!redirects Grothendieck cofibration]]
[[!redirects Grothendieck opfibrations]]
[[!redirects Grothendieck cofibrations]]
[[!redirects opfibration]]
[[!redirects opfibrations]]
[[!redirects bifibration]]
[[!redirects bifibrations]]

[[!redirects fibered category]]
[[!redirects fibred category]]
[[!redirects fibered categories]]
[[!redirects fibred categories]]

[[!redirects (Grothendieck) fibration]]
[[!redirects (Grothendieck) fibrations]]

[[!redirects two-sided fibration]]
[[!redirects two-sided fibrations]]

[[!redirects morphism of fibrations]]
[[!redirects morphisms of fibrations]]
