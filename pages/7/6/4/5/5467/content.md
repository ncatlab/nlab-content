__G&#246;del's constructible universe__ is a [[proper class|subclass]] $L$ of the von Neumann universe $V$ defined by transfinite induction as $L = \cup_\alpha L_\alpha$ where 

$$L_0 = \emptyset$$

$$ L_{\alpha +1} = P(L_\alpha) \cap I(L_\alpha \cup \{L_\alpha\}) $$

and if $\alpha$ is a limit ordinal:

$$ L_\alpha = \cup_{\beta\lt \alpha} L_\beta$$

Here, for $X$ a set, by $I(X)$ we denote the smallest set containing $X$ and closed with respect to the operations of product, set difference, unordered pair, ordered pair, taking domain of a relation and performing the permutation of an ordered triple. 

The elements of the constructible universe are called __constructible sets__; the idea is similar to the [[constructible set]]s in topology and algebraic geometry. $L$ is a [[transitive set|transitive]] [[big class]] containing all the ordinals. In fact, it is the smallest transitive model of the set theory containing all the ordinals. On the other hand, the sets in this class can be effectively enumerated by von Neumann ordinals. The question weather $L\neq V$ can not be decided in ZF. If $L\neq V$ then still we do not know how, without an axiom of choice, to produce
specific sets which are not constructible. 

[[!redirects Gödel's constructible universe]]

