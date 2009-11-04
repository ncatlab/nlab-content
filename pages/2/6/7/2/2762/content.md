

<div class="rightHandSide toc">


[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]


***

[[!include cohomology - contents]]

</div>


>**Abstract** We sketch some basic ideas ([[Jacob Lurie]]'s ideas, that is) about [[higher geometry]] motivated from the [[higher category theory|higher]] version of the [[moduli stack]] of [[elliptic curve]]s: the derived moduli stack of [[derived elliptic curve]]s. We survey aspects of the theory of [[generalized scheme]]s and then sketch how the derived moduli stack of derived elliptic curves is an example of a generalized scheme modeled on the formal dual of [[E-∞ ring]]s.


+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

=--

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


## Notions of Space  ##

The statement that we are after really lives in the context of [[higher geometry]] (often called "derived geometry"). Here is an outline of the central aspects. 


The **central ingredient** which we choose at the beginning to get a theory of [[higher geometry]] going is an [[(∞,1)-category]] $\mathcal{G}$ whose objects we think of as **model spaces** : the simplest objects exhibiting the geometric structures that we mean to consider.

+-- {: .standout}

**Examples for categories of model spaces**

* with smooth structure

  * $\mathcal{G} = $ [[Diff]], the category of smooth [[manifold]]s;

  * $\mathcal{G} = \mathbb{L}$, the category of [[smooth locus|smooth loci]];

* without smooth structure

  * $\mathcal{G} = (C Ring^{fin})^{op}$, the formal dual of [[CRing]]: the category of (finitely generated) algebraic [[affine scheme]]s;

  * $\mathcal{G} = (sC Ring^{fin})^{op}$, the formal dual of [[simplicial object]]s in  [[CRing]];

  * $\mathcal{G} = (E_\infty Ring^{fin})^{op}$, the formal dual of [[E-∞ ring]]s: the category of (finitely generated) algebraic derived [[affine scheme]]s.

=--


These [[(∞,1)-category|(∞,1)-categories]] $\mathcal{G}$ are naturally equipped with the structure of a [[site]] (and a bit more, which we won't make explicit for the present purpose). Following [[Jacob Lurie]] we call such a $\mathcal{G}$ a **[[geometry (for structured (infinity,1)-toposes)|geometry]]** . 

We want to be talking about generalized spaces _modeled on_ the objects of $\mathcal{G}$. There is a hierarchy of notions of what that may mean:

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
    Sh_{(\infty,1)}(Pro(\mathcal{G}))
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


### spaces probeable by model spaces: $\infty$-stacks ###

An object $X$ _probeable_ by objects of $\mathcal{G}$ should come with an assignment

$$
  X : (U \in \mathcal{G}) \mapsto (X(U) \in \infty Grpd)
$$

of an [[∞-groupoid]] of possible ways to probe $X$ by $U$, for each possible $U$, natural in $U$. More precisely, this should define an object in the [[(∞,1)-category of (∞,1)-presheaves]] on $\mathcal{G}$

$$
   X \in PSh(\mathcal{G}) 
   = 
   Funct(\mathcal{G}^{op}, \infty Grpd)
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

The [[∞-stack]]s on $\mathcal{G}$ that are used in the following are those that satisfy [[descent]] on [[Cech cover]]s. But we will see [[(∞,1)-topos]]es of [[∞-stack]]s that may satisfy different descent conditions, in particular with respect to [[hypercover]]s. Every [[∞-stack]] [[(∞,1)-topos]] has a [[hypercompletion]] to one of this form.

For concretely working with [[hypercomplete (∞,1)-topos]]es it is often useful to use [[models for ∞-stack (∞,1)-toposes]] in terms of the [[model structure on simplicial presheaves]].

+-- {: .standout}

$$
  \array{
    Sh^{hc}_{(\infty,1)}(C) 
   &\stackrel{\stackrel{\;\;\;\;\;lex\;\;\;\;\;\;}{\leftarrow}}  
  {\hookrightarrow}&
     PSh_{(\infty,1)}(C)
    && \text{abstract nonsense def of (∞,1)-topos}
    \\
    \uparrow^{\simeq} &&
    \uparrow^{\simeq}
    && \text{Lurie's theorem}
    \\
    ([C^{op}, SSet]_{loc})^\circ
    &\stackrel{\stackrel{Bousfield\;loc.}{\leftarrow}}{\to}&
    ([C^{op}, SSet]_{glob})^\circ
    &&
    \text{model category of simplicial presheaves}
  }
$$

=--

+-- {: .un_remark}
###### Warning

This discussion here is glossing over all set-theoretic size issues. See [[Structured Spaces|StSp, warning 2.4.5]].

=--

### concrete spaces co-probeable by model spaces: structured $(\infty,1)$-toposes ###

Spaces probeable by $\mathcal{G}$ in the above sense can be very general. They need not even have a _concrete underlying space_ , even for general definitions of what _that_ might mean.

**(Counter-)Example** For $\mathcal{G} = $ [[Diff]], for every $n \in \mathbb{N}$ we have the [[∞-stack]] $\Omega_{cl}^n(-)$ (which happens to be an ordinary [[sheaf]]) that assigns to each manifold $U$ the set of closed [[differential form|n-form]]s on $U$. This is important as a generalized space: it is something like the rational version of the [[Eilenberg-MacLane space]] $K(\mathbb{Z}, n)$. But at the same time this is a "wild" space that has exotic properties: for instance for $n=3$ this space has just a single point, just a single curve in it, just a single surface in it, but has many nontrivial probes by 3-dimensional manifolds.

In the classical theory for instance of [[ringed space]]s or [[diffeological space]]s a _concrete underlying space_ is taken to be a [[topological space]]. But this in turn is a bit _too_ restrictive for general purposes: a topological space is the same as a [[localic topos]]: a [[category of sheaves]] on a [[category of open subsets]] of a [[topological space]]. The obvious generalization of this to [[higher geometry]] is: an [[n-localic (∞,1)-topos]] $\mathcal{X}$.

This makes us want to say and make precise the statement that

+-- {: .standout}

An **concrete [[∞-stack]]** $X$ is one which has an _underlying_ [[(∞,1)-topos]] $\mathcal{X}$:

the collection of $U$-probes of $X$ is a subobject of the collection of [[(∞,1)-topos]] morphisms from $U$ to $mathcal{X}$:

$$
  X(U) \subset \mathcal{L}Top(\mathcal{G})^{op}(Sh_{\infty}(U),\mathcal{X})
$$

=--


We think of $\mathcal{X}$ as the [[(∞,1)-topos]] of [[∞-stack]]s on a category of open subsets of a would-be space $X$, only that this would be space $X$ might not have an independent existence as a space apart from $\mathcal{X}$. The available entity closest to it is the [[terminal object]] ${*}_{\mathcal{X}} \in \mathcal{X}$. 

To say that $\mathcal{X}$ is _modeled on $\mathcal{G}$_ means that among all the [[∞-stack]]s on the would-be space a [[structure sheaf]] of functions with values in objects of $\mathcal{G}$ is singled out: for each object $V \in \mathcal{G}$ there is a [[structure sheaf]] $\mathcal{O}(-,V) \in \mathcal{X}$, naturally in $V$.

This yields an [[(∞,1)-functor]]

$$
  \mathcal{O} : \mathcal{G} \to \mathcal{X}
  \,.
$$

We think of $X$ as being a concrete space _co-probebale_ by $\mathcal{G}$ (we can map from the concrete $X$ into objects of $\mathcal{G}$).

Such an $\mathcal{O}$ is a _consistent_ collection of coprobes if coprobes with values in $V$ may be reconstructed from co-probes with values in pieces of $V$.

More precisely:

+-- {: .un_def}
###### Definition
**($\mathcal{G}$-structure, [[Structured Spaces|StSp, def. 1.2.8]])**

An [[(∞,1)-functor]] $\mathcal{O} : \mathcal{G} \to \mathcal{X}$  is a **$\mathcal{G}$-valued structure sheaf** on the [[(∞,1)-topos]] if

* it preserves finite [[limit]]s 

* and sends covering coproducts $(\coprod_i U_i) \to U$ to [[effective epimorphism]]s.

A pair $(\mathcal{X}, \mathcal{O})$ of an [[(∞,1)-topos]] $\mathcal{X}$ equipped with $\mathcal{G}$-valued [[structure sheaf]] $\mathcal{O} : \mathcal{G} \to \mathcal{X}$ we call a [[structured (∞,1)-topos]].

=--

In summary:

+-- {: .standout}

A **concrete [[∞-stack]] $X$ modeled on $\mathcal{G}$** is 

* an [[(∞,1)-topos]] $\mathcal{X}$ ("of $\infty$-stacks on $X$")

* equipped with a $\mathcal{G}$-valued structure sheaf $\mathcal{O}$ in the form of a finite limits and cover preserving functor $\mathcal{O} : \mathcal{G} \to \mathcal{X}$.

=--

The fundamental **example** for [[structured (∞,1)-topos]]es
are provided by the objects of $\mathcal{G}$ themselves, which are canonically equipped with a $\mathcal{G}$-structure as follows.

+-- {: .un_theorem}
###### Theorem
**([[Structured Spaces|StSp, thm. 2.1.1]])**

Let $f : \mathcal{G} \to \mathcal{G}'$ be a morphism of [[geometry (for structured (infinity,1)-toposes)|geometries], 
then the obvious [[(∞,1)-functor]] $f^* : \mathcal{L}Top(\mathcal{G}) \to \mathcal{L}Top(\mathcal{G}')$ admits a [[left adjoint]]

$$
  f^*
  :
  \mathcal{L}Top(\mathcal{G}') 
   \stackrel{\leftarrow}{\to} 
  \mathcal{L}Top(\mathcal{G}) 
  :
  Spec_{\mathcal{G}}^{\mathcal{G}'}
$$

called the **relative spectrum functor**.

=--

For $\mathcal{G}$ any [[geometry (for structured (infinity,1)-toposes)|geometry]], write $\mathcal{G}_{disc}$ for the [[geometry (for structured (infinity,1)-toposes)|geometry]] obtained from this by forgetting its [[coverage|Grothendieck topology]] and instead using the discrete topology where only equivalences cover.

Notice 
that we may identify $\mathcal{G}_{disc}$-structures on 
the archetypical [[(∞,1)-topos]] [[∞Grpd]], being finite [[limit]]-preserving functors $\mathcal{G}_{disc}^{op} \to \infty Grpd$
with [[ind-object]]s in $\mathcal{G}^{op}$, hence with the 
opposite of [[pro-object]]s in $\mathcal{G}$. This gives a canonical inclusion

$$
  Pro(\mathcal{G}) 
    \hookrightarrow 
  \mathcal{L}Top(\mathcal{G})^{op}
  \,.
$$


+-- {: .un_def}
###### Definition
**([[Structured Spaces|StSp, def. 2.1.2]])**

The composite [[(∞,1)-functor]]

$$
  Spec^{\mathcal{G}}
  : 
  Pro(\mathcal{G})^{op}
  \hookrightarrow 
  \mathcal{L}Top(\mathcal{G}_{disc})
  \stackrel{Spec_{\mathcal{G}}^{\mathcal{G}_{disc}}}{\to}
  \mathcal{L}Top(\mathcal{G})
$$

we call the **absolute spectrum functor**

=--

This [[category theory|abstract nonsense]] is reassuring, but we want a more concrete definition of what such $Spec^{\mathcal{G}} U$ is like:

+-- {: .un_def}
###### Definition
**([[Structured Spaces|StSp, def. 2.2.9]])**

For every $U \in \mathcal{G}$ there is naturally induced a [[coverage|topology]] on the [[over category]] $Pro(\mathcal{G})/U$. Define the [[(∞,1)-topos]]

$$
  Spec U := Sh_{(\infty,1)}(Pro(\mathcal{G})/U)
  \,,
$$

naturally to be thought of as the [[(∞,1)-topos]] of [[∞-stack]]s _on $U$_ .

This is canonically equipped with a [[(∞,1)-functor]]

$$
  \mathcal{O}_{Spec X}
  : 
  \mathcal{G} \to Spec X
  \,.
$$

=--

And this is indeed the concrete underlying space produced by the absolute spectrum functor:

+-- {: .un_theorem}
###### Theorem
**[[Structured Spaces|StSp, prop. 2.2.11, thm. 2.2.12]])**

For every $U \in \mathcal{G}$ the pair $(Spec U, \mathcal{O}_{Spec U})$ is indeed a [[structured (∞,1)-topos]] and is indeed equivalent to the $Spec^{\mathcal{G}} U$ defined more abstractly above.

=--


**Example** For $\mathcal{G} = (C Ring^{fin})^{op}$ with the standard [[coverage|topology]] we have that 0-localic $\mathcal{G}$-structured spaces are _[[locally ringed space]]s_ , while $\mathcal{G}_{disc}$-structured 0-localic spaces are just arbitrary [[ringed space]]s. Applying the above machinery to this situaton gives a spectrum functor that takes a [[ring]] $R$ first to the [[ringed space]] $({*,R})$ and this then to the [[locally ringed space]] $(Spec R, R)$. 



### spaces locally like model spaces: generalized schemes ###

We have seen that $\mathcal{G}$-[[structured (∞,1)-topos]]es are those general spaces modeled on $\mathcal{G}$ that are well-behaved in that at least they do have an "underlying topological structure" in the form of an underlying [[(∞,1)-topos]]. But such concrete spaces may still be very different from the model objects in $\mathcal{G}$.

In parts this is desireable: many objects that one would naturally build out of the objects in $\mathcal{G}$, such as mapping spaces $[\Sigma,X]$, are much more general than objects in $\mathcal{G}$ but do live happily in $\mathcal{L}Top(\mathcal{G})^{op}$.

But in many situations one would like to regard $\mathcal{G}$-[[structured (∞,1)-topos]]es that are not globally but _locally_ equivalent to objects in $\mathcal{G}$. This is supposed to be captured by the following definition.

+-- {: .un_def}
###### Definition
**[[Structured Spaces|StSp, def. 2.3.9]]

A [[structured (∞,1)-topos]] $(\mathcal{X}, \mathcal{O})$ is a **$\mathcal{G}$-generalized scheme** if

* there exists a collection $\{V_i \in \mathcal{X}\}$

* such that

  * this covers $\mathcal{X}$ in that the canonical morphism

    $$ 
      (\coprod_i V_i) \to {*}_{\mathcal{X}}
    $$

    to the [[terminal object]] in $\mathcal{X}$ 
    is an [[effective epimorphism]]

  * the [[structured (∞,1)-topos]]es     
    $(\mathcal{X}/V_i, \mathcal{O}|_{V_i})$ induced by
    the $V_i$ are model spaces in that there exists 
    $\{U_i \in \mathcal{G}\}$ and equivalences

    $$
      (\mathcal{X}/V_i, \mathcal{O}|_{V_i})
      \simeq
      Spec^{\mathcal{G}} U_i
    $$

=--

> **warning** these statement pertain to pregeometries, not geometries. for the moment this here is glossing over the difference between the two. See [[geometry (for structured (∞,1)-toposes)]] for the details.

**examples**

* ordinary smooth [[manifold]]s are [[n-localic (infinity,1)-topos|0-localic]] [[Diff]]-[[generalized scheme]]s ([Structured Spaces|StSp, ex. 4.5.2]])

* ordinary [[schemes]] are those $(CRing^{fin})^{op}$-[[generalized scheme]]s whose underlying [[(∞,1)-topos]] is
[[n-localic (infinity,1)-topos|0-localic]] and whose [[structure sheaf]] is [[n-truncated object of an (infinity,1)-category|0-truncated]]  ([Structured Spaces|StSp, prop. 4.2.9]])

* [[Deligne-Mumford stack]]s are 1-localic $(CRing^{fin})_{et}^{op}$-[[generalized scheme]]s ([Structured Spaces|StSp, prop. 4.2.9]])

* This last statement is then the basis for calling a general $(CRing^{fin})_{et}^{op}$-[[generalized scheme]] a **derived Deligne-Mumford stack

* Finally, to make contact with the application to the derived moduli stack of derived elliptic curves, it seems that in [[Spectral Schemes]] a derived Deligne-Mumford stack (with derived in the sense of having replaced ordinary commutative rings by [[E-∞ ring]]s) is gonna be a 1-localic  $(E_\infty Ring^{fin})^{op}$-[[generalized scheme]].





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


Using constructions in [[elliptic cohomology]] we may associate to each [[elliptic curve]] over $R$, i.e. each morphism $\phi : Spec R \to \mathcal{X}$, an [[E-infinity ring]] $E_\phi$ -- the multiplicative spectrum that represents the elliptic cohomology theory given by $T$.

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

Jacob Lurie writes that the proof proceeds alonmg these steps. Details will be discussed in the next session.

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


