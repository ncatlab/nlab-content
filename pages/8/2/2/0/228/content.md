A set equipped with an __apartness relation__ is an [[enriched category]] over the [[monoidal category]] of $(-1)$-[[(-1)-category|categories]] under the [[coproduct]]. By the law of [[excluded middle]], this is equivalent to the same set with an [[equivalence relation]] (which is a category enriched over the monoidal category of $(-1)$-categories under the *[[product]]*). But in constructive mathematics, it is a richer concept with a topological flavour.

+--{.query}

_[[Urs Schreiber|Urs]] says_: What you say at the entry [[vector space]] about the relation between apartness relations and topology and the continuum sounds very interesting. It would be nice if you could move these comments here and maybe flesh them out a little. Because, while it sounds interesting, I don't yet understand what you are saying!

I already have problems with the above definition. When you say "coproduct" do you mean to equip $\{true, false\}$ with the monoidal structure given by logical OR? This is the only meaning I can give this word here, but a category enriched over $(\{true, false\},\otimes = OR)$ seems necessarily  to be an indiscrete groupoid over its set of objects. (Because $hom(a,a) = true$ for all objects $a$ and then $hom(a,b) = hom(a,a) OR hom(a,b) = true$, too, for all $b$.)

I am also not sure in which sense you refer to the law of the excluded middle. Should we maybe more generally say that the 0-category of (-1)-categories internal to a given topos $T$ is the subobject classifier, $(-1)Cat := \Omega$?

=--