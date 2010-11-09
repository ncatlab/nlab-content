
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--




#Contents#
* tic
{:toc}


## Idea

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

**Remarks**

* The [[vertical categorification|categorifications]] of sheaves are
  * [[stack|stacks]];
  * [[infinity-stack|infinity-stacks]].

Here the [[descent]] set ($0$-category) is replaced by a [[descent]] [[category]] or $\infty$-[[infinity-category|category]]. Notably in the context of [[(infinity,1)-category]] theory the [[(infinity,1)-category of (infinity,1)-sheaves]] has literally the same definition as the [[category of sheaves]] itself as a [[geometric embedding]] into the corresponding collection of presheaves.

## Definition

There are many different equivalent aspects of the definition of sheaf.

Let $S$ be a [[site]].

A **sheaf** (of [[set]]s) is a [[presheaf]] (of sets) in $S$ that satisfies [[descent]] with respect to the corresponding [[Grothendieck topology]] in that it is a [[local object]] with respect to the [[local isomorphism]]s defined by the [[Grothendieck topology]]. For this it is sufficient to be a [[local object]] with respect to the [[dense monomorphism]]s into [[representable functor|representables]], as described in more detail below. A [[dense monomorphism]] into a representable is a covering [[sieve]], namely a morphism of the form

$$
  colim( U \times_X U \stackrel{\to}{\to} U)
  \to 
  X
$$

where

$U = \coprod_\alpha U_\alpha$ is the [[coproduct]] of a covering family $\{U_\alpha \}$ for $X$ of objects in $S$ as presheaves (the [[Yoneda embedding]] $S \to PSh(S)$ is implicit throughout).

So a [[presheaf]] $A$ is [[local object|local]] with respect to this morphism if there is a bijection of sets

$$
  Hom(X,A) \simeq Hom(colim( U \times_X U \stackrel{\to}{\to} U)
)
 \,.
$$

By the defining universal property of the [[colimit]] ([[coproduct]] and [[coequalizer]] in this case) it follows that the [[hom-set]] on the right consists of 

* morphisms $U \to A$, wich by the [[coproduct]] property are the same as collections of morphisms $\{U_\alpha \to A\}$, which by the [[Yoneda lemma]] are the same as collections of elements $\{s_\alpha \in A(U_\alpha)\}$;

* such that the two pullbacks to $U \times X U = \coprod_{\alpha,\beta} U_\alpha \times_X U_\beta$ coincide; which means in terms of the $\{s_\alpha\}$ that these glue on double overlaps in that $s_\alpha|_{U_{\alpha,\beta}} = s_\beta|_{U_{\alpha, \beta}}$.

This is the sheaf condition as one often sees it stated in the literature, especially for the case that $S$ is a [[category of open subsets]] of some [[topological space]].


The [[category of sheaves]] $Sh(S)$ is the full [[subcategory]] of $PSh(S) = [S^{op}, Set]$ on presheaves that are sheaves. The [[category of sheaves]] is a [[topos]] and the [[full and faithful functor]]

$$
  f_* : Sh(S) \hookrightarrow PSh(S)
$$

is a [[geometric embedding]] of topoi. The left [[exact functor|exact]] [[left adjoint]] $f^* : PSh(S) \to Sh(S)$ is [[sheafification]].

Conversely, every category of sheaves, hence every [[Grothendieck topology]] arises this way. So Gorthendieck topologies and their corresponding categories of sheaves can alternatively be defined as [[geometric embedding]]s into categories of presheaves.

The notion of sheaf and of [[sheafification]] makes sense for presheaves with values in some classes of categories $A$ other than sets, notably for $A$ a [[Grothendieck category]]. Such [[abelian sheaf|abelian sheaves]] give rise to [[abelian sheaf cohomology]].


**Remark** The definition of [[category of sheaves]] as [[geometric embedding]] into [[presheaf]] categories is the one that generalizes straightforward to an [[(infinity,1)-category|(infinity,1)-categorical]] context where it yields a notion of [[infinity-stack]] in terms of [[(infinity,1)-category of (infinity,1)-sheaves]].


## Explicit description


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


### In terms of geometric embedding 

Here we start by assuming that a [[geometric embedding]] into a [[presheaf]] category is given and derive the consequences.

So let $S$ be a [[small category]] and write $PSh(S) = PSh_S = [S^{op}, Set]$ for the corresponding [[topos]] of [[presheaf|presheaves]].

Assume then that another topos $Sh(S) = Sh_S$ is given together with a [[geometric embedding]]

$$
  f : Sh(S) \to PSh(S)
$$

i.e. with a [[full and faithful functor]]

$$
  f_* : Sh(S) \to PSh(S)
$$

and a left [[exact functor]]

$$
  f^* : PSh(S) \to Sh(S)
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
  W = (f^*)^{-1}(Core(Sh_S))
  \,.
$$

From the discussion at [[geometric embedding]] we know that $Sh(S)$ is equivalent to the full [[subcategory]] of $PSh(S)$ on all $W$-[[local object]]s.

Recall that an object $A \in PSh(S)$ is called a $W$-[[local object]] if for all $p : Y \to X$ in $W$ the morphism

$$
  p^* : PSh_S(X,A) \to PSh_S(Y,A)
$$

is an [[isomorphism]]. This we call the [[descent]] condition on presheaves (saying that a presheaf "descends" along $p$ from $Y$ "down to" $X$). Our task is therefore to identify the category $W$, show how it determines and is determed by a [[Grothendieck topology]] on $S$ -- equipping $S$ with the structure of a  [[site]] -- and characterize the $W$-[[local object]]s. These are (up to equivalence of categories) the objects of $Sh$, i.e. the sheaves with respect to the given [[Grothendieck topology]].


+-- {: .un_lemma}
###### Lemma

A morphism $Y \to X$ is in $W$ if and only if for every [[representable functor|representable presheaf]] $U$ and every morphism $U\to X$ the pullback $Y \times_X U \to U$ is in $W$
$$
  \array{
     Y \times_X U &\to& Y
     \\
     \downarrow^{\in W} && \downarrow^{\Leftrightarrow \in W}
     \\
     U &\to& X
  }
  \,.
$$
=--



+-- {: .proof}
###### Proof

Since $W$ is stable under [[pullback]] (as described at [[geometric embedding]]: simply because $f^*$ preserves finite limits) it is clear that $Y \times_X U \to U$ is in $W$ if $Y \to X$ is.

To get the other direction, use the [[co-Yoneda lemma]] to write $X$ as a [[colimit]] of [[representable functor|representables]] over the [[comma category]] $(Y/const_X)$ (with $Y$ the [[Yoneda embedding]]):

$$
  X \simeq colim_{U_i \to X} U_i
  \,.
$$

Then pull back $Y \to colim_{U_i \to X} U$ over the entire colimiting cone, so that over each component we have

$$
  \array{
    Y \times_X U_i &\to& Y
    \\
    \downarrow && \downarrow
    \\
    U_i &\to& X
  }
  \,.
$$

Using that in $PSh(S)$ [[commutativity of limits and colimits|colimits are stable under base change]] we get

$$
  colim_i (Y \times_X U_i) \simeq (colim_i U_i) \times_X Y
  \,.
$$

But since $X \simeq colim_i U_i$ the right hand is $X \times_X Y$, which is just $Y$. So $Y = colim_i (Y \times_X U_i)$ and we find that $Y \to X$ is a morphism of colimits. But under $f^*$ the two respective diagrams become isomorphic, since $Y \times_X U_i \to U_i$ is in $W$. That means that the corresponding morphism of colimits $f^*(Y \to X)$ (since $f^*$ preserves colimits) is an isomorphism, which finally means that $Y \to X$ is in $W$.
=--

+-- {: .un_lemma}
###### Lemma

A presheaf $A \in PSh(S)$ is a [[local object]] with respect to all of $W$ already if it is local with respect to those morphisms in $W$ whose codomain is [[representable functor|representable]]
=--


+-- {: .proof}
###### Proof

Rewriting the morphism $Y \to X$ in $W$ in terms of
colimits as in the above proof

$$
  \array{  
     colim_{U \to X} U_i \times_X Y 
      &\stackrel{\simeq}{\to}& Y 
     \\
     \downarrow && \downarrow
     \\
     colim_{U \to X} U &\stackrel{\simeq}{\to}& X
  }
$$

we find that $A(X) \to A(Y)$ equals

$$
  lim_{U \to X} (A(U) \to A(U \times_X Y))
  \,.
$$

If $A$ is local with respect to morphisms $W$ with representable codomain, then by the above if $Y \to X$ is in $W$ all the morphisms in the limit here are isomorphisms, hence

$$
  \cdots = Id_{A(X)}
  \,.
$$
=--


+-- {: .un_lemma}
###### Lemma

Every morphism $Y \to X$ in $W \subset PSh(S)$ factors as an epimorphism followed by a monomorphism in $PSh(S)$ with both being morphisms in $W$.
=--

+-- {: .proof}
###### Proof

Use factorization through [[image]] and [[coimage]], use exactness of $f^*$ to deduce that the factorization exists not only in $PSh(S)$ but even in $W$.

More in detail, given $Y \to X$ we get the diagram

$$
  \array{
    Y \times_X Y &&\to&& Y
    \\
     &&& \swarrow
    \\
    \downarrow &&Y \sqcup_{Y \times_X Y} Y && \downarrow
    \\
    & \nearrow && \searrow
    \\
    Y && \to && X
  }
  \,.
$$

Because $f^*$ is exact, the pullbacks and pushouts in this diagram remain such under $f^*$. But since $f^*(Y \to X)$ is an isomorphism by assumption, the all these are pullbacks and pushouts along isomorphisms in $Sh(S)$, so all morphisms in the above diagram map to isomorphisms in $Sh(S)$, hence the entire diagram in $PSh(S)$ is in $W$.

Since the morphism $Y \sqcup_{Y \times_X Y} Y  \to X$ out of the [[coimage]] is at the same time the [[equalizer|equalizing]] morphism into the [[image]] $lim(X \stackrel{\to}{\to} X \sqcup_Y X)$, it is a [[monomorphism]].
=--


+-- {: .un_definition}
###### Definition

The monomorphisms in $PSh(S)$ which are in $W$ are
called [[dense monomorphism]]s.

=--


+-- {: .un_lemma}
###### Lemma

Every [[monomorphism]] $Y \to X$ with $X$ [[representable functor|representable]] is of the form

$$
  Y = colim ( U \times_X U \to U  )
$$

for $U = \sqcup_{\alpha} U_\alpha$ a disjoint union of representables
=--

+-- {: .proof}
###### Proof

This is a direct consequence of the standard fact that
subfunctors are in bijection with [[sieve]]s.
=--


+-- {: .un_corollary}
###### Corollary

If a presheaf $A$ is [[local object|local]] with
respect to all [[dense monomorphism]]s, then it is already local with respect to all morphisms $Y \to X$ of the form

$$
  \array{
    Y
    \\
    \downarrow
    \\
    X
  }
  =
  colim
  \left(
  \array{
    W &\stackrel{\to}{\to}& U 
    \\
    \;\;\downarrow^{dense mono} && \downarrow^{Id}
    \\
    U \times_X U & \stackrel{\to}{\to}&  U
  }
  \right)
$$

with the left vertical morphism a [[dense monomorphism]]
 
(and with $U = \sqcup_\alpha U_\alpha$ the disjoint union (of representable presheaves) over a [[cover]]ing family of objects.)
=--


+-- {: .un_definition}
###### Definition 

The morphisms in $W$ with representable codomain 


* of the form $colim (U \times_X U \stackrel{\to}{\to} U) \to X$ as above are [[cover]]s:

* of the form $colim (W  \stackrel{\to}{\to} U) \to X$ (with $W$ a cover of $U \times_X U$) as above are [[hypercover]]s

of the representable $X$.
=--




+-- {: .un_proposition}
###### Proposition

A presheaf $A$ is $W$-local, i.e. a sheaf, already if it is local (satisfies [[descent]]) with respect to all [[cover]]s, i.e. all [[dense monomorphism]]s with codomain a [[representable functor|representable]].
=--

>[[Urs Schreiber|Urs]]: the above shows this almost. I am not sure yet how to see the remaining bit directly, without making recourse to the full machinery leading up to section VII, 4, corollary 7 in [[Sheaves in Geometry and Logic]].

So we finally conclude:


+-- {: .un_corollary}
###### Corollaries

We have:

* Systems $W$ of weak equivalences defined by choice of [[geometric embedding]] $f : Sh(S) \to PSh(S)$ are in canonical bijection with choice of [[Grothendieck topology]]. 

* A presheaf $A$ is $W$-local, i.e. local with respect to all [[local isomorphism]]s, if and only if it is local already with respect to all [[dense monomorphism]], i.e. if and only if it satisfies sheaf condition for all covering [[sieve]]s.
=--

From the _assumption_ that $f : Sh(S) \to PSh(S)$ is a [[geometric embedding]] follows at once the following explicit description of the [[sheafification]] functor
$f^* : PSh(S) \to Sh(S)$.

+-- {: .un_lemma}
###### Lemma (Sheafification)

For $A \in PSh(S)$ a presheaf, its [[sheafification]] $\bar A := f_* f^* A$ is the presheaf given by

$$
  \bar A : U \mapsto colim_{(Y \to U) \in W} A(U)
$$
=--

+-- {: .proof}
###### Proof

By the discussion at [[geometric embedding]] the category $Sh(S)$ is equivalent to the [[localization]] $PSh(S)[W^{-1}]$, which in turn is the category with the same objects as $PSh(S)$ and with morphisms given by spans out of hypercovers in $W$

$$
  PSh(S)[W^{-1}](X,A) =
  colim_{(Y \to X) \in W} A(X)
  \,.
$$

So we have

$$ \array {
  Sh(S) &&\stackrel{\stackrel{f_*}{\to}}{\stackrel{f^*}{\leftarrow}}&
  PSh(S)
  \\
  & \searrow_{\simeq}&\Downarrow^{\simeq}&  \downarrow
  \\
  &&
  PSh(S)[W^{-1}]
  \,.
} $$

and deduce

* by [[Yoneda lemma|Yoneda]] that $\bar A(U) = PSh_S(U, \bar A)$;

* by the [[adjoint functor|hom-adjunction]] this is $\cdots \simeq Sh_S(\bar U, \bar A)$;

*  by the equivalence just mentioned this is
$\cdots \simeq PSh_S[W^{-1}](U,A)$.
=--



+-- {: .un_remark}
###### Remark: covers versus hypercovers

For checking the sheaf condition the [[dense monomorphism]]s, i.e. the ordinary [[cover]]s are already sufficient. But for [[sheafification]] one really needs the [[local isomorphism]]s, i.e. the [[hypercover]]s. If one takes the colimit in the sheafification prescription above only over [[cover]]s, one obtains instead of sheafification the plus-construction.
=--


+-- {: .un_definition}
###### Definition: plus-construction

For $A \in PSh(S)$ a presheaf, the **plus-construction**
on $A$ is the presheaf 

$$
  A^+ : X \mapsto  colim_{(Y \hookrightarrow X) \in W } A(Y)
$$

where the colimit is over all [[dense monomorphism]]s (instead of over all [[local isomorphism]]s as for [[sheafification]] $\bar A$).
=--

+-- {: .un_remark}
###### Remark: plus-construction versus sheafification

In general $A^+$ is not yet a sheaf. It is howver in general closer to being a sheaf than $A$ is, in that it is a [[separated presheaf]].


But applying the plus-construction twice yields the desired sheaf

$$
  (A^+)^+ = \bar A
  \,.
$$

This is essentially due to the fact that in the context of ordinary sheaves discussed here, all [[hypercover]]s are already of the form

$$
  colim(W \stackrel{\to}{\to} U)
$$

for $W \to U \times_X U$ a cover. For higher [[stack]]s the hypercover is in general a longer simplicial object of covers and accordingly if one restricts to covers instead of using hypercovers one will need to use the plus-construction more and more often.
=--


### In terms of sieves

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

### In terms of orientals 

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



## Examples

The archetypical example of sheaves are _sheaves of functions_:

* for $X$ a topological space, $\mathbb{C}$ a topological space and $O(X)$ the [[site]] of open subsets of $X$, the assignment $U \mapsto C(U,\mathbb{C})$ of continuous functions from $U$ to $\mathbb{C}$ for every open subset $U \subset X$ is a sheaf on $O(X)$.

* for $X$ a complex manifold and $\mathbb{C}$ a complex manifold, the assignment $U \mapsto C_{hol}{X,\mathbb{C}}$ of holomorphic functions in a sheaf.


## Related concepts

* [[presheaf]] /  **sheaf** / [[cosheaf]]

* [[2-sheaf]] / [[stack]]

* [[(∞,1)-sheaf]] / [[∞-stack]] 


## References

The book by MacLane and Moerdijk has an emphasis on the [[topos]]-theoretic aspects of sheaves:

* S. MacLane, I. Moerdijk, [[Sheaves in Geometry and Logic]]

The book by Kashiwara and Shapira discusses sheaves with motivation from [[homological algebra]], [[abelian sheaf cohomology]] and [[homotopy theory]], leading over in the last chapter to the notion of [[stack]].

* Kashiwara, Shapira, [[Categories and Sheaves]], Springer

* Dugger, Sheaves and Homotopy Theory ([pdf](http://ncatlab.org/nlab/files/cech.pdf))

[[!redirects sheaves]]