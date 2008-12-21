A set $S$ equipped with an __apartness relation__ is a [[category]] (with $S$ as the set of objects) [[enriched category|enriched]] over the [[cartesian category]] $(-1)\Cat^\op$, that is the [[opposite category|opposite]] of the [[poset]] of $(-1)$-[[(-1)-category|categories]] (truth values), made into a [[monoidal category]] using [[disjunction]]. By the law of [[excluded middle]] (which says that $(-1)\Cat$ is self-dual under [[negation]]), this is equivalent to equipping $S$ with an [[equivalence relation]] (which makes $S$ a category enriched over the cartesian category of $(-1)$-categories *itself*). But in constructive mathematics (or interpreted [[internalization|internally]]), it is a richer concept with a topological flavour.

# Discussion

_[[Urs Schreiber|Urs]] says_: What you say at the entry [[vector space]] about the relation between apartness relations and topology and the continuum sounds very interesting. It would be nice if you could move these comments here and maybe flesh them out a little. Because, while it sounds interesting, I don't yet understand what you are saying!

(_[[Toby Bartels|Toby]] replies_: I will try to write a bit about the topological ideas that come up. But keep in mind that classically it is all trivial, unless you rephrase it internal to some more general notion of category than a boolean topos, and these things are not normally so phrased.

_[[Urs Schreiber|Urs]] replies to the reply:_ Okay, I'll keep it in mind. But I am still interested! :-)

)

I already have problems with the above definition. When you say "coproduct" do you mean to equip $\{true, false\}$ with the monoidal structure given by logical OR? This is the only meaning I can give this word here, but a category enriched over $(\{true, false\},\otimes = OR)$ seems necessarily  to be an indiscrete groupoid over its set of objects. (Because $hom(a,a) = true$ for all objects $a$ and then $hom(a,b) = hom(a,a) OR hom(a,b) = true$, too, for all $b$.)

(_[[Toby Bartels|Toby]] replies_: To begin with, I defined it incorrectly; the trouble with these slick category-theoretic definitions is that a small error makes things completely messed up! I rephrased it quite a bit, but the key point is the new word 'opposite'. That said, your analysis of even my original definition is unsound; keep in mind that the unit of disjunction is *false*.)

I am also not sure in which sense you refer to the law of the excluded middle. Should we maybe more generally say that the 0-category of (-1)-categories internal to a given topos $T$ is the subobject classifier, $(-1)Cat := \Omega$?

(_[[Toby Bartels|Toby]] replies_: Yes, that is correct; $(-1)\Cat = \Omega$. Even when $T := \Set$, you have $(-1)\Cat = \{\top, \bot\}$ *only* if you believe excluded middle, which constructivists do not. Thus, constructivists will talk about apartness relations in $\Set$, while a classical mathematician will have to put the discussion internal to $T$ to get nontrivial results.

_[[Urs Schreiber|Urs]] replies to the reply:_ I like this statement "$(-1)\Cat = \Omega$". Would we also want to say $(-2)Cat = \{1 \stackrel{\top}{\to} \Omega\}$?

)

## Constructive mathematics

_[[Urs Schreiber|Urs]] asks_: Can you explicitly specify for me the topos which describes Sets as viewed by constructivists? Or is that the wrong question to ask?

_[[Toby Bartels|Toby]] replies_: It is the wrong question to ask. Constructivists believe that the category of sets is the category of sets; what more can they say? It is the classical mathematicians that go around making unjustifiable claims about this category, such as that it is boolean, or is a topos, or has choice.

Instead, the questions to ask are: What do constructivists believe about the category of sets? and What sort of category\'s internal logic serves as a model of constructivist reasoning? The first question asks what axioms to use as an [[ETCS]]-like foundation of mathematics if you are a constructivist; the second question asks how a classical mathematician can understand constructive mathematics by interpreting it as a discussion of internalisation. Note that these are different questions; even for classical mathematics, the answers to the questions are different. (In particular, everybody agrees that the category of sets is [[well-pointed topos|well-pointed]], but classical mathematicians cannot understand constructive mathematics by doing it internal to a well-pointed topos, since *they* can prove that such a topos must be boolean!)

What\'s more, the answers to these questions depend on what constructivists you\'re talking about! A simple answer, good for many purposes, is that a constructivist believes that the category of sets is a well-pointed topos (whereas a classical mathematician believes that it\'s a well-pointed topos satisfying choice). This is actually a fairly strong statement that many constructivists would disagree with (and then again, it is too weak for some reasoning that some constructivists would accept), but at least it does not imply excluded middle. Correspondingly, a simple answer for what kind of category to internalise constructive mathematics in is that it should be done internal to an arbitrary topos; again, this allows one to produce proofs that many constructivists would dispute, but at least not any proof of excluded middle.

I know, I know, you want to know *which* topos! But do you see how unfair this question is? A constructivist might as well ask you which topos to interpret classical mathematics in, and you would reply 'Why, $\Set$, of course!'. But this would tell the constructivist nothing, since the constructivist is also working with $\Set$. What you need to tell the constructivist is that you assume that $\Set$ has choice; *then* the constructivist can follow your reasoning. To be sure, there are various specific toposes (the effective topos, the realisability topos, the category of sheaves on the real line, etc) that are useful for understanding some aspects of constructive reasoning, but you can\'t point to any of them and say 'There, *that\'s* the topos that constructive mathematics is done in.', because none of those toposes is the category of sets.

_[[Mike Shulman|Mike]] comments_: While I agree with everything Toby has said, I think there is nevertheless a particular topos in which a classical mathematician could work internally to reproduce constructive mathematics: the [[free topos]].  Of course, this is something of a cheat, since the free topos is defined just so that the only statements true in it are those which are intuitionistically provable, so it's not particularly helpful to the classical mathematician trying to understand the intuitionist.  Neither do I mean that an intuitionist would claim that the free topos _is_ the category of sets.  But it nevertheless encapsulates everything the intuitionist can _prove_ about the category of sets.

=--  