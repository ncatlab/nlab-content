
#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #DirectDefinitionOfSpinC}
###### Definition

For $n \in \mathbb{N}$, the [[Lie group]] $Spin^c(n)$ is the [[quotient]]

$$
  \begin{aligned}
    Spin^c & := Spin \times_{\mathbb{Z}_2} U(1)
    \\
    & = (Spin \times U(1))/{\mathbb{Z}_2}
    \,,
  \end{aligned}
$$

of the [[product]] of the [[spin group]] with the [[circle group]] by the common sub[[group of order 2]] $\mathbb{Z}_2 \hookrightarrow \mathbb{Z}$ and $\mathbb{Z}_2 \hookrightarrow U(1)$.

=--

## Properties

+-- {: .num_prop}
###### Proposition

We have a [[short exact sequence]]

$$
 U(1) \to Spin^c \to SO
 \,,
$$

where $U(1) \to Spin^c$ is the canonical inclusion into the defining product $U(1) \to Spin \times U(1) \to Spin \times_{\mathbb{Z}_2} U(1)$.

=--

+-- {: .num_prop}
###### Proposition

We have a [[homotopy pullback]] diagram

$$
  \array{
     \mathbf{B} Spin^c &\to& \mathbf{B}U(1)
     \\
     \downarrow && \downarrow^{\mathrlap{\mathbf{c}_1 mod 2}}
     \\
     \mathbf{B} SO &\stackrel{\mathbf{w}_2}{\to}&
     \mathbf{B}^2 \mathbb{Z}_2 
  }
$$

in [[Smooth∞Grpd]], where 

* the right morphism is the universal first [[Chern class]] modulo 2;

* the bottom morphism is the universal second [[Stiefel-Whitney class]].

=--

+-- {: .proof}
###### Proof

We present the sitation as usual in the projective [[model structure on simplicial presheaves]] over [[CartSp]] by [[∞-anafunctors]].

The first [[Chern class]] is given by the [[∞-anafunctor]]

$$
  \array{
     \mathbf{B}(\mathbb{Z} \to \mathbb{R})
     &\stackrel{\mathbf{c}_1}{\to}&
     \mathbf{B}(\mathbb{Z} \to 1)
     = 
     \mathbf{B}^2 \mathbb{Z}
     \\
     \downarrow^{\mathrlap{\simeq}}
     \\
     \mathbf{B} U(1)     
  }
  \,,
$$

where $(G_1 \to G_0)$ denotes a presentation of a [[strict 2-group]] by a [[crossed module]].

The second [[Stiefel-Whitney class]] is given by

$$
  \array{
    \mathbf{B}(\mathbb{Z}_2 \to Spin)
    &\stackrel{\mathbf{w}_2}{\to}&
    \mathbf{B}(\mathbb{Z}_2 \to 1)
    = 
    \mathbf{B}^2 \mathbb{Z}_2
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B} SO
  }
  \,.
$$

Notice that the top horizontal morphism here is a [[fibration]].

Therefore the [[homotopy pullback]] in question is (as discussed there) given by the ordinary [[pullback]] $Q$ in

$$
  \array{
    Q
    &\to& 
    \mathbf{B}(\mathbb{Z} \to \mathbb{R})
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}(\mathbb{Z}_2 \to Spin)
    &\to&
    \mathbf{B}^2 \mathbb{Z}_2
  }
  \,.
$$

This pullback is $\mathbf{B}(\mathbb{Z} \stackrel{\partial}{\to} Spin \times \mathbb{R})$, where 

$$
  \partial : n \mapsto ( n mod 2 , n)
  \,.
$$

This is equivalent to 

$$
  \mathbf{B}(\mathbb{Z}_2 \stackrel{\partial'}{\to} Spin \times U(1))
$$

where now $\partial'$ is the [[diagonal]] embedding of the subgroup

$$
  \partial' : \sigma \mapsto (\sigma, \sigma)
  \,.
$$

This in turn is equivalent to 

$$
  \mathbf{B} (Spin \times_{\mathbb{Z}_2} U(1))
  \,,
$$

which is def. \ref{DirectDefinitionOfSpinC}.

=--

+-- {: .num_remark}
###### Remark

Compare this with the similar but different [[homotopy pullback]] that defines the [[spin group]]

$$
  \array{
    \mathbf{B}Spin &\to& * 
    \\
    \downarrow && \downarrow 
    \\
    \mathbf{B}SO &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
  }
$$ 

=--

Notice from _[[integral Stiefel-Whitney class]]_ that the universal third integral SW-class 

$$
  W_3 := \beta_2 \circ w_2 
$$

has a smooth refinement 

$$
  \mathbf{W}_3 = \mathbf{\beta}_2 \circ \mathbf{w}_2
  \,,
$$

where

$$
  \mathbf{\beta}_2 : \mathbf{B}^2 \mathbb{Z} \to \mathbf{B}^2 U(1)
$$

is simply given by the canonical subgroup embedding.

+-- {: .num_cor}
###### Corollary

The [[delooping]] $\mathbf{B}Spin^c$ of the group $Spin^c$ is the [[homotoy fiber]] of the universal third [[integral Stiefel-Whitney class]].

$$
  \mathbf{B}Spin^c 
   \to 
  \mathbf{B} SO
   \stackrle{\mathbf{W}_2}{\to}
  \mathbf{B}^2 U(1)
  \,,
$$

=--

+-- {: .proof}
###### Proof

Notice that we have a [[fiber sequence]]

$$
  \mathbf{B} U(1)
    \to
  \mathbf{B}^2 \mathbb{Z}_2 
    \stackrel{\mathbf{\beta}_2}{\to}
  \mathbf{B}^2 U(1)
    \to
  \mathbf{B}^2 U(1)
$$

Pasting this to the above homotopy pullback gives the desired result.

(...)

=--

## Related concepts

* [[spin group]], **$Spin^c$-group**

* [[spin^c structure]]

[[!redirects spin^c group]]
