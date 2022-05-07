# Church numerals

* toc
{: toc}

## Idea

The Church numerals are an encoding of the [[natural numbers]] into [[untyped lambda-calculus]].

## Definition

The $n$th Church numeral $\underline{n}$ is the operation of "iteration $n$ times", sending a function $f$ to its $n$th iterate.  Thus $\inderline{0}(f)$ is the identity function, $\underline{1}(f) = f$, $\underline{2}(f) = f\circ f = \lambda x. f(f(x))$, and so on.

## Connection to realizability

The Church numeral $\underline{n}$ can be regarded as a [[realizer]] or "proof" that we can do induction up to $n$.  See [this discussion](https://nforum.ncatlab.org/discussion/8622/church-numerals-are-realizers/).

[[!redirects Church numerals]]


