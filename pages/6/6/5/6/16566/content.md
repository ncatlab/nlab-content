
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An **arithmetic pretopos** is a [[pretopos]] $C$ with a _[parameterized natural numbers object](natural+numbers+object#in_a_symmetric_monoidal_category)_. A **list-arithmetic pretopos** is a pretopos with all _parameterized list objects_ ([Maietti 10, 2.6](#Maietti10)).

Using the (equivalent) definition given in [Cockett 1990](#Cockett90), a **parameterized list object** is a [[W-type]] for the [[polynomial functor]] $B+ A\times(-)\colon C\to C$. This definition makes sense since a pretopos has [[finite products]] and [[disjoint coproducts]] (here denoted "$+$").


Discussion via its [[internal language]], which is a [[dependent type theory]]... ([Maietti 05](#Maietti05), [Maietti 10, p.6](#Maietti10)).

Maietti ([05](#Maetti05),[10](#Maetti10)) proposed that list-arithmetic pretoposes serve as the **arithmetic universes** that [[André Joyal]] (cf. [Joyal 05](#Joyal05)) once suggested to use for discussion of [[incompleteness theorems]] (cf. [van Dijk/Oldenziel 2020](#VanDijkOldenziel)); they are used directly as the definition of arithmetic universes e.g. in ([Maietti-Vickers 2012](#MaiettiVickers12)).

## First-order Peano arithmetic

In classical logic, [first-order Peano arithmetic](https://ncatlab.org/nlab/show/Peano+arithmetic#firstorder_peano_arithmetic) is often called "PA".  Unlike [second-order Peano arithmetic](https://ncatlab.org/nlab/show/Peano+arithmetic#secondorder_peano_arithmetic), this theory does not have a unique model up to isomorphism in the category of sets: there is an initial model, called the 'standard' model of the natural numbers, but also others called 'nonstandard'.  It is interesting to ask how we can rephrase and also generalize PA using the concept of arithmetic pretopos.   The following is a tentative proposal put forth by Sridhar Ramesh:

> Let me expand on why the initial Heyting/Boolean pretopos with a parametrized NNO is equivalent to first-order intuitionistic/classical PA. [By "intuitionistic PA", I mean the same thing as what is standardly called "Heyting Arithmetic".]

> Remember, intuitionistic/classical PA is the first-order intuitionistic/classical theory with a sort $N$, a zero element $0 : N$, a successor function $S : N \to N$, operations $+ : N \times N \to N$ and $\times : N \times N \to N$, axioms stating that $S$ is injective, $0$ is not in the range of $S$, recurrence identities $x + 0 = x$, $x + S(y) = S(x + y)$, $x \times 0 = 0$, $x \times S(y) = x \times y + x$, and the induction schema, which says any definable (in the sense of first-order definable in this language by a relation with parameters) subset of $N$ which contains $0$ and is closed under $S$ must contain all of $N$.

> So, let's see that a Heyting/Boolean pretopos with parameterized NNO proves everything first-order intuitionistic/classical PA proves: An NNO is an initial algebra for the $T \mapsto 1 + T$ endofunctor, and thus by Lambek's lemma, we obtain an isomorphism between $1 + N$ and $N$, where $N$ is the carrier of the NNO and the isomorphism is given by the combination of zero and successor. This being an isomorphism says in the internal language of the pretopos that every element of $N$ is precisely one of zero or a successor (not both; thus, $0$ is not in the range of the successor map) and that the successor map is injective.

> Furthermore, our recurrence identities for $+$ and $\times$ directly describe how to define unique operators satisfying those recurrences on a parametrized NNO.

> Finally, note that Heyting pretoposes are "closed under" first-order definability, so to speak (this is their raison d'être as a concept), so that any first-order definable relation $R(n, x)$ on $N$ and some other tuples of sorts $X$ in this language will correspond to some subobject of $N \times X$ in this pretopos. The set $\{x : X \mid R(0, x) \wedge \forall n : N \left( R(n, x) \Rightarrow R(S(n), x) \right) \}$ is first-order definable as a subobject of $X$ in this pretopos, and by passing to the slice category over it, we obtain another pretopos, where $N$ remains an NNO. In this slice pretopos, $\{n : N \mid R(n, x) \}$ is a subobject of $N$ which contains $0$ and is closed under $S$; thus, a sub-algebra of $N$ as algebras for the $T \mapsto 1 + T$ endofunctor. But as $N$ is an initial algebra, it is isomorphic to this subalgebra (any subobject of an initial object is isomorphic to the initial object). Thus, in this slice pretopos over $\{x : X \mid R(0, x) \wedge \forall n : N \left( R(n, x) \Rightarrow R(S(n), x) \right) \}$, we have established $\forall n : N, R(n, x)$, which amounts to having established the parametrized induction schema in our original pretopos.

> Given the closure of Heyting/Boolean pretoposes under the derivations of first-order intuitionistic/classical logic, this concludes showing that a Heyting/Boolean pretopos with parametrized NNO proves in its internal language everything that first-order intuitionistic/classical PA does.

> In the other direction, it's well-known how any first-order intuitionistic/classical logical theory gives rise to a Heyting/Boolean pretopos as its "syntactic category" in a suitable sense. We've just seen that when we apply this construction to first-order intuitionistic/classical PA, we get something "no stronger" than the initial Heyting/Boolean pretopos with a parametrized NNO. But what may not be obvious is that these are indeed equal; that we actually get the full structure of an NNO in the syntactic category for PA.

> The induction schema guarantees the uniqueness aspect of algebra maps out of $N$, but their existence is not obvious. This existence however is granted by Gödel's Chinese remainder theorem trick showing how "primitive recursions" of functions from naturals to tuples of naturals can be defined in a first-order way using $+$ and $\times$.

## Related entries

* [[free monoid]]

* [[Gödel's incompleteness theorem]]

* [[Lawvere's fixed point theorem]]

* [[classifying topos for the theory of objects]]

* [[ΠW-pretopos]]

* [[strongly predicative dependent type theory]]

## References

* {#Cockett90} [[Robin Cockett]], _List-arithmetic distributive categories: Locoi_, JPAA **66** no.1 (1990) pp.1-29.

* {#Cockett97} [[Robin Cockett]], _Finite objects in a locos_, JPAA **116** (1997) pp.169-183.

* {#vanDijkOldenziel20} Joost van Dijk, Alexander Gietelink Oldenziel, _Gödel's Incompleteness after Joyal_, arXiv:2004.10482 (2020). ([abstract](https://arxiv.org/abs/2004.10482))

* {#Joyal05} [[André Joyal]], _The G&#246;del incompleteness theorem, a categorical approach_, (abstract) Amiens 2005, Cah. Top. G&#233;om. Diff. Cat. **46** no.3 (2005) p.202. ([numdam](http://www.numdam.org/item/CTGDC_2005__46_3_163_0))

* {#Maietti05a} [[Maria Maietti]], _Reflection Into Models of Finite Decidable FP-sketches in an Arithmetic Universe_, Electronic Notes in Theoretical Computer Science
**122** (2005) 105-126 &lbrack;[doi:10.1016/j.entcs.2004.06.054](https://doi.org/10.1016/j.entcs.2004.06.054)&rbrack;

* {#Maietti05} [[Maria Maietti]], _Modular correspondence between dependent type theories and categories including pretopoi and topoi_, Mathematical Structures in Computer Science **15**  6 (2005) 1089-1149 &lbrack;[doi:10.1017/S0960129505004962](https://doi.org/10.1017/S0960129505004962), [pdf](https://www.math.unipd.it/~maietti/papers/tumscs.pdf)&rbrack;

* {#Maietti10} [[Maria E. Maietti]], _Joyal's arithmetic universe as list-arithmetic pretopos_, TAC **24** 3 (2010) 39-83 &lbrack;[tac:24-03](http://www.tac.mta.ca/tac/volumes/24/3/24-03abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/24/3/24-03.pdf)&rbrack;

* {#MaettiVickers12} [[Maria E. Maietti]], [[Steve Vickers]], _An induction principle for consequence in arithmetic universes_, JPAA **216** (2012) pp.2049-2067. &lbrack;[doi:10.1016/j.jpaa.2012.02.040](https://doi.org/10.1016/j.jpaa.2012.02.040), [pdf](http://www.math.unipd.it/~maietti/papers/aumv12.pdf)&rbrack;

* [[Sridhar Ramesh]], comments on the Category Theory Community Server.   &lbrack;[web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Godel's.20Second.20IT.20vs.20Category.20Theory/near/440728238)&rbrack;

* [[Paul Taylor]], _Inside Every Model of Abstract Stone Duality Lies an Arithmetic Universe_, Electronic Notes in Theoretical Computer Science **122** (2005) 247-296 &lbrack;[doi:10.1016/j.entcs.2004.06.059](https://doi.org/10.1016/j.entcs.2004.06.059)&rbrack;

* {#Vickers16} [[Steve Vickers]], _Sketches for arithmetic universes_, arXiv:1608.0159 (2016) &lbrack[arXiv:1608.01559](http://arxiv.org/abs/1608.01559)&rbrack;

* {#Vickers17} [[Steve Vickers]], _Arithmetic universes and classifying toposes_ &lbrack;[arXiv:1701.04611](https://arxiv.org/abs/1701.04611)&rbrack;

[[!redirects arithmetic pretoposes]]
[[!redirects arithmetic pretopoi]]

[[!redirects list-arithmetic pretopos]]
[[!redirects list-arithmetic pretoposes]]
[[!redirects list-arithmetic pretopoi]]

[[!redirects arithmetic universe]]
[[!redirects arithmetic universes]]
