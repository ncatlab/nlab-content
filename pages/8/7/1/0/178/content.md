
<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


## Idea

The notion of **$\infty$-Lie groupoid** is the generalization of the notion of [[Lie group]] and [[Lie groupoid]] from [[category theory]] to [[higher category theory]] and [[homotopy theory]]:

an $\infty$-Lie groupoid is an [[∞-groupoid]] that is _smooth_ in some sense.

One way to realize this is to pick a [[site]] $C$ of smooth test spaces -- such as [[CartSp]] or [[Diff]] -- and take a smooth $\infty$-groupoid $A$ to be an [[∞-stack]] $A : C^{op} \to $ [[∞Grpd]] on this site. 

* Evalutaed on the [[point]] $* \in C$ this encodes an ordinary [[∞-groupoid]] $A(*) \in \infty Grpd$, which is the underlying $\infty$-groupoid of our smooth $\infty$-groupoid.

* Evaluated on an object $U \in C$ this encodes an $\infty$-groupoid $A(U)$ that is to be thought of as the $\infty$-groupoid of _smooth families paramterized by $U$_ of [[object]]s, [[morphism]]s, ... [[k-morphism]]s in $A(*)$.

This way of encoding smooth structure is entirely analogous to, and in fact a generalization of, the way a [[diffeological space]] is encoded as a [[sheaf]] on [[CartSp]]. 

Accordingly, the generic [[∞-stack]] on [[CartSp]] or [[Diff]] is a smooth $\infty$-groupoid that may be a more general object than one may want to call an "$\infty$-Lie groupoid". The latter term one may want to reserve for special such stacks -- for [[geometric stack]]s and their $\infty$-categorical analogs.

Notice that for the definition of the smooth structure on a [[diffeological space]] or on an ordinary [[Lie groupoid]] it is not in fact necessary to regard these as objects tested by objects in all of [[Diff]]: since smoothness is a local property, it is entirely sufficient to know around every point in the set of [[k-morphism]]s of the $\infty$-groupoid is, what all the extensions of this point to a _ball_ -shaped smooth family of points around that point are. This is precisely what an [[∞-stack]] on [[CartSp]] encodes. See the discussion below for the difference between $\infty$-stacks on [[CartSp]] and on [[Diff]].

There are other sites on wich one may want a smooth $\infty$-groupoid to be modeled on. For instance instead of testing only with [[smooth manifold]]s, one may want to test with [[smooth loci]]. An ordinary [[sheaf]] on the category $\mathbb{L}$ of smooth loci is a generalized [[smooth space]] as considered in [[synthetic differential geometry]]. Accordingly, an $\infty$-stack on $\mathbb{L}$ may be thought of as a smooth $\infty$-Lie groupoid to which synthetic differential geometry applies.

The key difference of $\mathbb{L}$ to [[Diff]] is that the former contains smooth [[infinitesimal space]]s. Therefore an $\infty$-Lie groupoid modeled on $\mathbb{L}$ may have spaces of [[k-morphism]]s that have infinitesimal extension in some direction. Notably one obtains a notion of $\infty$-Lie groupoids for which _all $k$-morphisms are infinitesimal_ in a precise sense. It sturns out that such **infinitesimal $\infty$-Lie groupoids** may be identified with [[∞-Lie algebroid]]s: generalizations to [[higher category theory]] of [[Lie algebra]]s and [[Lie algebroid]]s.

## Relation between $\infty$-stacks on $Diff$ and on $CartSp$

In the literature on [[Lie groupoid]]s and [[differentiable stack]]s, these are traditionally conceived as [[stack]]s on the [[site]] [[Diff]] of all [[smooth manifold]]s. As mentioned above, for the purpose of encoding a smooth structure on a [[groupoid]] the category [[Diff]] regarded as a category of test objects is larger than necessary. After all, every manifold is, by definition, itself patched together from [[Cartesian space]]s, and passing to sheaves or stacks on a site really just means that one allows objects patched together from the objects in the site, so that one could just as well take the site to be just that of [[Cartesian space]]s in the first place.

More precisely, notice that we have an [[equivalence of categories]] between the [[category of sheaves]] on [[CartSp]] and on [[Diff]]

$$
  Sh(Diff) \stackrel{\simeq}{\to} Sh(CartSp)
$$

induced from the [[full and faithful functor]] $CartSp \hookrightarrow Diff$. Under this equivalence a sheaf on all of $Diff$ is simply restricted to just the subcategory [[CartSp]].

To see this, simply notice that every [[smooth manifold]] $X$ admits a [[good cover]] $\{U_i \to X\}$, where each $U_i$ is [[diffeomorphism|diffeomorphic]] to a [[Cartesian space]] (essentially by definition of [[manifold]]). By the [[sheaf]] condition, the value $A(X)$ of a sheaf on $X$ is determined by its value on these $U_i$. Hence the sheaf on [[Diff]] is already entirely determined by its restriction to [[CartSp]].


An analogous discussion holds for $\infty$-stacks on these sites. To see what is going on, the following standard example should be a helpful illustration:

...




[[!redirects Lie infinity-groupoids]]
[[!redirects infinity-Lie-groupoid]]
[[!redirects infinity-Lie-groupoids]]
[[!redirects Lie ∞-groupoid]]
[[!redirects Lie ∞-groupoids]]
[[!redirects ∞-Lie groupoid]]
[[!redirects ∞-Lie groupoids]]
[[!redirects Lie-infinity-groupoid]]