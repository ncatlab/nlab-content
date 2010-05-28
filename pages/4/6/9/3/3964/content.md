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

The "if" direction of this is easy, since $u\colon \emptyset \to J$ is always a sieve, while $u_*\colon * \to U(J)$ assigns the terminal object of $D(J)$.  Thus, if $u_*$ has a further right adjoint, it must preserve colimits, and in particular its value must be an initial object (as well as a terminal one).  The converse is a "super-difficult" excercise in [Maltsionitis' notes](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf).


### Loop and suspension

In a pointed derivator, we have a [[suspension]] functor $\Sigma\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{a_*}{\to} D \Gamma \overset{abc_!}{\to} D \square \overset{d^*}{\to} D 1$$
where $\square$ denotes the category
$$ \array{ a & \to & b \\ \downarrow & & \downarrow \\ c & \to & d } $$
and $\Gamma$ its full subcategory on $\{a,b,c\}$.

Similarly, we have a [[loop space]] functor $\Omega\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{d_!}{\to} D \Gamma^{op} \overset{bcd_*}{\to} D \square \overset{a^*}{\to} D 1.$$
where $\Gamma^{op}$ is the full subcategory of $\square$ on $\{b,c,d\}$.  One can verify that $\Sigma \dashv \Omega$; this also follows from the considerations below.

### Relative diagram categories

If $D$ is a pointed derivator and $i\colon A\hookrightarrow B$ is a [[full subcategory]], we write $D(B,A)$ for the full subcategory of $D B$ on those diagrams $X\in D B$ such that $i^*X$ is null.

+-- {: .un_theorem}
###### Theorem
$D(B,A)$ is a [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]] subcategory of $D(B)$.
=--

+-- {: .query}
[[Mike Shulman]]: This is Proposition 7.4 in Heller's paper cited below.  All he says about the proof is that the reflector at $X$ is the homotopy cofibre of the [[counit]] $i_! i^* X \to X$.  This is the shortest proof I've been able to come up with, but there may well be a much shorter one.
=--

+-- {: .proof}
###### Proof
We define a reflector $L\colon D(B) \to D(B,A)$.  Let $M i$ be the "directed mapping cylinder" of $i$, meaning the full subcategory of $B\times I$ containing all objects $(x,1)$ for $x\in B$, but only objects $(x,0)$ when $x\in A$.  Write $j\colon M i \to B\times I$ for the inclusion, $k\colon M i \to B$ for the obvious projection, and $ab\colon I\to \Gamma$ for the inclusion.  Then $L$ is the composite
$$
D(B) \overset{k^*}{\to} D(M i)
\overset{j_!}{\to} D(B\times I)
\overset{ab_*}{\to} D(B\times \Gamma)
\overset{\Gamma_!}{\to} D(B)
$$
Note that $j_! k^* X \in D(B\times I)$ is a representative of the counit $i_! i^* X \to X$ in $D(B)$, and $ab_*$ inserts the zero object at objects $(x,c)$ in $B\times\Gamma$.  Thus $L(X)$ is morally the cofiber of this counit.

We first rephrase this definition a little.  Let $P$ denote the full subcategory of $B\times \Gamma$ containing all objects $(x,b)$ for $x\in B$ but only objects $(x,a)$ and $(x,c)$ for $x\in A$, with inclusions $M i\overset{Mab}{\to} P \overset{v}{\to} B\times \Gamma$.  Then we claim that $ab_* j_! \cong v_! Mab_*$.  First note that the following square is exact:
$$\array{M i & \overset{Mab}{\to} & P\\
  ^j \downarrow && \downarrow ^v\\
  B\times I & \underset{ab}{\to} & B\times \Gamma}$$
so that we have an isomorphism $v^* ab_* \cong Mab_* j^*$, whose [[mate]] is a transformation $v_! Mab_* \to ab_* j_!$.  It is then easy to verify that this mate is an isomorphism objectwise.  Therefore, $L$ can also be written as the composite
$$
D(B) \overset{k^*}{\to} D(M i)
\overset{Mab_*}{\to} D(P)
\overset{w_!}{\to} D(B).
$$
where $w = \colon P \to B$ is the obvious projection.

We next show that $L X\in D(B,A)$.  Observe that the following square is exact:
$$\array{A\times \Gamma & \overset{r}{\to} & P \\
  ^s \downarrow && \downarrow^w \\
  A & \underset{i}{\to} & B }
$$
Thus, $i^* L(X) = i^* w_! Mab_* k^* X \cong s_! r^* Mab_* k^* X$.  But $r^* Mab_* k^* X \in D(A\times \Gamma)$ has the schematic form
$$\array{X & \Rightarrow & X\\
  \Downarrow && \\
  0 & }$$
and it is easy to check that $s_!$ of this is always zero.  Thus $L X\in D(B,A)$.

Finally, let $X\in D(B)$ and $Y\in D(B,A)$; we have the following sequence of isomorphisms, showing that $L$ is a reflection of $X$ into $D(B,A)$.
$$
\begin{aligned}
D(B)(L X, Y) &= D(B)(w_! Mab_* k^* X, Y)\\
&\cong D(P)(Mab_* k^* X, w^* Y)\\
&\overset{(1)}{\cong} D(P)(Mab_* k^* X, Mab_* k^* Y)\\
&\overset{(2)}{\cong} D(P)(k^* X, k^* Y)\\
&\cong D(P)(k_! k^* X, Y)\\
&\overset{(3)}{\cong} D(P)(X, Y).
\end{aligned}
$$
To see isomorphism (1), note that since $Y\in D(B,A)$, $w^* Y$ is zero on both copies of $A$, and in particular on the copy consisting of objects $(x,c)$ for $x\in A$; thus the canonical map $w^*Y \to Mab_* Mab^* w^* Y = Mab_* k^* Y$ is an isomorphism.  The isomorphism (2) is because $Mab_*$ is fully faithful (since $Mab$ is).  Finally, isomorphism (3) is because the following square is exact:
$$\array{P & \overset{k}{\to} & B\\
  ^k\downarrow && \downarrow\\
  B & \underset{}{\to} & B}$$
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
