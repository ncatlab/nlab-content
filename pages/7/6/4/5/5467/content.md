
# The constructible universe
* table of contents
{: toc}

## Definition

__G&#246;del's constructible universe__ is a [[proper class|subclass]] $L$ of the von Neumann universe $V$ of well-founded [[pure sets]], defined by [[transfinite induction]] as $L = \bigcup_\alpha L_\alpha$ where 

$$L_0 = \emptyset$$

$$ L_{\alpha +1} = P(L_\alpha) \cap I(L_\alpha \cup \{L_\alpha\}) $$

and if $\alpha$ is a limit ordinal:

$$ L_\alpha = \bigcup_{\beta\lt \alpha} L_\beta$$

Alternatively, we may say that
$$ L_\alpha = \bigcup_{\beta \lt \alpha} P(L_\beta) \cap I(L_\beta \cup \{L_\beta\}) $$
for any ordinal $\alpha$ ($0$, successor, or limit).

Here, for $X$ a pure set, by $I(X)$ we denote the smallest set containing $X$ and closed with respect to the operations of [[Cartesian product]], [[relative complement|set difference]], [[unordered pair]], [[pairing|ordered pair]], taking the [[domain]] of a [[binary relation]], and performing a [[permutation]] of an ordered triple. 

The elements of the constructible universe are called __[[constructible sets]]__; the idea is similar to the [[constructible sets]] in topology and algebraic geometry. 


## Properties

$L$ is a [[transitive set|transitive]] [[big class]] containing all the ordinals. In fact, it is the smallest transitive model of the set theory containing all the ordinals. On the other hand, the sets in this class can be effectively enumerated by von Neumann ordinals. The question weather $L\neq V$ can not be decided in ZF. If $L\neq V$ then still we do not know how, without an axiom of choice, to produce
specific sets which are not constructible. 


## Links

The wikipedia entry [constructible universe](http://en.wikipedia.org/wiki/Constructible_universe) is pretty elaborate. 


[[!redirects constructible universe]]
[[!redirects Gödel's constructible universe]]
[[!redirects Gödel's constructible universe]]
[[!redirects Godel's constructible universe]]
[[!redirects Godel's constructible universe]]
