
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $A$ an [[abelian ∞-group]] write $E \coloneqq \mathbb{S}[A] = \Sigma^\infty_+ A$ for its [[∞-group E-∞ ring]]. 

+-- {: .num_defn}
###### Definition

For $\beta \in \pi_n(E)$ an element of the $n$th stable [[homotopy group]], then _multiplication by $\beta$_ is a homomorphism

$$
  \beta_\ast
  \;\colon\;
  E 
  \to
  \Sigma^{-n} E
  \,.
$$

The _localization_ of $E$ at $\beta$ is the [[homotopy colimit]] over the iterated multiplication with $\beta$

$$
  E[\beta^{-1}]
  \coloneqq
  \underset{\to}{\lim}
  \left[
    E \stackrel{\beta_\ast}{\to}
    \Sigma^{-n}E 
    \stackrel{\Sigma^{-n} \beta_\ast}{\to}
   \Sigma^{-2n} E
   \to
   \cdots
  \right]
$$

which has the [[universal property]] that $\mu_\beta$ becomes an [[equivalence]] on $E[\beta^{-1}]$.

=--



**Snaith's theorem** asserts that 

+-- {: .num_theorem}
###### Theorem

1. the [[K-theory spectrum]] for [[complex K-theory]] is the [[∞-group ∞-ring]] of the [[circle 2-group]] localized at the [[Bott element]] $\beta$:

   $$
     KU \simeq (\mathbb{S}[B U(1)])[\beta^{-1}]
     \,;
   $$

1. the [[periodic complex cobordism spectrum]] is the [[∞-group ∞-ring]] of the [[classifying space]] for stable [[complex vector bundles]] (the classifying space for [[topological K-theory]]) localized at the [[Bott element]] $\beta$:

   $$
     PMU \simeq (\mathbb{S}[B U])[\beta^{-1}]
     \,.
   $$

=--
 
([Snaith 79](#Snaith79))

+-- {: .num_remark}
###### Remark

The analog of this result for the periodic [[algebraic cobordism spectrum]] and [[algebraic K-theory]] is discussed in ([GepnerSnaith 08](#GepnerSnaith08)).

=--

## References

The theorem is due to 

* [[Victor Snaith]], _Algebraic Cobordism and K-theory_, Mem. Amer. Math. Soc. no 221 (1979)
 {#Snaith79}

with a simpler proof given in 

* [[Victor Snaith]], _Localized stable homotopy of some classifying spaces_, Math. Proc. Cambridge Philos. Soc. 89 (1981), no. 2,
325-330. MR 600247 (82g:55006)

Another proof due to [[Mike Hopkins]] is in 

* [[Akhil Mathew]], _Snaith's construction of complex K-theory_, ([pdf](http://people.fas.harvard.edu/~amathew/snaith.pdf))

A version for [[algebraic K-theory]] is discussed in 

* [[David Gepner]], [[Victor Snaith]], _On the motivic spectra representing algebraic cobordism and algebraic K-theory_, Documenta Math.  2008 ([arXiv:0712.2817](http://arxiv.org/abs/0712.2817))
 {#GepnerSnaith08}

and for [[motivic cohomology]] in 

* [[Markus Spitzweck]], [[Paul Arne Østvær]], _The Bott inverted infinite projective space is homotopy algebraic K-theory_ ([pdf](http://folk.uio.no/paularne/bott.pdf))

Higher [[chromatic homotopy theory|chromatic]] analogs for [[Morava E-theory]] are discussed in 

* [[Craig Westerland]], _A higher chromatic analogue of the image of J_ ([arXiv:1210.2472](http://arxiv.org/abs/1210.2472))


[[!redirects Snaith's theorem]]

