#Contents#
* the following line creates the automatic table of contents
{:toc}

## Idea ##
The Borchers property is a property of [[local nets]] in the [[Haag-Kastler approach]] to [[quantum field theory]] that follows, by a theorem of Borchers, from three physically motivated axioms on [[local nets]]. 
If every local algebra of the net is a type III factor, then the Borchers property is also a direct consequence. 

The Borchers property is therefore often used as an "intermediate technical assumption".

Sometimes this property is also abbreviated as "property B".

## Definition ##
Let $\mathcal{M}(\mathcal{O})$ be a net of [[von Neumann algebras]] indexed by bounded open subsets of [[Minkowski spacetime]], for more details see [[Haag-Kastler vacuum representation]] for more details, 

+-- {: .un_defn}
###### Definition
The net $\mathcal{M}(\mathcal{O})$ satisfies the **Borchers property** if for every double cones $K_1, K_2$ with $\bar K_1 \subseteq K_2$ and $E \in \mathcal{M}(\mathcal{K}_1)$ a nonzero projection, $E$ is (Murray-von Neumann) equivalent to the identity with respect to $\mathcal{M}(\mathcal{K}_2)$. That is, there is a partial isometry $V \in \mathcal{M}(\mathcal{K}_2)$ such that $VV^* = E, V^*V = \mathbb{1}$.
=--

## Properties ##

+-- {: .un_prop}
###### Proposition
A net satisfying causality, the spectrum condition and weak additivity (see [[Haag-Kastler vacuum representation]] for definitions) satisfies the Borchers property.
=--

_Remark_ : In particular the local algebras of nets that satisfy the Borchers property cannot be finite where finite is meant in the sense of the Murray-von Neumann classification of factors.

## References ##

* H.-J. Borchers: _A remark on a theorem of B. Misra_ (available online from project euclid [here](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.cmp/1103839939))

[[!redirects B property]]