
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Pullbacks in derivators

* table of contents
{: toc}

## Idea

A *pullback in a derivator* is the generalization to the context of a [[derivator]] of the notion of [[pullback]] in ordinary category theory.  Viewing a derivator as the "shadow" of an [[(∞,1)-category]], the notion of pullback therein coincides with the notion of [[homotopy pullback]] in an $(\infty,1)$-category.

## Definition

Let $\square$ denote the category
$$ \array{a & \to & b \\ \downarrow & & \downarrow \\ c & \to & d} $$
that is the "free-living [[commutative square]]", and let $L$ be the full subcategory of $\square$ on $b,c,d$, with inclusion $u\colon L\to \square$.

Let $D$ be a [[derivator]] and let $X\in D(\square)$ be a commutative square in $D$.  We say that $X$ is a **pullback square**, or is **cartesian**, if the unit $X\to u_* u^* X$ of the [[adjunction]] $u^*\dashv u_*$ is an isomorphism.  Since $u$ is [[fully faithful]], so is $u_*$, so this is equivalent to saying that there exists some $Y\in D(L)$ such that $X\cong u_* Y$.

If $D$ is merely a prederivator, then we can phrase the same definition by saying that $X$ has the [[free object|universal property]] that $u_* u^* X$ would, if the whole functor $u_*$ existed.

The dual notion, of course, is a **pushout** or **cocartesian** square.

## Properties

### Pasting law {#Pasting}

Using properties of [[homotopy exact squares]], we can prove the "pasting law" for pullback squares in a derivator:

+-- {: .un_lemma}
###### Lemma
Given a diagram
$$ \array{a & \to & b & \to & c \\
\downarrow & & \downarrow & & \downarrow \\
d & \to & e & \to & f } $$
in which the right-hand square $bcef$ is a pullback, then the left-hand square $abde$ is a pullback if and only if the outer rectangle $acdf$ is a pullback.
=--

The following proof should be compared and contrasted with the [standard proof](http://ncatlab.org/nlab/show/pullback#Pasting) for pullbacks in 1-categories, and the [quasi-categorical proof](http://ncatlab.org/nlab/show/%28infinity%2C1%29-pullback#QuasiCatPastingLaw) for pullbacks in $(\infty,1)$-categories.  In particular, note that the statement for derivators is a generalization of both, since both 1-categories and $(\infty,1)$-categories give rise to derivators.

+-- {: .proof}
###### Proof
First of all, by "a diagram" in a derivator, we mean an object of $D(X)$ for some suitable category $X$.  In the above case, $X$ is the category consisting of two commutative squares, as pictured above.  We'll write $abcdef$ for this $X$, and similarly $cdef$ for its lower-right L-shaped subcategory, and so on.  We leave the verification of [[homotopy exact square|homotopy exactness]] of all squares to the reader.

Firstly, since the squares
$$\array{cef & \overset{}{\to} & bcef\\
  \downarrow && \downarrow\\
  cdef & \underset{}{\to} & abcdef} \qquad and \qquad
\array{cdf & \overset{}{\to} & acdf\\
  \downarrow && \downarrow\\
  cdef& \underset{}{\to} & abcdef}$$
are exact, if we start from a $cdef$-diagram and right Kan extend it to a full $abcdef$-diagram, then the right-hand square and outer rectangle must be pullback squares.  Moreover, by composition of adjoints, right Kan extension from $cdef$ to $abcdef$ is equivalent to first extending to $bcdef$ and then to $abcdef$, and since the square
$$\array{bde & \overset{}{\to} & abde\\
  \downarrow && \downarrow\\
  bcdef & \underset{}{\to} & abcdef}$$
is exact, the left-hand square in such an extension must also be a pullback.

Now if we start with an $abcdef$-diagram, say $F$, we can restrict it to a $cdef$-diagram and then right Kan-extend it to a new $abcdef$-diagram.  If $u\colon cdef \to abcdef$ is the inclusion, then this results in $u_\ast u^\ast F$, and we have a canonical natural transformation $\eta \colon F \to u_\ast u^\ast F$ (the unit of the adjunction $u^\ast \dashv u_\ast$).  Since the square
$$\array{cdef & \overset{}{\to} & cdef \\
  \downarrow && \downarrow\\
  cdef & \underset{}{\to} & abcdef}$$
is exact, the counit $u^\ast u_\ast G \to G$ is an isomorphism for any $G$, and in particular for $G=u^\ast F$, from which it follows by the triangle identities that $u^\ast F \to u^\ast u_\ast u^\ast F$ is also an isomorphism --- i.e. the components of $\eta\colon F \to u_\ast u^\ast F$ at $c$, $d$, $e$, and $f$ are isomorphisms.  Now if the right-hand square of $F$ is a pullback, then the restrictions of $F$ and $u_\ast u^\ast F$ to $bcef$ are both pullback squares; hence since the $cef$-components of $\eta$ are isomorphisms, so is the $b$-component.  And if the left-hand square of $F$ is a pullback, then we can play the same game with $abde$ to show that the $a$-component of $\eta$ is an isomorphism, while if the outer rectangle is a pullback, we can play it with $acdf$.  Hence in both of these cases, $\eta$ itself is an isomorphism, since all of its components are --- and thus the remaining square in $F$ is also a pullback, since we have shown that it is so in $u_\ast u^\ast F$.
=--

### Detection Lemma {#Detection}

The following lemma, which detects when squares occurring in a Kan extension are pullbacks or pushouts, is due to [Jens Franke](#Franke); see also [Groth](#Groth).  We state it in terms of pushouts.

+-- {: .num_lemma #CartesianSquareDetection}
###### Lemma
Let $f\colon K\to J$ be any functor and let $i\colon \square \to J$ be injective on objects, with lower vertex $i(1,1) = z$.  Suppose that $z$ is not in the image of $f$, and that the induced functor $\Gamma \to (J \setminus z)/z$ is a nerve equivalence (such as if it has an adjoint).  Then for any derivator $D$ and any $Y\in D(K)$, the square $i^* f_! Y$ is cocartesian.
=--
+-- {: .proof}
###### Proof
Since $f_! = j_! \bar{f}_!$ where $\bar{f}\colon K\to (J\setminus z)$ is induced by $f$ and $j\colon (J\setminus z) \to J$ is the inclusion, it suffices to suppose that $K = (J\setminus z)$.  Now what we want is to prove that the following square is [[homotopy exact square|homotopy exact]]:
$$ \array{ \Gamma &\to & (J\setminus z) \\
  \downarrow && \downarrow\\
  \square &\to & J}$$
Exactness is trivial at all objects of $\square$ except $(1,1)$.  In that case, we paste with another square:
$$ \array{ \Gamma &\to& \Gamma &\to & (J\setminus z) \\
  \downarrow & \swArrow & \downarrow && \downarrow\\
  \ast &\underset{(1,1)}{\to} &\square &\to & J}$$
The left-hand square is a [[comma square]], hence homotopy exact, so it suffices to show that the composite square is homotopy exact.  But the comma object associated to the cospan $\ast \to J \leftarrow (J\setminus z)$ is $(J \setminus z)/z$, and of course this comma square is also exact.  And the composite square factors through this comma square by the functor $\Gamma \to (J \setminus z)/z$ which is assumed a nerve equivalence; hence it is also homotopy exact.
=--


## References

See all references at [[derivator]].  Referred to particularly above are:

* Jens Franke, _Uniqueness theorems for certain triangulated categories with an Adams spectral sequence_, [K-theory archive](http://www.math.uiuc.edu/K-theory/0139/)
{#Franke}

* Moritz Groth, _Derivators, pointed derivators, and stable derivators_ [pdf](http://www.math.uni-bonn.de/~mgroth/groth_derivators.pdf)
{#Groth}

[[!redirects pullbacks in a derivator]]
[[!redirects pullbacks in derivators]]
[[!redirects cartesian square in a derivator]]
[[!redirects cartesian squares in a derivator]]
[[!redirects cartesian squares in derivators]]
[[!redirects Cartesian square in a derivator]]
[[!redirects Cartesian squares in a derivator]]
[[!redirects Cartesian squares in derivators]]
[[!redirects fiber product in a derivator]]
[[!redirects fiber products in a derivator]]
[[!redirects fiber products in derivators]]
[[!redirects pushout in a derivator]]
[[!redirects pushouts in a derivator]]
[[!redirects pushoutss in derivators]]
[[!redirects cocartesian square in a derivator]]
[[!redirects cocartesian squares in a derivator]]
[[!redirects cocartesian squares in derivators]]
[[!redirects coCartesian square in a derivator]]
[[!redirects coCartesian squares in a derivator]]
[[!redirects coCartesian squares in derivators]]
