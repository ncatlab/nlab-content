Broadly speaking, __constructive mathematics__ is mathematics done without the principle of [[excluded middle]] (or other principles, such as the full [[axiom of choice]], that imply it).  Sometimes one adds further restrictions or alternatively adds axioms that contradict excluded middle but are otherwise consistent.

__Constructivism__ is the philosophy that such mathematics is useful, or (more strongly) that non-constructive mathematics is wrong.

## Origins and schools ##

During the "[[foundations|foundational]] crisis" in mathematics around the beginning of the 20th century, a number of mathematicians espoused philosophies that are generally grouped together and labeled **constructivist**. The common feature of these philosophies was a rejection of axioms and principles of logic that lead to nonconstructive proofs.  There was much talk at the time about potential vs absolute infinity, but from an axiomatic perspective, it turns out that (if one stops short of finitism) the two main culprits are
* the [[axiom of choice]] and
* the principle of [[excluded middle]].

Thus, constructivists (including many still active today) reject proofs that make use of either of these.  (In fact, it was realized in 1975 by Diaconescu that the axiom of choice implies the principle of excluded middle.  Excluded middle is precisely the "finitely indexed" axiom of choice; see [[excluded middle]] for a proof.)

There are, however, differences among constructivists as well.

* Some, like Errett Bishop, simply remove choice and excluded middle from classical mathematics with nothing to replace them.  However, this makes it difficult to define a satisfactory notion of continuous function, even $R \to R$; see (Waaldijk 2003).

* Others add "non-classical" axioms which contradict choice or excluded middle, but which are consistent in their absence, such as "all total functions $R \to R$ are continuous" (the "intuitionistic" school of L. E. J. Brouwer) or "all partial functions $N \to N$ are computable" (the "Russian" school of Markov, also called "constructive recursive analysis").

* Most accept weaker versions of choice, such as [[countable choice]] or even [[dependent choice]], but the school of Fred Richman rejects even these; see (Richman 2000).  [[Toby Bartels]] argues that the intuition behind accepting these justifies the (stronger) axiom [[COSHEP]] (the category of sets has enough projectives).

* Still others, following Weyl, go even further and refuse to allow "impredicative" constructions; see [[predicative mathematics]].  Most of the work done by the schools of Brouwer, Bishop, and Markov (but not Richman) is also predicative, even though those founders were not adamant about it; as a result, predicativism often appears in the foundations of constructive mathematics (in particular, in those of Aczel and Martin-L&#246;f, but not those of Friedman or Coquand).

* Very extreme constructivists, like Doron Zeilberger, reject the existence of infinite sets; see [[finite mathematics]].  (Kronecker, the 'father of constructivism', is often considered a finitist, but as he came before the foundational crisis, it is difficult to classify him accurately.)  Ironically, this means that excluded middle and choice, as such, may become acceptable, or even true.  (Even constructivists believe that they are true in the topos [[FinSet]] of [[finite set]]s.)

* The most extreme position of all is to deny even the existence of very large finite sets.  This is called [[finite mathematics|ultrafinitism]].  According to [Wikipedia](http://en.wikipedia.org/wiki/Ultrafinitism) (to be fair, in an edit originally made by our own [[Toby Bartels]]), "even constructivists generally view \[ultrafinitism\] as unworkably extreme."

Many constructivists (like many classical mathematicians) believe in an absolute mathematical sense of "truth," and that in this sense choice and excluded middle are simply _wrong_. (Some constructivists, using classically false axioms, can even refute them; others merely claim that no possible correct reasoning could ever prove them.  See "Truth versus assertability," below.) To most mathematicians, this makes them seem quite strange.


## Topos Theory ##

With the invention of [[topos|topos theory]] in the second half of the 20th century, a new sort of constructivism arose.  It was observed (by Lawvere and others) that any topos with a [[natural numbers object]] has an [[internal logic]] which is powerful enough to interpret most of mathematics, but that this logic in general fails to satisfy choice and excluded middle.  This meant that even for a mathematican who likes to use choice and excluded middle (and _a fortiori_ for one who believes them to be "true"), there is a reason to care about what can be proven without them, because only if a proof is constructive can it be interpreted in an arbitrary topos with NNO.

Even starting from a "completely classical" world of mathematics, many interesting toposes arise naturally (such as the category of [[sheaf|sheaves]] on any [[topological space]], or more generally any [[site]]) whose internal logic is not classical.  Then by internal (constructive) reasoning in such a topos, one can prove various useful facts, which can then be reinterpreted as external statements about the behavior of the topos itself.  (Some examples would be nice.)

By now it is known that many of the non-classical axioms used by the early constructivists have natural models in particular toposes.  For instance, in the topos of sheaves on the real numbers $R$, it is true that "all functions $R \to R$ are continuous."  And in the [[effective topos]], it is true that "all functions $N\to N$ are computable."

However, there are no non-classical (or classical) axioms beyond "pure constructivism" that are true in _all_ toposes with NNO.  In particular, there is a [[free topos]] with NNO such that a statement is true in the free topos precisely when it is provable in pure (Richman-school) constructive mathematics.  This means that for an argument to apply in all toposes, even mild assumptions such as countable or dependent choice are unacceptable.  However, topos theory has also provided ideas that solve many of the problems with pure constructivism.  For example, a well-behaved notion of "continuous function" can be recovered by using [[locale|locales]] instead of topological spaces.

## Some features of constructive mathematics ##

### Rephrasing of classical ideas ###

Sometimes, all that is necessary to make a piece of mathematics constructive is careful use of language.  It is common in classical mathematics to define things with an unnecessary amount of negation.  This doesn't work so well constructively, since a statement can be not false without being true, but we can sometimes do perfectly well by just removing unnecessary [[double negation]]s.

For example, classically one often speaks about "nonempty" sets, meaning a set which "does _not_ have _no_ elements."  Constructively it is much better to say that a set "<i>does</i> have at least one element"; constructivists often call such a set _[[inhabited set|inhabited]]_ or _occupied_ to remind themselves that it is a "positive" notion to replace the negative one of "nonempty". Others continue to use the word "non-empty" but understand it as a term of art that really means "inhabited".

### Bifurcation of notions ###

On the other hand, differences in axiomatization or definition that make no difference classically can result in actual differences in behavior in a topos.  Therefore, classically equivalent notions often "bifurcate" (or "trifurcate" or worse) into multiple inequivalent constructive ones.  This tends to happen whenever a concept involves _negation_ and, to a lesser degree, _disjunction_ and _existential quantification_.  In some cases there is a "correct" constructive version of the definition, although it may take some thought to uncover it, but in many cases more than one of the resulting concepts is important and useful.  For example:

* There are multiple inequivalent constructive definitions of a [[field]], because of the axioms "every _nonzero_ element has an inverse" and $0 \neq 1$.

* In pure constructive logic, the Dedekind [[real number]]s and the Cauchy real numbers need no longer coincide.  The Cauchy reals sit inside the Dedekind reals, but in general not every Dedekind real need be approximable by a _[[sequence]]_ of rationals.  From a topos-theoretic viewpoint, the Dedekind reals are usually the "correct" notion to study (although see also [[locale]]).  However, either excluded middle or countable choice suffices to ensure that every Dedekind real is a Cauchy real, and hence that the two notions coincide; see (Bridges et al, 1998) for details.

* There are at least three different constructive notions of [[ordinal number]]; see (Taylor 1996) and (Joyal-Moerdijk 1995).

* Without the axiom of choice, [[functor|functors]] and [[anafunctor|anafunctors]] become distinct, and often the latter is more appropriate; see (Makkai, 1996).

* Perhaps most disturbingly of all to the classical mathematician, one must distinguish between _finite sets_, _subfinite sets_, _finitely-indexed sets_, and even _subfinitely indexed sets_; see [[finite set]] for definitions.  However, in practice it is usually either finite or finitely-indexed sets that are important, and with practice a little bit of thought suffices to show which is the relevant concept.

### Negative translation ###

(Say something about how to interpret classical logic in constructive logic.)

### Truth versus assertability ###

Already in classical mathematics, there is a difference in saying that something is true and saying that something is provable. If you adopt ZFC because you believe it correct, then (assuming that you\'re aware of certain theorems) you believe that ZFC is consistent even though you also know that you cannot prove it so. In that case, you also believe that the continuum hypothesis is either true or false; you may or may not have an opinion on which it is, but in any case again you know that you cannot prove it either way.

A constructive mathematician can be even subtler. If you belong to the Bishop school, then you accept no classically false axioms, and anything that you can prove is valid also in classical mathematics. Even so, you can believe that the principle of excluded middle is false (even though, of course, you know that you cannot prove it false). So you can really confuse the classical mathematicians by saying, on the one hand, that they can safely accept all of your proofs as valid, and then saying, on the other hand, that you know excluded middle to be false. The resolution, of course, is that you never claimed to be able to *prove* it false.

This way of talking has even been formalised in (Bishop, 1967) with a convention adopted by many (but not all) of his followers. In this convention, the word 'not', used normally in a vernacular sentence whose mathematical content would otherwise be the proposition $p$, changes to the content to $\neg p$, or $p \to \bot$, as usual. This follows all of the rules of intuitionistic logic; in particular, any statement that is 'not' true is false (just as in classical logic). However, the word '<i>not</i>', in italics as shown here, changes the content to $p \to x$, where $x$ is some statement that is known (although not proved!), according to Bishop, to be false. Now a statement that is '<i>not</i>' true may be false, but this may be unknown, and it is even possible that it is '<i>not</i>' false (so $\neg p \to x$, possibly for a different $x$) either!

Bishop gives in his introduction several statements, suitable for use as $x$ above, including:
* excluded middle itself, which Bishop call the 'principle of omniscience';
* the 'limited principle of omniscience': any infinite sequence in $\{0,1\}^N$ is either all $0$ or has at least one $1$;
* the 'lesser limited principle of omniscience': any infinite sequence in $\{0,1\}^N$ that is not all $0$ has at least one $1$;
* others.

At one point, discussing the possibility of a pointwise-continuous function $[0,1] \to R$ that is not uniformly continuous (a 'Specker function', which Markov\'s school claims to exist), Bishop seems to assert that this theorem is both '<i>not</i>' true and '<i>not</i>' false; he does not put it this way, so this may not be exactly what he meant, but there is no contradiction if it is. (But *is* a contradiction, even in intuitionistic logic, if a statment is both 'not' true and 'not' false; indeed, the definition of 'false' may be taken to be 'not true'.)

This practice can be understood through a careful distinction between object language and metalanguage. A mathematical statement $p$ \(such as the continuum hypothesis, or that a Specker function exists\) belongs to the object language, as does $\neg p$ or $p \to x$ for any specific mathematical statement $x$. But the statement that $p$ is provable in some formal system (although capable of being phrased internal to any object language suitable for mathematics) belongs to the metalanguage, and as such may be written $\vdash p$. The metalanguage has its own metalogic (which for the sake of argument we may even assume classical), but notice that $\neg \vdash p$ and $\vdash \neg p$ are different; the first claims that $p$ cannot be proved, while the second claims that $p$ can be disproved, which (in a consistent formal system) is stronger. Although Bishop did not commit to any formal system, if we assume for the sake of argument that he settles on one, then we may write $\vdash \neg p$ as our interpretation of his meaning when he asserts 'not' $p$ but $\neg \vdash p$ as his meaning when he asserts '<i>not</i>' $p$.

Even without this convention, which is peculiar to the Bishop school, it is important when reading constructive mathematics to remember the difference between what can be refuted (proved false) and what merely cannot be proved true. Although Brouwer\'s and Markov\'s schools will sometimes make claims that are (classically) outright false (such as that every function $[0,1] \to R$ is pointwise-continuous), it is more common (and can happen in any school) that a constructive mathematician makes a claim that merely *sounds* false, when what they really mean is only that they don\'t accept what you say as true. Often modal phrases like 'not necessarily' will be used where Bishop would use '<i>not</i>', as a clue that we\'re shifting to a metalanguage, or at least merely remaining agnostic rather than outright disagreeing.

The distinction between object language and metalanguage exists even in classical logic, but it seems that most classical mathematicians are not used to remembering it, although it is not entirely clear why this should be so.  One possibly relevant observation is that even if P is a statement which is neither provable nor disprovable (like the continuum hypothesis), in classical mathematics it is still provable that "P is either true or false."  Moreover, classical model theory often restricts itself to two-valued models in which the only truth values are "true" and "false," although classical logic still holds in [[Boolean algebra|Boolean-valued]] models, and in such a case the truth value of P may be neither "true" nor "false," although the truth value of "P or not P" is still "true."  Certainly when talking about classical truths which fail constructively, such as excluded middle, it is important to remember that "fails to be provable" is different from "is provably false."


## Related entries ##

Concepts that usually arise in constructive mathematics, often because they are classically trivial:

*  [[anafunctor]] (classically equivalent to [[functor]])
*  [[apartness relation]] (classically dual to [[equivalence relation]])
*  [[comparison]] (classically dual to [[transitive relation]])
*  [[decidable equality]] (classically trivial)
*  [[decidable subset]] (classically trivial)
*  [[inhabited set]] (classically equivalent to non-[[empty set]])
*  [[linear order]] (classically dual to [[total order]])
*  [[locale]] (classically similar to but not equivalent to [[topological space]])
*  [[quasiorder]] (classically dual to [[partial order]])
*  [[subsingleton]] (classically equivalent to empty set or [[singleton]])

Some of these are also useful internally or even classically.


Topics relevant to the foundations of constructive mathematics:

*  [[axiom of choice]]
*  [[centipede mathematics]]
*  [[choice object]]
*  [[COSHEP]]
*  [[excluded middle]]
*  [[finite mathematics]]
*  [[internalization]]
*  [[internal logic]]
*  [[intuitionistic logic]]
*  [[Markov's principle]]
*  [[power set]]
*  [[predicative mathematics]]
*  [[pretopos]]
*  [[set theory]]
*  [[topos]]
*  [[truth value]]


Other articles with content relating to constructive mathematics:

*  [[axiom of foundation]]
*  [[biproduct]]
*  [[Cantor's theorem]]
*  [[cardinal number]]
*  [[complement]]
*  [[complete lattice]]
*  [[countable set]]
*  [[cyclic order]]
*  [[direct sum]]
*  [[extended natural number system]]
*  [[field]]
*  [[filter]]
*  [[finite set]]
*  [[Grothendieck topos]]
*  [[Hausdorff space]]
*  [[hereditarily finite set]]
*  [[infinite set]]
*  [[injection]]
*  [[local ring]]
*  [[metric space]]
*  [[partial function]]
*  [[pure set]]
*  [[real number]]
*  [[sequence]]
*  [[Set]]
*  [[Sierpinski space]]
*  [[simple object]]
*  [[sober space]]
*  [[topological space]]
*  [[Tychonoff theorem]]
*  [[uniform space]]
*  [[well-founded relation]]
*  [[well-order]]
*  [[well-ordering theorem]]
*  [[well-pointed topos]]
*  [[Zorn's lemma]]

In principle, every article could explain how it applies to constructive mathematics, but that will probably never happen.


## References ##

Errett Bishop (1967). _Foundations of Constructive Analysis_. Rewritten with Douglas Bridges in 1985 as _Constructive Analysis_.

Douglas Bridges, Fred Richman, and Peter Schuster (1998). A weak countable choice principle. Available from [Fred Richman's Documents](http://www.math.fau.edu/Richman/HTML/DOCS.HTM).

Michael Makkai (1996). [Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/).

Fred Richman (2000). [Constructive mathematics without choice](http://www.math.fau.edu/Richman/HTML/nsf.htm).

Paul Taylor (1996). Intuitionistic Sets and Ordinals. Available (with several other references) at [Induction, recursion, replacement and the ordinals](http://www.PaulTaylor.EU/ordinals/index.php).

Joyal, A. and Moerdijk, I. (1995).  Algebraic set theory.

Frank Waaldijk (2003). [on the foundations of constructive mathematics - especially in relation to the theory of continuous functions](http://home.hetnet.nl/~sufra/foundations%20of%20constructive%20mathematics.pdf) (PDF).

Most books on [[topos]] theory include some discussion of their [[internal logic|internal]] constructive logic.  One good reference is Part D of _Sketches of an elephant (vol. 2)_ by Peter Johnstone.


## Discussion ##

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


[[!redirects constructivism]]