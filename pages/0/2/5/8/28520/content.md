
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=-- 


\tableofcontents

## Idea

The notion of *categorical spectra* is the full [[categorification]] of that of ([[Omega-spectrum|Omega]]-) [[spectra]] of [[topological spaces|spaces]]/[[infinity-groupoids|$\infty$-groupoids]], hence the generalization of *spectra* from [[(infinity,0)-categories|$(\infty,0)$-categories]] to [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]]:


A *categorical spectrum* ([Stefanich 2021](#Stefanich21Thesis)) is an [[natural numbers|$\mathbb{N}$]]-[[indexed set]] of [[pointed object|pointed]] [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]] $(\mathcal{C}_n, X_n)_{n \in \mathbb{N}}$ such that each stage is [[equivalence|equivalent]] to the [[endomorphism monoid|endomorphism]] object of the next stage:

\[
  \label{CategoricalOmegaSpectrumCondition}
  \begin{array}{ccc}
    \mathcal{C}_n 
      &\overset{\sim}{\longrightarrow}&
    End_{\mathcal{C}_{n+1}}\big(X_{n+1}\big)
    \\
    X_n 
      &\mapsto& 
    id_{X_{n+1}}
    \mathrlap{\,.}
  \end{array}
\] 

This may be thought of as stagewise revealing a [[higher category]] structure with [[k-morphism]] possibly also in [[negative number|negative]] degrees: The [[k-morphisms]] of $\mathcal{C}_{n}$ are the $k-n$-morphisms of the categorical spectrum. Therefore one also speaks of [[(∞,Z)-category|$(\infty,\mathbb{Z})$-categories]] ([Kern 2024](#Kern2024), following [Lessard 2019](#Lessard2019), [2022](#Lessard2022)).

Since [[endomorphism monoid object|endomorphism objects]] $End(-)$ as in (eq:CategoricalOmegaSpectrumCondition) are canonically [[monoid objects]], the stages of a categorical spectrum carry the structure of [[monoid objects]] [[internalization|internal to]] [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]] and, by iteration, in fact of [[coherence|coherently]] [[commutative monoid objects]]. 

Concretely, in many examples, $\mathcal{C}_{n}$ happens to be an [[(infinity,n)-category|$(\infty,n)$-category]]. In this case, each stage $\mathcal{C}_n$ in a categorical spectrum is exhibited as a [[monoidal (infinity,n)-category|monoidal $(\infty,n)$-category]] and, by iteration, as a [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-category]]. 

If these [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-categories]] are [[locally presentable (infinity,n)-category|presentable]], then [Scholze 2026 Def. 1.18](#Scholze2026) speaks of *StRings* ([[duality between algebra and geometry|formally dual]] to "[[Gestalten]]").

Stagewise forming [[Picard infinity-groupoids|Picard $\infty$-groupoids]] of these [[symmetric monoidal (infinity,n)-category|symmetric monoidal $(\infty,n)$-categories]] yields an ordinary [[spectrum]] of [[infinity-groupoids|$\infty$-groupoids]]:

\[
  \label{PicardSpectrumFunctor}
  (-)^\times
  \;\colon\;
  CatSpectra \longrightarrow Spectra
  \mathrlap{\,.}
\]




## Examples

\begin{example}
The [[(infinity,n)-category|$(\infty,n)$-categories]] of [[complex vector space|complex]] [[super vector spaces|super]] [[n-vector space|$n$-vector spaces]] form a categorical spectrum whose Picard spectrum (eq:PicardSpectrumFunctor) is the [[Anderson duality|Anderson dual]] $I_{\mathbb{C}^\times}$ of the [[sphere spectrum]].
\end{example}
(Due to [[David Reutter]] and [[Theo Johnson-Freyd]], upcoming.)


## Related concepts

* [[combinatorial spectrum]]

* [[(∞,Z)-category]]


## References

Precursor discussion referring only to [[strict omega-categories|strict $\omega$-categories]]:

* {#Lessard2019} [[Paul Lessard]]: *Spectra as Locally Finite $\mathbb{Z}$-Groupoids* (2019) \[<a href="https://youtu.be/nXHUHdCvDl8">video:YT</a>\]

* {#Lessard2022} [[Paul Lessard]]: *$\mathbf{Z}$-Categories I* \[<a href="https://arxiv.org/abs/2206.00849">arXiv:2206.00849</a>\]


Original discussion in the generality of [[(infinity,infinity)-categories|$(\infty,\infty)$-categories]]:

* {#Stefanich21Thesis} [[Germán Stefanich]]: *Categorical spectra*,  §8.6 & §13 in: *Higher Quasicoherent Sheaves*, PhD thesis, UC Berkeley (2021) &lbrack;[escholarship:19h1f1tv](https://escholarship.org/uc/item/19h1f1tv), [pdf](https://web.ma.utexas.edu/users/gs29722/Thesis.pdf)&rbrack;


* [[Naruki Masuda]]: *The Algebra of Categorical Spectra*, PhD thesis, Johns Hopkins University (2024) &lbrack;[handle:1774.2/70013](https://jscholarship.library.jhu.edu/handle/1774.2/70013), [arXiv:2605.03114](https://arxiv.org/abs/2605.03114)&rbrack;

* {#Kern2024} [[David Kern]]: _Categorical spectra as pointed $(\infty,\mathbb{Z})$-categories_ &lbrack;[arXiv:2410.02578](https://arxiv.org/abs/2410.02578)&rbrack;

See also:

* [[Félix Loubaton]]: *Theory and models of $(\infty,\omega)$-categories* \[<a href="https://arxiv.org/abs/2307.11931">arXiv:2307.11931</a>\]


On the generalization of [[Whitehead-generalized homology]] to [[coefficients]] being categorical spectra:

* [[Hadrian Heine]]: *Homology of higher categories* \[<a href="https://arxiv.org/abs/2505.22640">arXiv:2505.22640</a>\]

On [[locally presentable (infinity,n)-category|presentable]] categorical spectra as $\infty$-categorical [[commutative rings]] ("StRings"), [[formal duals|formally dual]] to *[[Gestalten]]* (cf. *[[duality between algebra and geometry]]*):

* {#Scholze2026} [[Peter Scholze]]; Def. 1.18 in: *Geometry and Higher Category Theory*, lecture notes (2026) &lbrack;[webpage](https://www.mpim-bonn.mpg.de/node/14764), [pdf](https://people.mpim-bonn.mpg.de/scholze/Gestalten.pdf)&rbrack;
 




[[!redirects categorical spectra]]

[[!redirects StRing]]
[[!redirects StRings]]

