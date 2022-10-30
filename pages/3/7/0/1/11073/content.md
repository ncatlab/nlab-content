## Idea

A symmetric sequence is a [[sequence]] of [[objects]] where the $n$th [[object]] has an [[action]] of the $n$th [[symmetric group]]. 

## Definition



+-- {: .num_defn}
###### Definition

1.  Let $C$ be a [[category]] and $G$ a [[group]].  A **$G$-representation** of $C$ is a functor $\bullet\{G\} \to C$, where $\bullet\{G\}$ is the [[category]] with a single object $\bullet$ and $\Hom(\bullet, \bullet) = G$.  Explicitly, a $G$-representation of $C$ is the data of an object $X \in C$ together with an [[group action|action]] $a : G \to \Aut_C(X)$.  We write $Rep(G, C)$ for the category of $G$-representations of $C$.

2.  Let $\Phi$ be a [[graded monoid]] in the category of [[groups]].  Explicitly this is the data of [[groups]] $\Phi_n$ for all $n \in \mathbf{N}$ with morphisms $\Phi_m \times \Phi_n \to \Phi_{m+n}$ for all $m,n \ge 0$ (subject to various axioms...).  $\Phi$ is usually either $\Sigma = (\Sigma_n)_n$, the [[graded monoid]] of [[symmetric groups]], or $1 = (1_n)_n$, the [[graded monoid]] of [[trivial group]]s.

3.  A **$\Phi$-symmetric sequence** in $C$ is a [[sequence]] of $\Phi_n$-representations for $n \ge 0$:
  $$ Seq(\Phi, C) = \sqcup_{n \ge 0} Rep(\Phi_n, C) $$
In other words a $\Phi$-symmetric sequence is a sequence of objects $(X_n)_{n \ge 0}$ together with [[actions]] $a_n : \Phi_n \to \Aut_C(X_n)$.  When $\Phi = \Sigma$, the [[graded monoid]] of [[symmetric groups]], we say simply "symmetric sequence".

=--

In the case that the graded group of interest is indeed $\Sigma$, we can define a $\Sigma$-symmetric sequence somewhat more simply:

+-- {: .num_defn}
###### Definition

A **$\Sigma$-symmetric sequence** in a [[symmetric monoidal category]] $C$ is a symmetric monoidal functor from $FinSet$, the [[category]] of [[finite sets]] and [[bijections]], to $C$. 

=--


The relationship between the two definitions is that given a functor $F:FinSet\to C$, we have a sequence of objects for each $n$ associated to the finite set with $n$ elements. The action of $\Sigma_n$ on these objects comes from the fact that for every [[permutation]] in $\Sigma_n$ there is an associated morphism in $FinSet$. Sometimes the category $FinSet$ is replaced with its [[skeleton]], the category of all finite [[ordinals]] with all bijections between them. This latter category is sometimes denoted $FinOrd$ or just $\Sigma$. In the latter case, we sometimes call $\Sigma$-symmetric sequences just "$\Sigma$-sequences." 

## Symmetric monoidal structure

4.  Let $\alpha : H \to G$ be a [[homomorphism]] of [[groups]] and consider the [[restriction of scalars]] functor
  $$ \Res^G_H : \Rep(G, C) \to \Rep(H, C) $$
which is defined in the obvious way.  It admits a left adjoint
  $$ Ind^G_H : \Rep(H, C) \to \Rep(G, C) $$
called the _induced representation_ functor.

5.  Suppose now that $C$ has a [[symmetric monoidal structure]].  Assume also that $C$ admits [[coproducts]] and that the functors $X \otimes -$ commute with them (for all $X \in C$).  Then there is an induced [[symmetric monoidal structure]] on $Seq(\Phi, C)$.  Given symmetric sequences $X = (X_n)_n$ and $Y = (Y_n)_n$, we define $X \otimes Y$ as the symmetric sequence which has in the $n$th component
  $$ (X \otimes Y)_n = \sqcup_{p+q=n} \Ind^{\Phi_n}_{\Phi_p \times \Phi_q} (X_p \otimes Y_q) $$
where $\Phi_p \times \Phi_q \to \Phi_n$ is the canonical morphism which is part of the [[structure]] of the [[graded monoid]] $\Phi = (\Phi_n)_n$.  The [[unit]] with respect to this [[monoidal structure]] is given by $1 = (1, \emptyset, \emptyset, ...)$.

## Relationship to Operads

Symmetric sequences are useful in defining [[operads]] in [[symmetric monoidal categories]]. In particular, an operad in a symmetric monoidal category $C$ can be defined to be a [[commutative monoid]] in the category of symmetric sequences of $C$. See, for instance, Definition 2.2.9 of [Ching](#Ching).


## See also

* [[spectra]], [[symmetric spectra]]

* [[symmetric color sequence]]

## References

The last chapter of

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique, I_. Ast&#233;risque, Vol. 314 (2008). Soci&#233;t&#233; Math&#233;matique de France. ([pdf](http://user.math.uzh.ch/ayoub/PDF-Files/THESE.PDF))


* {#Ching} [[Michael Ching]], _Bar constructions for topological operads and the
Goodwillie derivatives of the identity_ (PhD Thesis), [Available Here](https://dspace.mit.edu/bitstream/handle/1721.1/27881/61212201-MIT.pdf?sequence=2).


[[!redirects symmetric sequences]]
[[!redirects sigma sequence]]
[[!redirects sigma sequences]]