An **inhabited set** or **occupied set** is a [[set]] that contains an element. (That is, it\'s a [[k-tuply monoidal n-category|0-tuply monoidal 0-category]].)

At least assuming [[classical logic]], this is the same thing as a set that is not [[empty set|empty]]. Usually inhabited sets are simply called 'non-empty', but the positive word 'inhabited' reminds us that this is the simpler notion, which emptiness is defined as the negation of.

The terms 'inhabited' and 'occupied' come from [[constructivism]]. In constructive mathematics, a set that is not empty isn\'t necessarily inhabited, because [[double negation]] is nontrivial in [[intuitionistic logic]]. All the same, many constructive mathematicians use the old word 'non-empty' with the understanding that it *really* means inhabited.

In a [[topos]] (or any category with a [[terminal object]] $1$), an object $X$ is **inhabited** if it has a [[global element]], that is a morphism $1 \to X$. The object $X$ is **well-supported** if the unique map $X \to 1$ is an [[epimorphism]]. Every inhabited object is well-supported, and every well-supported object in a [[well-pointed topos]] (or any category where $1$ is [[projective object|projective]]) is inhabited.

+--{.query}

_[[Mike Shulman|Mike]]_: I strongly disagree that "inhabited" means "has a global element" in a topos.  Intuitionistically, "$X$ is inhabited" means "there exists an $x\in X$" which when interpreted in the internal logic of a topos means that $X$ is well-supported.  By contrast, the property of having a global element is not expressible in the internal language at all.  "Inhabited" is also universally used in the topos-theoretic literature to mean well-supported.

_Toby_: Then what is the term for what I have called 'inhabited'? [At least one reference](www.dcs.kcl.ac.uk/technical-reports/papers/tr97-04.ps.gz) uses the term that way; I see (through Google) that it\'s used in the Elephant, but it\'s not in the index and I haven\'t managed to tell what the definition is. Certainly I\'m not in the position to make a good literature search.

_Mike_: How about "has a global element?"  I would argue that the reference you give uses the term incorrectly.  I don't know where it's defined in the Elephant, but on p618 you can see that it means "there exists an $x\in X$" in the internal language.

You yourself wrote that in constructive mathematics, an inhabited/occupied set is one that contains an element.  Given that, it makes no sense to me to use "inhabited" in a topos to mean "has a global element," which is not expressible in the internal language.  Or would you want to distinguish between "inhabited" and "internally inhabited"?  I would argue that the notion of "inhabited" really only makes sense in a set-like or well-pointed situation, and so it should really only be interpreted internally.

=--
