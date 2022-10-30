+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **presheaf** on a [[category]] $C$ is a [[functor]]

$$
 F : C^{op} \to Set
$$

from the [[opposite category]] $C^{op}$ of $C$ to the category [[Set]] of [[set]]s. Equivalently this may be thought of as a [[contravariant functor]] $F : C \to Set$.

More generally, given any category $S$, an **$S$-valued presheaf** on $C$ is a functor 

$$
  C^{op} \to S.
$$

Historically, the initial applications of presheaves and sheaves involved cases like $S = CRing$ (the category of [[commutative ring|commutative rings]]), $S = $[[Ab]], $S = R$-$Mod$, etc. Later, especially with the development of topos theory, the primary importance of the [[sheaf topos|category of set-valued (pre)sheaves]] as topos was recognized; these other cases could be considered algebraic objects which live in the topos. This article and the one on [[sheaf topos]] recognize these later developments by making the set-valued case the default (in other words, presheaf or sheaf without further qualification is understood to refer to the set-valued case). 

The **[[category of presheaves]]** on $C$, usually denoted $Set^{C^{op}}$ or $[C^{op},Set]$, but often abbreviated as $\widehat{C}$, has:

* functors $F : C^{op} \to Set$ as objects;

* [[natural transformation|natural transformations]] between such functors as morphisms.

As such, it is an example of a [[functor category]].

## Remarks

* Speaking of functors as presheaves indicates operations that one wants to do apply to these functors, or certain properties that one wants to check.

  * when $S = Set$, and especially one is interested in the [[Yoneda embedding]] of a category $C$ into its presheaf category $[C^{op}, Set]$ for purposes of studying, for instance, [[limit]]s, [[colimit]]s, [[ind-object]]s, and [[pro-object]]s of $C$;

  * or when there is the structure of a [[site]] on $C$, such that it makes sense to ask if a given presheaf is actually a [[sheaf]].

* One generally useful way to think of presheaves is in the sense of [[space and quantity]].

* In the case where $S = Set$ and $C$ is [[small category|small]], an important general principle is that the presheaf category $[C^{op},Set]$ is the [[free cocompletion]] of $C$.  Intuitively, it is formed by taking $C$ and 'freely throwing in small colimits'.  The category $C$ is contained in $[C^{op},Set]$ via the [[Yoneda embedding]]
$$ Y : C \to [C^{op},Set]$$
The Yoneda embedding sends each object $c \in C$ to the presheaf
$$ F(-) = hom(-, c) $$
Presheaves of this form, or isomorphic to those of this form, are called [[representable functors|representable]]; among their properties, representable presheaves always turn colimits into limits, in the sense that a representable functor from $C^{op}$ to $Set$ turns colimits in $C$ (i.e., limits in $C^{op}$) into limits in $Set$ (i.e., colimits in $Set^{op}$). In general, such continuity is a necessary but not sufficient criterion for representability; however, nicely enough, it _is_ sufficient when $C$ itself is a presheaf category. To see this, suppose $K$ is such a presheaf on $C = [D^{op}, Set]$, and let $G = K Y$, a presheaf on $D$. By the [[Yoneda lemma]], we have a natural isomorphism between $[D^{op}, Set](Y(-), G)$ and $K Y(-)$. But by the free cocompletion property of the Yoneda embedding, a colimit-preserving functor on presheaves is entirely determined by its precomposition with $Y$; accordingly, our isomorphism must extend to an identification of $[C^{op}, Set](-, G)$ with $K(-)$, thus establishing the representability of $K$.

## Properties

### Limits and colimits

Any [[category of presheaves]] is [[complete category|complete]] and [[cocomplete category|cocomplete]], with both [[limit|limits]] and [[colimit|colimits]] being computed _pointwise_.  That is, to compute the limit or colimit of a diagram $F : D \to Set^{C^op}$, we think of it as a functor $F: D \times C^{op} \to Set$ and take the limit or colimit in the $D$ variable.

+-- {: .un_prop}
###### Proposition

Every presheaf is a [[colimit]] of [[representable functor|representable presheaves]].

=--

An elegant way to express this colimit for a presheaf $F : C^{op} \to Set$ is in terms of the [[coend]] identity

$$
  F(-) = \int^{c \in C} F(c) \times hom_C(-,c)
  \,,
$$

which follows by [[Yoneda reduction]]. See also [[co-Yoneda lemma]].

More concretely: let $Y : C \to [C^{op}, Set]$ denote the [[Yoneda embedding]] and let $C_F := Y/F$ be the corresponding [[comma category]], the [[category of elements]] of $F$:

$$
  C_F := 
  \left\lbrace
     \array{
        Y(V) &&\stackrel{Y(g)}{\to}&& Y(V')
        \\
        & {}_f\searrow && \swarrow_{f'}
        \\
        && F
     }
  \right\rbrace 
$$

and let $p : C_F \to C$ the canonical forgetful functor. Then the colimit over representables expression $F$ is

$$
   F \simeq colim_{(Y(V) \to F) \in C_F} (Y\circ p)
  \,.
$$

This is often written with some convenient abuse of notation as

$$
  F \simeq colim_{V \to F} V
  \,.
$$

Notice that these formulas can also be understood as those for the left [[Kan extension]] (see there) of $F$ along the identity functor.

+-- {: .proof}
###### Proof

Notice that for every $B \in [C^{op}, Set]$
and using the property of the [[hom-functor]] we have

$$
 \begin{aligned}
  Hom_{[C^{op}, Set]}(colim_{(Y(V) \to F) \in C_F} (Y\circ p),B)
  &\simeq
  lim_{(Y(V) \to F) \in C_F} Hom_{[C^{op}, Set]}(Y(V),B)
  \\
  & \simeq
  lim_{(Y(V) \to F) \in C_F} B(V)
 \end{aligned}
$$
by the [[Yoneda lemma]]. 

By the definition of [[limit]] we have that 

$$\cdots=Hom_{[C_F^{op}, Set]}(pt,B),$$

so for each natural transformation $\alpha \in Hom_{[C_F^{op}, Set]}(pt,B)$ and each object $h: Y(V)\to F\in C_F$, $\alpha_h$ is a map $\{*\}\to B(V)$, that is, it is an element of $B(V)$. However, by Yoneda, we know that each object $h:Y(V)\to F\in C_F$ specifies a unique element $h\in F(V)$. Then rephrasing this, $\alpha$ specifies a [[function]] $F(V)\to B(V)$.  The naturality of this assignment is guaranteed by the naturality of the map $\alpha$.  Then $\alpha$ induces a natural transformation $k^\alpha:F\to B$. It's easy to check that $k$ defines an isomorphism:

$$
  Hom_{[C_F^{op}, Set]}(pt,B) \simeq Hom_{[C^{op}, Set]}(F,B)
  \,.
$$
Since this holds for all $B$, the claim follows, again using the [[Yoneda lemma|Yoneda lemma]].

=--


## Special cases

* [[representable functor|represenatble presheaf]]

* [[concrete presheaf]]

## Examples

Examples for presheaves are abundant. Here is a non-representative selection of some examples.

* For $C$ a [[locally small]] category, every object $c \in C$ gives rise to the [[representable functor|representable presheaf]] $Hom_C(-, c) : C^{op} \to Set$.

* More generally, for $i : C \hookrightarrow D$ a [[subcategory]] of a locally small category $D$, every object $d \in D$ gives rise to the presheaf

  $$
    Hom_D(i(-), D) : C^{op} \to Set
    \,.
  $$

  Let's spell this out in more detail: given a mophism $\phi : V \to U$ 
  in $C$, we can take any morphism $f : i(U) \to X$ in $Hom_{D}(U,X)$ 
  and turn it into a morphism $V \stackrel{f}{\to} U \stackrel{\phi}{\to} X$ 
  in $Hom_{D}(i(V),X)$. This determines a map of set

  $$
    f^* : Hom_{D}(i(U),X) \to Hom_{D}(i(V),X)
    \,.
  $$

  So we have a functorial assignment of the form

  $$
     \array{
        W && \mapsto && Hom_{Diff}(i(W),X)
         \\
        \downarrow^g &&&& \uparrow^{g^*}
        \\
         V && \mapsto && Hom_{Diff}(i(V),X)
         \\
        \downarrow^f &&&& \uparrow^{f^*}
        \\
        U && \mapsto && Hom_{Diff}(i(U),X)
     }
     \,.
  $$


  Of course $i$ here could be any functor whatsoever. 
  Asking if such a presheaf
  is [[representable functor|representable]] is asking 
  for a right [[adjoint functor]] of $i$.

* A [[simplicial set]] is a presheaf on the [[simplex category]]

  A [[globular set]] is a presheaf on the [[globe category]].

  A [[cubical set]] is a presheaf on the [[cube category]].

* A [[diffeological space]] is a [[concrete presheaf]] on [[CartSp]].

* An important class of presheaves is those on a 
  [[category of open subsets]] $Op(X)$ of a [[topological space]] 
  or [[smooth manifold]] $X$.
  
  Traditional standard examples include: the presheaf of [[smooth function]]s
  on $X$, that assigns to each $U \subset X$ the set 
  $C^\infty(C,\mathbb{R})$ of smooth functions and to each unclusion 
  $V \subset U$ the corresponding restriction operation of functions.


... etc. pp.


## Related concepts

* **presheaf**

* [[(2,1)-presheaf]]

* [[(∞,1)-presheaf]]
 
* [[(∞,n)-presheaf]]

[[!redirects presheaves]]
[[!redirects presheaf category]]
[[!redirects presheaf categories]]