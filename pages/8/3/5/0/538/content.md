#Definition#

A **coproduct** of two [[object|objects]] $a,b$ in a [[category]] $C$ is an object $a+b$ (also written $a\sqcup b$, especially when it is [[disjoint coproduct|disjoint]]) equipped with [[morphism|morphisms]] $i:a\to a+b$ and $j:b\to a+b$ such that for any object $c$ with morphisms $f:a\to c$ and $g:b\to c$, there is a unique morphism $p:a+b\to c$ such that $p \circ i=f$ and $p \circ j=g$.

This map $p$ is called the __[[copairing]]__ of $f$ and $g$ and is often denoted $[f,g]$ or $\{f,g\}$ or (when possible) given vertically:
$$\left\{{f \atop g}\right\}$$

# Remarks #

* When they exist, coproducts are unique up to unique canonical isomorphism, so we often say "[[generalized the|the]] coproduct."
* One can define in a similar way a coproduct of any family of objects.  A coproduct of the [[empty set|empty]] family is an [[initial object]].
* A coproduct is a special case of a [[colimit]] in which the diagram category is [[discrete category|discrete]].
* A coproduct in $C$ is the same as a [[product]] in the [[opposite category]] $C^{op}$.

[[!redirects coproducts]]