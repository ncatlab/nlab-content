[[!redirects cofinal (∞,1)-functor]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **cofinal $(\infty,1)$-functor** is the generalization of the notion of [[cofinal functor]] from [[category theory]] to [[(∞,1)-category]]-theory.

An [[(∞,1)-functor]] $p : K' \to K$ is cofinal precisely if precomposition with $p$ preserves [[colimit]]s: 

if $p$ is cofinal then for for $F : K \to C$ any [[(∞,1)-functor]] we have

$$
  \lim_\to (K \stackrel{F}{\to} C)
  \simeq
  \lim_{\to} ( K' \stackrel{p}{\to} K \stackrel{F}{\to} C)  
$$

when either of these [[colimit]]s exist. 

## Definition


+-- {: .un_defn}
###### Definition 
**(cofinal morphism of simplicial set)**

A morphism $p : S \to T$ of [[simplicial set]]s is **cofinal** if for every [[fibrations of quasi-categories|right fibration]] $X \to T$ the induced morphism of simplicial sets

$$
  sSet_{/T}(T,X) \to sSet_{/T}(S,X)
$$

is a [[homotopy equivalence]].


=--

So in the [[overcategory]] $sSet/T$ a cofinal morphism is an object such that morphisms out of it into any right fibration are the same as morphisms out of the [[terminal object]] into that right fibration.

$$
  \left\{
    \array{
      T &&\to&& X
      \\
      & {}_{\mathllap{=}}\searrow && \swarrow_{}
      \\
      && T
    }
  \right\}
  \;\;
  \simeq
  \left\{
    \array{
      S &&\to&& X
      \\
      & {}_{\mathllap{p}}\searrow && \swarrow_{}
      \\
      && T
    }
  \right\}
  \,.
$$


This definition is originally due to [[Andre Joyal]]. It appears as [[Higher Topos Theory|HTT, def 4.1.1.1]].

This is equivalent to the following definition, in terms of the [[model structure for right fibrations]]:

+-- {: .un_prop}
###### Proposition 

The morphism $p : S \to T$ is cofinal precisely if the terminal morphism $(p \to *) =   \left(
    \array{
      S &&\to&& T
      \\
      & {}_{\mathllap{}}\searrow && \swarrow_{=}
      \\
      && T
    }
  \right)$ in the [[overcategory]] $sSet_T$ is a weak equivalence in the [[model structure for right fibrations]] on $sSet_T$.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 4.1.2.5]].

=--

+-- {: .un_cor}
###### Corollary

If $T$ is a [[Kan complex]] then $p : S \to T$ is cofinal precisely if it is a weak equivalence in the standard [[model structure on simplicial sets]]. 

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, cor. 4.1.2.6]].

=--



## Properties

+-- {: .un_prop}
###### Proposition 
**(preservation of undercategories and colimits)**

A morphism $p : K' \to K$ of [[simplicial set]]s is cofinal precisely if for every [[quasicategory]] $C$

*  and for every morphism $\bar F : K^{\triangleright} \to C$ that exibits a [[colimit in a quasi-category|colimit co-cone in]] $C$, also $(K')^\triangleright \stackrel{p}{\to} K^{\triangleright} \stackrel{\bar F}{\to} C$ is a colimit co-cone.

and equivalently precisely if

* ... and for every $F : K \to C$ the morphism

  $$
    F/C \to (F\circ p)/C
  $$

  of [[over quasi-category|under quasi-categories]] induced by composition with $p$ is an equivalence of [[(∞,1)-categories]].

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 4.1.1.8]].

=--

The following result is the $(\infty,1)$-categorical analog of what is known as **Quillen's Theorem A**.

+-- {: .un_theorem}
###### Theorem 
**(recognition theorem for cofinal $(\infty,1)$-functors)**

A morphism $p : K \to C$ of [[simplicial set]]s with $C$ a [[quasi-category]] is cofinal precisely if for each object $c \in C$ the [[comma category|comma]]-object $c/p := c/C \times_C K$ is weakly [[contractible]]. 

=--

More explicitly, the comma object in question here is the [[pullback]]

$$
  \array{
    c/p &\to& c/C
    \\
    \downarrow && \downarrow
    \\
    K &\stackrel{p}{\to}& C
  }
  \,,
$$

where $c/C$ is the [[over quasi-category|under quasi-category]] under $c$.

+-- {: .proof}
###### Proof

This is due to [[Andre Joyal]]. A proof appears as [[Higher Topos Theory|HTT, prop. 4.1.3.1]].

=--


## References

Section 4.1 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_