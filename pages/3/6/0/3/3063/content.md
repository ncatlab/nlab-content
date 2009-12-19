
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _inner automorphism 2-group_ of a [[group]] is essentially the sub-[[2-group]] of the [[automorphism 2-group]] $AUT(G)$ of $G$ of those automorphisms that are connected by a [[transfor|transformation]] to the identity: this makes the automorphism necessarily an [[inner automorphism]].

In fact, more precisely the inner automorphism 2-group is the 2-group of these connecting transformations, i.e. it remembers the group element and the inner automorphism that it induces under conjugation.

## Definition

Let $G$ be a [[group]]. Write $\mathbf{B}G$ for its [[delooping]]. 

The **inner automorphism 2-group** $INN(G)$ of $G$ is the [[strict 2-group]]

* whose [[object]]s are diagrams

  $$
    \array{
      & \nearrow \searrow^{\mathrlap{Id}}
      \\ 
      \mathbf{B}G
      &\Downarrow^{\eta}&
      \mathbf{B}G
      \\
      & \searrow \nearrow_{\mathrlap{\alpha}}
    }
  $$

  in [[Grpd]]. 

* morphisms $\kappa : (\eta_1, \alpha_1) \to (\eta_2, \alpha_2)$ are commuting triangles of transformations

  $$  
    \array{
       && Id
       \\
       & {}^{\mathllap{\eta_1}}\swArrow && \seArrow^{\mathrlap{\eta_2}}
       \\
       \alpha_1 &&\stackrel{\kappa}{\Rightarrow}&&
       \alpha_2
    }
  $$

Equivalently, this is the [[action groupoid]]

$$
  INN(G) = G//G =: \mathbf{E}G
$$

of $G$ acting on itself.

Equivalently , this is the [[strict 2-group]] corresponding to the [[crossed module]] 

$$
  [INN(G)] =
  \left(
    G \stackrel{Id}{\to} G
  \right)
$$

with action $G \to Aut(G)$ given by right multiplication in $G$.

This makes it evident that $INN(G)$ is contractible

$$
  \mathbf{B} INN(G) \stackrel{\simeq}{\to} {*}
  \,.
$$

In fact, we may think of $INN(G)$ as the [[generalized universal bundle|universal]] $G$-[[principal bundle]] in its incarnation in [[Grpd]] (as opposed to the more tradition incarnation in [[Top]], to which it is [[Quillen equivalence|Quillen equivalent]] by the [[homotopy hypothesis]] theorem).

To emphasize this we also write

$$
  \mathbf{E}G := INN(G)
  \,.
$$

We have a natural sequence of groupoids

$$
  G \to \mathbf{E}G \to \mathbf{B}G
  \,.
$$

It is an old theorem by [[Graeme Segal]] that under [[nerve]] followed by [[geometric realization]] this maps to the sequence of [[topological space]]s

$$
  G \to \mathcal{E} G \to \mathcal{B}G
$$

that is the universal $G$-bundle over the [[classifying space]] $\mathcal{B}G$ in its incarnation in [[Top]].


The 2-group structure on $INN(G)$ is evident, and hence makes the fact evident that the universal $G$-bundle itself carries a group structure, which is compatibel with the group structure, in that the morphism $ G \to \mathbf{E}G$ [[delooping|deloops]] to a morphism

$$
  \mathbf{B}G \to \mathbf{B} \mathbf{E}G
  \,.
$$

This fact is useful in various applications in [[nonabelian cohomology]].

