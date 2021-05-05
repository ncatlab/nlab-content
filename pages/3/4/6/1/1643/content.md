
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Binary operations
* table of contents
{: toc}

## Definitions

A __binary operation__ on a [[set]] $S$ is a [[function]] $(-)\cdot (-) \colon S \times S \to S$ from the [[Cartesian product]] $S \times S$ to $S$.  A __magma__ (or binary algebraic structure, or, alternatively, a mono-binary algebra) $(S,\cdot)$ is a set equipped with a binary operation on it. 

A magma is called

* _[[unital magma|unital]]_ if it has a [[identity element|neutral element]] $1$, hence an element $1 \in S$ in that $1 \cdot x = x = x \cdot 1$  Some authors mean by 'magma' what we call a unital magma (cf. [[Borceux-Bourn]] Def. 1.2.1). One can consider one-sided unital elements separately: $1_L \cdot x = x$ and/or $x = x \cdot 1_R$. Units may be far from unique.

* _[[commutative magma|commutative]]_ if the binary operation takes the same value when its two arguments are interchanged: $x \cdot y = y \cdot x$;

* _[[associative magma|associative]]_ if the binary operation satisfies the [[associativity]] condition $(x \cdot y) \cdot z = x \cdot (y \cdot z)$. 

The term 'magma' is from [[Bourbaki]] and intends to suggest the fluidity of the concept; special cases include [[semigroups]]/[[monoids]], [[quasigroups]], [[groups]], and so on.  The term 'groupoid' is also used, but here that word means [[groupoid|something else]] (see also related discussion at [[historical notes on quasigroups]]).

More generally, in any [[multicategory]] $M$, a **magma object** or **magma in $M$** is an [[object]] $X$ of $M$ equipped with a [[multimorphism]] $m: X, X \to X$ in $M$.  Here the multimorphism from $X$ and $X$ to $X$ is a __binary operation in $M$__.  In particular, for $M$ a [[monoidal category]], a magma structure on $X$ is a [[morphism]] $m\colon X \otimes X \to X$; and in a [[closed category]], a magma structure on $X$ is a morphisms $m\colon X \to [X, X]$.

## Properties

The [[Eckmann-Hilton argument]] holds for unital magma structures: two compatible ones on a set must be equal, associative and commutative.

## Related concepts

* [[magmoid]]


## Literature

The wikipedia entry [magma](http://en.wikipedia.org/wiki/Magma_%28algebra%29) is quite useful, having a list and a table of various subclasses of magmas, hence of binary algebraic structures. 

* [[eom]]: [magma](http://www.encyclopediaofmath.org/index.php?title=m/m110040)
* R.H. Bruck, _A survey of binary systems_, Springer-Verlag 1958


category: algebra

[[!redirects magmas]]

[[!redirects binary operation]]
[[!redirects binary operations]]

[[!redirects binary algebraic structure]]

[[!redirects magma object]]
[[!redirects magma objects]]
