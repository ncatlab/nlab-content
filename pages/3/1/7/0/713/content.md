
#Idea#

Passing from a [[category]] $C$ to its [[presheaf]] category $PSh(C) := [C^{op},Set]$ may be regarded as the operation of
"freely adjoining [[colimit]]s to $C$". 

The precise version of this statement is that the [[Yoneda embedding]]

$$
  Y : C \hookrightarrow PSh(C)
$$

is the **free cocompletion** of $C$.

The [[universal property]] of the [[Yoneda embedding]] is expressed in terms of the [[Yoneda extension]] of any [[functor]] $F : C \to D$ to a category $D$ with colimits.


# Technical details #


The [[Yoneda embedding]]
$$y_S: S \to Set^{S^{op}}$$ 
of a [[small category]] $S$ into the category $Set^{S^{op}}$ of [[presheaf|presheaves]] on $S$ 
is universal among functors from $S$ into (small) [[cocomplete category|cocomplete categories]], in the sense that given a functor $F: S \to D$ where $D$ is cocomplete, there exists a unique (up to isomorphism) [[cocontinuous functor|cocontinuous]] extension 
$$\hat{F}: Set^{S^{op}} \to D,$$
called the [[Yoneda extension]],
meaning that $\hat{F} y_S \cong F$ and $\hat{F}$ preserves small colimits. Indeed, the desired $\hat{F}$ is [[adjoint functor|left adjoint]] to the functor 
$$D \to Set^{S^{op}}: d \mapsto \hom_D(F-, d)$$ 

An explicit formula for the left adjoint is given by the [[weighted colimit]] or [[end|coend]] formula 
$$\hat{F}(X) = X \otimes_S F = \int^{s: S} X(s) \cdot F(s)$$ 
where $S \cdot d$ is notation for [[power|copowering]] (or tensoring) an object $d$ of $D$ by a set $S$ (in this case, a coproduct of an $S$-indexed set of copies of $D$). This formula recurs frequently throughout this wiki; see also [[nerve]], [[Day convolution]]. 

This "free cocompletion" property generalizes to [[enriched category]] theory. If $V$ is complete, cocomplete, symmetric monoidal closed, and $S$ is (small) enriched in $V$, then the enriched presheaf category $V^{S^{op}}$ is a free $V$-cocompletion of $S$. The explicit meaning is analogous to the case where $V = Set$, where all ordinary category concepts are replaced by their $V$-enriched analogues; in particular, the notion of "$V$-cocontinuous functor" referes to preservation of enriched weighted colimits (not just ordinary conical colimits). 


# Gentle explanation #

This section is a slightly new sort of experiment.
Here [[John Baez]] would like to explain this remark to [[Mike Stay]]:


+-- {: .standout}

In the case where $C = Set$ and $S$ is [[small category|small]], an important general principle is that the [[category]] of $C$-valued [[presheaf|presheaves]] on $S$ and [[natural transformation|natural transformations]] between them is the [[free cocompletion]] of $S$.

=--

The idea is that I'll write some stuff, then Mike will write some questions, and so on.  Other people are welcome to join, but only if they _keep it simple_.  Please: _no showing off!_  In particular, Mike does not yet understand coends or Kan extensions, so part of my job is to explain these, not just use them.

First, let me state the above result precisely.

Given a [[small category]] $A$, let $\hat{A}$ be our short name for $Set^{A^{op}}$, the category of presheaves on $A$ and natural transformations between them.

The [[Yoneda lemma]] gives an embedding $Y : A \to \hat{A}$ -- the [[Yoneda embedding]].

The result says: 

+-- {: .un_theorem}
###### Theorem

Given any [[small category|small]] [[cocomplete category]] $B$, and any functor $F : A \to B$, there is a [[cocontinuous functor]] $\widehat{F} : \hat{A} \to B$ making this triangle commute up to natural isomorphism:

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


Our job is to understand how to construct this $\widehat{F}$.  

But before we do that:

##Why do we care?##

There are many reasons why this theorem is important.  Mike Stay needs it to convert between two equivalent descriptions of [[profunctors]] from a category $A$ to a category $B$.  On the one hand, we can think of them as [[functor|functors]]

$$ G : A \to \widehat{B}$$

On the other hand, we can think of them as [[cocontinuous functor|cocontinuous functors]]

$$ \widehat{G} : \widehat{A} \to \widehat{B} $$

Getting from $G$ to $\widehat{G}$ here is a special case of the above Theorem.  Getting from $\widehat{G}$ to $G$ is vastly easier, so I'll leave that as a little exercise:

**Exercise.**  Given a cocontinuous functor $\widehat{A} \to \widehat{B}$, explain how to get a functor $A \to \widehat{B}$.

[[Mike Stay]]: Precompose with $Y$.

[[John Baez]]: Right.  So, going <i>back</i> --- the <i>hard part</i>, which is what the Theorem lets us do --- 
is a bit like trying to find an 'inverse' to precomposition with $Y$.  And that's exactly what [[Kan extension|Kan extensions]] are all about.  So the theorem asserts that a certain Kan extension exists.  

But don't worry: I'm only mentioning this to intimidate you... err, I mean: to start getting you used to Kan extensions.  They're 'best possible approximations to the perhaps impossible task of finding an inverse to precomposition with a functor'.   But never mind!

[[Mike Stay]]: So the real content of the Theorem is saying that there's always a "best" one; I can imagine that in other situations, you might have a bunch of inequivalent approximations, none of which is better than all the others, and would need to make an arbitrary choice.

[[John Baez]]:  Yeah, for starters.  However, I must admit: the Theorem actually says a lot _more_ than the existence of a certain Kan extension.  A Kan extension would merely 'do its best' to make a triangle commute up to natural isomorphism.  In this particular case it actually _succeeds!_   But never mind!  I'm just trying to sneak certain ideas into your brain, so they'll quietly take root: I don't want to actually talk about them yet.

Now, try these exercises:

**Exercise.**  Using the Theorem, show that going from 
a functor $A \to \widehat{B}$ to a cocontinuous functor
$\widehat{A} \to \widehat{B}$ and then precomposing with $Y$ to get a functor $A \to \widehat{B}$ gets you back where you started---at least up to natural isomorphism.  

[[Mike Stay]]: Well, given any functor $F:A \to \widehat{B}$, you get from the Theorem a cocontinuous functor $\widehat{F}:\widehat{A} \to \widehat{B}$ such that $\widehat{F} \circ Y$ is naturally isomorphic to $F$.

[[John Baez]]: Right, so we're back where we started, at least up to natural isomorphism.

**Exercise.** 
Also show that going from a cocontinuous functor $\widehat{A} \to \widehat{B}$ to a functor $A \to \widehat{B}$ and then using the Theorem to turn that back into a cocontinuous functor $\widehat{A} \to \widehat{B}$ 
gets you back where you started---at least up to natural isomorphism.

[[Mike Stay]]: Call our given functor $\widehat{F}: \widehat{A} \to \widehat{B}$.  Precompose with $Y$ to get $\widehat{F} \circ Y: A \to \widehat{B}$.  Then the theorem gives us a cocontinuous functor $G: \widehat{A} \to \widehat{B}$ such that $G \circ Y$ is the best approximation to $\widehat{F} \circ Y$.  But this is $\widehat{F}$ itself--at least up to natural isomorphism.

[[John Baez]]:  I don't think that's a proof.  First, I find the hand-waving about 'best approximations' a bit distracting---that's the kind of talk we use in explaining stuff, not proving stuff.  And it's not good to call the functor we start with $\widehat{F}$, since it's just any cocontinuous functor that someone handed us, not one we got from the Theorem.   If we fix these problems, we get something like this:  

Start with any cocontinuous functor $G: \widehat{A} \to \widehat{B}$.  Precompose with $Y$ to get $G \circ Y: A \to \widehat{B}$.  Then go back using the Theorem, obtaining a cocontinuous functor $\widehat{G}: \widehat{A} \to \widehat{B}$ such that $\widehat{G} \circ Y$ is naturally isomorphic to $G \circ Y$.  We need to show that we got back where we started, up to natural isomorphism.  So, we need to show that $\widehat{G}$ is natural isomorphic to $G$.  What next?

(Hint: don't be afraid to get stuck and realize that you could get out of being stuck if you knew a certain Lemma which might also be useful for other things we're talking about below.)

[[Mike Stay]]: Well, we need to show that $G \circ Y \cong \widehat{G} \circ Y \Rightarrow G \cong \widehat{G}$; is $Y$ an epimorphism?

[[John Baez]]: That would suffice, but it's radically overoptimistic.  

Consider the second decategorified analogue below, where $y: A \to \widetilde{A}$ is the inclusion of a set in the vector space having that set as a basis.  Is this $y$ an epimorphism?  In other words: is it onto?   _No!_   The vector space $\widetilde{A}$ is vastly larger than $A$.

What does this mean?  It means: it's _not true_ that given any vector space $B$ and function $F : A \to B$, there is a unique _function_ $\tilde{F} : \tilde{A} \to B$ making this triangle commute:
$$
  \array{
     A &\stackrel{F}{\to}& B
     \\
     \downarrow^y & \nearrow_{\tilde{F}}
     \\
     \tilde{A}
  }
$$
But this is okay: we don't want a unique _function_ $\tilde{F}$ making this diagram commute: we want a unique _linear function_ making it commute.  And that's obviously true.

Having gained some intuition from the decategorified analogue, let's go back to the situation we're really interested in.  If $A$ is the category with one object and one morphism, $\widehat{A}$ is vastly larger than $A$: it's the category $\Set$.  So, the Yoneda embedding $Y : A \to \widetilde{A}$ is far from being onto in any sense.  

In particular, it's _not true_ that given any cocomplete $B$ and functor $F : A \to B$, there is an essentially unique _functor_ $\widehat{F} : \widehat{A} \to B$ making this triangle commute:
$$
  \array{
     A &\stackrel{F}{\to}& B
     \\
     \downarrow^Y & \nearrow_{\widehat{F}}
     \\
     \widehat{A}
  }
$$
But this is okay: we don't want a unique _functor_ $\widehat{F}$ making this diagram commute: we want a unique _cocontinuous functor_ making it commute.

And this too should be obviously true, once we know what's going on.  What lemma would help?

##How should we think about this, intuitively?##
  
When we say $\widehat{A}$ is the 'free cocompletion' of the category $A$, it means we're freely throwing in [[colimit]]s (and thus wrecking the old colimits $A$ may have had).  Since colimits are generalized 'sums', we can consider a [[decategorification|decategorified]] analogue:

**Decategorified Theorem.** Given any set $A$, let $\tilde{A}$ be the free commutative monoid on $A$, and let $y : A \to \tilde{A}$ be the obvious inclusion.  If $B$ is a commutative monoid, given any function $F : A \to B$, there is a monoid homomorphism $\tilde{F} : \tilde{A} \to B$ making this triangle commute:
$$
  \array{
     A &\stackrel{F}{\to}& B
     \\
     \downarrow^y & \nearrow_{\tilde{F}}
     \\
     \tilde{A}
  }
  
$$

**Proof.** The proof here is easy.   Elements of $\tilde{A}$ are formal sums of elements of $A$, like

$$ x = \sum a_i $$

So, $\tilde{F}$ is determined by the fact that it preserves addition and acts like $F$ on guys in $A$:

$$\tilde{F}(x) = \tilde{F} (\sum a_i) =
\sum \tilde{F}(a_i) = \sum F(a_i)  $$

Lo and behold --- now we have a _formula_ for $\tilde{F}$.  So, we just need to check some stuff.  Check that $\tilde{F}$ is well-defined.  Check that it's a monoid homomorphism.  Check that it makes the diagram commute.  Check that it's unique.  All this is follow-your-nose stuff.

[[David Corfield]]: In the above Decategorified Theorem, shouldn't you say commutative monoid $A$, and then $\tilde{A}$ is the free commutative monoid on the underlying set of $A$? 

[[John Baez]]: No!  We're taking a set $A$ and freely throwing in sums to get the commutative monoid $\tilde{A}$.  This is like taking a category $A$ and freely throwing in colimits to get the cocomplete category $\widehat{A}$.   See?  There may be other fun things to do when our set was _already_ a commutative monoid, but they're not relevant to the analogy here.

[[David Corfield]]: Oh I see. Though I wonder if prettier category theory would have you talk about the underlying sets of $\tilde{A}$ and $B$, and of commutative monoid morphism.

[[John Baez]]: You're right: in some gold-plated treatment it would be good to carefully distinguish between commutative monoids and their underlying categories, or cocomplete categories and their underlying categories.  That would be especially nice if we wanted to see 'free commutative monoid' or 'free cocompletion' as some sort of [[monad]].  But let's prove the Theorem first and gold-plate it later, in the section below called **Free cocompletion as a pseudomonad**.

##But really: why should we care?##

[[Eric]]: Will this Theorem also help us understand [[An Exercise in Kantization]]?

[[John Baez]]:  I don't know and I don't really care.  I certainly don't want to talk about that stuff here!  But if you need to understand left Kan extensions or coends, you should find this Theorem good practice. 

[[Urs Schreiber]]: At least the [[Yoneda extension]] that is being discussed here is a special case of a left [[Kan extension]].

[[John Baez]]: Okay, so maybe this class will help Eric.  But if Eric is the sort of guy who likes vector spaces better than commutative monoids, he may prefer to understand the Theorem as a souped-up analogue of _this_:

**Decategorified Theorem.** Given any set $A$, let $\tilde{A}$ be the vector space with elements of $A$ as its basis, and let $y : A \to \tilde{A}$ be the obvious inclusion.  If $B$ is a vector space, given any function $F : A \to B$, there is a linear operator $\tilde{F} : \tilde{A} \to B$ making this triangle commute:
$$
  \array{
     A &\stackrel{F}{\to}& B
     \\
     \downarrow^y & \nearrow_{\tilde{F}}
     \\
     \tilde{A}
  }
  
$$

**Proof.** The proof here is easy.   Elements of $\tilde{A}$ are linear combinations of elements of $A$, like

$$ x = \sum c_i a_i $$

with some coefficients $c_i$.  So, $\tilde{F}$ is determined by the fact that it's linear and acts like $F$ on guys in $A$:

$$\tilde{F}(x) = \tilde{F} (\sum c_i a_i) =
\sum c_i \tilde{F}(a_i) = \sum c_i F(a_i)  $$

Lo and behold --- now we have a _formula_ for $\tilde{F}$.  So, we just need to check some stuff.  Check that $\tilde{F}$ is well-defined.  Check that it's linear.  Check that it makes the diagram commute.  Check that it's unique.  All this is follow-your-nose stuff.

[[Eric]]: Maybe this is _too_ pedestrian, but if we assume $A$ is finite and $B$ is finite dimensional, we can do this with matrices. Given $a_i\in A$, we have

$$y(a_i) = \sum_j y_{ij} a_j\quad\text{and}\quad\tilde{F}\circ y(a_i) = \sum_i y_{ij} \tilde{F}(a_j) = \sum_{j,k} y_{ij} \tilde{F}_{jk} b_k.$$

Also,

$$F(a_i) = \sum_k F_{ik} b_k.$$

If the triangle commutes, we have

$$F_{ik} = \sum_j y_{ij} \tilde{F}_{jk}.$$

Therefore, we can determine $\tilde{F}$ as long a $y$ has a right inverse (which the obvious inclusion does). In hindsight, it is obvious. If $\tilde{F}\circ y = F\implies \tilde{F} = F\circ y^{-1}$.

[[John Baez]]: This is a slightly bizarre argument, but it can probably be rescued.  $F$ is not a linear operator: it's just a function from a set $A$ to a vector space $B$.  So, it's slightly bizarre to write down a _matrix_ for $F$ as you do above!  Nonetheless, if you think it about it, there's a perfectly sensible way to use a matrix to describe a function from a set to a vector space with a chosen basis.  And what the theorem is doing is using this matrix to define the linear operator $\tilde{F}$ from $\tilde{A}$ to $B$.

[[Eric]]: Bizarre?? But this is exactly the way I meant it.

[[John Baez]]: Okay, but you didn't explain yourself: you just introduced this matrix $F_{ij}$ without saying what it was, leaving us to guess that you'd invented a new idea: using a matrix to describe a map from a set to a vector space.  To add to the fun, you also introduced _another_ matrix $\tilde{F}_{ij}$ which happens to be precisely _equal_ to $F_{ij}$, but _means something different_.  But all's well that ends well: I eventually guessed what you meant, and now everything is hunky-dory.  

And indeed, all these ideas have nice analogues in the categorified version---the Theorem I'm struggling to get Mike to understand!  If we live long enough, we'll see that [[profunctors]] are categorified matrices.  But maybe we should just prove the Theorem and then ponder the analogies further.   So....

##Proving the theorem##

Okay, now let's stop fiddling around and try to prove the bloody Theorem:

+-- {: .un_theorem}
###### Theorem

Given any [[small category|small]] [[cocomplete category]] $B$, and any functor $F : A \to B$, there is a [[cocontinuous functor]] $\widehat{F} : \hat{A} \to B$ making this triangle commute up to natural isomorphism:

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

There are probably lots of ways to prove it, but let's take a simple-minded approach that mimics the obvious proof of the Decategorified Theorem.  We proved the Decategorified Theorem by finding a formula for the map we needed.  So
let's try to write a _formula_ for $\widehat{F}$, based on three ideas:

1. Since the triangle commutes, we know what $\widehat{F}$ should do to guys in the image of $Y$.  Namely:
$$\widehat{F}(Y(x)) = F(x)$$
(The triangle could just commute up to natural isomorphism, but let's not worry about that yet --- that's just a nuance.)
1. We know that $\widehat{F}$ preserves colimits.
1. We know that every object in $\widehat{A}$ is a colimit of guys in the image of $Y$.  (Such guys are called [[representable functor|representable]].)

Maybe you don't actually _know_ fact 3, but it's true.  If you don't know why, don't worry --- you'll soon find out!

These three facts are already enough to determine $\widehat{F}$ on objects.   

**Exercise:** Why?

So $\widehat{F}$ is well on its way to being unique. 

But why does $\widehat{F}$ exist?  For this it will really be good to have a _formula_ expressing every object in $\widehat{A}$ as a colimit of guys in the image of $Y$.  As a side-effect this will prove fact 3.  But even better: thanks to fact 2, this formula will yield a formula for $\widehat{F}$.  And a formula is the best way to prove existence.

[[Mike Stay]] Given categories $A, B$ and a profunctor $F: A \to B$, the fact that all objects in $B$ can be written as a sum over representables says

$$\array{F:A  &\to& \hat{B}\\ a &\mapsto& \int_{b \in B} F(a)(b) \; \times \; hom(-, b)}$$

In a similar way, the Yoneda embedding says

$$\array{Y:A &\to& \hat{A}\\ a &\mapsto& \int_{a' \in A} Y(a)(a') \times hom(-, a')\\&&= \int_{a' \in A} hom(a', a) \times hom(-, a')\\&&= hom(-, a)}$$

That is, the set of morphisms from $-$ to $a$ is the set of morphisms from $-$ to an intermediate object $a'$ times the morphisms from $a'$ to $a$, where $a'$ ranges over all possible objects in $A$.

Doing the same for an arbitrary cocontinuous functor $G:\hat{A} \to \hat{B}$ says

$$c = \int_{a \in A} c(a) \times hom(-, a)$$

maps to

$$G(x) = \int_{a \in A} \int_{b \in B} G(a)(b) \times hom(a, b) ) \times c(a) \times hom(-, a)$$

which simplifies to

$$G(x) = \int_{b \in B} \int_{a \in A} G(a)(b) \times c(a) \times hom(-, b)$$

by taking $a$ as the midpoint between $-$ and $b$.  So $G$ is completely determined (up to isomorphism) by its values on the embedding of $A$.

This reference might also give helpful clues:

* Daniel Dugger, _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

A pedagogical explanation of the universal property of the [[Yoneda embedding]] is given starting on page 7.
On page 8 there's an explanation with lots of pictures how a presheaf is an "instruction for how to build a colimit".
Then on p. 9 the universal morphism that we are looking for here is identified as the one that "takes the instructions for building a colimit and actually _builds_ it".

(This text, by the way, contains various other gems. A pity that it is left unfinished.)

##Free cocompletion as a pseudomonad##

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
