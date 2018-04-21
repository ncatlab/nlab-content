#Contents#
* table of contents 
{:toc}


## Definition

+-- {: .num_defn #CrossedGSet} 
###### Definition

Let $G$ be a [[group]]. A _crossed G-set_ consists of the following data.

1. A [[G-set]], that is to say, a set $X$ together with an [[action]] $\cdot : U(G) \times X \rightarrow X$ of $G$ upon it, where $U$ is the [[forgetful functor]] from [[Grp]] to [[Set]].

2. A map of sets $\left| - \right|: X \rightarrow U(G)$.

We require that $\left| g \cdot x \right| = g \left| x \right| g^{-1}$ for all $g \in G$ and $x \in X$.

=--

+-- {: .num_defn #MorphismOfCrossedGSets} 
###### Definition

Let $\underline{X}$ and $\underline{Y}$ be crossed $G$-sets. A _morphism_ from $\underline{X}$ to $\underline{Y}$ is a map of sets $f : X \rightarrow Y$ which is a morphism of $G$-sets, that is to say, $f(g \cdot x) = g \cdot f(x)$ for all $g \in G$ and $x \in X$, and which has the property that $\left| f(x) \right| = \left| x \right|$ for all $x \in X$.

=--

Crossed $G$-sets and morphisms between them assemble into a category. The identity morphism on a crossed $G$-set $\underline{X}$ is defined by the identity map $X \rightarrow X$. 

##Braided monoidal structure on the category of crossed G-sets

+-- {: .num_defn #MonoidalStructure} 
###### Definition

Let $\underline{X}$ and $\underline{Y}$ be crossed G-sets. The _tensor product_ of $\underline{X}$ and $\underline{Y}$ is the product of the underlying $G$-sets, namely the product of sets $X \times Y$ equipped with the action $g \cdot (x,y) = (g \cdot x, g \cdot y)$, equipped with the map $X \times Y \rightarrow U(G)$ given by $(x,y) \mapsto \left| x \right| \left| y \right|$.   

=--

Extending in the evident way to morphisms, the tensor product of crossed G-sets equips the category of crossed $G$-sets with the structure of a (not strict, and not symmetric) monoidal category. The unit is the set with one element equipped with its unique crossed $G$-set structure.

+-- {: .num_defn #BraidedMonoidalStructure} 
###### Definition

Let $\underline{X}$ and $\underline{Y}$ be crossed $G$-sets. The _braiding_ of $\underline{X}$ and $\underline{Y}$ is the morphism of crossed $G$-sets $X \times Y \rightarrow Y \times X$ given by $(x,y) \mapsto (\left| x \right| \cdot y, x)$. 

=--

The braiding of crossed $G$-sets gives rise, together with the monoidal structure of Definition \ref{MonoidalStructure}, to a braided monoidal structure on the category of crossed $G$-sets.

##References

* [[André Joyal]] and [[Ross Street]], _Braided tensor categories_ , Adv. Math. **102** (1993), 20--78.  (Example 5.1)