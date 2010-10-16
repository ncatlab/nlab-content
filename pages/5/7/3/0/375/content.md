
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A __cartesian closed category__ (sometimes: __ccc__) is a category with finite [[products]] which is [[closed monoidal category|closed]] with respect to its [[cartesian monoidal category|cartesian monoidal structure]].

The [[internal hom]] $[S,X]$ in a cartesian closed category is often called [[exponentiation]] and is denoted $Y^S$.

## Examples

* Any [[topos]] or [[quasitopos]], such as [[Set]], is cartesian closed.

  See also [[closed monoidal structure on presheaves]].

* [[Cat]] is also cartesian closed.

* Many [[nice category of spaces|nice categories of topological spaces]] are also cartesian closed, particularly the [[convenient category of topological spaces|convenient categories of spaces]].




## Properties

* In a cartesian closed category, the product functors $A \times -$ have [[right adjoints]], so they preserve all [[colimits]].  In particular, a cartesian closed category that has finite [[coproducts]] is a [[distributive category]].

* The [[internal logic]] of cartesian closed categories is the [[typed lambda-calculus]].

### Inheritance by reflective subcategories

In showing that a given category is cartesian closed, the following theorem is often useful (cf. A4.3.1 in the [[Elephant]]):

+-- {: .un_theorem}
###### Theorem
If $C$ is cartesian closed, and $D\subseteq C$ is a [[reflective subcategory]], then the reflector $L\colon C\to D$ preserves finite [[products]] if and only if $D$ is an [[exponential ideal]] (i.e. $Y\in D$ implies $Y^X\in D$ for any $X\in C$).  In particular, if $L$ preserves finite products, then $D$ is cartesian closed.
=--



[[!redirects cartesian closed category]]
[[!redirects cartesian closed categories]]
[[!redirects cartesian closed]]
[[!redirects closed cartesian category]]
[[!redirects closed cartesian categories]]
