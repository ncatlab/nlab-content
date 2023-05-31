

\begin{proposition}
Give a [[contravariant functor|contravariant]] [[pseudofunctor]]
$$
  \array{
    \mathbf{D}^{op}
    &\overset{C_{(-)}}{\longrightarrow}&
    Cat
    \\
    \mathbf{x} 
      &\mapsto& 
    C_{\mathbf{x}}
    \\
    \Big\downarrow\mathrlap{{}^{\mathbf{f}}}
    &&
    \Big\uparrow\mathrlap{{}^{\mathbf{f}^\ast}}
    \\
    \mathbf{y}
      &\mapsto&
    C_{\mathbf{y}}
  }
$$
and a pair of [[adjoint functors]] of the form
$$
  \mathcal{D}
  \underoverset
    {\underset{R}{\longleftarrow}}
    {\overset{L}{\longrightarrow}}
    {\;\; \bot \;\;}
  \mathbf{D}
$$
then there is an induced [[adjoint functor|adjunction]] between the [[Grothendieck constructions]] on $C_{(-)}$ and on $C_{L(-)}$
$$
  \Bigg\{
    \mathscr{V}_{x}
      \xrightarrow{ \phi_{f} }
    \mathscr{V}_{x'}
    \;\displaystyle{\Bigg\vert}\;
    \array{
      \mathscr{V} 
        &\xrightarrow{ \phi }& 
      L(f)^\ast \mathscr{V}' 
      & \in C_{L(x)}
      \\
      x 
        &\xrightarrow{ f }& 
      y 
      & \in \mathcal{D}
    }
  \Bigg\}
  \;
    \equiv
  \;
  \Big(
    \underset
      {x \in \mathcal{D}}
      {\textstyle{\int}} 
    C_{L(x)}
  \Big)
  \;
  \underoverset
    {\underset{\tilde R}{\longleftarrow}}
    {\overset{\tilde L}{\longrightarrow}}
    {\;\; \bot \;\;}
  \;
  \Big(
    \underset
      {\mathbf{x} \in \mathbf{D}}
      {\textstyle{\int}} 
    C_{\mathbf{x}}
  \Big)
  \;
    \equiv
  \;
  \Bigg\{
    \mathscr{V}_{\mathbf{x}}
      \xrightarrow{ \phi_{\mathbf{f}} }
    \mathscr{V}_{\mathbf{x}'}
    \;\displaystyle{\Bigg\vert}\;
    \array{
      \mathscr{V} 
        &\xrightarrow{ \phi }& 
      \mathbf{f}^\ast \mathscr{V}' 
      & \in C_{\mathbf{x}}
      \\
      x 
        &\xrightarrow{ \mathbf{f} }& 
      y 
      & \in \mathbf{D}
    }
  \Bigg\}
  \mathrlap{\,,}
$$
where $\tilde L$ acts as $L$ on [[underlying]] morphisms and as the [[identity functor|identity]] on components:
$$
  \array{
  \mathscr{V}_{x}
  \\
  \Big\downarrow\mathrlap{{}^{\phi_{f}}}
  \\
  \mathscr{V}'_{x'}
  }
  \;\;\;\;\;\;\;
  \overset{\tilde L}{\mapsto}
  \;\;\;\;\;
  \array{
  \mathscr{V}_{L(x)}
  \\
  \Big\downarrow\mathrlap{{}^{\phi_{L(f)}}}
  \\
  \mathscr{V}'_{L(x')}
  \mathrlap{\,,}
  }
$$
while $\tilde R$ acts as $R$ on [[underlying]] morphisms and on components by [[base change]] along the [[adjunction unit]] $\epsilon_{\mathbf{x}} \colon L \circ R(\mathbf{x}) \to \mathbf{x}$:
$$
  \array{
  \mathscr{V}_{\mathbf{x}}
  \\
  \Big\downarrow\mathrlap{{}^{\phi_{\mathbf{f}}}}
  \\
  \mathscr{V}'_{\mathbf{x}'}
  }
  \;\;\;\;\;\;\;
  \overset{\tilde R}{\mapsto}
  \;\;\;\;\;
  \array{
    \big(\epsilon_{\mathbf{x}}^\ast 
      \mathscr{V}\big)_{R(\mathbf{x})}
    \\
    \Big\downarrow
    \mathrlap{{}^{ (\epsilon_\mathbf{x}^\ast \phi)_{ R(\mathbf{f}) } }}
    \\
    \big(\epsilon_{\mathbf{x}}^\ast \mathscr{V}\big)_{ R(\mathbf{x}')}
  }
$$
\end{proposition}
\begin{proof}
First notice that $\tilde R$ is indeed well-defined in that we have an [[equality]] on the right of
$$
  \epsilon_{\mathbf{x}}^\ast \phi
  \;\colon\;
  \epsilon_{\mathbf{x}}^\ast \mathscr{V}
  \longrightarrow
  \epsilon_{\mathbf{x}}^\ast \mathbf{f}^\ast \mathscr{V}'
  =
  \big(L R(\mathbf{f})\big)^\ast
  \epsilon_{\mathbf{x}'}^\ast \mathscr{V}'
$$
induced from the [[commuting square|commutativity]] of the [[naturality square]] of the [[adjunction counit]]:
$$
  \array{
    L R(\mathbf{x}) 
    &\overset{ L R(\mathbf{f}) }{\longrightarrow}&
    L R(\mathbf{x}')
    \\
    \mathllap{{}^{ \epsilon_{\mathbf{x}} }}
    \Big\downarrow
    &&
    \Big\downarrow
    \mathrlap{{}^{ \epsilon_{\mathbf{x}'} }}
    \\
    \mathbf{x} 
      &\underset{\; \mathbf{f} \;}{\longrightarrow}& 
    \mathbf{x}'
    \mathrlap{\,.}
  }
$$

Now
if we write $f \colon x \to R(\mathbf{x}')$ for the $(L \dashv R)$-[[adjunct]] of a given $\mathbf{f} \colon L(x) \to \mathbf{x}'$ then we have natural bijections
$$
\begin{array}{ll}
  \Big\{
    \tilde L\big( \mathscr{V}_x \big)
    \xrightarrow{ \phi_{\mathbf{f}} }
    \mathscr{V}'_{\mathbf{x}'}
  \Big\}
  \\
  \;\simeq\;
  \Big\{
    \mathscr{V}_{L(x)}
    \xrightarrow{ \phi_{\mathbf{f}} }
    \mathscr{V}'_{\mathbf{x}'}
  \Big\}
  &
  \text{by def.}
  \\
  \;\simeq\;
  \Big\{
    \mathscr{V}_{x}
    \xrightarrow{ \phi_{f} }
    \big(
      \epsilon^\ast_{\mathbf{x}'}
      \mathscr{V}'
    \big)_{R(\mathbf{x}')}
  \Big\}  
  &
  \text{see below}
  \\
  \;\simeq\;
  \Big\{
    \mathscr{V}_{x}
    \xrightarrow{ \phi_{f} }
    \tilde R \big(
      \mathscr{V}'_{\mathbf{x}'}
    \big)
  \Big\}     
  &
  \text{by def.,}
\end{array}
$$
where the one step that is not a definition is on [[underlying]] morphisms the $(L \dashv R)$-[hom-isomorphism](adjoint+functor#eq:HomIsomorphismForAdjointFunctors) 
$$
\begin{array}{ll}
  \Big\{
    L(x) \xrightarrow{ \mathbf{f} } \mathbf{x}'
  \Big\}
  \;\simeq\;
  \Big\{
    x \xrightarrow{ f } R(\mathbf{x}')
  \Big\}
\end{array}
$$
and on components the following natural bijection
$$
\begin{array}{ll}
  \Big\{
    \mathscr{V}
    \xrightarrow{ \phi }
    \mathbf{f}^\ast \mathscr{V}'
  \Big\}
  \\
  \;\simeq\;
  \Big\{
    \mathscr{V}
    \xrightarrow{ \phi }
    \big( \epsilon_{\mathbf{x}'} \,\circ\, L(f) \big)^\ast 
    \mathscr{V}'
  \Big\}
  &
  \text{ formula for adjuncts }
  \\
  \;\simeq\;
  \Big\{
    \mathscr{V}
    \xrightarrow{ \phi }
    L(f)^\ast 
    \big(
    \epsilon_{\mathbf{x}'}^\ast
    \mathscr{V}'
    \big)
  \Big\}
  &
  \text{ pseudo-functoriality }
\end{array}
$$
where the first step uses the general formula $\mathbf{f} \,=\, \epsilon_{\mathbf{x}'} \circ L(f)$ ([here](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit)) that expresses [[adjuncts]] in terms of the [[counit of an adjunction|counit]] and the second step is the [[contravariant functor|contravariant]] [[pseudo-functor|pseudo-functoriality]] of $C_{(-)}$.

This establishes a [hom-isomorphism](adjoint+functor#eq:HomIsomorphismForAdjointFunctors) exhibiting adjoint functors $\tilde L \dashv \tilde R$.
\end{proof}