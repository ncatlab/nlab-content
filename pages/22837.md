
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $\mathcal{G}$ a [[topological group]] or [[simplicial group]], or generally an [[∞-group]], the [[homotopy type]] of the [[free loop space]] of its [[classifying space]]/[[delooping]] is [[equivalence in an (infinity,1)-category|equivalent]] to the [[homotopy quotient]] of the [[conjugation action|conjugation]] [[∞-action]] of $\mathcal{G}$ on iself:

$$
  \mathcal{L} \mathbf{B}\mathcal{G}
  \;\;
  \simeq
  \;\;
  \mathcal{G} \sslash_{ad} \mathcal{G}
  \,.
$$

## Proof

The statement is [[folklore]], but complete proofs in the literature are rare.

Recall that the [[free loop space object]] of $\mathbf{B}\mathcal{G}$ (in particular) is defined to be [[homotopy pullback]]/[[homotopy fiber product]] of the [[diagonal morphism]] on $\mathbf{B}\mathcal{G}$ along/with itself:

\[
  \label{HomotopyPullbaclDefiningFreeLoopSpaceObject}
  \array{
    \mathcal{L} \mathbf{B}\mathcal{G}
    &\longrightarrow&
    \mathbf{B}\mathcal{G}
    \\
    \big\downarrow 
    &\swArrow_{\mathrlap{pb}}& 
    \big\downarrow {}^{\mathrlap{diag}}
    \\
    \mathbf{B}\mathcal{G}
    &\xrightarrow{\;\;\;diag\;\;\;}&
    \mathbf{B}\mathcal{G} \times \mathbf{B} \mathcal{G}
  }
\]


### For simplicial sets

We discuss the [[presentable (infinity,1)-category|presentation]] of the phenomenon in the [[classical model structure on simplicial sets]]. 

Let 

* $\mathcal{G}$ be a [[simplicial group]], 

and write

* $\mathcal{G}\Actions(sSet)$ for the [[category]] of $\mathcal{G}$-[[action objects]] [[internalization|internal to]] [[SimplicialSets]]l

* $W \mathcal{G} \in \mathcal{G}Actions(sSet)$ for its [[universal principal simplicial complex]];

* $\overline{W}\mathcal{G} \,=\, \frac{W \mathcal{G}}{\mathcal{G}} \in sSet$ for the [[simplicial classifying space]];

* $\mathcal{G}_{ad} \in \mathcal{G}Actions(sSet)$ for the [[conjugation action]] of $\mathcal{G}$ on itself:

  \[
    \label{ConjugationAction}
    \array{
      \mathcal{G}_{ad} \times \mathcal{G}
      &\xrightarrow{\;\;\;}&
      \mathcal{G}_{ad}
      \\
      (g_k,h_k) &\mapsto&  h_k \cdot g_k \cdot h_k^{-1}
    }
  \]

  which we may understand as the restriction along the [[diagonal morphism]] $\mathcal{G} \xrightarrow{diag} \mathcal{G} \times \mathcal{G}$ of the following action of the [[direct product group]]:

  $$
    \array{
      \mathcal{G}_{ad}
      \times 
      (\mathcal{G} \times \mathcal{G})
      &\xrightarrow{\;\;\;}&
      \mathcal{G}_{ad}
      \\
      (g_k, (h'_k, h_k))
      &\mapsto&
      h'_k \cdot g_k \cdot h^{-1}_k
      \mathrlap{\,.}
    }
  $$


\begin{proposition}
  The [[free loop space object]] of the [[simplicial classifying space]] $\overline{W} \mathcal{G}$ is [[isomorphism|isomorphic]] in the [[classical homotopy category]] to the [[Borel construction]] of the [[conjugation action]] (eq:ConjugationAction):

$$
  \mathcal{L}
  \big(
    \overline{W}\mathcal{G}
  \big)
  \;\;
  \simeq
  \;\;
  \mathcal{G}_{ad} \sslash \mathcal{G}
  \;\;\;\;\;\;
  \in
  \;\;
  Ho\big(
    sSet_{Qu}
  \big)
$$
\end{proposition}
\begin{proof}

Consider the following [[commuting diagram]] of [[SimplicialSets]]:

\begin{tikzcd}
    &&
    &[-15pt]
    \frac{W \mathcal{G}}{\mathcal{G}}
    \times W\mathcal{G}
    \ar[
      dr,
      "\mathrm{pr}_1 \in \mathrm{W}"{description}
    ]
    &[-15pt]
    \\
    \frac{
      \mathclap{\phantom{\vert_a}}
      W \mathcal{G} \times \mathcal{G}_{\scalebox{.4}{ad}}
    }{
      \mathcal{G}
    }
    \ar[dd]
    \ar[rr]
    \ar[
      ddrr,
      phantom,
      "\mbox{\tiny\rm (pb)}"{pos=.14}
    ]
    &&
    \frac{
      \mathclap{\phantom{\vert_a}}
      W \mathcal{G} \times W\mathcal{G} \times \mathcal{G}_{\scalebox{.4}{ad}}
    }
    {
      \mathcal{G} \times \mathcal{G}
    }
    \ar[
      ur,
      "\sim"{sloped, below},
      "{
        \scalebox{.7}{$
        \!\!\!\!
        [\vec g, (\vec g',h)] \mapsto ([\vec g], h^{-1}\cdot \vec g')
        $}
      }"{sloped, above}
    ]
    \ar[
      dd,
      "\in \mathrm{Fib}"{right},
      "
       \frac{
         W(\mathcal{G} \times \mathcal{G})
         \times
         \left(
           \!\!\!\!\!\!
           \begin{array}{c}
             \mathcal{G}_{\scalebox{.4}{ad}}
             \\
             \downarrow
             \\
             \ast
           \end{array}
           \!\!\!\!\!\!
         \right)
       }{
         \mathclap{\phantom{\vert^{a}}}
         \mathcal{G} \times \mathcal{G}
       }
      "{left}
    ]
    &
    &
    \frac{
      W\mathcal{G}
    }
    {
     \mathcal{G}
    }
    \ar[
      ddll,
      "\mathrm{diag}"{right, xshift=4pt}
    ]
    \ar[
      ll,
      "\in \mathrm{W}"{below},
      "{
        [ \vec g, (\vec g, e) ]
        \raisebox{5pt}{\rotatebox{180}{$\mapsto$}}
        [\vec g]
      }"{above}
    ]
    \\
    \\
    \frac{
      W\mathcal{G}
    }{
      \mathcal{G}
    }
    \ar[
      rr,
      "\mathrm{diag}"{below}
    ]
    &&
    \frac{
      W \mathcal{G} \times W\mathcal{G}
    }{
      \mathcal{G} \times \mathcal{G}
    }
\end{tikzcd}

Here:

* all [[objects]] are [[fibrant objects]] ([[Kan complexes]]), since 

  * [[simplicial groups]] have underlying [[Kan complexes]] ([this Thm.](simplicial+group#MooreTheorem)) hence are [[fibrant objects]] in the [[model structure on simplicial groups]];

  * the [[simplicial classifying space]]-functor $W(-)/(-)$ is a [[right Quillen functor]] to the [[model structure on reduced simplicial sets]] ([this Prop.](model+structure+on+reduced+simplicial+sets#QuillenAdjunctionWithSimplicialGroups)), hence takes values in [[fibrant objects]];

  * fibrant reduced simplicial sets are Kan complexes ([this Prop.](model+structure+on+reduced+simplicial+sets#FibrationsInTermsOfKanFibrations));

* the right vertical morphism is a [[fibration]] ([[Kan fibration]]), since it is the image under the [[right Quillen functor]] $(W \mathcal{G} \times (-)) /\mathcal{G}$ on the [[Borel model structure]] ([this Prop.](Borel+model+structure#QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace));

* the top right morphism is a [[simplicial weak equivalence]], by [[two-out-of-three]], as it is a [[right inverse]] of the triangular morphisms, which are manifestly a simplicial weak eqivalence since $W \mathcal{G}$ is [[contractible homotopy type|contractible]] (by ... the discussion at *[[decalage]]*, at least).

One verifies by inspection that the [[commuting square]] shown is an ordinary [[pullback]] in [[SimplicialSets]]. 

Finally notice that the [[simplicial classifying space]]-construction is indeed a model for the [[delooping]] 

$$
  \overline{W}\mathcal{G}
  \;\;
  \simeq
  \;\;
  \mathbf{B}\mathcal{G}
  \;\;\;
  \in
  \;
  Ho(\infty Groupoids)
$$

(essentially by its [[Quillen adjunction]] to the [[simplicial loop space]]-functor ([here](model+structure+on+reduced+simplicial+sets#RelationToSimplicialGroups)) and the [[May recognition theorem]], see [NSS12b, Cor. 3.33](free+loop+space+of+classifying+space#NSS12b)).

In summary this means (by [this Prop.](homotopy+pullback#HomotopyPullbackByOrdinaryPullback)) that this ordinary [[pullback]]-square represents the [[homotopy pullback]] (eq:HomotopyPullbaclDefiningFreeLoopSpaceObject) that defines the [[free loop space object]].

\end{proof}


### For topological spaces

We discuss the [[presentable (infinity,1)-category|presentation]] of the phenomenon in the [[classical model structure on topological spaces]]. 


(...)

## Related concepts

* [[free loop space]], [[free loop stack]]

* [[classifying space]], [[simplicial classifying space]],

* [[Sullivan model of classifying space]]



## References

The proof idea for [[topological spaces]] is indicated in:

* John R. Klein, [[Claude Schochet]], Samuel B. Smith, Lemma 9.1 of: *Continuous trace $C^\ast$-algebras, gauge groups and rationalization*,  Journal of Topology and Analysis Vol. 01, No. 03, pp. 261-288 (2009)  ([arXiv:0811.0771](https://arxiv.org/abs/0811.0771), [doi:10.1142/S179352530900014X](https://doi.org/10.1142/S179352530900014X))

See also:

* MathOverflow discussion [MO/q/20671](https://mathoverflow.net/q/20671/381)

Discussion in the generality of [[∞-groups]] in [[(∞,1)-toposes]]:

* {#NSS12b} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], Example 4.13 (3) in: *[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- General theory]]*, Journal of Homotopy and Related Structures, Volume 10, Issue 4 (2015), pages 749-801 
([doi:10.1007/s40062-014-0083-6](http://link.springer.com/article/10.1007/s40062-014-0083-6), [arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

* [[Hisham Sati]], [[Urs Schreiber]], Example 2.82 in: *[[schreiber:Proper Orbifold Cohomology]]* ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

[[!redirects free loop spaces of classifying spaces]]

