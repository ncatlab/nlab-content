
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
"freely adjoining [[colimit]]s to $C$". 

A more precise version of this statement is that the [[Yoneda embedding]]

$$
  Y : C \hookrightarrow PSh(C)
$$

is the **free cocompletion** of $C$.

The [[universal property]] of the [[Yoneda embedding]] is expressed in terms of the [[Yoneda extension]] of any [[functor]] $F : C \to D$ to a category $D$ with colimits.


## Technical details 


The [[Yoneda embedding]]
$$y_S: S \to Set^{S^{op}}$$ 
of a [[small category]] $S$ into the category $Set^{S^{op}}$ of [[presheaf|presheaves]] on $S$ 
is universal among functors from $S$ into [[cocomplete category|cocomplete categories]], in the sense that given a functor $F: S \to D$ where $D$ is cocomplete, there exists a unique (up to isomorphism) [[cocontinuous functor|cocontinuous]] extension 
$$\hat{F}: Set^{S^{op}} \to D,$$
called the [[Yoneda extension]],
meaning that $\hat{F} y_S \cong F$ and $\hat{F}$ preserves small colimits. Indeed, the desired $\hat{F}$ is [[adjoint functor|left adjoint]] to the functor 
$$D \to Set^{S^{op}}: d \mapsto \hom_D(F-, d)$$ 

An explicit formula for the left adjoint is given by the [[weighted colimit]], [[end|coend]], or [[tensor product of functors]] formula 
$$\hat{F}(X) = X \otimes_S F = \int^{s: S} X(s) \cdot F(s)$$ 
where $S \cdot d$ is notation for [[power|copowering]] (or tensoring) an object $d$ of $D$ by a set $S$ (in this case, a coproduct of an $S$-indexed set of copies of $D$). This formula recurs frequently throughout this wiki; see also [[nerve]], [[Day convolution]]. 

This "free cocompletion" property generalizes to [[enriched category]] theory. If $V$ is complete, cocomplete, symmetric monoidal closed, and $S$ is a small $V$-enriched category, then the enriched presheaf category $V^{S^{op}}$ is a free $V$-cocompletion of $S$. The explicit meaning is analogous to the case where $V = Set$, where all ordinary category concepts are replaced by their $V$-enriched analogues; in particular, the notion of "$V$-cocontinuous functor" referes to preservation of enriched weighted colimits (not just ordinary conical colimits). 

If $C$ is not small, then its free cocompletion still exists, but it is not the category of all presheaves on $C$.  Rather, it is the category of [[small presheaves]] on $C$, i.e. presheaves that are small colimits of representables.


### Proving the theorem


+-- {: .un_theorem}
###### Theorem

Given any [[cocomplete category]] $B$, and any functor $F : A \to B$, there is a [[cocontinuous functor]] $\widehat{F} : \hat{A} \to B$ making this triangle commute up to natural isomorphism:

$$
  \array{
     A &\stackrel{F}{\to}& B
     \\
     \downarrow^Y & \nearrow_{\widehat{F}}
     \\
     \widehat{A}
  }
  
$$

Moreover, $\widehat{F}$ is unique up to natural isomorphism.

=--

There are probably lots of ways to prove it, but let's take a simple-minded approach that mimics the obvious proof of the Decategorified Theorem.  We proved the Decategorified Theorem by finding a formula for the map we needed.  So let's try to write a _formula_ for $\widehat{F}$, based on three ideas:

1. Since the triangle commutes, we know what $\widehat{F}$ should do to guys in the image of $Y$.  Namely:
$$\widehat{F}(Y(x)) = F(x)$$
(The triangle could just commute up to natural isomorphism, but let's not worry about that yet --- that's just a nuance.)
1. We know that $\widehat{F}$ preserves colimits.
1. We know that every object in $\widehat{A}$ is a colimit of guys in the image of $Y$.  (Such guys are called [[representable functor|representable]].)

The key fact in item 3 is also called the _[[co-Yoneda lemma]]_. For more see there, or see below.

These three facts are already enough to determine $\widehat{F}$ on objects.   

**Exercise:** Why?

So $\widehat{F}$ is well on its way to being unique. 

But why does $\widehat{F}$ exist?  For this it will really be good to have a _formula_ expressing every object in $\widehat{A}$ as a colimit of guys in the image of $Y$.  As a side-effect this will prove fact 3.  But even better: thanks to fact 2, this formula will yield a formula for $\widehat{F}$.  And a formula is the best way to prove existence.

[[Mike Stay]]: Given categories $A, B$ and a functor $F: A \to \hat{B}$, the fact that all objects in $\hat{B}$ can be written as a sum over representables says that

$$\array{F:A  &\to& \hat{B}\\ a &\mapsto& \int_{b \in B} F(a)(b) \; \times \; hom(-, b)}$$

In a similar way, the Yoneda embedding says

$$\array{Y:A &\to& \hat{A}\\ a &\mapsto& \int_{a' \in A} Y(a)(a') \; \times \; hom(-, a')\\&&= \int_{a' \in A} hom(a', a) \; \times \; hom(-, a')\\&&= hom(-, a)}$$

That is, the set of morphisms from $-$ to $a$ is the set of morphisms from $-$ to an intermediate object $a'$ times the morphisms from $a'$ to $a$, where $a'$ ranges over all possible objects in $A$.

Doing the same for an arbitrary cocontinuous functor $G:\hat{A} \to \hat{B}$ says

$$c = \int_{a \in A} c(a) \; \times \; hom(-, a)$$

maps to

$$G(c) = \int_{a \in A} \left(\int_{b \in B} G(a)(b) \; \times \; hom(a, b) \right) \; \times \; c(a) \; \times \; hom(-, a)$$

which simplifies to

$$G(c) = \int_{b \in B} \int_{a \in A} G(a)(b) \; \times \; c(a) \; \times \; hom(-, b)$$

by taking $a$ as the midpoint between $-$ and $b$.  So $G$ is completely determined (up to isomorphism) by its values on the embedding of $A$.

[[John Baez]]:  Very good!  But let me ask a few questions, starting with this.  You say

"Given categories $A, B$ and a functor $F: A \to \hat{B}$, the fact that all objects in $B$ can be written as a sum over representables says that

$$\array{F:A  &\to& \hat{B}\\ a &\mapsto& \int_{b \in B} F(a)(b) \; \times \; hom(-, b)} $$

I feel funny about this, because you say "all objects of $B$ can be written as a sum over representables", but this doesn't really make sense.  It's true that "all objects of $\widehat{B}$ can be written as a colimit of representables" --- is that what you meant?   But even if so, how does this fact "say that

$$\array{F:A  &\to& \widehat{B}\\ a &\mapsto& \int_{b \in B} F(a)(b) \; \times \; hom(-, b)?} $$

And I'd like us to write up a proof of the Theorem, so try to fit what you've written into a proof.

[[Mike Stay]].  Yes, I was being sloppy when I said "sum".  As for how it's a colimit, consider two functors $F:C^{op} \to Set, \; G:C \to Set.$  Then

$$\int_{c \in C} F(c) \; \times \; G(c)$$

is a colimit: for each $f:c \to c'$ in $C$, we get a diagram

$$\array{F(c) \;\times\; G(c) & \stackrel{F(f) \;\times\; G(c)}{\leftarrow} & F(c') \;\times\; G(c) & \stackrel{F(c') \;\times\; G(f)}{\to} & F(c') \;\times\; G(c')}$$

and the colimit of all these is the "integral" above.

If I do a "search and replace" on the decategorified proofs, I get this:

"**Proof.** The proof here is easy.   Objects of $\widehat{A}$ are colimits of objects of $Y(A) = hom(-, A)$, like

$$ x = \int_{a \in A} x(a) \;\times\; hom(-, a) $$

with some "coefficients" $x(a).$  So, $\widehat{F}$ is determined by the fact that it preserves colimits and acts like $F$ on guys in $hom(-, A)$:

$$\widehat{F}(x) = \widehat{F} (\int_{a \in A} x(a) \;\times\; hom(-, a)) =
\int_{a \in A} x(a) \;\times\; \widehat{F}(hom(-, a)) = \int_{a \in A} x(a) \;\times\; F(hom(-, a))  $$

Lo and behold --- now we have a _formula_ for $\widehat{F}$.  So, we just need to check some stuff.  Check that $\widehat{F}$ is well-defined.  Check that it preserves colimits.  Check that it makes the diagram commute up to natural isomorphism.  Check that it's unique up to natural isomorphism.  All this is follow-your-nose stuff."

But I bet you want me to actually follow my nose this time.


## Free cocompletion as a pseudomonad

[[David Corfield]]: So is this 'free cocompletion' part of  an adjunction between the category of categories and the category of cocomplete categories (modulo size worries?).
Or should we think of it as part of a [[pseudoadjunction]] between _2-categories_?  (I would start a page on that, but how are naming conventions going in this area?)

[[John Baez]]:  Equations between functors tends to hold only up to natural isomorphism.  So, your first guess should not be that there's an _adjunction_ between the _categories_ $Cat$ and $CocompleteCat$, but rather, a _pseudoadjunction_ between the _2-categories_ $Cat$ and $CocompleteCat$.   

If this were true, what would it mean?  It would mean that there's a forgetful 2-functor:

$$ U: CocompleteCat \to Cat $$

together with a 'free cocompletion' 2-functor, which right now we've been calling 'hat':

$$ F: Cat \to CocompleteCat $$
$$  F: C \mapsto \widehat{C} = Set^{C^{op}}$$

And, it would mean there's an equivalence of categories

$$ hom_{CocompleteCat} (F C, D) \simeq
   hom_{Cat} (C, U D)  $$

for every $C \in Cat$, $D \in CocompleteCat$.  And fiinally, it would also be saying that this equivalence is [[pseudonatural transformation|pseudonatural]] as a function of $C$ and $D$.

If we have a pseudonatural equivalence of categories

$$ hom_{CocompleteCat} (F C, D) \simeq
   hom_{Cat} (C, U D)  $$

instead of a natural isomorphism of sets, then we say we have a 'pseudoadjunction' instead of an adjunction.   A pseudoadjunction is the right generalization of adjunction when we go to 2-categories; if we were feeling in a modern mood we might just say 'adjunction' and expect people to know we meant 'pseudo'.

Naively, it seems we _do_ have such a pseudoadjunction, at least _modulo size issues_---which unfortunately is sort of like saying "modulo truth"!  The problem is that if Cat is the 2-category of [[small category|small]] categories then to define the free cocompletion functor

$$ F : Cat \to CocompleteCat $$

we need $CocompleteCat$ to be the 2-category of [[large category|large]] categories.  But if $CocompleteCat$ is the 2-category of [[large category|large]] categories then to define 

$$ U: CocompleteCat \to Cat $$

we need $Cat$ to be the 2-category of large categories!   So, instead of an honest pseudoadjunction that bounces us back and forth between two 2-categories, the size keeps ratcheting up each time we make a round trip!

In particular, if we try to define a [[pseudomonad]]

$$ U F : Cat \to Cat $$

we're stuck: the '$Cat$' at right contains larger categories than the one at left.

In [their work on species](http://www.lacim.uqam.ca/~gambino/species.pdf), Fiore, Gambino, Hyland and Winskel had to confront this issue.  In one draft of this paper they had a very artful and sophisticated device for dealing with this size problem.  In the latest draft they seem to have sidestepped it entirely: you'll see they discuss the 'free symmetric monoidal category on a category' pseudomonad, but never the 'free cocomplete category on a category' pseudomonad, even though they _do_ use the $\widehat{C}$ construction all over the place.  Somehow they've managed to avoid the need to consider this construction as a pseudomonad!

## In higher category theory

One can ask for the notion of free cocompletion in the wider context of [[higher category theory]].

* for [[(∞,1)-category]] theory there is [[free (∞,1)-cocompletion]] .

## References 

This reference might also give helpful clues:

* [[Daniel Dugger]], _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

A pedagogical explanation of the universal property of the [[Yoneda embedding]] is given starting on page 7.
On page 8 there's an explanation with lots of pictures how a presheaf is an "instruction for how to build a colimit".
Then on p. 9 the universal morphism that we are looking for here is identified as the one that "takes the instructions for building a colimit and actually _builds_ it".

(This text, by the way, contains various other gems. A pity that it is left unfinished.)


[[!redirects free colimit completion]]
[[!redirects free co-completion]]