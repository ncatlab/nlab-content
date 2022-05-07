
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

One of the basic facts of [[category theory]] is that [[left adjoint|left]]/[[right adjoint|right]] [[adjoint functors]] [[preserved limit|preserves]] [[colimits|co]]/[[limits]], respectively.

## Statement

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]] and let

$$
  (L \dashv R)
  \;\colon\;
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

be a pair of [[adjoint functors]] between them.

Then 

1. If $X \colon \mathcal{I} \to \mathcal{C}$ is a [[diagram]] whose [[limit]] $\underset{\longleftarrow}{\lim}_{i} X_i$ exists in $\mathcal{C}$, then this limit is preserved by the [[right adjoint]] $R$ in that there is a [[natural isomorphism]]

   $$
     R 
     \left(
       \underset{\longleftarrow}{\lim}_i \left(X_i\right)
     \right)
     \;\simeq\;
     \underset{\longleftarrow}{\lim}_i \left( R(X_i) \right)
     \,,
   $$

   where on the right we have the [[limit]] in $\mathcal{D}$ over the [[diagram]] $R \circ X \colon \mathcal{I} \overset{X}{\longrightarrow} \mathcal{C} \overset{R}{\longrightarrow} \mathcal{D}$.

1. If $X \colon \mathcal{I} \to \mathcal{D}$ is a [[diagram]] whose [[colimit]] $\underset{\longrightarrow}{\lim}_{i} X_i$ exists in $\mathcal{D}$, then this colimit is preserved by the [[left adjoint]] $l$ in that there is a [[natural isomorphism]]

   $$
     L
     \left(
       \underset{\longrightarrow}{\lim}_i \left(X_i\right)
     \right)
     \;\simeq\;
     \underset{\longrightarrow}{\lim}_i \left( L(X_i) \right)
     \,,
   $$

   where on the right we have the [[colimit]] in $\mathcal{C}$ over the [[diagram]] $L \circ X \colon \mathcal{I} \overset{X}{\longrightarrow} \mathcal{D} \overset{L}{\longrightarrow} \mathcal{C}$.


=--

+-- {: .proof}
###### Proof

We show the first statement, the proof of the second is [[formal dual|formally dual]].

We use the following facts

1. There is a [[natural isomorphism]], $Hom_{\mathcal{C}}(L(d),c) \simeq Hom_{\mathcal{D}}(d,R(c))$; this equivalently characterizes the fact that $(L \dashv R)$ is a pair of [[adjoint functors]];

1. ([[hom-functor preserves limits]]) The [[hom-functor]] sends colimits in the first argument and limits in the second argument to limits of [[hom-sets]]

   $$
      Hom\left( X, \underset{\longleftarrow}{\lim}_i X_i \right)
     \simeq
     \underset{\longleftarrow}{\lim}_i Hom\left(X,X_i\right)
   $$

   and

   $$
     Hom\left(\underset{\longrightarrow}{\lim}_i X_i, X\right)
     \simeq
     \underset{\longleftarrow}{\lim} \left(Hom\left(X_i,X\right) \right)
     \,.
   $$
  
   Again, this is essentially by definition of [[limits]]/[[colimits]].

1. ([[Yoneda lemma]]) If for two objects $X$ and $Y$ in some [[category]] the [[hom-sets]] out of or into these objects (their [[representable functors]]) are [[naturally isomorphic]], then the two objects are isomorphic.

Now using the first two items, we obtain the following chain of [[natural isomorphisms]], for every [[object]] $Y \in \mathcal{D}$:

$$
  \begin{aligned}
    Hom_{\mathcal{D}}\left( Y, R \left( \underset{\longleftarrow}{\lim}_i X_i \right) \right)
    & \simeq 
    Hom_{\mathcal{C}}\left( L(Y), \underset{\longleftarrow}{\lim}_i X_i\right)
    \\
    & \simeq
    \underset{\longleftarrow}{\lim}_i \left( Hom_{\mathcal{C}}\left(L\left(Y\right), X_i\right)\right)
    \\
    & \simeq
    \underset{\longleftarrow}{\lim}_i \left(Hom_{\mathcal{D}}\left(Y, R\left(X_i\right)\right)\right)
    \\
    & \simeq
    Hom_{\mathcal{D}}\left(Y, \underset{\longleftarrow}{\lim}_i \left(R\left(X_i\right) \right) \right)
  \end{aligned}
  \,.
$$

Hence the third item above, the [[Yoneda lemma]], implies the claim.

=--


## Related entries

* [[hom-functor preserves limits]]

* [[limits preserve limits]]

* [[limits of presheaves are computed objectwise]]

* [[interactions of images and pre-images with unions and intersections]]

* [[limits and colimits by example]]


[[!redirects left adjoints preserve colimits and right adjoints preserve limits]]
[[!redirects right adjoints preserve limits and left adjoints preserve colimits]]

[[!redirects left adjoints preserve colimits]]
[[!redirects right adjoints preserve limits]]


