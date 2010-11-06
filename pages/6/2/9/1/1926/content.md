

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
* table of contents
{:toc}


## Idea 

In the context of [[structured (∞,1)-topos]]es a _pre-geometry_ is an [[(∞,1)-algebraic theory]] $\mathcal{T}$, such that the _structure $(\infty,1)$-sheaf_ of an [[little topos|little]] [[(∞,1)-topos]] $\mathcal{X}$ _with $\mathcal{T}$-structure_ is a $\mathcal{T}$-algebra in $\mathcal{X}$, hence a [[(∞,1)-limit|(∞,1)-product]]-preserving [[(∞,1)-functor]]

$$
  \mathcal{O} : \mathcal{T} \to \mathcal{X}
  \,.
$$

If we think of $\mathcal{X} = Sh_{(\infty,1)}(C)$ as an [[(∞,1)-sheaf (∞,1)-topos]] then this encodes precisely an $(\infty,1)$-sheaf of $\mathcal{T}$-algebras on $C$. Extra conditions on $\mathcal{O}$ ensure that this indeed looks like a sheaf of geometric-structure-preserving functions.

A _geometry_ $\mathcal{G}$ is a universal completion of a pre-geometry under [[(∞,1)-limit]]s, such that this $\mathcal{O}$ is equivalently an $(\infty,1)$-limit preserving $(\infty,1)$-functor

$$
  \mathcal{O} : \mathcal{G} \to \mathcal{X}
$$

subject to a condition that ensures that this looks like an $(\infty,1)$-sheaf of $\infty$-functions algebras.

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

A **$\mathcal{T}$-structure** on $\mathcal{X}$ is an [[(∞,1)-functor]]
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

+-- {: .un_remark}
###### Remark

The first clause says that $\mathcal{O} : \mathcal{T} \to \mathcal{X}$ is in particular an $\infty$-algebra over the (multi-sorted) [[(∞,1)-algebraic theory]] $\mathcal{T}$.

The other two clauses encode that this this $\infty$-algebra $mathcal{O}$ indeed behaves like a _function algebra_ . 

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

* [[Jacob Lurie]], _[[Structured Spaces]]_
{#Lurie}

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