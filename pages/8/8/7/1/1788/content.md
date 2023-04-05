
\begin{definition}
  For any [[ground field]], write [[VectBund|$Vect_{Set}$]] for the [[category]] of [[indexed sets]] of [[vector spaces]].
\end{definition}
\begin{remark}
We may and will present [[objects]] $\mathcal{V}$ of [[VectBund|$Vect_{Set}$]] as [[pairs]] consisting of a [[set]] $S$ and a [[function]] $\mathcal{V}_{(-)}$ (really a [[functor]] on the [[discrete category]] on $S$) to [[Vect]]:
$$
  \left(
    \array{
      S &\longrightarrow& Vect
      \\
      s &\mapsto& \mathcal{V}_s
    }
  \right)
  \;\;
  \in
  \;\;
  Vect_{Set}
  \mathrlap{\,.}
$$
\end{remark}

\begin{definition}
\label{ExternalTensorProductInVectSet}
The "[[external tensor product|external]]" [[tensor product]] on [[VectBund|$Vect_{Set}$]] is the [[functor]] 
$$
  \boxtimes
  \,\colon\,
  Vect_{Set} \times VectSet 
    \longrightarrow
  Vect_{Set}
$$
given by
$$
  \big(
    \mathcal{V}_{(-)} \,\colon\, S \to \Vect
  \big)
  \,\boxtimes\,
  \big(
    \mathcal{V}'_{(-)} \,\colon\, S' \to \Vect
  \big)
  \;\;
  \coloneqq
  \;\;
  \left(
    \array{
      S \times S' &\longrightarrow& \Vect
      \\
      (s, s') 
        &\mapsto& 
      \mathcal{V}_s \otimes \mathcal{V}'_{s'}
    }
  \right)
  \mathrlap{\,.}
$$
\end{definition}

\begin{proposition}
\label{CoproductInVectSet}
  The [[coproduct]] in [[VectBund|$Vect_{Set}$]] is given by [[disjoint union]] of [[bundles]]:
$$
  \big(
    \mathcal{V}^{(1)}_{(-)} \,\colon\, S_1 \to \Vect
  \big)
  \;
  \sqcup
  \;
  \big(
    \mathcal{V}^{(1)}_{(-)} \,\colon\, S_2 \to \Vect
  \big)
  \;\;
  \simeq
  \;\;
  \left(
    \array{
      S_1 \sqcup S_2 &\longrightarrow& \Vect
      \\
      s_i &\mapsto& \mathcal{V}^{(i)}_{s_i}
    }
  \right)
$$
\end{proposition}
\begin{proof}
  It is immediate to check the [[universal property]] characterizing the coproduct.
\end{proof}

\begin{proposition}
The [[external tensor product]] $\boxtimes$ 
(Def. \ref{ExternalTensorProductInVectSet})
[[distributive monoidal category|distributes]] over the coproduct (Prop. \ref{CoproductInVectSet}):
$$
  \mathcal{E} \boxtimes ( \mathcal{V}^{(1)} \sqcup  \mathcal{V}^{(2)}) 
  \;\simeq\;
  \big(  
    \mathcal{E} \boxtimes \mathcal{V}^{(1)}
  \big)
  \,\sqcup\,
  \big(
    \mathcal{E} \boxtimes \mathcal{V}^{(2)}
  \big)
$$
and hence gives a [[distributive monoidal category]]:
$$
  \big(
    Vect_{Set}
    ,
    \sqcup
    ,
    \boxtimes
  \big)
  \;\in\;
  DistMonCat
  \mathrlap{\,.}
$$
\end{proposition}
\begin{proof}
Unwinding the above definitions and using that [[Set]] is a [[distributive category]], we have the following sequence of [[natural isomorphisms]]:
$$
  \begin{array}{l}
    \mathcal{E} 
    \,\boxtimes\,
    \big(
      \mathcal{V}^{(1)}
      \,\sqcup\,
      \mathcal{V}^{(2)}
    \big)
    \\
    \;\equiv\;
    \big(
      \mathcal{E}_{(-)} \,\colon\, S_E \to Vect
    \big)
    \,\boxtimes\,
    \Big(
      \big(
        \mathcal{V}^{(1)}_{(-)} \,\colon\, S_1 \to Vect
      \big)
      \,\sqcup\,
      \big(
        \mathcal{V}^{(2)}_{(-)} \,\colon\, S_2 \to Vect
      \big)
    \Big)
    \\
    \;\simeq\;
    \big(
      \mathcal{E}_{(-)} \,\colon\, S_E \to Vect
    \big)
    \,\boxtimes\,
    \left(
      \array{
        S_1 \sqcup S_2 &\longrightarrow& Vect
        \\
        s_i &\mapsto& \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        S_E \times (S_1 \sqcup S_2)
        &\longrightarrow& Vect
        \\
        (s_E , s_i) &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        (S_E \times S_1) \,\sqcup\, (S_2 \times S_2)
        &\longrightarrow& Vect
        \\
        (s_E , s_i) &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        S_E \times S_1 
        &\longrightarrow& Vect
        \\
        (s_E , s_1) 
         &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(1)}_{s_1}
      }
    \right)
    \,\sqcup\,
    \left(
      \array{
        S_E \times S_2 
        &\longrightarrow& Vect
        \\
        (s_E , s_2) 
         &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(2)}_{s_2}
      }
    \right)
    \\
    \;\equiv\;
    \mathcal{E} \boxtimes \mathcal{V}^{(1)}
    \,\sqcup\,
    \mathcal{E} \boxtimes \mathcal{V}^{(2)}
  \end{array}
$$
\end{proof}









Consider the following [[very large category|very large]] [[(2,1)-categories]]:

* $Cat$ of [[categories]] 

* $MonCat$ of [[monoidal categories]];

* $CoCartCart$ of [[cocartesian monoidal categories]];

* $DistMonCat$ of [[distributive monoidal categories]] (with [[underlying]] [[cocartesian monoidal categories]]).

Here we understand that 

* the [[1-morphisms]] in these [[2-categories]] are [[functors]] which respect all given [[tensor products]] up to [[isomorphism]], i.e. [[strong monoidal functors]]

* the [[2-morphisms]] are [[natural isomorphisms]] between these functors.

The system of [[forgetful functor|forgetful]] [[2-functors]] between these [[(2,1)-categories]] forms a square [[diagram]] which we may regard as the [[image]] of a corresponding [[contravariant functor|contravariant]] [[pseudofunctor]] from the [[commuting square]]-[[diagram category]] to [[2Cat]]:


$$
  \mathbf{C}
  \;\;
    \colon
  \;\;
  \array{
    (1,0) &\longrightarrow& (1,1)
    \\
    \big\downarrow && \big\downarrow
    \\
    (0,0) &\longrightarrow& (1,0)
  }
  \;\;\;\;
    \mapsto
  \;\;\;\;
  \array{
     MonCat &\longleftarrow& DistMonCat
     \\
     \big\downarrow && \big\downarrow
     \\
     Cat &\longleftarrow& CoCartCat
  }
$$

Now consider the [[(infinity,1)-Grothendieck construction|(2,1)-]][[Grothendieck construction]] $\int \mathbf{C}$ on this [[pseudofunctor]]. Here [[1-morphisms]] are functors which strictly preserve the [[tensor products]] present on their [[domain]] category, but whose [[codomain]] may be equipped with further [[tensor products]] (though not with fewer tensor products).

**Claim.** In $\int \mathbf{C}$ the following [[diagram]] is a ([[homotopy pushout|homotopy]]) [[pushout]]

\begin{tikzcd}
  \big(
    \mathrm{Vect}
    , 
    \otimes
  \big)
  \ar[rr]
  &&
  \big(
    \mathrm{Vect}_{\mathrm{Set}}
    ,
    \sqcup
    , 
    \otimes
  \big)
  \\
  \mathrm{Vect}
  \ar[u]
  \ar[
    rr
  ]
  &&
  \big(
    \mathrm{Vect}_{\mathrm{Set}}
    ,
    \sqcup
  \big)
  \ar[u]
\end{tikzcd}


**Proof.**

We check the [[universal property]]. To this end, observe that any [[cocone]] under the diagram must have tip a [[distributive monoidal category]], since only these can receive morphisms in $\int \mathbf{C}$ both from a monoidal and a cocartesian category.

This means that a general [[cocone]] looks like the following solid diagram:

\begin{tikzcd}
  && 
  &[-10pt]
  \big(
    \mathcal{C}
    ,
    \sqcup
    ,
    \otimes
  \big)
  \\[-10pt]
  \big(
    \mathrm{Vect}
    , 
    \otimes
  \big)
  \ar[rr]
  \ar[urrr]
  &&
  \big(
    \mathrm{Vect}_{\mathrm{Set}}
    ,
    \sqcup
    , 
    \otimes
  \big)
  \ar[
    ur,
    dashed
  ]
  \\
  \mathrm{Vect}
  \ar[u]
  \ar[
    rr
  ]
  &&
  \big(
    \mathrm{Vect}_{\mathrm{Set}}
    ,
    \sqcup
  \big)
  \ar[u]
  \ar[uur]
\end{tikzcd}

We need to see that this uniquely admits the dashed arrow. Unwinding the definitions, the existence of the dashed arrow means that any functor $F \,\colon\, Vect_{Set} \to \mathcal{C}$ which preserves both the coproduct of vector bundles as well as the tensor product on fibers already respects the [[external tensor product]]. But this follows by the [[distributive monoidal category|distributivity]] and using that any [[set]] is the [[coproduct]] of its elements:

$$
  \begin{array}{l}
    F\big( \mathcal{E} \boxtimes \mathcal{E}' \big)
    \\
    \;\simeq\;
    F
    \Bigg(
      \underset{s \in S}{\coprod} 
      \left(
        \array{
          \{s\} &\longrightarrow& Vect
          \\
          s &\mapsto& \mathcal{E}_s 
        }
      \right)
      \;\;
      \boxtimes
      \;\;
      \underset{s' \in S'}{\coprod} 
      \left(
        \array{
          \{s'\} &\longrightarrow& Vect
          \\
          s' &\mapsto& \mathcal{E}'_{s'} 
        }
      \right)
    \Bigg)
    \\
    \;\simeq\;
    F
    \Bigg(
      \underset{(s, s') \in S \times S'}{\coprod}
      \Big(
        \big(
          (s \colon \{s\}) \mapsto \mathcal{E}_s
        \big)
        \boxtimes
        \big(
          (s' \colon \{s'\}) \mapsto \mathcal{E}_{s'}
        \big)
      \Big)
    \Bigg)
    \\
    \;\simeq\;
    \underset{(s, s') \in S \times S'}{\coprod}
    \bigg(
      \Big(
        F
        \big(
          (s \colon \{s\}) \mapsto \mathcal{E}_s
        \big)
       \Big)
        \boxtimes
       \Big(
        F
        \big(
          (s' \colon \{s'\}) \mapsto \mathcal{E}_{s'}
        \big)
      \Big)
    \bigg)
    \\
    \;\simeq\;
      \Big(
        F
        \big(
          \underset{s \in S}{\coprod}
          (s \colon \{s\}) \mapsto \mathcal{E}_s
        \big)
       \Big)
        \boxtimes
       \Big(
        F
        \big(
          \underset{s' \in S'}{\coprod}
          (s' \colon \{s'\}) \mapsto \mathcal{E}_{s'}
        \big)
      \Big)
    \\
    \;\simeq\;
    F(\mathcal{E}) \boxtimes F(\mathcal{E}')
    \,.
  \end{array} 
$$







