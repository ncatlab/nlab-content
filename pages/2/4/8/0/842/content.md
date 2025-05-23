

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
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

The notion of [[limit]] and [[colimit]] generalize from [[category theory]] to [[(∞,1)-category theory]]. One model for [[(∞,1)-categories]] are [[quasi-categories]]. This entry discusses limits and colimits in quasi-categories.


## Definition

+-- {: .num_defn}
###### Definition

For $K$ and $C$ two [[quasi-category|quasi-categories]] and $F : K \to 
C$ an [[(∞,1)-functor]] (a morphism of the underlying [[simplicial set]]s) , the **limit** over $F$ is, if it exists, the [[terminal object in a quasi-category|quasi-categorical terminal object]] in the [[over quasi-category]] $C_{/F}$:

$$
  \underset{\leftarrow}{\lim} F \coloneqq TerminalObj(C_{/F})
$$

(well defined up to a contractible space of choices).

A **colimit** in a quasi-category is accordingly a limit in the [[opposite quasi-category]].

=--

+-- {: .num_remark}
###### Remark

Notice from the discussion at [[join of quasi-categories]] that there are two definitions -- denoted $\star$ and $\diamondsuit$ -- of join, which yield results that differ as simplicial sets, though are equivalent as quasi-categories.

The notation $C_{/F}$ denotes the definition of [[over quasi-category]] induced from $\star$, while the notation $C^{/F}$ denotes that induced from $\diamondsuit$. Either can be used for the computation of limits in a quasi-category, as for quasi-categorical purposes they are weakly equivalent.

So we also have

$$
  \underset{\leftarrow}{\lim} F \coloneqq TerminalObj(C^{/F})
  \,.
$$

See [[Higher Topos Theory|HTT, prop 4.2.1.5]].

=--





## Properties 

### In terms of slice $\infty$-categories
 {#InTermsOfSlices}

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a [[quasi-category]] and let 
$f \colon K \to \mathcal{C}$ be a [[diagram]] with $(\infty,1)$-colimiting [[cocone]] $\tilde f \colon K \star \Delta^0 \to \mathcal{C}$. Then the induced map of [[slice (∞,1)-categories|slice quasi-categories]]

$$
  \mathcal{C}_{/\tilde f} \to \mathcal{C}_{f}
$$

is an [[acyclic Kan fibration]].

=--

+-- {: .num_prop #SlicingOverLimitingCone}
###### Proposition

For $F \colon \mathcal{K} \to \mathcal{C}$ a diagram in an $(\infty,1)$-category and $\underset{\leftarrow}{\lim} F$ its limit, there is a natural [[equivalence of (∞,1)-categories]] 

$$
  \mathcal{C}_{/F} \simeq \mathcal{C}_{/\underset{\leftarrow}{\lim} F}
$$

between the [[slice (∞,1)-categories]] over $F$ (the $(\infty,1)$-category of $\infty$-[[cones]] over $F$) and over just $\underset{\leftarrow}{\lim}F$.

=--

+-- {: .proof}
###### Proof

Let $\tilde F \colon \Delta^0 \star \mathcal{K} \to \mathcal{C}$
be the limiting cone. The canonical cospan of $\infty$-functors
$$
  \ast \to \Delta^0 \star \mathcal{K} \leftarrow \mathcal{K}
$$

induces a span of slice $\infty$-categories

$$
  \mathcal{C}_{/\underset{\leftarrow}{\lim}F}
  \leftarrow
  \mathcal{C}_{/\tilde F}
  \rightarrow
  \mathcal{C}_{/F}
  \,.
$$

The right functor is an equivalence by prop. \ref{SlicingOverLimitingCone}. The left functor is induced by restriction along an op-[[final (∞,1)-functor]] (by the Examples discussed there) and hence is an equivalence by the discussion at _[[slice (∞,1)-category]]_ ([Lurie, prop. 4.1.1.8](#Lurie)).

=--


This appears for instance in ([Lurie, proof of prop. 1.2.13.8](#Lurie)).

### In terms of $\infty$-Hom adjunction


The definition of the limit in a quasi-category in terms of terminal objects in the corresponding [[over quasi-category]] is well adapted to the particular nature the incarnation of $(\infty,1)$-categories by quasi-categories. But more intrinsically in $(\infty,1)$-category theory, it should be true that there is an [[adjunction]] characterization of 
$(\infty,1)$-limits : limit and colimit, should be (pointwise or global) [[right adjoint|right]] and [[left adjoint|left]]
[[adjoint (infinity,1)-functor]] of the constant diagram $(\infinity,1)$-functor,
$const : C \to Func(K,C)$.

$$
  (colim \dashv const \dashv lim)
  :
  Func(K,C)
  \stackrel{\overset{lim}{\to}}{\stackrel{\overset{const}{\leftarrow}}
  {\underset{colim}{\to}}}
  Func(*,C) \simeq C
  \,.
$$

By the discussion at [[adjoint (∞,1)-functor]] ([[Higher Topos Theory|HTT, prop. 5.2.2.8]]) this requires exhibiitng a morphism $\eta : Id_{Func(K,C)} \to const colim$ in $Func(Func(K,C),Func(K,C))$ such that for every $f \in Func(K,C)$ and $Y \in C$ 
the induced morphism

$$
  Hom_{C}(colim(f),Y) \to Hom_{Func(K,C)}(const colim(f), const Y)
  \stackrel{Hom(\eta, const Y)}{\to}
  Hom_{Func(K,Y)}(f, const Y)
$$

is a weak equivalence in $sSet_{Quillen}$.


But first consider the following pointwise characterization.


+-- {: .num_prop}
###### Proposition

Let $C$ be a [[quasi-category]], $K$ a [[simplicial set]]. A [[co-cone]] [[diagram]]
$\bar p : K \star \Delta[0] \to C$ with cone point $X \in C$ 
is a [[colimit|colimiting]] [[diagram]] (an initial object in
$C_{p/}$) precisely if for every object $Y \in C$ the morphism

$$
  \phi_Y : Hom_C(X,Y) \to Hom_{Func(K,C)}(p, const Y)
$$

induced by the morpism $ p \to const X$ that is encoded by $\bar p$ is an 
equivalence (i.e. a [[homotopy equivalence]] of [[Kan complex]]es).

=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma 4.2.4.3]].

The key step is to realize that $Hom_{Func(K,C)}(p, const Y)$ is given (up to equivalence) by
the [[pullback]] $C^{p/} \times_C \{Y\}$ in [[sSet]].

Here is a detailed way to see this, 
using the discussion at [[hom-object in a quasi-category]]. 

We have that $Hom_{Func(K,C)}(p, const Y)$ is given by 
$(C^K)^{p/} \times_{C^K} const Y$. We compute

$$
  \begin{aligned}
    ((C^K)^{p/} \times_{C^K} const Y)_n
    & =
    Hom_{{\Delta[0]}/sSet}( \Delta[0] \diamondsuit \Delta[n] , C^K ) \times_{(C^K)_n} \{const Y\}
    \\
    & =
    Hom_{{\Delta[0]}/sSet}( \Delta[0] \coprod_{\Delta[n]} \Delta[n] \times \Delta[1] , C^K )
    \times_{(C^K)_n} \{const Y\}
    \\
    & =
    \{p\}
      \times_{Hom(\Delta[0],C^K)}
    Hom(\Delta[0], C^K)
      \times_{Hom(\Delta[n], C^K)}
    Hom(\Delta[n] \times \Delta[1], C^K)
      \times_{Hom(\Delta[n], C^K)}
    \{const Y\}
    \\
    & =
    \{p\}
      \times_{Hom(K,C)}
    Hom(K,C)
      \times_{Hom(\Delta[n]\times K,C)}
    Hom(\Delta[n]\times K \times \Delta[1], C)
      \times_{Hom(\Delta[n]\times K, C)}
    Hom(\Delta[n],C)
      \times_{\Delta[n],C}
    \{Y\}
    \\
    &=
    \{p\} 
      \times_{Hom(K,C)}
    Hom(K \diamondsuit \Delta[n], C)
      \times_{Hom(\Delta[n],C)}
    \{Y\}
    \\
    &=
    (C^{p/}\times_C \{Y\})_n
  \end{aligned}
$$

Under this identification, $\phi_Y$ is the morphism

$$
  \left(
  C^{X/} 
   \stackrel{\phi'}{\to}
  C^{\bar p/}
    \stackrel{\phi''}{\to}
  C^{p/}
  \right)
  \times_C \{Y\}
  \,,
$$

in [[sSet]] where $\phi'$ is a section of the map $C^{\bar p/} \to C^{X/}$,
(which one checks is an acyclic [[Kan fibration]]) obtained by choosing composites
of the co-cone components with a given morphism $X \to Y$. 

The morphism $\phi''$ is a [[left fibration]] (using [[Higher Topos Theory|HTT, prop. 4.2.1.6]])

One finds that the morphism $\phi''$ is a [[left fibration]].

The strategy for the completion of the proof is: realize that the first condition
of the proposition is equivalent to $\phi''$ being an acyclic Kan fibration, and the
second statement equivalent to $\phi''_Y$ being an acyclic Kan fibration, then 
show that these two conditions in turn are equivalent.

=--


### In terms of products and equalizers

A central theorem in ordinary [[category theory]] asserts that a [[category]] has [[limit]]s already if it has [[product]]s and [[equalizer]]s. The analog statement is true here:

+-- {: .num_prop}
###### Proposition

Let $\kappa$ be a [[regular cardinal]]. An [[(∞,1)-category]] $C$ has all $\kappa$-small limits precisely if it has [[equalizer]]s and $\kappa$-small [[product]]s.

=--

This is [[Higher Topos Theory|HTT, prop. 4.4.3.2]].


### In terms of homotopy limits {#TermsOfHomotopy}

The notion of [[homotopy limit]], which exists for [[model categories]] and in particular for [[simplicial model categories]] and in fact in all plain [[Kan complex]]-[[enriched categories]] -- as described in more detail at [[homotopy Kan extension]] -- is supposed to be a model for $(\infty,1)$-categorical limits. In particular, under sending the Kan-complex enriched categories $C$ to quasi-categories $N(C)$ using the [[homotopy coherent nerve]] functor, homotopy limits should precisely corespond to quasi-categorical limits. That this is indeed the case is asserted by the following statements.


+-- {: .num_prop}
###### Proposition

Let $C$ and $J$ be [[Kan complex]]-[[enriched categories]] and let $F : J \to C$ be an [[sSet]]-[[enriched functor]]. 

Then a [[cocone]] $\{\eta_i : F(i) \to c\}_{i \in J}$ under $F$ exhibits the object $c \in C$ as a [[homotopy colimit]] (in the sense discussed in detail at [[homotopy Kan extension]]) precisely if the induced morphism of quasi-categories

$$
  \bar {N(F)} : N(J)^{\triangleright} \to N(C) 
$$

is a quasi-categorical colimit [[diagram]] in $N(C)$. 

=--

Here $N$ is the [[homotopy coherent nerve]], $N(J)^{\triangleright}$ the [[join of quasi-categories]] with the point, $N(F)$ the image of the simplicial functor $F$ under the homotopy coherent nerve and $\bar{N(F)}$ its extension to the join determined by the cocone maps $\eta$.

+-- {: .proof}
###### Proof


This is [[Higher Topos Theory|HTT, theorem 4.2.4.1]]

A central ingredient in the proof is the fact, discused at [[(∞,1)-category of (∞,1)-functors]] and at [[model structure on functors]], that [[sSet]]-[[enriched functor]]s do model [[(∞,1)-functor]]s, in that for $A$ a [[combinatorial simplicial model category]], $S$ a [[quasi-category]] and $\tau(S)$ the corresponding $sSet$-category under the left adjoint of the [[homotopy coherent nerve]], we have an [[equivalence of quasi-categories]]

$$
  N(([C,A]_{proj})^\circ)
  \simeq
  Func(S, N(A^\circ))
$$

and the same is trued for $A$ itself replaced by a [[chunk of a model category|chunk]] $U \subset A$.

With this and the discussion at [[homotopy Kan extension]], we find that the cocone components $\eta$ induce for each $a \in [C,sSet]$ a [[homotopy equivalence]]

$$
  C(c,a) \stackrel{}{\to}
  [J^{op}, C](j F, const a)
$$

which is hence equivalently an equivalence of the corresponding [[hom-object in a quasi-category|quasi-categorical hom-objects]]. The claim follows then from the above discussion of characterization of (co)limits in terms of $\infty$-hom adjunctions.



=--



+-- {: .num_cor}
###### Corollary

The quasi-category $N(A^\circ)$ [[presentable (∞,1)-category|presented]] by a [[combinatorial simplicial model category]] $A$ has all small quasi-categorical limits and colimits.

=--


+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, 4.2.4.8]]. 

It follows from the fact that $A$ has 
(pretty much by definition of [[model category]] and [[combinatorial model category]]) 
all [[homotopy limit]]s and [[homotopy colimit]]s (in fact all [[homotopy Kan extension]]s)
by the above proposition.

=--

Since $(\infty,1)$-categories equivalent to those of the form $N(A^\circ)$ for $A$ a [[combinatorial simplicial model category]] are precisely the [[locally presentable (∞,1)-categories]], it follows from this in particular that every locally presentable $(\infty,1)$-category has all limits and colimits.


### Commutativity of limits {#CommutativityOfLimits}

The following proposition says that if for an $(\infty,1)$-functor $F : X \times Y \to C$ limits (colimits) over each of the two variables exist separately, then they commute.

+-- {: .num_prop }
###### Proposition

Let $X$ and $Y$ be [[simplicial set]]s and $C$ a [[quasi-category]]. Let $p : X^{\triangleleft} \times Y^{\triangleleft} \to C$ be a [[diagram]]. If

1. for every object $x \in X^{\triangleleft}$ (including the cone point) the restricted diagram $p_x : Y^{\triangleleft} \to C$ is a limit diagram;

1. for every object $y \in Y$ (not including the cone point) the restricted diagram $p_y : X^{\triangleleft} \to C$ is a limit diagram;

then, with $c$ denoting the cone point of $Y^{\triangleleft}$, the restricted diagram, $p_c : X^{\triangleleft} \to C$ is also a limit diagram.

=-- 

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, lemma 5.5.2.3]]

=--


In other words, suppose that $\lim_x F(x,y)$ exists for all $y$ and $\lim_y F(x,y)$ exists for all $x$ and also that $\lim_y (\lim_x F(x,y))$ exists, then this object is also $\lim_x \lim_y F(x,y)$.


## Examples

### $\infty$-Limits of special shape

#### Coproduct

See also at [[(infinity,1)-coproduct]].

(...)

#### Pullback / Pushout

See also [[(∞,1)-pullback]].

The non-degenerate cells of the [[simplicial set]] $\Delta[1] \times \Delta[1]$ obtained as the [[cartesian product]] of the simplicial 1-[[simplex]] with itself look like

$$
  \array{
    (0,0) &\to& (1,0)
    \\
    \downarrow &\searrow& \downarrow
    \\
    (0,1) &\to& (1,1)
  }
$$

A **sqare** in a [[quasi-category]] $C$ is an image of this in $C$, i.e. a morphism

$$
  s : \Delta[1] \times \Delta[1] \to C
  \,.
$$

The simplicial square $\Delta[1]^{\times 2}$ is [[isomorphism|isomorphic]], as a [[simplicial set]], to the [[join of simplicial sets]] of a 2-[[horn]] with the point:

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \{v\} \star \Lambda[2]_2
  = 
  \left(
  \array{
    v &\to& 1
    \\
    \downarrow &\searrow& \downarrow
    \\
    0 &\to& 2
  }
  \right)
$$

and

$$
  \Delta[1] \times \Delta[1]
  \simeq
  \Lambda[2]_0 \star \{v\}
  = 
  \left(
  \array{
    0&\to& 1
    \\
    \downarrow &\searrow& \downarrow
    \\
    2 &\to& v
  }
  \right)
  \,.
$$

If a square $\Delta[1] \times \Delta[1] \simeq \Lambda[2]_0 \star \{v\} \to C$ exhibits $\{v\} \to C$ as a colimit over $F : \Lambda[2]_0 \to C$, we say the colimit

$$
  v := \lim_\to F := F(1) \coprod_{F(0)} F(2)
$$

is [[generalized the|the]] **pushout** of the diagram $F$.

##### Pasting law of pushouts {#PushoutPasting}

We have the following $(\infty,1)$-categorical analog of the familiar [pasting law of pushouts](http://ncatlab.org/nlab/show/pullback#Pasting) in ordinary [[category theory]]:

+-- {: .num_prop}
###### Proposition

A pasting diagram of two squares is a morphism

$$
  \Delta[2] \times \Delta[1] \to C
  \,.
$$

Schematically this looks like

$$
  \array{
     x &\to& y &\to& z
     \\
     \downarrow && \downarrow && \downarrow
     \\
     x' &\to& y' &\to& z'
  }
  \,.
$$

If the left square is a pushout diagram in $C$, then the right square is precisely if the outer square is.

=--

+-- {: .proof}
###### Proof

A proof appears as [[Higher Topos Theory|HTT, lemma 4.4.2.1]]

=--


#### Coequalizer

See also at [[(infinity,1)-coequalizer]].

(...)

#### Quotients

* [[infinity-quotient]]

#### Tensoring and cotensoring with an  $\infty$-groupoid {#Tensoring}

##### Recap of the 1-categorical situation

An ordinary [[category]] with [[limit]]s is canonically [[power|cotensored]] over [[Set]]:


For $S, T \in $ [[Set]] and $const_T : S \to Set$ the [[diagram]] parameterized by $S$ that is constant on $T$, we have

$$
  \lim_{\leftarrow} \, const_T \simeq T^S
  \,.
$$

Accordingly the cotensoring

$$
  (-)^{(-)} : Set^{op} \times C \to C
$$

is defined by

$$
  c^S := \lim_{\leftarrow} (S \stackrel{const_c}{\to} C)
  = \prod_{S} c
  \,.
$$

And by continuity of the [[hom-functor]] this implies the required natural isomorphisms

$$
  Hom_C(d,c^S) = Hom_C(d, {\lim_{\leftarrow}}_S c) \simeq {\lim_{\leftarrow}}_S 
  Hom_C(d,c) \simeq Set(S,Hom_C(d,C))
  \,.
$$

Correspondingly if $C$ has [[colimit]]s, then the [[copower|tensoring]]

$$
  (-) \otimes (-) : Set \times C \to C
$$

is given by forming [[colimit]]s over constant diagrams: $S \otimes c := {\lim_{\to}}_S c$, and again by continuity of the [[hom-functor]] we have the required natural isomorphism

$$
  Hom_C(S \otimes c, d) = 
  Hom_C({\lim_{\to}}_S c,d)
  \simeq
  {\lim_{\leftarrow}}_S Hom_C(c,d)

  \simeq
  Set(S,Hom_C(c,d))
  \,.
$$

Of course all the colimits appearing here are just [[coproduct]]s and all limits just [[product]]s, but for the generalization to $(\infty,1)$-categories this is a misleading simplification, it is really the notion of limit and colimit that matters here.

##### Definition

We expect for $S, T \in $ [[∞Grpd]] and for $const_T : S \to \infty Grpd$ the constant diagram, that 

$$
  \lim_{\leftarrow} \, const_T \simeq T^S
  \,,
$$ 

where on the right we have the [[internal hom]] of $\infty$-groupoids, which is modeled in the [[model structure on simplicial sets]] $sSet_{Quillen}$ by the fact that this is a [[closed monoidal category|closed]] [[monoidal category]].

Correspondingly, for $C$ an $(\infty,1)$-category with colimits, it is [[copower|tensored]] over [[∞Grpd]] by setting

$$
  (-)\otimes (-) : \infty Grpd \times C \to C
$$

$$
  S \otimes c := {\lim_{\to}}_S c
  \,,
$$

where now on the right we have the $(\infty,1)$-categorical colimit over the constant diagram $const : S \to C$ of shape $S$ on $c$.

Then by the $(\infty,1)$-continuity of the hom, and using the above characterization of the [[internal hom]] in $\infty Grpd$ we have the required natural equivalence

$$
  Hom_C(S \otimes c, d)
  =
  Hom_C({\lim_{\to}}_S c, d)
  \simeq
  {\lim_{\leftarrow}}_S Hom_C(c,d)
  \simeq
  \infty Grpd(S,Hom_C(c,d))
  \,.
$$ 

The following proposition should assert that this is all true

+-- {: .num_prop #TensoringProposition}
###### Proposition

The $(\infty,1)$-categorical colimit ${\lim_{\to}} c$ over the diagram of shape $S \in \infty Grpd$ constant on $c \in C$ is characterized by the fact that it induces natural equivalences

$$
  Hom_C({\lim_{\to}}_S c, d)
  \simeq
  \infty Grpd(S, Hom_C(c,d))
$$

for all $d \in C$.

=--

This is essentially [[Higher Topos Theory|HTT, corollary 4.4.4.9]].

+-- {: .num_cor #EveryInfinityGroupoidIsHomotopyColimitOfConstantFunctorOverItself}
###### Corollary

Every [[∞-groupoid]] $S$ is the $(\infty,1)$-colimit in [[∞Grpd]] of the constant diagram on the [[point]] over itself:

$$
  S \simeq {\lim_{\to}}_S const_*
  \,.
$$

=--


This justifies the following definition

+-- {: .num_defn}
###### Definition

For $C$ an $(\infty,1)$-category with colimits, the **tensoring of $C$ over $\infty Grpd$** is the $(\infty,1)$-functor

$$
  (-) \otimes (-) : \infty Grpd \times C \to C
$$

given by

$$
  S \otimes c = \lim_{\to} (const_c : S \to C) 
  \,.
$$

=--

See [[Higher Topos Theory|HTT, section 4.4.4]].

##### Models {#ModelsForTensoring}

We discuss models for $(\infty,1)$-(co)limits in terms of ordinary [[category theory]] and [[homotopy theory]].


\begin{lemma}
If $C$ is [[presentable (infinity,1)-category|presented]] by a [[simplicial model category]] $A$, in that $C \simeq A^\circ$, then the 
$(\infty,1)$-tensoring and $(\infty,1)$-cotensoring of $C$ over [[∞Grpd]]
is modeled by the ordinary [[copower|tensoring]] and [[power|powering]]
of $A$ over [[sSet]]:

For $\hat c \in A$ cofibant and representing an object $c \in C$ and for $S \in sSet$ any simplicial set, we have an equivalence

$$
  c \otimes S \simeq \hat C \cdot S
  \,.
$$

\end{lemma}

+-- {: .proof}
###### Proof


The powering in $A$ satisfies the [[natural isomorphism]]

$$
  sSet(S,A(\hat c,\hat d)) \simeq A(\hat c \cdot S, \hat d)
$$

in [[sSet]].

For $\hat c$ a cofibrant and $\hat d$ a fibrant representative, we have that both sides here are [[Kan complex]]es that are equivalent to the corresponding [[derived hom space]]s in the corresponding $(\infty,1)$-category $C$, so that this translates into an equivalence

$$
  Hom_C(c \cdot S, d)
  \simeq
  \infty Grpd(S, Hom_C(c,d))
  \,.
$$

The claim then follows from the above proposition.


=--

### Limits in over-$(\infty,1)$-categories {#InOvercategories}

+-- {: .num_prop }
###### Proposition

For $C$ an $(\infty,1)$-category, $X \colon D \to C$ a [[diagram]], $C/X$ the [[over-(∞,1)-category]] and $F \colon K \to C/X$ a diagram in the over-$(\infty,1)$-category, then the [[(∞,1)-limit]] $\underset{\leftarrow}{\lim} F$ in $C/X$ coincides with the $(\infty,1)$-limit $\underset{\leftarrow}{\lim} F/X$ in $C$. 
 
=--

+-- {: .proof}
###### Proof

Modelling $C$ as a [[quasi-category]] we have that $C/X$ is given by the [[simplicial set]]

$$
  C/X 
    \;\colon\; 
  [n] \mapsto Hom_X\big([n] \star D, C\big) 
  \,,
$$

where $\star$ denotes the [[join of simplicial sets]]. The limit $\underset{\leftarrow}{\lim} F$ is the terminal object in $(C/X)/F$, which is the quasi-category given by the simplicial set

$$
  (C/X)/F 
   \;\colon\; 
  [n] \mapsto Hom_{F}\big([n] \star K, C/X\big)
  \,.
$$

Since the join [[preserved colimit|preserves]] [[colimits]] of simplicial sets in both arguments, we can apply the [[co-Yoneda lemma]] to decompose $[n] \star K = \underset{\underset{{[r] \to [n]\star K}}{\to}}{\lim} [r]$, use that the [[hom-functor]] [[hom-functor preserves limits|sends colimits in the first argument to limits]] and obtain

$$
  \begin{aligned}
     Hom([n] \star K, C/X) 
     &\simeq
     Hom\big( {\lim_{\to}}_r [r], C/X\big)
     \\
     & \simeq {\lim_{\leftarrow}}_r Hom([r], C/X)
     \\
     & \simeq {\lim_{\leftarrow}}_r Hom_F\big( [r] \star D, C \big)
     \\
     & \simeq  Hom_F\big({\lim_{\to}}_r ([r] \star D), C \big)
     \\
     & \simeq  Hom_F\big( ({\lim_{\to}}_r[r]) \star D, C \big)     
     \\
     & \simeq Hom_F\big(([n] \star K) \star D, C\big)
     \\
     & \simeq Hom_F\big([n] \star (K \star D), C\big)
     \mathrlap{\,.}
  \end{aligned}
$$

Here $Hom_F\big([r]\star D,C\big)$ is shorthand for the hom in the (ordinary) [[under category]] $sSet^{D/}$ from the canonical inclusion $D \to [r] \star D$ to $X \colon D \to C$. Notice that we use the 1-categorical analog of the statement that we are proving here when computing the colimit in this under-category as just the colimit in [[sSet|$sSet$]]. We also use that the [[join of simplicial sets]], being given by [[Day convolution]], is an associative tensor product.

In conclusion we have an isomorphism of simplicial sets

$$
  (C/X)/F \,\simeq\, C/(X/F)
$$

and therefore the terminal objects of these quasi-categories coincide on both sides. This shows that $\underset{\leftarrow}{\lim} F$ is computed as an terminal object in $C/(X/F)$.

=--


### Limits and colimits with values in $\infty Grpd$ {#WithValInooGrpd}

Limits and colimits over a [[(∞,1)-functor]] with values in the [[(∞,1)-category]] [[∞-Grpd]] of [[∞-groupoids]] may be reformulated in terms of the  [[universal fibration of (∞,1)-categories]], hence in terms of the [[(∞,1)-Grothendieck construction]].

Let [[∞Grpd]] be the [[(∞,1)-category]] of [[∞-groupoid]]s. Let the [[(∞,1)-functor]] $Z|_{Grpd} \to \infty Grpd^{op}$ be the [[universal fibration of (infinity,1)-categories|universal ∞-groupoid fibration]] whose fiber over the object denoting some $\infty$-groupoid is that very $\infty$-groupoid.

Then let $X$ be any [[∞-groupoid]] and

$$
  F : X \to \infty Grpd
$$

an [[(∞,1)-functor]]. Recall that the [[Cartesian fibration|coCartesian fibration]] $E_F \to X$ classified by $F$ is the pullback of the [[universal fibration of ∞-groupoids]] $Z|_{Grpd}$ along F:

$$
  \array{
    E_F &\to& Z|_{Grpd}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{F}{\to}& \infty Grpd
  }
$$

+-- {: .num_prop #InfinityGroupoidalCoLimitsViaIntegrationAndSlicing}
###### Proposition

Let the assumptions be as above. Then:

* The $\infty$-colimit of $F$ is equivalent to the [[(∞,1)-Grothendieck construction]] $E_F$:

  $$
    \underset{\longrightarrow}{\lim} F \simeq E_F 
  $$

* The $\infty$-limit of $F$ is equivalent to the [[∞-groupoid of sections]] of $E_F \to X$

  $$
    \underset{\longleftarrow}{\lim} \simeq \Gamma_X(E_F) 
    \,.
  $$

=-- 

The statement for the colimit is corollary 3.3.4.6 in [[Higher Topos Theory|HTT]]. The statement for the limit is corollary 3.3.3.4.

+-- {: .num_remark }
###### Remark

The form of the statement in prop. \ref{InfinityGroupoidalCoLimitsViaIntegrationAndSlicing} is the special case of the general form of [[internal (co-)limits]], here internal to the [[(∞,1)-topos]] [[∞Grpd]] with $Core(\inftyGrpd_{small})$ its small [[object classifier]]. See at _[internal (co-)limit -- Groupoidal homotopy (co-)limits](internal+%28co-%29limit#ExamplesInfinityGroupoidal)_ for more on this.

=--


### Limits and colimits with values in $(\infty,1)$Cat
 {#ColimitsInInfinityCat}

+-- {: .num_prop }
###### Proposition

For $F : D \to $ [[(∞,1)Cat]] an [[(∞,1)-functor]], its $\infty$-colimit is given by forming the [[(∞,1)-Grothendieck construction]] $\int F$ of $F$ and then inverting the [[Cartesian morphism]]s.

Formally this means, with respect to the [[model structure for Cartesian fibrations]] that there is a [[natural isomorphism]]

$$
  \lim_\to F \simeq (\int F)^\sharp
$$

in the [[homotopy category]] of the presentation of $(\infty,1)$-category by [[marked simplicial sets]].

=--

This is [[Higher Topos Theory|HTT, corollary 3.3.4.3]].

For the special case that $F$ takes values in ordinary categories see also at [[2-limit]] the section [2-limits in Cat](http://ncatlab.org/nlab/show/2-limit#2ColimitsInCat).


### Limits in $\infty$-functor categories

For $C$ an ordinary [[category]] that admits small [[limit]]s and [[colimit]]s, and for $K$ a [[small category]], the [[functor category]] $Func(D,C)$ has all small limits and colimits, and these are computed objectwise. See [[limits and colimits by example]]. The analogous statement is true for an [[(∞,1)-category of (∞,1)-functors]].


+-- {: .num_prop}
###### Proposition

Let $K$ and $C$ be [[quasi-categories]], such that $C$ has all [[limit in a quasi-category|colimits]] indexed by $K$. 

Let $D$ be a small quasi-category. Then 

* The [[(∞,1)-category of (∞,1)-functors]] $Func(D,C)$ has all $K$-indexed colimits;

* A morphism $K^\triangleright \to Func(D,C)$ is a colimiting cocone precisely if for each object $d \in D$ the induced morphism $K^\triangleright \to C$ is a colimiting cocone.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, corollary 5.1.2.3]]

=--

## Related concepts

* [[limit]], [[internal limit]]

* [[2-limit]]

* **$(\infty,1)$-limit

  * [[finite (∞,1)-limit]], [[relative (∞,1)-limit]]

  * [[homotopy limit]]

  * [[lax (∞,1)-colimit]]


## References

### General

The definition of limit in quasi-categories is due to

* [[André Joyal]], _Quasi-categories and Kan complexes_ Journal of Pure and Applied Algebra 175 (2002), 207-222.

A brief survey is on page 159 of

* [[André Joyal]], _The theory of quasicategories and its applications_ lectures at [Simplicial Methods in Higher Categories](http://www.crm.es/HigherCategories/), ([pdf](http://www.crm.cat/HigherCategories/hc2.pdf))


A detailed account is in [definition 1.2.13.4, p. 48](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=48) in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 
 {#Lurie}

* [[Denis-Charles Cisinski]], _Do homotopy limits compute limits in the associated quasicategory in the non-combinatorial model category case?_, [MO/176111/176142](http://mathoverflow.net/questions/176111/do-homotopy-limits-compute-limits-in-the-associated-quasicategory-in-the-non-com/176142#176142).

A discussion of [[weighted limit|weighted]] $(\infty,1)$-limits is in

* Martina Rovelli, _Weighted limits in an (∞,1)-category_, 2019, [arxiv:1902.00805](https://arxiv.org/abs/1902.00805)

A discussion of free colimit completion constructions is in

* [[Charles Rezk]], _Free colimit completion in ∞-categories_ ([arXiv:2210.08582](https://arxiv.org/abs/2210.08582))


Discussion [[category internal to an (infinity,1)-topos|internal to]] any [[(∞,1)-topos]]:

* [[Louis Martini]], [[Sebastian Wolf]], *Limits and colimits in internal higher category theory* &lbrack;[arXiv:2111.14495](https://arxiv.org/abs/2111.14495)&rbrack;




### In homotopy type theory

A formalization of some aspects of $(\infty,1)$-limits in terms of [[homotopy type theory]] is [[Coq]]-coded in 

* [[Guillaume Brunerie]], _[HoTT/Coq/Limits](https://github.com/guillaumebrunerie/HoTT/tree/master/Coq/Limits)_

See also

* [[Egbert Rijke]], _Homotopy Colimits and a Descent Theorem_, March 14, 2013 ([video](http://video.ias.edu/univalent-1213-0314-EgbertRijke))

[[!redirects limit in a quasi-category]]
[[!redirects limits in a quasi-category]]
[[!redirects colimit in a quasi-category]]
[[!redirects colimits in a quasi-category]]
[[!redirects limit in quasi-categories]]
[[!redirects limits in quasi-categories]]
[[!redirects colimit in quasi-categories]]
[[!redirects colimits in quasi-categories]]
[[!redirects limit in a quasicategory]]
[[!redirects colimit in a quasicategory]]
[[!redirects limit in quasicategories]]
[[!redirects limits in quasicategories]]
[[!redirects colimit in quasicategories]]
[[!redirects colimits in quasicategories]]
[[!redirects (infinity,1)-limit]]
[[!redirects (infinity,1)-colimit]]
[[!redirects (infinity,1)-limits]]
[[!redirects (infinity,1)-colimits]]

[[!redirects (∞,1)-limit]]
[[!redirects (∞,1)-colimit]]
[[!redirects (∞,1)-limits]]
[[!redirects (∞,1)-colimits]]

[[!redirects limit in an (infinity,1)-category]]
[[!redirects limits in an (infinity,1)-category]]
[[!redirects limits in (infinity,1)-categories]]
[[!redirects limit in an (∞,1)-category]]
[[!redirects limits in an (∞,1)-category]]
[[!redirects limits in (∞,1)-categories]]

[[!redirects colimit in an (infinity,1)-category]]
[[!redirects colimits in an (infinity,1)-category]]
[[!redirects colimits in (infinity,1)-categories]]
[[!redirects colimit in an (∞,1)-category]]
[[!redirects colimits in an (∞,1)-category]]
[[!redirects colimits in (∞,1)-categories]]

[[!redirects (∞,1)-powering]]
[[!redirects (∞,1)-tensoring]]
[[!redirects (∞,1)-copower]]

[[!redirects infinity1-limit]]
[[!redirects infinity1-colimit]]

