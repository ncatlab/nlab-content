
<div class="rightHandSide toc">
[[!include topology - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **nerve theorem** asserts that the [[homotopy type]] of a sufficiently nice [[topological space]] is encoded in the [[Cech nerve]] of a [[good cover]].

## Statement

+-- {: .un_theorem}
###### Theorem

Let $X$ be a [[paracompact space]] and $\{U_i \to X\}$ a [[good open cover]]. Write $C(\{U_i\})$ for the [[Cech nerve]] of this cover

$$
  C(\{U_i\}) = \left(
    \stackrel{\to}{\stackrel{\to}{\to}}\coprod_{i,j} U_i \cap U_j \stackrel{\to}{\to} \coprod_{i} U_i
  \right)
  \,,
$$

(a [[simplicial object|simplicial]] [[space]]) and write 

$$
  \tilde C(\{U_i\}) = \left(
    \stackrel{\to}{\stackrel{\to}{\to}}\coprod_{i,j} * \stackrel{\to}{\to} \coprod_{i} *
  \right)
$$

for the [[simplicial set]] obtained by replacing in $C(\{U_i\})$ each [[direct sum]]mand space by the [[point]]. Let $|\tilde C(\{U_i\})|$ be the [[geometric realization]]. 

This is [[homotopy equivalence|homotopy equivalent]] to $X$.

=--

## $(\infty,1)$-Topos-theoretic interpretation

There is a useful [[nPOV]] interpretation of the meaning of the nerve theorem. For details see [[homotopy groups in an (∞,1)-topos]].

We may think of the [[manifold]] $X$ as an object in the [[(∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$, the [[(∞,1)-category of (∞,1)-sheaves]] on the [[site]] [[CartSp]] with the [[good open cover]] [[coverage]] (details are at [[∞-Lie groupoid]]). This is [[presentable (∞,1)-category|presented]] by the projective [[model structure on simplicial presheaves]], [[Bousfield localization of model categories|left Bousfield localized]] at [[Cech nerve]]s of [[good cover]]s.

$$
  Sh_{(\infty,1)}(CartSp) \simeq (sPsh(CartSp)_{proj,cov})^\circ
  \,.
$$

By the general characterization of <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#CofibrantObjects">cofibrant objects</a> and <a href="http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#Descent">local weak equivalences</a> one finds that the [[Cech nerve]] of a [[good open cover]] of $X$ provides a cofibrant replacement of $X$ in $sPSh(C)_{proj,cov}$

$$
  C(\{U_i\}) \stackrel{\simeq}{\to} X
  \,.
$$

Here the fact that the cover is _good_ is crucial for this to be cofibrant, a general [[open cover]] will not do: cofibrant objects in $sPSh(C)_{proj}$ are obtained as simplicial presheaves whose degenerate cells in each degree split off a direct sums (which is the case for any open cover) and which in addition are degreewise coproducts of representables (this is on the site [[CartSp]] the case for Cech nerver of good open covers).

The point of working over the site [[CartSp]] here is that this makes $Sh_{(\inftty,1)}(CartSp)$ a [[locally ∞-connected (∞,1)-topos]], which means that the _[[left adjoint]]_ to the [[constant (∞,1)-sheaf]]-functor 

$$
  \Pi : Sh_{(\infty,1)}(CartSp) \to \infty Grpd
$$

exists. This is the left [[derived functor]] of the functor which sends each [[representable functor|representable]] to the point. Accordingly, it acts on an arbitrary object by forming a cofibrant replacement and then identifying in that each representable with the point. By the above, this means that applied to $X$ it produces precisely the simplicial set $\tilde C(\{U_i\})$:

$$
  \Pi(X) \simeq \lim_{\to} C(\{U_i\}) = \tilde C(\{U_i\})
  \,.
$$

Regarded from this perspective, the nerve theorem states that with ([[paracompact space|paracompact]]) [[manifold]]s regarded as objects in the [[locally ∞-connected (∞,1)-topos]] $Sh_{(\infty,1)}(CartSp)$, the [[schreiber:path ∞-groupoid]] functor $\Pi : Sh_{(\infty,1)}(CartSp) \to \infty Grpd$ remembers their nature as objects in [[Top] $\simeq$ [[∞Grpd]].
 

## References

The nerve theorem appears as corollary 4G.3 in 

* [[Allen Hatcher]], _Algebraic topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html))