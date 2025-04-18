
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###coContext###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The concept of _external tensor product_ is a variant of that of [[tensor product]] in a [[monoidal category]] when the latter is generalized to [[indexed monoidal categories]] ([[dependent linear type theory]]).

## Definition

Consider an [[indexed monoidal category]] given by a [[Cartesian fibration]]

$$
  \array{
    Mod(-)
    \\
    \downarrow
    \\
    \mathbf{H}
  }
$$

over a [[cartesian monoidal category]] $\mathbf{H}$.


\begin{definition}\label{ExternalTensorProduct}
**(external tensor product)**
\linebreak
Given $X_1, X_2 \in \mathbf{H}$ the _external tensor product_ over these is the [[functor]]

$$
  \boxtimes \;\colon\;
  Mod(X_1)\times Mod(X_2)
  \longrightarrow
  Mod(X_1 \times X_2)
$$

given  on $A_1 \in Mod(X_1)$ with $A_2 \in Mod(X_2)$ by

$$
  A_1 \boxtimes A_2 \coloneqq (p_1^\ast A_1) \otimes_{X_1 \times X_2} (p_2^\ast A_2)
  \in Mod(X_1 \times X_2)
  \,,
$$

where $p_1, p_2$ denote the [[projection]] maps out of the [[Cartesian product]] $X_1 \times X_2 \in \mathbf{H}$.
\end{definition}

+-- {: .num_remark}
###### Remark

The external tensor product constitutes a [[tensor product]] on the total category $Mod$ of the given [[Grothendieck fibration]] $Mod(-)\to \mathbf{H}$; and with respect to this it is a [[monoidal fibration]].

=--

## Properties

### Relation to fiberwise tensor product

+-- {: .num_prop}
###### Proposition

The fiberwise ("internal") tensor product over $X\in \mathbf{H}$ is recovered form the external one via a [[natural equivalence]]

$$
  A_1 \otimes_X A_2 \simeq \Delta_X^\ast (A_1 \boxtimes A_2)
$$

for $A_1, A_2 \in Mod(X)$, where $\Delta \colon X \longrightarrow X \times X$ is the [[diagonal]] in $\mathbf{H}$ on $X$.


=--

### Generation of $Mod(X_1 \times X_2)$ from external tensor products

Under suitable conditions on compact generation of $Mod(-)$ then one may deduce that $Mod(X_1 \times X_2)$ is generated under external product from 
$Mod(X_1)$ and $Mod(X_2)$.

([Bondal-vdBerg 03](#BondalvdBerg03), [BFN 08, proof of prop. 3.24](#BFN08))

### In indexed monoidal categories
 {#CocontinuityAndAdjoints}

Suppose an [[indexed monoidal category]] which satisfies the [[motivic yoga]] ([[Wirthmüller context]]-form) in that:

1. the corresponding [[pseudofunctor]] takes values in [[adjoint functors]]

   $$
     \array{
       \mathllap{
         \mathbf{C} \,\colon\,
         \;
       }
       Base &\longrightarrow& Cat
       \\
       \mathcal{X} &\mapsto& \mathbf{C}_{\mathcal{X}}
       \\
       \Big\downarrow\mathrlap{{}^{f}}
       &&
       \mathllap{^{f_!}}\Big\downarrow
       \dashv
       \Big\uparrow\mathrlap{{}^{f^\ast}}
       \\
       \mathcal{Y} 
       &\mapsto& 
       \mathbf{C}_{\mathcal{Y}}
     }
   $$

1. between [[closed monoidal categories]]

1. the [[base change]] functors $f^\ast$ are 

   1. besides being [[strong monoidal functors]]

   1. also [[strong closed functors]], 

      hence the pushforward functors $f_!$ satisfy the [[projection formula]] ("[[Frobenius reciprocity]]")

   1. [[preserving colimits]]

1. pull-push through [[cartesian squares]] in $Base$ satisfies the [[Beck-Chevalley condition]].

Also assume that 

* $Base$ is [[cocomplete]] and [[cartesian closed category|cartesian closed]],

* $\mathbf{C}_{\mathcal{X}}$ is cocomplete for each $\mathcal{X} \in Base$.

Then:

\begin{proposition}  
  The external tensor product (Def. \ref{ExternalTensorProduct}) on the [[Grothendieck construction]] $\int \mathbf{C}$ [[preserves colimits]] in each variable.
\end{proposition}
\begin{proof}

Consider any [[object]]
$$
  \mathcal{W}_{\mathcal{Y}} 
    \,\in\, 
  \textstyle{\int} \mathbf{C}
$$
and any [[diagram]]
$$
  \begin{array}{ccc}
    \mathcal{V}_{\mathcal{X}}
    \,\colon\,
    I &\longrightarrow& \int \mathbf{C}
    \\
    i &\mapsto& \mathcal{V}(i)_{\mathcal{X}_i}
  \end{array}
$$
in the Grothendieck construction category $\int \mathbf{C}$.

Then with

* the description of colimits in Grothendieck constructions as (see [there](Grothendieck+construction#CoLimitsInAGrothendieckConstruction)) 

  $$
    \underset{\underset{i \in I}{\longrightarrow}}{lim}
    \big(
      \mathcal{V}(i)_{\mathcal{X}_i}
    \big)
    \;\simeq\;
    \left(
      \underset{\underset{i \in I}{\longrightarrow}}{lim}
      q^{\mathcal{X}_i}_! 
      \mathcal{V}(i)
    \right)_{
      \underset{\underset{i \in I}{\longrightarrow}}{lim}
      \mathcal{X}_i
    }
  $$

  where 

  $$
    q^{\mathcal{X}_i}
    \;\colon\;
    \mathcal{X}_i 
      \longrightarrow
    \underset{\longrightarrow}{lim} \mathcal{X}
  $$

  denote the [[coprojections]] of the [[colimit]] of the [[underlying]] [[diagram]] in $Base$,

* the [[Beck-Chevalley condition]] for the following [[cartesian squares]] in $Base$

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
      \underset{\underset{j \in I}{\longrightarrow}}{lim} 
      \mathcal{X}_j
      \mathrlap{\,,}
    }
  $$

* the fact that both $(-) \times \mathcal{Y}$ and $(-)\otimes (pr_{\mathcal{Y}})^\ast\mathscr{W}$ [[preserve colimits]] ([[left adjoints preserve colimits|being left adjoints]])

we obtain the following sequence of [[natural isomorphisms]]:

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
  \text{tensoring preserves colimits}
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
    \mathcal{X}_i
    \times
    \mathcal{Y}
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
  \text{def of external tensor.}
  \end{array}
$$
\end{proof}

The following proposition still assumes the "motivic yoga" [above](#CocontinuityAndAdjoints), but in fact we need to assume the [[Beck-Chevalley condition]] only for the very special squares of this form:
$$
  \array{
    \mathcal{X} \times \mathcal{Y}
    &\overset{ f \times id }{\longrightarrow}&
    \mathcal{X}' \times \mathcal{Y}
    \\
    \mathllap{{}^{ pr_{\mathcal{X}} }}
    \Big\downarrow 
      && 
    \Big\downarrow
    \\
    \mathcal{X} 
      &\underset{\;\;\; f \;\;\;}{\longrightarrow}&
    \mathcal{X}'
  }
$$ 

\begin{proposition}
\label{PullAndPushAlongProductsOfMaps}
Given 
$$
\array{
  f \,\colon\, \mathcal{X} &\longrightarrow& \mathcal{X}'
\\
g \,\colon\, \mathcal{Y} &\longrightarrow& \mathcal{Y}'
}
$$

we have

1. for $\mathscr{V} \,\in\, \mathbf{C}_{\mathcal{X}'}$ and $\mathscr{W} \,\in\, \mathbf{C}_{\mathcal{Y}'}$ [[natural isomorphism]] of this form:
   \[
     \label{PullbackOfExternalTensorAlongProductOfMaps}
     (f \times g)^\ast (\mathscr{V} \boxtimes \mathscr{W})
     \;\simeq\;
     \big(f^\ast \mathscr{V}\big)
     \boxtimes
     \big(g^\ast \mathscr{W}\big)
   \]

1. for $\mathscr{V} \,\in\, \mathbf{C}_{\mathcal{X}}$ and $\mathscr{W} \,\in\, \mathbf{C}_{\mathcal{Y}}$ [[natural isomorphism]] of this form:

   \[
     \label{PushforwardOfExternalTensorAlongProductOfMaps}
     (f \times g)_! (\mathscr{V} \boxtimes \mathscr{W})
     \;\simeq\;
     \big(f_! \mathscr{V}\big)
     \boxtimes
     \big(g_! \mathscr{W}\big)
     \mathrlap{\,.}
   \]

\end{proposition}
(The first statement is essentially immediate from the fact that pullback $(-)^*$ is assumed to be strong closed, but the second statement is not quite so immediate; it is discussed for the case of [[smash product]] of [[retractive spaces]] and [[parameterized spectra]] in [May & Sigurdsson (2006), Rem. 2.5.8, Prop. 13.7.2](#MaySigurdsson06), see also [Malkiewich (2019), Lem. 3.4.1](#Malkiewich19), [Malkiewich (2023), Lem. 2.5.1](#Malkiewich23), and is  mentioned in generality but without proof in [Shulman (2012), p. 624](#Shulman12).)
\begin{proof}
For the first statement (eq:PullbackOfExternalTensorAlongProductOfMaps) we have the following sequence of [[natural isomorphisms]]:
$$
  \begin{array}{ll}
      (f \times g)^\ast
      \big(
        \mathscr{V} 
        \,\boxtimes\,
        \mathscr{W}
      \big)
      \\
      \;\simeq\;
      (f \times g)^\ast
      \Big(
        \big(
          \mathrm{pr}_{\mathbf{Y}}^\ast 
          \mathscr{V}
        \big)
        \,\otimes_{\mathbf{Y} \times \mathbf{Y}'}\,
        \big(
          \mathrm{pr}_{\mathbf{Y}'}^\ast 
          \mathscr{W}
        \big)        
      \Big)
      &
      \text{by definition}
      \\
      \;\simeq\;
      \big(
        (f \times g)^\ast
        \mathrm{pr}_{\mathbf{Y}}^\ast
        \mathscr{V}
      \big)
      \otimes_{\mathbf{X} \times \mathbf{X}'}
      \big(
        (f \times g)^\ast
        \mathrm{pr}_{\mathbf{Y}'}^\ast
        \mathscr{W}
      \big)
      &
      \text{since pullback is strong closed}
      \\
      \;\simeq\;
      \big(
        \mathrm{pr}_{\mathbf{X}}^\ast
        f^\ast
        \mathscr{V}
      \big)
      \otimes_{\mathbf{X} \times \mathbf{X}'}
      \big(
        \mathrm{pr}_{\mathbf{X}'}^\ast
        g^\ast
        \mathscr{W}
      \big)
      &
      \text{by pseudo-functoriality}
      \\
      \;\simeq\;
      \big(f^\ast \mathscr{V}\big)
      \boxtimes
      \big(g^\ast \mathscr{W}\big)
      &
      \text{by definition.}
    \end{array}
$$

For the second statement (eq:PushforwardOfExternalTensorAlongProductOfMaps), first notice the special case where one of the maps is an [[identity morphism]] and the corresponding external tensor factor is the [[tensor unit]]; and notice here that external tensoring with the tensor unit is just pullback to a product (since pullback along the other leg preserves tensor units, being strong monoidal):
$$
  \mathscr{V} \boxtimes \mathbb{1}
  \;\simeq\;
  (pr_{\mathcal{X}})^\ast \mathscr{V}
  \,.
$$
This way we first find
$$
  \begin{array}{ll}
    (f \times id)_!
    \big(
      \mathscr{V} \boxtimes \mathbb{1}
    \big)
    \\
    \;\simeq\;
    (f \times id)_!
    \big(
      pr_{\mathcal{X}}^\ast \mathscr{V}
    \big)    
    &
    \text{ by the above comment }
    \\
    \;\simeq\;
    pr_{\mathcal{X}'}^\ast\big(f_! \mathscr{V}\big)
    &
    \text{ using the BC-condition }
    \\
    \;\simeq\;
    (f_! \mathscr{V}) \boxtimes \mathbb{1}
    &
    \text{ by the above comment }
    \,,
  \end{array}
$$
from which the general case is obtained as follows:
$$
  \begin{array}{ll}
    (f \times g)_!
    \big(
      \mathscr{V}
      \boxtimes
      \mathscr{W}
    \big)
    \\
    \;\simeq\;
    (f \times g)_!
    \big(
      (\mathscr{V} \boxtimes \mathbb{1})
      \otimes
      (\mathbb{1} \boxtimes \mathscr{W})
    \big)
    &
    \text{by the above comment}
    \\
    \;\simeq\;
    (f \times g)_!
    \Big(
      \big(
      (id \times g)^\ast
      (\mathscr{V} \boxtimes \mathbb{1})
      \big)
      \otimes
      (\mathbb{1} \boxtimes \mathscr{W})
    \Big)
    &
    \text{by first claim and strong monoidalness}
    \\
    \;\simeq\;
    (f \times id)_!
    (id \times g)_! 
    \Big(
      \big(
      (id \times g)^\ast
      (\mathscr{V} \boxtimes \mathbb{1})
      \big)
      \otimes
      \big(\mathbb{1} \boxtimes \mathscr{W}\big)
    \Big)
    &
    \text{by pseudo-functoriality}
    \\
    \;\simeq\;
    (f \times id)_!
    \Big(
      \big(\mathscr{V} \boxtimes \mathbb{1}\big)
      \otimes
      \big(
        (id \times g)_! 
        \big(\mathbb{1} \boxtimes \mathscr{W}\big)
      \big)
    \Big)
    &
    \text{by the projection formula}
    \\
    \;\simeq\;
    (f \times id)_!
    \Big(
      \big(\mathscr{V} \boxtimes \mathbb{1}\big)
      \otimes
      \big(
        \mathbb{1} \boxtimes (g_!\mathscr{W})
      \big)
    \Big)
    &
    \text{by the special case above}
    \\
    \;\simeq\;
    (f \times id)_!
    \Big(
      \big(\mathscr{V} \boxtimes \mathbb{1}\big)
      \otimes
      (f \times id)^\ast
      \big(
        \mathbb{1} \boxtimes (g_!\mathscr{W})
      \big)
    \Big)
    &
    \text{by first claim and strong monoidalness}
    \\
    \;\simeq\;
    \Big(
      (f \times id)_!
      \big(\mathscr{V} \boxtimes \mathbb{1}\big)
    \Big)
      \otimes
      \big(
        \mathbb{1} \boxtimes (g_!\mathscr{W})
      \big)
    &
    \text{by the projection formula}
    \\
    \;\simeq\;
    \big(
      (f_!\mathscr{V}) \boxtimes \mathbb{1}
    \big)
    \otimes
    \big(
      \mathbb{1} \boxtimes (g_!\mathscr{W})
    \big)
    &
    \text{by the special case above}
    \\
    \;\simeq\;
    (f_! \mathscr{V})
    \boxtimes
    (g_! \mathscr{W})
    &
    \text{by the above comment}.
  \end{array}
$$
\end{proof}

\begin{corollary}
\label{PullPushAdjunctsOfExternalTensorProducts}
  The $\big((f \times g)_! \dashv (f \times g)^\ast\big)$-[[adjunct]] $\widetilde{f \boxtimes g}$ of an external tensor product of morphisms into the separate pullbacks
$$
  \mathscr{V} 
    \boxtimes
  \mathscr{W}
  \overset{ \phi \boxtimes \gamma  }{\longrightarrow}
  (f^\ast \mathscr{V}') \boxtimes (g^\ast \mathscr{W}')
  \;\simeq\;
  (f \times g)^\ast
  (\mathscr{V}' \boxtimes \mathscr{W}')
$$
is the external tensor product of the separate [[adjuncts]] 
$$
  \widetilde{ f \boxtimes g }
  \,\colon\,
  (f \times g)_!( \mathscr{V} \boxtimes \mathscr{W} ) 
  \,\simeq\,
  (f_! \mathscr{V}) \boxtimes (g_! \mathscr{W})
  \overset{
    \widetilde \phi \,\boxtimes\, \widetilde \gamma 
  }{\longrightarrow}
  \mathscr{V}' \boxtimes \mathscr{W}'
  \,,
$$
where the natural isomorphisms shown are those form Prop. \ref{PullAndPushAlongProductsOfMaps}.
\end{corollary}
\begin{proof}
After restriction along the (non-full) [[subcategory]]-inclusion
$$
  \array{
    \mathbf{C}_{\mathcal{X}} 
    \times
    \mathbf{C}_{\mathcal{Y}}
    &\longrightarrow&
    \mathbf{C}_{\mathcal{X} \times \mathcal{Y}}
    \\
    \big(\mathscr{V},\, \mathscr{W}\big)
    &\mapsto&
    \mathscr{V} \boxtimes \mathscr{W}
    \\
    \mathllap{{}^{ (\phi, \gamma) }}
    \Big\downarrow
    &&
    \Big\downarrow
    \mathrlap{{}^{ \phi \boxtimes \gamma }}
    \\
    \big(\mathscr{V}',\, \mathscr{W}'\big)
    &\mapsto&
    \mathscr{V}' \boxtimes \mathscr{W}'
  }
$$
we can clearly make the restriction of the functors $(f \times g)_!$ and $(f \times g)^\ast$ into adjoints by declaring the [[counit of an adjunction|adjunction counit]] $\epsilon$ to be the external tensor product of the $(f_! \dashv f^\ast)$- with the $(f_! \dashv g^\ast)$-[[adjunction counits]]. But by uniqueness of adjoints ([here](adjoint+functor#UniquenessOfAdjoints)) this must be isomorphic to the actual adjunction counit restricted to external tensor products:
$$
  \epsilon^{ 
    \big((f \times g)_! \dashv (f \times g)^\ast\big)
  }_{\mathcal{X} \boxtimes \mathcal{Y}}
  \;\;
  \simeq
  \;\;
  \epsilon^{ (f_! \dashv f^\ast) }_{\mathcal{X}}
  \,\boxtimes\,
  \epsilon^{ (g_! \dashv g^\ast) }_{\mathcal{Y}}
  \,.
$$
Now using the expression on the right together with Prop. \ref{PullAndPushAlongProductsOfMaps}
in the formula ([here](adjoint+functor#GeneralAdjunctsInTermsOfAdjunctionUnitCounit)) that expresses [[adjuncts]] as functor-images composed with the (co)unit gives that the adjunct is formed external tensor-factor wise, as claimed:
$$
  \begin{array}{ll}
    \widetilde{ \phi \boxtimes \gamma }
    \\
    \;\simeq\;
    \epsilon^{
      (f \times g)_! \dashv (f \times g)^\ast
    }_{ \mathscr{V}' \boxtimes \mathscr{W}' }
    \circ
    (f \times g)_!\big(\phi \boxtimes \gamma\big)
    &
    \text{ by the formula for adjuncts }
    \\
    \;\simeq\;
    \big(
      \epsilon^{ f_! \dashv f^\ast }_{\mathscr{V}'} 
        \circ 
      (f_! \phi)
    \big)
    \,\boxtimes\,
    \big(
      \epsilon^{ g_! \dashv g^\ast }_{\mathscr{W}'} 
        \circ 
      (g_! \gamma)
    \big)
    &
    \text{ by the previous discussion }
    \\
    \;\simeq\;
    \widetilde \phi
    \,\boxtimes\,
    \widetilde \gamma
    &
    \text{ by the formula for adjuncts. }
  \end{array}
$$
\end{proof}
\begin{proposition}
\label{ExternalPushoutProduct}
**(external [[pushout-product]])**
\linebreak
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
where here we use the left-handed convention for component maps in morphisms in the Grothendieck construction:
$$
  \phi_f \,\colon\, \mathscr{V}_X \to \mathscr{V}'_{X'}
  \;\;\;\;\;\;
  \text{stands for}
  \;\;\;\;\;\;
  \begin{array}{rcl}  
    X &\xrightarrow{f}& X'
    \\
    f_!\mathscr{V} &\xrightarrow{\phi}& \mathscr{V}'
  \end{array}
$$
\begin{proof}
By the general formula for colimits in Grothendieck constructions ([here](Grothendieck+construction#CoLimitsInAGrothendieckConstruction)) the underlying colimit in the base category is the evident one
\begin{tikzcd}
  X \times Y 
  \ar[r, "{ \mathrm{id}\,\times\, g }"{description}]
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
Here in the second-but-last step we used (eq:PushforwardOfExternalTensorAlongProductOfMaps).
\end{proof}


\linebreak


## Examples
 {#Examples}

\begin{example}
**([[external tensor product of vector bundles]])**
\linebreak

Given a [[pair]] of [[topological spaces]] $X,\,Y \,\in\, Top$ and a respective [[pair]] of [[topological vector bundles]] $\mathscr{V}_X \,\in\, $ [[Vect(X)|$Vect(X)$]] and $\mathscr{V}_X \,\in\, $ [[Vect(X)|$Vect(X)$]], their [[external tensor product of vector bundles|external tensor product]] is formed via [[pullback of bundles]] $(-)^\ast$ and ordinary [[tensor product of vector bundles]] $(-) \otimes (-)$ by the formula
$$
  \mathscr{V}_X 
    \,\boxtimes\, 
  \mathscr{W}_Y
  \;\;
  \equiv
  \;\; 
  \Big(
  \big(
    (pr_X)^\ast \mathscr{V}     
  \big)
  \otimes
  \big(
    (pr_Y)^\ast \mathscr{W}     
  \big)
  \Big)_{X \times Y}
  \;\;\;
  \in
  \;
  Vect(X \times Y)
  \,,
$$  
where we are denoting by
$$
  \array{
    && X \times Y
    \\
    & 
    \mathllap{{}^{pr_X}}\swarrow 
    && 
    \searrow\mathrlap{{}^{pr_Y}}
    \\
    X && && Y
  }
$$
the product [[projection]] maps in [[Top]].

This is a [[vector bundle]] over the [[product topological space]] $X \times Y$ whose [[fiber]] over a point $(x,y) \,\in\, X \times Y$ is the [[tensor product of vector spaces]] $\mathscr{V}_x \otimes \mathscr{W}_y$.
\end{example}

\begin{example}\label{CartesianProductInGrothendieckConstruction}
**([[Cartesian product]] in a [[Grothendieck construction]] is external cartesian product)**
\linebreak
  Given a [[contravariant functor|contravariant]] [[pseudofunctor]] 
  $$
    \array{
       X
       \\
       \Big\downarrow\mathrlap{{}^{f}}
       \\
       Y
    }
    \;\;\;\;\;\mapsto\;\;\;
    \array{
       \mathcal{C}_X
       \\
       \Big\uparrow\mathrlap{{}^{f^\ast}}
       \\
       \mathcal{C}_Y
    }
  $$
  where the base category and all fiber categories $\mathcal{C}_{(-)}$ have [[Cartesian products]] and all [[base change]] morphisms $f^\ast$ [[preserved limit|preserve]] these products, then the [[Grothendieck construction]] $\int_X \mathcal{C}_X$ has cartesian products 
(as a special case of a general result on limits in Grothendieck constructions, discussed [there](Grothendieck+construction#CoLimitsInAGrothendieckConstruction))
which is given on objects
$$
  \mathscr{V}_X \,\equiv\,
  \big(
    \mathscr{V} \,\in\, \mathcal{C}_X
  \big)
$$
by the formula
\[
  \label{CartesianProductInGrothendieckConstruction}
  \mathscr{V}_X
  \times
  \mathscr{W}_Y
  \;\;
  \simeq
  \;\;
  \Big(
    \big(pr_X^\ast \mathscr{V}\big)
    \,\times\,
    \big(pr_Y^\ast \mathscr{W}\big)
  \Big)_{X \times Y}
  \,.
\]
This is the general form of what might be called the "external cartesian product"; see also [this Proposition](free+coproduct+completion#FreeDistributiveCategoryMonad) at *[[free coproduct completion]]*.
\end{example}


## Related concepts

* [[external tensor product of vector bundles]], [[VectBund]]

* [direct product group representations](direct+product+group#Representations)

* [[doubly closed monoidal category]]


## References


The notion of the [[external tensor product of vector bundles]] originates in discussion of [[topological K-theory]]:

*  {#Atiyah67}  [[Michael Atiyah]], §2.6 in: *K-theory*, Harvard Lecture 1964 (notes by D. W. Anderson), Benjamin (1967) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/atiyahk.pdf), [[AtiyahKTheory.pdf:file]]&rbrack;

* {#Bott69} [[Raoul Bott]], p. 19 of: *Lectures on $K(X)$*, Benjamin (1969) &lbrack;[pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/bottk.pdf), [[Bott-KTheory.pdf:file]]&rbrack;

* {#Karoubi} [[Max Karoubi]], §4.9 in: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften **226**, Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007/978-3-540-79890-3](https://doi.org/10.1007/978-3-540-79890-3)&rbrack;

The notion of [[external tensor product of representations]] seems to be [[folklore]], it is mentioned in most textbooks but without any attribution:

* [[William Fulton]], [[Joe Harris]], Ex. 2.36 in: *Representation Theory: a First Course*, Springer (1991) &lbrack;[doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9)&rbrack;

* Caroline Gruson, Vera Serganova, p. 3 of: *From Finite Groups to Quivers via Algebras -- A Journey Through Representation Theory*, Springer (2018) &lbrack;[doi:10.1007/978-3-319-98271-7](https://doi.org/10.1007/978-3-319-98271-7)&rbrack;

The external tensor product of [[perverse sheaves]]:

* [[Volodymyr Lyubashenko]], *External tensor product of categories of perverse sheaves*, Ukr. Math. J. **53** 3 (2001) 311-322 &lbrack;[arXiv:math/9911207](https://arxiv.org/abs/math/9911207)&rbrack;

The external tensor product of of [[quasicoherent sheaves]]  in ([[derived algebraic geometry|derived]]) [[algebraic geometry]]: 

* {#BondalvdBerg03} [[Alexei Bondal]], [[Michel Van den Bergh]], _Generators and representability of functors in commutative and noncommutative geometry_, Mosc. Math. J. **3** 1 (2003) 1-36 &lbrack;[arXiv:math/0204218](https://arxiv.org/abs/math/0204218)&rbrack;

* {#BFN08} [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_, J. Amer. Math. Soc. **23** 4 (2010) 909-966 &lbrack;[arXiv:0805.0157](http://arxiv.org/abs/0805.0157), [ISSN:1088-6834](https://www.ams.org/journals/jams/2010-23-04/S0894-0347-10-00669-7)&rbrack;

The external product on [[cobordism rings]]:

* {#Quillen71} [[Daniel Quillen]], §1.6 in: *Elementary Proofs of Some Results of Cobordism Theory Using Steenrod Operations*, Advances in Mathematics **7** (1971) 29–56 &lbrack;<a href="http://dx.doi.org/10.1016/0001-8708(71)90041-7">doi:10.1016/0001-8708(71)90041-7</a>&rbrack;

and on [[differential cobordism cohomology|differential cobordism rings]]:

* [[Ulrich Bunke]], [[Thomas Schick]], Ingo Schroeder, Moritz Wiethaup, §3.3.10 in: *Landweber exact formal group laws and smooth cohomology theories*, Algebr. Geom. Topol. **9** (2009) 1751-1790 &lbrack;[arXiv:0711.1134](https://arxiv.org/abs/0711.1134), [doi:10.2140/agt.2009.9.1751](https://doi.org/10.2140/agt.2009.9.1751)&rbrack;

and in the [[Hodge-filtered differential cohomology|Hodge-filtered version]]:

* [[Knut Bjarte Haus]], §4.1.8, §4.10 in: *Geometric Hodge filtered complex cobordism*, PhD thesis (2022) &lbrack;[ntnuopen:3017489](https://ntnuopen.ntnu.no/ntnu-xmlui/handle/11250/3017489)&rbrack;

* [[Knut B. Haus]], [[Gereon Quick]], §2.11 in: *Geometric Hodge filtered complex cobordism* &lbrack;[arXiv:2210.13259](https://arxiv.org/abs/2210.13259)&rbrack;


{#ReferencesExternalSmashProduct} The external [[smash product]] of [[retractive spaces]] and of [[parameterized spectra]]:

* {#MaySigurdsson06} [[Peter May]], [[Johann Sigurdsson]], §7.3 of: _[[Parametrized Homotopy Theory]]_, Mathematical Surveys and Monographs **132**, AMS (2006) &lbrack;[arXiv:math/0411656](https://arxiv.org/abs/math/0411656)&rbrack;

* {#Malkiewich19} [[Cary Malkiewich]], §3.1 of: *Parametrized spectra, a low-tech approach* &lbrack;[arXiv:1906.04773](https://arxiv.org/abs/1906.04773), user guide: [pdf](https://people.math.binghamton.edu/malkiewich/users_guide_parametrized.pdf), [[Malkiewich-ParametrizedSpectraUserGuide.pdf:file]]&rbrack;

* {#Malkiewich23} [[Cary Malkiewich]], §2.3 and §4.4 of: *A convenient category of parametrized spectra* &lbrack;[arXiv:2305.15327](https://arxiv.org/abs/2305.15327)&rbrack;


For general abstract literature dealing with the external tensor products see the references at _[[indexed monoidal category]]_ and at _[[dependent linear type theory]]_, such as

* {#Shulman12} [[Mike Shulman]], *Enriched indexed categories*, Theory Appl. Categ. **28** (2013) 616-695 &lbrack;[arXiv:1212.3914](http://arxiv.org/abs/1212.3914), [tac:28-21](http://www.tac.mta.ca/tac/volumes/28/21/28-21abs.html)&rbrack;



[[!redirects external tensor products]]

[[!redirects external product]]
[[!redirects external products]]

[[!redirects external tensor product of representations]]

