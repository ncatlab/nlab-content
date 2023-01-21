
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In [[type theory]], a _dependent type_ or _[[type]] in [[context]]_ is a *[[family]]* or *[[bundle]]* of [[types]] which vary over the elements ([[terms]]) of some other type.  It can be regarded as a formalization of the notion of "indexed family," providing a [[structural set theory|structural]] account of families (in contrast to the [[material set theory|material]] approach which requires sets to be able to contain other sets as elements).

Type theory with the notion of dependent types is called _[[dependent type theory]]_.

In the [categorical semantics of type theory](http://ncatlab.org/nlab/show/type+theory#CategoricalSemantics), a dependent type 

$$
  x:A \; \vdash \;B(x) \;\mathrm{type}
$$ 

is represented by a particular [[morphism]] $p\colon B\to A$, the intended meaning being that each type $B(x)$ is the [[fiber]] of $p$ over $x\in A$.  The morphism in a category that may represent dependent types in this way are sometimes called [[display morphisms]] (especially when not every morphism is a display morphism).

Dependent types can be thought of as [[fibrations]] ([[Serre fibrations]]) in classical homotopy theory. The base space is $X$, the total space is $\sum_{(x:X)}P(x)$ and the fiber $P(\star_X)$. This gives the fibration:

$$P(\star_X)\to \sum_{x:X}P(x) \to X$$

## Relation to families of elements. 
 {#RelationToFamiliesOfElements}

Given a family of types, $x:A \vdash B(x)$, one could construct a family of elements $z:\sum_{x:A} B(x) \vdash \pi_1(z):A$ via the [[elimination rules]] for [[negative type|negative]] [[dependent sum types]]: 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, z:\sum_{x:A} B(x) \vdash \pi_1(z):A}$$

Conversely, given a family of elements $x:A \vdash f(x):B$ one could construct a family of types $y:B \vdash \sum_{x:A} f(x) =_B y$ as the family of [[fiber types]] of $x:A \vdash f(x):B$, via the [[formation rules]] for [[identity types]] and [[dependent sum types]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B}{\Gamma, x:A, y:B \vdash f(x) =_B y \; \mathrm{type}}}{\Gamma, y:B \vdash \sum_{x:A} f(x) =_B y \; \mathrm{type}}$$

This corresponds to the [[relation between type theory and category theory]]: there are two ways to interpret a morphism $f:\mathrm{Hom}_C(A, B)$ in a [[category]] $C$

* as a family of elements $x:A \vdash f(x):B$
* as a family of types $y:B \vdash A(y)$

One can additionally derive the following [[equivalence of types]]: 

$$p:A \simeq \sum_{y:B} \sum_{x:A} f(x) =_B y$$

$$y:B \vdash q(y):A(y) \simeq \sum_{z:\sum_{x:B} A(x)} \pi_1(z) =_A y$$

## Examples

When the [[theory]] of a [[category]] is phrased in dependent type theory then there is one type "$obj$" of [[objects]] and a type $hom$ of [[morphisms]], which is dependent on two terms of type $obj$, so that for any $x,y:obj$ there is a type $hom(x,y)$ of arrows from $x$ to $y$.  This dependency is usually written as $x,y:obj \vdash hom(x,y):Type$.  In some theories, it makes sense to say that the type of "$hom$" itself is $obj, obj\to Type$ (usually understood as $obj \to (obj \to Type)$ or $(\obj \times \obj) \to Type$), i.e. a function from pairs of elements of $A$ to the [[type of types|universe]] $Type$ of types.

## Related concepts

* [[Martin-Löf dependent type theory]]

* [[term in context]]

* [[telescope]]

* [[dependent sum]], [[dependent product]]

* [[indexed set]]

## References

See the references at *[[dependent type theory]]*.

* Blog post: [In praise of dependent types](http://golem.ph.utexas.edu/category/2010/03/in_praise_of_dependent_types.html)

In [[Coq]]:

* Yves Bertot, _Introduction to dependent types in Coq_ ([pdf](http://www-sop.inria.fr/members/Yves.Bertot/tsinghua/tsinghua-1.pdf))


[[!redirects dependent types]]

[[!redirects type family]]
[[!redirects type families]]

[[!redirects type in context]]
[[!redirects types in context]]
[[!redirects types in contexts]]
