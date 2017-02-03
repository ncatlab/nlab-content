
#Contents#
* table of contents
{:toc}

## Idea

An [[action]] by the [[circle group]].


## In rational homotopy theory

We discuss models of circle actions in [[rational homotopy theory]].

Throughout, let $A$ be a [[dg-algebra]]. Eventually this is thought of as being a [[Sullivan model]] for the [[rationalization]] of the [[quotient]] of a [[topological space]] by a circle action.

We take all [[differentials]] to have degree +1. For $V$ a [[vector space]] and $n$ a [[natural number]], we write $V[n]$ for the [[chain complex]] concentrated on $V$ in degree $n$.

+-- {: .num_defn #HirschExtension}
###### Definition
**(Hirsch extension of dg-modules)**

Let $N$ be a [[dg-module]] over $A$ and let $n \in \mathbb{N}$ be a [[natural number]]. Then a degree $n$ **Hirsch extension** of $N$  is 
a [[monomorphisms]] of [[dg-modules]] of the form

$$
  N \hookrightarrow (N \oplus (A \otimes V[n]), d_{\phi})
$$

given by a choice of

1. a [[vector space]] $V$

1. a [[linear map]] $d_V \;\colon\; V \to N_{n+1}$

where the differential $d_{\phi}$ is $d_N$ on $N$, is $d_A$ on $A$, and is given on $V$ by $\phi$ followed by the [[action]] $\rho$ of $A$ on $V$:

$$
  d_\phi (a \otimes v) = (d_A a) \otimes v + (-1)^{\vert a \vert}  \rho(a,\phi(v))
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

It follows that for $N_1, N_2$ two $A$-[[dg-modules]] then homomorphisms $f$ out of a Hirsch extension of the former (def. \ref{HirschExtension}) 

$$
  f 
   \;\colon\;
  (N_1 \olpus (A \otimes V[n]), d_\phi)
   \longrightarrow
  N_2
$$

is equivalently

1. a homomorphism of dg-modules $h \colon N_1 \to N_2$;

1. a [[linear map]] $g \colon V \to (N_2)_{n}$

such that

* $h \circ d_{\phi} = d_{N_2} \circ g$.

=--

The following defines a kind of [[minimal cofibrations]] of dg-modules.

+-- {: .num_defn}
###### Definition
**(minimal KS-extension)**

For $N$ a [[dg-module]] over $A$, then a **[[minimal KS-extension]]** of $N$ is a certain [[transfinite composition]] of Hirsch extensions, namely a [[monomorphism]]

$$
  N \hookrightarrow \hat N
$$

equipped with an [[exhaustive filtration]] $\{\hat N(n,q)\}_{n,q \in \mathbb{N}}$ such that:

1. $\hat N(0,0) \simeq N$;

1. the inclusions $\hat N(n,q) \hookrightarrow \hat N(n,q+1)$ are Hirsch extensions (def. \ref{HirschExtension}).

1. $N(n+1,0) = \underset{\longrightarrow}{\lim}_q \hat N(n,q)$ ([[colimit]] over the sequence of Hirsch extensions in the previous degree).

Accordingly, a **minimal KS-factorization** of a morphism $N_1 \to N_2$ of $A$-dg-modules is a factorization as a minimal KS-extension followed by a [[quasi-isomorphism]]

$$
  \array{
    N _1 && \longrightarrow && N_2
    \\
    & {}_{\mathllap{\text{minimal} \atop \text{KS-extension}}}\searrow && \nearrow_{\mathrlap{\text{quasi-iso}}}
    \\
    && N_1 \oplus (A \otimes V)
  }
  \,.
$$

Finally a **minimal KS-model** is a [[dg-module]] $N$ such that $0 \hookrightarrow N$ is a minimla KS-fibration.


=--

## Related concepts

* [[free loop space]], [[Sullivan model for free loop spaces]]


## References

### Models in rational homotopy theory

Discussion of models in [[rational homotopy theory]] includes:

* [[Agusti Roig]], [[Martintxo Saralegi-Aranguren]], _Minimal Models for Non-Free Circle Actions_ ([arXiv:math/0004141](https://arxiv.org/abs/math/0004141))

* [[Martin Raussen]], _Circle Actions on Rational Homology Manifolds and deformations of rational homotopy theory_,  Transactions of the American Mathematical Society Vol. 347, No. 1 (Jan., 1995), pp. 137-153  ([jstor](http://www.jstor.org/stable/2154792))
 


[[!redirects circle actions]]
