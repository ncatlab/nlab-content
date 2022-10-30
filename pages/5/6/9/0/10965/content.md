
> under construction


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

**Abstract** While [[analytic philosophy]] famously rejected the
speculative [[metaphysics]] of [[Hegel]] in favor of the analysis of concepts by means of [[mathematical logic]], in particular [[predicate logic]], recent developments in the [[foundations of mathematics]]  via [[homotopy type theory]] offer a way to re-read [[Hegel]] as having useful formal meaning not in [[predicate logic]], but in '[[modal type theory]]'. The essence of this suggestion has been made by [[Lawvere]] [[Some Thoughts on the Future of Category Theory|in 1991]], which however remains largely unnoticed. Here we aim to give a transparent account of this perspective both [[philosophy|philosophically]] as well as [[category theory|category-theoretically]]. We then further expand on Lawvere's formalization of Hegel's "[[Science of Logic]]" in terms of the [[categorical semantics]] given by [[cohesive (infinity,1)-topos|cohesive higher toposes]]. We discuss how there is a _useful_ formalization of a fair bit of modern fundamental [[physics]], in fact of [[local quantum field theory|local]] [[gauge field theory|gauge]] [[quantum field theory]], to be found here.


#Contents#
* table of contents
{:toc}

## Introduction

With the rise of [[analytic philosophy]] in Britain, and its adoption and development of the new logic forged by [[Frege]] and [[Peano]], there came a radical rejection of the existing philosophical paradigm, the [[idealism]] of [[T. H. Green]] and [[F. H. Bradley]], and those considered to have provided its primary source, notably [[Hegel]]. [[Bertrand Russell]] was adamant that the new logic would thoroughly transform philosophy, as he made clear at the end of his chapter _Logic As The Essence Of Philosophy_:

> The old logic put thought in fetters, while the new logic gives it wings. It has, in my opinion, introduced the same kind of advance into philosophy as Galileo introduced into physics, making it possible at last to see what kinds of problems may be capable of solution, and what kinds are beyond human powers. And where a solution appears possible, the new logic provides a method which enables us to obtain results that do not merely embody personal idiosyncrasies, but must command the assent of all who are competent to form an opinion. (Logic As The Essence Of Philosophy, 1914)

In the same chapter, Hegel was taken to task for his attempt to widen logic to a form of [[metaphysics]]. Much of it appears to Russell to result from muddled thinking, for instance, a failure to distinguish the 'is' of predication from the 'is' of identity.

This set the tone for analytic philosophy's opinion of Hegel for several decades. In 1951, the logical empiricist [[Hans Reichenbach]] wrote

>Hegel has been called the successor of Kant; that is a serious misunderstanding of Kant and an unjustified elevation of Hegel. Kant's system, though proved untenable by later developments, was the attempt of a great mind to establish rationalism on a scientific basis. Hegel's system is the poor construction of a fanatic who has seen one empirical truth and attempts to make it a logical law within the most unscientific of all logics. Whereas Kant's system marks the peak of the historical line of rationalism, Hegel's system belongs in the period of decay of speculative philosophy which characterizes the nineteenth century. (Reichenbach 1951, p. 72)

However, despite the initial lengthy rejection of Hegelian ideas by analytic philosophy, there have recently been increasing signs of a willingness to re-engage with Hegel's writings, in particular on the part of [[John MacDowell]] and [[Robert Brandom]] (Redding, 2007). Interestingly, one feature of analytic philosophy which needs reconsidering according to Redding is the primacy of [[first-order logic|first-order]] predicate logic, not, however, that he is promoting an alternative formalization based on Hegel's ideas. 

It took a mathematician [[William Lawvere]] to find something formalizable of value in Hegel's _Logic_, in particular the concept of a '[[unity of opposites|Unity of Opposites]]'. In this paper, taking our lead from Lawvere in seeing common elements between [[categorical logic]] and Hegel's logic, we will pursue this connection right up to [[modal type theory|modal]] forms of [[homotopy type theory]].

Now, Hegel's understanding of the term 'Logik' was much broader than is normally the case. Indeed, the 'Objective logic' of [[Science of Logic]] is more akin to a kind of [[metaphysics]].  While the [[Vienna Circle]], admirers of Russell, had adopted the [[positivism|positivist]] attitude towards [[metaphysics]], dismissing it as meaningless ([Carnap 32](#Carnap32)), later in the twentieth century there was a resurgence of analytic metaphysics. One important source of this resurgence was the rise of [[modal logic]] as a tool for philosophy, especially due to [[Saul Kripke]] in _Naming and Necessity_. If the necessity of a proposition consists in its holding in all neighboring possible worlds, sense had to be made of these possible worlds. To what would have been Carnaps' amazement, philophers such as David Lewis proposed the reality of all possible worlds, the actual world being in no way special, except for its being our world.

Today, standard topics for analytic metaphysics today include causality, necessity, space and time, identity, and mental states. Little attention is paid to the question of explaining the kind of physical principles which operate in our universe. It is noteworthy, however, that the need for some such questioning seems to be as strongly felt among modern physicists as it must have been to Hegel and his predecessors, as witnessed by ... debates such as critically reviewed in ([Albert 12](#Albert12)). (...) Attempts to re-install this kind of metaphysics are these days undertaken by [[particle physics|particle physicists]] and [[cosmology|cosmologists]] themselves, whose success at formally describing remote aspects of the [[observable universe]] has emboldened many to feel as superior to modern philosophy as modern philosophy typically feels towards Hegel' idealism. 

(...)

## Modern foundations -- Types, Judgements and Deduction

(...) something like: 

analytic philosophy was certainly right to ask for a formal basis of philosophical reasoning, in order to make genuine intellectual progress possible. Back then [[predicate logic]] and [[set theory]] was the state of the art concerning the [[foundations of mathematics]] and so this is what analytic philosophy adopted and developed. But since then there has been much progress in the foundations of maths. ... [[intuitionistic type theory]] ... [[homotopy type theory]]...

Accordingly, the original starting point of analytic philosophy needs to be re-examined. While predicate logic has no way of making formal sense of Hegel's "Logic", for type theory the situation is rather different...

## Categorical semantics and Categorical logic

... type theory proper is a formal system for symbol manipulation ... useful for computer encoding, and much more readable than full formalization in, say, ZFC, but still not really what a discussion such as our here would directly work with...

... instead, the [[syntax]] of type theory has [[semantics]] in [[categories]] -- [[categorical semantics]] ... [[relation between category theory and type theory]] -- and this semantic level is what we will be concerned with here

... originates with Lawvere's thesis, see also "[[Adjointness in Foundations]]"

## Modalities, moments and opposites

(... basics of [[modalities]], [[modal operators]], [[monads]], leading up to [[adjoint modality]]/[[unity of opposites]]...)


## Formal determinations of Being

... using this and building on Lawvere's lead, we are led to objectively investigate the following:

starting with bare homotopy type theory and adding [[adjoint modalities]] to it, what is the nature of the new propositions that can be proven with these modalities, hence what is the new "quality" of the types in the presence of these new axioms...

...

$$
   \array{
      reines\;Sein && Dasein && Realitaet
      \\
      being && existence && reality
      \\
       pure being && determinate being 
      \\
      \\
      && && \Re
      \\
     && && \bot
      \\
      && \int & \subset & \oint
      \\
      && \bot && \bot 
      \\
      \emptyset &\subset& \flat & \subset & \Im
      \\
      \bot & & \bot && 
      \\
      \ast & \subset& \sharp      
   }
$$

| symbol | $\;\;$ name |
|---|---|
| $\int$ | [[shape modality]] |
| $\flat$ | [[flat modality]] |
| $\sharp$ | [[sharp modality]] |
| $\oint$ | [[infinitesimal shape modality]] |
| $\Re$ | [[reduction modality]] |
| $\Im$ | [[infinitesimal flat modality]] |

(...)


## References

* [[Rudolf Carnap]], _&#220;berwindung der Metaphysik durch logische Analyse der Sprache_, Erkenntnis Vol II (1932). Translated by A. Pap as _The Elimination of Metaphysics Through Logical Analysis of Language_ ([pdf](http://www.calstatela.edu/sites/default/files/dept/phil/pdf/res/Carnap-Elimination-of-Metaphysics.pdf))
 {#Carnap32}

* [[Georg Hegel]], _[[Science of Logic]]_ (1812)

* [[William Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ (1991)

* [[William Lawvere]] _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_ (1994)

* [[William Lawvere]] _[[Unity and Identity of Opposites in Calculus and Physics]]_ (1996)

* [[Higher toposes of laws of motion]]

* [[schreiber:Homotopy-type semantics for quantization]]

* Paul Redding, _Analytic Philosophy and the Return of Hegelian Thought_, Cambridge University Press, 2007 ([review](http://ndpr.nd.edu/news/23465-analytic-philosophy-and-the-return-of-hegelian-thought/) by Willem A. deVries)

* [[Bertrand Russell]], 'Logic As The Essence Of Philosophy', chap. 2 of _Our Knowledge of the External World_, (1914)

* [[Hans Reichenbach]], 'The Rise of Scientific Philosophy', 1951.

* [[David Albert]], _On the Origin of Everything_, book review of 
"A Universe From Nothing", by Lawrence M. Krauss, in the New York Times from March 25, 2012, on page BR20 of the _Sunday Book Review_ ([web](http://www.nytimes.com/2012/03/25/books/review/a-universe-from-nothing-by-lawrence-m-krauss.html?))
 {#Albert12}

* [[Max Tegmark]], _The mathematical Universe_ ([arXiv:0704.0646](http://arxiv.org/abs/0704.0646))
 {#Tegmark07}


[[!redirects Lawverian formalization of Hegelian metaphysics]]

