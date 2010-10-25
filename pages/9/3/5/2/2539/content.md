
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

The _Tietze extension theorem_ says that [[continuous function]]s extend from [[closed subset]]s of a [[normal space]] $X$ to the whole space $X$. 


## Statement 

### For topological spaces


+-- {: .un_theorem}
###### Theorem

For $X$ a [[normal topological space]] and $A \subset X$ a [[closed subset]], there is for every [[continuous function]] $f : A \to \mathbb{R}$ to the [[real line]] a continuous function $F : X \to \mathbb{R}$ extending it, i.e. such that $F|_A = f$.

=--


### In the category of smooth manifolds and smooth loci {#Manifolds}

Let $\mathbb{L} = (C^\infty Ring^{fin})^{op}$ be the category of [[smooth loci]],
the [[opposite category]] of finitely generated [[generalized smooth algebra]]s.
By the theorem discussed there, there is a [[full and faithful functor]]
[[Diff]] $\hookrightarrow \mathbb{L}$.

+-- {: .un_def}
###### Definition

For $A = C^\infty(\mathbb{R}^n)/J$ and $B = C^\infty(\mathbb{R}^n)/I$
with $I \subset J$ and $B \to A$ the projection of [[generalized smooth algebra]]s
the corresponding [[monomorphism]] $\ell A \to \ell B$ in $\mathbb{L}$ 
exhibits $\ell A$ as a **closed smooth sublocus** of $\ell B$.

=--

+-- {: .un_lemma}
###### Lemma

Let $X$ be a [[smooth manifold]] and let $\{g_i \in C^\infty(X)\}_{i = 1}^n$ be [[smooth function]]s that are independent in the sense that at each common zero point $x\in X$, $\forall i : g_i(x)= 0$ we have the [[derivative]] $(d g_i) : T_x X \to \mathbb{R}^n$ is a surjection, then the ideal $(g_1, \cdots, g_n)$ coincides with the ideal of functions that vanish on the zero-set of the $g_i$.

=--

This is lemma 2.1 in ([MoerdijkReyes](#MoerdijkReyes)).

+-- {: .un_prop}
###### Proposition

If $\ell A \hookrightarrow \ell B$  is a closed
sublocus of $\ell B$ then every morphism $\ell A \to A$
extends to a morphism $\ell B \to R$



=--

This is prop. 1.6 in ([MoerdijkReyes](#MoerdijkReyes)).

+-- {: .proof}
###### Proof


Since we have $R = \ell C^\infty(\mathbb{R})$ and $C^\infty(\mathbb{R})$
is the free [[generalized smooth algebra]] on a single generator,
a morphism $\ell A \to R$ is precisely an element of $C^\infty(\mathbb{R}^n)/J$.
This is represented by an element in $C^\infty(\mathbb{R}^n)$ which in particular
defines an element in $C^\infty(\mathbb{R}^n)/I$.

=--




## References

The smooth version is discussed in  chapter I and II of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_
{#MoerdijkReyes}