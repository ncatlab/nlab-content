[[!redirects Feynman categories]]

## Definition

Let $C$ be a groupoid, $C^\otimes$ the free symmetric monoidal category on $C$ and $M$ a symmetric monoidal category. 

([Kaufman 2017, Defn 2.1](#Kaufman17)) A symmetric strong monoidal functor $\tau: C^\otimes\to M$ is a __Feynman category__ if the following are satisfied

* _isomorphisms condition_: $\tau^\otimes$ induces an equivalence of symmetric monoidal categories $C^\otimes \cong M_{iso}$
* _hereditary condition_: $\tau$ and $\tau^\otimes$ induce an equivalence of symmetric monoidal categories  $(C\downarrow M)^\otimes_{iso}\cong(M\downarrow M)_{iso}$
* _size condition_: For any $\ast \in C$, $(M \downarrow \ast)$ is [[essentially small]].

(Getzler 2009) A symmetric strong monoidal functor $\tau: C^\otimes\to M$ is a __regular pattern__ if the following are satisfied

* $\tau$ is [[essentially surjective functor|essentially surjective]]
* the induced functor of presheaves $\tau^{\hat{}} : M^{\hat{}}\to (C^\otimes)^{\hat{}}$ is strong monoidal for the [[Day convolution]] product

The latter condition on [[comma categories]] ensures the existence of certain (pointed) [[Kan extension]]s. 

## Literature

Related items include [[operad]], [[Feynman transform]].

The axiomatics is proposed in

*  Ralph M. Kaufmann, Benjamin C. Ward, _Feynman categories_, Astérisque
387 (2017), vii+161pp. [arxiv/1312.1269](https://arxiv.org/abs/1312.1269)

A more recent survey is in 

* {#Kaufman17} Ralph M. Kaufmann, _Lectures on Feynman categories_, [arxiv:1702.06843](https://arxiv.org/abs/1702.06843)

A representation-theoretical viewpoint is given in 

* Ralph M. Kaufmann, _Feynman categories and Representation Theory_, ([arXiv:1911.10169](https://arxiv.org/abs/1911.10169)) 

A useful generalization is exhibited in 

* Ralph M. Kaufmann, Jason Lucas, _Decorated Feynman categories_, [arxiv/1602.00823](https://arxiv.org/abs/1602.00823)

Certain bialgebras and Hopf algebras appear by universal constructions in the setting of Feynman categories:

*  Imma Gálvez-Carrillo, Ralph M. Kaufmann, Andrew Tonks, _Three Hopf algebras and their common simplicial and categorical background_, [arxiv:1607.00196](https://arxiv.org/abs/1607.00196)

> We consider three a priori totally different setups for Hopf algebras from number theory, mathematical physics and algebraic topology. These are the Hopf algebras of Goncharov for multiple zeta values, that of Connes--Kreimer for renormalization, and a Hopf algebra constructed by Baues to study double loop spaces. We show that these examples can be successively unified by considering simplicial objects, cooperads with multiplication and Feynman categories at the ultimate level. These considerations open the door to new constructions and reinterpretation of known constructions in a large common framework. 


Role of left [[Kan extension]]s of specific kind in operadic theory, including in the setup of Feynman categories is investigated in

*  Mark Weber, _Algebraic Kan extensions along morphisms of internal algebra classifiers_, [arxiv/1511.04911](https://arxiv.org/abs/1511.04911)

Getzler's axiomatics of regular patterns is similar in spirit to Feynman categories.

* [[Ezra Getzler]], _Operads revisited_, in: Algebra, arithmetic, and geometry: in honor of Yu. I. Manin. Vol. I, vol. 269 of Progr. Math., pp. 675–698 (2009) [math/0701767](https://arxiv.org/abs/math/0701767)

A comparison of both with related notions like Day-Street [[substitude]]s as well as [[colored operad]]s is in 

* Michael Batanin, Joachim Kock, Mark Weber, _Regular patterns, substitudes, Feynman categories and operads_, [arxiv/1510.08934](https://arxiv.org/abs/1510.08934)

A connection of Feynman categories to (a generalization of) profunctors and to rewriting systems within a proposal to categorification of the [[cyclic operad]]s are exhibited in

* Pierre-Louis Curien, Jovana Obradović, _Categorified cyclic operads_, [arxiv/1706.06788](https://arxiv.org/abs/1706.06788) 

Interesting pair of functors (not an adjoint pair!) between operadic categories and Feynman categories is among the topics studied in

* M. Batanin, M. Markl, _Koszul duality for operadic categories_, [arxiv.org/abs/1812.02935](https://arxiv.org/abs/1812.02935)