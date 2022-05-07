

+-- {: .num_defn #DiffeologicalSingularSimplicialSet} 
###### Definition
**(diffeological singular simplicial set)**

Consider the [[simplicial object|simplicial]] [[diffeological space]]

$$
  \array{
    \Delta 
    &
    \overset{
      \Delta^\bullet_{diff}
    }{
      \longrightarrow
    }   
    &
    DiffeologicalSpaces
    \\
    [n] 
      &\mapsto&
    \Delta^n_{diff}
    \mathrlap{
    \coloneqq
    \big\{
      \vec x \in \mathbb{R}^{n+1}
      \;\vert\;
      \underset{i}{\sum} x^i = 1
    \big\}
    }
  }
$$

which in degree $n$ is the standard extended [[n-simplex]] inside [[Cartesian space]] $\mathbb{R}^{n+1}$, equipped with its sub-[[diffeology]].

This induces a [[nerve and realization]] [[adjunction]] between [[diffeological spaces]] and [[simplicial sets]]:

\[
  \label{NerveAndRealizationForDiffeologicalSpaces}
  DiffeologicalSpaces
  \underoverset
    {
      \underset{Sing_{\mathrlap{diff}}}{\longrightarrow}
    }
    {
      \overset{ \left\vert - \right\vert_{\mathrlap{diff}} }{\longleftarrow}
    }
    {
      \phantom{AA}\bot\phantom{AA}
    }
  SimplicialSets
  \,,
\]

where the [[right adjoint]] is the _diffeological [[singular simplicial set]] [[functor]]_ $Sing_{diff}$. 

=--

(e.g. [Christensen-Wu 13, Def. 4.3](diffeological+space#ChristensenWu13))

+-- {: .num_remark #DiffeologicalSingularSetIsPathGroupoid} 
###### Remark
**(diffeological singular simplicial set as [[path ∞-groupoid]])**

Regarding [[simplicial sets]] as [[classical model structure on simplicial sets|presenting]] [[∞-groupoids]], we may think of $Sing_{diff}(X)$ (Def. \ref{DiffeologicalSingularSimplicialSet}) as the [[path ∞-groupoid]] of the [[diffeological space]] $X$. 

In fact, by the discussion at [[shape via cohesive path ∞-groupoid]] we have that $Sing_{diff}$ is [[equivalence in an (∞,1)-category|equvialent]] to the [[shape modality|shape]] of [[diffeological spaces]] regarded as [[objects]] of the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoids]]:

$$
  Sing_{diff}
  \;\simeq\;
  Shp \circ i
  \;\;\colon\;\;
  DiffeologicalSpaces
  \overset{i}{\hookrightarrow}
  SmoothGroupoids_{\infty}
  \overset{Shape}{\longrightarrow}
   Groupoids_\infty
$$ 

=--
