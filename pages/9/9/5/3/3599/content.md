
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

In [[type theory]], a _dependent type_ or _[[type]] in [[context]]_ is a family or [[bundle]] of [[types]] which vary over the elements ([[terms]]) of some other type.  It can be regarded as a formalization of the notion of "indexed family," providing a [[structural set theory|structural]] account of families (in contrast to the [[material set theory|material]] approach which requires sets to be able to contain other sets as elements).

Type theory with the notion of dependent types is called _[[dependent type theory]]_.

In the [categorical semantics of type theory](http://ncatlab.org/nlab/show/type+theory#CategoricalSemantics), a dependent type 

$$
  x:A \; \vdash \;B(x):Type
$$ 

is represented by a particular [[morphism]] $p\colon B\to A$, the intended meaning being that each type $B(x)$ is the [[fiber]] of $p$ over $x\in A$.  The morphism in a category may represent dependent types in this way are sometimes called [[display morphisms]] (especially when not every morphism is a display morphism).

## Examples

When the [[theory]] of a [[category]] is phrased in dependent type theory, there is one type "$obj$" of [[objects]], and a type $hom$ of [[morphisms]] which is dependent on two terms of type $obj$, so that for any $x,y:obj$ there is a type $hom(x,y)$ of arrows from $x$ to $y$.  This dependency is usually written as $x,y:obj \vdash hom(x,y):Type$.  In some theories, it makes sense to say that the type of "$hom$" itself is $obj, obj\to Type$ (usually understood as $obj \to (obj \to Type)$ or $(\obj \times \obj) \to Type$), i.e. a function from pairs of elements of $A$ to the [[type-theoretic universe|universe]] $Type$ of types.


## Related concepts

* [[Martin-Löf dependent type theory]]

* [[dependent term]]

* [[dependent sum]], [[dependent product]]

## References

* Blog post: [In praise of dependent types](http://golem.ph.utexas.edu/category/2010/03/in_praise_of_dependent_types.html)

In [[Coq]]:

* Yves Bertot, _Introduction to dependent types in Coq_ ([pdf](http://www-sop.inria.fr/members/Yves.Bertot/tsinghua/tsinghua-1.pdf))



[[!redirects dependent types]]

[[!redirects type in context]]
[[!redirects types in context]]
[[!redirects types in contexts]]
