## Idea

In quantum algebra, the partial trace is a generalization of trace. Instead of taking in an endomorphism $f:A\to A$ and returning a scalar $\tr(f)$, the partial trace takes in a function $f:A\otimes X\to B\otimes X$ and returns a restricted morphism $\tr^X(f):A\to B$.

In quantum physics, [[measurement]] (and in particular partial measurement) play a very subtle but very key role. The partial trace corresponds to partial measurement on a physical system.

The partial trace is generalized by [[traced monoidal categories]]. That is, a traced monoidal category is a [[monoidal category]] paired with an operation which behaves like the partial trace.

## Definition 

Let $\text{Vec}_k$ denote the category of finite dimensional vector spaces over a field $k$. The partial trace gives a compatible collection of linear maps

$$\tr_W: \text{End}(V\otimes W)\to \text{End}(V)$$

for all $V,W\in\text{Vec}_k$, "tracing out" $W$. In particular, when $V=k$ we get maps

$$\tr_{W}:\text{End}(W)\to \text{End}(k).$$

To recover the usual trace, we make the canonical identification $\text{End}(k)\cong k$ sending $\text{id}_k$ to $1$.

It is a standard fact from linear algebra that morphisms of the form $f\otimes g$, $f:V\to V$, $g:W\to W$ generate $\text{End}(V\otimes W)$. Hence, we can define the partial trace as the unique linear assignment such that

$$\tr_W(f\otimes g)=\tr(g)\cdot f$$

where $\tr(g)$ is the usual trace. Explicitly, the partial trace can also be defined as follows. Let $f:V\otimes W\to V\otimes W$ be an endomorphism. Let $v_{1}, \ldots, v_{m}$ and $w_{1}, \ldots, w_{n}$ be bases for $V$ and $W$ respectively. Then $f$ has a matrix representation $\{a_{kl,ij}\}$ where $1 \le k,i \le m$ and $1 \le l,j \le n$ relative to the basis of the space $V \otimes W$ given by $e_{k} \otimes f_{l}$. Consider the sum

$$b_{k,i} = \sum_{j=1}^{n}a_{kj,ij}$$

for $k,i$ over $1, \ldots, m$.  This gives the matrix $b_{k,i}$.  The associated linear operator on $V$ is independent of the choice of bases and is defined as the partial trace.

## Graphical language

Given vector spaces $A,B$, or more generally, given objects $A,B$ in a traced monoidal category, we will often write the partial trace using [[string diagrams]] as follows:


\begin{imagefromfile}
"file_name": "partial-trace.png",
"width": 200,
"unit": "px"
\end{imagefromfile}


Considering $\text{Vec}_k$ as a [[pivotal category]], this diagram is completely rigorous. To make sure this notation is consistent, we verify

\begin{imagefromfile}
"file_name": "partial-trace-computation.png",
"width": 450,
"unit": "px"
\end{imagefromfile}


Additionally the closed loop can _only_ be trace. This is because the axioms of a pivotal category we can move around the loop, so

\begin{imagefromfile}
"file_name": "composition-commutes.png",
"width": 500,
"unit": "px"
\end{imagefromfile}


It is a standard fact from linear algebra that the trace is uniquely characterized by the fact that it is linear and acts the same on $f\circ g$ and $g\circ f$ for all $f,g:A\to A$.

## Example

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