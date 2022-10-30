
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **derivator** is a refinement of a [[homotopy category]] which also includes information about [[homotopy limits]] and colimits.  In some cases derivators can be used where one might otherwise need to use [[(∞,1)-categories]], which can be helpful since their theory is much simpler and purely (2-)categorical.

Very similar structures were invented independently by [[Grothendieck]] (who introduced the name "derivator"), Heller (who called his version "homotopy theories"), and Franke (who considered only the [[stable derivator|stable]] case and called his version a "system of triangulated diagram categories").  The definition given below combines elements from the work of all three.

## Motivation

The notion of derivator can be motivated in several ways.

### As a halfway house

Suppose we start from the perspective that what we really study in [[homotopy theory]] are [[(∞,1)-categories]].  The [[homotopy category of an (∞,1)-category]] (the 1-category obtained by setting all equivalent 1-morphisms equal) is a fairly coarse invariant, but for some purposes it is sufficient.  On the other hand, sometimes we need more than merely the homotopy category, but doing everything with $(\infty,1)$-categories can be technically daunting.  Frequently, all we need from an $(\infty,1)$-category that is not present in its homotopy category is to know that we have well-behaved constructions of [[homotopy limit]]s and [[homotopy colimit]]s.

A *derivator* is thus a halfway-house, containing more information than a homotopy category, but being easier to work with than an $(\infty,1)$-category.  It consists of a homotopy category together with extra structure that enables one to compute with homotopy limits and colimits.  Any $(\infty,1)$-category with sufficiently many limits and colimits has an underlying derivator, and working with these derivators suffices for a surprising number of things we may want to do with $(\infty,1)$-categories.  However, derivators are an essentially 1-categorical notion, so we can study them using ordinary [[2-category]] theory.  Thus derivators provide a "truncated" version of [[higher category theory]], which gives us the language to characterize higher category theory using only usual [[category theory]], without any emphasis on any particular model (in fact, without assuming we even know any such model).

For instance, it turns out that we can also express many convenient [[universal properties]] in terms of derivators. A striking example is the theory of [[triangulated category|triangulated categories]]: if $A$ is an [[abelian category]], its (bounded) [[derived category]] $D^b(A)$ is not defined by a universal property.  A natural statement would be that, given a triangulated category, the category of additive functors $A\to T$ which send [[short exact sequence]]s to distinguished triangles is equivalent to the category of triangulated functors $D^b(A)\to T$, but this statement is false, and in fact, does not even make sense (unless $A$ is [[semisimple category|semi-simple]]). But, in practice, everything behaves as if the above statement were meaningful and true. The 'reason' why this does not work is that the [[mapping cone|cone]] of a map in a triangulated category is not defined by a universal property. On the other hand, the cone of a morphism of complexes $X\to Y$ is canonically defined: this is the [[homotopy colimit]] of the diagram $0\leftarrow X \to Y$.  In the world of derivators, we can remedy this situation and recover a suitable universal property.


### As a motivation for $(\infty,1)$-categories

On the other hand, we may ask: Why do we take for granted that the [[homotopy theory]] of [[topological space|spaces]] provides a good notion (among others) of [[∞-groupoid]]?  And why should we expect everything to be [[enriched category|enriched]] in higher groupoids anyway?  A priori this may seem arbitrary (although it certainly works very well).  Instead we might ask: what is the mathematical structure over which everything is canonically enriched?  How can we even correctly formulate such a question?

The notion of *derivator* provides a way to correctly formulate such a question, and the answer turns out to be mostly what we expect.  Every type of "category theory" (at least, category theory without an *a priori* given [[enriched category|enrichment]]) that we might want to do is automatically and uniquely enriched in [[homotopy types]], i.e. in the homotopy category of [[CW-complexes]] or [[Kan complexes]].  (For ordinary 1-category theory, this enrichment is trivial, i.e. factors through sets considered as discrete homotopy types.)  A derivator is simply a structure with the characteristics of ordinary [[category theory]]: [[category|categories]], [[functor]]s, [[natural transformation]]s, [[Kan extension]]s, [[Grothendieck fibration]]s.  We can then show that any derivator acquires such an enrichment, so that homotopy types are a canonical enriching place for "category theories."


## Definition

### Prederivators

Let [[Cat]] denote the [[2-category]] of [[large category|large]] [[categories]] (not necessarily even [[locally small category|locally small]]), and let $Dia$ be some 2-category of [[small categories]], thought of as **[[diagram]]s**.  One common choice is the 2-category of *all* small categories (which generates $Cat$), but we might also choose the 2-category of finite categories.  A **prederivator** with domain $Dia$ is a strict [[2-functor]]

$$ Dia^{op} \overset{D}{\to} Cat $$

As usual, $(-)^{op}$ denotes the 1-cell dual of a 2-category.  Thus, a prederivator is a "$Cat$-valued [[presheaf]]" on $Dia$.  Prederivators form a 2-category $PDer$ whose morphisms are [[pseudonatural transformations]] and whose 2-cells are [[modification]]s.

Another common convention is to use the double dual $Dia^{coop}$ which reverses both 1-cells and 2-cells, although confusingly sometimes in the literature this double dual is still denoted "$Dia^{op}$".  The motivation for the latter choice seems to be that then $D(A)$ is the category of "[[presheaves]] on $A$ with values in $D$" instead of the category of "[[diagrams]] of shape $A$ in $D$."  We have chosen the convention above since the main purpose of a derivator is a calculus of homotopy limits and colimits, and it is more usual to take limits and colimits of covariant functors.  However, since $Dia^{coop}$ is isomorphic to $Dia^{op}$ via the 2-functor $(-)^{op}$ (as long as $Dia$ is closed under opposite categories in $Cat$), there is really very little difference.

There are two main motivating examples.  Firstly, any category $C$ defines a "representable" prederivator by the assignation $A\mapsto Hom(A,C)$, sending $A\in Dia$ to the category of functors $A\to C$.  This defines an embedding of $Cat$ into $PDer$.

Secondly, if $C$ is any [[category with weak equivalences]], there is a prederivator $Ho(C)$ which sends $A\in Dia$ to the [[localization]]/[[homotopy category]] $Ho(C)(A)$ of $Hom(A,C)$ relative to the [[model structure on functors|objectwise weak equivalences]] (as we allowed categories in $Cat$ to have large [[hom-set]]s, these localization exist).  In general, this is a non-representable prederivator, although of course if the weak equivalences are just the [[isomorphism]]s, it reduces to the representable case.  Note that to construct it, we don't need anything besides ordinary [[2-category|(2-)]][[category theory]]. 

### Derivators

A **derivator** is a prederivator $D$ which satisfies a list of axioms.  These axioms are of two sorts.

The first set of axioms says that there exist well-behaved homotopy limits and colimits, and more generally [[homotopy Kan extension]]s.  Specifically, we require the following.

* **(Der3)** {#Der3} For any functor $u : X\to Y$ in $Dia$, the [[inverse image]] functor $u^*:D(Y)\to D(X)$ admits a [[left adjoint]] $u_!$ and a [[right adjoint]] $u_*$.  These can be understood as [[homotopy Kan extension]]s

  $$
    (u_! \dashv u^* \dashv u_*) 
    :
    D(X)
      \stackrel{
         \overset{u_!}{\to}
      }
      {
        \stackrel{
          \overset{u^*}{\leftarrow}
        }{
          \underset{u_*}{\to}
        }
      }
    D(Y)
  $$

* **(Der4)** For any [[comma square]]
  $$\array{A & \overset{g}{\to} & B \\
  ^f\downarrow &\swArrow& \downarrow^v\\
  C& \underset{u}{\to} & D}$$
  in $Dia$, the [[Beck-Chevalley transformation]]s
  $$ f_! g^* \to u^* v_! \quad \text{and} \quad v^* u_* \to g_* f^* $$
  are [[isomorphism]]s.  Intuitively, this says that the Kan extensions in question are *[pointwise](http://ncatlab.org/nlab/show/Kan+extension#Pointwise)*.  In the presence of the second set of axioms, it suffices to require this when $C$ is the [[terminal category]] (for the first case) and when $D$ is so (for the second).

The second set of axioms are "[[sheaf]]" conditions.  Of course, we cannot assert that $D$ is exactly a sheaf (in the appropriate [[stack|2-categorical sense]]), since the terminal category in $Dia$ is 2-categorically dense and so any sheaf on it is representable (and represented by $D(1)$), whereas we want to also allow non-representable derivators.  But we do need some sheaf-like properties in order to do [[category theory]].  All of the following axioms can be understood as asserting that for some [[cover|covering family]] $\{Y_i \to X\}$ in $Dia$, the canonical map $D(X) \to Desc(D,\{Y_i\})$ from $D(X)$ to the category of [[descent]] data for the covering, while not an [[equivalence of categories|equivalence]], has some weaker good properties.  They can also be understood as 2-categorical [[sketch]] conditions.

The standard axioms are:

* **(Der1)** $D\colon Dia^{coop} \to Cat$ takes [[coproduct]]s to products.  Sometimes we require this only for finite coproducts.  In particular, we have $D(\emptyset) = 1$.

* **(Der2)** For any $X\in Dia$, consider the family of functors $x\colon 1\to X$ determined by the objects of $X$.  Then the induced functor
  $$ D(X) \overset{(x^*)}{\to} \prod_x D(1)$$
  is [[conservative functor|conservative]] (though not generally faithful).  This in turn implies that the same is true for any jointly [[essentially surjective functor|essentially surjective]] family of functors.

* **(Der5)** For any $X\in Dia$, if $I$ denotes the [[interval category]], then the induced functor
  $$ D(X\times I) \to Hom(I,D(X)) $$
  is [[essentially surjective functor|essentially surjective]] and [[full functor|full]] (though again, it is not generally faithful).  Sometimes it is convenient to assume this property when $I$ is any (perhaps finite) [[free category]].

+--{: .query}
[[Mike Shulman]]: It's clear to me that these are desirable requirements, which are moreover satisfied by all derivators of the form $Ho(C)$, but I would really like a conceptual explanation for why these axioms are *sufficient*.
=--

It is easy to see that if $C$ has pointwise left and right Kan extensions along all functors in $Dia$, then its representable prederivator is a derivator.  Somewhat more difficult to prove is that if $C$ is a [[model category]] (or more generally, has well-behaved homotopy Kan extensions), then the prederivator $Ho(C)$ is also a derivator.  Thus the derivator encodes the notions of [[homotopy colimit]] and of [[homotopy limit]].  Note again that this way of seeing homotopy (co)limits does not use anything besides usual (2-)category theory.

### Semiderivators

It may sometimes be useful to consider prederivators which are like derivators, but which "do not have *all* limits and colimits."  Let us say that a **semiderivator** is a prederivator satisfying (Der1), (Der2), and (Der5).

If $D$ is a semiderivator, $x\in D(B)$ is a $B$-shaped diagram, and $v\colon B\to C$ is a functor in $Dia$, then a **pointwise left extension** of $x$ along $v$ is an object "$v_! x$" in $D(C)$, together with a morphism $x \to v^* v_! x$ which is [[initial object|initial]] in the [[comma category]] $(x / v^*)$ (this says that $v_! x$ is a "local" or "partial" value of the left adjoint $v_!$ at $x$, although the entire functor $v_!$ may not exist) which additionally satisfies the [local Beck-Chevalley condition](/nlab/show/Beck-Chevalley+condition#Local) for any comma square as above.  We have a dual notion of **pointwise right extension**. 

We say a semiderivator is **complete** (resp. **cocomplete**) if it admits all pointwise right (resp. left) extension.  Clearly a semiderivator is a derivator just when it is both complete and cocomplete.

### Historical remarks

* Grothendieck's definition of a *derivator* included only axioms (Der1), (Der2), (Der3), and (Der4).

* Heller's definition of a *homotopy theory* included axioms (Der1), (Der2), (Der3), a weaker form of (Der4), and (Der5) for finite free categories.  His *pointed homotopy theories* add the axiom of a [[pointed derivator]], and his *stable homotopy theories* include a weaker version of the axiom now used for a [[stable derivator]].

* Franke's definition of a *system of triangulated diagram categories* was irreducibly [[pointed derivator|pointed]], taking $Dia$ to consist of categories enriched over pointed sets.  (See [[pointed derivator]] for the relationship of this approach to that of adding a "pointedness" axiom to an unpointed notion of derivator.)  In this context, he assumed axioms analogous to (Der1), (Der2), (Der3), (Der4), and (Der5) for the interval category, plus the [[stable derivator|stability]] axiom.  He also observed that if $Dia$ consists entirely of posets, then (Der4) follows from the other axioms.

Axioms (Der1)--(Der4) are clearly the easiest to motivate and the most obviously necessary.  Axiom (Der5) is used in order to do things with morphisms in $D(*)$, by first lifting them to objects of $D(I)$.  In particular, it is necessary to conclude that a stable derivator gives a [[triangulated category]].


## Computing homotopy Kan extensions

We now describe an "omnibus" theorem which is the main thing enabling us to compute with [[homotopy Kan extension]]s in a derivator.

### $D$-equivalences

For any functor $u\colon I\to J$ in $Dia$, we say it is a $D$-**equivalence** if the induced transformation $(\pi_I)_! (\pi_I)^* \to (\pi_J)_!(\pi_J)^*$ is an isomorphism, where $\pi_I\colon I\to *$ is the projection to the [[terminal category]], and similarly for $\pi_J$.  This means that homotopy colimits of *constant* diagrams of shapes $I$ and $J$ are equivalent.  By the [[Yoneda lemma]], this is equivalent to saying that
$$ D(*)((\pi_J)_!(\pi_J)^* X , Y) \to D(*)((\pi_I)_!(\pi_I)^* X , Y)$$
is an isomorphism for all $X,Y\in D(*)$, and by adjunction this is equivalent to saying that
$$ D(J)((\pi_J)^* X , (\pi_J)^*Y) \to D(I)((\pi_I)^* X , (\pi_I)^*Y)$$
is an isomorphism---i.e. that $u^*$ is fully faithful when restricted to the image of $\pi_J^*$.  In particular, if $u^*$ is fully faithful, then $u$ is a $D$-equivalence.

In a representable derivator (i.e. in ordinary category theory), the colimit of a constant diagram of shape $I$ is a [[copower]] with the set of connected components of $I$.  Thus, in a representable derivator, any functor that induces an isomorphism on sets of connected components will be a $D$-equivalence, and the converse is true as long as the category in question is not a [[preorder]].

By contrast, in the derivator coming from a model category or $(\infty,1)$-category, the colimit of a constant diagram of shape $I$ is a copower with the [[nerve]] of $I$ regarded as an $\infty$-groupoid, so in this case any functor that induces a homotopy equivalence of nerves (a stronger condition) will be a $D$-equivalence.  In fact, one can show:

+-- {: .num_theorem #NerveEquiv}
###### Theorem (Cisinski)
In any derivator $D$, any functor which induces a homotopy equivalence of nerves is a $D$-equivalence.
=--

This theorem follows from Cisinski's theorem that the nerve equivalences are the smallest [[basic localizer]], once we verify that the $D$-equivalences are in fact a basic localizer.

+-- {: .un_lemma}
###### Lemma
Any functor in $Dia$ with a fully faithful left or right adjoint is a $D$-equivalence.
=--
+-- {: .proof}
###### Proof
If $f\dashv g$ in $Dia$, then $g^* \dashv f^*$, and if $f$ is fully faithful, then the unit $1 \to g f$ is an isomorphism, and thus so is the unit $1\to f^* g^*$.  Hence $g^*$ is also fully faithful and so $g$ is a $D$-equivalence.  The other case is dual.
=--

+-- {: .un_lemma}
###### Lemma
Let $W_D$ denote the class of $D$-equivalences in $Dia$.  Then $W_D$ is saturated, in the sense that if $u\colon I\to J$ is a morphism in $Dia$ which becomes an isomorphism in $Dia[W_D^{-1}]$, then $u$ is a $D$-equivalence.
=--
+-- {: .proof}
###### Proof
Fix some $X,Y\in D(*)$ and consider the functor $\Phi\colon Dia \to Set^{op}$ which sends $I$ to $D(I)(\pi_I^*X, \pi_I^*Y)$.  Since $\Phi$ inverts $D$-equivalences, it factors through $Dia[W_D^{-1}]$.  But if $u$ becomes an isomorphism in $Dia[W_D^{-1}]$, then it must be inverted by $\Phi$, but that is the definition of being a $D$-equivalence (as $X$ and $Y$ vary).
=--

+-- {: .un_lemma}
###### Lemma
For any $D$, the class of $D$-equivalences is a [[basic localizer]].
=--
+-- {: .proof}
###### Proof
Saturation gives 2-out-of-3 property and closure under retracts.  If $A$ has a terminal object, then $A\to 1$ has a fully faithful right adjoint and hence is a $D$-equivalence.  Finally, given a triangle
$$\array{ A & & \overset{u}{\to} & & B\\ & _v \searrow & & \swarrow_w \\ & & C, } $$
to show that $u$ is a $D$-equivalence, it suffices to show that the transformation $v_! \pi_A^* \to w_! \pi_B^*$ is an isomorphism.  By (Der2) it suffices to check this for any $c\in C$.  We can then form the comma objects
$$\array{v/c & \overset{g}{\to} & A\\
  ^f\downarrow && \downarrow^v\\
  *& \underset{}{\to} & C} \quad\text{and}\quad
\array{w/c & \overset{k}{\to} & B\\
  ^h\downarrow && \downarrow^w\\
  * & \underset{}{\to} & C}$$
and the transformation $c^* v_! \pi_A^* \to c^* w_! \pi_B^*$ factors as
$$ c^* v_! \pi_A^* \cong f_! g^* \pi_A^* \cong f_! \pi_{v/c}^* \to h_! \pi_{w/c}^* \cong c^* w_! \pi_B^*$$
using the analogous map for the functor $v/c \to w/c$.  Therefore, if $v/c \to w/c$ is a $D$-equivalence, this composite is an isomorphism, and if this holds for all $c$, then by (Der2), $u$ is a $D$-equivalence.
=--

Therefore, since the nerve equivalences are the smallest basic localizer, every nerve equivalence is a $D$-equivalence for any derivator $D$.

### Exact squares {#ExactSquares}

Now suppose given any square
$$\array{L & \overset{p}{\to} & I\\
  ^q\downarrow & \Downarrow^\mu & \downarrow^u\\
  J & \underset{v}{\to} & K}$$
in $Dia$ which commutes up to a specified 2-cell $\mu$.  Given a derivator $D$, we say that this square is $D$-**exact** if the [[Beck-Chevalley transformation]]s
$$ q_! p^* \to v^* u_! \quad \text{and} \quad u^* v_* \to p_* q^* $$
are isomorphisms.  (In fact, if one of these is an isomorphism, so is the other, since they are [[mate|mates]].)  Thus, the derivator axioms say that all comma squares are exact.

Like the notion of [[exact square]] in ordinary category theory, this is a "functional" definition, but we can also give a more explicit characterization, using more or less the same argument.  Given such a square as above and $i\in I$, $j\in J$, we write $(i/L/j)$ for the category whose objects are triples
$$\big(\ell\in L,\, i\overset{\alpha}{\to} p(\ell),\, q(\ell)\overset{\beta}{\to} j\big).$$
The morphisms of $(i/L/j)$ are morphisms $\gamma\colon \ell \to \ell'$ in $L$ which make the evident triangles commute.  Now there is a functor $r\colon (i/L/j) \to K(u(i),v(j))$ (the latter considered as a discrete category), which sends the above triple to the composite
\[ u(i) \overset{u(\alpha)}{\to} u(p(\ell)) \overset{\mu}{\to} v(q(\ell)) \overset{v(\beta)}{\to} v(j) \label{commacomp}\]
in $K$.

+-- {: .un_theorem}
###### Theorem
A square as above is $D$-exact if and only if for all $i\in I$ and $j\in J$, the functor $(i/L/j) \to K(u(i),v(j))$ is a $D$-equivalence.
=--
+-- {: .proof}
###### Proof
It is easy to verify that the horizontal or vertical pasting composite of exact squares is exact; hence if the given square is exact, then so is the composite
$$\array{(L/j) & \overset{}{\to} & L & \overset{p}{\to} & I \\
  \downarrow & \Downarrow & \downarrow^q & \Downarrow & \downarrow^u\\
  * & \underset{j}{\to} & J & \underset{v}{\to} & K}$$
for any $j\in J$, where the left-hand square is a comma square.  Conversely, if all of these squares are exact, then so is the given one, by (Der2).  We play the same game by composing with comma squares on the top to conclude that the given square is exact if and only if all the induced squares
\[\array{(i/L/j) & \overset{f}{\to} & *\\
  ^g\downarrow & \Downarrow & \downarrow^{\mathrlap{u(i)}}\\
  * & \underset{v(j)}{\to} & K}\label{ijsquare}\]
are exact.  But the square
$$\array{K(u(i),v(j)) & \overset{s}{\to} & *\\
  ^t\downarrow & \Downarrow & \downarrow^{\mathrlap{u(i)}}\\
  * & \underset{v(j)}{\to} & K}$$
is exact, since it is a comma square, and by the universal property of a comma square, the square \eqref{ijsquare} factors uniquely through this one by a functor $r\colon (i/L/j) \to K(u(i),v(j))$, which is precisely the functor $r$ defined above.  Specifically, we have $f = s r$ and $g = t r$.  Therefore, the Beck-Chevalley transformation $g_! f^* \to (v j)^* (u i)^*$ is equal to the composite
$$ g_! f^* = t_! r_! r^* s^* \to t_! s^* \to (v j)^* (u i)^* $$
where the second map is the Beck-Chevalley transformation for the comma square, which is an isomorphism.  Thus, \eqref{ijsquare} is exact just when $t_! r_! r^* s^* \to t_! s^*$ is an isomorphism.  But this says exactly that $r$ is a $D$-equivalence.
=--

A square is said to be [[homotopy exact square|homotopy exact]] if it is $D$-exact for all derivators $D$ (or, equivalently, for all $(\infty,1)$-categories, or for all model categories, or simplicially enriched categories).

+-- {: .un_cor}
###### Corollary
A square is homotopy exact if and only if for all $i\in I$ and $j\in J$, the functor $(i/L/j) \to K(u(i),v(j))$ induces a weak homotopy equivalence of nerves.
=--
+-- {: .proof}
###### Proof
"If" follows directly from Theorem \ref{NerveEquiv} and the previous theorem.  Conversely, we can take $D$ to be the derivator of spaces ($\infty$-groupoids), where the $D$-equivalences are precisely the nerve equivalences.
=--

+-- {: .un_cor}
###### Corollary
For each $i\in I$, $j\in J$, and $\varphi\colon u(i) \to v(j)$ in $K$, let $(i/L/j)_\varphi$ denote the subcategory of $(i/L/j)$ consisting of those triples for which the composite \eqref{commacomp} is equal to $\varphi$.  Then the square is homotopy exact if and only if each category $(i/L/j)_\varphi$ has a contractible nerve.
=--

This gives a convenient way to compute many homotopy limits and colimits, which works in any derivator, and *a fortiori* in any $(\infty,1)$-category or model category.  Example applications can be found at [[homotopy exact square]].


## The 2-category of derivators

We can consider now the 2-category of derivators.  Actually, there are several different ways to define such a 2-category, depending on whether we require morphisms to preserve homotopy colimits, limits, both, or neither.  Let us write $Der_!$ for the 2-category whose morphisms preserve colimits.  Thus:

* its [[object]]s are derivators,

* its 1-[[morphism]]s are [[pseudonatural transformations]] $F:D\to D'$ which commute with the functors $u_!$ (i.e. the canonical comparison maps for these are isomorphisms),

* its 2-cells are the [[modifications]] between these.

We write $Hom_!(D,D') = Der_!(D,D')$ for hom-categories in this 2-category.

### Free cocompletions

Now, given a small category $X$, there is a $2$-functor, defined by evaluating at $X$
$$Der_!\to Cat \quad , \qquad D\mapsto D(X).$$
Note that, for any (pre)derivator $D$, the category $D(X)$ is canonically equivalent to the category $Hom(X,D)$ of morphisms of *prederivators* from $X$ to $D$ (considering $X$ as a representable prederivator).  Of course, $X$ will usually not itself be a derivator, but nevertheless this $2$-functor is *representable* in the 2-category $Der_!$.

Thus, there exists a derivator $\widehat{X}$, endowed with a morphism of prederivators $h:X\to \widehat{X}$ (called the Yoneda embedding), such that, for any derivator $D$, composing with h defines an equivalence of categories
$$Hom_!(\widehat{X},D)\simeq Hom(X,D)=D(X).$$
In other words, the map $h:X\to \widehat{X}$ is the "free completion of $X$ by homotopy colimits" in the sense of derivators.

Furthermore, $\widehat{X}$ can be described rather explicitly: it is the derivator associated to the [[model structure on simplicial presheaves|model category of simplicial presheaves]] on $X$.  In particular, the usual [[model structure on simplicial sets|homotopy theory of simplicial sets]] gives rise to the derivator $\widehat{*}$, where $*$ stands for the [[terminal object|terminal]] category.  Note that in order to conclude this, we didn't take for granted that [[homotopy type]]s should be important: its universal property is formulated purely with ordinary category theory.

From there, you can see that any derivator is canonically enriched in the derivator $\widehat{*}\simeq Ho(SSet)$: as $*$ acts uniquely on any prederivator, $\widehat{*}\simeq Ho(SSet)$ acts uniquely on any derivator (as far as we ask compatibility with homotopy colimits).  Thus the [[homotopy hypothesis]] might be reformulated vaguely as: is there an algebraic model of $\widehat{*}$?  Then one may guess that some notion of higher groupoid might do the job.

## Constructions of derivators

Viewing a derivator as a partway point between an $(\infty,1)$-category and its homotopy category, and recalling that $(\infty,1)$-categories are often presented by [[categories with weak equivalences]] and in particular [[model categories]], we can construct derivators in two general ways.

### From homotopy theory

If $(C,W)$ is a [[category with weak equivalences]], then the representable prederivator defined by $D_C(X) = Cat(X,C) = C^X$ comes equipped with weak equivalences $W^X$ on each category $C^X$.  We define the *homotopy prederivator* $Ho(C)$ by inverting these weak equivalences in each diagram category:
$$Ho(C)(X) = Ho(C^X,W^X) = C^X[(W^X)^{-1}]$$

+--{: .un_theorem}
###### Theorem (Cisinski)
If $C$ is a [[model category]], then $Ho(C)$ is a derivator.
=--

Axioms (Der1), (Der2), and (Der5) are easy to check.  Axiom (Der3) is also easy, since [[homotopy limits]] and colimits in categories with weak equivalences are [[derived functor]]s of the usual limits and colimits, and so they supply left and right adjoints to derived pullback functors.  (This shows moreover that homotopy limits and Kan extensions in a model category coincide with the notions of homotopy limit and Kan extension in its homotopy derivator, so that by working in $Ho(C)$ we really are studying the things we want to study.)  Axiom (Der4) requires a bit of work; there is a proof for combinatorial model categories using the [[injective model structure]] in [(Groth)](#Groth).


### From $(\infty,1)$-categories

If $C$ is an $(\infty,1)$-category, it has a homotopy category $Ho(C)$ obtained by identifying equivalent 1-morphisms.  If our $(\infty,1)$-categories are modeled by [[quasicategories]], then $Ho(-)$ is the [[left adjoint]] of the [[nerve]], often denoted $\tau_1$.

Now since categories are in particular $(\infty,1)$-categories, for any category $X$ we have a [[functor (∞,1)-category]] $C^X$, and thus a homotopy category $Ho(C^X)$.  We define the *homotopy prederivator* of $C$ by
$$Ho(C)(X) = Ho(C^X).$$
If $C$ has [[limit in an (∞,1)-category|limits]] and colimits in the $(\infty,1)$-categorical sense, then $Ho(C)$ should be a derivator.


## Related pages

Special kinds of derivators:

* [[pointed derivator]]
* [[stable derivator]]
* [[monoidal derivator]]
* [[enriched derivator]]
* [[finitely complete prederivator]]
* [[regular derivator]]

The calculus of homotopy Kan extensions used in derivators:

* [[homotopy exact square]]

Special limits and structures in derivators:

* [[pullback in a derivator]]
* [[monomorphism in a derivator]]

## References

The name of derivator is originally due to [[Grothendieck]] in [[Pursuing Stacks]]. 
The first fifteen chapters of a 2000 page manuscript of Grothendieck (in French) about derivators can be found at:

* [[Alexander Grothendieck]],  _[Les D&#233;rivateurs](http://people.math.jussieu.fr/~maltsin/groth/Derivateurs.html)_

Independently, there is a version due to Heller (who called them "homotopy theories"):

* Alex Heller, _Homotopy theories_ , Memoirs of the American Mathematical Society, Vol. 71, No 383 (1988).
* Alex Heller, _Stable homotopy theories and stabilization_ , [MR](http://www.ams.org/mathscinet-getitem?mr=1431157) -- see [[pointed derivator]] and [[stable derivator]]

Apparently also independent is the development by Franke, who takes an enriched approach to the pointed case and also assumes stability:

* Jens Franke, _Uniqueness theorems for certain triangulated categories with an Adams spectral sequence_, [K-theory archive](http://www.math.uiuc.edu/K-theory/0139/)

Georges Maltsiniotis has written an introduction to the topic (in French):

* [[Georges Maltsiniotis]], _Introduction &#224; la th&#233;orie des d&#233;rivateurs, d'apr&#232;s Grothendieck_ , Preprint (2001) [ps](http://www.math.jussieu.fr/~maltsin/ps/m.ps)

He also gave a [course](http://congreso.us.es/htag09/php/index.php?carga=courses) (in English) in Seville, Sep 2010, and part 3 is on derivators:

* [[Georges Maltsiniotis]]

  * [Lecture I (Localizers)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_I_Localizers.pdf)

    [Lecture II (Model Categories)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_II_Model_Categories.pdf)

    [Lecture III (Derivators)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf)

    [Summary on Derivators](http://people.math.jussieu.fr/~maltsin/Seville/Summary_on_Derivators.pdf)

Part of the above material is adapted from

* [[Denis-Charles Cisinski]], _[blog comment on derivators](http://golem.ph.utexas.edu/category/2010/03/a_perspective_on_higher_catego.html#c032227)_

Cisinski has also written a number of papers on the subject (in French), which can be found at [his homepage](http://www-math.univ-paris13.fr/~cisinski/publications.html).

Derivators were also recently used by [[Gonçalo Tabuada]] in a universal characterization of higher [[algebraic K-theory]]:

* [[Gonçalo Tabuada]], "Higher K-theory via universal invariants" [arXiv](http://arxiv.org/abs/0706.2420).

An introduction to some of the theory of pointed and stable derivators, in English, can be found in the paper:

* [[Denis-Charles Cisinski]] and [[Amnon Neeman]], _Additivity for derivator K-theory_ , [MR](http://www.ams.org/mathscinet-getitem?mr=2382732)

An brief informal discussion of derivators as a 2-categorical tool for studying $(\infty,1)$-categories is contained in

* [[Mike Shulman]], _Squeezing Higher Categories out of Lower Categories_ ([blog](http://golem.ph.utexas.edu/category/2010/05/squeezing_higher_categories_ou.html))

In the paper

* Olivier Renaudin, _Theories homotopiques de Quillen combinatoires et derivateurs de Grothendieck_, [arxiv](http://arxiv.org/abs/math/0603339)

it is proven that the 2-category of "[[locally presentable category|locally presentable]]" derivators is equivalent to the [[localization]] of the 2-category of [[combinatorial model categories]] at the [[Quillen equivalences]].  Thus in some sense derivators capture "all the information" about a combinatorial model category, hence also about a [[locally presentable (∞,1)-category]].

An introductory discussion aimed towards [[stable derivator]]s is also in

* [[Moritz Groth]], _Derivators, pointed derivators, and stable derivators_ ([pdf](http://www.math.uni-bonn.de/~mgroth/groth_derivators.pdf))
{#Groth}


[[!redirects derivators]]
[[!redirects prederivator]]
[[!redirects prederivators]]
[[!redirects derivateur]]
[[!redirects dérivateur]]
[[!redirects derivateurs]]
[[!redirects dérivateurs]]
[[!redirects semiderivator]]
[[!redirects semiderivators]]
