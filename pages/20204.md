+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 
+--{: .hide}
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Motivation

Several generalizations of [[effect algebras]] exist, based on the needs of various logics; these may not have a clear relationship to the quantum foundations of effect algebras, but deal with informationally similar situations where the "resources" of the deductions rules are subject to certain restrictions. _Separation algebras_  correspond to [[separation logic]] in the way effect algebras correspond to [[quantum logic]], and are often used as models for memory allocation and program modularity, where the outcome of a program must be guaranteed with respect to specified memory states. Separation algebra therefore has a role in [[certified programming]].

## Definition



+-- {: .num_defn #SA}
###### Definition
**((Generalized) Separation Algebra)**

A _generalized separation algebra_ (GSA) is a partial [[monoid]] satisfying the following equations:

(1) $ab = ac \rightarrow b=c$,

(2) $ab=cb \rightarrow a=c$,

and the non-equational formula:

(3) $\forall a, b (\exists d : da=b \iff \exists c : ac = b)$

A _separation algebra_ is a commutative GSA, which removes the axiom (3). The real interest of (3) lies in other order-theoretic properties.
=--

This reveals effect algebras to be those separation algebras with the positivity property.

### A Family of Partial Algebras  
  {#familytree}

(...)

## Examples 

Aside from low-dimensional cases found in a model generator such as Mace, many natural examples which are not effect algebras arise from ordered bisemigroups.

(...)



## Related Concepts

* [[separation logic]]

* [[Hoare logic]]

* [[effect algebras]]


## References 

(...)


[[!redirects separation algebra]]
[[!redirects separation-algebra]]