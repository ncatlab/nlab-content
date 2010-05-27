# Pointed derivators
* table of contents
{: toc}

## Idea

A [[derivator]] is *pointed* if it has a [[zero object]] in the sense appropriate to a derivator.

## Definition

A derivator $D\colon Dia^{op} \to Cat$ is **pointed**, or has a **zero object**, if each category $D(X)$ has a zero object.

## Properties

### Extra adjoints to sieve extensions

+-- {: .un_theorem}
###### Theorem
A derivator $D$ is pointed if and only if whenever $u\colon I\to J$ is a [[sieve]] in $Dia$, the functor $u_* \colon D(I) \to D(J)$ has a right adjoint $u^!$, and dually whenever $u$ is a cosieve, the functor $u_!$ has a left adjoint $u^?$.
=--

The "only if" direction of this is not too hard to prove.  The converse is a "super-difficult" excercise in [Maltsionitis' notes](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf).


### Loop and suspension

In a pointed derivator, we have a [[suspension]] functor $\Sigma\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{a_*}{\to} D \Gamma \overset{abc_!}{\to} D \square \overset{d^*}{\to} D 1$$
where $\square$ denotes the category
$$ \array{ a & \to & b \\ \downarrow & & \downarrow \\ c & \to & d } $$
and $\Gamma$ its full subcategory on $\{a,b,c\}$.

Similarly, we have a [[loop space]] functor $\Omega\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{d_!}{\to} D \Gamma^{op} \overset{bcd_*}{\to} D \square \overset{a^*}{\to} D 1.$$
where $\Gamma^{op}$ is the full subcategory of $\square$ on $\{b,c,d\}$.  One can verify that $\Sigma \dashv \Omega$.

### Relative diagram categories

If $D$ is a pointed derivator and $i\colon A\hookrightarrow B$ is a [[full subcategory]], we write $D(B,A)$ for the full subcategory of $D B$ on those diagrams $X\in D B$ such that $i^*X$ is null.

+-- {: .un_theorem}
###### Theorem
$D(B,A)$ is a [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]] subcategory of $D(B)$.
=--
+-- {: .query}
[[Mike Shulman]]: This is Proposition 7.4 in Heller's paper cited below.  All he says about the proof is that the reflector at $X$ is the homotopy cofibre of the [[counit]] $i_! i^* X \to X$.  It seems to me that a little thought is required to even make this functorial (since a priori the counit is a morphism in $D(B)$, but to take its homotopy cofiber we need to *choose* an object of $D(B\times I)$ representing it), and I haven't succeeded yet in showing that it's a reflection.
=--

If $i'\colon A'\hookrightarrow B'$ is another full inclusion and
$$\array{A & \overset{f}{\to} & A'\\
  ^i\downarrow && \downarrow^{i'}\\
  B& \underset{g}{\to} & B'}$$
commutes, then we have a restriction $(g,f)^*\colon D(B',A') \to D(B,A)$, which has a left adjoint $(g,f)_!$ given by the composite
$$ D(B,A) \hookrightarrow D(B) \overset{g_!}{\to} D(B') \overset{L_{B',A'}}{\to} D(B',A') $$
where $L_{B,A}\colon D(B) \to D(B,A)$ denotes the reflection.

We now observe that the suspension functor can equivalently be defined as the composite
$$ D 1 = D(1,\emptyset) \overset{(a,\emptyset)_!}{\to} D(\square,bc) \overset{(d,\emptyset)^*}{\to} D(1,\emptyset) = D 1.$$
This follows because we have $D 1 \simeq D(\Gamma,bc)$, and thus $(a,\emptyset)_!$ is isomorphic to $(abc,bc)_!\colon D(\Gamma,bc) \to D(\square,bc)$, which by definition is $L_{\square,bc} \circ abc_!$.  But $abc_!$ is fully faithful since $abc\colon \Gamma \hookrightarrow \square$ is, and so it already takes $D(\Gamma,bc)$ into $D(\square,bc)$.  Thus $L_{\square,bc}$ is doing nothing, so $(a,\emptyset)_!$ is essentially just $abc_!$ which appeared in our previous definition of $\Sigma$.  (The other functor $a_*$ essentially implements the equivalence $D 1 \simeq D(\Gamma,bc)$.)

All of this dualizes as well to show that the loop space functor can be defined as the composite
$$ D 1 = D(1,\emptyset) \overset{(d,\emptyset)_*}{\to} D(\square,bc) \overset{(a,\emptyset)^*}{\to} D(1,\emptyset) = D 1.$$
This description makes it clear that $\Sigma \dashv \Omega$.

## The pointed reflection

Every derivator can be made pointed in a universal way; given $D$ we define $D_*(A)$ to be the full subcategory of $D(A\times I)$ which is terminal when restricted along $0\colon A\to A\times I$.  It requires a little work to show that this is a derivator, the main observation being that the inclusion $D_*(A) \hookrightarrow D(A\times I)$ has a left adjoint (the "mapping cone").  See III.5 of Heller's memoir.


## References

See [[derivator]] for general references.  The pointed reflection is discussed in III.5 of

* Alex Heller, "Homotopy theories," Mem. AMS 71:383.

The section on relative diagram categories is taken from:

* Alex Heller, "Stable homotopy theories and stabilization", [MR](http://www.ams.org/mathscinet-getitem?mr=1431157)


[[!redirects pointed derivators]]
[[!redirects derivator with a zero object]]
[[!redirects zero object in a derivator]]
[[!redirects derivators with zero objects]]
[[!redirects zero objects in a derivator]]
