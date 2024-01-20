
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Given a [[small category]] $S$, we may consider freely adjoining (small) [[colimits]] to $S$, giving the [[free cocompletion]] of $S$. Concretely, this is the [[category of presheaves]] on $S$. Dually, we may consider freely adjoining (small) [[limits]] to $S$, giving the [[free completion]] of $S$. Concretely, this is the [[category of copresheaves]] on $S$.

Alternatively, we may consider freely adjoining both (small) limits *and* colimits to $S$ simultaneously. (Note that this means there will be no [[distributivity of limits and colimits]].) This is known as the **free bicompletion** of $S$.

Unlike the [[free completion]] or [[free cocompletion]], it is not known whether a concrete description of the free bicompletion of a small category exists.

Abstractly, the free bicompletion construction is the [[coproduct]] of the two [[2-monads]] associated to the [[free completion]] and the [[free cocompletion]].

## Examples

* The [[Cauchy completion]] of a category is its free bicompletion under absolute limits and absolute colimits.

* The free bicompletion of a category $C$ under an [[initial object]] and [[terminal object]] is given by adjoining two objects $\bot$ and $\top$ and defining:
$$
  C(\bot, \bot) = 1
  C(\bot, c) = 1
  C(c, \top) = 1
  C(\bot, \top) = 1
  C(\top, \top) = 1
$$
The composition laws are uniquely determined. (This is equivalently the result of completing $C$ under a terminal object, and then cocompleting under an initial object.)

## Related concepts

* [[free cocompletion]], [[free completion]]

* [[Cauchy completion]]

## References

* [[André Joyal]]. _Free bicomplete categories_. Mathematical Reports of the Academy of Sciences 17.5 (1995): 219-224. ([link](https://mathreports.ca/article/free-bicomplete-categories/))

* [[André Joyal]]. _Free bicompletion of enriched categories_. Mathematical Reports of the Academy of Sciences 17.5 (1995): 213-218. ([link](https://mathreports.ca/article/free-bicomplete-categories/))

The above references do not contain proofs. For a sketch of the existence of free bicompletions of categories, see [this MathOverflow question](https://math.stackexchange.com/questions/1686774/can-we-simultaneously-freely-adjoin-both-limits-and-colimits-to-a-category).

The free bicompletion of a category $C$ under nonempty [[products]] and nonempty [[coproducts]] is characterised as the category of nonempty $C$-valued contractible [[coherence spaces]] and $C$-maximal maps in:

* [[Hongde Hu]], _Contractible coherence spaces and maximal maps_, Electronic Notes in Theoretical Computer Science 20 (1999): 309-319.

A different approach for discrete categories is described in:

* [[Dominic J. D. Hughes]], _A canonical graphical syntax for non-empty finite products and sums_, Technical report (2002).

The free completion of a category $C$ under [[products]], [[coproducts]], and a [[zero object]] is characterised as the category of **contractible $C$-coherence spaces** in:

* [[Hongde Hu]] and [[André Joyal]], _Coherence completions of categories and their enriched softness_, Electronic Notes in Theoretical Computer Science 6 (1997): 174-190.

* [[Hongde Hu]] and [[André Joyal]], _Coherence completions of categories_, Theoretical Computer Science 227.1-2 (1999): 153-184.

[[!redirects free bicompletion]]

