# Locally regular categories
* table of contents
{: toc}

## Idea

A *locally regular category* is a relative of a [[regular category]] in which the condition of [[finite limits]] is weakened to finite [[connected limits]].  It is so named because every [[slice category]] of a locally regular category is a regular category, although the converse is not quite true.

## Definition

A [[category]] $C$ is **locally regular** if

1. It has finite [[connected limits]] --- equivalently, it has [[pullbacks]] and [[equalizers]];

1. It has ([[extremal epi]], [[monomorphism|mono]]) factorizations which are stable under pullback; and

1. Every [[span]] factors as an extremal epi followed by a jointly-monic span.

## Examples

* Every [[regular category]] is locally regular.  Factorizations of spans may be obtained by factorizations of single morphisms into a binary product.

* The [[empty category]] is a locally regular category which is not regular. 

* The category $LH$ of [[topological spaces]] (or [[locales]]) and [[local homeomorphisms]] is locally regular, but not regular.  Its slice categories are precisely the [[sheaf toposes]] of spaces (or locales).

* The [[syntactic category]] of an [[extensional type theory]] with [[dependent sum types]], [[identity types]], and [[propositional truncations]] is a [[locally regular category]]. If the dependent type theory also has [[dependent product types]], the syntactic category becomes [[locally cartesian closed category|locally cartesian closed]]. If the type theory also has a [[unit type]] its syntactic category becomes a [[regular category]]. 

## Properties

* A locally regular category is regular if and only if it has a [[terminal object]].

* The factorization axiom for spans implies, by [[induction]], a similar factorization property for nonempty finite [[cosinks]].  However, similar factorizations for empty cosinks (i.e. "supports") do not necessarily exist.

* Every locally regular category gives rise to a tabular [[allegory]] of binary relations (where we define a "binary relation" to mean a jointly-monic span).  For composition of relations, we require pullbacks and stable factorizations of spans.  For intersection of binary relations, we require equalizers.

* Conversely, every tabular allegory has a locally regular category of maps (left adjoints).  So locally regular categories are essentially the same as tabular allegories.

## References

* [[Peter Johnstone]], [[Sketches of an Elephant]], A3.2.7

[[!redirects locally regular categories]]
