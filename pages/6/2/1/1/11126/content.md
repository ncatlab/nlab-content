
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
       \mathllap{^{f^\ast}}\Big\uparrow
       \Big\downarrow\mathrlap{{}^{f_!}}
       \\
       \mathcal{Y} &\mapsto& \mathbf{C}_{\mathcal{Y}}
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
  \mathcal{W}_{\mathcal{Y}} \,\in\, \int \mathbf{C}
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
  \text{products preserve colimits}
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
    \underset{\longrightarrow}{lim} 
    (
    \mathcal{X}
    \times
    \mathcal{Y}
    )
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
(The first statement is essentially immediate from the fact that pullback $(-)^*$ is assumed to be strong closed, but the second statement is a not quite so immediate; it is mentioned without proof in [Shulman (2012), p. 624](#Shulman12).)
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
    \,.
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
    \text{by projection formula}
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
    \text{by projection formula}
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

\linebreak


## Examples

* [[external tensor product of vector bundles]]

## Related concepts

* [direct product group representations](direct+product+group#Representations)

* [[VectBund]]

* [[doubly closed monoidal category]]

## References

Textbook accounts concerning the [[external tensor product of vector bundles]]:

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], p. 84 of: *[[Connections, Curvature, and Cohomology]]* Volume 1: _De Rham Cohomology of Manifolds and Vector Bundles_, Academic Press (1973) &lbrack;[ISBN:978-0-12-302701-6](https://www.elsevier.com/books/connections-curvature-and-cohomology-v1/greub/978-0-12-302701-6)&rbrack;

Discussion in the context of categories of [[quasicoherent sheaves]]  in ([[derived algebraic geometry|derived]]) algebraic geometry: 

* {#BondalvdBerg03} [[Alexei Bondal]], [[Michel Van den Bergh]], _Generators and representability of functors in commutative and noncommutative geometry_, Mosc. Math. J. **3** 1 (2003) 1-36 &lbrack;[arXiv:math/0204218](https://arxiv.org/abs/math/0204218)&rbrack;

* {#BFN08} [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_, J. Amer. Math. Soc. 23 (2010), no. 4, 909-966 ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

For general abstract literature dealing with the external tensor products see the references at _[[indexed monoidal category]]_ and at _[[dependent linear type theory]]_, such as

* {#Shulman12} [[Mike Shulman]], *Enriched indexed categories*, Theory Appl. Categ. **28** (2013) 616-695 &lbrack;[arXiv:1212.3914](http://arxiv.org/abs/1212.3914), [tac:28-21](http://www.tac.mta.ca/tac/volumes/28/21/28-21abs.html)&rbrack;


[[!redirects external tensor products]]

[[!redirects external product]]
[[!redirects external products]]

