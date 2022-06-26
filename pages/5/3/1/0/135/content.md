

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition

$SmoothManifolds$ is the [[category]] whose 

* [[objects]] are [[smooth manifolds]] 

* [[morphisms]] are [[smooth functions]] between these.

Similarly, for $n \in \mathbb{N}$

$DifferentiableManifolds_n$ is the [[category]] whose 

* [[objects]] are [[differentiable manifolds]] 

* [[morphisms]] are [[differentiable functions]] between these

for $n$-fold differentiabiliy.

Each of these categories is also commonly denoted $Man$ or $Mfd$ or [[Diff]] etc.

=--


## Properties

### As a site

+-- {: .un_defn}
###### Proposition

The category $SmoothManifolds$ becomes a [[large site]] by equipping it with the [[coverage]] consisting of [[open cover]]s.

This is an [[essentially small site]]: a [[dense sub-site]] for $SmoothManifolds$ is given by [[CartSp]]${}_{smooth}$.

=--

+-- {: .proof}
###### Proof

The first statement follows trivially as for [[Top]]: the preimage of an [[open subset]] under a [[continuous function]] is again open (by definition of continuouss function).

For the second statement one needs that every [[paracompact manifold]] admits a _differentially [[good open cover]]_ : an [[open cover]] by [[open ball]]s that are [[diffeomorphic]] to a [[Cartesian space]]s. The proof for this is spelled out at [[good open cover]].

=--



+-- {: .un_corollary}
###### Corollary

The [[sheaf topos]] over $SmoothManifolds$ is a [[cohesive topos]].

The [[hypercompletion]] of the [[(∞,1)-sheaf (∞,1)-topos]] over $SmoothManifolds$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

For the first statement, use that by the _comparison lemma_ discussed at [[dense sub-site]] we have an [[equivalence of categories]]

$$
  Sh(SmoothManifolds) \simeq Sh(CartSp_{smooth})
  \,.
$$

By the discussion at [[CartSp]] we have that $CartSp_{smooth}$ is a [[cohesive site]]. By the discussion there the claim follows.

For the second statement observe that the Joyal-Jardine [[model structure on simplicial sheaves]] $Sh(SmoothManifolds)^{\Delta^{op}}_{loc}$ is a [[presentable (∞,1)-category|presentation]] for the [[hypercompletion]] of the [[(∞,1)-category of (∞,1)-sheaves]] $\hat Sh_{(\infty,1)}(SmoothManifolds)$ (see [[presentations of (∞,1)-sheaf (∞,1)-toposes]]). By the above result it follows that there is an [[equivalence of (∞,1)-categories]] between the [[hypercompletion]]s 

$$
  \hat Sh_{(\infty,1)}(SmoothManifolds) \simeq \hat Sh_{(\infty,1)}(CartSp_{smooth})
  \,.
$$

Now [[CartSp]]${}_{smooth}$ is even an [[∞-cohesive site]]. By the discussion there it follows that $Sh_{(\infty,1)}(CartSp_{smooth})$ (before [[hypercompletion]]) is a [[cohesive (∞,1)-topos]]. This means that it is in particular a [[local (∞,1)-topos]]. But this implies (as discussed there), that the [[(∞,1)-category of (∞,1)-sheaves]] already is the [[hypercomplete (∞,1)-topos]]. Therefore finally

$$
  \cdots \simeq Sh_{(\infty,1)}(CartSp_{smooth})
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

The [[cohesive topos]] $Sh(SmoothManifolds) \simeq Sh(CartSp_{smooth})$ is in particular the home of [[diffeological space]]s. See there for more details.

The [[cohesive (∞,1)-topos]]

$$
  Smooth \infty Grp := Sh_{(\infty,1)}(SmoothManifolds) \simeq Sh_{(\infty,1)}(CartSp_{smooth})
$$

is that of [[smooth ∞-groupoid]]s. Discussed at [[Smooth∞Grpd]].

The theory of [[differentiable stacks]] is that of [[geometric stack]]s in the [[(2,1)-sheaf]] [[(2,1)-topos]]

$$
  Sh_{(2,1)}(SmoothManifolds) \simeq Sh_{(2,1)}(CartSp_{smooth})
   \simeq 
  \tau_{\leq 1} Sh_{(\infty,1)}(CartSp_{smooth})
$$


=--

## Related concepts

* [[CartSp]]${}_{top}$ ,  [[TopMfd]]

* [[CartSp]]${}_{smth}$ 

* [[Diff]]


category: category


[[!redirects Man]]
[[!redirects Mfd]]

[[!redirects SmoothMfd]]
[[!redirects SmthMfd]]
[[!redirects SmthManifolds]]

