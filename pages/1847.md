
# Definition #

A [[topological space]] $X$ is **paracompact** if every open [[cover]]ing $U$ has a [[refinement]] by an open covering $V$ that is _locally finite_, i.e. such that every point has a neighbourhood that intersects only finitely many open subsets in $V$ .

Often one requires a paracompact space to be [[Hausdorff space|Hausdorff]] as well; the issues here are the same as those for [[compact space]]s.  In particular, a __paracompactum__ is a paracompact Hausdorff space.


# Examples #

* locally compact spaces

  * every [[compact space]] is paracompact;

  * any [[second-countable space|second-countable]] [[locally compact space|locally compact]] Hausdorff space is paracompact;


* manifolds

  *  finite-dimensional manifolds are locally compact, but we also have some converses:

     * a finite-dimensional Hausdorff topological [[manifold]] is paracompact precisely if it is [[metric space|metrizable]]

     * a finite-dimensional [[connected space|connected]] Hausdorff topological manifold (actually, it can have up to [[countable set|countably]] many components) is paracompact precisely if it is [[second-countable space|second countable]]

     * a finite-dimensional Hausdorff topological manifold is paracompact precisely if each component is second-countable

   * infinite-dimensional manifolds are generally not locally compact, but we still have some results:

     * The [[Frechet manifold]] of smooth loops of a compact finite dimensional manifold is paracompact 


     * More generally, if $E$ is the sequential [[limit]] of separable Hilbert spaces $H_n$, such that the canonical projections
       $$
         p_n : E \to H_n
       $$
       satisfy
       $$
         closure(p_n^{-1}(B)) = p_n^{-1}(closure(B))
       $$

       for any open ball $B$ in $H_n$, then $E$ is paracompact, and so is any manifold modelled on $E$. Such a manifold is called an _[[ILH-manifold]]_, $E$ is an _[[ILH-space]]_. In particular, [[Hilbert manifold|Hilbert manifolds]] are paracompact.

       ( _Bry_ , section I.4)

       +-- {: .query}
       [[Urs Schreiber]]: don't we need some extra assumption here? Otherwise why wouldn't this imply  that every space modeled on $\mathbb{R}^n$ is paracompact, while it is only the second-countable such that are?

       _Toby_:  Probably Brylinski has a requirement of metrisability or something.

       [[Andrew Stacey]]: Consider a locally connected space $X$ whose connected components are paracompact.  As $X$ is locally connected, the connected components, say $\{X_\lambda\}$, are open.  Thus any open cover, say $\mathcal{U}$, of $X$ has a refinement by open sets, say $\mathcal{V}$, such that each $V \in \mathcal{V}$ is contained in some $X_\lambda$.  Thus we can write $\mathcal{V} = \coprod \mathcal{V}_\lambda$.  As each $X_\lambda$ is paracompact, each $\mathcal{V}_\lambda$ has a locally finite refinement, say $\mathcal{W}_\lambda$.  Then let $\mathcal{W} := \coprod \mathcal{W}_\lambda$.  As each $\mathcal{W}_\lambda$ is a refinement of the corresponding $\mathcal{V}_\lambda$, $\mathcal{W}$ is a refinement of $\mathcal{V}$, and hence of $\mathcal{U}$.  As each point of $X$ has a neighbourhood which meets only elements of _one_ of the $\mathcal{W}_\lambda$, and as that $\mathcal{W}_\lambda$ is locally finite, $\mathcal{W}$ is locally finite.  Thus $\mathcal{U}$ has a locally finite refinement.

       More generally, the coproduct of paracompact spaces is again paracompact.

       Spivak, in _A Comprehensive Introduction to Differential Geometry, I_ has an appendix on non-metrisable manifolds.  He starts (in the appendix) by defining a manifold to be a Hausdorff locally Euclidean space.  Then he proves that for any manifold $M$ TFAE:

       1. Each component of $M$ is $\sigma$-compact.
       2. Each component of $M$ is second countable.
       3. $M$ is metrisable.
       4. $M$ is paracompact.

       The bit to highlight is the words "Each component of ..." in the first two.
       =--



* metric spaces

  * every [[separable space|separable]] [[metric space]] is paracompact;

  * every [[metric space]] whatsoever is paracompact, assuming the [[axiom of choice]];

  * pseudometric spaces are paracompact under the same conditions, if one does not require Hausdorffness;

* In particular we have the following implications

  * [[second-countable space]] and [[regular space]]
    $\Rightarrow$ [[metric space|metrizable space]]
    $\Rightarrow$ paracompact space

    (the first is Urysohn's metrization theorem, the second is due to A. H. Stone)

  * paracompact space and locally metric space
    $\Rightarrow$
    [[metric space|metrizable space]]

    (this is due to Smirnov)


* special cases

  * the [[Sorgenfrey line]] is a good example of a paracompact space that doesn\'t fit into other general classes of paracompact spaces (in particular, it is not metrisable, locally compact, or a manifold);

* counterexamples

  * the [[long line]] is *not* paracompact, even though it is a [[manifold]] (unless one specifically requires paracompactness of manifolds) but it fails to be [[second-countable space|second-countable]] (even though it is connnected) or metrisable.


# Properties #

* __Dieudonne's theorem__: Every paracompact Hausdorff space is [[normal space|normal]].

* every paracompact finite-dimensional [[manifold]] has a [[partition of unity]]

* For paracompact spaces, [[numerable open cover|numerable open covers]] are cofinal in all open covers.

## cohomology of paracompact spaces ##

* On paracompact spaces, abelian [[Cech cohomology]] does compute [[abelian sheaf cohomology]], 

  i.e. the canonical morphism $H_{Cech}(X,A) \to H(X,A)$ for  $A$ any [[chain complex]] of [[sheaf|sheaves]] is an [[isomorphism]] when the [[topological space]] underlying $X$ is paracompact.

# References #

*  the English Wikipedia\'s [article](http://en.wikipedia.org/wiki/Paracompact_space)

A discussion with an eye towards [[abelian sheaf cohomology]] and abelian [[Cech cohomology]] is around page 32 of

* **Bry** Brylinski, _Loop spaces, characteristic classes geoemetric quantization_






[[!redirects Dieudonne's theorem]]
[[!redirects Dieudonne theorem]]
[[!redirects paracompact spaces]]