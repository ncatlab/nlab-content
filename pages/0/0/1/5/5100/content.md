
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let  $\mathbb{C}$ and $\mathbb{D}$ be $\mathbb{E}$-[[indexed categories]]. 

Then an **$\mathbb{E}$-indexed functor** $F:{\mathbb{C}}\to{\mathbb{D}}$ is a [[functor]] that assigns to each [[object]] $A$ of $\mathbb{E}$ a functor $F^A:{\mathbb{C}}^A\to{\mathbb{D}}^A$ and to each [[morphism]] $f:A\to B$ of $\mathbb{E}$ a [[natural isomorphism]] from $F^B$ to $F^A$ (note reversal of direction).

+-- {: .standout}

Would it be fair to define a "weak indexed functor" as above except with a natural transformation rather than natural isomorphism?  I'm starting to wonder why Johnstone bothered reversing the direction if the components are all isos. -- [[Adam]]

=--

## References

* [[Peter Johnstone]], _[[Sketches of an Elephant]]: A Topos Theory Compendium_ Clarendon Press; New York: Oxford University Press, 2002, (p260)

[[!redirects indexed functors]]