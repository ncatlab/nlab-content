
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An analog of [[enriched category]] in [[higher category theory]].

## Definition

In the context of [[(∞,1)-category theory]] see at
_[[enriched (∞,1)-category]]_.

In the context of [[(∞,1)-operad]] theory see ([Lurie, def. 4.2.1.12](#Lurie)):

Write $\mathcal{LM}^\otimes$ the [[operad for modules over an algebra]] regarded as an [[(∞,1)-operad]], regarded as the [[(∞,1)-category of operators]]. Similarly write $\mathcal{Ass}^\otimes$ for the [[(∞,1)-category of operators]] of the [[associative operad]].

Then for $\mathcal{V}^\otimes \to \mathcal{Ass}^\otimes$ exhibiting a  [[planar (∞,1)-operad]], a **weak enrichment** of an [[(∞,1)-category]] $\mathcal{C}$ over $\mathcal{C}^\otimes$ is a fibration

$$
  q \colon \mathcal{O}^\otimes \to \mathcal{LM}^{\otimes}
$$

which exhibits $\mathcal{C}$ as a module over $\mathcal{V}^\otimes$ in that it is   equipped with [[equivalence in an (∞,1)-category|equivalences]]

$$
  \mathcal{V}^\otimes \simeq \mathcal{O}^\otimes_{\mathfrak{a}}
$$

and

$$
  \mathcal{C} \simeq \mathcal{O}^\otimes_{\mathfrak{m}}
  \,.
$$
 

## Related concepts

* [[homotopical enrichment]];

* [[enriched (∞,1)-category]]


## References

Section 4.2.1 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

## Discussion

This was originally at [[bicategory]]:

_Sebastian_: Is there a formal meaning of _weak enrichment_? 

[[John Baez]]: Yes there is; indeed Clark Barwick is writing a huge book on this.

_Sebastian_: If not, is there at least a method how to get the definition of a weak $n$-category if I know the definition of a (strict) $n$-category?

[[John Baez]]: that sounds harder!  That's like pushing a rock uphill.  It's easier to go down from weak to strict.

_Sebastian_: Of course, I have recognised that there are actually different definitions of what a weak n-category should be... so to give my question a bit more precision: How do I get a definition of a weak $n$-category that is as close as possible to the definition of a strict $n$-category? The weak $n$-category should be what you call "globular", I think. (Are there different definitions of globular (weak or strict) n-categories?)

[[John Baez]]: globular strict n-categories have been understood since time immemorial, or at least around 1963, and there is just one reasonable definition.   Globular weak n-categories were defined in the 1990s by Michael Batanin, and his theory relates them quite nicely to the globular strict ones.   But there is also a _different_ definition of globular weak n-categories due to Penon.  It had a mistake in it which has now been fixed.

From the preface to [[johnbaez:Towards Higher Categories|Towards Higher Categories]]:

There is a quite different and more extensively developed operadic approach to globular [[nlab:weak omega-category|weak infinity-categories]] due to Batanin (Bat1, Str2), with a variant due to Leinster (Lein3).  Penon (Penon) gave a related, very compact definition of infinity-category; this definition was later corrected and improved by Batanin (Bat2) and Cheng and Makkai (ChMakkai).

You can get the references there.

I think this discussion should be moved over to some page on n-categories, since it's not really about bicategories.
