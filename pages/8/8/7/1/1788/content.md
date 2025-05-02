

> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***


### Groupoid formulation


\begin{proposition}
**(resolved left induced representation)**
  The functor $\widehat{\mathbf{B}\iota}$ (eq:ResolutionOfBIota) has a [[left adjoint]] $\big(\widehat{\mathbf{B}\iota}\big)_!$ given by
$$
  \mathscr{V}
  \,\in\,
  Func\big(
    G \backslash\!\backslash G/H
  \big)
  \;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;
  \big(\widehat{\mathbf{B}\iota}\big)_!
  \mathscr{V}
  \;\coloneqq\;
  \underset{
    g\cdot H
  }{\bigoplus}
  \mathscr{V}_{g\cdot H}
  \,,
$$
where on the right we let $G$ act in the evident way between direct summands.
\end{proposition}
\begin{proof}
The [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism)  is essentially tautologous:
$$  
  \left.
  \begin{array}{l}
    \mathscr{V} \,\in\,  
    Func\big( G\backslash\!\backslash G/H, Vect\big)
    \\
    \mathscr{W} \,\in\,
    Func\big( G\backslash\!\backslash \ast, Vect\big)
  \end{array}
  \right\}
  \;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;
  \frac{
    \Big(
    \displaystyle{
    \underset{
      g\cdot H \in G/H
    }{\bigoplus}
    \mathscr{V}_{{}_{g\cdot H}}
    }
    \Big)
    \xrightarrow{
      \Big(
        f_{{}_{g \cdot H}}
      \Big)_{g \cdot H \in G/H}
    }
    \mathscr{W}
  }{
    g\cdot H 
    \;\;\;\vdash\;\;\;
    \mathscr{V}_{g \cdot H}
    \xrightarrow{\;\;
      f_{g \cdot H}
    \;\;}
    \mathscr{V}
    \mathrlap{\,,}
  }
$$
where we don't display the $G$-action, which is however evident and evidently respected.
\end{proof}


[[InducedRep-LeftInductionByResolution.png:file]]


On electrodynamics via field strengths instead of gauge potentials:

* Joshua Newey, John Terning, Christopher B. Verhaaren: *Geometrizing the Anomaly* &lbrack;[arXiv:2504.16998](https://arxiv.org/abs/2504.16998)&rbrack;


