
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _external tensor product_ is a variant of that of [[tensor product]] in a [[monoidal category]] when the latter is generalized to [[indexed monoidal categories]] ([[dependent linear type theory]]).

## Definition

Consider an [[indexed monoidal category]] given by a [[Cartesian fibration]]

$$
  \array{
    Mod(-)
    \\
    \downarrow
    \\
    \mathbf{H}
  }
$$

over a [[cartesian monoidal category]] $\mathbf{H}$.

+-- {: .num_defn}
###### Definition

Given $X_1, X_2 \in \mathbf{H}$ the _external tensor product_ over these is the [[functor]]

$$
  \boxtimes \;\colon\;
  Mod(X_1)\times Mod(X_2)
  \longrightarrow
  Mod(X_1 \times X_2)
$$

given  on $A_1 \in Mod(X_1)$ with $A_2 \in Mod(X_2)$ by

$$
  A_1 \boxtimes A_2 \coloneqq (p_1^\ast A_1) \otimes_{X_1 \times X_2} (p_2^\ast A_2)
  \in Mod(X_1 \times X_2)
  \,,
$$

where $p_1, p_2$ denote the [[projection]] maps out of the [[Cartesian product]] $X_1 \times X_2 \in \mathbf{H}$.

=--

+-- {: .num_remark}
###### Remark

The external tensor product constitutes a [[tensor product]] on the total category $Mod$ of the given [[Grothendieck fibration]] $Mod(-)\to \mathbf{H}$; and with respect to this it is a [[monoidal fibration]].

=--

## Properties

### Relation to fiberwise tensor product

+-- {: .num_prop}
###### Proposition

The fiberwise ("internal") tensor product over $X\in \mathbf{H}$ is recovered form the external one via a [[natural equivalence]]

$$
  A_1 \otimes_X A_2 \simeq \Delta_X^\ast (A_1 \boxtimes A_2)
$$

for $A_1, A_2 \in Mod(X)$, where $\Delta \colon X \longrightarrow X \times X$ is the [[diagonal]] in $\mathbf{H}$ on $X$.


=--

### Generation of $Mod(X_1 \times X_2)$ from external tensor products

Under suitable conditions on compact generation of $Mod(-)$ then one may deduce that $Mod(X_1 \times X_2)$ is generated under external product from 
$Mod(X_1)$ and $Mod(X_2)$.

([Bondal-vdBerg 03](#BondalvdBerg03), [BFN 08, proof of prop. 3.24](#BFN08))

## References

For general abstract literature dealing with the external tensor products see the references at _[[indexed monoidal category]]_ and at _[[dependent linear type theory]]_.

For discussion in the context of categories of [[quasicoherent sheaves]]  in ([[derived algebraic geometry|derived]]) see for instance

* {#BondalvdBerg03} [[Alexei Bondal]] and M. Van den Bergh, _Generators and representability of functors in commutative and noncommutative geometry_, Mosc. Math. J. 3 (2003), no. 1, 1&#8211;36, 258.

* {#BFN08} [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_, J. Amer. Math. Soc. 23 (2010), no. 4, 909-966 ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

[[!redirects external tensor products]]

[[!redirects external product]]
[[!redirects external products]]

