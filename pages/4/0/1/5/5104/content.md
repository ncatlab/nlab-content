
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


# Concepts of basis in functional analysis
* table of contents
{: toc}

## Idea

A _basis in functional analysis_ is a [[linear basis]] that is compatible with the [[topological space|topology]] of the underlying [[topological vector space]]. Therefore this is sometimes also referred to as a "topological basis", but beware that this term is also used for referring to the unrelated concept of a  "[[basis for the topology]]".
 
[[basis|Bases]] in [[linear algebra]] are extremely useful tools for analysing problems.  Using a basis, one can often rephrase a complicated abstract problem in concrete terms, perhaps even suitable for a computer to work with.  A basis provides a way of describing a [[vector space]] in a way that:

1. Is complete: every point in the space can be described in this fashion.
2. Has no redundancies: the description of a point is unique.

When translated into the language of linear algebra, we recover the key properties of a basis: that it be a spanning set and linearly independent.

In infinite dimensions, having a basis becomes more valuable as the spaces get more complicated.  However, the notion of a basis also becomes complex because the question of what makes a description admits different answers depending on whether we want only finite sums, we allow sequences, or we want infinite sums.


## Definitions

+-- {: .num_defn #basis}
Let $V$ be a [[topological vector space]] and $B \subseteq V$ a subset.

1. We say that $B$ is a **[[Hamel basis]]** if:
   1. Every element of $v$ is a finite linear combination of elements of $B$,
   2. If $v = \sum_{b \in B} \alpha_b b$ then the $\alpha_b$ are unique.

   Alternatively, $B$ is [[linearly independent subset|linearly independent]] and $\Span(B) = V$; in other words, the [[span]] of $B$ is $V$ but no [[proper subset]] of $B$ has this property.

2. We say that $B$ is a **topological basis** if:
   1. Every element $v \in V$ is a limit of a [[sequence]] or (more generally) a [[net]] of finite linear combinations of elements of $B$,
   2. No element of $B$ is a limit of a sequence or net of finite linear combinations of the _other_ elements of $B$.

   Alternatively, $B$ is [[total subset|total]] (meaning that its span is [[dense subspace|dense]]) but no proper subset of $B$ is total.

3. We say that $B$ is a **Schauder basis** if:
   1. Every element of $v$ is a (possibly infinite) sum of scales of elements of $B$,
   2. If $v = \sum_{b \in B} \alpha_b b$ then the $\alpha_b$ are unique.
=--


## Properties

1. In the presence of the [[axiom of choice]], Hamel bases always exist.

2. If $B$ is a topological basis, then $B$ has a dual basis.  Since $B \setminus \{b\}$ is not total but $B$ is total, the closure of the span of $B \setminus \{b\}$ must be a codimension $1$ subspace, whence the kernel of a non-trivial continuous linear functional on $V$, say $f_b$.  By scaling, this functional can be assumed to satisfy $f_b(b) = 1$.  Since $B \setminus \{b\} \subseteq \ker f$, $f(b') = 0$ for all $b' \in B$, $b' \ne b$.

3. If $B$ is a Schauder basis then it is a topological basis and so, as mentioned, has a dual basis.  Then the coefficients in the sum $v = \sum \alpha_b b$ must be given by evaluating the dual basis on $v$: $v = \sum f_b(v) b$.


## Examples

1. In $C([0,1],\mathbb{C})$ with the norm ${\|f\|} = \max\{{|f(t)|}\}$:

   1. The monomials are linearly independent and have dense span, but do not form a topological basis as there is a sequence of polynomials with no linear term converging to $t$.

   2. The trigonometric polynomials do form a topological basis.  The dual basis is given by taking the Fourier coefficients of a function.  However, it is not a Schauder basis as there are continuous functions which are not the uniform limit of their Fourier series.

   3. The following is a Schauder basis.  Let $(d_n)$ be the sequence $\{0, 1, \frac{1}{2}, \frac{1}{4}, \frac{3}{4}, \dots\}$.  Define $f_n$ to be the piecewise-linear function with the property that: $f_n(d_n) = 1$ and $f_n(d_k) = 0$ for $k \lt n$, and $f_n$ has the least "breaks".  Then $f_n$ forms a Schauder basis for $C([0,1],\mathbb{C})$.  This is the classical _Faber-Schader_ basis.


## References

* Enflo, P. (1973). A counterexample to the approximation problem in Banach spaces. _Acta Math._, _130_, 309--317.

* [[Zbigniew Semadeni]], _Schauder bases in Banach spaces of continuous functions_, Springer Lecture Notes in Mathematics 918. Berlin 2008.


category: functional analysis

[[!redirects basis in functional analysis]]
[[!redirects bases in functional analysis]]
[[!redirects basises in functional analysis]]

[[!redirects Schauder basis]]
[[!redirects Schauder bases]]
[[!redirects Schauder basises]]
