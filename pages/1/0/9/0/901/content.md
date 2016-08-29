

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc} 

## Idea 

An **ind-object** of a [[category]] $\mathcal{C}$ is a **formal [[filtered colimit]]** of objects of $C$.  Here "formal" means that the colimit is taken in the [[category of presheaves]] of $C$ (the [[free cocompletion]] of $X$). The category of ind-objects of $\mathcal{C}$ is written $ind$-$\mathcal{C}$ or $Ind(\mathcal{C})$.

Here, "ind" is short for "[[inductive system]]", as in the inductive systems used to define [[directed colimits]], and as contrasted with "pro" in the dual notion of [[pro-object]] corresponding to "projective system".

Recalling the nature of [[filtered colimits]], this means that in particular chains of inclusions 

$$
  c_1 \hookrightarrow c_2 \hookrightarrow c_3 \hookrightarrow c_4 \hookrightarrow \cdots
$$

of objects in $\mathcal{C}$ are regarded to converge to an object in $Ind(\mathcal{C})$, even if that object does not exist in $\mathcal{C}$ itself.  Standard examples where ind-objects are relevant are categories $\mathcal{C}$ whose objects are finite in some sense, such as [[finite sets]] or [[finite dimensional vector spaces]]. Their ind-categories contain then also the infinite versions of these objects as limits of sequences of inclusions of finite objects of ever increasing size. 

Moreover, ind-categories allow one to handle "big things in terms of small things" also in another important sense: many [[large category|large categories]] are actually ([[equivalence of categories|equivalent]] to) ind-categories of [[small category|small categories]]. This means that, while [[large category|large]], they are for all practical purposes controlled by a [[small category]] (see the description of the [[hom-set]] of $Ind(\mathcal{C})$ in terms of that of $C$ below). Such [[large category|large categories]] equivalent to ind-categories are therefore called [[accessible category|accessible categories]].


## Definition 

There are several equivalent ways to define ind-objects.


### As diagrams 

One definition is to define the objects of $ind$-$C$ to be diagrams $F:D\to C$ where $D$ is a [[small category|small]] [[filtered category|filtered]] category.  
The idea is to think of these diagrams as being the placeholder for the [[colimit]] over them (possibly non-existent in $C$).
We identify an ordinary object of $C$ with the corresponding diagram $1\to C$.  To see what the morphisms should be between $F:D\to C$ and $G:E\to C$, we stipulate that

1. The embedding $C\to ind$-$C$ should be [[full and faithful functor|full and faithful]],
1. each diagram $F:D\to C$ should be the colimit of itself (considered as a diagram in $ind$-$C$ via the above embedding), and
1. the objects of $C$ should be [[compact object|compact]] in $ind$-$C$.

Thus, we should have

$$
\begin{aligned}
  ind\text{-}C(F,G) &= ind\text{-}C(colim_{d\in D} F d, colim_{e\in E} G   e)\\
   &\cong lim_{d\in D}\; ind\text{-}C(F d, colim_{e\in E} G e)\\
   &\cong lim_{d\in D} colim_{e\in E}\; ind\text{-}C(F d, G e)\\
   &\cong lim_{d\in D} colim_{e\in E}\; C(F d, G e)
\end{aligned}$$

Here

* the first step is by assumption that each object is a suitable colimit;

* the second by the fact that the contravariant Hom sends colimits to limits (see properties of [[colimit]]);

* the third by the assumption that each object is a [[compact object]];

*  the last by the assumption that the embedding is a [[full and faithful functor]].

So then one _defines_ 

$$
  ind\text{-}C(F,G) \coloneqq lim_{d\in D} colim_{e\in E}\; C(F d, G e)
  \,.
$$


### As filtered colimits of representable presheaves 

Recall the [[co-Yoneda lemma]] that every presheaf $X \in PSh(C)$ is a [[colimit]] over [[representable functor|representable presheaves]]:


there is a functor $\alpha : D \to C$ (with $D$ possibly large) such that

$$
  X \simeq colim_{d \in D} Y(\alpha(d))
  \,.
$$



+-- {: .num_defn}
###### Definition

Let $ind\text{-}C \subset PSh(C)$ be the [[full subcategory]] of the [[presheaf]] [[category]] $PSh(C) = [C^{op},Set]$ on those [[functor]]s which are [[filtered colimits]] of [[representable functor|representables]], i.e. those for which 
$$
  X \simeq colim_{d \in D} Y(\alpha(d))
$$
with $D$ a [[filtered category]].
=--

+-- {: .num_remark}
###### Remark

The functors $C^{op}\to Set$ belonging to $ind\text{-}C$ under this definition --- those which are filtered colimits of representables --- have an equivalent characterization as the [[flat functors]]: those which "would preserve all finite colimits if $C$ had them".  In particular, if $C$ has finite colimits, then $ind\text{-}C$ consists exactly of the finitely cocontinuous presheaves.

For more equivalent characterizations see at _[accessible category -- Definition](accessible+category#definition)_.

=--



+-- {: .num_remark}
###### Remark

Given that $[C^{op},Set]$ is the [[free cocompletion]] of $C$, $ind$-$C$ defined in this way is its "free cocompletion under filtered colimits."

=--

To compare with the first definition, notice that indeed the formula for the [[hom-set]]s is reproduced:

Generally we have

$$
  \begin{aligned}
     [C^{op},Set](X,Y)
     & \simeq
     [C^{op}, Set](colim_{d \in D} Y F d, colim_{d' \in D'} Y G d)
     \\
     & \simeq 
     lim_{d \in D} [C^{op}, Set]( Y F d, colim_{d' \in D'} Y G d)
  \end{aligned}
$$

by the fact that the [[hom-functor]] sends [[colimit]]s to [[limit]]s in its first argument (see _properties_ at [[colimit]]). 

By the [[Yoneda lemma]] this is

$$
  \cdots \simeq 
   lim_{d \in D} (colim_{d' \in D'} Y G d')(F d)
  \,.
$$

Using that [[colimit]]s in $PSh(C)$ are computed objectwise (see again _properties_ at [[colimit]]) this is

$$
  \cdots \simeq 
   lim_{d \in D} colim_{d' \in D'} 
   C(F d, G d')  \,.
$$


## Examples 

* Let [[FinVect]] be the category of [[finite-dimensional vector spaces]] (over some [[field]]). Let $V$ be an infinite-dimensional vector space. Then $V$ can be regarded as an object of $ind-FinVect$ as the colimit $colim_{V' \hookrightarrow V} Y(V')$ over the [[filtered category]] whose objects are inclusions $V' \hookrightarrow V$ of finite dimensional vector spaces $V'$ into $V$ of the representables $Y(V') : FinVect^{op} \to Set$ ($Y$ is the [[Yoneda embedding]]).

* For $C$ the category of finitely presented objects of some equationally defined structure, $ind\text{-}C$ is the category of all these structures.

  * The category [[Grp]] of [[group]]s is the ind-category of the category of finitely generated groups.

    * The category [[Ab]] of [[abelian group]]s is the ind-category of the category of finitely generated abelian groups.

* A [[formal scheme]] is an ind-object in [[schemes]].

## Properties 


In the following we write $\underset{\longrightarrow}{\lim}^f$ for the "formal colimits" defining ind-object. I.e. if $\alpha \colon \mathcal{I} \to \mathcal{C}$ is a small [[diagram]] and with $i \colon Ind(\mathcal{C}) \hookrightarrow PSh(\mathcal{C})$ the defining inclusion, then

$$
  \underset{\longrightarrow}{\lim}^f (\alpha)
  \;\coloneqq\;
  \underset{\longrightarrow}{\lim} (i \circ \alpha )
  \,.
$$

### The category of ind-objects

+-- {: .num_prop}
###### Proposition


If $\mathcal{C}$ is a [[locally small category]] then so is $Ind(\mathcal{C})$.

=--

+-- {: .num_prop}
###### Proposition

$Ind(\mathcal{C})$ admits small [[filtered colimits]] and the defining inclusion $Ind(\mathcal{C}) \hookrightarrow PSh(\mathcal{C})$ commutes with these colimits.

=--

(e.g. [KashiwaraSchapira 06, theorem 6.1.8](#KashiwaraSchapira06))

The following says that morphisms between ind-objects are represented by [[natural transformation]] of the filtered diagrams that represent them, possibly up to restricting these diagrams first along a [[cofinal functor]].

+-- {: .num_prop}
###### Proposition

Let 

1. $\mathcal{I}_1$ and $\mathcal{I}_2$ be two [[small category|small]] [[filtered category]];

1. $\alpha_1 \colon \mathcal{I}_1 \longrightarrow \mathcal{C}$ and $\alpha_2 \colon \mathcal{I}_2 \longrightarrow \mathcal{C}$ be two [[functors]];

1. $f 
    \;\colon\;
  \underset{\longrightarrow}{\lim}^f \alpha_1
    \longrightarrow
  \underset{\longrightarrow}{\lim}^f \alpha_2$

  a [[morphism]] between their images in $Ind(\mathcal{C})$. 

Then there exists 

1. a small [[filtered category]] $K$

1. [[cofinal functors]] $p_i \colon K \longrightarrow \mathcal{I}_i$

1. a [[natural transformation]] $\phi \;\colon\; \alpha_1 \circ p_1  \longrightarrow \alpha_2 \circ p_2$

such that the following [[commuting diagram|diagram commutes]]

$$
  \array{
    \underset{\longrightarrow}{\lim}^f(\alpha_1 \circ p_1)
      &\overset{\underset{\longrightarrow}{\lim}^f \phi}{\longrightarrow}&
    \underset{\longrightarrow}{\lim}^f(\alpha_2 \circ p_2)
    \\
    {}^{\mathllap{\simeq}}\donwarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \underset{\longrightarrow}{\lim}^f \alpha_1
      &\underset{f}{\longrightarrow}&
    \underset{\longrightarrow}{\lim}^f \alpha_2
  }
  \,.
$$

=--

(e.g. [KashiwaraSchapira 06, prop. 6.1.13](#KashiwaraSchapira06))

+-- {: .num_cor}
###### Corollary

For each $f \colon A_1 \longrightarrow A_2$ a [[morphism]] in $Ind(\mathcal{C})$, then there exists

1. a [[small category|small]] [[filtered category]] $\mathcal{I}$;

1. [[functors]] $\lapha_i \;\colon\; \mathcal{I} \to \mathcal{C}$ ($i \in \{1,2\}$);

1. a [[natural transformation]] $\phi \colon \alpha_1 \longrightarrow \alpha_2$

such that 

$$
  \array{
    A_1 &\overset{f}{\longrightarrow}& A_2
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \underset{\longrightarrow}{\lim}^f \alpha_1
      &\underset{\underset{\longrightarrow}{\lim}^f \phi }{\longrightarrow}&
    \underset{\longrightarrow}{\lim}^f \alpha_2
  }
  \,.
$$

=--

(e.g. [KashiwaraSchapira 06, corollary 6.1.14](#KashiwaraSchapira06))


+-- {: .num_prop}
###### Proposition

The canonical inclusion $y \;\colon\; \mathcal{C} \hookrightarrow Ind(\mathcal{C})$ (factoring the [[Yoneda embedding]]) is [[exact functor|right exact]].

=--

(e.g. [KashiwaraSchapira 06, corollary 6.1.6](#KashiwaraSchapira06))

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ have all [[finite limits]] or all [[small limits]]. Then also $Ind(\mathcal{C})$ has all finite or small limits, respectively, and the canonical functor $y \;\colon\; \mathcal{C} \longrightarrow Ind(\mathcal{C})$ preserves these, respectively.

=--

(e.g. [KashiwaraSchapira 06, corollary 6.1.17](#KashiwaraSchapira06))

+-- {: .num_prop}
###### Proposition

If $\mathcal{C}$ has [[cokernels]], then so does $Ind(\mathcal{C})$.

If $\mathcal{C}$ has [[finite colimit]] [[coproducts]], then $Ind(\mathcal{C})$ has small [[coproducts]].

If $\mathcal{C}$ has all [[finite colimits]], then $Ind(\mathcal{C})$ has all small [[colimits]].

=--

(e.g. [KashiwaraSchapira 06, prop. 6.1.18](#KashiwaraSchapira06))


### Recognition of Ind-objects

+-- {: .num_prop}
###### Proposition

A [[functor]] $F \colon \mathcal{C}^{op} \to Set$ is in $Ind(\mathcal{C})$ (i.e. is a [[filtered colimit]] of [[representable functor|representables]]) precisely if the [[comma category]] $(Y,const_F)$ (with $Y$ the [[Yoneda embedding]]) is [[filtered category|filtered]] and [[cofinally small category|cofinally small]].

=--

+-- {: .num_prop}
###### Proposition

If $\mathcal{C}$ admits finite [[colimits]], then $Ind(\mathcal{C})$ is the [[full subcategory]] of the [[presheaf]] category $PSh(\mathcal{C})$ consisting of those functors $F \colon \mathcal{C}^{op} \to Set$ such that $F$ is [[exact functor|left exact]] and the [[comma category]] $(Y,F)$ (with $Y$ the [[Yoneda embedding]]) is [[cofinally small category|cofinally small]].

=--

### Functoriality

Ind-cocompletion is functorial -- in fact an underlying 2-functor of a [[lax-idempotent 2-monad]] (KZ-monad). More in detail:

+-- {: .num_prop #FunctorialityOfInd}
###### Proposition

Let $F \colon \mathcal{C}_1 \longrightarrow \mathcal{C}$ be a [[functor]]. Then there is a unique [[extension]] $Ind(F)$ of this functor to ind-objects, i.e. a [[commuting diagram]]

$$
  \array{
    \mathcal{C}_1 &\overset{F}{\longrightarrow}& \mathcal{C}_2
    \\
    \downarrow
      &&
    \downarrow
    \\
    Ind(\mathcal{C}_1)
      &\underset{Ind(F)}{\longrightarrow}&
    Ind(\mathcal{C}_2)
  }
  \,,
$$

such that $Ind(F)$ preserves small [[filtered colimits]].

Moreover, 

1. this construction respects [[composition]] in that 

   $$
     Inf(G \circ F ) \simeq Ind(G) \circ Ind(F)
   $$

1. if $F$ is a [[faithful functor]] or [[fully faithful functor]], then so is $Ind(F)$, respectively.

=--

(e.g. [KashiwaraSchapira 06, prop.6.1.9-6.1.11](#KashiwaraSchapira06))

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}_1$ and $\mathcal{C}_2$ be two [[small categories]]. By prop. \ref{FunctorialityOfInd} the two [[projections]] out of their [[product category]] induce a functor of the form

$$
  Ind(\mathcal{C}_1 \times \mathcal{C}_2)
    \longrightarrow
  Ind(\mathcal{C}_1) \times Ind(\mathcal{C}_2)
  \,.
$$

This is an [[equivalence of categories]].

=--

([KashiwaraSchapira 06, prop. 6.1.12](#KashiwaraSchapira06))


### The case that $\mathcal{C}$ already admits filtered colimits


([KashiwaraSchapira 06, chapter 6.3](#KashiwaraSchapira06))

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a [[category]] which has all small [[filtered colimits]]. Then the canonical functor $\mathcal{C} \longrightarrow Ind(\mathcal{C})$ defines a [[reflective subcategory]], i.e. it is a [[fully faithful functor]] with a [[left adjoint]]

$$
  \mathcal{C}
    \underoverset
     {\underset{}{\longrightarrow}}
     {\overset{J}{\longleftarrow}}
     {\bot}
  Ind(\mathcal{C})
$$

=--

([KashiwaraSchapira 06, prop. 6.3.1](#KashiwaraSchapira06))

+-- {: .num_prop}
###### Proposition

Let $F \colon \mathcal{J} \longrightarrow \mathcal{C}$ be a [[functor]] such that

1. $F$ is a [[fully faithful functor]];

1. $\mathcal{C}$ has all small [[filtered colimits]];

1. for every object $J \in \mathcal{J}$ its image $F(J) \in \mathcal{C}$ is [[compact object|compact]].

Then the composite

$$
  Ind(\mathcal{J})
    \overset{Ind(F)}{\longrightarrow}
  Ind(\mathcal{C})
    \overset{J}{\longrightarrow}
  \mathcal{C}
$$

is a [[fully faithful functor]].

=--

([KashiwaraSchapira 06, prop. 6.3.4](#KashiwaraSchapira06))


+-- {: .num_prop}
###### Proposition

If $\mathcal{C}$ is a [[category]] such that

1. every object of $\mathcal{C}$ is a [[filtered colimit]] of [[compact object]];

1. $\mathcal{C}$ has all small [[filtered colimits]]

then the functor

$$
  Ind(\mathcal{C}_{cpt}) 
    \longrightarrow 
  Ind(\mathcal{C})
    \overset{J}{\longrightarrow}
  \mathcal{C}
$$

is an [[equivalence of categories]].

=--

([KashiwaraSchapira 06, corollary 6.3.5](#KashiwaraSchapira06))


## Applications

* One important use of categories of ind-objects is in [[abelian sheaf]]-theory: for every [[small category|small]] [[abelian category]] $C$ the category $ind\text{-}C$ is a [[Grothendieck category]] and hence a good coefficient object for [[abelian sheaf cohomology]].

## In higher category theory

### In $(\infty,1)$-categories 

There is a notion of [[ind-object in an (∞,1)-category]].

With regard to the third of the properties listed above, notice that the [[comma category]] $(Y,const_F)$ is the [[category of elements]] of $F$, i.e. the [[pullback]] of the [[generalized universal bundle|universal Set-bundle]] $U : Set_* \to Set$ along $F : C^{op} \to Set$. This means that the [[stuff, structure, property|forgetful functor]]
$
  (Y,const_F) \to C
$
is the fibration classified by $F$. 

This is the starting point for the definition at [[ind-object in an (∞,1)-category]].

## Related concepts

* **ind-object** / [[ind-object in an (∞,1)-category]]

* [[pro-object]] / [[pro-object in an (∞,1)-category]]

* [[ind-pro-object]]

* [[flat functor]]

* [[KZ-monad]]


## References
Ind-categories were introduced in 

* Grothendieck and Verdier in SGA4 Exp. 1 [pdf file](http://sage.math.washington.edu/home/wstein/www/home/craigcitro/sga4/Grothendieck/SGA4/sga41.pdf)

and the dual notion of [[pro-object]] in 

* A. Grothendieck, _Techniques de d&#233;scente et th&#233;or&#232;mes d'existence en g&#233;om&#233;trie alg&#233;brique, II: le th&#233;or&#232;me d'existence en th&#233;orie formelle des modules_, Seminaire Bourbaki __195__, 1960, [(pdf)](http://archive.numdam.org/ARCHIVE/SB/SB_1958-1960__5_/SB_1958-1960__5__369_0/SB_1958-1960__5__369_0.pdf).

Ind-categories are discussed in

* {#KashiwaraSchapira06} [[Masaki Kashiwara]], [[Pierre Schapira]], section 6 of _[[Categories and Sheaves]]_ , Grundlehren der mathematischen Wissenschaften 332 (2006)

* [[Peter Johnstone]], section VI.1 of _[[Stone Spaces]]_

They are discussed in relation to generalisations in

* [[Ji?í Adámek]], [[Francis Borceux]], [[Stephen Lack]], [[Ji?í Rosický]], _A classification of accessible categories,_ Journal of Pure and Applied Algebra 175:7-30, 2002. [abstract](http://maths.mq.edu.au/~slack/papers/acc.html)

See also the remarks at the beginning of section 5.3 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects ind-objects]]
[[!redirects ind object]]
[[!redirects ind-completion]]
[[!redirects ind-cocompletion]]
