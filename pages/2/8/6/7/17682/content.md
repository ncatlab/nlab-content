* table of contents
{: toc}

##Idea

A number of researchers have proposed that the [[category theory|category theoretic]] concept of [[monads]] may play a role in understanding semantic and pragmatic issues in the use of natural language.

>Side effects are to programming languages what pragmatics are to natural languages: they both study how expressions interact with the worlds of their users. It might then come as no surprise that phenomena such as anaphora, presupposition, deixis and conventional implicature yield a monadic description. ([Mar&#353;&#237;k Amblard 2016, p. 3](#MarAmb16))

In overview papers ([Cohn-Gordon](#Cohn-Gordon), [Asudeh](#Asudeh)), it is proposed that the following topics are explained by specific monads:

1. Conventional implicature: the [[writer monad]]
1. Optional arguments: the [[maybe monad]]
1. Presupposition failure: the exception monad
1. Anaphora: the [[state monad]] and set monad
1. Perspective, opacity and intentionality: the [[reader monad]]
1. Conjunction fallacies: the [[Giry monad|probability monad]]
1. Quantifier Scope: the [[continuation monad]]
1. Focus: the pointed set monad
1. Interrogatives: the set monad
1. Performatives: the [[IO monad]]



## Related concepts

* [[monad (in computer science)]]
* [[dependent type theoretic methods in natural language semantics]]

##References

For a summary of uses, see 

* {#Cohn-Gordon} Reuben Cohn-Gordon, _Monad Transformers for Natural Language:Combining Monads to Model Effect Interaction_, [pdf](https://reubenharry.github.io/docs/monads.pdf)

* {#Asudeh} [[Ash Asudeh]], _Monads: Some Linguistic Applications_, [pdf](http://www.sas.rochester.edu/lin/sites/asudeh/handouts/asudeh-se-lfg13.pdf)

* [[Gianluca Giorgolo]] and [[Ash Asudeh]], _Natural Language Semantics with Enriched Meanings_, [pdf](http://www.sas.rochester.edu/lin/sites/asudeh/pdf/esslli2015-course-notes.pdf)


These refer to:

* [[Gianluca Giorgolo]] and [[Ash Asudeh]], 2011. Multidimensional Semantics with Unidimensional Glue Logic. In Butt and King 2011, 236&#8211;256.
* [[Gianluca Giorgolo]] and [[Ash Asudeh]], 2012a. _$\langle M, \eta, \star \rangle$ Monads for Conventional Implicatures_. In Ana Aguilar Guevara, Anna Chernilovskaya, and Rick Nouwen, eds., Proceedings of Sinn und Bedeutung 16. MIT Working Papers in Linguistics.
* [[Gianluca Giorgolo]] and [[Ash Asudeh]], 2012b. _Missing Resources in a Resource-Sensitive Semantics._ In Miriam Butt and Tracy Holloway King, eds., Proceedings of the LFG12 Conference, 219&#8211;239. Stanford, CA: CSLI Publications.
* [[Gianluca Giorgolo]] and [[Ash Asudeh]], 2013a. _Monads as a Solution for Generalized Opacity._ Ms., University of Oxford.
* [[Gianluca Giorgolo]] and [[Ash Asudeh]], 2013b. _One Semiring to Rule Them All._ Ms., University of Oxford.
* [[Ash Asudeh]] and [[Gianluca Giorgolo]], 2016. _Perspectives._ Semantics and Pragmatics vol. 9, [doi](http://dx.doi.org/10.3765/sp.9.21).
* Shan, Chung-chieh. 2001. _Monads for Natural Language Semantics._ In Kristina Striegnitz, ed., Proceedings of the ESSLLI-2001 Student Session, 285&#8211;298. 13th European Summer School in Logic, Language and Information.
* Christina Unger, 2011. _Dynamic Semantics as Monadic Computation._ In Manabu Okumura, Daisuke Bekki, and Ken Satoh, eds., New Frontiers in Artificial Intelligence - JSAI-isAI 2011, 68&#8211;81.
* Simon Charlow, 2014. _On the semantics of exceptional scope_, New York University dissertation.

For the specific use of [[continuation-passing style]] techniques, see

* Chris Barker, Chung-Chieh Shan, _Continuations and Natural Language_, OUP, 2014, ([introduction](https://www.nyu.edu/projects/barker/barker-shan-continuations-book-intro.pdf))
* Chris Barker, _Continuations and the nature of quantification_, Natural Language Semantics, 10(3):211&#8211;242, 2002.
*  Chris Barker, _Continuations in natural language_, in Hayo Thielecke, editor, Proceedings of the Fourth ACM SIGPLAN Continuations Workshop (CW'04), Birmingham, UK, 2004.
* Ekaterina Lebedeva, _Expression de la dynamique du discours &#224; l'aide de continuations_, ([thesis](http://www.theses.fr/2012LORR0025)) 

The alternative approach to treating [[side effects]], known as [[algebraic effects]], has also been employed in natural language semantics:

* Jirka Mar&#353;&#237;k, Maxime Amblard, _Algebraic Effects and Handlers in Natural Language Interpretation_, [pdf](https://hal.archives-ouvertes.fr/hal-01079206/file/effects-paper.pdf)
* {#MarAmb16} Jirka Mar&#353;&#237;k, Maxime Amblard, _Introducing a Calculus of Effects and Handlers for Natural Language Semantics_, [arXiv:1606.06125](https://arxiv.org/abs/1606.06125)

The weaker notion of [[applicative functors]] has also been used:

* Oleg Kiselyov, _Applicative Abstract Categorial Grammars_, ([pdf](http://okmij.org/ftp/gengo/applicative-symantics/AACG.pdf))
* Oleg Kiselyov, _Applicative Abstract Categorial Grammars in Full Swing_, ([pdf](http://okmij.org/ftp/gengo/applicative-symantics/AACG1.pdf))
* Simon Charlow, _A modular theory of pronouns and binding_, ([pdf](http://ling.auf.net/lingbuzz/003720))