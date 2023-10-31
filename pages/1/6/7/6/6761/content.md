
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# The representable functor theorem
* table of contents
{: toc}

## Statement

The __representable functor theorem__ states that a [[Set]]-valued [[functor]] on a [[cocomplete category]] is [[representable functor|representable]] if and only if it is [[continuous functor|continuous]] and has a [[solution set condition|solution set]].

Dually, a [[Set]]-valued [[presheaf]] on a [[complete category]] is [[representable functor|representable]] if and only if it takes [[colimits]] to [[limits]] and has a [[solution set condition|solution set]].

## Related facts

As representable functors are closely connected to [[adjoint functors]], this theorem is essentially equivalent to the [[adjoint functor theorem]] and to theorems guaranteeing the existence of [[limits]].

Specifically, assuming that $C$ is [[copowered]] over [[Set]] (in particular, this is true if $C$ is [[cocomplete]]), a functor $C\to Set$
is a right adjoint functor if and only if it is representable, in which case the left adjoint functor $Set\to C$ sends the [[singleton]] set to the representing object, and more generally a set $X$ to the [[copower]] of $X$ with the representing object.

## Related concepts

* [[adjoint functor theorem]]


[[!redirects representable functor theorem]]
