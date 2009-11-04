> **under construction**


<div class="rightHandSide toc">
[[!include cohomology - contents]]


***

[[!include higher algebra - contents]]


</div>



+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

=--



>**Abstract** We sketch some basic ideas ([[Jacob Lurie]]'s ideas, that is) about [[higher geometry]] and the higher-geomety version of the [[moduli stack]] of [[elliptic curve]]s: the derived moduli stack of [[derived elliptic curve]]s. We survey aspects of the theory of [[generalized scheme]]s and then sketch how the derived moduli stack of derived elliptic curves is an example of a generalized scheme modeled on the formal dual of [[E-∞ ring]]s.


For fully appreciating the details of  the main theorem here the material discussed in the previous sessions (and a little bit more) is necessary, but our exposition of [[generalized scheme]]s is meant to be relatively self-contained (albeit necessarily superficial).

This are the entries on the previous sessions:


* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]

* [[A Survey of Elliptic Cohomology - elliptic curves]]

* [[A Survey of Elliptic Cohomology - equivariant cohomology]]

 
* [[A Survey of Elliptic Cohomology - derived group schemes and (pre-)orientations]]

* [[A Survey of Elliptic Cohomology - A-equivariant cohomology]]

***

> **under construction**



# the derived moduli stack of derived elliptic curves #
* automatic table of contents goes here
{:toc}


## Motivation and Statement ##

In  the context of [[elliptic cohomology]] one assigns to every [[elliptic curve]] $\phi$ over a [[ring]] $R$ a [[cohomology theory]] [[Brown representability theorem|represented]] by an [[E-∞ ring]] [[spectrum]] $E_\phi$.

Since, by definition, we may identify the [[elliptic curve]] $\phi$ over $R$ with a patch $\phi : Spec R \to \mathcal{M}_{1,1}$ of the [[moduli stack]] $\mathcal{M}_{1,1}$ of elliptic curves, this assignment

$$
  \mathcal{O}^{Der} : \phi \mapsto E_\phi
$$

looks like an [[E-∞ ring]] valued [[structure sheaf]] on $\mathcal{M}_{1,1}$.

There is a very general theory of [[higher geometry]] for [[nLab:generalized scheme|generalized spaces]] with generalized [[nLab:structure sheaf|structure sheaves]]. Using this one may regard the pair 

$$
  (\mathcal{M}_{1,1}, \mathcal{O}^{Der})
$$ 

as a [[structured (infinity,1)-topos|structured space]] that is a "derived" [[Deligne-Mumford stack]].

The central theorem about [[elliptic cohomology]] of [[Jacob Lurie]], refining the Goerss-Hopkins-Miller theorem says that

+-- {: .standout}

**the central theorem, first version**

The [[moduli stack]] $\mathcal{M}_{1,1}$ of [[elliptic curve]]s equipped with the [[E-∞ ring]]-valued [[structure sheaf]] $\mathcal{O}^{Der}$ may be regarded as the _derived moduli stack_ of [[derived elliptic curve]]s in that for any [[E-∞ ring]] $R$ the space of derived stack morphisms

$$
  (Spec R, R) \to (\mathcal{M}_{1,1}, \mathcal{O}^{Der})
$$

is equivalent to the space of [[derived elliptic curve]]s over $R$.


=--

After we have looked at some concepts in [[higher geometry]] a bit more closely below, we will restate this in slightly nicer fashion.


## References ##

A sketch of what this theorem means and how it is proven is part of the content of 

* [[Jacob Lurie]], [[A Survey of Elliptic Cohomology]].

and goes back to Jacob Lurie's PhD thesis (listed [[Jacob Lurie|here]]).

The general theory for the context of [[higher geometry]] invoked here has later been spelled out in

* [[Jacob Lurie]], [[Structured Spaces]]

but the special case of the general theory that is needed here, where the coefficient objects of structure sheaves are [[E-∞ ring]]s has only been announced as

* [[Jacob Lurie]], [[Spectral Schemes]]

and isn't available yet. On the other hand, the general theory of [[E-∞ ring]]s themselves, in the [[(∞,1)-category]] theory context needed here, is developed in

* [[Jacob Lurie]], [[higher algebra|Commutative geometry]].


## higher geometry ##

The statement that we are after really lives in the context of [[higher geometry]] (often called "derived geometry"). Here is an outline of the central aspects. 

### notions of space  ###

The general story of [[higher geometry]] is this:

We fix some [[(∞,1)-category]] $\mathcal{G}$ whose objects we think of as _model spaces_ : the simplest objects exhibiting the geometric structures that we mean to consider.

+-- {: .standout}

**Examples for categories of model spaces**

* with smooth structure

  * $\mathcal{G} = $ [[Diff]], the category of smooth [[manifold]]s;

  * $\mathcal{G} = \mathcal{L}$, the category of [[smooth locus|smooth loci]];

* without smooth structure

  * $\mathcal{G} = (C Ring^{fin})^{op}$, the formal dual of [[CRing]]: the category of (finitely generated) algebraic [[affine scheme]]s;

  * $\mathcal{G} = (E_\infty Ring^{fin})^{op}$, the formal dual of [[E-∞ ring]]s: the category of (finitely generated) algebraic derived [[affine scheme]]s.

=--


These [[(∞,1)-category|(∞,1)-categories]] $\mathcal{G}$ are naturally equipped with the structure of a [[site]] (and a bit more, which we don't need here). Following [[Jacob Lurie]] we call such a $\mathcal{G}$ a **[[geometry (for structured (infinity,1)-toposes)|geometry]]** . 

We want to be talking about generalized spaces _modelled on_ the objects of $\mathcal{G}$. There is a hierarchy of notions of what that may mean:

+-- {: .standout}

**Hierarchy of generalized spaces modeled on $\mathcal{G}$**

$$
  \array{
    \mathcal{G} 
    &\stackrel{Spec^{\mathcal{G}}}{\hookrightarrow}&   
    Sch(\mathcal{G}) 
    &\hookrightarrow&
    \mathcal{L}Top(\mathcal{G})^{op} 
    &\hookrightarrow&      
    Sh_\infty(Pro(\mathcal{G}))
    \\
    \\
    model spaces
    &&
    spaces locally like model spaces
    &&
    concrete spaces coprobeable by model spaces
    &&
    spaces probeable by model spaces
    \\
    \\
    affine\;\mathcal{G}-schemes
    &&
    \mathcal{G}-schemes
    &&
    \mathcal{G}-structured\;(\infty,1)-toposes
    &&
    \infty-stacks\;on\;\mathcal{G}
    \\
    \stackrel{specific, nice}{\leftarrow} & 
    &&&&
    &
    \stackrel{general, possibly wild}{\to}
  }
$$

=--

We explain what this means from right to left.


#### spaces probeable by model spaces: $\infty$-stacks ####

An object $X$ _probeable_ by objects of $\mathcal{G}$ should come with an assignment

$$
  X : (U \in \mathcal{G}) \mapsto (X(U) \in \infty Grpd)
$$

of an [[∞-groupoid]] of possible ways to probe $X$ by $U$, for each possible $U$, natural in $U$. More prrecisely, should define an object in the [[(∞,1)-category of (∞,1)-presheaves]] on $\mathcal{G}$

$$
   X \in PSh(\mathcal{G}) 
   = 
   (\infty,1)Func(\mathcal{G}^{op}, \infty Grpd)
$$

But for $X$ to be _consistently_ probeable it must be true that probes by $U$ can be reconstructed from overlapping probes of pieces of $U$, as seen by the [[coverage|topology]] of $\mathcal{G}$. More precisely, this should mean that the [[(∞,1)-presheaf]] $X$ is actually an object in an [[(∞,1)-category of (∞,1)-sheaves]] on $\mathcal{G}$

$$
  X \in 
  Sh(\mathcal{G}) \stackrel{}{\hookrightarrow}
  PSh(\mathcal{G})
  \,.
$$

Such objects are called [[∞-stack]]s on $\mathcal{G}$. The [[(∞,1)-category]] $Sh(\mathcal{G})$ is called an [[∞-stack]] [[(∞,1)-topos]].

A supposedly pedagogical discussion of the general philosophy of [[∞-stacks]] as probebable spaces is at [[motivation for sheaves, cohomology and higher stacks]].

For concretely working with [[hypercomplete (∞,1)-topos]]es it is often useful to use [[models for ∞-stack (∞,1)-toposes]] in terms of the [[model structure on simplicial presheaves]].

+-- {: .standout}

$$
  \array{
    \mathbf{H} := & Sh_{(\infty,1)}(C) &\stackrel{\leftarrow}  
  {\hookrightarrow}&
     PSh_{(\infty,1)}(C)
    && \text{abstract nonsense def of (∞,1)-topos}
    \\
    & \uparrow^{\simeq} &&
    \uparrow^{\simeq}
    && \text{Lurie's theorem}
    \\
    & ([C^{op}, SSet]_{loc})^\circ
    &\stackrel{\leftarrow}{\to}&
    ([C^{op}, SSet]_{glob})^\circ
    &&
    \text{model category of simplicial presheaves}
  }
$$

=--



#### concrete spaces co-probeable by model spaces: structured $(\infty,1)$-toposes ####

Spaces probeable by $\mathcal{G}$ in the above sense can be very general. They need not even have a "concrete underlying space", even for general definition of what _that_ might mean.

**(Counter-)Example** For $\mathcal{G} = $ [[Diff]], for every $n \in \mathbb{N}$ we have the [[∞-stack]] $\Omega_{cl}^n(-)$ (which happens to be an ordinary [[sheaf]]) that assigns to each manifold $U$ the set of closed [[differential form|n-form]]s on $U$. This is important as a generalized space: it is something like the rational version of the [[Eilenberg-MacLane space]] $K(\mathbb{Z}, n)$. But at the same time this is a "wild" space that has exotic properties: for instance for $n=3$ this space has just a single point, just a single curve in it, just a single surface in it, but has many nontrivial probes by 3-dimensional manifolds.

In contrast to that, a _structured space_ is supposeed to be a probable space/[[∞-stack]] on $\mathcal{G}$ which does have an "underlying concrete space".

In the classical theory for instance of [[diffeological space]]s one requires that this means that there is at least an underlying [[topological space]]. But this in turn is a bit _too_ restrictive for general purposes. We observe that a topological space is the same as a [[0-localic topos]]: a [[categiry of sheaves]] on a [[category of open subsets]] of a [[topological space]]. The obvious generalization of this to [[higher geometry]] is: an [[n-localic (∞,1)-topos]] $\mathcal{X}$.

We think of $\mathcal{X}$ as the [[(∞,1)-topos]] of [[∞-stack]]s on a category of open subsets of a would-be space, only that this would be space $X$ might not have an independent existence apart from $\mathcal{X}$.

To say that $\mathcal{X}$ is _modeled on $\mathcal{G}$_ means that among all the [[∞-stack]]s on the would-be space is singled out one that is the [[structure sheaf]] of functions with values in objects of $\mathcal{G}$: for each object $V \in \mathcal{G}$ there is a [[structure sheaf]] $\mathcal{O}(-,V) \in \mathcal{X}$, naturally in $V$.

This yields an [[(∞,1)-functor]]

$$
  \mathcal{O} : \mathcal{G} \to \mathcal{X}
  \,.
$$

We think of $X$ as being a concrete space _co-probebale_ by $\mathcal{G}$ (we can map from the concrete $X$ into objects of $\mathcal{G}$).

We say $\mathcal{O}$ is a _consistent_ collection of co-probes if coprobes with values in $V$ may be reconstructed from co-probes with values in pieces of $V$.

(means: $\mathcal{O}$ preserves [[limit]]s and sends covering coproducts to [[effective epimorphism]]s).

**Definition** A pair $(\mathcal{X}, \mathcal{O})$ of an [[(∞,1)-topos]] $\mathcal{X}$ equipped with $\mathcal{G}$-valued [[structure sheaf|structure sheaves]] $\mathcal{O} : \mathcal{G} \to \mathcal{X}$ a
[[structured (∞,1)-topos]].

**example**

The archetypical examples are those obtained from the model space objects in $\mathcal{G}$ themselves

$$
  \mathcal{G} \stackrel{Spec^{\mathcal{G}}}{\hookrightarrow}
  \mathcal{L}Top(\mathcal{G})^{op}
$$

Abstractly, this inclusion works as follows: let $\mathcal{G}_{disc}$ be the geometry $\mathcal{G}$ equipped with the discrete [[coverage|topology]] (no nontrivial covers). Then one can identify...


#### spaces locally like model spaces: generalized schemes ####


a $\mathcal{G}$-[[structured (∞,1)-topos]] such that there is $U_i \in \mathcal{G}$ and an [[effective epimorphism]] $\coprod_i U_i \to \mathcal{X}$.

+-- {: .un_proposition}
###### Proposition

The inclusion of $\mathcal{G}$-[[generalized scheme]] into $PSh_\infty(Pro(\mathcal{G}))$ 

* does factor through $Sh(Pro(\mathcal{G})) \hookrightarrow PSh(Pro(\mathcal{G}))$;

* and as such is a [[full and faithful (infinity,1)-functor]] $Sch(\mathcal{G})$.

=--

+-- {: .proof}
###### Proof

The second statement is theorem 2.4.1 in [[Structured Spaces]], the first one is lemma 2.4.13

=--

**examples**

* ordinary smooth [[manifold]] are 0-localic [[Diff]]-[[generalized scheme]]s

* ordinary [[schemes]] are 0-localic $(CRing^{fin})^{op}$-[[generalized scheme]]s

* [[Deligne-Mumford stack]]s are 1-localic $(CRing^{fin})^{op}$-[[generalized scheme]]s


### sheaves on $(\infty,1)$-toposes ###


In this approach we entirely switch from thinking about a space to thinking about an [[(∞,1)-topos]] thought of as the collection of [[∞-stack]]s on that space.

But we also want to be talking about generalized sheaves _on_ our generalized spaces. This is actually easy: for $\mathcal{C}$ any [[(∞,1)-category]] with finite limits, 
a $\mathcal{C}$-valued sheaf on  $(\mathcal{X}, \mathcal{O})$ is a small limit preserving functor $\mathcal{X}^{op} \to \mathcal{C}$. 

If we think of $\mathcal{X} = Sh(C)$ as being the [[∞-stack]] [[(∞,1)-topos]] on a [[site]] $C$, then
by the [[nLab:Yoneda lemma for (∞,1)-categories]] every object in the [[(∞,1)-topos]] $\mathcal{X}$ is a [[colimit]] of [[representable functor|representables]], which means that such a sheaf is fixed by its value on representables, i.e. on objects in $C$, as one would expect.


In particular, every object of $\mathcal{X}$ gives a sheaf on $\mathcal{X}$ this way.

### spaces with $E_\infty$-ring valued structure sheaves ###

For the applications to [[elliptic cohomology]] and [[derived elliptic curve]]s our [[geometry (for structured (∞,1)-toposes)|geometry]] $\mathcal{G}$ is the opposite [[(∞,1)-category]] of [[E-∞ ring]]s.

This case hasn't been fully spelled out yet, it is supposed to be the content of

* [[Jacob Lurie]], [[Spectral Schemes]].

But heuristically it is clear that everything works "as for ordinary rings, but up to homotopy". So we proceed with fingers crossed.


## the derived moduli space of elliptic curves ##

With the above machinery for [[higher geometry]] in hand, we now set out to describe the particular application that we are interested in: the study of the derived [[moduli stack]] of [[derived elliptic curve]]s.

### derived elliptic curves ###


* [[derived elliptic curve]]

$$
  A \mapsto E(A)
$$

### the derived moduli stack ###

Lurie's discussion of the derived moduli stack $(\mathcal{M}_{1,1}, \mathcal{O}^{Der})$  is more than a re-interpretation of the Goerss-Miller-Hopkins theorem. It is in particular a re-derivation of this result, from the following perspective

+-- {: .standout}

**the central statement, conceptually**

**Input** We have the $(E_\infty Ring)^{op}$-probeable space

$$
  (E : R \mapsto \{derived\;elliptic\;curves\;over\;R\})
  \in Sh(E_\infty Ring^{op})
  \,.
$$

**Question**: Does this happen to even be a $E_\infty Ring^{op}$-[[generalized scheme]]?

**Answer** Yes. It is actually a [[derived Deligne-Mumford stack]].

=--



Let $\mathcal{M}_{1,1}$ be the ordinary [[moduli stack]] of [[elliptic curve]]s. 


Using constructions in [[nLab:elliptic cohomology]] we may associate to each [[nLab:elliptic curve]] over $R$, i.e. each morphism $\phi : Spec R \to \mathcal{X}$, an [[nLab:E-infinity ring]] $E_\phi$ -- the multiplicative spectrum that represents the elliptic cohomology theory given by $T$.

This gives an $E_\infty$-ring valued structure sheaf

$$
  \mathcal{O}^{Der} : (\phi : Spec R \to \mathcal{X}) \mapsto
  E_\phi
  \,.
$$


**Question** What, if anything, is this derived stack a derived [[moduli stack]] of?




### the classification of derived elliptic curves ###


The big theorem is that the derived space $(\mathcal{X}, \mathcal{O}^{Der})$ classifies derived elliptic curves over $E_\infty$-rings

This is the theorem that we said above we wanted to consider, stated now a little bit more precisely.


+-- {: .un_theorem }
###### Theorem
**(J. Lurie)**

For

* $A$ any [[E-∞ ring]]

* and $E(A)$ is the space of [[derived elliptic curve]]s over $A$ (the realization of the topological category of elliptic curves over $A$).

we have an equivalence

$$
  Hom(Spec A, (\mathcal{X}, \mathcal{O}^{Der}))  
  \simeq
  E(A)
$$

naturally in $A$.

=--


+-- {: .proof}
###### Proof

We proceed in these steps:

1. consider the presheaf of preoriented ellitptic curves $E'(A)$ first

1. observe that this restricted to ordinary rings produces the ordinary moduli stack

1. notice that every oo-stack with good deformation theory that restricts this way is a derived Deligne-Mumford stack $(\mathcal{X}, \mathcal{O}')$ that assigns connective $E_\infty$-rings over affines

1. let $\omega$ be the line bundle on $\mathcal{M}_{1,1}$ regarded as a coheren sheaf. There is then from the preorientation of the universal curve over $(\mathcal{M}, \mathcal{O}')$ a morphism

   $$
     \beta : \omega \to \pi_2 \mathcal{O}'
   $$

1. let $\mathcal{O}$ be the sheaf obtained from $\mathcal{O}'$ by inverting $\beta$

1. show that

   1. for $n = 2 k $ we have an isomorphism $\omega^k \to \pi_{2 k}\mathcal{O}$

   1. for $n = 2 k + 1$ we have an isomorphism $0 \to \pi_{2k +1}\mathcal{O}$

      strategy: reduce to neighbourhood of a point

1. notice that this implies the desired statement

=--
