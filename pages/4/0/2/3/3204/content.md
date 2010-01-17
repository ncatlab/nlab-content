# Infinitesimal numbers
* table of contents
{: toc}


## Idea

The term 'infinitesimal' means the same as 'infinitely small in absolute value'; in Latin, it literally means 'infinity-eth' and should be interpreted in the sense of a fraction.  In the ordinary [[analysis]] of [[real numbers]], the only infinitesimal number is [[zero]].  However, the basic intuitions of calculus since its beginnings have dealt with infinitely small (and sometimes also infinitely large) numbers.  There are several different ways to develop a rigorous theory that includes infinitesimal numbers.


## Definition

Briefly we recall the definition of what makes a number infinitesimal, which we give in some generality.

Let $P$ be a [[rig]] equipped with a [[partial order]] such that $0 \leq x$ holds for every element $x$ of $R$; that is, the additive [[identity]] is a [[bottom element]].  Let $R$ be a rig equipped with a function ${|\cdot|}\colon R \to P$, thought of as a measure of [[absolute value]], such that ${|0|} = 0$.  For example, $R$ could consist of the [[real numbers]] with $P$ the nonnegative real numbers; similarly, we may consider the [[natural numbers]], the [[complex numbers]], the [[cardinal numbers]], and many other familiar examples of numbers.  (In these examples, $\leq$ and ${|\cdot|}$ satisfy additional compatibility properties with respect to the rigs $R$ and $P$, but these do not seem to enter into the definition.  Conversely, we do not use the full rig structures of $R$ and $P$, so the definition should work in even greater generality.)

An element $x$ of $R$ is __infinitesimal__ if ${|n i|} \leq 1$ for every [[natural number]] $n$.  (Recall that every natural number, including $1$, may be interpreted as an element of any given rig, since $\mathbb{N}$ is the [[initial object|initial]] rig.  Multiplication by natural numbers is always commutative, so there is no need to distinguish between left and right infinitesimals.)

According to this definition, $0$ is always infinitesimal.  Traditionally, one adds to the definition the requirement that $i \neq 0$, but this leads to a less useful notion of the space of all infinitesimals.  We allow $0$ to be infinitesimal for some of the same reasons that we allow it to be a [[natural number]].  (Although the argument is even stronger here, since it's always [[decidable set|decidable]] whether a given natural number is zero, but it may not be decidable whether a given infinitesimal is zero.  This is especially important in [[synthetic differential geometry]], where the logic is unavoidably [[constructive mathematics|constructive]].)

In the usual systems of numbers (real, natural, complex, cardinal, etc), $0$ is the *only* infinitesimal number.  So the interesting question is how to get other infinitesimals.


## Free infinitesimals

The simplest way to add an infinitesimal to an [[ordered ring]] (or rig) is [[free object|freely]].  For example, if we start with the field $\mathbb{R}$ of real numbers, then form the [[polynomial ring]] $\mathbb{R}[x]$, we may make $x$ (and every nonconstant polynomial) infinitesimal by defining $x \leq c$ for every positive real number $c$ and generating the rest of $\leq$ by requiring that $\mathbb{R}[x]$ be an ordered ring.  (This amounts to defining $f \leq g$ to mean that $f(x) \leq g(x)$ for sufficiently small positive values of $x$.)

If you want a [[field]], then form the [[field of fractions]] $\mathbb{R}(x)$ of $\mathbb{R}[x]$, which is the field of [[rational function]]s.  This is a very commonly known example, although it is more usual to make $x$ infinitely large (so that $1/x$ is infinitesimal).

Similarly, one can use polynomials to define infinitesimal versions of complex numbers, cardinal numbers, etc.

The downside of this approach is that the resulting infinitesimal numbers will be subject only to those operations that apply to the category in which one forms the free construction.  For example, there is no way to apply transcendental functions to infinitesimals with this approach.  Presumably that could be fixed by working with $C^\infty$-[[C-infinity-ring|rings]], but no algebraic theory covers everything that can be done with real numbers (or whatever numbers you start with).


## Nonstandard analysis

If the point is to do with infinitesimal numbers everything that we can do with ordinary numbers, then why not use high-powered [[logic]] to do this for us?  That is the approach taken by [[Abraham Robinson]] in [[nonstandard analysis]].

Nonstandard analysis can be applied to [[mathematics]] as a whole, so it treats complex numbers, cardinal numbers, and the rest all together.

...


## Smooth toposes

Another approach is to focus only on what we want to do with infinitesimals in a particular field.  Since infinitesimals were used to do calculus, then let\'s just do calculus.  We can take as axiomatic the familiar properties of [[smooth map|smooth functions]] used in calculus, including the ways these were applied to infinitesimals before analysis was made rigorous (by modern standards) in the 19th century.  This is the approach taken by [[Bill Lawvere]] and others in [[synthetic differential geometry]].

...


## Other approaches

The [[surreal number]]s have infinitesimals, and include both the real numbers and the [[ordinal numbers]].  But they are not much good for ordinary calculus, although there are some indications that they might have applications in asymptotics.

There is also an interpretation of pre-Cauchy calculus in which infinitesimals are interpreted as [[infinite sequences]] that converge to $0$.  I don\'t know much about this.


## Comparisons

### Invertible infinitesimals in NSA and SDG {#NSAvsSDG}

All the infinitesimals appearing in nonstandard analysis are *invertible*, since the [[hyperreal numbers]] form a [[field]].  (This is also true for all the surreal infinitesimals.)  By contrast, most of the infinitesimals appearing in synthetic differential geometry are [[nilpotent]], and hence not invertible.  However, there are some models that do contain invertible infinitesimals, and hence also 'infinite' numbers as their inverses (see [[smooth natural number]]).  Two such models are the [[smooth topos]]es called $\mathcal{Z}$ and $\mathcal{B}$ in

* [[Ieke Moerdijk]] and [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_

These toposes are related to the smooth topos called $\mathcal{G}$ there, which has nilpotent but no invertible infinitesimals, by a transfer theorem (chapter VII, section 4) valid for a certain class of [[coherent formula]]s.  Additionally, the 'object of nonstandard smooth natural numbers' in these toposes is defined by an 'algebra of unbounded sequences', similar in spirit to the unbounded sequences which represent infinitely large numbers in nonstandard analysis.  However, it is not clear whether any more precise comparison can be made.


## References

*  article in the [English Wikipedia](http://en.wikipedia.org/wiki/Infinitesimal) for etymology


[[!redirects infinitesimal]]
[[!redirects notions of infinitesimals]]
[[!redirects infinitesimals]]
[[!redirects infinitesimal numbers]]
