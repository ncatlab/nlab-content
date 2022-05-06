
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A __functorial factorization__ is a structure on a category that factors any morphism into a composite of two morphisms, in a way that depends functorially on commutative squares.

Functorial factorizations play a prominent role in [[model category]] theory.  On the one hand, many constructions there do rely on the factorizations into (acyclic) [[cofibrations]] and (acyclic) [[fibrations]] to be functorial, while on the other hand via the [[small object argument]] many examples of model categories do in fact carry a functorial factorization.  (As a result, some authors include functorial factorization in the axioms of a model category right away.)

Functorial factorizations also play an important role as an ingredient in [[algebraic weak factorization systems]].

## Definition

### Concrete explicit

+-- {: .un_defn}
###### Definition
A __functorial factorization__ on a category $\mathcal{C}$ is a way of assigning to any arrow $f$ in $\mathcal{C}$ a pair of composable arrows $f_L, f_R$ such that $f = f_R \circ f_L$, together with for any [[commuting square]]

$$
  \array{
    & \overset{h}{\longrightarrow}
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{g}}
    \\
    & \overset{k}{\longrightarrow}
  }
$$

a morphism $E(h,k)$ completing their factorizations $f = f_R \circ f_L$ and $g = g_R \circ g_L$ to a further [[commuting diagram]]

$$
  \array{
    & \overset{h}{\longrightarrow}
    \\
    {}^{\mathllap{f_L}}\downarrow && \downarrow^{\mathrlap{g_L}}
    \\
    & \overset{E(h,k)}{\longrightarrow}
    \\
    {}^{\mathllap{f_R}}\downarrow && \downarrow^{\mathrlap{g_R}}
    \\
    & \overset{k}{\longrightarrow}
  }
  \,,
$$

in a way that depends functorially on the given commutative square, i.e. $E(h_1\circ h_2,k_1\circ k_2) = E(h_1,k_1) \circ E(h_2,k_2)$.
=--

### Abstract version

Write $\Delta[1] = \{0 \to 1\}$ and $\Delta[2] = \{0 \to 1 \to 2\}$ for the [[ordinal numbers]], regarded as [[posets]] and hence as [[categories]]. The [[arrow category]] $Arr(\mathcal{C})$ is equivalently the [[functor category]] $\mathcal{C}^{\Delta[1]} \coloneqq Funct(\Delta[1], \mathcal{C})$, while $\mathcal{C}^{\Delta[2]}\coloneqq Funct(\Delta[2], \mathcal{C})$ has as objects pairs of composable morphisms in $\mathcal{C}$. There are three injective functors $\delta_i \colon [1] \rightarrow [2]$, where $\delta_i$ omits the index $i$ in its image. 
By precomposition, this induces [[functors]] $d_i  \colon \mathcal{C}^{\Delta[2]} \longrightarrow \mathcal{C}^{\Delta[1]}$. Here 

* $d_1$ sends a pair of composable morphisms to their [[composition]];

* $d_2$ sends a pair of composable morphisms to the first morphism;

* $d_0$ sends a pair of composable morphisms to the second morphism.

+-- {: .num_defn #FunctorialFactorization}
###### Definition

For $\mathcal{C}$ a [[category]], a **functorial factorization** of the morphisms in $\mathcal{C}$ is a [[functor]] 

$$
  fact \;\colon\; \mathcal{C}^{\Delta[1]} \longrightarrow \mathcal{C}^{\Delta[2]}
$$ 

which is a [[section]] of the [[composition]] functor $d_1 \;\colon\; \mathcal{C}^{\Delta[2]}\to \mathcal{C}^{\Delta[1]}$.

=--


## Examples

* Not all [[weak factorization systems]] are functorial, although most are.  This includes those produced by the [[small object argument]], with due care, and also all [[algebraic weak factorization systems]].

* All [[orthogonal factorization systems]] are automatically functorial.

## Properties
 {#Properties}

### Enriched functorial factorizations

Sufficient conditions in [[enriched category theory]] (in particular [[enriched model category]]-theory) for functorial factorization to exist as an [[enriched functor]] is discussed in [Hirschhorn 02, Theorem 4.3.8](#Hirschhorn02), [Shulman 06, Prop. 24.2](#Shulman06)

### Equivalence to pointed endofunctors

+-- {: .un_prop}
###### Proposition
The following are equivalent:

1. A functorial factorization on $\mathcal{C}$.
2. A [[pointed endofunctor]] $R$ of $\mathcal{C}^{\Delta[1]}$ such that $cod : \mathcal{C}^{\Delta[1]} \to \mathcal{C}$ is a strict morphism of pointed endofunctors from $R$ to $Id_{\mathcal{C}}$, i.e. $cod \circ R = cod$ and $cod$ maps the point $Id_{\mathcal{C}^{\Delta[1]}}\to R$ to the identity map of $Id_{\mathcal{C}}$.  (This is called a **pointed endofunctor over $cod$**.)
3. Dually, a copointed endofunctor $L$ of $\mathcal{C}^{\Delta[1]}$ under $dom$.
=--
+-- {: .proof}
###### Proof
A endofunctor $R$ of $\mathcal{C}^{\Delta[1]}$ maps every morphism $f$ in $\mathcal{C}$ to a morphism $f_R$, in a functorial way.  A point of such an endofunctor  assigns to each $f$ a pair of morphisms $f_L, f_M$ such that $f_R \circ f_L = f_M\circ f$, naturally with respect to commutative squares.  To say $cod \circ R = cod$ means that $f_R$ has the same codomain as $f$, and to say that $cod$ respects the points says that $f_M$ is an identity.  Thus, $f = f_R \circ f_L$ is a factorization.  For functoriality, the functoriality of $R$ gives the commutative square $k \circ f = f_R \circ E(h,k)$ and the functoriality of $E(-,-)$, while the naturality of $(-)_L$ gives the commutative square $E(h,k) \circ f = f_L \circ h$.  The converse and dual are straightforward.
=--

An [[algebraic weak factorization system]] is a functorial factorization together with compatible enhancements of these endofunctors to a monad and comonad.  This can often be detected with the help of a [[composition law for factorizations]].

## References

* {#Hirschhorn02} [[Philip Hirschhorn]], _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([AMS](http://www.ams.org/bookstore?fn=20&arg1=whatsnew&item=SURV-99), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

* {#Shulman06} [[Michael Shulman]], _Homotopy limits and colimits and enriched homotopy theory_ ([arXiv:math/0610194](https://arxiv.org/abs/math/0610194))

[[!redirects functorial factorizations]]

[[!redirects functorial factorization system]]
[[!redirects functorial factorization systems]]
