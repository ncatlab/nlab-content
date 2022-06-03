
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The notion of _coframe_ is a generalization of the notion of [[category of closed subsets]] of a [[topological space]]. A _coframe_ is like a category of closed subsets in a space possibly more general than a topological space: a [[locale]]. This in turn is effectively defined to be anything that has a collection of closed subsets that behaves essentially like the closed subsets of a topological space do.

It is also the [[opposite poset]] of a [[frame]]. 

## Definition

+-- {: .num_defn}
###### Definition

A **coframe** $\mathcal{C}$ is 

* a [[partial order|poset]] 

* that has 

  * all [[small limit|small]] [[products]]s, called [[meet|meets]] $\bigwedge$

  * all [[finite colimits]], called [[join|joins]] $\vee$

* and which satisfies the _infinite distributive law_:

  $$ 
    \bigwedge_i (x\vee y_i) \leq x \vee (\bigwedge_i y_i)
  $$

  for all $x, \{y_i\}_i$ in $A$

  (Note that the converse holds in any case, so we have equality.)

A _coframe homomorphism_ is a homomorphism of posets that preserves finite joins and arbitrary meets. Coframes and coframe homomorphisms form the category Cofrm.

=--

## See also

* [[co-Heyting algebra]]

* [[frame]]

* [[cotopos]]

## References

* Mamuka Jibladze, "Cosheaves, coframes, cotoposes: some new facts, some old questions" ([web archive](https://web.archive.org/web/20130602214748/http://www.wra1th.plus.com/gcw/rants/math/PSSL/1997.html))