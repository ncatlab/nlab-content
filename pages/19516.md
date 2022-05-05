

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of [[adjoint triples]] generalized form [[adjoint functors]] to [[Quillen adjunctions]].

## Definition

+-- {: .num_defn #QuillenAdjointTriple}
###### Definition

Let $\mathcal{C}_1, \mathcal{C}_2, \mathcal{D}$ be [[model categories]], where $\mathcal{C}_1$ and $\mathcal{C}_2$ share the same underlying [[category]] $\mathcal{C}$, and such that the [[identity functor]] on $\mathcal{C}$ constitutes a [[Quillen equivalence]]

$$
  \mathcal{C}_2 
    \underoverset
      {\underset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}}
      {\overset{ \phantom{AA}id\phantom{AA} }{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{C}_1
$$

Then 

1. a [[Quillen adjoint triple]] of the form

   $$
     \mathcal{C}_{1/2}
       \array{
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
         \\
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
         \\
         \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
         \\
       }
     \mathcal{D}
   $$ 

   is a diagram in the [[double category of model categories]] of the form

   $$
     \array{
       && 
       \mathcal{C}_1
       &\overset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
       \mathcal{C}_2
       \\
       && 
       {}^{\mathllap{ L }}\Big\downarrow 
       &{}^{\mathllap{\eta}}\swArrow&
       \Big\downarrow{}^{\mathrlap{id}}
       \\
       \mathcal{C}_2    
        &\overset{ \phantom{A}R\phantom{A} }{\longrightarrow}&
       \mathcal{D}
        &\overset{\phantom{A}C\phantom{A}}{\longrightarrow}&
       \mathcal{C}_1
       \\
       {}^{\mathllap{ id }}\Big\downarrow
       & {}^{\mathllap{\epsilon}}\swArrow &
       {}^{\mathllap{C}}
       \Big\downarrow
         &\swArrow_{\mathrlap{id}}& 
       \Big\downarrow{}^{ \mathrlap{ id } }
       \\
       \mathcal{C}_2
       &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}&
       \mathcal{C}_2
       &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}& 
       \mathcal{C}_2
     }
   $$

   such that $\eta$ is the [[unit of an adjunction]] and $\epsilon$ the [[counit of an adjunction]], thus exhibiting [[Quillen adjunctions]] 

   $$
     \array{
       \mathcal{C}_1
         \underoverset
           {\underset{C}{\longleftarrow}}
           {\overset{L}{\longrightarrow}}
           {{}_{\phantom{Qu}}\bot_{Qu}}
       \mathcal{D}
       \\
       \\
       \mathcal{C}_2
         \underoverset
           {\underset{R}{\longrightarrow}}
           {\overset{C}{\longleftarrow}}
           {{}_{\phantom{Qu}}\bot_{Qu}}
       \mathcal{D}
     }
   $$

   and such that the [[derived natural transformation]] $Ho(id)$ of the bottom right square ([here](double+category+of+model+categories#DerivedNaturalTransformation)) is invertible (a [[natural isomorphism]]);
   

1. a [[Quillen adjoint triple]] of the form

   $$
     \mathcal{C}_{1/2}
       \array{
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longleftarrow}
         \\
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longrightarrow}
         \\
         \overset{\phantom{AA}R\phantom{AA}}{\longleftarrow}
         \\
       }
     \mathcal{D}
   $$ 

   is a diagram in the [[double category of model categories]] of the form

   $$
     \array{
       \mathcal{C}_2
       &\overset{ \phantom{AA} id \phantom{AA} }{\longrightarrow}& 
       \mathcal{C}_1   
       &\overset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
       \mathcal{C}_1
       \\
       {}^{\mathllap{id}}
       \Big\downarrow
         &{}^{ \mathllap{ id } }\swArrow& 
       \Big\downarrow{}^{ \mathrlap{ C } }
        & {}^{ \mathllap{\epsilon} }\swArrow &  
       \Big\downarrow{}^{\mathrlap{id}}
       \\
       \mathcal{C}_2
       &\underset{ \phantom{A}C\phantom{A} }{\longrightarrow}&
       \mathcal{D}
       &\underset{R}{\longrightarrow}&
       \mathcal{C}_1
       \\
       {}^{\mathllap{id}}\Big\downarrow 
         &{}^{\mathllap{ \epsilon }}\swArrow& 
       \Big\downarrow{}^{\mathrlap{L}}
       \\
       \mathcal{C}_2
       &\underset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
       \mathcal{C}_2
     }
   $$

   such that $\eta$ is the [[unit of an adjunction]] and $\epsilon$ the [[counit of an adjunction]], thus exhibiting [[Quillen adjunctions]] 

   $$
     \array{
       \mathcal{C}_2
         \underoverset
           {\underset{C}{\longrightarrow}}
           {\overset{L}{\longleftarrow}}
           {{}_{\phantom{Qu}}\bot_{Qu}}
       \mathcal{D}
       \\
       \\
       \mathcal{C}_1
         \underoverset
           {\underset{R}{\longleftarrow}}
           {\overset{C}{\longrightarrow}}
           {{}_{\phantom{Qu}}\bot_{Qu}}
       \mathcal{D}
     }
   $$

   and such that the [[derived natural transformation]] $Ho(id)$ of the top left square square ([here](double+category+of+model+categories#DerivedNaturalTransformation)) is invertible (a [[natural isomorphism]]).


If a Quillen adjoint triple of the first kind overlaps with one of the second kind

   $$
     \mathcal{C}_{1/2}
       \array{
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L_1 \phantom{= A_a}}{\longrightarrow}
         \\
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C_1 = L_2}{\longleftarrow}
         \\
         \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{R_1 = C_2}{\longrightarrow}
         \\
         \overset{\phantom{A_a = } R_2}{\longleftarrow}
         \\
       }
     \mathcal{D}
   $$ 

we speak of a _Quillen [[adjoint quadruple]]_, and so forth.

=--

## Properties

+-- {: .num_prop #QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}
###### Proposition
**([[Quillen adjoint triple]] induces [[adjoint triple]] of [[derived functors]] on [[homotopy category of a model category|homotopy categories]])**

Given a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}), the induced [[derived functors]] on the [[homotopy category of a model category|homotopy categories]] form an ordinary [[adjoint triple]]:

$$
  \mathcal{C}_{1/2}
     \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
      \\
    }
  \mathcal{D}
  \phantom{AAAA}
  \overset{Ho(-)}{\mapsto}
  \phantom{AAAA}
  Ho(\mathcal{C})
     \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}C \simeq \mathbb{R}C}{\longleftarrow}
      \\
      \overset{\phantom{AA}\mathbb{R}R\phantom{AA}}{\longrightarrow}
      \\
    }
  Ho(\mathcal{D})
$$ 

$\,$

$$
  \mathcal{C}_{1/2}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{C}{\longleftarrow}
      \\
      \overset{\phantom{AA}R\phantom{AA}}{\longrightarrow}
      \\
    }
  \mathcal{D}
  \phantom{AAAA}
  \overset{Ho(-)}{\mapsto}
  \phantom{AAAA}
  Ho(\mathcal{C})
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}L}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{\phantom{Qu}}}{\mathbb{L}C \simeq \mathbb{R}C}{\longleftarrow}
      \\
      \overset{\phantom{AA}\mathbb{R}R\phantom{AA}}{\longrightarrow}
      \\
    }
  Ho(\mathcal{D})
$$ 

=--

+-- {: .proof}
###### Proof

This follows immediately from the fact that passing to [[homotopy categories of model categories]] is a [[double pseudofunctor]] from the [[double category of model categories]] to the [[double category of squares]] in [[Cat]] ([this Prop.](double+category+of+model+categories#HomotopyDoublePseudofunctor)).

=--


## Examples 

### Homotopy (co-)limits

+-- {: .num_example #HomotopyLimitQuillenAdjointTriple}
###### Example
**([[Quillen adjoint triple]] of [[homotopy limits]]/[[homotopy colimits|colimits]] of [[simplicial sets]])**

Let $\mathcal{C}$ be a [[small category]], and write $[\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}$ for the projective/injective [[model structure on simplicial presheaves]] over $\mathcal{C}$, which participate in a [[Quillen equivalence]] of the form 

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}id\phantom{AA}}{\longleftarrow}}
      {\simeq_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
$$

(by [this Prop.](geometry+of+physics+--+categories+and+toposes#ModelCategoriesOfSimplicialPresheaves)).

Moreover, the [[constant functor|constant diagram]]-assigning functor

$$
  [\mathcal{C}^{op}, sSet] \overset{const}{\longleftarrow} sSet
$$

is clearly a [[left Quillen functor]] for the injective model structure, and a [[right Quillen functor]] for the projective model structure.

Together this means that in the [[double category of model categories]] we have a [[2-morphism]] of the form

$$
  \array{
    sSet_{Qu}
      &\overset{const}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{const}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{id}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$

Moreover, the [[derived natural transformation]] $Ho(id)$ of this square is invertible, if for every [[Kan complex]] $X$

$$
  Q const X
    \overset{}{\longrightarrow}
  const X
    \longrightarrow
  P const X  
$$ 

is a [[weak homotopy equivalence]] (by [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos)), which here is trivially the case.

Therefore we have a Quillen adjoint triple of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{\underset{\longrightarrow}{\lim}}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{const}{\longleftarrow}
      \\
      \overset{\underset{\longleftarrow}{\lim}}{\longrightarrow}
      \\
    }
  sSet_{Qu}
$$ 

witnessed by the following diagram in the [[double category of model categories]]

$$
  \array{
    && 
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    &\overset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}    
    \\
    && 
    {}^{\mathllap{ \underset{\longrightarrow}{\lim} }}\Big\downarrow 
    &{}^{\mathllap{\eta}}\swArrow&
    \Big\downarrow{}^{\mathrlap{id}}
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}    
     &\overset{ \phantom{A}\underset{\longleftarrow}{\lim}\phantom{A} }{\longrightarrow}&
    sSet_{Qu}
      &\overset{\phantom{A}const\phantom{A}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{ id }}\Big\downarrow
    & {}^{\mathllap{\epsilon}}\swArrow &
    {}^{\mathllap{const}}
    \big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \big\downarrow{}^{ \mathrlap{ id } }
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$

The induced [[adjoint triple]] of [[derived functors]] on the [[homotopy category of a model category|homotopy categories]] (via [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) is the [[homotopy colimit]]/[[homotopy limit]] adjoint triple

$$
  Ho([\mathcal{C}^{op}, sSet])
  \;
    \array{
       \overset{\phantom{AA}\mathbb{L}\underset{\longrightarrow}{\lim}\phantom{AA}}{\longrightarrow}
       \\
       \overset{\phantom{AA}const\phantom{AA}}{\longleftarrow}
       \\
       \overset{\phantom{AA}\mathbb{R}\underset{\longleftarrow}{\lim}\phantom{AA}}{\longrightarrow}
    }
  \;
  Ho(sSet)
$$ 

=--


+-- {: .num_example #QuillenAdjointQuadrupleOverSiteWithTerminalObject}
###### Example
**([[homotopy limit|limit]]/[[homotopy colimit|colimit]] [[Quillen adjoint quadruple]] over [[site]] with [[terminal object]])**

If $\mathcal{C}$ has a [[terminal object]] $\ast \in \mathcal{C}$, then 

$$
  \underset{\longleftarrow}{\lim}
  = \Gamma
  \;\colon\;
  [\mathcal{C}^{op}, sSet]
  \longrightarrow
  sSet
$$

is given by evaluation on that terminal object

$$
  \Gamma(\mathbf{X}) \coloneqq \mathbf{X}(\ast)  
$$

and this operation has a further [[right adjoint]]

$$
  coconst \;\colon\; sSet \longrightarrow [\mathcal{C}^{op}, sSet]
$$

given by [[right Kan extension]] along the terminal object inclusion.

Hence in this case $\underset{\longleftarrow}{\lim} =\Gamma$ is also a [[left Quillen functor]] on the projective model structure (using that $id : [\mathcal{C}^{op}, sSet_{Qu}]_{proj} \to [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$ is also left Quillen, as above) and hence we get a further Quillen adjoint triple

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj/proj}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{const}{\longleftarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{\underset{\longleftarrow}{\lim}=\Gamma}{\longrightarrow}
      \\
      \overset{coconst}{\longleftarrow}
      \\
    }
  sSet_{Qu}
$$ 
 
witnessed by the following diagram in the [[double category of model categories]]


$$
  \array{
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\overset{ \phantom{AA} id \phantom{AA} }{\longrightarrow}& 
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}   
    &\overset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{id}}
    \Big\downarrow
      &{}^{ \mathllap{ id } }\swArrow& 
    \Big\downarrow{}^{ \mathrlap{ \underset{\longleftarrow}{\lim}=\Gamma } }
      & {}^{ \mathllap{\epsilon} }\swArrow &
    \Big\downarrow{}^{\mathrlap{id}}
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{ \phantom{A}\underset{\longleftarrow}{\lim}=\Gamma\phantom{A} }{\longrightarrow}&
    sSet_{Qu}
    &\underset{coconst}{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \\
    {}^{\mathllap{id}}\Big\downarrow 
      &{}^{\mathllap{ \epsilon }}\swArrow& 
    \Big\downarrow{}^{\mathrlap{const}}
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    &\underset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}&
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  }
$$


Moreover, the [[derived natural transformation]] $Ho(id)$ of the top left square is invertible, if for every injectively fibrant simplicial presheaf $\mathbf{X}$ the composite

$$
  \Gamma Q_{inj} \mathbf{X}
    \overset{}{\longrightarrow}
  \Gamma \mathbf{X}
    \longrightarrow
  \Gamma P_{proj} \mathbf{X}  
$$ 

is a [[weak equivalence]] (by [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos)), which here is trivially the case.


Hence in this case we have a [[Quillen adjoint quadruple]]


$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{\phantom{AA}\underset{\longrightarrow}{\lim}\phantom{AA}}{\longrightarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{\phantom{AA}const\phantom{AA}}{\longleftarrow}
      \\
      \underoverset{{}_{\phantom{Qu}}\bot_{Qu}}{ \phantom{AA}\underset{\longleftarrow}{\lim}\phantom{AA} }{\longrightarrow}
      \\
      \overset{\phantom{A}coconst\phantom{A} }{\longleftarrow}
      \\
    }
  sSet_{Qu}
$$ 

witnessing the [[model topos]] over a [[site]] with [[terminal object]] as being [[cohesive (infinity,1)-topos|cohesive]].

=--

### Homotopy Kan extension

More generally:

+-- {: .num_example #QuillenAdjointTripleHomotopyKanExtension}
###### Example
**([[Quillen adjoint triple]] of [[homotopy Kan extension]] of [[simplicial presheaves]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[small categories]], and let 

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
      \underoverset{\bot}{ \phantom{AA}F^\ast\phantom{AA}  }{\longleftarrow}
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

is the operation of precomposition with $F$. This means that $F^\ast$ preserves all objectwise cofibrations/fibrations/weak equivalences. Hence it is 

1. a [[right Quillen functor]] $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$;

1. a [[left Quillen functor]] $[\mathcal{D}^{op}, sSet]_{inj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$;

and since $[\mathcal{D}^{op}, sSet]_{proj} \overset{id}{\to} [\mathcal{D}^{op}, sSet]_{inj}$ is also a left Quillen functor, the second point implies that $F^\ast$ is also 

* a [[left Quillen functor]] $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$.

In summary this means that we have a [[2-morphism]] in the [[double category of model categories]] of the following form:

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

Hence we have a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) of the form

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

The corresponding derived [[adjoint triple]] on [[homotopy category of a model category|homotopy categories]] (Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}) is that of _[[homotopy Kan extension]]_:


$$
  Ho([\mathcal{C}^{op}, sSet])
    \array{
      \underoverset{\bot \phantom{\simeq A_a}}{ \phantom{A}\mathbb{L}F_! \phantom{\simeq A_a}\phantom{A}  }{\longrightarrow}
      \\
      \underoverset{\phantom{\simeq A_a} \bot}{ \phantom{A}\mathbb{R}F^\ast \simeq \mathbb{L}F^\ast\phantom{A}  }{\longleftarrow}
      \\
      \overset{ \phantom{A} \phantom{A_a \simeq} \mathbb{R}F_\ast\phantom{A}  }{\longrightarrow}
    }
  Ho([\mathcal{D}^{op}, sSet])
$$

=--




[[!redirects Quillen adjoint triples]]

[[!redirects Quillen adjoint quadruple]]
[[!redirects Quillen adjoint quadruples]]

