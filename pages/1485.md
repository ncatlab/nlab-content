+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ChartsOfAManifold.png" width="500"> 
</div>

A _manifold_ is a [[topological space]] which looks locally like a [[Cartesian space]], commonly a finite-dimensional Cartesian space $\mathbb{R}^n$, in which case one speaks of a _manifold of [[dimension]] $n$_ or _$n$-fold_, but possibly an infinite-dimensional [[topological vector space]], in which case one has an [[infinite-dimensional manifold]].

What "locally looks like" means depends on what sort of structure we are considering a Cartesian space to embody. At one extreme, we can think of $\mathbb{R}^n$ as merely a [[topological space]]. Or, $\mathbb{R}^n$ may be considered as carrying more rigid types of structure, such as $C^k$-[[differential structure]], [[smooth structure]], [[PL structure|piecewise-linear (PL) structure]], real [[analytic function|analytic structure]], affine structure, hyperbolic structure, foliated structure, etc., etc. Accordingly we have notions of _[[topological manifold]]_, _[[differentiable manifold]]_, _[[smooth manifold]]_, _[[analytic manifold]]_ etc. By default these are modeled on [[finite number|finite]] [[dimension|dimensional]] spaces, but most notions have generalizations to a corresponding notion of [[infinite dimensional manifold]].

> graphics grabbed from [[The Geometry of Physics - An Introduction|Frankel]]


In any case, the type of geometry embodied in a particular flavor of manifold is controlled by a particular [[groupoid]] or, more generally, [[category]] of transformations which preserves whatever geometric features one is interested in; cf. Felix Klein's _[[Erlangen program|Erlanger Programm]]_.

## Definitions

Here we will focus on the general notion of a manifold. More concrete examples can be found in individual pages such as [[topological manifold]] and [[smooth manifold]].

We will present two possible definitions. The first, via [[pseudogroups]], has a simpler definition, but has two (rather serious) drawbacks:

1. There is in general no notion of morphisms between manifolds. At best, we can only talk about isomorphisms of manifolds.
1. We can only define smooth $n$-manifolds for each $n$ separately, but not smooth manifolds in general (and the same applies to complex manifolds etc.)

The second definition via cartologies was proposed by [[Todd Trimble]] to solve the above two problems.

### Definition via pseudogroups

The setting is a [[topological space]] $X$ together with a [[pseudogroup]] $G$ on $X$. For the sake of concreteness, the reader may as well focus on the case $X = \mathbb{R}^n$ and $G$ is the [[groupoid]] of [[diffeomorphisms]] between open subsets of $X$.

#### Definitions

+-- {: .num_defn #Chart}
###### Definition

A **[[chart]]** on a [[topological space]] $M$ is an [[open subset]] $U$ of $M$ together with an open embedding
$$
  \phi: U \to X\,.
$$

Two charts $\phi: U \to X$ and $\psi: V \to X$ are  $G$-**compatible** if
$$\psi \circ \phi^{-1}: \phi(U \cap V) \to \psi(U \cap V)$$
belongs to $G$. 
=--

+-- {: .num_defn #Atlas}
###### Definition

A $G$-**atlas** on a [[topological space]] $M$ is a family of  $G$-compatible charts $(\phi_\alpha: U_\alpha \to X)_\alpha$, def. \ref{Chart}, such that $(U_\alpha)_\alpha$ covers $M$.  The (restricted) maps $\phi_{\alpha \beta} = \phi_\beta \circ \phi_{\alpha}^{-1}$ are called **transition functions** between the charts of the atlas.

=--

+-- {: .num_defn}
###### Definition

A $G$-**manifold** is a [[topological space]] equipped with a $G$-atlas (definition \ref{Atlas}).

=--

+-- {: .num_remark}
###### Remark

This means that we can think of a $G$-manifold as a space which is _locally modeled_ on $X$ according to the geometry $G$.

=--

+-- {: .num_remark}
###### Remark

It is almost invariably the case in classical manifold theory that one requires some technical [[nice topological space|niceness]] properties on the [[topological space]] underlying a manifold.

Usually, in the definition of manifold it is understood that the underlying topological space

1. is a [[Hausdorff topological space]] (if not one usually speaks explicitly of a _[[non-Hausdorff manifold]]_)

1. is a [[paracompact topological space]];

Often it is also assumed that the topology has a countable [[basis of a topology|basis]] as well. 

In many of the typical cases, this will mean that $M$ is [[metric space|metrizable]]. In many studies, for example in 
[[cobordism theory]], one goes even further and assumes the manifolds are [[compact space|compact]].

=--

+-- {: .num_remark}
###### Remark

An atlas is _not_ considered an essential part of the structure of a manifold: two different atlases may yield the same manifold structure. This is encoded by the following definition \ref{IsomorphismOfManifolds} of [[isomorphisms]] between manifolds.

=--
#### Examples

If the term "manifold" appears without further qualification, what is usually meant is a **smooth $n$-manifold** of some [[natural number]] **dimension** $n$: a $G$-manifold where $G$ is the pseudogroup of invertible $C^{\infty}$ maps between open sets of $\mathbb{R}^n$. Replacing $\mathbb{R}^n$ here by a half-space $\{x \in \mathbb{R}^n: x_1 \geq 0\}$, one obtains the notion of smooth **manifold with boundary**. Or, replacing $\mathbb{R}^n$ here by the $n$-cube $I^n$, one obtains the notion of (smooth) $n$-**manifold with (cubical) corners**.  Morphisms of manifolds are here called **smooth maps**, and isomorphisms are called **diffeomorphisms**.  (In manifold theory, one usually reserves the term **smooth function** for smooth maps to $\mathbb{R}$.)

A **topological $n$-manifold** is a manifold with respect to the pseudogroup of homeomorphisms between open sets of $\mathbb{R}^n$. Any continuous function between topological manifolds is a morphisms, and any homeomorphism is an isomorphism. A **[[piecewise-linear manifold|piecewise-linear (PL) $n$-manifold]]** is where the pseudogroup consists of piecewise-linear homeomorphisms between such open sets; morphisms are called **piecewise-linear (PL) maps**.

One can go on to define, in a straighforward way, real [[analytic manifolds]], complex analytic manifolds, elliptic manifolds, hyperbolic manifolds, and so on, using the general notion of pseudogroup.

Any space $X$ can always be turned into a manifold modelled on itself, using any pseudogroup $G$. Simply take the inclusions of open sets as charts.

#### Isomorphisms of manifolds
+-- {: .num_defn #IsomorphismOfManifolds}
###### Definition

An **[[isomorphism]]** of $G$-manifolds $f: M \to N$ (defined by chosen atlas structures, def. \ref{Atlas}) is a [[homeomorphism]] $f$ such that

$$
  \phi(U \cap f^{-1}(V)) \overset{\phi^{-1}}{\to} U \cap f^{-1}(V) \overset{f}{\to} f(U) \cap V \overset{\psi}{\to} \psi(f(U) \cap V)
$$

is in $G$ whenever $(U, \phi)$ is a [[coordinate chart]], def. \ref{Chart} of $x \in M$, and $(V, \psi)$ is a coordinate chart of $f(x) \in N$. 

If $M_1$ and $M_2$ are two $G$-manifold structures on the same topological space $M$, then $M_1$ and $M_2$ are considered **equal** as $G$-manifolds if $id: M \to M$ is an isomorphism from $M_1$ to $M_2$ (and hence also from $M_2$ to $M_1$).

=--

Alternatively, atlases are ordered by inclusion, and two atlases define the same manifold structure on $M$ if they have a common upper bound. Equivalently, two atlases define the same manifold structure if each chart of one is compatible with each chart of the other. Or, one could extend any atlas to the (unique) maximal atlas containing it, which consists of all charts compatible with each of the charts in the original atlas, and simply identify a manifold structure with a maximal atlas.

+-- {: .query}

  _Rafael_: Can one define a manifold object in a category C as a G-manifold with G related to C? What would the relation between G and C be to obtain G-manifolds in C as manifold objects?

_Toby_:  Yes, I think that this would make perfect sense; I think that we\'d want $G$ to be an [[internal groupoid]] in $C$.  Note that defining things like 'smooth manifold' in $C$ might still be difficult, but we\'ve reduced it to internalising [[Cart Sp]] in $C$.  (There\'s also the matter that the above definition takes a notion of [[space]] for granted, so you\'d have to internalise that into $C$ too, but I\'m not sure how important that really is, when I think about how the topology on a smooth manifold can be recovered from the smooth structure.)

_Rafael_: Can someone that knows more than me about this add the result of this question to this article so nobody have to ask again.

_Toby_:  I\'d rather not, since it\'s all 'I think' and 'might be difficult'; it\'s better as a query box, moved to the bottom if necessary.  But if Todd agrees with me, then maybe he\'ll add it.
=--


### Definition via cartologies

+-- {: .query}
Note: the following is tentative "original research". It is prompted by the desire to extend the pseudogroup approach for defining general notions of manifold, so as to cover also an appropriate general notion of "map". Comments, improvements, and corrections are encouraged -- _Todd_.

I\'ve read through it once, and it makes sense.  I\'ll read through it again more carefully later.  ---Toby
=--

We begin by defining the [[2-poset]] (i.e., locally [[preorder]]ed [[bicategory]]) of **regions**, denoted $Reg$. The objects are topological spaces (or locales if you prefer); the morphisms are [[partial functions]] with open domain, that is spans
$$X \overset{i}{\leftarrow} U \overset{f}{\to} Y$$
where $f$ is continuous and $i$ is an open embedding. The spans are locally (that is, for fixed $X$ and $Y$) ordered by inclusion.

These local posets are not cocomplete, but they admit certain obvious [[joins]]: given a family of regional maps
$$(U_\alpha, f_\alpha): X \to Y$$
the join $\bigvee_\alpha (U_\alpha, f_\alpha)$ exists iff we have local compatibility:
$$f_{\alpha}|_{U_\alpha \cap U_\beta} = f_{\beta}|_{U_\alpha \cap U_\beta}$$
for all $\alpha, \beta$. Notice that composition on either side with a $1$-cell preserves any local joins which exist.

Every coreflexive morphism $r \leq 1_X$ in $Reg$ [[retract|splits]]: there is a map in $Reg$,
$$Ext(r) \overset{id}{\leftarrow} Ext(r) \overset{i}{\to} X,$$
whose opposite $i^op: X \to Ext(r)$ also belongs to $Reg$ (that is, $i$ is an open embedding), and the equations
$$i^{op} \circ i = 1_{Ext(r)} \qquad i \circ i^{op} = r$$
hold. The object $Ext(r)$ may be called the _extension_ of $r$. This splitting is a kind of [[comprehension principle]] familiar from the theory of [[allegory|allegories]], among other things.

A **cartology** is a (locally [[full subcategory|full]]) subbicategory $i: C \hookrightarrow Reg$ such that

* (Closure under open subspaces) If $X \in Ob(C)$ and $r \leq 1_X$ in $Reg$, then $i: Ext(r) \to X$ and its opposite $i^{op}$ are morphisms of $C$.
* ("Sheaf condition") The inclusion $i: C \to Reg$ reflects and preserves local joins.

Intended examples include the case where the objects of $C$ are Euclidean spaces $\mathbb{R}^n$, and morphisms are spans
$$(U, f): \mathbb{R}^m \to \mathbb{R}^n$$
where $f$ is smooth.

Given a cartology $C$, a morphism $r = (U, f): X \to Y$ in $C$ is **pseudo-invertible** if there exists $s = (V, g): Y \to X$ such that $s \circ r = 1_U$ and $r \circ s = 1_V$.

+-- {: .num_lemma}
###### Lemma

In a cartology, the pseudo-invertible morphisms from an object $X$ to itself form a pseudogroup (as defined earlier).
=--

The notion of a $C$-manifold modeled on an object $X$ of $C$ is defined just as before, using the pseudogroup on $X$ implied by the previous lemma. In particular, we have $C$-**charts** of an atlas structure on $M$, which are morphisms in $Reg$
$$X \overset{i}{\leftarrow} U \overset{\phi}{\to} M$$
satisfying the expected properties. We can thus speak of $C$-**manifolds** (or $(C, X)$-manifolds if we want to make explicit the modeling space $X$).

Now, given a cartology $C$, we define the category of $C$-manifolds. Let $M$ be a $(C, X)$-manifold and $N$ a $(C, Y)$-manifold. Then, a $C$-**morphism** from $M$ to $N$ is a continuous map $f: M \to N$ such that the $Reg$-composite
$$\array{
&& U &&&& M &&&& V && \\
& i \swarrow && \searrow \phi && 1 \swarrow && \searrow  f && \psi \swarrow && \searrow j & \\
X &&&& M &&&& N &&&& Y
}$$
belongs to $C$, for every pair of charts $(U, \phi): X \to M$ and $(V, \psi): Y \to N$.

These definitions need to be carefully checked against known examples (e.g., the categories $Top$, $PL$, and $Smooth$, among others).


## Generalizations

* [[generalized smooth space]]

* [[differentiable stack]]

* [[derived smooth manifold]]

* [[supermanifold]]

  * [[Euclidean supermanifold]] (notice that the definition of that is very much along the lines of the Klein-program-style definition above).

* [[semialgebraic manifold]]

## Related concepts

* [[dimension of a manifold]]

* [[low-dimensional topology]]

* [[projective manifold]]

* [[manifold with boundary]]

* [[closed manifold]]

* [[product manifold]]

## References

* John Loftin, _The real definition of a smooth manifold_ ([pdf](http://andromeda.rutgers.edu/~loftin/difffal03/manifold.pdf))


[[!redirects manifold]]
[[!redirects manifolds]]
[[!redirects manfold]]
