
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


[[Finn Lawler|Finn]]:  The components of the transformation $F$ are not invertible in general --- it's the 2-cells in the naturality squares for $F$ that are isos.

You might be thinking of [[lax natural transformations]].  B&#233;nabou has done some work on generalizing Grothendieck's correspondence between pseudofunctors (i.e. indexed categories) and fibrations where lax transformations turn up.  See e.g. some lecture notes [here](http://www.mathematik.tu-darmstadt.de/~streicher/FIBR/DiWo.pdf).

Finn, after I wrote my comment somebody completely rewrote the page; you saw a comment which referred to a previous version.  I had copied the original version directly from the [[Elephant]]; it says "natural isomorphism" quite clearly on page 260.  Perhaps this new definition is better.  Who knows.  Anyways, I've deleted the reference since the page now describes something different. -- [[Adam]]

[[Finn Lawler|Finn]]:  You can see the revision history of a page by clicking on the **History** link below.  After you created the page [[Urs Schreiber|Urs]] tidied it up but didn't change the content.

The Elephant gives essentially the same definition as above; in particular, the 'natural isomorphism' it mentions is (in this page's notation) between $\mathbb{D}(f) \circ F^B$ and $F^A \circ \mathbb{C}(f)$ as above, not $F^B$ and $F^A$ as you'd written.

=--


[[!redirects indexed functors]]