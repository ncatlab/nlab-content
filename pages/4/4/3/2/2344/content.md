
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **derivator** is a refinement of a [[homotopy category]] which also includes information about [[homotopy limits]] and colimits.  In some cases derivators can be used where one might otherwise need to use [[(∞,1)-categories]], which can be helpful since their theory is much simpler and purely (2-)categorical.  They were invented by [[Grothendieck]] and Heller.

## Motivation

The notion of derivator can be motivated in several ways.

### As a halfway house

Suppose we start from the perspective that what we really study in [[homotopy theory]] are [[(∞,1)-categories]].  The [[homotopy category of an (∞,1)-category]] (the 1-category obtained by setting all equivalent 1-morphisms equal) is a fairly coarse invariant, but for some purposes it is sufficient.  On the other hand, sometimes we need more than merely the homotopy category, but doing everything with $(\infty,1)$-categories can be technically daunting.  Frequently, all we need from an $(\infty,1)$-category that is not present in its homotopy category is to know that we have well-behaved constructions of [[homotopy limit]]s and [[homotopy colimit]]s.

A *derivator* is thus a halfway-house, containing more information than a homotopy category, but easier to work with than an $(\infty,1)$-category.  It consists of a homotopy category together with extra structure that enables one to compute with homotopy limits and colimits.  Any $(\infty,1)$-category with sufficiently many limits and colimits has an underlying derivator, and working with these derivators suffices for a surprising number of things we may want to do with $(\infty,1)$-categories.  However, derivators are an essentially 1-categorical notion, so we can study them using ordinary [[2-category]] theory.  Thus derivators provide a "truncated" version of [[higher category theory]], which gives us the language to characterize higher category theory using only usual [[category theory]], without any emphasis on any particular model (in fact, without assuming we even know any such model).

For instance, it turns out that we can also express many convenient [[universal properties]] in terms of derivators. A striking example is the theory of [[triangulated category|triangulated categories]]: if $A$ is an [[abelian category]], its (bounded) [[derived category]] $D^b(A)$ is not defined by a universal property.  A natural statement would be that, given a triangulated category, the category of additive functors $A\to T$ which send [[short exact sequence]]s to distinguished triangles is equivalent to the category of triangulated functors $D^b(A)\to T$, but this statement is false, and in fact, does not even make sense (unless $A$ is [[semisimple category|semi-simple]]). But, in practice, everything behaves as if the above statement were meaningful and true. The 'reason' why this does not work is that the [[mapping cone|cone]] of a map in a triangulated category is not defined by a universal property. On the other hand, the cone of a morphism of complexes $X\to Y$ is canonically defined: this is the [[homotopy colimit]] of the diagram $0\leftarrow X \to Y$.  In the world of derivators, we can remedy this situation and recover a suitable universal property.


### As a motivation for $(\infty,1)$-categories

On the other hand, we may ask: Why do we take for granted that the [[homotopy theory]] of [[topological space|spaces]] provides a good notion (among others) of [[∞-groupoid]]?  And why should we expect everything to be [[enriched category|enriched]] in higher groupoids anyway?  A priori this may seem arbitrary (although it certainly works very well).  Instead we might ask: what is the mathematical structure over which everything is canonically enriched?  How can we even correctly formulate such a question?

The notion of *derivator* provides a way to correctly formulate such a question, and the answer turns out to be mostly what we expect.  Every type of "category theory" (at least, category theory without an *a priori* given [[enriched category|enrichment]]) that we might want to do is automatically and uniquely enriched in [[homotopy types]], i.e. in the homotopy category of [[CW-complexes]] or [[Kan complexes]].  (For ordinary 1-category theory, this enrichment is trivial, i.e. factors through sets considered as discrete homotopy types.)  A derivator is simply a structure with the characteristics of ordinary [[category theory]]: [[category|categories]], [[functor]]s, [[natural transformation]]s, [[Kan extension]]s, [[Grothendieck fibration]]s.  We can then show that any derivator acquires such an enrichment, so that homotopy types are a canonical enriching place for "category theories."


## Definition

### Prederivators

Let [[Cat]] denote the [[2-category]] of [[large category|large]] [[categories]] (not necessarily even [[locally small category|locally small]]), and let $Dia$ be some 2-category of [[small categories]], thought of as **[[diagram]]s**.  One common choice is the 2-category of *all* small categories (which generates $Cat$), but we might also choose the 2-category of finite categories.  A **prederivator** with domain $Dia$ is a strict [[2-functor]]

$$ Dia^{coop} \to Cat $$

As usual, $(-)^{coop}$ denotes the double dual of a 2-category, which reverses both 1-cells and 2-cells.  Thus, a prederivator is a "$Cat$-valued [[presheaf]]" on $Dia$.  Prederivators form a 2-category $PDer$ whose morphisms are [[pseudonatural transformations]] and whose 2-cells are [[modification]]s.

+--{: .query}
[[Mike Shulman]]: Is it universal to use $Dia^{coop}$ here?  It seems *much* more natural to me to use $Dia^{op}$, since we usually take limits and colimits of covariant functors, not contravariant ones.
=--

There are two main motivating examples.  Firstly, any category $C$ defines a "representable" prederivator by the assignation $X\mapsto Hom(X^{op},C)$, sending $X\in Dia$ to the category of functors $X^{op}\to C$.  This defines an embedding of $Cat$ into $PDer$.

Secondly, if $C$ is any [[category with weak equivalences]], there is a prederivator $Ho(C)$ which sends $X\in Dia$ to the [[localization]]/[[homotopy category]] $Ho(C)(X)$ of $Hom(X^{op},C)$ relative to the [[model structure on functors|objectwise weak equivalences]] (as we allowed categories in $Cat$ to have large [[hom-set]]s, these localization exist).  In general, this is a non-representable prederivator, although of course if the weak equivalences are just the [[isomorphism]]s, it reduces to the representable case.  Note that to construct it, we don't need anything besides ordinary [[2-category|(2-)]][[category theory]]. 

### Derivators

A **derivator** is a prederivator $D$ which satisfies a list of axioms.  These axioms are of two sorts.

The first set of axioms says that there exist well-behaved homotopy limits and colimits, and more generally [[homotopy Kan extension]]s.  Specifically, we require the following.

* **(Der3)** For any functor $u : X\to Y$ in $Dia$, the [[inverse image]] functor $u^*:D(Y)\to D(X)$ admits a [[left adjoint]] $u_!$ and a [[right adjoint]] $u_*$.  These can be understood as [[homotopy Kan extension]]s

  $$
    (u_! \dashv u^* \dashv u_*) 
    :
    D(Y)
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
    D(X)
  $$

* **(Der4)** For any [[comma square]]
  $$\array{A & \overset{g}{\to} & B \\
  ^f\downarrow &\Downarrow& \downarrow^v\\
  C& \underset{u}{\to} & D}$$
  in $Dia$, the Beck-Chevalley transformations
  $$ f_! g^* \to u^* v_! \quad \text{and} \quad v^* u_* \to g_* f^* $$
  are isomorphisms.  Intuitively, this says that the Kan extensions in question are *pointwise*.  In the presence of the second set of axioms, it suffices to require this when $C$ is the [[terminal category]] (for the first case) and when $D$ is so (for the second).

The second set of axioms are "[[sheaf]]" conditions.  Of course, we cannot assert that $D$ is exactly a sheaf (in the appropriate [[stack|2-categorical sense]]), since the terminal category in $Dia$ is dense and so any sheaf on it is representable (and represented by $D(1)$), whereas we want to also allow non-representable derivators.  But we do need some sheaf-like properties in order to do category theory.  All of the following axioms can be understood as asserting that for some [[cover|covering family]] $\{Y_i \to X\}$ in $Dia$, the canonical map $D(X) \to Desc(D,\{Y_i\})$ from $D(X)$ to the category of [[descent]] data for the covering, while not an [[equivalence of categories|equivalence]], has some weaker good properties.

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


## Computing homotopy Kan extensions

We now describe an "omnibus" theorem which is the main thing enabling us to compute with homotopy Kan extensions in a derivator.

### $D$-equivalences

For any functor $u\colon I\to J$ in $Dia$, we say it is a $D$-**equivalence** if the induced transformation $(\pi_I)_! (\pi_I)^* \to (\pi_J)_!(\pi_J)^*$ is an isomorphism, where $\pi_I\colon I\to *$ is the projection to the [[terminal category]], and similarly for $\pi_J$.  This means that homotopy colimits of *constant* diagrams of shapes $I$ and $J$ are equivalent.  By the [[Yoneda lemma]], this is equivalent to saying that
$$ D(*)((\pi_J)_!(\pi_J)^* X , Y) \to D(*)((\pi_I)_!(\pi_I)^* X , Y)$$
is an isomorphism for all $X,Y\in D(*)$, and by adjunction this is equivalent to saying that
$$ D(*)((\pi_J)^* X , (\pi_J)^*Y) \to D(*)((\pi_I)^* X , (\pi_I)^*Y)$$
is an isomorphism---i.e. that $u^*$ is fully faithful when restricted to the image of $\pi_J^*$.  In particular, if $u^*$ is fully faithful, then $u$ is a $D$-equivalence.

In a representable derivator (i.e. in ordinary category theory), the colimit of a constant diagram of shape $I$ is a [[copower]] with the set of connected components of $I$.  Thus, in a representable derivator, any functor that induces an isomorphism on sets of connected components will be a $D$-equivalence, and the converse is true as long as the category in question is not a [[preorder]].

By contrast, in the derivator coming from a model category or $(\infty,1)$-category, the colimit of a constant diagram of shape $I$ is a copower with the [[nerve]] of $I$ regarded as an $\infty$-groupoid, so in this case any functor that induces a homotopy equivalence of nerves (a stronger condition) will be a $D$-equivalence.  In fact, one can show:

+-- {: .num_theorem #NerveEquiv}
###### Theorem (Cisinski)
In any derivator $D$, any functor which induces a homotopy equivalence of nerves is a $D$-equivalence.
=--

As a first step towards this theorem, we can show that if $u\colon I\to J$ is a "homotopy equivalence" in $Dia$, i.e. there exists a functor $v\colon J\to I$ and zigzags of natural transformations relating $u v$ and $v u$ to identities, then $u$ is a $D$-equivalence.  We first observe:

+-- {: .un_lemma}
###### Lemma
Any functor in $Dia$ with a fully faithful left or right adjoint is a $D$-equivalence.
=--
+-- {: .proof}
###### Proof
If $f\dashv g$ in $Dia$, then $g^* \dashv f^*$, and if $f$ is fully faithful, then the unit $1 \to g f$ is an isomorphism, and thus so is the unit $1\to f^* g^*$.  Hence $g^*$ is also fully faithful and so $g$ is a $D$-equivalence.  The other case is dual.
=--

It follows that if $I$ has an initial or terminal object, then the projection $I\times J\to J$ is a $D$-equivalence.  In particular, this is the case when $I$ is the [[interval category]].  We now need to know:

+-- {: .un_lemma}
###### Lemma
Let $W_D$ denote the class of $D$-equivalences in $Dia$.  Then $W_D$ is saturated, in the sense that if $u\colon I\to J$ is a morphism in $Dia$ which becomes an isomorphism in $Dia[W_D^{-1}]$, then $u$ is a $D$-equivalence.
=--
+-- {: .proof}
###### Proof
Fix some $X,Y\in D(*)$ and consider the functor $\Phi\colon Dia \to Set^{op}$ which sends $I$ to $D(I)(\pi_I^*X, \pi_I^*Y)$.  Since $\Phi$ inverts $D$-equivalences, it factors through $Dia[W_D^{-1}]$.  But if $u$ becomes an isomorphism in $Dia[W_D^{-1}]$, then it must be inverted by $\Phi$, but that is the definition of being a $D$-equivalence (as $X$ and $Y$ vary).
=--

In particular, $D$-equivalences satisfy the 2-out-of-3 property.  Therefore, if $I$ is again the interval category, then the two inclusions $J\rightrightarrows I\times J$ are both $D$-equivalences.  Since the interval category is an [[interval object]] that describes natural transformations, it follows that if there is a natural transformation $f\to g$ in $Dia$, then $f$ is a $D$-equivalence if and only if $g$ is.

Of course this then extends to arbitrary zigzags of natural transformations by induction.  Finally, if $f:I \rightleftarrows J:g$ is a homotopy equivalence, so that $f g$ and $g f$ are connected to identities by natural zigzags, then we can conclude that $f g$ and $g f$ are $D$-equivalences, and thus since $D$-equivalences also satisfy the 2-out-of-6 property, both $f$ and $g$ must be $D$-equivalences.

Note, though, that there exist functors inducing an equivalence of nerves which are not homotopy equivalences in this sense.  For instance, the category $\mathbb{N}$ has a contractible nerve, but is not homotopy equivalent to $*$.  So we haven't fully proven Cisinski's theorem.


### Exact squares

Now suppose given any square
$$\array{L & \overset{p}{\to} & I\\
  ^q\downarrow & \Downarrow^\mu & \downarrow^u\\
  J & \underset{v}{\to} & K}$$
in $Dia$ which commutes up to a specified 2-cell $\mu$.  Given a derivator $D$, we say that this square is $D$-**exact** if the Beck-Chevalley transformations
$$ q_! p^* \to v^* u_! \quad \text{and} \quad u^* v_* \to p_* q^* $$
are isomorphisms.  (In fact, if one of these is an isomorphism, so is the other, since they are [[mate|mates]].)  Thus, the derivator axioms say that all comma squares are exact.

Now, given such a square as above and $i\in I$, $j\in J$, we write $(i/L/j)$ for the category whose objects are triples
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
  ^g\downarrow & \Downarrow & \downarrow^{u(i)}\\
  * & \underset{v(j)}{\to} & K}\label{ijsquare}\]
are exact.  But the square
$$\array{K(u(i),v(j)) & \overset{s}{\to} & *\\
  ^t\downarrow & \Downarrow & \downarrow^{u(i)}\\
  * & \underset{v(j)}{\to} & K}$$
is exact, since it is a comma square, and by the universal property of a comma square, the square \eqref{ijsquare} factors uniquely through this one by a functor $r\colon (i/L/j) \to K(u(i),v(j))$, which is precisely the functor $r$ defined above.  Specifically, we have $f = s r$ and $g = t r$.  Therefore, the Beck-Chevalley transformation $g_! f^* \to (v j)^* (u i)^*$ is equal to the composite
$$ g_! f^* = t_! r_! r^* s^* \to t_! s^* \to (v j)^* (u i)^* $$
where the second map is the Beck-Chevalley transformation for the comma square, which is an isomorphism.  Thus, \eqref{ijsquare} is exact just when $t_! r_! r^* s^* \to t_! s^*$ is an isomorphism.  But this says exactly that $r$ is a $D$-equivalence.
=--

+-- {: .un_cor}
###### Corollary
For each $i\in I$, $j\in J$, and $\varphi\colon u(i) \to v(j)$ in $K$, let $(i/L/j)_\varphi$ denote the subcategory of $(i/L/j)$ consisting of those triples for which the composite \eqref{commacomp} is equal to $\varphi$.  If each category $(i/L/j)_\varphi$ has a contractible nerve, then the square is $D$-exact.
=--
+-- {: .proof}
###### Proof
This follows from Theorem \ref{NerveEquiv}, together with the observation that assuming axiom (Der1), a coproduct of $D$-equivalences must be a $D$-equivalence.
=--

The corollary gives a convenient way to compute many homotopy limits and colimits, which works in any derivator, and *a fortiori* in any $(\infty,1)$-category or model category.


## The 2-category of derivators

We can consider now the 2-category of derivators.  Actually, there are several different ways to define such a 2-category, depending on whether we require morphisms to preserve homotopy colimits, limits, both, or neither.  Let us write $Der_!$ for the 2-category whose morphisms preserve colimits.  Thus:

* its [[object]]s are derivators,

* its 1-[[morphism]]s are [[pseudonatural transformations]] $F:D\to D'$ which commute with the functors $u_!$ (i.e. the canonical comparison maps for these are isomorphisms),

* its 2-cells are the [[modifications]] between these.

We write $Hom_!(D,D') = Der_!(D,D')$ for hom-categories in this 2-category.

### Free cocompletions

Now, given a small category $X$, there is a $2$-functor, defined by evaluating at $X^{op}$
$$Der_!\to Cat \quad , \qquad D\mapsto D(X^{op}).$$
Note that, for any (pre)derivator $D$, the category $D(X^{op})$ is canonically equivalent to the category $Hom(X,D)$ of morphisms of *prederivators* from $X$ to $D$ (considering $X$ as a representable prederivator).  Of course, $X$ will usually not itself be a derivator, but nevertheless this $2$-functor is *representable* in the 2-category $Der_!$.

Thus, there exists a derivator $\widehat{X}$, endowed with a morphism of prederivators $h:X\to \widehat{X}$ (called the Yoneda embedding), such that, for any derivator $D$, composing with h defines an equivalence of categories
$$Hom_!(\widehat{X},D)\simeq Hom(X,D)=D(X^{op}).$$
In other words, the map $h:X\to \widehat{X}$ is the "free completion of $X$ by homotopy colimits" in the sense of derivators.

Furthermore, $\widehat{X}$ can be described rather explicitly: it is the derivator associated to the [[model structure on simplicial presheaves|model category of simplicial presheaves]] on $X$.  In particular, the usual [[model structure on simplicial sets|homotopy theory of simplicial sets]] gives rise to the derivator $\widehat{*}$, where $*$ stands for the [[terminal object|terminal]] category.  Note that in order to conclude this, we didn't take for granted that [[homotopy type]]s should be important: its universal property is formulated purely with ordinary category theory.

From there, you can see that any derivator is canonically enriched in the derivator $\widehat{*}\simeq Ho(SSet)$: as $*$ acts uniquely on any prederivator, $\widehat{*}\simeq Ho(SSet)$ acts uniquely on any derivator (as far as we ask compatibility with homotopy colimits).  Thus the [[homotopy hypothesis]] might be reformulated vaguely as: is there an algebraic model of $\widehat{*}$?  Then one may guess that some notion of higher groupoid might do the job.


## Related pages

* [[pointed derivator]]
* [[stable derivator]]
* [[monoidal derivator]]


## References

The notion of derivator is originally due to [[Grothendieck]] in [[Pursuing Stacks]]. 
The first thirteen chapters of a 2000 page manuscript of Grothendieck (in French) about derivators can be found at:

* [[Alexander Grothendieck]],  _[Les D&#233;rivateurs](http://people.math.jussieu.fr/~maltsin/groth/Derivateurs.html)_

Independently, there is a version due to Heller (who called them "homotopy theories"):

*  A. Heller, _Homotopy theories_ , Memoirs of the American Mathematical Society, Vol. 71, No 383 (1988).

Georges Maltsiniotis has written an introduction to the topic (in French):

* [[Georges Maltsiniotis]], "Introduction &#224; la th&#233;orie des d&#233;rivateurs, d'apr&#232;s Grothendieck", Preprint (2001) [ps](http://www.math.jussieu.fr/~maltsin/ps/m.ps)

He also gave a [course](http://congreso.us.es/htag09/php/index.php?carga=courses) (in English) in Seville, Sep 2010, and part 3 is on derivators:

* [Lecture I (Localizers)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_I_Localizers.pdf)

  [Lecture II (Model Categories)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_II_Model_Categories.pdf)

  [Lecture III (Derivators)](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf)

  [Summary on Derivators](http://people.math.jussieu.fr/~maltsin/Seville/Summary_on_Derivators.pdf)

Part of the above material is adapted from

* [[Denis-Charles Cisinski]], _[blog comment on derivators](http://golem.ph.utexas.edu/category/2010/03/a_perspective_on_higher_catego.html#c032227)_

Cisinski has also written a number of papers on the subject (in French), which can be found at [his homepage](http://www-math.univ-paris13.fr/~cisinski/publications.html).

Derivators were also recently used by [[Gonçalo Tabuada]] in a universal characterization of higher [[algebraic K-theory]]:

* Gon&#231;alo Tabuada, "Higher K-theory via universal invariants" [arXiv](http://arxiv.org/abs/0706.2420).

[[!redirects derivators]]
[[!redirects prederivator]]
[[!redirects prederivators]]
[[!redirects derivateur]]
[[!redirects dérivateur]]
[[!redirects derivateurs]]
[[!redirects dérivateurs]]
