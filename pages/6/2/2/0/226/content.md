We assume you know the [usual definition](http://en.wikipedia.org/wiki/Vector_space#Definition) of a vector space over a field $k$.

The [[category]] of vector spaces is called [[Vect]], or 
$Vect_k$ if we wish to make the field $k$ explicit.  This category has vector spaces over $k$ as objects, and linear maps between these as morphisms.

Vector spaces over fields are a special case of [[module|modules]] of [[ring|rings]]. A vector space over the field $F$ is just an $R$-module where the ring $R$ happens to be the field $k$, and a linear map between vector spaces is then an $R$-module morphism.  So, the category $Vect_k$ is the same as the category $R Mod$ when $R = k$.  There is a lot of nice abstract stuff to be said about the category $R Mod$ --- see the entry on [[module|modules]].

#Discussion#

_[[Eric Forgy]] says_: Is there a nice _arrow theoretic_ way to define vector spaces?

_[[Urs Schreiber|Urs]] says_: There is comparatively nice abstract nonsense to be said about _rings_. For instance, a [[ring]] is a category with one object [[enriched category|enriched in]] the category of abelian groups. From that starting point the concepts of ring theory develop rather naturally from pure category theoretic reasoning. In particular [[module|modules]] over rings appear naturally.

For some reason this is different when rings are refined to _fields_ and modules to vector spaces. The very concept of a _field_ is somehow not as natural from a category theoretic perspective, or at least I don't see how it is. This problem becomes very manifest when one tries to categorify fields and vector spaces: it is very straightforward to categorify rings and their modules, but their refinement to categorified fields  and vector spaces is harder.

_[[Eric Forgy|Eric]] says_: <nowiki>*tongue in cheek*</nowiki> Well, fields are closely tied to the continuum and we know the continuum is not natural :)

_[[Toby Bartels|Toby]] says_: \*tongue where it belongs\* A field may be defined a ring that has been decomposed (as a set) as the sum of a point and a group, with the point being the zero element and the the group being a multiplicative submonoid. However, this definition does not work in constructive analysis; one cannot prove constructively that the ring of real numbers has this property. Instead, one must define a field to be a ring equipped with an [[apartness relation]] satisfying some properties (which I can write down if desired). Classically, an apartness relation is a vacuous structure, but in constructive mathematics its properties have a very topological flavour, even though it\'s much simpler than a topology. All of the deep issues about the continuum are already there in the constructivists\' notion of apartness, which they require to even define what a field is.

_[[John Baez|John]] says_: As Toby notes, fields are a somewhat awkward concept in constructive mathematics.  The basic problem is that their definition involves a clause "if $x \ne 0$, then $x$ has an inverse..."  A clause of the for "if something is not true, then..." is rather annoying in constructive mathematics.  This means fields are not very nice if you're trying to do math in an arbitrary topos.  And since topos theory was invented when Grothendieck was working on algebraic geometry, this should mean that fields are not very nice when you're trying to do algebraic geometry!   

Of course this is a bit shocking, since the first thing an elementary text on algebraic geometry does is say "Let $k$ be a field."  But Grothendieck's revolutionary approach to algebraic geometry also downplays the importance of fields, so presumably it all hangs together once you understand it.

I wish I understood this better.  There's a nice exposition of <i>a little bit</i> of these ideas in Mac Lane and Moerdijk's <i>Sheaves in Geometry and Logic: A First Introduction to Topos Theory</i>.  Look up 'local ring' in their index: you'll see that unlike the notion of field, the notion of [local ring](http://en.wikipedia.org/wiki/Local_ring) can be defined using 'geometric logic', which is (very roughly) the kind of logic that works well in topoi.

[[Eric Forgy|Eric]]: The wikipedia article on "Category of fields" has some interesting things to say about the difficulties with fields in category theory.

If fields are less than perfectly natural, then vector spaces are somewhat troublesome too. But what about the [tangent bundle of a category](http://golem.ph.utexas.edu/category/2007/07/tangent_categories.html)? That idea is very pretty. In what way does it fail to converge to the usual concept of a tangent space, which should contain vector spaces (obviously)? <nowiki>[Edit: Sorry. The answer was in the very link I provided, but any further light on the subject would be appreciated.]</nowiki>