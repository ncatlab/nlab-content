##Idea ##
In 1959, Edgar Brown introduced a _twisted tensor product_ to give an algebraic description of a [[fibration]]. The chain complex of a total space of a principal fibration is obtained as a small perturbation (at the level of a differential) of the [[chain complex]] of the trivial fibration (hence a [[tensor product]]).

##Definition##
Let $C$ be a [[dg-algebra]], $A$ a dg-[[coalgebra]], $\tau:C\to A$ the [[twisting cochain]], $L$ a right $C$-dg-co[[module]] with co[[action]] $\delta_L:L\otimes C$ and $M$ a left $A$-dg-module with action $m_M:M\otimes A\to A$. The __twisted tensor product__ $L\otimes_\tau M$ is the chain complex that coincides with the ordinary tensor product $L\otimes M$ as a [[graded vector space|graded module]] over the ground ring, and whose differential $d_\tau$ is given by 
$$
d_\tau = d_L\otimes 1 + 1\otimes d_M + (1\otimes m_M)\circ(1\otimes\tau\otimes 1)\circ(\delta_L\otimes 1).
$$ 

##Literature##

Brown, Edgar H., Jr. Twisted tensor products. I. 
Annals of Math. (2) 69 1959 223--246.

V. A. Smirnov, Simplicial and operadic methods in algebraic topology, Translations of mathematical monographs 198, AMS, Providence, Rhode Island 2001. 

Lefevre-Hasegawa thesis (Paris) 

