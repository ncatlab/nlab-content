
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



# Restriction category
* table of contents
{: toc}


## Idea

The concept of **restriction category** is an [[element]]-free formalisation of the idea of a [[category]] of [[partial maps]], where the [[domain]] of a map $f\colon X\to Y$ is encoded in a specified [[idempotent]] [[endomorphism]] $\overline{f}$ of $X$.

## Definition

Given a [[category]] $C$, a _restriction structure_ consists of the assignment to each [[morphism]] $f\colon X\to Y$ a morphism $\overline{f}\colon X\to X$ satisfying the following conditions:

* $f\circ \overline{f} = f$,
* $\overline{f}\circ \overline{g} = \overline{g}\circ\overline{f}$ whenever $s(f)=s(g)$,
* $\overline{g\circ \overline{f}} = \overline{g}\circ \overline{f}$ whenever $s(f)=s(g)$, and
* $\overline{g}\circ f = f\circ \overline{g\circ f}$ whenever $s(g) = t(f)$

where $s(f) = \text{dom}(f)$ is the domain of $f$. A _restriction category_ is a category with a restriction structure. 

Note that a restriction structure is a [[structure]] in the technical sense of the word, not a [[property]]. Note that it follows from the above definition that $\overline{f}$ is idempotent for composition: $\overline{f}\circ \overline{f} = \overline{f}$, and that the operation $f \mapsto \overline{f}$ is also idempotent: $\overline{\overline{f}} = \overline{f}$ (among other properties).


## Examples

Every category admits the _trivial_ restriction structure, with $\overline{f} = id_{s(f)}$.

Conversely the [[wide subcategory]] consisting off all the [[objects]] together with the morphisms $f$ satsfying $\overline{f}=id_{s(f)}$—the _total_ morphisms—has a trivial induced restriction structure.

The category $PF$ of [[sets]] and [[partial functions]] is the prototypical example, where for a partial function $X \supseteq U \stackrel{f}{\to} Y$, the partial endomorphism $\overline{f}$ is the partially-defined identity function $X \supseteq U \hookrightarrow X$. Many other examples are listed in ([Cockett–Lack 2002](#CockettLack02))


## Related concepts

* [[partial function]]
* [[cartesian restriction category]]
* [[Turing category]]

## References

* {#CockettLack02} [[Robin Cockett]], [[Steve Lack]], _Restriction categories I: categories of partial maps_, Theoretical Computer Science **270** (2002) pp 223–259 ([author pdf](http://pages.cpsc.ucalgary.ca/~robin/FMCS/FMCS_06/RestrictionsI.pdf))

* [[Robin Cockett]], [[Steve Lack]], _Restriction categories II: partial map classification_ ([web](http://maths.mq.edu.au/~slack/papers/restii.html))

* [[Robin Cockett]], [[Steve Lack]], _Restriction categories III: colimits, partial limits, and extensivity_ ([arXiv:math/0610500](http://arxiv.org/abs/math/0610500))

[[!redirects restriction categories]]

[[!redirects cartesian restriction category]]
[[!redirects cartesian restriction categories]]

