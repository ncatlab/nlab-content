

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#

* automatic table of contents goes here
{:toc}


## Idea 

The [[space]]s of relevance in many applications -- notably in those related to [[physics]] -- crucially carry more structure than plain [[nLab:topological space|topological space]], they carry certain _geometric_ structure, specified by local model spaces.

### Geometries 

This may be formalized by fixing an [[(∞,1)-category]]
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

* $Str(\mathcal{G})$ are the **$\mathcal{G}$-[[structured (∞,1)-topos]]es**: those $\mathcal{G}$-probeable [[space]]s that have something like an _underlying topological space_ in the generalized form of an underlying **petit [[(∞,1)-topos]]** which is equipped with [[structure sheaf|structure sheaves]] of [[quantity|function quantities]] with values in objects of $\mathcal{G}$;
  
* $Sch(\mathcal{G})$ are the **$\mathcal{G}$-[[generalized scheme]]s**: those $\mathcal{G}$-structured spaces that are not only probeable by object of $\mathcal{G}$, but are **locally [[nLab:isomorphism|isomorphic]] to objects in $\mathcal{G}$**.

  

### Structured $(\infty,1)$-toposes 


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


## Definition 

### Geometry {#Geometry}

+-- {: .un_remark}
###### Summary 

A **geometry** on an [[(∞,1)-category]] $\mathcal{G}$ is a [[Grothendieck topology]] on $\mathcal{G}$ together with 

* the extra structure given the information of which covering morphisms are to be thought of as [[local homeomorphism]]s

* the extra property that it has all finite [[limit]]s.

If only all finite [[product]]s exist we speak of a pre-geometry. Every pregeometry $\mathcal{T}$ extends uniquely $\mathcal{T} \hookrightarrow \mathcal{G}$ to an _enveloping geometry_ $\mathcal{G}$. 

When the objects of the geopmetry $\mathcal{G}$ are thought of as test spaces (affine schemes), the objects of the pregeometry $\mathcal{T} \hookrightarrow \mathcal{G}$ are to be thought of as the [[affine space]]s. This distinction is used to encode [[smooth map|smoothness]] of maps between test spaces: a morphism in $\mathcal{G}$ is smooth if it locally factors through admissible maps between objects in $\mathcal{T}$. 

=--



+-- {: .un_defn}
###### Definition (admissibility structure, [[Structured Spaces|StSp]] )

An **admissibility structure** on an [[(∞,1)-category]] $\mathcal{G}$ is a [[Grothendieck topology]] on $\mathcal{G}$ that is generated from its intersection with a subcategory $\mathcal{G}^{ad} \subset \mathcal{G}$ whose morphisms -- called the  **admissible morphisms** have the following properties

* admissible morphisms are stable under [[pullback]];

* admissible morphism satisfy [[category with weak equivalences|2-out-of-3]].

Equivalently, this is a [[Grothendieck topology]] on $\mathcal{G}$ which is _generated_ from admissible morphisms.

=--

+-- {: .un_remark}
###### Admissibility 

As will become clear when looking at examples, the notion of
admissible morphisms models the idea of maps between test spaces that behave like _open injections_ or, more generally, as _local homeomorphisms_ .

=--


+-- {: .un_defn}
###### Definition ( [[Structured Spaces]] 1.2.5 )

A **geometry (for $(\infty,1)$-toposes)** is 

* An [[(∞,1)-category]] $\mathcal{G}$ that

  * is [[essentially small category|essentially small]];
  
  * has all finite [[limit]]s
  
  * is [[idempotent complete category|idempotent complete]].

* equipped with a _homotopical topology_ .

=--


+-- {: .un_defn}
###### Definition (discrete geometry, [[Structured Spaces|StSp]], 1.2.10)

The **disscrete geometry** $\mathcal{G}^0$ on $\mathcal{G}$ is given by

* the admissible morphisms in $\mathcal{G}$ are precisely the equivalences

* the [[Grothendieck topology]] on $\mathcal{G}$ is trivial: a [[sieve]] is covering only if it is maximal.

Every (essentially small) [[(infinity,1)-category]] $C$ becomes a 
geometry by regarding it as a discrete geometry in the above way.

=--



### Pregeometry {#Pregeometry}

+-- {: .un_defn}
###### Definition (pregeometry, [[Structured Spaces|StSp]], 3.1.1)

A **pregeometry** (for structured [[(∞,1)-topos]]es) is 

* an [[(∞,1)-category]] $\mathcal{T}$;

* equipped with an admissibility structure (homotopical topology)

such that

* $\mathcal{T}$ has all [[product]]s.

=--


+-- {: .un_remark}
###### Remark 


So a geometry differs from a pregeometry in that it is [[idempotent complete category|idempotent complete]] and closed not
only under [[products]] but under all finite [[limit]]s.

Various concepts for geometries have immediate analogues for
pregeometries.

=--



#### Smooth morphisms

+-- {: .un_defn}
###### Definition (smooth morphism, [[Structured Spaces]], 3.1.7)

A morphism $f : X \to S$ in a pregeometry $\mathcal{T}$ is called **smooth**
if it is _locally stably admissaible_ in that there exists a  cover $\{u_i : U_i \to X\}$ (meaning: generators of a covering [[sieve]])
of $X$ by admissible morphisms, such that on $U_i$ the morphism $f$
factors admissibly through some $S \times V_i$ in that there is a commuting
diagram

$$
  \array{
    U_i &\stackrel{u_i}{\to}& X
    \\
    \downarrow && \downarrow
    \\
    S \times V_i &\stackrel{p_1}{\to}& S
  }
  \,.
$$


=--

+-- {: .un_remark}
###### Remark 

To interpret this, recall that we think of 
admissible morphisms as injections of open subsets.

=--

+-- {: .un_prop}
###### Proposition ([[Structured Spaces]], 3.1.8)

* Smooth morphisms are stable under [[pullback]].

* pregeometric $\mathcal{T}$-structures $\mathcal{O} : \mathcal{T} \to \mathcal{X}$  preserve pullbacks of smooth morphisms.


=--







### Structured $(\infty,1)$-topos {#StructTop}

+-- {: .un_defn}
###### Definition (geometry structure on an $(\infty,1)$-topos, [[Structured Spaces|StSp]], 1.2.8)

For $\mathcal{G}$ a geometry, and $T \simeq Sh_\infty(S)$ an [[(∞,1)-topos]],
a **$\mathcal{G}$-structure on the $(\infty,1)$-topos $T$** making it a 
[[structured (∞,1)-topos]] is a [[(∞,1)-functor]]

$$
  C(-) : \mathcal{G} \to T
$$ 

such that

* $C(-)$ is left [[exact functor|exact]] (preserves finite [[limit]]s);

* $C(-)$ satisfies [[codescent]] (the dual notion of [[descent]]): 
  for $\pi : (V = \coprod_i V_i) \to W$ any 
  [[cover]] by admissable morphisms in $G$, the induced morphism
  $$
    C(\pi) : C(V) \to C(W)
  $$
  is an [[effective epimorphism]] in $T$, i.e. its [[?ech nerve]]
  is a [[simplicial resolution]] of $C(W)$:
  $$
    \mathop{&#268;ech}(C(\pi)) \stackrel{\simeq}{\to} C(W)
    \,.
  $$

=--


+-- {: .un_defn}
###### Definition (pregeometry structure on an $(\infty,1)$-topos, [[Structured Spaces|StrSp]] 3.1.4)

Let $\mathcal{T}$ be a pregeometry and $\mathcal{X}$ an [[(∞,1)-topos]].

A **$\mathcal{T}$-structure** on $\mathcal{X}$ is an [[(infinity,1)-functor]]
$\mathcal{O} : \mathcal{T} \to \mathcal{X}$ such that

* $\mathcal{O}$ preserves finite [[product]]s.

* $\mathcal{O}$ preserves [[pullback]]s of  admissible morphism
  in that for every [[pullback]] diagram

  $$
    \array{
      U' &\to& U
      \\
      \downarrow && \downarrow^f
      \\
      X' &\to& X
    }
  $$
  
  in $\mathcal{T}$ with $f$ admissable, the image
  
  $$
    \array{
      \mathcal{O}(U') &\to& \mathcal{O}(U)
      \\
      \downarrow && \downarrow^f
      \\
      \mathcal{O}(X') &\to& \mathcal{O}(X)
    }
  $$
  
  is again a [[pullback]].
  
* $\mathcal{O}$ respects covers by admissable morphisms in that for every
  covering sieve $\{f_i : U_i \to X\}$ in $\mathcal{T}$ by admissble $f_i$
  the induced map $\coprod_i \mathcal{O}(U_i) \to \mathcal{O}(X)$
  is an [[effective epimorphism]] in $\mathcal{X}$.

=--

+-- {: .un_defn}
###### Definition (geometric envelope, [[Structured Spaces|StrSp]] 3.4.1)

...the universal geometry extending a pregeometry...

=--



+-- {: .un_prop}
###### Proposition ([[Structured Spaces|StSp]]  3.4.5) 


Let $\mathcal{T}$ be a pregeometry and $f : \mathcal{T} \to \mathcal{G}$
a morphism that exhibts the geometry $\mathcal{G}$ as a geometric envelope
of $\mathcal{T}$. Then for every [[(∞,1)-topos]] $\mathcal{X}$ precomposition with $f$ induces an equivalence of 
[[(infinity,1)-category|(∞,1)-categories]] of $\mathcal{T}$- and
$\mathcal{G}$-structures on $\mathcal{X}$:

$$
  Str_{\mathcal{G}}(\mathcal{X}) \stackrel{\simeq}{\to}
  Str_{\mathcal{T}}(\mathcal{X})
  \,,\;\;\;\;
  Str_{\mathcal{G}}(\mathcal{X})^{loc} \stackrel{\simeq}{\to}
  Str_{\mathcal{T}}(\mathcal{X})^{loc}
$$

=--




## Examples 

### Deligne-Mumford stacks 

There is a geometry $\mathcal{G} = \mathcal{G}_{et}(k)$, the _etale geometry_, such that $\mathcal{G}$-[[generalized scheme]]s that are [[n-localic (∞,1)-topos|1-localic]] are precisely [[Deligne-Mumford stack]]s. See there for more details.

### Derived smooth manifolds 

There should be a geometry $\mathcal{G}$ such that $\mathcal{G}$-[[generalized scheme]]s are precisely [[derived smooth manifold]]s.

## References 

The general theory is developed in

* **StrSh** [[Jacob Lurie]], _[[Structured Spaces]]_

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

The special case of "smoothly structured spaces" called [[derived smooth manifold]] is  discussed in 

* [[David Spivak]], _Derived smooth manifolds_ PhD thesis ([original version pdf](http://www.uoregon.edu/~dspivak/files/thesis1.pdf) [arXiv:0810.5174](http://arxiv.org/abs/0810.5174)) 

Apart from looking at the special case this article also contains useful introduction
and details on the general case.

In the version of this that is available on the arXiv ([arXiv](http://arxiv.org/abs/0810.5174))
the point of view is more on bi-presheaves, a useful discussion to the relation
to structured morphisms here is in section 10.1. there.


[[!redirects geometry (for structured (∞,1)-toposes)]]
[[!redirects pregeometry (for structured (infinity,1)-toposes)]]
[[!redirects pregeometry (for structured (∞,1)-toposes)]]