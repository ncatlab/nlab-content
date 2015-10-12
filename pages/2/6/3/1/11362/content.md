
# Contents #
* table of contents 
{: toc}

## Idea 

A _continued fraction_ (*Kettenbr&#252;che* in German) is a finite or infinite expression of the form 

$$x = a_0 + \frac{b_1}{a_1 + \frac{b_2}{a_2 + \frac{b_3}{a_3 + \cdots}}} $$ 

with convergence under appropriate conditions. The most commonly used form is where $b_i = 1$ for all $i$; such is called a _regular_ continued fraction. 

Every real number may be (more or less[^fine]) uniquely expressed as a finite or infinite regular continued fraction for which all the $a_i$ are [[integers]] and $a_i \gt 0$ for $i \gt 0$. The expression is an infinite continued fraction if and only if the real number is [[irrational number|irrational]], so that there is a [[bijection]] 

$$\mathbb{Z} \times (\mathbb{N}_+)^{\mathbb{N}_+} \to \{irrationals\}$$ 

$$(a_0; a_1, a_2, \ldots) \mapsto x = a_0 + \frac{1}{a_1 + \frac{1}{a_2 + \frac{1}{a_3 + \cdots}}}.$$ 

[^fine]: For rational numbers, there are two continued fraction representations, agreeing up to say $a_{n-1}$, but ending with $a_n \gt 1$ in one case and $a_n - 1, a_{n+1} = 1$ in the other (since after all $a_n = (a_n - 1) + 1/1$). This can be an annoyance, but there are various workarounds. 

This is in fact a [[homeomorphism]] if we endow the left side with the [[product topology]] and the right side with the [[subspace]] topology, regarding the set of irrationals as a subset of the real line (with its standard [[topological space|topology]]). (The space of irrationals becomes in this way a kind of prototypical chaotic dynamical system, where the dynamics on the product space is given by a shift map.) 

## Coalgebraic formulation 

We can describe the basic theory of continued fractions for real numbers in terms of dynamics of [[fractional linear transformations]] on the real [[projective line]] $\mathbb{P}^1(\mathbb{R})$, with the point at infinity playing a special role. From an nPOV, it is useful to cast this in [[coalgebra of an endofunctor|coalgebraic]] terms. 

Let us denote by $\mathbf{R}$ the [[interval]] $[1, \infty]$ (considered as a subset of the projective line $\mathbb{P}^1(\mathbb{R})$); if $1 \leq x \lt \infty$, we let $fl(x)$ be the floor of $x$ (the greatest integer such that $fl(x) \leq x$). We denote by $\mathbb{N}_+$ the set of positive integers (so, excluding $0$). Put $\mathbf{1} = \{\ast\}$, and define a map 

$$\alpha: \mathbf{R} \to \mathbf{1} + \mathbf{R} \times \mathbb{N}_+$$ 

where $\alpha(x) = ((x - fl(x))^{-1}, fl(x))$ if $x \lt \infty$, and $\alpha(\infty) = \ast$. This defines a coalgebra of the functor $F: Set \to Set$ defined by the formula 

$$F(X) = \mathbf{1} + X \times \mathbb{N}_+.$$ 

Let us define $x \in \mathbf{R}$ to be _rational_ if it is a quotient of two integers (including $0$, so $1/0 = \infty$ is here considered "rational"). Define $\tau: \mathbf{R} \to \mathbf{R}$ by $\tau(x) = (x - fl(x))^{-1}$ if $x \lt \infty$, and $\tau(\infty) = \infty$. 

+-- {: .num_lemma #rational} 
###### Lemma 
An element $x \in \mathbf{R}$ is rational if and only if there exists $n \geq 0$ such that $\tau^n(x) = \infty$. 
=-- 

+-- {: .proof} 
###### Proof 
Only if: this is clear for $x = \infty$. Otherwise, write $x = p/q$ in lowest terms, so that $p, q \gt 0$ and $\gcd(p, q) = 1$. We argue by strong induction on $q$, where we have $p = n q + r$ for which $n = fl(p/q)$ and $0 \leq r \lt q$ by the Euclidean algorithm. If $r = 0$, then $\tau(x) = \infty$ and we are done; otherwise $\tau(p/q) = q/r$ where $q \gt r \gt 0$ and $\gcd(q, r) = 1$, whence $\tau^n (q/r) = \infty$ for some $n$ by inductive hypothesis, and then $\tau^{n+1}(p/q) = \infty$. 

If: argue by induction on the least $n$ such that $\tau^n(x) = \infty$. If $n = 0$, then $x = \tau^0(x) = \infty$ is rational. Otherwise, we have 

$$x = fl(x) + 1/\tau(x)$$ 

and since $\tau^{n-1}(\tau(x)) = \infty$, we have that $\tau(x)$ is rational by inductive hypothesis, and therefore $x$ is also rational. 
=-- 

+-- {: .num_lemma #converge} 
###### Lemma 
If $(a_0, a_1, a_2, \ldots) \in (\mathbb{N}_+)^{\mathbb{N}}$ is any sequence of positive integers, then there is a unique $x \in \mathbf{R}$ such that $a_n = fl(\tau^n(x))$ for all $n \geq 0$. (This $x$ must be irrational by Lemma \ref{rational}.) 
=-- 

+-- {: .proof} 
###### Proof 
In a nutshell, $x$ is given by the continued fraction 

$$x = a_0 + \frac{1}{a_1 + \frac{1}{a_2 + \frac{1}{a_3 + \cdots}}} $$ 

and so it is really only a matter of proving that this continued fraction converges, i.e., that its truncations $p_n/q_n = [a_0, a_1, \ldots, a_n]$, namely the rational numbers $p_n/q_n$ with $\tau^{n+1}(p_n/q_n) = \infty$ and $fl(\tau^k(p_n/q_n)) = a_k$ for $0 \leq k \leq n$, form a [[Cauchy sequence]]. 

For $a \in \mathbb{N}_+$, let $a \cdot -: \mathbf{R} \to \mathbf{R}$ denote the fractional linear transformation $x \mapsto a + \frac1{x}$. We have 

$$[a] = a \cdot \infty, \qquad [a_0, a_1, \ldots, a_n] = a_0 \cdot [a_1, \ldots, a_n]$$ 

and since $a \cdot -: \mathbf{R} \to \mathbf{R}$ is monotone decreasing, we have that $a_0 \cdot (a_1 \cdot -)$ is monotone increasing. Thus some easy inductions establish 

* $$[a_0] \lt [a_0, a_1, a_2] \lt [a_0, a_1, a_2, a_3, a_4] \lt \ldots$$ 

* $$[a_0, a_1] \gt [a_0, a_1, a_2, a_3] \gt [a_0, a_1, a_2, a_3, a_4, a_5] \gt \ldots$$ 

* $$[a_0, \ldots, a_{2n}] \lt [a_0, \ldots, a_{2n}, a_{2n+1}]$$ 

so that $\sup_n [a_0, \ldots, a_{2n}] \leq \inf_n [a_0, \ldots, a_{2n+1}]$, and all that remains is to show $lim_{m\to \infty} {|p_m/q_m - p_{m+1}/q_{m+1}|} = 0$. 

In fact we have 

$${|\frac{p_m}{q_m} - \frac{p_{m+1}}{q_{m+1}}|} = \frac{{|p_m q_{m+1} - p_{m+1}q_m|}}{q_m q_{m+1}} = \frac1{q_m q_{m+1}}$$ 

The second equation is proved by induction on the length $j$ of continued fraction representations $[x_1, \ldots, x_j]$. Put $[a_1, \ldots, a_m] = \frac{q_m}{r_m}$ and $[a_1, \ldots, a_{m+1}] = \frac{q_{m+1}}{r_{m+1}}$, with all fractions in reduced form, and suppose as induction hypothesis that ${|q_m r_{m+1} - q_{m+1}r_m|} = 1$. The fractional linear transformation $a_0 \cdot -$, being represented by the integral [[matrix]] 

$$A_0 = \left(
\array{ 
a_0 & 1 \\
1 & 0
}\right)$$ 

with [[determinant]] $-1$, takes $(\pm 1)$-determinant matrices to $(\pm 1)$-determinant matrices. In particular it takes the determinant of absolute value $1$ on the left to one on the right,

$$\left(
\array{
q_m & q_{m+1} \\
r_m & r_{m+1}
}\right) \; \; \stackrel{A_0}{\mapsto} \; \; \left(
\array{
p_m & p_{m+1} \\
q_m & q_{m+1}
}\right),$$ 

and this completes the induction. 

Here $p_m = a_0 q_m + r_m \gt 2r_m$ and $p_{m+1} = a_0 q_{m+1} + r_{m+1} \gt 2r_{m+1}$. Similarly, if 

$$[a_2, \ldots, a_m] = \frac{r_m}{s_m}, \qquad [a_2, \ldots, a_{m+1}] = \frac{r_{m+1}}{s_{m+1}},$$ 

then $q_m \gt 2s_m$ and $q_{m+1} \gt 2s_{m+1}$. Thus we have 

* $${|[a_2, \ldots, a_m] - [a_2, \ldots, a_{m+1}]|} = \frac1{s_m s_{m+1}}$$ 

* $${[a_0, \ldots, a_m] - [a_0, \ldots, a_{m+1}]|} = \frac1{q_m q_{m+1}} \lt \frac1{(2s_m)(2s_{m+1})} = \frac1{4s_m s_{m+1}}$$ 

so that by induction, ${|p_{2m}/q_{2m} - p_{2m+1}/q_{2m+1}|} \leq \frac1{4^m}$, completing the proof that the infinite continued fraction converges. 
=-- 

+-- {: .num_remark} 
###### Remark 
It may be tempting to believe that this $F$-coalgebra structure makes $\mathbf{R}$ the terminal coalgebra. That is unfortunately not correct because the coalgebra structure $\xi: \mathbf{R} \to F(\mathbf{R})$ is not an isomorphism (it fails to be surjective because no element maps to $(1, 1, \infty)$ under $\xi$; this is the fact that the standard continued fraction for $2$ is just $2$ and not $1 + 1/1$). However, [below](#half-open) we will exhibit a different kind of coalgebra making half-open intervals a terminal coalgebra. 
=-- 

## Topology of infinite continued fractions 

Let $\mathbf{I}$ be the set of irrational elements $x \in \mathbf{R}$. The results above imply that $\mathbf{I}$ equipped with the map 

$$\mathbf{I} \to \mathbf{I} \times \mathbb{N}_+: x \stackrel{\alpha}{\mapsto} ((x - fl(x))^{-1}, fl(x))$$ 

is a terminal coalgebra for the functor $- \times \mathbb{N}_+: Set \to Set$, isomorphic to $(\mathbb{N}_+)^{\mathbb{N}}$ under the coalgebra structure 

$$(\mathbb{N}_+)^{\mathbb{N}} \stackrel{(\mathbb{N}_+)^{\langle s, o\rangle}}{\to} (\mathbb{N}_+)^{\mathbb{N} + \mathbf{1}} \cong (\mathbb{N}_+)^\mathbb{N} \times \mathbb{N}_+.$$ 

Endow $\mathbf{I}$ with the subspace topology coming from $\mathbf{R}$ (as one-point [[compactification]] of $[1, \infty)$), and $(\mathbb{N}_+)^{\mathbb{N}}$ with the topology of the [[product]] of countably many [[discrete spaces]] $\mathbb{N}$. 

+-- {: .num_lemma} 
###### Lemma 
The coalgebra isomorphism $\mathbf{I} \to (\mathbb{N}_+)^{\mathbb{N}}$ is a [[continuous map]]. 
=-- 

+-- {: .proof} 
###### Proof 
It suffices to check that each composite 

$$\mathbf{I} \to (\mathbb{N}_+)^{\mathbb{N}} \stackrel{\pi_n}{\to} \mathbb{N}_+$$ 

is continuous. Following the notation $\tau(x) = (x - fl(x))^{-1}$ above, this composite map is $x \mapsto fl(\tau^n(x))$, so it suffices to check that $fl: \mathbf{I} \to \mathbb{N}_+$ is continuous, or in other words that 

$$\{x \in \mathbf{I}: fl(x) = m\}$$ 

is [[open set|open]] for every $m$. This set is clearly open, being the intersection $(m, m+1) \cap \mathbf{I}$ (noting that of course $m \notin \mathbf{I}$!). 
=-- 

+-- {: .num_lemma} 
###### Lemma 
The coalgebra isomorphism $\psi: (\mathbb{N}_+)^{\mathbb{N}} \to \mathbf{I}$ is continuous. 
=-- 

+-- {: .proof} 
###### Proof 
This merely says that for each sequence of positive integers $(a_0, a_1, \ldots)$ and for a given $\epsilon \gt 0$, that there exists $N$ such that 
${|\psi(a_0, a_1, \ldots) - \psi(b_0, b_1, \ldots)|} \lt \epsilon$ provided 
$a_i = b_i$ for $i = 0, \ldots, N$. But this just follows the proof of convergence of continued fractions given in the proof of Lemma \ref{converge}. 
=-- 

+-- {: .num_corollary} 
###### Corollary 
The coalgebra isomorphism $\psi$ is a homeomorphism. 
=-- 

This makes the space of irrationals $\mathbf{I}$ the terminal coalgebra for the endofunctor $- \times \mathbb{N}_{+}: Top \to Top$. 

## Examples and further results 

+-- {: .num_example} 
###### Example 
A continued fraction $[a_0, a_1, \ldots]$ is periodic, i.e., satisfies $a_i = a_{k+i}$ for some fixed $k$ and all $i$, only if it is the root of a quadratic equation $a_0 \cdot (a_1 \cdot \ldots (a_{k-1} \cdot x)\ldots ) = x$ (where the operator on the left can be written as a fractional linear transformation). Every quadratic irrational is _eventually_ periodic (i.e., for some $k$ and $N$ we have $a_i = a_{k+i}$ for all $i \geq N$): the proof is part of the theory of [[Pell's equation]]. 
=-- 

This example shows that periodic points are [[dense subset|dense]] in the discrete [[dynamical system]] $\alpha^{-1}: \mathbf{I} \times \mathbb{N}_+ \to \mathbf{I}$, since quadratic surds are dense among all irrationals. 

Part of the story of Pell's equation is that an integer solution to $x^2 - D y^2 = \pm 1$, with $D$ is a square-free integer, is a pair $(x, y) = (p, q)$ where $p/q$ is a reduced form fraction (a rational approximant) represented by a finite truncation of the continued fraction of $\sqrt{D}$. 

+-- {: .num_example} 
###### Example 
The quadratic irrational represented by $[1, 1, 1, \ldots]$ is the [[golden ratio]] $\Phi = \frac1{2}(1 + \sqrt{5}) \approx 1.618\ldots$. Many properties of this constant (as manifested both mathematically and physically) are due to this fact and the fact that of all infinite continued fractions, the convergence rate of its rational approximants is slowest for this number. 
=-- 

+-- {: .num_remark} 
###### Remark 
Were the Pythagoreans the first to do coalgebra? John Baez remarks in [Week 265](http://math.ucr.edu/home/baez/week265.html) that the Pythagoreans were fascinated by pentagrams, and drops hints that they may have been aware of the continued fraction for the golden ratio and also the fact that $\Phi$ is irrational. The Pythagorean pentagram on display in Baez's page clearly indicates an infinite stream of pentagons which can be viewed as a coalgebraic behavior stream. And indeed if $\Phi$ were a rational number $p/q$ with $p, q$ as small as possible, then we would also have $\Phi = q/(p-q)$, with numerator and denominator even smaller, contradiction. This is analogous to one of the famous proofs of irrationality of $\sqrt{2}$: if $\sqrt{2} = p/q$, then also $\sqrt{2} = (2q - p)/(p-q)$, which generates an infinite descending stream of positive numerators and denominators, contradiction. 
=-- 

+-- {: .num_example} 
###### Example 
The continued fraction for [[Euler's number]] [[e]] is given by 

$$[2, 1, 2, 1, 1, 4, 1, 1, 6, 1, 1, 8, \ldots].$$ 

A proof may be found [here](http://topologicalmusings.wordpress.com/2008/08/04/continued-fraction-for-e/). 
=-- 

+-- {: .num_example} 
###### Example 
The regular continued fraction for [[pi|Ludolph's number]] $\pi$ displays no regularity, but other types of continued fractions do. See [Wikipedia](http://en.wikipedia.org/wiki/Pi#Continued_fractions). 
=-- 

The popularity of certain rational approximations to [[pi]] such as $\frac{22}{7}$ or $\frac{355}{113}$ can be explained by the fact that these are rational approximants obtained by truncating the regular continued fraction for $\pi$, coupled with the following result. 

+-- {: .num_theorem} 
###### Theorem 
The truncation $p/q = [a_0, a_1, \ldots, a_n]$ is a "best" rational approximant to the irrational number $\beta = [a_0, a_1, \ldots]$, in the sense that it minimizes the distance to $\beta$ among all rational numbers $r/s$ whose denominators $s$ are less than or equal to $q$. 
=-- 

The space of irrationals $\mathbf{I}$ may be identified with the space of irrationals in the interval $(0, 1)$ (by taking their reciprocals). Here the action $\alpha^{-1}: Irr(0, 1) \times \mathbb{N} \to Irr(0, 1)$ is generated by the shift map $\tau: x \mapsto x^{-1} \; mod \; 1$. 

+-- {: .num_theorem} 
###### Theorem 
The map $\tau$ is topologically mixing. Moreover, if $Irr(0, 1)$ is equipped with the [[probability measure]] 

$$\mu(I) = \frac1{\log 2} \int_I \frac{d x}{1+x},$$ 

then $\tau$ is an [[ergodic transformation]] with respect to $\mu$, making $(Irr(0, 1), \tau, \mu)$ an ergodic system. 
=-- 

A proof may be found [here](http://www.mathematik.uni-wuerzburg.de/~christ/nihon.pdf). 

### Reals as terminal coalgebra {#half-open} 

Returning to the theme of coalgebras, an alternative form of continued fractions may be used to exhibit a half-open real interval as a terminal coalgebra. The alternative continued fractions are of the form 

$$x = a_0 - \frac{1}{a_1 - \frac{1}{a_2 - \frac{1}{a_3 - \cdots}}} $$ 

where the $a_i$ are suitable integers; for now we will call them _antiregular_ continued fractions (not knowing what others call them), or acf's for short. These acf's correspond to [[fractional linear transformations]] belonging to $PSL_2(\mathbb{Z})$, generated by the transformations $z \mapsto -1/z$, $z \mapsto z-n$. 

Consider the linear order $\mathbb{R}_{\geq 1}$ (this time excluding $\infty$); let $\beta(x)$ be the smallest integer _strictly_ greater than $x$. 

Consider the endofunctor $G$ on the category of [[linearly ordered sets]] $X$ where $G(X)$ is the set $\mathbb{N} \times X$ equipped with the ordinal product or [[lexicographic order]]. (Actually we replace $\mathbb{N}$ with the set of integers greater than or equal to $2$.) Define a map  

$$\xi: \mathbb{R}_{\geq 1} \to \mathbb{N}_{\geq 2} \times \mathbb{R}_{\geq 1}$$ 

where $\xi(x) = (\beta(x), -\frac1{x - \beta(x)})$. 

+-- {: .num_theorem #PavPratt} 
###### Theorem 
**([Pavlovic-Pratt](#PP))** 
The map $\xi$ defines a $G$-coalgebra structure $\xi: \mathbb{R}_{\geq 1} \to G(\mathbb{R}_{\geq 1})$, making $\mathbb{R}_{\geq 1}$ the terminal $G$-coalgebra. 
=-- 


### Rationals as initial algebra  

Now let $\mathbf{Q} = \{r \in \mathbb{Q}: r \gt 1\} \cup \{\infty\}$, the set of rational elements of $\mathbf{R}$. On the category of linear orders, let $H$ be the endofunctor $H(X) = G(X) + 1$, the [[ordinal sum]] where $G$ was defined [above](#half-open). 

The initial $H$-algebra is the free monoid $\mathbb{N}_+^\ast$, [[lexicographic order|lexicographically ordered]] according to the convention given in this [remark](/nlab/show/lexicographic+order#antidictionary) (where initial segments of words $w$ are _greater_ than $w$). 

On the other hand, we have an $H$-algebra structure on $\mathbb{Q}$, a function 

$$\xi:\; (\mathbb{N}_+ \times \mathbf{Q}) + 1 \to \mathbf{Q}$$ 

where for $\ast \in 1$, $\xi(\ast) = \infty$, otherwise $\xi(n, r) = n+1-1/r$. Observe that this is indeed a monotone map between the linear orders $H(\mathbf{Q}) \to \mathbf{Q}$. 

+-- {: .num_theorem #initial} 
###### Theorem 
$(\mathbf{Q}, \xi)$ is the initial $H$-algebra. 
=-- 

The inverse map $\xi^{-1}: \mathbf{Q} \to H(\mathbf{Q})$ is in essence another form of the acf (see above): if $ceil(s)$ denotes the least integer greater than or equal to $s$, then $\xi^{-1}(\infty) = \ast$, and otherwise 

$$\xi^{-1}(r) = (ceil(r) - 1, -1/(r - ceil(r)).$$ 

The $H$-algebra isomorphism $\mathbb{N}_+^\ast \to \mathbf{Q}$ takes a finite word $a_0 a_1 \ldots a_n$ to the rational number to which the acf 

$$a_0 + 1 - \frac{1}{a_1 + 1 - \frac{1}{a_2 + 1 - \frac{1}{a_3 + 1 - \cdots}}}$$

evaluates. 


## Rational tangles 

Among the many uses of continued fractions, we mention a quite remarkable one due to John H. Conway. 

+-- {: .num_defn} 
###### Definition 
A _rational tangle_ is a subspace $T$ of the 3-disk $D^3$ obtained by embedding two arcs 

$$(\alpha_1, \alpha_2): I + I \to D^3,$$ 

with endpoints on the boundary $\partial D^3$, such that the pair of spaces $(D^3, T = \alpha_1(I) + \alpha_2(I))$ is homeomorphic to the pair $(D^2 \times I, \{x, y\} \times I)$, with $x, y \in D^2$ distinct points. Two rational tangles $S, T$ are _isotopic_ if there exists an orientation-preserving homeomorphism $(D^3, S) \to (D^3, T)$ that is the identity on $\partial D^3$. 
=-- 

Conventionally, rational tangles (or more general 2-tangles) are exhibited by tangle diagrams placed within a disk (with appropriate over- and under-crossings), say a unit disk ${|z|} \leq 1$ in the complex plane, with endpoints situated at primitive $8^{th}$ roots of unity $\exp((2k+1)i\pi/8)$; these endpoints are indicated by their directions NE, NW, SW, SE. There is a trivial 2-tangle with a chord from NE to NW and another from SE to SW; this is denoted $[0]$. Two operations that can be used to generate further 2-tangles are 

* "Turn" (rotate the disk through 90 degrees counterclockwise), 

* "Twist" (insert a "horizontal" twist that interchanges NE and SE, which can be a positive twist or a negative twist depending on convention). 

+-- {: .num_theorem} 
###### Theorem 
**(Conway)** 
The set of isotopy classes of rational tangles is in bijection with the set of rational elements $q \in \mathbb{Q} \cup \{\infty\}$, in such a way that if $[q]$ is the isotopy class corresponding to $q$, then $[-1/q]$ is the class corresponding to a turn of $[q]$, and $[1+q]$ is the class corresponding to a positive twist of $[q]$. 
=-- 

In particular, every rational tangle can be brought back to the trivial tangle $[0]$ by a series of (positive) twists and turns, and every rational tangle is isotopic to the tangle obtained by applying a 180 degree counterclockwise turn to it. A very readable account of this result may be found in an article by Kauffman and Lambropoulou, [here](http://arxiv.org/pdf/math/0311499.pdf). 

It should be remarked that the twist and turn operations correspond to group elements in $PSL_2(\mathbb{Z})$ (cf. the article [[Moebius transformation]], in particular the remarks on the surjective homomorphism $B_3 \to PSL_2(\mathbb{Z})$ where $B_3$ is the braid group on $3$ strands): 

$$turn = \left(
\array{
0 & 1 \\
-1 & 0
}\right), \qquad pos.twist = \left(
\array{
1 & 1 \\
0 & 1
}\right)$$ 

John Baez asks a question about this in [TWF228](http://math.ucr.edu/home/baez/week228.html), and reports on an answer in [TWF229](http://math.ucr.edu/home/baez/week229.html). He returns to this topic in an illuminating comment [here](http://golem.ph.utexas.edu/category/2014/04/the_modular_flow_on_the_space.html#c046316). 

David Corfield speculates at the [Caf&#233;](http://golem.ph.utexas.edu/category/2011/01/coalgebraic_tangles.html) that the infinite tangles mentioned by [Kauffman and Lambropoulou](#KL), as limits of rational tangles, might be viewed as belonging to a coalgebraic completion of the collection of rational tangles (along the lines of seeing the terminal coalgebra $\mathbf{R}$ as a coalgebraic completion of the initial algebra $\mathbf{Q}$, as in Theorem \ref{initial}). 

## The Calkin-Wilf and Stern-Brocot trees

The Calkin-Wilf tree is an infinite complete binary tree whose vertices are in 1-to-1 correspondence with the positive rational numbers.  The tree may be defined inductively by the following very simple recipe (Calkin & Wilf, 2000):

* $1/1$ is at the top of the tree, and
* each vertex $i/j$ has two children: its left child is $i/(i+j)$ and its right child is $(i+j)/j$

For example, the first four levels of the Calkin-Wilf tree are:

$$
\frac{1/1}{
 \frac{1/2}{
  \frac{1/3}{1/4\quad 4/3}
  \quad
  \frac{3/2}{3/5\quad 5/2}}
 \quad
 \frac{2/1}{
  \frac{2/3}{2/5\quad 5/3}
  \quad
  \frac{3/1}{3/4\quad 4/1}}}
$$

Remarkably, every positive rational number appears exactly once in the tree, and so performing a breadth-first traversal ($1/1, 1/2, 2/1, 1/3, 3/2, \dots$) gives an enumeration of the positive rationals with no double-counting.  In fact, Calkin and Wilf proved that the $n$th number in this sequence is equal to

$$\frac{b(n)}{b(n+1)}$$

where $b(n)$ is the number of ways of writing the integer $n$ as a sum of powers of 2, each power being used at most twice.

By locating a positive rational $q$ in the Calkin-Wilf tree and describing the path to $q$ from the root as a sequence of binary choices, one generates a string of bits which may be interpreted as an "uncompressed" representation of the continued fraction of $q$.  In turn, compressing this path by counting the number of repeated bits (i.e., by performing a "run-length encoding") is a way of reconstructing the continued fraction.  This is perhaps easier to see if we first express the two operations returning the left and right children of a vertex $x$ equivalently as

$$
\begin{aligned}
L(x) &= \frac{1}{1 + \frac{1}{x}} \\
R(x) &= 1 + x
\end{aligned}
$$

from which it follows that

$$
\begin{aligned}
L^a(x) &= \frac{1}{a + \frac{1}{x}} \\
R^a(x) &= a + x
\end{aligned}
$$

Now, suppose a positive rational $q$ has continued fraction $[a_0,\dots,a_n]$, assuming without loss of generality that $n$ is odd (we allow for $a_n = 1$).  Then the path from 1 to $q$ in the Calkin-Wilf tree begins by taking $a_n - 1$ steps to the left, followed by $a_{n-1}$ steps to the right, $a_{n-2}$ steps to the left, and so on, ending with $a_0$ steps to the right.  In other words, 

$$q = R^{a_0}L^{a_1}\dots R^{a_{n-1}} L^{a_n-1} 1$$

For example:

$$
\begin{aligned}
2/5 & = LLR(1) = \frac{1}{2 + \frac{1}{1 + 1}} \\
12/7 &= RLRRL(1) = 1 + \frac{1}{1 + \frac{1}{2 + \frac{1}{1 + \frac{1}{1}}}}
\end{aligned}
$$

Finally, the Calkin-Wilf tree gives a simple algebraic characterization of the positive rationals, namely as an initial object in the category of pointed modules for the free monoid on two elements $\{L,R\}$.  Given any such module $X$ and point $x \in X$, there is a unique module homomorphism $\mathbb{Q}^+ \to X$ sending $1$ to $x$, defined as follows: given a positive rational $q$, locate $q$ on the Calkin-Wilf tree, and then retrace the path from $1$ to $q$ in $X$, beginning at $x$ and applying the actions $L : X \to X$ and $R : X \to X$ as appropriate.

The Calkin-Wilf tree was first described in a 2000 paper by Neil Calkin and Herbert Wilf, "Recounting the rationals", but is closely related to the much older Stern-Brocot tree, another arrangement of the positive rationals with the special property that the values are ordered from left to right.  Here are the first four levels of the Stern-Brocot tree:

$$
\frac{1/1}{
 \frac{1/2}{
  \frac{1/3}{1/4\quad 2/5}
  \quad
  \frac{2/3}{3/5\quad 3/4}}
 \quad
 \frac{2/1}{
  \frac{3/2}{4/3\quad 5/3}
  \quad
  \frac{3/1}{5/2\quad 4/1}}}
$$

In fact, each tree may be obtained from the other by reversing the paths from the root (e.g., $2/5 = LLR(1)$ is reached from the root of the Stern-Brocot tree by going down left twice and then right once).

## Constructive aspects

The construction of a continued fraction from an arbitrary [[real number]] relies on the [[limited principle of omniscience]] to define the [[floor]]; it is not acceptable in [[constructive mathematics]].  Nevertheless, using the usual constructive meaning of [[rational number]] and [[irrational number]] (as well as [[convergence]] in the real numbers), we have that a continued fraction (involving [[natural numbers]]) represents a rational number iff it is finite and an irrational number iff it is infinite; and every rational or irrational number (if positive) is so representable.  Constructively, we simply cannot say that every real number is either rational or irrational.

Now, just because a real number has an expansion as a continued fraction, that doesn\'t mean that it must be rational or irrational.  In general, a continued fraction expansion (according to the coalgebraic formulation) is given by a [[stream]] of natural numbers, and a stream is not necessarily finite (so a [[list]]) or infinite (so a [[sequence]]).  However, a stream that is not finite must be infinite; accordingly, a real number that is not rational must be irrational *if* it has a continued fraction; even this is not constructively valid without the continued fraction.


## References 

* Wikipedia, _[Continued fraction](http://en.wikipedia.org/wiki/Continued_fraction)_ 

* Claude Brezinski, _Continued fractions and Pad&#233; approximants_, North-Holland 1991. ([vendor](http://www.amazon.com/Continued-Fractions-Pade-Approximants-Brezinski/dp/0444881697)) 

* A. Ya. Khinchin, _Continued fractions_, U. Chicago Press 1964. 

* Ilan Vardi, _Continued fractions from Euclid to the present day_, unpublished manuscript ([web](http://chronomaitre.org/ContinuedFractions.pdf))

* [[Louis Kauffman]] and Sofia Lambropoulou, _On the classification of rational tangles_, arXiv ([web](http://arxiv.org/pdf/math/0311499.pdf)). 
 {#KL} 

Dan Piponi wrote a series of posts on his blog "A Neighborhood of Infinity", using the programming language Haskell to illustrate some of the connections between continued fractions, rational tangles and linear operators:

* Dan Piponi, "Untangling with Continued Fractions" ([Part 0](http://blog.sigfpe.com/2008/08/untangling-with-continued-fractions.html), [Part 1](http://blog.sigfpe.com/2008/08/untangling-with-continued-fractions_16.html), [Part 2](http://blog.sigfpe.com/2008/08/untangling-with-continued-fractions_23.html), [Part 3](http://blog.sigfpe.com/2008/08/untangling-with-continued-fractions_31.html), [Part 4](http://blog.sigfpe.com/2008/09/untangling-with-continued-fractions.html), [Part 5](http://blog.sigfpe.com/2008/10/untangling-with-continued-fractions.html)). 

The material on half-open intervals as terminal coalgebras was first given by Pavlovi&#263; and Pratt, 

* [[Dusko Pavlovic]] and [[Vaughan Pratt]], _On coalgebras of real numbers_, Electronic Notes in Theoretical Computer Science, Volume 19 (1999), 103&#8211;117. ([web](http://www.sciencedirect.com/science/article/pii/S1571066105802725?np=y)) 
 {#PP} 

A type-theoretic formalization of the rationals in [[Coq]] based on the Stern-Brocot/Calkin-Wilf representation is described in:

* Milad Niqui and Yves Bertot, _QArith: Coq Formalisation of Lazy Rational Arithmetic_, INRIA report RR-5004, November 2003. ([web](http://hal.inria.fr/inria-00077041/))

Their library includes two implementations of the field operations: 1. a "strict" implementation (in the programming languages sense) in which the operations are performed by first converting continued fractions to ordinary fractions, applying the usual algorithms for arithmetic, and then converting back, and 2. a "lazy" implementation operating directly on continued fractions, in which the operations only need to inspect a portion of the input stream in order to determine a portion of the output stream.  This latter approach is based on ideas originally due to Gosper:

* Bill Gosper, ["Continued fraction arithmetic"](http://hack.org/mc/writings/hackerdom/hakmem/cf.html), MIT AI, Memo 239 HAKMEM, 1972.  (Also described in more detail in [this unpublished note](http://www.tweedledum.com/rwg/cfup.htm).)

[[!redirects continued fractions]] 