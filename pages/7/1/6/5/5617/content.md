
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _volume form_ on a [[Riemannian manifold]] $(X,g)$ is the [[differential form]] whose [[integral]] over pieces of $X$ computes the [[volume]] of $X$ as measured by the [[metric]] $g$.

## Definition

For $(X,g)$ a [[Riemannian manifold]] of [[dimension]] $n$, its **volume form** $vol_g \in \Omega^n(X)$ is the [[differential form]] of degree $n$ that is defined by one of the following equivalent statements.

* The volume form is the image under the [[Hodge star]] operator $\star_g : \Omega^k(X) \to \Omega^{n-k}(X)$ of the [[smooth function]] $1 \in \Omega^0(X)$

  $$
    vol_g = \star_g 1
    \,.
  $$

* For $(E, \Omega) : T X \to iso(n)$ the [[Lie algebra valued differential form]] on $X$ with values in the [[Poincare Lie algebra]] $iso(n)$ that encodes the metric (the _[[spin connection]]_ $\Omega$ with the _[[vielbein]]_ $E$) the volume form is the image of $(E,\Omega)$ under the canonical volume [[Lie algebra cohomology|Lie algebra cocycle]] $vol \in CE(iso(n))$:

  $$
    vol_g = vol(E)
    \,.
  $$

  See [[Poincare Lie algebra]] for more on this.

[[!redirects volume forms]]