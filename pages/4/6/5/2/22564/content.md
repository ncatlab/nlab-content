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

Given a [[cardinal number]] $n$, an __n-ary operation__ on a [[set]] $S$ is a [[function]] 

$$
  \phi
  \;\colon\;
  \big(
    \prod_{i:[n]} 
    S
  \big)
  \,=\, 
  S^n 
  \overset{\;\;\;\;\;}{\longrightarrow} 
  S
$$ 

from the $n$th [[cartesian power]] $S^n$ of $S$ to $S$ itself, where [n] is a set with $n$ elements. The __arity__ of the operation is $n$.

Sets with $n$-ary operations are called **$n$-ary magmas** or **$n$-ary groupoids**. 

More generally, an n-ary operation in a [[multicategory]] is just a [[multimorphism]]. 

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