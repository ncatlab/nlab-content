#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In [[category theory]], a concept is (half-jokingly) said to be _evil_ if it involves equations between [[object|objects]], or more generally if it distinguishes between [[isomorphism|isomorphic]] objects.  More precisely:

* A property of categories is _non-evil_ if when it holds for a [[category]] $C$, it also holds for any category $C'$ that is [[equivalence of categories|equivalent]] to $C$.

* A property of functors is _non-evil_ if when it holds for a [[functor]] $F$, it also holds for any functor $F'$ that is [[natural isomorphism|naturally isomorphic]] to $F$.

By rigorously avoiding equations between objects, we can ensure that the properties we define are non-evil.  (This should be made more precise, to become a theorem.)

The ideas here generalize in many directions.  For example not only properties, but also constructions involving categories and functors, can be evil or non-evil.  The idea also generalizes to $n$-categories and to objects, morphisms etc. [[internalization|internal]] to $n$-categories.


## General definition

If $X$ is an $\infty$-[[infinity-groupoid|groupoid]], then a property $P$ of objects of $X$ is __non-evil__ if, whenever $P(a)$ holds for an object $a$ of $X$ and $b$ is [[equivalence|equivalent]] (as an object of $X$) to $a$, then $P(b)$ holds. Alternatively, an operation $f$ from objects of $X$ to objects of (another $\infty$-groupoid) $Y$ is __non-evil__ if, whenever $a$ and $b$ are equivalent objects of $X$, $f(a)$ and $f(b)$ are equivalent (as objects of $Y$).

(Note that everything is an object of some $\infty$-groupoid. For example, a $2$-morphism in some random $5$-category is an object of a hom-$3$-category, which has an [[core|underlying]] $3$-groupoid, which is a special kind of $\infty$-groupoid. For some purposes, this $2$-morphism may instead need to be seen as an object in a $2$-arrow $5$-category, which has an underlying $\infty$-groupoid as well; exactly which $\infty$-groupoid is relevant depends on the [[context]]. Also note that we really do need $\infty$-groupoids here, rather than $\infty$-categories, since dualities are not evil.)

The operation-version of evil gives the property-version if you think of a property as an operation taking values in the $\infty$-groupoid (in fact a $0$-groupoid, or [[set]]) of [[truth value|truth values]]. (The property-version also gives the operation-version, although that is a little more involved.) An operation will be non-evil if it is given (as the object-operation) by a [[functor]] ('$\infty$-functor', if you prefer). A property is non-evil precisely iff it\'s a functor to the $\infty$-groupoid of truth values.

This definition should be the conclusion of a theorem that using certain language (including avoiding equations between objects of a category) makes it impossible to say anything evil. [[Michael Makkai]] works on such a language, [[FOLDS]] ('first-order logic with dependent sorts'), which does not include an axiomatic notion of [[equality]] at all. This pertains to the [[foundations|mathematical foundations of category theory]]. To learn more, see his paper _[First Order Logic with Dependent Sorts, with Applications to Category Theory](http://www.math.mcgill.ca/makkai/)_.


## Examples

The most common source of evil is a statement that two [[objects]] of a given category are [[equality|equal]].  One should instead say that they are [[isomorphism|isomorphic]] and then (usually) impose some [[coherence relation]] on the relevant family of isomorphisms.  But of course, this is more complicated!

It is not evil to state that two [[morphisms]] are equal, given a common [[source]] and [[target]]; this is because a [[hom-set]] is a [[set]], where equality is meaningful.  However, it is evil to state that two morphisms are equal if the source and target are *not* given, because this includes the claim that their sources (which are objects) are equal, and similarly for the targets.

It is evil to state that two morphisms in a $2$-[[2-category|category]] are equal, because these morphisms are objects in a [[hom-category]], but it\'s not evil to state that that two $2$-moprhisms are equal, given a common source and target.  And so on.  In an $\infty$-[[infinity-category|category]], *every* claim of equality is evil.

Defining higher categorial structures using such evil equalities tends to lead to *strict* concepts; avoiding them and imposing coherence relations leads to *weak* concepts.  Sometimes there is a [[coherence theorem]] showing that every weak concept can be strictified, which justifies using equality as a figure of speech.  See [[Gray-category]] and [[model category]] for examples of this in action.


### Evil in quantum theory

The concept of [[dagger-category|†-category]] is important in [[topological quantum field theory]] and [[quantum computation]].  A **[[†-category]]** is a category $C$ with a functor

$$F: C \to C^{op} $$

which is the identity on objects and has $F^2 = 1$.  

This definition is evil: it imposes equations between objects, so we cannot transport a dagger-category structure along an equivalence of categories.
Often evil concepts (like the concept of "strict monoidal category") have non-evil counterparts (like the concept of "monoidal category").  But in this particular case there appears to be no known way to express the idea without equations between objects.  Both [[Hilb]] and [[nCob]] are dagger-categories.  This fact is important.  Try saying it in a non-evil way!  

It is possible that this problem will force a change in thinking in either the concept of evil or our thinking in quantum theory.

+-- {: .query}
By default, there is a non-evil way to say it:

Given a category $C$, a __non-evil $\dagger$-category structure__ on $C$ consists of a $\dagger$-category $C'$ and an equivalence $F\colon C \to C'$ of categories.

So one question is whether there is a less long-winded way to say that.  Another question (which logically comes before the first question) is what is the right notion of equivalence of such structures.
=--

+--{: .query}
[[Mike Shulman]]: Actually, I believe that $\dagger$-structure on a category *can* be transported along an equivalence of categories!  Suppose that $F\colon C \to D \colon G$ is an [[adjoint equivalence]] with unit $\eta\colon Id_C \overset{\cong}{\to} G F$ and counit $\varepsilon\colon F G \overset{\cong}{\to} Id_D$, where $D$ is a $\dagger$-category.  Given $f\colon x\to y$ in $C$, define $f^\dagger$ to be the following composite:
$$ y \overset{\eta}{\to} G F y \overset{G((F f)^\dagger)}{\to} G F x \overset{\eta^{-1}}{\to} x. $$
This evidently defines a functor $C^{op} \to C$ that is the identity on objects.  Now $F(f^\dagger)$ is given by
$$ F y \overset{F \eta}{\to} F G F y \overset{F G((F f)^\dagger)}{\to} F G F x \overset{F \eta^{-1}}{\to} F x $$
but by the triangle identities this is equal to
$$ F y \overset{\varepsilon^{-1}_F}{\to} F G F y \overset{F G((F f)^\dagger)}{\to} F G F x \overset{\varepsilon_F}{\to} F x $$
and hence equal to $(F f)^\dagger$ by naturality of $\varepsilon$.  Thus, since $((F f)^\dagger)^\dagger = F f$ in $D$, in $C$ we have that $(f^\dagger)^\dagger$ is given by
$$ x \overset{\eta}{\to} G F x \overset{G F f}{\to} G F y \overset{\eta^{-1}}{\to} y. $$
which is equal to $f$ by naturality of $\eta$.  Thus, $C$ is a $\dagger$-category, and essentially by construction $F$ and $G$ are $\dagger$-functors (though $\eta$ and $\varepsilon$ need not be unitary).

So if a notion refers to equality of objects in a seemingly irreducible way, but it can nevertheless be transported along an equivalence of categories, is it evil or isn't it?  Thinking about it some more, I'm actually not convinced that $\dagger$-structure is evil at all.  Consider the assertion that a category is a groupoid.  Clearly this is not evil!  But what it means is that for any morphism $f\colon x\to y$, there exists a morphism $f^{-1}\colon y\to x$ whose source is *equal* to the target of $f$, and whose target is *equal* to the source of $f$, and such that $f f^{-1}$ and $f^{-1} f$ are identities.  The notion of $\dagger$-category is entirely analogous: for any morphism $f\colon x\to y$, we are given a specified morphism $f^\dagger\colon y\to x$ with certain properties.  The only difference is that the first is a *property* and the second is *structure*, but why should that matter?

As remarked in the discussion below, equality of objects is all over the place in category theory: whenever we introduce an arrow, we have to say what its source and target are, and one or the other (or both) will often be *equal* to some object we are already considering.  But this is not really evil; it's really just a *typing assertion*.  (If you write category theory in a logic of [[dependent types]] like [[FOLDS]], then that's exactly what it is.)  Maybe $\dagger$-structure is just the same.

[[Mike Shulman]]: Here's an interesting analogy: let $G$ be a group and consider categories enriched over $G$-sets.  In such a category, for every morphism $f\colon x\to y$ and every $g\in G$ we have another morphism $f^g\colon x\to y$ satisfying certain axioms, which may look evil (since $f^g$ has equal source and target to $f$) but is really not.  Moreover, just like for $\dagger$-categories and unitary isomorphisms, in this case the "underlying groupoid" is not the naive core of the original category, but consists of only the $G$-fixed isomorphisms.  Actually, $\dagger$-categories have always felt a lot like enriched categories to me, though the "enrichment" is sort of "non-local" in that the structure on homsets relates more than one of them, so it's hard to make this precise.
=--


## Discussion

There's been a lot of discussion of this on the $n$-Category Caf&#233; --- someone find it and cite it!


+-- {: .query}
Comment: It seems that at some level you can't avoid equality, at least if you want to completely formalise things (say, in a proof assistant). For example, in the definition of "category" itself (on which the definitions of isomorphism and $\infty$-groupoid seem to depend), we say that $g \circ f$ is defined iff $\dom g = \cod f$.

Now if you start your theorem with "let $a,b,c$ be objects of $C$ and let $g : b \to c$,$f: a \to b$ be morphisms", then there's no problem. But what if you need to compose morphisms whose dom/cod aren't definitionally/syntactically equal? I suppose that at this point it depends on which foundations you use.

Reply:  Yes, it can depend on the foundations.  [[FOLDS]] is a foundation specifically designed to avoid evil, and higher category theory has been formulated in it (by [[Michael Makkai]], who invented both FOLDS and a multitopic definition of higher categories to go with it).  More generally, the style of terminology that you gave comes naturally to a development of (higher) category theory in a foundation based on dependent [[type theory]].

Even in your first example, the quesion of whether we can compose $g \circ f$, we can avoid evil if we try.  Na&#239;vely, we can compose them if and only if $\dom g = \cod f$; composability is a property of the pair ---but an evil property.  Less evilly, we make composability a *structure* on the pair; we can compose them along any isomorphism between $\dom g$ and $\cod f$.  So as usual in category theory, we don\'t ask whether these objects are equal but instead how they might be isomorphic.

Of course, if $f$ and $g$ are given as $g: b \to c$ and $f: a \to b$, then we can compose them along the identity morphism of $b$; this is the usual notion of compoisition in that case.  It is only when $f$ and $g$ are not given to us in such a way that we have to talk about composing along an arbitrary (possibly nonexistent, certainly not likely to exist uniquely) isomorphism.

Can you say everything that you want to say about (higher) categories while avoiding evil throughout?  That will always be an open question, as people think of new things to say about them.  But I think that it is a fruiful attitude to take that one should try.  ---[[Toby Bartels]]

[[Mike Shulman]]: I'm not convinced by "composing along isomorphisms," because what does it mean for an isomorphism $h$ to be "between" $\dom g$ and $\cod f$?  It means that $\dom h = \cod f$ and $\cod h = \dom g$.

_Toby_:  But <del>you</del><ins>the Anonymous Coward</ins> already told us how to phrase things above: "let $a,b,c$ be objects of $C$ and let $g : b \to c$,$f: a \to b$ be morphisms".  So now we take a case where $dom g$ and $cod f$ are not definitionally/syntactically equal, as so:
> Let $a,b,c,d$ be objects and let $g: c \to d,\; f: a \to b$ be morphisms.
Then we can form the composite $g \circ f$ relative to any isomophism $h: b \to c$.  (Of course, the notation $g \circ f$ suppresses $h$, so it\'s more proper to write $g \circ_h f$, or just $g \circ h \circ f$ as a normal person would.)

Note that the definability of $g \circ f$ is now the set $Iso(b,c)$ rather than the truth value $b = c$.  In an $\infty$-category, it would be an $\infty$-groupoid $Iso(b,c)$.

[[Mike Shulman]]: That wasn't me above, I don't think.  I would consider "let $g : b \to c$ and $f: a \to b$ be morphisms" as implicitly using dependent types if you're considering it to avoid evil.  It seems to me that in a non-dependently typed theory, the only thing "let $g : b \to c$ and $f: a \to b$ be morphisms" can mean is "let $g$ and $f$ be morphisms such that $\dom f = a$, $\cod f = b$, $\dom g = b$, and $\cod g=c$," which does involve talking about equality of objects.

_Toby_:  Right on both counts: that was an [[Anonymous Coward]] in the first comment, and the phrasing that the Coward suggested does implicitly use dependent types (as I alluded to in my original reply).  Makkai says 'dependent sorts' (the 'DS' in 'FOLDS') instead for some reason.  Can we avoid evil in an independently typed (possibly even untyped) language?  I think that this should be possible; we would need rules about when you can and can\'t state equalities; maybe, you can state $\forall f, dom f = x \Rightarrow ...$ and the obvious variations, but no others?

[[Mike Shulman]]: In other words, you can secretly make your independent types act like dependent ones?  (-:

_Toby_:  Yeah, a dependent type theory can always be rephrased as an independent type theory, although you have to use equality to do this; this is equivalent to the original dependent type theory if (as is the common practice) that theory also had equality predicates, but otherwise it\'s stonger.  Similarly, a typed theory can be rephrased as an untyped theory, although you have to use typing predicates to do this, and again this is stronger.  Conversely, we know (well, some people know) how to limit the use of the typing predicates in the untyped theory to make it equivalent to the typed theory.  Now I think that there also ought to be rules to limit the use of equality in a simple type theory to make it equivalent to a dependent type theory *without* equality.

[[Mike Shulman]]: Amazingly enough, as you said at latest changes, this conversation does seem to be leading in the direction of actual mathematics.  It does seem like that should be possible, but I don't have the time to think about it any more deeply now.  Aside from pointing out the obvious fact that until we get to $\omega$-categories, we do want to allow equality relations on *some* of the types in the dependent type theory.

_Toby_:  I also don\'t have the time to think about it carefully; I feel pretty secure about my intuition, but that is all.  But I would see the equality relation between parallel $n$-morphisms in an $n$-category as something extralogical, just as much as the type of $n$-morphisms between parallel $(n-1)$-morphisms.

_Harry_: Couldn't we just say: Let $f$ and $g$ be (left? right?)-composable iff $h[dom g]$ is isomorphic to $h[cod f]$ where $h$ is the homotopy category functor (assuming quasicategories, but there should be a good enough way to define this in more generality, no?).  This way, $g \circ f$ is only specified up to homotopy (that is, we know that it's in the homotopy class of $h[g] \circ h[f]$.  I think there might be a few technicalities to work out with 1-Categories, but applying the homotopy functor immediately collapses it to that case.  

_Toby_:  That seems to bring us back to the idea of composing along an isomorphism between $dom g$ and $cod f$, now generalised to quasicategories.

[[Mike Shulman]]: Yes, if you only know that $h[dom g]$ is isomorphic to $h[cod f]$, you still need to *choose* an isomorphism along which to compose $f$ and $g$.  Different choices will give you different "composites".

_Harry_: Can two wrongs (or evils in this case) make a right?  Maybe we can solve the composition problem by passing to the skeleton of the homotopy category?

[[Mike Shulman]]: I think the short answer is "no."  Choosing a skeleton (together with an equivalence to the category one started with, naturally) involves choosing a bunch of specified isomorphisms between isomorphic objects, so really you aren't doing anything different.
=--
