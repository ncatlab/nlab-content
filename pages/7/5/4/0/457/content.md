An **inhabited set** or **occupied set** is a [[set]] that contains an element. (That is, it\'s a [[k-tuply monoidal n-category|0-tuply monoidal 0-category]].)

At least assuming [[classical logic]], this is the same thing as a set that is not [[empty set|empty]]. Usually inhabited sets are simply called 'non-empty', but the positive word 'inhabited' reminds us that this is the simpler notion, which emptiness is defined as the negation of.

The terms 'inhabited' and 'occupied' come from [[constructivism]]. In constructive mathematics, a set that is not empty isn\'t necessarily inhabited, because [[double negation]] is nontrivial in [[intuitionistic logic]]. All the same, many constructive mathematicians use the old word 'non-empty' with the understanding that it *really* means inhabited.

In a [[topos]] (or any category with a [[terminal object]] $1$), an object $X$ is **inhabited** if it has a [[global element]], that is a morphism $1 \to X$. The object $X$ is **well-supported** if the unique map $X \to 1$ is an [[epimorphism]]. Every inhabited object is well-supported, and every well-supported object in a [[well-pointed topos]] (or any category where $1$ is [[projective object|projective]]) is inhabited.

+--{.query}

_[[Mike Shulman|Mike]]_: I strongly disagree that "inhabited" means "has a global element" in a topos.  Intuitionistically, "$X$ is inhabited" means "there exists an $x\in X$" which when interpreted in the internal logic of a topos means that $X$ is well-supported.  By contrast, the property of having a global element is not expressible in the internal language at all.  "Inhabited" is also universally used in the topos-theoretic literature to mean well-supported.

=--
