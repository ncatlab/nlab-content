## Idea

A manifold is a space which looks locally like a Euclidean space, most commonly a finite-dimensional Euclidean space $\mathbb{R}^n$. 

What "locally looks like" means really depends on what sort of structure we are considering Euclidean space to embody. At one extreme, we can think of $\mathbb{R}^n$ as merely a topological space. Or, $\mathbb{R}^n$ may be considered as carrying more rigid types of structure ($C^k$, smooth, PL, real analytic, affine, hyperbolic, foliated, etc., etc.). In any case, the type of geometry embodied in a particular flavor of manifold is controlled by a particular [[groupoid]] of transformations which preserves whatever geometric features one is interested in; cf. Felix Klein's [[Erlangen Program|_Erlanger Programm_]]. 

## Definitions 

To give a reasonably general notion of manifold, we first specify the kinds of concrete geometric groupoids which come into play. 

A **pseudogroup** on a nonempty [[topological space]] $X$ is a [[groupoid]] each of whose objects is an open set of $X$, and whose morphisms are homeomorphisms between such open sets, satisfying the following conditions: 

* The objects [[cover]] $X$. 
* If $g: V \to W$ belongs to $G$ and $U \subseteq V$ is an open set, then the restriction $g|_U: U \to g(U)$ belongs to $G$. 
* (Covering property) If $g: U \to V$ is a homeomorphism and if there is a covering $U_\alpha$ of $U$ such that the restrictions $g|_{U_\alpha}: U_\alpha \to g(U_\alpha)$ are morphisms of $G$, then $g$ is also morphism of $G$. 

Commonly used choices for $X$ include $\mathbb{R}^n$ or $\mathbb{C}^n$, or the half-space 

$$H^n = \{(x_1, \ldots, x_n) \in \mathbb{R}^n: x_1 \geq 0\},$$ 

or the $n$-cube $I^n = [0, 1]^n$. For the sake of concreteness, the reader may as well focus on the case $X = \mathbb{R}^n$. 

Let $G$ be a pseudogroup on $X$. A $G$-**manifold** is a topological space $M$ equipped with a $G$-**atlas**, which is an open covering $U_\alpha$ of $M$ together with embeddings 

$$\phi_\alpha: U_\alpha \to X$$ 

with the property that for all $\alpha, \beta,$

$$\phi_\beta \circ \phi_{\alpha}^{-1}: \phi_\alpha(U_\alpha \cap U_\beta) \to \phi_\beta(U_\alpha \cap U_\beta)$$ 

belongs to $G$. The pairs $(U_\alpha, \phi_\alpha)$ are called **coordinate charts** of the atlas. The (restricted) maps $\phi_{\alpha \beta} = \phi_\beta \circ \phi_{\alpha}^{-1}$ are called **transition functions** between the coordinate charts. 

We can think of a $G$-manifold as a space which is _locally modeled_ on $X$ according to the geometry $G$. 

* It is almost invariably the case in classical manifold theory that one makes some technical [[nice topological space|niceness]] assumptions on the space $M$: viz. it is Hausdorff and paracompact; often one assumes it has a countable basis as well. In the typical cases mentioned above for $X$, this will mean that $M$ is [[metric space|metrizable]]. In many studies, for example in cobordism theory, one goes even further and assumes the manifolds are [[compact space|compact]]. 

An atlas is _not_ considered an essential part of the structure of a manifold: two different atlases may yield the same manifold structure. Here are the relevant definitions: 

An **isomorphism** of $G$-manifolds $f: M \to N$ (defined by chosen atlas structures) is a homeomorphism such that 

$$\phi(U \cap f^{-1}(V)) \overset{\phi^{-1}}{\to} U \cap f^{-1}(V) \overset{f}{\to} f(U) \cap V \overset{\psi}{\to} \psi(f(U) \cap V)$$ 

is a morphism of $G$ whenever $(U, \phi)$ is a coordinate chart of $x \in M$, and $(V, \psi)$ is a coordinate chart of $f(x) \in N$. If $M_1$ and $M_2$ are two $G$-manifold structures on the same topological space $M$, then $M_1$ and $M_2$ are considered the same as $G$-manifolds if $id: M \to M$ is an isomorphism from $M_1$ to $M_2$. 

* Alternatively, atlases are ordered by inclusion, and two atlases define the same manifold structure on $M$ if they have a common upper bound. Or, one could apply [[Zorn's lemma]] to prove the existence of a (unique) maximal atlas containing a given atlas, and simply identify a manifold structure with a maximal atlas. 

## Examples 

If the term "manifold" appears without further qualification, what is usually meant is a _smooth_ manifold of some dimension $n$, meaning a $G$-manifold where $G$ is the pseudogroup of invertible $C^{\infty}$ maps between open sets of $\mathbb{R}^n$. Replacing $\mathbb{R}^n$ here by a half-space $\{x \in \mathbb{R}^n: x_1 \geq 0\}$, one obtains the notion of smooth **manifold with boundary**. Or, replacing $\mathbb{R}^n$ here by the $n$-cube $I^n$, one obtains the notion of (smooth) $n$-**manifold with (cubical) corners**. 

A _topological_ $n$-manifold is a manifold with respect to the pseudogroup of homeomorphisms between open sets of $\mathbb{R}^n$. A _PL_ $n$-manifold is where the pseudogroup consists of piecewise-linear homeomorphisms between such open sets. 

One can go on to define, in a straighforward way, real analytic manifolds, complex analytic manifolds, elliptic manifolds, hyperbolic manifolds, and so on, using the general notion of pseudogroup. 

## Tangent Bundle

Many species of manifolds (Riemannian, Lorentzian, symplectic, and so on) involve extra structures defined on the _tangent bundle_ of a smooth manifold. This is perhaps the most fundamental construction of all in manifold theory. 

If $M$ is a smooth $n$-manifold defined by an atlas $(U_\alpha, \phi_\alpha)$, then we may define the tangent bundle by a gluing construction in $Top$, taking the quotient space $T M$ of the disjoint sum 

$$\sum_\alpha U_\alpha \times \mathbb{R}^n$$

modulo the equivalence relation generated by 

$$(p \in U_\alpha, v) \sim (p \in U_\beta, g_{\alpha\beta}(p) v)$$ 

where $p \in U_\alpha \cap U_\beta$, and $g_{\alpha\beta}(p)$ is the result of differentiating the transition function $\phi_{\alpha\beta}$ at the point $\phi_\alpha(p)$. We thus obtain a covering $U_\alpha \times \mathbb{R}^n$ of $T M$, and these form coordinate charts of a smooth manifold structure on $T M$ in a more or less evident way. 

To be continued (and cleaned up)...
