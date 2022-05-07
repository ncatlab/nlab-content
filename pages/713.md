
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Passing from a [[category]] $C$ to its [[presheaf]] category $PSh(C) := [C^{op},Set]$ may be regarded as the operation of
"freely adjoining [[colimits]] to $C$". 

A slightly more precise version of this statement is that the [[Yoneda embedding]]

$$
  Y : C \hookrightarrow PSh(C)
$$

is the **[[free construction|free]] [[cocomplete category|cocompletion]]** of $C$.

The [[universal property]] of the [[Yoneda embedding]] is expressed in terms of the [[Yoneda extension]] of any [[functor]] $F : C \to D$ to a category $D$ with colimits.


## Technical details 


The rough statement is that the [[Yoneda embedding]]

$$y_S: S \to Set^{S^{op}}$$ 

of a [[small category]] $S$ into the category $Set^{S^{op}}$ of [[presheaf|presheaves]] on $S$ is universal among functors from $S$ into [[cocomplete category|cocomplete categories]]. Technically, this should be understood in an appropriate [[2-category|2-categorical]] sense: given a [[functor]] $F: S \to D$ where $D$ is ([[small colimit|small]]-)cocomplete, there exists a unique (up to [[isomorphism]]) [[cocontinuous functor|cocontinuous]] [[extension]] 
$$\hat{F}: Set^{S^{op}} \to D,$$
called the [[Yoneda extension]],
meaning that $\hat{F} y_S \cong F$ and $\hat{F}$ [[preserved limit|preserves]] [[small colimits]]. 

Put slightly differently: let $Cocomp$ denote the 2-category of cocomplete categories, cocontinuous functors, and natural transformations between them. Then for cocomplete $D$, the Yoneda embedding $y S: S \to Set^{S^{op}}$ induces by restriction a functor 

$$res_{y S} D: Cocomp(Set^{S^{op}}, D) \to Cat(S, D)$$ 

that is an [[equivalence of categories|equivalence]] for each $D$, one that is [[2-natural transformation|2-natural]] in $D$. In fact we show that the Yoneda extension $F \mapsto \hat{F}$ gives a functor $ext_{y S}D: Cat(S, D) \to Cocomp(Set^{S^{op}}, D)$ that is a left adjoint to $res_{y S}D$, giving a 2-natural adjoint equivalence. 

As a first step, we construct the desired extension $\hat{F}$ as a [[adjoint functor|left adjoint]] to the functor 

$$D \to Set^{S^{op}}: d \mapsto \hom_D(F-, d).$$ 

Being a left adjoint, $\hat{F}$ is cocontinuous. 

An explicit formula for the left adjoint is given by the [[weighted colimit]], [[end|coend]], or [[tensor product of functors]] formula 
$$\hat{F}(X) = X \otimes_S F = \int^{s: S} X(s) \cdot F(s)$$ 
where $S \cdot d$ is notation for [[power|copowering]] (or tensoring) an object $d$ of $D$ by a set $S$ (in this case, a coproduct of an $S$-indexed set of copies of $D$). This formula recurs frequently throughout this wiki; see also [[nerve]], [[Day convolution]]. 

This "free cocompletion" property generalizes to [[enriched category]] theory. If $V$ is complete, cocomplete, symmetric monoidal closed, and $S$ is a small $V$-enriched category, then the enriched presheaf category $V^{S^{op}}$ is a free $V$-cocompletion of $S$. The explicit meaning is analogous to the case where $V = Set$, where all ordinary category concepts are replaced by their $V$-enriched analogues; in particular, the notion of "$V$-cocontinuous functor" referes to preservation of enriched weighted colimits (not just ordinary conical colimits). 

If $C$ is not small, then its free cocompletion still exists, but it is not the category of all presheaves on $C$.  Rather, it is the category of [[small presheaves]] on $C$, i.e. presheaves that are small colimits of representables.



### Proofs 


+-- {: .num_prop #FreeCocompletion}
###### Proposition

For $\mathcal{C}$ a [[small category]], its [[Yoneda embedding]] $\mathcal{C} \overset{y}{\hookrightarrow} [\mathcal{C}^{op}, Set]$ exhibits the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ as the _free co-completion_ of $\mathcal{C}$, in that it is a [[universal morphism]] (as in [this Def.](adjoint+functor#UniversalArrow)  but "up to natural isomorphism") into a [[cocomplete category]], in that:

1. for $\mathcal{D}$ any [[cocomplete category]];

1. for $F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ any [[functor]];

there is a [[functor]] $\widetilde F \;\colon\; [\mathcal{C}^{op}, Set] \longrightarrow \mathcal{D}$, unique up to [[natural isomorphism]], such that

1. $\widetilde F$ [[preserved limit|preserves]] all [[colimits]],

1. $\widetilde F$ [[extension|extends]] $F$ through the [[Yoneda embedding]], in that the following [[commuting diagram|diagram commutes]], up to [[natural isomorphism]]:

$$
  \array{
    && \mathcal{C}
    \\
    & {}^{y}\swarrow &\swArrow& \searrow^{\mathrlap{F}}
    \\
    \mathrlap{ \!\!\!\!\!\!\!\!\!\!\!\!\! [\mathcal{C}^{op}, Set] }
      && \underset{ \widetilde F }{\longrightarrow} &&
    \mathcal{D}
  }
$$

=--

+-- {: .proof}
###### Proof

The last condition says that $\widetilde F$ is fixed on [[representable presheaves]], up to isomorphism, by

\[
  \label{YonedaRestriction}
  \widetilde F( y(c) ) \simeq F(c)
\]

and in fact [[natural isomorphism|naturally]] so:

\[
  \label{FunctorialYonedaRestriction}
  \array{
    c_1&&
    \widetilde F( y(c_1) ) &\simeq& F(c_1)
    \\
    {}^{\mathllap{f}}\big\downarrow
     && {}^{\mathllap{ F(y(f)) }}\big\downarrow && \big\downarrow^{\mathrlap{ F(f) }}
    \\
    c_2 && \widetilde F (y(c_2)) &\simeq& F(c_2)
  }
\]


But the [[co-Yoneda lemma]] expresses every [[presheaf]] $\mathbf{X} \in [\mathcal{C}^{op}, Set]$ as a [[colimit]] of [[representable presheaves]]

$$
  \mathbf{X} \;\simeq\; \int^{c \in \mathcal{C}} y(c) \cdot \mathbf{X}(c)
  \,.
$$

Since $\tilde F$ is required to preserve any colimit and hence these particular colimits, (eq:YonedaRestriction) implies that $\widetilde F$ is fixed to act, up to isomorphism, as

$$
  \begin{aligned}
    \widetilde F(\mathbf{X})
    & =
    \widetilde F
    \left(
      \int^{c \in \mathcal{C}} y(c) \cdot \mathbf{X}(c)
    \right)
    & \coloneqq
    \int^{c \in \mathcal{C}} F(c) \cdot \mathbf{X}(c)
    \;\;\;\;\in \mathcal{D}
  \end{aligned}
$$

(where the colimit (a [[coend]]) on the right is computed in $\mathcal{D}$!).

=--

## Free cocompletion of large categories

In general, given a locally small (but possibly large) category $\mathcal{A}$, we can define a locally small category of _small presheaves_ on $\mathcal{A}$ as the full subcategory of the functor category $Fun(\mathcal{A}^{\mathrm{op}},\operatorname{Set})$ spanned by those functors  that are colimits of small diagrams of representables.  Equivalently, a _small presheaf_ is a functor $F:\mathcal{A}^{\mathrm{op}} \to \operatorname{Set}$ such that there exists a functor $\gamma:\mathcal{C} \to \mathcal{A}$ with $\mathcal{C}$ small and a presheaf $F': \mathcal{C}^{\mathrm{op}}\to \operatorname{Set}$ such that

$$F=\operatorname{Lan}_{\gamma} F'.$$  

This process of free cocompletion defines a functor $L$ from the 2-category 

$$ CAT = [locally \; small \; categories, \; functors, \; natural \; transformations ] $$

to the 2-category 

$$ Cocomp = [locally \; small \; cocomplete \; categories, \; cocontinuous \; functors, natural \; transformations ] $$

where, just to be clear, 'cocomplete' means having all *small* colimits, as usual.   Moreover, this functor $L$ is part of a [[pseudoadjunction]] where the right adjoint $R: Cocomp \to CAT$ assigns each locally small coccomplete category its underlying category, and so on.

In the case where $\mathcal{A}^{\mathrm{op}}$ is [[locally presentable]], the category of small presheaves on $\mathcal{A}$ is equivalent to the category of [[accessible functors]] $\mathcal{A}^{\mathrm{op}}\to \operatorname{Set}$. In this situation, the category of small functors has many nice properties and is often said to be _almost a topos_. In particular, under this assumption, the category of small presheaves is complete, cocomplete, and Cartesian-closed. 

See [Day-Lack](#DayLack) for more details on all these matters. They handle the more general case of enriched categories.

## Free cocompletion as a pseudomonad

[[David Corfield]]: So is this 'free cocompletion' part of  an adjunction between the category of categories and the category of cocomplete categories (modulo size worries?).  Or should we think of it as part of a [[pseudoadjunction]] between _2-categories_?  (I would start a page on that, but how are naming conventions going in this area?)

[[John Baez]]:  Equations between functors tends to hold only up to natural isomorphism.  So, your first guess should not be that there's an _adjunction_ between the _categories_ $CAT$ and $Cocomp$, but rather, a _pseudoadjunction_ between the _2-categories_ $CAT$ and $Cocomp$.   

This means there's a forgetful 2-functor:

$$ R: Cocomp \to CAT $$

together with a 'free cocompletion' 2-functor:

$$  L: CAT \to Cocomp $$

And, it mean there's an equivalence of categories

$$ hom_{Cocomp} (F C, D) \simeq
   hom_{CAT} (C, U D)  $$

for every $C \in CAT$, $D \in Cocomp$.  And finally, it means that this equivalence is [[pseudonatural transformation|pseudonatural]] as a function of $C$ and $D$.

If we have a pseudonatural equivalence of categories

$$ hom_{Cocomp} (F C, D) \simeq
   hom_{CAT} (C, U D)  $$

instead of a natural isomorphism of sets, then we say we have a 'pseudoadjunction' instead of an adjunction.   A pseudoadjunction is the right generalization of adjunction when we go to 2-categories; if we were feeling in a modern mood we might just say 'adjunction' and expect people to know we meant 'pseudo'.

The details have been worked out by [Day-Lack](#DayLack) in even more generality: they consider enriched categories.  Note that the free cocompletion of a *small* category $C$ is the category of all presheaves on $C$, but for a more general *locally small* category it's just the category of small presheaves.

In [their work on species](http://www.lacim.uqam.ca/~gambino/species.pdf), Fiore, Gambino, Hyland and Winskel confronted the size issues in another way.  In one draft of this paper they had a very artful and sophisticated device for dealing with this size problem.  In the latest draft they seem to have sidestepped it entirely: you'll see they discuss the 'free symmetric monoidal category on a category' pseudomonad, but never the 'free cocomplete category on a category' pseudomonad, even though they _do_ use the $\widehat{C}$ construction all over the place.  Somehow they've managed to avoid the need to consider this construction as a pseudomonad!

Fiore, Gambino, Hyland and Winskel later exhibited the free cocompletion of a small category as a [[relative pseudomonad]] from the 2-category Cat of small categories into the 2-category CAT of locally-small categories (via the 2-category COC of locally-small cocomplete categories). See [FGHW](#FGHW) for more details.

## In higher category theory

One can ask for the notion of free cocompletion in the wider context of [[higher category theory]].

* for [[(∞,1)-category]] theory there is [[free (∞,1)-cocompletion]].

## Related concepts

* [[free coproduct completion]]

* [[idempotent completion]]

* [[Cauchy completion]]

## References 

* {#DayLack} [[Brian Day]], [[Steve Lack]], _Limits of small functors_ ([web](https://arxiv.org/abs/math/0610439))


* {#FGHW} Fiore, Gambino, Hyland and Winskel, _Relative pseudomonads, Kleisli bicategories, and substitution monoidal structures_, ([web](https://arxiv.org/pdf/1612.03678.pdf))


This reference might also give helpful clues:

* [[Daniel Dugger]], _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

A pedagogical explanation of the universal property of the [[Yoneda embedding]] is given starting on page 7.
On page 8 there's an explanation with lots of pictures how a presheaf is an "instruction for how to build a colimit".
Then on p. 9 the universal morphism that we are looking for here is identified as the one that "takes the instructions for building a colimit and actually _builds_ it".

(This text, by the way, contains various other gems. A pity that it is left unfinished.)

[[!redirects free cocompletions]]

[[!redirects free colimit completion]]
[[!redirects free colimit completions]]

[[!redirects free co-completion]]
[[!redirects free co-completions]]
