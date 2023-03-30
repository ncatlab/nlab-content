
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

In [[algebraic quantum field theory]], the *Borchers property* is a property of [[local nets]] in the [[Haag-Kastler approach]] to [[quantum field theory]] that follows, by a theorem of Borchers, from three physically motivated axioms on [[local nets]]. 
If every local algebra of the net is a type III factor, then the Borchers property is also a direct consequence. 

The Borchers property is therefore often used as an "intermediate technical assumption".

Sometimes this property is also abbreviated as "property B".

## Definition ##

Let $\mathcal{M}(\mathcal{O})$ be a net of [[von Neumann algebras]] indexed by bounded open subsets of [[Minkowski spacetime]], for more details see [[Haag-Kastler vacuum representation]], 

\begin{definition}

The net $\mathcal{M}(\mathcal{O})$ satisfies the **Borchers property** if for every double cones $K_1, K_2$ with $\bar K_1 \subseteq K_2$ and $E \in \mathcal{M}(\mathcal{K}_1)$ a nonzero projection, $E$ is (Murray-von Neumann) equivalent to the identity with respect to $\mathcal{M}(\mathcal{K}_2)$. That is, there is a partial isometry $V \in \mathcal{M}(\mathcal{K}_2)$ such that $VV^* = E, V^*V = \mathbb{1}$.

\end{definition}


## Properties ##

\begin{proposition}
A net satisfying causality, the spectrum condition and weak additivity (see [[Haag-Kastler vacuum representation]] for definitions) satisfies the Borchers property.
\end{proposition}


\begin{remark}
In particular. the local algebras of nets that satisfy the Borchers property cannot be finite where finite is meant in the sense of the Murray-von Neumann classification of [[von Neumann algebra factor|factors]].
\end{remark}

## References ##

* [[Hans-Jürgen Borchers]], _A remark on a theorem of B. Misra_,  Comm. Math. Phys. **4** 5 (1967) 315-323 &lbrack;[euclid](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-4/issue-5/A-remark-on-a-theorem-of-B-Misra/cmp/1103839939.full)&rbrack;

[[!redirects B property]]


