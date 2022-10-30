

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

In an [[(∞,1)-category]] $C$ with $(\infty,1)$-[[pullbacks]], the _free loop space object_ $\mathcal{L}X$ of any object $X$ -- also called the _[[inertia groupoid]]_ -- is an object that behaves as if its [[generalized elements]] are loops in $X$, morphisms between generalized elements [[homotopy|homotopies]] of loops, and so on.

For the case that $C = $ [[Top]] this reproduces the ordinary notion of  [[free loop spaces]] of [[topological spaces]].

Over each fixed element $x \in X$, the free loop space object $\mathcal{L}X$ looks like the based [[loop space object]] $\Omega_x X$ of $X$.

Free loop space objects come naturally equipped with various structures of interest, such as a categorical circle action. The [[cohomology]] of $\mathcal{L}X$ is [[Hochschild cohomology]] or [[cyclic cohomology]] of function algebras $C(X)$ on $X$. The categorical circle action induces [[differential]]s on these cohomologies, identifying them, in suitable cases, with algebras of [[Kähler differential|Kähler]] [[differential form]]s on $X$.


## Definition

### In higher category theory

There are various equivalent ways to define the free loop space object.

Let $C$ be an [[(∞,1)-category]].  Recall that every $(\infty,1)$-category is [[enriched category|enriched]] over [[?Gpd]], in that there is a hom-space $Map(X,Y) \in \infty Gpd$ for any $X,Y\in C$.  This enables us to define the [[power]] of an object $X\in C$ by any $\infty$-groupoid $K$, as an object $X^K \in C$ together with a map $K \to Map(X^K,X)$ inducing equivalences $Map(Y,X)^K \simeq Map(Y,X^K)$ for all $Y\in C$ (where $Map(Y,X)^K$ denotes the mapping-space from $K$ to $Map(Y,X)$ in $\infty Gpd$), if such exists.

+-- {: .num_defn}
###### Definition
The **free loop space object** of $X\in C$ is the power $\mathcal{L}X = X^{S^1}$, if it exists, where $S^1$ denotes the homotopical [[circle]].
=--

This can also be written in terms of "conical" limits in $C$.  Most commonly, if we note that $S^1$ is the pushout of two copies of $\ast$ under $\ast\sqcup \ast$, and that $Map(\ast,X) \simeq X$ while $Map(\ast\sqcup \ast ,X) \simeq X\times X$, we find that $X^{S^1}$ is the pullback of $X$ and $X$ over $X\times X$:

+-- {: .num_defn}
###### Definition

In an [[(∞,1)-category]] $C$ with [[(∞,1)-pullbacks]], for $X \in C$ an [[object]], its **free loop space object** $\mathcal{L}X$ is the $(\infty,1)$-pullback of the [[diagonal]] along itself

$$
  \array{
    \mathcal{L} X &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    X &\stackrel{(Id,Id)}{\to}& X \times X
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark


This is the $(\infty,1)$-categorical [[span trace]] of the identity-[[span]]

$$
  \mathcal{L}X =
  Tr
  \left(
    \array{
       && X
       \\
       & {}^{\mathllap{Id}}\swarrow && \searrow^{\mathrlap{Id}}
       \\
       X &&&& X
    }
  \right)
  \,.
$$

=--

We can also use the fact that $S^1$ is the [[homotopy coequalizer]] of $\ast \rightrightarrows \ast$:

+-- {: .num_defn}
###### Definition
The **free loop space object** of $X\in C$ is the homotopy equalizer of two copies of the identity map $X \rightrightarrows X$.
=--


### In homotopy type theory
 {#InHomotopyTypeTheory}

In the literature (see [below](#References)) when the free loop space object $\mathcal{L}X$ is defined as the homotopy pullback $X\times_{X\times X} X$, it is sometimes described heuristically as: "a point of $\mathcal{L}X$ is a choice of making two points of $X$ equal in two ways." In terms of [[homotopy type theory]] this heuristics becomes a theorem. In that higher categorical logic we have the expression

$$
  \begin{aligned}
    \mathcal{L}X 
    & \coloneqq 
    \left\{
       x,y : X \;|\; (x = y) \, and\, (x = y) 
    \right\}
    \\
    & =
    \left\{
       x,y : X \;|\; (x,x) = (y,y) 
    \right\}
  \end{aligned} 
  \,.
$$

Here on the right we have

1. the [[dependent sum]];

1. over the [[identity type]] $Id (X \times X)$;

1. of the [[product type]] $X \times X$.

See the discussion at _[[homotopy pullback]]_ in the section _[Construction in homotopy type theory](http://ncatlab.org/nlab/show/homotopy+pullback#ConstructionInHomotopyTypeTheory)_ for how this is equivalent to the previous definition.

Now since $\sum_{y:X} (x=y)$ is [[contractible type|contractible]], the above type is equivalent to

$$ \sum_{x:X} (x=x) $$

i.e. the type of points that are equal to themselves (in a specified, not necessarily reflexivity, way).  This corresponds to the other definitions, as a homotopy equalizer or a powering by $S^1$.


## Properties


### Models by homotopy pullbacks {#HomPullModel}

To see what the definition of a free loop space object amounts to in more detail, assume that the [[(∞,1)-category]] is modeled by a [[homotopical category]], say for simplicity a [[category of fibrant objects]], for instance the full subcategory on fibrant objects of a [[model category]]. 

Then following the discussion at [[homotopy pullback]] and [[generalized universal bundle]] we can compute the about $(\infty,1)$-pullback $X\times_{X\times X}^h X$ as the ordinary [[limit]] 

$$
  \array{
    \mathcal{L}X &\to& &\to& X
     \\
    \downarrow && && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    && (X \times X)^I &\stackrel{(d_0,d_0)}{\to}& X \times X
    \\
    \downarrow &&  {}^{\mathllap{(d_1,d_1)}}\downarrow
    \\
    X &\stackrel{(Id,Id)}{\to} &  X \times X
    \,,
  }
$$

where $(X\times X)^I$ is a [[path space object]] for $X \times X$.  At least if we have the structure of a [[model category]] we may take $(X \times X)^I = X^I \times X^I$ for a [[path space object]] $X^I$ of $X$. 

From this description one sees that $\mathcal{L}X$ is built from _pairs of paths_ in $X$ with coinciding endpoints, that are _glued at their coinciding endpoint_ . So the loops here are all built from two semi-ciricle paths.



### Relation to based loop space object
 {#RelationToBasedLoops}

The fiber of $\mathcal{L}X$ over a [[point]] $x : {*} \to X$ is the corresponding (based) [[loop space object]] $\Omega_x X$ of $X$: we have an $(\infty,1)$-[[pullback]] diagram

$$
  \array{
    \Omega_x X &\to& \mathcal{L}X &\to& X
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{(Id,Id)}} 
    \\
    {*} &\stackrel{x}{\to} & X &\stackrel{(Id,Id)}{\to}& X\times X
  }
  \,.
$$

To see this, use that [[homotopy pullback]]s paste to homotopy pullbacks, so that the outer pullback is modeled by the ordinary [[limit]]

$$
  \array{
    \Omega_x^{I \vee I}X &\to& &\to& X
     \\
    \downarrow && && \downarrow^{\mathrlap{(Id,Id)}}
    \\
    && (X \times X)^I &\stackrel{(d_0,d_0)}{\to}& X \times X
    \\
    \downarrow &&  {}^{\mathllap{(d_1,d_1)}}\downarrow
    \\
    {*} &\stackrel{(x,x))}{\to} &  X \times X
    \,,
  }
$$

which builds based loops on $X$ from two consecutive paths, the first starting at the basepoint $x$, the second ending there. This is weakly equivalent $\Omega_x X = \Omega^I_x X \stackrel{\simeq}{\to} \Omega^{I \vee I} X$ to the based [[loop space object]] $\Omega_x X$ built from just the path space object $X^I$ with a single copy of $I$, by standard arguments as for instance form page 12 on in 

* [[Kenneth Brown]], _[[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_ .

### Action on objects of the slice
 {#SliceAction}

The free loop space object $\mathcal{L} X$ is a [[group object]] in the [[slice (∞,1)-category]] $C/X$, and has a canonical [[action]] on all objects of $C/X$.

Intuitively, the group structure comes from composition and inversion of loops.  When the free loop space is expressed as a [[power]] $X^{S^1}$, this group structure comes from the canonical [[cogroup]] structure on $S^1$.  In [[homotopy type theory]], it is literally concatenation of paths.  And when $\mathcal{L}X$ is expressed as the pullback $X\times_{X\times X} X$, the group multiplication can be obtained by considering the following pasting square:

$$\array{
\mathcal{L}X \times_X \mathcal{L}X & \to & \mathcal{L} X & \to & X\\
\downarrow && \downarrow && \downarrow \\
\mathcal{L} X & \to & X & \to & X\times X \\
\downarrow && \downarrow && \downarrow^{id} \\
X & \to & X\times X & \xrightarrow{id} & X\times X
}$$

Here the bottom-left and top-right squares are the pullback defining $\mathcal{L}X$, the top-left square is the pullback defining $\mathcal{L}X \times_X\mathcal{L}X$, and the bottom-right square commutes but is not a pullback.  By the universal property of the pullback square defining $\mathcal{L}X$, this square factors through it uniquely, giving the composition map $\mathcal{L}X \times_X \mathcal{L}X\to \mathcal{L}X$.  Similarly but more simply, the inversion map $\mathcal{L}X\to \mathcal{L}X$ comes from transposing its defining pullback square and factoring it through itself.

Now consider $Y\to X$ an object of $C/X$.  There is a canonical projection $\mathcal{L}X \times_X Y \to Y$, which is not the action of $\mathcal{L}X$ on $Y$, but it almost is.  In fact since this projection is a morphism in the "homotopy" slice $C/X$, it consists not just of a morphism in $C$ but a homotopy witnessing that a certain triangle commutes, which is equivalently the homotopy in the left-hand commutative square below (which is the pullback defining $\mathcal{L}X \times_X Y$):

$$\array{ \mathcal{L}X \times_X Y & \to & \mathcal{L} X & \xrightarrow{id} & \mathcal{L}X \\
\downarrow && \downarrow && \downarrow \\
Y & \to & X & \xrightarrow{id} & X}
$$

Pasting this with the right-hand commutative square, which is the canonical automorphism of the projection $\mathcal{L}X\to X$, we obtain a different homotopy witnessing a  different morphism $\mathcal{L}X \times_X Y \to Y$ in $C/X$ (with the same underlying morphism in $C$), and *this* is the action of $\mathcal{L}X$ on $Y$.

The definitiong of the right-hand commutative square above may not be obvious.  It is clear when we write $\mathcal{L}X = X^{S^1}$; when we write $\mathcal{L}X = X\times_{X\times X} X$ it can be obtained as the following pasting square, where $p$ and $q$ are the two projections in the defining pullback of $\mathcal{L}X$:

$$ \array{
\mathcal{L}X & \xrightarrow{p} & X & \to & X\times X & \xrightarrow{\pi_1} & X\\
^{id}\downarrow && && \downarrow^{id} && \downarrow \\
\mathcal{L}X & \xrightarrow{q} & X & \to & X\times X & \xrightarrow{\pi_1} & X\\
^{id}\downarrow && \downarrow^{id} && && \downarrow \\
\mathcal{L}X & \xrightarrow{q} & X & \to & X\times X & \xrightarrow{\pi_2} & X\\
^{id}\downarrow && && \downarrow^{id} && \downarrow \\
\mathcal{L}X & \xrightarrow{p} & X & \to & X\times X & \xrightarrow{\pi_2} & X\\
^{id}\downarrow && \downarrow^{id} && && \downarrow \\
\mathcal{L}X & \xrightarrow{p} & X & \to & X\times X & \xrightarrow{\pi_1} & X
}$$

To extend these structures to a coherent $\infty$-group structure and a coherent $\infty$-action, see for instance [this MO answer](https://mathoverflow.net/a/281937).

### In an $(\infty,1)$-topos {#InATopos}

We consider now the case that $C = \mathbf{H}$ is an  [[(∞,1)-topos]] (of [[(∞,1)-sheaves]]/[[∞-stack]]s). This comes canonically with its [[terminal object|terminal]] [[global section]]s [[(∞,1)-geometric morphism]]

$$
  (LConst \dashv \Gamma) : \mathbf{H} \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
  \,.
$$ 

In this case we can reformulate the power definition $\mathcal{L}X = X^{S^1}$ using a version of $S^1$ that is an object of $\mathbf{H}$ itself.

#### As a mapping space object {#AsMappingSpaceObject}

+-- {: .num_defn}
###### Definition/Proposition

Write 

$$
  S^1 \in Top \simeq \infty Grpd \stackrel{LConst}{\hookrightarrow} \mathbf{H}
$$

for the [[circle]]. In [[Top]] this is the usual topological circle. In [[∞Grpd]] this is (the [[homotopy type]] of) the [[fundamental ∞-groupoid]] of the topological circle. We may think of this as the [[(∞,1)-pushout]]

$$
  S^1 \simeq * \coprod_{* \coprod *} *
$$

hence as the universal [[cocone]]

$$
  \array{
    * \coprod * &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    * &\to& S^1
  }
$$

in $\infty Grpd$. 

In $\mathbf{H}$ we still write $S^1$ for the [[constant ∞-stack]] on this, the image of this under $LConst$. Since $LConst$ is a [[left adjoint]] and hence preserves this poushout, there is no risk of confusion.

=--

+-- {: .proof}
###### Proof

To see that the given $(\infty,1)$-pushout indeed produces the circle, we use the standard [[model structure on simplicial sets]] $sSet_{Quillen}$ to [[presentable (∞,1)-category|present]] [[∞Grpd]]. In $sSet_{Quillen}$ the $(\infty,1)$-pushout is computed by the [[homotopy pushout]]. By general facts about this, it may be computed as an ordinary [[pushout]] in [[sSet]] once we pass to an equivalent pushout diagram in which at least one morphism is a [[monomorphism]]. This is the case for

$$
  \array{
    * \coprod * &\to& *
    \\
    \downarrow && \downarrow
    \\
    \Delta[1] &\to& \Delta[1]/\partial \Delta[1]
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Informally the $(\infty,1)$-pushout $* \coprod_{* \coprod *} *$ may be thought of as 

* the disjoint union of two points $*_1$, $*_2$;

* equipped with _two_ non-equivalent abstract [[homotopies]] between them

  $$
    S^1 
    =
   \left\{
    \array{
       & \nearrow \searrow^{\mathrlap{\simeq}}
       \\
       *_1 && *_2
       \\
       & \searrow \nearrow_{\mathllap{\simeq}}
    }
    \right\}
    \,.
  $$ 

This equivalent way of modelling the circle not as a single point with an automorphism, but as two points with two isomorphisms is what connects directly to the definition of the free loop space object. This we now come to. It is also the fundamenal source of the basic structure of [[Hochschild cohomology|Hochschild (co)homology]] (as discussed there).

=--

\begin{lemma}

Every [[(∞,1)-topos]] is a [[cartesian closed (∞,1)-category]]: we have for every object $X \in \mathbf{H}$ an [[internal hom]]-[[(∞,1)-functor]]

$$
  [X,-] : \mathbf{H} \to \mathbf{H}
  \,.
$$

\end{lemma}

+-- {: .proof}
###### Proof

This is discussed at [[(∞,1)-topos]] in the section <a href="http://ncatlab.org/nlab/show/(infinity,1)-topos#ClosedMonoidalStructure">Closed monoidal structure</a>.

=--

+-- {: .num_prop}
###### Proposition

There is a natural [[equivalence in an (∞,1)-category|equivalence]]

$$
  \mathcal{L}X \simeq [S^1 , X]
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows from the above by the fact (see <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-topos#ClosedMonoidalStructure">closed monoidal structure on (∞,1)-toposes</a>) that the internal hom in an $(\infty,1)$-topos preserves finite colimits in its first argument and satisfies 

$$
  [*,X] \simeq X
  \,.
$$

This yields

$$
  \begin{aligned}
    [S^1 ,X] &\simeq [* \coprod_{* \coprod *} *, X]
    \\
      & \simeq
      [*,X] \times_{[* \coprod *, X]} [*,X]
     \\
      & \simeq X \times_{X \times X} X
     \\
     & \simeq \mathcal{L}X
     \,.
  \end{aligned}
$$

=--

+-- {: .num_prop}
###### Corollary

We have that the free loop space object of $X \in \mathbf{H}$ is equivalently the <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#Tensoring">powering</a> of $X$ by the $\infty$-groupoid $S^1$:

$$  
  \mathcal{L} X \simeq X^{S^1}
$$

=--

+-- {: .proof}
###### Proof

Follows by the above from the equivalence $[LConst S^1 , X] \simeq X^{S^1}$ discussed at [[(∞,1)-topos]].

=--

#### Intrinsic circle action {#CircleAction}



By precomposition, the [[automorphism 2-group]] of the [[circle]] $S^1$ acts on free loop space of an object $X \in \mathbf{H}$

$$
  Aut(S^1) \times [S^1, X] 
  \to 
  [S^1, S^1] \times [S^1, X] \stackrel{\circ}{\to} [S^1, X]
  \,.
$$


+-- {: .num_prop}
###### Proposition

The connected component of $[S^1,S^1]$ on the identity is equivalent to $S^1$

$$
  [S^1 , S^1]_{Id} \simeq S^1
$$

=--

+-- {: .num_defn}
###### Definition

We say that

$$
  S^1 \times [S^1, X] 
    \simeq
  [S^1, S^1]_{Id} \times [S^1, X]
  \stackrel{\circ}{\to} 
  [S^1, X]
$$

is the intrinsic **circle action** on the free loop space object.

=--

+-- {: .proof}
###### Proof

We spell out in detail what this action looks like.
The reader should thoughout keep the [[homotopy hypothesis]]-equivalence, $(|-| \dashv \Pi) : Top \simeq \infty Grpd$ in mind.

We may realize the [[circle]] $S^1 \in $ [[Top]] under $\Pi : Top \simeq \infty Grpd$ as the [delooping]] [[groupoid]] $\mathbf{B}\mathbb{Z}$ of the additive [[group]] $\mathbb{Z}$ of [[integer]]s 

The [[automorphism 2-group]] of this object is the [[functor category|functor groupoid]]

$$
  Aut_{Grpd}(\mathbf{B}\mathbb{Z})
$$

whose [[object]]s are invertible [[functor]]s $\mathbf{B}\mathbb{Z} \to \mathbf{B}\mathbb{Z}$ and whose [[morphism]]s are [[natural transformation]]s between these. 

The functors $\mathbf{B}\mathbb{Z} \to \mathbf{B}\mathbb{Z}$ correspond bijectively to group [[homomorphism]]s $\mathbb{Z} \to \mathbb{Z}$, hence to multiplication by $n\in\mathbb{Z}$

$$
  [n] : \mathbf{B}\mathbb{Z} \to \mathbf{B}\mathbb{Z}
$$

$$
  (\bullet \stackrel{k}{\to} \bullet) \mapsto (\bullet \stackrel{n\cdot k}{\to} \bullet).
$$

Natural transformations between two such endomorphisms are given by a component $\ell \in \mathbb{Z}$ such that all diagrams

$$
  \array{
    \bullet &\stackrel{\ell}{\to}& \bullet
    \\
    {}^{\mathllap{n\cdot k}}\downarrow && \downarrow^{\mathrlap{n' \cdot k}}
    \\
    \bullet &\stackrel{\ell}{\to}& \bullet    
  }
$$

commute in $\mathbf{B}\mathbb{Z}$. This can happen only for $n = n'$, but then it happens for arbitrary $\ell$. 

In other words we have

$$
  Aut(\mathbf{B}\mathbb{Z}) \simeq 
  \coprod_{[n] \in \mathbb{Z}^\times}\mathbf{B}\mathbb{Z}
  \,.
$$

and 

$$
Aut_{Id}(\mathbf{B}\mathbb{Z}) \simeq \mathbf{B}\mathbb{Z}
  \,.
$$

The object $[n]$ corresponds to the self-mapping of the circle that fixes the basepoint and has winding number $n\in\mathbb{Z}$. The transformation $\ell$ corresponds then to a rigid rotation of the loop by $\ell$ full circles

Notably for $n = 1$ and $k = 1$ we may think of the diagram

$$
  \array{
    \bullet &\stackrel{\ell}{\to}& \bullet
    \\
    {}^{\mathllap{1}}\downarrow && \downarrow^{\mathrlap{1}}
    \\
    \bullet &\stackrel{\ell}{\to}& \bullet    
  }
$$

as depicting the unit loop around the circle (on the left, say) and the result of translating its basepoint $\ell$-times around the circle (the rest of the diagram). Of course since we are using a model of $S^1$ with a single object here, every rotation of the loop is a full circle rotation, which is a bit hard to see.

=--

> Exercise: spell out the above discussion analogously for the equivalent model given by the [[fundamental groupoid]] $\Pi_1(S^1)$ of the standard circle. The is the groupoid with $S^1_{Top}$ as its set of objects homotopy classes of paths in the circle as morphisms. In this model things look more like one might expect from a circle action. Notice that $\mathbf{B}\mathbb{Z}$ is the [[skeleton]] of $\Pi_1(S^1)$.

+-- {: .num_example}
###### Example

Consider $\mathbf{H} = $ [[∞Grpd]], $G$ a [[group]] and  $X = \mathbf{B}G$ the [[delooping groupoid]]. Then $\mathcal{L}X = G//_{Ad}G$ (as discussed in detail [below](#LoopsInBG)). A morphism $(g \stackrel{h}{\to} Ad_h a)$ in $G//G$ corresponds to a natural transformation

$$
  \array{
    & \nearrow \searrow^{\mathrlap{g}}
    \\
    \mathbf{B}\mathbb{Z}
    &\Downarrow^{h}&
    \mathbf{B}G
    \\
    & \searrow \nearrow_{\mathrlap{Ad_h g}}
  }
  \,.
$$

Precomposing this with the automorphism $\ell$ of the object $[n]$ in $END(\mathbf{B}\mathbb{Z})$

$$
  \array{
    & \nearrow \searrow^{\mathrlap{n}}
    \\
    \mathbf{B}\mathbb{Z}
    &\Downarrow^{\ell}&
    \mathbf{B}\mathbb{Z}
    \\
    & \searrow \nearrow_{\mathrlap{n}}
  }
$$

produces the new transformation

$$
  \array{
    & \nearrow \searrow^{\mathrlap{n}} && \nearrow \searrow^{\mathrlap{g}}
    \\
    \mathbf{B}\mathbb{Z}
    &\Downarrow^{\ell}&
    \mathbf{B}\mathbb{Z}
    &\Downarrow^{h}&
    \mathbf{B}G
    \\
    & \searrow \nearrow_{\mathrlap{n}} && \searrow \nearrow_{\mathrlap{Ad_h g}}
  }
  \,.
$$

By the rules of horizontal composition of [[natural transformation]]s, this is the transformation whose component naturality square on $(\bullet \stackrel{1}{\to} \bullet)$ in $\mathbf{B}\mathbb{Z}$ is the diagram

$$
  \array{
    \bullet &\stackrel{g^\ell}{\to}& \bullet &\stackrel{h}{\to}&\bullet
    \\
    {}^{\mathllap{g^{n}}}\downarrow && {}^{g^n}\downarrow && \downarrow^{\mathrlap{Ad_h g^n}}
   \\
    \bullet &\underset{g^\ell}{\to}& \bullet &\underset{h}{\to}&\bullet
  }
$$

in $\mathbf{B}\mathbb{Z}$, hence the morphism $(g^n \stackrel{g^{\ell} h}{\to} Ad_h g^n)$ in $G//_{Ad}G$. In particular, the categorical circle action is 
$$
\ell:(g \stackrel{h}{\to} Ad_h g)\mapsto (g \stackrel{g^{\ell} h}{\to} Ad_h g).
$$ 

=--

### Hochschild cohomology and cyclic cohomology

[[quasicoherent ∞-stack]]s on $\mathcal{L}X$ form the [[Hochschild cohomology|Hochschild homology]] object of $X$ (if the axioms of [[geometric function theory]] are met) as described there. The circle acton on $\mathcal{L}X$ induces differentials on these.

> ... details to be written, but see [[Hochschild cohomology]] and [[cyclic cohomology]] for more.




## Examples 

### Free topological loop spaces

In [[Top]] the notion of free loop space objects reproduces the standard notion of topological [[free loop space]]s.

### Details for $\mathcal{L} \mathbf{B}G$ 
  {#LoopsInBG}

Let the ambient [[(∞,1)-category]] be [[∞Grpd]], let $G$ be an ordinary [[group]] and $\mathbf{B}G$ its one-object [[delooping]] [[groupoid]]. 

+-- {: .num_prop}
###### Proposition

We have that the [[loop groupoid]]

$$
  \mathcal{L} \mathbf{B}G \simeq G//_{Ad} G
  \,,
$$

the [[action groupoid]] of the adjoint action of $G$ on itself.

=--


+-- {: .proof}
###### Proof

We spell this out in full pedestrian detail, as a little exercise in computing [[homotopy pullback]]s.

We have that the [[path space object]] is $\mathbf{B}G^I = [I,\mathbf{B}G]$ -- the [[functor category|functor groupoid]], where $I$ is the free groupoid $I = \{a \stackrel{\simeq}{\to} b\}$ on the standard [[interval object]] -- which is (by the definition of [[natural transformation]]) the [[action groupoid]]

$$
  \mathbf{B}G^I = G\backslash \backslash G // G
$$

for the action of $G$ on itself, by _inverse_ left and direct right multiplication separately: the naturality square of a [[natural transformation]] defining a morphism $g \stackrel{h_1,h_2}{\to} h_1^{-1} g h_2$ in this groupoid is the commuting square

$$
  \array{
    \bullet &\stackrel{g}{\to}& \bullet
    \\  
    {}^{\mathllap{h_1}}\downarrow && \downarrow^{\mathrlap{h_2}}
    \\
    \bullet &\stackrel{h_1^{-1}g h_2}{\to}& \bullet    
  }
$$

in $\mathbf{B}G = {*}//G$.

The [[pullback]] of the top right corner of the above defining limit diagram is

$$
  \array{
    (G\backslash\backslash G \times 
    G\backslash\backslash G)//G
    &\to& \mathbf{B}G
    \\
    \downarrow && \downarrow^{\mathrlap{(Id,Id)}} 
    \\
    (G\backslash\backslash G//G) \times
    (G\backslash\backslash G//G)
    &\to& \mathbf{B}G \times \mathbf{B}G
  }
$$

identifying the two actions from the right, and then the remaining pullback completing the limit diagram is

$$
  \array{
    G\backslash\backslash (G\times G)//G
    &\to& 
    (G\backslash\backslash G \times 
    G\backslash\backslash G)//G
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{(Id,Id)}{\to}&  
    \mathbf{B}G \times \mathbf{B}G
  }
$$

now identifying also the two actions from the left, so that  $G\backslash\backslash (G\times G)//G$ is the [[action groupoid]] of $G$ acting diagonally on $G \times G$ by multiplication from the left and from the right, separately.

To see better what this is, we pass to an equivalent smaller groupoid (the [[homotopy pullback]] is defined, of course, only up to weak equivalence). Notice that every morphism 
$(g_1,g_2) \stackrel{h_1,h_2}{\to} (g'_1, g'_2)$ 
in $G\backslash\backslash (G\times G)//G$ corresponding to a [[natural transformation]]

$$
  \array{
     \bullet &\stackrel{(g_1,g_2)}{\to}& \bullet
     \\
     {}^{\mathllap{(h_1,h_1)}}\downarrow && \downarrow^{\mathrlap{(h_2,h_2)}}
     \\
     \bullet &\stackrel{(h_1^{-1} g_1 h_2, h_1^{-1} g_2 h_2)}{\to}
     & \bullet
  }
$$

between functors $I\times I \to \mathbf{B}G \times \mathbf{B}G$
may always be decomposed as

$$
  \array{
     \bullet &\stackrel{(g_1,g_2)}{\to}& \bullet
     \\
     {}^{\mathllap{(e,e)}}\downarrow 
     && \downarrow^{\mathrlap{(g_2^{-1}, g_2^{-1})}}
     \\
     \bullet &\stackrel{(g_1 g_2^{-1}, e)}{\to}& \bullet
     \\
     {}^{\mathllap{(h_1,h_1)}}\downarrow 
     && \downarrow^{\mathrlap{(h_1,h_1)}}
     \\
     \bullet &\stackrel{(h_1^{-1}(g_1 g_2^{-1})h_1, e)}{\to}& \bullet
     \\
     {}^{\mathllap{(e,e)}}\downarrow 
     && \downarrow^{\mathrlap{(g'_2,g'_2)}}
     \\
     \bullet &\stackrel{(h_1^{-1}(g_1 g_2^{-1})h_1 g'_2, g'_2)}{\to}& \bullet
  }
  \,.
$$

Staring at this for a moment shows that this is a unique factorization of every morphism through one of the form

$$
  \array{
    \bullet & \stackrel{(g,e)}{\to} & \bullet
    \\
    {}^{\mathllap{k}}\downarrow && \downarrow^{\mathrlap{k}}
    \\
    \bullet & \stackrel{(Ad_k g,e)}{\to} & \bullet    
  }
  \,,
$$

which is naturally identified with a morphism in the [[action groupoid]] $G//_{Ad} G$ of the adjoint action of $G$ on itself.

This means that the inclusion

$$
  G//_{Ad} G 
  \stackrel{}{\hookrightarrow}
  G\backslash\backslash(G \times G)//G
$$

given by this identification
is [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|full and faithful]], and hence an [[equivalence of categories|equivalence of groupoids]].

So in conclusion we have that the free loop space object of the [[delooping]] $\mathbf{B}G$ of a group is

$$
  \mathcal{L} \mathbf{B}G \simeq G//_{Ad}G
  \,.
$$

=--

### Chern character

We describe how the [[Chern character]] of [[vector bundle]]s over $X$ may be realized in terms of the [[cohomology]] of the free loop space object $\mathcal{L}X$.

Assume now $C$ is a nice category of smooth spaces, and let $X$ be an object of $C$.

Consider a [[group object]] $G$ in $C$ and a [[representation]] of $G$ given by a group homomorphism to the [[general linear group]] (in $C$):  $\rho:G\to GL(n;\mathbb{C})$. For instance $G$ could be $GL(n)$ itself and this morphism the identity.

The [[trace]] of the representation $\rho$ is invariant under conjugation in the group and so defnes a map $Tr(\rho): G//_{Ad}G\to \mathbb {C}$ -- a [[class function]]. By the equivalence $\mathcal{L}\mathbf{B}G \simeq G//_{Ad} G$ discussed above, this may be regarded as a [[characteristic class]]

$$
  Tr(\rho(-)) : \mathcal{L}\mathbf{B}G\to \mathbb {C}
$$

on the free loop space of $\mathbf{B}G$.

The [[cocycle]] $g : X\to \mathbf{B}G$ of a $G$-[[principal bundle]] on $X$ transgresses to a cocycle 

$$
  \mathcal{L} g : \mathcal{L}X \to \mathcal{L}\mathbf{B}G
$$

on the free loop space, by the functoriality of the free loop space object construction.

The above [[characteristic class]] of this cocycle is the composite morphism

$$
  Tr(\rho(\mathcal{L}g)) : \mathcal{L}X \to \mathcal{L} \mathbf{B}G \to \mathbb{C}
  \,,
$$

which by the $Ad$-invariance of the [[trace]] is now $S^1$-invariant and hence defines an element in the [[cyclic cohomology]]
$C(\mathcal{L}X,\mathbb{C})^{S^1_C}$ of $X$. 

The Hom-space $C(\mathcal{L}X,\mathbb{C})$ is a model for the graded commutative algebra of complex-valued [[differential form]]s on $X$, with the categorical circle action corresponding to the [[de Rham complex|de Rham differential]]. Hence $C(\mathcal{L}X,\mathbb{C})^{S^1_C}$ is a model for closed forms and maps to [[de Rham cohomology]] $H_{dR}^\bullet(X)$ of $X$. If the [[de Rham theorem]] holds for $X$ in $C$, then this may be identified with the real cohomology $H^\bullet(X,\mathbb{R})$.



In the case that $G=GL(\infty;\mathbb{C})$, the compatibility of the trace with [[direct sum]]s and [[tensor product]]s of [[vector bundle]]s over $X$ makes the above construction a [[ring]] homomorphism $K(X)\to H_{dR}(X)$ from the [[topological K-theory]] of $X$ to [[de Rham cohomology]], hence a very good candidate to being the [[Chern character]] 

( _to be completed..._ )


### Isotropy of a topos

The [[isotropy group of a topos]] is its free loop space object in the 2-category [[Topos]].


## Related concepts

* [[loop space object]], **free loop space object**,

  * [[delooping]]

  * [[loop space]], [[free loop space]], [[derived loop space]]


* [[suspension object]]

  * [[suspension]]






## References
 {#References}

Free loop space objects in the [[(∞,1)-topos]] of [[derived stack]]s on the site of [[differential graded algebra]]s are discussed in

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv](http://arxiv.org/abs/1002.3636))

More information in the topological case is given in:

* [[Ronnie Brown]] _Crossed modules and the homotopy 2-type of a free loop space_, ([arXiv](http://arxiv.org/abs/1003.5617))

which gives complete information on the 2-type of $\mathcal{L}X$ for a space $X$ which is the classifying space of a crossed module of groups. This generalises the above example of  $ \mathcal{L} \mathbf{B}G$. 

[[!redirects free loop space objects]]
