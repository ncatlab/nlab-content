
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _universal principal ∞-bundle_ over an [[∞-group]]-object in an [[(∞,1)-topos]] $\mathbf{H}$ is a morphism $\mathbf{E}G \to \mathbf{B}G$ in a _1-categorical model_ $C$ for $\mathbf{H}$ (a [[homotopical category]]) such that every $G$-[[principal ∞-bundle]] $P \to X$ in $\mathbf{H}$ is modeled in $C$ by an (ordinary) [[pullback]] of $\mathbf{E}G \to \mathbf{B}G$.

Notice that in the proper [[nLab:(∞,1)-topos]]-context the _universal_ $G$-[[nLab:principal ∞-bundle]] for an [[nLab:∞-group]] $G$ is nothing but the point inclusion $* \to \mathbf{B}G$ into the [[nLab:delooping]] of $G$: every $G$-principal $\infty$-bundle $P \to X$ is the [[(∞,1)-pullback]] 

$$
  \array{
    P &\to& *
    \\
    \downarrow &{}^{\mathllap{\simeq}}\swArrow& \downarrow 
    \\
    X &\stackrel{}{\to}& \mathbf{B}G
  }
$$

of the point in $\mathbf{H}$, namely the [[nLab:homotopy kernel]] of its classifying map $g$. In other words, in a full $(\infty,1)$-categorical context the notion of universal bundle disappears. It is a notion genuinely associated with 1-categorical _models_ for $\mathbf{H}$.

## Standard models

Assume that we have a [[homotopical category]] model $C$ for $\mathbf{H}$ that has the structure of a [[category of fibrant objects]]. Notably this can be the [[full subcategory]] on fibrant objects of a [[model structure on simplicial presheaves]].


### By fibrations

By standard results on [[homotopy pullback]]s every morphism $\mathbf{E}G \to \mathbf{B}'G$ that

1. is a fibration

1. fits into a diagram

   $$
     \array{
       \mathbf{E}G &\stackrel{\simeq}{\to}& *
       \\
       \downarrow && \downarrow
       \\
       \mathbf{B}'G &\stackrel{\simeq}{\to}& \mathbf{B}G
     }
   $$

   with the horizontal morphisms being weak equivalences;

is a model for the universal $G$-principal $\infty$-bundle.

### By path fibrations

A standard construction of a fibration $\mathbf{E}G \to \mathbf{B}G$ is above is obtained as follows: 

by standard results on [[homotopy pullback]]s, we have that the bundle $P \to X$ classified by a morphism $X \stackrel{\simeq}{\leftarrow} \hat X\to \mathbf{B}G$ is given by the [[limit]]

$$
  \array{
     P &\to& &\to& *
     \\
     \downarrow && && \downarrow
     \\
     && (\mathbf{B}G)^I &\stackrel{\simeq}{\to}& \mathbf{B}G
     \\
     \downarrow && \downarrow^{\mathrlap{\simeq}}
     \\
     * &\to& \mathbf{B}G
  }
  \,,
$$

where $(\mathbf{B}G)^I $ is a [[path space object]] for $\mathbf{B}G$.

This limit may be computed as two consecutive [[pullback]]s

$$
  \array{
     P &\to& \mathbf{E}G &\to& *
     \\
     \downarrow && && \downarrow
     \\
     && (\mathbf{B}G)^I &\to& \mathbf{B}G
     \\
     \downarrow && \downarrow
     \\
     * &\to& \mathbf{B}G
  }
  \,.
$$

The intermediate pullback

$$
  \mathbf{E}G := (\mathbf{B}G)^I \times_{\mathbf{B}G} *
$$

is the path fibration over $\mathbf{B}G$. By the [[factorization lemma]] we have that the projecton $\mathbf{E}G \to \mathbf{B}G$ is indeed a fibration and by the fact that the acyclic fibration $(\mathbf{B}G)^I \to \mathbf{B}G$ is preserved under pullback that indeed $\mathbf{E}G \to *$ is a weak equivalence.






### By decalage

For $X$ a [[Kan complex]] with a single vertex, the [[decalage]] construction $Dec X \to X$ is a [[Kan fibration]] that fits into a diagram

$$
  \array{
    Dec X &\stackrel{\simeq}{\to}& * 
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{=}{to}& X
  }
  \,.
$$

For $G$ a [[simplicial group]] the standard simplicial model for the [[delooping]] of $G$ in $\mathbf{H} = $[[∞Grpd]] is denoted $\bar W G$. This is a Kan complex with a single vertex and $Dec \bar W G$ is the standard model for the universal [[simplicial principal bundle]], traditionally written $W G$.

$$
  Dec \bar W G = W G \to \bar W G
  \,.
$$

These constructions are functorial and hence extend to models for [[(∞,1)-topos]]es by a [[model structure on simplicial presheaves]].

The model $W G$ for the universal $G$-principal bundle has the special property that it is a [[groupal model for universal principal ∞-bundles]].



[[!redirects universal principal ∞-bundle]]

[[!redirects universal principal ∞-bundles]]

[[!redirects universal principal infinity-bundles]]

[[!redirects universal principal bundle]]