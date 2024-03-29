
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
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

## Statement

For $S$ any [[spectrum]] and $H A$ an [[Eilenberg-MacLane spectrum]],
then the [[smash product of spectra|smash product]] $S\wedge H A$ (the $A$-[[ordinary homology]] spectrum)
is non-canonically equivalent to a product of EM-spectra (hence a [[wedge sum]] of EM-spectra in the finite case).

([Adams 74, part II, lemma 6.1](#Adams74))

A variant for [[generalized (Eilenberg-Steenrod) cohomology]]:

Let $X$ be a [[topological space]] such that each of the [[ordinary homology|ordinary]] [[homology groups]] $H_n(X,\mathbb{Z})$ is a [[free abelian group]] on genrators $\{h_{\alpha,n}\}_{\alpha \in B_n}$. Write $c_{\alpha,n} \in H^n(X,\mathbb{Z}) \simeq Hom(H_n(X,\mathbb{Z}), \mathbb{Z})$ for the corresponding [[dual basis]].

Let $E$ be a [[multiplicative cohomology theory]] and write $h'_{n,\alpha} \in (\tau_{\leq 0} E)_n(X)$ and $c'_{n,\aloha} \in (\tau_{\leq 0} E)^n(X) $for the images of these generators under the [[0-truncated]] unit map 

$$
  H \mathbb{Z} \simeq \tau_{\leq 0} \mathbb{S} \stackrel{}{\longrightarrow} \tau_{\leq 0} E
  \,.
$$

+-- {: .num_prop #WhenGeneralizedHomologySpectraSplit}
###### Proposition

If one of the following conditions is satisfied

* Each $h'_{n,\alpha}$ lifts through $E_n(X) \to (\tau_{\leq 0}E)_n(X)$;

* each $H_n(X,\mathbb{Z})$ is [[finitely generated module|finitely generated]] and each $c'_{n,\alpha}$ lifts through $E^n(X) \to (\tau_{\leq 0}E)^n(X)$, 

then there are non-canonical [[equivalence in an (infinity,1)-category|equivalences]] as follows:

1. $E \wedge \Sigma^\infty X_+ \simeq \underset{n,\alpha}{\vee} \Sigma^n E \;\; \in E Mod$ ;

1. $[X,E] \simeq \underset{n,\alpha}{\prod} \Sigma^{-n} E$;

1. $E_\bullet(X) \simeq \pi_\bullet(E) \otimes H_\bullet(X,\mathbb{Z})$

   and

   $E^\bullet(X)\simeq Hom(H_\bullet(X), \pi_\bullet(E))$


=--

([Lurie 10, lecture 4, prop. 7](#Lurie10), [Adams 74, part II, lemma 2.5](#Adams74))

## Related concepts

* [[splitting principle]]

## References

* {#Adams74} [[Frank Adams]], _[[Stable homotopy and generalised homology]]_, 1974

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010 ([web](http://www.math.harvard.edu/~lurie/252x.html)), Lecture 4 _[[complex oriented cohomology theory|Complex-oriented cohomology theories]]_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf))

[[!redirects homology spectra that split]]

[[!redirects homology spectra split]]
