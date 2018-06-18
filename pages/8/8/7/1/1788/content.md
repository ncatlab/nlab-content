| $\phantom{A}$[[category theory]] <br/> $\phantom{A}$and <br/> $\phantom{A}$[[topos theory]] |   | $\phantom{A}$[[geometry]] of [[generalized spaces]] <br/> $\phantom{A}$probe-able by given model [[spaces]] |
|-------|--|---------|
| $\phantom{A}$[[representable presheaf]]$\phantom{A}$ | $\phantom{A}$Expl. \ref{CategoryOfPresheaves}$\phantom{A}$ |  $\phantom{A}$model [[space]] regarded as [[generalized space]] |
| $\phantom{A}$[[Yoneda lemma]] | $\phantom{A}$Prop. \ref{YonedaLemma}$\phantom{A}$  |  $\phantom{A}$sets of probes of [[generalized spaces]] really are <b/> $\phantom{A}$sets of maps from model [[spaces]] $\phantom{A}$ |
| $\phantom{A}$[[Yoneda embedding]] $\phantom{A}$ | $\phantom{A}$Prop. \ref{YonedaEmbedding}$\phantom{A}$ |  $\phantom{A}$nature of model [[spaces]] is preserved when <br/> $\pahntom{A}$regarding them as [[generalized spaces]] $\phantom{A}$ |
| $\phantom{A}$[[sheaf|sheaf condition]] | $\phantom{A}$Def. \ref{Sheaf}$\phantom{A}$ <br/> $\phantom{A}$Prop. \ref{CechGroupoidCoRepresents}$\phantom{A}$ | $\phantom{A}$plots of [[generalized spaces]] satisfy [[local-to-global principle]] $\phantom{A}$ |

\[
  \label{YonedaFunctor}
  \array{
    y & \colon &
    \mathcal{C}
      &\longrightarrow&
    [\mathcal{C}^{op}, Set]
    \\
    \\
    && && && c_1 &\overset{g}{\longrightarrow}& c_2
    \\
    &&
    X
    &\mapsto&
    Hom_{\mathcal{C}}(-,X) 
     &\phantom{AA}\colon\phantom{AA}& 
    Hom_{\mathcal{C}}(c_1,X) 
      &\overset{Hom_{\mathcal{C}}( g, X ) }{\longleftarrow}& 
    Hom_{\mathcal{C}}(c_2, X)
    \\
    &&
    {}^{\mathllap{ f }}\big\downarrow
    &&
    \big\downarrow^{ \mathrlap{ Hom_{\mathcal{C}}(-,f) } } 
    &&
    \big\downarrow^{ \mathrlap{ Hom_{\mathcal{C}}( c_2, f )  } } 
    && 
    \big\downarrow^{ \mathrlap{ Hom_{\mathcal{C}}(c_1,f) } }
    \\
    &&
    Y &\mapsto& 
    Hom_{\mathcal{C}}(-,Y) 
      &\phantom{AA}\colon\phantom{AA}& 
    Hom_{\mathcal{C}}(c_1,Y) 
      &\overset{Hom_{\mathcal{C}}( g, Y ) }{\longleftarrow}& 
    Hom_{\mathcal{C}}(c_2, Y)
  } 
\]
