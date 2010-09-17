
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Type-theoretic definition of category
* table of contents
{: toc}

## Motivation

There are two broad definitions of [[category]] in the literature: one which immediately generalises to the usual definition of [[internal category]] and one which immediately generalises to the usual definition of [[enriched category]].

Here we consider the latter definition and show how it may naturally be expressed in [[dependent type theory]].  In a [[type theory]] where [[types]] are [[presets]] (without an inherent [[equality predicate]]), it is not manifestly possible to express so-called [[evil]] ideas in category theory.


## Definition

In a [[dependent type theory]] with [[dependent record type|dependent record types]] we can define a type of categories as follows (using a two-dimensional syntax):
\[\begin{aligned}
  \biggl\{&\mathrm{Obj}\colon\mathrm{Type}, \\
    &\frac{a,b\colon\mathrm{Obj}}{\hom(a,b)\colon\mathrm{Type}_=}, \\
    &\frac{a\colon\mathrm{Obj}}{1_a\colon\hom(a,a)}, \\
    &\frac{f\colon\hom(b,c) \quad g\colon\hom(a,b)}{f\circ g\colon\hom(a,c)}, \\
    &\frac{g\colon\hom(a,b)}{\mathrm{left}\text{-}\mathrm{unit}\coloneq 1_b\circ g=g}, \\
    &\frac{f\colon\hom(a,b)}{\mathrm{right}\text{-}\mathrm{unit}\coloneq f\circ 1_a=f}, \\
    &\frac{f\colon\hom(c,d) \quad
        g\colon\hom(b,c) \quad h\colon\hom(a,b)}{\circ\text{-}\mathrm{assoc}\coloneq f\circ(g\circ h) =
        (f\circ g)\circ h} \\
  &\!\biggr\}
\end{aligned}\]
Here, $\mathrm{Type}$ is a type of types, and $\mathrm{Type}_=$ is a type of types with equality predicates (we may or may not have $\mathrm{Type}=\mathrm{Type}_=$).

The two-dimensional syntax is convenient to allow inference of [[implicit parameter|implicit parameters]], and to signify notation. We read the horizontal line as a rule, so for instance the second line means that whenever $a$ and $b$ have type $\mathrm{Obj}$, then we have a type $\hom(a,b)$ (with equality).

The notation $p\coloneq P$ signifies that $p$ is a proof of the [[proposition]] $P$ (under [[propositions as types]], this may be the same as $p\colon P$, but many type theories treat propositions as distinct from types).

So the above defines that a category is a record consisting of a type of objects, and for each pair of objects a type of homomorphisms between them, and also identity and composition operations satisfying unit laws and associativity.


## Discussion

The defined type of categories cannot itself be a member of $\mathrm{Type}$, otherwise we run into [[Girard's paradox]]. This is related to the size issues for categories. 

+--{.query}
_Anonymous from the Peanut Gallery asks_: How do we define small categories type-theoretically? It seems to me that a natural thing to try is to make "small" mean "$\mathrm{Obj}$ is a setoid (ie, element of $\mathrm{Type}_=$)", but then the coherence conditions on the type operator of morphisms make my head explode. (Namely, if $(A, \simeq)$ is a setoid, and $a \simeq a'$, then we expect $\hom(a,b) \triangleq \hom(a',b)$, but I don't see how $\triangleq$ should be defined! What should the type of homs be now, and what properties should they satisfy?) 

_Ulrik_: The above does define a type of small categories (given that $\mathrm{Type}$ is a type of small types). Adding equality to $\mathrm{Obj}$ (making it a setoid), defines small [[strict categories]]. Then, as you mention, we need an equality on $\mathrm{Type}$ in order to formulate the coherence condition (the type theory might do this automatically, though). To define large categories we need a larger universe of types (just like the situation in set theory).

_Toby_:  In other words, smallness and strictness are two separate things, although sometimes they go together.  If $Type$ is the type of small types (and therefore is itself a moderate type but not a small type) and similarly for $Type_=$, then the definition above gives small categories.  If $Type$ is the type of moderate types but $Type_=$ remains the type of small types with equality, then the definition above gives locally small moderate categories.  If $Type$ and $Type_=$ are both types of moderate types, then the definition above gives moderate categories.  Independently of this, if you change the type of $Obj$ from $Type$ to $Type_=$ (and add some coherence conditions), then you get strict categories.

But it seems like there\'s still something to make your head explode: how do we define strict categories in this framework?  (The tricky part is the coherence conditions in my previous parenthetical remark above.)  You have the right idea that, if $a \simeq a'$, then $\hom(a,b) \triangleq \hom(a',b)$, but what you\'re missing is that $\triangleq$ means isomorphism of setoids.  That is, we have a rule
$$ \frac{p\coloneq a \simeq a' \quad f\colon\hom(a,b)}{\mathrm{conv}_{a,a'}f\colon\hom(a',b)} ,$$
representing a map of setoids $\mathrm{conv}_{a,a'}\colon \hom(a,b) \to \hom(a',b)$.  (There is a similar rule on the other side.)  Then you also need some coherence laws stating that $\mathrm{conv}_{a,a} = \id_{\hom(a,b)}$ and $\mathrm{conv}_{a',a''} \circ \mathrm{conv}_{a,a'} = \mathrm{conv}_{a,a''}$ (and two laws on the other side).  I *think* that this is all.

The definition that I usually use for a [[strict category]], however, is this:  a __strict category__ consists of a set (of type $Type_=$, what we\'ve been calling 'setoid' above) $O$, a category (in the weak sense defined here) $C$, and an [[essentially surjective functor]] $\overline{}$ to $C$ from the [[discrete category]] on $O$.  We then think of $O$ as the set of objects, the set of morphisms from $a$ to $b$ (for $a,b\colon O$) is $\hom_C(\overline{a},\overline{b})$, etc.  (Again, strictness is independent of smallness; $O$ might be a small set, or a large proper class, or whatever.)

_Anonymous_: Ulrik, Toby: Thank you for the advice! You're exactly right that what I've been groping for is strictness, not smallness. My true motivation is to implement a few constructions on functor categories in type theory. However, the way that the exponential in presheaf categories is usually defined has been pretty puzzling to me: given the category $\mathrm{Set}^I$, the exponential is defined as $F \Rightarrow G (X) = \mathrm{Set}(I(X, -) \times F, G)$. It's exactly the lack of strict structure on objects in the type-theoretic definition that has left me puzzled. I'll go play with the constructions you've suggested and see if I can make it work for me.

However, I do have another question, though this one arises out of curiosity rather than for any practical reason. In impredicative type theories (like the calculus of constructions) you basically give up the powerset axiom in exchange for the ability to index over the universe (i.e., you can define types like $\forall \alpha:\mathrm{Type}. A(\alpha)$). It seems like you would still need a strictness condition to define constructions on functor categories, even though traditional size issues are cunningly rendered unsayable. Has anyone looked at what happens when you formalize category theory in such type theories (or for that matter, in set theories with a set of all sets, like NF)?

_Ulrik_: Some quick remarks on your last questions: In impredicative type theory strong sums are inconsistent (by interpreting Girard's paradox again), so you can't form a type of meta-categories (you can still have types of types, you just can't sum over ALL types). As for NF (or NFU), the category of sets is not cartesian closed, which causes a host of problems.
=--


[[!redirects type-theoretic definition of category]]
[[!redirects type-theoretic definition of a category]]
[[!redirects type-theoretic definition of categories]]
[[!redirects type-theoretic definitions of category]]
[[!redirects type-theoretic definitions of a category]]
[[!redirects type-theoretic definitions of categories]]
[[!redirects preset-theoretic definition of category]]
[[!redirects preset-theoretic definition of a category]]
[[!redirects preset-theoretic definition of categories]]
[[!redirects preset-theoretic definitions of category]]
[[!redirects preset-theoretic definitions of a category]]
[[!redirects preset-theoretic definitions of categories]]
