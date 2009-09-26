<div class="rightHandSide toc">
[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]
</div>

A general idea of Grothendieck is that to do a geometry more general than schemes instead of the gluing of affine schemes as ringed spaces, one glues the functors of points; hence **a space is simply a sheaf of sets on some category $Loc$ of local models in a Grothendieck topology** $\tau$ on. If the local model are the usual affine schemes, then Grothendieck calls the outcome a $\tau$-locally affine space, rather than a scheme. The usual schemes are obtained for $\tau=Zariski$ and $Loc=Aff$. Algebraic spaces are another example. In general various generalizations which do not have exactness properties of Zariski or etale coverings, are usually among algebraic geometers called generalized _spaces_ rather than (generalized) _schemes_; thus the terminology almost scheme is OK because though the local objects are more general the exactness properties are basically the same (similarly for derived schemes of Toen et al. noncommutative schemes of Rosenberg etc.). 

There are many generalizations of [[schemes]], some are even called by their respective authors generalized schemes (e.g. Lurie, Durov). Deligne in [[Catégories Tannakiennes]] suggested algebraic geometry in arbitrary symmetric monoidal category. 
Aspects of toric geometry and the foundations of the geometry over a field of one element (Smirnov-Kapranov, Dietmar, Connes...) can be founded using structure sheaves of monoids, not rings. Another example is tropical geometry. Rings are sometimes noncommutative (e.g. D-schemes of Beilinson); the underlying topological space can be replaced by a site, locale, topos or a non-distributive lattice by localizations. Usual commutative unital rings suffice for manifolds, rigid analytic spaces, schemes, formal schemes and so on. The emphasis in Lurie is to categorify the space and to take the homotopy version of a ring, restating a formalism fitting the [[derived algebraic geometry]], mainly of Simpson's school.  

#Generalized scheme formalism of Lurie#

One notion of  _generalized scheme_ or _$G$-scheme_ is a generalization of the notion of [[scheme]] from [[algebraic geometry]] to [[geometry]] more generally and from [[geometry]] to [[higher geometry]]. In particular it yields a generalization of [[scheme]] to the context of [[derived algebraic geometry]] but also for instance a generalization of the notion of [[manifold|smooth manifold]] to [[derived smooth manifold]].

Recall that one way to define a [[scheme]] is as a [[ringed space]], namely as a [[topological space]] $X$ with a special [[ring]]-valued [[sheaf]] $O \in Sh(X,Rings)$ on (the [[category of open subsets]] of) $X$ singled out: the _structure sheaf_ that assigns to a subset $U \subset X$ the [[ring]] of _admissible functions_ on $U$.

Using the [[category theory|general nonsense]] of [[space and quantity]] one may regard a ring-valued sheaf on $X$ as a sheaves-of-sets-valued presheaf on rings, i.e. as a functor  $O : Rings^{op} \to Sh(X,Set)$ =: Sh(X). 

This is useful because $Sh(X)$ is a [[topos]] (a [[Grothendieck topos]]) and as such has a good theory for higher generalizations in [[higher topos theory]]: to every [[topological space]] $X$ we have not just the 1-[[topos]] of [[sheaf|sheaves]], but also the [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-topos of (infinity,1)-sheaves]] (often called [[infinity-stack]]s).

A **generalized scheme** is essentially a [[topological space]] $X$ together with a prescribed functor
 
$$
  G \to Sh_\infty(X)
$$

from some category $G$ of [[geometry (for structured (infinity,1)-toposes)]]

such that it locally looks like an _affine $G$-scheme_ in  that

So a generalized scheme is a [[structured (infinity,1)-topos]] such that ...

**References**

Generalized schemes are definition 2.3.9 of

* [[Jacob Lurie]], [[Structured Spaces]]

The definition of affine $G$-schemes (absolute spectra) is in section 2.2.

#Generalized schemes of Durov#

N. Durov replaces the commutative rings by commutative [[algebraic monad]]s (aka generalized rings) in sets and defines spectra in that context, and glues them together. This way he defines what he calls __generalized schemes__: in a nutshell generalized schemes are schemes glued from affine spectra of generalized rings. The corresponding category of quasicoherent $\mathcal{O}$-modules is not abelian in general. 

#Other generalized schemes#

O. Gabber considers replacing rings by *almost rings*, this results in the theory of [[almost schemes]].

One should note that Grothendieck school has occasionally studied ringed sites where ring is not required to be commutative and considered quasicoherent sheaves and cohomology in that context. D-schemes of Beilinson are an example where this formalism is useful. 

Rosenberg considers generalized relative schemes as categories over an arbitrary base category with a relatively affine cover satisfying some exactness conditions. The scheme as a category is in fact abstracting the category of quasicoherent sheaves over some generalized scheme. Rosenberg calls the Zariski version of that formalism [[noncommutative scheme]]; some other versions of locally affine spaces can be also relativized.

Rigid analytic geometry is featuring locally affinoid spaces (spectra of Banach algebras in a special class called affinoid algebras) in so-called G-topology. 