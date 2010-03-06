Suppose $V$, $W$ are finite-dimensional vector spaces over a field, with dimensions $m$ and $n$, respectively. For any space $A$ let $L(A)$ denote the space of linear operators on $A$. The partial trace over $W$, Tr$_{W}$, is a mapping

$$
  T \in L(V \otimes W) \mapsto Tr_{W}(T) \in L(V).
$$

+-- {: .un_defn}
###### Definition
Let $e_{1}, \ldots, e_{m}$ and $f_{1}, \ldots, f_{n}$ be bases for $V$ and $W$ respectively.  Then $T$ has a matrix representation $\{a_{kl,ij}\}$ where $1 \le k,i \le m$ and $1 \le l,j \le n$ relative to the basis of the space $V \otimes W$ given by $e_{k} \otimes f_{l}$.  Consider the sum

$$
  b_{k,i} = \sum_{j=1}^{n}a_{kj,ij}
$$

for $k,i$ over $1, \ldots, m$.  This gives the matrix $b_{k,i}$.  The associated linear operator on $V$ is independent of the choice of bases and is defined as the partial trace.
=--

# Example

Consider a quantum system, $\rho$, in the presence of an environment, $\rho_{env}$.  Consider what is known in [[quantum information theory]] as the CNOT gate:

$$
  U=|00\rangle\langle 00|+|01\rangle\langle 01|+|11\rangle\langle 10|+|10\rangle\langle 11|.
$$

Suppose our system has the simple state $|1\rangle\langle 1|$ and the environment has the simple state $|0\rangle\langle 0|$.  Then $\rho \otimes \rho_{env} = |10\rangle\langle 10|$.  In the quantum operation formalism we have

$$
  T(\rho) = \frac{1}{2}Tr_{env}U(\rho \otimes \rho_{env})U^{\dagger}
          = \frac{1}{2}Tr_{env}(|10\rangle\langle 10|+|11\rangle\langle 11|)
          = \frac{|1\rangle\langle 1|\langle 0|0\rangle + |1\rangle\langle 1|\langle 1|1\rangle}{2}
          = |1\rangle\langle 1|
$$

where we inserted the normalization factor $\frac{1}{2}$.