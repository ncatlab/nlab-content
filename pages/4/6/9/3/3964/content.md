# Pointed derivators
* table of contents
{: toc}

## Idea

A [[derivator]] is *pointed* if it has a [[zero object]] in the sense appropriate to a derivator.

## Definition

A derivator $D\colon Dia^{op} \to Cat$ is **pointed**, or has a **zero object**, if each category $D(X)$ has a zero object.

Note that these zero objects are automatically preserved by all the functors $u_!,u^*,u_*$, since they are all adjoints on one side or the other.

## Properties

This simple definitions hides a lot of structure.

### Relative diagram categories

If $D$ is a pointed derivator and $i\colon A\hookrightarrow B$ is a [[full subcategory]], we write $D(B,A)$ for the full subcategory of $D B$ on those diagrams $X\in D B$ such that $i^*X$ is null.

+-- {: .num_lemma #SieveRel}
###### Lemma
If $i$ is the inclusion of a [[sieve]], then $i_*\colon D(A) \to D(B)$ is fully faithful and its essential image is $D(B,B\setminus A)$.  Similarly, if $i$ is a cosieve, then $i_!$ identifies $D(A)$ with $D(B,B\setminus A)$.
=--
+-- {: .proof}
###### Proof
Suppose $i$ is a sieve.  Since $i$ is in particular fully faithful, so is $i_*$ by general arguments (see [[homotopy exact square]]).  Moreover, since $i$ is a sieve, the square
$$\array{ \emptyset & \to & A\\
\downarrow & & \downarrow^i\\
B\setminus A & \underset{j}{\to} & B}
$$
is homotopy exact (where $j$ is the inclusion).  Therefore $j^* i_* X$ is terminal for any $X\in D(A)$, so that $i_*$ lands inside $D(B,B\setminus A)$.  Conversely, if $X\in D(B,B\setminus A)$, then the map $X \to i_* i^* X$ is an isomorphism on $A$ (since $i_*$ is fully faithful) and on $B\setminus A$ (since both are terminal there), hence is itself an isomorphism; so $X$ is in the essential image of $i_*$.
=--

The following theorem is stated as Proposition 7.4 of Heller's paper "Stable homotopy theories and stabilization".

+-- {: .num_theorem #RelRefl}
###### Theorem
$D(B,A)$ is a [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]] subcategory of $D(B)$.
=--
+-- {: .proof}
Let $M i$ denote the "codirected mapping cylinder" of $i\colon A \hookrightarrow B$, by which we mean the full subcategory of $B\times I$ on the objects $(x,0)$ for $x\in B$ and $(i(x),1)$ for $x\in A$ (here $I$ is the [[interval category]] $(0\to 1)$).  This is also the same as the [[cocomma object]] $(B \uparrow i)$.  Write $B \overset{u}{\to} M i \overset{p}{\to} B$ for the evident inclusion and projection.

Consider the adjunction
$$ D(M i) \underoverset{p^*}{p_!}{\rightleftarrows} D(B). $$
We claim that this restricts to an adjunction
\[ D(M i,A) \underoverset{p^*}{p_!}{\rightleftarrows} D(B,A) \label{ppadj} \]
where $A$ denotes the subcategory of $M i$ on the objects $(i(x),1)$.  Certainly $p^*$ takes $D(B,A)$ into $D(M i,A)$, since $i\colon A \hookrightarrow B$ is the composite $A \hookrightarrow M i \overset{p}{\to} B$.  On the other hand, the square
$$\array{A & \hookrightarrow & M i \\
\downarrow & & \downarrow^p\\
A & \underset{i}{\to} & B }
$$
is [[homotopy exact square|homotopy exact]], so $p_!$ takes $D(M i,A)$ into $D(B,A)$.

Now since $u$ is the inclusion of a [[sieve]], by the previous lemma, $u_*$ identifies $D(B)$ with $D(M i,A)$.  Therefore, the inclusion $D(B,A)\hookrightarrow D(B)$ can be identified with the restricted right adjoint $p^*\colon D(B,A) \to D(M i,A)$, which therefore has a left adjoint $p_!$.  Explicitly, the left adjoint is $p_! u_*$.

The proof of coreflectivity is of course dual, using the directed mapping cylinder instead of the codirected one.
=--

Note that if $i'\colon A'\hookrightarrow B'$ is another full inclusion and
$$\array{A & \overset{f}{\to} & A'\\
  ^i\downarrow && \downarrow^{i'}\\
  B& \underset{g}{\to} & B'}$$
commutes, then we have a restriction $(g,f)^*\colon D(B',A') \to D(B,A)$, which has a left adjoint $(g,f)_!$ given by the composite
$$ D(B,A) \hookrightarrow D(B) \overset{g_!}{\to} D(B') \overset{L_{B',A'}}{\to} D(B',A') $$
where $L_{B,A}\colon D(B) \to D(B,A)$ denotes the reflection.  It also has a right adjoint defined dually.  Thus, if we wish, we can consider a pointed derivator to be a functor on the 2-category of pairs $(B,A)$ of a category together with a full subcategory, all of whose transition functors have both adjoints.

+-- {: .query}
Is it possible to characterize the "homotopy exact squares" in the 2-category of category-pairs?
=--


### Extraordinary inverse images


+-- {: .num_theorem #EOInv}
###### Theorem
A derivator $D$ is pointed if and only if whenever $u\colon A\to B$ is a [[sieve]] in $Dia$, the functor $u_* \colon D(A) \to D(B)$ has a right adjoint $u^!$, and dually whenever $u$ is a cosieve, the functor $u_!$ has a left adjoint $u^?$.
=--
+-- {: .proof}
The "if" direction of this is easy, since $u\colon \emptyset \to B$ is always a sieve, while $u_*\colon * \to U(B)$ assigns the terminal object of $D(B)$.  Thus, if $u_*$ has a further right adjoint, it must preserve colimits, and in particular its value on the unique object of $D(\emptyset)$ must be an initial object (as well as a terminal one).

Conversely, if $D$ is pointed and $u$ is a sieve, then by Lemma \ref{SieveRel}, $u_*$ identifies $D(A)$ with $D(B,B\setminus A)$.  But by Theorem \ref{RelRefl}, the inclusion $D(B,B\setminus A)\hookrightarrow D(B)$ has a right adjoint.  The other case is dual.
=--

The functors $u^!$ and $u^?$ are sometimes referred to as *extraordinary* and *co-extraordinary inverse image* functors.  Our proof shows that $u^? = u^* p_! v_*$, where $v$ and $p$ are respectively the inclusion of $B$ in the codirected mapping cylinder of $B\setminus A \hookrightarrow B$, and its projection to $B$.

In the literature, the existence of these functors is often taken as the definition of when a derivator is pointed.  The equivalence of the two definitions is a "super-difficult" excercise in [Maltsionitis' notes](http://people.math.jussieu.fr/~maltsin/Seville/Lecture_III_Derivators.pdf).


### Loop and suspension

In a pointed derivator, we have a [[suspension]] functor $\Sigma\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{a_*}{\to} D \Gamma \overset{abc_!}{\to} D \square \overset{d^*}{\to} D 1$$
where $\square$ denotes the category
$$ \array{ a & \to & b \\ \downarrow & & \downarrow \\ c & \to & d } $$
and $\Gamma$ its full subcategory on $\{a,b,c\}$.

Equivalently, the suspension can be defined as the composite
$$ D 1 = D(1,\emptyset) \overset{(a,\emptyset)_!}{\to} D(\square,bc) \overset{(d,\emptyset)^*}{\to} D(1,\emptyset) = D 1.$$
This follows because we have $D 1 \simeq D(\Gamma,bc)$, and thus $(a,\emptyset)_!$ is isomorphic to $(abc,bc)_!\colon D(\Gamma,bc) \to D(\square,bc)$, which by definition is $L_{\square,bc} \circ abc_!$.  But $abc_!$ is fully faithful since $abc\colon \Gamma \hookrightarrow \square$ is, and so it already takes $D(\Gamma,bc)$ into $D(\square,bc)$.  Thus $L_{\square,bc}$ is doing nothing, so $(a,\emptyset)_!$ is essentially just $abc_!$ which appeared in our previous definition of $\Sigma$.  (The other functor $a_*$ essentially implements the equivalence $D 1 \simeq D(\Gamma,bc)$.)

Similarly, we have a [[loop space]] functor $\Omega\colon D 1 \to D 1$ defined as the composite
$$ D 1 \overset{d_!}{\to} D \Gamma^{op} \overset{bcd_*}{\to} D \square \overset{a^*}{\to} D 1.$$
where $\Gamma^{op}$ is the full subcategory of $\square$ on $\{b,c,d\}$, and it can equivalently be given as the composite
$$ D 1 = D(1,\emptyset) \overset{(d,\emptyset)_*}{\to} D(\square,bc) \overset{(a,\emptyset)^*}{\to} D(1,\emptyset) = D 1.$$
The description in terms of relative diagram categories makes it clear that $\Sigma \dashv \Omega$.

We can also describe $\Sigma$ and $\Omega$ in terms of the extraordinary inverse image functors.  Since the square
$$ \array{ \Gamma & \to & \Gamma \\
^r\downarrow & & \downarrow^{abc}\\
* & \underset{d}{\to} & \square}$$
is homotopy exact, the composite $d^* abc_!$ in our first definition is the same as $r_!$.  The other functor $a_*$ can in turn be decomposed as a composite $ab_* s_*$, where $s\colon * \to I$ is the inclusion of $s$ into the interval category $(s\to t)$, and $ab\colon I\to \Gamma$ is the inclusion into $\{a,b\}$.

Therefore we have $\Sigma \cong r_! ab_* s_*$.  But $\Gamma$ can be identified with $M s$ and $ab$ with the inclusion $u\colon I \hookrightarrow M s$, while $r$ factors as $M s \overset{p}{\to} I \overset{q}{\to} *$ so that $r_! \cong q_! p_!$.  But finally, the square
$$\array{* & \overset{t}{\to} & I\\
\downarrow & & \downarrow^q\\
*& \to & *}$$
is homotopy exact, so $q_! \cong t^*$ and thus
$$\Sigma \cong t^* p_! u_* s_* \cong t^? s_*.$$
Dually, we can identify $\Omega \cong s^! t_!$, from which it again follows directly that $\Sigma \dashv \Omega$.


## The pointed reflection

Every derivator can be made pointed in a universal way; given $D$ we define $D_*(A)$ to be the full subcategory of $D(A\times I)$ which is terminal when restricted along $0\colon A\to A\times I$.  It requires a little work to show that this is a derivator.  The main observation being that the inclusion $D_*(A) \hookrightarrow D(A\times I)$ has a left adjoint (the "mapping cone"), which can be constructed just as in the proof of Theorem \ref{RelRefl}.  See III.5 of Heller's memoir.


## References

See [[derivator]] for general references.  The pointed reflection is discussed in III.5 of

* Alex Heller, "Homotopy theories," Mem. AMS 71:383.

The definition of relative diagram categories is taken from:

* Alex Heller, "Stable homotopy theories and stabilization", [MR](http://www.ams.org/mathscinet-getitem?mr=1431157)


[[!redirects pointed derivators]]
[[!redirects derivator with a zero object]]
[[!redirects zero object in a derivator]]
[[!redirects derivators with zero objects]]
[[!redirects zero objects in a derivator]]
