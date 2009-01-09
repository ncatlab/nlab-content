In classical mathematics, a **field** is a commutative [[ring]] in which every nonzero element has a multiplicative inverse and $0\neq 1$ (which may be combined as: an element is invertible if and only if it is nonzero).

Fields are not as well-behaved categorically as most other common algebraic structures ([[group]]s, [[ring]]s, [[module]]s, etc.).  In particular, the category of fields is not [[complete category|complete]] or [[cocomplete category|cocomplete]], although it is [[accessible category|accessible]].

For the same reason, in [[constructivism|constructive mathematics]] (such as the [[internal logic]] of a topos) there are different inequivalent ways to define a field.  In this case the above definition is not usually the best one; for instance, the real numbers do not satisfy it.  There are several potential replacements with their own advantages and disadvantages.

* If we replace "an element is invertible iff it is nonzero" by "an element is invertible xor (exclusive or) it equals zero" (which is classically equivalent but constructively stronger), we obtain the notion of **discrete field**. An advantage is that this is a [[coherent logic|coherent theory]]; a disadvantage is that it is not satisfied (constructively) by the ring of real numbers (however defined).

* If instead we replace this clause by "an element is noninvertible iff it is zero" (which is classically equivalent but constructively incomparable), we obtain the notion of **residue field**. A disadvantage is that this is not a coherent axiom and so cannot be [[internalization|internalized]] in as many categories. An advantage is that the real numbers (in the located Dedekind sense) form a residue field; furthermore, the quotient of any [[local ring]] by its ideal of noninvertible elements is a residue field (hence the name).

* If we interpret 'nonzero' as a reference to an [[apartness relation]] and assume that the ring operations are strongly extensional, then we obtain the notion of **Heyting field**. (Although this seems to have extra structure, the apartness relation is definable from the algebra: $x # y$ iff $x - y$ is invertible.) This is how 'practising' constructive analysts of the Bishop school usually define the simple word 'field'; it has the same advantages and disadvantages given above for a residue field.

Note that every discrete field or Heyting field is also a residue field; a residue field is a discrete field if and only if [[decidable equality|equality is decidable]], and it\'s a Heyting field if and only if it is a local ring.

+--{.query}
Mike (or anybody): It seems to me that the term 'residue field' should only be used if the field actually *is* the residue field of a local ring, in which case it will be itself a local ring (and thus also a Heyting field). I would like to prove that every residue field as here defined is a local ring, but I can\'t do it; how do I decide the disjunction? If this can\'t be proved, perhaps a residue field should be required by definition to be local? (That is, $x$ or $1 + x$ is always invertible.)
=--

### Discussion ###

    This discussion was originally at [[vector space]], but most of it is really about fields.

_[[Eric Forgy]] says_: Is there a nice _arrow theoretic_ way to define vector spaces?

_[[Urs Schreiber|Urs]] says_: There is comparatively nice abstract nonsense to be said about _rings_. For instance, a [[ring]] is a category with one object [[enriched category|enriched in]] the category of abelian groups. From that starting point the concepts of ring theory develop rather naturally from pure category theoretic reasoning. In particular [[module|modules]] over rings appear naturally.

For some reason this is different when rings are refined to _fields_ and modules to vector spaces. The very concept of a _field_ is somehow not as natural from a category theoretic perspective, or at least I don't see how it is. This problem becomes very manifest when one tries to categorify fields and vector spaces: it is very straightforward to categorify rings and their modules, but their refinement to categorified fields  and vector spaces is harder.

_[[Eric Forgy|Eric]] says_: <nowiki>*tongue in cheek*</nowiki> Well, fields are closely tied to the continuum and we know the continuum is not natural :)

_[[Toby Bartels|Toby]] says_: \*tongue where it belongs\* A field may be defined a ring that has been decomposed (as a set) as the sum of a point and a group, with the point being the zero element and the the group being a multiplicative submonoid. However, this definition does not work in constructive analysis; one cannot prove constructively that the ring of real numbers has this property. Instead, one must define a field to be a ring equipped with an [[apartness relation]] satisfying some properties (which I can write down if desired). Classically, an apartness relation is a vacuous structure, but in constructive mathematics its properties have a very topological flavour, even though it\'s much simpler than a topology. All of the deep issues about the continuum are already there in the constructivists\' notion of apartness, which they require to even define what a field is.

_[[John Baez|John]] says_: As Toby notes, fields are a somewhat awkward concept in constructive mathematics.  The basic problem is that their definition involves a clause "if $x \ne 0$, then $x$ has an inverse..."  A clause of the for "if something is not true, then..." is rather annoying in constructive mathematics.  This means fields are not very nice if you're trying to do math in an arbitrary topos.  And since topos theory was invented when Grothendieck was working on algebraic geometry, this should mean that fields are not very nice when you're trying to do algebraic geometry!   

Of course this is a bit shocking, since the first thing an elementary text on algebraic geometry does is say "Let $k$ be a field."  But Grothendieck's revolutionary approach to algebraic geometry also downplays the importance of fields, so presumably it all hangs together once you understand it.

I wish I understood this better.  There's a nice exposition of <i>a little bit</i> of these ideas in Mac Lane and Moerdijk's <i>Sheaves in Geometry and Logic: A First Introduction to Topos Theory</i>.  Look up 'local ring' in their index: you'll see that unlike the notion of field, the notion of [local ring](http://en.wikipedia.org/wiki/Local_ring) can be defined using 'geometric logic', which is (very roughly) the kind of logic that works well in topoi.

_[[Eric Forgy|Eric]] says_: The wikipedia article on [Category of fields](http://en.wikipedia.org/wiki/Category_of_fields) has some interesting things to say about the difficulties with fields in category theory.

If fields are less than perfectly natural, then vector spaces are somewhat troublesome too. But what about the [tangent bundle of a category](http://golem.ph.utexas.edu/category/2007/07/tangent_categories.html)? That idea is very pretty. In what way does it fail to converge to the usual concept of a tangent space, which should contain vector spaces (obviously)? <nowiki>[Edit: Sorry. The answer was in the very link I provided, but any further light on the subject would be appreciated.]</nowiki>

_Toby says_: Rather than think about the category of fields, shouldn\'t we think of fields as [[dichotomy between nice objects and nice categories|nice objects in the nice category]] of rings? Modules, after all, behave beautifully.