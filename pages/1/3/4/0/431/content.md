# Origins and schools #

During the "[[foundations|foundational]] crisis" in mathematics around the beginning of the 20th century, a number of mathematicians espoused philosophies that are generally grouped together and labeled **constructivist**. The common feature of these philosophies was a rejection of axioms and principles of logic that lead to nonconstructive proofs.  There was much talk at the time about potential vs absolute infinity, but from an axiomatic perspective, it turns out that (if one stops short of finitism) the two main culprits are
* the [[axiom of choice]] and
* the principle of [[excluded middle]].

Thus, constructivists (including many still active today) reject proofs that make use of either of these.  (In fact, it was realized in 1975 by Diaconescu that the axiom of choice implies the principle of excluded middle; excluded middle is the 'finitely-indexed axiom of choice'.)

There are, however, differences among constructivists as well.

* Some, like Errett Bishop, simply remove choice and excluded middle from classical mathematics with nothing to replace them.  However, this makes it difficult to define a satisfactory notion of continuous function, even $R \to R$; see (Waaldijk 2003).

* Others add "non-classical" axioms which contradict choice or excluded middle, but which are consistent in their absence, such as "all total functions $R \to R$ are continuous" (the "intuitionistic" school of L. E. J. Brouwer) or "all partial functions $N \to N$ are computable" (the "Russian" school of Markov, also called "constructive recursive analysis").

* Most accept weaker versions of choice, such as [[countable choice]] or even [[dependent choice]], but the school of Fred Richman rejects even these; see (Richman 2000).  [[Toby Bartels]] argues that the intuition behind accepting these justifies the (stronger) axiom [[COSHEP]] (the category of sets has enough projectives).

* Still others, following Weyl, go even further and refuse to allow "impredicative" constructions; see [[predicativism]].  Most of the work done by the schools of Brouwer, Bishop, and Markov (but not Richman) is also predicative, even though those founders were not adamant about it; as a result, predicativism often appears in the foundations of constructive mathematics (in particular, in those of Aczel and Martin-L&#246;f, but not those of Friedman or Coquand).

* Very extreme constructivists, like Doron Zeilberger, reject the existence of infinite sets; see [[finitism]].  (Kronecker, the 'father of constructivism', is often considered a finitist, but as he came before the foundational crisis, it is difficult to classify him accurately.)  Ironically, this means that excluded middle and choice, as such, may become acceptable, or even true.  (Even constructivists believe that they are true in the topos [[FinSet]] of finite sets&#8212;although see below regarding the constructive meaning of "finite".)

* The most extreme position of all is to deny even the existence of very large finite sets.  This is called [[ultrafinitism]].  According to [Wikipedia](http://en.wikipedia.org/wiki/Ultrafinitism), "even constructivists generally view [ultrafinitism] as unworkably extreme."

Many constructivists (like many classical mathematicians) believe in an absolute mathematical sense of "truth," and that in this sense choice and excluded middle are _not_ true (and may even be false).  To most mathematicians, this makes them seem quite strange.

+--{.query}

_Mike:_ What do you mean by "not true (and may even be false)?"  Are there constructivists who claim that "false" is distinct from "not true?"  The two are certainly the same in the constructive logic I'm familiar with.

_Toby_: Take Errett Bishop. In his analysis book, he says that a statement is true only if it has a proof, that various construtively invalid principles (like excluded middle) are not true, but carefully does not say that they are false because (he says) he makes no classically false claims. And then he claims to be a mathematical realist who believes in an absolute mathematical sense of truth. Clearly he can do this by distinguishing an object language and a metalanguage, and this interpretation is bolstered by his technical use of italicised 'not' in statements like 'Excluded middle is _not_ true.' or 'Exercise: Construct a surjective function which is _not_ onto \[by which he means split epic\].'. Of course, even a classical mathematician can make this distinction, and many do by saying 'not constructively provable' where (setting aside the difference in what the consider provable) Bishop would say '_not_ true'. Yet only a constructivist can claim that this is the final word on the matter, while the classical realist must be left wondering whether an undecidable proposition is *really* true or false.

I\'m not sure that I agree with Bishop. I\'m just trying to be true to his language and views. Probably I should just rewrite that paragraph. Certainly _some_ constructivists can refute excluded middle; Bishop can\'t, but he still claims that it is, in an objective sense, wrong.

=--

# Topos Theory #

With the invention of [[topos|topos theory]] in the second half of the 20th century, a new sort of constructivism arose.  It was observed (by Lawvere and others) that any topos with a [[natural numbers object]] has an [[internal logic]] which is powerful enough to interpret most of mathematics, but that this logic in general fails to satisfy choice and excluded middle.  This meant that even for a mathematican who likes to use choice and excluded middle (and _a fortiori_ for one who believes them to be "true"), there is a reason to care about what can be proven without them, because only if a proof is constructive can it be interpreted in an arbitrary topos with NNO.

Even starting from a "completely classical" world of mathematics, many interesting toposes arise naturally (such as the category of [[sheaf|sheaves]] on any [[topological space]], or more generally any [[site]]) whose internal logic is not classical.  Then by internal (constructive) reasoning in such a topos, one can prove various useful facts, which can then be reinterpreted as external statements about the behavior of the topos itself.  (Some examples would be nice.)

By now it is known that many of the non-classical axioms used by the early constructivists have natural models in particular toposes.  For instance, in the topos of sheaves on the real numbers $R$, it is true that "all functions $R \to R$ are continuous."  And in the [[effective topos]], it is true that "all functions $N\to N$ are computable."

However, there are no non-classical (or classical) axioms beyond "pure constructivism" that are true in _all_ toposes with NNO.  In particular, there is a [[free topos]] with NNO such that a statement is true in the free topos precisely when it is provable in pure (Richman-school) constructive mathematics.  This means that for an argument to apply in all toposes, even mild assumptions such as countable or dependent choice are unacceptable.  However, topos theory has also provided ideas that solve many of the problems with pure constructivism.  For example, a well-behaved notion of "continuous function" can be recovered by using [[locale|locales]] instead of topological spaces.

# Some features of constructive mathematics #

## Rephrasing of classical ideas ##

Sometimes, all that is necessary to make a piece of mathematics constructive is careful use of language.  It is common in classical mathematics to define things with an unnecessary amount of negation.  This doesn't work so well constructively, since a statement can be not false without being true, but we can sometimes do perfectly well by just removing unnecessary [[double negation]]s.

For example, classically one often speaks about "nonempty" sets, meaning a set which "does _not_ have _no_ elements."  Constructively it is much better to say that a set "<i>does</i> have at least one element"; constructivists often call such a set [[inhabited set|inhabited]] or _occupied_ to remind themselves that it is a "positive" notion to replace the negative one of "nonempty". Others continue to use the word "non-empty" but understand it as a term of art that really means "occupied".

## Bifurcation of notions ##

On the other hand, differences in axiomatization or definition that make no difference classically can result in actual differences in behavior in a topos.  Therefore, classically equivalent notions often "bifurcate" (or "trifurcate" or worse) into multiple inequivalent constructive ones.  This tends to happen whenever a concept involves _negation_ and, to a lesser degree, _disjunction_ and _existential quantification_.  In some cases there is a "correct" constructive version of the definition, although it may take some thought to uncover it, but in many cases more than one of the resulting concepts is important and useful.  For example:

* There are multiple inequivalent constructive definitions of a [[field]], because of the axioms "every _nonzero_ element has an inverse" and $0 \neq 1$.

* Without excluded middle or countable choice, the Dedekind [[real numbers]] and the Cauchy real numbers are no longer the same.  From a topos-theoretic viewpoint, the Dedekind reals are usually the "correct" notion to study.  See also (Bridges et al, 1998).

+--{.query}

_Mike_: Is excluded middle really necessary for this?  I thought that countable choice was enough.  I know that they are the same in the effective topos, which satisfies countable choice but is not Boolean.

_Toby_: Ah, this is the old problem that English doesn\'t easily distinguish $\neg(p \wedge q)$ from $\neg{p} \wedge \neg{q}$. You\'re not mistaken.

=--

* There are at least three different constructive notions of [[ordinal number]]; see (Taylor 1996) and (Joyal-Moerdijk 1995).

* Without the axiom of choice, [[functor|functors]] and [[anafunctor|anafunctors]] become distinct, and often the latter is more appropriate; see (Makkai, 1996).

* Perhaps most disturbingly of all to the classical mathematician, one must distinguish between _finite sets_ (those equipped with a bijection to $\{1,\dots, n\}$ for some natural number $n$), _subfinite sets_ (those equipped with an injection from some finite set), _finitely indexed sets_ (those equipped with a surjection from some finite set, also called _Kuratowski-finite sets_ or, confusingly, _subfinite sets_), and even _subfinitely indexed sets_.  However, in practice it is usually either the finite sets or the K-finite sets that are important, and with practice a little bit of thought suffices to show which is the relevant concept.


# References #

Douglas Bridges, Fred Richman, and Peter Schuster (1998). A weak countable choice principle. Available from [Fred Richman's Documents](http://www.math.fau.edu/Richman/HTML/DOCS.HTM).

Michael Makkai (1996). [Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/).

Fred Richman (2000). [Constructive mathematics without choice](http://www.math.fau.edu/Richman/HTML/nsf.htm).

Paul Taylor (1996). Intuitionistic Sets and Ordinals. Available (with several other references) at [Induction, recursion, replacement and the ordinals](http://www.PaulTaylor.EU/ordinals/index.php).

Joyal, A. and Moerdijk, I. (1995).  Algebraic set theory.

Frank Waaldijk (2003). [on the foundations of constructive mathematics - especially in relation to the theory of continuous functions](http://home.hetnet.nl/~sufra/foundations%20of%20constructive%20mathematics.pdf) (PDF).

# Discussion #

This discussion originally took place at [[apartness relation]]:

+--{.query}

_[[Urs Schreiber|Urs]] asks_: Can you explicitly specify for me the topos which describes Sets as viewed by constructivists? Or is that the wrong question to ask?

_[[Toby Bartels|Toby]] replies_: It is the wrong question to ask. Constructivists believe that the category of sets is the category of sets; what more can they say? It is the classical mathematicians that go around making unjustifiable claims about this category, such as that it is boolean, or is a topos, or has choice.

Instead, the questions to ask are: What do constructivists believe about the category of sets? and What sort of category\'s internal logic serves as a model of constructivist reasoning? The first question asks what axioms to use as an [[ETCS]]-like foundation of mathematics if you are a constructivist; the second question asks how a classical mathematician can understand constructive mathematics by interpreting it as a discussion of internalisation. Note that these are different questions; even for classical mathematics, the answers to the questions are different. (In particular, everybody agrees that the category of sets is [[well-pointed topos|well-pointed]], but classical mathematicians cannot understand constructive mathematics by doing it internal to a well-pointed topos, since *they* can prove that such a topos must be boolean!)

What\'s more, the answers to these questions depend on what constructivists you\'re talking about! A simple answer, good for many purposes, is that a constructivist believes that the category of sets is a well-pointed topos (whereas a classical mathematician believes that it\'s a well-pointed topos satisfying choice). This is actually a fairly strong statement that many constructivists would disagree with (and then again, it is too weak for some reasoning that some constructivists would accept), but at least it does not imply excluded middle. Correspondingly, a simple answer for what kind of category to internalise constructive mathematics in is that it should be done internal to an arbitrary topos; again, this allows one to produce proofs that many constructivists would dispute, but at least not any proof of excluded middle.

I know, I know, you want to know *which* topos! But do you see how unfair this question is? A constructivist might as well ask you which topos to interpret classical mathematics in, and you would reply 'Why, $\Set$, of course!'. But this would tell the constructivist nothing, since the constructivist is also working with $\Set$. What you need to tell the constructivist is that you assume that $\Set$ has choice; *then* the constructivist can follow your reasoning. To be sure, there are various specific toposes (the effective topos, the realisability topos, the category of sheaves on the real line, etc) that are useful for understanding some aspects of constructive reasoning, but you can\'t point to any of them and say 'There, *that\'s* the topos that constructive mathematics is done in.', because none of those toposes is the category of sets.

_Mike comments_: While I agree with everything Toby has said, I think there is nevertheless a particular topos in which a classical mathematician could work internally to reproduce constructive mathematics: the [[free topos]]. Of course, this is something of a cheat, since the free topos is defined just so that the only statements true in it are those which are intuitionistically provable, so it's not particularly helpful to the classical mathematician trying to understand the intuitionist. Neither do I mean that an intuitionist would claim that the free topos *is* the category of sets. But it nevertheless encapsulates everything the intuitionist can *prove* about the category of sets.

_Toby replies_: OK, that's a good point, Mike. Similarly, one can understand the classical mathematician by working in the free boolean topos (or rather, the free topos-with-choice, although I'm not entirely certain that this exists). But classical mathematicians don't believe that this topos *is* the category of sets either. (Indeed, to assume that it is probably amounts to something like the axiom of constructibility. $\langle$insert standard disclaimer that 'constructible' $\neq$ 'constructive'.$\rangle$).

_Mike 2-replies_: Actually, I don't think that asserting that the free boolean topos is the category of sets has anything to do with the axiom of constructibility.  On the one hand, since the axiom of constructibility is not provable from ZFC, there is no reason for it to be true in any free topos (except the "free topos satisfying the axiom of constructibility," to whatever extent that exists).  On the other hand, any free topos (on a countable theory) is countable, so there are many models of ZFC + constructibility that are not the free boolean topos.

I have been trying for some time to figure out the "categorical meaning" of the axiom of constructibility, but I have so far mostly failed.  It seems to be very closely tied to membership-based set theory.

_Toby_: OK, forget I said anything about constructibilty.

=--