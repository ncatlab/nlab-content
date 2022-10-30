
#Contents#
* autoamtic table of contents goes here
{:toc}

## Motivation

Let $X$ be a [[smooth manifold]], Write $L X = C^\infty(S^1,X)$
for the [[free loop space object|free loop space]].

then [[transgression]] gives a map on [[cohomology]]

$$
  \tau : H^k(X) \to H^{k-1}(L X)
$$ 

**Example**

$\mathbb{Z}_2$-coefficients, $k = 2$

$$
  \array{
     H^2(X, \mathbb{Z}_2) &\stackrel{\tau}{\to}& H^1(L X, \mathbb{Z}_2)
     \\
     \xi &\mapsto& \tau(\xi)
  }
$$

where $\xi$ is the second [[Stiefel-Whitney class]] we have that $X$ has  [[spin structure]] precisely if $\xi = 0$ is the trivial class.
This implies of course that also $\tau(\xi)$ vanishes. Atiyah showed that if 
the [[fundamental group]] $\pi_1(X) = 1$ of $X$ vanishes, i.e. if $X$ is a
[[simply connected space]], that the also the converse holds: $X$ is spin if
$\tau(\xi)$ vanishes in the cohomology of the loop space.

**Questions** 

1. What is the relation between $\xi$ and $\tau(\xi)$ in general, that would make $\tau$ 
   a bijection.
   
1. What are relation between trivializations of $\xi$ and those of $\tau(\xi)$
   that would make $\tau$ a [[functor]] -- such that this makes transgression
   an [[equivalence of categories]].

## Transgression as a functor 

Let $A$ be an [[abelian group|abelian]] [[Lie group]]. Write $H^2(X,A)$ for the 
[[abelian sheaf cohomology]].

we want to realize this as the connected components of a [[2-groupoid]]
$Grb_A^\nabla(X)$ of [[bundle gerbe]]s with connection on $X$.

Similarly we want to refine $H^1(L X, A)$ to a groupoid $Bun_A^\nabla(L X)$
of [[connection on a bundle|connections]] on smooth $A$-[[principal bundle]]s.

[[Jean-Luc Brylinski]] and MacLaughlin define a [[functor]]

$$
   L : Grb_{A}^\nabla(X) \to Bun_A^\nabla(L X)
   \,.
$$

by

$$
  \mathcal{G} \mapsto L \mathcal{G}|_{\beta}
   :=
   Hom_{Grb_A^\nabla(S^1)}(\beta^* \mathcal{G}, I_0)
$$

for $\beta \in L X$ and where $I_0$ denotes the trivial gerbe on the circle.

We want to understand the image of this transgression map, i.e. to characterize those bundles over $L X$ that can be obtained by transgression of a gerbe on $X$.

**Definition** Let $P$ be an $A$-[[principal bundle]] over $L X$, then 
a **fusion product** on $P$ is a bundle [[isomorphism]] $\lambda$
that is [[fiber]]wise given for a triple of paths

$$
  \gamma_i : x \to y \,,\;\;\;\;\; i \in \{1,2,3\}
$$

$$
  \lambda_{\gamma_1, \gamma_2,\gamma_3}
  :
  P_{\bar\gamma_2 \star \gamma_1}
  \otimes
  P_{\bar \gamma_3 \star \gamma_2}
  \to 
  P_{\bar \gamma_3 \star \gamma_1}
$$

Brylinske-MacLaughlin have a similar fusion product but over figur-8s of paths.
This however gives associativity only up to homotopy. Here we are aiming for
a product that is strictly associative.

**Definition** A connection on the fusion  bundle $(P,\lambda)$ is called

1. **compactible** if $\lambda$ is connection-preserving;

1. **symmetrizing**, if

   $$
     R_\pi(\lambda(q_1 \otimes q_2))
     =
     \lambda(R_\pi(q_2) \otimes R_\pi(q_1))
     \,,
   $$
   
   where $R_\pi$ is a lift of the 

   $$
     \array{
       P &\stackrel{}{\to}& P
       \\
       \downarrow && \downarrow
       \\
       L X &\stackrel{r_\pi}{\to}& L X
     }
   $$ 

   lifts the loop rotation operation by an angle $\pi$ from loop space to the bundle
   over loop space.
   
   We can take $R$ to be the [[parallel transport]] of the connection on loop space
   along the canonical path in loop space that connects a loop to its rotated loop.
   
1. **superficial** (German: _oberfl&#228;chlich_ -- this is a joke with translations)
   if it behaves like a surface holonomy in that
   
   1. if $\phi \in L L X$, $\tilde \phi : S^1 \times S^1 \to X$ has rank one, then
      $Hol_P(\phi) = 1$;
      
   1. if $\phi_1, \phi_2  \in L L X$ such that $\tilde \phi_1, \tilde \phi_2$
      are rank-2-homotopic (i.e. think homotopic) then $Hol_p(\phi_1) = Hol_p(\phi_2)$.
      
**Definition** An $A$-**fusion bundle** with connection over $L X$ is an 
$A$-[[nLab:principal bundle]] over $L X$ with fusion product and compatible, 
symmetrizing and superficial connection.

**Lemma** Transgression lifts

$$
  \array{
    Grb_A^\nabla(X) &&\stackrel{\tilde K}{\to}&&
    FusBund_A^\nabla(L X)
    \\
    & {}_{\mathllap{L}}\searrow && \swarrow_{\mathrlap{forget}}
    \\
    && Bun_A^\nabla(L X)
  }
$$

**Theorem** Lifted transgression $\tilde L$ is an equivalence of categories


## Application: Spin structures and loop space orientation

Assume $\mathcal{G}$ is the $\mathbb{Z}_2$-[[lifting gerbe]] for [[spin structure]] on $X$ whose characteristic class is 

$$
  [\mathcal{G}] = \xi \in H^3(X, \mathbb{Z}_2)
$$

the [[Steifel-Whitney class]] of $X$. So [[spin structure]]s on $X$ are in corresppndence with trivializations of $\mathcal{G}$.

On the other hand we have that [[orientation]]s of $L X$ correspond to [[section]]s of $L \mathcal{G}$. Inside there are the fusion preserving sections, which by the above are equivalent to trivializations of $\mathcal{G}$.

So we find that in general [[spin structure]]s on $X$ are not in bijection to just all orientations of $L X$, but precisely ot the fusion-compatible ones.


##References

* [[Konrad Waldorf]], _Transgression to Loop Spaces and its Inverse_

  _I: Diffeological Bundles and Fusion Maps _ ([arXiv:0911.3212](http://arxiv.org/abs/0911.3212))

  _II: Gerbes and Fusion Bundles with Connection_ ([arXiv:1004.0031](http://arxiv.org/abs/1004.0031))