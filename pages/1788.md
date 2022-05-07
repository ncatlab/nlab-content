
#Contents#
* table of contents
{:toc}

The following assumes some familiarity with the ingredients and notation at *[[Cayley distance kernel]]*. Will make a more comprehensive lead-in later.

## The algebra

We regard the [[linear span]] $\mathbb{C}[Sym(n)]$ as equipped with the [[sesquilinear form]] given by

$$
  (a_1 \sigma_1, a_2 \sigma_2)
  \;\coloneqq\;
  \bar a_1 
  \,
   a_2
  \,
  \delta_{\sigma_1, \sigma_2}
  \,,
  \;\;\;\;\;
  for \; a_1, a_2 \in \mathbb{C}, \; \sigma_1, \sigma_2 \in Sym(n)
  \,.
$$

We regard any [[linear map|linear]] [[endomorphism]] $\phi$ on the [[linear span]] $\mathbb{C}[Sym(n)]$ as a [[matrix]] $[\phi]$ with respect to the canonical [[linear basis]] 

$$
  [\phi]_{\sigma_1, \sigma_2}
  \;\coloneqq\;
  \big(
    \sigma_1, \phi(\sigma_2)
  \big)
  \,.
$$

We denote [[matrix multiplication]] by "$\cdot$", so that 

$$
  [ \phi_2 \circ \phi_1 ]
  \;=\;
  [\phi_2]
  \cdot
  [\phi_1]
  \,.
$$

Next, with $\mathbb{C}[Sym(n)]$ regarded as the [[group algebra]],
we will write the algebra product as $\bullet$. 

This way, for $A_1, A_2 \in \mathbb{C}[Sym(n)]$ and with any element of the group algebra conflated with the endomorphism of left multiplication by this element, we have

$$
  [ A \bullet B]
  \;=\;
  [A] \cdot [B]
$$

Notice that in this notation 

$$
  A \;=\; A \bullet e \;=\; [A] \cdot e
  \,,
$$

reflecting that $e \in \mathbb{C}[Sym(n)]$ is a [[cyclic vector]].



Finally, we consider $\mathbb{C}[Sym(n)]$ as a complex [[star-algebra]] via

$$
  (a \, \sigma)^\ast \;=\; \bar a \, \sigma^{-1}
  \,.
$$

Noticing

$$
  \big(
    [A^\ast] \cdot [\sigma_1]
    ,\,
    [\sigma_2]
  \big)
  \;=\;
  a_{ \sigma_1 \sigma_2^{-1} }
  \;=\;
  \big(
    [\sigma_1]
    ,\,
    [A]\cdot [\sigma_2]
  \big)
$$

we see that 

$$
  [A]^\dagger \;=\; \big[ A^\ast \big]
$$

and so that 

$$  
  \mathbb{C}[Sym(n)] 
    \overset{ [-] }{\longrightarrow}
  Mat(n! \times n!, \mathbb{C})
$$

is a homomorphism of complex star-algebras.

\linebreak

## The state

For 

$$
  e^\beta \in \{1,2, \cdots, n-1\} \cup \mathbb{R}_{\gt n-1}
$$ 

a [[state on a star-algebra|state]] on this algebra is given by sending any 

$$
  A \;=\; \underset{\sigma \in Sym(n)}{\sum} a_\sigma \sigma
$$ 

to

$$
  \big\langle
    A
  \big\rangle_{\beta}
  \;\coloneqq\;
  \big(
    e,
    [e^{-\beta \cdot d_C}] 
    \cdot 
    A
  \big)
  \;\coloneqq\;
  \underset{ 
    \sigma \in Sym(n) 
  }{\sum} 
  a_\sigma 
  \cdot
  e^{ -\beta \cdot d_C(e, \sigma ) }
  \;=\;
  e^{- \beta \cdot n}
  \underset{ 
    \sigma \in Sym(n) 
  }{\sum} 
  a_\sigma 
  \cdot
  e^{ \beta \cdot \# cycles(\sigma) }
  \,.
$$

This is indeed a state, because 

$$
  \begin{aligned}
  \big\langle
    A^\ast \bullet A
  \big\rangle_{\beta}
  & \;\coloneqq\;
  \Big(  
    e,
    \big[ e^{-\beta \cdot d_C} \big] 
      \cdot 
    (A^\ast \bullet A )
  \Big)
  \\
  &
  \;\coloneqq\;
  \underset{ 
    \sigma_1, \sigma_2 \in Sym(n) 
  }{\sum} 
  \bar a _{\sigma_1}
  a_{\sigma_2}
  \cdot
  e^{ -\beta \cdot d_C(e, \sigma_1^{-1} \sigma_2 ) }
  \\
  & \;=\;
  \underset{ 
    \sigma_1, \sigma_2 \in Sym(n) 
  }{\sum} 
  \bar a _{\sigma_1}
  a_{\sigma_2}
  \cdot
  e^{ -\beta \cdot d_C(\sigma_1,  \sigma_2 ) }
  \\
  & \;=\;
  \Big(
    A,
    \,
    [e^{- \beta \cdot d_C}] \cdot A
  \Big)
  \\
  & \;\geq \; 0 
  \end{aligned}
$$

by left-invariance and by positive (semi-)definity of the Cayley distance kernel at the given $\beta$.

\linebreak

## The invariant subspaces

Regarding $\mathbb{C}[Sym(n)]$ as the [[regular representation]] of $Sym(n)$ it [decomposes into irreps](regular+representation#RegularRepDecomposedIntoIrreps) ([[Specht modules]]) $S^{(\lambda)}$ with multiplicity their dimension.

For $\lambda \in Part(n)$ write

$$
  P^{(\lambda)}
  \;\colon\;
  \mathbb{C}[Sym(n)]
  \longrightarrow
  \mathbb{C}[Sym(n)]
$$

for the linear projection onto the linear span of

$$
  \left\{
    \underset{ \sigma \in Sym(n) }{\sum}
    \bar S^{(\lambda)}_{i j}(\sigma) \sigma
    \;\in\;
    \mathbb{C}[Sym(n)]
  \right\}
    _{ 1 \leq i,j \leq dim(S^{(\lambda)}) }
  \,.
$$


Thus

$$
  \underset{
    \lambda \in Part(n)
  }{ \sum }
  P^{(\lambda)}
  \;=\;
  id
  \,.
$$

Notice that each $P^{(\lambda)}\big( \mathbb{C}[Sym(n)]  \big)$ is a left ideal of the group algebra:


$$
  \begin{aligned}
  \sigma' 
    \;\bullet\;
  \underset{
    \sigma \in Part(n)
  }{\sum}
  \bar S^{(\lambda)}(\sigma)_{i j}
  \,
  \sigma
  & \;=\;
  \underset{
    \sigma \in Part(n)
  }{\sum}
  \bar S^{(\lambda)}(\sigma)_{i j}  
  \,
  \sigma' \bullet \sigma
  \\
  & =
  \underset{
    \sigma \in Part(n)
  }{\sum}
  \bar S^{(\lambda)}( (\sigma')^{-1} \sigma)_{i j}  
  \,
  \sigma
  \\
  & \;=\;
  \underset{
    \sigma \in Part(n)
  }{\sum}
  \underset{ 1 \leq k \leq dim(S^{(\lambda)}) }{\sum}
  S^{(\lambda)}( \sigma' )_{i k}  
  \bar S^{(\lambda)}( \sigma)_{k j}  
  \,
  \sigma
  \\
  & \;=\;
  \underset{ 
    1 \leq k \leq dim(S^{(\lambda)}) 
  }{\sum}
  S^{(\lambda)}( \sigma' )_{i k}  
  \underset{
    \sigma \in Part(n)
  }{\sum}
  \bar S^{(\lambda)}( \sigma)_{k j}  
  \,
  \sigma
  \end{aligned}
$$

Hence 

$$
  \mathbb{C}[Sym(n)]
  \;\simeq\;  
  \underset{
    { \lambda \in Part(n) }
  }{\oplus}
  P^{(\lambda)}\big( \mathbb{C}[Sym(n)]  \big)
$$

is a decomposition into left ideals.

This implies that for all $A \in \mathbb{C}[Sym(n)]$ we have

$$
  [P^{(\lambda)}] \cdot [A]
  \;=\;
  [A] \cdot [P^{(\lambda)}]
$$

Moreover, we have 

$$
  [e^{- \beta \cdot d_C}] 
    \cdot 
  [P^{(\lambda)}]
  \;=\;
  [P^{(\lambda)}]
    \cdot
  [e^{- \beta \cdot d_C}] 
$$

by the fact that the $\underset{ \sigma }{ \sum } \bar S^{(\lambda)}(\sigma) \, \sigma $ are eigenvectors of the Cayley distance kernel.

Finally, we have

$$
  \left(  
    P^{(\lambda)}( \bar S^{(\lambda_1)}_{i_1, j_1} ),
    \,
    \bar S^{(\lambda_2)}_{i_2, j_2} 
  \right)
  \;=\;
  \left(  
    \bar S^{(\lambda_1)}_{i_1, j_1},
    \,
    P^{(\lambda)}
    (
    \bar S^{(\lambda_2)}_{i_2, j_2} 
    )
  \right)  
$$

hence $[P^{(\lambda)}]^\dagger = [P^{(\lambda)}]$ (by grand Schur orthogonality, see [this Prop.](Cayley+distance+kernel#DualEigenvectorBasis)).


## The mixture

Using the above properties of the projectors $[P^{(\lambda)}]$, we observe that each

$$
  \big\langle
    -
  \big\rangle_{\beta, \lambda}
  \;\coloneqq\;
  \frac{1}{ 
    \big\langle  P^{(\lambda)}(e) \big\rangle_\beta
  }
  \,
  \big\langle 
    P^{(\lambda)}(-)
  \big\rangle_\beta
$$

is still a [[state on a star-algebra|state]]:

$$
  \begin{aligned}
    \big\langle 
      P^{(\lambda)}( A^\ast \bullet A)
    \big\rangle_\beta  
    & \;=\;
    \big(
      e
      ,\,
      [e^{- \beta \cdot d_C}]
        \cdot
      [P^{(\lambda)}] 
        \cdot 
      [A]^\dagger 
        \cdot 
      [A]
      \cdot
      e
    \big)
    \\
    & \;=\;
    \big(
      e
      ,\,
      [e^{- \beta \cdot d_C}]
        \cdot
      [P^{(\lambda)}] 
        \cdot
      [P^{(\lambda)}] 
        \cdot 
      [A]^\dagger 
        \cdot 
      [A]
      \cdot
      e
    \big)
    \\
    & \;=\;
    \big(
      e
      ,\,
      [P^{(\lambda)}] 
        \cdot
      [e^{- \beta \cdot d_C}]
        \cdot
      [A]^\dagger 
        \cdot 
      [P^{(\lambda)}] 
        \cdot
      [A]
        \cdot
      e
    \big)
    \\
    & \;=\;
    \big(
      P^{(\lambda)}(A)
      ,\,
      [e^{- \beta \cdot d_C}]
        \cdot 
      P^{(\lambda)}(A)
    \big)
    \\
    & \;\geq\; 0
  \end{aligned}
$$

It follows that we have decomposed our state into a [[convex combination]] of other states as follows:

\[
  \label{TheConvexCombination}
  \big\langle    
     -
  \big\rangle_\beta
  \;=\;
  \underset{ \lambda \in Part(n) }{ \sum }
  p_\lambda
  \cdot
  \big\langle    
     -
  \big\rangle_{\beta, \lambda}
  \,,
\]

where

$$
  p_\lambda
  \;\coloneqq\;
  \big\langle  P^{(\lambda)}(e) \big\rangle_\beta
  \,.
$$


**Conjecture**. The $\langle  - \rangle_{\beta, \lambda}$
are [[pure states]].

If so, then (eq:TheConvexCombination) exhibits our state as a mixture in which the $\lambda$th pure state appears with probability $p_\lambda$.

