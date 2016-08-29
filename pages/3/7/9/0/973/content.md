
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
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
In a [[Lawvere theory]], one specifies an algebraic theory by giving a [[small category|small]] [[category]] $T$ with finite [[products]]. Then a [[model]] of the theory is given by a [[functor]] $T \to Set$ that [[preserved limit|preserves]] products. A **sketch** is a generalization of this idea, where we take a small category $T$, and pick some distinguished limit and colimit cones. Then a model of the sketch is a functor that preserves these limits and colimits.

## Definition

+-- {: .num_defn }
###### Definition 

A **sketch** is a [[small category|small]] [[category]] $T$ equipped with subsets $(L, C)$ of its [[limit]] [[cones]] and [[colimit]] [[cocones]]. 

A **limit-sketch** is a sketch with just limits and no colimits specified, ie. with $C = \emptyset$. Dually, a **colimit-sketch** is a sketch with $L = \emptyset$.

A **model of a sketch** is a [[Set]]-valued [[functor]] preserving the specified limits and colimits.

A [[category]] is called **sketchable** if it is the category of models of a sketch.

=--

## Examples

+-- {: .num_example}
###### Example
A [[Lawvere theory]] is a special case of a (limit-)sketch, where the category is one with a distinguished object $X$ such that all objects are ([[isomorphic]] to) powers of $X$, and $C = \emptyset$ and $L$ is the set of all product cones.
=--

## Properties

### Relation to accessible and locally representable categories
 {#RelationToLocallyRepresentableCategories}

+-- {: .num_prop }
###### Proposition 

The categories of models of sketches are equivalently the [[accessible categories]].

=--

+-- {: .num_prop }
###### Proposition 

The categories of models of limit-sketches are the [[locally presentable categories]].

=--

+-- {: .num_prop }
###### Remark

From the discussion there we have that

* an [[accessible category]] is equivalently:
  * a full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a sketch

* a [[locally presentable category]] is equivalently:
  * a *reflective* full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a *limit* sketch
  * an accessible category with all small limits
  * an accessible category with all small colimits

We can "break in half" the difference between the two and define

* a *locally multipresentable category* to be equivalently:
  * a *multireflective* full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a *limit and coproduct* sketch
  * an accessible category with all small *connected* limits
  * an accessible category with all small multicolimits

and

* a *weakly locally presentable category* to be equivalently:
  * a *weakly reflective* full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a *limit and epi* sketch
  * an accessible category with all small products
  * an accessible category with all small weak colimits

=--

## References

An overview of the theory is given in

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AdamekRosicky}

An extensive treatment of the links between theories, sketches and models can be found in 

* [[Michael Makkai]], [[Robert Paré]], _Accessible categories: The foundations of categorical model theory_ Contemporary Mathematics 104. American Mathematical
Society, Rhode Island, 1989. 
{#MakkaiPare}

* [[Michael Barr]], [[Charles Wells]], _[[Toposes, Triples, and Theories]]_, Originally published by:
Springer-Verlag, New York, 1985, republished in:
Reprints in [Theory and Applications of Categories, No. 12 (2005) pp. 1-287](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)

That not only every sketchable category is [[accessible category|accessible]] but that conversely every [[accessible category]] is sketchable is due to

* Christian Lair, _Cat&#233;gories modelables et cat&#233;gories esquissables_, [Diagrammes (1981)](https://eudml.org/doc/192986).


[[!redirects sketches]]

[[!redirects finite limit sketch]]
[[!redirects finite limit sketches]]
