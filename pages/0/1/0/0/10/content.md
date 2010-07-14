<div class="rightHandSide toc">
[[!include topos theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## The idea 


The _classifying topos_ for a given type of mathematical structure $T$ --- for example the structures: "[[group]]", "[[torsor]]", "[[ring]]", "[[category]]"  etc. --- is a ([[Grothendieck topos|Grothendieck]]) [[topos]] $S[T]$ such that [[geometric morphisms]] $f: E \to S[T]$ are the same as structures of this sort in the topos $E$, i.e. groups [[internalization|internal to]] $E$, torsors internal to $E$, etc.  In other words, a classifying topos is a [[representing object]] for the functor which sends a topos $E$ to the category of structures of the desired sort in $E$.

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

In a tautological way, every topos $F$ is the classifying topos for something, namely for the categories of [[geometric morphism]]s $E \to F$ into it. The concept of [[geometric theory]] allows to usefully interpret these categories as _categories of certain structures in $E$_ :

as decribed in [Geometric theories -- In terms of sheaf topoi](http://ncatlab.org/nlab/show/geometric+theory#InTermsOfSheafTopoi), every [[sheaf topos]] $F$ is a completion $S[T]$ of the [[syntactic category]] $C_T$ of _some_ [[geometric theory]] $T$

$$
  F \simeq S[T]  
  \,.
$$

And structures of type $T$ in $E$ is what geometric morphisms $E \to F$ classify.

So the **classifying [[topos]]** for the geometric theory $T$ is a [[Grothendieck topos]] $S[T]$ equipped with a "universal model $U$ of $T$".  This means that for any Grothendieck topos $E$ together with a model $X$ of $T$ in $E$, there exists a unique (up to isomorphism) [[geometric morphism]] $f: E \to S[T]$ such that $f^*$ maps the $T$-model $U$ to the model $X$.  More precisely, for any Grothendieck topos $E$, the category of $T$-models in $E$ is equivalent to the category of geometric morphisms $E \to S[T]$.

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

Classifying toposes can also be defined over any base topos $S$ instead of [[Set]].  In that case "Grothendieck topos" is replaced by "bounded $S$-topos."


## Background on the theory of theories


The notion of _classifying topos_ is part of a trend, begun by [[Bill Lawvere|Lawvere]], of viewing a mathematical [[theory]] as a category with suitable exactness properties and which contains a "generic model", and a model of the theory as a functor which preserves those properties.  This is described in more detail at [[internal logic]] and [[type theory]], but here are some simple examples to give the flavor.  The original example is that of a 'finite products theory':

* **Finite products theory.**  Roughly speaking, a 'finite products theory', 'Lawvere theory', or 'algebraic theory' is a theory describing some mathematical structure that can be defined in an arbitrary category with finite products.  An example would be the theory of [[groups]]. As explained in the entry for [[Lawvere theory]], for each such theory $T$ there is a category with finite products $C_{fp}[T]$, which serves as a "classifying category" for $T$, in that models of $T$ in the category of sets correspond to product-preserving functors $f : C_{fp}[T] \to Set$.   More generally, for any category with finite products, say $E$, models of $T$ in $E$ correspond to product-preserving functors $f : C_{fp}[T] \to E$.   

* **Finite limits theory.** Next up the line is the notion of  'finite limits theory', sometimes called an [[essentially algebraic theory]].  This is roughly a theory describing some structure that can be defined in an arbitrary category with finite limits (also called a [[finitely complete category]]).  An example of a finite limits theory would be the theory of categories.   (The notion of 'category' requires finite limits, while the notion of 'group' does not, because categories but not groups involve a _partially defined_ operation, namely composition of morphisms.)    Every finite limits theory $T$ admits a classifying category $C_{fl}(T)$: a finitely complete category such that models of $T$ in a category $E$ with finite limits correspond to functors $f: C_{fl}(T) \to E$ that preserve finite limits.  (Such functors are called [[left exact]], or 'lex' for short.)  

* **Geometric theory.** Further up the line, a [[geometric theory]] is roughly a theory which can be formulated in that fragment of first-order logic that deals in finite limits and arbitrary (small) colimits, plus certain [[familial regularity and exactness|exactness]] properties the details of which need not concern us.  The point is that a category with finite limits, small colimits, and appropriate exactness is just a Grothendieck topos, and a functor preserving finite limits and small colimits is just the inverse image part of a geometric morphism.  Just as in the previous two cases, any 'geometric theory' has a classifying category $S[T]$ (which is now a Grothendieck topos) which possesses a "generic object" for that theory, and T-models in any other Grothendieck topos E can be identified with geometric morphisms $f\colon E\to S[T]$, or specifically with their inverse image parts.

Each type of theory may be considered a $2$-theory, or [[doctrine]].  Furthermore, each type of theory can be promoted to a theory "further up the line", by [[completion|freely adding]] the missing structure to the classifying category.  This can always be done purely formally, but in a few cases this promotion also has other, more explicit descriptions.

For instance, to go from a finite products theory $T$ to the corresponding finite limits theory, we can take the opposite of the category of [[finitely presentable object|finitely presentable models]] of $T$ in $Set$, thanks to [[Gabriel-Ulmer duality]].  Similarly, to go from a finite limits theory to the classifying topos of the corresponding geometric theory, we can take the category of presheaves on the classifying category of the finite limits theory.

## Examples 

### For objects

The [[presheaf topos]] $[FinSet, Set]$ on the [[opposite category]] of [[FinSet]] is the classifying topos _for objects_, sometimes called the "object classifier" (not to be confused with the notion of an [[object classifier]] in an $(\infty,1)$-topos).

For $E$ any topos, a geometric morphism $E \to [FinSet,Set]$ is equivalently just an [[object]] of $E$.

### For groups

We discuss the [[finite product theory]] of [[group]]s. This theory has a classifying category $C_{fp}(Grp)$.  $C_{fp}(Grp)$ is a category with finite products equipped with an object $G$, the "[[walking]] group", a morphism $m: G \times G \to G$ describing multiplication, a morphism $inv : G \to G$ describing inverses, and a morphism $i: 1 \to G$ describing the identity element of $G$, obeying the usual group axioms.   For any category with finite products, say $E$, a finite-product-preserving functor $f: C_{fp}(Grp) \to E$ is the same as a [[group object]] in $E$.   For more details, see [[Lawvere theory]].

We can promote $C_{fp}(Grp)$ to a category with finite limits, $C_{fl}(Grp)$, by adjoining all finite limits.   As mentioned above, one way to do this is to take the category of models of $C_{fp}(Grp)$ in Set, which is simply $Grp$, and then take the full subcategory of [[finitely presentable object|finitely presentable]] groups.  By [[Gabriel-Ulmer duality]], the opposite of this is $C_{fl}(Grp)$.
For any category with finite products, say $E$, a left exact functor $f: C_{fp}(Grp) \to E$ is the same as a [[group object]] in $E$.

We can further promote $C_{fl}(Grp)$ to a [[Grothendieck topos]] by taking the category of [[presheaves]].  This gives the classifying topos for groups:
$$       S[Grp] = Set^{C_{fl}(Grp)^{op}}  \, . \]
For any Grothendieck topos, say $E$, a left exact left adjoint functor $ f^*: S[T] \to E $ is the same as a [[group object]] in $E$.

### For rings

The discussion above for groups can be repeated verbatim for rings, since they too are described by a finite products theory.

### For intervals

[[Andre Joyal]] showed that $Set^{{\Delta}^{op}}$, the category of [[simplicial sets]], is the classifying topos for [[interval objects]].  For example, a geometric morphism from $Set$ to $Set^{{\Delta}^{op}}$ is an **interval** in $Set$, meaning a linearly ordered set with a top and bottom element.  

### For local rings

The classifying topos for [[local ring|local rings]] is the [[big Zariski topos]] of the [[scheme]] $Spec(\mathbb{Z})$.  Note that a "local ring" in a topos (the structure classified by this topos) is precisely what algebraic geometers usually call a "sheaf of local rings": namely, a sheaf of rings all of whose [[stalk|stalks]] are local.

### Any Grothendieck topos 

In fact, _any_ [[Grothendieck topos]] can be thought of as a classifying topos.  This is related to the discussion above, since Joyal and Tierney showed that any Grothendieck topos is equivalent to the $B G$ for some localic groupoid $G$.  A useful discussion of this idea starts
[here](http://golem.ph.utexas.edu/category/2007/10/geometric_representation_theor_2.html#c012724).

### Any topos of presheaves

As a special case of the above, any presheaf topos, i.e. any topos of the form $Set^{C^{op}}$, is the classifying topos for [[flat functors]] from $C$ (sometimes also called "$C$-torsors").  In other words, geometric morphisms $E \to Set^{C^{op}}$ are the same as flat functors $C \to E$.  This is [[Diaconescu's theorem]].  If $C$ has finite limits, then a flat functor $C \to E$ is the same as a functor that preserves finite limits.

### For cover-preserving flat functors on a site

Another way of viewing any Grothendieck topos $E$ as a classifynig topos is to start with a small [[site]] of definition for it.  Any such site gives rise to a [[geometric theory]] called the theory of [[cover-preserving functor|cover-preserving]] flat functors on that site.  The classifying topos of this theory is again $E$.

Moreover, for any object $X$ of $E$, there is a small site of definition
for $E$ which includes $X$, and thus for which $X$ is (part of) the universal object.  

> [[Urs Schreiber|Urs]]: check if the following paragraph is correct

The [[vertical categorification]] of this to the context of [[(∞,1)-category]] theory is the notion of [[structured (∞,1)-topos]] and of [[geometry (for structured (∞,1)-toposes)]]:

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

+-- {: .un_theorem}
###### Theorem

Let $G$ be a (bare, discrete) group, write $\mathcal{B}G \in $ [[Top]] for the ordinary [[classifying space]] and $\mathbf{B}G \in $ [[Grpd]] the one-object groupoid version of $G$. There is a canonical [[geometric morphism]]s

$$
  PSh(\mathbf{B}C)
  \to
  Sh(\mathcal{B}G)
  \,.
$$

This is a _weak homotopy equivalence_ of toposes, in that it induces isomorphisms on [[geometric homotopy groups in an (∞,1)-topos|geometric homotopy groups]] of the terminal object.

=--

+-- {: .proof}
###### Proof

This is theorem 1.1, proven in chapter IV of

* [[Ieke Moerdijk]], Classifying spaces and classifying topoi, _Lecture Notes in Math._ **1616**, Springer-Verlag, New York, 1995.

=--




#### In terms of geometric theories {#BareGTorGeomTheo}

A [[geometric theory]] $T$ whose [[model]]s are $G$-torsors can be described as follows.  It has one sort, $X$, and one unary operation $g:X\to X$ for every element $g\in G$.  It has algebraic axioms $\top\vdash_x \;1(x) = x$ and $\top\vdash_x \;g(h(x)) = (g h)(x)$, which make $X$ into a $G$-set, and geometric axioms $\top \vdash\; \exists x \in X$ (inhabited-ness), $g(x) = x \;\vdash_x \;\bot$ for all $g\neq 1$ (freeness), and $\top\vdash_{x,y}\; \bigvee_{g\in G}\; g(x) = y$ (transitivity).

#### Over topological groups {#TopGTor}

If $G$ is a general [[topological group]] we have the  is a [[simplicial object|simplicial]] [[topological space]] $G^{\times \bullet}$. The category $Sh(G^{\times \bullet})$ of [[sheaves on a simplicial topological space|sheaves on this simplicial space]] is a topos. 

This is such that for $X$ a topological space, geometric morphisms $Sh(X) \to Sh(G^{\times \bullet})$ classifies topological $G$-principal bundles on $X$.

This idea admits generalizations to [[localic groups]] --- and even to [[localic groupoids]].  For more details, see [[classifying topos of a localic groupoid]] .

## Classifying topos as a generalization of the notion of classifying space in topology

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


## References ##

* [[Ieke Moerdijk]],  The classifying topos of a continuous groupoid I, _Trans. A.M.S._ **310** (1988), 629-668.

* [[Ieke Moerdijk]], The classifying topos of a continuous groupoid  II, _Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques_, **31** no. 2 (1990), 137-168.  ([web](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1990__31_2_137_0))

* [[Ieke Moerdijk]], Classifying spaces and classifying topoi, _Lecture Notes in Math._ **1616**, Springer-Verlag, New York, 1995.


[[!redirects Another page]]
[[!redirects classifying toposes]]
[[!redirects classifying topoi]]
