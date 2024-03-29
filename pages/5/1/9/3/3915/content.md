
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
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

+-- {: .num_defn}
###### Definition

For $i : X \hookrightarrow Y$ an [[immersion]] (notably an [[embedding]]) of [[smooth manifolds]], the **normal bundle** of $X$ in $Y$ relative to $i$ is the  [[vector bundle]] 

$$
  N_i X  \to X
$$

defined as the [[fiber|fiberwise]] [[quotient]] bundle 

$$
  N_i X =\frac{i^* T Y}{T X}  
$$

If $Y$ is equipped with [[Riemannian metric]] structure then this is equivalently the space of [[tangent vectors]] to $Y$ which are [[normal vectors]] to the [[tangent vectors]] to $X$, whence the name.

=--

The pullback $i^* T Y$ can be of course interpreted as the restriction $T Y|_X$. The normal bundle is [[fiber]]wise the [[quotient]] of the fiber of the [[tangent bundle]] of $Y$ by the fiber of the [[tangent bundle]] of $X$: for $x \in X$

$$
  N_i (X)_x =  T_{i(x)}Y/T_x(X)
  \,.
$$

The dual notion is that of [[conormal bundle]]. The notion also makes sense for some other contexts, e.g. for smooth algebraic varieties. 

+-- {: .num_remark}
###### Remark


There is always an [[isomorphism]]

$$
  T X \oplus N_i X  \simeq T Y|_X
  \,,
$$

but it is not canonically given, hence in particular cannot it general be chosen [[natural transformation|naturally]]. Except if certain additional structure is given:

If $Y$ is equipped with a [[Riemannian metric]] $g$, then we may identify the normal bundle with the bundle of [[vector]]s that are _orthogonal_  to ("normal to") the vectors in $T X$:

$$
  N_i(X) \simeq (T X)^\perp :=
  \{
    (x,v) \in T Y|_{X} | \forall w \in T_x X :  g(v,w) = 0
  \}
  \,.
$$

=--

Let $M^n$ be a smooth compact $n$-dimensional manifold without boundary, then the question of triviality of the normal bundle for an embedding $M^n\hookrightarrow \mathbf{R}^{n+r}$ for sufficiently large $r$ does not depend on the embedding. For this one uses the fact that any two such embeddings are regularly homotopic (this means the existence of a smooth homotopy $H(x,t)$ which is immersion for every $t \in [0,1]$ and which induces on the level of differentials a homotopy for the tangent bundles) and that any two regular homotopies are themselves homotopic through regular homotopies leaving end points fixed. Then one just uses the homotopy invariance of vector bundles. Thus, if $M^n$ admits an embedding into $\mathbf{R}^{n+r}$ with a trivial normal bundle then one says that $M^n$ has a __stably trivial normal bundle__. In that case, if $M^n_+$ is the union of $M$ with a disjoint base point, then there is a homeomorphism $T (M^n\times \mathbf{R}^{r})\cong \Sigma^r M^n_+$ where $\Sigma^r$ denotes the $r$-fold (reduced) suspension of based spaces $(S^r\times M^n_+)/(S^r\wedge M_+)$.

## Related concepts

* Normal bundle plays a central role for instance in the theory of [[fiber integration]] by means of [[Pontrjagin-Thom collapse map]]s.

* [[tubular neighbourhood]], [[conormal bundle]]

## Literature

* [[Victor Snaith]], _Stable homotopy around the Arf-Kervaire invariant_, Birkhauser 2009

[[!redirects normal bundles]]

