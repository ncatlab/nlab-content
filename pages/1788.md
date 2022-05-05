

$$
  \array{
  \phantom{
  sSet_{Qu}
    \underoverset
      {{\longrightarrow}}
      {\overset{\Pi_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {\underset{id}{\longleftarrow}}
      {\overset{id}{\longrightarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  }
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longleftarrow}}
      {\overset{L_! \phantom{= A_a}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj}
  \\
  sSet_{Qu}
    \underoverset
      {{\longrightarrow}}
      {\overset{\Pi_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {\underset{id}{\longleftarrow}}
      {\overset{id}{\longrightarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {{\longrightarrow}}
      {\overset{L^\ast = R_!}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {\underset{id}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\simeq_{Qu} }
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{proj}
  \\
  sSet_{Qu}
    \underoverset
      {{\longleftarrow}}
      {\overset{Disc_{red}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {{\longleftarrow}}
      {\overset{L_\ast = R^\ast}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj}
  \\
  sSet_{Qu}
    \underoverset
      {\underset{coDisc_{red}}{\longrightarrow}}
      {\overset{\Gamma_{red}}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}      
  [\mathcal{C}_{red}^{op}, sSet_{Qu}]_{inj}
  \phantom{
    \underoverset
      {{\longleftarrow}}
      {\overset{L_\ast = R^\ast}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}_{inf}^{op}, sSet_{Qu}]_{inj}
  }
  }
$$


$$
  [\mathcal{C}^{op}, sSet]
    \array{
      \underoverset{\bot}{ \phantom{AA}F_!\phantom{AA}  }{\longrightarrow}
      \\
      \underoverset{\bot}{ \phantom{AA}F^\ast\phantom{AA}  }{\longrightarrow}
      \\
      \overset{ \phantom{AA}F_\ast\phantom{AA}  }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]
$$

Now let 

$$
  \mathcal{C}
    \underoverset
      {\underset{\phantom{AA}R\phantom{AA}}{\longleftarrow}}
      {\overset{\phantom{AA}L\phantom{AA}}{\longrightarrow}}
      {\bot}
  \mathcal{D}
$$

be a [[adjoint pair|pair]] of [[adjoint functors]]. By [[Kan extension]] this induces an [[adjoint quadruple]] between [[categories of simplicial presheaves]]

$$
  [\mathcal{C}^{op}, sSet]
    \array{
      \underoverset{\bot \phantom{\simeq A_a}}{ L_! \phantom{\simeq A_a} }{\longrightarrow}
      \\
      \underoverset{\bot \phantom{\simeq} \bot }{ L^\ast \simeq R_! }{\longleftarrow}
      \\
      \underoverset{\phantom{A_a \simeq}\bot}{ L_\ast \simeq R^\ast }{\longrightarrow}
      \\
      \overset{ \phantom{A_a \simeq } R_\ast }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]
$$

By the previous example the top three of these form a [[Quillen adjoint triple]]. To see that the bottom three form another, compatible [[Quillen adjoint triple]], we need to show that the following is a [[2-morphism]] in the [[double category of model categories]]:

$$
  \array{
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\overset{ \phantom{AA} id \phantom{AA} }{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}   
    \\
    {}^{\mathllap{id}}
    \Big\downarrow
      &{}^{ \mathllap{ id } }\swArrow& 
    \Big\downarrow{}^{ R^\ast }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{ \phantom{AA}R^\ast\phantom{AA} }{\longrightarrow}&
    [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
  }
$$

But since $R^\ast \mathbf{X} = \mathbf{X}(R(-))$ is given by precomposition, this functor preserves all object-wise cofibrations/fibrations weak equivalences, and hence is

1. a [[left Quillen functor]] $[\mathcal{C}^{op}, sSet_{Qu}]_{inj} \overset{R^\ast}{\to} [\mathcal{D}^{op}, sSet_{Qu}]_{inj}$;

1. a [[right Quillen functor]] $[\mathcal{C}^{op}, sSet_{Qu}]_{proj} \overset{R^\ast}{\to} [\mathcal{D}^{op}, sSet_{Qu}]_{proj}$;

But since also $[\mathcal{C}^{op}, sSet_{Qu}]_{inj} \overset{id}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$ is a right Quillen functor, the second point implies that $R^\ast$ is also 

1. a [[right Quillen functor]] $[\mathcal{C}^{op}, sSet_{Qu}]_{inj} \overset{R^\ast}{\to} [\mathcal{D}^{op}, sSet_{Qu}]_{proj}$.

This demonstrates the above square.



Finally to check that $Ho(id)$ is invertible


But since $\mathbf{X}$ 


Hence in conclusion, we have a [[Quillen adjoint quadruple]]

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
      \underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ L_! \phantom{\simeq A_a} }{\longrightarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ L^\ast \simeq R_! }{\longleftarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ L_\ast \simeq R^\ast }{\longrightarrow}
      \\
      \overset{ \phantom{A_a \simeq } R_\ast }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]_{proj}
$$


$\,$

Now let 

$$
  \ast
    \array{
      \phantom{\underoverset{\bot}{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}}
      \\
      \underoverset{\bot}{\phantom{AA}\Pi\phantom{AA}}{\longleftarrow}
      \\
      \underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}
    }
  CartSp
    \array{
      \underoverset{\bot}{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}
      \\
      \underoverset{}{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}
      \\
      \phantom{\underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}}
    }
  FormalCartSp
$$

This induces [[Quillen adjoint quadruples]] of the form

$$
  sSet_{Qu}
  \;\;
    \array{
      \phantom{\underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \iota_{inf} }{\hookrightarrow}}
      \\
      \underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ \Pi }{\longleftarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ Disc }{\hookrightarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \Gamma }{\longleftarrow}
      \\
      \overset{ coDisc }{\hookrightarrow}
    }
  \;\;
  [CartSp^{op}, sSet_{Qu}]_{proj/inj}
  \;\;
    \array{
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \iota_{inf} }{\hookrightarrow}
      \\
      \underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ \Pi_{inf} }{\longleftarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ Disc_{inf} }{\hookrightarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \Gamma_{inf} }{\longleftarrow}
      \\
      \phantom{\overset{ coDisc }{\longrightarrow}}
    }
  \;\;
  [FormalCartSp^{op}, sSet_{Qu}]_{proj}
$$


Finally let

$$
  \ast
    \array{
      \phantom{\underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}}      
      \\
      \phantom{\underoverset{\bot}{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}}
      \\
      \underoverset{\bot}{\phantom{AA}\Pi\phantom{AA}}{\longleftarrow}
      \\
      \underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}
    }
  CartSp
    \array{
      \phantom{\underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}}      
      \\
      \underoverset{\bot}{\phantom{AA}\iota_{inf}\phantom{AA}}{\hookrightarrow}
      \\
      \underoverset{}{\phantom{AA}\Pi_{inf}\phantom{AA}}{\longleftarrow}
      \\
      \phantom{\underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}}
    }
  FormalCartSp
    \array{
      \underoverset{\bot}{\phantom{AA}even\phantom{AA}}{\longleftarrow}      
      \\
      \underoverset{\bot}{\phantom{AA}\iota_{sup}\phantom{AA}}{\hookrightarrow}      
      \\
      \underoverset{}{\phantom{AA}\Pi_{sup}\phantom{AA}}{\longleftarrow}
      \\
      \phantom{\underoverset{}{\phantom{A}Disc\phantom{A}}{\hookrightarrow}}
    }
  SuperFormalCartSp
$$

This induces [[Quillen adjoint quadruples]] of the form

$$
  sSet_{Qu}
  \;\;
    \array{
      \phantom{\underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ even }{\longleftarrow}}
      \\
      \phantom{\underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \iota_{inf} }{\hookrightarrow}}
      \\
      \underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ \Pi }{\longleftarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ Disc }{\hookrightarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \Gamma }{\longleftarrow}
      \\
      \overset{ coDisc }{\hookrightarrow}
    }
  \;\;
  [CartSp^{op}, sSet_{Qu}]_{proj/inj}
  \;\;
    \array{
      \phantom{\underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ even }{\longleftarrow}}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \iota_{inf} }{\hookrightarrow}
      \\
      \underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ \Pi_{inf} }{\longleftarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ Disc_{inf} }{\hookrightarrow}
      \\
      \underoverset{ \phantom{\phantom{{}_{Qu}}\bot_{Qu}} }{ \Gamma_{inf} }{\longleftarrow}
      \\
      \phantom{\overset{ coDisc }{\longrightarrow}}
    }
  \;\;
  [FormalCartSp^{op}, sSet_{Qu}]_{proj}
  \;\;
    \array{
      \underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ even }{\longleftarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \iota_{sup} }{\hookrightarrow}
      \\
      \underoverset{\phantom{{}_{Qu}}\bot_{Qu} }{ \Pi_{sup} }{\longleftarrow}
      \\
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ Disc_{sup} }{\hookrightarrow}
      \\
      \underoverset{ \phantom{\phantom{{}_{Qu}}\bot_{Qu}} }{ \Gamma_{sup} }{\longleftarrow}
      \\
      \phantom{\overset{ coDisc }{\longrightarrow}}
    }
  \;\;
  [SuperFormalCartSp^{op}, sSet_{Qu}]_{proj/inj}
$$


$x^ab$
























