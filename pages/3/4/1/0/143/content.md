#Idea#

A _sheaf_ is a [[presheaf]] that satisfies [[descent]].

A gentle, detailed introduction to the basic ideas of the notion "sheaf" is at

* [[motivation for sheaves, cohomology and higher stacks]].

A [[presheaf]] can be regarded as an assignment of "sets of structures to [[space and quantity|spaces]]", such that these structures can be pulled back along maps of spaces. A presheaf is a _sheaf_ if this assignment satisfies [[descent]]: if $\pi: Y \to X$ is a [[cover]] of a space $X$ by a space $Y$, then the collection of structures assigned to $X$ is [[isomorphism|isomorphic]] to the collection of structures assigned to $Y$ which _glue_ and hence descend from $Y$ down to $X$.

Generally, to any [[hypercover]] or [[local isomorphism]] $Y \to X$  and [[presheaf]] $A$ there is associated a [[descent]] [[set]] $Desc(Y,A)$ whose objects are the elements of $A(Y)$ which glue. There is also a canonical morphism

$$
  Hom(X,A) = A(X) \to Desc(Y,G) = Hom(Y,A)
  \,.
$$

A presheaf is a _sheaf_ if this canonical morphism is an [[isomorphism]], i.e. which is a [[local object]] with respect to [[local isomorphism]]s (or already for [[dense monomorphism]]s).

#Remarks#

* The [[vertical categorification|categorifications]] of sheaves are
  * [[stack|stacks]];
  * [[infinity-stack|infinity-stacks]].

Here the [[descent]] set ($0$-category) is replaced by a [[descent]] [[category]] or $\infty$-[[infinity-category|category]]. Notably in the context of [[(infinity,1)-category]] theory the [[(infinity,1)-category of (infinity,1)-sheaves]] has literally the same definition as the [[category of sheaves]] itself as a [[geometric embedding]] into the corresponding collection of presheaves.

#Definition#

There are many different equivalent aspects of the definition of sheaf.

Let $S$ be a [[site]].

A **sheaf** (of [[set]]s) is a [[presheaf]] (of sets) in $S$ that satisfies [[descent]] with respect to the corresponding [[Grothendieck topology]] in that it is a [[local object]] with respect to the [[local isomorphism]]s defined by the [[Grothendieck topology]] (for which it is sufficient to be a [[local object]] with respect to the [[local epimorphism]]s, see below).

The [[category of sheaves]] $Sh(S)$ is the full [[subcategory]] of $PSh(S) = [S^{op}, Set]$ on presheaves that are sheaves. The [[category of sheaves]] is a [[topos]] and the [[full and faithful functor]]

$$
  f_* : Sh(S) \hookrightarrow PSh(S)
$$

is a [[geometric embedding]] of topoi. The left [[exact functor|exact]] [[left adjoint]] $f^* : PSh(S) \to Sh(S)$ is [[sheafification]].

Conversely, every category of sheaves, hence every [[Grothendieck topology]] arises this way. So Gorthendieck topologies and their corresponding categories of sheaves can alternatively be defined as [[geometric embedding]]s into categories of presheaves.

The notion of sheaf and of [[sheafification]] makes sense for presheaves with values in some classes of categories $A$ other than sets, notably for $A$ a [[Grothendieck category]]. Such [[abelian sheaf|abelian sheaves]] give rise to [[abelian sheaf cohomology]].


##Remarks##

* The definition of [[category of sheaves]] as [[geometric embedding]] into [[presheaf]] categories is the one that generalizes straightforward to an [[(infinity,1)-category|(infinity,1)-categorical]] context where it yields a notion of [[infinity-stack]] in terms of [[(infinity,1)-category of (infinity,1)-sheaves]].


#Explicit description#


We now describe the derivation and the detailed description of various aspects of sheaves, the [[descent]] condition for sheaves and [[sheafification]], relating it to all the related notions

* [[geometric embedding]]

  * [[localization]]

  * [[homotopy category]]

* [[coverage]]

  * [[Grothendieck topology]]

  * [[Lawvere-Tierney topology]]

* [[local isomorphism]]

  * [[sieve]]

    * [[cover]]

    * [[hypercover]]

  * [[dense monomorphism]]

  * [[local epimorphism]]


## In terms of geometric embedding ##

Here we start by assuming that a [[geometric embedding]] into a [[presheaf]] category is given and derive the consequences.

So let $S$ be a [[small category]] and write $PSh(S) = [S^{op}, Set]$ for the corresponding [[topos]] of [[presheaf|presheaves]].

Assume then that another topos $Sh$ is given together with a [[geometric embedding]]

$$
  f : Sh \to PSh(S)
$$

i.e. with a [[full and faithful functor]]

$$
  f_* : Sh \to PSh(S)
$$

and a left [[exact functor]]

$$
  f^* : PSh(S) \to Sh
$$

Such that both form a pair of [[adjoint functor]]s

$$
  f^* \dashv f_*
$$

with $f^*$ [[left adjoint]] to $f_*$.

Write $W$ for the category

$$
  Core(PSh(S)) \hookrightarrow W \hookrightarrow PSh(S)
$$

consisting of all those morphisms in $PSh(S)$ that are sent to [[isomorphism]]s under $f^*$.

$$
  W = (f^*)^{-1}(Core(Sh))
  \,.
$$

From the discussion at [[geometric embedding]] we know that $Sh$ is equivalent to the full [[subcategory]] of $PSh(S)$ on all $W$-[[local object]]s.

Recall that an object $A \in PSh(S)$ is called a $W$-[[local object]] if for all $p : Y \to X$ in $W$ the morphism

$$
  p^* : PSh(S)(X,A) \to PSh(S)(Y,A)
$$

is an [[isomorphism]]. This we call the [[descent]] condition on presheaves (saying that a presheaf "descends" along $p$ from $Y$ "down to" $X$). Our task is therefore to identify the category $W$, show how it determines and is determed by a [[Grothendieck topology]] on $S$ -- equipping $S$ with the structure of a  [[site]] -- and characterize the $W$-[[local object]]s. These are (up to equivalence of categories) the objects of $Sh$, i.e. the sheaves with respect to the given [[Grothendieck topology]].

...

+-- {: .un_theorem}
###### Lemma

A morphism $Y \to X$ is in $W$ if and only if for every [[representable functor|representable presheaf]] $U$ and every morphism $U\to X$ the pullback $Y \times_X U \to U$ is in $W$
$$
  \array{
     Y \times_X U &\to& Y
     \\
     \downarrow^{\in W} && \downarrow^{\Leftrigtharroow \in W}
     \\
     U &\to& X
  }
  \,.
$$
=--

+-- {: .proof}
###### Proof

One direction is obvious; the other follows because in $PSh(S)$ [[commutativity of limits and colimits|colimits are stable under base change]].
=--

+-- {: .un_theorem}
###### Lemma

Every morphism in $W$ factors as an epimorphism followed by a monomorphism in $W$.
=--

+-- {: .proof}
###### Proof

Use factorization through [[image]] and [[coimage]], use exactness of $f^*$ to deduce that the factorization exists not only in $PSh(S)$ but even in $W$.
=--

+-- {: .un_theorem}
###### Corollary

A presheaf $A$ is $W$-local, i.e. a sheaf, already if it is local (satisfies descent) with respect to all [[monomorphism]]s in $W$.
=--

+-- {: .un_theorem}
###### Lemma

Monomorphisms in $PSh(S)$ are canonically in bijection with [[sieve]]s.
=--

+-- {: .un_theorem}
###### Corollaries

We have:
* Systems $W$ of weak equivalences defined by choice of [[geometric embedding]] $Sh \to PSh(S)$ is in canonical bijection with choice of [[Grothendieck topology]].
* A presheaf $A$ is $W$-local, i.e. local with respect to all [[local isomorphism]]s, if and only if it is local already with respect to all local isomorphisms which are monomorphisms, i.e. all [[dense monomorphism]], i.e. if and only if it satisfies sheaf condition for all covering [[sieve]]s.
=--

## In terms of sieves ##

One formalization of the descent set is obtained from representing a cover $Y$ by the corresponding [[presheaf]] $S_Y : C^{op} \to Set$ -- a [[sieve]] -- and defining the descent set as

$$
  Desc(Y,G) := [S^{op}, Set](S_Y, G)
  \,.
$$

So: given a [[site]] $(C, J)$, a _sheaf_ over that site is a [[presheaf]]

$$G: C^{op} \to Set$$

such that whenever $i: F \hookrightarrow \hom(-, c)$ is a [[Grothendieck topology|covering sieve]], the map

$$G(c) \stackrel{Yoneda}{\cong} Set^{C^{op}}(\hom(-, c), G) \stackrel{Set^{C^{op}}(i, G)}{\to} Set^{C^{op}}(F, G)$$

is an isomorphism.

## In terms of orientals ##

When generalizing sheaves to  [[stack|stacks]] and then to  [[infinity-stack|infinity-stacks]] the Hom-set $Set^{C^{op}}(F, G)$ in the above definition, representing the descent set (0-category), needs to be generalized to a corresponding [[category]] or [[infinity-category]] [[functor category|of infinity-functors]] whose objects are the $\infty$-functors from the cover/sieve $F$ to the presheaf $G$, whose morphisms are homotopies between these, whose higher morphisms are the higher homotopies. The technical problem is to formalize these $\infty$-categories of $\infty$-functors. This is one of the central issues of [[higher category theory]].

One partial solution to the problem has been given by Ross Street, who defined descent [[strict omega-category|strict omega-categories]] $Desc(Y,G)$ for $\omega$-category-valued presheaves $G : C^{op} \to \omega Cat$ in terms of [[oriental|orientals]]. The $\omega$-category $Desc(Y,G)$ can be regarded as the $\omega$-category of lax $\infty$-functors from the sieve associated with $Y$ to $G$.

In the case that the $\omega$-categories in questions happen to be just [[n-category|0-categories]] this reduces to the definitin of descent 0-categories for presheaves.

Of course the machinery of [[oriental|orientals]] is overkill for just defining sheaves, but it is instructive to understand sheaves in this language, since then the generalization to [[stack|stacks]] and [[infinity-stack|infinity-stacks]] is straightforward.

So let $\pi : Y \to X$ be a morphism of objects of $C$ such that the pullback of $\pi$ along itself

$$
  \array{
    Y^{[2]} &\stackrel{\pi_1}{\to}& Y
    \\
    \downarrow^{\pi_2} && \downarrow^\pi
    \\
    Y &\stackrel{\pi}{\to}& X
  }
$$

exists. Let $G : C^{op} \to Set \hookrightarrow \omega Cat$ be a [[strict omega-category]] valued presheaf which happens to take values just in $0$-[[0-category|categories]]. Then an _object_ (an element) in the descent $\omega$-category $Desc(Y,G)$ (which is a set here) is a tuple consisting of

* an element $a \in G(Y)$;

* a morphism $\pi_1^* a \stackrel{g}{\to} \pi_2^* a$ in $G(Y^{[2]})$, which is by assumption necessarily an
[[identity morphism]]: $\pi_1^* a \stackrel{=}{\to} \pi_2^* a$.

The point to notice is that the morphism $\pi_1^* a \stackrel{g}{\to} \pi_2^* a$ is the image of the [[oriental|first oriental]] $G_1 = \{a \to b\}$ in $G(Y^{[2]})$.

This definition can be formalized as an [[end]]

$$
  Desc(Y,G) := \int_{[n] \in \Delta}
  hom(O([n]), G(Y^n))
  \,,
$$

where

* $\Delta$ is the [[simplex category]];

* $O : \Delta \to \omega Cat$ are the [[oriental|orientals]].


From this definition one obtains the canonical morphism

$$
  G(X) \to Desc(Y,G)
$$

form the universal property of then end. The _sheaf condition_ is, as before, that this canonical morphism is an isomorphism for all covers $Y \to X$.

From the above explicit characterization of $Desc(Y,G)$ this is manifestly the familiar gluing condition for sheaves: the presheaf $G$ is a sheaf if the elements in $G(Y)$ which coincide (glue) on double intersections $Y^{[2]}$ correspond bijectively to the elements in $G(Y)$.



#Examples#

The archetypical example of sheaves are _sheaves of functions_:

* for $X$ a topological space, $\mathbb{C}$ a topological space and $O(X)$ the [[site]] of open subsets of $X$, the assignment $U \mapsto C(U,\mathbb{C})$ of continuous functions from $U$ to $\mathbb{C}$ for every open subset $U \subset X$ is a sheaf on $O(X)$.

* for $X$ a complex manifold and $\mathbb{C}$ a complex manifold, the assignment $U \mapsto C_{hol}{X,\mathbb{C}}$ of holomorphic functions in a sheaf.


#References#

The book by MacLane and Moerdijk has an emphasis on the [[topos]]-theoretic aspects of sheaves:

* S. MacLane, I. Moerdijk, [[Sheaves in Geometry and Logic]]

The book by Kashiwara and Shapira discusses sheaves with motivation from [[homological algebra]], [[abelian sheaf cohomology]] and [[homotopy theory]], leading over in the last chapter to the notion of [[stack]].

* Kashiwara, Shapira, [[Categories and Sheaves]], Springer
