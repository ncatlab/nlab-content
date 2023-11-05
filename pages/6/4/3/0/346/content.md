
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

A familiar kind of closed categories are [[closed monoidal category|closed monoidal categories]]. However, there is also a definition of _closed category_ that does not require the category to already be monoidal.  A monoidal structure $\otimes$, if it exists, can then be universally characterized as an (enriched) _left_ adjoint to the internal-hom, dual to the above characterization of internal-homs as right adjoints to $\otimes$; see below.

Although it may seem that in general the closed structure is less intuitive to work with than the monoidal structure, in some cases it is in fact more obvious what the correct internal-homs are than what the correct tensor product is, so the latter was originally defined as an adjoint to the former.  This is the case for the [[Gray tensor product]] and the [[projective tensor product]], for example, and was probably the case for [[abelian groups]] (the original notion of [[tensor product]]) as well.


## Definition

### Basic definition

A __closed category__ is a [[category]] $C$ together with the following data:

* A [[functor]] $[-,-] : C^{op} \times C \to C$, called the [[internal hom]]-functor.

* An [[object]] $I\in C$ called the *[[unit object]]*.

* A [[natural isomorphism]] $i\colon Id_C \cong [I,-]$.

* A transformation $j_X\colon I \to [X,X]$, [[extranatural]] in $X$.

* A transformation $L^X_{Y Z} \colon  [Y,Z] \to [ [X,Y],[X,Z]]$, natural in $Y$ and $Z$ and extranatural in $X$.

which is required to satisfy the following axioms.

* The following [[diagram]] commutes for any $X,Y$.

  $$\array{I & \overset{j_Y}{\to} & [Y,Y]\\
  & _{\mathllap{j_{[X,Y]}}}\searrow & \downarrow^{L^X_{Y Y}}\\
  & & [ [X,Y],[X,Y]]}$$

* The following diagram commutes for any $X,Y$.

  $$\array{[X,Y] & \overset{L^X_{X Y}}{\to} & [ [X,X],[X,Y]]\\
  & _{\mathllap{i_{[X,Y]}}}\searrow & \downarrow^{[j_X,1]}\\
  & & [I,[X,Y]]}$$

* The following diagram commutes for any $Y,Z$.

  $$\array{[Y,Z] & \overset{L^I_{Y Z}}{\to} & [ [I,Y],[I,Z]]\\
  & _{\mathllap{[1,i_Z]}}\searrow & \downarrow^{[i_Y,1]}\\
  & & [Y,[I,Z]]}$$

* The following diagram commutes for any $X,Y,U,V$.

  $$\array{[U,V] & \overset{L^Y_{U V}}{\to} & [ [Y,U],[Y,V]]\\
  ^{L^X_{U V}}\downarrow && \\
  [ [X,U],[X,V]] & &  \downarrow^{[1,L^X_{Y V}]} \\
  ^{L^{[X,Y]}_{[X,U],[X,V]}}\downarrow && \\
  [ [ [X,Y],[X,U]],[ [X,Y],[X,V]]] & \underset{[L^X_{Y U},1]}{\to} & [ [Y,U],[ [X,Y],[X,V]]]}$$

* Finally, the map $\gamma\colon C(X,Y) \to C(I,[X,Y])$ defined by $f \mapsto [1,f](j_X)$ is a [[bijection]].

Note that both a left-closed (non-symmetric) monoidal category and a right-closed (non-symmetric) monoidal category give rise to a closed category in this sense. See the discussion [on the nForum](https://nforum.ncatlab.org/discussion/4632/closed-category/?Focus=66659#Comment_66659).

### The Eilenberg-Kelly definition

The above definition is the one used in [LaPlaza](#LaPlaza77) and [Manzyuk](#Manzyuk09).  It differs slightly from the original definition in [Eilenberg & Kelly 1965](#EK65), which omitted the axiom involving $\gamma$ but assumed an "underlying-set-functor" $U\colon C \to Set$ as part of the structure, with an axiom asserting that $U([X,Y]) = C(X,Y)$ (naturally, i.e. as a strict equality of functors $C^{op}\times C\to Set$) and that the resulting isomorphism
$$ C(X,X) = U([X,X]) \overset{U i_{[X,X]}}{\to} U([I,[X,X]]) = C(I,[X,X]) $$
sends $1_X$ to $j_X$.  (This is then essentially a definition of $j_X$, so that it could be omitted from the definition.)

The two are essentially equivalent, and the one given here is perhaps a little simpler, as well as obeying the [[principle of equivalence]].  To be precise, every closed category in the sense of Eilenberg-Kelly is also one in the above sense, and conversely every closed category in the above sense is *isomorphic* to one in the sense of [Eilenberg & Kelly 1965](#EK65).  The latter has the same objects and internal-homs, but new hom-sets $\hat{C}(X,Y) \coloneqq C(I,[X,Y])$, and underlying-set functor $U(X) \coloneqq C(I,X)$ (note that this is different from $\hat{C}(I,X) = C(I,[I,X])$).  See [Manzyuk](#Manzyuk09) for the proof.

### Omitting units: prounital closed categories

The fact (discussed below) that closed categories, in the above sense, are equivalent to closed [[multicategories]] with unit, suggests that there ought to be a version of closed categories that *don't* necessarily have a unit object $I$.  In fact in this case the definition becomes simpler because we can omit all the $i$'s and $j$'s, but there is an additional wrinkle that we have to include "left evaluation" as a new operation.  Furthermore, it seems that we have to use the Eilenberg-Kelly version of the definition, not the LaPlaza one; the "underlying set" functor $U:C\to Set$ corresponds to the nullary homsets $C(;-)$ of a multicategory.

A **prounital closed category** is a [[category]] $C$ together with the following data:

* A [[functor]] $[-,-] : C^{op} \times C \to C$, called the [[internal hom]]-functor.

* A functor $U : C \to Set$.

* A transformation $L^X_{Y Z} \colon  [Y,Z] \to [ [X,Y],[X,Z]]$, natural in $Y$ and $Z$ and extranatural in $X$.

* A transformation $ev : U(X) \to C([X,Y], Y)$, natural in $X$ and extranatural in $Y$.

which is required to satisfy the following axioms.

* $U([X,Y]) = C(X,Y)$ strictly and naturally, i.e. $U \circ [-,-] = C(-,-)$ as functors $C^{op}\times C\to Set$.  (Note that this can be phrased in accord with the [[principle of equivalence]] by considering $U : C \to Set$ as a [[displayed category]] over $Set$.)

* For any $x\in U(X)$ and $f\in C(X,Y) = U([X,Y])$ we have $U(ev_x)(f) = U(f)(x)$ in $U(Y)$.

* For any $X,Y\in C$ we have $U(L^X_{Y Y})(1_Y) = 1_{[X,Y]}$.  (Note that $L^X_{Y Y} : [X,X] \to [ [X,Y],[X,Y]]$, so $U(L^X_{Y Y})(1_Y) : C(X,X) \to C([X,Y],[X,Y])$.)

* For any $X,Y\in C$ the composite $[X,Y] \xrightarrow{L^X_{X Y}} [ [X,X],[X,Y]] \xrightarrow{ev_{1_X}} [X,Y]$ is the identity.

* The following diagram commutes for any $X,Y,U,V$.

  $$\array{[U,V] & \overset{L^Y_{U V}}{\to} & [ [Y,U],[Y,V]]\\
  ^{L^X_{U V}}\downarrow && \\
  [ [X,U],[X,V]] & &  \downarrow^{[1,L^X_{Y V}]} \\
  ^{L^{[X,Y]}_{[X,U],[X,V]}}\downarrow && \\
  [ [ [X,Y],[X,U]],[ [X,Y],[X,V]]] & \underset{[L^X_{Y U},1]}{\to} & [ [Y,U],[ [X,Y],[X,V]]]}$$

* Some axiom(s) relating $L$ to $ev$.  For instance, for any $x\in U(X)$ the following diagram should commute:

  $$\array{ [Y,Z] & \overset{L^X_{Y Z}}{\to} & [ [X,Y],[X,Z]]\\
  & _{[ev_x,Z]}\searrow & \downarrow^{[ [X,Y],ev_x]} \\
  && [ [X,Y],Z]} $$

The third and fourth axioms, plus naturality of $ev$, should imply a more general form of the third axiom: for any $f:X\to Y$, the composite $[Y,Z] \xrightarrow{L^X_{Y Z}} [ [X,Y],[X,Z]] \xrightarrow{ev_f} [X,Z]$ equals the functorial action $[f,Z]$.

+--{: .standout}
I haven't worked out exactly what axioms are required here.
=--

### Symmetric and cartesian versions

A **symmetric closed category** is additionally equipped with natural isomorphisms $C^{X Y}_Z : [X,[Y,Z]] \cong [Y,[X,Z]]$ satisfying appropriate axioms; see [deSchipper75](#deSchipper75) and [DayLaPlaza78](#DayLaPlaza78).  These should correspond to [[symmetric multicategories]].  

Similarly, a "cartesian closed category" (there is an unfortunate terminological clash with [[cartesian closed category]]) should furthermore have morphisms $K^X_Y : Y\to [X,Y]$ and $T^X_Y : [X,[X,Y]]\to [X,Y]$ satisfying appropriate axioms.  They should correspond to [[cartesian multicategories]].  The relation to [[combinatory logic]] suggests that it should also be possible to axiomatize the cartesian case by replacing $L$, $C$, and $T$ with a single family of morphisms $S^X_{Y Z} : [X,[Y,Z]]\to [ [X,Y],[X,Z]]$.

+--{: .standout}
I don't know of anywhere that the details are worked out for the cartesian case.
=--


## Examples

* Any [[closed monoidal category]] gives a closed category, by simply forgetting the tensor product and remembering only the internal-hom.  Most examples seem to be of this sort (in fact, as discussed [below](#EmbedIntoCloseMon), *every* closed category arises as the full [[subcategory]] of a closed monoidal category).  However, as remarked above it, is often the case that the closed structure is "primary" and the tensor product is defined as a [[left adjoint]] to it (see below).  For instance:

  * In the category [[Ab]] of [[abelian groups]] the internal-hom $[X,Y]$ is the set of group homomorphisms $X\to Y$ with the pointwise addition, giving a closed category.

  * More generally, for any [[commutative theory]] $T$, the category of $T$-algebras has an internal-hom $[X,Y]$ that is the set of $T$-algebra maps with the pointwise operations (this is again a $T$-algebra by commutativity).

  * In the category [[2Cat]] of [[strict 2-categories]], the internal-hom $[X,Y]$ can be taken to be the category of strict 2-functors $X\to Y$ and [[lax natural transformation|pseudo, lax, or oplax natural transformations]] between them, giving three closed categories.

  * In the category $Unif$ of [[uniform spaces]] the internal-hom $[X,Y]$ can be taken to be the set of uniformly continuous functions $X\to Y$ with either the uniformity of uniform convergence or of pointwise convergence, giving two closed categories.

  In all these examples there is a corresponding tensor product, but its construction is much less intuitive, being essentially defined by a sort of [[adjoint functor theorem]] or [[initial lift]] that gives little information about what it actually looks like.

* Any [[multicategory]] which has a unit, i.e. an object $I$ such that $C(;Y) \cong C(I;Y)$ naturally, and is closed in the sense that for any $Y,Z$ there is an object $[Y,Z]$ with natural isomorphisms $C(X_1,\dots,X_n,Y;Z) \cong C(X_1,\dots,X_n; [Y,Z])$, gives rise to a closed category.  Conversely, from any closed category we can construct a multicategory of this sort, by defining the multimaps as $C(X_1,\dots,X_n; Z) = C(I, [X_1,\dots,[X_n,Z]])$.  Thus closed categories are essentially equivalent to closed unital multicategories.


## Properties

### The closed enrichment context

The closed structure on a category $\mathcal{V}_0$ is an enrichment context $\mathcal{V}$ relative to which we can define a [[category of V-enriched categories]]. From this point of view, a closed structure is more natural than a monoidal structure since most (if not all) of this structure is forced if one insists for an enrichment context $\mathcal{V}$ for which $\mathcal{V}_0$ is self-enriched, that is, isomorphic to the underlying category $\mathcal{V}^e_0$ of some $\mathcal{V}$-enriched category $\mathcal{V}^e$. See [[category of V-enriched categories]] for details.

### Reconstruction of monoidal structure

Suppose $C$ is a closed category such that the functor $[A,[B,-]] : C \to C$ is [[representable functor|representable]] as a $C$-enriched functor.  This means we have an object $A\otimes B$ and a $C$-natural isomorphism

$$ [A,[B,X]] \cong [A\otimes B,X]. $$

Then $C$ is a (closed) monoidal category.  See [Eilenberg--Kelly (1965)](#EK65) for details.

Note that although this is analogous to the fact that a monoidal category with right adjoints to tensor product is a closed category, the requisite hypothesis is stronger.  When $C$ is given as monoidal, we need only $Set$-natural isomorphisms of hom-sets $C(A\otimes B,X) \cong C(A,[B,X])$ to make it closed, whereas when $C$ is closed we need the above $C$-natural isomorphism of *internal* hom-objects to make it monoidal.

However, in the case when $C$ is a *symmetric* closed category, this stronger condition is unnecessary: to make $C$ (symmetric) monoidal it suffices to have external natural isomorphisms of hom-sets

$$ C(A, [B,X]) \cong C(A\otimes B, X). $$

Put differently, any symmetric closed category has an underlying (symmetric) [[promonoidal category]], whereas for a non-symmetric closed category the associativity of the promonoidal structure is an extra condition.  See [Day-Laplaza, Proposition 2.3](#DayLaPlaza78).


### Embedding into closed monoidal categories {#EmbedIntoCloseMon}

By a result due to Miguel LaPlaza [(1977)](#LaPlaza77), every closed category embeds [[full and faithful functor|fully and faithfully]] into a [[closed monoidal category]] by a strong [[closed functor]], i.e., one respecting closed structure up to suitably coherent isomorphism, and this closed functor is also strong monoidal if the original closed category is closed monoidal.  In particular, this functor is defined as the composition $q = y \circ p$ of the functor

$$p : C \to E^\op$$

sending an object $X \in C$ to the object (endofunctor) $[X,-] \in E = [C,C]$, together with the [[Yoneda embedding]] $y : E^\op \to [E, Set]$.  The closed monoidal structure on the presheaf category $[E,Set]$ is given by [[Day convolution]], using the monoidal structure of the category of endofunctors $E$ (see [[closed monoidal structure on presheaves#presheaves_over_a_monoidal_category|closed monoidal structure on presheaves over a monoidal category]]).

An alternative embedding was also sketched by Day [(1974)](#Day74), and later studied by Day and LaPlaza [(1978)](#DayLaPlaza78) in the case of symmetric closed categories.  This embedding is based on the fact that the construction of a closed monoidal category of presheaves does not actually require the base category to be monoidal: it suffices for it to be a [[promonoidal category#notes|promonoidal category]], and any closed category gives rise to such a promonoidal structure (perhaps a "lax" one with noninvertible associativity).  So, instead of using the category of copresheaves on the monoidal category of endofunctors $[ [C,C],Set]$ as in (LaPlaza 1977), the embedding in (Day 1974) and (Day and LaPlaza 1978) uses $[C,Set]$ itself.  One can then restrict to a small subcategory $A$ of $[C,Set]$ and compose further with a restricted version of its Yoneda embedding in order to obtain an embedding of $C$ into a closed monoidal category that also preserves certain colimits in $C$.


### Monadicity and 2-categories

Since the notion of closed category involves a contravariant functor and extranatural transformations, it cannot be expected to be [[2-monad|2-monadic]] over the [[2-category]] [[Cat]].  It is, however, 2-monadic over the 2-category $Cat_g$ of categories, functors, and natural isomorphisms, the [[core]] of [[Cat]].  In this way we obtain a 2-category $ClCat$ of closed categories, strong [[closed functors]], and [[closed natural transformations]].  One can also define a notion of non-strong, or "lax," closed functor; although these do not seemingly arise from the 2-monad in question, they generalize lax monoidal functors between closed monoidal categories.

## Extension systems

There is a notion that is related to a [[bicategory]] in the same way that a closed category is related to a [[monoidal category]], i.e. a [[horizontal categorification]] of a closed category.  It has a set of "objects", for any two objects $A,B$ a category $\mathcal{B}(A,B)$, and internal-hom functors like those in a [[closed bicategory]].  It was defined by [Street](#Street74) under the name **extension system**, although our page [[extension system]] is about an unrelated concept with the same name.

## Related concepts

* [[closed functor]]

* [[dual object in a closed category]]

* [[dualizing object in a closed category]]

* [[Kelly–Mac Lane graph]]

* [[locally cartesian closed category]]

## References 

Closed categories were first defined in:

* {#EK65} [[Samuel Eilenberg]], [[G. Max Kelly]], *Closed Categories*, in:  [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

Their [[coherence theorem]] was considered in terms of [[Kelly-Mac Lane graphs]] in 

* {#KM71} [[Max Kelly]], [[Saunders MacLane]], _Coherence in closed categories_, JPAA 1 (1971), 97-140 ([web](http://www.sciencedirect.com/science/article/pii/0022404971900132))

The relationship to [[monoidal categories]] was studied more deeply in:

* Jan Pavelka, _A note on closed categories_, Commentationes Mathematicae Universitatis Carolinae 17.2 (1976) 261-272. &lbrack;[10338.dmlcz/105692](https://dml.cz/handle/10338.dmlcz/105692), [pdf](https://dml.cz/bitstream/handle/10338.dmlcz/105692/CommentatMathUnivCarol_017-1976-2_5.pdf)&rbrack;


They were shown to be equivalent to closed unital [[multicategories]] here:

* Oleksandr Manzyuk, _Closed categories vs. closed multicategories_, [arXiv](http://arxiv.org/abs/0904.3137), 2009
 {#Manzyuk09}, [TAC 26, 2012] (http://www.tac.mta.ca/tac/volumes/26/5/26-05abs.html)

You can get some of the idea from a [post by Owen Biesel at the $n$-Caf&#233;](http://golem.ph.utexas.edu/category/2009/02/monoidal_closed_categories_and.html#c022133).

LaPlaza's theorem on embedding closed categories in closed monoidal categories is given in 

* {#LaPlaza77} Miguel LaPlaza, [_Embedding of Closed Categories Into Monoidal Closed Categories_](http://www.jstor.org/pss/1997823), Trans. AMS, Vol. 233 (1977). 

The alternative embedding of closed categories based on promonoidal Day convolution is discussed in

* {#Day74} [[Brian Day]], An embedding theorem for closed categories, _Lecture Notes in Mathematics_ 420 (1974), 55-64.

* {#DayLaPlaza78} B. J. Day and M. L. Laplaza, On Embedding Closed Categories, _Bull. Austral. Math. Soc._ 18 (1978), 357-371.

The latter uses the notion of symmetric closed category, which was first defined in

* {#deSchipper75} W.J. de Schipper, _Symmetric  closed categories_ (Mathematical Centre Tracts,  64.  Mathematisch Centrum, Amsterdam, 1975)

The generalization to a bicategory-like notion ("extension systems") appears in

* {#Street74} [[Ross Street]], *Elementary cosmoi I*, Category Seminar (Proc. Sem., Sydney, 1972/1973), 134–180, Lecture Notes in Math., vol. 420, Springer, Berlin, 1974.

[[!redirects closed categories]]
[[!redirects symmetric closed category]]
[[!redirects symmetric closed categories]]
[[!redirects semiclosed category]]
[[!redirects semiclosed categories]]
[[!redirects semi-closed category]]
[[!redirects semi-closed categories]]
[[!redirects prounital closed category]]
[[!redirects prounital closed categories]]
