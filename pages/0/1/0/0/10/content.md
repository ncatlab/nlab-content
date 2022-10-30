
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 


The _classifying topos_ for a given type of mathematical [[structure]] $T$ --- for example the structures: "[[group]]", "[[torsor]]", "[[ring]]", "[[category]]"  etc. --- is a ([[Grothendieck topos|Grothendieck]]) [[topos]] $S[T]$ such that [[geometric morphisms]] $f: E \to S[T]$ are the same as structures of this sort in the topos $E$, i.e. groups [[internalization|internal to]] $E$, torsors internal to $E$, etc.  In other words, a classifying topos is a [[representing object]] for the functor which sends a topos $E$ to the category of structures of the desired sort in $E$.

In particular for $E$ a [[sheaf topos]] on a [[topological space]] $X$ and $G$ a (bare, i.e. discrete) [[group]], a $G$-torsor in $E$ is a $G$-[[principal bundle]] over $X$. There is a classifying topos denoted $B G$, such that the [[groupoid]] $G Bund(X)$ of $G$-[[principal bundle]]s over $X$ is equivalent to geometric morphims $Sh(X) \to B G$:

$$
  G Bund(X) \simeq Topos(Sh(X), B G)
  \,.
$$

This is evidently analogous to the notion of [[classifying space]] in [[topology]], which for the discrete group $G$ is a [[topological space]] $\mathcal{B} G$ such that

$$
  \pi_0 G Bund(X) \simeq \pi_0 Top(X, \mathcal{B}G)
  \,.
$$

Hence one can think of classifying topoi as a grand generalization of the notion of [[classifying space]] in topology.




## Definition

In a tautological way, every [[topos]] $F$ is the classifying topos for something, namely for the categories of [[geometric morphisms]] $E \to F$ into it. The concept of [[geometric theory]] allows one to usefully interpret these categories as _categories of certain structures in $E$_ :

as decribed in _[Geometric theories -- In terms of sheaf topoi](geometric+theory#InTermsOfSheafTopoi)_, every [[sheaf topos]] $F$ is a completion $S[T]$ of the [[syntactic category]] $C_T$ of _some_ [[geometric theory]] $T$

$$
  F \simeq S[T]  
  \,.
$$

And structures of type $T$ in $E$ is what geometric morphisms $E \to F$ classify.

So the **classifying [[topos]]** for the [[geometric theory]] $T$ is a [[Grothendieck topos]] $S[T]$ equipped with a "universal model $U$ of $T$".  This means that for any Grothendieck topos $E$ together with a model $X$ of $T$ in $E$, there exists a unique (up to isomorphism) [[geometric morphism]] $f: E \to S[T]$ such that $f^*$ maps the $T$-model $U$ to the model $X$.  More precisely, for any Grothendieck topos $E$, the category of $T$-models in $E$ is equivalent to the category of geometric morphisms $E \to S[T]$.

The fact that a classifying topos is like the ambient [[set theory]] but equipped with that universal model is essentially the notion of _[[forcing]]_ in [[logic]]: the passage to the [[internal logic]] of the classifying topos _forces_ the universal model to exist.

If $C_T$ is the [[syntactic category]] of $T$, so that $T$-models are the same as [[geometric category|geometric functors]] out of $C_T$, then this universal model can be identified with a certain geometric functor

$$
  U : C_T \to S[T]
  \,.
$$

Its universality property means that any geometric functor

$$
  X : C_T \to E
$$

factors essentially uniquely as

$$
  X : C_T \stackrel{U}{\to} S[T] \stackrel{f^*}{\to} E
$$

for $U$ the universal model and $f^*$ the [[left adjoint]] part of a [[geometric morphism]].  More precisely, composition with $U$ defines an equivalence between the category of geometric morphisms $E\to S[T]$ and the category of geometric functors $C_T\to E$.

More specifically, for any [[cartesian theory]], [[regular theory]] or [[coherent theory]] $\mathbb{T}$ (which in ascending order are special cases of each other and all of geometric theories), the corresponding [[syntactic category]] $\mathcal{C}_{\mathbb{T}}$ comes equipped with the structure of a [[syntactic site]] $(\mathcal{C},\mathbb{T}, J)$ (see there) and the classifying topos for $\mathbb{T}$ is the [[sheaf topos]] $Sh(\mathcal{C}_{\mathbb{T}}, J)$.

Classifying toposes can also be defined over any [[base topos]] $S$ instead of [[Set]].  In that case "Grothendieck topos" is replaced by "bounded $S$-topos."

If the classifying topos of a geometric theory $T$ is a [[presheaf topos]], one called $T$ a _[[theory of presheaf type]]_.

## Background on the theory of theories


The notion of _classifying topos_ is part of a trend, begun by [[Bill Lawvere|Lawvere]], of viewing a mathematical [[theory]] in [[logic]] as a [[category]] with suitable [[exact functor|exactness]] properties and which contains a "generic model", and a [[model]] of the theory as a functor which preserves those properties.  This is described in more detail at [[internal logic]] and [[type theory]], but here are some simple examples to give the flavor.  The original example is that of a 'finite products theory':

* **Finite products theory.**  Roughly speaking, a 'finite products theory', '[[Lawvere theory]]', or '[[algebraic theory]]' is a [[theory]] describing some mathematical structure that can be defined in an arbitrary category with finite [[product]]s.  An example would be the theory of [[groups]]. As explained in the entry for [[Lawvere theory]], for each such theory $T$ there is a category with finite products $C_{fp}[T]$ -- the [[syntactic category]], which serves as a "classifying category" for $T$, in that models of $T$ in the category of sets correspond to product-preserving [[functor]]s $f : C_{fp}[T] \to Set$.   More generally, for any category with finite products, say $E$, models of $T$ in $E$ correspond to product-preserving functors $f : C_{fp}[T] \to E$.   

* **Finite limits theory.** Next up the line is the notion of  'finite limits theory', sometimes called an [[essentially algebraic theory]].  This is roughly a theory describing some structure that can be defined in an arbitrary category with [[finite limit]]s (also called a [[finitely complete category]]).  An example of a finite limits theory would be the theory of categories.   (The notion of 'category' requires finite limits, while the notion of 'group' does not, because categories but not groups involve a _partially defined_ operation, namely composition of morphisms.)    Every finite limits theory $T$ admits a [[syntactic category|classifying category]] $C_{fl}(T)$: a finitely complete category such that models of $T$ in a category $E$ with finite limits correspond to functors $f: C_{fl}(T) \to E$ that preserve finite limits.  (Such functors are called [[left exact]], or 'lex' for short.)  

* **Geometric theory.** Further up the line, a [[geometric theory]] is roughly a theory which can be formulated in that fragment of first-order logic that deals in finite limits and arbitrary (small) colimits, plus certain [[familial regularity and exactness|exactness]] properties the details of which need not concern us.  The point is that a category with finite limits, small colimits, and appropriate exactness is just a Grothendieck topos, and a functor preserving finite limits and small colimits is just the inverse image part of a geometric morphism.  Just as in the previous two cases, any 'geometric theory' has a classifying category $S[T]$ (which is now a Grothendieck topos) which possesses a "generic object" for that theory, and T-models in any other Grothendieck topos E can be identified with geometric morphisms $f\colon E\to S[T]$, or specifically with their inverse image parts.

Each type of theory may be considered a $2$-theory, or [[doctrine]].  Furthermore, each type of theory can be promoted to a theory "further up the line", by [[completion|freely adding]] the missing structure to the classifying category.  This can always be done purely formally, but in a few cases this promotion also has other, more explicit descriptions.

For instance, to go from a finite products theory $T$ to the corresponding finite limits theory, we can take the opposite of the category of [[finitely presentable object|finitely presentable models]] of $T$ in $Set$, thanks to [[Gabriel-Ulmer duality]].  Similarly, to go from a finite limits theory to the classifying topos of the corresponding geometric theory, we can take the category of presheaves on the classifying category of the finite limits theory.

## Properties

### Geometric morphisms equivalent to morphisms of sites
 {#GeometricMorphismsAndMorphismsOfSites}

The fact that classifying toposes are what they all comes down,
if spelled out explicitly, to the fact that [[geometric morphism]]
$f : \mathcal{E} \to \mathcal{F}$ of toposes can be identified with certain
morphism of [[site]]s $C_{\mathcal{E}}$, $C_{\mathcal{F}}$  for these toposes, going the other way round, $C_\mathcal{E} \leftarrow C_{\mathcal{F}}$, and having certain properties. If here $C_\mathcal{F}$ is the [[syntactic site]] of some [[theory]] $\mathbb{T}$ and we choose $C_{\mathcal{E}}$ to be the [[canonical site]] of $\mathcal{E}$ (itself equipped with the [[canonical coverage]]) this makes manifest why the geometric morphisms in $\mathcal{F}$ correspond to [[model]]s of $\mathcal{T}$ in $\mathcal{E}$. 

We now say this in precise manner. In the following a _[[cartesian site]]_ means a [[site]] whose underlying category is [[finitely complete category|finitely complete]].

+-- {: .num_prop }
###### Proposition

Let $(\mathcal{C}, J)$ and $(\mathcal{D}, K)$ be [[cartesian site]]s such that $\mathcal{C}$ is a [[small category]], $\mathcal{D}$ is an [[essentially small category]] and the [[coverage]] $K$ is [[subcanonical coverage|subcanonical]]. 

Then a [[geometric morphism]] of the corresponding [[sheaf toposes]]

$$
  f : Sh(\mathcal{D}, K) \to Sh(\mathcal{C}, J)
$$

is induced by a [[morphism of sites]]

$$
  (\mathcal{D}, K) \leftarrow (\mathcal{C}, J)  
$$

precisely if the [[inverse image]] of $f$ respects the [[Yoneda embedding]]s $j$ as

$$
  \array{
    \mathcal{D } &\leftarrow& \mathcal{C}
    \\
    {}^{\mathllap{j_{\mathcal{D}}}}\downarrow && \downarrow^{\mathrlap{j_{\mathcal{C}}}}
    \\
    Sh(\mathcal{D}, K) &\stackrel{f^*}{\leftarrow}&
    Sh(\mathcal{C}, J)    
  }
  \,.
$$

=--

This appears as ([Johnstone, lemma C2.3.8](#Johnstone)).

+-- {: .proof}
###### Proof

It suffices to observe that the factorization, if it exists, is a morphism of sites.

=--

+-- {: .num_cor #SheafToposesAreClassifyingForTheirTheoryOfLocalAlgegras}
###### Corollary

Let $(\mathcal{C},J)$ be a [[small category|small]] [[cartesian site]] and let $\mathcal{E}$ be any [[sheaf topos]]. Then we have an [[equivalence of categories]]

$$
  Topos(\mathcal{E}, Sh(\mathcal{C}, J))
  \simeq
  Site((\mathcal{C}, J), (\mathcal{E}, C))
$$

between the [[geometric morphism]]s from $\mathcal{E}$ to $Sh(\mathcal{C}, J)$ and the morphisms of [[sites]] from $(\mathcal{C}, J)$ to the [[big site]] $(\mathcal{E}, C)$ for $C$ the [[canonical coverage]] on $\mathcal{E}$.

=--

This appears as ([Johnstone, cor. C2.3.9](#Johnstone)).

+-- {: .num_remark}
###### Remark

This means that a sheaf topos $Sh(\mathcal{C},J)$ is the classifying topos for the theory of [[local algebras]] determined by the [[site]] $(\mathcal{C},J)$.

=--



## Examples 

We list and discuss explicit examples of classifying toposes.

### For objects

The [[presheaf topos]] $[FinSet, Set]$ on the [[opposite category]] of [[FinSet]] is the classifying topos for the [[theory of objects]], sometimes called the "object classifier" This is not to be confused with the notion of an [[object classifier]] in an [[(∞,1)-topos]]  and maybe better called in full the _[[classifying topos for the theory of objects]]_.

For $E$ any [[topos]], a [[geometric morphism]] $E \to [FinSet,Set]$ is equivalently just an [[object]] of $E$.

Similarly, the presheaf topos $[FinSet_*, Set]$ (where $FinSet_*$ is the category of finite [[pointed sets]]) classifies pointed objects; cf. [this question](http://mathoverflow.net/questions/85600/what-do-gamma-sets-classify) and answer.  This is the topos of "$\Gamma$-sets"; see [[Gamma-space]].

### For groups

We discuss the [[finite product theory]] of [[group]]s. This theory has a classifying category $C_{fp}(Grp)$.  $C_{fp}(Grp)$ is a category with finite products equipped with an object $G$, the "[[walking]] group", a morphism $m: G \times G \to G$ describing multiplication, a morphism $inv : G \to G$ describing inverses, and a morphism $i: 1 \to G$ describing the identity element of $G$, obeying the usual group axioms.   For any category with finite products, say $E$, a finite-product-preserving functor $f: C_{fp}(Grp) \to E$ is the same as a [[group object]] in $E$.   For more details, see [[Lawvere theory]].

We can promote $C_{fp}(Grp)$ to a category with finite limits, $C_{fl}(Grp)$, by adjoining all finite limits.   As mentioned above, one way to do this is to take the category of models of $C_{fp}(Grp)$ in Set, which is simply $Grp$, and then take the full subcategory of [[finitely presentable object|finitely presentable]] groups.  By [[Gabriel-Ulmer duality]], the opposite of this is $C_{fl}(Grp)$.
For any category with finite products, say $E$, a left exact functor $f: C_{fp}(Grp) \to E$ is the same as a [[group object]] in $E$.

We can further promote $C_{fl}(Grp)$ to a [[Grothendieck topos]] by taking the category of [[presheaves]].  This gives the classifying topos for groups:
$$       S[Grp] = Set^{C_{fl}(Grp)^{op}}  \, . \]
For any Grothendieck topos, say $E$, a left exact left adjoint functor $ f^*: S[T] \to E $ is the same as a [[group object]] in $E$.

### For rings

The discussion above for groups can be repeated verbatim for rings, since they too are described by a finite products theory.








### For (inhabited) linear orders
 {#ForLinearOrders}

+-- {: .num_prop }
###### Proposition

The category of [[cosimplicial sets]] $[\Delta, Set]$ -- hence the [[presheaf topos]] over the [[opposite category]] $\Delta^{op}$ of the [[simplex category]] --  is the classifying topos for [[inhabited set|inhabited]] [[linear orders]].

=--

This appears as ([Moerdijk, prop. 5.4](#Moerdijk)).

+-- {: .proof}
###### Proof

For ease of notation we discuss this in [[Set]], hence we show that [[geometric morphisms]] $Set \to PSh(\Delta^{op})$ are equivalently [[linear orders]]. Or, by [[Diaconescu's theorem]], that [[flat functors]] 

$$
  X : \Delta^{op} \to Set
$$

are equivalently linear orders. Evidently, such a functor is in particular a [[simplicial set]] and we will show that $X$ being flat is equivalent to this simplicial set being the [[nerve]] of an [[inhabited set|inhabited]] linear order regarded as a [[category]] (a [[(0,1)-category]]).

First assume that $X$ is a [[flat functor]]. Since (by the discussion there) this preserves all [[finite limits]] that exist in $\Delta^{op}$, equivalently that it sends the finite [[colimits]] that exist in $\Delta$ to limits in $Set$, it in particular sends the gluings of intervals

$$
  \begin{aligned}
    [n] & \simeq [k] \coprod_{[0]} [l] \;\;\;\; (n = k + l)
    \\
    & \simeq [1] \coprod_{[0]} [1] \coprod_{[0]} \cdots \coprod_{[0]} [1]
  \end{aligned}
$$

in $\Delta$ to [[isomorphisms]]

$$
  \begin{aligned}
    X_n & \simeq X_k \times_{X_0} X_l
    \\
    & \simeq 
      X_1 \times_{X_0} \cdots \times_{X_0} X_1
  \end{aligned}
  \,.
$$

This are the [[Segal space|Segal relations]] that say that $X$ is the [[nerve]] of a [[category]].

Moreover, since [[monomorphisms]] are characterized by [[pullbacks]], $F$ being flat means that it sends jointly epimorphic families of morphisms in $\Delta$ to monomorphisms in $Set$. In particular, the epimorphic family $\{\partial_0 : [0] \to [1], \partial_1 : [0] \to [1]\}$ is sent to an injection

$$
  (d_0, d_1) : X_1 \hookrightarrow X_0 \times X_0
  \,.
$$

Since $X_1$ is the set of [[morphisms]] of the category that $X$ is the nerve of, this means that there is at most one morphism in this category from any one object to any other. Hence this category is a [[poset]].

Finally to show that this poset is an inhabited linear order, we use the fact that a functor is flat precisely if its [[category of elements]] [[filtered category|cofiltered]].

This means

1. The category of elements is inhabited, hence the poset of which $X$ is the nerve is inhabited.

1. For every two elements $y, z \in X_0$ there exist morphisms $\alpha, \beta : [0] \to [k]$ in $\Delta$ and $w \in X_k$ such that $X(\alpha) : w \mapsto y$ and $X(\beta) : w \mapsto z$. Since $X$ is the nerve of a poset, this means that there is a totally ordered set $w  = (w_0 \leq  \cdots \leq w_k)$ and $y$ and $z$ are among its elements $y = w_{\alpha(0)}$, $z = w_{\beta(0)}$. Accordingly we have either $y \leq z$ or $z \leq y$ and hence $X$ is in fact the nerve of a [[total order]].

1. If $y,z$ are elements in the total order  with  $y \leq z$ and $z \leq y$, this means that in the nerve we have elements $(y,z) \in X_1$ and $(z,y) \in X_1$ with $d_0(y,z) = d_1(z,y)$ and $d_1(y,z) = d_1(z,y)$. 

   By co-filtering, there exists a [[cone]] over this diagram in the category of elements, hence morphisms $\alpha, \beta : [1] \to [k]$ in $\Delta$ and $w \in X_k$ such that 

   1. $X(\alpha) : w \mapsto (y,z)$ and $X(\beta) : w \mapsto (z,y)$;

   1. $\partial_0 \circ \alpha = \partial_1 \circ \beta$ and $\partial_1 \circ \alpha = \partial_0 \circ \beta$.

   Here the last condition in $\Delta$ can only hold if $\alpha = \beta = const_{i}$, hence if $y = z$.

Conversely, assume that $X$ is the nerve of a linear order. We show that then it is a flat functor $X : \Delta^{op} \to Set$.

(...) 


=--

### For intervals
 {#ForIntervals}

[[Andre Joyal]] showed that $Set^{{\Delta}^{op}}$, the category of [[simplicial sets]], is the classifying topos for linear [[intervals]] (compare [[interval objects]]). For example, a geometric morphism from $Set$ to $Set^{{\Delta}^{op}}$ is an **[[interval]]** in $Set$, meaning a [[totally ordered set]] with distinct top and bottom elements. In general, a linear interval is a model for the one-sorted [[geometric theory]] whose [[signature]] consists of a binary [[relation]] $\leq$ and two [[constant|constants]] $0$, $1$, subject to the following [[axiom|axioms]]: 

* $\vdash (x \leq x)$
* $\exists_y (x \leq y) \wedge (y \leq z) \vdash (x \leq z)$ 
* $(x \leq y) \wedge (y \leq x) \vdash (x = y)$ 
* $\vdash (x \leq y) \vee (y \leq x)$ 
* $\vdash (0 \leq x) \wedge (x \leq 1)$ 
* $(0 = 1) \vdash false$ 

(Joyal calls this a **strict** linear interval; by removing the hypothesis of distinct top and bottom, one arrives at a weaker notion he calls "linear interval". Linear intervals in this sense are classified by the topos $Set^{\Delta_{a}^{op}}$, where $\Delta_a$, sometimes called the algebraist's Delta or the augmented [[simplex category]], is the category of all finite ordinals including the empty one.) 








### For local rings
 
#### Local rings

The classifying topos for [[local ring|local rings]] is the [[big Zariski topos]] of the [[scheme]] $Spec(\mathbb{Z})$.  A **local ring** is a model of the geometric theory of commutative unital rings subject to the extra axioms 

* $(0 = 1) \vdash false$ 
* $x + y = 1 \vdash \exists_z (x z = 1) \vee \exists_z (y z = 1)$ 

In a topos of sheaves over a [[sober space]], a local ring is precisely what algebraic geometers usually call a "sheaf of local rings": namely, a sheaf of rings all of whose [[stalk|stalks]] are local. See [[locally ringed topos]]. This is a special case of the case of [Cover-preserving flat functors](#CoverPreservingFLatFunctors) below.

#### Strict local rings
 {#StrictLocalRings}

For $Spec R$ an [[affine scheme]], the [[étale topos]] $Sh(X_{et})$ classifies "[[strict local ring|strict local R-algebras]]". The [[point of a topos|points of this topos]] are _[[strict Henselian ring|strict Henselian R-algebras]]_ ([Hakim, III.2-4](#Hakim)) and ([Wraith](#Wraith)).

See also [this MO discussion](http://mathoverflow.net/questions/48690/what-does-an-etale-topos-classify)

### For principal bundles {#PrincipalBund}

Essentially every topos may be regarded as a classifying topos for certain [[torsor]]s/[[principal bundle]]s.

#### Over bare groups {#BareGTor}

For any (bare / discrete) [[group]] $G$, write $\mathbf{B}G$ for its [[delooping]] groupoid, the groupoid with a single object and $G$ as its endomorphisms. The presheaf topos

$$
  G Set := PSh(\mathbf{B}G)
$$

of [[permutation representation]]s (objects are [[set]]s equipped with a $G$-[[action]], morphisms are $G$-equivariant maps between these) is the classifying topos for $G$-[[torsor]]s.

For example, if $X$ is a [[topological space]], geometric morphisms from the [[sheaf topos]] $Sh(X)$ of [[sheaves]] on (the [[category of open subsets]] of) $X$ to $G Set$ are the same as $G$-[[principal bundle]]s over $X$

$$
  G Bund(X) \simeq Topos(Sh(X), G Set)
  \,.
$$

This follows via [[Diaconescu's theorem]], which asserts that [[geometric morphism]]s $Sh(X) \to Sh(\mathbf{B}G)$ are equivalent to [[flat functor]]s

$$
  \mathbf{B}G \to Sh(X)
  \,.
$$

Such a flat functor picks a single sheaf on $X$ and encodes a $G$-action on this sheaf such that this sheaf is the sheaf of [[section]]s of a $G$-[[principal bundle]] on $X$.

+-- {: .num_theorem}
###### Theorem

Let $G$ be a (bare, discrete) group, write $\mathcal{B}G \in $ [[Top]] for the ordinary [[classifying space]] and $\mathbf{B}G \in $ [[Grpd]] the one-object groupoid version of $G$. There is a canonical [[geometric morphism]]s

$$
  PSh(\mathbf{B}G)
  \to
  Sh(\mathcal{B}G)
  \,.
$$

This is a _weak homotopy equivalence_ of toposes, in that it induces isomorphisms on [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of the terminal object.

=--

This is ([Moerdijk, theorem 1.1, proven in chapter IV](#Moerdijk)).
 





#### In terms of geometric theories {#BareGTorGeomTheo}

A [[geometric theory]] $T$ whose [[model]]s are $G$-torsors can be described as follows.  It has one sort, $X$, and one unary operation $g:X\to X$ for every element $g\in G$.  It has algebraic axioms $\top\vdash_x \;1(x) = x$ and $\top\vdash_x \;g(h(x)) = (g h)(x)$, which make $X$ into a $G$-set, and geometric axioms $\top \vdash\; \exists x \in X$ (inhabited-ness), $g(x) = x \;\vdash_x \;\bot$ for all $g\neq 1$ (freeness), and $\top\vdash_{x,y}\; \bigvee_{g\in G}\; g(x) = y$ (transitivity).

#### Over topological groups {#TopGTor}

If $G$ is a general [[topological group]] we have a [[simplicial object|simplicial]] [[topological space]] $G^{\times \bullet}$. The category $Sh(G^{\times \bullet})$ of [[sheaves on a simplicial topological space|sheaves on this simplicial space]] is a topos. 

This is such that for $X$ a topological space, geometric morphisms $Sh(X) \to Sh(G^{\times \bullet})$ classifies topological $G$-principal bundles on $X$.

This idea admits generalizations to [[localic groups]] --- and even to [[localic groupoids]].  For more details, see [[classifying topos of a localic groupoid]] .


#### The universal $G$-bundle topos {#UniversalBundle}

At [[generalized universal bundle]] and [[principal ∞-bundle]] it is discussed that the principal bundle classified by a morphims into a classifying object is its [[homotopy fiber]], and how the universal bundle is a replacement of the point such that its ordinary pullback models that [[homotopy pullback]].

Concretely, for $G$ a [[group]] and $\mathbf{B}G = \{\bullet \stackrel{g \in G}{\to} \bullet\}$ in [[∞Grpd]] its [[delooping]] [[groupoid]], the universal $G$-bundle is really just the point inclusion

$$
  \array{
    * 
    \\
    \downarrow
    \\
    \mathbf{B}G
  }
$$

in that for $X \to \mathbf{B}G$ a morphism, the corresponding $G$-[[principal ∞-bundle]] in [[? Grpd]] is the [[homotopy pullback]]

$$
  \array{
    P &\to& *
    \\
    \downarrow &{}^{\simeq}\swArrow& \downarrow
    \\
    X &\to& \mathbf{B}G 
  }
  \,.
$$

We can send this morphism $(* \to \mathbf{B}G)$ in [[Grpd]] with 

$$
  PSh(-) : Grpd \to Toposes
$$

to the [[2-category of toposes]] to get a [[geometric morphism]]

$$
  \array{
    PSh(*) = Set
    \\
    \downarrow^{\mathrlap{p}}
    \\
    PSh(\mathbf{B}G) = Set^G
  }
  \,.
$$

By the rules of morphisms of [[site]]s we have that the [[inverse image]] $p^* : PSh(\mathbf{B}G) \to Set$ is precomposition with $p : * \to \mathbf{B}G$, i.e. the functor that just forgets the $G$-action on a set. 

Its [[right adjoint]] [[direct image]] $p_* : Set \to PSh(\mathbf{B}G)$ is the functor

$$
  p_* : S \mapsto S \times G
$$

which sends a set $S$ to the $G$-set $S \times G$ equipped with the evident $G$-action induced by that of $G$ on itself.

Because for $(V,\rho)$ any set with $G$-action $\rho$ we have naturally

$$
  Hom_{Set}(S,V) \simeq Hom_{Set^G}(S \times G, (V,\rho))
  \,.
$$

The object 

$$
  p_*(*) = G \in PSh(\mathbf{B}G)
$$

singled out this way in this way is the universal object in $Set^G$, namely $G$ equipped with the canonical $G$-action on itself.

It ought to be true that the topos-incarnation of the $G$-principal bundle on a topological space $X$ classified by a [[geometric morphism]] $Sh(X) \to PSh(\mathbf{B}G)$ is the $(2,1)$-pullback

$$
  \array{
    \mathcal{P} &\to& Set
    \\
    \downarrow &{}^{\simeq}\swArrow& \downarrow
    \\
    Sh(X) &\to& PSh(\mathbf{B}G)
  }
  \,.
$$

> needs more discussion...

### For general localic groupoids
  {#ForLocalicGroupoids} 

In fact, _any_ [[Grothendieck topos]] can be thought of as a classifying topos for some [[localic groupoid]].  This is related to the discussion above, since Joyal and Tierney showed that any Grothendieck topos is equivalent to the $B G$ for some [[localic groupoid]] $G$.  A useful discussion of this idea starts
[here](http://golem.ph.utexas.edu/category/2007/10/geometric_representation_theor_2.html#c012724).

### For flat functors

As a special case of the above, any [[presheaf topos]], i.e. any topos of the form $Set^{C^{op}}$, is the classifying topos for [[flat functors]] from $C$ (sometimes also called "$C$-[[torsor]]s").  In other words, geometric morphisms $E \to Set^{C^{op}}$ are the same as [[flat functor]]s $C \to E$.  This is [[Diaconescu's theorem]].  If $C$ has finite limits, then a flat functor $C \to E$ is the same as a functor that preserves finite limits.

### For geometric theories / cover-preserving flat functors on a site
 {#CoverPreservingFLatFunctors}

Another way, apart from that [above](#ForLocalicGroupoids), of viewing any [[Grothendieck topos]] $E$ as a classifying topos is to start with a small [[site]] of definition for it.  Any such site gives rise to a [[geometric theory]] called the theory of [[cover-preserving functor|cover-preserving]] flat functors on that site.  The classifying topos of this theory is again $E$.

Moreover, for any object $X$ of $E$, there is a small site of definition
for $E$ which includes $X$, and thus for which $X$ is (part of) the universal object.  


We have:

+-- {: .num_prop #EveryToposIsAClassifyingToposForLocalAlgebras}
###### Proposition

Every [[sheaf topos]] has a [[cartesian site]] $(\mathcal{C}, J)$ of definition.

This $Sh(\mathcal{C}, J)$ is the classifying topos for cover-preserving [[flat functor]]s out of $\mathcal{C}$.

Every category of such functors is the category of [[model]]s of some geometric theory, and for every geometric theory there is such a cartesian site.

=--

This appears as ([Johnstone, remark D3.1.13](#Johnstone)).


### For local algebras
 {#LocalAlgebras}

As a special case or rather re-interpretation of the [above](#CoverPreservingFLatFunctors), let $\mathcal{T}$ be any
[[essentially algebraic theory]] and equip its [[syntactic category]] $\mathcal{C}_{\mathbb{T}}$ with some [[coverage]] $J$. Then the [[sheaf topos]] $Sh(\mathcal{C}_{\mathbb{T}}, J)$ is the classifying topos for _local $\mathbb{T}$-algebras_ : 

for $Sh(X)$ any [[sheaf topos]] a [[geometric morphism]]

$$
  \mathcal{O} : Sh(X) \to Sh(\mathcal{C}_{\mathbb{T}}, J)
$$

is

1. a $\mathbb{T}$-[[algebra over an algebraic theory|algebra]] in $Sh(X)$, hence a [[sheaf]] of $\mathbb{T}$-algebras over the site $X$;

1. such that this sheaf of algebras is local as seen by the respective topologies.

See [[locally algebra-ed  topos]] for more on this.

By prop. \ref{EveryToposIsAClassifyingToposForLocalAlgebras} we have that every [[sheaf topos]] is the classifying topos of _some_ theory of local algebras.

The [[vertical categorification]] of this situation to the context of [[(∞,1)-category]] theory is the notion of [[structured (∞,1)-topos]] and of [[geometry (for structured (∞,1)-toposes)]]:

The geometry $\mathcal{G}$ is the [[(∞,1)-category]] that plays role of the syntactic theory. For $\mathcal{X}$ an [[(∞,1)-topos]], a model of this theory is a limits and covering-preserving [[(∞,1)-functor]]

$$
  \mathcal{G} \to \mathcal{X}
  \,.
$$

The [[Yoneda embedding]] followed by [[∞-stackification]] 


$$
  \mathcal{G} \stackrel{Y}{\to} PSh_{(\infty,1)}(\mathcal{G})
  \stackrel{\bar(-)}{\to} Sh_{(\infty,1)}(\mathcal{G})
$$

constitutes a model of $\mathcal{G}$ in the (Cech) [[∞-stack]] [[(∞,1)-topos]] $Sh_{(\infty,1)}(\mathcal{G})$ and exhibits it as the classifying topos for such models (geometries):

This is _[[Structured Spaces]]_ [prop 1.4.2](http://arxiv.org/PS_cache/arxiv/pdf/0905/0905.0459v1.pdf#page=26).


## As a generalization of the notion of classifying space in topology

In view of the analogy between the classifying topos denoted $B G$, such that the [[groupoid]] $G Bund(X)$ of $G$-[[principal bundle]]s over $X$ is equivalent to geometric morphims $Sh(X) \to B G$:

$$
  G Bund(X) \simeq Topos(Sh(X), B G)
  \,
$$

and the notion of [[classifying space]] in [[topology]], which for the discrete group $G$ is a [[topological space]] $\mathcal{B} G$ such that

$$
  \pi_0 G Bund(X) \simeq \pi_0 Top(X, \mathcal{B}G)
  \,
$$

we should expect there to be a topos analog of the total space, $E G$, for the classifying space. This analog is the *generic G-torsor*, which is an internal $G$-torsor in the topos $Set^G$.  The important aspect of the space $E G$ is that as a principal $G$-bundle over $\mathcal{B} G$, it is a *universal element*, i.e. the natural transformation $Hom(X, \mathcal{B}G) \to G Bdl(X)$ that it induces (by the [[Yoneda lemma]]) is the isomorphism which exhibits $\mathcal{B}G$ as the object representing the functor $X \mapsto G Bdl(X)$.  For the same Yoneda reasons, the classifying topos $Sh(C_T)$ of any geometric theory $T$ comes with a *generic $T$-model*, which is a $T$-model in $Sh(C_T)$ which represents the functor $E \mapsto T Mod(E)$ in the same way.  For $T$ = the theory of $G$-torsors, this generic model is the generic $G$-torsor.

## Related concepts

* [[representable functor]]

* [[classifying space]], [[classifying stack]], [[moduli space]], [[moduli stack]], [[derived moduli space]]

* [[universal principal bundle]], [[universal principal infinity-bundle]]

* [[classifying morphism]]

* [[classifying (infinity,1)-topos]]



## References ##

A standard textbook reference is section D3 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

Original articles include

* [[Ieke Moerdijk]],  The classifying topos of a continuous groupoid I, _Trans. A.M.S._ **310** (1988), 629-668.

* [[Ieke Moerdijk]], The classifying topos of a continuous groupoid  II, _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_, **31** no. 2 (1990), 137-168.  ([web](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1990__31_2_137_0))
 

* [[Ieke Moerdijk]], Classifying spaces and classifying topoi, _Lecture Notes in Math._ **1616**, Springer-Verlag, New York, 1995.
 {#Moerdijk}

Classifying toposes as [[locally algebra-ed (infinity,1)-toposes]] are discussed in section 1.4 of

* [[Jacob Lurie]], _[[Structured Spaces]]_
 {#Lurie}

The [[étale topos]] as a classifying topos for [[strint local rings]] is discussed in III.2-4 of

* [[Monique Hakim]], _Topos annel&#233;s et sch&#233;mas relatifs_
 {#Hakim}

and

* [[Gavin Wraith]], _Generic Galois theory of local rings_
 {#Wraith}

[[!redirects Another page]]
[[!redirects classifying toposes]]
[[!redirects classifying topoi]]
