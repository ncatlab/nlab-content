
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

[[AnonymousCoward]]: Does there exist a [[structural set theory]] definition of a constructible set and the constructible universe?


## Properties

$L$ is a [[transitive set|transitive]] [[big class]] containing all the ordinals.

The sets in this class can be effectively enumerated by von Neumann ordinals. 


## As inner model
In fact, $L$ is a model of the set theory (consider ZF), namely the smallest transitive class containing all the ordinals. Indeed, we can well-order all sets and the axiom of choice holds for $L$ as a model. And even the generalized continuum hypothesis holds for $L$ as a model. 
Note that properties of sets in the set theory might not hold as seen from within the inner model.


## Relation to the von Neumann universe

By $L=V$, set theories refer to the collapsing of the von Neumann universe $V$ to the "thinner" $L$. The question of whether $L\neq V$ can not be decided in ZF. If $L\neq V$ then we still do not know how, without an axiom of choice, to produce specific sets that are not constructible.

Given the independence, one may add $L=V$ as an axiom. However, note that formally stating that axiom is more technical (involving ordinals, etc.) than the standard set theory axioms. Moreover, by its restrictiveness, that axiom also rules out many other popular studied axioms (e.g. it is inconsistent with the existence of "large" [[large cardinals]] such as [[measurable cardinals]] and above).


## Links

* The wikipedia entry [constructible universe](http://en.wikipedia.org/wiki/Constructible_universe) is pretty elaborate.

* Richard Matthews, Michael Rathjen, _Constructing the Constructible Universe Constructively_, [arxiv](https://arxiv.org/abs/2206.08283)


[[!redirects constructible universe]]
[[!redirects Gödel's constructible universe]]
[[!redirects Gödel's constructible universe]]
[[!redirects Godel's constructible universe]]
[[!redirects Godel's constructible universe]]
