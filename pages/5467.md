
# The constructible universe
* table of contents
{: toc}

## Definition

__G&#246;del's constructible universe__ $L$ is a [[proper class|subclass]] of the von Neumann universe $V$ of well-founded [[pure sets]]. It is defined by [[transfinite induction]] as $L = \bigcup_\alpha L_\alpha$ where 

$$L_0 = \emptyset$$

$$ L_{\alpha +1} = P(L_\alpha) \cap I(L_\alpha \cup \{L_\alpha\}) $$

and if $\alpha$ is a limit ordinal:

$$ L_\alpha = \bigcup_{\beta\lt \alpha} L_\beta$$

Here, for $X$ a pure set, by $I(X)$ we denote the smallest set containing $X$ and closed with respect to the operations of [[Cartesian product]], [[relative complement|set difference]], [[unordered pair]], [[pairing|ordered pair]], taking the [[domain]] of a [[binary relation]], and performing a [[permutation]] of an ordered triple. 

Alternatively, we may say that
$$ L_\alpha = \bigcup_{\beta \lt \alpha} P(L_\beta) \cap I(L_\beta \cup \{L_\beta\}) $$
for any ordinal $\alpha$ ($0$, successor, or limit).

The elements of the constructible universe are called __[[constructible sets]]__; the idea is similar to the [[constructible sets]] in topology and algebraic geometry. 


## Properties

$L$ is a [[transitive set|transitive]] [[big class]] containing all the ordinals. In fact, it is an (inner) model of the set theory (consider ZF), the smallest transitive containing all the ordinals. The sets in this class can be effectively enumerated by von Neumann ordinals. Indeed, we can well-order all sets and the axiom of choice holds in the model. And even the generalized continuum hypothesis holds for L as a model. Properties of sets in the set theory might not hold as seen from within the inner model.

One may add the axiom $L=V$ to set theory, i.e. collapsing the von Neumann universe $V$ to the "thinner" $L$. However, note that formally stating that axiom is more technical (involving ordinals, etc.) than the standard set theory axioms. The question weather $L\neq V$ can not be decided in ZF. If $L\neq V$ then we still do not know how, without an axiom of choice, to produce specific sets that are not constructible. 


## Links

The wikipedia entry [constructible universe](http://en.wikipedia.org/wiki/Constructible_universe) is pretty elaborate. 


[[!redirects constructible universe]]
[[!redirects Gödel's constructible universe]]
[[!redirects Gödel's constructible universe]]
[[!redirects Godel's constructible universe]]
[[!redirects Godel's constructible universe]]
