
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

Let  $\mathbb{C}$ and $\mathbb{D}$ be $\mathbb{E}$-[[indexed categories]], that is, [[pseudofunctors]] $\mathbb{E}^\mathrm{op} \to Cat$.

Then an **$\mathbb{E}$-indexed functor** $F:{\mathbb{C}}\to{\mathbb{D}}$ is a [[pseudonatural transformation]] $F \colon \mathbb{C} \Rightarrow \mathbb{D}$: it assigns to each [[object]] $A$ of $\mathbb{E}$ a functor $F^A:{\mathbb{C}}^A\to{\mathbb{D}}^A$ and to each [[morphism]] $f:A\to B$ of $\mathbb{E}$ a coherent [[isomorphism]] $\mathbb{D}(f) \circ F^B \cong F^A \circ \mathbb{C}(f)$.

+-- {: .query}

Would it be fair to define a "weak indexed functor" as above except with a natural transformation rather than natural isomorphism?  I'm starting to wonder why Johnstone bothered reversing the direction if the components are all isos. -- [[Adam]]

[[Finn Lawler|Finn]]:  The components of the transformation $F$ are not invertible in general --- it's the 2-cells in the naturality squares for $F$ that are isos.

You might be thinking of [[lax natural transformations]].  B&#233;nabou has done some work on generalizing Grothendieck's correspondence between pseudofunctors (i.e. indexed categories) and fibrations where lax transformations turn up.  See e.g. some lecture notes [here](http://www.mathematik.tu-darmstadt.de/~streicher/FIBR/DiWo.pdf).

=--

## References

* [[Peter Johnstone]], _[[Sketches of an Elephant]]: A Topos Theory Compendium_ Clarendon Press; New York: Oxford University Press, 2002, (p260)

[[!redirects indexed functors]]