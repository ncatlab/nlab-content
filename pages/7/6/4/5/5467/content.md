
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# The constructible universe
* table of contents
{: toc}

## Definition

__G&#246;del's constructible universe__ $L$ is a [[proper class|subclass]] of the [[von Neumann universe]] $V$ of well-founded [[pure sets]]. It is defined by [[transfinite induction]] as $L = \bigcup_\alpha L_\alpha$ where 

$$L_0 = \emptyset$$

$$ L_{\alpha +1} = P(L_\alpha) \cap I(L_\alpha \cup \{L_\alpha\}) $$

and if $\alpha$ is a limit ordinal:

$$ L_\alpha = \bigcup_{\beta\lt \alpha} L_\beta$$

Here, for $X$ a pure set, by $I(X)$ we denote the smallest set containing $X$ and closed with respect to the operations of [[Cartesian product]], [[relative complement|set difference]], [[unordered pair]], [[pairing|ordered pair]], taking the [[domain]] of a [[binary relation]], and performing a [[permutation]] of an ordered triple. This definition, while less technical, offers different levels than the standard set-theoretical definition, for example the ordinal $\alpha$ need not be a member of $L_{\alpha+1}$.

Alternatively, we may say that
$$ L_\alpha = \bigcup_{\beta \lt \alpha} P(L_\beta) \cap I(L_\beta \cup \{L_\beta\}) $$
for any ordinal $\alpha$ ($0$, successor, or limit).

The elements of the constructible universe are called __[[constructible sets]]__; the idea is similar to the [[constructible sets]] in topology and algebraic geometry. 

[[AnonymousCoward]]: Does there exist a [[structural set theory]] definition of a constructible set and the constructible universe?


## Properties

$L$ is a [[transitive set|transitive]] [[big class]] containing all the ordinals.

There is a standard definition of a well-ordering of $L$, <${}_L$, therefore the sets in this class can be effectively enumerated by von Neumann ordinals, via the ranking function of <${}_L$.


## As inner model
In fact, $L$ is a model of the set theory (consider ZF), namely the smallest transitive class containing all the ordinals. Indeed, we can well-order all sets by a well-ordering <${}_L$ and therefore the axiom of choice holds in $L$. The generalized continuum hypothesis also holds in $L$.
Note that properties that hold in $V$ need not hold in $L$.


## Relation to the von Neumann universe

$L=V$ is an axiom which states that every set is in $L$. This collapses the [[von Neumann universe]] $V$ to the "thinner" inner model $L$. The question of whether $L\neq V$ can not be decided in ZF. If $L\neq V$ then we still do not know how, without an axiom of choice, to produce specific sets that are not constructible.

Given the independence, one may add $L=V$ as an axiom. However, note that formally stating that axiom is more technical (involving ordinals, etc.) than the standard set theory axioms. Moreover, by its restrictiveness, that axiom also rules out many other popular studied axioms (e.g. it is inconsistent with the existence of "large" [[large cardinals]] such as [[measurable cardinals]] and above).


## References

* [[Richard Matthews]], [[Michael Rathjen]], _Constructing the Constructible Universe Constructively_ &lbrack;[arxiv:2206.08283](https://arxiv.org/abs/2206.08283)&rbrack;

See also:

* Wikipedia, *[Constructible universe](http://en.wikipedia.org/wiki/Constructible_universe)*



[[!redirects constructible universe]]

[[!redirects constructible universes]]

[[!redirects Gödel's constructible universe]]
[[!redirects Gödel's constructible universe]]
[[!redirects Godel's constructible universe]]
[[!redirects Godel's constructible universe]]
