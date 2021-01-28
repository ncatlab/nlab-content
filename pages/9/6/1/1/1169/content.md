
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Reedy category_ is a [[category]] $R$ equipped with a structure enabling the inductive construction of [[diagrams]] and [[natural transformations]] of shape $R$. It is named after [[Christopher Reedy]].  

The most important consequence of a Reedy structure on $R$ is the existence of a certain [[model category|model structure]] on the [[functor category]] $M^R$ whenever $M$ is a [[model category]] (no extra hypotheses on $M$ are required): the _[[Reedy model structure]]_.

## Definition

A **Reedy category** is a [[category]] $R$ equipped with two [[wide subcategories]] $R_+$ and $R_-$ and a [[total ordering]] on the objects of $R$, defined by a _degree_ function $d:Ob(R) \to \alpha$, where $\alpha$ is an [[ordinal number]], such that:

* Every nonidentity morphism in $R_+$ raises degree,
* Every nonidentity morphism in $R_-$ lowers degree, and
* Every morphism $f$ in $R$ factors uniquely as a map in $R_-$ followed by a map in $R_+$.


## Examples

* Any ordinal $\alpha$, considered as a [[poset]] and hence a category, is a Reedy category with $\alpha_+=\alpha$, $\alpha_-$ the [[discrete category]] on $Ob(\alpha)$, and $d$ the identity.

* The [[opposite category|opposite]] of any Reedy category is a Reedy category: use the same degree function, and exchange $R_+$ and $R_-$.

* The integers regarded as a poset is NOT a Reedy category, since it is not well-founded in either direction.

* [[Theta category|Joyal's category]],   $\Theta$, is also a Reedy category.

* Many very small categories of diagram shapes are Reedy categories, such as $(\cdot\to\cdot\to \dots)$, or $(\cdot\leftarrow \cdot\rightarrow\cdot)$, or $(\cdot\rightrightarrows\cdot)$.  This is of importance for the construction of [[homotopy limits]] and colimits over such diagram shapes.


### The simplex category

The prototypical examples of Reedy categories are the [[simplex category]] $\Delta$ and its opposite $\Delta^{op}$.  More generally, for any [[simplicial set]] $X$, its [[category of simplices]] $\Delta/X$ is a Reedy category.

The Reedy category structure on $\Delta$ is defined by:

* The degree function $d: Ob(\Delta) \to \mathbb{N}$ is defined by $[k] \mapsto k$. 

* a map $[k] \to [n]$ is in $\Delta_+$ precisely if it is injective;

* a map $[n] \to [k]$ is in $\Delta_-$ precisely if it is surjective.

And the Reedy category structure on $\Delta^{op}$ is defined by switching $\Delta_+$ and $\Delta_-$.

## Related notions

### Direct and inverse categories

A Reedy category in which $R_-$ contains only identities is called a [[direct category]]; the factorization axiom then says simply that $R=R_+$.  Similarly, if $R_+$ contains only identities it is said to be an [[inverse category]].

Any ordinal is of course a direct category, and so is the subcategory $R_+$ of any Reedy category considered as a category in its own right.  This amounts to "discarding the degeneracies" in a shape category.  In some examples there are no degeneracies to begin with, such as the category of [[opetopes]]; thus these are naturally direct categories.

Dually, so is the subcategory $R_-$ of any Reedy category considered as a category in its own right.  This amounts to "discarding the faces" in a shape category.

### Generalized Reedy categories

One problem with the notion of Reedy category is that it is [[evil]]: it is not invariant under [[equivalence of categories]].  It's not hard to see that any Reedy category is necessarily [[skeletal category|skeletal]].  In fact, it's even worse: no Reedy category can have _any_ [[identity|nonidentity]] [[isomorphisms]]!  

*Proof:* Take any isomorphism $f$, let $f = g h$ and $h f^{-1} = g' h'$ be the unique factorizations. Then $id = g h f^{-1} = (g g') h'$, so $h' = id$ and $g g' = id$, whence $g = id$ and $g' = id$ since $g, g' \in R_+$. Thus $f = h \in R_-$. The same argument applied to $f^{-1}$ shows that $f$ preserves the degree, hence $f = id$. $\qed$

This is problematic for many $\Delta$-like categories such as the [[category of cycles]], Segal's category $\Gamma$, the [[tree category]] $\Omega$, and so on.  The concept of 

* [[generalized Reedy category]],

due to [[Clemens Berger]] and [[Ieke Moerdijk]], avoids these problems.  There is a similar notion (which however does not comprise all Reedy categories) due to [[Denis-Charles Cisinski]].  A further generalization which allows noninvertible level morphisms is a

* [[c-Reedy category]].

### Elegant Reedy categories

The notion of [[elegant Reedy category]], introduced by [[Julie Bergner]] and [[Charles Rezk]], is a *restriction* of the notion which captures the property that the Reedy model structure and injective model structure coincide.  Several important Reedy categories are elegant, such as the $\Delta$ and $\Theta$.

### Eilenberg-Zilber categories

[[Eilenberg-Zilber categories]] are a special sort of generalized Reedy category that behave rather like an elegant strict Reedy category.

### Enriched Reedy categories

There is also a generalization of the notion of Reedy category to the context of [[enriched category theory]]: this is an [[enriched Reedy category]].

### Reedy categories with fibrant constants.

If $R$ is a [[direct category]], then for any [[model category]] $M$ the colimit functor $\colim_R \colon M^R \to M$ is a [[Quillen adjunction|left Quillen functor]]. However, there are non-direct Reedy categories with the same property, they are called [[Reedy category with fibrant constants|Reedy categories with fibrant constants]].

## References

See the references at _[[Reedy model structure]]_

[[!redirects Reedy categories]]
