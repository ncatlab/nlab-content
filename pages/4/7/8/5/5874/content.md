
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[bundle gerbe]] or [[circle n-bundle with connection|circle 2-bundle]] has a unique [[characteristic class]] in [[integral cohomology]] in degree 3, the higher analog of the [[Chern class]] of a [[circle group]]-[[principal bundle]] (or complex [[line bundle]]): this is called the **Dixmier-Douady class** of the [[bundle gerbe]].

## Definition

In the literature one find a universal Dixmier-Douady class defined for different entities, notably for [[projective unitary group|projective unitary]]-[[principal bundles]] and for $U(1)$-[[bundle gerbes]], as well as for [[C-star algebra]] constructions related to these. All these notions are equivalent in one sense, namely in bare [[homotopy theory]], but differ in other sense, namely in geometric homotopy theory. 


### In bare homotopy-type theory

The [[classifying space]] of the [[circle n-group|circle 2-group]] $\mathbf{B}U(1)$ is an [[Eilenberg-MacLane space]] $B \mathbf{B} U(1) \simeq B^3 \mathbb{Z} \simeq K(\mathbb{Z}, 3)$.
The bare _Dixmier-Douday class_ is the [[universal characteristic class]] 

$$
  DD : B B U(1) \stackrel{\simeq}{\to} K(\mathbb{Z}, 3)
$$

exhibited by this equivalence. Hence if we identify $B B U(1)$ with $K(\mathbb{Z}, 3)$, then the DD-class is the _identity_ on this space.

This is directly analogous to how the [[first Chern class]] is, as a [[universal characteristic class]], the identity on $K(\mathbb{Z},2) \simeq B U(1)$.

This means conversely that the [[equivalence class]] of a $U(1)$-[[bundle gerbe]]/[[circle n-bundle with connection|circle 2-bundle]] is entirely characterized by its Dixmier-Douady class.

### In smooth homotopy-type theory

The [[circle 2-group]] $\mathbf{B}U(1)$ naturally carries a _smooth_ structure, hence is naturally regarded not just as an [[∞-group]] in [[∞Grpd]], but as a [[smooth ∞-group]] in $\mathbf{H} \coloneqq$ [[Smooth∞Grpd]].

For each $n$, the [[central extension]] of Lie groups

$$
  U(1) \to U(n) \to PU(n)
$$

that exhibits the [[unitary group]] as a [[circle group]]-extension of the [[projective unitary group]] induces the corresponding morphism of smooth [[moduli stacks]]

$$
  \mathbf{B} U(1) \to \mathbf{B} U(n) \to \mathbf{B} PU(n)
$$

in $\mathbf{H}$.

This is part of a [[fiber sequence|long fiber sequence]] in $\mathbf{H}$ which continues to the right by a [[connecting homomorphism]] $\mathbf{dd}_n$

$$
  \mathbf{B} U(1) \to \mathbf{B} U(n) \to \mathbf{B} PU(n)
   \stackrel{\mathbf{dd}_n}{\to}
  \mathbf{B}^2 U(1)
$$

in $\mathbf{H}$. Here the last morphism is presented in 
[[simplicial presheaves]] by the zig-zag/[[∞-anafunctor]] of sheaves of [[crossed modules]]

$$
  \array{
     [U(1) \to U(n)] &\to& [U(1) \to 1]   
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     PU(n)
  }
  \,.
$$

To get rid of the dependence on the rank $n$ -- to _stabilize_ the rank -- 
we may form the [[directed colimit]] of smooth moduli stacks

$$
  \mathbf{B}U \coloneqq \underset{\rightarrow_n}{\lim} \mathbf{B} U(n)
$$

$$
  \mathbf{B} PU \coloneqq \underset{\rightarrow_n}{\lim} \mathbf{B} PU(n)
  \,.
$$

On these we have the smooth universal class

$$
  \mathbf{dd} : \mathbf{B} PU \to \mathbf{B}^2 U(1)
  \,.
$$

Since the [[(∞,1)-topos]] [[Smooth∞Grpd]] has [[universal colimits]], it follows that there is a [[fiber sequence]]

$$
  \array{
    \mathbf{B}U &\to& \mathbf{B} PU
    \\
    && \downarrow^{\mathbf{dd}}
    \\
    && \mathbf{B}^2 U(1)
  }
$$


exhibiting the moduli stack of smooth stable unitary bundles as the homotopy fiber of $\mathbf{dd}$.


## References
 {#References}

* [[Jacques Dixmier]], [[Adrien Douady]], _Champs continus d'espaces hilbertiens et de $C^*$-algebres_, Bull. Soc. Math. France **91** (1963) 227-284 &lbrack;[numdam:10.24033/bsmf.1596](http://www.numdam.org/articles/10.24033/bsmf.1596), [pdf](http://www.numdam.org/item/10.24033/bsmf.1596.pdf)&rbrack;

* [[Jacques Dixmier]], _Les $C^*$--algébres et leurs représentations, Gauthier--Villars (1969)


[[!redirects Dixmier-Douady classes]]

