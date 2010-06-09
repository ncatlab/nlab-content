#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
The split property for inclusions of [[von Neumann algebras]] was first introduced by [[Detlev Buchholz]] in the study of the [[AQFT]] approach to [[quantum field theory]], but has become a much used concept in the mathematical structure theory as well.


## Definition ##
Let $M, N$ be two von Neumann algebras with $M \subseteq N$. This inclusion is called **split** if there is a type I-factor $F$ with
$$
M \subseteq F \subseteq N
$$

## Properties ##
+-- {: .un_theorem}
###### Theorem

The inclusion $M \subseteq N$ is split iff there exist faithful normal representations $\pi_1$ of $M$, $\pi_2$ of $N'$ such that the map $\Phi: M \vee N' \to \pi_1(M) \otimes \pi_2(N')$ given by
$$
\Phi(mn') := \pi_1(m) \otimes \phi_2(n')
$$
extends to a spatial isomorphism, the tensor product used here is the [[spatial tensor product]].
=--

## References ##

Definition 5.4.1 und Lemma 5.4.2 in

* Wollenberg, Baumg&#228;rtel: _Causal nets of operator algebras. Mathematical aspects of algebraic quantum field theory._

[[!redirects <put page name here>s]]