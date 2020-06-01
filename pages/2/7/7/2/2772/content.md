
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Contents
* table of contents 
{: toc}

## Idea

The generalization to the context of [[(∞,1)-category]]-theory of the notion of a [[full and faithful functor]] in ordinary [[category theory]].


## Definition

An [[(∞,1)-functor]] $F : C \to D$ is **full and faithful** if for all objects $x,y \in C$  it induces an equivalence on the [[hom-object in a quasi-category|hom-∞-groupoids]]

$$
  F_{x,y} : Hom_C(x,y) \stackrel{\simeq}{\to}
   Hom_D(F(x), F(y))
  \,.
$$

A full and faithful $(\infty,1)$-functor $F : C \to D$ exhibits $C$ as a [[full sub-(∞,1)-category]] of $D$ and one tends to write

$$
  F : C \hookrightarrow D
$$

to indicate this. This is definition 1.2.10 of [Lurie](#Lurie)


## Properties

+-- {: .num_lemma }
###### Lemma
For an $(\infty,1)$-functor $F : C \to D$, the following are equivalent:

* $F$ is fully faithful 

* $Ho(F) : Ho(C) \to Ho(D)$ is a fully faithful functor of (1-)categories and the following square is a pullback in the $(\infty,1)$ category of $\infty$-categories:

$$
  \array{
    C &\to& D
    \\
    \downarrow && \downarrow
    \\
    Ho(C) &\to& Ho(D)
  }
$$

* The following square is a pullback in the $(\infty,1)$ category of $\infty$-categories:

$$
  \array{
    Core(C^{[1]}) &\to& Core(D^{[1]})
    \\
    \downarrow && \downarrow
    \\
    Core(C) \times Core(C) &\to& Core(D) \times Core(D)
  }
$$

* The following square is a pullback in the $(\infty,1)$ category of $\infty$-categories:

$$
  \array{
    C^{[1]} &\to& D^{[1]}
    \\
    \downarrow && \downarrow
    \\
    C \times C &\to& D \times D
  }
$$

=--

+-- {: .proof}
###### Proof
The equivalence of the first two points is basically remark 1.2.11.1 of [Lurie](#Lurie) that a fully faithful functor factors as an equivalence onto a full subcategory.

The equivalence of the first and third points is proposition 3.9.6 of [Cisinski](#Cisinski). The idea is to exploit the fact that the hom-spaces of an $\infty$-category $X$ are the fibers of $X^{[1]} \to X \times X$ (and similarly for the map on cores).

The fourth point implies the third point since Core preserves pullbacks. The second point implies the fourth point by the following arugment.

$$
  \array{
    C^{[1]} &\to& D^{[1]} &\qquad \qquad& C^{[1]} &\to& D^{[1]}
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    Ho(C)^{[1]} &\to& Ho(D)^{[1]} && C \times C &\to& D \times D
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    Ho(C) \times Ho(C) &\to& Ho(D) \times Ho(D)
    &&     Ho(C) \times Ho(C) &\to& Ho(D) \times Ho(D)
  }
$$

Assume the second point. Since $Ho(C) \to Ho(D)$ is a fully faithful functor of 1-categories, the bottom square is a pullback (and a homotopy pullback). The top square is a pullback since $(-)^{[1]}$ preserves limits. Thus the outer square is a pullback.

On the right, we've seen the outer square is a pullback and the bottom square is a pullback since limits commute with limits. Thus, the upper square is a pullback.

=--

Every full and faithful $(\infty,1)$-functor is a [[monomorphism in an (∞,1)-category|monomorphism]] in [[(∞,1)Cat]], but being a full and faithful $(\infty,1)$-functor is a stronger condition. An $(\infty,1)$-functor $F$ is a monomorphism if and only if it induces a [[monomorphism in an (∞,1)-category|monomorphism]] on [[hom-spaces]] and every equivalence $F X \simeq F Y$ is in the effective image of $F$ (see [this MathOverflow question](https://mathoverflow.net/questions/345686/monomorphisms-in-mathcalc-at-infty/345700)).

An [[(∞,1)-functor]] which is both full and faithful as well as an [[essentially surjective (∞,1)-functor]] is an [[equivalence of (∞,1)-categories]].


## Related concepts


[[!include properties of functors -- contents]]



## References 

This appears as definition 1.2.10 in

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_
* {#Cisinksi} [[Denis-Charles Cisinski]], "Higher Categories and Homotopical Algebra"


[[!redirects fully faithful (infinity,1)-functor]]
[[!redirects fully faithful (infinity,1)-functors]]
[[!redirects fully faithful (∞,1)-functor]]
[[!redirects fully faithful (∞,1)-functors]]
[[!redirects full and faithful (infinity,1)-functor]]
[[!redirects full and faithful (infinity,1)-functors]]
[[!redirects full and faithful (∞,1)-functor]]
[[!redirects full and faithful (∞,1)-functors]]
