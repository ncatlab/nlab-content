
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


A _smooth manifold_ is a [[space]] that is _locally [[isomorphic]]_ to a [[Cartesian space]] $\mathbb{R}^n$ equipped with its canonical [[smooth structure]].


## Definition

### Traditional definition

Traditionally, a _smooth manifold_ is defined as follows.

#### As special topological manifolds

+-- {: .un_defn}
###### Definition

A [[manifold]] is a **smooth manifold** if its transition functions are [[smooth function]]s $\mathbb{R}^n \to \mathbb{R}^n$. 

So a smooth manifold is a $C^k$-[[differentiable manifold]] for all $k$.

A [[homomorphism]] of smooth manifolds is a [[smooth function]]s. Smooth manifolds and smooth functions form the category [[Diff]].


=--

#### As special locally ringed spaces


+-- {: .un_prop}
###### Proposition

A  smooth manifold is equivalently a  [[locally ringed space]] $(X,\mathcal{O}_X)$ which is locally isomorphic to the ringed space $(\mathbb{R}^n, C^\infty(-) )$.

(...)

=--



### General abstract geometric definition

There is a more fundamental and [[category theory|general abstract]] way to think of smooth manifolds, which realizes their theory as a special case of general constructions in [[higher geometry]]. In this context one specifies $\mathcal{G}$ a [[geometry (for structured (∞,1)-toposes)]] and then plenty of geometric notions are defined canonically in terms of $\mathcal{G}$. The theory of smooth manifolds appears if one takes $\mathcal{G} = $ [[CartSp]]. 

This is discussed in [The geometry CartSp](#TheGeometryCartSp) below.



#### The geometry $CartSp$ {#TheGeometryCartSp}

Let [[CartSp]] be the [[category]] of [[Cartesian space]]s and [[smooth function]]s between them. This has finite [[product]]s and is in fact (the [[syntactic category]]) of a [[Lawvere theory]]: the theory of [[smooth algebras]].

Moreover, $CartSp$ is naturally equipped with the [[good open cover]] [[coverage]] that makes it a [[site]]. 

Both properties together make it a [[pregeometry (for structured (∞,1)-toposes)]] (if the notion of [[Grothendieck topology]] is relaxed to that of [[coverage]] in [StrSp](#StrSp)).

For $\mathcal{X}$ a [[topos]], a [[product]]-preserving [[functor]]

$$
  \mathcal{O} : \mathcal{G} \to \mathcal{X}
$$

is a $\mathcal{G}$-[[algebra over an algebraic theory|algebra]] in $\mathcal{X}$. This makes $\mathcal{X}$ is $\mathcal{G}$-[[ringed topos]]. For $\mathcal{G} = $ [[CartSp]] this algebra is a [[smooth algebra]] in $\mathcal{X}$. If $\mathcal{X}$ has a [[site]] of definition $X$, then this is a [sheaf] of [[smooth algebra]]s on $X$. 

If $\mathcal{O}$ sends [[covering]] families $\{U_i \to U\}$ in $\mathcal{G}$ to [[effective epimorphism]] $\coprod_i \mathcal{O}(U_i) \to \mathcal{O}(U)$ we say that it is a _local $\mathcal{G}$-algebra_ in $\mathcal{X}$, making $\mathcal{X}$ a $\mathcal{G}$-[[locally ringed topos]].

The [[big topos]] $Sh(\mathcal{G})$ itself is canonically equipped with such a local $\mathcal{G}$-algebra, given by the [[Yoneda embedding]] $j$ followed by [[sheafification]] $L$

$$
  \mathcal{O} : \mathcal{G} \stackrel{j}{\to} PSh(\mathcal{G}) \stackrel{L}{\to}
  Sh(\mathcal{G})
  \,.
$$

It is important in the context of [[locally representable structured (infinity,1)-topos|locally representable locally ringed toposes]] that we regard $Sh(\mathcal{G})$ as equipped with this local $\mathcal{G}$-algebra. This is what remembers the [[site]] and gives a notion of local representability in the first place.

The [[big topos]] $Sh(CartSp)$ is a [[cohesive topos]] of [[generalized smooth space]]s. Its [[concrete sheaves]] are precisely the [[diffeological space]]s. See there for more details. We now discuss how with $Sh(CartSp)$ regarded as a $CartSp$-structured topos, smooth manifolds are precisely its [[locally representable structured (infinity,1)-toposes|locally representable objects]].

#### Cartesian spaces as representable objects of $Sh(CartSp)$

The representables themselves should evidently be locally representable and canonically have the structure of $CartSp$-structured toposes.

Indeed, every object $U \in \mathrm{CartSp}$ is canonically a [[CartSp]]-[[ringed space]], meaning a [[topological space]] equipped with a local sheaf of [[smooth algebra]]s. More generally: every object $U \in CartSp$ is canonically incarnated as the $CartSp$-[[structured (∞,1)-topos] 

$$
  (\mathcal{X}, \mathcal{O}_{\mathcal{X}})
  :=
  (Sh_{(\infty,1)}(CartSp)/U ,
    \;\;\; \mathcal{O}_U : CartSp \stackrel{j}{\to} Sh_{(\infty,1)}(CartSp) \stackrel{U^*}{\to} Sh_{(\infty,1)}(CartSp)/U)
$$ 

given by the [[over-(∞,1)-topos]] of the [[big topos|big]] [[(∞,1)-sheaf (∞,1)-topos]] over $CartSp$ and the [[structure sheaf]] given by the composite of the [[(∞,1)-Yoneda embedding]] and the [[inverse image]] of the [[etale geometric morphism]] induced by $U$.


#### Smooth manifolds as locally representable objects of $Sh(CartSp)$ {#smoothManifoldsAsLocallyRepresentableObjects}

+-- {: .un_defn}
###### Definition

Say a [[concrete sheaf|concrete object]] $X$ in the [[sheaf topos]] $Sh(CartSp)$ -- a [[diffeological space]] -- is _locally representable_ if there exists a family of open embeddings $\{U_i \hookrightarrow X\}_{i \in X}$ with $U_i \in CartSp \stackrel{j}{\hookrightarrow} Sh(CartSp)$ such that the canonical morphism out of the [[coproduct]]

$$
  \coprod_i U_i \to X
$$

is an [[effective epimorphism]] in $Sh(CartSp)$.

Let $LocRep(CartSp) \hookrightarrow Sh(CartSp)$ be the full [[subcategory]] on locally representable sheaves.

=--

+-- {: .un_prop}
###### Proposition

There is an [[equivalence of categories]]

$$
  Diff \simeq LocRep(CartSp)
$$


of the category [[Diff]] of smooth manifolds with that of locally representable sheaves for the [[geometry (for structured (infinity,1)-toposes)|pre-geometry]] $CartSp$.

=--


+-- {: .proof}
###### Proof


Define a functor $Diff \to LocRep(CartSp)$ by sending each smooth manifold to the sheaf over $CartSp$ that it naturally represents. By definition of [[manifold]] there is an [[open cover]] $\{U_i \hookrightarrow X\}$. We claim that $\coprod_i U_i \to X$ is an [[effective epimorphism]], so that this functor indeed lands in $LocRep(CartSp)$. (This is a standard argument of sheaf theory in [[Diff]], we really only need to observe that it goes through over [[CartSp]], too.)

For that we need to show that

$$
  \coprod_{i, j} U_i \times_X U_j \stackrel{\to}{\to} \coprod_i U_i \to X
$$

is a [[coequalizer]] diagram in $Sh(CartSp)$. Notice that the [[fiber product]] here is just the intersection in $X$ $U_i \times_X U_j \simeq U_i \cap U_j$. By the fact that the [[sheaf topos]] $Sh(CartSp)$ is by definition a [[reflective subcategory]] of the [[presheaf topos]] $PSh(CartSp)$ we have that [[colimit]]s in $Sh(CartSp)$ are computed as the [[sheafification]] of the corresponding colimit in $PSh(CartSp)$. The colimit in $PSh(CartSp)$ in turn is computed objectwise. Using this, we see that that we have a coequalizer diagram

$$
  \coprod_{i, j} U_i \times_X U_j \stackrel{\to}{\to} \coprod_i U_i \to S(\{U_i\})
$$

in $PSh(CartSp)$, where $S(\{U_i\})$ is the [[sieve]] corresponding to the cover: the [[subfunctor]] $S(\{U_i\}) \hookrightarrow X$ of the functor $X : CartSp^{op} \to Set $ which assigns to $V \in CartSp$ the set of [[smooth function]]s $V \to X$ that have the property that they factor through any one of the $U_i$.

Essentially by the definition of the [[coverage]] on $CartSp$, it follows that [[sheafification]] takes this subfunctor inclusion to an [[isomorphism]]. This shows that $X$ is indeed the tip of the coequalizer in $Sh(CartSp)$ as above, and hence that it is a locally representable sheaf.

Conversely, suppose that for $X \in Conc(Sh(CartSp)) \hookrightarrow Sh(CartSp)$ there is a family of open embeddings $\{U_i \hookrightarrow X\}$ such that we have a coequalizer diagram

$$
  \coprod_{i, j} U_i \times_X U_j \stackrel{\to}{\to} \coprod_{i} U_i \to X
$$

in $Sh(CartSp)$, which is the sheafification of the corresponding coequalizer in $PSh(CartSp)$. By evaluating this on the point, we find that the underlying set of $X$ is the coequalizer of the underlying set of the $U_i$ in $Set$. Since every plot of $X$ factors locally through one of the $U_i$ it follows that $X$ is a [[diffeological space]].  

It follows that in the pullback diagrams

$$
  \array{
    U_i \times_X U_j &\to& U_j
   \\
    \downarrow && \downarrow
   \\
   U_i &\to& X 
  }
$$

the object $U_i \cap U_j$ is the diffeological space whose underlying topological space is the intersection of $U_i$ and $U_j$ in the topological space underlying $X$. In particular the inclusions $U_i \times_X U_j \hookrightarrow U_i$ are open embeddings. 

=--

#### As locally representable $CartSp$-structured $(\infty,1)$-toposes

We may switch from regarding smooth manifolds as objects in the [[big topos]] $X \in Sh(CartSp)$ to regrading them as [[topos]]es themselves, by passing to the [[over-topos]] $Sh(CartSp)/X$. This remembers the extra (smooth) structure on the [[topological space]] $X$ by being canonically a [[locally ringed topos]] with the [[structure sheaf]] of [[smooth function]]s on $X$: a [[CartSp]]-[[structured (∞,1)-toposes]]


For every choice of [[geometry (for structured (∞,1)-toposes)]]   there is a notion of $\mathcal{G}$-[[locally representable structured (∞,1)-topos]] ([StrSp](#StrSp)). 

+-- {: .un_prop}
###### Claim

Smooth manifolds are equivalently the [[n-localic (infinity,1)-topos|0-localic]] [[CartSp]]-[[generalized scheme]]s of locally finite presentation.

=--

+-- {: .proof}
###### Sketch of proof

The statement says that a smooth manifold $X$ may be identified with an [[∞-stack]] on [[CartSp]] (an [[∞-Lie groupoid]]) which is represented by a [[CartSp]]-[[structured (∞,1)-topos]] $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ such that

1. $\mathcal{X}$ is a [[n-localic (∞,1)-topos|0-localic (∞,1)-topos]];

1. There exists a family of objects $\{U_i \in \mathcal{X}\}$ such that the canonical morphism $\coprod_i U_i \to *_{\mathcal{X}}$ to the [[terminal object in an (∞,1)-category|terminal object]] in $\mathcal{X}$ is a [[regular epimorphism]];

1. For every $i \in I$ there is an equivalence

  $$
    (\mathcal{X}/U_i, \mathcal{O}_{\mathcal{X}|U_i})
    \underoverset{\simeq}{t_i}{\to} (Sh_{(\infty,1)}(\mathbb{R}^n), \mathcal{O}(\mathbb{R}^n))
     \,.
  $$

The second and third condition say in words that $(\mathcal{X}, \mathcal{O}_{\mathcal{X}})$ is locally equivalent to the ordinary cannonically [[CartSp]]-[[locally ringed space]] $\mathbb{R}^n$ (for $n \in \mathbb{N}$ the [[dimension]]. The first condition then says that these local identifications cover $\mathcal{X}$.

(...)

(...)


=--

## Related concepts

* [[infinite dimensional smooth manifold]]

## References

Standard references on smooth manifolds include

(...)

The general abstract framework of [[higher geometry]] referred to above is discussed in 

* [[Jacob Lurie]], _[[Structured Spaces]]_
{#StrSp}

[[!redirects smooth manifolds]]
