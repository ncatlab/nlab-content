

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***


### Groupoid formulation

A first step towards a deeper understanding for what's going on with induced representations is to [[resolution|resolve]] the subgroup inclusion $H \xhookrightarrow{\iota} G$ to a ([[Kan fibration|Kan]]) [[fibration]] of [[groupoids]].

To that end, recall for any [[group action]] $G \curvearrowright S$ on a [[set]] $S$ the [[action groupoid]]

\begin{imagefromfile}
    "file_name": "InducedRep-ActionGroupid.png",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

Examples are [[delooping groupoids]] $\mathbf{B}G$ and "[[homotopy quotient|homotopy]] [[double cosets]]" like $G \backslash\!\backslash G\!/\!H$:


\begin{imagefromfile}
    "file_name": "InducedRep-DeloopingGroupoid.png",
    "width": 760,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

where our variance convention is such that [[functors]] $\mathbf{B}G \xrightarrow{\;} \mathcal{C}$ are equivalent to *left* [[group actions]] [[action object|in]] $\mathcal{C}$, and in particular functors $\mathbf{B}G \xrightarrow{\;} Vec$ are directly identified with [[linear representations]] of $G$:

$$
  Func(\mathbf{B}G,\, Vec)
  \;\simeq\;
  G Rep
  \,.
$$

Accordingly, for $\mathcal{G} \in Grpd$ any [[groupoid]], a functor $\mathcal{G} \xrightarrow{\;} Vec$ is a *[[groupoid representation]]*.

\begin{proposition}\label{ResolvingHRepsToGroupoidReps}
For $H \xhookrightarrow{\iota} G$ a [[subgroup]] inclusion,
the [[homotopy quotient|homotopy]] [[double coset]] $G \backslash\!\backslash G\!/\!H$  

1. is [[equivalence of groupoids|equivalent]] to the [[delooping groupoid]] of $H$:

   $$
     \mathbf{B}G \,\simeq\, G \backslash\!\backslash G\!/\!H
     \,,
   $$ 

1. such that the canonical functor

   $$
     G \backslash\!\backslash G\!/\!H
     \xrightarrow{\phantom{---}}
     G \backslash\!\backslash \{\ast\}
     \,\simeq\,
     \mathbf{B}G
   $$

   is a [[resolution]] of $\mathbf{B}\iota \,\colon\, \mathbf{B}H \xrightarrow{\;} \mathbf{B}G$ by a [surjective](Kan+fibration#SurjectiveKanFibrations) [[Kan fibration]], 

   [thus](fiber+sequence#HomotopyFiber) exhibiting its ordinary [[fiber]] $G/H$ as the [[homotopy fiber]] of $\mathbf{B}\iota$,

1. the induced [[equivalence of categories|equivalence]] of [[groupoid representation|representation]][[representation categories|-categories]]

   $$
     H Rep 
       \;\simeq\; 
     Func(\mathbf{B}H,\,Vect)
       \;\simeq\;
     Func(G \backslash\!\backslash G\!/\!H,\,Vect)
   $$

   is exhibited by sending a given $G$-representation $\mathscr{V}$ to the groupoid representation $\widehat{\mathscr{V}}$ given by

\begin{imagefromfile}
    "file_name": "InducedRep-ResolvingHRep.png",
    "width": 230,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

\end{proposition}
\begin{proof}
The following functor is evidently both [[essentially surjective functor|essentially surjective]] as well as [[fully faithful functor|fully faithful]], [therefore](equivalence+of+categories#ViaEssentiallySurjectiveAndFullyFaithful) is an [[equivalence of groupoids]]:

\begin{imagefromfile}
    "file_name": "InducedRep-ResolvingBH.png",
    "width": 240,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

The claim that this factors $\mathbf{B}\iota$ through a [surjective](Kan+fibration#SurjectiveKanFibrations) [[Kan fibration]] [[Kan fibration]], as claimed, is immediate from inspection.

Moreover, the following inspection shows that the claimed operation $\widehat{(-)}$ extends to a functor which is a strict [[right inverse]] to precomposition with the previous resolution functor:

\begin{imagefromfile}
    "file_name": "InducedRep-ProofOfResolvingHRep.png",
    "width": 540,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

> (To note here that the [[natural transformation]] in the middle is indeed well-defined, due to the the [[intertwiner|intertwining]]-property of the [[homomorphism]] $\eta$ of [[linear representations]].)

Hence by the [[2-out-of-3]]-property enjoyed by [[equivalences of groupoids]] (cf. the [[canonical model structure on groupoids]]) it follows that $\widehat{(-)}$ is an equivalence, as claimed.
\end{proof}

With this in hand we have an equivalent but "more obvious" re-statement of the existence of left induced representations:

\begin{corollary}
  Under the identification of $H$-representations $\mathscr{V}$ with groupoid representations $\widehat{\mathscr{V}}$ according to Prop. \ref{ResolvingHRepsToGroupoidReps}, their left induced representations are simply the [[direct sum]] of the contributions of $\widehat{\mathscr{V}}$ over the [[homotopy fiber]] of $\mathbf{B}\iota$:

$$
  \underset{
    g\cdot H \in G/H
  }{\bigoplus}
  \widehat{\mathscr{V}}_{g \cdot H}
  \;\;
  \equiv
  \;\;
  \underset{
    g\cdot H \in G/H
  }{\bigoplus}
  \mathbb{K}[g\!\cdot\!H]
  \otimes_H
  \mathscr{V}
  \;\simeq\;
  \mathbb{K}[G]\otimes_H \mathscr{V}
$$

\end{corollary}


On electrodynamics via field strengths instead of gauge potentials:

* Joshua Newey, John Terning, Christopher B. Verhaaren: *Geometrizing the Anomaly* &lbrack;[arXiv:2504.16998](https://arxiv.org/abs/2504.16998)&rbrack;


