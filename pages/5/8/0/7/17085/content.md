
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The generalization of the [[stable homotopy category]] from [[stable homotopy theory]] to [[equivariant stable homotopy theory]].

## Definition

A [[homomorphism]] $f \colon E_1 \longrightarrow E_2$ between two [[G-spectra]], indexed on a [[G-universe]] $\mathcal{U}$, is called an equivariant [[weak homotopy equivalence]] if the following equivalent conditions hold

1. For each $V\in \mathcal{U}$ the component map $f_V \colon f$ induces ordinary [[weak homotopy equivalences]] $(E_1)_V^H \to (E_2)_V^H$ on all [[fixed point]] spaces for all closed [[subgroups]] $H \hookrightarrow G$.

1. For each $n \in \mathbb{Z}$ and each closed subgroup $H \hookrightarrow G$ the morphism $f$ induces an [[isomorphism]] of [[Mackey functors]] of [[equivariant homotopy groups]] $\pi_n^H(E_1) \stackrel{\simeq}{\longrightarrow} \pi_n^H(E_2)$.

(The equivalence of these conditions is part of the [[equivariant Whitehead theorem]].)

The $G$-equivariant stable homotopy category is the [[homotopy category]] of [[G-spectra]] with respect to these weak equivalences.

## Properties

### Relation to Mackey functors

The  [[full subcategory]] $\mathcal{B}_G$ of the equivariant stable homotopy category on the objects of the form 

$$
  G/H_* \wedge \Sigma^\infty S^n
$$

is, as an [[additive category]], the [[domain]] of [[Mackey functors]], such as the [[equivariant homotopy group]]-functors.



## References

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], section 2 of _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* {#Bohmann} [[Anna Marie Bohmann]], _Basic notions of equivariant stable homotopy theory_, ([pdf](https://math.vanderbilt.edu/bohmanar/basicequivnotions.pdf))
