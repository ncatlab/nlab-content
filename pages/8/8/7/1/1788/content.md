
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



