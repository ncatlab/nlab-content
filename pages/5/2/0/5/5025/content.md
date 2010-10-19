
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contemts#
* table of contents
{:toc}

## Idea

A [[Lie groupoid]] is said to be _effective_ if its morphisms act locally freely, in a sense.

Beware that this use of the term is entirely independent of "effective" in the sense of Giraud's axuioms, as discussed are [[groupoid object in an (infinity,1)-category]].

## Definition

Given a [[Lie groupoid]] $X$ a [[morphism]] $f : x \to y$ induces a [[germ]] of a local [[diffeomorphism]] $\tilde f : (X_0,x) \to (X_0,y)$: for that choose $U \subset X_0$ to be any [[neighbourhood]] of $x$ small enough such that the restricted source and target maps 

$$
  \array{
    X_1 \times_{X_0} U&\to& X_1
    \\
    {}^{\mathllap{s|_U, t|_U}}\downarrow && \downarrow^{\mathrlap{s,t}}
    \\
    U &\stackrel{}{\hookrightarrow} & X_0
  }
$$

are [[diffeomorphism]]s. Then define $\tilde f$ to be the germ $t \circ (s|_U)^{-1}$.

The Lie groupoid $X$ is called _effective_ if this assignment of morphisms to germs of local diffeomorphisms is [[injective]].

## References

* [[Ieke Moerdijk]], Janez Mr&#269;un _Introduction to Foliations and Lie Groupoids_ ,Cambridge Studies in Advanced Mathematics 91, Cambridge University Press, Cambridge, (2003)
