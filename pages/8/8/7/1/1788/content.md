
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
    0 & k^{n + n'}
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
$$

$$
  k^n a + e(f) k^n(k^{n'}-1) = k^{n + n'} a
$$

$$
  a 
  = 
  e(f)
$$

$$
  ch\big( 
    V_{2(n + n')} 
  \big)
  =
  -
  e(f)
  \cdot
  \underset{
    \in \, H^{2n}(C_f;\, \mathbb{Q})
  }{
    \underbrace{
    \mathclap{\phantom{\Big(}}
    ch\big(
      V_{2 n}
    \big)
    \mathclap{\phantom{\Big)}}
    }
  }
  +
  \underset{
    \in \, H^{2(n + n')}(C_f;\, \mathbb{Q})
  }{
  \underbrace{
  \Big(
    e(f)
    \cdot
    ch\big( 
      V_{2 n}
    \big) 
    + 
    ch\big(
      V_{2(n + n')}
    \big)
  \Big)
  }
  }
$$


\linebreak

\linebreak

+-- {: .num_defn #AbelianGroupWithAdamsOperations} 
###### Definition
**(abelian group with Adams operations)**

We say that an _abelian group with Adams operation_ $\big(A,\{\psi_A^k\}_{k \in \mathbb{N}}\big)$ is an [[abelian group]] $A$ equipped with an [[action]] of the [[multiplicative group|multiplicative]] [[monoid]] $(\mathbb{N}, \cdot)$ of [[natural numbers]], hence equipped with [[group homomorphism]]

$$
  \psi_A^k \;\colon\; A \to A
  \,,
  \;\;\;
  k \in \mathbb{N}
$$

such that 

$$
  \psi_A^{k_1}
  \circ
  \psi_A^{k_2}
  \;=\;
  \psi_A^{ k_1 \cdot k_2 }
  \,,
  \;\;\;\;\;\;\;\;\;
  \text{for all}
  \,
  k_1, k_2 \,\in\, \mathbb{N}
  \,.
$$

Moreover, for $\big(A,\{\psi_A^k\}_{k \in \mathbb{N}}\big), \, \big(A',\{\psi_{A'}^k\}_{k \in \mathbb{N}}\big)$ two abelian groups with Adams operations, a [[homomorphism]] between them is a [[group homomorphism]] (a [[linear map]]) $\phi \;\colon\; A \to A'$ which respect these operations, hence such that the following [[commuting square|squares commute]]:

$$
  \array{
    A &\overset{\;\;\;\phi\;\;\;}{\longrightarrow}& A'
    \\
    {}^{\mathllap{ \psi^k_A }}  
    \big\downarrow 
    && 
    \big\downarrow
    {}^{\mathrlap{\psi_{A'}^k}}
    \\
    A &\overset{\;\;\;\phi\;\;\;}{\longrightarrow}& A'
    \,,
  }
  \;\;\;\;\;\;\;\;
  \text{for all}
  \;
  k \in \mathbb{N}
  \,.
$$


=--

+-- {: .num_example} 
###### Example

For $X$ a [[compact topological space]], the  [[complex topological K-theory]] [[cohomology group|group]] $K(X)$ becomes an abelian group with Adams operations in the sense of Def. \ref{AbelianGroupWithAdamsOperations}, via the actual [[Adams operations]], hence so does the [[reduced K-theory]] $\widetilde K(X)$:

$$
  \array{
    \widetilde K(X)
    &\overset{\;\;ker(i^\ast)\;\;}{\longrightarrow}&
    K(X)
    &\overset{\;i^\ast\;}{\longrightarrow}&
    K(\ast)
    \\
    \big\downarrow
    {}^{\mathrlap{\psi^k_{\widetilde K(X)}}}
    &&
    \big\downarrow
    {}^{\mathrlap{\psi^k_{K(X)}}}
    &&
    \big\downarrow
    {}^{\mathrlap{\psi^k_{K(\ast)}}}
    \\
    \widetilde K(X)
    &\underset{\;\;ker(i^\ast)\;\;}{\longrightarrow}&
    K(X)
    &\underset{\;i^\ast\;}{\longrightarrow}&
    K(\ast)
  }
$$

(...)

=--


Throughout, we write $\widetilde K(-) \,\coloneqq\, \widetilde KU^0(-)$ for the [[reduced cohomology|reduced]] [[complex topological K-theory]]-[[cohomology groups|groups]], regarded as ahelian groups with Adams operations.

llll