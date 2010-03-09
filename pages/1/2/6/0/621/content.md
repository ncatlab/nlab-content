# Traces
* tic
{: toc}


## Definition

If $a$ is a [[dualizable object]] in a [[symmetric monoidal category]] $C$, there is a notion of the _trace_ of an [[endomorphism]] $f:a \to a$, which reproduces the ordinary notion of trace of a linear map of finite dimensional vector spaces for the case that $C = Vect$.

The idea of the trace operation is easily seen in [[string diagram]] notation: essentially one takes the endomorphism 
$a \stackrel{f}{\to} a$, "bends it around" using the duality and the symmetry and connects its output to its input.

$$
 \array{
   1 
   \\
   \;\;\;\downarrow^{tr(f)}
   \\
   1
 }
  \;\;\;
  :=
  \;\;\;
  \array{
     & 1
     \\
     & \downarrow
     \\
     a^* &\otimes& a
     \\
     \;\;\;\downarrow^{Id_{a^*}} && \;\;\downarrow^f
     \\
     a^* &\otimes& a
     \\
     & \downarrow^{b_{a^*, a}} 
     \\
     a &\otimes& a^*
     \\
     & \downarrow
     \\
     & 1     
  }
$$

This definition makes sense in any [[braided monoidal category]], but often in non-symmetric cases one wants instead a slightly modified version which requires the extra structure of a [[balanced monoidal category|balancing]].

The trace of the identity $1_a:a \to a$ is called the **dimension** or [[Euler characteristic]] of $a$.


## Examples

* $C = Vect$ with its standard monoidal structure ([[tensor product]] of vector spaces): in this case tr(f) is the usual trace of a linear map;

* $C = SuperVect = (Vect_{\mathbb{Z}_2}, \otimes, b)$, the category of $\mathbb{Z}_2$-graded vector spaces with the _non_trivial symmetric braiding which is $-1$ on two odd graded vector spaces: in this case the above is the **supertrace** on supervectorspaces, $str(V) = tr(V_{even}) - tr(V_odd)$.


* $C = Span(Top^{op})$: here the trace is the [[co-span co-trace]] which can be seen as describing the gluing of in/out boundaries of [[cobordism]]s 
 
* $C = Span(Grpd)$: this reproduces the notion of trace of a linear map within the interpretation of spans of groupoids as linear maps in the context of [[groupoidification]] and [[geometric function theory]], made explicit at [[span trace]]


## Categorification

See [[trace of a category]]

## Partial trace

If the morphism described above is the endomorphism of a tensor product object $V \otimes W$, then there is a similarly evident way to "bend around" only the W-strand.

+--{: .query}
TO DO: Draw the diagram just described.
=--

### Matrix representation

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

#### Example

Consider a quantum system, $\rho$, in the presence of an environment, $\rho_{env}$.  Consider what is known in [[quantum information theory]] as the CNOT gate:

$$
  U={|00\rangle}{\langle 00|} + {|01\rangle}{\langle 01|} + {|11\rangle}{\langle 10|} + {|10\rangle}{\langle 11|}.
$$

Suppose our system has the simple state ${|1\rangle}{\langle 1|}$ and the environment has the simple state ${|0\rangle}{\langle 0|}$.  Then $\rho \otimes \rho_{env} = {|10\rangle}{\langle 10|}$.  In the quantum operation formalism we have

$$
  T(\rho) = \frac{1}{2}Tr_{env}U(\rho \otimes \rho_{env})U^{\dagger}
          = \frac{1}{2}Tr_{env}({|10\rangle}{\langle 10|} + {|11\rangle}{\langle 11|})
          = \frac{{|1\rangle}{\langle 1|}{\langle 0|0\rangle} + {|1\rangle}{\langle 1|}{\langle 1|1\rangle}}{2}
          = {|1\rangle}{\langle 1|}
$$

where we inserted the normalization factor $\frac{1}{2}$.

## References

* Joyal, Street, and Verity, _Traced Monoidal Categories_  
* Dold, Albrecht and Puppe, Dieter, _Duality, trace, and transfer_
* Peter Selinger, _A survey of graphical languages for monoidal categories_ ([pdf](http://www.mathstat.dal.ca/~selinger/papers/graphical.pdf)), Section 5

For partial trace, particularly its application to quantum mechanics, see:

* Nielsen and Chuang, _Quantum Computation and Quantum Information_

[[!redirects partial trace]]