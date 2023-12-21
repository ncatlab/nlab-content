
* table of contents
{:toc}

## Idea

[[enriched category|Enriched categories]] and [[internal categories]] are both generalisations of categories to category-like structures that are defined in terms of another category. An enriched category is (usually) defined in terms of a [[monoidal category]], while an internal category is (usually) defined in terms of a category with [[finite limits]]. The two notions are not unrelated, but they are different. One difference is that in a $V$-enriched category, the objects still form a _set_ (or a proper class) while the arrows are replaced by objects of $V$, while in a category internal to $E$, both the set of objects _and_ the set of arrows are replaced by objects of $E$.

One way that internalisation and enrichment are related is that internal categories and enriched categories are both instances of [[monad|monads]] in bicategories (the bicategory of spans and the bicategory of matrices, respectively). Since monads in a bicategory $B$ are one-object categories enriched in the bicategory $B$, it is thus possible to capture $E$-internal categories as one-object categories enriched in the [[bicategory of spans]] $Span(E)$.

It is useful to contrast the notion of [[internal category]] with that of [[enriched category]], each of which may be considered as a generalization according to whether categories are [defined](category#definitions) (i) by a single collection of all morphisms or (ii) by a family of collections indexed by pairs of objects. In some cases, one of these generalizations is a special case of the other, but in general they are incomparable. These two presentations may be seen as different presentations of the theory of categories as a [generalized algebraic theory](generalized+algebraic+theory#relationship_to_enriched_categories).

[[internalization|Internalisation]] is a quite general phenomenon, of which [[internal categories]] are a particular case. However, the distinction between "internalization" and "enrichment" becomes less clear in generality.

For example, in addition to categories enriched over a monoidal category, one can define categories enriched over a [[bicategory]] or an [[virtual double category]]. It then turns out that a category enriched over the bicategory (or virtual double category) of [[span|spans]] in a lex category $C$ which has one object is precisely an internal category in $C$.

## Comparing internalisation and enrichment in the same category

While enriched categories and internal categories are defined with respect to different kinds of category, making it impossible to compare them in general, we can compare the two notions when our category $V$ or $E$ has enough structure. E.g. $K$ is an $\infty$-[[extensive category]], such as [[Set]] or [[simplicial set|simplicial sets]] (or more generally any [[Grothendieck topos]]), (small) $K$-enriched categories can be identified with $K$-internal categories whose object-of-objects is discrete (that is, a coproduct of copies of the terminal object).

We may also internalise a category in a [[internal category in a monoidal category|monoidal category]]. One might expect that the same relationship holds in this generalised setting, though it does not appear this has been worked out in the literature.

## Related concepts

* [[enriched category]] and [[internal category]]

* [[model structure on enriched categories]] and [[model structure on internal categories]]

## References

The equivalence between categories enriched in $K$ and categories internal to $K$ with a discrete object of objects is due to the appendix of:

* [[Andrée Bastiani]], [[Charles Ehresmann]], _Multiple functors. III. The cartesian closed category $Cat_n$_, Cahiers de topologie et géométrie différentielle 19.4 (1978): 387-443.

This relationship has also been studied in:

* [[Michał R. Przybyłek]], *Kategorie wewnętrzne a kategorie wzbogacone* (2008), master's thesis ([pdf](https://www.mimuw.edu.pl/~mrp/mgr_mrp.pdf))

* [[Thomas Cottrell]], [[Soichiro Fujii]], and [[John Power]], _Enriched and internal categories: an extensive relationship (2017).
* [[Bojana Femić]] and [[Enrico Ghiorzi]], _Internalization and enrichment via spans and matrices in a tricategory_, _Journal of Algebraic Combinatorics_ (2023): 1-54.


[[!redirects internalisation versus enrichment]]
[[!redirects internalization versus enrichment]]
[[!redirects internalisation vs enrichment]]
[[!redirects internalization vs enrichment]]
[[!redirects enrichment versus internalization]]
[[!redirects enrichment vs internalisation]]
[[!redirects enrichment vs internalization]]