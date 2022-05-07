
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of **final $(\infty,1)$-functor** (also called a **cofinal $(\infty,1)$-functor**) is the generalization of the notion of [[final functor]] from [[category theory]] to [[(∞,1)-category]]-theory.

An [[(∞,1)-functor]] $p : K' \to K$ is final precisely if precomposition with $p$ preserves [[(∞,1)-colimit]]: 

if $p$ is final then for $F : K \to C$ any [[(∞,1)-functor]] we have

$$
  \lim_\to (K \stackrel{F}{\to} C)
  \simeq
  \lim_{\to} ( K' \stackrel{p}{\to} K \stackrel{F}{\to} C)  
$$

when either of these [[(∞,1)-colimits]] exist.

## Definition


+-- {: .num_defn}
###### Definition 
**(final morphism of simplicial set)**

A morphism $p : S \to T$ of [[simplicial set]]s is **final** if for every [[fibrations of quasi-categories|right fibration]] $X \to T$ the induced morphism of simplicial sets

$$
  sSet_{/T}(T,X) \to sSet_{/T}(S,X)
$$

is a [[homotopy equivalence]].


=--

So in the [[overcategory]] $sSet/T$ a final morphism is an object such that morphisms out of it into any right fibration are the same as morphisms out of the [[terminal object]] into that right fibration.

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

+-- {: .num_prop}
###### Proposition 

The morphism $p : S \to T$ is final precisely if the terminal morphism $(p \to *) =   \left(
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

+-- {: .num_cor}
###### Corollary

If $T$ is a [[Kan complex]] then $p : S \to T$ is final precisely if it is a weak equivalence in the standard [[model structure on simplicial sets]]. 

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, cor. 4.1.2.6]].

=--



## Properties {#Properties}

+-- {: .num_prop}
###### Proposition 
**(preservation of undercategories and colimits)**

A morphism $p : K' \to K$ of [[simplicial set]]s is final precisely if for every [[quasicategory]] $C$

*  and for every morphism $\bar F : K^{\triangleright} \to C$ that exhibits a [[colimit in a quasi-category|colimit co-cone in]] $C$, also $(K')^\triangleright \stackrel{p}{\to} K^{\triangleright} \stackrel{\bar F}{\to} C$ is a colimit co-cone.

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

+-- {: .num_theorem #Recognition}
###### Theorem 
**(recognition theorem for final $(\infty,1)$-functors)**

A morphism $p : K \to C$ of [[simplicial sets]] with $C$ a [[quasi-category]] is final precisely if for each object $c \in C$ the [[comma category|comma]]-object $c/p \coloneqq c/C \times_C K$ is weakly [[contractible]]. 

=--

More explicitly, the comma object in question here is the [[pullback]]

$$
  \array{
    c/p &\to& c/C
    \\
    \downarrow && \downarrow
    \\
    K &\stackrel{p}{\to}& C
    \mathrlap{\,.}
  }
$$

where $c/C$ is the [[over quasi-category|under quasi-category]] under $c$.

+-- {: .proof}
###### Proof

This is due to [[Andre Joyal]]. A proof appears as [[Higher Topos Theory|HTT, prop. 4.1.3.1]].

=--

The following says that up to equivalence, the cofinal maps of simplicial sets are the right [[anodyne morphisms]]

+-- {: .num_prop}
###### Proposition

A map of simplicial sets is cofinal precisely if it factors as a right anodyne map followed by a trivial fibration.

=--

This is ([Lurie, cor. 4.1.1.12](#Lurie)).

## Examples

### General
 {#General}

+-- {: .num_example}
###### Example

The inclusion $\ast \to \mathcal{C}$ of a [[terminal object in an (∞,1)-category|terminal object]] is final.

=--

+-- {: .proof}
###### Proof

By theorem \ref{Recognition} the inclusion of the point is final precisely if for all $c \in \mathcal{C}$, the [[(∞,1)-categorical hom-space]] $\mathcal{C}(c,\ast)$ is contractible. This is the definition of $\ast$ being terminal.

=--

+-- {: .num_example}
###### Example

A (weak) localization $f: \mathcal{C} \to \mathcal{D}$ is both initial and final.

=--

This appears, for example, as ([Cisinski, 7.1.10](#Cisinski)).

### Cofiber products in co-slice categories
 {#CofiberProductsInCosliseCategories}

+-- {: .num_example }  
###### Example

Consider the inclusion of the [[walking structure|walking]] [[span]]-category, into the result of adjoining an [[initial object]] $t$:

\[
  \label{SpanCategoryAndInitialObjectAdjoined}
  \Big\{
  \array{
     x 
     &\longleftarrow&
     b
     &\longrightarrow&
     y
  }
  \Big\}
  \;\;
  \overset{\phantom{AAAA}}{\hookrightarrow}
  \;\;
  \left\{
  \array{
     && t
     \\
     & \swarrow & \downarrow & \searrow
     \\
     x 
     &\longleftarrow&
     b
     &\longrightarrow&
     y
  }
  \right\}
\]

One readily sees that for each object on the right, its comma category over this inclusion has contractible nerve, whence Theorem \ref{Recognition} implies that this inclusion is a final $\infty$-functor.

As an application of the finality of (eq:SpanCategoryAndInitialObjectAdjoined), observe that for $\mathcal{C}$ an [[(∞,1)-category]] and $T \in \mathcal{C}$ an object, [[(∞,1)-colimits]] in the [[under-(∞,1)-category]] 

$$
  \mathcal{C}^{T/}
  \overset{\;\;U\;\;}{\longrightarrow}
  \mathcal{C}
$$ 

are given by the $\infty$-colimit in $\mathcal{C}$ itself of the given [[cone]] of the original diagram, with tip $X$ (by [this Prop.](over+quasi-categories#LimitsInSliceAreLimitsInUnderlyingCategoryOverCoconeDiagram)): For

$$
  F \;\colon\; \mathcal{I} \longrightarrow \mathcal{C}^{T/}
$$

a small [[diagram]], we have 

$$
  U \big(
    \underset{\longrightarrow}{\lim}\, F
  \big)
  \;\simeq\;
  \underset{\longrightarrow}{\lim}\, \big( T/U(F) \big)
$$

(when either $\infty$-colimit exists).

Now for $\mathcal{I}$ the [[walking structure|walking]] [[span]] diagram on the left of (eq:SpanCategoryAndInitialObjectAdjoined), this means that [[homotopy cofiber products]] in $\mathcal{C}^{T/}$ are computed as $\infty$-colimits in $\mathcal{C}$ of diagrams of the shape on the right of (eq:SpanCategoryAndInitialObjectAdjoined). But since the inclusion in (eq:SpanCategoryAndInitialObjectAdjoined) is final, these are just homotopy cofiber products in $\mathcal{C}$.

Explicitly: Given 

$$
  \array{
     T &=& T &=& T
     \\
     {}^{\mathllap{
       \phi_X
     }}
     \big\downarrow
     &&
     {}^{\mathllap{
       \phi_B
     }}
     \big\downarrow
     &&
     {}^{\mathllap{
       \phi_Y
     }}
     \big\downarrow
     \\
     X 
     &
       \underset{
       f
       }{\longleftarrow}
     &
     B
     &
       \underset{
         g
       }{
         \longrightarrow
       }
     &
     Y
  }
$$

regarded as a [[span]] in $\mathcal{C}^T$, hence with underlying objects

$$
  U\big(  (X,\phi_X) \big) \;=\; X
  \,,
  \;\;\;\;\;\;
  U\big(  (B,\phi_B) \big) \;=\; B
  \,,
  \;\;\;\;\;\;
  U\big(  (Y,\phi_Y) \big) \;=\; Y
  \,,
$$

we have:

$$
  U
  \Big(
    \;
    (X,\phi_X)
    \underset{
      (B,\phi_B)
    }{\coprod}
    (Y,\phi_Y)
    \;
  \Big)
  \;\;\;\simeq\;\;\;
  X \underset{B}{\coprod} Y
  \,.
$$


In particular, if $(B,\phi_B) \;\coloneqq\; (T,id_T) $ is the [[initial object]] in $\mathcal{C}^{T/}$, in which case the cofiber product is just the coproduct

$$
  (X,\phi_X)
  \coprod
  (Y,\phi_Y)
  \;\;=\;\;
  (X,\phi_X)
  \underset{
    (T,id_T)
  }{\coprod}
  (Y,\phi_Y)
$$

we find that the coproduct in the co-slice category is the co-fiber product under the given tip object in the underlying category

$$
  U
  \Big(
    \;
    (X,\phi_X)
    \coprod
    (Y,\phi_Y)
    \;
  \Big)
  \;\;\;\simeq\;\;\;
  X \underset{T}{\coprod} Y
  \,.
$$



=--

### On categories of simplices
 {#OnCategoriesOfSimplices}

+-- {: .num_defn}
###### Definition

For $K \in $ [[sSet]] a [[simplicial set]], write $\Delta_{/K}$ for its [[category of elements]], called here the [[category of simplices]] of the simplicial set: 

an [[object]] of $\Delta_{/K}$ is a morphism of simplicial sets of the form $\Delta^n \to K$ for some $n \in \mathbb{N}$ (hence an $n$-[[simplex]] of $K$) and a morphism is a [[commuting diagram]]

$$
  \array{
    \Delta^{n_1}&&\to&& \Delta^{n_2}
    \\
    & \searrow && \swarrow
    \\
    && K
  }
  \,.
$$

Moreover, write

$$
  \Delta_{/K}^{nd} \hookrightarrow \Delta_{/K}
$$

for the non-full subcategory on the non-degenerate simplices.

=--

+-- {: .num_remark}
###### Remark

When the simplicial set $K$ is non-singular, i.e. every face of a non-degenerate simplex is still non-degenerate, then the category $\Delta_{/K}^{nd}$ is a [[poset]] and it coincides with the [[barycentric subdivision]] of $K$.

=--

+-- {: .num_prop}
###### Proposition

Suppose $K$ is a non-singular simplicial set. Then the inclusion 

$$
  N(\Delta_{/K}^{nd}) \hookrightarrow N(\Delta_{/K})
$$

is a cofinal morphism of [[quasi-categories]].


=--

This appears as ([Lurie, variant 4.2.3.15](#Lurie)).

+-- {: .num_prop}
###### Proposition

For every simplicial set $K$ there exists a cofinal map

$$
  N(\Delta_{/K}) \to K
  \,.
$$

=--

This is ([Lurie, prop. 4.2.3.14](#Lurie)).

+-- {: .num_remark}
###### Remark

If the simplicial set $K$ is singular, it is not in general true
that the inclusion $N(\Delta_{/K}^{nd}) \hookrightarrow N(\Delta_{/K})$
is final. For a counter-example, see ([Hovey, 9](#Hovey)). 

=--

+-- {: .num_prop}
###### Proposition

For every simplicial set $K$, evaluation at the initial vertex

$$
  N(\Delta_{/K})^{op} \to K
  \,.
$$

is both initial and final.

=--

This appears as ([Shah, 12.2](#Shah)) and also follows from the fact that this map is a weak localization ([Cisinski, 7.3.15](#Cisinski)).

+-- {: .num_remark}
###### Remark

This can be used to establish a Bousfield-Kan formula for homotopy colimits; see ([Shah, 12.3](#Shah)). 

=--




## Related concepts

* [[final functor]]

* [[homotopy final functor]]

* final $(\infty,1)$-functor

## References

 
* {#Lurie} [[Jacob Lurie]], Section 4.1 of: _[[Higher Topos Theory]]_
 
* [[Dan Dugger]], Section 6 ofL _A primer on homotopy colimits_ ([pdf](http://pages.uoregon.edu/ddugger/hocolim.pdf))

* {#Hovey} [[Mark Hovey]], Item 9 of: _Errata to Model Categories_ ([pdf](http://hopf.math.purdue.edu/Hovey/model-err.pdf))

* {#Shah} [[Jay Shah]], *Parametrized higher categories and higher algebra: Expose II- Indexed homotopy limits and colimits*

* {#Cisinski} [[Denis-Charles Cisinski]], *Higher Categories and Homotopical Algebra*


[[!redirects cofinal (infinity,1)-functor]]
[[!redirects cofinal (∞,1)-functor]]
[[!redirects cofinal (infinity,1)-functors]]
[[!redirects cofinal (∞,1)-functors]]
[[!redirects final (infinity,1)-functor]]
[[!redirects final (∞,1)-functor]]
[[!redirects final (infinity,1)-functors]]
[[!redirects final (∞,1)-functors]]
[[!redirects initial (infinity,1)-functor]]
[[!redirects initial (∞,1)-functor]]
[[!redirects initial (infinity,1)-functors]]
[[!redirects initial (∞,1)-functors]]
[[!redirects homotopy final functor]]
[[!redirects homotopy final functors]]
[[!redirects homotopically final functor]]
[[!redirects homotopically final functors]]
[[!redirects homotopy cofinal functor]]
[[!redirects homotopy cofinal functors]]
[[!redirects homotopically cofinal functor]]
[[!redirects homotopically cofinal functors]]
[[!redirects homotopy initial functor]]
[[!redirects homotopy initial functors]]
[[!redirects homotopically initial functor]]
[[!redirects homotopically initial functors]]
