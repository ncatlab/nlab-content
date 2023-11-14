
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

* {#CockettLack02} [[Robin Cockett]] and [[Steve Lack]], _Restriction categories I: categories of partial maps_, Theoretical Computer Science **270** 1-2 (2002) 223-259 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(00)00382-0">doi:10.1016/S0304-3975(00)00382-0</a>&rbrack;

* {#CockettLack03} [[Robin Cockett]] and [[Steve Lack]], _Restriction categories II: partial map classification_, Theoretical Computer Science **294** 1-2 (2003) 61-102 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(01)00245-6">doi:10.1016/S0304-3975(01)00245-6</a>&rbrack;

* {#CockettLack07} [[Robin Cockett]] and [[Steve Lack]], _Restriction categories III: colimits, partial limits and extensivity_, Mathematical Structures in Computer Science **17** 4 (2007)  775-817 &lbrack;[arXiv:math/0610500](https://arxiv.org/abs/math/0610500), [doi:10.1017/S0960129507006056](https://doi.org/10.1017/S0960129507006056)&rbrack;

* {#CockettGarner14} [[Robin Cockett]] and [[Richard Garner]], _Restriction categories as enriched categories_, Theoretical Computer Science **523** (2014) 37-55 &lbrack;[arXiv:1211.6170](https://arxiv.org/abs/1211.6170), [doi:10.1016/j.tcs.2013.12.018](https://doi.org/10.1016/j.tcs.2013.12.018)&rbrack;

A [[double category|double categorical]] approach to restriction categories is proposed in:

* [[Robert Paré]], _A double category take on restriction categories_, ([slides](https://www.mscs.dal.ca/~pare/Azores.pdf))

On showing that restriction categories are [[categories enriched in a double category]]:

* [[Robin Cockett]] and [[Richard Garner]], _Restriction categories as enriched categories_, Theoretical Computer Science 523 (2014): 37-55.

On [[free cocompletions]] of restriction categories:

* [[Richard Garner]] and Daniel Lin, _Cocompletion of restriction categories_, Theory and Applications of Categories 35.22 (2020): 809-844.

On using restriction categories to model [[essentially algebraic theories]]:

* [[Ivan Di Liberti]], [[Fosco Loregian]], [[Chad Nester]], [[Paweł Sobociński]]. _Functorial semantics for partial theories_, Proceedings of the ACM on Programming Languages 5.POPL (2021): 1-28.

On *range restriction categories*:

* Xiuzhan Guo, *Ranges, restrictions, partial maps, and fibrations* (2004), Master's thesis ([pdf](https://www.collectionscanada.gc.ca/obj/s4/f2/dsk4/etd/MQ93373.PDF?is_thesis=1&oclc_number=60669889)).

[[!redirects restriction categories]]

[[!redirects cartesian restriction category]]
[[!redirects cartesian restriction categories]]
