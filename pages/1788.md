

\linebreak


### As the $2(n+n')$-form component of the Chern character on cofiber space
  {#AsThe2nFormComponentOfTheChernCharacterOnCofiberSpaces}

(...) under construction (...)

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

The [[eigenvectors]] to this operation over the [[rational numbers]] would be:

$$
  \psi^k_{\mathbb{Q}} 
    \;\;\colon\;\; 
  \left\{
  \array{
     \big(
       V_{2 n} 
       -
       e(f)
       \cdot
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
       V_{2 n} 
       -
       e(f)
       \cdot
       V_{2(n + n')}
     \big) 
     \\
     V_{2(n+n')} 
     &
       \mapsto
     & 
       k^{n + n'} 
     &
       \cdot 
     & 
      V_{2 (n + n')}
   }
  \right.
$$


Since the [[Adams operations are compatible with the Chern character]], this means equivalently that under the [[Chern character]] map $ch$ we have in [[ordinary cohomology|ordinary]] [[rational cohomology]]:

$$
  \psi^k_H 
    \;\;\colon\;\; 
  \left\{
  \array{
     ch
     \big(
       V_{2 n} 
       -
       e(f)
       \cdot
       V_{2(n + n')}
     \big) 
     &
       \mapsto
     & 
       k^{n } 
     &
       \cdot 
     & 
     ch
     \big(
       V_{2 n} 
       -
       e(f)
       \cdot
       V_{2(n + n')}
     \big) 
     \\
     ch
     \big(
       V_{2(n+n')} 
     \big)
     &
       \mapsto
     & 
       k^{n + n'} 
     &
       \cdot 
     & 
     ch
     \big(
        V_{2 (n + n')}
     \big)
   }
  \right.
  \;\;\;\;
  \in
  \;
  H^{ev}\big( C_f; \, \mathbb{Q} \big)
$$

But since the [[eigenvectors]] of $\psi^k_H $ to [[eigenvalue]] $k^r$ are precisely the classes in $H^{2r}\big( C_f;\, \mathbb{Q} \big) \,\subset\, H^{ev}\big( C_f;\, \mathbb{Q} \big)$ (see [there](Adams+operations+compatible+with+the+Chern+character#eq:AdamsOperationOnOrdinaryCohomologyInDegree2r)), this means that

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
          - 
          e(f)
          \cdot
          V_{2(n+n')}
       \big)
    }
  }
  \;+\;
  \underset{
    \in \; H^{2(n + n')}\big( C_f; \, \mathbb{Q} \big)
  }{
    \underbrace{
       ch
       \big(
          e(f)
          \cdot
          V_{2(n+n')}
       \big)
    }
  }
$$

Hence we find that the e-invariant measures equivalently the rational offset of the degree-$2(n+n')$-component of the Chern character of the choice of lift of the generator $V_{2n} \,\in\, \widetilde K(S^{2n})$ to $ \widetilde K(C_f)$

(...)

