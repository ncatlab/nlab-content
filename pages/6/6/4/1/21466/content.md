

### Embedding tensors and tensor hierarchy in super/dg-Lie theory
  {#EmbeddingTensorsAndTensorHierarchyInSuperdgLieTheory}

We spell out aspects of the formalization of the concept of [[embedding tensors]] and their [[tensor hierarchies]] in terms of [[super Lie algebras]]/[[dg-Lie algebras]].


#### The super Lie algebra of multi-endomorphisms
  {#TheSuperLieAlgebraOfEndomorphisms}

The algebra of [[embedding tensors]] and their [[tensor hierarchies]] turns out to be neatly captured by structure found in or induced from the following [[super Lie algebra]].

The following construction is briefly highlighted in [Palmkvist 09, 2.3](M-brane+3-algebra#Palmkvist09) [Palmkvist 13, 3.1](tensor+hierarchy#Palmkvist13) (reviewed more clearly in [Lavau-Palmkvist 19, 2.4](tensor+hierarchy#LavauPalmkvist19)) where it is attributed to [Kantor 70](super+Lie+algebra#Kantor70):


+-- {: .num_defn #TheSuperLieAlgebraInducedFromVectorSpace}
###### Definition
**([[super Lie algebra]] of [[multimorphism|multi]]-[[endomorphisms]])**

Let $V$ be a [[finite-dimensional vector space]] over some [[ground field]] $k$.

Define a $\mathbb{Z}$-[[graded vector space]] 

$$
  MultEnd(V) \;\in \; Vect_k^{\mathbb{Z}}
  \,,
$$

concentrated in degrees $\leq 1$, [[recursion|recursively]] as follows:

For $n =1$ we set

$$
  MultEnd(V)_{1}
  \;\coloneqq\;
  V
  \,.
$$

For $n \leq 0 \in \mathbb{Z}$, the component space in degree $n-1$ is taken to be the vector space of [[linear maps]] from $V$ to the component space in degree $n$:

$$
  MultEnd(V)_{n-1}
  \;\coloneqq\;
  Hom_k( V, MultEnd(V)_n )
  \,.
$$

Hence:

\[
  \label{ExplicitComponentSpacesOfSuperLieAlgebraInducedFromVectorSpace}
  \begin{aligned}
    MultEnd(V)_1 & = V
    \\
    MultEnd(V)_0 & = Hom_k(V,V) = \mathfrak{gl}(V)
    \\
    MultEnd(V)_{-1} & =  Hom_k(V, Hom_k(V,V)) \simeq  Hom_k(V \otimes V, V)
    \\
    MultEnd(V)_{-2} & = Hom_k(V, Hom_k(V, Hom_k(V,V))) \simeq  Hom_k(V \otimes V \otimes V, V)
    \\
    \vdots
  \end{aligned}
\]

Consider then the [[direct sum]] of these component spaces as a [[super vector space]] with the [[even number]]/[[odd number]]-degrees being in super-even/super-odd degree, respectively.

On this [[super vector  space]] consider a [[super Lie bracket]] defined [[recursion|recusively]] as follows:

For all $v_1, v_2 \in MultEnd(V)_1 = V$ we set

$$
  [v_1, v_2] \;=\; 0
  \,.
$$

For $f \in MultEnd(V)_{n \leq 0}$ and $v \in MultEnd(V)_1 = V$ we set

\[
  \label{SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace}
  [f, v]
  \;\coloneqq\;
  f(v)
\]

Finally, for $f\in MultEnd(V)_{ deg(f) \leq 0 }$ and $g\in MultEnd(V)_{deg(g) \leq 0}$ we set

\[
  \label{SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace}
  \begin{aligned}
  [f, g]
  &
  \colon\;
  v 
  \;\mapsto\;
  [f, g(v)]
  -
  (-1)^{
    deg(f) deg(g)
  }
  [ g, f(v) ]
  \\
  \end{aligned}
\]

=--

+-- {: .num_remark #ConstraintsOnBracketInSuperLieAlgebraInducedByVectorSpace}
###### Remark

By (eq:SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace) the definition (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) is equivalent to

$$
  [ [f,g],v ]
  \;=\;
  [f, [g,v] ]
  -
  (-1)^{
    deg(f) deg(g)
  }
  [ g, [f,v] ]
$$


Hence (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) is already implied by (eq:SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace) if the bracket is to satisfy the [super Jacobi identity](super+Lie+algebra#eq:GradedJacobiIdentity)

=--

It remains to show that:

+-- {: .num_prop #SuperJacobiForSuperLieAlgebraInducedFromVectorSpace}
###### Proposition

Def. \ref{TheSuperLieAlgebraInducedFromVectorSpace} indeed gives a [[super Lie algebra]] in that the bracket (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) satisfies the [super Jacobi identity](super+Lie+algebra#eq:GradedJacobiIdentity).

=--

+-- {: .proof}
###### Proof

We proceed by [[induction]]:

By Remark \ref{ConstraintsOnBracketInSuperLieAlgebraInducedByVectorSpace} we have that the super Jacobi identity holds for all [[triples]] $f_1, f_2, f_3 \in MultEnd(V)$ with $deg(f_3) \geq 0$.

Now assume that the super Jacobi identity has been shown for triples $(f_1, f_2, f_3(v))$ and $(f_1, f_3, f_2(v))$, for any $v \in V$. The following computation shows that then it holds for $(f_1, f_2, f_3)$:

$$
  \begin{aligned}
    [f_1, [f_2, f_3] ] (v)
    & 
    =
    [ f_1,  [f_2, f_3](v) ] 
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    [  [ f_2, f_3 ], f_1(v)  ]
    \\
    & =
    [ f_1,  [  f_2, f_3(v) ] ] 
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_2)deg(f_3)}
    [ f_1,  [  f_3, f_2(v) ] ] 
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    [  f_2,  [ f_3,  f_1(v) ] ]
    \\
    & \phantom{=}
    +    
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3)) + deg(f_2)deg(f_3)}
    [  f_3,  [ f_2,  f_1(v) ] ]
    \\
    & = 
    [ f_1,  [  f_2, f_3(v) ] ] 
    -
    (-1)^{deg(f_1) deg(f_2)}
    {
    \color{green}
    [ f_2,  [  f_1, f_3(v) ] ] 
    }
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_2) deg(f_3)}
    \big(
    [ f_1,  [  f_3, f_2(v) ] ] 
    -
    (-1)^{deg(f_1) deg(f_3)}
    {
    \color{orange}
    [ f_3,  [  f_1, f_2(v) ] ] 
    }
    \big)
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    \big(
    [  f_2,  [ f_3,  f_1(v) ] ]
    -
    (-1)^{deg(f_1)deg(f_3)}
    {
    \color{blue}
    [  f_2,  [ f_1,  f_3(v) ] ]   
    }
    \big)
    \\
    & \phantom{=}
    +    
    (-1)^{deg(f_1) deg(f_2 ) + deg(f_1) deg(f_3) + deg(f_2) deg(f_3)}
    \big(
    [  f_3,  [ f_2,  f_1(v) ] ]
    -
    (-1)^{deg(f_1) deg(f_2)}
    {
    \color{cyan}
    [  f_3,  [ f_1,  f_2(c) ] ]
    }
    \big)
    \\
    & \phantom{=}
    +
    (-1)^{deg(f_1) deg(f_2)}
    \big(
    \underset{
      = 0
    }{
    \underbrace{
    +
    {
    \color{green}
    [ f_2,  [  f_1, f_3(v) ] ] 
    }
    -
    {
    \color{blue}
    [  f_2,  [ f_1,  f_3(v) ] ]
    }
    }
    }
    \big)
    \\
    & \phantom{=}
    +
    (-1)^{deg(f_1) deg(f_3) + deg(f_2) deg(f_3)}
    \big(
    \underset{
      = 0
    }{
    \underbrace{
    {
    \color{orange}
    [  f_3,  [ f_1,  f_2(v) ] ]
    }
    -
    {
    \color{cyan}
    [ f_3,  [  f_1, f_2(v) ] ] 
    }
    }
    }
    \big)
    \\
    & =
    \big[
      [f_1, f_2], f_3(v)
    \big]   
    \\
    & \phantom{=}
    -
    (-1)^{ deg(f_2) deg(f_3) } 
    \big[
      [f_1, f_3], f_2(c) 
    \big]
    \\
    & \phantom{=}
    +
    (-1)^{ deg(f_1) deg(f_2)  }
    \big[
      f_2, [f_1, f_3](v)
    \big]
    \\
    & \phantom{=}
    -
    (-1)^{ deg(f_3)( deg(f_1) + deg(f_2) ) } 
    \big[
      f_3, [f_1, f_2](v) 
    \big]
    \\
    & =
    \big[
     [f_1, f_2], f_3
    \big](v)
    +
    (-1)^{deg(f_1)deg(f_2))}
    \big[
      f_2, [f_1, f_3]
    \big](v)
  \end{aligned}
$$

> (Fine, but is this sufficient to induct over the full range of all three degrees?)

=--


+-- {: .num_example #LieBracketOnglInsideSuperLieAlgebraInducedFromVectorSpace}
###### Example

For $f,g \in MultEnd(V)_0 = Hom_k(V,V)$ (eq:ExplicitComponentSpacesOfSuperLieAlgebraInducedFromVectorSpace) we have that the bracket on $MultEnd(V)$ in Def. \ref{SuperLieAlgebraInducedFromVectorSpace} restricts to

$$
  [f,g](v)
  \;=\;
  [f,g(v)] - [g,f(v)]
  \;=\;
  f(g(v)) - g(f(v))
$$

(by combining (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) with (eq:SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace)).

This is the [[Lie bracket]] of the [[general linear Lie algebra]] $\mathfrak{gl}(V)$, as indicated on the right in (eq:ExplicitComponentSpacesOfSuperLieAlgebraInducedFromVectorSpace).

=--

#### Embedding tensors

+-- {: .num_defn #EmbeddingTensor}
###### Definition
**([[embedding tensor]])**

Given 

* $\mathfrak{g}$ a [[Lie algebra]],

* $\mathfrak{g} \otimes V \overset{\rho}{\longrightarrow} V $ a [[Lie algebra representation]] of $\mathfrak{g}$ 

  (typically required to be a [[faithful representation]], see Remark \ref{EmbeddingTensorsInduceTensorHierarchies} below),

then an *embedding tensor* is a [[linear map]]

$$
  \Theta
  \;\colon\;
  V \longrightarrow \mathfrak{g}
$$

such that for all $v_i \in V$ the following condition ("quadratic constraint") is satisfied:

\[
  \label{QuadraticConstraint}
  [\Theta(v_1), \Theta(v_2)]
  \;=\;
  \Theta
  \big(
    \rho_{\Theta(v_1)}(v_2)
  \big)
  \,,
\]

where on the left we have the [[Lie bracket]] of $\mathfrak{g}$.

=--

The idea of this definition goes back to [Nicolai-Samtleben 00](embedding+tensor#NicolaiSamtleben00), with many followups  in the literature on [[tensor hierarchies]] in [[gauged supergravity]]. The above mathematical formulation is due to [Lavau 17](embedding+tensor#Lavau17).

+-- {: .num_remark #RelationToLeibnizAlgebraStructure}
###### Remark
**([[Leibniz algebra]]-[[mathematical structure|structure]])**

The "quadratic constraint" (eq:QuadraticConstraint) implies (see [this Prop.](Leibniz+algebra#LeibnizAlgebraFromLieModuleAndEmbeddingTensor)) that the [[magma|product]]

\[
  \label{InducedLeibnizAlgebraStructure}
  \array{
     V \otimes V
     &\overset{ }{\longrightarrow}&
     V
     \\
     (v_1, v_2) 
       &\mapsto& 
     v_1 \cdot v_2 
     \mathrlap{
       \;\coloneqq\;
       \rho_{\Theta(v_1)}(v_2)
     }
  }
\]

makes (the underlying [[vector space]] of) $V$ a [[Leibniz algebra]].
Conversely, if a [[Leibniz algebra]] structure "$\cdot$" on $V$ is already given, we may ask that it coincides with this one induced from the embedding tensor, a condition then called the _linear constraint_:

\[
  \label{LinearConstraint}
  v_1 \cdot v_2 \;=\; \rho_{\Theta(v_1)}(v_2)
  \,.
\]

With respect to this induced Leibniz algebra structure, hence equivalently with the "linear constraint" (eq:LinearConstraint) understood, the "quadratic constraint" (eq:QuadraticConstraint) equivalently says that the embedding tensor is a [[homomorphism]] of [[Leibniz algebras]] (using that [[Lie algebras]] are special cases of a Leibniz algebras):

$$
  [\Theta(v_1), \Theta(v_2)]
  \;=\;
  \Theta(v_1 \cdot v_2)
  \,.
$$

=--



+-- {: .num_prop #EmbeddingTensorViaSuperLieAlgebraInducedFromVectorSpace}
###### Proposition
**([[embedding tensors]] are square-0 elements in $MultEnd(V)$)**

Let $k$ be a [[ground field]] of [[characteristic zero]].

An element in degree -1 of the [[super Lie algebra]] $MultEnd(V)$ from Def. \ref{TheSuperLieAlgebraInducedFromVectorSpace}, 

$$
  \Theta \in MultEnd(V)_{-1} \simeq Hom_{k}(V, \mathfrak{gl}(V))
  \,,
$$

which by Example \ref{LieBracketOnglInsideSuperLieAlgebraInducedFromVectorSpace} is identified with a [[linear map]] 

$$
  \Theta \;\colon\; V \longrightarrow \mathfrak{g} \coloneqq \mathfrak{gl}(V)
$$

from $V$ to the [[general linear Lie algebra]] on $V$, is square-0 precisely if it is an _[[embedding tensor]]_ (Def. \ref{EmbeddingTensor}), in that:

$$
  [\Theta, \Theta]
  \;=\;
  0
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  [\Theta(v_1), \Theta(v_2) ]
  \;=\;
  \Theta( \rho_{\Theta(v_1)}(v_2) )
  \,.
$$

Here on the right, $[-,-]$ denotes the [[Lie bracket]] in $\mathfrak{gl}(V)$, while $\rho$ denotes the canonical [[Lie algebra action]] of $\mathfrak{gl}(V)$ on $V$.

=--

+-- {: .proof}
###### Proof

By unwinding of the definition (eq:SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace) and (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) and using again Example \ref{LieBracketOnglInsideSuperLieAlgebraInducedFromVectorSpace} we compute as follows:

$$
  \begin{aligned}
    \big( \tfrac{1}{2} [\Theta,\Theta](v_1) \big)(v_2)
    & =
    [\Theta, \Theta(v_1)](v_2)
    \\
    & =
    [\Theta, 
      \underset{
        \mathclap{
          = \rho_{\Theta(v_1)}(v_2)   
        }
      }
      {
        \underbrace{
          (\Theta(v_1))(v_2)
        }
      }
    ] 
    - 
    [\Theta(v_1), \Theta(v_2)]
    \\
    & =
    \Theta( \rho_{\Theta(v_1)}(v_2) )
    -
    [ \Theta(v_1), \Theta(v_2) ]
  \end{aligned}
$$


=--

#### Tensor hierarchies

+-- {: .num_prop #EmbeddingTensorsInduceTensorHierarchies}
###### Remark
**([[embedding tensors]] induce [[tensor hierarchies]])**

In view of the relation between [[super Lie algebras]] and [[dg-Lie algebras]] ([above](#RelationToDGLieAlgebras)), Prop. \ref{EmbeddingTensorViaSuperLieAlgebraInducedFromVectorSpace} says that every choice of an [[embedding tensor]] for a [[faithful representation]] on a [[vector space]] $V$ induces a [[dg-Lie algebra]] 
$(MultEnd(V), [-,-], \partial \coloneqq [\Theta, -])$.

According to [Palmkvist 13, 3.1](tensor+hierarchy#Palmkvist13), [Lavau-Palmkvist 19, 2.4](tensor+hierarchy#LavauPalmkvist19) this [[dg-Lie algebra]] (or some extension of some sub-algebra of it) is the _[[tensor hierarchy]]_ associated with the embedding tensor.

=--



[[!redirects embedding tensors and tensor hierarchy in super Lie theory -- references]]




