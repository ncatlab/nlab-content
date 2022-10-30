
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $X$ and $Y$ [[topological spaces]], a [[continuous function]] $X \to Y$ induces (in particular) two [[functors]]

* the [[direct image]] $f_* : Sh(X) \to Sh(Y)$

* the [[inverse image]] $f^* : Sh(Y) \to Sh(X)$

between the corresponding  [[Grothendieck topos|Grothendieck topoi]] of [[sheaf|sheaves]] on $X$ and $Y$. These are such that:

* $f^*$ is [[adjoint functor|left adjoint]] to $f_*$, so $f^*$ preserves all small [[colimits]] and $f_*$ preserves all small [[limits]].

* furthermore, $f^*$ is [[exact functor|left exact]] in that it preserves finite [[limits]].

Morever, if $X$ and $Y$ are 
[[sober space|sober]] [[topological spaces]]
every pair of functors with these properties comes uniquely from a continuous map $X \to Y$ (see the theorem below).

A _geometric morphism_ between arbitrary [[topos|topoi]] is the direct generalization of this situation.

Another motivation of the concept comes from the the fact that a [[functor]] such as $f^*$ that preserves finite [[limits]] and arbitrary [[colimits]] (since it is a [[adjoint functor|left adjoint]]) necessarily preserves all constructions in [[geometric logic]].  See also [[classifying topos]].


## Definition


+-- {: .num_defn}
###### Definition

If $E$ and $F$ are [[topos|toposes]], a **geometric morphism** $f:E\to F$ consists of an pair of [[adjoint functors]] $(f^*,f_*)$

$$
  f_* : E \to F
$$
$$
  E \leftarrow F : f^* 
  \,,
$$

such that the [[left adjoint]] $f^*:F \to E$ preserves [[finite limits]].

We say that 

* $f_*$ is the [[direct image]]

* $f^*$ is the [[inverse image]]

of the geometric morphism.

=--

If moreover the [[inverse image]] $f^*$ has also a [[left adjoint]] $f_! : E \to F$, then $f$ is an [[essential geometric morphism]].

+-- {: .num_remark}
###### Remark

Since [[Grothendieck topos|Grothendieck toposes]] satisfy the (dual) hypotheses of Freyd's special [[adjoint functor theorem]], any functor $f^*$ between Grothendieck toposes which preserves all small [[colimit]]s must have a [[right adjoint]].  Therefore, a geometric morphism $f : E \to F$ between Grothendieck toposes could equivalently be defined as a functor $E \leftarrow F : f^* $ preserving [[finite limits]] and all [[small set|small]] [[colimits]].

=--

+-- {: .num_remark}
###### Remark

In view of its definition in terms of a pair of [[adjoint functor]]s, the direction of a geometric morphism is a convention. However, with the other convention it would better be called an **algebraic morphism**.

See [[Isbell duality]] for more on this [[duality]] between [[algebra]] and [[geometry]].

=--

See also ([Johnstone, p. 162/163](#Johnstone)).


## Properties

We discuss some general properties of geometric morphisms. The 

* [Relation to homomorphisms of locales](#RelationToHomomorphismOfLocales)

also serves as a motivation or justification of the notion of geometric morphism. The

* [Relation to homomorphisms of sites](#RelationToMorphismsOfSites)

is a fairly straightforward generalization of that situation, reflecting the passage from (sheaf-) [[(0,1)-topos]]es to general [[topos|(1,1)-toposes]].

A somewhat subtle point about geometric morphisms of toposes is that there is also another sensible notion of topos [[homomorphism]]s: [[logical morphism]]s. In

* [Relation to logical morphism](#RelationToLogicalMorphisms)

aspects of the relation between the two concepts are discussed.

The reader wishing to learn about geometric morphisms systematically might want to first read the section on _[Geometric morphisms between presheaf toposes](#BetweenPresheafToposes)_ below, as much of the following discussion makes use of a few basic facts discussed there.

### Relation to homomorphisms of locales
 {#RelationToHomomorphismOfLocales}

The definition of geometric morphisms may be motivated as being a [[categorification]] of the definition of morphisms of [[locale]]s.

Recall that

+-- {: .num_defn #LocaleHomomorphisms}
###### Definition

A [[homomorphism]] of [[locale]]s 

$$
  f : X \to Y
$$

is dually a morphism of [[frame]]s (the "[[frame of opens|frames of open subsets]]" of $X$ and $Y$, respectively)

$$
  \mathcal{O}(X) \leftarrow \mathcal{O}(Y) : f^*
  \,.
$$

This, in turn, is a [[functor]] (of [[posets]]) that

1. preserves finite [[limit]]s (called [[meet]]s in this context);

1. preserves arbitrary (small) [[colimit]]s (called [[join]]s in this context).

=--

Such a preservation of finite limits and arbitrary colimits is precisely what characterizes the [[inverse image]] part of a geometric morphism, and hence by the [[adjoint functor theorem]] already characterizes the full notion of geometric morphisms. Since a [[locale]] may equivalently be thought of as a [[(0,1)-topos]], this means that geometric morphisms are direct generalization of the notion of locale homorphisms to 1-toposes.

The following says this in more precise fashion.

+-- {: .num_defn #DirectImageInducedByLocaleMorphism}
###### Definition

For $f : X \to Y$ a homomorphism of [[locale]]s, let

$$
  f_* : Sh(X) \to Sh(Y)
$$

be the functor between their [[sheaf topos]]es that sends a sheaf $F : \mathcal{O}(X)^{op} \to Set$ to the composite

$$
  f_* F : \mathcal{O}(Y)^{op} \stackrel{f^*}{\longrightarrow}
    \mathcal{O}(X)^{op} \stackrel{F}{\longrightarrow}
  Set
  \,,
$$

where $f^*$ is the corresponding frame morphism as in def. \ref{LocaleHomomorphisms}.

=--

+-- {: .num_prop}
###### Propositon

The functor $f_*$ in def. \ref{DirectImageInducedByLocaleMorphism} is the [[direct image]] part of a geometric morphism of sheaf toposes

$$
  (f^* \dashv f_*) : Sh(X) \stackrel{\overset{f^*}{\longleftarrow}}{\underset{f_*}{\longrightarrow}}
   Sh(Y)
  \,.
$$

Moreover, the corresponding [[inverse image]] functor $f^*$ does restrict on [[representable functor|representable]]s to the frame morphism that we also denoted $f^*$.

=--

In ([Johnstone](#Johnstone)) this appears as lemma C1.4.1 and theorem C1.4.3.

+-- {: .proof}
###### Proof

Since a morphism of [[frame]]s is a morphism of [[site]]s, as discussed there, this follows from the corresponding propositions in the section [Morphisms of sites and geometric morphisms](site#MorphismsOfSitesAndGeometricMorphisms).

=--

+-- {: .num_prop}
###### Propositon

The construction $X \mapsto Sh(X)$ extends to a [[2-functor]]

$$
  Sh : Locale \hookrightarrow Topos
$$

from the [[category]] [[Locale]] of [[locales]] to the [[2-category]] [[Topos]] of [[topos]]es and geometric morphisms between them

=--

See also at [[locale]] the section [relation to toposes](locale#RelationToToposes).

### Relation to morphisms of sites
 {#RelationToMorphismsOfSites}

See at [[morphism of sites]] the section _[Relation to geometric morphisms](morphism+of+sites#RelationToGeometricMorphisms)_.


### Relation to logical morphisms
 {#RelationToLogicalMorphisms}

+-- {: .num_prop}
###### Proposition

Every geometric morphism whose [[direct image]] is a [[logical morphism]] is an [[equivalence of categories|equivalence]].

=--

This is a restatement of [this proposition](logical+functor#LogicalMorphismsRightAdjointToCartesianFunctors) at [[logical morphism]]. See there for a proof.

But [[inverse images]] can be nontrivial logical morphisms:

+-- {: .num_prop}
###### Proposition

 The [[inverse image]] of an [[etale geometric morphism]] is a [[logical morphism]].

=--

Generally, a geometric morphism with logical inverse image is called an 
[[atomic geometric morphism]]. See there for more details.


### Structure preserved by geometric morphisms
 {#StructurePreserved}

The [[inverse image]]s of geometric morphisms preserves the structure of toposes in the sense of their characterization as _categories with [[finite limit]]s that are [well-powered](indexed+category#WellPoweredness) [[indexed categories]] with respect to the canonical indexing over themselves.

This appears in ([Johnstone](#Johnstone)) as remark B2.2.7 based on example B1.3.17 and prop. B1.3.14. See at [[indexed category]] the section [Well-poweredness](indexed+category#WellPoweredness)


### Surjection/embedding factorization

Every geometric morphism factors, essentially uniquely, as a [[geometric surjection]] followed by a [[geometric embedding]]. See _[[geometric surjection/embedding factorization]]_ for more on this.

## Special classes of geometric morphisms

There are various special cases and types of classes of geometric morphisms. For instance

* [[global section|global sections]]

* [[geometric embedding]]

* [[locally connected geometric morphism]]

  * [[essential geometric morphism]]

  * [[connected geometric morphism]]

* [[etale geometric morphism]]

* [[open geometric morphism]], [[closed geometric morphism]]

* [[proper geometric morphism]]

* [[local geometric morphism]]

* [[bounded geometric morphism]]

* [[base change]]

* [[localic geometric morphism]]

* [[hyperconnected geometric morphism]]

* [[cohesive topos|cohesive morphism]]

* [[atomic geometric morphism]]

The following subsections describe some of these in more detail.


### Between presheaf toposes
 {#BetweenPresheafToposes}

Let $C$ and $D$ be any two [[categories]]. We write $C^{op}$ and $D^{op}$ for their [[opposite categories]] and $[C, Set]$, $[D, Set]$ for the corresponding [[presheaf toposes]] over $C^{op}$ and $D^{op}$, respectively.

+-- {: .num_prop }
###### Proposition

Every [[functor]] $f : C \to D$ induces an ([[essential geometric morphism|essential]], even) geometric morphism

$$
  f := (f^* \dashv f_*) 
  : 
  [C,Set] 
    \stackrel{\overset{f_!}{\longrightarrow}}{\stackrel{\overset{f^*}{\longleftarrow}}{\underset{f_*}{\longrightarrow}}}
  [D, Set]
  \,,
$$

where $f^* = (-) \circ f$ is the functor given by precomposition presheaves with $f$.

Moreover, for $\eta : f \Rightarrow g : C \to D$ a [[natural transformation]] between two such functors there is an induced [[geometric transformation]] $(f^* \dashv f_*) \Rightarrow (g^* \dashv g_*)$. This is compatible with composition in that it makes forming [[presheaf topos]]es a [[2-functor]]

$$
  [-,Set] : Cat \to Topos
$$

from the [[2-category]] [[Cat]] to the [[2-category]] [[Topos]].

=--

This appears as ([Johnstone, example A4.1.4](#Johnstone)).

+-- {: .proof}
###### Proof

Since [[categories of presheaves]] have all [[limit]]s and [[colimit]]s, the left and right [[Kan extension]]s $Lan_f$ and $Ran_f$  along $f$ exists, and form with $f^*$ an [[adjoint triple]]

$$
  [C,Set]
    \stackrel{\overset{Lan_f}{\longrightarrow}}{\stackrel{\overset{f^*}{\longleftarrow}}{\underset{Ran_f}{\longrightarrow}}}
  [D, Set]
  \,.
$$

Hence $f_! \simeq Lan_f$ and $f_* \simeq Ran_f$. Notice that [[left adjoint]]s and [[right adjoint]]s to a functor are, if they exist, unique up to unique [[isomorphism]].

=--

Next we consider extra [[property]] on $C$, $D$ and $f$ such that $f^*$ induces also a second geometric morphism, going the other way round. This plays a role for the discussion of [morphisms of sites](#RelationToMorphismsOfSites). For that reason we pass now from $C$ and $D$ to their [[opposite categories]] hence consider genuine [[presheaves]] on $C$ and $D$.

+-- {: .num_prop }
###### Proposition

Let $C$ and $D$ by categories with [[finite limit]]s and let $f : C \to D$ be a finite-limit [[preserved limit|preserving]] functor.

Then in the [[adjoint triple]]

$$
  (f_! \dashv f^* \dashv f_*) 
  :
  [C^{op},Set] 
    \stackrel{\overset{f_!}{\longrightarrow}}{\stackrel{\overset{f^*}{\longleftarrow}}{\underset{f_*}{\longrightarrow}}}
  [D^{op}, Set]
$$

the left [[Kan extension]] $f_!$ also preserves finite limits and hence in this case $f^*$ is also the [[direct image]] of a geometric morphism going the other way round:

$$
  (f_! \dashv f^* ) : [D^{op},Set] \to [C^{op}, Set]
  \,.
$$

=--

This appears as ([Johnstone, example A4.1.10](#Johnstone)).

+-- {: .proof}
###### Proof

Recall that for $F : C^{op} \to Set$ a functor, the left [[Kan extension]] $f_! F : D^{op} \to Set$ is computed over each object $d \in D$ by the [[colimit]]

$$
  (f_! F)(d) = 
  \lim_\to
  \left(
     (d/f)^{op} \stackrel{U}{\to} C^{op} \stackrel{F}{\to} Set
  \right)
$$

where $(d/f)$ is the [[comma category]] and 

$$
  U : (d/f) \to C
$$

is the evident forgetful functor. This is natural in $F$ and so $(f_! -)(d)$ is the functor

$$
  (f_! -)(d) : [C^{op}, Set] \stackrel{U^*}{\to}
   [(d/f)^{op}, Set]
   \stackrel{\lim_\to}{\to}  
   Set
  \,.
$$

By the above argument $U^*$ has a [[left adjoint]] (the left [[Kan extension]] along $U$) hence itself preserves all [[limit]]s. 

It then suffices to observe (see below) that by the fact that $f$ preserves finite limits we have that the categories $(d/f)^{op}$ are [[filtered categories]]. Then by the fact (see there) that [[filtered colimit]]s commute with finite limits, it follows that also $\lim_\to$ preserves finite limits, and hence $(f_! -)(d)$ does. Since colimits of presheaves are computed objectwise, this shows that $f_!$ preserves finite limits. This completes the proof.

Here is an explicit desciption of the filteredness of the [[comma category]] $(d/f)^{op}$ for any object $f$.

We check the axioms on a [[filtered category]]:

* _non-emptiness_ : There is an object in $(d/f)^{op}$: since $f$ by assumption preserves the [[terminal object]],  take the terminal morphism $(d \to f(*) = *)$;

* _connectedness_ : for any two objects $(d \stackrel{h_1}{\to} f(c_1))$ and $(d \stackrel{h_2}{\to} f(c_2))$ form the [[product]] $c_1 \times c_2$ and use that $f$ preserves this to produce the object $(d \stackrel{f(h_1), f(h_2)}{\to} f(c_1) \times f(c_2) \simeq f(c_1 \times c_2))$. Then the image under $f$ of the two projections provides the required [[span]]

  $$
    \array{
      && d
      \\
      & {}^{\mathllap{f(h_1)}}\swarrow & \downarrow^{(f(h_1),f(h_2))} & \searrow^{\mathrlap{f(h_2)}} 
      \\
      f(c_1) &\stackrel{f(p_1)}{\leftarrow}&
      f(c_1 \times c_2)
      &   
      \stackrel{f(p_2)}{\to}
      & f(c_2)
    }
    \,.
  $$

* finally, for 

  $$
    \array{
       && d
       \\
       & \swarrow && \searrow
       \\
       f(c_1) && \stackrel{\overset{h_1}{\to}}{\underset{h_2}{\to}}& & f(c_2)
    }
  $$

  two [[parallel morphism]], let $eq(h_1,h_2)$ be the [[equalizer]] of the underlying morphism in $C$. Since $f$ preserves equalizers we have an object $(d \to f(eq(h_1,h_2)))$ and a morphism to $(d \to f(c_1))$ that equalizes the above two morphisms.


=--

### Surjections and embeddings

A geometric morphism $f : E \to F$ is a **surjection** if $f^*$ is [[faithful functor|faithful]].  It is an **[[geometric embedding|embedding]]** if $f_*$ is [[full and faithful functor|fully faithful]].

+--{: .un_prop}
###### Proposition
Up to equivalence, every [[geometric embedding|embedding]] of toposes is of the form 
$$
  Sh_j(E) \to E
  \,,
$$
where $Sh_j(E)$ is the topos of [[sheaf|sheaves]] with respect to a [[Lawvere-Tierney topology]] $j : \Omega \to \Omega$ on $E$.
=--

This means in particular that fully faithful geometric morphisms into [[Grothendieck topos|Grothendieck topoi]] are an equivalent way of encoding a [[Grothendieck topology]]. 

+--{: .un_prop}
###### Proposition
Up to equivalence, every surjection of topoi is of the form 
$$ E \to E_G $$
where $E_G$ is the category of coalgebras for a finite-limit-preserving [[comonad]] on $E$.
=--

Every geometric morphism $f:E\to F$ factors, uniquely up to equivalence, as a surjection followed by an embedding.  There are two ways to produce this factorization: either construct $E_G$ where $G= f^*f_*$ is the comonad induced by the adjunction $f^*\dashv f_*$, or construct $Sh_j(F)$ where $j$ is the smallest Lawvere-Tierney topology on $F$ such that $f$ factors through $Sh_j(F)$.  In fact, surjections and embeddings form a 2-categorical [[orthogonal factorization system]] on the 2-category of topoi.


### Global sections and constant sheaves

For every [[Grothendieck topos]] $E$, there is a geometric morphism

$$
  \Gamma : E  \stackrel{\leftarrow}{\to} Set : const
$$

called the [[global section]]s functor. It is given by the [[hom-set]] out of the [[terminal object]]

$$
  \Gamma(-) = Hom_E({*}, -)
$$

and hence assigns to each object $A\in E$ its set of [[global element]]s $\Gamma(A) = Hom_E(*,A)$. If we think of $A$ as a [[sheaf]], then $\Gamma(A)$ is the set of **global sections**.

The [[left adjoint]] $const : Set \to E$ of the global section functor is the canonical [[Set]]-[[copower|tensoring]] functor

$$
  \otimes : Set \times E \to E
$$

applied to the [[terminal object]]

$$
  const = (-)\otimes {*} : Set \to E
$$

which sends a set $S$ to the [[coproduct]] of $|S|$ copies of the terminal object

$$
  S \otimes {*} = \coprod_{s \in S} {*}
  \,.
$$

This is called the **constant object** of $E$ on the set $S$. Notably when $E$ is a [[Grothendieck topos|sheaf topos]] this is the **[[constant sheaf]]** on $S$. 

The [[left adjoint]]ness is just the defining property of the [[copower|tensoring]]

$$
  Hom_E(const S, A) \simeq Hom_E(S \otimes {*},A)
  \simeq
  Hom_{Set}(S, Hom_E(*,A))
  \,.
$$

This left adjoint preserves [[product]]s, using that colimits in a  topos are stable by base change (see [[commutativity of limits and colimits]])

$$
   \left( \coprod_{s_1 \in S_1} *\right)
   \times
   \left( \coprod_{s_2 \in S_2} *\right)
   =
   \coprod_{s_1 \in S_1}  \left(* \times \left( \coprod_{s_2 \in S_2} *\right)\right)
   =
   \coprod_{s_1 \in S_1}  \left( \coprod_{s_2 \in S_2} *\right)
   =
   \coprod_{s_1 \in S_1} \coprod_{s_2 \in S_2} *
   =
   \coprod_{s \in S_1 \times S_2} *
$$

and it preserves [[equalizer]]s and therefore [[limit]]s. So it is left exact and we do have a geometric morphism.



### Point of a topos

For $E$ a topos, a geometric morphism 

$$
  x : Set \to E
$$

is called a [[point of a topos]].


### Change-of-base

For $E$ any [[topos]] and $k : B \to A$ any morphism in $E$ there is the [[base change|change-of-base]] functor of [[over category|over categories]] 
$$
  k^* : (E/A) \to (E/B)
$$
by [[pullback]]. As described at [[dependent product]] this functor has both a [[left adjoint]] $\coprod_k : E/B \to E/A$ as well as a [[right adjoint]] $\prod_k : E/A \to E/B$.  Therefore
$$
  (\Pi_k, k^*) : E/B \leftrightarrow E/B
$$

is a geometric morphism. Hence $(\Pi_k \dashv k^* \dashv \coprod_k)$ is an [[essential geometric morphism]].

### Sheafification

A [[category of sheaves]] is a [[geometric embedding]] into a presheaf topos

$$
  Sh(C) \hookrightarrow PSh(C)
  \,.
$$


### Geometric morphisms of sheaf topoi 
 {#sheaftopoi}

Geometric morphisms between [[localic topoi]] are equivalent to [[continuous maps]] of [[locales]], which in turn are equivalent to continuous maps of [[topological spaces]] if you restrict to [[sober spaces]].

Unrolling this: For $X$ a [[topological space]], write $Sh(X) := Sh(Op(X))$ as usual for the [[topos]] given by the [[category of sheaves]] on the [[category of open subsets]] $Op(X)$ with the standard [[coverage]]

+-- {: .un_lemma}
###### Lemma

For every continuous map $f : X \to Y$ of [[sober space|sober]] [[topological spaces]] with the induced [[functor]] $f^{-1} : Op(Y) \to Op(X)$ of [[sites]], the [[direct image]]

$$
  f_* : Sh(X) \to Sh(Y)
$$

and the [[inverse image]]

$$
  f^* : Sh(Y) \to Sh(X)
$$

constitute a geometric morphism 

$$
   f : Sh(X) \to Sh(Y)
$$

(denoted by the same symbol, by convenient abuse of notation). 

This map $Hom_{Top}(X,Y) \to GeomMor(Sh(X),Sh(Y))$ is an bijection of sets.

=--

+-- {: .proof}
###### Proof

That the induced pair $(f^*, f_*)$ forms a geometric morphism is (or should eventually be) discussed at [[inverse image]].

We now show that every geometric morphism of sheaf toposes arises this way from a continuous function, at least up to isomorphism.  (In fact, more is true: the category of geometric morphisms $Sh(X)\to Sh(Y)$ is equivalent to the poset of continuous functons $X\to Y$ with the [[specialization ordering]].)  We follow [MacLane-Moerdijk, page 348](#MacLaneMoerdijk).


One reconstructs the continuous map $f : X \to Y$ from a geometric morphism $f : Sh(X) \to Sh(Y)$ as follows.

Write ${*} = Y \in Sh(Y)$ for the sheaf on $Op(Y)$ constant on the singleton set, the [[terminal object]] in $Sh(Y)$.

Notice that since the [[inverse image]] $f^*$ preserves finite [[limits]], every [[subobject]] $U_Y \hookrightarrow {*}$ is taken by $f^*$ to a subobject $U_X \hookrightarrow X$, obtained by applying $f^*$ to the [[pullback]] diagram 

$$
  \array{
    U_Y &\to& {*} = Y
    \\
    \downarrow && \downarrow
    \\
    {*} = Y &\to& \Omega
  }
$$

that characterizes the subobject $U_Y$ in the [[topos]].

But, as the notation already suggests, the subobjects of $X,Y$ are just the open sets, i.e. the representable sheaves.

This yields a _function_ $f^* : Obj(Op(Y)) \to Obj(Op(X))$ from open subsets to open subsets.  By assumption, this preserves finite limits and arbitrary colimits, i.e. finite intersections and arbitrary unions of open sets.  In other words, it is a [[frame|frame homomorphism]], and thus can be regarded as a morphism $X\to Y$ of [[locales]].

We can now use this to define a function $\bar f : X \to Y$ of the sets underlying the topological spaces $X$ and $Y$ by setting

$$
  (\bar f(x) = y)
  \Leftrightarrow
  \forall V \ni y: x \in f^*(V)  
  \,.
$$

This yields a well defined function for the following reasons (which for the moment we spell out in the case where $Y$ is [[Hausdorff space|Hausdorff]], although the result should hold ---and furthermore, hold [[constructive mathematics|constructively]]--- whenever $Y$ is sober):

* there is at most one $y$ satisfying this equation: if $y_1 \neq y_2$ both satisfy it, there are, by assumption of $Y$ being [[Hausdorff space|Hausdorff]], neighbourhoods $V_1 \ni y_1$ and $V_2 \ni y_2$ such that (using that $f^*$ preserves limits hence intersections) $f^*(V_1) \cap f^*(V_2) = f^*(V_1 \cap V_2) = \emptyset$, which contradicts the assumption.

* there is at least one $y$ satisfying this equation: again by contradiction: if there were none then every $y \in Y$ has a neighbourhood $V_y$ with $x \not\in f^*(V_y)$, so that similarly to above we conclude with $x \not\in \cup_{y \in Y} f^*(V_y) = f^*(\cup_y V_y) = f^*(Y) = X$ again a contradiction.

+-- {: .query}
Am I right that what we are really need of our space here is not necessarily that it be Hausdorff but simply that it be [[sober space|sober]]?  (Then the nonconstructive aspects of the argument ---which is what made me look at this--- come in only because the theorem that a Hausdorff space must be sober is not constructively valid.)  ---Toby

[[Mike Shulman]]: Yes, that's exactly right.  All the complication defining $\bar f$ above is just an unrolled way of saying that geometric morphisms between [[locale|localic]] topoi are equivalent to continuous maps of locales, which are equivalent to continuous functions if you have sober spaces.  I think that should be clarified.

_Toby_:  OK, I added a paragraph at the beginning of the example to clarify this.  I still need to rewrite the argument immediately above to apply to sober spaces.  (Everything else seems to go through exactly the same.)
=--

So our function $\bar f : X \to Y$ is well defined and satisfies $\bar f^{-1}(U_Y) = f^*(U_Y)$ for every open set $U_Y \in Obj(Op(Y))$. In particular it is therefore a continuous map.

It remains to check that this map reproduces the geometric morphism that we started with. For that we compute its [[direct image]] on any sheaf $A \in Sh(X)$ as

$$
  \begin{aligned}
    \bar f_*(A) : U_Y &\mapsto A(\bar f^{-1}(U_Y))
    \\
    & \simeq Hom_{Sh(X)}(\bar f^{-1}(U_Y),A)
    \\
    & = Hom_{Sh(X)}(f^* V, E)
    \\
    & \simeq Hom_{Sh(X)}(V, f_* E)
    \\
    & \simeq (f_* A)(U_Y)
  \end{aligned}
$$

=--

+-- {: .num_cor}
###### Corollary

The points $x \in X$ of the topological space $X$ are in canonical bijection with the points of $Sh(X)$ in the sense of [[point of a topos]].

=--



## Related concepts

* [[étale map]]

* [[logical morphism]]

* **geometric morphism**

  * [[geometric logic]], [[geometric theory]]

* [[(∞,1)-geometric morphism]]


## References

Geometric morphisms are the topic of section VII of

* [[Saunders MacLane]] and [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ .
 {#MacLaneMoerdijk}

Embeddings and surjections are discussed in section VII.4.

Geometric morphisms are defined in section A4 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

The special classes of geometric morphisms are discussed in section C3.

[[!redirects geometric morphisms]]