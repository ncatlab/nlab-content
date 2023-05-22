
\begin{proposition}
  For $\mathcal{C}$ a category with all [[Cartesian products]], its [[free cocompletion]] $PSh_{\sqcup}(\mathcal{C})$ also has [[products]] and they [[distributive category|distribute]] over the [[coproducts]].
\end{proposition}
\begin{proof}
  This is readily seen by component inspection, but it may be instructive to see it from more abstract reasoning.

Namely, with the free cocompletion understood as the [[Grothendieck construction]] on the system of [[product categories]], $PSh_{\sqcup}(\mathcal{C}) \,\simeq\, \int_{S \in Set} \mathcal{C}^S$, its cartesian produducts are computed by the general formula for limits in Grothendieck constructions ([here](Grothendieck+construction#CoLimitsInAGrothendieckConstruction)) as the "external cartesian product" ([here](Grothendieck+construction#CartesianProductInGrothendieckConstruction), we now show binary products only, just for ease notation):
$$
  X_S,\, Y_T \,\in\, \textstyle{\int}_{S \in Set} \mathcal{C}
  \;\;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;\;
  X_S \times Y_T 
  \;\simeq\;
  \Big(
  \big(
    (pr_S)^\ast X
  \big) 
    \times_{S \times T} 
  \big(
    (pr_T)^\ast Y
  \big)   
  \Big)_{S \times T}
  \,.
$$
Of course this comes down to the expected component formula
$$
  s \in S
  ,\,
  t \in T
  \;\;\;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;\;\;
  \Big(
  \big(
    (pr_S)^\ast X
  \big) 
    \times_{S \times T} 
  \big(
    (pr_T)^\ast Y
  \big)   
  \Big)_{s,t}
  \;\;
  =
  \;\;
  X_s \times Y_t 
  \;\;\;\;
  \in
  \;\;
  \mathcal{C}
  \,.
$$

Now

$$
  \begin{array}{ll}
  X_S 
  \,\times\,
  \big(
    Y_T
    \amalg
    Y'_{T'}
  \big)
  \\
  \;\simeq\;
  X_S 
  \,\times\,
  \big(
    (q_T)_! X
    \sqcup 
    (q_{T'})_! Y
  \big)_{T \sqcup T'}
  \\
  \;\simeq\;
  \big(
    (pr_S)^\ast X
  \big)
    \times
  \Big(
  (pr_{T \sqcup T'})^\ast
  \big(
    (q_T)_! X
    \sqcup 
    (q_{T'})_! Y
  \big)
  \Big)_{T \sqcup T'}
  \\
  \;\simeq\;
  \bigg(
  \big(
    (pr_S)^\ast X
  \big)
    \times
  \Big(
  \big(
    (pr_{T \sqcup T'})^\ast
    (q_T)_! X
  \big)
    \sqcup 
  \big(
    (pr_{T \sqcup T'})^\ast
    (q_{T'})_! Y
  \big)
  \Big)
  \bigg)_{S \times T \sqcup S \times T'}
  \\
  \;\simeq\;
  \bigg(
  \big(
    (pr_S)^\ast X
  \big)
    \times
  (pr_{T \sqcup T'})^\ast
  \Big(
  \big(
    (q_T)_! X
  \big)
    \sqcup 
  \big(
    (q_{T'})_! Y
  \big)
  \Big)
  \bigg)_{S \times T \sqcup S \times T'}
  \end{array}
$$

$$
  \array{   
    S \times T
    &\overset{\; id_S \times q_T \;}{\longrightarrow}&
    S \times (T \sqcup T')
    \\
    \mathllap{{}^{pr_T}}
    \Big\downarrow
    &&
    \Big\downarrow
    \mathrlap{{}^{pr_{T \sqcup T'}}}
    \\
    T 
      &\underset{\;\; q_T \;\;}{\longrightarrow}&
    T \sqcup T'
  }
$$

\end{proof}


$$
  \mathrm{idToIso}(x, y)
  \;\colon\;
  (x =_A y) 
  \;
  \to 
  \;
  x \cong_A y
$$


$$
  \textstyle{\coprod}
  \displaystyle{\widehat{\otimes}}
  \scriptstyle{a b c}
  \scriptscriptstyle{a a a}
$$

For the following proposition we use the left-handed convention for component maps in morphisms in the Grothendieck construction:
$$
  \phi_f \,\colon\, \mathscr{V}_X \to \mathscr{V}'_{X'}
  \;\;\;\;\;\;
  \text{shall stand for}
  \;\;\;\;\;\;
  \begin{array}{rcl}  
    X &\xrightarrow{f}& X'
    \\
    f_!\mathscr{V} &\xrightarrow{\phi}& \mathscr{V}'
  \end{array}
$$
\begin{proposition}
  In the situation above, the $\boxtimes$-[[pushout-product]] (with respect to the external tensor product) is given by 
$$
  \big(
    \phi_f 
  \big)
    \,\widehat{\boxtimes}\, 
  \big(
    \gamma_g
  \big)
  \;\;\;
  \simeq
  \;\;\;
  \Big(
    \big(
      (pr_{X'})^\ast \phi
    \big)
    \,\widehat{\otimes}\,
    \big(
      (pr_{Y'})^\ast \gamma
    \big)
  \Big)_{ f \,\widehat{\times}\, g }
$$
\end{proposition}
\begin{proof}
By the general formula for colimits in Grothendieck constructions ([here](Grothendieck+construction#CoLimitsInAGrothendieckConstruction)) the underlying colimit in the base category is the evident one
\begin{tikzcd}
  X \times Y 
  \ar[r, "{ id\,\times\, g }"{description}]
  \ar[d, "{ f \,\times\, \mathrm{id} }"{description}]
  &
  X \times Y'
  \ar[d, "{ q_r }"{description}]
  \ar[ddr, bend left=15, "{ f \,\times\, \mathrm{id} }"{description}]
  &[-40pt]
  \\
  X' \times Y
  \ar[r, "{ q_l }"{description}]
  \ar[drr, bend right=15, "{ \mathrm{id} \,\times\, g}"{description}]
  &
  f\,\widehat{\times}\,g
  \ar[dr, dashed]
  \\[-20pt]
  && X' \times Y'
\end{tikzcd}
and the component map over the dashed morphism is the colimiting cocone of the diagram obtained from pushing the separate component maps along the [[coprojections]] $q_\cdot$ to form a span in $\mathbf{C}_{f \widehat{\times} g}$. This yields:
$$
  \begin{array}{ll}
  (f \widehat{\times} g)_!
  \Bigg(
    \bigg(
      (q_l)_! 
      \Big(
        \big(
          (pr_{X'})^\ast \phi
        \big)
        \otimes
        \big(
          (pr_{Y})^\ast
          \mathrm{id}_{\mathscr{W}}
        \big)
      \Big)
    \bigg)
    \wedge
    \bigg(
      (q_r)_! 
      \Big(
        \big(
          (pr_X)^\ast
          \mathrm{id}_{\mathscr{V}}
        \big)
        \otimes
        \big(
          (pr_{Y'})^\ast \gamma
        \big)
      \Big)
    \bigg)
  \Bigg)
  \\
  \;\simeq\;
  \Bigg(
    \bigg(
      (f \widehat{\times} g)_!
      (q_l)_! 
      \Big(
        \big(
          (pr_{X'})^\ast \phi
        \big)
        \otimes
        \big(
          (pr_{Y})^\ast
          \mathrm{id}_{\mathscr{W}}
        \big)
      \Big)
    \bigg)
    \wedge
    \bigg(
      (f \widehat{\times} g)_!
      (q_r)_! 
      \Big(
        \big(
          (pr_X)^\ast
          \mathrm{id}_{\mathscr{V}}
        \big)
        \otimes
        \big(
          (pr_{Y'})^\ast \gamma
        \big)
      \Big)
    \bigg)
  \Bigg)
  &
  \begin{array}{l}
  \text{since the left adjoint}\; (-)_! 
  \\
  \text{preserves pushouts}
  \end{array}
  \\
  \;\simeq\;
  \Bigg(
    \bigg(
      (id \otimes g)_!
      \Big(
        \big(
          (pr_{X'})^\ast \phi
        \big)
        \otimes
        \big(
          (pr_{Y})^\ast
          \mathrm{id}_{\mathscr{W}}
        \big)
      \Big)
    \bigg)
    \wedge
    \bigg(
      (f \otimes id)_!
      \Big(
        \big(
          (pr_X)^\ast
          \mathrm{id}_{\mathscr{V}}
        \big)
        \otimes
        \big(
          (pr_{Y'})^\ast \gamma
        \big)
      \Big)
    \bigg)
  \Bigg)
  &
  \begin{array}{l}
  \text{by commutativity of} 
  \\
  \text{the above diagram}
  \end{array}
  \\
  \;\simeq\;
  \Bigg(
    \bigg(
      \Big(
        \big(
          (pr_{X'})^\ast \phi
        \big)
        \otimes
        \big(
          (pr_{Y})^\ast
          \mathrm{id}_{f_!\mathscr{W}}
        \big)
      \Big)
    \bigg)
    \wedge
    \bigg(
      \Big(
        \big(
          (pr_X)^\ast
          \mathrm{id}_{f_!\mathscr{V}}
        \big)
        \otimes
        \big(
          (pr_{Y'})^\ast \gamma
        \big)
      \Big)
    \bigg)
  \Bigg)
   &
  \text{by the above result}
  \\
  \;\simeq\;
  \big(
    (pr_{X'})^\ast \phi
  \big)
  \,\displaystyle{\widehat{\otimes}}\,
  \big(
    (pr_{Y'})^\ast \gamma
  \big)
  &
  \text{by definition}
  \end{array}
$$
\end{proof}

