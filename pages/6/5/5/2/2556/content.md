
<div class="rightHandSide toc">
[[!include homotopy - contents]]
***
[[!include synthetic differential geometry - contents]]
</div>


#Contents#

* automatic table of contents goes here
{:toc}

## Idea

An _infinitesimal interval object_ is like an [[interval object]] that is an [[infinitesimal space]].

Where maps out of an [[interval object]] model paths that may arrange themselves into [[path ∞-groupoid]]s, maps out of infinitesimal interval object model infinitesimal paths that may arrange themselves into [[infinitesimal path ∞-groupoid in a smooth topos|infinitesimal path ∞-groupoid]].


## Definition

In any [[lined topos]] $(\mathcal{T},(R,+,\cdot))$ the line object $R$ is naturally regarded as a [[interval object|cartesian interval object]]. 

$$
  \array{
    && R
    \\
    & 
    {}^{0_{*}}\nearrow && \nwarrow^{1_{*}}
    \\
    {*}
    &&&&
    {*}
  }
  \,.
$$

If the [[lined topos]] $(\mathcal{T}, R)$ is also a [[smooth topos]] in that it satisfies the [[Kock-Lawvere axiom]] it makes sense to consider the [[subobject]] $D$ of $R$ defined as the [[equalizer]]

$$
  D = \lim\left( R \stackrel{\stackrel{(-)^2}{\to}}{\underset{0}{\to}} R \right)
$$

or equivalently expressed in [[topos]] [[logic]] as

$$
  D = \{x \in R | x^2 = 0 \}
  \,.
$$

and think of $D$ as the **infinitesimal interval object** of the [[smooth topos]] $(\mathcal{T},R)$ inside its finite [[interval object]] $R$. By the axioms satisfied by a [[smooth topos]] it is in particular an [[infinitesimal object]].

Various constructions induced by a finite [[interval object]] have their infinitesimal analog for infinitesimal interval objects.



## Infintesimal path $\infty$-groupoid induced from infinitesimal interval

+-- {: .query}

[[Urs Schreiber]]: the following should be checked

=--


### Introduction 

Recall the discussion at [[interval object]] of how the interval ${*}\sqcup {*} \stackrel{\to}{\to} R$ in $\mathcal{T}$ alone gave rise to the [[cosimplicial object]]

$$
  \Delta_R : \Delta \to \mathcal{T}
$$

of (collared) $k$-simplices modeled on $R$, and how that induces for each object $X \in \mathcal{T}$ the [[simplicial object]]

$$
  \Pi(X) := X^{\Delta_R^\bullet}
  \,.
$$ 

Here as an object in $\mathcal{T}$ the $k$-simplex is actually a $k$-cube $\Delta_R^k := R^k$, but equipped with face and degeneracy maps that identify the boundary of a $k$-simplex inside the $k$-cube thus realizing the interior of that boundary as the $k$-simplex proper and the exterior as its _collar_ .

We want to mimic that construction with the finite interval $R$ replaced by the infinitesimal interval object $D$, to get a simplicial object $\Pi^{inf}(X)$ for every object $X$.

While the infinitesimal situation is formally very similar to the finite situation, one technical diference is that the infinitesimal interval does not fit into a nontrivial [[cospan]] as the finite interval does. This is because $D$ typically has a _unique_ morphism ${*} \to D$ from the terminal object, as a consequence of the fact that all the infinitesimal elements it contains are genuinely [[generalized element]]s.

The natural way to encode an infinitesimal path between two elements in an object $X$ in the [[smooth topos]] $\mathcal{T}$ is therefore not as an element of $X^D$ but of $X^D \times D$, which we may think of as the space of pairs consisting of infinitesimal paths in $X$ and infinitesimal parameter lengths of these paths.

This naturally yields the [[span]]

$$
  \array{
    && X^D \times D
    \\
    & {}^{\mathllap{p_{T X}\circ p_1}}\swarrow && \searrow^{\mathrlap{ev}}
    \\
    X &&&& X
  }
  \,,
$$

where 

* the left leg is the projection $X^D \times D \to X^D$ followed by the [[tangent bundle]] projection $p_{T X} = X^{(* \to D)} : X^D \to X$ 

* the right leg is the evaluation map, i.e. the [[inner hom]]-[[adjunct]] of $Id : X^D \to X^D$.

With this setup a pair of ([[generalized element|generalized]]) elements $x,y \in X$ may be thought of as connected by an infinitesimal path if there is an element $(v,\epsilon) \in X^D \times D$ such that 

$$
  \delta_1(v,\epsilon) = v(0) = x
$$ 

and 

$$
  \delta_0(v,\epsilon) = v(\epsilon) = y
  \,.
$$

But not all elements $(v,\epsilon)$ define _different_ pairs of [[infinitesimal neighbour]] elements this way: specifically in the case that $X$ is a [[microlinear space]], the [[tangent bundle]] object $X^D$ is fiberwise $R$-linear, and thus for any $t \in R$ the elements $(v,t \epsilon)$ and $(t v, \epsilon)$ define the same pair of [[infinitesimal neighbour]]s, $x = v(0)$ and $y = (t v)(\epsilon) = v(t \epsilon)$.

We may identify such elements $(t v, \epsilon)$ and $(v, t \epsilon)$ by passing to the [[tensor product]] $X^D \otimes_R D$, i.e. the coequalizer of

$$
  X^D \times R \times D \stackrel{\stackrel{\cdot \times Id}{\to}}{\underset{Id \times \cdot}{\to}}
  X^D \times D
$$

where $\cdot$ here denotes the [[monoid]]-[[action]] of $(R,\cdot)$ on $D$ (by the embedding $D \hookrightarrow R$) and on $X^D$ (by the fact that $X$ is assumed to be [[microlinear space|microlinear]]).

In this same fashion we can then define infinitesimal analogs of the finite higher path object $X^{\Delta_R^k} = X^{R^{\times k}}$.

### The definition 

+-- {: .un_defn}
###### Definition
**(infinitesimal path simplicial object)**

Let $X \in \mathcal{T}$ be a [[microlinear space]] in the
[[smooth topos]] $(\mathcal{T},R)$ with infinitesimal
interval object $D$. 

Then define the [[simplicial object]] 

$$
  \Pi^{inf}(X)
  : \Delta^{op} \to
  \mathcal{T}
$$ 

as follows:

* in degree $n$ it assigns the object

  $$
    [n] \mapsto 
    X^{D(n)} \otimes_{R^n} D(n)
    \hookrightarrow
    (X^D \otimes_R D)^{\times_X^n}
  $$

  whose [[generalized element]]s we write $(\epsilon_i v_i)_x$ with $\vec \epsilon \in D(n)$ or $(\nu_i)_x$ for short; where $x \in X$ indicates the fiber of $X^{D(n)} \to X$ that the element lives in 


* the face maps $d_i : (X^D \times_R D)^{\times_X^{n+1}} \to (X^D \times_R D)^{\times_X^{n}}$ are

  * for $0 \lt i \lt n+1$

    given on [[generalized element]]s by

    $$
      d_i : (\nu_i)_x
      \mapsto
      (\nu_0 , \cdots, \nu_{i-2},
      \nu_{i-1} + \nu_i, \nu_{i+1}, \cdots, \nu_{m+1} )_x
    $$

  * for $i = 0$

    given by

    $$
      d_0 : (\nu_i) \mapsto (v_0(\epsilon_0) + \nu_i)
    $$

    where the element on the right denotes the evaluation of the map $(\nu_i) : D(n) \to X$ in its first argument on $\epsilon_0$, regarded as an element in the fiber over $v_0(\epsilon_0)$.

  * for $i = n+1$ 

    given by 

    $d_{n+1} : (\nu_0, \cdots, \nu_{n+1}) \mapsto (\nu_0, \cdots, \nu_n)$

* the degeneracy maps $\sigma_i$ act by inserting the 0-vector in position i:

  $\sigma_i : (\ni_i) \mapsto (\nu_0, \cdots, \nu_{i-1}, 0, \nu_{i+1}, \cdots, \nu_{n})$.


=--

+-- {: .un_prop}
###### Proposition

These face and degeneracy maps indeed satisfy the 
[[simplicial identities]].

=--

+-- {: .proof}
###### Proof

This is straightforward checking that proceeds entirely analogously as the proof of the simplicial identities for the finite path $\infty$-groupoid $\Pi(X)$ discussed at [[interval object]]. See also the following remark.

=--


+-- {: .un_remark}
###### Remark

By thinking of the $v_i : D  \to X$ as infinitesimal collared curves in $X$ with source $v_i(0)$ and target $v_i(\epsilon_i)$ the above definition is an immediate analog of the definition of the path $\infty$-groupoid $\Pi(X)$ of finite paths as discussed at [[interval object]].

This is made manifest by the following construction that embeds $\Pi^{inf}(X)$ into $\Pi(X)$. 

=--


### The inclusion of infinitesimal paths into finite paths ##

Recall the finite path $\infty$-groupoid $\Pi(X)$ induced from the [[interval object]]

$$
  (0_*,1_*) : * \coprod * \to R
$$ 

as discussed there. On object this assigns

$$
  \Pi(X) : [n] \mapsto X^{R^n}
  \,.
$$


+-- {: .un_defn}
###### Definition
**(inclusion of infinitesimal into finite paths)**

For $n \in \mathbb{N}$ define a morphism

$$
  X^(D(n)) \otimes_{R^n} D(n)
  \to 
  X^{R^n}
$$

on [[generalized element]]s by

$$
  \iota_n : 
  (\epsilon_i v_i) \mapsto 
  ((t_0, \cdots, t_{n-1}) 
   \mapsto \sum_{i=0}^{n-1} v_i(t_i \epsilon_i))
   \,.
$$

=--

+-- {: .un_prop}
###### Proposition

These morphism $(\iota_n)$ respect the face and degeneracy maps on both sides and hence induce an inclusion of simplicial objects

$$
  \Pi^{inf}(X) \hookrightarrow \Pi(X)
$$

=--

+-- {: .proof}
###### Proof

Straightforward checking on [[generalized element]]s.

=--

### Properties

> under construction

Let  $X$ be a micorlinear space. 

We want to show that the morphism of simplicial sets

$$
  Hom(U \times D, X^{(\Delta_\inf)^\bullet})
  \to
  Hom(U , X^{(\Delta_\inf)^\bullet})
$$

induced by pullback along $U \simeq U \times * \to U \times D$
is a [[weak homotopy equivalence]].

...


Let $f : U \times D \to X$ be a morphism. Then 

$$
  \array{
    && U \times D
    \\
    &{}^{\mathllap{f(-,*)}}\swarrow& \downarrow & \searrow^{\mathrlap{f}}
    \\
    X &\underset{p_{T X} p_1}{\leftarrow}& X^D \times D &\underset{ev}{\to}& X
  }
  \,,
$$

where the vertical morphism is $(u, \epsilon) \mapsto (f(u,-),\epsilon)$, so that the left diagonal morphism is $(u,\epsilon) \mapsto f(u,*)$ exhibits a homotopy in $Hom(U\times D, X^{(\Delta^\bullet_{inf})})$ from $f : U \times D \to X$ to $U \times D \to U \times * \simeq U \to X$.
