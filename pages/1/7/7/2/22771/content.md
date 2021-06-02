+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The idea of a Heyting scale comes from [[Peter Freyd]]. 

## Definition

### In terms of Heyting implication

A __Heyting scale__ or __chromatic scale__ is a [[scale]] $(M,\vert, \odot, (-)^\bullet, \bot, \top,(-)^\wedge,(-)^\vee)$ with a [[Heyting implication]] operation $(-)\rightarrow(-):M \times M \to M$ such that 

* $(\bot \rightarrow \bot)^\bullet = \bot$

* for all $a$ in $M$, $a \wedge (a \rightarrow \bot) = \bot$

* for all $a$ and $b$ in $M$, $((a \wedge b) \rightarrow \bot)^\bullet = (a \rightarrow \bot)^\bullet \wedge (b \rightarrow \bot)^\bullet$

### In terms of support

...

## Properties

Every Heyting scale with $\bot = \top$ is [[trivial object|trivial]]. 

## Relation to Girard's linear logic

...

## Examples

The set of truth values in Girard's [[linear logic]] is a Heyting scale. 

## Related concepts

* [[scale]]

* [[linear logic]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

[[!redirects Heyting scales]]

[[!redirects chromatic scale]]
[[!redirects chromatic scales]]
