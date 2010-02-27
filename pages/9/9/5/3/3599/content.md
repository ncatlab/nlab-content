<div class="rightHandSide toc">
[[!include type theory - contents]]
</div>
In [[type theory]], a **dependent type** is a family of types which vary over the elements (terms) of some other type.  It can be regarded as a formalization of the notion of "indexed family," providing a [[structural set theory|structural]] account of families (in contrast to the [[material set theory|material]] approach which requires sets to be able to contain other sets as elements).

For example, when the theory of a [[category]] is phrased in dependent type theory, there is one type "$obj$" of objects, and a type $hom$ of arrows which is dependent on two terms of type $obj$, so that for any $x,y:obj$ there is a type $hom(x,y)$ of arrows from $x$ to $y$.  This dependency is usually written as $x,y:obj \vdash hom(x,y):Type$.  In some theories, it makes sense to say that the type of "$hom$" itself is $A\to A\to Type$, i.e. a function from pairs of elements of $A$ to the [[type-theoretic universe|universe]] $Type$ of types.

In the categorical semantics of type theory, a dependent type $x:A \vdash B(x):Type$ is represented by a particular map $p\colon B\to A$, the intended meaning being that each type $B(x)$ is the [[fiber]] of $p$ over $x\in A$.  The maps in a category which are intended to represent dependent types are sometimes called [[display maps]].

See also:

* [[dependent type theory]]
* [[Martin-Lof dependent type theory]]
* [[dependent sum type]]
* [[dependent product type]]

[[!redirects dependent types]]
