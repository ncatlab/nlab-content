
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A _projective representation_ of a [[group]] $G$ is a [[representation]] up to a central term: a [[group]] [[homomorphism]] $G\longrightarrow PGL(V)$, to the [[projective general linear group]] of some $\mathbb{K}$-[[vector space]] $V$. 

## Properties
 {#Properties}

### The group extension and its cocycle
 {#GroupExtensionAndCocycle}

By construction, there is a [[short exact sequence]]

$$
  1 \to \mathbb{K}^\times \longrightarrow GL(V) \longrightarrow PGL(V)\to 1
$$

which exhibits $GL(V)$ as a [[group extension]] of $PGL(V)$ by the [[group of units]] $\mathbb{K}^\times$ of the [[ground field]]. This is classified by a 2-[[cocycle]] $c$ in [[group cohomology]] $H^2_{Grp}(PGL(V),\mathbb{K}^\times)$. 

It is useful to re-express this equivalently in terms of [[homotopy theory]] via the discussion at [[looping and delooping]], by which [[group]] [[homomorphisms]] $\phi \colon G\longrightarrow H$ are equivalently maps $\mathbf{B}\phi \colon \mathbf{B}G\longrightarrow \mathbf{B}H$ between their [[delooping]] [[groupoids]].

In terms of this the above [[group extension]] and its classifying cocycle is exhibited by a [[homotopy fiber sequence]] of [[deloopings]] of the form

$$
 \array{
    \mathbf{B}\mathbb{K}^*& \longrightarrow & \mathbf{B}GL(V) &\longrightarrow& \ast
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \ast &\longrightarrow&\mathbf{B}PGL(V) &\stackrel{c}{\longrightarrow}& \mathbf{B}^2 \mathbb{K}^\times
}
  \,.
$$

### Relation to genuine representations
 {#RelationToGenuineRepresentations}

Via the projection $GL(V)\to PGL(V)=GL(V)/\mathbb{K}^\times$, every linear representation of $G$ induces a projective representation. 

By the [[universal property]] of the [[homotopy pullback]], the discussion [above](#GroupExtensionAndCocycle) means that the [[obstruction]] to lift a given projective representation $\mathbf{B}\rho \colon \mathbf{B}G\longrightarrow \mathbf{B} PGL(V)$ to a linear representation $\hat \rho$

$$
 \array{
    &  & \mathbf{B}GL(V) &\longrightarrow& \ast
    \\
    & {}^{\mathllap{\mathbf{B}\hat \rho}}\nearrow & \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\mathbf{B}\rho}{\longrightarrow}&\mathbf{B}PGL(V) &\stackrel{c}{\longrightarrow}& \mathbf{B}^2 \mathbb{K}^\times
}
$$

is the class of the 2-[[cocycle]] $c(\rho)\coloneqq c \circ \mathbf{B}\rho$ in  the [[group cohomology]] class $H^2_{Grp}(G,\mathbb{K}^\times)$.

### As twisted linear representations

By the [above](#GroupExtensionAndCocycle) and the discussion at _[group extension -- Central group extensions -- Formulation in homotopy theory](group+extension#FormulationInHomotopyTheory)_ the cocycle map $\mathbf{B}c \colon \mathbf{B}PGL(V)\to \mathbf{B}^2 \mathbb{K}^\times$ of [[homotopy types]] may be represented by a [[zigzag]] ("[[infinity-anafunctor|2-anafunctor]]") of [[crossed complexes]] as 

$$
  \array{
    \mathbf{B}(\mathbb{K}^\times \to GL(V)) &\longrightarrow& \mathbf{B}(\mathbb{K}^\times \to 1) 
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathbf{B}PGL(V)
  }
  \,.
$$

Here the [[2-groupoid]] $\mathbf{B}(\mathbb{K}^\times \to GL(V))$ looks schematically like

$$
  \left\{   
     \array{
       && \ast
       \\
       & {}^{\mathllap{p_1}}\nearrow &\Downarrow^{\mathrlap{k}}& \searrow^{\mathrlap{p_2}}
       \\
       \ast && \underset{k p_1 p_2}{\longrightarrow}&& \ast
     }
  \right\}
$$

This shows that a map $\mathbf{B}G\to \mathbf{B}PGL(V)$ may equivalently be represented by two [[functions]] (not group homomorphisms in general!)

1. $\rho \colon G\to GL(V)$ 

1.  $\lambda \colon G\times G\to \mathbb{K}^\times$ 

such that for all $g,h \in G$ 

1.  $\rho(g)\rho(h)=\lambda(g,h)\rho(g h)$

1. $\lambda$ is a [[group cohomology|group 2-cocycle]] on $G$ with values in $\mathbb{K}^*$ representing the above cohomology class of $c_\rho$.

This is the form in which projective representations are often discussed in the literature.

### As genuine representations after extensions

Alternatively, one may consider the [above](#RelationToGenuineRepresentations) diagram 

$$
 \array{
    &  & \mathbf{B}GL(V) &\longrightarrow& \ast
    \\
    & & \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\mathbf{B}\rho}{\longrightarrow}&\mathbf{B}PGL(V) &\stackrel{c}{\longrightarrow}& \mathbf{B}^2 \mathbb{K}^\times
}
$$

and form the further [[pullback]] along $\mathbf{B}\rho$. By the [[pasting law]] this is (the [[delooping]] of) the [[group extension]] $\hat G$ of $G$ which is classified by $c(\rho)$:

$$
 \array{
    \mathbf{B}\hat G  & \stackrel{\mathbf{B}\tilde \rho}{\longrightarrow} & \mathbf{B}GL(V) &\longrightarrow& \ast
    \\
    \downarrow & & \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\mathbf{B}\rho}{\longrightarrow}&\mathbf{B}PGL(V) &\stackrel{c}{\longrightarrow}& \mathbf{B}^2 \mathbb{K}^\times
}
$$

This way the projective representation $\rho$ of $G$ induces a genuine linear representation $\tilde \rho$ of $\hat G$. One finds (this is a special case of the general discussion at [[twisted infinity-bundle]]) that this constitutes an equivalence between projective representations of $G$ and genuine representations of $\hat G$.

## Related concepts

* [[projectively flat connection]] 

## References

(...)

Relation to [[twisted equivariant K-theory]]:


* José Manuel Gómez, Johana Ramírez, _A Decomposition of twisted equivariant K-theory_ ([arXiv:2001.02164](https://arxiv.org/abs/2001.02164))

[[!redirects projective representations]]