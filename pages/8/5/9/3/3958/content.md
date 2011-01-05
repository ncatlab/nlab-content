
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

Traditionally, a _smooth manifold_ is defined as follows.

+-- {: .un_defn}
###### Definition

A **smooth manifold** is a [[manifold]] if its transition functions are [[smooth function]]s $\mathbb{R}^n \to \mathbb{R}^n$. 

So a smooth manifold is a $C^k$-[[differentiable manifold]] for all $k$.

A [[homomorphism]] of smooth manifolds is a [[smooth function]]s. Smooth manifolds and smooth functions form the category [[Diff]].


=--


There is a more fundamental and [[category theory|general abstract]] way to think of smooth manifolds, which realizes their theory as a special case of general constructions in [[higher geometry]]. In this context one specifies $\mathcal{G}$ a [[geometry (for structured (∞,1)-toposes)]] and then plenty of geometric notions are defined canonically in terms of $\mathcal{G}$. The theory of smooth manifolds appears if one takes $\mathcal{G} = $ [[CartSp]]. 

This is discussed in [The geometry CartSp](#TheGeometryCartSp) below.



### The geometry $CartSp$ {#TheGeometryCartSp}

Let [[CartSp]] be the [[category]] of [[Cartesian space]]s and [[smooth function]]s between them. This has finite [[product]]s and is in fact (the [[syntactic category]]) of a [[Lawvere theory]]: the theory of [[smooth algebras]].

Moreover, $CartSp$ is naturally equipped with the [[good open cover]] [[coverage]] that makes it a [[site]]. 

Both properties together make it a [[pregeometry (for structured (∞,1)-toposes)]] (if the notion of [[Grothendieck topology]] is relaxed to that of [[coverage]] in [StrSp](#StrSp)).


#### The spectrum construction

Every object $U \in \mathrm{CartSp}$ is canonically a [[CartSp]]-[[ringed space]], meaning a [[topological space]] equipped with a local sheaf of [[smooth algebra]]s. More generally: every object $U \in CartSp$ is canonically incarnated as the $CartSp$-[[structured (∞,1)-topos] 

$$
  (\mathcal{X}, \mathcal{O}_{\mathcal{X}})
  :=
  (Sh_{(\infty,1)}(CartSp)/U ,
    \;\;\; \mathcal{O}_U : CartSp \stackrel{j}{\to} Sh_{(\infty,1)}(CartSp) \stackrel{U^*}{\to} Sh_{(\infty,1)}(CartSp)/U)
$$ 

given by the [[over-(∞,1)-topos]] of the [[big topos|big]] [[(∞,1)-sheaf (∞,1)-topos]] over $CartSp$ and the [[structure sheaf]] given by the composite of the [[(∞,1)-Yoneda embedding]] and the [[inverse image]] of the [[etale geometric morphism]] induced by $U$.


### Smooth manifolds as locally representable sheaves

+-- {: .un_defn}
###### Definition

Say an object $X$ in the [[sheaf topos]] $Sh(CartSp)$ (see [[diffeological space]] ) is _locally representable_ if there exists a family of morphisms $\{U_i \to X\}_{i \in X}$ with $U_i \in CartSp \stackrel{j}{\hookrightarrow} Sh(CartSp)$ such that the canonical morphism our of the [[coproduct]]

$$
  \coprod_i U_i \to X
$$

is an [[effective epimorphism]] in $Sh(CartSp)$.

Let $LocRep(CartSp) \hookrigharrow Sh(CartSp)$ be the full [[subcategory]] on locally representable sheaves.

=--

+-- {: .un_prop}
###### Proposition

There is an [[equivalence of categories]]

$$
  Diff \simeq LocRep(CartSp)
$$


of the category [[Diff]] of [[paracompact space|paracompact]] smooth manifolds with that of locally representable sheaves on $CartSp$.

=--

+-- {: .proof}
###### Proof


Define a functor $Diff \to LocRep(CartSp)$ by sending each smooth manifold to the sheaf over $CartSp$ that it naturally represents. By the fact that $X$ is assumed to be paracompact it admits a [[good open cover]] $\{U_i \to X\}$. We claim that $\coprod_i U_i \to X$ is an [[effective epimorphism]], so that this functor indeed lands in $LocRep(CartSp)$.

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

By the same kind of argument, every locally representable sheaf is locally isomorphic to a $U_i \in CartSp$, hence is a space locally isomorphic to a [[Cartesian space]] with its [[smooth structure]].

This shows that our functor $Diff \to LocRep(CartSp)$ is an [[essentially surjective functor]]. That it is also a [[full and faithful functor]] follows with arguments as discussed at [[diffeological space]]. Hence it is an [[equivalence of categories]].




=--

### As locally ringed spaces


We may switch from regarding smooth manifolds as objects in the [[big topos]] $X \in Sh(CartSp)$ to regrading them as [[topos]]es themselves, by passing to the [[over-topos]] $Sh(CartSp)/X$. This remembers the extra (smooth) structure on the [[topological space]] $X$ by being canonically a [[locally ringed topos]] with the [[structure sheaf]] of [[smooth function]]s on $X$.

+-- {: .un_prop}
###### Proposition

A  smooth manifold is equivalently a (paracomopact) [[locally ringed space]] $(X,\mathcal{O}_X)$ which is locally isomorphic to the ringed space $(\mathbb{R}^n, C^\infty(-) )$.

(...)

=--

### As locally representable structured $(\infty,1)$-toposes

The above discussion of smooth manifolds as [[ringed space]]s, generalizes to the context of [[ringed topos]]es and generally to [[structured (∞,1)-toposes]].

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



## References

The general abstract framework of [[higher geometry]] mentioned above is discussed in 

* [[Jacob Lurie]], _[[Structured Spaces]]_
{#StrSp}

[[!redirects smooth manifolds]]
