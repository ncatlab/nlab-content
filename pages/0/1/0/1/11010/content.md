
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of _amplimorphism_ is a way to present [[bimodules]] in terms of linear maps.

For $A$ an [[associative algebra]] (not necessarily unital) over some [[ring]] $R$ (possibly with extra structure, in applications often a [[C*-algebra]]) then an _amplimorphism_ from $A$ to $A$ is an algebra homomorphism of the form

$$
  \alpha \;\colon\; A \longrightarrow A \otimes_R Mat_n(R) \simeq Mat_n(A)
$$

for $n \in \mathbb{N}$ and $Mat_n(R)$ the ring of [[matrices]] with [[coefficients]] in $R$ under [[matrix multiplication]].

This map induces the $R$-[[bimodules]] $N_\alpha \subset A \otimes R^n$ on elements $N_\alpha = \{\psi \;|\;  \alpha(1)\psi = \psi\}$ with left $A$-action given by $\alpha$ and right $A$ action given by componentwise multiplication with $A$ from the right. 

(If $R = \mathbb{C}$ and $A$ is a [[C*-algebra]] then this is canonically equipped with the structure of a [[Hilbert bimodule]]). 

## References

At least in the context of [[AQFT]] amplimorphisms were  introduced

* K. Szlach&#225;nyi, K. Vecsernyes, _Quantum symmetry and braid group statistics in $G$-spin models_, Commun. Math. Phys. __156__:1 (1993), 127-168, [euclid](http://projecteuclid.org/euclid.cmp/1104253519) [doi](http://dx.doi.org/10.1007/BF02096735)

The concept is recalled for instance in 

* Ezio Vasselli, page 6 of _The $C^\ast$-algebra of a vector bundle and fields of Cuntz algebras_, Journal of Functional Analysis 222(2) (2005), 491-502, [arXiv:math/0404166](http://arxiv.org/abs/math/0404166)


* Fernando Lled&#243;, Ezio Vasselli, section 3.3 of _Realization of minimal $C^\ast$-dynamical systems in terms of Cuntz-Pimsner algebras_ ([arXiv:math.OA/0702775](http://arxiv.org/abs/math.OA/0702775))

[[!redirects amplimorphisms]]