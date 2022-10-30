
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Constructive mathematics
* table of contents
{: toc}

## Idea

Broadly speaking, __constructive mathematics__ is [[mathematics]] done without the [[principle of excluded middle]], or other principles, such as the full [[axiom of choice]], that imply it, hence without "non-constructive" methods of [[formal proof]], such as [[proof by contradiction]]. This is in contrast to _[[classical mathematics]]_, where such principles are taken to hold.

There are variations of what exactly is regarded as constructive mathematics, for instance [[intuitionistic mathematics|intuitionism]] or [[predicative mathematics|predicativism]], see the list of schools [below](#OriginsAndSchools). But beware the ambiguity in terminology: In [[Brouwer]]-style [[intuitionistic mathematics]] one includes [[axioms]] that _[[contradiction|contradict]]_ [[classical logic]], while other authors use "intuitionistic" to mean what elsewhere is called "constructive", and referring only to rejection of [[excluded middle]] and [[axiom of choice|choice]]. Some authors (particularly [[material set theory|material set theorists]]) use "constructive" to mean *[[predicative]]* constructive and "intuitionistic" to mean impredicative constructive. 
Other authors emphasize the necessity that constructive theories be [[proof relevance|proof relevant]], with denial of the excluded middle's universality subordinate to this requirement; see ([Harper 2013](#Harper13)).

__Constructivism__ is the philosophy that such mathematics is useful, or (more strongly) that non-constructive mathematics is wrong.  Historically, constructive mathematics was first pursued explicitly by mathematicians who believed the latter.  However, many modern mathematicians who do constructive mathematics do it not because of any philosophical belief about the wrongness of non-constructive mathematics, but because constructive mathematics is interesting in its own right.  In the '[pluralist](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.93.9892)' approach to the [[foundations]] of mathematics, a constructive proof (when it exists) is better because it is valid in more versions of mathematics, but a classical proof remains valid for [[classical mathematics]].

Another motivation for modern mathematicians ---especially category theorists like those on the nLab--- is that the study of constructive mathematics has potential applications to non-constructive mathematics.  For example, even if one believes the principle of excluded middle to be true, the "[[internal logic|internal]]" version of excluded middle in many interesting [[category|categories]] is still false; thus constructive mathematics can be useful in the study of such categories, even if mathematics is "globally" non-constructive.  This is the neutral motivation for constructive mathematics from the [nPOV](/nlab/show/nPOV#Logic).

Here we write mostly about the mathematics, trying to be mostly neutral philosophically.


## Origins and schools
 {#OriginsAndSchools}

During the "[[foundations|foundational]] crisis" in mathematics around the beginning of the 20th century, a number of mathematicians espoused philosophies that are generally grouped together and labeled **constructivist**. The common feature of these philosophies was a rejection of axioms and principles of logic that lead to nonconstructive proofs.  There was much talk at the time about potential vs absolute infinity, but from an axiomatic perspective, it turns out that (if one stops short of finitism) the two main culprits are

* the [[axiom of choice]] and
* the principle of [[excluded middle]].

Thus, constructivists (including many still active today) reject proofs that make use of either of these.  (In fact, it was realized in 1975 by Diaconescu that the axiom of choice implies the principle of excluded middle.  Excluded middle is precisely the "finitely indexed" axiom of choice; see [[excluded middle]] for a proof.)

There are, however, differences among constructivists as well, even discounting the pluralists.

* Some, like [[Errett Bishop]], simply remove choice and excluded middle from [[classical mathematics]] with nothing to replace them.  (Although this is not quite a correct and complete description of [[Bishop's constructive mathematics]]; see there.)   However, this makes it difficult to define a satisfactory notion of [[continuous function]], even from the [[real line]] to itself, without using [[locales]]; see (Waaldijk 2003).

* Others add "non-classical" axioms which contradict choice or excluded middle, but which are consistent in their absence, such as "all total functions $[0,1] \to \mathbb{R}$ are continuous" (the [[continuity axiom]] of the "[[intuitionism|intuitionistic]]" school of [[L. E. J. Brouwer]]) or "all partial functions $\mathbb{N} \to \mathbb{N}$ are computable" (the [[computability axiom]] of the "[[Russian constructivism|Russian]]" school of [[Andrey Markov Jr|A. A. Markov]], which is also called "constructive recursive analysis").

* Most accept weaker versions of choice, such as [[countable choice]] or even [[dependent choice]].  [[Toby Bartels]] argues that the intuition behind accepting these justifies the (yet stronger) [[presentation axiom]] (that [[the category of sets]] has [[enough projectives]]).  On the other hand, [[Fred Richman]] rejects even these limited forms of choice; see (Richman 2000).

* Still others, following [[Hermann Weyl]], go even further and refuse to allow "impredicative" constructions; see [[predicative mathematics]].  Most of the work done by the schools of Brouwer, Bishop, and Markov (but not Richman) is also predicative, even though those founders were not adamant about it; as a result, predicativism often appears in the [[foundations]] of constructive mathematics (in particular, in those of [[Peter Aczel|Aczel]] and [[Per Martin-Löf|Martin-Löf]], but not those of [[Harvey Friedman|Friedman]] or [[Thierry Coquand|Coquand]]).

* Very extreme constructivists, like [[Doron Zeilberger]], reject the existence of infinite sets; see [[finitism]].  (Kronecker, the 'father of constructivism', is often considered a finitist, but as he came before the foundational crisis, it is difficult to classify him accurately.)  Ironically, this means that excluded middle and choice, in their na&#239;ve forms, may become acceptable, or even true.  (Even constructivists believe that they are true [[internal logic|in]] the category [[FinSet]] of [[finite sets]].)

* The most extreme position of all is to deny even the existence of very large finite sets.  This is called [[ultrafinitism]].  This has been studied largely by [[Alexander Yesenin-Volpin]] and (more recently) [[Edward Nelson]]; foundational systems such as [[soft linear logic]] can also be argued to have an ultrafinitist flavor.  Zeilberger also claims sympathy with ultrafinitist philosophy, although his actual work fits well into a (merely) finitist framework.

Many constructivists (like many classical mathematicians) believe in an absolute mathematical sense of "truth," and that in this sense choice and excluded middle are simply _wrong_.  (Some constructivists, using classically false axioms, can even refute them; others merely claim that no possible correct reasoning could ever prove them.  See [Truth versus assertability](#truevassert) below.)  To most mathematicians, this makes them seem quite strange.  Other constructivists adopt a wait-and-see attitude, or even a relative notion of truth (which can seem strange in another way).

The following is a partial list of schools and subtheories of constructive mathematics:

* Brouwer's [[intuitionistic mathematics]]
* [[Russian constructivism]]
* [[Bishop's constructive mathematics]]
* [[constructive reverse mathematics]]
* (at least related) [[explicit mathematics]]


## Topos theory

With the invention of [[topos|topos theory]] in the second half of the 20th century, a new sort of constructivism arose.  It was observed (by [[Bill Lawvere|Lawvere]] and others) that any topos with a [[natural numbers object]] has an [[internal logic]] which is powerful enough to interpret most of mathematics, but that this logic in general fails to satisfy choice and excluded middle.  This meant that even for a mathematican who likes to use choice and excluded middle (and _a fortiori_ for one who believes them to be "true"), there is a reason to care about what can be proven without them, because only if a proof is constructive can it be interpreted in an arbitrary topos with NNO.

Even starting from a "completely classical" world of mathematics, many interesting toposes arise naturally (such as the category of [[sheaf|sheaves]] on any [[topological space]], or more generally any [[site]]) whose internal logic is not [[classical logic]].  Then by internal reasoning in such a topos (which is constructive reasoning), one can prove various useful facts, which can then be reinterpreted as external statements about the behavior of the topos itself.  For example, the constructive theorem that every [[one-sided real number]] that is both a lower real and an upper real must be located (which, classically, is an utter triviality) becomes the theorem that any [[semicontinuous function]] (from any [[topological space]] to the [[real line]]) that is both upper and lower semicontinuous must be [[continuous map|continuous]] (which is at least somewhat nontrivial).

By now it is known that many of the non-classical axioms used by the early constructivists have natural models in particular toposes.  For instance, in the topos of sheaves on the real numbers $R$, the [[continuity axiom]] that "all total functions $R \to R$ are continuous" holds.  And in the [[effective topos]], the [[computability axiom]] that "all partial functions $N\to N$ are computable" holds.

However, there are no non-classical (or classical) axioms beyond "pure constructivism" that are true in _all_ toposes with NNO.  In particular, there is a [[free topos]] with NNO such that a statement is true in the free topos precisely when it is provable in pure (Richman-school) constructive mathematics.  This means that for an argument to apply in all toposes, even mild assumptions such as countable or dependent choice are unacceptable (but impredicativity is fine).  However, topos theory has also provided ideas that solve many of the problems with pure constructivism.  For example, a well-behaved notion of "continuous function" can be recovered by using [[locale|locales]] instead of topological spaces, which was first discovered in the context of toposes and is closely related to them in any case.


## Some features of constructive mathematics

### Rephrasing of classical ideas

Sometimes, all that is necessary to make a piece of mathematics constructive is careful use of language.  It is common in [[classical mathematics]] to define things with an unnecessary amount of [[negation]].  This doesn't work so well constructively, since a statement can be not false without being true, but we can sometimes do perfectly well by just removing unnecessary [[double negations]].

For example, classically one often speaks about "nonempty" sets, meaning a set which "does _not_ have _no_ elements."  Constructively it is much better to say that a set "*does* have at least one element"; constructivists often call such a set _[[inhabited set|inhabited]]_ to remind themselves that it is a "positive" notion to replace the negative one of "nonempty". Others continue to use the word "non-empty" but understand it as a term of art that really means "inhabited".


### Bifurcation of notions

On the other hand, differences in axiomatization or definition that make no difference classically can result in actual differences in behavior constructively.  Therefore, classically equivalent notions often "bifurcate" (or "trifurcate" or worse) into multiple inequivalent constructive ones.  This tends to happen whenever a concept involves _[[negation]]_ and, to a lesser degree, _[[disjunction]]_ and _[[existential quantification]]_.  In some cases there is a "correct" constructive version of the definition, although it may take some thought to uncover it, but in many cases more than one of the resulting concepts is important and useful.  For example:

* There are multiple inequivalent constructive definitions of a [[field]], because of the axioms "every _nonzero_ element has an inverse" and $0 \neq 1$.

* In pure constructive logic, there are multiple inequivalent definitions of [[real numbers]].
  * the [[Dedekind real numbers]] and the [[Cauchy real numbers]] need no longer coincide.  The Cauchy reals sit inside the Dedekind reals, but in general not every Dedekind real need be approximable by a _[[sequence]]_ of rationals.  From a topos-theoretic viewpoint, the Dedekind reals are usually the "correct" notion to study (if not the [[locale of real numbers]] as a whole). However, the weak [[limited principle of omniscience]] suffices to ensure that every Dedekind real is a Cauchy real, and hence that the two notions coincide; see ([[Univalent Foundations Project]] 2013) and (Booij 2020). Weak countable choice implies the weak limited principle of omniscience, which in turn is implied by excluded middle and the axiom of choice; see (Bridges et al. 1993).
  * Similarly, the [[Cauchy real numbers]] are not sequentially [[Cauchy complete]]. There is an intermediate set of [[real numbers]] between the Cauchy reals and the Dedekind reals that are sequentially Cauchy complete called the [[HoTT book real numbers]], such that there are embeddings from the Cauchy reals to the HoTT reals, and from the HoTT reals to the Dedekind reals, but there are no embeddings in the reverse direction. 
  * That every [[Cauchy real number]] in the [[unit interval]] can be represented by a [[sequence]] of digits is equivalent to the lesser [[limited principle of omniscience]], so it is no longer true that every [[Cauchy real number]] has an infinite decimal representation. The set of all real numbers with infinite decimal representations are called [[prealgebra real numbers]]. 

* There are at least three different constructive notions of [[ordinal number]]; see (Taylor 1996) and (Joyal--Moerdijk 1995).

* Without the axiom of choice, [[functor|functors]] and [[anafunctor|anafunctors]] become distinct, and often the latter is more appropriate; see (Makkai, 1996).

* Perhaps most disturbingly of all to the classical mathematician, one must distinguish between _finite sets_, _subfinite sets_, _finitely-indexed sets_, and even _subfinitely indexed sets_; see [[finite set]] for definitions.  However, in practice it is usually either finite or finitely-indexed sets that are important, and with practice a little bit of thought suffices to show which is the relevant concept.


### Negative translation

This allows one to translate classically valid theorems into intuitionistically valid theorems. See [[double negation translation]]. 


### Truth versus assertability
{#truevassert}

Already in [[classical mathematics]], there is a difference between saying that something is true and saying that something is [[proof|provable]]. If you adopt [[ZFC]] because you believe it correct, then presumably you believe that ZFC is consistent even though (assuming that you\'re aware of certain theorems) you also know that you cannot prove it so. In that case, you also believe that the [[continuum hypothesis]] (for example) is either true or false; you may or may not have an opinion on which it is, but in any case again you know that you cannot prove it either way.

A constructive mathematician can be even subtler. If you belong to the Bishop school, then you accept no classically false axioms, and anything that you can prove is valid also in classical mathematics. Even so, you can believe that the principle of excluded middle is false (even though, of course, you know that you cannot prove it false). So you can really confuse the classical mathematicians by saying, on the one hand, that they can safely accept all of your theorems as valid, and then saying, on the other hand, that you know excluded middle to be false. The resolution, of course, is that you never claimed that this was a *theorem*.

This way of talking has even been formalised in (Bishop, 1967) with a convention adopted by many (but not all) of his followers. In this convention, the word 'not', used normally in a vernacular sentence whose mathematical content would otherwise be the proposition $p$, changes to the content to $\neg p$, or $p \to \bot$, as usual. (This follows all of the rules of [[intuitionistic logic]]; in particular, any statement that is 'not' true is false (just as in [[classical logic]]).) However, the word '<i>not</i>', in italics as shown here, changes the content to $p \to x$, where $x$ is some statement that is known (although not proved!), according to Bishop, to be false. Now a statement that is '<i>not</i>' true may be false, but this may be unknown, and it is even possible that it is also '<i>not</i>' false (so $\neg p \to x$, possibly for a different $x$).

Bishop gives in his introduction several statements, suitable for use as $x$ above, including:

* excluded middle itself, which Bishop call the 'principle of omniscience';
* the '[[limited principle of omniscience]]': any infinite sequence in $\{0,1\}^N$ is either all $0$ or has at least one $1$;
* the '[[lesser limited principle of omniscience]]': for any two infinite sequence in $\{0,1\}^N$ that do not both have at least one $1$, at least one of these sequences does not have at least one $1$;
* others.

At one point in his book, while discussing the possibility of a pointwise-continuous function $[0,1] \to R$ that is not uniformly continuous (a [[Specker function]], whose existence Markov\'s school claims as a theorem), Bishop seems to assert that this theorem is both <i>not</i> true and <i>not</i> false; he does not put it this way, so this may not be exactly what he meant, but there is no contradiction if it is. (But it *is* a contradiction, even in intuitionistic logic, if a statment is both not true and not false; indeed, a definition of 'false' may be taken to be 'not true'.)

This practice can be understood through a careful distinction between [[object language]] and [[metalanguage]]. A mathematical statement $p$ (such as the continuum hypothesis, or that a Specker function exists) belongs to the object language, as does $\neg p$ or $p \to x$ for any specific mathematical statement $x$. But the statement that $p$ is provable in some formal system belongs to the metalanguage (although it can also phrased internal to any object language suitable for mathematics), and as such may be written $\vdash p$. The metalanguage has its own logic (the metalogic, which for the sake of argument we may even assume to be classical), but notice that $\neg \vdash p$ and $\vdash \neg p$ are different; the first claims that $p$ cannot be proved, while the second claims that $p$ can be refuted, which (in any [[consistent logic|consistent]] formal system, even a classical one) is strictly stronger. Although Bishop did not commit to any formal system, if we assume for the sake of argument that he settled on one, then we may write $\vdash \neg p$ as our interpretation of his meaning when he asserts 'not $p$' but $\neg \vdash p$ as his meaning when he asserts '<i>not</i> $p$'.

Even without the notational convention of the Bishop school, it is important when reading constructive mathematics to remember the difference between what can be refuted (proved false) and what merely cannot be proved true. Although Brouwer\'s and Markov\'s schools will sometimes claim to prove statements that are (classically) outright false (such as that every function $[0,1] \to R$ is pointwise-continuous), it is more common (and can happen in any school) that a constructive mathematician makes a claim that merely *sounds* false, when what they really mean is only that they don\'t accept what you say as true. Often modal phrases like 'not necessarily' will be used where Bishop would use '<i>not</i>', as a clue that we\'re shifting to a metalanguage, or at least merely remaining agnostic rather than outright disagreeing.

The distinction between object language and metalanguage exists even in [[classical mathematics]], but it seems that most classical mathematicians are not used to remembering it, although it is not entirely clear why this should be so.  One possibly relevant observation is that even if $P$ is a statement which is neither provable nor disprovable (like the continuum hypothesis), in classical mathematics it is still provable that "$P$ is either true or false."  Moreover, classical [[model theory]] often restricts itself to [[two-valued model]]s in which the only truth values are "true" and "false," although classical logic still holds in [[Boolean algebra|Boolean-valued]] models, and in such a case the truth value of $P$ may be neither "true" nor "false," although the truth value of "$P$ or not $P$" is still "true."  Certainly when talking about classical truths which fail constructively, such as excluded middle, it is important to remember that "fails to be provable" is different from "is provably false."


## Prehistory

In 

* [[Georg Hegel]], _[[Phenomenology of Spirit]]_  (1807)

the following comment about mathematical proof (in section _[12 Historical and mathematical proof](https://www.marxists.org/reference/archive/hegel/works/ph/phprefac.htm#12)_ of the Preface) might be read as being a complaint about the traditional non-constructive concept of proof and about the traditional lack of [[proof relevance]]:

> {#PoSOnProofRelevance} All the same, while proof is essential in the case of mathematical knowledge, it still does not have the significance and nature of being
a moment in the result itself; the proof is over when we get the
result, and has disappeared. The process of mathematical proof does not belong to the object; it is a function that takes place outside the matter in hand.

> [footnote 42](https://www.marxists.org/reference/archive/hegel/help/finpref.htm#m042): Mathematical truths are not thought to be known unless proved true. Their demonstrations are not, however, kept as parts of what they prove, but are only our subjective means towards knowing the latter. In philosophy, however, consequences always form part of the essence made manifest in them, which returns to itself in such expressions.

See also earlier conceptions of proofs expressing the 'cause' of a theorem, where *reductio* proofs in particular were taken generally to fail. Such an idea goes back to Aristotle for whom a proper answer to the question "Why is the angle in a semicircle a right-angle?" gives its cause.

* Paolo Mancosu, _Philosophy of Mathematics and Mathematical Practice in the Seventeenth Century_, OUP, 1996.


## Related entries

See also 

* [[intuitionistic mathematics]]

* [[realizability]]

* [[computability]]

* [[constrictive set theory]]

* [[constructive analysis]]

* [[taboo]]


Concepts that usually arise in constructive mathematics, often because they are classically trivial:

*  [[proof relevance]]
*  [[anafunctor]] (classically equivalent to a [[functor]])
*  [[apartness relation]] (classically complementary to an [[equivalence relation]])
*  [[comparison]] (classically complementary to a [[transitive relation]])
*  [[decidable equality]] (classically trivial)
*  [[decidable subset]] (classically trivial)
*  [[inhabited set]] (classically equivalent to a non-[[empty set]])
*  [[linear order]] (classically complementary to a [[total order]])
*  [[locale]] (classically similar to but not equivalent to a [[topological space]])
*  [[quasiorder]] (classically complementary to a [[partial order]])
*  [[subsingleton]] (classically equivalent to the empty set or a [[singleton]])

Some of these are also useful internally or even classically.


Topics relevant to the foundations of constructive mathematics:

*  [[axiom of choice]]
*  [[Bishop set]]
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
*  [[type theory]]
   *  [[intuitionistic type theory]]
   *  [[homotopy type theory]]


Other articles with content relating to constructive mathematics (rather incomplete):

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

There is also

* [[constructivism and idealism]]

## References
 {#References}

See also the references at _[[intuitionistic mathematics]]_ for more.


Gentle introductions:

* [[Douglas Bridges]], _Introducing constructive mathematics_, Lecture Notes, Nis 2013 ([pdf](http://www.masfak.ni.ac.rs/cmfp2013/Nis%20lecture%20170113.pdf))

* [[Andrej Bauer]], _Five Stages of Accepting Constructive Mathematics_, 
Bull. Amer. Math. Soc. 54 (2017), 481-498 ([pdf](http://dx.doi.org/10.1090/bull/1556)]. See also a talk at IAS March 18, 2013  ([video](http://video.ias.edu/members/1213/0318-AndrejBauer)).

* [[Fred Richman]], _[Interview with a constructive mathematician](http://math.fau.edu/richman/docs/intrview.html)_,  Modern Logic 6 (1996), no. 3, 247&#8211;271 ([MathSciNet](http://www.ams.org/mathscinet-getitem?mr=1400617))

* {#Blechschmidt15} [[Ingo Blechschmidt]], _Double-negation translation and CPS transforms_, 2015 ([pdf](http://rawgit.com/iblech/talk-constructive-mathematics/master/negneg-translation-notes.pdf))

* Stanford Encyclopedia of Philosophy, _[Constructive mathematics](http://plato.stanford.edu/entries/mathematics-constructive/)_

An more technical introduction to constructive reasoning in mathematics is (with an eye towards [[homotopy type theory]]) in the introduction of:

* [[Univalent Foundations Project]], _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

Other accounts:

*  [[Errett Bishop]] (1967). _Foundations of Constructive Analysis_. Rewritten with Douglas Bridges in 1985 as _Constructive Analysis_.

* [[Michael J. Beeson]], *Foundations of Constructive Mathematics*,  Ergebnisse der Mathematik und ihrer Grenzgebiete **3** 6, Springer 1985 ([doi:10.1007/978-3-642-68952-9](https://link.springer.com/book/10.1007/978-3-642-68952-9), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-642-68952-9.pdf))

* [[Douglas Bridges]] and [[Fred Richman]], _Varieties of constructive mathematics_ (1987)

*  [[Douglas Bridges]], [[Fred Richman]], Peter Schuster (1998). A weak countable choice principle. Available from [Fred Richman's Documents](http://math.fau.edu/richman/html/docs.htm).

*  [[Michael Makkai]] (1996). [Avoiding the axiom of choice in general category theory](http://www.math.mcgill.ca/makkai/anafun/).

*  [[Fred Richman]] (2000). [Constructive mathematics without choice](http://math.fau.edu/richman/html/nsf.htm).

*  [[Paul Taylor]] (1996). Intuitionistic Sets and Ordinals. Available (with several other references) at [Induction, recursion, replacement and the ordinals](http://www.PaulTaylor.EU/ordinals/index.php).

*  [[André Joyal]] and [[Ieke Moerdijk]] (1995). _Algebraic set theory_.

*  [[Frank Waaldijk]] (2003). [On the foundations of constructive mathematics - especially in relation to the theory of continuous functions](http://www.fwaaldijk.nl/foundations%20of%20constructive%20mathematics.pdf) (PDF).

*   [[Auke B. Booij]], Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

In view of [[reverse mathematics]]:

* [[Hajime Ishihara]], _Reverse Mathematics in Bishop's Constructive Mathematics_, Philosophia Scienti&#230;, CS 6 (2006) ([doi:10.4000/philosophiascientiae.406](https://doi.org/10.4000/philosophiascientiae.406),  [pdf](https://philosophiascientiae.revues.org/pdf/406))

* [[Hannes Diener]], *Constructive Reverse Mathematics*, 2018 ([arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306))


General comments on intuitionistic mathematics/logic as the natural language for [[physics]] are in

* [[Andrej Bauer]], _[Intuitionistic mathematics for physics](http://math.andrej.com/2008/08/13/intuitionistic-mathematics-for-physics/)_, August 2008

For more on [[physics]] formalized in intuitionistic mathematics (notably in [[topos theory]]) see at _[[geometry of physics]]_.

For an emphasis on proof relevance, see:

* {#Harper13} [[Robert Harper]],  _[Constructive Mathematics is not Metamathematics](https://existentialtype.wordpress.com/2013/07/10/constructive-mathematics-is-not-meta-mathematics/)_ (2013)

Most books on [[topos theory]] include some discussion of toposes\' [[internal logic|internal]] constructive logic.  One good reference is:

*  [[Peter Johnstone]] (2003). _[[Elephant|Sketches of an elephant]]_. Part D (in volume 2).

A historical account is in 

* [[Anne Sjerp Troelstra]], _History of Constructivism in the Twentieth Century_ (1991). ([pdf](https://www.illc.uva.nl/Research/Publications/Reports/ML-1991-05.text.pdf)) 
 {#Troelstra91}

The relation to [[realizability]] and [[computability]] is discussed in

* {#Bauer05} [[Andrej Bauer]], _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))

On [[commutative algebra]] with constructive methods:

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))



[[!redirects constructive]]
[[!redirects constructive mathematics]]
[[!redirects constructivist mathematics]]

[[!redirects constructivist]]
[[!redirects constructivism]]

[[!redirects construction]]
[[!redirects constructions]]

[[!redirects constructive logic]]
[[!redirects constructivist logic]]

