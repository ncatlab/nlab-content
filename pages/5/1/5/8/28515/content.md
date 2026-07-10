
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

_Call-by-value_ (CbV) is a widely used [[evaluation strategy]]
for the [[λ-calculus]] and many [[programming languages]].
It is often studied in comparison with _[[call-by-name]]_ (CbN).

## Reduction rules

The small-step [[operational semantics]] for the CbV $\lambda$-calculus
is given by the following rules:

- if $e_1 \to e'_1$, then $e_1 e_2 \to e_1' e_2$ (left application rule),
- if $e \to e'$, then $v e \to v e'$ (right application rule), and
- $(\lambda x. e) v \to e[v/x]$ ($\beta_v$ rule),

where $v$ ranges over values, that is, over variables and abstractions.

This reduction is said to be _weak_
as terms inside abstractions cannot be reduced.

## Side effects

In the presence of [[side effects]],
such as state mutation or random number sampling,
the unrestricted $\beta$ reduction is no longer confluent,
and CbV and CbN no longer always agree on all computations.

For example, only in the former is `(fun x -> x + x) (random 0 1) : int` always even.

## Denotational semantics

For calculi featuring recursion or side effects,
one needs to be careful about the interpretation of values and functions
for the substitution and computational soundness properties to hold.
A common choice is to interpret function types as _strict_ functions,
i.e., as functions mapping $\bot$ to $\bot$.

## Relation to [[linear logic]]

We can define various translations from the standard $\lambda$-calculus
to the linear $\lambda$-calculus, in particular $e \mapsto e^\mathsf{v}$.

We have $e \to^\ast v$ in the (weak) CbV $\lambda$-calculus
if and only if $e^\mathsf{v} \to^\ast v^\mathsf{v}$
in the linear $\lambda$-calculus with (surface) reduction.
Similarly, strong call-by-value corresponds to deep linear reduction.

## Related notions

- [[call-by-name]]
- [[call-by-need]]
- [[call-by-push-value]]

## References

- J. Maraist, M. Odersky, D.N. Turner, P. Wadler. _Call-by-name, call-by-value, call-by-need and the linear lambda calculus_ (1999).

[[!redirects call by value]]
[[!redirects cbv]]
[[!redirects CbV]]
[[!redirects CBV]]