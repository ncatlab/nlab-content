
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Summary

The Tietze extension theorem says that continuous functions extend from closed subsets of a [[normal space]] $X$ to the whole space $X$. There is another less well-known variant: smooth functions on _closed_ subdomains of a smooth manifold may always be extended.


## Statement 


### In the category of smooth manifolds {#Manifolds}

+-- {: .un_theorem}
###### Theorem

For every closed subset $X \subset \mathbb{R}^n$ every smooth function $X \to \mathbb{R}$ has an extension to a smooth function $\mathbb{R}^n \to \mathbb{R}$

=--

One way to prove this is to use the fact that there is a [[full and faithful functor]]
[[Diff]] $\to \mathbb{L}$ into the category of smooth loci, discussed in the next
section. After using that fact the proof becomes trivial.


### In the category of smooth loci {#SmoothLoci}

Let $\mathbb{L} = (C^\infty Ring^{fin})^{op}$ be the category of [[smooth loci]],
the [[opposite category]] of finitely generated [[generalized smooth algebra]]s.
By the theorem discussed there, there is a [[full and faithful functor]]
[[Diff]] $\hookrightarrow \mathbb{L}$.

For $A = C^\infty(\mathbb{R}^n)/J$ and $B = C^\infty(\mathbb{R}^n)/I$
with $I \subset J$ and $B \to A$ the projection of [[generalized smooth algebra]]s
the corresponding [[monomorphism]] $\ell A \to \ell B$ in $\mathbb{L}$ 
exhibits $\ell A$ as a 
closed smooth sublocus of $\ell B$.


+-- {: .un_prop}
###### Proposition

If $\ell A \hookrightarrow \ell B$  is a closed
sublocus of $\ell B$ then every morphism $\ell A \to A$
extends to a morphism $\ell B \to R$



=--



+-- {: .proof}
###### Proof


Since we have $R = \ell C^\infty(\mathbb{R})$ and $C^\infty(\mathbb{R})$
is the free [[generalized smooth algebra]] on a single generator,
a morphism $\ell A \to R$ is precisely an element of $C^\infty(\mathbb{R}^n)/J$.
This is represented by an element in $C^\infty(\mathbb{R}^n)$ which in particular
defines an element in $C^\infty(\mathbb{R}^n)/I$.

=--


So in the category $\mathbb{L}$ of [[smooth locus|smooth loci]] the extension theorem holds trivially. 



## References

chapter I and II of

* [[Ieke Moerdijk]] and [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]