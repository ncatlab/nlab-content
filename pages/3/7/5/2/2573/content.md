## Idea

The axiom of replacement is one of the 'strong' axioms of [[set theory]].  It is not necessary for formalising 'ordinary' mathematics and does not hold in such basic systems as [[ETCS]].  It is necessary, however, whenever [[recursion|recursively]] constructing a set that is 'larger' than any set known before.

There are many variations on the axiom (which is actually an axiom *schema* in most systems), with names based on 'replacement' and 'collection'.


## Statements

In general, the axiom applies to a binary [[relation]] that relates elements of one [[set]] $A$ to arbitrary sets.  However, we do *not* expect that the relation itself be an object in the theory; really, this is an axiom schema with one axiom for every binary [[predicate]] of the proper form.  We will write it $\phi(x,Y)$, where $x$ stands for an elment of $A$ and $Y$ stands for any set.  (Note that there may well be other free variables in the predicate.)

Generally, $\phi$ will need to be an [[entire relation]] for the axiom to apply; that is, the axiom has as a hypothesis that, for every $x \in A$, there is some $Y$ such that $\phi(x,Y)$ holds.  In versions called 'replacement' instead of 'collection', $\phi$ also needs to be [[functional relation|functional]]; that is, the axiom has the hypothesis that, for every $x \in A$, there is a *unique* $Y$ such that $\phi(x,Y)$ holds.  Thus, most of the 'replacement' versions only make sense if the language has a notion of [[equality]] of sets.

So much for the hypothesis of the axiom; the conclusion asserts the existence of a [[family of sets]] to which appropriate $Y$s belong.  In a material set theory, we can simply state the existence of set $\mathcal{F}$ such that certain $Y \in \mathcal{F}$.  In a structural set theory, we state the existence of an index set $I$, a total set $E$, and a function $f\colon E \to I$ such that each [[fibre]] $f^*(x)$ for $x \in I$ is equal to (or at least isomorphic to) certain $Y$.  (Often we can take $I$ to be $A$, but that does not come into the statement of the axioms.)

...


[[!redirects axiom of collection]]

category: foundational axiom