
> This article is about the notion prevalent in [[category theory]] and [[homotopy theory]], also known as a Brandt groupoid. For the notion involving a globally defined binary operation, see [[magma]].
#

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

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/AssociativityDiagram.png" width="400">
</div>


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

such that this composition is [[associativity|associative]] and such that for each object $x$ there is identity transformation $x \overset{id_X}{\longrightarrow} x$ in that this is a [[neutral element]] for the composition of transformations, whenever defined.

So far this structure is what is called a _[[small category]]_. What makes this a _([[small groupoid|small]]) groupoid_ is that all these transformations are to be "symmetries" in that they are [[invertible morphisms]] meaning that for each transformation $x \overset{f}{\longrightarrow} y$ there is a transformation the other way around $y \overset{f^{-1}}{\longrightarrow} x$ such that

$$
  f^{-1} \circ f  = id_x
  \phantom{AAAA}
  f \circ f^{-1} = id_y
  \,.
$$

If there is only a single object $x$, then this definition reduces to that of a [[group]], and in this sense groupoids are "groups with many objects". Conversely, given any groupoid $\mathcal{G}$ and a choice of one of its objects $x$, then the subcollection of transformations from and to $x$ is a group, sometimes called the [[automorphism group]] $Aut_{\mathcal{G}}(x)$ of $x$ in $\mathcal{G}$.

Just as for groups, the "transformations" above need not necessarily be given by concrete transformations (say by [[bijections]] between [[objects]] which are [[sets]]). Just as for groups, such a concrete realization is always possible, but is an extra choice (called a [[representation]] of the groupoid). Generally one calls these "transformations" _[[morphisms]]_: $x \overset{f}{\longrightarrow} y$ is a morphism with "[[source]]" $x$ and "[[domain]]" $y$.

An archetypical example of a groupoid is the [[fundamental groupoid]] $\Pi_1(X)$ of a [[topological space]] (for introduction see [here](Introduction+to+Topology+--+2#Homotopy)): For $X$ a topological space, this is the groupoid whose

* [[objects]] are the points $x \in X$;

* [[morphisms]] $x \overset{[\gamma]}{\longrightarrow} y$ are the [[homotopy relative boundary]]-[[equivalence classes]] $[\gamma]$ of [[paths]] $\gamma \colon [0,1] \to X$ in $X$, with $\gamma(0) = x$ and $\gamma(1) = y$;

and [[composition]] is given, on representatives, by [[concatenation]] of paths. Here the class of the [[reverse path]] $\bar\gamma \;\colon\; t \mapsto \gamma(1-t)$ constitutes the inverse morphism, making this a groupoid.

If one _chooses_ a point $x \in X$, then the corresponding group at that point is the _[[fundamental group]]_ $\pi_1(X,x) \coloneqq Aut_{\Pi_1(X)}(x)$ of $X$ at that point.

This highlights one of the reasons for being interested in groupoids over groups: Sometimes this allows to avoid unnatural ad-hoc choices and it serves to streamline and simplify the theory.

A [[homomorphism]] between groupoids is the obvious: a [[function]] between their underlying [[objects]] together with a function between their morphisms which respects [[source]] and [[target]] objects as well as [[composition]] and [[identity morphisms]]. If one thinks of the groupoid as a special case of a [[category]], then this is a _[[functor]]_. Between groupoids with only a single object this is the same as a [[group homomorphism]].

For example if $f \;\colon\; X \to Y$ is a [[continuous function]] between topological spaces, then postcomposition of [[paths]] with this function induces a groupoid homomorphism $f_\ast \;\colon\; \Pi_1(X) \longrightarrow \Pi_1(Y)$ between the [[fundamental groupoids]] from above.

Groupoids with groupoid homomorphisms ([[functors]]) between them form a [[category]] [[Grp]] which includes the categeory [[Grp]] of [[groups]] as the [[full subcategory]] of the groupoids with a single object. This makes precise how groupoid theory is a genralization of [[group theory]].

However, for groupoids more than for groups one is typically interested in "[[conjugation actions]]" on homomorphisms. These are richer for groupoids than for groups, because one may conjugate with a different morphism at each object. If we think of groupoids as special cases of [[categories]], then these "conjugation actions on homomorphisms" are _[[natural transformations]]_ between [[functors]].

For examples if $f,g \;\colon\; X \longrightarrow Y$ are two [[continuous functions]] between [[topological spaces]], and if $\eta \;\colon\; f \Rightarrow g$ is a [[homotopy]] from $f$ to $g$, then the [[homotopy relative boundary]] classes of the [[paths]] $\eta(x,-) \;\colon\; [0,1] \to Y$ constitute a natural transformation between $f_*, g_\ast \;\colon\; \Pi_1(X) \to \Pi_y(Y) $ in that for all paths $x_1 \overset{[\gamma]}{\longrightarrow} x_2$ in $X$ we have the "conjugation relation"

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
    {}^{\mathllap{[f \circ \gamma]}}\downarrow && \downarrow^{\mathrlap{[f \circ \gamma]}}
    \\
    f(x_1) &\underset{[\eta(x_2,-)]}{\longrightarrow}& g(x_2)
  }
  \,.
$$

One may take care of the existence of these conjugation actions/natutaral transformation in two way:

1. If one quotients them out, i.e. if one identifies two groupoid homomorphisms that differ by a conjugation action, then the resulting [[category]] of groupoids and classes of homomorphisms is called the _[[homotopy category]]_ $Ho(Grp)$ of [[Grp]]. This is [[equivalence of categories|equivalent]] to the [[full subcategory]] of the [[classical homotopy category]] of [[topological spaces]] on those that are ([[CW-complexes]] and) [[homotopy 1-types]], i.e. those for which the [[fundamental groupoid]] is the _only_ homotopy invariant, with all higher [[homotopy groups]] being trivial:

   $$
     Ho(Grpd) \simeq Ho(Top^{CW}_{\leq 1}) \hookrightarrow Ho(Top^{CW})
     \,.
   $$

   This means that the concept of groupoids may be regarded as a combinatorial model for [[homotopy 1-types]] in [[homotopy theory]], in contrast to the models by [[topological spaces]] given by [[topological homotopy theory]]. This equivalence generalizes to [[homotopy n-types]] as one passes to [[n-groupoids]] and eventually to all [[homotopy types]] as one passes to [[infinity-groupoids]].

1. Instead of forgetting all the information encoded in the conjugations/natural transformations, one may also collect it all into the structure of a [[2-category]] [[Grp]] (in fact a [[(2,1)-category]]). As such this is the sub-2-category of [[Cat]] on those (small) categories all whose morphisms are [[invertible morphism]].

For more introduction on this see at _[[geometry of physics -- homotopy types]]_.

In either of these two cases, beware that the category [[Grp]] of [[groups]] is _not_ a [[full subcategory]] either of the [[homotopy category]] $Ho(Grpd)$ or of the [[(2,1)-category]] [[Grpd]], because conjugation action is is not part of the definition of $Grp$. Instead in [[homotopy theory]] it is _[[pointed object|pointed]]_ one-object groupoids which are equivalent to groups

$$
  Grp \hookrightarrow Grpd^{\ast/}
  \,.
$$

(Even though there is a unique choice of point for a one-object groupoid, the respect for this (unique) choice forces the conjugation actions on groupoids to be trivial. ) This simple statement is in fact a special case of the [[May recognition theorem]] (see [there](Ek-Algebras#MainResult)) which holds for more general [[homotopy types]] and even for [[directed homotopy types]].

The equivalence of groupoids with [[homotopy 1-types]] shows immediately that, with [[homotopy]] taken into accont, the difference between groupoids and groups is rather mild, after all: Every [[groupoid]] is [[equivalence of groupoids|equvalent]] ([[isomorphism|isomorphic]] in $Ho(Grpd)$) to a [[disjoint union]] of groupoids with a single object. This is the reason why the competition between [[general topology]] textbooks that do and that do not prefer the [[fundamental groupoid]] over the [[fundamental group]] remains inconclusive.

However, this equivalence of groupoids with disjoint unions of groups depends on the [[axiom of choice]]. Even if this is assumed in the underlying [[foundations]]/[[set theory]], it breaks once one considers groupoids equipped with geometric stucture:

Just as one may consider [[topological groups]] and [[Lie groups]], etc., there are the evident concepts of [[topological groupoids]] and [[Lie groupoids]] etc. (generally: _[[internal  groupoids]]_). Their theory turns out to be genuinely richer than that of their group analogs, due to the interaction between the [[geometry]] and the [[homotopy theory]] ("[[higher geometry]]").

The correct concept of homomorphisms between [[Lie groupoids]] for instance goes by many names, including _[[Morita morphisms]]_, _[[Hilsum-Skandalis morphisms]]_ and _[[bibundles]]_. The general way to understand this and all other geometric groupoid theory is via the concept of _[[stacks]] of groupoids_. For more pointers on this see at _[[higher geometry]]_ and for introduction in the case of [[higher differential geometry]] see at _[[geometry of physics -- smooth homotopy types]]_.










## Definition


+-- {: .num_defn #GroupoidDependentlyTypes}
###### Definition
**(groupoid -- dependently typed definition)

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

1. for all pairs $x,y \in Hom(x,y)$ of obects a function

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

For $\mathcal{G}_1, \mathcal{G}_2$ two groupoids, and for $F,G \;\colon\; \mathcal{G}_1 \to \mathcal{G}_2$ two groupoid homomorphisms/functors, then a _conjugation_ or _[[natural transformation]]_ (necessarily a [[natural isomorphism]])

$$
  \eta \;\colon\; F \Rightarrow G
$$

is

* for each object $x \in X_1$ of $\mathcal{G}_1$ a morphism $\eta_{x} \in Hom_{\mathcal{G}_2}(F(x), G(y))$

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

Hence there is a [[category]], to be denoted [[Grpd]], whose

* [[objects]] are the small groupoids;

* [[morphisms]] are the groupoid homomorphisms ([[functors]]).

There is also the [[homotopy category]] $Ho(Grpd)$ whose

* [[objects]] are small groupoids;

* [[morphisms]] are [[equivalence classes]] of groupoid homomorphisms modulo conjugation actions (i.e. [[functors]] modulo [[natural transformations]])


=--


+-- {: .num_remark}
###### Remark

A [[small groupoid]] (def. \ref{GroupoidGlobalDefinition}) is equivalently a [[small category]] in which all [[morphisms]] are [[isomorphism|isomorphisms]].

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

+-- {: .num_defn #EquivalenceOfGroupoids}
###### Definition
**([[equivalence of groupoids]])**

Given two groupoids $\mathcal{G}_1$ and $\mathcal{G}_2$, then a homomorphism

$$
  F\;\colon\; \mathcal{G}_1 \longrightarrow \mathcal{G}_2
$$

is an _[[equivalence of groupoids|equivalence]]_ it it is an [[isomorphism]]
in the [[homotopy category]] $Ho(Grpd)$, hence if there exists a homomorphism the
other way around

$$
  G \;\colon\; \mathcal{G}_2 \longrightarrow \mathcal{G}_1
$$

and conjugations/natural transformations of the form

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
**(automorphism group)

Given a [[groupoid]] $\mathcal{G}$ and an object $x$, then under composition the set $Hom_{\mathcal{G}}(x,x)$ forms a [[group]]. This is called the _[[automorphism group]]_ $Aut_{\mathcal{G}}(x)$ or _vertex group_ or _isotropy group_ of $x$ in $\mathcal{G}$.

=--

+-- {: .num_defn}
###### Definition
**(tame groupoids)**

A groupoid is called **tame** if its [[groupoid cardinality]] is finite.

=--



## Examples

+-- {: .num_example #GroupoidFromDelooping}
###### Example
**([[delooping]] of a  [[group]])**

Let $G$ be a [[group]]. Then there is a groupoid, denoted $B G$, with a single object $p$, with morphisms

$$
  Hom_{B G}(p,p) \coloneqq G
$$

the elements of $G$, with composition the multiplication in $G$, with identity morphism the [[neutral element]] in $G$ and with inverse morphisms the inverse elements in $G$.

This is also called the _[[delooping]]_ of $G$.

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



1. Any [[group]] $H$ gives rise to a groupoid, sometimes denoted $\mathbf{B}H$ but often conflated with $H$ itself, which has exactly one object $*$ and with $\mathbf{B}H(*,*) = H$.  That is, there is an inclusion of categories $Group \to Groupoids$, and this functor has a left adjoint, giving the _universal group_ of a groupoid. Any inhabited connected groupoid is [[equivalence of categories|equivalent]] to one arising in this way.

2. A [[disjoint union]] of (the one-object groupoids corresponding to) groups is naturally a groupoid, also called a _bundle of groups_.  The [[axiom of choice]] is equivalent to the claim that any groupoid is equivalent to one of this form.

3. From any [[group action|action]] of a [[group]] $H$ on a [[set]] $X$ we obtain an [[action groupoid]] or "[[weak quotient]]" $X/ \!\! /H$. This is also written $X \rtimes H$, a semidirect product, since it is a special case of the semidirext product of an action of a groupoid on a groupoid.  If $X=\{*\}$ this gives the groupoid $\mathbf{B}H$, above.

4. A [[setoid]], that is a set $X$ equipped with an [[equivalence relation]] $E$, becomes a groupoid with the multiplication $(x,y);(y,z) = (x,z)$ for all $(x,y), (y,z) \in E$.  (This gives one reason for the forward notation for composition.)  Such a groupoid is equivalent to the [[discrete category]] on the [[quotient set]] $X/E$.

5. In particular, if $E$ is the universal relation $X \times X$, then we get the _[[square groupoid]]_ $X^2$, also called the _[[trivial groupoid]]_ on $X$. Despite the latter name, there is an important special case, namely the groupoid $I= \{0,1\}^2$. This groupoid has non-identity elements $\iota:0 \to 1, \iota^{-1}: 1 \to 0$, and can be regarded as a groupoid model of the unit [[interval]] $[0,1]$ in [[topology]].

6. Any [[topological space]] $X$ has a [[fundamental groupoid]] $\pi_1(X)$ whose objects are the [[points]] of $X$ and whose arrows are (homotopy classes rel end points of of) [[paths]], with composition by [[concatenation]] of paths.  Note that $\pi_0(\pi_1(X)) = \pi_0(X)$ is the set of [[path component|path components]] of $X$, and for any $x\in X$, $\pi_1(\Pi_1(X),x) = \pi_1(X,x)$ is the [[fundamental group]] of $X$ with basepoint $x$.  In theory one can obtain the higher [[homotopy groups]] in this way as well, by generalizing from the fundamental groupoid to the [[fundamental infinity-groupoid]].

7. More generally, if we choose some [[subset]] $S$ of the points of a space $X$, then we have a [[full subcategory|full subgroupoid]] of $\pi_1(X)$ containing only those points in $S$, denoted $\pi_1(X,S)$.  This can result in much more manageable groupoids; for instance $\Pi_1([0,1],\{0,1\})$ is the groupoid $I$ considered above, while $\Pi_1([0,1])$ has [[uncountable set|uncountably]] many objects (but is [[equivalence of categories|equivalent]] to $I$).

8. If $\Gamma$ is a [[directed graph]] or [[quiver]], then the _[[free groupoid]]_ $F(\Gamma)$ is well defined. It is the left [[adjoint functor]] to the [[forgetful functor]] from groupoids to directed graphs. This shows an advantage of groupoids: the notion of _free equivalence relation_ or _free action groupoid_ does not easily make sense. But we can still talk of a presentation of an equivalence relation or action groupoid by [[generators and relations]], by considering presentations of groupoids instead.

   +-- {: .query}
   [[Mike Shulman|Mike]]: It's not clear to me that the notion of "free equivalence relation" doesn't make sense.  Can't I talk about a left adjoint to the forgetful functor from equivalence relations to, say, directed graphs?  Maybe sets-equipped-with-a-binary-relation would be more appropriate, but either one works fine.

   [[Ronnie Brown|Ronnie]]: Are you sure this forgetful functor equivalence relations to directed graphs has a left adjoint? Suppose the directed graph $\Gamma$ has one vertex $x$ and one loop $u:x  \to x$. The free groupoid on $\Gamma$ is the group of integers, which as a groupoid is not an equivalence relation.

   _Toby_:  But there is still a free [[setoid]] (set equipped with an equivalence relation) on $\Gamma$; it is the [[point]].  As a groupoid, it is not the same as the free groupoid on $\Gamma$, although it *is* the same as the free setoid on the free groupoid on $\Gamma$.  If there\'s an advantage to working with groupoids, perhaps it\'s that the free groupoid functor preserves distinctions that the free setoid functor forgets?  (In this case, a distinction preserved or forgotten is that between $\Gamma$ and the point, which as a graph does not have $u$.)
   =--

9. A [paper by &#381;ivaljevi&#263;](#Zivaljevic) gives examples of groupoids used in combinatorics.

10. The book "Topology and Groupoids" listed below takes the view that 1-dimensional homotopy theory, including the Seifert-van Kampen Theorem, the theory of covering spaces, and the less well known theory of the fundamental group(oid) of an orbit space by a discontinuous group action, is best presented using the notion of groupoid rather than group as basic. This had led in the 1960s to the question of the prospective use of (strict) groupoids in higher homotopy theory. One answer is given in the book _[[Nonabelian algebraic topology]]_.


## Properties

### Basic properties

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


+-- {: .num_prop #EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}
###### Proposition
**(every [[groupoid]] is [[equivalence of groupoids|equivalent]] to a [[disjoint union]] of [[group]] [[delooping]])

Assuming the [[axiom of choice]], then:

For $\mathcal{G}$ any [[groupoid]], then there exists a [[set]] $\{G_i\}_{i \in I}$ of groups and an [[equivalence of groupoids]] (def. \ref{EquivalenceOfGroupoids})

$$
  \mathcal{G} \simeq \underset{i \in I}{\sqcup} G_i
$$

between $\mathcal{G}$ and a [[disjoint union]] of [[delooping]] groupoids (example \ref{DeloopingGroupoidDisjointUnion}).
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
  \mmathcal{G}
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
    Hom_{\mathcal{G}}(y,z) &\overset{p_{y,z}}{\longrightarrow}& Aut_{\mathcal{G}}(x_i)
    \\
    \\
    y                 &&                     y & \overset{f_{x_i,y}}{\longleftarrow}& x_i
    \\
    {}^{\mathllap{f}}\dwnarrow &\mapsto&     {}^{\mathllap{f}}\downarrow
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

* [[topological groupoid]], [[Lie groupoid]], [[smooth groupoid]]

* [[stack]], [[geometric stack]]

* [[Hopf algebroid]]


## References

A motivation and introduction of the concept of groupoid and a tour of examples (including the refinement to [[topological groupoids]] and [[Lie groupoids]]) is in

* [[Alan Weinstein]], _Groupoids: Unifying Internal and External Symmetry -- A Tour through some Examples_, Notices of the AMS volume 43, Number 7 ([pdf](http://www.ams.org/notices/199607/weinstein.pdf))

Further exposition includes

* [[Ronnie Brown]], _From groups to groupoids: A brief survey_ at _[Groupoids in Mathematics](http://pages.bangor.ac.uk/~mas010/gpdsweb.html)_, ([pdf](http://pages.bangor.ac.uk/~mas010/pdffiles/groupoidsurvey.pdf))

Technical discussion is for instance in the following references.

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

[[!redirects 1-type]]
[[!redirects 1-types]]
[[!redirects homotopy 1-type]]
[[!redirects homotopy 1-types]] 