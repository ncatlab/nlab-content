
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


# Irrational numbers
* table of contents
{: toc}

## Idea

An irrational number is of course a [[number]] that is not [[rational number|rational]].  As such, the concept is perhaps uninteresting.  However, the term 'irrational number' is often used for an irrational *[[real number|real]]* number; in this case, it is interesting to consider such numbers for two reasons:

*  Historically, it was an important discovery that irrational real numbers exist.
*  The [[topological space]] of all irrational real numbers is interesting in [[constructive analysis]], [[computability]] theory, and [[descriptive set theory]].

Of course, there are also various theorems about general classes of numbers that distinguish rational from irrational numbers.


## Definition

### In the real numbers

An [[affine function]] on the real numbers consists of a function $f$ and real number [[coefficients]] $a$ and $b$ such that for all real numbers $x$, $f(x) = a x + b$. The [[constant function]] at zero $\lambda x.0$ is an affine function where $a = 0$ and $b = 0$. A real number is **irrational** if for all affine functions $f$ with [[integer]] coefficients, if $f(x) = 0$, then $f = \lambda x.0$. This is equivalent to saying that a real number is irrational if for all rational numbers $a$, $x \neq a$.

Alternatively, a [[real number]] $x$ is **irrational** if given any [[rational number]] $a$ (thought of as a real number), the [[absolute value]] ${|x - a|}$ is [[positive number|positive]]. 

These two definitions are equivalent in [[classical mathematics]]. However, these two definitions no longer coincide in [[constructive mathematics]]; the former definition of irrational number is called **weakly irrational** while the latter definition is called **strongly irrational** or **strictly irrational**. Strongly irrational numbers are most commonly used in constructive mathematics, since it uses the apartness relation or strict order relation of the real numbers, which, unlike equality, is what is detected of the real numbers in constructive mathematics. 

The [[set]] of irrational real numbers (a [[subset]] of the set of real numbers) is variously denoted $\mathbb{I}$, $\mathbb{J}$, or $\mathbb{B}$ (in various fonts).  The $\mathbb{I}$ and $\mathbb{J}$ stand for 'irrational', while the $\mathbb{B}$ stands for 'Baire' (see the next paragraph).  Here we will use $\mathbb{J}$.

We may give $\mathbb{J}$ a [[topological structure|topology]] as a [[subspace]] of the [[real line]] $\mathbb{R}$.  With this topology, $\mathbb{J}$ is sometimes called __[[Baire space of irrational numbers|Baire space]]__; however, one uses a different [[uniform structure]].  (This should be distinguished from the sense of [[Baire space]] as a space to which the [[Baire category theorem]] applies; however, $\mathbb{J}$ is an example of such a space.)

### As non-repeating radix expansions

There is another definition of irrational number, common in the prealgebra and high school algebra literature, which directly defines the irrational numbers in terms of base 10 infinite radix expansions. (see [[radix notation]]). This can be done in every base greater than 1:

Let the natural number $b \gt 1$ denote the base of the radix expansion, $[0, b)$ denote the half-open [[interval]] in the [[natural numbers]] of all natural numbers less than $b$. Base $b$ infinite radix expansions are elements of $\mathbb{Z} \times [0, b)^\mathbb{N}$, with the idea that each pair $(i, d)$ consists of an integer $i$ and a sequence of digits $d(n)$ in the base $b$ infinite radix expansion. The [[series]] 
$$\sum_{n = 0}^\infty i + \frac{d(n)}{b^{n + 1}}$$
can be shown to be a [[Cauchy sequence]]. 

The set of repeating base $b$ infinite radix expansion is the subset of $\mathbb{Z} \times [0, b)^\mathbb{N}$ such that for pairs $(i, d)$ in the subset, there exist natural number $k$ and positive natural number $n$ such that the sequence $\lambda m.d(m + k)$ factors through the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$. 

$$\lambda m.d(m + k):\mathbb{N} \to \mathbb{Z}/n\mathbb{Z} \to [0, b)$$

Two base $b$ infinite radix expansions $(i, d)$ and $(j, e)$ are said to be [[apartness relation|apart from]] each other if $i \neq j$ or there exists a natural number $n$ such that $d(n) \neq e(n)$

$$(i, d) \# (j, e) \coloneqq (i \neq j) \vee \exists n \in \mathbb{N}.d(n) \neq e(n)$$

A base $b$ infinite radix expansion $x$ is *strictly non-repeating* if it is apart from every repeating base $b$ infinite radix expansion. An **irrational number** is a strictly non-repeating base $b$ infinite radix expansion. 

In [[constructive mathematics]], not every strictly irrational number is the limit of the series
$$\sum_{n = 0}^\infty i + \frac{d(n)}{b^{n + 1}}$$
given by a non-repeating base $b$ infinite radix expansion. However, it is still the case that strictly irrational numbers which are also [[Cauchy real numbers]] are interdefinable with strictly non-repeating base $b$ infinite radix expansions. 

### In Archimedean integral domains

Let $R$ be an [[Archimedean integral domain]] with the [[integers]] $\mathbb{Z} \subseteq R$ being a integral subdomain of $R$. 

An element $r \in R$ is irrational if for all $a \in \mathbb{Z}$ and $b \in \mathbb{Z}$, $\vert a \vert \gt 0$ and $\vert a \cdot r - b \vert \gt 0$. 

The set of __irrational numbers__ in $R$ is defined as
$$\mathbb{J}_R \coloneqq \{r \in R \vert \forall a, b \in \mathbb{Z}. (\vert a \vert \gt 0) \wedge (\vert a \cdot r - b \vert \gt 0) \}$$

### In integral domains with a p-adic norm

Let $R$ be an [[integral domain]] with a [[p-adic norm]] $\vert(-)\vert_p$ for a [[prime number]] $p$, with the [[integers]] $\mathbb{Z} \subseteq R$ being a integral subdomain of $R$. 

An element $r \in R$ is irrational if for all $a \in \mathbb{Z}$ and $b \in \mathbb{Z}$, $\vert a \vert_p \gt 0$ and $\vert a \cdot r - b \vert_p \gt 0$. 

The set of __irrational numbers__ in $R$ is defined as
$$\mathbb{J}_R \coloneqq \{r \in R \vert \forall a, b \in \mathbb{Z}. (\vert a \vert_p \gt 0) \wedge (\vert a \cdot r - b \vert_p \gt 0) \}$$

## History

The followers of [[Pythagoras]] believed that 'All is number', meaning what we now call (positive) [[natural numbers]].  In [[geometry]], this meant that any two lengths (or other geometric magnitudes) $x$ and $y$ are [[commensurable quantities|commensurable]] in the sense that there exists a [[unit]] length $u$ such that $x = m u$ and $y = n u$ for some natural numbers $m$ and $n$.  Identifying the ratios of geometric magnitudes with (positive) [[real numbers]], this becomes the claim that every real number is rational.  The discovery that this is *false* is also attributed to the Pythagoreans (but the legends of punishment for this secret date from several hundred years later).  Greek mathematicians developed further the theory of irrational numbers, up to the general theory of magnitudes (which we may now regard as a theory of [[positive real numbers]]) attributed to [[Eudoxus]] in Book X of [[Euclid's Elements]].

Mathematicians coming from the cultures of the Islamic Golden Age (particularly [[Abu Kamil]]) were the first to treat irrational numbers algebraically as numbers (rather than geometrically as ratios of magnitudes); they applied the [[algebra]] of [[Al-Khwarizmi]] to [[square roots]], cube [[roots]], etc.  (Ultimately, [[Omar Khayyam]] developed a general method to find the real roots of any cubic [[polynomial]].)  However, they seem to have implicitly believed that all real numbers were expressible using such roots ([[radical number]]s), which we now know is false even for some algebraic numbers, such as the real root of $x^5 + 2 x + 1$.  In any case, they only used such numbers.

Later, European mathematicians of the early modern era (particularly [[Gerolamo Cardano|Cardano]], [[Tartaglia]], and [[Lodovico Ferrari|Ferrari]]) had begun work with [[imaginary number]]s, which are necessarily irrational.  Following this, [[Johann Lambert|Lambert]] and [[Adrien-Marie Legendre|Legendre]] succeeded in proving the irrationality of [[pi]], [[e]], and their powers, which ultimately led to the conjecture that they were transcendental (whereas radical numbers, and even the root of $x^5 + 2x + 1$, are by definition [[algebraic number|algebraic]]); this conjecture was later established by [[Charles Hermite|Hermite]] and [[Ferdinand von Lindemann|Lindemann]]. Around this time, [[Leonhard Euler|Euler]] and [[Joseph-Louis Lagrange|Lagrange]] popularized [[continued fraction]]s (see below) to study both rational and irrational numbers.

During the [[arithmetization of analysis]] in the 19th century, people sometimes wrote of the problem of 'defining irrational numbers'.  The actual issue here was defining real numbers in general; one could define rational numbers algebraically, leaving only the irrational numbers as the problem.  However, this may be a red herring; one could just as easily define [[algebraic number]]s algebraically and say that the problem is defining transcendental numbers; indeed, it was only with the discovery that such numbers as $\pi$ and $\mathrm{e}$ are irrational that work on this problem came to life.  On the other hand, it\'s not clear that anybody could completely work out the [[order]] properties of algebraic numbers without already coming upon [[Richard Dedekind|Dedekind]]\'s solution.  In any case, specific irrational algebraic numbers such as $\sqrt{2}$ posed no difficulty to the [[finitist mathematics|finitist]] methods used by such algebraists as [[Leopold Kronecker]].

To this day, there are various specific real numbers (such as $\pi + \mathrm{e}$, the [[Euler number|Euler–Mascheroni constant]] $\gamma$, etc.) whose rationality or irrationality is unknown.  In [[constructive mathematics]], this makes it unproved that these numbers are rational or irrational (although the [[double negation]] of this statement can be proved for any real number).  The question of whether ${\sqrt{2}}^{\sqrt{2}}$ is rational or irrational is part of a famous illustration of the nature of constructive vs nonconstructive proof.  (Namely, there is a cheap and easy nonconstructive proof that there exist irrational numbers $a$ and $b$ such that $a^b$ is rational: let $b$ be $\sqrt{2}$ and let $a$ be either $\sqrt{2}$ or ${\sqrt{2}}^{\sqrt{2}}$, depending on whether the latter is rational or irrational.  A constructive proof that decides which of these is the case is much harder: ${\sqrt{2}}^{\sqrt{2}}$ turns out to be irrational, by a constructive version of the [[Gelfond-Schneider theorem|Gelfond–Schneider theorem]].[^fine]) 

[^fine]: Of course, one could also take $a = \sqrt{2}$ and $b = 2\frac{\log 3}{\log 2})$, which are both irrational by easy constructive proofs, if one is after definite irrational numbers $a$ and $b$ such that $a^b$ is rational (here the result is $a^b = 3$). The irrationality of $\frac{\log 3}{\log 2}$ follows, as easily as that of $\sqrt{2}$, from the [[fundamental theorem of arithmetic]]: there do not exist nonzero integers $p, q$ such that $2^p = 3^q$. 


## Properties

The Baire space $\mathbb{J}$ is [[homeomorphic]] to the [[product space]] $\mathbb{N}^{\mathbb{N}}$ of $\aleph_0$ copies of the [[discrete space]] of [[natural numbers]].  The homeomorphism is given by [[continued fraction]]s (see below).

Every [[inhabited space|inhabited]] [[Polish space]] is a [[quotient space]] of $\mathbb{J}$, and $\mathbb{J}$ is itself a Polish space.

As a subset of the real line, $\mathbb{J}$ is a [[full set]] (meaning that its complement, the set of rational numbers, is [[null set|null]]).

[[Cantor space]] may be identified with a [[subspace]] of $\mathbb{J}$, consisting of those irrational numbers whose continued fraction expansion consists only of $1$ and $2$ (but this does not agree with the usual inclusions into $\mathbb{R}$).

The [[fan theorem]] states precisely that $\mathbb{J}$ (when thought of as a [[topological space]]) is [[sober space|sober]] or that $\mathbb{J}$ (when thought of as a [[locale]]) is [[topological locale|topological/spatial/has enough points]].  This is true in [[classical mathematics]] and in [[intuitionistic mathematics]] but fails in other forms of [[constructive mathematics]].


## Continued fractions

(Main article: [[continued fraction]].) 

Let $[a_0;a_1,a_2,a_3,\ldots]$ be an [[infinite sequence]] of [[integers]], all positive except (possibly) $a_0$.  We interpret this as the number
$$ a_0 + \frac{1}{a_1 + \frac{1}{a_2 + \frac{1}{a_3 + \cdots}}} .$$
By truncating this expression after $a_i$, we produce a rational number; altogether, this is an infinite sequence of rational numbers.

+-- {: .un_theorem}
###### Theorems

This is a [[Cauchy sequence]] whose limit is irrational.  Furthermore, every irrational number has a unique representation in this way.  Yet more, the [[bijection]] thus shown between $\mathbb{J}$ and the infinitary [[cartesian product]] $\mathbb{Z} \times \mathbb{N}^+ \times \mathbb{N}^+ \times \mathbb{N}^+ \times \cdots$ is a [[homeomorphism]] when the two sets are given their usual [[topological structure|topologies]].
=--

The usual proofs of these theorems are entirely [[constructive mathematics|constructive]].  Accordingly, in the [[foundations of mathematics]], one may define Baire space either as the space of irrational numbers or as the infinite product $\mathbb{N}^{\mathbb{N}}$.  However, to treat Baire space as a [[uniform space]] or as a [[metric space]], one uses the structure from $\mathbb{N}^{\mathbb{N}}$.

## Examples

* [[pi]]

* [[e]]

* [[golden ratio]]

## References

*  Wikipedia (English):
   *  [Baire space (set theory)](http://en.wikipedia.org/wiki/Baire_space_%28set_theory%29)
   *  [Irrational numbers &#8594; History](http://en.wikipedia.org/wiki/Irrational_number#History)

For the definition of the irrational numbers in terms of non-repeating base 10 infinite radix expansions

* Nichols, Eugene D, et al. Holt Algebra with Trigonometry. Holt, Rinehart and Winston : Harcourt Brace Jovanovich, 1992. 

* Marecek, Lynn, et al. Prealgebra 2e. OpenStax, Rice University, 2020. 

That Cauchy irrational numbers have radix expansions in constructive mathematics

* {#Swan24} Andrew Swan (2024) on Category Theory Zulip, [Radix expansions in constructive mathematics](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Radix.20expansions.20in.20constructive.20mathematics/near/456366041)

[[!redirects irrational number]]
[[!redirects irrational numbers]]

[[!redirects irrational real number]]
[[!redirects irrational real numbers]]
[[!redirects irrational real]]
[[!redirects irrational reals]]

[[!redirects weakly irrational number]]
[[!redirects weakly irrational numbers]]

[[!redirects weakly irrational real number]]
[[!redirects weakly irrational real numbers]]
[[!redirects weakly irrational real]]
[[!redirects weakly irrational reals]]

[[!redirects strongly irrational number]]
[[!redirects strongly irrational numbers]]

[[!redirects strongly irrational real number]]
[[!redirects strongly irrational real numbers]]
[[!redirects strongly irrational real]]
[[!redirects strongly irrational reals]]

[[!redirects strictly irrational number]]
[[!redirects strictly irrational numbers]]

[[!redirects strictly irrational real number]]
[[!redirects strictly irrational real numbers]]
[[!redirects strictly irrational real]]
[[!redirects strictly irrational reals]]

[[!redirects set of irrational numbers]]
[[!redirects space of irrational numbers]]
