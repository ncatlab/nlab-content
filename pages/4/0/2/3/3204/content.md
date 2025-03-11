# Infinitesimal numbers
* table of contents
{: toc}


## Idea

The term 'infinitesimal' means the same as 'infinitely small in absolute value'; in Latin, it literally means 'infinity-eth' and should be interpreted in the sense of a fraction.  In the ordinary [[analysis]] of [[real numbers]], the only infinitesimal number is [[zero]].  However, the basic intuitions of calculus since its beginnings have dealt with infinitely small (and sometimes also infinitely large) numbers.  There are several different ways to develop a rigorous theory that includes infinitesimal numbers.


## Definition

Briefly we recall the definition of what makes a number infinitesimal, which we give in some generality.

Let $P$ be a [[cancellative monoid|cancellative]] [[commutative monoid]] equipped with a [[strict weak order]] such that $x \lt 0$ does not hold for any element $x$ of $P$; that is, the additive [[identity]] is a [[bottom element]] with respect to the [[partial order]] induced by the [[negation]] of the strict weak order, and an element $1$ such that $0 \lt 1$. Let $M$ be a [[cancellative monoid|cancellative]] [[commutative monoid]] equipped with a function ${|\cdot|}\colon M \to P$, thought of as a measure of [[absolute value]], such that ${|0|} = 0$. For example, $M$ could consist of the [[real numbers]] with $P$ the nonnegative real numbers; similarly, we may consider the [[natural numbers]], the [[complex numbers]], the [[cardinal numbers]], and many other familiar examples of numbers. (In these examples, $\lt$ and ${|\cdot|}$ satisfy additional compatibility properties with respect to the cancellative commutative monoids $M$ and $P$, but these do not seem to enter into the definition. Conversely, we do not use the full cancellative commutative monoid structure of $M$ and $P$, so the definition should work in even greater generality.)

An element $x$ of $M$ is __infinitesimal__ if the sum of $n$ elements of $x$ has absolute value less than $1$: ${|\sum_{i = 1}^n x|} \lt 1$ for every [[natural number]] $n$. The sum of $n$ elements of an element in a cancellative commutative monoid $M$ always exists, since every monoid is power-associative. 

According to this definition, $0$ is always infinitesimal.  Traditionally, one adds to the definition the requirement that $i \neq 0$, but this leads to a less useful notion of the space of all infinitesimals.  We allow $0$ to be infinitesimal for some of the same reasons that we allow it to be a [[natural number]].  (Although the argument is even stronger here, since it's always [[decidable set|decidable]] whether a given natural number is zero, but it may not be decidable whether a given infinitesimal is zero.  This is especially important in [[synthetic differential geometry]], where the logic is unavoidably [[constructive mathematics|constructive]].)

In the usual systems of numbers (real, natural, complex, cardinal, etc), $0$ is the *only* infinitesimal number.  So the interesting question is how to get other infinitesimals.

## Free infinitesimals

The simplest way to add an infinitesimal to an [[ordered ring]] (or rig) is [[free object|freely]].  For example, if we start with the field $\mathbb{R}$ of real numbers, then form the [[polynomial ring]] $\mathbb{R}[x]$, we may make $x$ (and every nonconstant polynomial) infinitesimal by defining $x \lt c$ for every positive real number $c$ and generating the rest of $\lt$ by requiring that $\mathbb{R}[x]$ be an ordered ring.  (This amounts to defining $f \lt g$ to mean that $f(x) \lt g(x)$ for sufficiently small positive values of $x$.)

If you want a [[field]], then form the [[field of fractions]] $\mathbb{R}(x)$ of $\mathbb{R}[x]$, which is the field of [[rational function]]s.  This is a very commonly known example, although it is more usual to make $x$ infinitely large (so that $1/x$ is infinitesimal).

Similarly, one can use polynomials to define infinitesimal versions of complex numbers, cardinal numbers, etc.

The downside of this approach is that the resulting infinitesimal numbers will be subject only to those operations that apply to the category in which one forms the free construction.  For example, there is no way to apply transcendental functions to infinitesimals with this approach.  Presumably that could be fixed by working with $C^\infty$-[[C-infinity-ring|rings]], but no algebraic theory covers everything that can be done with real numbers (or whatever numbers you start with).

Alternatively, one could [[formally complete]] the [[polynomial ring]] $R[x]$ to get the ring of [[formal power series]] $R[[x]]$. This results in a [[local integral domain]] if $R$ is a [[field]]. In the case that $R$ is an [[Archimedean ordered field]], then $R[[x]]$ is an [[Archimedean ordered local integral domain]]; and if $R$ is [[sequentially Cauchy complete]], this allows for any [[analytic function]] to be defined on $R[[x]]$. The infinitesimals in $R[[x]]$ are the formal power series whose leading 0th-power term is equal to zero, or equivalently, the product of $x$ and a formal power series. 

## Nilpotent infinitesimals

Instead of working with free infinitesimals, we could also work with [[nilpotent]] infintiesimals. This requires working in an [[Archimedean ordered Artinian local algebra|Archimedean ordered Artinian local $\mathbb{R}$-algebras]]. Since these are not ordered fields, the [[strict weak order]] is not a [[strict total order]], the [[preorder]] is not a [[partial order]], and the [[apartness relation]] is not [[tight apartness relation|tight]]. There is an [[equivalence relation]] $a \approx b$ which says that $a$ is approximately equal to $b$, and is defined by $a \approx b$ if and only if the difference $a - b$ is a zero divisor. 

Given an Archimedean ordered Artinian local $\mathbb{R}$-algebra $A$, since $A$ is a [[local ring]], the quotient of $A$ by its [[ideal]] $D$ of non-invertible elements is the real numbers $\mathbb{R}$, and the canonical function used in defining the [[quotient ring]] is the function $\Re:A \to \mathbb{R}$ which takes a number $a \in A$ to its purely real component $\Re(a) \in \mathbb{R}$. Since $A$ is an ordered $\mathbb{R}$-algebra, there is a [[strictly monotone]] [[ring homomorphism]] $h:\mathbb{R} \to A$. A number $a \in A$ is **purely real** if $h(\Re(a)) = a$, and a number $a \in A$ is **purely infinitesimal** if it is in the ideal of zero divisors $D$, the [[fiber]] of $\Re$ at the real number $0$. Zero is the only number in $A$ which is both purely real and purely infinitesimal. 

The advantage of working with nilpotent infinitesimals is that the ring homomorphism $h:\mathbb{R} \to A$ preserves [[smooth functions]]: given a natural number $n \in \mathbb{N}$ and a purely infinitesimal number $\epsilon \in D$ such that $\epsilon^{n + 1} = 0$, then for every [[smooth function]] $f \in C^\omega(\mathbb{R})$, there is a function $f_A:A \to A$ such that for all real numbers $x \in \mathbb{R}$, $f_A(h(x)) = h(f(x))$ and 
$$f_A(h(x) + \epsilon) = \sum_{i = 0}^{n} \frac{1}{i!} h\left(\frac{d^i f}{d x^i}(x)\right) \epsilon^i$$ 

If we restrict to Archimedean ordered local Artinian $\mathbb{R}$-algebras $A$ where every element of the nilradical $D$ is a nilsquare element, where for all $\epsilon \in D$, $\epsilon^2 = 0$, then the ring homomorphism $h:\mathbb{R} \to A$ preserves [[differentiable functions]]; for every [[differentiable function]] $f:\mathbb{R} \to \mathbb{R}$, there is a function $f_A:A \to A$ such that for all real numbers $x \in \mathbb{R}$ and nilpotent elements $\epsilon \in D$, $f_A(h(x)) = h(f(x))$ and 
$$f_A(h(x) + \epsilon) = h(f(x)) + h\left(\frac{d f}{d x}(x)\right) \epsilon$$ 

This allows us to define certain differentiable functions on the [[real numbers]], such as the [[exponential function]], the [[sine function]], and the [[cosine function]], through its property as solutions to systems of first-order [[ordinary differential equations]], without having to define the notion of [[limit of a sequence]], [[series]], [[integral]], and prove the [[fundamental theorem of calculus]] and/or [[convergence]] of [[Taylor series]]. 

One could also work with partial functions instead of functions. Given a predicate $P$ on the real numbers $\mathbb{R}$, let $I$ denote the set of all elements in $\mathbb{R}$ for which $P$ holds. A [[partial function]] $f:\mathbb{R} \to \mathbb{R}$ is equivalently a function $f:I \to \mathbb{R}$ for any such predicate $P$ and set $I$. 

A function $f:I \to \mathbb{R}$ is smooth at a subset $S \subseteq I$ with injection $j:S \hookrightarrow \mathbb{R}$ if it has a function $(D^{(-)} j)(-):\mathbb{N} \times S \to \mathbb{R}$ with $(D^0 j)(a) = a$ for all $a \in S$, such that for all [[Archimedean ordered Artinian local ring|Archimedean ordered Artinian local $\mathbb{R}$-algebras]] $A$ with ring homomorphism $h_A:\mathbb{R} \to A$, natural numbers $n \in \mathbb{N}$, and purely infinitesimal elements $\epsilon \in D$ such that $\epsilon^{n + 1} = 0$
$$f_A(h_A(j(a)) + \epsilon) = \sum_{i = 0}^{n} \frac{1}{i!} h_A((D^i j)(a)) \epsilon^i$$ 

Special cases include being smooth at an element $a \in I$, which is the same as being smooth at the [[singleton subset]] $\{a\}$, and being **smooth** which is the same as being smooth at the [[improper subset]] of $I$. 

This approach is used in [[synthetic differential geometry]], where one adds additional axioms to the foundations stating that the only functions on $A$ are the [[smooth functions]]. 

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

## Related concepts

* [[infinitesimal object]]

* [[infinitesimal neighbourhood]]

| [[ring]] with [[infinitesimals]] | [[function]] | 
---------------------|-----------------|
| [[dual numbers]] | [[differentiable function]] |
| [[Weil ring]] | [[smooth function]] |
| [[power series ring]] | [[analytic function]] |

## References

For more see references at 

* *[[infinitesimal neighbourhood]]* 

* *[[synthetic differential geometry]]*.

See also

*  Wikipedia: [Infinitesimals](http://en.wikipedia.org/wiki/Infinitesimal)

* {#Cohen83} [[Hermann Cohen]]: *Das Prinzip der Infinitesimal-Methode und seine Geschichte*, Berlin (1883) &lbrack;[html](http://www.gleichsatz.de/b-u-t/archiv/Cohen/hc-infinit1.html)&rbrack;

* {#KatzSherry13} [[Mikhail Katz]], David Sherry, _Leibniz's Infinitesimals: Their Fictionality, Their Modern Implementations, And Their Foes From Berkeley To Russell And Beyond_, D. Erkenn (2013) 78: 571 ([arXiv:1205.0174](https://arxiv.org/abs/1205.0174), [doi:10.1007/s10670-012-9370-y](https://link.springer.com/article/10.1007/s10670-012-9370-y))
  > (on [[Gottfried Leibniz]]'s concept of infinitesimals)


[[!redirects notions of infinitesimals]]
[[!redirects infinitesimal]]
[[!redirects infinitesimals]]
[[!redirects infinitesimal number]]
[[!redirects infinitesimal numbers]]

[[!redirects purely infinitesimal]]
[[!redirects purely infinitesimal number]]
[[!redirects purely infinitesimal numbers]]