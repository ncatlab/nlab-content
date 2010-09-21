# Bicategories of relations
* tic
{: toc}


## Idea

A *bicategory of relations* is a [[(1,2)-category]] which behaves like the 2-category of internal [[relations]] in a [[regular category]].  The notion is due to Carboni and Walters.


## Definition

[Note: in this article, the direction of composition is diagrammatic (i.e., "anti-Leibniz"). 

A **bicategory of relations** is a [[cartesian bicategory]] which is [[locally posetal 2-category|locally posetal]] and moreover in which for every object $X$, the [[diagonal morphism|diagonal]] $\Delta\colon X\to X\times X$ and [[codiagonal]] $\nabla\colon X\times X\to X$ satisfy the [[Frobenius condition]]:
$$\nabla\Delta = (1\times \Delta)(\nabla \times 1).$$

+--{: .query}
There is also the dual Frobenius condition $\nabla\Delta = (\Delta\times 1)(1\times \nabla)$, and the "separable axiom" $\Delta\nabla = 1$, which as far as I can tell are not in the original paper, but appear in the blog post.  Do they follow from the rest of the definition? 

[[Todd Trimble]]: I have been struggling to derive the dual Frobenius condition from the one Frobenius condition. On the other hand, separability 
is easy and given below. 
=--

+-- {: .un_prop} 
######Proposition 
(Separability condition) $\Delta\nabla = 1$.
=-- 

+-- {: .proof} 
######Proof
In one direction, we have the 2-cell $1 \leq \Delta\nabla$ which is the unit of the adjunction $\Delta \dashv \Delta_* = \nabla$. In the other direction, there is an adjunction $\varepsilon \dashv \varepsilon_*$ between the counit and its dual, and the unit of this adjunction is a 2-cell $1 \leq \varepsilon\varepsilon_*$, from which we derive 

$$\Delta\nabla = \Delta\Delta_* \leq \Delta (1 \times \varepsilon)(1 \times \varepsilon_*)\Delta_* = 1$$ 

where the last equation follows from the equation $\Delta(1 \times \varepsilon) = 1$ and its dual $(1 \times \varepsilon_*)\Delta_* = 1$. 
=--



Of course, in the locally posetal case the definition of [[cartesian bicategory]] can be simplified.  (Should say something about that.)


## See also

Other attempted axiomatizations of the same idea "something that acts like the category of relations in a regular category" include:

* [[allegories]]

* [[1-category equipped with relations]]



## References

* Carboni and Walters, "Cartesian Bicategories, I"

* [blog post](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html) showing that any bicategory of relations is an [[allegory]].


[[!redirects bicategories of relations]]