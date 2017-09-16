## Idea

A manifold is a space which looks locally like a Euclidean space, most commonly a finite-dimensional Euclidean space $\mathbb{R}^n$. 

What "locally looks like" means really depends on what sort of structure we are considering Euclidean space to embody. At one extreme, we can think of $\mathbb{R}^n$ as merely a topological space. Or, $\mathbb{R}^n$ may be considered as carrying more rigid types of structure ($C^k$, smooth, PL, real analytic, affine, hyperbolic, foliated, etc., etc.). In any case, the type of geometry embodied in a particular flavor of manifold is controlled by a particular [[groupoid]] of transformations which preserves whatever geometric features one is interested in; cf. Felix Klein's _[[Erlangen program|Erlanger Programm]]_. 

## Definitions 

To give a reasonably general notion of manifold, we first specify the kinds of concrete geometric groupoids which come into play. 

A **pseudogroup** on a [[topological space]] (or [[locale]]) $X$ is a [[groupoid]] $G$ each of whose objects is an open set of $X$, and whose morphisms are homeomorphisms between such open sets, satisfying the following conditions: 

* The objects [[cover]] $X$. (Equivalently, in light of the last axiom, every open set of $X$ is an object of $G$.)
* If $g: V \to W$ belongs to $G$ and $U \subseteq V$ is an open set, then the restriction $g|_U: U \to g(U)$ belongs to $G$. (Equivalently, in light of the other axioms, every inclusion map $id|_U: U \to V$ belongs to $G$.)
* ([[sheaf]] property) If $g: U \to V$ is a homeomorphism and if there is a covering $U_\alpha$ of $U$ such that the restrictions $g|_{U_\alpha}: U_\alpha \to g(U_\alpha)$ are morphisms of $G$, then $g$ is also morphism of $G$. 

Commonly used choices for $X$ include $\mathbb{R}^n$ or $\mathbb{C}^n$, the half-space 
$$H^n = \{(x_1, \ldots, x_n) \in \mathbb{R}^n: x_1 \geq 0\},$$ 
or the $n$-[[cube]] $I^n = [0, 1]^n$. For the sake of concreteness, the reader may as well focus on the case $X = \mathbb{R}^n$. 

Let $G$ be a pseudogroup on $X$. A $G$-**chart** on a topological space $M$ is an open subset $U$ of $M$ together with an embedding
$$\phi: U \to X.$$
Two charts $\phi: U \to X$ and $\psi: V \to X$ are **compatible** if
$$\psi \circ \phi^{-1}: \phi(U \cap V) \to \psi(U \cap V)$$ 
belongs to $G$. A $G$-**atlas** on $M$ is a family of compatible charts $(\phi_\alpha: U_\alpha \to X)_\alpha$ such that $(U_\alpha)_\alpha)_\alpha$ covers $M$.  The (restricted) maps $\phi_{\alpha \beta} = \phi_\beta \circ \phi_{\alpha}^{-1}$ are called **transition functions** between the charts of the atlas.

Finaly, a $G$-**manifold** is a topological space equipped with a $G$-atlas. 

We can think of a $G$-manifold as a space which is _locally modeled_ on $X$ according to the geometry $G$. 

* It is almost invariably the case in classical manifold theory that one makes some technical [[nice topological space|niceness]] assumptions on the space $M$: viz. it is [[Hausdorff space|Hausdorff]] and paracompact; often one assumes its topology has a countable basis as well. In the typical cases mentioned above for $X$, this will mean that $M$ is [[metric space|metrizable]]. In many studies, for example in cobordism theory, one goes even further and assumes the manifolds are [[compact space|compact]]. 

An atlas is _not_ considered an essential part of the structure of a manifold: two different atlases may yield the same manifold structure. Here are the relevant definitions: 

An **isomorphism** of $G$-manifolds $f: M \to N$ (defined by chosen atlas structures) is a homoeomorphism $f$ such that 
$$\phi(U \cap f^{-1}(V)) \overset{\phi^{-1}}{\to} U \cap f^{-1}(V) \overset{f}{\to} f(U) \cap V \overset{\psi}{\to} \psi(f(U) \cap V)$$ 
is in $G$ whenever $(U, \phi)$ is a coordinate chart of $x \in M$, and $(V, \psi)$ is a coordinate chart of $f(x) \in N$. If $M_1$ and $M_2$ are two $G$-manifold structures on the same topological space $M$, then $M_1$ and $M_2$ are considered **equal** as $G$-manifolds if $id: M \to M$ is an isomorphism from $M_1$ to $M_2$ (and hence also from $M_2$ to $M_1$). 

* Alternatively, atlases are ordered by inclusion, and two atlases define the same manifold structure on $M$ if they have a common upper bound. Equivalently, two atlases define the same manifold structure if each chart of one is compatible with each chart of the other. Or, one could extend any atlas to the (unique) maximal atlas containing it, which consists of all charts compatible with each of the charts in the original atlas, and simply identify a manifold structure with a maximal atlas. 

+--{.query}
_Todd_: I think I'd want to hold off on calling these morphisms (where one uses a general continuous $f: M \to N$), because it may give rise to later confusion when one settles down to define categories of manifolds (in the usual way, with manifolds of varying dimensions). For example, even between manifolds of the same dimension, we'd want constant maps as part of that category, but constant maps are (almost) never morphisms in the sense here. I just think we're asking for trouble here. 

[In fact, it seems to me that the pseudogroup approach may be a bit limiting: really we should be reformulating the definitions so that the pseudogroups (for varying $X$, like $X = \mathbb{R}^n$) are part of a larger category, e.g., the category of open maps in Euclidean space and smooth maps between them, so that it becomes easier to say what we mean by a map between manifolds of the same type (i.e., real, complex, PL, etc.). But I've not seen this actually carried out, and it looks like this would involve some original research which I haven't had time to, um, research yet.] 

_Toby_:  Ah yes, I forgot that the morphisms of $G$ are invertible; I was imagining that all smooth maps (between the relevant objects) were in $G$.  It seems like this *should* be doable, but I haven\'t seen it either.
=-- 

## Examples 

If the term "manifold" appears without further qualification, what is usually meant is a **smooth $n$-manifold** of some [[natural number]] **dimension** $n$: a $G$-manifold where $G$ is the pseudogroup of invertible $C^{\infty}$ maps between open sets of $\mathbb{R}^n$. Replacing $\mathbb{R}^n$ here by a half-space $\{x \in \mathbb{R}^n: x_1 \geq 0\}$, one obtains the notion of smooth **manifold with boundary**. Or, replacing $\mathbb{R}^n$ here by the $n$-cube $I^n$, one obtains the notion of (smooth) $n$-**manifold with (cubical) corners**.  Morphisms of manifolds are here called **smooth maps**, and isomorphisms are called **diffeomorphisms**.  (In manifold theory, one usually reserves the term **smooth function** for smooth maps to $\mathbb{R}$.)

A **topological $n$-manifold** is a manifold with respect to the pseudogroup of homeomorphisms between open sets of $\mathbb{R}^n$. Any continuous function between topological manifolds is a morphisms, and any homeomorphism is an isomorphism. A **piecewise-linear (PL) $n$-manifold** is where the pseudogroup consists of piecewise-linear homeomorphisms between such open sets; morphisms are called **piecewise-linear (PL) maps**.

One can go on to define, in a straighforward way, real analytic manifolds, complex analytic manifolds, elliptic manifolds, hyperbolic manifolds, and so on, using the general notion of pseudogroup. 

Any space $X$ can always be turned into a manifold modelled on itself, using any pseudogroup $G$.  Simply take the inclusions of open sets as charts.

## Tangent Bundle

Many species of manifolds (Riemannian, Lorentzian, symplectic, and so on) involve extra structures defined on the _tangent bundle_ of a smooth manifold. This is perhaps the most fundamental construction in manifold theory. 

If $M$ is a smooth $n$-manifold defined by an atlas $(U_\alpha, \phi_\alpha)$, then we may define its tangent bundle $T M$ by a gluing construction in $Top$, taking $T M$ to be the quotient of the disjoint sum 

$$\sum_\alpha U_\alpha \times \mathbb{R}^n$$

obtained by dividing by the equivalence relation 

$$(p \in U_\alpha, v) \sim (p \in U_\beta, g_{\alpha\beta}(p) v)$$ 

where $p \in U_\alpha \cap U_\beta$, and $g_{\alpha\beta}(p) \in GL(\mathbb{R}^n)$ is the result of differentiating the transition function $\phi_{\alpha\beta}$ at the point $\phi_\alpha(p)$. We thus obtain a covering $U_\alpha \times \mathbb{R}^n$ of $T M$, and these form coordinate charts of a smooth manifold structure on $T M$ in a more or less evident way. There is an obvious projection map $\pi: T M \to M$, called the _tangent bundle_; the fiber $\pi^{-1}(p)$ over a point $p \in M$ is called the _tangent space_ at $p$, denoted $T_p M$. Elements $v \in T_p M$ are called _tangent vectors_ at $p$. 

* It is not immediately apparent that this construction yields the same manifold (in the sense described earlier) independent of the atlas chosen. To make this manifest, it is preferable to deal with coordinate-free expressions, defining for example tangent vectors with reference to the sheaf of smooth functions on $M$. We discuss this below. 

The functions 

$$g_{\alpha \beta}: U_\alpha \cap U_\beta \to GL(\mathbb{R}^n)$$ 

satisfy Cech 1-cocycle relations 

$$g_{\alpha \gamma} = g_{\beta\gamma} \circ g_{\alpha\beta}: U_{\alpha} \cap U_\beta \cap U_\gamma \to GL(\mathbb{R}^n)$$ 

$$\qquad g_{\alpha\alpha} = 1: U_{\alpha} \to GL(\mathbb{R}^n)$$ 

These 1-cocycle data make the tangent bundle an $n$-dimensional [[vector bundle]] with structure group $GL(\mathbb{R}^n)$. 
