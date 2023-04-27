

$$
  \begin{array}{l}
   Hom\big(
    (p_X)^\ast
    \mathscr{V}_\ast
    ,\,
    \mathscr{W}_{X}
  \big)
  \\
  \;\simeq\;
   Hom\big(
    \mathbb{1}_{X}
    \otimes
    \mathscr{V}_{\ast}
    ,\,
    \mathscr{W}_X
  \big)
  \end{array}
$$



$$
  \array{ 
    \mathcal{X}_i
    \times
    \mathcal{Y}
    &
    \overset{\; pr_{\mathcal{X}_i} \;}{\longrightarrow}
    &
    \mathcal{X}_i
    \\
    \mathllap{{q}^{\mathcal{X}_i} \times id_{\mathcal{Y}}}
    \Big\downarrow
    && 
    \Big\downarrow
    \mathrlap{{}^{ q^{\mathcal{X}_i} }}
    \\
    \underset{\underset{j \in I}{\longrightarrow}}{lim}
    \mathcal{X}_j 
       \times 
    \mathcal{Y}
    &
    \underset
      {pr_{\underset{\longrightarrow}{lim}\mathcal{X}}}  
      {\longrightarrow}
    &
    \underset{\underset{j \in I}{\longrightarrow}}{lim} \mathcal{X}_j
  }
$$


$$
  \begin{array}{ll}
  \Big(
  \underset{\underset{i \in I}{\longrightarrow}}{lim}
  \mathscr{V}(i)_{\mathcal{X}_i}
  \Big)
  \boxtimes 
  \mathscr{W}_{\mathcal{Y}}
  \\
  \;\simeq\;
  \left(
  \big(
    \underset{\longrightarrow}{\lim}
    q^{\mathcal{X}}_!\mathscr{V}
  \big)_{\underset{\longrightarrow}{\lim}\mathcal{X}}
  \right)
  \boxtimes
  \mathscr{W}_{\mathcal{Y}}
  &
  \text{colimit in Groth. constr.}
  \\
  \;\simeq\;
  \Big(
    \big(
    (pr_{\underset{\longrightarrow}{lim}\mathcal{X}})^\ast
    (
      \underset{\longrightarrow}{\lim}
      q^{\mathcal{X}}_!\mathscr{V}
    )
    \big)
    \,\otimes\,
    \big(
    (pr_{\mathcal{Y}})^\ast
    \mathscr{W}
    \big)
  \Big)_{
    \big(\underset{\longrightarrow}{\lim}\mathcal{X}\big)
    \times
    \mathcal{Y}
  }
  &
  \text{def. of external tensor}
  \\
  \;\simeq\;
  \Big(
    \big(
      \underset{\longrightarrow}{\lim}
      (pr_{\underset{\longrightarrow}{lim}\mathcal{X}})^\ast
      q^{\mathcal{X}}_!
      \mathscr{V}
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{W}
    \big)
  \Big)_{
    \big(\underset{\longrightarrow}{\lim}\mathcal{X}\big)
    \times
    \mathcal{Y}
  }
  &
  \text{pullback preserves colimits}
  \\
  \;\simeq\;
  \Big(
    \big(
      \underset{\longrightarrow}{\lim}
      (q^{\mathcal{X}} \times id_{\mathcal{Y}} )_!
      (pr_{\mathcal{X}})^\ast
      \mathscr{V}
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{W}
    \big)
  \Big)_{
    \big(\underset{\longrightarrow}{\lim}\mathcal{X}\big)
    \times
    \mathcal{Y}
  }
  &
  \text{Beck-Chevalley}
  \\
  \;\simeq\;
  \bigg(
    \underset{\longrightarrow}{\lim}
    \Big(
    \big(
      (q^{\mathcal{X}} \times id_{\mathcal{Y}} )_!
      (pr_{\mathcal{X}})^\ast
      \mathscr{V}
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{W}
    \big)
    \Big)
  \bigg)_{
    \underset{\longrightarrow}{\lim}
    \big(
    \mathcal{X}
    \times
    \mathcal{Y}
    \big)
  }
  &
  \text{products preserve colimits}
  \\
  \;\simeq\;
  \bigg(
    \underset{\longrightarrow}{\lim}
    (q^{\mathcal{X}} \times id_{\mathcal{Y}} )_!
    \Big(
    \big(
      (pr_{\mathcal{X}})^\ast
      \mathscr{V}
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast
      \mathscr{W}
    \big)
    \Big)
  \bigg)_{
    \underset{\longrightarrow}{\lim}
    \big(
    \mathcal{X}
    \times
    \mathcal{Y}
    \big)
  }
  &
  \text{projection formula}
  \\
  \;\simeq\;
  \underset{\underset{i \in I}{\longrightarrow}}{lim}
  \bigg(
  \Big(
    \big(
      (pr_{\mathcal{X}_i})^\ast \mathscr{V}(i)
    \big)
    \,\otimes\,
    \big(
      (pr_{\mathcal{Y}})^\ast \mathscr{W}
    \big)
  \Big)_{ 
    \underset{\longrightarrow}{lim} 
    (
    \mathcal{X}
    \times
    \mathcal{Y}
    )
  } 
  \bigg)
  &
  \text{colimit in Groth. constr.}
  \\
  \;\simeq\;
  \underset{\underset{i \in I}{\longrightarrow}}{lim}
  \Big(
    \mathscr{V}(i)_{\mathcal{X}_i}
    \,\boxtimes\,
    \mathscr{W}_{\mathcal{Y}}
  \Big)
  &
  \text{def of external tensor}
  \end{array}
$$



