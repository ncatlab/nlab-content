
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

A _functorial factorization_ is a [[weak factorization system]] with a certain compatibility condition on how the factorizations  relate as the morphisms are "translated".

The bare axioms on a [[weak factorization system]] only demand that every [[morphism]] in a given ambient [[category]] admits a factorization as the composite of two morphisms with certain properties, but there is no condition on these factorizations being compatible as one translates the morphism. One says that the weak factorization system is _functorial_ if whenever two morphisms $f$ and $g$ fit into a [[commuting square|commuting square]]

$$
  \array{
    & \longrightarrow
    \\
    {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{g}}
    \\
    & \longrightarrow
  }
$$

then their factorizations $f = f_R \circ f_L$ and $g = g_R \circ g_L$ may be chosen accordingly to fit into a [[commuting diagram]] of the form

$$
  \array{
    & \longrightarrow
    \\
    {}^{\mathllap{f_L}}\downarrow && \downarrow^{\mathrlap{g_L}}
    \\
    & \longrightarrow
    \\
    {}^{\mathllap{f_R}}\downarrow && \downarrow^{\mathrlap{g_R}}
    \\
    & \longrightarrow
  }
  \,.
$$

Functorial factorizations play a prominent role in [[model category]] theory. On the one hand, many constructions there do rely on the factorizations into (acyclic) [[cofibrations]] and (acyclic) [[fibrations]] to be functorial, on the other hand via the [[small object argument]] many examples of model categories do in fact carry a functorial factorization. (As a result some authors include functorial factorization in the axioms of a model category right away.)


## Definition

+-- {: .num_defn #FunctorialFactorization}
###### Definition

For $\mathcal{C}$ a [[category]], a **functorial factorization** of the morphisms in $\mathcal{C}$ is a [[functor]] 

$$
  fact \;\colon\; \mathcal{C}^{\Delta[1]} \longrightarrow \mathcal{C}^{\Delta[2]}
$$ 

which is a [[section]] of the [[composition]] functor $d_1 \;\colon\; \mathcal{C}^{\Delta[2]}\to \mathcal{C}^{\Delta[1]}$.

=--

+-- {: .num_remark}
###### Remark

In def. \ref{FunctorialFactorization} we are using the following notation, see at _[[simplex category]]_ and at _[[nerve of a category]]_:

Write $\Delta[1] = \{0 \to 1\}$ and $\Delta[2] = \{0 \to 1 \to 2\}$ for the [[ordinal numbers]], regarded as [[posets]] and hence as [[categories]]. The [[arrow category]] $Arr(\mathcal{C})$ is equivalently the [[functor category]] $\mathcal{C}^{\Delta[1]} \coloneqq Funct(\Delta[1], \mathcal{C})$, while $\mathcal{C}^{\Delta[2]}\coloneqq Funct(\Delta[2], \mathcal{C})$ has as objects pairs of composable morphisms in $\mathcal{C}$. There are three injective functors $\delta_i \colon [1] \rightarrow [2]$, where $\delta_i$ omits the index $i$ in its image. 
By precomposition, this induces [[functors]] $d_i  \colon \mathcal{C}^{\Delta[2]} \longrightarrow \mathcal{C}^{\Delta[1]}$. Here 

* $d_1$ sends a pair of composable morphisms to their [[composition]];

* $d_2$ sends a pair of composable morphisms to the first morphism;

* $d_0$ sends a pair of composable morphisms to the second morphism.


=--

## Examples

Not all [[weak factorization systems]] are functorial, although most (including those produced by the [[small object argument]], with due care) are.

All [[orthogonal factorization systems]] are automatically functorial.

## Properties
 {#Properties}

* Sufficient conditions in [[enriched category theory]] (in particular [[enriched model category]]-theory) for functorial factorization to exist as an [[enriched functor]] is discussed in [Hirschhorn 02, Theorem 4.3.8](#Hirschhorn02), [Shulman 06, Prop. 24.2](#Shulman06)

## References

* {#Hirschhorn02} [[Philip Hirschhorn]], _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([AMS](http://www.ams.org/bookstore?fn=20&arg1=whatsnew&item=SURV-99), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))


* {#Shulman06} [[Michael Shulman]], _Homotopy limits and colimits and enriched homotopy theory_ ([arXiv:math/0610194](https://arxiv.org/abs/math/0610194))

[[!redirects functorial factorizations]]

[[!redirects functorial factorization system]]
[[!redirects functorial factorization systems]]
