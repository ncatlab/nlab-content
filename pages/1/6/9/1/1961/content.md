#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The _tangent bundle_ $T X \to X$ of a [[space]] $X$ is a bundle whose fiber over a point $x \in X$ is a collection of [[infinitesimal space|infinitesimal]] curves emanating at $x$: the linear approximation of $X$ at $x$.

For nice enough [[space]]s such as [[manifold]] or more generally [[microlinear space]]s, the _tangent bundle_ $T X := T_*(X)$ of $X$ is a [[vector bundle]] over $X$.  

A _tangent vector_ on $X$ at $x \in X$ is an element of $T_x X$.  

The _tangent space_ of $X$ at a point $x$ is the [[fiber]] $T_x(X)$ of $T_*(X)$ over $x$;.  

A _tangent vector field_ on $X$ is a [[section]] of $T X$.

The precise definition of tangent bundle depends on the nature of the ambient category of [[space]]s. Below we give first the traditional definitions in ordinary [[differential geometry]]. Then we discuss the construction in more general context of [[smooth topos]]es in [[synthetic differential geometry]] and other categories of [[generalized smooth space]]s.

#Definitions in ordinary differential geometry#

Here we define the notion of tangent bundle in the [[category]] [[Diff]] of smooth [[manifold]]s

There are 3 standard definitions of tangent vector known as algebraic (derivation), geometric (equivalence class of germs of curves) and physical definition (via components in local coordinate system with prescribed behaviour under change of coordinates). 

## algebraic definition ##

Algebraically, we may define a __tangent vector__ $v$ at $a$ on $X$ as a [[scalar]]-valued [[derivation]] on the space of [[germ]]s of differentiable [[functions]] defined on $X$ near $a$, augmented by evaluation at $a$.  That is, given [[partial functions]] $f$ and $g$, each defined on some [[neighbourhood]] of $a$, we have:

1.  $v[f] = v[g]$ if $f = g$ on some (perhaps smaller) neighbourhood of $a$,
2.  $v[f + g] = v[f] + v[g]$,
3.  $v[c f] = c\, v[f]$ for $c$ a scalar,
4.  $v[f g] = f(a)\, v[g] + v[f]\, g(a)$;

In light of (4), (3) is equivalent to:

*  $v[k] = 0$ for $k$ a [[constant function]] (or indeed, for any function constant on any neighbourhood of $a$).

Globally, we may define a __tangent vector field__ $v$ as an ordinary (unaugmented) derivation on the space of differentiable functions defined on all of $X$.  (This works for differentiable manifolds and smooth manifolds, but not for [[analytic manifold]]s and [[algebraic manifold]]s; we need to be able to change functions locally.)  That is, given [[functions]] $f$ and $g$, we have:

1.  $v[f] = v[g]$ if $f = g$ (so really, the only reason to list this is to keep the numbering the same),
2.  $v[f + g] = v[f] + v[g]$,
3.  $v[c f] = c\, v[f]$ for $c$ a scalar,
4.  $v[f g] = f\, v[g] + v[f]\, g$;

In light of (4), (3) is again equivalent to:

*  $v[k] = 0$ for $k$ a [[constant function]].


Given a differentiable [[curve]] $c: \mathbf{R} \to X$, the __derivative__ $\dot{c}$ of $c$ is a curve in the tangent bundle; given an argument $t$ and a function $f$ defined near $c(t)$, the action is given by
$$ \dot{c}[f](t) = (f \circ c)'(t) ,$$
where $'$ indicates the usual derivative on the real line, so that $\dot{c}(t)$ is a tangent vector at $c(t)$.  (We really only need $c$ to be defined on a neighbourhood of $t$, of course.)

## geometric definition ##


One can also *define* vectors at $a$ to be curves $c$ such that $c(0) = a$, modulo the [[equivalence relation]] that $\dot{c}(0) = \dot{d}(0)$ if $c = d$ on some neighbourhood of $0$.  (Of course, $0$ could be replaced by any argument $t$ in this definition.)  A particularly important case is when $c$ is a level curve in some system of local coordinates $(x^1,\ldots,x^n)$ at $a$; that is, $c^i(t)$ is the point whose $i$th coordinate is $t$ and whose other coordinates are the same as at $a$.  The local tangent vector field given by these curves may be written $\partial/\partial{x^i}$ or $\partial_i$ (note the placement of the scripts).  This is because, if a function $f$ defined on that coordinate patch is identified with a function $f(x^1,\ldots,x^n)$ of $n$ real variables, then $\partial_i f$ becomes identified with the partial derivative $\partial{f(x^1,\ldots,x^n)}/\partial{x^i}$.  In general, a local vector field $v$ on such a coordinate patch can be written
$$ v = \sum_i v^i\, \partial_i .$$
This fact can also be turned into a definition of tanget vector.


(Yet another possible definition comes from the duality with the [[cotangent bundle]]; of course, then you have to pick a definition of *that* that doesn\'t use duality.)


Note that $\partial/\partial{f}$ doesn\'t make sense for an arbitrary function $f$; it only makes sense when $f$ is given as one component $x^i$ of a coordinate system.  That is, if $(f,g)$ and $(f,h)$ are both coordinate systems, then the two meanings of $\partial/\partial{f}$ need not be the same, because constant $g$ and constant $h$ aren\'t the same condition.  However, we can use the more complicated notation $(\partial/\partial{f})_g$ or $(\partial/\partial{f})_h$; this is common when $X$ is a [[phase space]] in [[thermodynamics]].  Of course, if a coordinate system is fixed by convention, then there is no ambiguity.

# Definition in synthetic differential geometry #

The above definitions in ordinary [[differential geometry]] suggest the slogan

+-- {: .standout}

Tangent vectors are infinitesimal curves in a space.

=--

One of the central motivations for [[synthetic differential geometry]] is the desire to provide a context in which this slogan becomes literally formally true.

+-- {: .un_defn}
###### Definition
**(tangent bundle in smooth toposes)**

Let $(\mathcal{T},(R,+,\cdot))$ be a [[smooth topos]] and write  $D = \{\epsilon \in R| \epsilon^2 = 0\}$ for the standard [[infinitesimal space|infinitesimal interval]]. For $X \in \mathcal{T}$ any object (any [[space]] in $\mathcal{T}$), the **tangent bundle** of $X$ is the morphism

$$
  p : T X \to X
$$

with

* $T X := X^D$ the [[internal hom]] of $D$ into $X$;

* $p = ev_0$ the evaluation map at the origin of $D$

  $ev_0 : (U \stackrel{v}{\to} X^D) \mapsto 
  (U \times {*} \stackrel{Id \times 0}{\to} U \times D
  \stackrel{\bar v}{\to} X)$,

  where $\bar v$ is the hom-[[adjunct]] of $v$.

=--

This definition captures elegantly and usefully the notion of tangent vectors as infinitesimal curves. But it is not guaranteed that the fibers of a synthetic tangent bundle $X^D$ are fiberwise linear, i.e. are fiberwise $R$-modules the way one expects. Objects $X$ for which this is true are [[microlinear space]]s in $\mathcal{T}$. See there for more details.

A [[smooth topos]] $\mathcal{T}$ is called a _well-adapted model_ for [[synthetic differential geometry]] if there is a [[full and faithful functor|full and faithful]] embedding [[Diff]] $\hookrightarrow \mathcal{T}$ of the cageory of [[manifold]]s into $\mathcal{T}$.

_Typically_ , for well adapted models_ under this embedding 

* manifolds are [[microlinear space]]s

* the synthetic definition of tangent bundle $X^D$ for $X$ a manifold does coincide with the ordinary notion of $T X$.

Let $\mathbb{L} = (C^\infty Ring^{fin})^{op}$ be the category of [[generalized smooth algebra|smooth loci]]. For $M$ a [[manifold]], the exponential $M^D$ does exist in $\mathbb{L}$ and is isomorphic to the ordinary tangent bundle $T X$ of $X$. (For instance  [[Models for Smooth Infinitesimal Analysis|MSIA, chapter II, prop 1.12]].

There are well-adapted [[smooth topos]]es $\mathcal{Z}$ and $\mathcal{B}$ presented as [[category of sheaves|categories of sheaves]] on $\mathbb{L}$: the first for the [[Grothendieck topology]] where covers are _finite_ open covers, the second where covers are finite open covers and projections ([[Models for Smooth Infinitesimal Analysis|MSIA, chapter VI]]). Both topologies are [[subcanonical coverage|subcanonical]], hence the [[Yoneda embedding]] $Y : \mathbb{L} \to Sh(\mathbb{L})$ does preserve the above property. 

Hence in these models for $X \in Diff$ a [[manifold]], $T X \in Diff$ its ordinary tangent bundle and $s : Diff \to Sh(\mathbb{L})$ the full and faithful embedding, we have isomorphisms

$$
  (s(X))^D  \simeq s(T X)
$$

which respect the bundle maps. 

# Definition for other generalized smooth spaces #

There are useful categories of [[generalized smooth space]]s which are neither categories of manifolds nor [[smooth topos]]es modeling [[synthetic differential geometry]]. But most of them admit useful notions of tangent bundles, too, sometimes more than one.

## tangent Fr&#246;licher spaces ##

See [[Frölicher space]] for the definition in that context.

## tangent diffeological spaces ##

* [[diffeological space]]

...


[[!redirects tangent vector]]
[[!redirects tangent space]]
[[!redirects tangent vector space]]
[[!redirects tangent vector field]]
[[!redirects tangent bundles]]
[[!redirects tangent vectors]]
[[!redirects tangent spaces]]
[[!redirects tangent vector spaces]]
[[!redirects tangent vector fields]]