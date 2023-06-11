This article is about the twisted tensor product of a dga-algebra and a dg-coalgebra (and generalizations). For another notion of [[twisted tensor product of algebras]] see there. 

##Idea ##

In 1959, Edgar Brown introduced a _twisted tensor product_ to give an algebraic description of a [[fibration]]. The chain complex of a total space of a principal fibration is obtained as a small perturbation (at the level of a differential) of the [[chain complex]] of the trivial fibration (hence a [[tensor product]] of chain complexes of the base and of the fiber). It is the analogue for differential algebra of the [[twisted cartesian product]] construction in the theory of simplicial fibre bundles.

##Definition##

Let $C$ be a dg-[[coalgebra]], $A$ a [[dg-algebra]], $\tau:C\to A$ the [[twisting cochain]], $L$ a right $C$-dg-co[[module]] with co[[action]] $\delta_L:L \to L\otimes C$ and $M$ a left $A$-dg-module with action $m_M:M\otimes A\to A$. The __twisted tensor product__ $L\otimes_\tau M$ is the chain complex that coincides with the ordinary tensor product $L\otimes M$ as a [[graded vector space|graded module]] over the [[ground ring]], and whose differential $d_\tau$ is given by 
$$
d_\tau = d_L\otimes 1 + 1\otimes d_M + (1\otimes m_M)\circ(1\otimes\tau\otimes 1)\circ(\delta_L\otimes 1).
$$ 

##Literature##

* Edgar H. Brown Jr. _Twisted tensor products I_, 
Annals of Math. (2) 69 1959 223--246.

* V. A. Smirnov, _Simplicial and operadic methods in algebraic topology_, Translations of mathematical monographs 198, AMS, Providence, Rhode Island 2001. 

* [[Kenji Lefèvre-Hasegawa]], _Sur les $A_\infty$-catégories_, [thesis](https://arxiv.org/abs/math/0310337), (Université Denis Diderot – Paris 7, Paris, November 2003).  Corrections, by B. Keller, available [here]( http://people.math.jussieu.fr/~keller/lefevre/publ.html).

* Manuel Rivera, [[Mahmoud Zeinalian]], _The colimit of an ∞-local system as a twisted tensor product_, Higher Structures 4(1), (2020) [higher-structures4.1](https://higher-structures.math.cas.cz/api/files/issues/Vol4Iss1/RiveraZeinalian) [arXiv:1805.01264](https://arxiv.org/abs/1805.01264) mpg:[pdf](https://pure.mpg.de/rest/items/item_3366473/component/file_3366474/content)

