An **inhabited set** or **occupied set** is a [[set]] that contains an element. (That is, it\'s a [[k-tuply monoidal n-category|0-tuply monoidal 0-category]].)

At least assuming [[classical logic]], this is the same thing as a set that is not [[empty set|empty]]. Usually inhabited sets are simply called 'non-empty', but the positive word 'inhabited' reminds us that this is the simpler notion, which emptiness is defined as the negation of.

The terms 'inhabited' and 'occupied' come from [[constructive mathematics]]. In constructive mathematics, a set that is not empty isn\'t necessarily inhabited, because [[double negation]] is nontrivial in [[intuitionistic logic]]. All the same, many constructive mathematicians use the old word 'non-empty' with the understanding that it *really* means inhabited.

An object $X$ of a [[topos]] is inhabited in the [[internal logic]] (or, one might say, "internally inhabited") if and only if it is **well-supported**, meaning that the unique map $X \to 1$ is an [[epimorphism]].  (The same is true in any [[regular category]], replacing "epimorphism" by [[regular epimorphism]].)  This is certainly true if $X$ has a [[global element]] $1\to X$, while the converse is true if $1$ is [[projective object|projective]], such as in a [[well-pointed topos]].  Some sources use "$X$ is inhabited" to mean that $X$ has a global element, which is not expressible in the internal language.  Others use the term "inhabited" only internally.  Regardless, a [[pointed object]] always means one _equipped with_ a global element $1\to X$, whether interpreted internally or externally.

## Discussion##

While writing this page, we had the following discussion about whether or not "$X$ is inhabited" in a topos should mean that $X$ has a [[global element]].

+--{.query}

_[[Mike Shulman|Mike]]_: I strongly disagree that "inhabited" means "has a global element" in a topos.  Intuitionistically, "$X$ is inhabited" means "there exists an $x\in X$" which when interpreted in the internal logic of a topos means that $X$ is well-supported.  By contrast, the property of having a global element is not expressible in the internal language at all.  "Inhabited" is also universally used in the topos-theoretic literature to mean well-supported.

_Toby_: Then what is the term for what I have called 'inhabited'? [At least one reference](www.dcs.kcl.ac.uk/technical-reports/papers/tr97-04.ps.gz) uses the term that way; I see (through Google) that it\'s used in the Elephant, but it\'s not in the index and I haven\'t managed to tell what the definition is. Certainly I\'m not in the position to make a good literature search.

_Mike_: On p618 of the Elephant he uses "inhabited" to mean "there exists an $x\in X$" in the internal language.  What do you think about the change I made above?

_Toby_: I certainly can\'t disagree with any of the statements there.

I would like us to be a bit bolder with the terminology if it\'s safe and useful (neither of which condition has been established, of course). The Elephant has its share of terminological changes (like 'cartesian category' and 'cartesian morphism', which I remember got a lot of complaints on the categories mailing list), so I\'d want to check its references (which I can do later).

The wiki saved a previous version of your comments; since you changed it, I won\'t hold you to it. But having read it does inspire me to say that the terminology that comes naturally to me is indeed 'inhabited' for having a global element and 'internally inhabited' for being well supported; the latter seems at least as well justified as 'internal axiom of choice' (as used in, say, Mac Lane \& Moerdijk). That\'s just me, of course.

_Mike_: Yeah, I wasn't sure if it would (there seems to be a certain timeout within which multiple edits by the same person overwrite each other?).  I also wasn't sure if it was kosher to remove/change my comment; perhaps I shouldn't have.  The reason I changed it was that "inhabited" and "internally inhabited" did start to make a little sense.  My current feeling is that "inhabited" is a set-theoretic term, and as such should only be used in set-theoretic-like situations.  This includes (1) constructive set theory, (2) IHOL and hence the internal language of a topos, and (3) a well-pointed topos. If we are talking about an arbitrary topos, and it is not clear that our statements are to be interpreted in the internal logic, I would rather use "has a global element" and "is well-supported" since they are both unambiguous.

You are certainly right about the Elephant and terminology.  "Cartesian category," "prone morphism," and "effective regular category" are the ones that come to mind that seem to have been rejected by much of the categorical community.

_Mike_: Another thought: one could argue that just as a "ring" in a topos means a model of the theory of rings, and likewise for many other concepts, so should an "inhabited object" mean a model of the theory of inhabited objects, which is the same as a well-supported object.  Of course this fails for "projective object," but I don't think there is a "theory of projective objects," at least not one interpetable in the usual internal logic of a topos.  And I suppose maybe it fails for "choice object" too, although that probably depends on whether you formulate the theory of choice objects to be equipped with a choice function or merely assert that one exists.  Perhaps the literature is not very consistent in its use of "internally" or lack thereof.

_Toby_: I see 'inhabited' as just a convenient abbreviation of 'that has an element' (convenient enough that 'is inhabited' is still nicer than 'has an element'). So an inhabited object should naturally be an object with an element (a global element, that is; every object has a generalised element, and we must at least reproduce the situation in $\Set$). And after all, 'inhabited' is hardly more of a set-theoretic term than 'axiom of choice'! (^_^)

Maybe life would be simpler if we always internalised using the internal language, but there\'s a lot of precedent that we don\'t, probably because it\'s a lot easier not to. And anyway, that\'s what the word 'internalised' is for!

As for the timeout, I think that it\'s an hour, although I haven\'t timed it carefully. (It definitely exists.) I think that it\'s fine to remove or change old comments, certainly if they haven\'t been replied to, but one should be aware that they can still be read. (And if you\'re not sure if they can still be read, try 'See changes' or 'Back in time' below.)

_Mike_: Well, I think that I will continue using "has a global element" myself for clarity, but you've convinced me that it's not entirely unreasonable to use "is inhabited" to mean the same thing.  Though I reserve the right to reopen the discussion if we discover precendent to the contrary.  (-:

A different question, as you mentioned earlier, is whether it is useful.  How often do we want to talk about objects that have a global element?  We may frequently care about _pointed_ objects, which are _equipped_ with a global element, but there isn't any dispute about what to call those.

_Toby_: You\'ve got a good point there. Probably 'pointed object' and 'well-supported object' are the only really useful notions. Actually, I think that a lot of constructivists (the ones that are really think that mathematics should talk about *constructions*, like Bishop and Coquand) would say that an inhabited set and a pointed set are really the same thing. We can distinguish them, of course, by their morphisms (or even isomorphisms), but that doesn\'t mean that we need two words (just as we don\'t use two different words for metric spaces with, say, continuous maps between them and uniformly continuous maps bewteen them). So as you move towards my position, I move towards yours ....

_Mike_: Does that mean you might be satisfied with the way it's written now?  (I added a note about pointed objects.)

_Toby_: Yes, I\'m happy now for now.

=--


[[!redirects occupied set]]
[[!redirects well-supported object]]