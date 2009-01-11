An **inhabited set** or **occupied set** is a [[set]] that contains an element. (That is, it\'s a [[k-tuply monoidal n-category|0-tuply monoidal 0-category]].)

At least assuming [[classical logic]], this is the same thing as a set that is not [[empty set|empty]]. Usually inhabited sets are simply called 'non-empty', but the positive word 'inhabited' reminds us that this is the simpler notion, which emptiness is defined as the negation of.

The terms 'inhabited' and 'occupied' come from [[constructivism]]. In constructive mathematics, a set that is not empty isn\'t necessarily inhabited, because [[double negation]] is nontrivial in [[intuitionistic logic]]. All the same, many constructive mathematicians use the old word 'non-empty' with the understanding that it *really* means inhabited.

An object $X$ of a [[topos]] is inhabited in the [[internal logic]] (or, one might say, "internally inhabited") if and only if it is **well-supported**, meaning that the unique map $X \to 1$ is an [[epimorphism]].  (The same is true in any [[regular category]], replacing "epimorphism" by [[regular epimorphism]].)  This is certainly true if $X$ has a [[global element]] $1\to X$, while the converse is true if $1$ is [[projective object|projective]], such as in a [[well-pointed topos]].  Some sources use "$X$ is inhabited" to mean that $X$ has a global element, which is not expressible in the internal language.  Others use the term "inhabited" only internally.

+--{.query}

_[[Mike Shulman|Mike]]_: I strongly disagree that "inhabited" means "has a global element" in a topos.  Intuitionistically, "$X$ is inhabited" means "there exists an $x\in X$" which when interpreted in the internal logic of a topos means that $X$ is well-supported.  By contrast, the property of having a global element is not expressible in the internal language at all.  "Inhabited" is also universally used in the topos-theoretic literature to mean well-supported.

_Toby_: Then what is the term for what I have called 'inhabited'? [At least one reference](www.dcs.kcl.ac.uk/technical-reports/papers/tr97-04.ps.gz) uses the term that way; I see (through Google) that it\'s used in the Elephant, but it\'s not in the index and I haven\'t managed to tell what the definition is. Certainly I\'m not in the position to make a good literature search.

_Mike_: On p618 of the Elephant he uses "inhabited" to mean "there exists an $x\in X$" in the internal language.  What do you think about the change I made above?

_Toby_: I certainly can\'t disagree with any of the statements there.

I would like us to be a bit bolder with the terminology if it\'s safe and useful (neither of which condition has been established, of course). The Elephant has its share of terminological changes (like 'cartesian category' and 'cartesian morphism', which I remember got a lot of complaints on the categories mailing list), so I\'d want to check its references (which I can do later).

The wiki saved a previous version of your comments; since you changed it, I won\'t hold you to it. But having read it does inspire me to say that the terminology that comes naturally to me is indeed 'inhabited' for having a global element and 'internally inhabited' for being well supported; the latter seems at least as well justified as 'internal axiom of choice' (as used in, say, Mac Lane \& Moerdijk). That\'s just me, of course.

=--