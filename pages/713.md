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

#Discussion about 'free cocompletion'#

This section is a slightly new sort of experiment.
Here [[John Baez]] would like to explain this remark to [[Mike Stay]]:

"In the case where $C = Set$ and $S$ is [[small category|small]], an important general principle is that the category of presheaves on $S$ and [[natural transformation|natural transformations]] between them is the [[free cocompletion]] of $S$."

The idea is that I'll write some stuff, then Mike will write some questions, and so on.  Other people are welcome to join but only if they _keep it simple_.  Please: _no showing off!_  In particular, Mike does not yet understand coends or Kan extensions, so part of my job is to explain these, not just use them.

First, let me state the above result precisely.

Given a small category $A$, let $\hat{A}$ be our short name for $Set^{A^{op}}$, the category of presheaves on $A$ and natural transformations between them.

The [[Yoneda lemma]] gives an embedding $Y : A \to \hat{A}$.

The result says: 

**Theorem.** Given any small [[cocomplete category]] $B$, and any functor $F : A \to B$, there is a [[cocontinuous functor]] $\widehat{F} : \hat{A} \to B$ making this triangle commute up to natural isomorphism:
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

Our job is to understand how to construct this $\widehat{F}$.  But before we do that:

####Why do we care?####

We want to convert between two equivalent descriptions of profunctors from a category $A$ to a category $B$.  On the one hand, they are functors

$$ G : A \to \widehat{B}$$

On the other hand, they are cocontinuous functors

$$ \widehat{G} : \widehat{A} \to \widehat{B} $$

Getting from $G$ to $\widehat{G}$ here is a special case of the above Theorem.  Getting from $\widehat{G}$ to $G$ is vastly easier, so I'll leave that as a little exercise:

**Exercise.**  Given a cocontinuous functor $\widehat{A} \to \widehat{B}$, explain how to get a functor $A \to \widehat{B}$.

[[Mike Stay]]: Precompose with Y.

**Exercise.**  Using the Theorem, show that going from 
a functor $A \to \widehat{B}$ to a cocontinuous functor
$\widehat{A} \to \widehat{B}$ gets you back where you started---at least up to natural isomorphism.  Also show that going from a cocontinuous functor
$\widehat{A} \to \widehat{B}$ to a functor $A \to \widehat{B}$ gets you back where you started---at least up to natural isomorphism.

####How should we think about this, intuitively?####
  
When we say $\widehat{A}$ is the 'free cocompletion' of the category $A$, it means we're freely throwing in colimits (and thus wrecking the old colimits $A$ may have had).  Since colimits are generalized 'sums', we can consider a decategorified analogue:

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

The proof here is easy: elements of $\tilde{A}$ are formal sums of elements of $A$.  So, we define $\tilde{F}$ of a formal sum of elements of $A$ by applying $F$ to each of those elements and then adding the results in $B$.  Check that $\tilde{F}$ is a monoid homomorphism.  Check that it makes the diagram commute.  Check that it's unique.

When colimits become as intuitive as sums, the Theorem should seem as intuitive as the Decategorified Theorem. 
But we also need to see how the Theorem is actually proved.

####A reference####

[[Urs Schreiber]]: By the way, there is a pretty good pedagogical and intuitive explanation of this from page 7 on of

* Daniel Dugger, _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html))

On page 8 this explains with lots of pictures how a presheaf is an "instruction for how to build a colimit".

Then on p. 9 the universal morphism that we are looking for here is identified as the one that "takes the instructions for building a colimit and actually _builds_ it".

(That text, by the way, contains various other gems. A pity that it is left unfinished.)