

\linebreak


### As the $2(n+n')$-form component of the Chern character on cofiber space
  {#AsThe2nFormComponentOfTheChernCharacterOnCofiberSpaces}

(...) under construction (...)


+-- {: .num_prop } 
###### Proposition

In the situation of ... we have that the [[e-invariant]] $e(f)$ is equivalently the evaluation [[modulo]] [[integers]] of the [[Chern character]] $ch(V_{2n}) \,\in\,  H^{ev}\big( C_f;\, \mathbb{Q}  \big)$ of any element $V_{2n} \in \widetilde K\big( C_f \big)$ (lifting the generator $\Sigma^{2n}1 \,\in\, \widetilde K\big( S^{2n} \big)$) on the [[fundamental class]] of $C_f$:

$$
  \exp
  \left(
    2 \pi \mathrm{i}
    \int_{C_f}
      ch\big( V_{2n} \big)
  \right)
  \;=\;
  \exp
  \left(
    2 \pi \mathrm{i}
    \,
    {
      \color{blue}
      e(f)
    }
  \right)
  \;\;\;
  \in 
  \mathrm{U}(1)
$$

=--

+-- {: .proof}
###### Proof

By (eq:ActionOfAdamsOperationsOnCofiberSpace) we have,
now in [[matrix calculus]]-notation:

$$
  \psi^k
  \;\colon\;
  \left[
  \array{
    V_{2 n }
    \\
    V_{2(n + n')}
  }
  \right]
  \;\;\;
  \mapsto
  \;\;\;
  \left[
  \array{
    k^n
    & 
    e(f) \, k^n (k^{n'} - 1)
    \\
    0
    & 
    k^{n + n'}
  }
  \right]
  \cdot
  \left[
  \array{
    V_{2 n }
    \\
    V_{2(n + n')}
  }
  \right]
  \;\;\;\;\;
  \in
  \;
  \widetilde K\big( C_f \big)
  \,.
$$

This [[matrix]] has two [[eigenvectors]] over the [[rational numbers]] (in general). Therefore we now consider the image of these K-theory classes under the [[Chern character]] map

$$
  ch 
    \;\colon\; 
  \widetilde K\big( C_f \big) 
    \longrightarrow 
  H^{ev}\big( C_f;\, \mathbb{Q}\big)
  \,.
$$

Since the [[Adams operations are compatible with the Chern character]], we have the following [[eigenvectors]] of the [[Adams operations]] under $ch$:

\[
  \label{EigenvectorsOfAdamsOperationsAfterPassageThroughChernCharacter}
  \psi^k_H 
    \;\;\colon\;\; 
  \left\{
  \array{
     ch
     \big(
       V_{2 n} 
     \big)
     -
     e(f)
     \cdot
     ch
     \big(
       V_{2(n + n')}
     \big) 
     &
       \mapsto
     & 
       k^{n } 
     &
       \cdot 
     & 
     \big(
     ch
     (
       V_{2 n} 
     )
     -
     e(f)
     \cdot
     ch
     (
       V_{2(n + n')}
     ) 
     \big)
     \\
     ch
     (
       V_{2(n+n')} 
     )
     &
       \mapsto
     & 
       k^{n + n'} 
     &
       \cdot 
     & 
     ch
     (
        V_{2 (n + n')}
     )
   }
  \right.
  \;\;\;\;
  \in
  \;
  H^{ev}\big( C_f; \, \mathbb{Q} \big)/H^{2(n+n')}\big( C_f; \, \mathbb{Z} \big)
  \,.
\]

Here, since $V_{2n}$ is well defined modulo addition of integral multiples of $V_{2(n+n')}$, and since 

\[
  \label{ChernCharacterOnCofiverSpaceOfGeneratorofTopCell}
  ch\big( V_{2(n+n')} \big)
  \;=\;
  1 
  \,\in\,
  \mathbb{Z}
  \,\simeq\,
  H^{2(n+n')}\big( C_f \big)
  \,,
\]

this expression (eq:EigenvectorsOfAdamsOperationsAfterPassageThroughChernCharacter) is well-defined in [[ordinary cohomology|ordinary]] [[rational cohomology]] in even degrees [[modulo]] [[integral cohomology]] in top degree, 

But since the [[eigenvectors]] of $\psi^k_H $ to [[eigenvalue]] $k^r$ are precisely the ordinary cohomology classes in homogeneous degree $H^{2r}\big( C_f;\, \mathbb{Q} \big) \,\subset\, H^{ev}\big( C_f;\, \mathbb{Q} \big)$ (see [there](Adams+operations+compatible+with+the+Chern+character#eq:AdamsOperationOnOrdinaryCohomologyInDegree2r)), this means that

$$
  ch
  \big(
    V_{2n}
  \big)
  \;\;=\;\;
  \underset{
    \in \; H^{2n}\big( C_f; \, \mathbb{Q} \big)
  }{
    \underbrace{
       ch
       \big(
         V_{2n} 
       \big)
       - 
       e(f)
       \cdot
       ch
       \big(
         V_{2(n+n')}
       \big)
    }
  }
  \;+\;
  \underset{
    \in \; H^{2(n + n')}\big( C_f; \, \mathbb{Q}/\mathbb{Z} \big)
  }{
    \underbrace{
       e(f)
       \cdot
       ch
       \big(
         V_{2(n+n')}
       \big)
    }
  }
$$

The evaluation of this cohomology class on the [[fundamental class]] of $C_f$ picks out the [[coefficient]] of $e(f)$, by (eq:ChernCharacterOnCofiverSpaceOfGeneratorofTopCell):

$$
  \int_{C_f}
  ch
  \big(
    V_{2n}
  \big)
  \;=\;
  e(f)
  \;\;\;
  \in
  \;
  \mathbb{Q}/\mathbb{Z}
$$

and hence the claim follows.

=--

$$
  \cdots
  \to
  Maps(X,B^n \mathbb{Z})
  \longrightarrow
  Maps(X,B^n \mathbb{Q})
  \longrightarrow
  Maps(X,B^n \mathbb{Q}/\mathbb{Z})
  \longrightarrow
  Maps(X,B^{n+1} \mathbb{Z})
  \longrightarrow
  Maps(X,B^{n+1} \mathbb{Q})
  \to \cdots
$$

$$
  \cdots
  \to
  H^n(X; \mathbb{Z})
  \longrightarrow
  H^n(X; \mathbb{Q})
  \longrightarrow
  H^n(X; \mathbb{Q}/\mathbb{Z})
  \longrightarrow
  H^{n+1}(X; \mathbb{Z})
  \longrightarrow
  H^{n+1}(X; \mathbb{Q})
  \to 
  \cdots
$$

$$
  0 \to
  H^n(X; \mathbb{Q})
  /
  H^n(X; \mathbb{Z})
  \longrightarrow
  H^n(X; \mathbb{Q}/\mathbb{Z})
  \longrightarrow
  H^{n+1}(X; \mathbb{Z})
  \longrightarrow
  H^{n+1}(X; \mathbb{Q})
$$

