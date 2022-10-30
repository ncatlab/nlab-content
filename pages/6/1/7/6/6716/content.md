
# Contents
* table of contents
{: toc}

## Definition

+-- {: .num_defn #DirectDefinitionOfSpinC}
###### Definition

For $n \in \mathbb{N}$, the [[Lie group]] $Spin^c(n)$ is the [[quotient]]

$$
  \begin{aligned}
    Spin^c & \coloneqq Spin \times_{\mathbb{Z}_2} U(1)
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

### General

### As homotopy fiber of smooth $\mathbf{W}_3$
 {#AsHomotopyFiberOfSmoothW3}

We dicuss in the following that 

1. the universal third [[integral Stiefel-Whitney class]] $W_3$ has an esentially unique lift from [[∞Grpd]] $\simeq$ [[Top]] to [[Smooth∞Grpd]];

* the smooth [[delooping]] $\mathbf{B}Spin^c \in Smooth\infty Grpd$ is the [[homotopy fiber]] of $\mathbf{W}_3$, hence is the [[circle n-bundle|circle 2-bundle]] over $\mathbf{B} SO$ classified by $\mathbf{W}_3$. 



+-- {: .num_prop #SpinCAsHomotopyPullbackOfW2AndC1}
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
  \partial\colon n \mapsto ( n mod 2 , n)
  \,.
$$

This is equivalent to 

$$
  \mathbf{B}(\mathbb{Z}_2 \stackrel{\partial'}{\to} Spin \times U(1))
$$

where now $\partial'$ is the [[diagonal]] embedding of the subgroup

$$
  \partial'\colon \sigma \mapsto (\sigma, \sigma)
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

+-- {: .num_prop #SmoothRefinementOfBockstein}
###### Proposition


The third _[[integral Stiefel-Whitney class]]_ 

$$
  W_3
   \coloneqq 
  \beta_2 \circ w_2 
   \colon
  B SO \stackrel{w_2}{\to} B^2 \mathbb{Z}
  \stackrel{\beta_2}{\to}
  B^3 \mathbb{Z}
$$

has an essentially unique lift through [[geometric realization]] ${\vert-\vert}\colon $ [[Smooth∞Grpd]] $\stackrel{\Pi}{\to}$ [[∞Grpd]] $\stackrel{\simeq}{\to}$ [[Top]] 

given by

$$
  \mathbf{W}_3 = \mathbf{\beta}_2 \circ \mathbf{w}_2
  \colon 
  \mathbf{B} SO(n)
   \stackrel{w_2}{\to}
  \mathbf{B}^2 \mathbb{Z}_2
    \stackrel{\mathbf{\beta}_2}{\to}
  \mathbf{B}^2 U(1)
  \,,
$$

where $\mathbf{\beta}_2$ is simply given by the canonical subgroup embedding.

=--

+-- {: .proof}
###### Proof

Once we establish that this is a lift at all, the essential uniqueness follows from the respective theorem at [[smooth ∞-groupoid -- structures]].

The ordinary [[Bockstein homomorphism]] $\beta_2$ is presented by the [[∞-anafunctor]]

$$
  \array{
    \mathbf{B}^2(\mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{Z})
    &\to&
    \mathbf{B}^2 (\mathbb{Z} \to 1)
    =
    \mathbf{B}^3 \mathbb{Z}
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}^2 \mathbb{Z}_2
  }
  \,.
$$

Accordingly we need to lift the canonical presentation of $\mathbf{\beta}_2$ to a comparable $\infty$-anafunctor. This is accomplished by

$$
  \array{  
    \mathbf{B}^2(\mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{Z})
    &\stackrel{\hat \mathbf{\beta}_2}{\to}&
    \mathbf{B}^2 (\mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{R})
    \\
    \downarrow^{\mathrlap{\simeq}}
     &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}^2 \mathbb{Z}_2
     &\stackrel{\mathbf{\beta}_2}{\to}&
    \mathbf{B}^2 U(1)
  }
  \,.
$$

Here the top horizontal morphism is induced from the morphism of [[crossed module]]s that is given by the commuting diagram

$$
  \array{
    \mathbb{Z} &\stackrel{id}{\to}& \mathbb{Z}
    \\
    \downarrow^{\mathrlap{\cdot 2}} && \downarrow^{\mathrlap{\cdot 2}}
    \\
    \mathbb{Z}
    &\stackrel{}{\hookrightarrow}&
    \mathbb{R}
  }
  \,.
$$

Since $\mathbb{R}$ is contractible, we have indeed under [[geometric realization]] an equivalence

$$
  \array{
    \vert\mathbf{B}^2(\mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{Z})\vert
    &\stackrel{\vert \hat {\mathbf{\beta}}_2\vert}{\to}&
    \vert
      \mathbf{B}^2 (\mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{R})
    \vert
    \\
    \downarrow^{\mathrlap{\simeq}}
    &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \vert\mathbf{B}^2(\mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{Z})\vert
    &\to&
    \vert\mathbf{B}^2(\mathbb{Z} \to 1)\vert
    \\
    \downarrow^{\mathrlap{\simeq}}
    &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \vert B^2 \mathbb{Z}_2\vert
     & \stackrel{\beta_2}{\to}&
    \vert B^3 \mathbb{Z}\vert
  }
  \,.
$$

=--

+-- {: .num_cor}
###### Corollary

The [[delooping]] $\mathbf{B}Spin^c$ of the Lie group $Spin^c$ in [[Smooth∞Grpd]] is the [[homotopy fiber]] of the universal third smooth [[integral Stiefel-Whitney class]] from \ref{SmoothRefinementOfBockstein}.

$$
  \mathbf{B}Spin^c 
   \to 
  \mathbf{B} SO
   \stackrel{\mathbf{W}_3}{\to}
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

where $\mathbf{\beta}_2$ is the smoothly refined [[Bockstein homomorphism]].

Then consider the [[pasting diagram]] of [[homotopy pullback]]

$$
  \array{
     \mathbf{B}Spin^c 
       &\to& 
     \mathbf{B} U(1)
     &\to&
     {*}
     \\
     \downarrow && \downarrow && \downarrow
     \\
     \mathbf{B} Spin 
       &\stackrel{\mathbf{w}_2}{\to}&
     \mathbf{B}^2 \mathbb{Z}_2
       &\stackrel{\mathbf{\beta}_2}{\to}&
     \mathbf{B}^2 U(1)
  }
  \,.
$$

The right square is a [[homotopy pullback]] by prop \ref{SmoothRefinementOfBockstein}. The left square is a homotopy pullback by 
prop. \ref{SpinCAsHomotopyPullbackOfW2AndC1}.
This implies by the [[pasting law]] for homotopy pullbacks that the total rectangle is also a homotopy pullback. This proves the claim.

=--

## Related concepts

* [[spin group]], **$Spin^c$-group**

* [[spin^c structure]]

[[!redirects spin^c group]]
