

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

The [[action]] of a [[topological group]] $G$ on a [[topological space]] $X$ is called a _proper action_ if the [[continuous function]]

$$
  \array{
    G \times X &\longrightarrow& X \times X
    \\
    (g,x) &\mapsto& (g\cdot x, x)
  }
$$

is a [[proper continuous function]].

## Examples

### Lie group actions on smooth manifolds

+-- {: .num_prop #SmoothActionOfCompactLieGroupOnSmoothManifoldIsProper} 
###### Proposition

Let $X$ be a [[smooth manifold]] and let $G$ be a [[compact Lie group]].
Then every [[smooth function|smooth]] [[action]] of $G$ on $X$ is [[proper action|proper]].

=--

(e.g. [Lee 12, Cor. 7.2](#Lee12))

For more see at _[[equivariant differential topology]]_.

## Related concepts

* [[properly discontinuous action]]

* [[free action]], [[semi-free action]], [[transitive action]], [[regular action]]

* [[equivariant differential topology]]

## References

For instance

* {#Kankaanrinta07} [[Marja Kankaanrinta]], Def. 2.1 in _Equivariant collaring, tubular neighbourhood and gluing theorems for proper Lie group actions_,     Algebr. Geom. Topol. Volume 7, Number 1 (2007), 1-27 ([euclid:agt/1513796653](https://projecteuclid.org/euclid.agt/1513796653))

* {#Lee12} [[John Lee]], around p. 147 of: _Introduction to Smooth Manifolds_, Springer 2012 ([doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [pdf](https://lost-contact.mit.edu/afs/adrake.org/usr/rkh/Books/books/Introduction%20to%20Smooth%20Manifolds%20-%20J.%20Lee.pdf))

See also

* [[John Lee|J. Lee]], [MO comment](https://math.stackexchange.com/a/989168/58526), Oct 2014


[[!redirects proper actions]]

[[!redirects proper group action]]
[[!redirects proper group actions]]

