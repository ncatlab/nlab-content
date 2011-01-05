
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### Traditional

+-- {: .un_defn}
###### Definition

A **smooth manifold** is a [[manifold]] if its transition functions are [[smooth function]]s $\mathbb{R}^n \to \mathbb{R}^n$. 

So a smooth manifold is a $C^k$-[[differentiable manifold]] for all $k$.

=--

A [[homomorphism]] of smooth manifolds is a [[smooth function]]s. Smooth manifolds and smooth functions form the category [[Diff]].

### Topos-theoretic

Let [[CartSp]] be the [[category]] of [[Cartesian space]]s and [[smooth function]]s between them. This has finite [[product]]s and is in fact (the [[syntactic category]]) of a [[Lawvere theory]]: the theory of [[smooth algebras]].

Moreover, $CartSp$ is naturally equipped with the [[good open cover]] [[coverage]] that makes it a [[site]]. 

Both properties together make it a [[pregeometry (for structured (∞,1)-toposes)]] (if the notion of [[Grothendieck topology]] is relaxed to that of [[coverage]] in [StrSp](#StrSp)).

This means there is canoncally a notion of [[CartSp]]-[[generalized scheme]]s ([StrSp](#StrSp)).

+-- {: .un_prop}
###### Claim

Smooth manifolds are equivalently the [[n-localic (infinity,1)-topos|0-localic]] [[CartSp]]-[[generalized scheme]]s of locally finite presentation.

=--

+-- {: .proof}
###### Sketch of proof

The statement says that a smooth manifold $X$ may be identified with an [[∞-stack]] on [[CartSp]] (an [[∞-Lie groupoid]]) which is represented by a [[CartSp]]-[[structured (∞,1)-topos]] $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ such that

1. $\mathcal{X}$ is a [[n-localic (∞,1)-topos|0-localic (∞,1)-topos]];

1. There exists a family of objects $\{U_i \in \mathcal{X}\}$ such that the canonical morphism $\coprod_i U_i \to *_{\mathcal{X}}$ to the [[terminal object in an (∞,1)-category|terminal object]] in $\mathcal{X}$ is a [[regular epimorphism]];

1. For every $i \in I$ there is an equivalence

  $$
    (\mathcal{X}/U_i, \mathcal{O}_{\mathcal{X}|U_i})
    \underoverset{\simeq}{t_i}{\to} (Sh_{(\infty,1)}(\mathbb{R}^n), \mathcal{O}(\mathbb{R}^n))
     \,.
  $$

The second and third condition say in words that $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is locally equivalent to the ordinary cannonically [[CartSp]]-[[locally ringed space]] $\mathbb{R}^n$ (for $n \in \mathbb{N}$ the [[dimension]]. The first condition then says that these local identifications cover $\mathcal{X}$.

(...)

(...)


=--



## References

* [[Jacob Lurie]], _[[Structured Spaces]]_
{#StrSp}

[[!redirects smooth manifolds]]
