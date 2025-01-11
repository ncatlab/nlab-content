
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Let $G$ be a finite group.
The [[Wirthmüller isomorphism]] implies that the [[equivariant suspension spectrum|suspension G-spectrum]] of a [[orbit category|transitive G-set]] is $\mathbb{S}_G$-linearly self-dual;
in particular, given a map $[G/K] \rightarrow [G/H]$, self-duality yields a transfer map $\Sigma_{G,+}^\infty [G/H] \rightarrow \Sigma_{G,+}^{\infty} [G/K]$.
This underlies a functor from the [[Burnside category]] into $\mathrm{Sp}_G$;
taking mapping spectra out of $[G/K]$ then yields a functor from $G$-spectra to [[Mackey functors]] valued in spectra:
$$
  F\colon \mathrm{Sp}_G \rightarrow \mathrm{Fun}^{\times}\left(\mathrm{Span}(\mathbb{F}_G), \mathrm{Sp}\right).
$$
The **Spectral Mackey functor theorem** states that $F$ is an equivalence.

## Precise statements
The first proof of the Spectral Mackey functor appeared in [Guillou-May 11](#Guillou). To state it, we write $\mathrm{Sp}_G^{O}$ for the model category of orthogonal $G$-spectra, and $\mathrm{Sp}^O$ for orthogonal spectra.
$\mathrm{Sp}_G^O$ comes enriched over $\mathrm{Sp}^O$, as does the projective model structure on the spectral presheaf category $\mathrm{Fun}_{\mathrm{Sp}^{\mathcal{O}}}(\mathrm{Span}^+(\mathbb{F}_G)^{\op}, \mathrm{Sp}^O)$.
\begin{theorem}
  There is a zigzag of $\mathrm{Sp}^O$-enriched quillen equivalences connecting $\mathrm{Sp}_G^O$ and $\mathrm{Fun}_{\mathrm{Sp}^{\mathcal{O}}}(\mathrm{Span}^+(\mathbb{F}_G)^{\op}, \mathrm{Sp}^O)$.
\end{theorem}

This presents an $\infty$-categorical equivalence, who was later directly proved using $\infty$-categorical means in [Nardin 16](#Nardin).
The strategy is to recognize the [[G-∞-category]] of [[orthogonal G-spectra]] as the $G$-stabilization of [[G-spaces]];
then, one may recognize $G$-stability as equivalent to _naive_ stability and $G$-semiadditivity.
Since each are presented by smashing localizations of the $\infty$-category of presentable $G$-$\infty$-categories, these processes preserve each other;
$G$-semiadditivization of a $G$-category of coefficient systems is computed by [[Mackey functors|(semi)-Mackey functors]], and naive stabilization by stabilization of the value category, so $G$-stabilization of coefficient systems in $\mathcal{C}$ is equivalent to Mackey functors valued in spectrum objects in $\mathcal{C}$.
Said altogether, Nardin proved the following.

\begin{theorem}
  The forgetful $G$-functor $\mathrm{Sp}_G^O[\mathrm{weq}^{-1}] \rightarrow \mathcal{S}_G$ lifts through an equivalence 
$$
  \mathrm{Sp}_G^O[\mathrm{weq}^{-1}] \simeq \mathrm{Fun}^\times \left( \mathrm{Span}(\mathbb{F}_G), \mathrm{Sp} \right).
$$
\end{theorem}


## References

* {#Guillou}[[Bertrand Guillou]], [[Peter May]], _Models of $G$-spectra as presheaves of spectra_ ([ arXiv:1110.3571](https://arxiv.org/abs/1110.3571))

* {#Nardin}[[Denis Nardin]], _Parametrized higher category theory and higher algebra: Exposé IV -- Stability with respect to an orbital \infty-category_ ([arXiv:1608.07704v4](https://arxiv.org/abs/1608.07704v4))