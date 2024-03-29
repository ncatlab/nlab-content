[[!redirects fundamental (∞,1)-category]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In analogy to how a [[topological space]] has a [[fundamental ∞-groupoid]], a [[directed space]] has a fundamental [[(∞,1)-category]]

## Definition


### Directed topological spaces

+-- {: .un_defn}
###### Definition

By a **[[directed space|directed topological space]]** we here mean specifically a pair $(X,D)$ consisting of 

* a [[topological space]] $X$;

* a subset $D \subset X^{[0,1]}$ of [[continuous map]]s $\gamma : [0,1] \to X$ that are are labeled as being _directed_ , 

* such that 

  * for every orientation preserving [[homeomorphism]] $\phi : [0,1] \to [0,1]$ and every directed map $\gamma$ also $\gamma \circ \phi$ is directed;

  *  for any two directed paths $\gamma_1, \gamma_2$ with $\gamma_1(1) = \gamma_2(0)$ also the concatenation

     $$
       [0,1] \stackrel{\times 2}{\to} [0,2]
       \simeq [0,1] \coprod_{*} [0,1]
       \stackrel{(\gamma_1, \gamma_2)}{\to} 
       X
     $$ 
 
     is a directed path.

A morphism $(X_1,D_1) \to (X_2, D_2)$ of directed spaces is a continuous map $X_1 \to X_2$ that takes elements in $D_1$ to elements in $D_2$.

This defines the [[category]] $DTop$ of directed topological spaces.

=--

+-- {: .un_example}
###### Example
**(topological poset)**

For $X$ a topological space equipped with the structure of a [[poset]] on its underlying set, say that $\gamma : [0,1] \to X$ is directed if for all $x \leq y$ in $[0,1]$ we have $\gamma(x) \leq \gamma(y)$ in $X$. 

=--

+-- {: .un_example}
###### Example
**(directed geometric simplex)**
{#DirectedSimplex}

For $\Delta^k_{Top}$ the standard topological $k$-[[simplex]] its _standard directed paths_ are order-preserving maps into its 1-[[simplicial skeleton|skeleton]] (the union of the 1-faces equipped with the evident [[poset]]-structure induced from that on the vertices), such that the endpoints land on vertices.

=--



+-- {: .un_example}
###### Example
**(directed geometric realization)**

For $C$ a [[quasi-category]] its [[geometric realization]] $|C|$ becomes a directed topological space by taking the directed paths to be all maps that factor through its 1-[[simplicial skeleton|skeleton]]: 

$$
  \int^{[k] \in \Delta_{\leq 1}} \Delta^k_{Top} \times C_k 
  \hookrightarrow
  \int^{[k] \in \Delta} 
  \Delta^k_{Top} \times C_k
  =
  |C|
$$

while preserving the canonical order and so that the endpoints land on vertices.

=--

The previous example of the directed topological simplex is the special case of this for $C = \Delta[k]$.

### Fundamental $(\infty,1)$-category

+-- {: .un_def}
###### Definition

The **fundamental $(\infty,1)$-category** of a directed topological space $(X,D)$ is given by the [[quasi-category]] $\Pi(X,D)$ whose [[k-morphism]]s are those continuous maps

$$
  \sigma : \Delta^k_{Top} \to X
$$

that are morphisms of directed spaces with respect to the [standard directed paths](#DirectedSimplex) in $\Delta^k$.

$$
  \Pi(X,D)_k := Hom_{DTop}(\Delta^k_{Top}, (X,D))
 \,.
$$

=--

+-- {: .un_lemma}
###### Lemma

This does indeed define a quasi-category

=--

+-- {: .proof}
###### Proof

Use the standard [[retract]]s $\Delta^k_{Top} \to \Lambda^k_i$ of the topological [[horn]] inclusions $\Lambda^k_i \hookrightarrow \Delta^k$ to fill horns in $\Pi(X,D)$.

For $k \geq 3$ these retracts are the identity on 1-faces, hence trivially preserve the directed paths. For $k = 2$ it is precisely the retract of the _inner_ horn $\Lambda^2_1$ that preserves the directed paths. This is sufficient to satisfy the inner horn filler condition of quasi-categories.


=--

## Properties

+-- {: .un_lemma}
###### Observation


If $X$ is undirected in that _all_ paths are labeled as directed -- $D = X^{[0,1]}$ -- then $\Pi(X,D)$ coincides with the [[fundamental ∞-groupoid]] $\Pi(X)$ of $X$.

=--



## Fundamental $\infty$-categories induced from intervals 

The interest in interval objects is that various further structures of interest may be built up from them. In particular, since picking an interval object $I$ is like picking a notion of _path_, in a category with interval object there is, under mild assumptions, for each object $X$ an [[infinity-category]] $\Pi_I(X)$ -- the fundamental $\infty$-category of $X$ with respect to $I$ -- whose [[k-morphism]]s are $k$-fold $I$-paths in $X$.

There are different ways to make this precise and realize it in detail. The main distinction is whether one uses

* an [[algebraic definition of higher category]]

or

* a [[geometric definition of higher category]].

We describe an algebraic version in terms of [[Trimble n-category|Trimble omega-categories]] and then a geometric version in terms of [[cubical object]]s and [[simplicial object]]s.

### Fundamental algebraic $\infty$-categories 

The collection of objects 
$\{ {}_{pt}[I, I^{\vee n}]_{pt}\}_{n \in \mathbb{N}}$ in a category with interval object naturally comes equipped with the structure of an [[operad]]: this is the tautological co-[[endomorphism operad]] on the object $I$ in the symmetric closed monoidal category of [[bi-pointed object]]s from $pt$ to $pt$. 

This induces in turn for all objects $X \in V$ on the object $[I,X]$ the structure of an operad, which is naturally interpreted as an internal $A_\infty$-[[A-infinity-category|category]] structure on

$$
  (X_0 := [pt,X]) 
  \stackrel{s := [\sigma,X]}{\leftarrow}  
  [I,X] 
  \stackrel{t := [\tau, X]}{\to} (X_0 := [pt,X])
  \,.  
$$

This internal $A_\infty$-category is denoted 

$$
  \Pi_1(X)
$$

and interpreted as the [[fundamental groupoid]] or rather, in general, the [[fundamental category]] of the object $B$ with respect to the interval object $I$ -- all internal to $V$.

Moreover, by iterating this process as described at [[Trimble n-category]] one should obtain, if everything goes through, on $X$ the structure of a [[Trimble n-category|Trimble]] $\omega$-[[infinity-category|category]] and indeed a functor

$$
  \Pi_\omega : V_0 \to Trimble \omega Cat
  \,.
$$

(... to be continued ...)

+-- {: .un_remark }
###### Remarks

* The condition that all ${}_{pt}[I, I^{\vee n}]_{pt}$ are contractible is the _coherence condition_ on all composition operations. 

* The above is _not_ demanding that the interval object $I$ itself is is weakly equivalent to the point. If it is, then $\Pi_1(X)$ is indeed a [[fundamental groupoid]]. If it is not, then $\Pi_1(X)$ may just be a [[fundamental category]].

* If $X_0$ has a notion of [[path object]] one may consider imposing the condition that $[I,X]$ is a path object of $X$ for all $X$. Similarly, if $V_0$ has a [[cylinder functor]], one may consider imposing the condition that it is given by $-\otimes I$.

=--


### Fundamental geometric $\infty$-categories {#FundGeomInftCat}

Let $C$ be a category with finite [[limit]]s and (plain) interval object $ {*} \stackrel{0}{\to} I \stackrel{1}{\leftarrow} {*}$, where ${*}$ denotes the [[terminal object]].

This may or may not come with further structures and properties as discussed in the definitions above. For the following however no more than that is neceesray.

Recall that the **cube category** is the initial strict [[monoidal category]] $(M, \otimes, I)$ equipped with an object $int$ together with two maps $i_0, i_1: I \to int$ and a map $p: int \to I$ such that $p i_0 = 1_I = p i_1$. 

In a tautological way, $I$ induces a [[cocubical object]] in $C$, a [[functor]] 

$$
  \Box_I : \Box \to C
$$

from the [[cube category]] $\Box$ to $C$. This sends the abstract interval object $int$ that the [[cube category]] is freely generated from to the given $I$, and sends $int^{\otimes n}$ to the $n$-cuber $\Box_I^n := I^{\times n}$.

For every object $X \in C$ homming cubes into $X$ thereby produces a [[cubical set]]

$$
  X^{\Box^\bullet_I} : int^n \mapsto C(\Box_I^n,X)
  \,.
$$

One tends to want to regard this as the cubical incarnation of the fundamental $\infty$-category of $X$ with respect to the notion of path given by $I$.

However, while cubes are nice for many purposes, it is a sad fact of life that the [[homotopy theory]] for cubical structures (while certainly it does exist in full beauty in principle) is much less well developed to date (maybe that will change in the future) than that of [[simplicial object|simplicial]] structures. For many purposes in [[higher category theory]], therefore, it will be useful to take a slightly different perspective on $X^{\Box}$, without essentially changing it.

In fact, there is also naturally the structure of a  [[cosimplicial object]] of the collection $I^\times \bullet$ of $I$-cubes. This differs from the cubical structure only in were precisely one injects the boundaries into an $I^{\times n}$

+-- {: .un_defn}
###### Definition (cosimplicial object induced from interval object)

Given a cartesian interval object $I \in C$, define a [[cosimplicial object]]

$$
  \Delta_I : \Delta \to C
$$

as follows:

* the object in degree $n$ is the $n$-fold [[product]] of $I$ with itself:

  $$
    \Delta_I^n := I^{\times n}
  $$
  
* the degeneracy map $\sigma_i : \Delta_I^{n+1} \to \Delta_I^n$ is given by
  projecting out the $(i+1)$-factor:
  
  $$
    \sigma_i := p_1 \times p_2 \times \cdots \times p_i \times p_{i+2} \times p_{i+3}
        \times \cdots \times p_{n+1}
  $$
  
* the face map $\delta_i : \Delta_I^{n} \to \Delta_I^{n+1}$ is given

  * for $i = n+1$ by inserting $0$ in the $(n+1)$-factor:
  
    $$
      \delta_{n+1} := p_1 \times \cdots \times p_{n} \times 0
    $$
    
  * for $i = 0$ by inserting $1$ in the $0$-factor:
  
    $$
      \delta_0 = 1 \times p_1 \times \cdots \times p_2
    $$
    
  * for $0 \lt i \lt n+1$ by duplicating the $i$-factor:
  
    $$
      \delta_i := p_1 \times \cdots \times_{p_{i-1}} 
        \times p_i \times p_i \times p_{i+1} \times \cdots \times p_n
    $$

=--



+-- {: .un_prop}
###### Proposition

The maps defined this way indeed satisfy the [[simplicial identities]].

=--

+-- {: .proof}
###### Proof

This is straightforward to check, if a little tedious due to the many case distinctions.

=--


+-- {: .un_remark}
###### Remark (unwrapping the definition)

It may be helpful to unpack the above definition a bit.

* The two faces of $\Delta_I^1$ are just the "boundary points" of the interval itself.

  * $(\delta_0 : {*} \to I) = (1 : {*} \to I)$

  * $(\delta_1 : {*} \to I) = (0 : {*} \to I)$

* The face maps of $\Delta^2_I$ may be depicted as follows:

  $$
    \delta_2 : 
    \array{
      I &\times& I 
      \\
      \uparrow^{Id} && \uparrow^{0}
      \\
      I &\times& {*}
    }
    \,,
    \;\;\;\;\;
    \delta_1 : 
    \array{
      I &\times& I
      \\
      & \uparrow^{Id \times Id} 
      \\
      & I
    }
    \,,
    \;\;\;\;\;
    \delta_0 : 
    \array{
      I &\times& I 
      \\
      \uparrow^{1} && \uparrow^{Id}
      \\
      {*} &\times& I
    }
  $$

  Therefore $\delta_1$, being a diagonal morphism (cartesian [[pairing]] of an [[identity]] with itself),
  literally identifies the **diagonal** in the "square" $I \times I$ as the 1st 1-dimensional boundary.

=--

+-- {: .un_remark}
###### Remark 
**([[collars]])**

This construction gives "collared simplices" in much the same sense as in [[collar|collared]] [[cobordism]] and in [[A1-homotopy]]: 

there is no condition that the morphisms $0,1  : {*} \to I$ "hit a boundary point" -- whatever that may mean
 in $C$ -- of $I$. For instance in a [[lined topos]] $I$ is canonically chosen to be the given line object and will hence typically "extended indefinitely" beyond these points. 

An example of this in practice is the [[A1-homotopy theory]] of schemes -- there is no exact analogue of the interval (with boundary points) in an algebraic setting, but the [[affine line]] $A^1$ together with the canonical points 0 and 1 is an interval object.
 
So $I$ need not "look" much like a 1-simplex, but the _choice of boundary points_ $\delta_1 = 0 : {*} \to I$ and $\delta_0 = 1 : {*} \to I$  allows us to regard
it as an interval for all practical purposes.
 
Similarly and more generally what the above construction manifestly defines are _cubes_ $I^n$ built from $I$. But then the simplicial choice of  boundaries inside these cubes allows to think of them as just the simplices
 "sitting inside" these cubes.
 
All these statement become precise for specific typical choices of the ambient category $C$, discussed in the examples below.

An important aspect is that once the cosimplicial object of _collared simplices_ $\Delta_I$ is used to form [[simplicial object]]s $\Pi(X) := [\Delta^\bullet_I,X]$ (discussed below) and when these are interpreted as [[model category|models]] for [[∞-groupoid]]s, then **the collars disappear**: they are part of the model, but, roughly, don't affect the equivalence class of the object that this model models.

For instance with ${*}\amalg {*} \stackrel{0, 1}{\to}\mathbb{R}$ used as the interval in [[Top]], a _path_ in a [[topological space]] $X$ is an entire curve $\gamma : \mathbb{R} \to X$, but two such paths $\gamma_1,\gamma_2$ are composable already when $\gamma_1(1) = \gamma_2(0)$, irrsepctive of how $\gamma_1$ extends $\gt 1$ and irrsepctive of how $\gamma_2$ extends $\lt 0$.

Moreover, the composite-up-to-homotopy of these two paths is an entire surface $\mathbb{R}^2 \to X$ in $X$, but what only matters for this surface qualifying as a compositor of $\gamma_1 and \gamma_2$ is that its $\delta_2$-segment $\{(x,y) \in \mathbb{R}^2 | 0 \leq x \leq 1, y = 0\}$ and its $\delta_0$segment $\{(x,y) \in \mathbb{R}^2 | 0 \leq y \leq 1, x = 0\}$ coincide with the corresponding segments in $\gamma_1$ and $\gamma_2$.

More on this in the following example section.

=--


#### Example: standard intervals, cubes and simplices in $Top$ and $Diff$ 

Let $X = $ [[Top]] or $C = $ [[Diff]] be the category of [[topological space]]s
or of [[manifold]]s.


A standard choice of interval object in $C$ is $I = [0,1] \subset \mathbb{R}$
with the obvious two boundary inclusions $0,1 : {*} \to [0,1]$.

But another possible choice is to let $I = \mathbb{R}$ be the whole
real line, but still equipped with the two maps $0,1 : {*} \to \mathbb{R}$,
that hit the $0 \in \mathbb{R}$ and $1 \in \mathbb{R}$, respectively.

Either of these two examples will do in the following discussion. 
The second choice is to be thought of as obtained from the first choice
by adding "infinitely wide collars" at both boundaries of $[0,1]$. While
${*} \stackrel{0}{\to}[0,1]
\stackrel{1}{\leftarrow} {*}$ may seem like a more natural choice for a representative of the 
idea of the "standard interval", the choice ${*} \stackrel{0}{\to} \mathbb{R}
\stackrel{1}{\leftarrow} {*}$ is actually more useful for many 
[[category theory|abstract nonsense]] constructions. 

But since it is hard to draw the full real line, in the following we depict the situation for the choice $I = [0,1]$.

Then for low $n \in \mathbb{N}$ the above construction yields this

* $n=0$ -- here $\Delta_I^0 = I^{\times 0} = {*}$ is the [[point]]. 

* $n=1$ -- here $\Delta_I^1 = I^{\times 1} = I$ is just the interval itself

  $$
    \array{
      (0) \to (1)

    }
  $$
  
  The two face maps $\delta_1 {*} \to I$ and $\delta_0 : {*} \to I$ pick
  the boundary points in the obvious way. The unique degeneracy map 
  $\sigma_0 : I \to {*}$ maps all points of the interval to the single point
  of the point. 

* $n=2$ -- here $\Delta_i^2 = I^{\times 2} = I \times I$ 
  is the **standard square**

  $$ 
    \array{
      (0,1) &\to& (1,1)
      \\
      \uparrow && \uparrow
      \\
      (0,0) &\to& (1,0)
    }
  $$

  But the three face maps $\delta_i : I \to I\times I$ of the cosimplicial
  object $\Delta_I$ constructed above don't regard the full square here, but
  just a triangle sitting inside it, in that pictorially they 
  identify $(\Delta_I^1 = I)$-shaped boundaries in $I \times I$ as follows:
  
  $$ 
    \array{
      (0,1) &\to& (1,1)
      \\
      \uparrow &^{= \delta_1(I)}\nearrow& \uparrow^{ = \delta_0(I)}
      \\
      (0,0) &\stackrel{= \delta_2(I)}{\to}& (1,0)
    }
  $$
  
  (here the arrows do not depict morphisms, but the standard topological interval, 
  i don't know how to typeset just lines without arrow heads in this fashion!)
  
* $n=3$ -- here $\Delta_i^3 = I^{\times 3} = I \times I \times I$ 
  is the **standard cube**
  
  +-- {: .un_example}
  ###### Exercise
  Insert the analog of the above discussion here
  and upload a nice graphics that shows the standard cube and how the
  cosimplicial object $\Delta_I$ picks a solid tetrahedron inside it.
  =--

As a start, we can illustrate how there are 6 3-simplices sitting inside each 3-cube.

<img src="http://ncatlab.org/nlab/files/3simplex_in_3cube.jpg" width = "550"/>

Once you see how the 3-simplices sit inside the 3-cube, the facemaps can be illustrated as follows:

<img src="http://ncatlab.org/nlab/files/3simplex_facemaps.jpg" width = "550"/>

Note that these face maps are to be thought of as maps into 3-simplices sitting inside a 3-cube.


### Fundamental little 1-cubes space induced from an interval {#Dendroidal}

+-- {: .query}

[[Urs Schreiber]]: something I am thinking about...

=--

The following is supposed to give an [[(∞,1)-operad]]ic incarnation of the notion of fundamental $\infty$-groupoid induced from an interval object. It should resemble a _geometric operadic_ version of the _algebraic operadic_ version described further above.

Let $\Omega^p$ be the category of planar [[tree]]s, so that a [[presheaf]] on $\Omega^p$ is a planar [[dendroidal set]]. 

Given an interval object ${*} \stackrel{0}{\to} I \stackrel{1}{\leftarrow} {*}$ in a category $C$, assume one isomorphism 
$\phi_n \in [I,I^{\vee n}]$ for each $n$ has been chosen.


Then there is a planar co-dendroidal object $\Omega^p_C : \Omega^p \to C$ in $C$ given by:

* a tree $T$ with $n$ leaves is sent to $I^{\vee n}$ 

  (we think of the
  $k$-th copy of $I$ here as being associated to the $k$th 
  leaf of the planar tree);

* every degeneracy map 
  is sent to the corresponding identity morphism

  (this corresponds to the fact that the co-dendroidal object encodes
  no nontrivial unary (co)operations, only the $(n \gt 1)$-ary
  operations encoded nontrivial infomation);

* an _outer face map_ on an $n$-ary vertex is the identity on all 
  copies of $I$ corresponding to the unaffected leaves and is 
  $\phi_n$ on the affected leaf;

* an _inner face map_ that contracts a $k_1$-ary vertex with 
  a $k_2$-ary one is the identity on all unaffected leaves and is 
  on the affected leaves the composition 

  $$
    I^{\vee (k_1+k_2)}
    \stackrel{\phi_{k_1+k_2}^{-1}}{\to}
    I
    \stackrel{\phi_{k_1}}{\to}
    I^{\vee k_1}
    \stackrel{(Id, \cdots, Id,\phi_{k_2},Id, \cdots, Id )}{\to}
    I^{\vee (k_1+k_2)}
    \,.
  $$

**Example**. In [[Top]] with $I = [0,1]$ the standard interval, 
and $I^{\vee n} = [0,n]$ let $\phi_n : [0,1] \to [0,n]$ be the map
given by multiplication of real numbers by $n$.

Then for the planar tree $T_1$ given by

$$
  T_1 = 
  \left[
    \array{
      \searrow && \swarrow
      \\
      & \bullet 
      \\
      && \searrow && \swarrow
      \\
      &&& \bullet
      \\
      &&& \downarrow
    }
  \right]
$$ 

the inclusion of the tree $\left[\downarrow\right]$ into $T$ given by identifying it with its root is sent to the map $f : [0,1] \to [0,3]$ that is the composite of the map $(-)\cdot 2 : [0,1] \to [0,2]$ wth the map $h : [0,2] \to [0,3]$ that is multiplication by two on $[0,1]$ and addition by 1 on $[1,2]$.

On the other hand the inner face map from

$$
  T_2 =
  \left[
    \array{
      \searrow & \downarrow & \swarrow
      \\
      & \bullet
      \\
      & \downarrow   
    }
  \right]
$$

to $T_1$ corresponds to the map $[0,3] \to [0,3]$ that is the composite of the map $(-)/3 : [0,3] \to [0,1]$ with the above map $[0,1] \to [0,3]$.

Now for $X \in C$ any object, we obtain the planar [[dendroidal set]]

$$
  Paths X : T \mapsto Hom_C( \Omega^p_C[T], X )
  \,.
$$

It assigns to any tree with $n$ leaves the hom-set  $Hom(I^{\vee n},X)$. This we can think of as the set of standard parameterized paths of parameter length $n$ in $X$. The action of tree morphisms $T_1 \to T_2$ on these sets is the _reparameterization_ of these paths as encoded in the tree structure. 

In particular, we have the dendroidal set $Paths(I)$ of the interval object itself. This is something like the [[little cubes operad|little 1-cubes]] operad as seen by $I$. 

I think for every $X$ there is an evident morphism of dendroidal sets

$$
  Paths X \to Paths I
  \,.
$$

The component over the tree $T$ sends all of $(Paths X)(T) = Hom_C(I^{\vee n},X)$ to ....

For $X$ a [[pointed object]], there is the sub-dendroidal set $\Omega X \subset Paths X$ of paths whose endpoints map to the basepoint.






## Related concepts

* [[fundamental groupoid]], [[fundamental ∞-groupoid]]

* [[fundamental category]], **fundamental $(\infty,1)$-category**


## References 

The above definition, evident as it may be, does not seem to be in the literature. Articles that do discuss proposals for aspects of fundamental higher categories of directed spaces include

* [[Marco Grandis]], _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))

* [[Tim Porter]], _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88--100.

* [[Tim Porter]], _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))

The [[simplicially enriched categories]] obtained from a directed space according to the latter have as morphisms directed paths, and as 2-morphisms _directed homotopies_  (paths of directed paths). This is in contrast to the above definition, where the 2-cells away from their boundary are unconstrained.

Accordingly it seems that the definition by Porter produces indeed not a Kan-complex enriched category (a model for an $(\infty,1)$-category) but a quasi-category-enriched category, hence actually a model for an [[(∞,2)-categories]], a candidate for the _fundamental $(\infty,2)$-category_ of a space. Generally, in the fundamental [[(∞,n)-category]] the $(k \leq n)$-cells should be directed maps, and the $k \gt n$-cells be otherwise unconstrained.