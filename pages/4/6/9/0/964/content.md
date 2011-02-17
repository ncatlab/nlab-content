
> This entry is about the notion of _frame_ in [[topos theory]]. For other notions, see elsewhere.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **frame** $A$ is 

* a [[partial order|poset]] 

* that has 

  * all [[join|joins]] $\wedge$

  * all [[finite limit|finite]] [[meet|meets]] $\vee$

* and which satisfies the _infinite distributive law_:

  $$ 
    x \wedge (\bigvee_i y_i) \leq \bigvee_i (x\wedge y_i)
  $$

  for all $x, \{y_i\}_i$ in $A$

  (Note that the converse holds in any case, so we have equality.)

A _frame homomorphism_ is a homomorphism of posets that preserves finite meets and arbitrary joins. Frames and frame homomorphisms form the category [[Frm]].

## Properties

A frame is automatically a [[Heyting algebra]] by the [[adjoint functor theorem]], so you can think of a frame as a [[cartesian closed category|cartesian closed]] [[suplattice]], or a cartesian [[quantale]].  

But notice that the frame [[homomorphism]]s are not required to preserve the Heyting implication.


## Formal duals: locales

The [[opposite category]] to the category [[Frm]] is the category [[Loc]] of [[locale]]s (possibly slightly generalized [[topological space]]s)

$$
  Loc := Frm^{op}
$$

Conversely, any [[topological space]] has a [[frame of opens|frame of open subsets]].  (In fact, one definition of a topological space is a set equipped with a subframe of its [[power set]].)


[[!redirects frames]]
