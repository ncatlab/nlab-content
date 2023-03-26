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

By a _bireflective subcategory_ one may mean a [[subcategory]] $\mathcal{B} \hookrightarrow \mathcal{C}$ which is both [[reflective subcategory|reflective]] and [[coreflective subcategory|coreflective]] --- i.e. a [[fully faithful functor]] possessing both [[left adjoint|left]] and [[right adjoints]].

The [[adjoint pair]] induced from the [[adjoint triple]] given by reflection, inclusion and coreflection of a bireflective subcategory is an [[adjoint modality]]. See there for more.

The terminology "bireflective" was coined in [FOPTST99](#FOPTST99) where --- beware --- it is in addition required that:

1. the left and right adjoints are equal, hence forming an [[ambidextrous adjoint]],

1. such that the [[adjunction unit]] followed by the [[adjunction counit]] is the [[identity morphism]].

## Ambidextrously bireflective subcategories
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

(2.) such that for all $E \in \mathcal{B}$ the [[counit of an adjunction|counit]] of the right adjunction followed by the [[unit of an adjunction|unit]] of the left adjunction equals the [[identity morphisms|identity]]:

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

A [[modal type theory]] for bireflection [[modalities]] has been proposed in [RFL21](#RFL21).

We show the [[inference rules]] which are added to plain [[intuitionistic type theory]] for encoding the presence of a bireflection $\natural$ on the type system.

(Beware the notational asymmetry: An underline of a context denotes application of $\natural$, but an underline of a type in context only means its pullback along $\epsilon$. The idea is that underlines indicate *dependency* on $\natural$-modal variables, to be distinguished of a type itself being $\natural$-modal or not.)

<center>
<img src="/nlab/files/BireflectiveTypesStructureRules-230327.jpg" width="690">
</center>

<center>
<img src="/nlab/files/BireflectiveModalityInferenceRules-230327.jpg" width="690">
</center>

<center>
<img src="/nlab/files/BireflectiveModalityComputationRules-230327.jpg" width="690">
</center>

\linebreak


## Examples

\begin{example}
  For any [[ground field]],
  let $\mathcal{B} \coloneqq Vect_{Set} \coloneqq \int_{S \in Set} Vect S$ be the category of of [[vector bundles]] over [[Sets]], hence of [[indexed set|indexed]] [[vector spaces]]. Then the functor
$$
  Set \xhookrightarrow{\;\; 0 \;\;} Vect_{Set}
$$
which sends any set $S$ to the [[zero object|zero]] vector bundle $S \times \{0\}$ over $S$ is an ambidextrously bireflective subcategory in the sense of Def. \ref{BireflectiveSubcategory}.
\end{example}

## References

The notion of ambidextrously bireflective subcategories is due to:

* {#FOPTST99} [[Peter Freyd]], [[Peter O’Hearn]],  [[A. John Power]], [[M. Takeyama]], [[Ross Street]], [[Robert D. Tennent]], *Bireflectivity*, Theoretical Computer Science **228** 1–2 (1999) 49-76 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00354-5">doi:10.1016/S0304-3975(98)00354-5</a>&rbrack;

Discussion of a [[modal type theory]] for bireflective [[modalities]], in a context of [[linear homotopy type theory]]:

* {#RFL21} [[Mitchell Riley]], [[Eric Finster]], [[Daniel R. Licata]], Section 7.1 in: *Synthetic Spectra via a Monadic and Comonadic Modality* &lbrack;[arXiv:2102.04099](https://arxiv.org/abs/2102.04099)&rbrack;



[[!redirects bireflective subcategories]]


