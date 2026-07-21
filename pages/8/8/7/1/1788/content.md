> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.




***

&ouml;

## Idea

The notion of *categorical spectra* is the full [[categorification]] of that of ([[Omega-spectrum|Omega]]-) [[spectra]] of [[topological spaces|spaces]]/[[infinity-groupoids|$\infty$-groupoids]], hence the generalization of *spectra* from [[(infinity,0)-categories|$(\infty,0)$-categories]] to [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]]:


A categorical spectrum is an [[natural numbers|$\mathbb{N}$]]-[[indexed set]] of [[pointed object|pointed]] [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]] $(\mathcal{C}_n, X_n)_{n \in \mathbb{N}}$ such that each stage is equivalent to the [[endomorphism monoid|endomorphism]] object of the next stage:

$$
  \mathcal{C}_n \simeq End_{\mathcal{C}_{n+1}}(X_{n+1})
  \mathrlap{\,.}
$$ 

This may be thought of as stagewise revealing a [[higher category]] structure with [[k-morphism]] in [[negative number|negative]] degrees: The [[k-morphisms]] of $\mathcal{C}_{n}$ are the $k-n$-morphisms of the categorical spectrum. Therefore one also speaks of [[(∞,Z)-category|$(\infty,\mathbb{Z})$-categories]] ([Kern 2024](#Kern2024), following [Lessard 2019](#Lessard2019), [2022](#Lessard2022)).

In many examples, $\mathcal{C}_{n}$ happens to be an [[(infinity,n)-category|$(\infty,n)$-category]].

In this case, since the [[endomorphism monoid object|endomorphism objects]] $End(-)$ are canonically [[monoid objects]], each stage $\mathcal{C}_n$ in a categorical spectrum is exhibited as a [[monoidal (infinity,n)-category|monoidal $(\infty,n)$-category]] and, by iteration, in fact as a [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-category]].

Stagewise forming [[Picard infinity-groupoids|Picard $\infty$-groupoids]] of these [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-categories]] yields an ordinary [[spectrum]] of [[infinity-groupoids|$\infty$-groupoids]]:

$$
  (-)^\times
  \;\colon\;
  CatSpectra \longrightarrow Spectra
  \mathrlap{\,.}
$$

## Examples

* The [[(infinity,n)-category|$(\infty,n)$-categories]] of [[complex vector space|complex]] [[super vector spaces|super]] [[n-vector space|$(n-1)$-vector spaces]] form a categorical spectrum whose Picard spectrum is the [[Anderson duality|Anderson dual]] $I_{\mathbb{C}^\times}$ of the [[sphere spectrum]].


## Related concepts

* [[combinatorial spectrum]]

* [[(∞,Z)-category]]

## References

Precursor discussion using only [[strict omega-categories|strict $\omega$-categories]]:

* {#Lessard2019} [[Paul Lessard]]: *Spectra as Locally Finite $\mathbb{Z}$-Groupoids* (2019) \[<a href="https://youtu.be/nXHUHdCvDl8">video:YT</a>\]

* {#Lessard2022} [[Paul Lessard]]: *$\mathbf{Z}$-Categories I* \[<a href="https://arxiv.org/abs/2206.00849">arXiv:2206.00849</a>\]

Original discussion in the generality of [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]]:

* {#Stefanich21Thesis} [[Germán Stefanich]]: *Categorical spectra*,  ## Idea

The notion of *categorical spectra* is the full [[categorification]] of that of ([[Omega-spectrum|Omega]]-) [[spectra]] of [[topological spaces|spaces]]/[[infinity-groupoids|$\infty$-groupoids]], hence the generalization of *spectra* from [[(infinity,0)-categories|$(\infty,0)$-categories]] to [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]]:


A categorical spectrum is an [[natural numbers|$\mathbb{N}$]]-[[indexed set]] of [[pointed object|pointed]] [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]] $(\mathcal{C}_n, X_n)_{n \in \mathbb{N}}$ such that each stage is equivalent to the [[endomorphism monoid|endomorphism]] object of the next stage:

$$
  \mathcal{C}_n \simeq End_{\mathcal{C}_{n+1}}(X_{n+1})
  \mathrlap{\,.}
$$ 

This may be thought of as stagewise revealing a [[higher category]] structure with [[k-morphism]] in [[negative number|negative]] degrees: The [[k-morphisms]] of $\mathcal{C}_{n}$ are the $k-n$-morphisms of the categorical spectrum. Therefore one also speaks of [[(∞,Z)-category|$(\infty,\mathbb{Z})$-categories]] ([Kern 2024](#Kern2024), following [Lessard 2019](#Lessard2019), [2022](#Lessard2022)).

In many examples, $\mathcal{C}_{n}$ happens to be an [[(infinity,n)-category|$(\infty,n)$-category]].

In this case, since the [[endomorphism monoid object|endomorphism objects]] $End(-)$ are canonically [[monoid objects]], each stage $\mathcal{C}_n$ in a categorical spectrum is exhibited as a [[monoidal (infinity,n)-category|monoidal $(\infty,n)$-category]] and, by iteration, in fact as a [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-category]].

Stagewise forming [[Picard infinity-groupoids|Picard $\infty$-groupoids]] of these [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-categories]] yields an ordinary [[spectrum]] of [[infinity-groupoids|$\infty$-groupoids]]:

$$
  (-)^\times
  \;\colon\;
  CatSpectra \longrightarrow Spectra
  \mathrlap{\,.}
$$

## Examples

* The [[(infinity,n)-category|$(\infty,n)$-categories]] of [[complex vector space|complex]] [[super vector spaces|super]] [[n-vector space|$(n-1)$-vector spaces]] form a categorical spectrum whose Picard spectrum is the [[Anderson duality|Anderson dual]] $I_{\mathbb{C}^\times}$ of the [[sphere spectrum]].


## Related concepts

* [[combinatorial spectrum]]

* [[(∞,Z)-category]]

## References

Precursor discussion using only [[strict omega-categories|strict $\omega$-categories]]:

* {#Lessard2019} [[Paul Lessard]]: *Spectra as Locally Finite $\mathbb{Z}$-Groupoids* (2019) \[<a href="https://youtu.be/nXHUHdCvDl8">video:YT</a>\]

* {#Lessard2022} [[Paul Lessard]]: *$\mathbf{Z}$-Categories I* \[<a href="https://arxiv.org/abs/2206.00849">arXiv:2206.00849</a>\]

Original discussion in the generality of [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]]:

* {#Stefanich21Thesis} [[Germán Stefanich]]: *Categorical spectra*,  §8.6 ## Idea

The notion of *categorical spectra* is the full [[categorification]] of that of ([[Omega-spectrum|Omega]]-) [[spectra]] of [[topological spaces|spaces]]/[[infinity-groupoids|$\infty$-groupoids]], hence the generalization of *spectra* from [[(infinity,0)-categories|$(\infty,0)$-categories]] to [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]]:


A categorical spectrum is an [[natural numbers|$\mathbb{N}$]]-[[indexed set]] of [[pointed object|pointed]] [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]] $(\mathcal{C}_n, X_n)_{n \in \mathbb{N}}$ such that each stage is equivalent to the [[endomorphism monoid|endomorphism]] object of the next stage:

$$
  \mathcal{C}_n \simeq End_{\mathcal{C}_{n+1}}(X_{n+1})
  \mathrlap{\,.}
$$ 

This may be thought of as stagewise revealing a [[higher category]] structure with [[k-morphism]] in [[negative number|negative]] degrees: The [[k-morphisms]] of $\mathcal{C}_{n}$ are the $k-n$-morphisms of the categorical spectrum. Therefore one also speaks of [[(∞,Z)-category|$(\infty,\mathbb{Z})$-categories]] ([Kern 2024](#Kern2024), following [Lessard 2019](#Lessard2019), [2022](#Lessard2022)).

In many examples, $\mathcal{C}_{n}$ happens to be an [[(infinity,n)-category|$(\infty,n)$-category]].

In this case, since the [[endomorphism monoid object|endomorphism objects]] $End(-)$ are canonically [[monoid objects]], each stage $\mathcal{C}_n$ in a categorical spectrum is exhibited as a [[monoidal (infinity,n)-category|monoidal $(\infty,n)$-category]] and, by iteration, in fact as a [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-category]].

Stagewise forming [[Picard infinity-groupoids|Picard $\infty$-groupoids]] of these [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-categories]] yields an ordinary [[spectrum]] of [[infinity-groupoids|$\infty$-groupoids]]:

$$
  (-)^\times
  \;\colon\;
  CatSpectra \longrightarrow Spectra
  \mathrlap{\,.}
$$

## Examples

\begin{example}
The [[(infinity,n)-category|$(\infty,n)$-categories]] of [[complex vector space|complex]] [[super vector spaces|super]] [[n-vector space|$(n-1)$-vector spaces]] form a categorical spectrum whose Picard spectrum is the [[Anderson duality|Anderson dual]] $I_{\mathbb{C}^\times}$ of the [[sphere spectrum]].
\end{example}
([[David Reutter]] and [[Theo Johnson-Freyd]], upcoming)

## Related concepts

* [[combinatorial spectrum]]

* [[(∞,Z)-category]]

## References

Precursor discussion using only [[strict omega-categories|strict $\omega$-categories]]:

* {#Lessard2019} [[Paul Lessard]]: *Spectra as Locally Finite $\mathbb{Z}$-Groupoids* (2019) \[<a href="https://youtu.be/nXHUHdCvDl8">video:YT</a>\]

* {#Lessard2022} [[Paul Lessard]]: *$\mathbf{Z}$-Categories I* \[<a href="https://arxiv.org/abs/2206.00849">arXiv:2206.00849</a>\]

Original discussion in the generality of [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]]:

* {#Stefanich21Thesis} [[Germán Stefanich]]: *Categorical spectra*,  §8.6 & §13 in: *Higher Quasicoherent Sheaves*, PhD thesis, UC Berkeley (2021) &lbrack;[escholarship:19h1f1tv](https://escholarship.org/uc/item/19h1f1tv), [pdf](https://web.ma.utexas.edu/users/gs29722/Thesis.pdf)&rbrack;

* [[Naruki Masuda]]: *The Algebra of Categorical Spectra*, PhD thesis, Johns Hopkins University (2024) &lbrack;[handle:1774.2/70013](https://jscholarship.library.jhu.edu/handle/1774.2/70013), [arXiv:2605.03114](https://arxiv.org/abs/2605.03114)&rbrack;

* {#Kern2024} [[David Kern]]: _Categorical spectra as pointed $(\infty,\mathbb{Z})$-categories_ &lbrack;[arXiv:2410.02578](https://arxiv.org/abs/2410.02578)&rbrack;


On the generalization of [[Whitehead-generalized homology]] to [[coefficients]] being categorical spectra:

* [[Hadrian Heine]]: *Homology of higher categories*

in: *Higher Quasicoherent Sheaves*, PhD thesis, UC Berkeley (2021) &lbrack;[escholarship:19h1f1tv](https://escholarship.org/uc/item/19h1f1tv), [pdf](https://web.ma.utexas.edu/users/gs29722/Thesis.pdf)&rbrack;

* [[Naruki Masuda]]: *The Algebra of Categorical Spectra*, PhD thesis, Johns Hopkins University (2024) &lbrack;[handle:1774.2/70013](https://jscholarship.library.jhu.edu/handle/1774.2/70013), [arXiv:2605.03114](https://arxiv.org/abs/2605.03114)&rbrack;

* {#Kern2024} [[David Kern]]: _Categorical spectra as pointed $(\infty,\mathbb{Z})$-categories_ &lbrack;[arXiv:2410.02578](https://arxiv.org/abs/2410.02578)&rbrack;


On the generalization of [[Whitehead-generalized homology]] to [[coefficients]] being categorical spectra:

* [[Hadrian Heine]]: *Homology of higher categories*

8.6 &  in: *Higher Quasicoherent Sheaves*, PhD thesis, UC Berkeley (2021) &lbrack;[escholarship:19h1f1tv](https://escholarship.org/uc/item/19h1f1tv), [pdf](https://web.ma.utexas.edu/users/gs29722/Thesis.pdf)&rbrack;

* [[Naruki Masuda]]: *The Algebra of Categorical Spectra*, PhD thesis, Johns Hopkins University (2024) &lbrack;[handle:1774.2/70013](https://jscholarship.library.jhu.edu/handle/1774.2/70013), [arXiv:2605.03114](https://arxiv.org/abs/2605.03114)&rbrack;

* {#Kern2024} [[David Kern]]: _Categorical spectra as pointed $(\infty,\mathbb{Z})$-categories_ &lbrack;[arXiv:2410.02578](https://arxiv.org/abs/2410.02578)&rbrack;


On the generalization of [[Whitehead-generalized homology]] to [[coefficients]] being categorical spectra:

* [[Hadrian Heine]]: *Homology of higher categories*





***

+-- {: .num_theorem #TheoremAffineVarietiesAffinekAlgebrasAreEquivalent}
###### Theorem

([Milne 2017, Propositions 3.24, 3.25](#Milne17)). Let $k$ be an algebraically closed field. The categories of affine varieties and affine $k$-algebras are [[dual equivalence|anti-equivalent]].

=--

The following result particularizes the [[schemes as sheaves on affine schemes#SchemesAsPresheaves|fundamental theorem on morphisms of schemes]] to prevarieties.

+-- {: .num_prop #PropositionSpmAndGammaAreMutuallyRightAdjoint}
###### Proposition

[Milne 2017, Propositions 5.11](#Milne17). Let $k$ be an algebraically closed field. Let $V$ be an algebraic $k$-prevariety. Let $A$ be an affine $k$-algebra. Then we have the following natural bijection:

$$
Hom(V,Spm(A))\cong Hom_{k\text{-algebra}}(A,\Gamma(V,\mathcal{O}_V)).
$$

=--

In other words, the maximal spectrum functor and the global sections functor, defined between the categories of affine $k$-algebras and $k$-prevarieties, are [[dual adjunction|mutually right adjoint]]. Note that Milne states the result for quasi-compact varieties, but his proof applies in the general case and never uses quasi-compactness nor separation. Note that from \ref{PropositionSpmAndGammaAreMutuallyRightAdjoint} we recover \ref{TheoremAffineVarietiesAffinekAlgebrasAreEquivalent}.

For additional information, look at this very related typing graph. 

$$\frac{\Gamma \vdash A ,; \Gamma \vdash B}{\Gamma \vdash A\times B}$$
