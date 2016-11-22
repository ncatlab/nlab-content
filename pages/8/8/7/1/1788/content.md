


We discuss aspects of steps of the proof of theorem \ref{TheTheorem}, given in [Deligne 02](#Deligne02)

> under construction

Throughout, let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).


The proof proceeds in three main steps:

1. Proposition \ref{LengthOfObjectIsBounded} states that in a $k$-[[tensor category]] an object $X$ being of subexponential growth is equivalent to the existence of a [[Schur functor]] that annihilates this, hence equivalent to the statement that some power of $X$, skew-symmetrized in sme variables and symmetrized in others, vaishes. 

   Hence this proposition is where the [[symmetric group]] action on tensor powers appears, from just a kind of finite-dimensionality assumption.

1. Proposition \ref{SchurFinitenessImpliesExistenceOfSuperFiberFunctor} in turn says that if every object in $\mathcal{A}$ is annihilated by some [[Schur functor]], then there exists a super [[fiber functor]] on $\mathcal{A}$ over some [[supercommutative superalgebra]] $R$, hence then every object of $\mathcal{A}$ has underlying it a [[super vector space]] with some extra structure.




+-- {: .num_prop #LengthOfObjectIsBounded}
###### Proposition

For $\mathcal{A}$ a $k$-[[tensor category]], then the following are equivalent:

1. the category $\mathcal{A}$ has subexponential growth (def. \ref{SubexponentialGrowth});

1. for every object $X \in \mathcal{A}$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, on $X$ vanishes: $S_\lambda(X) = 0$. 

=--

([Deligne 02, prop. 05](#Deligne02))


+-- {: .num_prop #SchurFinitenessImpliesExistenceOfSuperFiberFunctor} 
###### Proposition

If for every object of a $k$-[[tensor category]] $\mathcal{A}$ there exists a [[Schur functor]] that annihilates it, then there exists a [[fiber functor|super fiber functor]] (def. \ref{FiberFunctor})

$$
  \omega 
    \;\colon\; 
  \mathcal{A}
    \longrightarrow
  R Mod(sVect)
$$

over some non-null [[supercommutative superalgebra]] $R$ over $k$.

=--

([Deligne 02, prop. 2.1 "r&#233;sultat cl&#233; de l'article"](#Deligne02)) 



