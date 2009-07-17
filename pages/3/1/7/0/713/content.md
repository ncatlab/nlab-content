
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

+--{.query}
[[Eric]]: Will this also help us understand [[An Exercise in Kantization]]?
=--

But before we do that:

####Why do we care?####

We want to convert between two equivalent descriptions of [[distributor|profunctors]] from a category $A$ to a category $B$.  On the one hand, we can think of them as [[functor|functors]]

$$ G : A \to \widehat{B}$$

On the other hand, we can think of them as [[cocontinuous functor|cocontinuous functors]]

$$ \widehat{G} : \widehat{A} \to \widehat{B} $$

Getting from $G$ to $\widehat{G}$ here is a special case of the above Theorem.  Getting from $\widehat{G}$ to $G$ is vastly easier, so I'll leave that as a little exercise:

**Exercise.**  Given a cocontinuous functor $\widehat{A} \to \widehat{B}$, explain how to get a functor $A \to \widehat{B}$.

[[Mike Stay]]: Precompose with $Y$.

[[John Baez]]: Right.  So, going <i>back</i> --- the <i>hard part</i>, which is what the Theorem lets us do --- 
is a bit like trying to find an 'inverse' to precomposition with $Y$.  And that's exactly what [[Kan extension|Kan extensions]] are all about.  So the theorem asserts that a certain Kan extension exists.  

But don't worry: I'm only mentioning this to intimidate you... err, I mean: to start getting you used to Kan extensions.  They're 'best possible approximations to the perhaps impossible task of finding an inverse to precomposition with a functor'.   But never mind!

Now, try this exercise:

**Exercise.**  Using the Theorem, show that going from 
a functor $A \to \widehat{B}$ to a cocontinuous functor
$\widehat{A} \to \widehat{B}$ gets you back where you started---at least up to natural isomorphism.  Also show that going from a cocontinuous functor
$\widehat{A} \to \widehat{B}$ to a functor $A \to \widehat{B}$ gets you back where you started---at least up to natural isomorphism.

I don't think it requires any special knowledge to do it.   I could be wrong, but I have a feeling that the answer, or at least part of it, just writes itself.  You write down what you want, and what the Theorem says you know...

####How should we think about this, intuitively?####
  
When we say $\widehat{A}$ is the 'free cocompletion' of the category $A$, it means we're freely throwing in [[colimit]]s (and thus wrecking the old colimits $A$ may have had).  Since colimits are generalized 'sums', we can consider a [[decategorification|decategorified]] analogue:

**Decategorified Theorem.** Given any set $A$, let $\tilde{A}$ be the free commutative monoid on $A$, and let $y : A \to \tilde{A}$ be the obvious inclusion.  If $B$ is a commutative monoid, given any function $F : A \to B$, there is a monoid homomorphism $\tilde{F} : \hat{A} \to B$ making this triangle commute:
$$
  \array{
     A &\stackrel{F}{\to}& B
     \\
     \downarrow^y & \nearrow_{\tilde{F}}
     \\
     \tilde{A}
  }
  
$$
Moreover, $\tilde{F}$ is unique up to natural isomorphism.

**Proof.** The proof here is easy.   Elements of $\tilde{A}$ are formal sums of elements of $A$, like

$$ x = \sum a_i $$

So, $\tilde{F}$ is determined by the fact that it preserves addition and acts like $F$ on guys in $A$:

$$\tilde{F}(x) = \tilde{F} (\sum a_i) =
\sum \tilde{F}(a_i) = \sum F(a_i)  $$

Lo and behold --- now we have a _formula_ for $\tilde{F}$.  So, we just need to check some stuff.  Check that $\tilde{F}$ is well-defined.  Check that it's a monoid homomorphism.  Check that it makes the diagram commute.  Check that it's unique.  All this is follow-your-nose stuff.

[[David Corfield]]: In the above Decategorified Theorem, shouldn't you say commutative monoid $A$, and then $\tilde{A}$ is the free commutative monoid on the underlying set of $A$? 

[[John Baez]]: No!  We're taking a set $A$ and freely throwing in sums to get the commutative monoid $\tilde{A}$.  This is like taking a category $A$ and freely throwing in colimits to get the cocomplete category $\widehat{A}$.   See?  There may be other fun things to do when our set was _already_ a commutative monoid, but they're not relevant to the analogy here.

[[David Corfield]]: Oh I see. Though I wonder if prettier category theory would have you talk about the underlying sets of $\tilde{A}$ and $B$, and of commutative monoid morphism.

####Back to proving the theorem###

Okay, now let's try to prove the actual Theorem:

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

Maybe you don't actually _know_ fact 3, but it's true.  If you don't know why, it's about time to find out!

These three facts are already enough to determine $\widehat{F}$ on objects.   Do you see why?

So $\widehat{F}$ is unique. 

But why does $\widehat{F}$ exist?  For this it will really be good to have a _formula_ expressing every object in $\widehat{A}$ as a colimit of guys in the image of $Y$.  As a side-effect this will prove fact 3.  But even better: thanks to fact 2, this formula will yield a formula for $\widehat{F}$.  And a formula is the best way to prove existence.

Get the plan?  If not, ask questions.  If so, try this:

**Exercise.**  Look at the page on [[presheaf|presheaves]].  Find a 
formula expressing every object in $\widehat{A}$ as a colimit of guys in the image of $Y$.  Copy that formula here.

This reference might also give helpful clues:

* Daniel Dugger, _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html))

A pedagogical explanation of the universal property of the [[Yoneda embedding]] is given starting on page 7.
On page 8 there's an explanation with lots of pictures how a presheaf is an "instruction for how to build a colimit".
Then on p. 9 the universal morphism that we are looking for here is identified as the one that "takes the instructions for building a colimit and actually _builds_ it".

(This text, by the way, contains various other gems. A pity that it is left unfinished.)