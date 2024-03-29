# Metric jets
* table of contents
{: toc}

## Idea

The notions of **metric tangency** and **metric jet** are generalizations of notions from [[differential calculus]] such as [[tangent vectors]] and [[jet spaces]] to the setting of arbitrary [[metric spaces]].

## Definition

Let $M$ and $M'$ be [[metric spaces]], $f,g:M\to M'$ two maps, and $a\in M$.

+-- {: .num_defn #Tangency}
###### Definition
We say that $f$ and $g$ are **tangent at $a$** if $f(a)=g(a)$ and the function $C_a:M\to \mathbb{R}_+$ defined by
$$
C_a(a) = 0 \qquad
C_a(x) = \frac{d(f(x),g(x))}{d(x,a)} \forall x\neq a
$$
is continuous at $x=a$.
=--

Now let $a'\in M'$ be another point.

+-- {: .num_defn #Jets}
###### Definition
The set of **jets from $(M,a)$ to $(M',a')$** is the [[quotient set]] of the set of maps $f:M\to M'$ which are [[locally Lipschitz map|locally Lipschitz]] at $a$ and satisfy $f(a)=a'$ by the [[equivalence relation]] of tangency at $a$.
=--

## References

* [[Elisabeth Burroni]] and [[Jacques Penon]], "A metric tangential calculus", [TAC](http://www.tac.mta.ca/tac/volumes/23/10/23-10abs.html).

[[!redirects metric jet]]
[[!redirects metric jets]]
[[!redirects metric tangency]]
