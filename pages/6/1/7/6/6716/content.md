

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

+-- {: .num_remark}
###### Remark

By definition of the [[spin group]] $Spin(n)$ there is a canonical inclusion

$$
  \mathbb{Z}/2\mathbb{Z}\hookrightarrow Spin(n)
$$

of the [[group of order 2]]. For $Spin(n)\hookrightarrow GL_1(Cl(\mathbb{R}^n))$ canonically realized by even [[Clifford algebra]] elements of unit norm, this is given by the inclusion of $\{+1,-1\}$.


=--

> We frequently write $\mathbb{Z}_2$ as shorthand for $\mathbb{Z}/2\mathbb{Z}$.

+-- {: .num_defn #DirectDefinitionOfSpinC}
###### Definition

For $n \in \mathbb{N}$, the [[Lie group]] $Spin^c(n)$ is the [[quotient group]]

$$
  \begin{aligned}
    Spin^c(n) & \coloneqq Spin(n) \times_{\mathbb{Z}_2} U(1)
    \\
    & = (Spin(n) \times U(1))/{\mathbb{Z}_2}
    \,,
  \end{aligned}
$$

of the [[product]] of the [[spin group]] with the [[circle group]] by the common [[subgroup|sub]]-[[group of order 2]] $\mathbb{Z}_2 \hookrightarrow Spin$ and $\mathbb{Z}_2 \hookrightarrow U(1)$ (i.e.: the [[central product group]]).

=--

Usually only the case $n \geq 3$ is considered.

Some authors (e.g. [Gompf 97, p. 2](#Gompf97)) denote this as 

$$
  \begin{aligned}
    Spin^c(n) 
     & \coloneqq 
    Spin(n)\cdot Spin(2) 
     \\
    & \simeq Spin(n) \cdot U(1)
  \end{aligned}
$$

following the notation [[Sp(n).Sp(1)]] (see [there](SpnSp1#SpinnSpin2IsSpinc)).


## Examples

* For $n=3$, the [[exceptional isomorphism]] between [[Spin(3)]] and [[SU(2)]] extends to an isomorphism between $Spin^c(3)$ and the [[unitary group]] $U(2)$:
  $$
    Spin^c(3) 
    \;\simeq\; 
    U(2)
  $$
over the exceptional isomorphism [[SO(3)|$SO(3) \simeq PU(2)$]], as both of these [[quotient groups]] are quotients by the respective [[centers]], both identifiable with the [[circle group]] $U(1)$ ([Ozbagci–Stipsicz 2004](#OzbagciStipsicz) Section 6.2). This isomorphism follows from considering the surjective homomorphism [[SU(2)|$SU(2) \times U(1) \to U(2)$]] given by $(A,z) \mapsto z A$, and noticing its [[kernel]] is precisely $\{\pm(I,1)\}$, hence $U(2)$ satisfies the [[universal property]] defining $Spin^c(3)$ as a quotient.

* For $n=4$, we have 
$$
    Spin^c(4) 
      = \big(SU(2)\times SU(2)\times U(1)\big) / \{\pm(I,I,1)\} 
      \simeq U(2)\times_{U(1)} U(2).  
$$
This latter group is the [[fibre product]] of groups over $U(1)$, namely $\{(A,B)\in U(2)\times U(2)\mid \det(A) = \det(B)\}$ ([Ozbagci–Stipsicz 2004](#OzbagciStipsicz) Section 6.3). The construction can be seen by considering the surjective homomorphism
$$
    SU(2) \times SU(2) \times U(1) 
     \to SU(2) \times SU(2) \times U(1) \times U(2) 
      \to U(2) \times U(2)
$$
defined by $(A,B,z) \mapsto (z A,z B)$, which has image $U(2)\times_{U(1)} U(2)$. Similarly to the case of $Spin^c(3)$, the kernel consists of triples $(A,B,z)$ such that $z A = I = z B$, hence that $A = B = (1/z) I$. Since $\det(A) = 1/z^2 = 1$, we must have $z=\pm 1$, and hence $A=B=\pm I$ with the same sign as $z$. Thus the kernel is precisely $\{\pm(I,I,1)\}$, and so again by the universal property we get the isomorphism as stated.

  The [[Spin(4)|$Spin(4)$]] subgroup can be seen as the subgroup of pairs of unitary matrices with both of them having determinant 1.

* Using the exceptional isomorphism [[Spin(6)|$Spin(6) \simeq SU(4)$]], and the multiplication map $SU(4)\times U(1) \to U(4)$ analogous to the above, it can be seen that the group $Spin^c(6)$ is the connected [[double cover]] of $U(4)$ corresponding to the (unique) index-2 subgroup $2\mathbb{Z} \hookrightarrow \mathbb{Z} \simeq \pi_1(U(4))$. This is because the multiplication map is surjective and has kernel canonically isomorphic to $\mu_4$, the fourth [[roots of unity]], via the map $\mu_4\to SU(4)\times U(1)$ sending $\zeta\mapsto (\zeta^{-1}I,\zeta)$. Hence there are a pair of 2:1 surjective homomorphisms
$$
SU(4) \times U(1) \to Spin^c(6) \to U(4),
$$
and hence the result.

The last two examples can also be considered as [[exceptional isomorphisms]], even if not to one of the more [[classical Lie groups]]. 

## Properties

### Group extension

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

### As the homotopy fiber of the smooth $\mathbf{W}_3$
 {#AsHomotopyFiberOfSmoothW3}

We discuss in the following that 

1. the universal third [[integral Stiefel-Whitney class]] $W_3$ has an essentially unique lift from [[∞Grpd]] $\simeq$ [[Top]] to [[Smooth∞Grpd]];

1. the smooth [[delooping]] $\mathbf{B}Spin^c \in Smooth\infty Grpd$ is the [[homotopy fiber]] of $\mathbf{W}_3$, hence is the [[circle n-bundle|circle 2-bundle]] over $\mathbf{B} SO$ classified by $\mathbf{W}_3$. 



+-- {: .num_prop #SpinCAsHomotopyPullbackOfW2AndC1}
###### Proposition

We have a [[homotopy pullback]] diagram

$$
  \array{
     \mathbf{B} Spin^c 
     &\stackrel{\mathbf{B}det}{\longrightarrow}& 
     \mathbf{B}U(1)
     \\
     \big\downarrow 
     && 
     \big\downarrow{}^{\mathrlap{\mathbf{c}_1 mod 2}}
     \\
     \mathbf{B} SO 
     &\stackrel{\mathbf{w}_2}{\longrightarrow}&
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
  \partial\colon n \mapsto ( n \,mod\, 2 , n)
  \,.
$$

This is equivalent to 

$$
  \begin{aligned}
   (\mathbb{Z} \stackrel{\partial}{\to} Spin \times \mathbb{R})
   & \simeq 
  (\mathbb{Z}_2 \stackrel{\partial'}{\to} Spin \times (\mathbb{R}/2\mathbb{Z}))
   \\
  & \simeq
  (\mathbb{Z}_2 \stackrel{\partial'}{\to} Spin \times U(1))
  \end{aligned}
  \,,
$$

(notice the non-standard identification $U(1) \simeq \mathbb{R}/(2\mathbb{Z})$ here, which is important below in prop. \ref{UniversalDeterminantLineBundleMap} for the identification of $det$)
where now $\partial'$ is the [[diagonal]] embedding of the [[subgroup]]

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

+-- {: .num_prop #UniversalDeterminantLineBundleMap}
###### Proposition

Under the identificaton $Spin^c \simeq Spin \underset{\mathbb{Z}_2}{\times} U(1)$ the "universal [[determinant line bundle]] map"

$$
  det \colon Spin^c \to U(1)
$$

is given in components by

$$
  (g,c) \mapsto 2 c
$$

(where on the right we write the group structure additively).

=--

+-- {: .proof}
###### Proof

By the proof of prop. \ref{SpinCAsHomotopyPullbackOfW2AndC1} the $U(1)$-factor in $Spin^c \simeq Spin \underset{\mathbb{Z}_2}{\times}U(1)$ arises from the identification $U(1) \simeq \mathbb{R}/2\mathbb{Z}$. But under the horizontal map as it appears in the homotopy pullback in that proof this corresponds to multiplication by 2.

=--

+-- {: .num_prop #SmoothRefinementOfBockstein}
###### Proposition


The third _[[integral Stiefel-Whitney class]]_ 

$$
  W_3
   \coloneqq 
  \beta_2 \circ w_2 
   \colon
  B SO \stackrel{w_2}{\to} B^2 \mathbb{Z}_2
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

+-- {: .num_prop #HomotopyFiberOfSmoothBeta2}
###### Proposition

The sequence  

$$
  \mathbf{B} U(1)
    \stackrel{\mathbf{c}_1 mod 2}{\to}
  \mathbf{B}^2 \mathbb{Z}_2 
    \stackrel{\mathbf{\beta}_2}{\to}
  \mathbf{B}^2 U(1)
  \,,
$$

where $\mathbf{\beta}_2$ is the smoothly refined [[Bockstein homomorphism]] from prop. \ref{SmoothRefinementOfBockstein},
is a [[fiber sequence]].


=--

+-- {: .proof}
###### Proof

The homotopy fiber of $\mathbf{B} \mathbb{Z}_2 \to \mathbf{B}U(1)$ is $U(1)/\mathbb{Z}_2 \simeq U(1)$. Thinking of this is $(\mathbb{Z} \stackrel{\cdot 1/2}{\to} \mathbb{R})$ one sees that the inclusion of this fiber is indeed $\mathbf{c}_1 mod 2$.



=--

+-- {: .num_prop}
###### Proposition

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


Then consider the [[pasting diagram]] of [[homotopy pullbacks]]

$$
  \array{
     \mathbf{B}Spin^c 
       &\to& 
     \mathbf{B} U(1)
     &\to&
     {*}
     \\
     \downarrow && \downarrow^{\mathrlap{\mathbf{c}_1 mod 2}} && \downarrow
     \\
     \mathbf{B} SO 
       &\stackrel{\mathbf{w}_2}{\to}&
     \mathbf{B}^2 \mathbb{Z}_2
       &\stackrel{\mathbf{\beta}_2}{\to}&
     \mathbf{B}^2 U(1)
  }
  \,.
$$

The right square is a homotopy pullback by prop. \ref{HomotopyFiberOfSmoothBeta2}.
The left square is a homotopy pullback by 
prop. \ref{SpinCAsHomotopyPullbackOfW2AndC1}.
The bottom composite is the smooth $\mathbf{W}_3$ by prop \ref{SmoothRefinementOfBockstein}. 

This implies by claim by the [[pasting law]].
=--

### Relation to metaplectic group $Mp^c$

There is a direct analogy between [[Spin]], [[Spin^c]] and the [[metaplectic groups]] [[Mp]] and [[Mp^c]] (see there for more).





## Related concepts

* [[spin group]], **$spin^c$-group**, [[spinʰ group]]

* [[spin structure]]

* [[MSpinᶜ]]

* [[spinᶜ structure]], [[twisted spinᶜ structure]]

* [[spinʰ structure]]

* [[string 2-group]], [[string structure]]

* [[stringᶜ 2-group]]

## References


* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], Appendix D in: _[[Spin geometry]]_, Princeton University Press (1989)

For more see the references at _[[spin^c structure]]_.

The [[exceptional isomorphisms]] in low dimension are described in

* {#OzbagciStipsicz} B. Ozbagci, A. I. Stipsicz, _$Spin^c$ Structures on 3- and 4-Manifolds_, in: *Surgery on Contact 3-Manifolds and Stein Surfaces* Bolyai Society Mathematical Studies **13**, Springer (2004) &lbrack;[doi:10.1007/978-3-662-10167-4_6](https://doi.org/10.1007/978-3-662-10167-4_6)&rbrack;


[[!redirects spinᶜ group]]
[[!redirects spinᶜ groups]]
[[!redirects spinᶜ-group]]
[[!redirects spinᶜ-groups]]


[[!redirects spin^c]]
[[!redirects spin^c group]]
[[!redirects spin^c groups]]
[[!redirects spin^c-group]]
[[!redirects spin^c-groups]]

[[!redirects Spin^c]]
[[!redirects Spin^c group]]
[[!redirects Spin^c groups]]
[[!redirects Spin^c-group]]
[[!redirects Spin^c-groups]]


