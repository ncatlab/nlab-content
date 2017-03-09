

Let $C$ be a [[cocommutative coalgebra]] augmented over a field $k$ with maximal coideal $C_+$. 

Write

$$
 C_+^1 \coloneqq (C_+ \hookrightarrow C)
$$

and given for $n \geq 1$ an inclusion

$$
  C_+^n 
    \hookrightarrow 
  C_+
   \otimes 
  \underset{n-1}{\underbrace{
    C \otimes \cdots \otimes C
  }}
$$

inductively define $C_+^{n+1}$ to be the image of

$$
 ...
$$

such that the filtration

$$
  C
  \longrightarrow
  C_+
  \longrightarrow
  C_+^2
  \longrightarrow
  C_+^3
  \longrightarrow
  \cdots
$$

is an exhaustive Hausdorff filtration ([def.](filtered+object#ExhaustiveHausdorffAndCompleteFiltrations)).

***


Let $A$ be a $k$-algebra with a maximal ideal $n_A$ such that the filtration

$$
  \cdots
    \hookrightarrow
  (n_A)^3
    \hookrightarrow
  (n_A)^2
    \hookrightarrow
  n_A
    \hookrightarrow 
  (n_A)^0 
    \coloneqq 
  A
$$

is an exhaustive Hausdorff filtration ([def.](filtered+object#ExhaustiveHausdorffAndCompleteFiltrations)), i.e. such that

1. $\underset{\longrightarrow}{\lim}_i (n_A)^i = A$ (this is trivially so)

1. $\underset{\longleftarrow}{\lim}_i (n_A)^i = 0$ (this is the actual condition).

Claim: Every [[projective module]] over $A$ is a [[free module]].

Proof:

Choose a splitting of the projection $N \to N/ n_A N$ at the level of $k$-vector spaces:

$$
  N 
    \;\simeq_k\;
  V \;\oplus \; n_A N 
  \,.
$$

Notice that by iteration this means that

$$
  \begin{aligned}
    N 
      & \simeq
    V \oplus n_A N
    \\
     & \simeq
    V \oplus n_A V + (n_A)^2 N
    \\
     & \simeq
    V \oplus n_A V + (n_A)^2 V + (n_A)^3 N 
    \\
     & \simeq
    \cdots
  \end{aligned}
$$

and so on. But due to the inclusions $(n_A)^{t+1} \hookrightarrow (n_A)^t$ this is in fact equal to 

$$
  \begin{aligned}
    N
      &\simeq
    V \oplus n_A N
    \\
      & \simeq
    \underset{\simeq A \oplus V}{\underbrace{ V \oplus n_A V}} + (n_A)^2 N
    \\
      & \simeq
    A \otimes V + (n_A)^3 N
    \\
    & \simeq
    A \otimes V + (n_A)^4 N
     \\
    & \simeq \cdots
  \end{aligned}
$$

Since all these are isomorphic but we want to take "$i$ to infinity" we write this as

$$
  \begin{aligned}
    N 
      &\simeq
    \underset{\longleftarrow}{\lim}_i 
    \left(
      A \otimes V + (n_A)^i N
    \right)
    \\
    & \simeq
    A \otimes V + \underset{\longleftarrow}{\lim}\left( (n_A)^i N \right)
 \end{aligned}
  \,.
$$

Now use that $N$ is projective, which means that it is a direct summand of a free module, $N \hookrightarrow A \otimes W$ . This implies that the images $(n_A)^i N$ may equivalently be computed in $A \otimes W$, and there, due to freeness, the limit may be computed in the algebra: 



$$
  \begin{aligned}
    \underset{\longleftarrow}{\lim}_i \left(  (n_A)^i N \right)
    & \simeq
    \underset{\simeq 0}{\underbrace{\left(\underset{\longleftarrow}{\lim}_i (n_A)^i\right) }} N
  \end{aligned}
$$ 

But by assumption that $\left((n_A)^i\right)_i$ is a Hausdorff filtration on $A$, the limit on the right vanishes, as indicated.

In conclusion, we have an $A$-module homomorphism from the [[free module]] on $V$ to $N$

$$
  A \otimes V \longrightarrow N
$$

given by

$$
  (a,v) \mapsto a v
$$

and by the previous argument this is an isomorphism on the underlying vector spaces. Therefore it is an isomorphism of $A$-modules.

