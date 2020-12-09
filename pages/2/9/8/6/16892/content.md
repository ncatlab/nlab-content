

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Linguistics
+-- {: .hide}
[[!include linguistics - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}



##Idea
A number of researchers are using [[dependent type theory]] as a formal tool to understand [[natural language]]. Some are using in particular [[homotopy type theory]].

## History

In the _Preface_ to his book, _Type-theoretic Grammar_ ([Ranta 94](#Ranta94)), [[Aarne Ranta]] recounts how the idea of studying natural language in constructive type theory occurred to him in 1986: 

> In Stockholm, when I first discussed the project with [[Per Martin-Löf]], he said that he had designed type theory for mathematics, and than natural language is something else. I said that similar work had been done within predicate calculus, which is just a part of type theory, to which he replied that he found it equally problematic. But his general attitude was far from discouraging: it was more that he was so serious about natural language and saw the problems of my enterprise more clearly than I, who had already assumed the point of view of logical semantics. His criticism was penetrating but patient, and he was generous in telling me about his own ideas. So we gradually developed a view that satisfied both of us, that formal grammar begins with what is well understood formally, and then tries to see how this formal structure is manifested in natural language, instead of starting with natural language in all it unlimitedness and trying to force it into some given formalism. 

A noted early application of dependent type theory to natural language was [[Göran Sundholm|Göran Sundholm's]] treatment ([Sundholm 86](#Sundholm86)) of the _Donkey sentence_

> Any farmer who owns a donkey beats it,

which he rendered, using [[dependent product]] and [[dependent sum]], as 

$$
\prod_{z: \sum_{x: Farmer} (\sum_{y: Donkey}Owns(x, y))}Beats(p(z), p(q(z))).
$$

This marks an improvement over first-order logic in which one has to rewrite the Donkey sentence as something like:

> For all farmers and for all donkeys, if the farmer owns the donkey then he beats it.

$$
\forall x \forall y (Farmer(x) \wedge Donkey(y) \wedge Own(x, y) \to Beat(x, y)).
$$


##Related entries

* [[monad (in linguistics)]]



##References

###Papers using dependent type theory

* René Ahn, _Agents, Objects and Events: A computational approach to knowledge, observation and communication_, Ph.D. dissertation, Eindhoven University, 2001.

* Asher, N.: Lexical Meaning in Context: A Web of Words. Cambridge University Press (2011)
* Asher, N., Luo, Z.: Formalisation of coercions in lexical semantics. In: Sinn und Bedeutung. vol. 17, pp. 63&#8211;80 (2012)
* [[Daisuke Bekki]]: Representing anaphora with dependent types. In: Asher, N., Soloviev, S. (eds.) Logical Aspects of Computational Linguistics, Lecture Notes in Computer Science, vol.8535, pp. 14&#8211;29 (2014), [Springer](http://link.springer.com/chapter/10.1007%2F978-3-662-43742-1_2).
* [[Daisuke Bekki]], Asher, N.: Logical polysemy and subtyping. In: Motomura, Y., Butler, A., Bekki, D. (eds.) New Frontiers in Artificial Intelligence, Lecture Notes in Computer Science, vol. 7856, pp. 17&#8211;24. Springer (2013)
* [[Daisuke Bekki]], Satoh, M.: Calculating projections via type checking. In: Proceedings of TYTLES (to appear)
* Robin Cooper, Austinian Truth, Attitudes and Type Theory, Research on Language and Computation. July 2005, Volume 3, Issue 2-3, pp 333-362 [Springer](http://link.springer.com/article/10.1007%2Fs11168-006-0002-z)
* Chatzikyriakidis, S., Luo, Z.: Natural language inference in Coq. Journal of Logic, Language and Information 23(4), 441&#8211;480 (2014)
* [[Zhaohui Luo]]: Type-theoretical semantics with coercive subtyping. In: Semantics and Linguistic Theory 20 (SALT 20). Vancouver (2010)
* [[Zhaohui Luo]]: Contextual analysis of word meanings in type-theoretical semantics. In: Pogodalla, S., Prost, J.-P. (eds.) LACL 2011. LNCS, vol. 6736, pp. 159&#8211;174. Springer, Heidelberg (2011)
* [[Zhaohui Luo]]: Common nouns as types. In: B&#233;chet, D., Dikovsky, A. (eds.) LACL 2012. LNCS, vol. 7351, pp. 173&#8211;185. Springer, Heidelberg (2012), [pdf](http://www.cs.rhul.ac.uk/home/zhaohui/LACL12.pdf).
* [[Zhaohui Luo]]: Event Semantics with Dependent Types, [pdf](http://www.cs.rhul.ac.uk/home/zhaohui/Evt15.pdf)
* [[Zhaohui Luo]], Formal Semantics in Modern Type Theories: Is It Model-theoretic, Proof-theoretic, or Both?, [pdf](http://www.cs.rhul.ac.uk/home/zhaohui/LACL14FINAL.pdf).
* Koji Mineshima, A Presuppositional Analysis of Definite Descriptions in Proof Theory, New Frontiers in Artificial Intelligence Lecture Notes in Computer Science Volume 4914, 2008, pp 214-227 [Springer](http://link.springer.com/chapter/10.1007%2F978-3-540-78197-4_20)
* P.  Piwek  and  E.  Krahmer,  ‘Presuppositions  in  Context:  Constructing Bridges’, in Formal Aspects of Context, eds., P. Bonzon, M. Cavalcanti,and R. Nossum, volume 20 of Applied Logic Series, 85–106, Kluwer Academic Publishers, Dordrecht, (2000).
* {#Ranta94} [[Aarne Ranta]], Type-theoretical grammar. Oxford University Press (1994)
* {#Sundholm86} [[Göran Sundholm]], _Proof theory and meaning_. In: Gabbay, D., Guenthner, F. (eds.) Handbook of Philosophical Logic, vol. 3, pp. 471&#8211;506. Springer (1986)
* Tanaka, R., Mineshima, K., Bekki, D.: Resolving modal anaphora in Dependent Type Semantics. In: Proceedings of LENLS11. pp. 43&#8211;56 (2014), [Springer](http://link.springer.com/chapter/10.1007%2F978-3-662-48119-6_7).

### Papers using homotopy type theory

* Bahramian, H., Nematollahi, N., Sabry, A.: Copredication in Homotopy Type Theory, [pdf](https://www.researchgate.net/publication/320704539_Copredication_in_homotopy_type_theory)
* [[David Corfield]], _Expressing 'the structure of' in homotopy type theory_, [webpage](https://ncatlab.org/davidcorfield/show/Expressing+%27The+Structure+of%27+in+Homotopy+Type+Theory)

A worked example, [[homotopy type theory]] in the [[Grammatical Framework]] 

* [GF-HoTT](http://www.grammaticalframework.org/~aarne/gf-hott/). 

###Talks

* [[Daisuke Bekki]], Anaphora and Presuppositions in [[Dependent Type Semantics]] (Theoretical side) [slides](http://www.u.tsukuba.ac.jp/~kubota.yusuke.fn/bekki1.pdf)
* [[Daisuke Bekki]], Anaphora and Presuppositions in Dependent Type Semantics (Empirical side) [slides](http://www.u.tsukuba.ac.jp/~kubota.yusuke.fn/bekki2.pdf)
* Ribeka Tanaka, Generalized Quantifiers in Dependent Type Semantics [slides](http://www.u.tsukuba.ac.jp/~kubota.yusuke.fn/tanaka.pdf)
* Yusuke Kubota and Robert Levine, Scope parallelism in coordination in
Dependent Type Semantics [slides](http://www.u.tsukuba.ac.jp/~kubota.yusuke.fn/kubota-levine.pdf)