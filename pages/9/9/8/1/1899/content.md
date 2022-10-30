# Idea #

Given an [[algebraic theory]] $V$, a $V$-algebra is a model of $V$ in the category $Set$.  A _Tall--Wraith $V$-monoid_ is _the kind of thing that acts on $V$-algebras_.  


# Definition #

+-- {: .num_definition #twmonoid}
###### Definition
Let $V$ be an [[algebraic theory]] and let $V Alg$ be the category of models of this theory in $Set$.  Then a **Tall--Wraith $V$-monoid** is a [[monoid|monoid object]] in the category of co-$V$-objects in $V Alg$.   
=--

To see why these are _what acts on $V$-algebras_ one needs to understand what a co-$V$-object in $V Alg$ actually is.
A co-$V$-object in some category $D$ is a [[representable functor|representable covariant functor]] from $D$ to $V Alg$.  To give a particular $D$-object, $d$, the structure of a co-$V$-object is to give a lift of the $Set$-valued $Hom$-functor $D(d,-)$ to $V Alg$.
Thus a co-$V$-object in $V Alg$ is a representable covariant functor from $V Alg$ to itself.

One can therefore consider composition of such representable covariant functors.
The main result of this can be simply stated:

+-- {: .num_proposition #repcomp}
###### Proposition
The composition of representable covariant functors $V Alg \to V Alg$ is again representable.
=--

This is a basic result in general algebra, and is not stated here in its full generality.

An almost corollary of this is that the category of representable covariant functors from $V Alg$ to itself is monoidal (the "almost" refers to the fact that you have to show that the identity functor is representable, but this is not hard).

Thus for two co-$V$-algebra objects in $V$, say $R_1$ and $R_2$, there is a product $R_1 \odot R_2$ and a natural isomorphism

$$
Hom_V(R_1 \odot R_2,A) \cong Hom_V(R_1, Hom_V(R_2,A))
$$

for any $V$-algebra, $A$.

A **Tall--Wraith $V$-monoid** is thus a triple $(P,\mu,\eta)$ with $\mu : P \odot P \to P$ and $\eta : I \to P$ (where $I$ is the free $V$-algebra on one element --- this represents the identity functor), satisfying the obvious coherence diagrams.
An action of $P$ on a $V$-algebra, say $A$, is then a morphism $\rho : P \odot A \to A$ again satisfying certain coherence diagrams.

Ah, but I have not told you what $P \odot A$ is!
At the moment, one can take the "product" of two co-$V$-algebra objects in $V Alg$ but now I want to take the product of a co-$V$-algebra object with a $V$-algebra.
How do I do this?
I do this by observing that a $V$-algebra is a _co-$Set$-algebra object in $V Alg$_!
That's a complicated way of saying that $V$ represents a covariant functor $V Alg \to Set$.
Precomposing this with the functor represented by $P$ yields again a covariant functor $V Alg \to Set$.
This is again representable and we write its representing object $P \odot A$.

As an aside, we note a consequence.  As we've seen, the category of co-$V$-algebra objects in $V$ is a monoidal category, with the tensor product $\odot$.  Now we're seeing this monoidal category [[action|acts]] on the category of $V$-algebras.   Indeed, it acts on the categories of $V$-algebra and co-$V$-algebra objects in a reasonably arbitrary base category.

One postscript to this is that although the category of co-$V$-algebra objects in $V Alg$ is not a variety of algebras, for a specific Tall--Wraith $V$-monoid $P$, the category of $P$-modules _is_ a variety of algebras.



# Examples #

* If $V$ is the theory of [[commutative ring|commutative unital rings]], a $V$-algebra is a commutative unital ring, and the corresponding sort of Tall--Wraith $V$-monoid is called a [[biring]].  

* If $V$ is the theory of [[commutative algebra|commutative associative algebras]] over a [[field]] $k$, then a $V$-algebra is a commutative associative algebra over $k$, and the corresponding sort of Tall--Wraith $V$-monoid is called a [[plethory]].

* If $V$ is the theory of [[abelian group|abelian groups]], than a $V$-algebra is an abelian group, and the corresponding sort of Tall--Wraith $V$-monoid is a [[ring]].

  To understand the last example, we need to think about _co-abelian group objects in the category of abelian groups_.  Abstractly, such a thing is an abelian group object [[internalization|internal to]] $AbGp^{op}$. Concretely, such a thing is an abelian group $A$ together with group homomorphisms

  $$
  \Delta : A \to A \coprod A, $$
  $$\epsilon : A \to I $$

  where $I$ is the initial object in the category of abelian groups.  These homomorphisms must satisfy certain laws: just the abelian group axioms written out diagrammatically, with all the arrows turned around.

  In fact, $I = \{0\}$.  Thus $\epsilon$ is forced to be the map that sends everything to $0$: we have no choice here.

  We also have that $A \coprod A = A \oplus A$.
That means that for $a \in A$, $\Delta(a) = (a_1,a_2)$ for some $a_1, a_2 \in A$.  Now, one of the laws says that $\epsilon$ is a counit for $\Delta$. This means that $(\epsilon \oplus 1) \Delta = 1$ and similarly for $1 \oplus \epsilon$. Thus $a_1 = a_2 = a$ and $\Delta$ is the diagonal map.  So, we have no choice here either.

  Indeed, it is easy to show that the triple $(A, \Delta, \epsilon)$ with $\Delta$ the diagonal map and $\epsilon$ the zero map _is_ a co-abelian group object in the category of abelian groups.  Thus the category of co-abelian group objects in the category of abelian groups is isomorphic, via the obvious forgetful functor, to the category of abelian group objects.

  (Indeed, our argument here has shown more generally that if $X$ is a category with finite products, the category of comonoid objects in $X$ is equivalent to $X$.  Something about $AbGp$ is making these comonoid objects be co-abelian group objects.)

  +-- {: .query}
  [[Andrew Stacey]]: I missed the inclusion of the above paragraph first time round.  History ascribes it to John, am I reading that right?

  [[John Baez]]: Yup.  It's a standard and very useful piece of wisdom that if $X$ is a category with finite products, the category of comonoid objects in $X$ is equivalent to $X$.  So, I couldn't resist pointing out that you'd proved that here.  Ultimately this very general fact should be moved somewhere else.  For example, this fact explains why people talk a lot about 'monoids' in the category of sets, but never 'comonoids'.

  [[Andrew Stacey]]: Expanding your statement, then the above shows that the category of comonoid objects in $(X,\times,1)$ (where $1$ is a terminal object) is equivalent to $X$.  The "[s]omething about $AbGrp$" is that in $AbGrp$ then finite coproducts are the same as finite products.  Thus a monoid object in $(AbGrp^{op},\times^{op},1^{op})$ is the same as a comonoid object in $(AbGrp,\coprod,0)$ which is the same as a comonoid object in $(AbGrp,\prod,1)$.  I guess we implicitly use the fact that monoids (and thus comonoids) can be specified by finitary operations and relations.

  [[John Baez]]:  That's not the "something about $AbGrp$" that I was hinting at.  I was taking it for granted that finite products and finite coproducts are the same in $AbGrp$.   

  You were trying to show that co-abelian group objects in the category of abelian groups are the same as abelian groups.  

  A general argument shows that comonoid objects in a category with finite products are the same as objects.  

  So we see comonoid objects in $AbGrp$ are the same as abelian groups. 

  But we still need to see that _**comonoid** objects in $AbGrp$ are the same as **co-abelian group** objects in $AbGrp$_.

  The quickest way to see this seems to be a little calculation --- as you say, it's "easy to show".  But I still think "there's something about $AbGrp$" that makes this calculation work --- some general fact.  Something about morphisms having negatives, I think.  So I bet it's true in any abelian category $X$, that comonoid objects in $X$ are the same as co-abelian group objects in $X$.
  
  But never mind... 

  [[Andrew Stacey]]: Ah, now I see.  It's the difference between "abelian group" and "monoid" that you're interested in.  Okay, I'll think about that.

  By the way, I'm not clear about how to interpret your hints.  Do you already know the answer to this and are trying to teach me some category theory by leading me through it, or do you not know and are hoping that, polymath-style, we'll figure it out without either of us having to expend too much energy?  Either is fine by me (I need to learn some more Cat. Th. so any help is helpful!), I just like to know which track I'm on.

  [[John Baez]]: I guess I'm just trying to figure it out. From the very start I knew _some_ answer to why comonoid objects in $AbGp$ are co-abelian group objects: namely, when you check, you see it's true.  But I like to understand these things using general principles, so I was wondering what general principle was at work here.  My current best guess is not very profound: it's "every comonoid object in an abelian category is a co-abelian group object", or if you prefer, "every object in an abelian category becomes a co-abelian group object in a unique way" - a variation on the well-trodden theme of "every object in a category with finite products becomes a cocommutative comonoid in a unique way".    

  [[Andrew Stacey]]: PS Don't forget to indent paragraphs in this query box.

   [[John Baez]]: Huh, wow, it really makes a big difference.

  [[Andrew Stacey]]: can't tell if you're being sarcastic here.  If so, try leaving a comment with _absolutely no_ indent and see what chaos ensues.

  [[John Baez]]: No, I wasn't being sarcastic.  I tried it and saw what chaos ensued.  But further down the page we're having a boxed discussion without these darned indents, and it's working fine.  So why bother with indents in the first place?

  _Toby_: The purpose of the indentation is to keep the query box with the appropriate entry in the unnumbered list.  Besides the obvious (and obviously small) aesthetic advantage, this does two things when it happens in the middle of a list:
  *  it helps the diff mechanism tell when a query box is inserted or removed with no other change to the list;
  *  it keeps the numbering in a numbered list correct.

  [[Lab Elf]]: Actually, it does more than that.  Without the indentation then the parser gets really confused as to where the list ends.  It tries to end the list before the comment ends, but that would lead to malformed XHTML so somewhere the offending section gets removed.  Have a go at removing the indentation of a comment and see what happens.

  The thing to remember is that indentation _means_ something and so should only be added or removed by experienced Lab Elves who have undergone rigorous training in how to safely remove indentation without risking danger to the public.

  The rule is: the _contents_ of a query box (or other box: theorems, proofs, all come under this heading) should have the same indentation (or more) as the opening demarkation.
  =-- 

  It is part of the general theory that the category of co-$V$-objects in $V$ is monoidal (though not, in general, symmetric). For details on this see _The Hunting of the Hopf Ring_, referred to belelow.  This monoidal structure for abelian groups turns out to be the tensor product.

  Thus a Tall--Wraith monoid for abelian groups is actually an ordinary monoid in the category of abelian groups: in other words, a [[ring]]!

# References #

* _Representable functors and operations on rings_, D. Tall and [[Gavin Wraith|G. Wraith]], Proc. London Math. Soc. (3), 1970

* _Plethystic algebra_, J. Borger and B. Wieland, Adv. Math, 2005

* _The Hunting of the Hopf Ring_, [[Andrew Stacey|A. Stacey]] and S. Whitehouse, [arXiv:0711:3722](http://arxiv.org/abs/0711.3722)

+-- {: .query}

[[Andrew Stacey]]: I changed the $V$ to $\mathcal{V}$ in line with the notation from _The Hunting of the Hopf Ring_.  Should there be a lab standard on fonts for categories, objects, functors, and the like?

_Toby_:  Based on [this discussion](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=37), '$\mathcal{V}$' is more likely to cause problems for people that haven\'t installed appropriate fonts.  (Not that I\'m changing it back, mind you ....)

[[John Baez]]: I hate 'fancy fonts for fancy gizmos', because they mainly serve to make gizmos seem fancy and intimidating.  That's why I had changed $\mathcal{V}$ to $V$.  I think I'll change it back again, just to annoy Andrew.  It's just a category with products, for god's sake!  Surely we can't insist on calligraphic font whenever we see one of those: must we say $\mathcal{Set}$?  (Yes, I'm being ornery.)

[[Andrew Stacey]]: Okay, okay, I surrender!  I'll even change back the ones that you missed.

But I reject the charge of 'fancy fonts for fancy gizmos'.  My intention was to use the change of fonts to represent the relationships between things.  Thus $a$ is an element of $A$ which is an object of $\mathcal{A}$ which is mapped by the functor $\mathfrak{A}$.  It's a bit like using $m,n$ for natural numbers.  Yes, we can and often do use $a$ for a natural number, but if I scan a page and see $n$ then I automatically think "natural number" (okay, maybe integer).  Since that is reasonably widespread, authors can use it to make their work clearer so that the reader doesn't continually have to go back to the first page to work out whether $A$ was the category or the object.  Of course we _can_ write

$$
\forall \delta \forall x \gt 0 \exists y \gt 0 : \forall \epsilon, |\epsilon - \delta| \lt y \implies |f(\epsilon) - f(\delta)| \lt x
$$

but, frankly, wouldn't you rather we didn't?

[[John Baez]]:  In lots of ordinary math the strategy of 'bigger fancier fonts for bigger fancier things' works fine: $a$ for an element of the set $A$ in the category $\mathcal{A}$.   But the problem is that in $n$-category theory everything is an object in some $n$-category... including every $n$-category, and every functor between them.   So, the idea of a clear hierarchy of two or three types of things, with bigger fancier things getting bigger fancier fonts, breaks down.  For example, while you might want to say

"Consider the functor $\mathfrak{A}: \mathcal{A} \to \mathcal{A}$..."

you'll often want to continue that sentence with 

"... and think of it as an object $\mathfrak{A} \in End(\mathcal{A})$.  Now, since $End(\mathcal{A}) \in MonCat$, it makes sense to equip $\mathfrak{A}$ with the structure of a monoid object, and we then call it a **monad**."

This is just a very simple example of the kind of fancy level-shifting that takes place.  And this level-shifting is _precisely the style of thinking that makes $n$-category theory so powerful_.

For this reason, at some point I decided Jim Dolan was very wise to put everything in the same font: it encourages mental flexibility.  I later impressed Ross Street greatly when I wrote on the blackboard "Consider a bicategory $x$."

Even though I'll be eternally proud of that moment, I think it can be good to use a couple of different fonts in a given discussion to help 'set the types' of the entities in question --- hence the term 'typesetting'.  But this sort of distinction is only helpful _locally_: it's not so good to demand _globally_ consistent typesetting.  Your big fancy algebraic theory $\mathcal{A}$ is likely to become someone else's puny little object $a$ in $FinProdCat$, and then $FinProdCat$ will become a puny little object in $Doctrines$, and so on.

[[Andrew Stacey]]: I take your point; I was aware that it would have been hard to continue further.  Whilst I have an old _Lettraset_ catalogue to draw on for blackboards, sadly it's not implemented in the STIX fonts.  But I would like to use the fonts we do have, and so Toby's point is more important that us squabbling over whether or not we should change $\mathcal{V}$ to $V$ or not. 

[[John Baez]]: I agree with that.  I guess some group of people should argue about whether most of our readers will have various fancy fonts installed... I think we should _not_ assume this.

[[Andrew Stacey]]: If we're going to take this sort of thing into account then we need it clear somewhere since otherwise those of us fortunate enough to have the correct fonts don't know what doesn't display so well on other, more limited, systems!

I did find it getting awkward in writing out the proof that a TW-monoid in abelian groups was a ring to talk of $A$ being an object of $V$.  I'd much rather have said $A$ is an object of $\mathcal{A}$.  So if we're allowed to use this sort of hierarchy locally, can I change it all back now?

[[John Baez]]: If you insist, but I don't like it: I don't think most reader will find the letter $V$ more 'awkward' than $\mathcal{A}$.  And more people will be able to read $V$ than $\mathcal{A}$.

[[Andrew Stacey]]: Linking this to your question above, for something like this where there is a fair amount of notation, what do you think of a "notation used in this page" section for easy reference?

[[John Baez]]: I don't think there's intrinsically more  notation in this subject compared to most subjects on the $n$Lab, or more need for fancy fonts.  I think that with this subject, as with almost any, it's possible to explain the material very nicely with only a little notation.  But that's a kind of pet peeve of mine: I think mathematicians tend to make their work hard to read by introducing more notation than necessary, and not reminding the reader about what it means frequently enough.  They like to build towers of thought that are beautiful in principle but not very user-friendly.

[[Andrew Stacey]]: firstly, when I was linking to your question above, I meant to the 'VV^c' question much higher.  It was awkward _not_ to use some notation for this category, but it wasn't clear to me that it merited a whole definition to itself.  An explanatory sentence is reasonable the first time that it is used, and maybe after a long period with no use, but one of the advantages of hyperlinks is that I could put a "Notation used in this page" section at the bottom, stick in:

* $VV^c$: the category of co-$V$-algebraic objects in $V$

and put a little hyperlink whenever it is used, something like $VV^c$$([notation](#notation)) (okay, that doesn't work as I haven't created the notation section); possibly with a little semi-quaver instead of the word "notation".

I completely agree with your peeve, but _no_ notation is as horrible as too much notation.  Notation should help and guide the reader through a complicated argument, never intruding but always easing the path.

If you take the Dolan principle to its extreme, we should just start the document at the letter $a$ and increase as we proceed.  Then the only thing that we have to keep track of is whether or not we have referred to something before or not.  Actually, if we combine this with the slogan "Do no evil" then we should _always_ use a new symbol and note where things are isomorphic.  Thus

$$
\forall a \forall b \gt c \exists d \gt e: \forall f, |g - h| \lt i \implies |j(k) - l(m)| \lt n
$$
where
$$
c \cong 0, e \cong 0, g \cong a, h \cong f, i \cong d, k \cong a, l \cong j, m \cong h, n \cong b
$$
(I think!)

[[John Baez]]: I never take any principle to extremes, not even this one.  I mainly just want to make life easy on people who read my stuff or hear my talks.   I think links to "notation used on this page" would be great when used _in addition_ to on-the-spot explanations of the notation when it's introduced, and occasional reminders.  I'm afraid however that most mathematicians would use these hyperlinks as an excuse to use more notation, when 99% of them should spend time figuring out how to use less.  

Anyway, I think I'm starting to repeat myself, so I'll stop.

[[David Roberts]]: I find myself writing $X$ for a topological groupoid as well as a space, as the latter is one of the former, and I want to replace spaces with groupoids anyway. Ditto with functors (and eventually anafunctors, but that is a little trickier). The move to replace spaces by stacks, which is a good thing, seems to have that psychological barrier of people obeying the urge to call a stack a symbol in an unreadable font. Many-folds were once tricky... 

That's my rant over

_Toby_:  Just stepping in to clear the air about what Jim Dolan actually does.  Here is an example, not as he would write it, but using symbols as he would write them on a blackboard:
> Let $C$ be a category.  Let $C_0$ and $C_1$ be objects of $C$.  Let $C_2$ be a morphism from $C_0$ to $C_1$.  ...
=--


[[!redirects Tall--Wraith monoid]]
[[!redirects Tall–Wraith monoid]]