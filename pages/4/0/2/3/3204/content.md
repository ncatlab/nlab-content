# Infinitesimal numbers
* table of contents
{: toc}


## Idea

The term 'infinitesimal' means the same as 'infinitely small in absolute value'; in Latin, it literally means 'infinity-eth' and should be interpreted in the sense of a fraction.  In the ordinary [[analysis]] of [[real numbers]], the only infinitesimal number is [[zero]].  However, the basic intuitions of calculus since its beginnings have dealt with infinitely small (and sometimes also infinitely large) numbers.  There are several different ways to develop a rigorous theory that includes infinitesimal numbers.


## Definition

Briefly we recall the definition of what makes a number infinitesimal, which we give in some generality.

Let $P$ be a [[rig]] equipped with a [[partial order]] such that $0 \leq x$ holds for every element $x$ of $R$; that is, the additive [[identity]] is a [[bottom element]].  Let $R$ be a rig equipped with a function ${|\cdot|}\colon R \to P$, thought of as a measure of [[absolute value]], such that ${|0|} = 0$.  For example, $R$ could consist of the [[real numbers]] with $P$ the nonnegative real numbers; similarly, we may consider the [[natural numbers]], the [[complex numbers]], the [[cardinal numbers]], and many other familiar examples of numbers.  (In these examples, $\leq$ and ${|\cdot|}$ satisfy additional compatibility properties with respect to the rigs $R$ and $P$, but these do not seem to enter into the definition.  Conversely, we do not use the full rig structures of $R$ and $P$, so the definition should work in even greater generality.)

An element $x$ of $R$ is __infinitesimal__ if ${|n i|} \leq 1$.  (Recall that every natural number, including $1$, may be interpreted as an element of any given rig, since $\mathbb{N}$ is the [[initial object|initial]] rig.  Multiplication by natural numbers is always commutative, so there is no need to distinguish between left and right infinitesimals.)

According to this definition, $0$ is always infinitesimal.  Traditionally, one adds to the definition the requirement that $i \neq 0$, but this leads to a less useful notion of the space of all infinitesimals.  We allow $0$ to be infinitesimal for much the same reasons that we allow it to be a [[natural number]].

In the usual systems of numbers (real, natural, complex, cardinal, etc), $0$ is the *only* infinitesimal number.  So the interesting question is how to get other infinitesimals.


## References

*  article in the [English Wikipedia](http://en.wikipedia.org/wiki/Infinitesimal) for etymology


[[!redirects infinitesimal]]
[[!redirects notions of infinitesimals]]