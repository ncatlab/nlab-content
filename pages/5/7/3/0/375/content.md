# Definition

A __cartesian closed category__ (sometimes: __ccc__) is a category with finite [[products]] which is [[closed monoidal category|closed]] with respect to its [[cartesian monoidal category|cartesian monoidal structure]].


# Examples

* Any [[topos]] or [[quasitopos]], such as [[Set]], is cartesian closed.

* [[Cat]] is also cartesian closed.

* Many [[nice category of spaces|nice categories of topological spaces]] are also cartesian closed, particularly the [[convenient category of topological spaces|convenient categories of spaces]].


## Inheritance by reflective subcategories

In showing that a given category is cartesian closed, the following theorem is often useful (cf. A4.3.1 in the [[Elephant]]):

+-- {: .un_theorem}
###### Theorem
If $C$ is cartesian closed, and $D\subseteq C$ is a [[reflective subcategory]], then the reflector $L\colon C\to D$ preserves finite [[products]] if and only if $D$ is an [[exponential ideal]] (i.e. $Y\in D$ implies $Y^X\in D$ for any $X\in C$).  In particular, if $L$ preserves finite products, then $D$ is cartesian closed.
=--


# Remarks

* In a cartesian closed category, the product functors $A \times -$ have [[right adjoints]], so they preserve all [[colimits]].  In particular, a cartesian closed category that has finite [[coproducts]] is a [[distributive category]].

* The [[internal logic]] of cartesian closed categories is the [[typed lambda-calculus]].



[[!redirects cartesian closed categories]]
