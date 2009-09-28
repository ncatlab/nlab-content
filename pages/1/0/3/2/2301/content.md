<div class="rightHandSide toc">
[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]
</div>

#Contents#

* automatic table of contents goes here
{:toc}


# Idea #

Recall that an ordinary [[scheme]] $X$ is a [[ringed space]] that is locally isomorphic to an [[affine scheme]]. 

Every scheme $X$ gives rise to a [[presheaf]] on the formal dual of commutative rings

$$
  X(-) : CRing \to Set
$$

$$
  A \mapsto Hom_{CRing}(Spec A, X)
$$

and that this is a [[sheaf]] with respect to various [[Grothendieck topology|Grothendieck topologies]] on $CRing^{op}$.

There are various way to (vastly) generalize this story to a theory of _generalized schemes_ .  

Already a general idea of [[Alexander Grothendieck]] was that to study a geometry more general than [[scheme]]s instead of the gluing of [[affine scheme]]s as [[ringed space]s, one glues the functors of points; hence **a [[space]] is simply a [[sheaf]] of sets on some [[site]] $Loc$ of local models with a [[Grothendieck topology]]** $\tau$ on it. 

If the local models are the usual [[affine scheme]]s, then for given choice of $\tau$ Grothendieck calls the outcome a $\tau$-locally affine space, rather than a scheme. The usual schemes are obtained for $\tau=Zariski$ and $Loc=Aff$. Algebraic spaces are another example. In general various generalizations which do not have exactness properties of Zariski or etale coverings, are usually among algebraic geometers called generalized _spaces_ rather than (generalized) _schemes_; thus the terminology almost scheme is OK because though the local objects are more general the exactness properties are basically the same (similarly for derived schemes of Toen et al. for locally affine spaces/stacks over model categories, noncommutative schemes of Rosenberg etc.). 

There are many generalizations of [[schemes]], some are even called by their respective authors generalized schemes (e.g. Lurie, Durov). Deligne in [[Catégories Tannakiennes]] suggested algebraic geometry in arbitrary symmetric monoidal category. 
Aspects of toric geometry and the foundations of the geometry over a field of one element (Smirnov-Kapranov, Dietmar, Connes...) can be founded using structure sheaves of monoids, not rings. Another example is tropical geometry. Rings are sometimes noncommutative (e.g. D-schemes of Beilinson); the underlying topological space can be replaced by a site, locale, topos or a non-distributive lattice by localizations. Usual commutative unital rings suffice for manifolds, rigid analytic spaces, schemes, formal schemes and so on. The emphasis in Lurie is to categorify the space and to take the homotopy version of a ring, restating a formalism fitting the [[derived algebraic geometry]], mainly of Simpson's school.  


Several different definitions by several authors exist.


# locally affine structured (∞,1)-toposes #

This is the definition in the context of 

* [[Jacob Lurie]], [[Structured Spaces]].

## Idea ##

The notion of [[structured (∞,1)-topos]] is in particular a [[vertical categorification|categorification]] of the notion of [[ringed space]]. In fact it is more general also in that it allows a choice of local model spaces: for $\mathcal{G}$ an [[(∞,1)-category]] of local models that is a [[geometry (for structured (∞,1)-toposes)]], a $\mathcal{G}$-[[structured (∞,1)-topos]] is a generalization of a space with a [[structure sheaf]] of functions that may take values in the objects of $\mathcal{G}$.

Therefore the ordinary statement "a scheme is a Zariski-locally affine space" may therefore be generalized 

+-- {: .standout}

A $\mathcal{G}$-scheme is a locally affine [[structured (∞,1)-topos]].

=--

## Definition in the variant of Lurie##

Let $\mathcal{G}$ be a [[geometry (for structured (∞,1)-toposes)]]. Write $\mathcal{G}_0$ for the underlying
discrete geometry. The identity functor

$$
  p : \mathcal{G} \to \mathcal{G}_0
$$

is then a morphism of geometries.

Recall the notation $LTop(\mathcal{G})$ for the [[(∞,1)-category]] of $\mathcal{G}$-[[structured (∞,1)-topos]]es and [[geometric morphism]]s between them.

### affine $\mathcal{G}$-schemes ###

+-- {: .un_theorem}
###### Theorem ( [[Structured Spaces|StSp]] 2.1.1 )

There is a pair of [[adjoint (∞,1)-functor]]s

$$
  p^* : LTop(\mathcal{G}) \stackrel{\leftarrow}{\to}
  LTop(\mathcal{G}_0)
  : 
  \mathbf{Spec}_{\mathcal{G}_0}^{\mathcal{G}}
$$

with $\mathbf{Spec}_{\mathcal{G}_0}^{\mathcal{G}}$
 left adjoint to the canonical functor $p^*$ given by precomposition with $p$.

=--

+-- {: .un_remark}
###### Remark ( [[StructuredSpaces|StSp]] p. 38 )

There is a canonical morphism

$$
  can :
  Pro(\mathcal{G})^{op}
  \to
  LTop(\mathcal{G}_0)
$$

=--


+-- {: .un_defn}
###### Definition ( affine $\mathcal{G}$-scheme, [[Structured Spaces|StSp]] 2.3.9)

Write $\mathbf{Spec}^{\mathcal{G}}$ for the [[(∞,1)-functor]]

$$
  \mathbf{Spec}^{\mathcal{G}} :
  Pro(\mathcal{G})^{op}
  \stackrel{can}{\to}
  LTop(\mathcal{G}_0)
  \stackrel{
    \mathbf{Spec}_{\mathcal{G}_0}^{\mathcal{G}}
  }{\to}
  LTop(\mathcal{G})
  \,.
$$

A $\mathcal{G}$-[[structured (∞,1)-topos]] in the image of this functor is an **affine $\mathcal{G}$-scheme**.

=--

### $\mathcal{G}$-schemes ###

+-- {: .un_defn}
###### Definition (geometric scheme, [[Structured Spaces|StSp]] 2.3.9)

Let $\mathcal{G}$ be a [[geometry (for structured (∞,1)-toposes)]].

A $\mathcal{G}$-[[structured (∞,1)-topos]] $(\mathcal{X},\mathcal{O}_{\mathcal{X}})$ is a **$\mathcal{G}$-scheme** if 

* there exists a collection $\{U_i \in \mathcal{X}\}$ 

such that

* the $\{U_i\}$ cover $\mathcal{X}$ in that the canonical morphism $\coprod_i U_i \to {*}$ (with ${*}$ the [[terminal object]] of $\mathcal{X}$) is an [[effective epimorphism]];

* for every $U_i$ there exists an equivalence

  $$
   (\mathcal{X}/{U_i}, \mathcal{O}_{\mathcal{X}}|_{U_i})
   \simeq \mathbf{Spec}^{\mathcal{G}} A_i
  $$

  of structured $(\infty,1)$-toposes for some $A_i \in Proj(\mathcal{G})$ (in the [[(∞,1)-category]] of [[pro-object]]s of $\mathcal{G}$).

=--

+-- {: .un_defn}
###### Definition (pregeometric scheme, [[Structured Spaces|StSp]], 3.4.6)


For $\mathcal{T}$ a pregeometry, a $\mathcal{T}$-[[structured (infinity,1)-topos]]
$(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is a **$\mathcal{T}$-scheme** if 
it is a $\mathcal{G}$-scheme for [[generalized the|the]] geometric envelope
$\mathcal{G}$ of $\mathcal{T}$.

This means that
for $f : \mathcal{T} \to \mathcal{G}$ [[generalized the|the]]  geometric envelope and
for $\mathcal{O}'_{\mathcal{X}}$
[[generalized the|the]] $\mathcal{G}$-structure on $\mathcal{X}$ such that
$\mathcal{O}_{\mathcal{X}} \simeq \mathcal{O}'_{\mathcal{X}} \circ f$, we have
that $(\mathcal{X}, \mathcal{O}'_{\mathcal{X}})$ is a $\mathcal{G}$-scheme.

=--


### smooth $\mathcal{G}$-schemes ###

Let $\Tau$ be a [[pregeometry (for structured (∞,1)-toposes)]] and let $\Tau \hookrightarrow \mathcal{G}$ be an inclusion into an enveloping [[geometry (for structured (∞,1)-toposes)]].

We think of the objects of $\Tau$ as the _smooth_ test spaces -- for instance the [[cartesian product]]s of some affine line $R$ with itsef -- and of the objects of $\mathcal{G}$ as affine test spaces that may have singular points where they are not smooth.

The idea is that a _smooth_ $\mathcal{G}$-scheme is a $\mathcal{G}$-structured space that is locally not only equivalent to objects in $\mathcal{G}$, but even to the very nice -- "smooth" -- objects in $\mathcal{Tau}$.

+-- {: .un_defn}
###### Definition ( smooth $\mathcal{G}$-scheme, [[Structured Spaces|StSp]] 3.5.6)

With an envelope $\Tau \hookrightarrow \mathcal{G}$ fixed, a $\mathcal{G}$-scheme is called **smooth** if there the affine schemes $\mathbf{Spec}^{\mathcal{G}} A_i$ appearing in its definition may be chosen with $A_i$ in the image of the includion $\tau \hookrightarrow \mathcal{G}$.

=--



### Examples ###

#### ordinary schemes ####

See the discussion at [[derived scheme]] for how ordinary [[scheme]]s are special cases of [[generalized scheme]]s.

#### ordinary Deligne-Mumford stacks ####

See the discussion at [[derived Deligne-Mumford stack]] for how ordinary [[Deligne-Mumford stack]]s are special cases of [[derived Deligne-Mumford stack]]s.

#### derived schemes ####

+-- {: .un_defn}
###### Definition (derived scheme, [[Structured Spaces]], 4.2.8)

Let $k$ be a commutative ring. Recall the pregoemtry $\mathcal{T}_{Zar}(k)$.

A **[[derived scheme]]** over $k$ is a $\mathcal{T}_{Zar}(k)$-scheme.

=--

#### derived Deligne-Mumford stacks ####

+-- {: .un_defn}
###### Definition (derived Deligne-Mumford stack, [[Structured Spaces]], 4.3.19)


Let $k$ be a commutative ring. Recall the pregeometry $\mathcal{T}_{et}(k)$

A **[[derived Deligne-Mumford stack]]** over $k$ is a $\mathcal{T}_{et}(k)$-scheme.

=--


#### derived smooth manifolds ####

...A $\mathcal{T}_{diff}$-scheme...

See

* [[derived smooth manifold]].

### References ###

The theory of $\mathcal{G}$-schenmes is due to [[Jacob Lurie]].

Generalized schemes are definition 2.3.9 of

* [[Jacob Lurie]], [[Structured Spaces]]

The definition of affine $\mathcal{G}$-schemes (absolute spectra) is in section 2.2.

# Generalized schemes of Durov #

N. Durov replaces the commutative rings by commutative [[algebraic monad]]s (aka generalized rings) in sets and defines spectra in that context, and glues them together. This way he defines what he calls __generalized schemes__: in a nutshell generalized schemes are schemes glued from affine spectra of generalized rings. The corresponding category of quasicoherent $\mathcal{O}$-modules is not abelian in general. 

# Other generalized schemes #

O. Gabber considers replacing rings by *almost rings*, this results in the theory of [[almost schemes]].

One should note that Grothendieck school has occasionally studied ringed sites where ring is not required to be commutative and considered quasicoherent sheaves and cohomology in that context. D-schemes of Beilinson are an example where this formalism is useful. 

Rosenberg considers generalized relative schemes as categories over an arbitrary base category with a relatively affine cover satisfying some exactness conditions. The scheme as a category is in fact abstracting the category of quasicoherent sheaves over some generalized scheme. Rosenberg calls the Zariski version of that formalism [[noncommutative scheme]]; some other versions of locally affine spaces can be also relativized.

Rigid analytic geometry is featuring locally affinoid spaces (spectra of Banach algebras in a special class called affinoid algebras) in so-called G-topology. 

[[!redirects generalized schemes]]