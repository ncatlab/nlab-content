
+-- {.standout}

  On the formalization of the process of [[quantization]] -- by [[category theory|abstract nonsense]] -- from classical [[∞-model]] data to the corresponding [[quantum field theory]] .

=--

# Contents #


1. [Background and motivation](#background)

1. [General procedure](#generalprocedure)

   1. [terminology](#terminology)

      1. [the notion of space](#space)

      1. [the notion of path](#path)

      1. [the notion of trajectory](#trajectory)

      1. [the notion of background field](#backgroundfield)

      1. [the notion of action functional](#actionfunctional)

      1. [the notion of section and state](#state)

   1. [the quantum propagation map](#propagation)

1. [Examples](#examples)

   1. [the electromagnetically charged particle](#eleccharged) 

   1. [Dijkgraaf-Witten theory](#dw)

   1. [Yetter model](#yetter)


# Background and motivation {#background} 

The search is on for the abstract formalization of the process of _[[quantization]]_ -- the process that reads in a "classical field theory" -- for instance presented in form of a [[gauge theory]] or in form of a [[∞-model]] background field data -- and spits out the corresponding [[quantum field theory]].

+-- {.standout}

There is an open problem of mathematical (-[[physics]]) model building: 

* what is the true formalism behind [[quantization]]?  

One that is to quantization as, say, [[symplectic geometry]] is to [[Hamiltonian mechanics]]?

The formalism of [[FQFT]] clearly suggests that the fundamental description of [[quantization]] is some natural operation on higher functors.

=--



While for various aspects and facets of this question there are well-developed formalisms -- such as [[geometric quantization]] or [[deformation quantization]] or [[BV theory]] -- a full answer is certainly still missing, not the least because the full formalization of the _question_ itself has still to be established.

Considerable progress on this formulation of the question has been achieved with the formalization and proof of the [[cobordism hypothesis]] in _[[On the Classification of Topological Field Theories]]_ by [[Jacob Lurie]]. This at least indicates what the _result_ of any full quantization procedure should be in that it clarifies what exactly a [[TQFT]] [[FQFT]] is: a morphism from the [[(∞,n)-category of cobordisms]] $Z : Bord_n \to C$.

In _[[On the Classification of Topological Field Theories]]_ Jacob Lurie indicates some first towards finding a similar formalization of "classical field theory" (in terms of his $(\infty,n)$-categories of "families") and a systematic procedure for turning the classical theory into the quantum theory. These thoughts were further developed in the article _[TFT from compact Lie groups](http://arxiv.org/abs/0905.0731)_ . But for the moment, that, too, remains rather sketchy.

For the purpose of the present entry this indication of a quantizaton proposal by Lurie et al. mainly serves as a reference for the idea itself that a formalization of something interesting is to be sought here, and of the kind of [[category theory|abstract nonsense]] answer one hopes to find. We will however discuss a somewhat different-looking approach. It may well be related to the Lurie-et al proposal in the end, but for the time being we shall not concentrate on that relation.

Rather, the approach for a formalization of the quantization  procedure that shall be discussed at this entry here is more in the spirit as indicated to some extent in the work of [[David Ben-Zvi]] et. al, which is described in some detail at [[geometric ∞-function theory]]. This is essentially based on the idea that a [[quantum field theory]] is obtained from a [[∞-model]] target space object $X$ by homming [[extended cobordism]] [[cospan]]s $\Sigma_in \to \Sigma \leftarrow \Sigma_{out}$ into the target object and then pull-pushing [[geometric function object]]s through the resulting [[span]]s of configuration space objects $[\Sigma_{in},X] \leftarrow [\Sigma,X] \to [\Sigma_{out},X]$. 

The resulting pull-push operation is an example or a generalization of what [[John Baez]] discusses under the term [[groupoidification]]. David Ben-Zvi et al would speak of [[geometric function theory]].

The main result of David Ben-Zvi et. al.'s work on this approach is that they point out that as soon as the [[geometric function object]] one uses satisfies the two [[geometric ∞-function theory|fundamental theorems of geometric infinity-function theory]], a considerable amount of rich structure that has in parts been known by itself gets unified into one coherent elegant story: the nature of partition functions (i.e. traces), of centers, of Hochschild (co)homology, Deligne-Kontsevich-statements, etc. all are understood by means of a suitable [[geometric function theory]] as induced from the underlying geometry of configuration space objects $[\Sigma,X]$ as well as the [[loop space object]]s of $X$.

Here in this entry the aim is to discuss in detail aspects and models for the quantization procedure that is suggested by applying [[geometric function theory]] to [[∞-model]] backgrounds.

But more precisely, the premise of the discussion here is that a fundamental understanding of the situation is obtained after regarding seriously the fact that

1. background fields are not just encoded by the [[cohomology]] with coefficients in the target space object $X$, but by the corresponding [[differential cohomology]];

1. and that the functorial notion of the [[FQFT]] that one wants to obtain suggests that these differential cocycles themselves are encoded functorially, as described at [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]].

This means that we shall take the classical structure $\nabla$ which the sought-after quantization procedure is supposed to send to an [[FQFT]] $Z_\nabla : Bord_n \to C$ to be, essentially, a functor

$$
  \nabla : \Pi_n(X) \to A
$$

from some [[path n-groupoid]] of $X$ to some coefficient object $A$. 

Here the [[k-morphism]]s in $\Pi_n(X)$ are generated from the existing $k$-morphisms in $X$ as well as the $k$-dimensional smooth paths in $X$. The functor $\nabla$ on this encodes the _parallel transport_ of a [[connection on a bundle|connection]] on a [[principal ∞-bundle]] over $X$: this assignment of [[k-morphism]]s in $A$ to $k$-dimensional paths in $X$ is the assignment of the **classical action** to trajectories in $X$.

More precisely, this is the classical action assigned to topologically disk-shaped $k$-paths. The full classical action of a classical [[∞-model]] quantum field theory is an extension of $\nabla$ 

$$
  \array{ 
    \Pi(X) \stackrel{\nabla}{\to}  A &\to& V
    \\
    \downarrow & \nearrow_{\exp(S_\nabla)}
    \\
    Bord(X)
  }
$$

from disk-shaped cobordisms to _all_ [[cobordism]]s in $X$ (possibly and usually after an extension of the codomain to some new codomain $V$). This extension $\exp(i S_\nabla)$ knows not just the parallel transport, but also the **holonomy** of the classical background field.

The question to be analyzed here is how this classical action $\exp(i S_\nabla) : Bord_n(X) \to F$ transmutes systematically to an [[FQFT]] $Z_\nabla : Bord_n \to C$ on abstract bordisms (possibly with extra structure, if we pass from [[TQFT]] to richer theories like [[CFT]]). This step should be the **[[path integral]]**: 

in some way the assignment of $Z_\nabla$ to a [[cobordism]] $\Sigma$ is expected to be obtained by "summing" in some way the value of $\exp(S_\nabla)$ on elements in the fiber of the [[forgetful functor]] $Bord_n(X) \to Bord_n$ over $\Sigma$, i.e. over all possible ways to map $\Sigma$ into $X$ -- the sum of $\exp(S_\nabla(\phi))$ over all _paths_ or _field configurations_  $\phi : \Sigma \to X$.

The basic idea that we shall follow has been sketched to some extent in the notes

* [[schreiber:Nonabelian cocycles and their sigma model QFTs]]. 

These notes in turn have grown out of the blog entry [An Exercise in Groupoidification -- the path integral](http://golem.ph.utexas.edu/category/2008/06/an_exercise_in_groupoidificati.html) from which the present entry draws its name. We hope to refine the discussion a bit more now, provide more details and more systematics.


# General procedure {#generalprocedure} 


This section describes the general formalism that we want to study as a candidate for (aspects of) a fundamental [[category theory|abstract-nonsense]] description of [[quantization]]. The next section then picks special (simple) cases and works out the action of the abstract machinery on these.

+-- {.standout}

In rough outline the procedure is this:

* In a context $\mathbf{H}$ of sufficiently general spaces;

* we extend the _background field_ parallel transport $\nabla : \Pi(X) \to A$ to an action functional $\exp(S_\nabla) : Bord(X) \to V$.

* Then for each [[cobordism]] $\Sigma$ the component of the action functional $\exp(S_\nabla)|_\Sigma : [\Sigma,X] \to V$ on $\Sigma$ defines a total $V$-[[principal infinity-bundle|bundle]] space $E_\Sigma$;

* the _points_ of $E_\Sigma$ are the Dirac-$\delta$-distributional _sections_ or _quantum states_   

  -- these are picked and added up by the objects in the [[over category]] [[examples for geometric function objects|geometric function object]] $C(E_x) := \mathbf{H}/{E_x}$.

* the quantum propagation along a [[cobordism]] [[cospan]] $\Sigma_{in} \to \Sigma \leftarrow \Sigma_{out}$ is the pull-push of [[geometric function theory]]/[[groupoidification]] 

  $$
    Z_\nabla(\Sigma) : C(E_{\Sigma_{in}})
      \stackrel{out_* in^*}{\to}
      C(E_{\Sigma_{out}})
  $$

  through the corresponding [[span]] $E_{\Sigma_{in}} \leftarrow E_{\Sigma} \to E_{\Sigma_{out}}$ of total spaces.

=--



# terminology {#terminology}

The definition of quantum propation defined by a classical background field that we describe [below](#propagation) is quite simple once we suitably organize the material by establishing a bit of terminology.


## the notion of space {#space}



We need to talk about various _spaces_ of sorts: 

* a space $X$ that is the **target space** -- often, but not always, to be interpreted as physical spacetime -- in which the $d$-dimensional object propagates -- for $d=0$ for instance a point particle such as an _electron_ -- whose dynamics we want to encode.

  This space might be just a [[manifold]] but we want to allow it to be a kind of space a bit more general than that, for instance an [[orbifold]].

  When we are describing [[gauge theory]] the target space is smooth refinement of a [[classifying space]] $\mathbf{B}G$.

  When we are describing finite gauge theory such as [[Dijkgraaf-Witten theory]], the target space is just the one-object [[groupoid]] $\mathbf{B}G$ that is the [[delooping]] of the gauge group $G$. 

* Moreover, for each $(d+1)$-dimensional [[manifold]] $\Sigma$ we need a **path space** or **configuration space** $[\Sigma,X]$ of maps from $\Sigma$ into $X$.

The [[category theory|general abstract nonsence]] for dealing with general spaces of this sort is that of [[space and quantity]]. As described at [[motivation for sheaves, cohomology and higher stacks]], this leads one to describe a space as an [[∞-stack]] on some [[site]] $S$.

In the simplest case, which the reader should keep in mind, the [[site]] in question is the [[point]] and an [[∞-stack]] on it is just an [[∞-groupoid]]. In turn in simple cases of this, which the reader should still keep in mind, this [[∞-groupoid]] will be just a [[groupoid]] or at most a [[2-groupoid]].

Whichever choice one makes, the collection of all such generalized spaces modeled on a certain [[site]] $S$ forms an [[(∞,1)-topos]] $\mathbf{H}$. 

Despite -- possibly -- its appearance, the reader should take this statement as suggesting an immense simplification instead of a huge complification: the language of [[(∞,1)-topos]] is a user interface that makes pretty sophisticated and rich notions of generalized spaces have the same look-and-feel as just plain [[topological space]]s. It's the inner workings of the formalism that will take of things coming out right even when we talk about richer objects.

In particular, it is the machinery of [[models for ∞-stack (∞,1)-toposes]] that provides all the tools for actually performing the operations that we shall consider. The reader unfamiliar with that will suffer little loss from concentrating his or attention on the toy examples where all "spaces" involved are finite [[groupoid]]s and trust that everything goes through analogously also in the other examples.


## the notion of path {#path}


With an [[(∞,1)-topos]] $\mathbf{H}$-fixed we are in a context that allows us to study [[cohomology]]. A classical background field on a target space $X$ is in parts a cocycle on $X$ with values in some coefficient object $A \in \mathbf{H}$.

But, as indicated above, it is actually, more: it is a _[[schreiber:Differential Nonabelian Cohomology|differential cocycle]]_ on $X$: something that depends not just on $X$ itself, but also on a notion of paths in $X$.

To encode this we may pick a [[simplicial object|cosimplicial object]]

$$
  \Delta_H : \Delta \to \mathbf{H}
$$

in our $(\infty,1)$-category of spaces, that encodes which object in $\mathbf{H}$ models the standard $k$-[[simplex]] regarded as a space. For instance if $\mathbf{H}$ is the [[(∞,1)-topos]] of [[Lie ∞-groupoid]]s modeled by [[∞-stack]]s on [[Diff]], we would take $\Delta_H^n$ to be the standard $n$-simplex $\Delta^n_H \subset \mathbb{R}^n$ regarded as a smooth [[manifold]] in the standard way.

Then denote the space of disk-shaped $k$-dimensional paths in $X$ by 

$$
  [\Delta_H^n,X]
  \,.
$$ 

These spaces glue together to the [[path ∞-groupoid]]

$$
  \Pi(X) := \lim_\to [\Delta_H^\bullet, X]
  \,.
$$

This is an [[∞-groupoid]] whose [[k-morphism]] are generated from the original $k$-morphisms of $X$ and the $k$-dimensional path $\phi : \Delta^k_H \to X$.

For instance if $X = Y//G$ is a global [[orbifold]], the 1-morphisms in $\Pi(X)$ are generated from smooth paths $\gamma: y_1 \to y_2$ in $Y$ as well as orbifold jumps $g : y_1 \to g(y_1)$ subject to the relation

$$
  \array{
    y_1 &\stackrel{g}{\to}& g(y_1)
    \\
    \downarrow^{\gamma} && \downarrow^{g(\gamma)}
    \\
    y_2 &\stackrel{g}{\to}& g(y_2)
  }
  \,.
$$

Or if $X = C(Y)$ is realized as the [[Cech nerve]] of some [[Cech cover]] $(U = \coprod_i U_i) \to Y$ then $\Pi(X)$ is generated from paths $(\gamma,i) : (y_1,i) \to (y_2,i)$ in $U_i$ for all $i$ and transitions $(y,i) \to (y,j)$ for all $y \in U_i \cap U_j$ subject to the condition

$$
  \array{
    (y_1,i) &\stackrel{}{\to}& (y_1,j)
    \\
    \downarrow^{(\gamma,i)} && \downarrow^{(\gamma,j)}
    \\
    (y_2,i) &\stackrel{}{\to}& (y_2,j)
  }
  \,.
$$


## the notion of trajectory {#trajectory}


More generally, let $D$ be some [[poset]] and specify a functor

$$
  \Sigma_H : D \to \mathbf{H}
  \,.
$$

We think the image of some $k \in D$ under $\Sigma_H$  as the realization in $\mathbf{H}$ of some abstract [[cobordism]] whose boundary component inclusions are the images $\Sigma^j_H \to \Sigma_H^k$ of all morphisms $j \to k$ in $D$.

So $\Sigma_H$ encodes a [[multispan|multi-cospan]] of cobordisms in $H$. In principle $\Sigma_H$ will in general be supposed to range over _all_ cobordisms in some sense, but for our discussion it will be complete sufficient to concentrate on much less. Most of our discussion concerns a handful of cobordisms, usually just two of them and their composites.

In any case, by slight abuse of notation, we shall write

$$
  Bord_\infty(X) := Bord(X) := \lim_\to [\Sigma_H^\bullet, X]
$$

for the ([[homotopy limit|homotopy]]) [[colimit]] over this [[multispan|multi-cospan]] of cobordisms
and speak of the $\infty$-groupoid of **bordisms in $X$**. If we assume that $\Sigma_H$ ranges at least over the disk-shaped cobordisms $\Delta^k_H$ we have a canonical inclusion

$$
  \Pi(X) \hookrightarrow Bord(X)
  \,.
$$


## the notion of background field {#backgroundfield}

A background field that is _flat_ (meaning that it has vanishing [[field strength]]) is a morphism


$$
  \nabla : \Pi(X) \to A
$$

in $\mathbf{H}$.

> The more general situation is described at ..., but need not concern us here for the moment. Its quantization is structurally slightly but not, for our purposes, essentially different from that of the flat case.

This encodes an $A$-[[principal ∞-bundle]] [[connection on a bundle|with connection]]: the value $\nabla : x \mapsto P_x$ over a point is the [[fiber]] of the principal $\infty$-bundle, and the value on a path $\nabla : x_1 \stackrel{\gamma_1}{\to} x_2 \mapsto P_{x_1} \to P_{x_2}$ is the parallel transport along $\gamma$.

In the case that $A = \mathbf{B}G$ is the [[delooping]] of an $\infty$-group $G$, so that $A$ has a unique [[pointed object|point]] $pt_A : {*} \to \mathbf{B}G$ the total space of this [[principal ∞-bundle]] is the ([[homotopy pullback|homotopy]]) [[pullback]] $P$ in

$$ 
 \array{
  P &\to& {*}
  \\
  \downarrow && \downarrow
  \\
  X \simeq [pt,X] &\stackrel{\nabla|_{pt}}{\to}& \mathbf{B}G
 }
  \,,
$$

where $\nabla|_{pt}$ is the component of $\nabla$ (as a morphism out of a colimit) on points in $X$.

We are interested in forming the associated $\infty$-bundle induced by a choice of [[representation]]

$$
  \rho : A \to V
$$

on some [[(∞,1)-category]] $V$. See below for examples.

As a cocycle this is just the composite

$$
  \rho_* \nabla : \Pi(X) \stackrel{\nabla}{\to}
   A \stackrel{\rho}{\to} V
  \,.
$$

This is the _background field_ that encodes the forces acting on the objects propagating in $X$ whose quantum dynamics we seek.

We will often abuse notation and write just $\nabla$ for $\rho_* \nabla$, when the context is clear.

## the notion of action functional {#actionfunctional}

A choice of extension of the parallel transport morphism $\nabla : \Pi(X) \to A$ through the inclusion $\Pi(X) \to Bord(X)$ is the corresponding **action functional** $\exp(S_\nabla)$

$$
  \array{
    \Pi(X) &\stackrel{\nabla}{\to}& V
    \\
    \downarrow & \nearrow_{\exp(S_\nabla)}
    \\
    Bord(X)
  }
  \,.
$$

This extension amounts to choosing (possibly uniquely) _traces_ over parallel transport. 

**example**
Let $\nabla : \Pi(X) \to Vect$ encode the parallel transport in a [[vector bundle]] with connection. And consider the extension to $Bord_1(X)$ with just 1-dimensional cobordisms in $X$. Then the extension amounts to finding a value for $\exp(S_\nabla)$ on the circle. To be functorial and symmetric monoidal, it must be true that the value on the circle is the result of cutting the circle open at any point, evaluating $\nabla$ on the resulting 1-disk-shaped cobordism and then applying the trace on the vector space over the endpoint.

For each cobordism $\Sigma$ the component $\exp(S_\nabla)|_\Sigma$ of the action functional will define a total space of an associated bundle $E_\Sigma$. These are discussed in the next section.


## the notion of section and state {#state}

A _state_ of the quantum theory over a cobordism $\Sigma$ is supposed to be a _[[section]]_ of the bundle $E_\Sigma \to [\Sigma,X]$ over the configuration space $[\Sigma,X]$ of fields on $\Sigma$, where we allow generalized sections that may be distributional. This we define now.

In order to define sections and states,
we need to fix a [[pointed object|point]] in the coefficient object $V$, i.e. a morphism

$$
  pt_V : {*} \to V
$$

from the [[terminal object]] ${*}$ into $V$. The choice of this point determines over which [[monoid]] our quantum theory will be linear:

**definition (ground monoid)**

Given the [[pointed object]] ${*} \stackrel{pt_V}{\to} V$ we say that the respective **ground monoid** is the [[endomorphism|endomorphism monoid]]

$$
  \Omega_{pt} V = End_V(pt_V)
$$

i.e. the [[2-limit|lax pullback]]

$$
  \array{
    \Omega_{pt} V &\to& {*}
    \\
    \downarrow && \downarrow^{pt_V}
    \\
    {*} &\stackrel{pt_V}{\to}& V
  }
  \,.
$$

**example: ordinary linear quantum mechanism**

In the special case that $V = $ [[Vect]] over some ground field $k$ the canonical point is that ground field. Then the "ground monoid" is again canonically identified with the ground field: $End_{Vect_k}(k) \simeq k$. Therefore the name "ground monoid" as a generalization of this situation.


More generally, for $W : {*}\to V$ any other point of $V$, we say that the [[2-limit|lax pullback]]

$$
  \array{
    el_{pt_V}(W) &\to& {*}
    \\
    \downarrow && \downarrow^{pt_V}
    \\
    {*} &\stackrel{W}{\to}& V
  }
$$

is the object of _elements of $W$_ relative to the chosen point.

**example: ordinary vectors**

Again in the special case that $V = $ [[Vect]] with the above standard point, $W \in V$ will be some vector space and $el_{k}(W)$ is the set -- regarded as a [[discrete category]] of its ordinaly elements -- of the vectors in $W$.

Moreover, given the background field differential cocycle or the action functional

$$
  \exp(S_\nabla)  : Bord(X)  \to V
$$

we have the [[2-limit|lax pullback]]

$$
  \array{  
    E &\to& {*}
    \\
    \downarrow && \downarrow^{pt_V}
    \\
    Bord(X) &\stackrel{\exp(S_\nabla)}{\to}&
   V
  }
  \,.
$$

This $E$ is really the [[action groupoid]] of the "[[action]]" of $Bord(X)$ on $V$: it is much like the [[Atiyah Lie groupoid]] of a [[principal bundle]], with the difference that its objects are elements in an associated (not a principal bundle) and its morphism connect only elements in the fibers that are related by parallel transport along the corresponding path down in $X$.

For each component $\exp(S_\nabla)|_\Sigma : [\Sigma,X] \to V$ we get a corresponding lax pullback

$$
  \array{  
    E_{\Sigma} &\to& {*}
    \\
    \downarrow && \downarrow^{pt_V}
    \\
    [\Sigma,X] &\stackrel{\exp(S_\nabla)|_\Sigma}{\to}&
   V
  }
$$

in particular the fiber over $x \in X$ of $E_{pt}$

$$
  \array{
    el_{pt_v}(E_x)
    &\to&
    E_{pt} &\to& {*}
    \\
    \downarrow &&\downarrow && \downarrow
    \\
    {*} &\stackrel{x}{\to}& X
     &\stackrel{\exp(S_\nabla)|_{pt}}{\to}& V
  }
$$

is the fiber of the underlying $V$-$\infty$-bundle over $x$-

**example**

In the case that $V = FinVect$ and $\nabla : \Pi(X) \to Vect$ is a [[vector bundle]] [[connection on a bundle|with connection]] and with the canonical point chosen for $Vect$ as above, this $el_{pt_V}(E_x)$ is simply the fiber of that vector bundle over $x$.

Picking a point $v : {*} \to E_{pt}$ in the total space is like picking a $\delta$-distributional section of $E_{pt} \to X$ with support at $x$ and value $v$ there. Picking two points $v_1 \sqcup v_2   : {*} \sqcup {*} \to E_{pt}$ is naturally interpreted as picking the _sum_ of two such sections.

Picking instead a map $v/k : \mathbf{B}G \to {*} \to E_{pt}$ for $G$ a finite group of cardinality $k$ is like picking a $\delta$-distributional section with value $v$ and dividing its value by $k$.

In light of this, we choose now the [[geometric function theory]] given by [[over category|over categories]] in $\mathbf{H}$.  This is as described at [[examples for geometric function objects]]

$$
  C :=  \mathbf{H}/(-) :   \mathbf{H} \to (\infty,1)Cat
$$

Then for $\Sigma$ a cobordism, a 
a **section** of the background field or **state** of the quantum system over $\Sigma$ is an object 

$$
  \psi \in C(E_{\Sigma})
  \,.
$$


### special case: degroupoidification for $V$-phased groupoids ##

For some choices of $V$ this general notion of section may be _degroupified_ -- to yield an ordinary notion of (still possibly distributional) section.

In the case that $V = FinVect$ we have that $E_x$ is (the [[discrete category]] on the set underlying) the vector space that is the fiber of the background vector bundle over $X$ at $x \in X$.

For $(\psi : \Psi \to E_x) \in C(E_x)$ consider the underlying morphism of plain $\infty$-groupoids and interpret this as the vector

$$
  \sum_{v \in E_x} |\psi^{-1}(v)|\cdot v
$$  

given by the linear combination of all elements $v \in E_x$ weighted by the [[groupoid cardinality]] of the [[∞-groupoid]] sitting over it.


##  the propagation map {#propagation}

In total the above discussion yields, starting from a background field $\nabla : \Pi(X) \to V$, a [[multispan]] of  $\infty$-bundles $E_\Sigma$ over configuration spaces $[\Sigma,X]$.

An an object in the [[over category]] $C(E_{\Sigma}) := \mathbf{H}/E_{\Sigma}$ encodes a -- possibly distributional -- section of $E_\Sigma \to [\Sigma,X]$. The quantum propagation we take to be the pull-push of the [[geometric function object]]s $C(E_\Sigma)$ through this [[multispan]].

Let $\Sigma_{in} \to \Sigma \leftarrow \Sigma_{out}$
be a [[cobordism]] [[cospan]] regarded as part of the [[multispan|multi-cospan]] $\Sigma_H$ that defines $Bord(X)$ as

$$
  Bord(X) = \lim_\to [\Sigma^\bullet_H,X]
$$

this realizes $Bord(X)$ as the universal cocone whose component under $\Sigma$ is

$$
  \array{
    && [\Sigma,X]
    \\
    & \swarrow && \searrow
    \\
    [\Sigma_{in},X]
    &&\downarrow^{\exp(S_\nabla)_\Sigma}
    &&
    [\Sigma_{out},X]
    \\
    &
    {}_{\exp(S_\nabla)}_{in}\searrow
    &     &
    \swarrow_{\exp(S_\nabla)_{out}}
    \\
    &&
    V
  }
$$

by lax pullback of $pt_V : {*} \to V$ this induces a span of total spaces

$$
  \array{
    && E_{\Sigma}
    \\
    & {}^{E_{in}}\swarrow && \searrow^{E_{out}}
    \\
    E_{\Sigma_{in}}
    &&
    &&
    E_{\Sigma_{out}}
  }
$$

<img src="http://latex.codecogs.com/gif.latex?$$ \xymatrix@R=23pt@C=12pt{ E_\Sigma \ar[rr]^{E_\mathrm{out}} \ar[dd]_{E_\mathrm{in}} \ar[ddr]  E_{\Sigma_{\mathrm{out}}} \ar[ddr] \\ \\ E_{\mathrm{in}} \ar[ddr]  [\Sigma,X] \ar[dd]^{\mathrm{in}} \ar[rr]^{\mathrm{out}} \ar[ddrr]  [\Sigma_{\mathrm{out}},X] \ar[dd] \ar@/^1pc/[rrdddd]^{\exp(S_\nabla)|_{\Sigma_\mathrm{out}}} \\ \\  [\Sigma_{\mathrm{in}},X] \ar[rr] \ar@/_1pc/[ddrrrr]_{\exp(S_\nabla)|_{\Sigma_\mathrm{in}}}  \mathrm{Bord}(X) \ar[ddrr]|{\exp(S_\nabla)} \\ \\  V } $$" title="$$ \xymatrix@R=23pt@C=12pt{ E_\Sigma \ar[rr]^{E_\mathrm{out}} \ar[dd]_{E_\mathrm{in}} \ar[ddr] E_{\Sigma_{\mathrm{out}}} \ar[ddr] \\ \\ E_{\mathrm{in}} \ar[ddr]  [\Sigma,X] \ar[dd]^{\mathrm{in}} \ar[rr]^{\mathrm{out}} \ar[ddrr] [\Sigma_{\mathrm{out}},X] \ar[dd] \ar@/^1pc/[rrdddd]^{\exp(S_\nabla)|_{\Sigma_\mathrm{out}}} \\ \\ [\Sigma_{\mathrm{in}},X] \ar[rr] \ar@/_1pc/[ddrrrr]_{\exp(S_\nabla)|_{\Sigma_\mathrm{in}}}  \mathrm{Bord}(X) \ar[ddrr]|{\exp(S_\nabla)} \\ \\  V } $$" />


**definition** the "quantum propagation along $\Sigma$" is the functor of [[geometric function object]]s

$$
  Z_\nabla(\Sigma)
  : 
  C(E_{\Sigma_{in}})
  \stackrel{(E_out)_* (E_{in})^*}{\to}
  C(E_{\Sigma_{out}})
$$


**remark** 
If instead of the over-category [[geometric function object]] we use its [[Kan fibrant replacement]] $Ex^\infty(\mathbf{H}/(-))$ this presciption becomes functorial also for higher morphisms coming from [[multispan|spans of spans]] 



# Concrete examples {#examples}


**Reminder on sections**
In order to unwrap the above abstract prescription in some special cases recall how we extract from the value $\psi_x \in C(E_{x})$ of a generalized section $\psi \in C(E_{pt})$ an ordinary vector in the case that $E$ is a [[vector bundle]]:

given $\psi : \Psi \to E_\Sigma$ we extract the corresponding "degroupoidified" vector of the corresponding section over $\phi|_{\Sigma} \in [\Sigma,X]$ as the pullback

$$
  \array{
    p^* \Psi
    &\to&
    \Psi
    \\
    \downarrow^{\psi|_{\phi|_{\Sigma}}}
    &&
    \downarrow
    \\
    V_{\phi|_{\Sigma}} &\stackrel{p}{\to}& E_\Sigma
    \\
    \downarrow && \downarrow
    \\
    {*}
    &\stackrel{\phi|_{\Sigma}}{\to}&
    [\Sigma,X]
  }
$$



## electromagnetically charged particle {#eleccharged}

The background field for the electrically charged particle is the [[electromagnetic field]]. As discussed there, is this modeled by a [[Deligne cohomology|Deligne cocycle]] in degree 2, or equivalently a line bundle with connection.

This is modeled in the present language by choosing as coefficient object $A = \mathbf{B}U(1)$,
the [[delooping]] of the circle [[Lie group]] $S^1 \simeq U(1)$.


Then an electromagnetic background field over a [[manifold]] $X$ is encoded in a morphism

$$
 \nabla : P_1(X) \to \mathbf{B}U(1)
  \,.
$$

See [[connection on a bundle]] for more details on this special case.

We choose the standard representation

$$
  \rho : \mathbf{B}U(1) \to Vect
$$

of $U(1)$ on $\mathbb{C}$.

Then 

* $E_{pt} \to X$ is the total space of the corresponding [[vector bundle|line bundle]]. 

* for $\Sigma = I = \Delta^1_H$ the [[interval]] the configuration space  $[\Delta^1_H,X] = [I,X]$ is the path space of $X$;

* the bundle $E_{I} \to [I,X]$ can be thought of as having as fiber over a path $(\gamma : x \to y) \in [I,X]$ the space of pairs of vectors $(v_x, v_y) \in E_x \times E_y$ that are related by parallel transport along $\gamma$, i.e. those for which $v_y = \rho\nabla(\gamma)(v_x)$.

* The two span maps
  
  $$
   \array{
    && E_{I}
    \\
    & {}^{E_{in}}\swarrow && \searrow^{E_{out}} 
    \\
    E_{pt} &&&& E_{pt}
   }
  $$

  project on the corresponding component:

  $$
    E_{in} : (v_x, v_y) \mapsto v_x
  $$

  $$
    E_{out} : (v_x, v_y) \mapsto v_y
  $$


To see how the corresponding quantum propagation acts on a section, it is sufficient to look at a single $\delta$-distribution state

$$
  \psi : {*} \to E_{pt}
$$

that hits a vector $\psi_x \in E_x$. In diagrams this means that

$$
  \array{
     &&
     E_{pt}
     \\
     & {}^\psi \nearrow & \downarrow
    \\
    {*} &\stackrel{x}{\to}& X
  }
$$

and

$$
  \array{
    p^* {*} &\to& {*}
    \\
    \downarrow^{\psi_x} && \downarrow^{\psi}
    \\
    E_x &\stackrel{p}{\to}& E_{pt}
    \\
    \downarrow && \downarrow
    \\
    {*} &\stackrel{x}{\to}& X
  }
  \,.
$$


Then the pull-push propagation functor

$$
  Z_\nabla(I) : C(E_{pt}) \to C(E_{pt})
$$

sends $\psi$ to the composite right diagonal morphism in

$$
  \array{
    && (E_{in})^* \Psi
    \\
    & \swarrow && \searrow^{(E_{in})^* \psi}
    \\
    {*}= \Psi&&&& E_{I}
    \\
    &\searrow^{\psi}&& {}^{E_{in}}\swarrow && \searrow^{E_{out}}
    \\
    &&E_{pt} &&&& E_{pt}
  }
  \,.
$$

We see that

* $(E_{in})^* \Psi$ is the space with points the set of pairs $(v_x,v_y) \in E_{I}$ such that $v_x = \psi_x$;

* hence the map 

  $$
   (E_{out})_* \psi : (E_{in})^* \Psi 
    \stackrel{(E_{in})^* \psi}{\to} E_{I}
    \stackrel{E_{out}}{\to} E_{pt}
  $$

  is on the level of sets the map whose fiber over 
  the vector $v_y \in E_y \subset E_{pt}$ at $y$ is 
  the set of paths $\gamma : x \to y$ 
  such that $v_y = \rho\nabla(\gamma)$.

This means that, by the above prescription, the degroupoidification of our propagated section is the section $Z_\nabla(I)(\psi)$ whose value over $y \in X$ is formally

  $$ 
    Z_\nabla(I)(\psi)_y = \sum_{\gamma: x \to y}
    \exp(S_\nabla(\gamma))(\psi_x)
    \,.
  $$

That's the expression of the Feynman-Kac [[path integral]] for the electron, except, of course,  that the [[Wiener measure]] on the space of paths is missing.



## Dijkgraaf-Witten theory {#dw}

[[Dijkgraaf-Witten theory]] is the [[gauge theory]] which, when regarded as a [[sigma-model]] is given by

* target space $X$ is the [[delooping]] $X := \mathbf{B}G$ of a finite [[group]] $G$;

* the background field is a morphism $\nabla : \Pi(\mathbf{B}G) \to \mathbf{B}^3 U(1)$ into the 3-fold [[delooping]] of the [[Lie group]] $U(1)$ (see [[Eilenberg-MacLane object]]).

This means that the configuration spaces of DW theory over a cobordisms $\Sigma$ are the [[groupoid]]s ([[orbifold]]s) $[\Sigma,\mathbf{B}G] = G Bund(\Sigma)$  of $G$-[[principal bundle]]s on $\Sigma$.

Since the cobordisms  $\Delta^k_H$ are disk-shaped, the groupoids of $G$-principal bundles on them are trivial and we have

$$
  \Pi(\mathbf{B}G) \simeq \mathbf{B}G
  \,.
$$


Hence the background field for DW theory is actually just a 

$$
  \nabla : \mathbf{B}G \to \mathbf{B}^3 U(1)
  \,.
$$

This just reflects the fact that $G$-principal bundles for discrete group $G$ have a unique and flat [[connection on a bundle|connection]].

By the discussion at [[group cohomology]] this DW background field is nothing but a group cocycle defining a class in degree 3 group cohomology $H^3(G,U(1))$. This is the form in which the background data for DW theory was originally and is still usually presented.


The standard representation of the gauge group $\mathbf{B}^2 U(1)$ (recall that $G$ is from the [[sigma-model]] perspective not a gauge group but defines the target space!) is on $\mathbf{B}^2 1dVect \hookrightarrow \mathbf{B} Vect Mod$ 

$$
  \rho : \mathbf{B}^3 U(1) \to \mathbf{B} Vect Mod
  \,.
$$



Then for $\Sigma_{in} \to \Sigma \leftarrow \Sigma_{out}$ a [[cobordism]] [[cospan]] the corresponding quantum propagation 

$$
  Z(\Sigma) : C(E_{\Sigma_{in}})  \to 
    C(E_{\Sigma_{out}})
$$

is under the above "degroupoidification" the action of Dijkgraaf-Witten theory, where the $\frac{1}{|Aut(P)|}$-weight comes from the fact that the pulled back state ${in}^* \psi$ picks up the automorphisms of $P$ by the push-forward

$$
  \array{
    && in^* \Psi
    \\
    & \swarrow && \searrow^{in^* \psi}
    \\
    \Psi && && E_{\Sigma}
    \\
    &\searrow^{\psi}& & \swarrow && \searrow
    \\
    && E_{\Sigma_{in}}
    &&&&
    E_{\Sigma_{out}}
  }
$$


Actually, more precisely due to the nature of the [[homotopy pullback]] this picks up another factor of $|Aut(P|_{in})|$.



## the Yetter model {#yetter}

The [[Yetter model]] is the name for the [[sigma-model]] whose 

* target space $X$ is the [[delooping]] $\mathbf{B}G$ of a strict [[2-group]] $G$ coming  from a [[crossed module]] $(G_2 \stackrel{\delta}{\to} G_1)$;

* background field is a morphism $\nabla : \Pi(\mathbf{B}G) \to \mathbf{B}^4 U(1)$.

So this is just as Dijkgraaf-Witten theory, discussed above, but in one degree higher.

Accordingly, its discussion is pretty analogous to that of the Dijkgraaf-Witten model discussed above. The important difference is that now the automorphisms of a [[principal 2-bundle]] classified by a map $\Sigma \to \mathbf{B}G$ form a [[2-group]] themselves, so that the [[Leinster measure]] coefficient $|p^{-1}(v_x)|$ in our degroupoidification formula becomes slightly more subtle.

The right factor was originally found in the literature by requiring the path integral of the Yetter model to be independent of choices made when representing $G$-2-bundles as cocycles. The following proposition shows that the factor obtained this way is indeed nothing but the 2-groupoid Leinster measure.

>this is an old version of this proof, I'll upload a better one...


**Proposition.** 

The combinatorial weighting for the "categorified DW" theory introduced by Yetter (and studied by Girelli, Pfeiffer, Popescu, Porter, Martins etc.) is indeed the [[Leinster measure]] of the corresponding configuration space.

Recall that for ordinary DW theory for finite group $G$ config space is the groupoid $[\Sigma,\mathbf{B}G]$, 
which, since $\Sigma$ is finite, may be computed by choosing a triangulation of $\Sigma$, letting $P_1(\Sigma)$
denote the free category on the corresponding graph
and considering $Func(P_1(\Sigma),\mathbf{B}G)$.

Since there are 
$$
  |G|^\nu
$$

many ways to assign group element to the $\nu$ vertices of the triangulation, there are $|G|^\nu$ many natural transformations starting at any functor $P_1(\Sigma) \to \mathbf{B}G$ and therefore the Leinster measure of the hom-groupoid is

$$
  d\mu = \frac{1}{|G|^\nu}
  \,.
$$

Now, Yetter et al find that when target space is replaced by
$$
  \mathbf{B}G_{(2)}
$$

for $G_{(2)}$ the finite strict [[2-group]] coming from the strict [[crossed module]]

$$
 H \stackrel{t}{\to} G \stackrel{\alpha}{\to} Aut(H)
  \,,
$$

then the corresponding combinatorial weight becomes

$$
  |G|^{- \nu} |H|^{-\nu + \lambda}
  \,,
$$

where $\nu$ is the number of vertices, as before, and where $\lambda$ is the number of edges in $X$.

(See for instance theorem 2.13 on p. 127 of Martins-Porter's <a href="http://www.tac.mta.ca/tac/volumes/18/4/18-04abs.html">On Yetter's invariants</a> or the discussion below theorem III.2 on p. 6 of Girelli-Pfeiffer-Popescu's <a href="http://golem.ph.utexas.edu/category/2007/12/bftheory_as_a_higher_gauge_the.html">BF to BFCG</a> (while the factor is not manifest in their expression (15))).

The claim here is that this factor is precisely the [[Leinster measure]] on the configuration space

$$
  conf
  =
  \mathrm{hom}_{2Cat}(P_2(\Sigma), \mathbf{B}G_{(2)})/\sim
$$

Here I am taking, to replace awkward pseudofunctors with nicer strict 2-functors, $P_2(\Sigma)$ now to be the strict 2-groupoid generated from the triangles in $\Sigma$.


Then the above hom-groupoid is supposed to be the 1-groupoid obtained by passing to equivalence classes of 1-morphisms in the 2-groupoid whose objects are strict 2-functors $P_2(\Sigma) \to \mathbf{B}G_{(2)}$, whose morphisms are pseudonatural transformations of these, and whose 2-morphisms are modifications of those.


To prove this, we need to compute how many 1-morphisms in $conf$ there start at any given object.

But that's easy: a 1-morphism 

$$g : A \to A'
$$ 

in the 2-groupoid of strict 2-functors $P_2(\Sigma) \to \mathbf{B}G_{(2)}$ is a transformation whose component is an assignment of squares in $\mathbf{B}G_{(2)}$ to edges in $X$:

$$
  g :
  (x \stackrel{\gamma}{\to} y)
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
     \bullet &\stackrel{A(\gamma)}{\to}& \bullet
     \\
     \downarrow^{g(x)}
     & \Downarrow^{g(\gamma)}
     &
     \downarrow^{g(y)}
     \\
     \bullet &\stackrel{A'(\gamma)}{\to}&     
     \bullet
  }
  \,.
$$

By the general yoga of strict 2-groups, we know that the square on the right is entirely and precisely fixed by

* the source 2-functor value $A(\gamma) \in G$ on the top;

* the two transformation elements $g(x), g(y) \in G$ on the two sides;

* and the label $g(\gamma) \in H$ of the 2-morphism filling the square.

This uniquely determines the value $A'(\gamma)$ of the pseudofunctor which is the target of the transformation whose component $g$ is.

Therefore, clearly, there are precisely

$$
  |G|^\nu |H|^\lambda
$$

many 1-morphisms in 

$$
  \mathrm{hom}_{2Cat}(P_1(X), \mathbf{B}G_{(2)})
$$

starting at any given object. 

But some of them are related by 2-morphisms 

To figure out many, we need to compute how many modifications $\eta : g \to g'$ there are starting at any transformation $g$.

But again the same logic applies: such a transformations is given by a component map which sends vertices in $X$ to 2-cells in $\mathbf{B}G_{(2)}$:

$$
  \eta : 
  x \mapsto
  \array{
    & \nearrow \searrow^{g(x)}
    \\
    \bullet 
    & \Downarrow^{\eta(x)}&
    \bullet
    \\
    & \searrow \nearrow_{g'(x)}
  }
$$
for $\eta(x) \in H$.

Again one sees, by drawing the relevant naturality  tin-can diagram which I won't bother to do here in MathML, that for each such choice of assignments of elements in $H$ to vertices in $X$ there is precisely one modification $\eta : g \to g'$. 

This means that we have

 - $|G|^\nu |H|^\lambda$ 1-morphisms emanating at each object

and

 - $|H|^\nu$ 2-morphisms emanating at every morphism.

The Leinster measure in this situation is

$$
  d\mu(A) = 
  |G|^{-\nu} |H|^{\nu - \lambda}
  \,,
$$

precisely the combinatorial factor which people found makes the Yetter state sum model a topological invariant.




+-- {.standout}

...

=--





[[!redirects exercise in groupoidification -- the path integral]]


[[!redirects An Exercise in Groupoidification]]