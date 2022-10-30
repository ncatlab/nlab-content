
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
* automatic table of contents goes here
{:toc}

## Definition

A **sketch** is a [[small category]] with specified [[limit]]s and [[colimit]]s.

A **model of a sketch** is a [[Set]]-valued [[functor]] preserving the specified limits and colimits.

A [[category]] is called **sketchable** if it is the category of models of a sketch.

The categories of models of sketches are precisely the [[accessible category|accessible categories]].

A **limit-sketch** is a sketch with just limits and no colimits specified.

The categories of models of limit-sketches are the [[locally presentable category|locally presentable categories]].

* an *accessible* category is equivalently:
  * a full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a sketch

* a *locally presentable* category is equivalently:
  * a *reflective* full subcategory of a presheaf category that's closed under $\kappa$-filtered colimits for some $\kappa$
  * the category of models of a *limit* sketch
  * an accessible category with all small limits
  * an accessible category with all small colimits

we can "break in half" the difference between the two and define

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

## References

An overview of the theory is given in

* Ad&#225;mek and Rosicky,  _[[Locally Presentable and Accessible Categories]]_. Cambridge University Press, Cambridge, 1994. 

An extensive treatment of the links between theories, sketches and models can be found in 

* Makkai, Par&#233;, _Accessible categories: The foundations of categorical model theory_ Contemporary Mathematics 104. American Mathematical Society, Rhode Island, 1989.1989.

* [[Michael Barr]] and [[Charles Wells]], _[[Toposes, Triples, and Theories]]_, Originally published by:
Springer-Verlag, New York, 1985, republished in:
[[Reprints]] in [Theory and Applications of Categories, No. 12 (2005) pp. 1-287](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)

That not only every sketchable category is [[accessible category|accessible]] but that conversely every [[accessible category]] is sketchable is due to

* Christian Lair, _Cat&#233;gories modelables et cat&#233;gories esquissables_, Diagrammes (1981).


[[!redirects sketches]]

[[!redirects finite limit sketch]]
[[!redirects finite limit sketches]]
