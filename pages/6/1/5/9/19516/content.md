

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

Just as a [[Quillen adjunction]] is a [[model category|model-categorical]] version of an [[adjunction]], a *Quillen adjoint triple* should be a model-categorical version of an [[adjoint triple]].

However, there are various levels of generality at which this could be defined.  The simplest would be an adjoint triple between model categories in which both adjunctions are Quillen adjunctions.  However, this would require the middle functor to be both Quillen left adjoint and Quillen right adjoint for the same model structures, which (though not impossible) is a strong restriction.  A more general notion is obtained by allowing the model structures on one or both of the categories to vary between the two Quillen adjunctions, but keeping the same [[Quillen equivalence]] type so that when we pass to [[homotopy categories]] or derived [[(infinity,1)-categories|$\infty$-categories]] we still get an adjoint triple (such as in [[2Ho(CombModCat)]]).

Currently, this page is primarily about a very restrictive case where only one of the model structures is allowed to vary, and the Quillen equivalence between the two model structures on that side must be an [[identity functor]].  However, more general versions could certainly also be defined.

## Definition

+-- {: .num_defn #QuillenAdjointTriple}
###### Definition
**(Quillen adjoint triple)**

Let $\mathcal{C}_1, \mathcal{C}_2, \mathcal{D}$ be [[model categories]], where $\mathcal{C}_1$ and $\mathcal{C}_2$ share the same underlying [[category]] $\mathcal{C}$, and such that the [[identity functor]] on $\mathcal{C}$ constitutes a [[Quillen equivalence]]

\[
  \label{EquivForQuillenAdjointTriple}
  \mathcal{C}_2 
    \underoverset
      {\underset{ \phantom{AA}id\phantom{AA} }{\longrightarrow}}
      {\overset{ \phantom{AA}id\phantom{AA} }{\longleftarrow}}
      {{}_{\phantom{Qu}}\simeq_{Qu}}
  \mathcal{C}_1
\]

Then a [[Quillen adjoint triple]] 

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{C}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$

is a [[pair]] of [[Quillen adjunctions]], as shown, together with a [[2-morphism]] in the [[double category of model categories]]

\[
  \label{Comparison2MorphismForQuillenAdjointTriple}
  \array{
    \mathcal{D}
     &\overset{\phantom{A}C\phantom{A}}{\longrightarrow}&
    \mathcal{C}_1
    \\
    {}^{\mathllap{C}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    \mathcal{C}_2
    &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}& 
    \mathcal{C}_2
  }
\]

whose [[derived natural transformation]] $Ho(id)$ ([here](double+category+of+model+categories#DerivedNaturalTransformation)) is invertible (a [[natural isomorphism]]).
   
If two Quillen adjoint triples overlap 

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L \phantom{= A}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {{\longrightarrow}}
      {\overset{C = L'}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{\phantom{A=} R'}{\longleftarrow}}
      {\overset{R = C'}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_2
$$

we speak of a _Quillen [[adjoint quadruple]]_, and so forth.

=--


## Examples 

### General

+-- {: .num_example #QuillenAdjointTripleFromLeftAndRightQuillenFunctor}
###### Example
**([[Quillen adjoint triple]] from left and right [[Quillen functor]])**

Given an [[adjoint triple]]

$$
  \mathcal{C}
    \array{
      \underoverset{\phantom{AA}\bot\phantom{AA}}{L}{\longrightarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{C}{\longleftarrow}
      \\
      \underoverset{\phantom{AA}\phantom{\bot}\phantom{AA}}{R}{\longrightarrow}
    }
  \mathcal{D}
$$

such that $C$ is both a [[left Quillen functor]] as well as a [[right Quillen functor]] for given [[model category]]-[[structures]] on the [[categories]] $\mathcal{C}$ and $\mathcal{D}$. Then this is a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) of the form

$$
  \mathcal{C}
    \underoverset
      {{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$
$$
  \mathcal{C}
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{C}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$

=--

+-- {: .proof}
###### Proof

The condition of a [[Quillen equivalence]] (eq:EquivForQuillenAdjointTriple) is trivially satisfied ([this Prop.](Quillen+equivalence#TrivialQuillenEquivalence)). Similarly the required [[2-morphism]] (eq:Comparison2MorphismForQuillenAdjointTriple)

$$
  \array{
    \mathcal{C}
     &\overset{\phantom{A}C\phantom{A}}{\longrightarrow}&
    \mathcal{D}
    \\
    {}^{\mathllap{C}}
    \Big\downarrow
      &\swArrow_{\mathrlap{id}}& 
    \Big\downarrow{}^{ \mathrlap{ id } }
    \\
    \mathcal{D}
    &\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}& 
    \mathcal{D}
  }
$$

exists trivially. To check that its [[derived natural transformation]] ([here](double+category+of+model+categories#DerivedNaturalTransformation)) is a [[natural isomorphism]] we need to check (by [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos)) that for every [[fibrant and cofibrant object]] $d \in \mathcal{D}$ the composite

$$
  Q C(d)
    \overset{ p_{C(d)} }{\longrightarrow}
  C(d)
    \overset{ j_{C(d)} }{\longrightarrow}
  P C(C)  
$$ 

is a [[weak equivalence]]. But this is trivially the case, by definition of [[fibrant resolution]]/[[cofibrant resolution]] (in fact, since $C$ is assumed to be both left and right Quillen, also $C(d)$ is a [[fibrant and cofibrant objects]] and hence we may even take both $p_{C(d)}$ as well as $j_{C(d)}$ to be the [[identity morphism]]).


=--

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
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
       {{\longleftarrow}}
       {\overset{ \underset{\longrightarrow}{\lim} }{\longrightarrow}}
       {\phantom{{}_{Qu}}\bot_{Qu} }
  sSet_{Qu}
$$ 
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
       {\underset{ \underset{\longleftarrow}{\lim} }{\longrightarrow}}
       {\overset{const}{\longleftarrow}}
       {\phantom{{}_{Qu}}\bot_{Qu} }
  sSet_{Qu}
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

and since 

$$
  [\mathcal{D}^{op}, sSet]_{inj}
    \underoverset
      {\underset{id}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{AA}\bot\phantom{AA}}
  [\mathcal{D}^{op}, sSet]_{proj} 
$$ 

is also a [[Quillen adjunction]], these imply that $F^\ast$ is also 

* a [[right Quillen functor]] $[\mathcal{D}^{op}, sSet]_{inj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{proj}$.


* a [[left Quillen functor]] $[\mathcal{D}^{op}, sSet]_{proj} \overset{F^\ast}{\to} [\mathcal{C}^{op}, sSet_{Qu}]_{inj}$.

In summary this means that we have [[2-morphisms]] in the [[double category of model categories]] of the following form:

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
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  \array{
    [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
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
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
  }
$$

To check that the corresponding [[derived natural transformations]] $Ho(id)$ are [[natural isomorphisms]], we need to check (by [this Prop.](double+category+of+model+categories#DerivedNaturalTransformationUpToIsos)) that the composites


$$
  Q_{inj} F^\ast \mathbf{X}
    \overset{ p_{F^\ast \mathbf{X}} }{\longrightarrow}
  F^\ast \mathbf{X}
    \overset{ j_{F^\ast \mathbf{X}} }{\longrightarrow}
  P_{proj} F^\ast \mathbf{X}  
$$ 

are invertible in the [[homotopy category of a model category|homotopy category]] $Ho([\mathcal{C}^{op}, sSet_{Qu}]_{inj/proj})$, for all fibrant-cofibrant simplicial presheaves $\mathbf{X}$ in $[\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}$. But this is immediate, since the two factors are weak equivalences, by definition of [[fibrant resolution|fibrant/cofibrant resolution]].

Hence we have a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) of the form

\[
  \label{QuillenAdjointTripleFromKanExtensionOfSimplicialPresheaves}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
       \underoverset{\bot}{\phantom{AA}F_!\phantom{AA}}{\longrightarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F^\ast\phantom{AA}}{\longleftarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F_\ast\phantom{AA}}{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}
    \array{
       \underoverset{\bot}{\phantom{AA}F_!\phantom{AA}}{\longrightarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F^\ast\phantom{AA}}{\longleftarrow}
       \\
       \underoverset{\bot}{\phantom{AA}F_\ast\phantom{AA}}{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
\]

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

+-- {: .num_example #QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair}
###### Example
**([[Quillen adjoint quadruple]] of [[homotopy Kan extension]] of [[simplicial presheaves]] along [[adjoint pair]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be [[small categories]], and let 

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

By Example \ref{QuillenAdjointTripleHomotopyKanExtension} the top three as well as the bottom three of these form [[Quillen adjoint triples]] (Def. \ref{QuillenAdjointTriple}) in two ways (eq:QuillenAdjointTripleFromKanExtensionOfSimplicialPresheaves). If for the top three we choose the first version, and for the bottom three the second version from (eq:QuillenAdjointTripleFromKanExtensionOfSimplicialPresheaves), then these combine to a Quillen [[adjoint quadruple]] of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longleftarrow}}
      {\overset{L_! \phantom{= A_a}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {{\longrightarrow}}
      {\overset{L^\ast = R_!}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{\phantom{A=} R_\ast}{\longleftarrow}}
      {\overset{L_\ast = R^\ast}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
$$


=--

+-- {: .num_example #QuillenAdjointQuintupleOfHomotopyKanExtensionAlongAdjointTriple}
###### Example
**([[Quillen adjoint quintuple]] of [[homotopy Kan extension]] of [[simplicial presheaves]] along [[adjoint triple]])**


Let $\mathcal{C}$ and $\mathcal{D}$ be [[small categories]] and let

$$
  \mathcal{C}
    \array{
      \underoverset{\phantom{AA}\bot\phantom{AA}}{L}{\longrightarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{C}{\longleftarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{C}{\longleftarrow}
    }
  \mathcal{D}
$$

be a [[adjoint triple|triple]] of [[adjoint functors]]. By [[Kan extension]] this induces an [[adjoint quintuple]] between [[categories of simplicial presheaves]]

\[
 \label{AdjointQuintupleFromKanExtensionInDiscussionOfQuillenAdjointQuintuple}
  [\mathcal{C}^{op}, sSet]
    \array{
      \underoverset{\bot \phantom{\simeq A_a \simeq A_a}}{ L_! \phantom{\simeq A_a \simeq A_a} }{\longrightarrow}
      \\
      \underoverset{\bot \phantom{\simeq} \bot \phantom{\simeq A_a} }{ L^\ast \simeq C_! \phantom{\simeq A_a} }{\longleftarrow}
      \\
      \underoverset{\phantom{A_a \simeq}\bot \phantom{\simeq} \bot}{ L_\ast \simeq C^\ast \simeq R_! }{\longrightarrow}
      \\
      \underoverset{\phantom{A_a \simeq A_a } \bot}{ \phantom{A_a \simeq } C_\ast \simeq R^\ast }{\longrightarrow}
      \\
      \underoverset{\phantom{A_a \simeq A_a } \phantom{\bot}}{ \phantom{A_a \simeq C_\ast \simeq}  R_\ast }{\longrightarrow}
    }
  [\mathcal{D}^{op}, sSet]
\]

By Example \ref{QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair} the top four functors in (eq:AdjointQuintupleFromKanExtensionInDiscussionOfQuillenAdjointQuintuple) form a [[Quillen adjoint quadruple]] ending in a [[right Quillen functor]]

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
   \overset{C_\ast \simeq R^\ast}{\longrightarrow}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
  \,.
$$

But $R^\ast$ here is also a [[left Quillen functor]] (as in Example \ref{QuillenAdjointTripleHomotopyKanExtension}), and hence this continues by one more Quillen adjoint triple via Example \ref{QuillenAdjointTripleFromLeftAndRightQuillenFunctor} to a [[Quillen adjoint quintuple]] of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longleftarrow}}
      {\overset{L_! \phantom{\simeq A_a \simeq A_a}}{\longrightarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {{\longrightarrow}}
      {\overset{L^\ast \simeq C_! \phantom{\simeq A_a}}{\longleftarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{}{\longleftarrow}}
      {\overset{L_\ast \simeq C^\ast \simeq R_!}{\longrightarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{ \phantom{ A_a \simeq A_a \simeq} R_\ast }{\longrightarrow}}
      {\overset{ \phantom{A_a \simeq} C_\ast \simeq R^\ast  }{\longleftarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
$$

Alternatively, we may regard the bottom four functors in (eq:AdjointQuintupleFromKanExtensionInDiscussionOfQuillenAdjointQuintuple) as a [[Quillen adjoint quadruple]] via example \ref{QuillenAdjointQuadrupleOfHomotopyKanExtensionAlongAdjointPair}, whose top functor is then the left Quillen functor

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \overset{ L^\ast }{\longleftarrow}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
  \,.
$$

But this is also a [[right Quillen functor]] (as in Example \ref{QuillenAdjointTripleHomotopyKanExtension}) and hence we may continue by one more [[Quillen adjoint triple]] upwards (via Example \ref{QuillenAdjointTripleFromLeftAndRightQuillenFunctor}) to obtain a [[Quillen adjoint quintuple]], now of the form

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longleftarrow}}
      {\overset{L_! \phantom{\simeq A_a \simeq A_a}}{\longrightarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {{\longrightarrow}}
      {\overset{L^\ast \simeq C_! \phantom{\simeq A_a}}{\longleftarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{}{\longleftarrow}}
      {\overset{L_\ast \simeq C^\ast \simeq R_!}{\longrightarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{proj}
$$
$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{ \phantom{ A_a \simeq A_a \simeq} R_\ast }{\longrightarrow}}
      {\overset{ \phantom{A_a \simeq} C_\ast \simeq R^\ast  }{\longleftarrow}}
      {\phantom{\phantom{A}{}_{Qu}}\bot_{Qu}\phantom{A}}
  [\mathcal{D}^{op}, sSet_{Qu}]_{inj}
$$


=--

## Properties

### Derived adjoint triple
 {#DerivedAdjointTriple}

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

=--

+-- {: .proof}
###### Proof

This follows immediately from the fact that passing to [[homotopy categories of model categories]] is a [[double pseudofunctor]] from the [[double category of model categories]] to the [[double category of squares]] in [[Cat]] ([this Prop.](double+category+of+model+categories#HomotopyDoublePseudofunctor)).

=--

A similar argument should show that we get an adjoint triple between the [[(infinity,1)-categories]] presented by the model categories.  We can therefore apply all $(\infty,1)$-category theoretic arguments.  But in what follows, we prove some basic facts about $(\infty,1)$-adjoint triples instead using model-categorical arguments.


### Derived adjoint modality
 {#DerivedAdjointModality}




+-- {: .num_lemma #DerivedAdjunctionUnitOfQuillenAdjointTriple}
###### Lemma
**([[derived adjunction units]] of [[Quillen adjoint triple]])**

Consider a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple})

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{C}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$


such that the two model structures $\mathcal{C}_1$ and $\mathcal{C}_2$ on the category $\mathcal{C}$ share the same class of [[weak equivalences]].

Then:

1. the [[derived adjunction unit]] of $(L \dashv C)$ in $\mathcal{C}_1$ differs only by a [[weak equivalence]] from the plain [[adjunction unit]].

1. the [[derived adjunction counit]] of $(C \dashv R)$ differs only by a [[weak equivalence]] form the plain [[adjunction counit]].


=--


+-- {: .proof}
###### Proof

The [[derived adjunction unit]] is on cofibrant objects $c \in \mathcal{C}_1$ given by

$$
  c 
    \overset{\eta_c}{\longrightarrow}
  C L (c)
    \overset{ C(j_{L(c)}) }{\longrightarrow}
  C P L (c)
$$

Here the [[fibrant resolution]]-morphism $j_{P(c)}$ is an [[acyclic cofibration]] in $\mathcal{D}$. Since $C$ is also a [[left Quillen functor]] $\mathcal{D} \overset{C}{\to} \mathcal{C}_2$, the comparison morphism $C(j_{L(c)})$ is an [[acyclic cofibration]] in $\mathcal{C}_2$, hence in particular a weak equivalence in $\mathcal{C}_2$ and therefore, by assumption, also in $\mathcal{C}_1$.

The [[derived adjunction counit]] of the second adjunction is

$$
  C Q R (c)
    \overset{ C(p_{R(c)}) }{\longrightarrow}
  C R (c) 
    \overset{ \epsilon_c }{\longrightarrow}
  c
$$

Here the [[cofibrant resolution]]-morphisms $p_{R(c)}$ is an [[acyclic fibration]] in $\mathcal{D}$. Since $C$ is also a [[right Quillen functor]] $\mathcal{D} \overset{C}{\to} \mathcal{C}_1$, the comparison morphism $C(p_{R(c)})$ is an acyclic fibration in $\mathcal{C}_1$, hence in particular a weak equivalence there, hence, by assumption, also a weak equivalence in $\mathcal{C}_2$.


=--


+-- {: .num_lemma #DerivedModalityFromQuillenAdjointTriple}
###### Lemma
**([[fully faithful functors]] in [[Quillen adjoint triple]])**

Consider a [[Quillen adjoint triple]] (Def. \ref{QuillenAdjointTriple}) 

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L}{\longrightarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{R}{\longrightarrow}}
      {\overset{C}{\longleftarrow}}
      {{}_{\phantom{Qu}}\bot_{Qu}}
  \mathcal{D}
$$

If $L$ and $R$ are [[fully faithful functors]] (necessarily jointly, by [this Prop.](adjoint+triple#FullyFaithful)), then so are their [[derived functors]] $\mathbb{L}L$ and $\mathbb{R}R$.

=--

+-- {: .proof}
###### Proof

We discuss that $R$ being fully faithful implies that $\mathbb{R}R$ is fully faithful. Since also the [[derived functors]] form an [[adjoint triple]] (by Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors}), this will imply the claim also for $L$ and $\mathbb{L}L$.

By Lemma \ref{DerivedAdjunctionUnitOfQuillenAdjointTriple} the [[derived adjunction counit]] of $C \dashv R$ is, up to weak equivalence, the ordinary [[adjunction counit]]. But the latter is an [[isomorphism]], since $R$ is fully faithful (by [this Prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints)). In summary this means that the [[derived adjunction unit]] of $(C \dashv R)$ is a weak equivalence, hence that its image in the homotopy category is an isomorphism. But the latter is the ordinary [[adjunction unit]] of $\mathbb{L}C \dashv \mathbb{R}R$ (by [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)), and hence the claim follows again by [that Prop.](adjoint+functor#FullyFaithfulAndInvertibleAdjoints).

=--


+-- {: .num_lemma #DerivedAdjointModalityFromQuillenAdjointQuadruple}
###### Lemma
**([[fully faithful functors]] in [[Quillen adjoint quadruple]])**

Given a [[Quillen adjoint quadruple]] (Def. \ref{QuillenAdjointTriple})

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L \phantom{= A}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {{\longrightarrow}}
      {\overset{C = L'}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{\phantom{A=} R'}{\longleftarrow}}
      {\overset{R = C'}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_2
$$

if any of the four functors is [[fully faithful functor]], then so is its [[derived functor]].


=--

+-- {: .proof}
###### Proof

Observing that each of the four functors is either the leftmost or the rightmost adjoint in the top or the bottom [[adjoint triple]] within the [[adjoint quadruple]], the claim follows by Lemma \ref{DerivedAdjointModalityFromQuillenAdjointQuadruple}.

=--

In summary

+-- {: .num_prop #DerivedAdjointModalitiesFromFullyFaithfulQuillenAdjointQuadruples}
###### Proposition
**([[derived functor|derived]] [[adjoint modalities]] from [[fully faithful functor|fully faithful]] [[Quillen adjoint quadruples]])**

Given a [[Quillen adjoint quadruple]] (Def. \ref{QuillenAdjointTriple})

$$
  \mathcal{C}_1
    \underoverset
      {{\longleftarrow}}
      {\overset{L \phantom{= A}}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {{\longrightarrow}}
      {\overset{C = L'}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_1
$$
$$
  \mathcal{C}_2
    \underoverset
      {\underset{\phantom{A=} R'}{\longleftarrow}}
      {\overset{R = C'}{\longrightarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  \mathcal{D}_2
$$

then the corresponding [[derived functors]] form an [[adjoint quadruple]]

$$
  Ho(\mathcal{C})
    \array{
      \underoverset{\phantom{AA}\bot\phantom{AA}}{ 
        \mathbb{L}L
      }{\longrightarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{ 
        \mathbb{L}C \simeq \mathbb{R}C \simeq \mathbb{L}L'
      }{\longleftarrow}
      \\
      \underoverset{\phantom{AA}\bot\phantom{AA}}{ 
        \mathbb{R}R \simeq \mathbb{L}C' \simeq \mathbb{R}C'
      }{\longrightarrow}
      \\
      \underoverset{\phantom{AA}\phantom{\bot}\phantom{AA}}{ 
        \mathbb{R}R'
      }{\longleftarrow}
    }
  Ho(\mathcal{D})
$$

Moreover, if one of the functors in the [[Quillen adjoint quadruple]] is a [[fully faithful functor]], then so is the corresponding [[derived functor]]. 

Hence if the original [[adjoint quadruple]] induces an [[adjoint modality]] on $\mathcal{C}$

$$
  \bigcirc \dashv \Box \dashv \lozenge
$$

or on $\mathcal{D}$

$$
  \Box \dashv \bigcirc \dashv \triangle
$$

then so do the corresponding [[derived functors]] on the [[homotopy category of a model category|homotopy categories]], respectively.

=--

+-- {: .proof}
###### Proof

The existence of the derived [[adjoint quadruple]] followy by Prop. \ref{QuillenAdjointTripleInducesAdjointTripleOfDerivedFunctors} and by uniqueness of adjoints ([this Prop.](adjoint+functor#UniquenessOfAdjoints)).

The statement about fully faithful functors is Lemma \ref{DerivedAdjointModalityFromQuillenAdjointQuadruple}. The reformulation in terms of [[adjoint modalities]] is by [this Prop.](geometry+of+physics+--+categories+and+toposes#ModalOperatorsEquivalentToReflectiveSubcategories)

=--

## Related concepts

* [[adjoint triple]]

* [[adjoint quadruple]]

[[!redirects Quillen adjoint triples]]

[[!redirects Quillen adjoint quadruple]]
[[!redirects Quillen adjoint quadruples]]

[[!redirects Quillen adjoint quintuple]]
[[!redirects Quillen adjoint quintuples]]

