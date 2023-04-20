+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

On [[model category]] [[structures]] [[presentable (infinity,1)-category|presenting]] [[(infinity,1)-category|$\infty$-categories]] of [[parameterized spectra]] (in [[parameterized stable homotopy theory]]), either over a fixed base or over varying bases and then presenting [[tangent (infinity,1)-category|tangent $\infty$-categories]].

(...)


## Properties
 {#Properties}

We consider some properties of model category 

\[
  \label{ModelCategoryOfSpectraInISpaces}
  \mathrm{Sp}^\Sigma_{\mathcal{R}}
  \;\;
  \in
  \;\;
  ModCat
\] 

of parameterized [[symmetric spectra]] in [[I-space|$\mathcal{I}$-spaces]] based on [[SimplicialSets]] and equipped with the absolute/positive local model structures.

$$
  \mathcal{S} \coloneqq sSet
$$

as given in [Hebestreit, Sagave & Schlichtkrull (2020)](#HebestreitSagaveSchlichtkrull20):

\begin{proposition}
With the [[external tensor product|external]] [[smash product of spectra]] the model category (eq:ModelCategoryOfSpectraInISpaces) 

1. is a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] 

1. with [[tensor unit]] the [[sphere spectrum]] $\mathcal{S}$,

1. which satisfies the [[pushout-product axiom]]

1. and the [[unit axiom]],

hence is a [[monoidal model category]].
\end{proposition}
\begin{proof}
The first statements are made explicit in [HSS, Prop. 4.5 & Prop. 5.11](#HebestreitSagaveSchlichtkrull20). 
To see that also the unit axiom is satisfied it is sufficient to see that $\mathbb{S}$ is a [[cofibrant object]]. For that use the definition of $\mathbb{S}$ as $\mathbb{S}_t^{\mathcal{I}}[\ast]$ (hidden on [p. 38](https://arxiv.org/pdf/1904.01824.pdf#page=38)) and the fact that $\mathbb{S}_t^{\mathcal{I}}$ is a [[left Quillen functor]], by [HSS, Lem. 5.12](#HebestreitSagaveSchlichtkrull20).
\end{proof}

\begin{proposition}
The inclusion of [[I-spaces|$\mathcal{I}$-spaces]] via their [[zero-spectrum bundles]] is a [[bireflective subcategory]] (according to [this Def.](bireflective+subcategory#BireflectiveSubcategory)) which is also a [[Quillen adjoint triple]]:

\[
  \label{BireflectionOfZeroSpectrumBundles}
\]

\begin{tikzcd}
  \phantom{-}
  \\[-70pt]
  \mathcal{S}^{\mathcal{I}}
  \ar[
    from=rr,
    shift left=22pt,
    "{ \beta }"{description}
  ]
  \ar[
    rr,
    hook,
    "{ 0 }"{description}
  ]
  \ar[
    from=rr,
    shift right=22pt,
    "{ \beta }"{description}
  ]
  \ar[
    rr,
    phantom,
    shift left=11pt,
    "{ \scalebox{.6}{$\bot_{{}_{\mathrlap{\mathrm{Qu}}}}$} }"
  ]
  \ar[
    rr,
    phantom,
    shift right=11pt,
    "{ \scalebox{.6}{$\bot_{{}_{\mathrlap{\mathrm{Qu}}}}$} }"
  ]
  &&
  \mathrm{Sp}^\Sigma_{\mathcal{R}}
\end{tikzcd}

\end{proposition}
\begin{proof}
This may be recognized from [HSS, Lem. 3.19 & Cor. 5.13](#HebestreitSagaveSchlichtkrull20).
\end{proof}

\begin{definition}
In the following we will leave the inclusions 
$$
  \mathcal{S} 
    \overset{const}{\hookrightarrow}   
  \mathcal{S}^{\mathcal{I}}
    \overset{0}{\hookrightarrow}
  \mathrm{Sp}^\Sigma_\mathcal{R}
$$
notationally implicit. For example, for $B$ a [[simplicial set]] we write $\big(\mathrm{Sp}^\Sigma_\mathcal{R}\big)_{/B}$ for the [[slice model structure]] of (eq:ModelCategoryOfSpectraInISpaces) over the [[zero-spectrum bundle]] over $B$.
\end{definition}

The model category (eq:ModelCategoryOfSpectraInISpaces) is not quite [[right proper]] (cf. [pp. 40](https://arxiv.org/pdf/1904.01824.pdf#page=40)) but, in its version based on [[simplicial sets]], we have:

\begin{proposition}\label{QuillenRightBaseChange}
Left [[base change]] $f^\ast$ along [[Kan fibrations]] $f \,\colon\, B_1 \to B_2$ of ([[zero-spectrum bundles]] (eq:BireflectionOfZeroSpectrumBundles) over) [[Kan complexes]] *is* a [[left Quillen functor]] between the [[slice model structures]] of the *absolute* local model structure. Since, generally, $f^\ast$ is also a [[right Quillen functor]], we have [[base change]] [[Quillen adjoint triples]] of this form: 

\begin{tikzcd}
  \left.
  \begin{array}{r}
    \mbox{$B_2$ Kan complex}
    \\
    \mbox{$f : B_1 \to B_2$ Kan fibration}
  \end{array}
  \right\}
  \;\;\;\;
    \vdash
  \;\;\;\;
  \big(\mathrm{Sp}^\Sigma_{\mathcal{R}}\big)_{/B_1}
  \ar[
    rr,
    shift left=22pt,
    "{ f_! }"{description}
  ]
  \ar[
    from=rr,
    shift left=00pt,
    "{ f^\ast }"{description}
  ]
  \ar[
    rr,
    shift right=22pt,
    "{ f_\ast }"{description}
  ]
  \ar[
    rr,
    phantom,
    shift left=11pt,
    "{ \scalebox{.6}{$\bot_{{}_{\mathrlap{\mathrm{Qu}}}}$} }"
  ]
  \ar[
    rr,
    phantom,
    shift right=11pt,
    "{ \scalebox{.6}{$\bot_{{}_{\mathrlap{\mathrm{Qu}}}}$} }"
  ]
  &&
  \big(\mathrm{Sp}^\Sigma_{\mathcal{R}}\big)_{/B_2}
\end{tikzcd}

\end{proposition}
\begin{proof}
  The left Quillen property of $f^\ast$ is HSS20, Lem. 7.22](#HebestreitSagaveSchlichtkrull20).
The right Quillen property is mentioned inside the proof of Lem. 8.10 there.
\end{proof}

Similarly, but now also for the positive local model structure, we have:

\begin{proposition}
With respect absolute *or* positive local model structure:

\begin{tikzcd}
  \left.
  \begin{array}{r}
    \mbox{$B_2$ Kan complex}
    \\
    \mbox{$f : B_1 \to B_2$ Kan fibration}
  \end{array}
  \right\}
  \;\;\;\;
    \vdash
  \;\;\;\;
  \mathrm{Sp}^\Sigma_{B_1}
  \ar[
    rr,
    shift left=22pt,
    "{ f_! }"{description}
  ]
  \ar[
    from=rr,
    shift left=00pt,
    "{ f^\ast }"{description}
  ]
  \ar[
    rr,
    shift right=22pt,
    "{ f_\ast }"{description}
  ]
  \ar[
    rr,
    phantom,
    shift left=11pt,
    "{ \scalebox{.6}{$\bot_{{}_{\mathrlap{\mathrm{Qu}}}}$} }"
  ]
  \ar[
    rr,
    phantom,
    shift right=11pt,
    "{ \scalebox{.6}{$\bot_{{}_{\mathrlap{\mathrm{Qu}}}}$} }"
  ]
  &&
  \mathrm{Sp}^\Sigma_{/B_2}
\end{tikzcd}

\end{proposition}
\begin{proof}
[HSS, Lem. 5.17 & Lem. 7.25](#HebestreitSagaveSchlichtkrull20) 
\end{proof}

(...)

## Related concepts

* [[model structure for spectra]]

* [[model structure on presheaves of spectra]]

* [[parameterized stable homotopy theory]]

* [[tangent (infinity,1)-category]]


## References

### Tools

Tools for creating [[model structures on spectra]] relative to suitable ambient model categories:

* {#Schwede97} [[Stefan Schwede]], Section 3 of: _Spectra in model categories and applications to the algebraic cotangent complex_, Journal of Pure and Applied Algebra **120** (1997) 104 &lbrack;[pdf](http://www.math.uni-bonn.de/people/schwede/modelspec.pdf)&rbrack;

and also for [[model structures on symmetric spectra]]:

* {#Hovey00} [[Mark Hovey]], *Spectra and symmetric spectra in general model categories*, Journal of Pure and Applied Algebra **165** 1 (2001) 63-127 &lbrack;[arXiv:0004051](http://arxiv.org/abs/math/0004051), <a href="https://doi.org/10.1016/S0022-4049(00)00172-9">doi:10.1016/S0022-4049(00)00172-9</a>&rbrack;


### Over a fixed base

Model structure for [[genuine equivariant spectra]] parameterized over a fixed base:

* {#MaySigurdsson06} [[Peter May]], [[Johann Sigurdsson]], Chapter 12 of: _[[Parametrized Homotopy Theory]]_, Mathematical Surveys and Monographs **132**, AMS (2006) &lbrack;[arXiv:math/0411656](https://arxiv.org/abs/math/0411656)&rbrack;


### Over varying bases
 {#ReferencesOverVaryingBases}

Model structures of parameterized spectra over varying bases:

* {#BraunackMayer19} [[Vincent Braunack-Mayer]], *Combinatorial parametrised spectra*, Algebr. Geom. Topol. **21** (2021) 801-891 &lbrack;[arXiv:1907.08496](https://arxiv.org/abs/1907.08496), [doi:10.2140/agt.2021.21.801](https://doi.org/10.2140/agt.2021.21.801)&rbrack;

  > (based on the [[schreiber:thesis Braunack-Mayer|PhD thesis]], 2018)

* {#HebestreitSagaveSchlichtkrull20} [[Fabian Hebestreit]], [[Steffen Sagave]], [[Christian Schlichtkrull]], *Multiplicative parametrized homotopy theory via symmetric spectra in retractive spaces*, Forum of Mathematics, Sigma **8** (2020) e16 &lbrack;[arXiv:1904.01824](https://arxiv.org/abs/1904.01824), [doi:10.1017/fms.2020.11](https://doi.org/10.1017/fms.2020.11)&rbrack;



[[!redirects model structures for parameterized spectra]]

[[!redirects model structure on parameterized spectra]]
[[!redirects model structures on parameterized spectra]]


