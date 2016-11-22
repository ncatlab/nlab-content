We outline key steps of the proof of theorem \ref{TheTheorem}, given in [Deligne 02](#Deligne02).

> under construction

Throughout, let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).


The proof proceeds in three main steps:

1. **Proposition \ref{LengthOfObjectIsBounded}** states that in a $k$-[[tensor category]] an object $X$ is of subexponential growth (def. \ref{SubexponentialGrowth}) precisely if their exists a [[Schur functor]] that annihilates it, hence if some power of $X$, skew-symmetrized in sme variables and symmetrized in others, vanishes. 

   This proposition is where the [[symmetric group]] and its [[permutation]] [[action]] on [[tensor powers]] appears, from just a kind of finite-dimensionality assumption.

1. **Proposition \ref{SchurFinitenessImpliesExistenceOfSuperFiberFunctor}** in turn says that if every object in $\mathcal{A}$ is annihilated by some [[Schur functor]], then there exists a super [[fiber functor]] on $\mathcal{A}$ over some [[supercommutative superalgebra]] $R$, hence then every object of $\mathcal{A}$ has underlying it a [[super vector space]] with some extra structure.

   This proposition is where [[superalgebra]] proper appears.

1. spring

+-- {: .num_prop #LengthOfObjectIsBounded}
###### Proposition

For $\mathcal{A}$ a $k$-[[tensor category]] (def. \ref{TensorCategory}), then the following are equivalent:

1. the category $\mathcal{A}$ has subexponential growth (def. \ref{SubexponentialGrowth});

1. for every object $X \in \mathcal{A}$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, on $X$ vanishes: $S_\lambda(X) = 0$. 

=--

([Deligne 02, prop. 05](#Deligne02))


+-- {: .num_prop #SchurFinitenessImpliesExistenceOfSuperFiberFunctor} 
###### Proposition

If for every object of a $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) there exists a [[Schur functor]] (def. \ref{SchurFunctor}) that annihilates it, then there exists a [[fiber functor|super fiber functor]] (def. \ref{FiberFunctor}) over $k$:

$$
  \omega 
    \;\colon\; 
  \mathcal{A}
    \longrightarrow
  sVect
  \,.
$$

=--

([Deligne 02, prop. 2.1 "r&#233;sultat cl&#233; de l'article", together with prop. 4.5](#Deligne02)) 

+-- {: .proof}
###### Proof idea 

First ([Deligne 02, middle of p. 16](#Deligne02)) consider the [[tensor category]]

$$
  s \mathcal{A}
    \coloneqq
  (\mathcal{A}^{\mathbb{Z}/2}, \tau_{super} )
$$

which is that of $\mathbb{Z}/2$-graded objects of $\mathcal{A}$, and whose [[braiding]] is given on objects $X,Y$ of homogeneous degree by that of $\mathcal{A}$ multiplied with $(-1)^{deg(X) deg(Y)}$.

Write $1$ and $\overline{1}$ for the [[tensor unit]] of $\mathcal{A}$, regarded in even degree and in odd degree in $s \mathcal{A}$, respectively. 

For $A \in CMon(\mathcal{A})$ a [[commutative monoid]], write

$$
  \mathcal{A}
  \simeq 
  1 Mod(\mathcal{A})
     \underoverset{\underset{U}{\longleftarrow}}{\overset{(-)_A \coloneqq F}{\longrightarrow}}
 {}
  A Mod(\mathcal{A})
$$

for the [[extension of scalars]] operation $A \otimes(-)$, [[left adjoint]] to [[restriction of scalars]]. (The [[free module]] construction from prop. \ref{MonoidModuleOverItself}).

Show then that the condition that an object $X$ is annihilated by some [[Schur functor]] is equivalent to the existence of an algebra $A$ such that 

$$
  X_A \simeq 1^p \oplus \overline{1}^q
$$

for some $p,q \in \mathbb{N}$, hence that each such object is _$A$-locally_ a [[super vector space]].

([Deligne 02, prop. 2.9](#Deligne02)).

Moreover, for each [[short exact sequence]] 

$$
  0 \to X \to Y \to Z \to 0
$$

in $s \mathcal{A}$, there exists an algebra $A$ such that 

$$
  0 \to X_A \to Y_A \to Z_A \to 0
$$

is a [[split exact sequence]], (hence every short exact sequence is _locally_ split).

([Deligne 90, 7.14](#Deligne90), [Deligne 02, rappel 2.10](#Deligne 02))

Now ([Deligne 02, middle of p. 17](Deligne02)) let $A$ be the commutative monoid which is the [[tensor product]] of commutative monoids (example \ref{TensorProductOfTwoCommutativeMonoids}) over all [[isomorphism classes]] of [[objects]] and of [[short exact sequences]] in $\mathcal{A}$ of choices of commutative monoids for which these objects/exact sequencs are locally split, as above.

Then for an $A$-module $N$, write $\rho(N)$ for the [[subobject]] of $N$ inside $sVect \simeq Ind\langle 1, \overline{1}\rangle \hookrightarrow s \mathcal{A}$.

Check ([Deligne 02, bottom of p. 17](Deligne02)) that $\rho(A)$ inherits the structure of a commutative monoid, and that $\rho(N)$ inherits the structure of a module over $\rho(N)$.

Set

$$
  R \coloneqq \rho(A) 
  \,.
$$

Hence for every object $X$, then 

$$
  \omega(X)
    \coloneqq
  \rho(X_A)
$$

has the structure of an $R$-module. By $A$-local splitness of all short exact sequence, $\omega$ is an [[exact functor]].

Hence 

$$
  \omega \;\colon\; s \mathcal{A} \longrightarrow R Mod(sVect)
$$

is a super fiber functor on $s\mathcal{A}$ over $R$. This restricts to a super fiber functor over $R$ on  $\mathcal{A}$, regarded as the sub-category of even-graded objects in $s \mathcal{A}$:

$$
  \mathcal{A}
    \hookrightarrow 
  s \mathcal{A} 
   \overset{\omega}{\longrightarrow} 
  R Mod(sVect)
  \,,
$$

Finally check ([Deligne 02, prop. 4.5](#Deligne02)) that
if a $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) admits a [[fiber functor|super fiber functor]] (def. \ref{FiberFunctor}) over a [[supercommutative superalgebra]] $R$ over $k$

$$
  \mathcal{A}
    \longrightarrow
  R Mod(sVect)
$$

then it also admits a super fiber functor over $k$ itself, i.e. a fiber functor to [[sVect]]

$$
  \mathcal{A}
    \longrightarrow
  k Mod(sVect)
  \simeq
  sVect
  \,.
$$

This is argued by expressing $R$ as an [[inductive limit]] 

$$
  R = \underset{\longrightarrow}{\lim}_\beta R_\beta
$$

over [[supercommutative superalgebras]] $R_\beta$ of finite type over $k$ and observing (...) that there exists $\beta$ such that $\omega_\beta$ is still a fiber functor and such that there exists an algebra homomorphism $R_\beta \to k$. 

Finally then the fiber functor in question is

$$
  \omega_\beta \otimes_{R_\beta} k
   \;\colon\;
  \mathcal{A}
    \longrightarrow
  sVect_k
  \,.
$$

=--



