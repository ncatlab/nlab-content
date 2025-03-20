+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

By a _bireflective subcategory_ one might mean:

1. A [[subcategory]] $\iota \,\colon\, \mathcal{C} \hookrightarrow \mathcal{B}$ which is both [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]] --- i.e. a [[fully faithful functor]] possessing both [[left adjoint|left]] and [[right adjoints]]: $L \dashv \iota \dashv R$ (*[[reflective localization]]* and *coreflective localization*).

   The [[adjoint pair]] $\iota \circ L \dashv \iota \circ R$ is then an [[adjoint modality]]; see there for more.

1. More specifically, one may in addition ask that $L \simeq R$, hence that the subcategory inclusion $\iota$ has an [[ambidextrous adjoint]] $\beta \dashv \iota \dashv \beta$. 

   Such subcategories are called **quintessential localizations** by [Johnstone (1996)](#JS96).

   The corresponding ([[comonad|co]]-)[[monad]] $\natural \coloneqq \iota \circ \beta$ is then a *[[Frobenius monad]]* (see at *[[classical modality]]*).

1. Finally, one may moreover ask that the [[points-to-pieces transform]] $\natural \overset{\epsilon}{\longrightarrow} id \overset{\eta}{\longrightarrow} \natural$ of a quintessential localization be the [[identity morphisms]].

   This strong form of the notion is the case actually called **bireflective subcategories** by [Freyd et al. (1999)](#FOPTST99).


## Definition
 {#AmbidextrouslyBireflectiveSubcategories}

\begin{definition}
  \label{BireflectiveSubcategory}
\linebreak
  A [[full subcategory]]-inclusion
  $$
    \iota
    \;\colon\;
    \mathcal{C} \hookrightarrow \mathcal{B}
  $$
  is *bireflective* in the sense of [FOPTST99, Def. 8](#FOPTST99)
  iff

(1.) the inclusion has an [[ambidextrous adjoint]]

  \begin{tikzcd}[column sep=20pt]
    \mathcal{C}
    \ar[
      from=rr,
      shift right=18pt,
      "{ \beta }"{description}
    ]
    \ar[
      rr,
      hook,
      "{ \iota }"{description}
    ]
    \ar[
      from=rr,
      shift left=18pt,
      "{ \beta }"{description}
    ]
    \ar[
      rr,
      shift left=8pt,
      phantom,
      "{
        \scalebox{.7}{$\bot$}
      }"
    ]
    \ar[
      rr,
      shift right=8pt,
      phantom,
      "{
        \scalebox{.7}{$\bot$}
      }"
    ]
    &&
    \mathcal{B}
    \ar[out=+50, in=-50,
      looseness=4.5,
      shorten=-3pt,
      shift left=0pt,
      "\scalebox{1.1}{${
          \hspace{-18pt}
          \mathclap{
            {
              \natural
            }
          }
          \hspace{4pt}
        }$}"{
          pos=.5,
          xshift=14pt
        }
    ]
  \end{tikzcd}

(2.) such that for all $E \in \mathcal{B}$ the [[counit of an adjunction|counit]] of the right adjunction followed by the [[unit of an adjunction|unit]] of the left adjunction (the [[points-to-pieces transform]]) equals the [[identity morphisms|identity]]:

  \begin{tikzcd}
    \natural E
    \ar[
      r,
      "{
        \epsilon^{\iota \,\dashv\, \beta}_{A}
      }"
    ]
    \ar[
      dr,
      equals
    ]
    &
    E
    \ar[
      d,
      "{
        \eta^{\beta \,\dashv\, \iota}_{A}
      }"
    ]
    \\
    &
    \natural E
  \end{tikzcd}

\end{definition}

\begin{remark}
  The first clause in Def. \ref{BireflectiveSubcategory} does not in general by itself enforce the second clause. A [[counter-example]] is given in [FOPTST99, Rem. 12](#FOPTST99).

However, the second clause does follow automatically when $\mathcal{B}$ is a [[Cauchy-complete category]] ([Johnstone (1996)](#JS96)).
\end{remark}

\begin{remark}
  In the other direction, the second clause in Def. \ref{BireflectiveSubcategory} implies that

  \begin{tikzcd}[column sep=20pt]
    \mathrm{id}_{\mathcal{B}}
    \ar[rr, "{ \eta^{\beta \,\dashv\, \iota} }"]
    &&
    \iota \beta
    \ar[rr, "{ \epsilon^{\iota \,\dashv\, \beta} }"]
    &&
    \mathrm{id}_{\mathcal{B}}
  \end{tikzcd}

is an [[idempotent]] [[natural transformation|natural]] [[endomorphism]], exhibited as a [[split idempotent]].
\end{remark}

\begin{prop}\label{BireflectionsInCCorrespondToSplitIdempotentsOnIdC}
  Given a [[category]] $\mathcal{B}$,
its bireflective subcategories (Def. \ref{BireflectiveSubcategory}) are in correspondence with the [[split idempotent]] [[natural transformation|natural]] [[endomorphisms]] on $id_\mathcal{B}$ with specified splitting, i.e.

  \begin{tikzcd}[column sep=20pt]
    \mathrm{id}_{\mathcal{B}}
    \ar[rr, "{ \eta^\natural }"]
    &&
    \natural
    \ar[rr, "{ \epsilon^\natural }"]
    &&
    \mathrm{id}_{\mathcal{B}}
  \end{tikzcd}

with

\[
  \label{EtaCircEpisolonIsIdentity}
  \eta^\natural \,\circ\, \epsilon^\natural
  \;=\;
  \mathrm{id}
  \,.
\]

\end{prop}
([FOPTST99, Thm. 13](#FOPTST99))

Concretely, from a split idempotent on $id_{\mathcal{B}}$ we recover the [[Frobenius monad]] $\natural$ as follows:

\begin{lemma}
  Given a split idempotent transformation as in Prop. \ref{BireflectionsInCCorrespondToSplitIdempotentsOnIdC} we have for all $E \,\in\, \mathcal{B}$
$$
  \natural
  (\eta^{\natural}_{E})
  \;=\;
  \eta^{\natural}_{\natural E}
  \;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;
  \natural
  (\epsilon^{\natural}_{E})
  \;=\;
  \epsilon^{\natural}_{\natural E}
  \,.
$$
\end{lemma}
([RFL21, Lem. 7.7](#RFL21))
\begin{proof}
  By [[natural transformation|naturality]] of the transformation $\eta$

\begin{tikzcd}[sep=30pt]
  E
  \ar[r, "{ \eta^\natural_E }"{description}]
  \ar[d, "{ \eta^\natural_E }"{description}]
  &
  \natural E
  \ar[d, "{ \natural \eta^\natural_E }"{description} ]
  \\
  \natural E
  \ar[r, "{ \eta^{\natural}_{\natural E} }"{description}]
  &
  \natural \natural E
\end{tikzcd}

and using (eq:EtaCircEpisolonIsIdentity) we get the first statement:

$$
  \natural
  (\eta^{\natural}_{E})
  \;=\;
  \natural
  (\eta^{\natural}_{E})
  \circ
  \overset
    { \mathrm{id}_E }
    {
      \overbrace{
        \eta^\natural_E
        \circ \epsilon^\natural_E
      }
    }
  \;=\;
  \eta^\natural_{\natural E}
  \circ
  \eta^{\natural}_{E}
  \circ
  \epsilon^\natural_E
  \;=\;
  \eta^{\natural}_{\natural E}
$$

The second follows analogously.
\end{proof}

\begin{prop}
  Given a split idempotent transformation as in Prop. \ref{BireflectionsInCCorrespondToSplitIdempotentsOnIdC}, $\natural \colon \mathcal{B} \to \mathcal{B}$ becomes

1. an [[idempotent monad]] $(\natural, \eta, \mu)$ by setting

   $$
     \mu \,\coloneqq\, \natural(\epsilon^\natural_{(-)})
   $$

1. an [[idempotent comonad]] $(\natural, \epsilon, \delta)$ by setting

   $$
     \delta \,\coloneqq\, \natural(\eta^\natural_{(-)})
   $$


\end{prop}
([RFL21, Prop. 7.8](#RFL21))
\begin{proof}
For the [[associativity]] of the monoid product we need to show the [[commuting square|commutativity]] of

  \begin{tikzcd}[sep=30pt]
    \natural
    \natural
    \natural
    E
    \ar[
      d,
      "{
        \natural(
          \natural \epsilon^\natural_E
        )
      }"{description}
    ]
    \ar[r, "{ \natural \epsilon^\natural_{\natural E} }"{description}]
    &
    \natural \natural E
    \ar[
      d,
      "{
        \natural
        \epsilon^\natural_E
      }"{description}
    ]
    \\
    \natural \natural E
    \ar[
      r,
      "{ \natural \epsilon^\natural_E }"{description}
    ]
    &
    \natural E
  \end{tikzcd}

By [[functor|functoriality]] of $\natural$ this follows from the commutativity of

  \begin{tikzcd}[sep=30pt]
    \natural
    \natural
    E
    \ar[
      d,
      "{
          \natural \epsilon^\natural_E
      }"{description}
    ]
    \ar[r, "{  \epsilon^\natural_{\natural E} }"{description}]
    &
    \natural E
    \ar[
      d,
      "{
        \epsilon^\natural_E
      }"{description}
    ]
    \\
    \natural E
    \ar[
      r,
      "{ \epsilon^\natural_E }"{description}
    ]
    &
    E
  \end{tikzcd}

which holds by [[natural transformation|naturality]] of $\epsilon$.

The other claims follow similarly.
\end{proof}

## Modal type theory
 {#ModalTypeTheory}

A [[modal type theory]] for bireflection [[modalities]] has been proposed in [Riley, Finster & Licata (2021)](#RFL21), [Riley (2022)](#Riley22).

We show the [[inference rules]] which these authors propose to add to plain [[intuitionistic type theory]] for encoding the presence of a bireflection [[classical modality]] $\natural$ on the type system, and we show corresponding [[categorical semantics]] via [[commuting diagrams]] in an interpreting [[locally cartesian closed category]]  (a more syntactic semantics is indicated in [RFL21, Sec. 7, esp. Fig. 6](#RFL21)).

\begin{remark}
  Given a bireflection $\natural \colon \mathcal{B} \to \mathcal{B}$ as above, then for $\Gamma \in \mathcal{B}$ we obtain a [[monad]] on the [[slice category]], to be denoted

\[
  \label{TheMonadOnSlices}
  \natural_\Gamma
  \;\colon\;
  \mathcal{B}_{/\Gamma} \to \mathcal{B}_{/\Gamma}
\]

by setting

$$
  \natural_\Gamma
  \left[
  \begin{array}{c}
    A
    \\
    \big\downarrow \mathrlap{\!\! {}^{p_A} }
    \\
    \Gamma
  \end{array}
  \;\;\;\;
  \right]
  \;\;\coloneqq\;\;
  \big(\eta^\natural_\Gamma\big)^\ast 
  \,\natural\, 
  \left[
  \begin{array}{c}
    \natural A
    \\
    \big\downarrow \mathrlap{\!\! {}^{\natural p_A} }
    \\
    \natural \Gamma
  \end{array}
  \;\;\;\;
  \right]
$$

\end{remark}

\begin{remark}\label{OdditiesOfTheRFLSyntax}
Beware of some non-obvious properties of the following type-theoretic [[syntax]]:

1. There is an asymmetry in the meaning of $\underline{(-)}$:

   An underline of a context denotes application of $\natural$, but an underline of a type in context only means its pullback along the [[counit of a comonad|counit]] $\epsilon^{\natural}$. The idea is that underlines indicate *dependency* on $\natural$-modal variables, to be distinguished of a type itself being $\natural$-[[modal type|modal]] or not.

1. The syntactic symbol "$\natural$" is not exactly [[categorical semantics|interpreted]] as the bireflective monad of that name. Rather:

   * An unadorned "$\natural$" in the syntax [[categorical semantics|interprets]], in [[context]] $\Gamma$, as the [[relative monad]]

     $$
       \classical^{rel}_\Gamma
       \;\;
       \colon
       \;\;
       \array{
         \mathcal{B}_{/\natural \Gamma}
         &
           \xrightarrow{
             (\eta^\natural_\Gamma)^\ast
           }
         &
         \mathcal{B}_{/\Gamma}
         &
           \xrightarrow{
             \natural_\Gamma
           }
         &
         \mathcal{B}_{/\Gamma}
       }
     $$

   * The combination $\natural \underline{(-)}$ is what actually [[categorical semantics|interprets]] as $\natural_\Gamma$ (eq:TheMonadOnSlices).

     This transpires syntactically in [RFL21, Cor. 2.14](#RFL21); [Riley22, Cor. 1.1.16](#Riley22), and semantically in (eq:InternalUnitConstruction) below.

\end{remark}

\linebreak

The list of [[inference rules]] and their [[categorical semantics]] (first the [[axioms]] then derived rules):

<center>
<img src="/nlab/files/BireflectiveTypesStructureRules-230327.jpg" width="690">
</center>

<center>
<img src="/nlab/files/BireflectiveModalityInferenceRules-230327.jpg" width="690">
</center>

<center>
<img src="/nlab/files/BireflectiveModalityComputationRules-230327b.jpg" width="690">
</center>

Using these ingredients, one finds that the function $a \,\mapsto\, \underline{a}^\natural$ is interpreted simply as postcomposition with the $\eta^{\natural}$-[[naturality square]]:

\linebreak
\linebreak

\[
  \label{InternalUnitConstruction}
  \;
\]

<center>
<div style="margin:-130px 10px 10px 0;">
<img src="/nlab/files/BireflectiveModalityUnitDefinition-230304b.jpg" width="690">
</div>
</center>

With this, one finds the following rule for $\natural$ respecting [[dependent pair types]]:


\linebreak
\linebreak

\[
  \label{NaturalRespectsDependentPairs}
  \;
\]

<center>
<div style="margin:-130px 10px 10px 0;">
<img src="/nlab/files/BireflectiveModalityRespectForPairs-230404b.jpg" width="690">
</div>
</center>

Using this one finds that every type $A$ is the [[dependent sum type]] of its fiber [[linear types]] $A_{\underline{x}}$ (NB: we show 1-categorical semantics, interpreting [[identification types]] as [[diagonal morphisms]]):


\linebreak
\linebreak

\[
  \label{LinearTpes}
  \;
\]

<center>
<div style="margin:-130px 10px 10px 0;">
<img src="/nlab/files/BireflectiveModalityLinearTpes-230404.jpg" width="690">
</div>
</center>





\linebreak




## Examples

\begin{example}\label{ReractiveSpaces}
**(spaces among retractive spaces)**
\linebreak
  Let $\mathcal{B}$ be the category of [[retractive space|retractive]] [[topological spaces]] (or just of [[Sets]]), i.e. the category of [[diagrams]] in [[Top]] ([[Set]]) of the form $B \xrightarrow{i} E \xrightarrow{p} B$ such that $p \circ i \,=\, id_B$. Then the functor

$$
  \begin{array}{ccc}
    Top &\hookrightarrow& Top_{\mathcal{R}}
    \\
    B &\mapsto& \big[ B \xrightarrow{id} B \xrightarrow{id} B \big]
  \end{array}
$$

is a bireflective subcategory inlusion (Def. \ref{BireflectiveSubcategory}) with [[ambidextrous adjoint]] given by 

$$
  \begin{array}{ccc}
    Top_{\mathcal{R}} &\longrightarrow& Top
    \\
    \big[
      B \xrightarrow{i} E \xrightarrow{p} B
    \big]
    &\mapsto&
    B
  \end{array}
$$


\end{example}

\begin{example}\label{ZeroVectorBundlesAmongVectorBundles}
**([[zero-vector bundles]] among all [[vector bundles]])**
\linebreak
  For any [[ground field]],
  let $\mathcal{B} \coloneqq Vect_{Set} \coloneqq \int_{S \in Set} Vect S$ be the category [[VectBund]] of [[vector bundles]] over [[Sets]], hence of [[indexed set|indexed]] [[vector spaces]]. Then the functor
$$
  Set \xhookrightarrow{\;\; 0 \;\;} Vect_{Set}
$$
which sends any set $S$ to the [[zero vector bundle]] $S \times \{0\}$ over $S$ is a bireflective subcategory in the sense of Def. \ref{BireflectiveSubcategory}.
\end{example}

\begin{example}\label{ZeroSpectrumBundlesAmongSpectrumBundles}
**([[zero-spectrum bundles]] among all [[parameterized spectra]])**
\linebreak
Let $T Grpd_\infty$ denote the [[(infinity,1)-category|$\infty$-category]] of [[parameterized spectra]] over varying [[infinity-groupoids|$\infty$-groupoids]] (the [[tangent (infinity,1)-category|tangent $\infty$-category]] of [[∞Grpd|$Grpd_\infty$]]). Then the inclusion
$$
  Grpd_\infty \hookrightarrow T Grpd_\infty
$$
given by sending $X \in Grpd_\infty$ to the [[zero-spectrum bundle]] over $X$ ought to count as a "bireflective [[sub-(infinity,1)-category|sub-$\infty$-category]]" (cf. [here](https://ncatlab.org/nlab/show/infinitesimal+cohesion#GoodwillieTangentCohesion) at *[[infinitesimal cohesion]]*). 

A [[model category]]-presentation of this situation by a (left and right) [[Quillen functor]] to a [[model structure for parameterized spectra]] [[underlying]] which is a bireflective sub-1-category inclusion (Def. \ref{BireflectiveSubcategory}) may be recognized in [Hebestreit, Sagave & Schlichtkrull (2020), Lem. 3.19](model+structure+for+parameterized+spectra#HebestreitSagaveSchlichtkrull20), there incarnated as the canonical inclusion
$$
  \mathcal{S}^{\mathcal{I}}
  \hookrightarrow
  Sp^{\Sigma}_{\mathcal{R}}
$$
of [[I-spaces|$\mathcal{I}$-spaces]] into [[symmetric spectra]] [[internalization|internal to]] [[retractive spaces]] (Exp. \ref{ReractiveSpaces}).

An analogous statement is in [Braunack-Mayer (2019), Cor. 2.45](model+structure+for+parameterized+spectra#BraunackMayer19).
\end{example}



## Related concepts

* [[infinitesimal cohesion]]

* [[classical modality]]

* [[VectBund]]

* [[parameterized spectra]]

## References

Subcategories whose inclusion functor admits both a left and right adjoint are called **bireflective** in:

* W. John Wilbur, "Reflective and coreflective hulls in the category of locally convex spaces." General topology and its applications 4.3 (1974): 235-254.

On subcategory inclusions with ambidextrous adjoints ([[quintessential localizations]]):

* {#JS96} [[Peter Johnstone]], _Remarks on Quintessential and Persistent Localizations_, TAC **2** 8 (1996) 90-99. &lbrack;[pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf), [2-08](http://www.tac.mta.ca/tac/volumes/1996/n8/2-08abs.html)&rbrack;

On subcategory inclusions with ambidextrous adjoints whose [[points-to-pieces transform]] is the [[identity]] (actual *bireflective subcategories*):

* {#FOPTST99} [[Peter Freyd]], [[Peter O’Hearn]],  [[A. John Power]], [[M. Takeyama]], [[Ross Street]], [[Robert D. Tennent]], *Bireflectivity*, Theoretical Computer Science **228** 1–2 (1999) 49-76 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00354-5">doi:10.1016/S0304-3975(98)00354-5</a>&rbrack;

Discussion of a [[modal type theory]] for bireflective [[modalities]], in a context of [[linear homotopy type theory]]:

* {#RFL21} [[Mitchell Riley]], [[Eric Finster]], [[Daniel R. Licata]], Section 7.1 in: *Synthetic Spectra via a Monadic and Comonadic Modality* &lbrack;[arXiv:2102.04099](https://arxiv.org/abs/2102.04099)&rbrack;

* {#Riley22} [[Mitchell Riley]], *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139), [ir:3269](https://digitalcollections.wesleyan.edu/object/ir%3A3269), [pdf](https://mvr.hosting.nyu.edu/pubs/thesis.pdf)&rbrack;


[[!redirects bireflective subcategories]]

