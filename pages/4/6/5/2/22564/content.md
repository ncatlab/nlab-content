+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# N-ary operations
* table of contents
{: toc}

## Definitions

Given a [[natural number]] $n$, an __n-ary operation__ on a [[set]] $S$ is a [[function]] 

$$
  \phi
  \;\colon\;
  \big(
    \mathrm{Fin}(n) \to S
  \big) 
  \longrightarrow 
  S
$$ 

from the [[function set]] $\mathrm{Fin}(n) \to S$ to $S$ itself, where $\mathrm{Fin}(n)$ is the [[finite set]] with $n$ elements. 

The __arity__ of the operation is $n$. 

In general, if the natural number $n$ is not specified, these are called **finitary operations**. 

Sets equipped with finitary operations are also called **finitary [[magmas]]** (or "finitary groupoids" in older terminology which now clashes with another meaning of *[[groupoid]]*, see at *[[historical notes on quasigroups]]*). 

More generally, a finitary operation in a [[multicategory]] is just a [[multimorphism]]. 

### Arbitrary arity

More generally, one could use an arbitrary [[set]] instead of a [[finite set]]. However, the generalizations are only definable in [[closed monoidal category|closed]] [[multicategories]], rather than any [[multicategory]]. 

## Properties

Every set $S$ with an $n$-ary operation $\phi$ comes with an [[endomorphism]] called the *$n$-th [[power operation]]*

$$
  \array{
    S
    & 
    \overset{\;\;(-)^n\;\;}{\longrightarrow} 
    &
    S
    \\
    x
    &\mapsto&
    \phi \circ diag_n(x)
    \,,
  }
$$ 

where $ S \overset{diag_n}{\longrightarrow} S^n$ is the [[diagonal morphism]].

## See also

* [[magma]]

* [[monoid]]

* [[operation]]

* [[multicategory]]

* [[operad]]

### $n$-ary algebraic structures

* [[n-ary semigroup]]

* [[n-ary quasigroup]]

* [[n-ary group]]

* [[group]]

## References

* Wikipedia, [n-ary group](https://en.wikipedia.org/wiki/N-ary_group)

[[!redirects n-ary operation]]
[[!redirects n-ary operations]]

[[!redirects n-ary magma]]
[[!redirects n-ary magmas]]

[[!redirects finitary operation]]
[[!redirects finitary operations]]

[[!redirects finitary magma]]
[[!redirects finitary magmas]]