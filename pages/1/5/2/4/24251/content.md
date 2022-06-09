#Contents#
* table of contents
{:toc}

## Definition ##

A __$\omega$-complete poset__ is a [[poset]] $(P, \leq)$ with

* an element $\bot \in P$, such that for every element $a \in P$, $\bot \leq a$, representing that $\bot$ is initial in the poset. 

* a function
$$\Vee_{n:\mathbb{N}} (-)(n): (\mathbb{N} \to P) \to L$$
such that for every natural number $n \in \mathbb{N}$ and sequence $s:\mathbb{N} \to P$, 
$$s(n) \leq \Vee_{n:\mathbb{N}} s(n)$$
and for every element $a \in P$ and sequence $s:\mathbb{N} \to P$, 
$$\left(\prod_{n:\mathbb{N}}(s(n) \leq x)\right)$$
implies that
$$\left(\Vee_{n:\mathbb{N}} s(n) \leq a\right)$$
representing that denumerable/countable joins exist in the poset. 

## See also ##

* [[poset]]

* [[join-semilattice]]

* [[sigma-complete lattice]]

* [[partial function classifier]]

* [[directed-complete poset]]

## References ##

* Partiality, Revisited: The Partiality Monad as a Quotient Inductive-Inductive Type ([abs:1610.09254](https://arxiv.org/abs/1610.09254))