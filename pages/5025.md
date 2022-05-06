
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[Lie groupoid]] is said to be _effective_ if its morphisms act locally freely on [[germs]], in a sense.

(Beware that this use of the term is entirely independent of "effective" in the sense of [[Giraud theorem|Giraud's axioms]], as discussed are [[groupoid object in an (infinity,1)-category]].)

## Definition

Let $X_\bullet = (X_1 \stackrel{\longrightarrow}{\longrightarrow} Y)$ be a [[Lie groupoid]]. Equivalently, let $X$ be a [[differentiable stack]] equipped with an [[atlas]] $X_0 \to X$.

Then given any element $f$ in $X_1$, hence given a [[morphism]] $f \colon x \to y$, it induces a [[germ]] of a local [[diffeomorphism]] $\tilde f \colon (X_0,x) \to (X_0,y)$ as follows: 

choose $U_x \subset X_0$ to be any [[neighbourhood]] of $x$ small enough such that the restricted [[source]] and [[target]] maps 

$$
  \array{
    X_1 \times_{X_0} U_x &\to& X_1
    \\
    {}^{\mathllap{s|_U, t|_U}}\downarrow && \downarrow^{\mathrlap{s,t}}
    \\
    U_x &\stackrel{}{\hookrightarrow} & X_0
  }
$$

are [[diffeomorphisms]]. Then define $\tilde f$ to be the germ $t \circ (s|_U)^{-1}$.

+-- {: .num_defn #EffectiveLieGroupoid}
###### Definition

The Lie groupoid $X_\bullet$ is called _effective_ if this assignment of morphisms to germs of local diffeomorphisms is [[injective]].

Similarly a [[differentiable stack]] is called an _effective &#233;tale stack_ if it is represented by an effective &#233;tale Lie groupoid.

=--

This means that the [[action]] of the [[automorphism group]] at any point $x$ on the germ at $x$ is [[faithful action|faithful]]. 


## Properties

### Equivalent characterizations
 {#EquivalentCharacterizations}

+-- {: .num_prop }
###### Proposition

The following are equivalent

1. $X_\bullet$ is an effective Lie groupoid, def. \ref{EffectiveLieGroupoid};

1. the canonical smooth [[functor]] $X_\bullet \to \mathbb{H}(X_0)$ (see [here](etale+groupoid#RelationToHaefligerGroupoids)) to the [[Haefliger groupoid]] of the manifold of objects is [[faithful functor|faithful]], i.e. gives a [[representable morphism of stacks]];

1. under the equivalence ([here](etale+groupoid#CharacterizationBySiteOfManifolds)) between smooth étale stacks and stacks on the [[site]] $SmthMfd^{et}$ of smooth manifolds with [[local diffeomorphisms]] between them, $X$ corresponds to a [[sheaf]] (i.e. to a [[0-truncated]] stack) on $SmthMfd^{et}$.

=--

([Carchedi 12, theorem 4.1](#Carchedi12)).


## Related concepts

* [[proper Lie groupoid]], [[étale groupoid]]

## References

A standard textbook aacount is in

* [[Ieke Moerdijk]], Janez Mr&#269;un _Introduction to Foliations and Lie Groupoids_ ,Cambridge Studies in Advanced Mathematics 91, Cambridge University Press, Cambridge, (2003)

Brief survey is in 

* [[David Carchedi]], _A quick note on &#233;tale stacks_ ([pdf](http://people.mpim-bonn.mpg.de/carchedi/Etale_Stacks.pdf))

Discussion in a more general context of [[étale stacks]] is in

* {#Carchedi12} [[David Carchedi]], _&#201;tale Stacks as Prolongations_ ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))