<div class="rightHandSide toc">
[[!include higher geometry - contents]]
</div>


#Contents#

* automatic table of contents goes here
{:toc}


# Idea #

The [[space]]s of relevance in many applications -- notably in those related to [[physics]] -- crucially carry more structure than plain [[nLab:topological space|topological space]], they carry certain _geometric_ structure, specified by local model spaces.

## geometries ##

This may be formalized by fixing a an [[(∞,1)-category]]
$\mathcal{G}$ whose objects we think of as **loci** -- test spaces with which all spaces with $\mathcal{G}$-geometry structure may be probed -- and whose morphisms we think of maps between loci that respect the geometric structure in question.

Since the specification of $\mathcal{G}$ encodes what we want to _mean_ by _geometric structure_, $\mathcal{G}$ is called a **geometry**.

By the general abstract nonsense of [[space and quantity]], the most general notion of [[space]] modeled on the test objects in $\mathcal{G}$ is an [[∞-stack]] on $\mathcal{G}$. We write

$$
  \mathbf{H} := Sh_\infty(Pro(C))
$$

for a choice of [[(∞,1)-category of (∞,1)-sheaves]] on [[pro-object]]s in $\mathcal{G}$: the **gros [[(∞,1)-topos]] of $\mathcal{G}$-geometric spaces**.
The choice of $\mathbf{H}$ on top of the choice of $\mathcal{G}$ encodes the notion **locality** of spaces modeled on $\mathcal{G}$.

The [[Yoneda embedding]] $\mathcal{G} \hookrightarrow Sh_\infty(\mathcal{G})$ ensures that every test space in $\mathcal{G}$ may canonically be regarded as a general space modeled on $\mathcal{G}$. When studying geometry it is of interest to refine this inclusion of very simple into very general spaces through a hierarchy
of types of spaces of decreasing rigid geometric structure, for instance:

$$
  \array{
    \mathcal{G} &\stackrel{Spec^{\mathcal{G}}}{\hookrightarrow}& Sch(\mathcal{G}) &\hookrightarrow&
   Sh_\infty(Pro(\mathcal{G}))
   \\
    && \downarrow && \downarrow
   \\
   && Str(\mathcal{G}) &\hookrightarrow& PSh_\infty(Pro(\mathcal{G}))
  }
$$

where 

* $Str(\mathcal{G})$ are the **$\mathcal{G}$-[[structured (∞,1)-topos]]es**: those $\mathcal{G}$-probeable [[space]]s that have something like an _underlying topological space_ in the generalized form of an underlying **petit [[nLab:(∞,1)-topos]]** which is equipped with [[structure sheaf|structure sheaves]] of [[quantity|function quantities]] with values in objects of $\mathcal{G}$;
  
* $Sch(\mathcal{G})$ are the **$\mathcal{G}$-[[generalized scheme]]s**: those $\mathcal{G}$-structured spaces that are not only probeable by object of $\mathcal{G}$, but are **locally [[nLab:isomorphism|isomorphic]] to objects in $\mathcal{G}$**.

## noncommutative geometries? ##  

Other shades of structures spaces in this hierarchy may be conceivable. For instance the [[stable (∞,1)-category|stable (∞,1)-categories]] that are used in [[noncommutative algebraic geometry]]  -- and there usually modeled in terms of [[triangulated category|triangulated categories]] -- should be on a similar conceptual footing as the petit $(\infty,1)$-toposes above: collections of generalized sheaves that characterize in their totality a certain geometric space.
  

## Structured $(\infty,1)$-toposes ##


A [[structured (∞,1)-topos]] $T \simeq Sh_\infty(S)$ is 
an [[(∞,1)-topos]] equipped
with a generalized [[quantity]] : a $C$-valued co-presheaf

$$
  C(-) : G \to T
$$

on some [[(∞,1)-category]] $G$. 

This is to be interpreted as

* assigning to each object $V \in G$ -- which we think of a _co-test space_

* the [[(∞,1)-sheaf]] of _structure preserving maps_ from $S$ to $V$,

  * i.e. the sheaf that assigns to each test space $U \in S$ the collection of _structure preserving maps_ from $U$ to $V$

Here the structure that is "preserved" is 
to be thought of as _defined_ (implicitly) by the choice of $C(-)$, following the
general idea of [[space and quantity]]. 

In standard motivating example (in the context of [[petit topos]]es), that of [[derived smooth manifold]]s, we have

* $S = Op(X)$ is the [[category of open subsets]] of a [[topological space]] $X$

* $G = CartSp$ is the full [[subcategory]] of [[Diff]] 
  on Cartesian [[manifold]]s (manifolds of the form
  $\mathbb{R}^n$)
  
* the choice $C(-) : G \to Sh_\infty(Op(X))$ is to be thought of as specifying
  a [[differential geometry]] on $X$ in that it amounts to specifying for each
  open (topological!) subset $U \subset X$ the collection of maps $U \to \mathbb{R}^n$
  that are to count as _smooth_ .
  
It is in this sense that one thinks of $G$ as encoding **geometry** over
topology: $G$ is to be thought of as a category of co-test spaces that are
topological spaces equipped with extra geometrical structure.


# Definition #

+-- {: .un_defn}
###### Definition

A **homotopical topology** on an [[(∞,1)-category]] $\mathcal{G}$ is a [[Grothendieck topology]] on $\mathcal{G}$ that is generated from its intersection with a subcategory $\mathcal{G}^{ad} \subset \mathcal{G}$ whose morphisms -- called the  **admissable morphisms** have the following properties

* admissable morphisms are stable under [[pullback]];

* admissable morphism satisfy [[category with weak equivalences|2-out-of-3]].
=--

+-- {: .un_defn}
###### Definition

A **geometry (for $(\infty,1)$-toposes)** is 

* An [[(∞,1)-category]] $\mathcal{G}$ that

  * is [[essentially small category|essentially small]];
  
  * has all finite [[limit]]s
  
  * is [[idempotent complete category|idempotent complete]].

* equipped with a _homotopical coverage_ .
=--

+-- {: .un_defn}
###### Definition

For $\mathcal{G}$ a geometry, and $T \simeq Sh_\infty(S)$ an [[(∞,1)-topos]],
a **$\mathcal{G}$-structure on the $(\infty,1)$-topos $T$** making it a 
[[structured (∞,1)-topos]] is a [[(∞,1)-functor]]

$$
  C(-) : \mathcal{G} \to T
$$ 

such that

* $C(-)$ is left [[exact functor|exact]] (preserves finite [[limit]]]s);

* $C(-)$ satisfies [[codescent]] (the dual notion of [[descent]]): 
  for $\pi : (V = \coprod_i V_i) \to W$ any 
  [[cover]] by admissable morphisms in $G$, the induced morphism
  $$
    C(\pi) : C(V) \to C(W)
  $$
  is an [[effective epimorphism]] in $T$, i.e. its [[Cech nerve]]
  is a [[simplicial resolution]] of $C(W)$:
  $$
    Cech(C(\pi)) \stackrel{\simeq}{\to} C(W)
    \,.
  $$
=--

# Examples #

## Deligne-Mumford stacks ##

There is a geometry $\mathcal{G} = \mathcal{G}_{et}(k)$, the _etale geometry_, such that $\mathcal{G}$-[[generalized scheme]]s that are [[n-localic (∞,1)-topos|1-localic]] are precisely [[Deligne-Mumford stack]]s. See there for more details.

## derived smooth manifolds ##

There should be a geometry $\mathcal{G}$ such that $\mathcal{G}$-[[generalized scheme]]s are precisely [[derived smooth manifold]]s.

# References #

The general theory is developed in

* **StrSh** [[Jacob Lurie]], [[Structured Spaces]]

The definition of a **geometry** $\mathcal{G}$ is def. 1.2.5.

A $\mathcal{G}$-stucture on an [[(infinity,1)-topos]] is in def. 1.2.8.

The notion of $\mathcal{G}$-spectrum -- which are [[(infinity,1)-topos]]es -- is the subject of section 2.1 .

The inclusion

$$
  Spec^{\mathcal{G}} : 
  \mathcal{G} \hookrightarrow Str(\mathcal{G})
$$

is definition 2.1.2.

The definition of $\mathcal{G}$-[[generalized scheme]] is definition 2.3.9, page 51.

The inclusion

$$
  Sch(\mathcal{G}) \hookrightarrow Sh_\infty(Ind(\mathcal{G}))
$$

is the topic of section 2.4, theorem 2.4.1

The special case of "smoothly structured spaces" called [[derived smooth manifold]] is 
discussed in 

* [[David Spivak]], _Derived smooth manifolds_ PhD thesis ([pdf](http://www.uoregon.edu/~dspivak/files/thesis1.pdf))

Apart from looking at the special case this article also contains useful introduction
and details on the general case.

In the version of this that is available on the arXiv ([arXiv](http://arxiv.org/abs/0810.5174))
the point of view is more on bi-presheaves, a useful discussion to the relation
to structured morphisms here is in section 10.1. there.


[[!redirects geometry (for structured (∞,1)-toposes)]]