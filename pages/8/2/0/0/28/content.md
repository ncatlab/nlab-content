> This article is about the notion prevalent in [[category theory]] and [[homotopy theory]], also known as a [[Brandt groupoid]] ([Brandt 27](#Brandt27)). For the notion involving a globally defined binary operation, see [[magma]].


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}



## Idea
 {#Idea}

Where a _[[group]]_ may be thought of as a _group of symmetry transformations_ that [[isomorphism|isomorphically]] relates one [[object]] to itself (the _[[symmetries]]_ of one object, such as the [[isometries]] of a [[polyhedron]]) a _groupoid_ is a collection of symmetry transformations acting between possibly more than one object.


Hence a groupoid consists of a [[set]] of objects $x, y, z, \cdots$ and for each [[pair]] of objects $(x,y)$ there is a set of transformations, usually denoted by arrows

$$
  x \overset{f}{\longrightarrow} y
$$

which may be composed if they are composable (i.e. if the first ends where the second starts)

$$
  \array{
    && y
    \\
    & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{g}}
    \\
    x && \underset{g \circ f}{\longrightarrow}  && z
  }
$$

such that this composition is [[associativity|associative]] 

\begin{imagefromfile}
  "file_name": "AssociativityDiagram.png",
  "width": 400
\end{imagefromfile}

and such that for each object $x$ there is identity transformation $x \overset{id_X}{\longrightarrow} x$ in that this is a [[neutral element]] for the composition of transformations, whenever defined.

So far this structure is what is called a _[[small category]]_. What makes this a _([[small groupoid|small]]) groupoid_ is that all these transformations are to be "symmetries" in that they are [[invertible morphisms]] meaning that for each transformation $x \overset{f}{\longrightarrow} y$ there is a transformation the other way around $y \overset{f^{-1}}{\longrightarrow} x$ such that

$$
  f^{-1} \circ f  = id_x
  \phantom{AAAA}
  f \circ f^{-1} = id_y
  \,.
$$

If there is only a single object $x$, then this definition reduces to that of a [[group]], and in this sense groupoids are "groups with many objects". Conversely, given any groupoid $\mathcal{G}$ and a choice of one of its objects $x$, then the subcollection of transformations from and to $x$ is a group, sometimes called the [[automorphism group]] $Aut_{\mathcal{G}}(x)$ of $x$ in $\mathcal{G}$.

Just as for groups, the "transformations" above need not necessarily be given by concrete transformations (say by [[bijections]] between [[objects]] which are [[sets]]). Just as for groups, such a concrete realization is always possible, but is an extra choice (called a [[representation]] of the groupoid). Generally one calls these "transformations" _[[morphisms]]_: $x \overset{f}{\longrightarrow} y$ is a morphism with "[[source]]" $x$ and "[[domain]]" $y$.

An archetypical example of a groupoid is the [[fundamental groupoid]] $\Pi_1(X)$ of a [[topological space]]
(def. \ref{FundamentalGroupoid} below, for introduction see [here](Introduction+to+Topology+--+2#Homotopy)): For $X$ a topological space, this is the groupoid whose

* [[objects]] are the points $x \in X$;

* [[morphisms]]  $x \overset{[\gamma]}{\longrightarrow} y$ are the [[homotopy relative boundary]]-[[equivalence classes]] $[\gamma]$ of [[paths]] $\gamma \colon [0,1] \to X$ in $X$, with $\gamma(0) = x$ and $\gamma(1) = y$;

and [[composition]] is given, on representatives, by [[concatenation]] of paths. Here the class of the [[reverse path]] $\bar\gamma \;\colon\; t \mapsto \gamma(1-t)$ constitutes the inverse morphism, making this a groupoid.

If one _chooses_ a point $x \in X$, then the corresponding group at that point is the _[[fundamental group]]_ $\pi_1(X,x) \coloneqq Aut_{\Pi_1(X)}(x)$ of $X$ at that point.

This highlights one of the reasons for being interested in groupoids over groups: Sometimes this allows to avoid unnatural ad-hoc choices and it serves to streamline and simplify the theory.

A [[homomorphism]] between groupoids is the obvious: a [[function]] between their underlying [[objects]] together with a function between their morphisms which respects [[source]] and [[target]] objects as well as [[composition]] and [[identity morphisms]]. If one thinks of the groupoid as a special case of a [[category]], then this is a _[[functor]]_. Between groupoids with only a single object this is the same as a [[group homomorphism]].

For example if $f \;\colon\; X \to Y$ is a [[continuous function]] between topological spaces, then postcomposition of [[paths]] with this function induces a groupoid homomorphism $f_\ast \;\colon\; \Pi_1(X) \longrightarrow \Pi_1(Y)$ between the [[fundamental groupoids]] from above.

Groupoids with groupoid homomorphisms ([[functors]]) between them form a [[category]] [[Grpd]] (def. \ref{1CategoryOfGroupoids} below) which includes the categeory [[Grp]] of [[groups]] as the [[full subcategory]] of the groupoids with a single object. This makes precise how groupoid theory is a generalization of [[group theory]].

However, for groupoids more than for groups one is typically interested in "[[conjugation actions]]" on homomorphisms. These are richer for groupoids than for groups, because one may conjugate with a different morphism at each object. If we think of groupoids as special cases of [[categories]], then these "conjugation actions on homomorphisms" are _[[natural transformations]]_ between [[functors]].

For examples if $f,g \;\colon\; X \longrightarrow Y$ are two [[continuous functions]] between [[topological spaces]], and if $\eta \;\colon\; f \Rightarrow g$ is a [[homotopy]] from $f$ to $g$, then the [[homotopy relative boundary]] classes of the [[paths]] $\eta(x,-) \;\colon\; [0,1] \to Y$ constitute a natural transformation between $f_*, g_\ast \;\colon\; \Pi_1(X) \to \Pi_1(Y) $ in that for all paths $x_1 \overset{[\gamma]}{\longrightarrow} x_2$ in $X$ we have the "conjugation relation"

$$
  [\eta(x_1,-)] \cdot [f\circ\gamma]
  =
  [g \circ \gamma] \cdot [\eta(x_2,-)]
  \phantom{AAAA}
  \text{i.e.}
  \phantom{AAAA}
  \array{
    f(x_1) &\overset{[\eta(x_1,-)]}{\longrightarrow}& g(x_1)
    \\
    {}^{\mathllap{[f \circ \gamma]}}\downarrow && \downarrow^{\mathrlap{[g \circ \gamma]}}
    \\
    f(x_2) &\underset{[\eta(x_2,-)]}{\longrightarrow}& g(x_2)
  }
  \,.
$$

One may take care of the existence of these conjugation actions/natural transformation in two ways:

1. If one quotients them out, i.e. if one identifies two groupoid homomorphisms that differ by a conjugation action, then the resulting [[category]] of groupoids and classes of homomorphisms is called the _[[homotopy category]]_ $Ho(Grpd)$ of [[Grpd]] (def. \ref{HomotopyCategoryOfGroupoids} below). This is [[equivalence of categories|equivalent]] to the [[full subcategory]] of the [[classical homotopy category]] of [[topological spaces]] on those that are ([[CW-complexes]] and) [[homotopy 1-types]], i.e. those for which the [[fundamental groupoid]] is the _only_ homotopy invariant, with all higher [[homotopy groups]] being trivial:

   $$
     Ho(Grpd) \simeq Ho(Top^{CW}_{\leq 1}) \hookrightarrow Ho(Top^{CW})
     \,.
   $$

   This means that the concept of groupoids may be regarded as a combinatorial model for [[homotopy 1-types]] in [[homotopy theory]], in contrast to the models by [[topological spaces]] given by [[topological homotopy theory]]. This equivalence generalizes to [[homotopy n-types]] as one passes to [[n-groupoids]] and eventually to all [[homotopy types]] as one passes to [[infinity-groupoids]].

1. Instead of forgetting all the information encoded in the conjugations/natural transformations, one may also collect it all into the structure of a [[2-category]] [[Grpd]] (in fact a [[(2,1)-category]]). As such this is the sub-2-category of [[Cat]] on those (small) categories all whose morphisms are [[invertible morphism]].

For more introduction on this see at _[[geometry of physics -- homotopy types]]_.

In either of these two cases, beware that the category [[Grp]] of [[groups]] is _not_ a [[full subcategory]] either of the [[homotopy category]] $Ho(Grpd)$ or of the [[(2,1)-category]] [[Grpd]], because conjugation action is is not part of the definition of $Grp$. Instead in [[homotopy theory]] it is _[[pointed object|pointed]]_ one-object groupoids which are equivalent to groups

$$
  Grp \hookrightarrow Grpd^{\ast/}
  \,.
$$

(Even though there is a unique choice of point for a one-object groupoid, the respect for this (unique) choice forces the conjugation actions on groupoids to be trivial. ) This simple statement is in fact a special case of the [[May recognition theorem]] (see [there](Ek-Algebras#MainResult)) which holds for more general [[homotopy types]] and even for [[directed homotopy types]].

The equivalence of groupoids with [[homotopy 1-types]] shows immediately that, with [[homotopy]] taken into accont, the difference between groupoids and groups is rather mild, after all: Every [[groupoid]] is [[equivalence of groupoids|equvalent]] ([[isomorphism|isomorphic]] in $Ho(Grpd)$) to a [[disjoint union]] of groupoids with a single object (prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings} below). In particular [[groupoid representations]] are equivalently just tuples of [[group representations]] (prop. \ref{GroupoidRepresentationsAreProductsOfGroupRepresentations} below.) This is the reason why the competition between [[general topology]] textbooks that do and that do not prefer the [[fundamental groupoid]] over the [[fundamental group]] remains inconclusive.

However, this equivalence of groupoids with disjoint unions of groups depends on the [[axiom of choice]]. Even if this is assumed in the underlying [[foundations]]/[[set theory]], it breaks once one considers groupoids equipped with geometric structure:

Just as one may consider [[topological groups]] and [[Lie groups]], etc., there are the evident concepts of [[topological groupoids]] and [[Lie groupoids]] etc. (generally: _[[internal  groupoids]]_). Their theory turns out to be genuinely richer than that of their group analogs, due to the interaction between the [[geometry]] and the [[homotopy theory]] ("[[higher geometry]]").

The correct concept of homomorphisms between [[Lie groupoids]] for instance goes by many names, including _[[Morita morphisms]]_, _[[Hilsum-Skandalis morphisms]]_ and _[[bibundles]]_. The general way to understand this and all other geometric groupoid theory is via the concept of _[[stacks]] of groupoids_. For more pointers on this see at _[[higher geometry]]_ and for introduction in the case of [[higher differential geometry]] see at _[[geometry of physics -- smooth homotopy types]]_.










## Definition

### Groupoids

+-- {: .num_defn #GroupoidDependentlyTypes}
###### Definition
**(groupoid -- [[dependent type theory|dependently typed]] definition)

A _[[small groupoid]]_ $\mathcal{G}$ is

1. a [[set]] $X$, to be called the _set of [[objects]]_;

1. for all [[pairs]] of objects $(x,y) \in X \times X$ a
   [[set]] $Hom(x,y)$,  to be called the _set of [[morphisms]] with [[domain]] or [[source]] $x$ and [[codomain]] or [[target]] $y$_;

1. for all [[triples]] of objects $(x,y,z) \in X \times X \times X$ a [[function]]

   $$
     \circ_{x,y,z} \;\colon\; Hom(y,z) \times Hom(x,y) \longrightarrow Hom(x,z)
   $$

   to be called _[[composition]]_

1. for all objects $x \in X$ an element

   $$
     id_x \in Hom(x,x)
   $$

   to be called the _[[identity morphism]]_ on $x$;

1. for all pairs $(x,y) \in X \times X$ of objects a function

   $$
     (-)^{-1} \;\colon\; Hom(x,y) \longrightarrow Hom(y,x)
   $$

   to be called the _[[inverse morphism|inverse-assigning]] function_


such that

1. ([[associativity]]) for all [[quadruples]] of objects $x_1, x_2, x_3, x_4 \in X$ and all [[triples]] of morphisms $f \in Hom(x_1,x_2)$, $g \in Hom(x_2,x_3)$ and $h \in Hom(x_3,x_4)$ an [[equality]]

   $$
     h \circ (g \circ f) \;=\; (h \circ g) \circ f
   $$

1. ([[unitality]]) for all [[pairs]] of objects $x,y \in X$ and all moprhisms $f \in Hom(x,y)$ [[equalities]]

    $$
      id_y \circ f = f
      \phantom{AAAA}
      f \circ id_x = f
    $$

1. ([[inverse morphism|invertibility]]) for all pairs of objects $x,y \in X$ and every morphism $f \in Hom(x,y)$ [[equalities]]

   $$
     f^{-1}\circ f = id_{x}
     \phantom{AAAA}
     f \circ f^{-1} = id_y
     \,.
   $$

If $\mathcal{G}_1, \mathcal{G}_2$ are two [[groupoids]], then a _[[homomorphism]]_ or _[[functor]]_ between them, denoted

$$
  F \;\colon\; \mathcal{G}_1 \longrightarrow  \mathcal{G}_2
$$

is

1. a [[function]] $F_0 \;\colon\; X_1 \longrightarrow X_2$ between the respective sets of objects;

1. for each pair $x,y \in X_1$ of objects a function

   $$
    F_{x,y} \;\colon\; Hom_{\mathcal{G}_1}(x,y) \longrightarrow Hom_{\mathcal{G}_2}(F_0(x), F_0(y))
   $$

   between sets of morphisms

such that

1. (respect for composition) for all triples $x,y,z \in X_1$ and all $f \in Hom(x,y)$ and $g \in Hom(y,z)$ an [[equality]]

   $$
    F_{y,z}(g) \circ_2 F_{x,y}(f)  \;=\; F_{x,z}(g\circ_1 f)
   $$

1. (respect for identities) for all $x \in X$ an equality

   $$
     F_{x,x}(id_x) = id_{F_0(x)}
     \,.
   $$

For $\mathcal{G}_1, \mathcal{G}_2$ two groupoids, and for $F,G \;\colon\; \mathcal{G}_1 \to \mathcal{G}_2$ two groupoid homomorphisms/functors, then a _conjugation_ or _[[homotopy]]_ or _[[natural transformation]]_ (necessarily a [[natural isomorphism]])

$$
  \eta \;\colon\; F \Rightarrow G
$$

is

* for each object $x \in X_1$ of $\mathcal{G}_1$ a morphism $\eta_{x} \in Hom_{\mathcal{G}_2}(F(x), G(x))$

such that

* for all $x,y \in X_1$ and $f \in Hom_{\mathcal{G}_1}(x,y)$ an [[equality]]

  $$
    \eta_y \circ_2 F(f)
     =
     G(f) \circ \eta_x
     \phantom{AAAAAA}
     \array{
       F(x) &\overset{\eta_x}{\longrightarrow}& G(x)
       \\
       {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{G(f)}}
       \\
       F(y) &\underset{\eta_y}{\longrightarrow}& G(y)
     }
  $$


For $\mathcal{G}_1, \mathcal{G}_2$  two groupoids and $F, G, H \colon \mathcal{G}_1  \longrightarrow \mathcal{G}_2$
three functors between them and $\eta_1 \;\colon\; F \Rightarrow G$ and $\eta_2 \;\colon\; G \Rightarrow H$
conjugation actions/natural isomorphisms between these, there is the composite

$$
  \eta_2 \circ \eta_1  \;\colon\; F \Rightarrow H
$$

with components the composite of the components

$$
  (\eta_2 \circ \eta_1)(x) \coloneqq \eta_2(x) \circ \eta_1(x)
  \,.
$$

This yields for any two groupoid a _[[hom-groupoid]]_

$$
  Hom_{Grpd}(\mathcal{G}_1, \mathcal{G}_2)
$$

whose objects are the groupoid homomorphisms / functors, and whose morphisms are the conjugation actions / natural transformations.


=--

+-- {: .num_remark}
###### Remark
**([[groupoids]] are special cases of [[categories]])**

A [[small groupoid]] (def. \ref{GroupoidDependentlyTypes}) is equivalently a [[small category]] in which all [[morphisms]] are [[isomorphism|isomorphisms]].

While therefore groupoid theory may be regarded as a special case of [[category theory]], it
is noteworthy that the two theories are quite different in character. For example [[higher groupoid]]
theory is _[[homotopy theory]]_ which is rich but quite tractable, for instance via tools
such as [[simplicial homotopy theory]] or [[homotopy type theory]], while [[higher category theory]]
is intricate and becomes tractable mostly by making recourse to higher groupoid theory in the guise of
[[(infinity,1)-category theory]] and [[(infinity,n)-categories]].

=--


+-- {: .num_defn #GroupoidGlobalDefinition}
###### Definition
**(groupoid -- global definition)**

A _[[small groupoid]]_ $\mathcal{G}$ is

1. a [[set]] $G_0$ called its _set of [[objects]]_;

1. a [[set]] $G_1$ called its _set of [[morphisms]]_ or _set of arrows_

1. a [[pair]] of [[functions]]

   $$
     s, t \;\colon\; G_1 \rightrightarrows G_0
   $$

   called _[[source]]_ and _[[target]]_ or _[[domain]]_ and _[[codomain]]_

   (an element $g\in G_1$ is denoted by $s(g) \overset{g}{\longrightarrow} t(g)$);

1. a multiplication or _[[composition]]_ map $m \colon G_1 \times_{s, G_0, t} G_1 \to G_1$, usually denoted as $g h$ for $m(g,h)$, which satisfies

   1. $s(g h)=s(h)$, $t(g h)=t(g)$, and

   1. [[associativity]]: $(g h)k=g(h k)$,

   1. identity section: $e: G_0\to G_1$, such that $e(t(g))g=g=ge(s(g))$ (in particular, $s\circ e= t \circ e$),

   1. [[inverse]], $i: G_1 \to G_1$, also denoted by $i(g)=g^{-1}$, such that for all $g\in G$,

      $ g^{-1} g = e(s(g)), \quad g g^{-1} = e(t(g)). $

=--



+-- {: .num_remark}
###### Remark
**(Notation and Terminology)**

If $x,y$ are [[objects]] (also called [[vertices]]) of the groupoid $G$ then the set of [[morphisms]] (also called arrows) from $x$ to $y$ is written $G(x,y)$, or other notations for [[hom-sets]].  The set $G(x,x)$ (which is a [[group]] under composition) is also written $G(x)$ and called the _vertex group_ of $G$ at $x$.  It is also written $Aut_G(x)$ and called the [[automorphism group]] of $x$ in $G$, or written $\pi_1(G,x)$ and called the [[fundamental group]] of $G$ at $x$ (especially if you think of a groupoid as giving a [[homotopy 1-type]]).

As in any [[category]], there is a question of notation for the [[composition]], and in particular of the order in which to write things. It can be more convenient to write the composition of $a:x \to y$ and $b: y \to z$ as $a b:x \to z$, although a more traditional notation would be $b a$.  The two conventions can be distinguished by writing $a; b$ or $b\circ a$ (which is the most traditional notation for categories).  See [[composition]] for further discussion.

A groupoid $G$ is _[[connected groupoid|connected]]_, or _[[transitive groupoid|transitive]]_, if $G(x,y)$ is nonempty for all $x,y \in Ob(G)$; it is called _[[inhabited groupoid|inhabited]]_, or _nonempty_, if it has at least one object. A [[maximal element|maximal]] inhabited connected [[subgroupoid]] of $G$ is called a _component_ of $G$, and $G$ is then the [[disjoint union]] (the [[coproduct]] in $\Grpd$) of its connected components. The set of components of $G$ is written $\pi_0(G)$ (especially if you think of a groupoid as giving a [[homotopy 1-type]]).


=--

+-- {: .num_defn}
###### Definition
**(tame groupoids)**

A groupoid is called **tame** if its [[groupoid cardinality]] is finite.

=--



### Categories of groupoids
 {#CategoriesOfGroupoids}


+-- {: .num_prop #1CategoryOfGroupoids}
###### Remark
**([[1-category]] of [[groupoids]])**

From def. \ref{GroupoidDependentlyTypes} we see that there
is a [[category]] whose

* [[objects]] are the small groupoids;

* [[morphisms]] are the groupoid homomorphisms ([[functors]]).

=--

But since this [[1-category]] does not reflect the existence of [[homotopies]]/[[natural isomorphisms]]
between homomorphsims/[[functors]] of groupoids (def. \ref{GroupoidDependentlyTypes})
this [[1-category]] is not what one is interested in when considering [[homotopy theory]]/[[higher category theory]].

In order to obtain the right notion of category of groupoids
that does reflect homotopies, we first consider now the _horizontal_ composition of homotopies/natural transformations.

+-- {: .num_lemma #HmotopiesWithMorphismsHorizontaComposition}
###### Lemma
**([[horizontal composition]] of [[homotopies]] with [[morphisms]])**

Let $\mathcal{G}_1$, $\mathcal{G}_2$, $\mathcal{G}_3$, $\mathcal{G}_4$ be groupoid and let

$$
  \mathcal{G}_1
    \overset{F_1}{\longrightarrow}
  \mathcal{G}_2
    \underoverset
      {\underset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}F^{'}_2\phantom{AA}}{\longrightarrow}}
      {\Downarrow{\mathrlap{\eta}}}
  \mathcal{G}_3
    \overset{F_3}{\longrightarrow}
  \mathcal{G}_4
$$

be morphisms and a homotopy $\eta$. Then there is a homotopy

$$
  \mathcal{G}_1
  \phantom{AAAA}
    \underoverset
      {\underset{F_3 \circ F_2\circ F_1}{\longrightarrow}}
      {\overset{F_3 \circ F^{'}_2\circ F_1}{\longrightarrow}}
      {\Downarrow{\mathrlap{ F_3 \cdot \eta_ \cdot F_1 }}}
  \phantom{AAAA}\mathcal{G}_2
$$

between the respective composites, with components given by

$$
  (F_3 \cdot \eta \cdot F_1)(x)
    \;\coloneqq\;
  F_3(\eta(F_1(x)))
  \,.
$$

This operation constitutes a groupoid homomorphism/functor

$$
  F_3\cdot (-)\cdot F_1
    \;\colon\;
  Hom_{Grpd}(\mathcal{G}_2, \mathcal{G}_3)
    \longrightarrow
  Hom_{Grp}(\mathcal{G}_1, \mathcal{G}_4)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The respect for identities is clear. To see the respect for composition, let

$$
  \mathcal{G}_2
  \array{
     \overset{F}{\longrightarrow}
     \\
     \Downarrow \eta_1
     \\
     \overset{G}{\longrightarrow}
     \\
     \Downarrow \eta_2
     \\
     \underset{H}{\longrightarrow}
  }
  \mathcal{G}_3
$$

be two composable homotopies. We need to show that

$$
  F_3 \cdot (\eta_2 \circ \eta_1) \cdot F_1
  =
  ( F_3 \cdot \eta_2 \cdot F_1 ) \circ ( F_3 \cdot \eta_1 \cdot F_1 )
  \,.
$$

Now for $x$ any object of $\mathcal{G}_1$ we find

$$
  \begin{aligned}
    (F_3 \cdot (\eta_2 \circ \eta_1) \cdot F_1)(x)
      & \coloneqq
    F_2((\eta_2 \circ \eta_1)(F_1(X)))
      \\
      & \coloneqq
   F_3( \eta_2(F_1(x)) \circ \eta_1 (F_1(x)))
     \\
     &=
    F_2( \eta_2(F_1(x)) ) \circ F_2( \eta_1(F_1(X)) )
      \\
     & =
    (( F_3 \cdot \eta_2 \cdot F_1 ) \circ ( F_3 \cdot \eta_1 \cdot F_1 ))(x)
  \end{aligned}
  \,.
$$

Here all steps are unwinding of the definition of horizontal and of ordinary (vertical)
composition of homotopies, except the third equality, which is the functoriality of $F_2$.

=--

+-- {: .num_lemma #GroupoidHomotopyHorizontalComposition}
###### Lemma
**([[horizontal composition]] of [[homotopies]])

Consider a [[diagram]] of [[groupoids]], groupoid homomorphsims (functors) and homotopies (natural transformations) as follows:

$$
  \mathcal{G}_1
    \underoverset
       {\underset{\phantom{AA}F'_1\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_1\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_1}}
  \mathcal{G}_2
    \underoverset
       {\underset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_2}}
  \mathcal{G}_3
$$

The _[[horizontal composition]]_ of the homotopies to a single homotopy of the form

$$
  \mathcal{G}_1
     \underoverset
       {\underset{F'_2 \circ F'_1}{\longrightarrow}}
       {\overset{F_2\circ F_1}{\longrightarrow}}
       {\Downarrow \eta_2 \cdot \eta_1}
  \mathcal{G}_3
$$

may be defined in temrs of the horizontal composition of homotopies with morphisms (lemma \ref{HmotopiesWithMorphismsHorizontaComposition}) and the ("vertical") composition of homotopies with themselves, in two different ways, namely by decomposing the above diagram as


$$
  \array{
  \mathcal{G}_1
    \underoverset
       {\underset{\phantom{AA}F'_1\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_1\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_1}}
  \mathcal{G}_2
    \underoverset
       {}
       {\overset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
       {}
  \mathcal{G}_3
  \\
  \mathcal{G}_1
    \underoverset
       {\underset{\phantom{AA}F'_1\phantom{AA}}{\longrightarrow}}
       {}
       {}
  \mathcal{G}_2
    \underoverset
       {\underset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_2}}
  \mathcal{G}_3
  }
$$

or as

$$
  \array{
  \mathcal{G}_1
    \underoverset
       {}
       {\overset{\phantom{AA}F_1\phantom{AA}}{\longrightarrow}}
       {}
  \mathcal{G}_2
    \underoverset
       {\underset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_2}}
  \mathcal{G}_3
  \\
  \mathcal{G}_1
    \underoverset
       {\underset{\phantom{AA}F'_1\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_1\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_1}}
  \mathcal{G}_2
    \underoverset
       {\underset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
       {}
       {}
  \mathcal{G}_3
  }
$$

In the first case we get

$$
  \eta_2 \cdot \eta_1
  \;\coloneqq\;
  (\eta_2 \cdot F'_1) \circ (F_2 \cdot \eta_1)
$$

while in the second case we get

$$
  \eta_2 \cdot \eta_1
   \;\coloneqq\;
   ( F'_2 \cdot \eta_1 ) \circ (\eta_2 \cdot F_1)
  \,.
$$

These two definitions coincide.

=--

+-- {: .proof}
###### Proof

For $x$ an object of $\mathcal{G}_1$, then we need that the following square [[diagram]] [[commuting diagram|commutes]] in $\mathcal{G}_3$

$$
  \array{
    F_2(F_1(x))
      &\overset{ (F_2\cdot \eta_1)(x) }{\longrightarrow}& F_2(F'_1(x))
    \\
    {}^{\mathllap{ (\eta_2 \cdot F_1)(x) }}\downarrow
      &&
    \downarrow^{\mathrlap{ (\eta_2\cdot F'_1)(x) }}
    \\
    F'_2(F_1(x))
      & \underset{ (F'_2 \cdot \eta_1)(x) }{\longrightarrow} &
    F'_2(F'_1(y))
  }
   \phantom{AAAA} = \phantom{AAAA}
  \array{
    F_2(F_1(x)) &\overset{F_2(\eta_1(x))}{\longrightarrow}& F_2(F'_1(x))
    \\
    { }^{\mathllap{\eta_2(F_1(x))}}\downarrow
      &&
    \downarrow^{\mathrlap{ \eta_2(F'_1(x)) }}
    \\
    F'_2(F_1(x))
      & \underset{F'_2(\eta_1(x))}{\longrightarrow} &
    F'_2(F'_1(y))
  }
  \,.
$$

But the ommutativity of the square on the right is the defining compatibility condition on the components of $\eta_2$ applied to the morphism $\eta_1(x)$ in $\mathcal{G}_2$.

=--


+-- {: .num_prop #HorizontalCompositionWithHomotopyIsNaturalTransformation}
###### Proposition
**([[horizontal composition]] with [[homotopy]] is [[natural transformation]])**

Consider groupoids, homomorphisms and homotopies of the form

$$
  \mathcal{G}_1
    \underoverset
       {\underset{F'_1}{\longrightarrow}}
       {\overset{F_1}{\longrightarrow}}
       {\Downarrow \eta_1}
  \mathcal{G}_2
  \phantom{AAAAAAA}
  \mathcal{G}_3
    \underoverset
       {\underset{F'_3}{\longrightarrow}}
       {\overset{F_3}{\longrightarrow}}
       {\Downarrow \eta_3}
  \mathcal{G}_4
  \,.
$$

Then horizontal composition with the homotopies (lemma \ref{GroupoidHomotopyHorizontalComposition})
constitutes a [[natural transformation]] between the functors of horizontal composition with morphisms (lemma \ref{HmotopiesWithMorphismsHorizontaComposition})

$$
  ( \eta_3\cdot (-)\cdot \eta_1 )
    \;\colon\;
  ( F_3 \cdot (-)\cdot F_1 )
    \;\Rightarrow\;
  (  F'_3 (-) \cdot  F'_1 )
  \;\colon\;
    Hom_{Grpd}(\mathcal{G}_2,\mathcal{G}_3)
      \longrightarrow
    Hom_{Grpd}(\mathcal{G}_1, \mathcal{G}_4)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{GroupoidHomotopyHorizontalComposition}.

=--

It first of all follows that the following makes sense

+-- {: .num_defn #HomotopyCategoryOfGroupoids}
###### Definition
**([[homotopy category]] of groupoids)**

There is also the [[homotopy category]] $Ho(Grpd)$ whose

* [[objects]] are small groupoids;

* [[morphisms]] are [[equivalence classes]] of groupoid homomorphisms modulo homotopy (i.e. [[functors]] modulo [[natural transformations]]).

This is usually denoted $Ho(Grpd)$.

=--

Of course what the above really means is that, without quotienting out homotopies,
groupoids form a [[2-category]], in fact a [[(2,1)-category]], in fact an [[enriched category]]
which is enriched over the naive 1-category of groupoids from remark \ref{1CategoryOfGroupoids},
hece a [[strict 2-category]] with [[hom-groupoids]].


### Equivalences of groupoids

+-- {: .num_defn #EquivalenceOfGroupoids}
###### Definition
**([[equivalence of groupoids]])**

Given two groupoids $\mathcal{G}_1$ and $\mathcal{G}_2$, then a homomorphism

$$
  F\;\colon\; \mathcal{G}_1 \longrightarrow \mathcal{G}_2
$$

is an _[[equivalence of groupoids|equivalence]]_ if it is an [[isomorphism]]
in the [[homotopy category]] $Ho(Grpd)$ (def. \ref{HomotopyCategoryOfGroupoids}), hence if there exists a homomorphism the
other way around

$$
  G \;\colon\; \mathcal{G}_2 \longrightarrow \mathcal{G}_1
$$

and a homotopy/natural transformations of the form

$$
  G \circ F \simeq id_{\mathcal{G}_1}
  \phantom{AAAA}
  F \circ G \simeq id_{\mathcal{G}_2}
  \,.
$$

=--


+-- {: .num_defn #GroupoidConnectedComponents}
###### Definition
**([[connected components]] of a groupoid)**

Given a [[groupoid]] $\mathcal{G}$ with set of objects $X$, then the [[relation]] "there exists a morphism from $x$ to $y$", i.e.

$$
  (x\sim y)
  \;\coloneqq\;
  \left( Hom(x,y) \neq \emptyset \right)
$$

is clearly an [[equivalence relation]] on $X$. The corresponding set of [[equivalence classes]] is denoted

$$
  \pi_0(\mathcal{G})
$$

and called the set of _[[connected components]]_ of $\mathcal{G}$.

=--


+-- {: .num_defn #InGrupoidAutomorphismGroup}
###### Definition
**([[automorphism groups]])

Given a [[groupoid]] $\mathcal{G}$ and an object $x$, then under composition the set $Hom_{\mathcal{G}}(x,x)$ forms a [[group]]. This is called the _[[automorphism group]]_ $Aut_{\mathcal{G}}(x)$ or _vertex group_ or _isotropy group_ of $x$ in $\mathcal{G}$.

=--


+-- {: .num_prop #GroupoidWeakHomotopyEquivalence}
###### Definition
**([[weak homotopy equivalence]] of [[groupoids]])

Let $\mathcal{G}_1$ and $\mathcal{G}_2$ be groupoids. Then a morphism (functor)

$$
  F \;\colon\; \mathcal{G}_1 \longrightarrow \mathcal{G}_2
$$

is called a _[[weak homotopy equivalence]]_ if

   1. it induces a [[bijection]] on [[connected components]] (def. \ref{GroupoidConnectedComponents}):

      $$
        \pi_0(F) \;\colon\; \pi_0(\mathcal{G}_1) \overset{\simeq}{\longrightarrow} \pi_0(\mathcal{G}_2)
      $$

   1. for each object $x$ of $\mathcal{G}_1$ the morphism

      $$
        F_{x,x} \;\colon\; Aut_{\mathcal{G}_1}(x) \overset{\simeq}{\longrightarrow} Aut_{\mathcal{G}_2}(F_0(x))
      $$

      is an [[isomorphism]] of [[automorphism groups]] (def. \ref{InGrupoidAutomorphismGroup})

=--


### Groupoid representations


+-- {: .num_defn #GroupoidRepresentation}
###### Definition
**([[groupoid representation]])

Let $\mathcal{G}$ be a [[groupoid]]. Then:

A [[linear representation]] of $\mathcal{G}$ is a groupoid homomorphism ([[functor]])

$$
  \rho \;\colon\; \mathcal{G} \longrightarrow Core(Vect)
$$

to the groupoid [[core]] of the category [[Vect]] of [[vector spaces]] (example \ref{CoreGroupoid}). Hence this is

1. For each object $x$ of $\mathcal{G}$ a [[vector space]] $V_x$;

1. for each morphism $x \overset{f}{\longrightarrow} y$ of $\mathcal{G}$ a
   [[linear map]] $\rho(f) \;\colon\; V_x \to V_y$

such that

1. (respect for composition) for all composable morphisms $x \overset{f}{\to}y \overset{g}{\to} z$ in the
   groupoid we have an [[equality]]

   $$
     \rho(g) \circ \rho(f) = \rho(g \circ f)
   $$

1. (respect for identities) for each object $x$ of the groupoid we have an equality

   $$
     \rho(id_x) = id_{V_x}
     \,.
   $$

Similarly a _[[permutation representation]]_ of $\mathcal{G}$ is a groupoid homomorphism ([[functor]])

$$
  \rho \;\colon\; \mathcal{G} \longrightarrow Core(Set)
$$

to the groupoid core of [[Set]]. Hence this is

1. For each object $x$ of $\mathcal{G}$ a [[set]] $S_x$;

1. for each morphism $x \overset{f}{\longrightarrow} y$ of $\mathcal{G}$ a
   [[function]] $\rho(f) \;\colon\; S_x \to S_y$

such that composition and identities are respected, as above.

For $\rho_1$ and $\rho_2$ two such representations, then a homomorphism of representations

$$
  \phi \;\colon\; \rho_1 \longrightarrow \rho_2
$$

is a [[natural transformation]] between these functors, hence is

* for each object $x$ of the groupoid a (linear) function

  $$
    (V_1)_x \overset{\phi(x)}{\longrightarrow} (V_2)_x
  $$

* such that for all morphisms $x \overset{f}{\longrightarrow} y$
  we have

  $$
    \phi(y) \circ \rho_1(f) = \rho_2(x) \circ \phi(x)
    \phantom{AAAAAA}
    \array{
      (V_1)_x &\overset{\phi(x)}{\longrightarrow}& (V_2)_x
      \\
      {}^{\mathllap{\rho_1(f)}}\downarrow && \downarrow^{\mathrlap{\phi_2(f)}}
      \\
      (V_1)_y &\underset{\phi(y)}{\longrightarrow}& (V_2)_y
    }
  $$

Representations of $\mathcal{G}$ and homomorphisms between them constitute a [[category]],
called the [[representation category]] $Rep_{Grpd}(\mathcal{G})$.

=--



## Examples


+-- {: .num_example #FundamentalGroupoid}
###### Example
**([[fundamental groupoid]])**

Let $X$ be a [[topological space]]. For $x,y \in X$ two points, write $P_{x,y}X$
for the set of [[paths]] in $X$ from $x$ to $y$. Consider the [[equivalence relation]]
"[[homotopy relative boundary]]" on this set and write

$$
  Hom(x,y) \coloneqq (P_{x,y}X)/\simeq
$$

for the set of [[equivalence classes]] under this relation. The [[concatenation of paths]]
descends to these equivalence classes. This yields a groupoid with set of objects the set $X$
of points in the topological space. This is the called the _[[fundamental groupoid]]_ $\Pi_1(X)$
of $X$.

This construction extends to a [[functor]]

$$
   \Pi_1 \;\colon\; Top \longrightarrow Grpd_1
$$

from the [[1-category]] [[Top]] to the [[1-category]] [[Grpd]]. In fact it extends to a functor

$$
  \Pi_1 \;\colon\; Ho(Top) \longrightarrow Ho(Grpd)
$$

on [[homotopy categories]].


=--



+-- {: .num_example #FundamentalGroupoid2Functor}
###### Example
**([[(2,1)-functor|(2,1)-functoriality]] of [[fundamental groupoid]])

If $X$ and $Y$ are [[topological spaces]] and $f \;\colon\; X \longrightarrow Y$
is a [[continuous function]] between them, then this induces a groupoid homomorphism (functor)
between the respective [[fundamental groupoids]] (def. \ref{FundamentalGroupoid})

$$
  F_f \;\colon\; \Pi_1(X) \longrightarrow \Pi_1(Y)
$$

given on objects by the underlying function of $f$

$$
  (F_f)_0 \coloneqq f
$$

and given on the class of a [[path]] by the evident postcomposition with $f$

$$
  (F_f)_{x,y}
    \;\colon\;
  (x \overset{[\gamma]}{\longrightarrow} y)
    \;\mapsto\;
  (f(x) \overset{[f \circ \gamma]}{\longrightarrow} f(y) )
  \,.
$$

This construction clearly respects [[identity morphisms]] and [[composition]] and hence is
itself a [[functor]] of the form

$$
  \Pi_1 \;\colon\; Top \longrightarrow Grpd_1
$$

from the [[category]] [[Top]] of [[topological  space]] to the [[1-category]] [[Grpd]] of groupoids.

But more is true: If $f,g \;\colon\; X \longrightarrow Y$ are two [[continuous function]] and

$$
  \eta \;\colon\; f \Rightarrow g
$$

is a [[left homotopy]] between them, hence a continuous function

$$
  \eta \;\colon\; X \times [0,1] \longrightarrow Y
$$

such that $\eta(-,0) = f$ and $\eta(-,1) = g$, then this induces a homotopy between the above groupoid homomorphisms
(a natural transformation of functors).

This shows that the fundamental groupoid functor in fact descends to [[homotopy categories]]

$$
  \Pi_1 \;\colon\; Ho(Top) \longrightarrow Ho(Grpd)
  \,.
$$

(In fact this means it even extends to a [[(2,1)-functor]] from the [[(2,1)-category]]
of topological spaces, continuous functions, and [[higher homotopy]]-classes of left homotopues,
to that of groupoids.)

As a direct consequence it follows that if there is a [[homotopy equivalence]]

$$
  X \simeq_h Y
$$

between [[topological spaces]], then there is an induced [[equivalence of groupoids]]
betwee their [[fundamental groupoids]]

$$
  \Pi_1(X) \simeq \Pi_1(Y)
  \,.
$$

Hence the [[fundamental groupoid]] is a _[[homotopy invariant]]_ of topological spaces.
Of course by prop. \ref{DeloopingGroupoidEquivalence} the fundamental groupoid is
equivalent, as a groupoid, to the disjoint union of the [[deloopings]] of
all the [[fundamental groups]] of the given topological spaces, one for each [[connected component]],
and hence this is equivalently the statement that the set of connected components
and the fundamental groups of a topological space are homotopy invariants.

=--


+-- {: .num_example #DiscreteGroupoid}
###### Example
**([[discrete groupoid]])**

For $X$ any set, there is the _[[discrete groupoid]]_ $Disc(X)$, whose set of objects
is $X$ and whose only morphisms are [[identity morphisms]].

This is also the  [[fundamental groupoid]] (example \ref{FundamentalGroupoid})
of the [[discrete topological space]] on the set $X$.

=--

+-- {: .num_example #CodiscreteGroupoid}
###### Example
**([[codiscrete groupoid]])**

For $X$ any set, there is the _[[codiscrete groupoid]]_ $Codisc(X)$, whose set of objects
is $X$ and whose homsets are singletons. In other words, it is a groupoid where every object is uniquely isomorphic to every object.

=--

+-- {: .num_example #GroupoidFromDelooping}
###### Example
**([[delooping]] of a  [[group]])**

Let $G$ be a [[group]]. Then there is a groupoid, denoted $B G$, with a single object $p$, with morphisms

$$
  Hom_{B G}(p,p) \coloneqq G
$$

the elements of $G$, with composition the multiplication in $G$, with identity morphism the [[neutral element]] in $G$ and with inverse morphisms the inverse elements in $G$.

This is also called the _[[delooping]]_ of $G$ (because the [[loop space object]] of $B G$ at the unique point is the given group:
$\Omega B G \simeq G$).

For $G_1, G_2$ two groups, then there is a [[natural bijection]] between [[group homomorphisms]]
$\phi \colon G_1 \to G_2$ and groupoid homomorphisms $G G_1 \to B_ G_2$: the latter are all of the form
$B \phi$, with $(B \phi)_0$ uniquely fixed and $(B \phi)_{p,p} = \phi$.

This means that the construction $B(-)$ is a  [[fully faithful functor]]

$$
  B(-) \;\colon\; Grp \hookrightarrow Grpd_1
$$

into from the category [[Grp]] of groups to the [[1-category]] of [[groupoids]].

But beware that this functor is not fully faithful when homotopies of groupoids are taken into acount,
because there are in general non-trivial homotopies between morphims of the form

$$
  B \phi_1, B \phi_2
  \;\colon\;
  B G \longrightarrow B H
$$

By definition, such a homotopy (natural transformation) $\eta \;\colon\; B \phi_1 \Rightarrow B \phi_2$
is a choice of a single elemet $\eta_p \in H$ such that for all $g \in G$
we have

$$
  \phi_2(g) = h \cdot \phi_1(g) \cdot h^{-1}
  \phantom{AAAAAAAAA}
  \array{
    p &\overset{h}{\longrightarrow}& p
    \\
    {}^{\mathllap{\phi_1(g)}}\downarrow && \downarrow^{\mathrlap{\phi_2(g)}}
    \\
    p &\underset{h}{\longrightarrow}& p
  }
$$

hence such that

$$
  \phi_2 = Ad_h \circ \phi_1
  \,.
$$

Therefore notably the induced functor

$$
  B(-) \;\colon\; Grp \longrightarrow Ho(Grp)
$$

to the [[homotopy category]] of groupoids is not fully faithful.

But since $B G$ is canonically a [[pointed object]] in groupoids, we may also regard [[delooping]]
as a functor

$$
  B(-) \;\colon\; Grp \longrightarrow Grpd^{\ast/}
$$

to the [[category of pointed objects]] of [[Grpd]]. Since groupoid homomorphisms $B G_1 \to B G_2$
necessarily preserve the basepoint, this makes no difference at this point. But as we now
pass to the [[homotopy category]]

$$
  B(-) \;\colon\; Grp \hookrightarrow Ho(Grpd^{\ast/})
$$

then also the homotopies are required to preserve the basepoint, and for
homotopies between homomorphisms between delooped groups this means, since there only
is a single point, that these homotopies are all trivial. Hence regarded this way
the functor is a [[fully faithful functor]] again, hence an [[equivalence of categories]]
onto its [[essential image]]. By prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings} below
this essential image consists precisely of the (pointed) [[connected object|connected]] groupoids:

_Groups are equivalently pointed connected groupoids_.

=--


+-- {: .num_example #GroupoidsCoproduct}
###### Example
**([[disjoint union]]/[[coproduct]] of groupoids)

Let $\{\mathcal{G}_i\}_{i \in I}$ be a [[set]] of groupoids. Then their [[disjoint union]] ([[coproduct]]) is the groupoid

$$
  \underset{i \in I}{\sqcup} \mathcal{G}_i
$$

whose set of objects is the disjoint union of the sets of objects of the summand groupoids, and whose sets of morphisms between two objects is that of $\mathcal{G}_i$ if both objects are form this groupoid, and is [[empty set|empty]] otherwise.

=--


+-- {: .num_example #DeloopingGroupoidDisjointUnion}
###### Example
**([[disjoint union]] of [[delooping]] groupoids)

Let $\{G_i\}_{i \in I}$ be a [[set]] of [[groups]]. Then there is a groupoid
$\underset{i \in I}{\sqcup} B G_i$ which is the disjoint union groupoid (example \ref{GroupoidsCoproduct}) of the [[delooping]] groupoids $B G_i$ (example \ref{GroupoidFromDelooping}).

Its set of objects is the index set $I$, and

$$
  Hom(i,j)
   =
  \left\{
    \array{
      G_i &\vert& i = j
      \\
      \emptyset &\vert& \text{otherwise}
    }
  \right.
$$

=--

+-- {: .num_example #CoreGroupoid}
###### Example
**(groupoid [[core]] of a [[category]])**

For $\mathcal{C}$ any ([[small category|small]]) [[category]], then there is a maximal groupoid inside

$$
  Core(\mathcal{C}) \hookrightarrow \mathcal{C}
$$

sometimes called the _[[core]]_ of $\mathcal{C}$. This is obtained from $\mathcal{C}$
simply by discarding all those [[morphisms]] that are not [[isomorphisms]].

For instance

* For $\mathcal{C} = $ [[Set]] then $Core(Set)$ is the goupoid of [[sets]] and [[bijections]] between them.

  For $\mathcal{C}  $ [[FinSet]] then the [[skeleton]] of this groupoid (prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}) is the disjoint union of deloopings (example \ref{DeloopingGroupoidDisjointUnion}) of all the [[symmetric groups]]:

  $$
    Core(FinSet) \simeq \underset{n \in \mathbb{N}}{\sqcup} \Sigma(n)
  $$

* For $\mathcal{C} = $ [[Vect]] then $Core(Vect)$ is the groupoid of [[vector spaces]] and [[linear map|linear]] [[bijections]] between them.

  For $\mathcal{C} = $ [[FinVect]] then the [[skeleton]] of this groupoid is the disjoint union of delooping of all the
  [[general linear groups]]

  $$
    Core(FinVect) \simeq \underset{n \in \mathbb{N}}{\sqcup} GL(n)
    \,.
  $$

=--


+-- {: .num_example #GroupoidRepresentationOfDeloopingGroupoid}
###### Example
**([[groupoid representation]] of [[delooping groupoid]] is [[group representation]])

If $B G$ is the [[delooping groupoid]] of a [[group]] $G$ (example \ref{GroupoidFromDelooping}),
then a [[groupoid representation]] of $B G$ according to def. \ref{GroupoidRepresentation} is
equivalently a [[group representation]] of the group $G$:

$$
  Rep_{Grpd}(B G) \simeq Rep(G)
  \,.
$$

=--

$\,$

> Here is some further examples that should be merged into the above text.



3. From any [[group action|action]] of a [[group]] $H$ on a [[set]] $X$ we obtain an [[action groupoid]] or "[[weak quotient]]" $X/ \!\! /H$. This is also written $X \rtimes H$, a semidirect product, since it is a special case of the semidirect product of an action of a groupoid on a groupoid.  If $X=\{*\}$ this gives the groupoid $\mathbf{B}H$, above.

4. A [[setoid]], that is a set $X$ equipped with an [[equivalence relation]] $E$, becomes a groupoid with the multiplication $(x,y);(y,z) = (x,z)$ for all $(x,y), (y,z) \in E$.  (This gives one reason for the forward notation for composition.)  Such a groupoid is equivalent to the [[discrete category]] on the [[quotient set]] $X/E$.

5. In particular, if $E$ is the universal relation $X \times X$, then we get the _[[square groupoid]]_ $X^2$, also called the _[[trivial groupoid]]_ on $X$. Despite the latter name, there is an important special case, namely the groupoid $I= \{0,1\}^2$. This groupoid has non-identity elements $\iota:0 \to 1, \iota^{-1}: 1 \to 0$, and can be regarded as a groupoid model of the unit [[interval]] $[0,1]$ in [[topology]].

6. More generally, if we choose some [[subset]] $S$ of the points of a space $X$, then we have a [[full subcategory|full subgroupoid]] of $\pi_1(X)$ containing only those points in $S$, denoted $\pi_1(X,S)$.  This can result in much more manageable groupoids; for instance $\Pi_1([0,1],\{0,1\})$ is the groupoid $I$ considered above, while $\Pi_1([0,1])$ has [[uncountable set|uncountably]] many objects (but is [[equivalence of categories|equivalent]] to $I$).

7. If $\Gamma$ is a [[directed graph]] or [[quiver]], then the _[[free groupoid]]_ $F(\Gamma)$ is well defined. It is the left [[adjoint functor]] to the [[forgetful functor]] from groupoids to directed graphs. This shows an advantage of groupoids: the notion of _free equivalence relation_ or _free action groupoid_ does not easily make sense. But we can still talk of a presentation of an equivalence relation or action groupoid by [[generators and relations]], by considering presentations of groupoids instead.

   +-- {: .query}
   [[Mike Shulman|Mike]]: It's not clear to me that the notion of "free equivalence relation" doesn't make sense.  Can't I talk about a left adjoint to the forgetful functor from equivalence relations to, say, directed graphs?  Maybe sets-equipped-with-a-binary-relation would be more appropriate, but either one works fine.

   [[Ronnie Brown|Ronnie]]: Are you sure this forgetful functor equivalence relations to directed graphs has a left adjoint? Suppose the directed graph $\Gamma$ has one vertex $x$ and one loop $u:x  \to x$. The free groupoid on $\Gamma$ is the group of integers, which as a groupoid is not an equivalence relation.

   _Toby_:  But there is still a free [[setoid]] (set equipped with an equivalence relation) on $\Gamma$; it is the [[point]].  As a groupoid, it is not the same as the free groupoid on $\Gamma$, although it *is* the same as the free setoid on the free groupoid on $\Gamma$.  If there\'s an advantage to working with groupoids, perhaps it\'s that the free groupoid functor preserves distinctions that the free setoid functor forgets?  (In this case, a distinction preserved or forgotten is that between $\Gamma$ and the point, which as a graph does not have $u$.)
   =--

8. A [paper by &#381;ivaljevi&#263;](#Zivaljevic) gives examples of groupoids used in combinatorics.

9. The book "Topology and Groupoids" listed below takes the view that 1-dimensional homotopy theory, including the Seifert-van Kampen Theorem, the theory of covering spaces, and the less well known theory of the fundamental group(oid) of an orbit space by a discontinuous group action, is best presented using the notion of groupoid rather than group as basic. This had led in the 1960s to the question of the prospective use of (strict) groupoids in higher homotopy theory. One answer is given in the book _[[Nonabelian algebraic topology]]_.


## Properties
 {#Properties}

### Equivalences of groupoids
 {#PropertiesEquivalencesOfGroupoids}

+-- {: .num_lemma #AutomorphismGroupDependsOnlyOnConnectedComponent}
###### Lemma
**([[automorphism group]] depends on basepoint only up to [[conjugation]])**

For $\mathcal{G}$ a groupoid, let $x$ and $y$ be two [[objects]] in the
same [[connected component]] (def. \ref{GroupoidConnectedComponents}). Then there is a group [[isomorphism]]

$$
  Aut_{\mathcal{G}}(x) \simeq Aut_{\mathcal{G}}(y)
$$

between their [[automorphism groups]] (def. \ref{InGrupoidAutomorphismGroup}).

=--

+-- {: .proof}
###### Proof

By assumption, there exists some morphism from $x$ to $y$

$$
  x \overset{f}{\longrightarrow} y
  \,.
$$

The operation of [[conjugation]] with this morphism

$$
  \array{
     Aut_{\mathcal{G}}(x)
       &\overset{Ad_{f}}{\longrightarrow}&
     Aut_{\mathcal{G}}(y)
     \\
     g &\mapsto& f^{-1} \circ g \circ f
  }
$$

is clearly a group isomorphism as required.

=--

+-- {: .num_lemma #DeloopingGroupoidEquivalence}
###### Lemma
**([[equivalence of groupoids|equivalences]] between [[coproducts|disjoint unions]] of [[delooping groupoids]])**

Let $\{G_i\}_{i \in I}$ and $\{H_j\}_{j \in J}$ be sets of [[groups]] and consider a homomorphism ([[functor]])

$$
  F
    \;\colon\;
  \underset{i \in I}{\sqcup} G_i
    \longrightarrow
  \underset{j \in J}{\sqcup} H_j
$$

between the corresponding disjoint unions of [[delooping groupoids]] (example \ref{GroupoidFromDelooping}).

Then the following are equivalent:

1. $F$ is an [[equivalence of groupoids]] (def. \ref{EquivalenceOfGroupoids});

1. $F$ is a [[weak homotopy equivalence]] (def. \ref{GroupoidWeakHomotopyEquivalence}).

=--

+-- {: .proof}
###### Proof


The implication 2) $\Rightarrow 1)$ is immediate.

In the other direction, assume that $F$ is an equivalence of groupoids, and let $G$ be an inverse up to natural isomorphism.
It is clear that both induces bijections on connected components. To see that both are isomorphisms
of automorphisms groups, observe that the conditions for the natural isomorphisms

$$
  \alpha \;\colon\; G \circ F \Rightarrow id
  \phantom{AAAA}
  \beta \;\colon\; F \circ G \Rightarrow id
$$

are in each separate [[delooping groupoid]] $B H_j$ of the form

$$
  \array{
    \ast &\overset{\alpha}{\longrightarrow}& \ast
    \\
    {}^{\mathllap{G_{F_0(i),F_0(i)}(F_{i,i}(f))}}\downarrow && \downarrow^{\mathrm{id}}
    \\
    \ast &\underset{\alpha}{\longrightarrow}& \ast
  }
  \phantom{AAAAAAAAAAAAAAAAAAAAA}
  \array{
    \ast &\overset{\beta}{\longrightarrow}& \ast
    \\
    {}^{\mathllap{F_{G_0(j),G_0(j)}(G_{j,j}(f))}}\downarrow && \downarrow^{\mathrm{id}}
    \\
    \ast &\underset{\beta}{\longrightarrow}& \ast
  }
$$

since there is only a single object. But this means $F_{i,i}$ and $F_{j,j}$ are group isomorphisms.

=--

+-- {: .num_prop #EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}
###### Proposition
**(every [[groupoid]] is [[equivalence of groupoids|equivalent]] to a [[disjoint union]] of [[group]] [[deloopings]])

Assuming the [[axiom of choice]], then:

For $\mathcal{G}$ any [[groupoid]], then there exists a [[set]] $\{G_i\}_{i \in I}$ of groups and an [[equivalence of groupoids]] (def. \ref{EquivalenceOfGroupoids})

$$
  \mathcal{G} \simeq \underset{i \in I}{\sqcup} B G_i
$$

between $\mathcal{G}$ and a [[disjoint union]] of [[delooping groupoids]] (example \ref{DeloopingGroupoidDisjointUnion}).
This is called a _[[skeleton]]_ of $\mathcal{G}$.

Concretely, this exists for $I = \pi_0(\mathcal{G})$ the set of [[connected components]] of $\mathcal{G}$ (def. \ref{GroupoidConnectedComponents}) and for $G_i \coloneqq Aut_{\mathcal{G}}(x)$ the [[automorphism group]] (def. \ref{InGrupoidAutomorphismGroup}) of any object $x$ in the given connected component.

=--

+-- {: .proof}
###### Proof


Using the [[axiom of choice]] we may find a set $\{x_i\}_{i \in \pi_0(\mathcal{G})}$ of objects of $\mathcal{G}$, with $x_i$ being in the [[connected component]] $i \in \pi_0(\mathcal{G})$.

This choice induces a functor

$$
  inc
   \;\colon\;
  \underset{i \in \pi_0(\mathcal{G})}{\sqcup} Aut_{\mathcal{G}}(x_i)
    \longrightarrow
  \mathcal{G}
$$

which takes each object and morphism "to itself".

Now using the [[axiom of choice]] once more, we choose in each connected component $i \in \pi_0(\mathcal{G})$
and for each object $y$ in that connected component a morphism

$$
  x_i \overset{f_{x_i,y}}{\longrightarrow} y
  \,.
$$

Using this we obtain a functor the other way around

$$
  p \;\colon\; \mathcal{G} \longrightarrow \underset{i \in \pi_0(\mathcal{G})}{\sqcup} Aut_{\mathcal{G}}(x_i)
$$

which sends each object to its connected component, and
which for pairs of objects $y$, $z$ of $\mathcal{G}$ is given by conjugation with the
morphisms choosen above:

$$
  \array{
    Hom_{\mathcal{G}}(y,z) &\overset{p_{y,z}}{\longrightarrow}& & Aut_{\mathcal{G}}(x_i) &
    \\
    \\
    y                 &&                     y & \overset{f_{x_i,y}}{\longleftarrow}& x_i
    \\
    {}^{\mathllap{f}} \downarrow &\mapsto&     {}^{\mathllap{f}}\downarrow
    \\
    z                 &&                     z & \underset{f_{x_i,z}^{-1}}{\longrightarrow} & x_i
  }
  \,.
$$

It is now sufficient to show that there are conjugations/natural isomorphisms

$$
  p \circ inc \simeq id
  \phantom{AAAA}
  inc \circ p \simeq id
  \,.
$$

For the first this is immediate, since we even have equality

$$
  p \circ inc \;=\; id
  \,.
$$

For the second we observe that choosing

$$
  \eta(y) \coloneqq f_{x_i,y}
$$

yields a naturality square by the above construction:

$$
  \array{
    x_i &\overset{f_{x_i,y}}{\longrightarrow}& y
    \\
    {}^{ \mathllap{ f_{x_i,z} \circ f \circ f_{x_i,y}^{-1} } }\downarrow && \downarrow^{\mathrlap{f}}
    \\
    x_i &\underset{f_{x_i,z}}{\longrightarrow}& z
  }
  \,.
$$

=--


+-- {: .num_prop #EquivalenceOfGroupoidsFromWeakHomotopyEquivalence}
###### Proposition
**([[weak homotopy equivalence]] is [[equivalence of groupoids]])

Let $F \;\colon\; \mathcal{G}_1 \longrightarrow \mathcal{G}_2$
be a homomorphism of [[groupoids]].

Assuming the [[axiom of choice]] then the following are equivalent:

1. $F$ is an [[equivalence of groupoids]] (def. \ref{EquivalenceOfGroupoids});

1. $F$ is a [[weak homotopy equivalence]] in that

   1. it induces an [[bijection]] of sets of [[connected]] components (def. \ref{GroupoidConnectedComponents});

      $$
        \pi_0(F) \;\colon\; \pi_0(\mathcal{G}_1) \overset{\simeq}{\longrightarrow} \pi_0(\mathcal{G}_0)
        \,,
      $$

  1. for each object $x \in \mathcal{G}_1$ it induces an isomorphism of [[automorphism groups]] (def. \ref{InGrupoidAutomorphismGroup}):

     $$
       F_{x,x} \;\colon\; Aut_{\mathcal{G}_1}(x) \overset{\simeq}{\longrightarrow} Aut_{\mathcal{G}_2}(F_0(x))
       \,.
     $$

=--

+-- {: .proof}
###### Proof


In one direction, if $F$ has an inverse up to natural isomorphism, then this induces by definition a bijection
on connected components, and it induces isomorphism on homotopy groups by lemma \ref{AutomorphismGroupDependsOnlyOnConnectedComponent}.

In the other direction, choose equivalences to [[skeleta]] as in prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}
to get a [[commuting diagram]] in the [[1-category]] of groupoids as follows:

$$
  \array{
    \mathcal{G}_1 &\underoverset{\simeq}{inc_1}{\longleftarrow}& \underset{i \in \pi_0(\mathcal{G}_1)}{\sqcup} Aut_{\mathcal{G}_1}(x_i)
    \\
    {}^{\mathllap{F}}\downarrow && \downarrow^{\mathrlap{\tilde F }}
    \\
    \mathcal{G}_2 &\underoverset{inc_2}{\simeq}{\longleftarrow}& \underset{i \in \pi_0(\mathcal{G}_1)}{\sqcup} Aut_{\mathcal{G}_2}(F_0(x_i))
  }
  \,.
$$

Here $inc_1$ and $inc_2$ are equivalences of groupoids by prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}.
Moreover, by assumption that $F$ is a weak homotopy equivalence $\tilde F$ is the union of of deloopings of 
isomorphisms of groups, and hence has a strict inverse, in particular a homotopy inverse, hence is in particular
an euivalence of groupoids. 

In conclusion, when regarded as a diagram in the [[homotopy category]] $Ho(Grpd)$ (def. \ref{HomotopyCategoryOfGroupoids}),
the top, bottom and right moprhism of the above diagram are isomorphisms. It follows that also 
$f$ is an isomorphism in $Ho(Grpd)$. But this means exactly that it is a homotopy equivalence of groupoids, by 
def. \ref{EquivalenceOfGroupoids}.


=--


+-- {: .num_prop #GroupoidRepresentationsAreProductsOfGroupRepresentations}
###### Proposition
**([[groupoid representations]] are [[product category|products]] of [[group representations]])

Assuming the [[axiom of choice]] then the following holds:

Let $\mathcal{G}$ be a [[groupoid]]. Then its [[category of representations|category of]]
[[groupoid representations]] is [[equivalence of categories|equivalent]] to the [[product category]]
indexed by the set of [[connected components]] $\pi_0(\mathcal{G})$ (def. \ref{GroupoidConnectedComponents}) of [[group representations]]
of the [[automorphism group]] $G_i \coloneqq Aut_{\mathcal{G}}(x_i)$ (def. \ref{InGrupoidAutomorphismGroup}) for $x_i$ any object in the $i$th
connected component:

$$
  Rep(\mathcal{G})
   \;\simeq\;
  \underset{i \in \pi_0(\mathcal{G})}{\prod} Rep(G_i)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let $\mmathcal{C}$ be the category that the representation is on. Then by definition

$$
  Rep(\mathcal{G}) = Hom( \mathcal{G} , \mathcal{C}  )
  \,.
$$

Consider the injection functor of the [[skeleton]] (from lemma \ref{DeloopingGroupoidEquivalence})

$$
  inc
  \;\colon\;
  \underset{i \in \pi_0(\mathcal{G})}{\sqcup} B G_i
  \overset{}{\longrightarrow}
  \mathcal{G}
  \,.
$$


By lemma \ref{HmotopiesWithMorphismsHorizontaComposition} the pre-composition with this constitutes a functor

$$
  inc^\ast \;\colon\; Hom( \mathcal{G}, \mathcal{C} ) \longrightarrow Hom( \underset{i \in \pi_0(\mathcal{G})}{\sqcup} B G_i, \mathcal{C} )
$$

and by combining lemma \ref{DeloopingGroupoidEquivalence} with lemma \ref{HorizontalCompositionWithHomotopyIsNaturalTransformation}
this is an [[equivalence of categories]]. Finally, by example \ref{GroupoidRepresentationOfDeloopingGroupoid} the
category on the right is the product of group representation categories as claimed.



=--



### As 2-coskeletal Kan complexes

Groupoids $K$ are equivalent to 1-[[hypergroupoids]], which are in particular 2-[[coskeletal]] [[Kan complexes]] $N(K)$ -- their [[nerves]].

The objects of the groupoids are the 0-[[simplices]] and the morphisms of the groupoid are the 1-simplices of the Kan complex. The [[composition]] operation $(f,g) \mapsto g \circ f $ in the grouopoid is encoded in the 2-simplices of the Kan complex

$$
  \array{
    && y
    \\
    & {}^{\mathllap{f}}\nearrow &=& \searrow^{\mathrlap{g}}
    \\
    x &&\underset{g\circ f}{\to}&& z
  }
  \,.
$$


The [[associativity]] condition on the composition is exhibited by the 3-[[coskeleton]]-property of the Kan complex. This says that every simplicial 2-sphere in the Kan complex has a unique filler. With the above identification of 2-simplices with composition operations, this means that the 2 ways

$$
  \array{
    y &\stackrel{g}{\to}& &\to& z
    \\
    \uparrow && &\nearrow&  \downarrow^{\mathrlap{h}}
    \\
    {}^{\mathllap{f}}\uparrow &^{\mathllap{g \circ f}}\nearrow& && \downarrow
    \\
    x &\underset{h \circ (g\circ f )}{\to}&&\to& w
  }
  \;\;\;
  and
  \;\;\;
  \array{
    y &\stackrel{g}{\to}& &\to& z
    \\
    \uparrow &\searrow& &&  \downarrow^{\mathrlap{h}}
    \\
    {}^{\mathllap{f}}\uparrow && &\searrow^{\mathrlap{h\circ g}}& \downarrow
    \\
    x &\underset{(h \circ g)\circ f}{\to}&&\to& w
  }
$$

of composing a sequence of three composable morphisms are equal

$$
  \array{
    y &\to& &\to& z
    \\
    \downarrow && &\nearrow&  \downarrow
    \\
    \downarrow &\nearrow& && \downarrow
    \\
    x &\to&&\to& w
  }
  \;\;\;
  \stackrel{=}{\to}
  \;\;\;
  \array{
    y &\to& &\to& z
    \\
    \downarrow &\searrow& &&  \downarrow
    \\
    \downarrow && &\searrow& \downarrow
    \\
    x &\to&&\to& w
  }
  \,.
$$


For handling just groupoids exclusively their description in terms of Kan complexes may be a bit of an overkill, but the advantage is that it embeds groupoids naturally in the more general context of [[2-groupoid]]s, [[3-groupoid]]s and eventually [[∞-groupoid]]s. For instance a [[pseudo-functor]] out of an ordinary groupoid into a 2-groupoid is simply a homomorphism of the corresponding Kan complexes.

The disadvantage of the simplicial approach is the difficulty of describing multiple compositions in higher dimensions, an important idea which is quite conveniently  handled cubically.


## Related concepts

[[!include homotopy n-types - table]]

* [[groupoid action]], [[groupoid-principal bundle]]

* [[presheaf of groupoids]]

* [[topological groupoid]], [[Lie groupoid]], [[smooth groupoid]]

* [[stack]], [[geometric stack]]

* [[Hopf algebroid]]

[[!include oidification - table]]

## References

An early occurence of the concept is (see also _[[Brandt groupoid]]_):

* {#Brandt27} H. Brandt, _&#220;ber eine Verallgemeinerung des Gruppenbegriffes_, Mathematische Annalen, (1927) 96 (1): 360&#8211;366, [doi:10.1007/BF01209171](https://doi.org/10.1007%2FBF01209171)


A motivation and introduction of the concept of groupoid and a tour of examples (including the refinement to [[topological groupoids]] and [[Lie groupoids]]) is in

* [[Alan Weinstein]], _Groupoids: Unifying Internal and External Symmetry -- A Tour through some Examples_, Notices of the AMS volume 43, Number 7 ([pdf](http://www.ams.org/notices/199607/weinstein.pdf))

Further exposition:

* [[Ronnie Brown]], _From groups to groupoids: A brief survey_ at _[Groupoids in Mathematics](http://pages.bangor.ac.uk/~mas010/gpdsweb.html)_, [pdf](http://pages.bangor.ac.uk/~mas010/pdffiles/groupoidsurvey.pdf), Bulletin of the London Mathematical Society 19(2):113-134, [doi](https://doi.org/10.1112/blms/19.2.113)

* [[Introduction to Topology -- 2]], *[Groupoids](https://ncatlab.org/nlab/show/Introduction+to+Topology+--+2#Groupoid)*


Technical discussion can be found, for instance, in the following references.

* [[Philip Higgins]], _Presentations of Groupoids, with Applications to Groups_, Proc. Camb. Phil. Soc., 60 (1964) 7--20.

* [[Philip Higgins]], _Categories and Groupoids_, van
Nostrand, New   York, 1971,Reprints in Theory and Applications of
Categories, 7 (2005) pp 1--195. ([web] (http://www.tac.mta.ca/tac/reprints/articles/7/tr7abs.html))

* [[Ronnie Brown]], _Topology and groupoids_, Booksurge, 2006. ([web] (http://pages.bangor.ac.uk/~mas010/topgpds.html))

* {#Zivaljevic} Rade T. &#381;ivaljevi&#263;, _Groupoids in combinatorics---applications of a theory of local symmetries_, Algebraic and geometric combinatorics, 305--324, Contemp. Math., 423, Amer. Math. Soc., Providence, RI, 2006.



[[!redirects groupoid]]
[[!redirects groupoids]]

[[!redirects tame groupoid]]
[[!redirects tame groupoids]]
