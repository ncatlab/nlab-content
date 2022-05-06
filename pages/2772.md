
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
An $(\infty,1)$-functor $F : C \to D$ is fully faithful if and only if the following square is a pullback in the $(\infty,1)$ category of $\infty$-categories:
$$
  \array{
    Core(C^{[1]}) &\to& Core(D^{[1]})
    \\
    \downarrow && \downarrow
    \\
    Core(C) \times Core(C) &\to& Core(D) \times Core(D)
  }
$$
where the horizontal maps are induced by $F$ and the vertical maps are the source and target maps.
=--

+-- {: .proof}
###### Proof
This is proposition 3.9.6 of [Cisinski](#Cisinski).

The idea is that if $X$ is an $\infty$-category, the fibers of $Core(X^{[1]}) \to Core(X) \times Core(X)$ are precisely the hom spaces of $X$. Thus, if the above square is a pullback, both vertical maps have the same fibers determined by any point $1 \to Core(C) \times Core(C)$, 

And conversely, the square above satisfies conditions for which the vertical maps having equivalent fibers implies it is a pullback.
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
