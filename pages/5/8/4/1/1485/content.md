
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A _manifold_ is a [[topological space]] which looks locally like a [[Cartesian space]], commonly a finite-dimensional Cartesian space $\mathbb{R}^n$ but possibly an infinite-dimensional [[topological vector space]]-

What "locally looks like" means depends on what sort of structure we are considering a Cartesian space to embody. At one extreme, we can think of $\mathbb{R}^n$ as merely a [[topological space]]. Or, $\mathbb{R}^n$ may be considered as carrying more rigid types of structure, such as $C^k$-[[differential structure]], [[smooth structure]], piecewise-linear (PL) structure, real [[analytic function|analytic structure]], affine structure, hyperbolic structure, foliated structure, etc., etc. Accordingly we have notions of [[topological manifold]], [[differential manifold]], [[smooth manifold]], etc. By default these are modeled on finite [[dimension]]al spaces, but most notions have generalizations to a corresponding notion of [[infinite dimensional manifold]].

In any case, the type of geometry embodied in a particular flavor of manifold is controlled by a particular [[groupoid]] of transformations which preserves whatever geometric features one is interested in; cf. Felix Klein's _[[Erlangen program|Erlanger Programm]]_.


## Definitions

To give a reasonably general notion of manifold, we first specify the kinds of concrete geometric groupoids which come into play.

### Pseudogroups

+-- {: .num_defn #Pseudogroup}
###### Definition

A **[[pseudogroup]]** on a [[topological space]] (or [[locale]]) $X$ is a [[groupoid]] $G$ each of whose [[objects]] is an [[open subset]] of $X$, and whose [[morphisms]] are [[homeomorphisms]] between such open sets, satisfying the following conditions:

* The objects [[cover]] $X$. (Equivalently, in light of the last axiom, every open set of $X$ is an object of $G$.)
* If $g: V \to W$ belongs to $G$ and $U \subseteq V$ is an open set, then the restriction $g|_U: U \to g(U)$ belongs to $G$. (Equivalently, in light of the other axioms, every inclusion map $id|_U: U \to V$ belongs to $G$.)
* ([[sheaf]] property) If $g: U \to V$ is a homeomorphism and if there is a covering $U_\alpha$ of $U$ such that the restrictions $g|_{U_\alpha}: U_\alpha \to g(U_\alpha)$ are morphisms of $G$, then $g$ is also morphism of $G$.

=--

+-- {: .num_example}
###### Example

Commonly used choices for $X$ in def. \ref{Pseudogroup} include 

* the [[Cartesian space]] $\mathbb{R}^n$ (for real manifolds)

* the [[complex plane]] $\mathbb{C}^n$ (for [[complex manifolds]])

* the half-space $H^n = \{(x_1, \ldots, x_n) \in \mathbb{R}^n: x_1 \geq 0\}$ (for [[manifolds with boundary]])

* the $n$-[[cube]] $I^n = [0, 1]^n$. 

=--

For the sake of concreteness, the reader may as well focus on the case $X = \mathbb{R}^n$.

### Charts

Let $G$ be a [[pseudogroup]] on $X$. 

+-- {: .num_defn #Chart}
###### Definition

A $G$-**[[chart]]** on a [[topological space]] $M$ is an [[open subset]] $U$ of $M$ together with an open embedding
$$
  \phi: U \to X\,.
$$

Two charts $\phi: U \to X$ and $\psi: V \to X$ are **compatible** if
$$\psi \circ \phi^{-1}: \phi(U \cap V) \to \psi(U \cap V)$$
belongs to $G$. 

=--

+-- {: .num_defn #Atlas}
###### Definition

A $G$-**atlas** on a [[topological space]] $M$ is a family of compatible charts $(\phi_\alpha: U_\alpha \to X)_\alpha$, def. \ref{Chart}, such that $(U_\alpha)_\alpha)_\alpha$ covers $M$.  The (restricted) maps $\phi_{\alpha \beta} = \phi_\beta \circ \phi_{\alpha}^{-1}$ are called **transition functions** between the charts of the atlas.

=--

### Manifolds

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

In the typical cases mentioned above for $X$, this will mean that $M$ is [[metric space|metrizable]]. In many studies, for example in 
[[cobordism theory]], one goes even further and assumes the manifolds are [[compact space|compact]].

=--

+-- {: .num_remark}
###### Remark

An atlas is _not_ considered an essential part of the structure of a manifold: two different atlases may yield the same manifold structure. This is encoded by the following definition \ref{IsomorphismOfManifolds} of [[isomorphisms]] between manifolds.

=--


### Isomorphism of manifolds

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


### Morphisms of Manifolds

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
hold. The object $Ext(r)$ may be called the _extension_ of $r$. This splitting is a kind of comprehension principle familiar from the theory of [[allegory|allegories]], among other things.

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


## Examples

If the term "manifold" appears without further qualification, what is usually meant is a **smooth $n$-manifold** of some [[natural number]] **dimension** $n$: a $G$-manifold where $G$ is the pseudogroup of invertible $C^{\infty}$ maps between open sets of $\mathbb{R}^n$. Replacing $\mathbb{R}^n$ here by a half-space $\{x \in \mathbb{R}^n: x_1 \geq 0\}$, one obtains the notion of smooth **manifold with boundary**. Or, replacing $\mathbb{R}^n$ here by the $n$-cube $I^n$, one obtains the notion of (smooth) $n$-**manifold with (cubical) corners**.  Morphisms of manifolds are here called **smooth maps**, and isomorphisms are called **diffeomorphisms**.  (In manifold theory, one usually reserves the term **smooth function** for smooth maps to $\mathbb{R}$.)

A **topological $n$-manifold** is a manifold with respect to the pseudogroup of homeomorphisms between open sets of $\mathbb{R}^n$. Any continuous function between topological manifolds is a morphisms, and any homeomorphism is an isomorphism. A **piecewise-linear (PL) $n$-manifold** is where the pseudogroup consists of piecewise-linear homeomorphisms between such open sets; morphisms are called **piecewise-linear (PL) maps**.

One can go on to define, in a straighforward way, real [[analytic manifolds]], complex analytic manifolds, elliptic manifolds, hyperbolic manifolds, and so on, using the general notion of pseudogroup.

Any space $X$ can always be turned into a manifold modelled on itself, using any pseudogroup $G$.  Simply take the inclusions of open sets as charts.

## Patching as Idempotent Splitting

In an exercise of his 1973 Perugia lectures [[F. William Lawvere]] reported a somewhat surprising observation: In the case of [[smooth manifolds]] the process of piecing together the local data can be elegantly summed up as [[Karoubi envelope|splitting of idempotents]] in a category of open subsets of Euclidian spaces. More precisely:

Let $Man$ be the category of [[smooth manifolds]] and [[smooth maps]], where by a "smooth manifold", we mean a finite-dimensional, second-countable, Hausdorff, $C^\infty$ [[manifold]] without boundary.  Let $i: Open \hookrightarrow Man$ be the [[full subcategory]] whose objects are the [[open subspaces]] of finite-dimensional [[Cartesian spaces]]. 

+-- {: .num_theorem} 
###### Theorem 
The subcategory $i: Open \hookrightarrow Man$ exhibits $Man$ as an idempotent-splitting completion of $Open$. 
=-- 

+-- {: .proof} 
###### Proof 
By a general [[Karoubi envelope#def2|lemma]] for idempotent splittings, it suffices to prove that 

* Every smooth manifold is a smooth retract of an open set in Euclidean space; 

* If $p : U \to U$ is a smooth idempotent on an open set $U \subseteq \mathbb{R}^n$, then the subset $Fix(p) \hookrightarrow U$ is an embedded submanifold. 

For the first statement, we use the fact that any manifold $M$ can be realized as a closed submanifold of some $\mathbb{R}^n$, and every closed submanifold has a [[tubular neighborhood theorem|tubular neighborhood]] $U \subseteq \mathbb{R}^n$. In this case $U$ carries a structure of vector bundle over $M$ in such a way that the inclusion $M \hookrightarrow U$ is identified with the zero section, so that the bundle projection $U \to M$ provides a retraction, with right inverse given by the zero section. 

For the second statement, assume that the origin $0$ is a fixed point of $p$, and let $T_0(U) \cong \mathbb{R}^n$ be its tangent space (observe the presence of a _canonical_ isomorphism to $\mathbb{R}^n$). Thus we have idempotent linear maps $d p(0), Id-d p(0): T_0(U) \to T_0(U)$ where the latter factors through the inclusion $\ker \; d p(0) \hookrightarrow T_0(U)$ via a projection map $\pi: T_0(U) \to \ker \; d p(0)$. We have a map $f: U \to \mathbb{R}^n$ that takes $x \in U$ to $x - p(x)$; let $g$ denote the composite 

$$U \stackrel{f}{\to} \mathbb{R}^n \cong T_0(U) \stackrel{\pi}{\to} \ker\; d p(0).$$ 

Now we make some easy observations: 

1. $Fix(p) \subseteq g^{-1}(0)$. 

1. The map $p: U \to U$ restricts to a map $p: g^{-1}(0) \to g^{-1}(0)$, by idempotence of $p$. 

1. The derivative $d g(0): T_0(U) \to T_0(\ker \; d p(0)) \cong \ker \; d p(0)$ is $\pi$ again since $Id - d p(0)$ is idempotent. Thus $d g(0)$ has full rank ($m$ say), and so the restriction of $g$ to some neighborhood $V$ has $0$ as a regular value, and $g^{-1}(0) \cap V$ is a manifold of dimension $m$ by the [[implicit function theorem]]. The tangent space $T_0(g^{-1}(0) \cap V)$ is canonically identified with $im(d p(0))$. 


1. There are smaller neighborhoods $V'' \subseteq V' \subseteq V$ so that $p$ restricts to maps $p_1, p_2$ as in the following diagram ($i, i', i''$ are inclusion maps, all taking a domain element $x$ to itself): 
$$\array{
g^{-1}(0) \cap V'' & \stackrel{i''}{\hookrightarrow} & g^{-1}(0) \\ 
 _\mathllap{p_2} \downarrow & & \downarrow _\mathrlap{p} \\ 
g^{-1}(0) \cap V' & \stackrel{i'}{\hookrightarrow} & g^{-1}(0) \\ 
 _\mathllap{p_1} \downarrow & & \downarrow _\mathrlap{p} \\ 
g^{-1}(0) \cap V & \stackrel{i}{\hookrightarrow} & g^{-1}(0)
}$$ 
and such that $p_1, p_2$ are diffeomorphisms by the [[implicit function theorem|inverse function theorem]] (noting here that $d p_i(0): im(d p(0)) \to im(d p(0))$ is the identity map, by idempotence of $p$). 

1. Letting $q: g^{-1}(0) \cap V' \to g^{-1}(0) \cap V''$ denote the smooth inverse to $p_2$, we calculate $i' = p \circ i'' \circ q$, and 
$$i p_1 = p i' = p p i''q = p i'' q = i',$$ 
so that $p_1(x) = x$ for every $x \in g^{-1}(0) \cap V'$. Hence $g^{-1}(0) \cap V' \subseteq Fix(p)$. 

From all this it follows that $Fix(p) \cap V' = g^{-1}(0) \cap V'$, meaning $Fix(p)$ is locally diffeomorphic to $\mathbb{R}^m$, and so $Fix(p)$ is an embedded submanifold of $\mathbb{R}^n$. 
=--

### Remark 
[[F. William Lawvere|Lawvere]] comments on this fact as follows:
 
>"This powerful theorem justifies bypassing the complicated considerations of charts, coordinate transformations, and atlases commonly offered as a "basic" definition of the concept of manifold. For example the 2-sphere, a manifold but not an open set of any Euclidean space, may be fully specified with its smooth structure by considering any open set $A$ in 3-space $E$ which contains it but not its center (taken to be $0$) and the smooth idempotent endomap of $A$ given by $e(x) = x/{|x|}$. All general constructions (i.e., functors into categories which are Cauchy complete) on manifolds now follow easily (without any need to check whether they are compatible with coverings, etc.) provided they are known on the opens of Euclidean spaces: for example, the tangent bundle on the sphere is obtained by splitting the idempotent $e'$ on the tangent bundle $A \times V$ of $A$ ($V$ being the vector space of translations of $E$) which is obtained by differentiating $e$. The same for cohomology groups, etc."  ([Lawvere 1989](#Law89), p.267)


## The Tangent Bundle

Many species of manifolds ([[Riemannian manifold]], [[pseudo-Riemannian manifold]], [[symplectic manifold]], and so on) involve extra structures defined on the _[[tangent bundle]]_ of a [[smooth manifold]]. This is perhaps the most fundamental construction in manifold theory.

If $M$ is a smooth $n$-manifold defined by an atlas $(U_\alpha, \phi_\alpha)$, then we may define its tangent bundle $T M$ by a gluing construction in $Top$, taking $T M$ to be the quotient of the disjoint sum

$$\sum_\alpha U_\alpha \times \mathbb{R}^n$$

obtained by dividing by the equivalence relation

$$(p \in U_\alpha, v) \sim (p \in U_\beta, g_{\alpha\beta}(p) v)$$

where $p \in U_\alpha \cap U_\beta$, and $g_{\alpha\beta}(p) \in GL(\mathbb{R}^n)$ is the result of differentiating the transition function $\phi_{\alpha\beta}$ at the point $\phi_\alpha(p)$. We thus obtain a covering $U_\alpha \times \mathbb{R}^n$ of $T M$, and these form coordinate charts of a smooth manifold structure on $T M$ in a more or less evident way. There is an obvious projection map $\pi: T M \to M$, called the _tangent bundle_; the fiber $\pi^{-1}(p)$ over a point $p \in M$ is called the _tangent space_ at $p$, denoted $T_p M$. Elements $v \in T_p M$ are called _tangent vectors_ at $p$.

* It is not immediately apparent that this construction yields the same manifold (in the sense described earlier) independent of the atlas chosen. To make this manifest, it is preferable to deal with coordinate-free expressions, defining for example tangent vectors with reference to the sheaf of smooth functions on $M$. We discuss this below.

The functions

$$g_{\alpha \beta}: U_\alpha \cap U_\beta \to GL(\mathbb{R}^n)$$

satisfy &#268;ech 1-cocycle relations

$$g_{\alpha \gamma} = g_{\beta\gamma} \circ g_{\alpha\beta}: U_{\alpha} \cap U_\beta \cap U_\gamma \to GL(\mathbb{R}^n)$$

$$\qquad g_{\alpha\alpha} = 1: U_{\alpha} \to GL(\mathbb{R}^n)$$

These 1-cocycle data make the tangent bundle an $n$-dimensional [[vector bundle]] with structure group $GL(\mathbb{R}^n)$.


## Generalizations

* [[generalized smooth space]]

* [[differentiable stack]]

* [[derived smooth manifold]]

* [[supermanifold]]

  * [[Euclidean supermanifold]] (notice that the definition of that is very much along the lines of the Klein-program-style definition above).

## Related concepts

* [[low-dimensional topology]]

* [[projective manifold]]

* [[manifold with boundary]]

* [[closed manifold]]

## References

* John Loftin, _The real definition of a smooth manifold_ ([pdf](http://andromeda.rutgers.edu/~loftin/difffal03/manifold.pdf))

The proof that idempotents split in the category of manifolds was adapted from this MO answer: 

* Zack (http://mathoverflow.net/users/300/zack), Idempotents split in category of smooth manifolds?, URL (version: 2014-04-06): http://mathoverflow.net/q/162556 ([web](http://mathoverflow.net/a/162556/2926)) 

Which provides a solution to exercise 3.21 in

* F. W. Lawvere, _Perugia Notes - Theory of Categories over a Base Topos_ , Ms. Universit&#224; di Perugia 1973.

The above comment by Lawvere is taken from 

* [[F. William Lawvere]], _Qualitative distinctions between some toposes of generalized graphs_, Contemporary Mathematics 92 (1989), 261-299. ([pdf](http://conceptualmathematics.files.wordpress.com/2013/01/toposesofgeneralizedgraphs.pdf)) 
 {#Law89} 


[[!redirects manifold]]
[[!redirects manifolds]]