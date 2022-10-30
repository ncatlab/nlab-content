## Idea

A symmetric sequence is a [[sequence]] of [[objects]] where the $n$th [[object]] has an [[action]] of the $n$th [[symmetric group]].

## Definition

1.  Let $C$ be a [[category]] and $G$ a [[group]].  A **$G$-representation** of $C$ is a functor $\bullet\{G\} \to C$, where $\bullet\{G\}$ is the [[category]] with a single object $\bullet$ and $\Hom(\bullet, \bullet) = G$.  Explicitly, a $G$-representation of $C$ is the data of an object $X \in C$ together with an [[group action|action]] $a : G \to \Aut_C(X)$.  We write $Rep(G, C)$ for the category of $G$-representations of $C$.

2.  Let $\Phi$ be a [[graded monoid]] in the category of [[groups]].  Explicitly this is the data of [[groups]] $\Phi_n$ for all $n \in \mathbf{N}$ with morphisms $\Phi_m \times \Phi_n \to \Phi_{m+n}$ for all $m,n \ge 0$ (subject to various axioms...).  $\Phi$ is usually either $\Sigma = (\Sigma_n)_n$, the [[graded monoid]] of [[symmetric groups]], or $1 = (1_n)_n$, the [[graded monoid]] of [[trivial group]]s.

3.  A **$\Phi$-symmetric sequence** in $C$ is a [[sequence]] of $\Phi_n$-representations for $n \ge 0$:
  $$ Seq(\Phi, C) = \sqcup_{n \ge 0} Rep(\Phi_n, C) $$
In other words a $\Phi$-symmetric sequence is a sequence of objects $(X_n)_{n \ge 0}$ together with [[actions]] $a_n : \Phi_n \to \Aut_C(X_n)$.  When $\Phi = \Sigma$, the [[graded monoid]] of [[symmetric groups]], we say simply "symmetric sequence".

## See also

* [[spectra]], [[symmetric spectra]]

## References

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique, I_. Ast&#233;risque, Vol. 314 (2008). Soci&#233;t&#233; Math&#233;matique de France. ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF))
