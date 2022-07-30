

The [[cardinality]] of a [[finite set]] is a _finite number_. 

## Category of finite numbers

Let's identify finite numbers with elements of $\mathbb{N}$.

$\mathbb{N}$ can be made into a [[category]] $FNumb$ with [[hom-sets]] $FNumb[n,p]=\{\bullet\}$ if $n \le p$ and $FNumb[n,p]= \emptyset$ else.

## Cardinality functor

Write $MonoFSet$ for the [[wide subcategory]] of $FSet$ with objects finite sets and morphisms injections.

We then have the cardinality functor $|.|: MonoFSet \rightarrow FNumb$ which associates its number of elements to every finite set.

This functor verifies the following properties:

* $|A \times B| = |A|.|B|$
* $|f \times g| = |f|.|g|$
* $|A \sqcup B| = |A|+|B|$
* $|f \sqcup g| = |f|+|g|$
* $|\emptyset| = 0$

[[!redirects finite numbers]]
[[!redirects cardinality functor]]