#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The Tietze extension theorem says that smooth functions on _closed_ subdomains may always be extended.

# Statement #


## in the category of smooth manifolds ##

**Theorem**

For every closed subset $X \subset \mathbb{R}^n$ every smooth function $X \to \mathbb{R}$
has an extension to a smooth function $\mathbb{R}^n \to \mathbb{R}$

One way to prove this is to use the fact that there is a [[full and faithful functor]]
[[Diff]] $\to \mathbb{L}$ into the category of smooth loci, discussed in the next
section. After using that fact the proof becomes trivial.


## in the category of smooth loci ##

Let $\mathbb{L} = (C^\infty Ring^{fin})^{op}$ be the category of [[smooth loci]],
the [[opposite category]] of finitely generated [[generalized smooth algebra]]s.
By the theorem discussed there, there is a [[full and faithful functor]]
[[Diff]] $\hookrightarrow \mathbb{L}$.

For $A = C^\infty(\mathbb{R}^n)/J$ and $B = C^\infty(\mathbb{R}^n)/I$
with $I \subset J$ and $B \to A$ the projection of [[generalized smooth algebra]]s
the corresponding [[monomorphism]] $\ell A \to \ell B$ in $\mathbb{L}$ 
exhibits $\ell A$ as a 
closed smooth sublocus of $\ell B$.

**Proposition** If $\ell A \hookrightarrow \ell B$  is a closed
sublocus of $\ell B$ then every morphism $\ell A \to A$
extends to a morphism $\ell B \to R$

**Proof**

Since we have $R = \ell C^\infty(\mathbb{R})$ and $C^\infty(\mathbb{R})$
is the free [[generalized smooth algebra]] on a single generator,
a morphism $\ell A \to R$ is precisely an element of $C^\infty(\mathbb{R}^n)/J$.
This is represented by an element in $C^\infty(\mathbb{R}^n)$ which in particular
defines an element in $C^\infty(\mathbb{R}^n)/I$.

So in $\mathbb{L}$ the extension theorem holds trivially. 

#References#

chapter I and II of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]