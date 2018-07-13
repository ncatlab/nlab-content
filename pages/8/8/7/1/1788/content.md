
Let 

$\mathcal{C}$ and $\mathcal{D}$ be [[small categories]], and let 

$$
  \mathcal{C}
    \overset{\phantom{AA}F\phantom{AA}}{\longrightarrow}
  \mathcal{D}
$$

be a [[functor]] between them. By [[Kan extension]] this induces an [[adjoint triple]] between [[categories of simplicial presheaves]]:

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

where 

$$
  F^\ast \mathbf{X}
  \;\coloneqq\;
  \mathbf{X}(F(-))
$$

is the operation of precomposition with $F$. 

This implies that $F^\ast$ preserves all objectwise cofibrations/fibrations/weak equivalences. Hence it is 

1. a [[right Quillen functor]] $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$;

1. a [[left Quillen functor]] $[\mathcal{D}^{op}, sSet]_{inj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$;

and since $[\mathcal{D}^{op}, sSet]_{proj} \overset{id}{\to} [\mathcal{D}^{op}, sSet]_{inj}$ is also a left Quillen functor, the second point implies that $F^\ast$ is also 

* a [[left Quillen functor]] $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$.

This means that we have a [[2-morphism]] in the [[double category of model categories]] of the following form:

$$
  \array{
    [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
      &\overset{\phantom{AA}F^\ast\phantom{AA}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{F^\ast}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{id}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$

To check that the corresponding [[derived natural transformation]] $Ho(id)$ is a [[natural isomorphism]], we need to check (by [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos)) that the composites


$$
  Q_{inj} F^\ast \mathbf{X}
    \overset{ p_{F^\ast \mathbf{X}} }{\longrightarrow}
  F^\ast \mathbf{X}
    \overset{ j_{F^\ast \mathbf{X}} }{\longrightarrow}
  P_{proj} F^\ast \mathbf{X}  
$$ 

are invertible in the [[homotopy category of a model category|homotopy category]] $Ho([\mathcal{C}^{op}, sSet_{Qu}]_{inj})$, for all projectively fibrant-cofibrant simplicial presheaves $\mathbf{X}$. But this is immediate, since the two factors are weak equivalences, by definition of [[fibrant resolution|fibrant/cofibrant resolution]].

Hence we have a [[Quillen adjoint triple]] of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
       \underoverset{\bot}{\phantom{AA}F_!\phantom{AA}}{\longrightarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F^\ast\phantom{AA}}{\longleftarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F_\ast\phantom{AA}}{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
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
      \underoverset{ \phantom{{}_{Qu}}\bot_{Qu} }{ \Gamma }{\hookleftarrow}
      \\
      \overset{ coDisc }{\longrightarrow}
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

























