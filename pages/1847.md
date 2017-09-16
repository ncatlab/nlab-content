
# Definition #

A [[topological space]] $X$ is **paracompact** if every open [[cover]]ing $U$ has a [[refinement]] by an open covering $V$ that is _locally finite_, i.e. such that every point has a neighbourhood that intersects only finitely many open subsets in $V$ .

Often one requires a paracompact space to be [[Hausdorff space|Hausdorff]] as well; the issues here are the same as those for [[compact space]]s.


For paracompact spaces, [[numerable open cover|numerable open covers]] are cofinal in all open covers.


# Examples #

* locally compact spaces

  * every [[compact space]] is paracompact;

  * any [[second-countable space|second-countable]] [[locally compact space|locally compact]] Hausdorff space is paracompact;

* manifolds

  * a finite-dimensional [[manifold]] is paracompact precisely if it is [[second-countable space|second countable]]

  *  and precisely if it is [[metric space|metrizable]]

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

* special cases

  * the [[Sorgenfrey line]] is a good example of a paracompact space that doesn\'t fit into other general classes of paracompact spaces;

* counterexamples

  * the [[long line]] is *not* paracompact, even though it is a [[manifold]] (unless one specifically requires paracompactness of manifolds) but it fails to be 
[[second-countable space|second-countable]].


# Properties #

__Dieudonne's theorem__: Every paracompact Hausdorff space is [[normal space|normal]]. A __paracompactum__ is by definition any paracompact Hausdorff space. 

## cohomology of paracompact spaces ##

* On paracompact spaces, abelian [[Cech cohomology]] does compute [[abelian sheaf cohomology]], 

  i.e. the canonical morphism $H_{Cech}(X,A) \to H(X,A)$ for  $A$ any [[chain complex]] of [[sheaf|sheaves]] is an [[isomorphism]] when the [[topological space]] underlying $X$ is paracompact.

# References #

*  the English Wikipedia\'s [article](http://en.wikipedia.org/wiki/Paracompact_space)

A discussion is for instance around page 32 of

* Brylinski, _Loop spaces, characteristic classes geoemtric quantization_

# Discussion #

A previous version caused the following discussion, which is probably taken care of now.

+-- {: .query}

[[Urs Schreiber]]: there is an inconsistency here with what it says at [[locally compact space]]: there it says that every topological manifold is locally compact and that the long line is a topological manifold. Here it says that every locally compact space is paracompact, but that the long line is not.

Apparently the same inconsistency is in the relevant Wikipedia entries. 

Or am I missing something?

_Zoran_ Sometimes people do consider nonparacompacts manifolds, but it is standard to assume that we work with paracompact ones. 

[[Urs Schreiber]]: Probably my mistake was that I missed the "second countable" clause above. 

So every second countable fin-dim manifold is paracompact. 
=--




[[!redirects Dieudonne's theorem]]
[[!redirects Dieudonne theorem]]
[[!redirects paracompact spaces]]