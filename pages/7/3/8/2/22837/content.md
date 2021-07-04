
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

For $\mathcal{G}$ a [[topological group]] or [[simplicial group]], or generally an [[∞-group]], the [[homotopy type]] of the [[free loop space]] of its [[classifying space]]/[[delooping]] is [[equivalence in an (infinity,1)-category|equivalent]] to the [[homotopy quotient]] of the [[adjoint action|conjugation]] [[∞-action]] of $\mathcal{G}$ on iself:

$$
  \mathcal{L} \mathbf{B}\mathcal{G}
  \;\;
  \simeq
  \;\;
  \mathcal{G} \sslash_{ad} \mathcal{G}
  \,.
$$

For [[discrete groups]] (in particular for [[finite groups]]) this is seen by elementary inspection (Example \ref{FreeLoopSpaceOfDeloopingOfDiscreteGroup} below) and as such is familiar from many related constructions, such as that of [[inertia groupoids]]. 

In more generality the statement is [[folklore]] (as witnessed by parts of the [MO discussion](#MODiscussion)) but rarely argued in detail.

For [[topological groups]] of the [[homotopy type]] of a [[CW-complex]] there is a [[point-set topology|point-set]] argument ([Gruher 2007](#Gruher07)) with continuous paths in the [[universal principal bundle]] which, with some care, largely mimics the naive example . 

More generally, such as for [[simplicial groups]], there is a more abstract computation of the defining [[homotopy pullback]] by [[fibrant resolution]], which is spelled out as Prop. \ref{FreeLoopSpaceOfSimplicialClassifyingSpaceAsAdQuotient} below, following an analogous argument for topological groups indicated in [Klein, Schochet & Smith 2009](#KleinSchochetSmith09).

Finally, since, in the full generality of [[∞-groups]] [[internalization|internal to]] any [[(∞,1)-topos]], hence for [[∞-group]] [[∞-stacks]] $\mathcal{G}$, the [[homotopy quotient]] of an action, regarded in the [[slice (∞,1)-topos|slice]] over the [[delooping]]/[[moduli stack]] $\mathbf{B}\mathcal{G}$, in fact characterizes and *defines* the action as an [[∞-action]]

$$
  \mathcal{G} \,\in\, Groups(\mathbf{H})
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  \mathcal{G}Actions(\mathbf{H})
  \;\;
  \underoverset
    {\;\;\;\;\simeq\;\;\;\;}
    {(-)\sslash \mathcal{G}}
    {\longrightarrow}
  \;\;
  \mathbf{H}_{/\mathbf{B}\mathcal{G}}
$$

one may turn this around ([NSS 12a, Exp. 4.13 (3)](#NSS12a), [SS 20, Exp. 2.82](#SS20)) and *define* the [[adjoint action]] of an [[∞-group]] [[∞-stack]] to be that whose [[homotopy quotient]] over $\mathbf{B}\mathcal{G}$ is the left vertical morphism (eq:HomotopyPullbaclDefiningFreeLoopSpaceObject) in the defining [[homotopy pullback]]-construction of the [[free loop space object]] of $\mathbf{B}\mathcal{G}$.

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
 {#ForSimplicialSets}

We discuss the [[presentable (infinity,1)-category|presentation]] of the phenomenon in the [[classical model structure on simplicial sets]]. 

Let 

* $\mathcal{G}$ be a [[simplicial group]], 

and write

* $\mathcal{G}\Actions(sSet)$ for the [[category]] of $\mathcal{G}$-[[action objects]] [[internalization|internal to]] [[SimplicialSets]]l

* $W \mathcal{G} \in \mathcal{G}Actions(sSet)$ for its [[universal principal simplicial complex]];

* $\overline{W}\mathcal{G} \,=\, \frac{W \mathcal{G}}{\mathcal{G}} \in sSet$ for the [[simplicial classifying space]];

* $\mathcal{G}_{ad} \in \mathcal{G}Actions(sSet)$ for the [[adjoint action]] of $\mathcal{G}$ on itself:

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


\begin{proposition}\label{FreeLoopSpaceOfSimplicialClassifyingSpaceAsAdQuotient}
  The [[free loop space object]] of the [[simplicial classifying space]] $\overline{W} \mathcal{G}$ is [[isomorphism|isomorphic]] in the [[classical homotopy category]] to the [[Borel construction]] of the [[adjoint action]] (eq:ConjugationAction):

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

* all [[objects]] are [[fibrant objects]] ([[Kan complexes]]), since [[simplicial classifying spaces]] $\overline{W}\mathcal{G}$ are Kan complexes, either directly by [this Prop.](simplicial+classifying+space#SimplicialClassifyingSpaces), or as follows:

  * [[simplicial groups]] have underlying [[Kan complexes]] ([this Thm.](simplicial+group#MooreTheorem), which we use below to know that $\mathcal{G}_{ad} \to \ast $ is a [[Kan fibration]]), hence are [[fibrant objects]] in the [[model structure on simplicial groups]];

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

(essentially by its [[Quillen adjunction]] to the [[simplicial loop space]]-functor ([here](model+structure+on+reduced+simplicial+sets#RelationToSimplicialGroups)) and the [[May recognition theorem]], see [NSS 12a, Cor. 3.33](free+loop+space+of+classifying+space#NSS12b)).

In summary this means (by [this Prop.](homotopy+pullback#HomotopyPullbackByOrdinaryPullback)) that this ordinary [[pullback]]-square represents the [[homotopy pullback]] (eq:HomotopyPullbaclDefiningFreeLoopSpaceObject) that defines the [[free loop space object]].

\end{proof}


### For topological spaces
 {#ForTopologicalSpaces}

A [[point-set topology|point-set argument]] for [[topological spaces]]/[[topological groups]] is spelled out in [Gruher 2007, App. A](#Gruher07). Discussion of the [[presentable (infinity,1)-category|presentation]] of the phenomenon in the [[classical model structure on topological spaces]] in the abstract style [above](#ForSimplicialSets) is indicated in [Klein, Schochet & Smith 2009](#KleinSchochetSmith09).

## Examples

### Discrete (finite) groups
 {#ExampleDiscreteGroups}

\begin{example}\label{FreeLoopSpaceOfDeloopingOfDiscreteGroup}
**([[free loop space]] of classifying space of [[discrete groups]])** \linebreak

The archetypical example has $\mathcal{G} = G \in Groups(Sets)$ a [[discrete group]], such as (but not necessarily) a [[finite group]]. In this case the [[classifying space]] $B \mathcal{G} \simeq K(G,1)$ is an [[Eilenberg-MacLane space]] whose [[homotopy type]] is represented in the [[classical homotopy category]] simply by the [[delooping groupoid]] $G \rightrightarrows \ast$ of $G$. With this, the analysis of its [[free loop space]] follows from elementary inspection:

The [[hom-groupoid]]

$$
  \big[
    \mathbf{B}\mathbb{Z}
    ,\,
    \mathbf{B}G
  \big]
  \;\simeq\;
  \big(
     G \times G 
     \underoverset
       {pr_2}
       { Ad }  
       {\rightrightarrows}
     G
  \big)
$$

has 

* as [[objects]] the [[functors]] $\mathbf{B}\mathbb{Z} \longrightarrow \mathbf{B}G$, hence equivalently [[group homomorphisms]] $\mathbb{Z} \to G$, hence equivalently elements $g \in G$;

* as [[morphisms]] the [[natural transformations]] between these, whose single component $h \in G$ must make the naturality [[commuting square|square commute]]

$$
  \array{
    \mathbf{B}\mathbb{Z}
    &\xrightarrow{\;\;\;}&
    \mathbf{B}G
    \\
    \\
    \bullet
    &&
    \bullet 
    &\xrightarrow{\;\;\;h\;\;\;}&
    \bullet
    \\
    \big\downarrow {}^{\mathrlap{1}}
    &&
    \big\downarrow {}^{\mathrlap{g}}
    &&
    \big\downarrow {}^{\mathrlap{g'}}
    \\
    \bullet
    &&
    \bullet
    &\xrightarrow{\;\;\;h\;\;\;}&
    \bullet
  }
$$

The condition that this commutes means equivalently that $g'$ is the image of $g$ under the [[conjugation action]] by $h$:

$$
  h \cdot g' \;=\; g \cdot h
  \;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;
  g' = h^{-1} \cdot g \cdot h \;=\; Ad_h(g) 
  \,.
$$

This shows that the [[hom-groupoid]] is the [[action groupoid]] of the [[conjugation action]]

$$
  \mathcal{L} \mathbf{B}G
  \;\simeq\;
  \big[
    \mathbf{B}\mathbb{Z}
    ,\,
    \mathbf{B}G
  \big]
  \;\simeq\;
  G \sslash_{ag} G
  \,.
$$

\end{example}

This simple example essentially re-appears in the discussion of [[inertia groupoids]].






## Related concepts

* [[free loop space]], [[free loop stack]]

* [[transchromatic character]]

* [[double dimensional reduction]]

* [[classifying space]], [[simplicial classifying space]],

* [[Sullivan model of classifying space]]


## References

A point-set proof in [[TopologicalSpaces]] is given in 

* {#Gruher07} [[Kate Gruher]], *A proof of $L B G \simeq Ad(E G)$*, Appendix A in: *String Topology of Classifying Spaces*, 2007 ([[Gruher_FreeLoopSpaceOfClassifyingSpace.pdf:file]], [proquest:304826261](https://www.proquest.com/docview/304826261))

An abstract proof in the [above](#ForSimplicialSets) style, for [[topological groups]]/[[topological spaces]], is indicated in:

* {#KleinSchochetSmith09} John R. Klein, [[Claude Schochet]], Samuel B. Smith, Lemma 9.1 of: *Continuous trace $C^\ast$-algebras, gauge groups and rationalization*,  Journal of Topology and Analysis Vol. 01, No. 03, pp. 261-288 (2009)  ([arXiv:0811.0771](https://arxiv.org/abs/0811.0771), [doi:10.1142/S179352530900014X](https://doi.org/10.1142/S179352530900014X))

See also:

* {#MODiscussion} MathOverflow discussion [MO/q/20671](https://mathoverflow.net/q/20671/381)

Discussion in the generality of [[∞-groups]] in [[(∞,1)-toposes]] and defining the [[adjoint action]] in this generality:

* {#NSS12a} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], Example 4.13 (3) in: *[[schreiber:Principal ∞-bundles -- theory, presentations and applications|Principal ∞-bundles -- General theory]]*, Journal of Homotopy and Related Structures, Volume 10, Issue 4 (2015), pages 749-801 
([doi:10.1007/s40062-014-0083-6](http://link.springer.com/article/10.1007/s40062-014-0083-6), [arXiv:1207.0248](http://arxiv.org/abs/1207.0248))

* {#SS20} [[Hisham Sati]], [[Urs Schreiber]], Example 2.82 in: *[[schreiber:Proper Orbifold Cohomology]]* ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

and formulated more in the language of [[homotopy type theory]]:

* {#BuchholtzDoornRijke18} [[Ulrik Buchholtz]], [[Floris van Doorn]], [[Egbert Rijke]], p. 11 of: _Higher Groups in Homotopy Type Theory_, LICS '18: Proceedings of the 33rd Annual ACM/IEEE Symposium on Logic in Computer Science  ([arXiv:1802.04315](https://arxiv.org/abs/1802.04315), [doi:10.1145/3209108.3209150](https://doi.org/10.1145/3209108.3209150))


[[!redirects free loop spaces of classifying spaces]]

[[!redirects free loop space of a classifying space]]

