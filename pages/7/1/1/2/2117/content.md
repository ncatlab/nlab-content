
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 

## Idea

Much of ordinary mathematics can be thought of as taking place [[internalization|inside]] "the archetypical [[category]] [[Set|SET]] of sets". However $SET$ itself can of course not be described from inside itself. But there may be objects in $SET$ ([[internal categories]]) that _look like_ $SET$ itself. These are called _universes_ or more specifically _[[Grothendieck universe]]s_ .

There is also the notion of univese in [[type theory]].


## Universes as models for $SET$

Universes come into existence by the following process.

1. We assume that we understand _a priori_ what it means to use [[first-order logic]].

1. Using first order logic, we can formulate a first-order theory called [[set theory]], for instance the version of the theory called [[ETCS]] that describes $SET$. 

   At [[fully formal ETCS]] this is spelled out explicitly. To the axioms listed there, we add one more: the **axiom of universes**. This demands that there exists an [[object]] $U$ of $SET$ that is a [[universe in a topos]] and hence there exists an [[internal category]] $U Set$ in $SET$, whose objects are the elements of the universe $U$, now to be called the [[small set]]s.

1. We show that $U Set$ is a [[model]] of the first order set theory that we started with. 



## Arbitrary categories as universes

More generally, one may pick any [[category]] and declare it to be a _universe_ inside of which one wants to do mathematics.

Of course without further assumptions on the category, there is in general very little math that can be formulated inside it, but a few extra properties and structures are usually necessary to provide something interesting.  On the other hand, perhaps too much can be formulated; in the [[terminal category]] everything is trivial; the attitude to take is that any *specific* category is merely one model, while a general *class* of categories is a theory 

For instance:
* If the category is equipped with the structure of a [[site]], then geometrical notions, such as defining [[morphism|arrow]]s locally on the domain with patching conditions (or more generally [[descent]] theory), exist inside it. 
* If it is a [[finitely complete category]], the existence of (finite) [[product]]s and [[terminal object]]s means that [[variety of algebras|varieties of algebras]] can be defined. 
* If the category is a [[topos]] with a [[natural numbers object]], then one can do a certain sort of "ordinary" mathematics inside it, specifically [[predicative mathematics|impredicative]] [[constructive mathematics]] without the fancier tools of [[model theory]] or (ironically) [[category theory]].
* Further extra conditions on the category, such as being a [[Boolean topos]] or being a [[superextensive site]], bring the internal mathematics closer to that of $Set$.


### Kinds of logic, kinds of categories

To each kind of category (technically, to each [[doctrine]]), we can consider those concepts from [[logic]] that can be [[internalisation|internalised]] in it.


### Large cardinals and small universes

Generally, the categories that we use as universes as [[large category|large]].  However, we can also consider the possibility that there exists a [[small category]] that is suitable for use as a universe for some forms of mathematics.  The statement that such a category exists is (in the meta-theory) the statement that the mathematics that it internalises is [[consistent theory|consistent]], which we can think of as a [[large cardinal]] axiom.

For example, that there exist small finitely complete categories is a form of the [[axiom of infinity]], which states that some [[infinite set|infinite cardinal]] exists; this is the smallest of the large cardinals.  On a much larger scale, a [[Grothendieck universe]] is a small [[subcategory]] of $Set$ in which all of [[ordinary mathematics]] can be internalised; the existence of one of these is equivalent to the existence of an uncountable [[inaccessible cardinal]].


## Universes in Type theory

(...)


[[!redirects universe]]
[[!redirects universes]]
[[!redirects universe > history]]
