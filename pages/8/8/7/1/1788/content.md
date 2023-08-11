
\begin{example}
\linebreak
For $W \,\in\,$ [[FiniteSets]], the $W$-fold [[direct sum]] 
$\mathrm{Q}W \equiv \underset{W}{\oplus} \mathbb{1}$ of the [[ground field]] $\mathbb{1}$ -- with its inherited [[direct sum]]-[[associative algebra]]-[[structure]] -- becomes a [[Frobenius algebra]] by taking the

* [[counit]] to be the canonical [[sum]]-operation;

* [[coproduct]] to be map induced by the [[diagonal]] on indices.

In components, if we choose the canonical [[linear basis]]
$$
  \mathrm{Q}W
  \;\simeq\;
  Span
  \Big(
    \big\{
      \left\vert w \right\rangle
    \big\}_{w \colon W}
  \Big)
$$
then on basis vectors these structure maps are expressed as follows (where "$\delta$" is the [[Kronecker delta]]):

\begin{tikzcd}[sep=0pt]
  \mathbb{K}
  \ar[rr, "{ \mathrm{unit} }"]
  &&
  \mathrm{Q}W
  \\
  1 &\mapsto& 
  \sum_{w} \left\vert w \right\rangle
\end{tikzcd}

\begin{tikzcd}[sep=0pt]
  \mathrm{Q}W
  \otimes 
  \mathrm{QW}
  \ar[rr, "{ \mathrm{prod} }"]
  &&
  \mathrm{Q}W
  \\
  \left\vert w, \, w' \right\rangle
  &\mapsto&
  \delta_w^{w'}
  \,
  \left\vert w \right\rangle
\end{tikzcd}

\begin{tikzcd}[sep=0pt]
  \mathrm{Q}W
  \ar[rr, "{ \mathrm{coprod} }"]
  &&
  \mathrm{Q}W
  \otimes
  \mathrm{Q}W
  \\
  \left\vert w \right\rangle
  &\;\mapsto\;&
  \left\vert w,\, w \right\rangle
\end{tikzcd}

\begin{tikzcd}[sep=0pt]
  \mathrm{Q}W
  \ar[rr, "{ \mathrm{counit} }"]
  &\;\;&
  \mathbb{K}
  \\
  \left\vert w \right\rangle
  &\mapsto&
  1
\end{tikzcd}

In these components, the Frobenius property is this equation:


\begin{tikzcd}[sep=0pt]
  \mathrm{Q}W
  \otimes
  \mathrm{Q}W
  \ar[
    rrrr, 
    "{ \mathrm{id} \,\otimes\, \mathrm{coprod} }"  
  ]
  \ar[
    dddd, 
    "{ 
      \mathrm{coprod} \,\otimes\, \mathrm{id} 
    }"{description}
   ]
  &&&&
  \mathrm{Q}W
  \otimes
  \mathrm{Q}W
  \otimes
  \mathrm{Q}W
  \ar[
    dddd, 
    "{ 
      \mathrm{prod} \,\otimes\, \mathrm{id} 
    }"
  ]
  \\
  &
  \left\vert w,\, w'\right\rangle
  &\mapsto&
  \left\vert w,\, w',\, w' \right\rangle  
  \\
  &
  \rotatebox[origin=c]{-90}{$\mapsto$}
  &&
  \rotatebox[origin=c]{-90}{$\mapsto$}
  \\
  &
  \left\vert w,\, w,\, w' \right\rangle
  &\mapsto&
  \delta_{w}^{w'}
  \left\vert w,\, w' \right\rangle
  \\
  \mathrm{Q}W 
  \otimes
  \mathrm{Q}W 
  \otimes
  \mathrm{W}W
  \ar[
    rrrr, 
    "{ 
      \mathrm{id} \,\otimes\, \mathrm{prod} 
    }"{swap}
  ]
  &&&&
  \mathrm{Q}W 
  \otimes
  \mathrm{Q}W
\end{tikzcd}

Elementary as this example may be, it embdies some important principles:

For $\mathbb{K} \,=\, \mathbb{C}$ the [[complex numbers]], the corresponding [[Frobenius monad]] $\mathrm{Q}W \otimes (\text{-}) \,\colon\, \mathbb{C}Mod \to \mathbb{C}Mod$ (or rather $\mathrm{Q}W \otimes (\text{-}) \,\colon\, FinDimHilb \to FinDimHilb$) has been proposed &lbrack;[Coecke & Pavlović 2008](quantum+measurement#CoeckePavlović08)&rbrack; to reflect aspects of [[quantum measurement]] in terms of [[quantum information via dagger-compact categories]] and is used as such in the *[[zxCalculus]]* (where the Frobenius property is embodied by "spider diagrams"). Various authors discuss the Frobenius algebras $\mathrm{Q}W$ in this context, see the references [there](quantum+information+theory+via+dagger-compact+categories#MeasurementReferencesQuantumInformationTheoryViaStringDiagrams).

From another perspective on the same phenomenon (discussed at *[[quantum circuits via dependent linear types]]*): The $\mathrm{Q}W$-[[writer monad]] underlying the [[Frobenius monad]] $\mathrm{Q}W \otimes (-) \,\colon\, \mathbb{K}Mod \to \mathbb{K}Mod$, 
is a linear version of the [[reader monad]], as such discussed at *[[quantum reader monad]]*. Regarded as an [[monad in computer science|computational effect]] its [[Kleisli morphisms]] encode [[quantum gates]] with an "indefiniteness"-effect (in the sense of [quantum modal logic](necessity+and+possibility#ModalQuantumLogic)) whose "[handling](monad+in+computer+science#MonadModulesInIdeaSection)" is the process of [[quantum measurement]].

In particular, the [[algebra over a monad|algebras]] (hence also the corresponding [[coalgebra over a comonad|coalgebras]]) over $\mathrm{Q}W \otimes (\text{-})$ the [[dependent linear types|$W$-dependent $\mathbb{K}$-linear types]], namely the $\mathbb{K}$-[[vector bundles]] over $W$, hence the $W$-[[indexed sets]] of $\mathbb{K}$-[[vector spaces]], understood as residual [[spaces of quantum states]] after [[quantum state collapse|after]] collapse to measurement result $w \in W$.
\end{example}
