
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[category]] $C$ is _closed_ if for any pair $a, b$ of [[objects]] the collection of [[morphisms]] from $a$ to $b$ can be regarded as forming itself an object of $C$.

This object is often denoted $hom(a,b)$ or $[a,b]$ or similar and often addressed as the _internal [[hom-object]]_ or simply the [[internal hom]].

A familiar kind of closed categories are [[closed monoidal category|closed monoidal categories]]. However, there is also a definition of _closed category_ that does not require the category to already be monoidal.  A monoidal structure $\otimes$, if it exists, can then be universally characterized as a _left_ adjoint to the internal-hom, dual to the above characterization of internal-homs as right adjoints to $\otimes$.  See [Eilenberg--Kelly (1965)](#EK65).

Although it may seem that in general the closed structure is less intuitive to work with than the monoidal structure, in some cases it is in fact more obvious what the correct internal-homs are than what the correct tensor product is, so the latter was originally defined as an adjoint to the former.  This is the case for the [[Gray tensor product]] and the [[projective tensor product]], for example, and was probably the case for [[abelian groups]] (the original notion of [[tensor product]]) as well.


## Definition

A __closed category__ is a [[category]] $C$ together with the following data:

* A [[functor]] $[-,-] : C^{op} \times C \to C$, called the [[internal hom]]-functor.

* An [[object]] $I\in C$ called the *[[unit object]]*.

* A [[natural isomorphism]] $i\colon Id_C \cong [I,-]$.

* A transformation $j_X\colon I \to [X,X]$, [[extranatural]] in $X$.

* A transformation $L^X_{Y Z} \colon  [Y,Z] \to [[X,Y],[X,Z]]$, natural in $Y$ and $Z$ and extranatural in $X$.

which is required to satisfy the following axioms.

* The following [[diagram]] commutes for any $X,Y$.

  $$\array{I & \overset{j_Y}{\to} & [Y,Y]\\
  & _{\mathllap{j_{[X,Y]}}}\searrow & \downarrow^{L^X_{Y Y}}\\
  & & [[X,Y],[X,Y]]}$$

* The following diagram commutes for any $X,Y$.

  $$\array{[X,Y] & \overset{L^X_{X Y}}{\to} & [[X,X],[X,Y]]\\
  & _{\mathllap{i_{[X,Y]}}}\searrow & \downarrow^{[j_X,1]}\\
  & & [I,[X,Y]]}$$

* The following diagram commutes for any $Y,Z$.

  $$\array{[Y,Z] & \overset{L^I_{Y Z}}{\to} & [[I,Y],[I,Z]]\\
  & _{\mathllap{[1,i_Z]}}\searrow & \downarrow^{[i_Y,1]}\\
  & & [Y,[I,Z]]}$$

* The following diagram commutes for any $X,Y,U,V$.

  $$\array{[U,V] & \overset{L^Y_{U V}}{\to} & [[Y,U],[Y,V]]\\
  ^{L^X_{U V}}\downarrow && \\
  [[X,U],[X,V]] & &  \downarrow^{[1,L^X_{Y V}]} \\
  ^{L^{[X,Y]}_{[X,U],[X,V]}}\downarrow && \\
  [[[X,Y],[X,U]],[[X,Y],[X,V]]] & \underset{[L^X_{Y U},1]}{\to} & [[Y,U],[[X,Y],[X,V]]]}$$

* Finally, the map $\gamma\colon C(X,Y) \to C(I,[X,Y])$ defined by $f \mapsto [1,f](j_X)$ is a [[bijection]].

This definition is from Manzyuk's paper below.  It differs slightly from Eilenberg-Kelly's original definition, which omitted $\gamma$ but assumed an "underlying-set-functor" $U\colon C \to Set$ as part of the structure, with an axiom asserting that $U([X,Y]) = C(X,Y)$ and that the resulting isomorphism
$$ C(X,X) = U([X,X]) \overset{U i_{[X,X]}}{\to} U([I,[X,X]]) = C(I,[X,X]) $$
sends $1_X$ to $j_X$.  The two are essentially equivalent, and the one given here is perhaps a little simpler.

+-- {: .query}
[[Tobias Fritz]]: I suspect there is a variant of the definition involving a transformation $R^Z_{X Y} \colon  [X,Y] \to [[Y,Z],[X,Z]]$ rather than $L$. Is this correct? If so, how do these two definitions relate? Can one of them be expressed in terms of the other? Or is there a refined definition which comprises both $L$ and $R$?

[Discussion](http://nforum.mathforge.org/discussion/4632/closed-category/)
=--


## Examples

* Any [[closed monoidal category]] gives a closed category, by simply forgetting the tensor product and remembering only the internal-hom.  Most examples seem to be of this sort, although as remarked above it is often the case that the closed structure is "primary" and the tensor product is defined as a [[left adjoint]] to it. Notice also, as discussed [below](#EmbedIntoCloseMon) that every closed category arises as the full [[subcategory]] of a closed monoidal category.

* Any [[multicategory]] which has a unit, i.e. an object $I$ such that $C(;Y) \cong C(I;Y)$ naturally, and is closed in the sense that for any $Y,Z$ there is an object $[Y,Z]$ with natural isomorphisms $C(X_1,\dots,X_n,Y;Z) \cong C(X_1,\dots,X_n; [Y,Z])$, gives rise to a closed category.  Conversely, from any closed category we can construct a multicategory of this sort, by defining the multimaps as $C(X_1,\dots,X_n; Z) = C(X_1, [X_2,\dots,[X_n,Z]])$.  Thus closed categories are essentially equivalent to closed unital multicategories.


## Properties

### Embedding into closed monoidal categories {#EmbedIntoCloseMon}

By a result due to Miguel LaPlaza [(1977)](#LaPlaza77), every closed category embeds [[full and faithful functor|fully and faithfully]] into a [[closed monoidal category]] by a strong [[closed functor]], i.e., one respecting closed structure up to suitably coherent isomorphism, and this closed functor is also strong monoidal if the original closed category is closed monoidal.  In particular, this functor is defined as the composition $q = y \circ p$ of the functor

$$p : C \to E^\op$$

sending an object $X \in C$ to the object (endofunctor) $[X,-] \in E = [C,C]$, together with the [[Yoneda embedding]] $y : E^\op \to [E, Set]$.  The closed monoidal structure on the presheaf category $[E,Set]$ is given by [[Day convolution]], using the monoidal structure of the category of endofunctors $E$ (see [[closed monoidal structure on presheaves#presheaves_over_a_monoidal_category|closed monoidal structure on presheaves over a monoidal category]]).

An alternative embedding was also sketched by Day [(1974)](#Day74), and later studied by Day and LaPlaza [(1978)](#DayLaPlaza78) in the case of symmetric closed categories.  This embedding is based on the fact that the construction of a closed monoidal category of presheaves does not actually require the base category to be monoidal: it suffices for it to be a [[promonoidal category]], and any closed category is equipped with such a promonoidal structure.  So, instead of using the monoidal category of endofunctors $E = [C,C]$ as in (LaPlaza 1977), the embedding in (Day 1974) and (Day and LaPlaza 1978) uses a small subcategory $A$ of the category of presheaves $[C,Set]$, and then again composes with the Yoneda embedding $A^{op} \to [A,Set]$.

### Monadicity and 2-categories

Since the notion of closed category involves a contravariant functor and extranatural transformations, it cannot be expected to be [[2-monad|2-monadic]] over the [[2-category]] [[Cat]].  It is, however, 2-monadic over the 2-category $Cat_g$ of categories, functors, and natural isomorphisms, the [[core]] of [[Cat]].  In this way we obtain a 2-category $ClCat$ of closed categories, strong [[closed functors]], and [[closed natural transformations]].  One can also define a notion of non-strong, or "lax," closed functor; although these do not seemingly arise from the 2-monad in question, they generalize lax monoidal functors between closed monoidal categories.

### The closed enrichment context

The closed structure on a category $\mathcal{V}_0$ is an enrichment context $\mathcal{V}$ relative to which we can define a [[category of V-enriched categories]]. From this point of view, a closed structure is more natural than a monoidal structure since most (if not all) of this structure is forced if one insists for an enrichment context $\mathcal{V}$ for which $\mathcal{V}_0$ is self-enriched, that is, isomorphic to the underlying category $\mathcal{V}^e_0$ of some $\mathcal{V}$-enriched category $\mathcal{V}^e$. See [[category of V-enriched categories]] for details.


## Related concepts

* [[closed functor]]

* [[dual object in a closed category]]

* [[dualizing object in a closed category]]

* [[Kelly–Mac Lane graph]]


## References 

Closed categories were first defined here:

* {#EK65} [[Samuel Eilenberg]] and [[Max Kelly]], _Closed categories_.  Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965).  (Please don\'t put a link to unauthorised copies here, since this may put the nLab, whose servers are located within the United States, at legal liability.  See [discussion](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=2048).)

Their [[coherence theorem]] was considered in terms of [[Kelly-Mac Lane graphs]] in 

* {#KM71} [[Max Kelly]], [[Saunders MacLane]], _Coherence in closed categories_, JPAA 1 (1971), 97-140 ([web](http://www.sciencedirect.com/science/article/pii/0022404971900132)) 


They were shown to be equivalent to closed unital [[multicategories]] here:

* Oleksandr Manzyuk, _Closed categories vs. closed multicategories_, [arXiv](http://arxiv.org/abs/0904.3137).

You can get some of the idea from a [post by Owen Biesel at the $n$-Caf&#233;](http://golem.ph.utexas.edu/category/2009/02/monoidal_closed_categories_and.html#c022133).

LaPlaza's theorem on embedding closed categories in closed monoidal categories is given in 

* {#LaPlaza77} Miguel LaPlaza, [_Embedding of Closed Categories Into Monoidal Closed Categories_](http://www.jstor.org/pss/1997823), Trans. AMS, Vol. 233 (1977). 

The alternative embedding of closed categories based on promonoidal Day convolution is discussed in

* {#Day74} [[Brian Day]], An embedding theorem for closed categories, _Lecture Notes in Mathematics_ 420 (1974), 55-64.

* {#DayLaPlaza78} B. J. Day and M. L. Laplaza, On Embedding Closed Categories, _Bull. Austral. Math. Soc._ 18 (1978), 357-371.

[[!redirects closed category]]
[[!redirects closed categories]]