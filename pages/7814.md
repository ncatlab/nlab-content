
#Contents#
* table of contents
{:toc}

## Idea

The term "support" means different things in different parts of mathematics:

### In set theory

There are two slightly different notions of support in set theory, one which is the generalization of the notion of support in [[real analysis]] and one which is a special case of [[image factorization]]/[[truncations]] commonly used in [[dependent type theory|dependent type theoretic]] and [[category theory|categorical]] models of [[set theory]]. 

Given a [[pointed set]] $A$ with specified [[element]] $0 \in A$, a [[set]] $X$, and a [[function]] $f \colon X \to A$, the _support_ of $f$ is the [[subset]] of $X$ on which $f$ is not equal to $0$.

The *support set* $[X]$ of any set $X$ is the [[image]] of the unique function into any [[singleton]] $X \to 1$, and is thus a [[subsingleton]], and a [[singleton]] if $X$ is pointed. Note that this is different from the support of the unique function $X \to 1$, which is always the [[empty set]] $\emptyset$. 

### In category theory

The above definitions could be interpreted not just in [[Set]] but in any [[category]] with a [[terminal object]]. This leads to the notions of [[support of a morphism]] and [[support object]]. 

The [[support object]] of an [[object]] $A$ of a [[category]] is the [[image]] of its map to the [[terminal object]]. In the [[internal logic]] of a category, this corresponds to the [[propositional truncation]].

### In topology
 {#InTopology}

In [[topology]] the support of a [[continuous function]] $f \colon X \to A$ as above is the [[topological closure]] of the set of points on which $f$ does not vanish:

$$
  Supp(f) = Cl(\{x \in X \vert f(x) \neq 0 \in A\})
  \,.
$$

If $Supp(f) \subset X$ is a [[compact subspace]], then one says that $f$ has _[[compact support]]_.

### In functional analysis

* [[support of a distribution]]

### In measure theory

* [[tau-additive measure#null_sets_and_support|Support of a measure]]
* [[valuation (measure theory)#null_sets_and_support|Support of a valuation]]

### In field theory

* [[spacetime support]]

## Related concepts

* [[compact support]]

* [[compactly supported cohomology]]

* [[split support]]

## References

* Wikipedia, _[Support (mathematics)](https://en.wikipedia.org/wiki/Support_%28mathematics%29)_


[[!redirects supports]]

[[!redirects support set]]
[[!redirects support sets]]
