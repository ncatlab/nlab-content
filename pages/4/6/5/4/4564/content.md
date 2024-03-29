
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Hyperconnected geometric morphisms
* table of contents
{: toc}

## Idea

A [[geometric morphism]] is _hyperconnected_ if it is (left) [[orthogonal factorization system|orthogonal]] to a [[localic geometric morphism]].

In particular, a _hyperconnected topos_ is a [[topos]] that is "as far from being a [[localic topos]] as possible". In view of the fact that a [[topos]] is a generalized [[space]], while a [[localic topos]] is an ordinary [[topological space]]/[[locale]], regarded as a topos, this means that hyperconnected toposes are the "purely-generalized generalized spaces".


## Definition

+-- {: .un_def}
###### Definition

A [[geometric morphism]] $f\colon E\to F$ between [[toposes]] is called **hyperconnected** if the [[inverse image]] [[functor]] $f^*\colon F\to E$

1. is a [[full and faithful functor]] 

1. its [[image]] is closed under [[subquotients]] in $E$.

=--

This appears ([Johnstone, p. 225](#Johnstone)).


## Examples

* If $g\colon C\to D$ is a [[functor]] between [[small categories]] which is both [[essentially surjective functor|essentially surjective]] and [[full functor|full]], then the induced geometric morphism $Set^C\to Set^D$ is hyperconnected.  In fact, instead of essentially surjective it suffices for $g$ to be [[Cauchy surjective functor|Cauchy surjective]], i.e. $D$ is the closure of $g(C)$ under retracts.

* In particular, the [[global sections]] geometric morphism $Set^C\to Set$ on the [[presheaf topos]] is hyperconnected  iff the [[category]] $C$ is strongly connected ([Johnstone, A4.6.9](#Johnstone)), i.e., [[inhabited]] and for any two [[objects]] $A,B$ there exist morphisms $f:A\to B$ and $g:B\to A$. 

  This includes for instance the case when $C=M$ is a [[monoid]], and the topos of [[simplicial set|simplicial sets]].

* A [[locally connected topos|locally connected]] and [[local topos]] is hyperconnected precisely if as a [[cohesive topos]] it satisfies _pieces have points_ or equivalently _discrete objects are concrete_. See [[cohesive topos]] for details.

## Properties

+-- {: .un_prop}
###### Observation


Any hyperconnected geometric morphism is [[connected geometric morphism|connected]], 

=--

So the name is not unreasonable.


+-- {: .num_prop #HyperconnLocalicFactorizationSystem}
###### Proposition

Hyperconnected geometric morphisms are the left class of a 2-categorical [[orthogonal factorization system]] on the 2-category of toposes; the right class is the class of [[localic geometric morphisms]].

([[(hyperconnected,localic) factorization system]]).  

=--

See ([Johnstone](#Johnstone)).

+-- {: .un_remark}
###### Remark

In particular, a [[geometric morphism]] can only be both hyperconnected and [[localic geometric morphism|localic]] if it is an [[equivalence of categories|equivalence]].  Therefore, if we view topoi as generalized [[topological spaces]] (or [[locales]]), the world of hyperconnected topoi and geometric morphisms lives entirely in the "generalized" part.

=--

This is further amplified by the following proposition. Recall that the inclusion $Sh(-) : Locale \simeq LocTopos \hookrightarrow$ [[Topos]] is [[reflective subcategory|reflective]]: it has a [[left adjoint]]: the [[localic reflection]]

$$
  (L \dashv Sh(-)) : Locale \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  Topos
  \,.
$$

+-- {: .un_prop}
###### Proposition

Hyperconnected toposes $\mathcal{E}$ are precisely those whose [[localic reflection]] is the point: $L\mathcal{E} \simeq Sh(*) \simeq Set$.

=--

+-- {: .proof}
###### Proof

Suppose $\Gamma : \mathcal{E} \to Set$ is hyperconnected. Let $X$ be a [[locale]] and $\mathcal{E} \to Sh(X)$ a [[geometric morphism]]. Notice that this sits in an essentially unique diagram 

$$
  \array{
    \mathcal{E} &\to& Sh(X)
    \\
    \downarrow && \downarrow
    \\
    Set &\stackrel{=}{\to}& Set
  }
$$

in [[Topos]], where the vertical morphisms are the essentially unique [[global section]] geometric morphisms (we notationally suppress [[2-morphism|2-isomorophisms]]).

By the [above proposition](#HyperconnLocalicFactorizationSystem) there is an essentially unique geometric morphism $p : Set \to Sh(X)$ fitting into this diagram

$$
  \array{
    \mathcal{E} &\to& Sh(X)
    \\
    \downarrow &\nearrow_{\mathrlap{p}}& \downarrow
    \\
    Set &\stackrel{=}{\to}& Set
  }
  \,.
$$

This establishes the [[natural equivalence]]

$$
  Topos(\mathcal{E}, Sh(X)) \simeq LocTopos(Set, Sh(X)) \simeq
  Locale(*, X)
$$

and hence identifies the point as the localic reflection of $\mathcal{E}$.

Conversely, suppose that $\mathcal{E}$ has as localic reflection the point. The [[unit of an adjunction|unit]] of the $(L \dashv Sh(-))$-[[adjunction]] -- the [[reflective subcategory|reflector]] -- $\mathcal{E} \to Set$ is by essential uniqueness the [[global section]] [[geometric morphism]].

Let then 

$$
  \array{
    \mathcal{E} &\to& \mathcal{S}
    \\
    \downarrow && \downarrow
    \\
    Set &\stackrel{f}{\to}& \mathcal{T}
  }
$$

be a lifting problem, with the right morphism a [[localic geometric morphism]]. Since these are preserved by [[pullback]] in [[Topos]], this is equivalently a diagram


$$
  \array{
    \mathcal{E} &\to& Sh(X) \simeq f^* \mathcal{S} &\to& \mathcal{S}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    Set &\stackrel{=}{\to}& Set &\stackrel{f}{\to}& \mathcal{T}
  }
  \,.
$$

Since this exhibits $f^* \mathcal{S}$ as a [[localic topos]] $Sh(X)$ for some [[locale]] $X$, we have by the <a href="http://nlab.mathforge.org/nlab/show/adjoint%20functor#UniversalArrows">universal property of the adjunction unit</a> an essentially unique lift $p$ in the left square

$$
  \array{
    \mathcal{E} &\to& Sh(X) \simeq f^* \mathcal{S} &\to& \mathcal{S}
    \\
    \downarrow &\nearrow_{\mathrlap{p}}& \downarrow && \downarrow
    \\
    Set = Sh(L(\mathcal{E})) &\stackrel{=}{\to}& Set &\stackrel{f}{\to}& \mathcal{T}
  }
  \,.
$$

By the universal property of the [[pullback]], this is then also an essentially unique solution to the original lifting problem.

=--

## References

* [[Peter Johnstone]], _Factorization theorems for geometric morphisms_ Cahiers, 22, no1 (1981) ([numdam](http://www.numdam.org/item?id=CTGDC_1981__22_1_3_0))
{#Johnstone}



[[!redirects hyperconnected geometric morphism]]
[[!redirects hyperconnected geometric morphisms]]

[[!redirects hyperconnected topos]]
[[!redirects hyperconnected toposes]]