A set $S$ equipped with an __apartness relation__ is a [[category]] (with $S$ as the set of objects) [[enriched category|enriched]] over the [[cartesian category]] $(-1)\Cat^\op$, that is the [[opposite category|opposite]] of the [[poset]] of $(-1)$-[[(-1)-category|categories]] (truth values), made into a [[monoidal category]] using [[disjunction]]. By the law of [[excluded middle]] (which says that $(-1)\Cat$ is self-dual under [[negation]]), this is equivalent to equipping $S$ with an [[equivalence relation]] (which makes $S$ a category enriched over the cartesian category of $(-1)$-categories *itself*). But in constructive mathematics (or interpreted [[internalization|internally]]), it is a richer concept with a topological flavour.

+--{.query}

_[[Urs Schreiber|Urs]] says_: What you say at the entry [[vector space]] about the relation between apartness relations and topology and the continuum sounds very interesting. It would be nice if you could move these comments here and maybe flesh them out a little. Because, while it sounds interesting, I don't yet understand what you are saying!

(_[[Toby Bartels|Toby]] replies_: I will try to write a bit about the topological ideas that come up. But keep in mind that classically it is all trivial, unless you rephrase it internal to some more general notion of category than a boolean topos, and these things are not normally so phrased.)

I already have problems with the above definition. When you say "coproduct" do you mean to equip $\{true, false\}$ with the monoidal structure given by logical OR? This is the only meaning I can give this word here, but a category enriched over $(\{true, false\},\otimes = OR)$ seems necessarily  to be an indiscrete groupoid over its set of objects. (Because $hom(a,a) = true$ for all objects $a$ and then $hom(a,b) = hom(a,a) OR hom(a,b) = true$, too, for all $b$.)

(_[[Toby Bartels|Toby]] replies_: To begin with, I defined it incorrectly; the trouble with these slick category-theoretic definitions is that a small error makes things completely messed up! I rephrased it quite a bit, but the key point is the new word 'opposite'. That said, your analysis of even my original definition is unsound; keep in mind that the unit of disjunction is *false*.)

I am also not sure in which sense you refer to the law of the excluded middle. Should we maybe more generally say that the 0-category of (-1)-categories internal to a given topos $T$ is the subobject classifier, $(-1)Cat := \Omega$?

(_[[Toby Bartels|Toby]] replies_: Yes, that is correct; $(-1)\Cat = \Omega$. Even when $T := \Set$, you have $(-1)\Cat = \{\top, \bot\}$ *only* if you believe excluded middle, which constructivists do not. Thus, constructivists will talk about apartness relations in $\Set$, while a classical mathematician will have to put the discussion internal to $T$ to get nontrivial results.)

=--