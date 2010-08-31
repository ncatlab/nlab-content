
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[higher category theory]], the _exchange law_, or _interchange law_, states that the multiple ways of forming the composite of a [[pasting diagram]] of [[k-morphism]]s are equivalent.

## Examples

The first exchange law (often called _the_ exchange law) asserts that for composition of 2-morphisms we have an equivalence

$$
  \array{
    && 1 &&&& 3
    \\
    & \nearrow &\Uparrow& \searrow && \nearrow && \searrow
    \\
    0 &&\to&& 2 &&  && 4
    \\
    &&  &&&& 3
    \\
    & && && \nearrow &\Uparrow& \searrow
    \\
    0 &&\to&& 2 && \to && 4  
  }
  \;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;
  \array{
    && 1 &&&& 3
    \\
    & \nearrow && \searrow && \nearrow &\Uparrow& \searrow
    \\
    0 &&&& 2 && \to && 4
    \\
    && 1 &&&& 
    \\
    & \nearrow &\Uparrow& \searrow &&  && 
    \\
    0 &&\to && 2 && \to && 4  
  }
$$

asserting a compatibility of [[horizontal composition]] and [[vertical composition]] of [[2-morphism]]s.

In a [[bicategory]] this equivalence is an identity. In even higher (and non-[[semi-strict n-category|semi-strict]]) category theory, the interchange law becomes a higher morphism itself: the _exchanger_.

## Combinatorics of exchange laws

One way to capture all exchange laws combinatorially is encoded by the cosimplicial $sSet$-cateory $S : \Delta \to sSet Cat$ that induces the [[homotopy coherent nerve]]. See there for more details on how this encodes the exchange laws.


[[!redirects interchange law]]
[[!redirects exchange laws]]
[[!redirects interchange laws]]
[[!redirects exchanger]]
[[!redirects exchangeor]]
[[!redirects exchangor]]
[[!redirects interchanger]]
[[!redirects interchangeor]]
[[!redirects interchangor]]