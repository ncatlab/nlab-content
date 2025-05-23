
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

An ordinary [[category]] consists of a set of objects and a set of arrows, each with a single input or domain object and a single output or codomain object. Arrows are composed by plugging outputs into inputs, as when one composes unary operations. 

An ordinary [[multicategory]] consists of a set of objects and a set of "multi-arrows", each with a finite list of inputs or domain objects and a single output or codomain object. These multi-arrows are composed by means of multiple plug-ins or substitutions, as when one substitutes a list of $m$ operations of varying arities into an $m$-ary operation. 

Both categories and multicategories can be seen as [[monads]] in an appropriate [[bicategory]] of [[span]]-like objects. Categories are monads in the bicategory of ordinary spans (of sets).  Multicategories are monads in a bicategory of spans of shape

$$X \leftarrow R \to Y^*$$

where $Y^*$ is the set of finite lists of elements of $Y$.  In order to compose spans of this type, one uses the fact that $(-)^*$ has itself the structure of a monad on $Set$, namely the [[list monad]] or "free monoid" monad.  The idea of a *generalized multicategory* is to replace this monad by some more general monad $T$.

There are a lot of ways of making this precise, ranging in abstractness from the fairly concrete (cartesian monads on a cartesian category) to the most general and abstract (monads on a [[virtual equipment]]).  We will start from the former and gradually generalize to the latter.


## Definitions

### Cartesian monads

Let $V$ be a [[finitely complete category]], and let $T$ be a [[cartesian monad]] on $V$, i.e. a monad whose functor part $T$ preserves pullbacks, and for which the naturality squares of its unit and multiplication are pullbacks.  Then there is a [[bicategory]] $Span(V,T)$ of **$T$-spans** in $V$, whose objects $X$ are objects of $V$, whose morphisms $X \to Y$ are spans from $X$ to $T Y$, and whose 2-cells are morphisms of such spans. The identity $X \to X$ is the span 

$$X \overset{id}{\leftarrow} X \overset{\eta X}{\to} T X$$ 

where $\eta: 1_V \to T$ is the unit of $T$.  The composite of $T$-spans $R\colon X \to Y$, $S\colon Y \to Z$ is given by taking the following pullback:

$$\array{
& & & & R \circ S & & & &\\
& & & \swarrow & & \searrow & & & \\
& & R & & & & T S & &\\
& ^f \swarrow & & \searrow ^g & & ^{T h} \swarrow & & \searrow ^{T k} & \\
X & & & & T Y & & & & T T Z & \overset{\mu Z}{\rightarrow} & TZ}$$

A $T$**-multicategory** in $V$ is by definition a [[monad]] in the bicategory described above.  However, it is convenient to use the alternate word *monoid* rather than *monad* here, to avoid confusion with the monad $T$ which lives *on* $V$, and because the relevant morphisms of monoids (see below) are rather different from any of the usual sort of morphisms of monads.

If we spell out what this means more explicitly, a $T$-multicategory consists of an object $C_0$ of $V$, along with a span $C_0 \leftarrow C_1 \to T C_0$, and suitable identity-assigning and composition morphisms.

If $C_0$ is the [[terminal object]], then we speak instead of a $T$**-operad**.


#### Examples

* When $T$ is the "free monoid" monad on $Set$, a $T$-multicategory is precisely an ordinary multicategory.

* When $T$ is the identity monad on $V$, a $T$-multicategory is simply an [[internal category]] in $V$.

* When $T$ is the "free [[strict ∞-category]]" monad on [[globular sets]], a $T$-multicategory with $C_0 = 1$ is a [[globular operad]] in the sense of Batanin (this reformulation was found by Leinster).

* If $M$ is a monoid in $Set$ and $T = M\times -$ is the "free $M$-set" monad, then a $T$-multicategory is an "$M$-graded category."

* When $T$ is the [[free category]] monad on [[quivers]], a $T$-multicategory is a [[virtual double category]] (also called an *fc-multicategory*, coming from the name "fc" for this monad).

* If $A$ is a small category and $T$ is the monad on $Set^{ob(A)}$ whose algebras are functors $A\to Set$, then a $T$-multicategory can be identified with an object of $Cat/A$.


### Kleisli bicategories

Note that when $T$ is a cartesian monad on a finitely complete category $V$, then it extends to a (pseudo) [[2-monad]] on the bicategory $Span(V)$.  The functor part of this 2-monad is given simply by applying $T$; this is a (pseudo) [[2-functor]] since $T$ preserves pullbacks.  The unit of this 2-monad is given by the spans
$$ X \overset{id}{\leftarrow} X \overset{\eta X}{\to} T X$$
and its multiplication by
$$ T T X \overset{id}{\leftarrow} T T X \overset{\mu X}{\to} T X;$$
these are [[pseudonatural transformations]] since $\eta$ and $\mu$ are cartesian natural transformations.

Moreover, the bicategory $Span(V,T)$ defined above is easily seen to be precisely the [[Kleisli category|Kleisli bicategory]] of this extended 2-monad $T$ on $Span(V)$.  Thus, a more general notion of "generalized multicategory" would be a monad (monoid) in some Kleisli bicategory.

#### Examples

Are ordinary *symmetric* multicategories the $T$-multicategories relative to any monad $T$?  Recall that in a symmetric multicategory, the source of a morphism $f\colon (x_1,\dots,x_n) \to y$ is still an *ordered* list, but we have an action of the symmetric groups on the morphisms, in such a way that for $\sigma\in S_n$ we have $\sigma \cdot f \colon (x_{\sigma 1}, \dots, x_{\sigma n}) \to y$, and composition is equivariant for this action.

It doesn't work to let $T$ be the "free commutative monoid" monad, since that would destroy all ordering on the lists.  (Also, that monad is not cartesian.)  Really what we want is to let $T$ be the "free symmetric strict monoidal category" monad, since for a discrete set $A$ we have $T A = $ the set of finite ordered lists of elements of $A$, with isomorphisms imposed for all permutations.

However, of course this monad does not live on $Set$, but rather on $Cat$.  But there is a natural bicategory which extends $Cat$ analogously to how $Span$ extends $Set$, namely the bicategory $Prof$ of categories and [[profunctors]].  The "free symmetric strict monoidal category" monad $T$ does extend to a pseudomonad on $Prof$, and symmetric multicategories can be identified with monads $C_0 &#8696; T C_0$ in the Kleisli bicategory of this $T$ such that $C_0$ is a [[discrete category]].


### Double categories

While the bicategorical framework is very nice, it does not provide a good definition of the *functors* between generalized multicategories.  From the explicit point of view, a functor $f\colon C\to D$ between $T$-multicategories should consist of morphisms

$$
\array { C_0 & \leftarrow & C_1 & \to & T C_0 \\
  ^{f_0} \downarrow & & ^{f_1}\downarrow & & \downarrow^{T f_0}\\
  D_0 & \leftarrow & D_1 & \to & T D_0 }
$$

which respect the identity and structure maps.  This reduces to the natural notion of functor in all the examples mentioned above.  However, such morphisms cannot be identified with any of the usual notions of "morphisms of monads" in the bicategory $Span(V,T)$.  The closest thing there is would be a "colax morphism of monads," but that would allow $f_0$ to be an arbitrary *span* rather than a morphism in $V$.

We can remedy this problem if instead of the bicategory $Span(V,T)$, we consider a [[pseudo double category]] whose horizontal bicategory is $Span(V,T)$, and whose vertical arrows are the morphisms of $V$.  In particular, a square in this double category will be precisely a diagram of the above sort.  Thus, if we define a *monoid* in a double category to be the same as monad in its horizontal bicategory, we can also define a *monoid homomorphism* in a double category to consist of a vertical arrow and a square respecting the multiplication and identities, in such a way that monoid homomorphisms in $Span(V,T)$ are precisely the correct functors of $T$-multicategories mentioned above.

Thus, a better definition of $T$-multicategory is "a monoid in the double category $Span(V,T)$," since this definition recovers the correct morphisms immediately.  And a better generalized definition, which works for symmetric multicategories as well (using the double category of categories, functors, and profunctors), is "a monoid in a Kleisli double category."


### Equipments

When we try to make the notion of "Kleisli double category" precise, however, we run into some issues.  We want the "Kleisli-ness" to happen *horizontally*, i.e. in the span/profunctor direction.  However, in the examples, the monads in question live most naturally in in the 2-category of double categories, functors, and *vertical* natural transformations.  For example, when $T$ is a monad on $V$, its multiplication and unit transformations naturally induce vertical transformations $Id_{Span(V)} \to Span(T)$ and $Span(T)^2 \to Span(T)$, where $Span(T)$ denotes the induced functor on $Span(V)$.  Similarly, for the "free symmetric strict monoidal category" monad on the double category $Prof$, the unit and multiplication are naturally *functors*, i.e. vertical arrows, not profunctors.

However, in general, if all we know is that $T$ is a monad on a double category $X$ in the "vertical" sense, then there is no way to define a "horizontally Kleisli" double category of $T$.  The composite of horizontal arrows $A\to T B$ and $B \to T C$ in such a double category would have to be the composite $A\to T B \to T T C \overset{\mu}{\to} T C$, but in a double category there is no way to compose the horizontal arrow $A\to T T C$ with the vertical arrow $\mu\colon T T C \to T C$.  Specifically, the problem is that while any (pseudo) double functor between pseudo double categories induces a (pseudo) 2-functor between horizontal bicategories, a vertical transformation does not necessarily induce a pseudonatural one.

There are two solutions to this problem, and it turns out that the best approach is to use them both.  The first, and most obvious, is to generalize the way in which the monads in these two examples do, in fact, induce pseudomonads on the horizontal bicategory.  Namely, in both of the double categories $Span$ and $Prof$, every vertical arrow $f\colon A\to B$ gives rise to a horizontal arrow $B(1,f)\colon A\to B$ in a universal way.  This construction, along with its dual, makes $Span$ and $Prof$ into [[framed bicategories]], or equivalently [[proarrow equipments]].

Now in general, a vertical transformation between double categories that are proarrow equipments does not quite induce a *pseudo* natural transformation on horizonal bicategories, but only an *oplax* natural transformation.  However, in the examples we have considered so far, the oplax transformations are in fact pseudo, and so there is a horizontally-Kleisli double category (which is easily seen to be, itself, a proarrow equipment).


### Virtual double categories

From the double-category point of view, it seems unnatural to require that the unit and multiplication of the monad induce "horizontally pseudo" transformations; the vertical transformation of double categories is surely the more basic notion.  Moreover, it is also unnatural to require the functor $T$ to be pseudo; there are interesting examples where $T$ is only a (horizontally) *lax* functor.  Note that unlike the case for bicategories, there is a 2-category of double categories, lax functors, and vertical transformations, so we can talk about monads in such a 2-category.

However, at this level of generality, the horizontal Kleisli construction does not yield a double category.  It does, however, yield a [[virtual double category]].  Moreover, it also suffices to take as *input* a monad $T$ on a virtual double category $X$; we write the result of this construction as $HKl(X,T)$.  (Recall that for pseudo double categories regarded as virtual ones, functors of virtual double categories can be identified with *lax* functors of pseudo double categories.)  Thus a natural and even more general notion of generalized multicategory is "a monoid in the horizontal-Kleisli virtual double category for some monad $T$ on a virtual double category;" we call such a thing a **$T$-monoid**.

Note also that for any virtual double category $X$, there is another virtual double category $Mod(X)$ whose objects are monoids in $X$, whose vertical arrows are monoid homomorphisms, and whose horizontal arrows are "bimodules."  Therefore, for any monad $T$ on a virtual double category $X$, there is another virtual double category $KMod(X,T) = Mod(HKl(X,T))$ whose objects are $T$-monoids, and whose vertical arrows are $T$-monoid homomorphisms.

#### Examples

* If $V$ has pullbacks and $T$ is a monad preserving pullbacks (no condition on $\eta$ and $\mu$), then $T$ induces a monad on the virtual double category (which is actually, of course, a pseudo double category) $Span(V)$.  The $T$-monoids in $Span(V)$ are then precisely the $T$-multicategories, as defined above.

* The "free symmetric strict monoidal category" monad on $Prof$ can also be regarded as a monad on the virtual double category $Prof$, and its $T$-monoids on a discrete category are [[symmetric multicategories]].

* If we use instead the "free category with finite products" monad on the virtual double category $Prof$, then $T$-monoids on discrete categories can be identified with [[cartesian multicategories]], which include a sub-collection equivalent to that of [[Lawvere theories]].

* More basically, we also have a "free strict monoidal category" monad on $Prof$, whose $T$-monoids on discrete categories are ordinary non-symmetric multicategories.  Noting that $Prof = Mod(Span)$, this $T$ is also $Mod(S)$, where $S$ is the "free monoid" monad on $Span = Span(Set)$.  In fact, quite generally for any monad $S$ on a virtual double category $X$, we can identify $S$-monoids in $X$ with $Mod(S)$-monoids in $Mod(X)$ on "discrete objects."

* The [[ultrafilter monad]] $U$ on $Set$ has a "canonical" extension to the virtual double category $Rel$ of sets, functions, and binary relations.  Although $Rel$ is a pseudo double category and this monad is a strict functor, $\eta$ is only oplax.  The $U$-monoids in $Rel$ can be identified with [[topological spaces]], by an observation originally due to Barr.  In this context they are often referred to as [[relational beta-modules]], where $\beta$ is another name for $U$.

* Similarly, the powerset monad $P$ on $Set$ extends to $Rel$ in a canonical way, and the $P$-monoids in $Rel$ are [[closure space]]s.  Topological examples of this sort are sometimes called **$(T,V)$-algebras**, where $T$ denotes a Set-monad like $U$ or $P$, and $V$ a category (usually a [[quantale]]) of enrichment.

* There is a 2-monad on $Cat-Prof$ (whose objects are [[2-categories]]) whose generalized multicategories are [[2-categories with contravariance]].


### Units and transformations

...


### Equipments and normalization

...

## Obtaining the relevant monads

Each of the above contexts for generalized multicategories requires a monad of a certain sort.  Various technologies exist for producing examples of such monads, for instance:

* [[clubs]] and [[polynomial monads]] give ways to construct cartesian monads.
* [[relative pseudomonads]] give a way to construct pseudomonads on bicategories like $Prof$.
* [[double clubs]] and [[double polynomials]] give ways to construct monads on double categories.


## References

* [[Albert Burroni]], $T$-cat&#233;gories (cat&#233;gories dans un triple). Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 12 no. 3 (1971), p. 215-321, [numdam: abstract](http://www.numdam.org/item/?id=CTGDC_1971__12_3_215_0) [djvu](http://archive.numdam.org/article/CTGDC_1971__12_3_215_0.djvu) [pdf](http://archive.numdam.org/article/CTGDC_1971__12_3_215_0.pdf) 

* [[Tom Leinster]], _Higher Operads, Higher Categories_, London Math. Soc. Lec. Note Series __298__, [math.CT/0305049](http://arxiv.org/abs/math.CT/0305049), [another link](http://www.maths.gla.ac.uk/~tl/book.html)

* {#CruttwellShulman10} [[Geoff Cruttwell]] and [[Mike Shulman]], _A unified framework for generalized multicategories_, Theory Appl. Categ. **24** 21 (2010) 580-655 &lbrack;[arxiv/0907.2460](http://arxiv.org/abs/0907.2460), [TAC:24-21](http://www.tac.mta.ca/tac/volumes/24/21/24-21abs.html)&rbrack;

* [[Tom Leinster]], _Generalized enrichment for categories and multicategories_,  [math.CT/9901139](http://arxiv.org/abs/math.CT/9901139)

* [[Claudio Hermida]], _From coherent structures to universal properties_, Journal of Pure and Applied Algebra 165.1 (2001): 7-61.

* A blog post (of probably many; someone should find some others): [Generalized Operads in Classical Algebraic Topology](http://golem.ph.utexas.edu/category/2009/10/generalized_operads_in_classic.html)

* [[Martin Hyland]], _Elements of a theory of algebraic theories_, [arXiv:1311.7642](http://arxiv.org/abs/1311.7642).

[[!redirects generalized multicategories]]
[[!redirects generalised multicategory]]
[[!redirects generalised multicategories]]
[[!redirects virtual T-algebra]]
[[!redirects virtual T-algebras]]
[[!redirects generalized operad]]
[[!redirects generalized operads]]
[[!redirects (T,V)-algebra]]
[[!redirects (T,V)-algebras]]
