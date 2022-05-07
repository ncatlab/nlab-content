
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Definition ##

Let $(X, \mathcal{O}_X)$ be a [[ringed space]].  Consider the [[sheaf|subsheaf]] of [[sets]] $\mathcal{S} \subset \mathcal{O}_X$ of the [[structure sheaf]] such that for each [[open subset]] $U \subset X$, $\Gamma(U, \mathcal{S})$ consists of only the regular sections of $\mathcal{O}_X$ over $U$, i.e. those elements $s\in\Gamma(U, \mathcal{O}_X)$ for which $s|_V f=0$ implies $f=0$ for all $f\in\Gamma(V,\mathcal{O}_X)$ for all opens $V\subseteq X$.  Consider the [[presheaf]] of rings on $X$
  \[ U \quad\mapsto\quad \Gamma(U, \mathcal{O}_X)[\Gamma(U, \mathcal{S})^{-1}] \]
which assigns to $U$ the [[ring of fractions]] of $\Gamma(U, \mathcal{O}_X)$ with denominators in $\Gamma(U, \mathcal{S})$; its [[sheafification]] $\mathcal{M}_X$ is called the **sheaf of ([[germs]] of) [[meromorphic functions]] on $X$**.  The sections of $\mathcal{M}_X$ over $X$ are called the **meromorphic functions on X** and we denote this ring $M(X) = \Gamma(X, \mathcal{M}_X)$.

## Properties ##

+-- {: .num_prop}
###### Proposition

For every open subset $U \subset X$ there is a canonical [[isomorphism]] between $\mathcal{M}_U$ and the restriction of $\mathcal{M}_X$ to $U$.

=--

+-- {: .num_prop}
###### Proposition

For every point $x \in X$ there is a canonical isomorphism between the stalk $\mathcal{M}_{X,x}$ and $\mathcal{O}_{X,x}[\mathcal{S}_x^{-1}]$.

=--

## References ##

* [[Alexander Grothendieck]], [[Jean Dieudonné]], _[[EGA]]_ (IV, 20.1).

* [[Stacks Project]], [sheaf of meromorphic functions and sections](http://stacks.math.columbia.edu/tag/01X1), tag 01X1.

* Steven L. Kleiman, Misconceptions about $K_X$, *L’Enseignement Mathématique* **25** (1979), 203–206 ([doi:10.5169/seals-50379](http://doi.org/10.5169/seals-50379))

category: sheaf theory, algebraic geometry
[[!redirects sheaf of germs of meromorphic functions]]