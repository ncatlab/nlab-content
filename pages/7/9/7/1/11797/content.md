
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In [[algebraic geometry|algebraic]]/[[complex geometry]] The term *Abel-Jacobi map* refers to various [[group homomorphisms]] from certain [[groups]] of [[algebraic cycles]] to some sorts of [[Jacobians]] or generalized Jacobians. Such maps generalize the classical Abel-Jacobi map from points of a complex algebraic curve to its [[Jacobian]], which answers the question of which divisors of degree zero arise from [[meromorphic functions]].

## Definition

### for curves

Let $X$ be a smooth projective [[complex curve]]. Recall that a [[Weil divisor]] on $X$ is a [[formal linear combination]] of [[closed points]]. Classically, the Abel-Jacobi map
$$ 
  \alpha 
  \;\colon\; 
  \Div^0(X) 
   \longrightarrow 
  J(X)
  ,\,
$$
on the group of [[Weil divisors]] of degree zero, is defined by [[integration]]. According to [[Abel's theorem]], its [[kernel]] consists of the [[principal divisors]], i.e. the ones coming from [[meromorphic functions]].

### on Deligne cohomology

The cycle map to [[de Rham cohomology]] due to [Zein & Zucker (1981)](#ZeinZucker81) is discussed in [Esnault & Viehweg (1988), section 6](#EsnaultViehweg88), the refinement to [[Deligne cohomology]] in [Esnault & Viehweg (1988), section 6](#EsnaultViehweg88). By the characterization of [[intermediate Jacobians]] as subgroups of the [[Deligne complex]] (see *[intermediate Jacobian -- characterization as Hodge-trivial Deligne cohomology](intermediate+Jacobian#CharacterizationAsHodgeTrivialDeligneCohomology)*) this induces a map from cycles to [[intermediate Jacobians]]. This is the Abel-Jacobi map ([Esnault & Viehweg (1988), theorem 7.11](#EsnaultViehweg88)).

### on higher Chow groups

An Abel-Jacobi map on [[higher Chow groups]] is discussed in [K-L-MS 04](#KLMS04).

### via extensions of mixed Hodge structures

An alternate construction of the Abel-Jacobi map, via [[Hodge theory]], is due to Arapura-Oh.
By a theorem of Carlson, the [[Jacobian]] is identified with the following group of [[extensions]] in the [[abelian category]] of [[mixed Hodge structures]]:
  $$ J(X) = Ext^1_{MHS}(\mathbf{Z}(-1), H^1(X, \mathbf{Z})) $$
where $\mathbf{Z}(-1)$ is the Tate Hodge structure.
Given a [[divisor]] $D$ of degree zero, one can associate to it a certain class in the above extension group.
This gives a map
  $$ \alpha : Div^0(X) \longrightarrow J(X) $$
which is called the Abel-Jacobi map.
The Abel theorem says that its [[kernel]] is precisely the subgroup of [[principal divisors]], i.e. divisors which come from invertible rational functions.
See ([Arapura-Oh, 1997](#ArapuraOh97)) for details of this construction.

## Related concepts

* [[Hodge-filtered differential cohomology]]

## References

* {#ZeinZucker81} Fouad El Zein and Steven Zucker, _Extendability of normal functions associated to algebraic cycles_, Topics in transcendental algebraic geometry (Princeton, N.J., 1981/1982), Ann. of Math. Stud., vol. 106, Princeton Univ. Press, Princeton, NJ, 1984, pp. 269&#8211;288. [MR 756857](http://www.ams.org/mathscinet-getitem?mr=756857) 

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_, in: [[Michael Rapoport]], [[Norbert Schappacher]], [[Peter Schneider]] (eds.), _[[Beilinson's Conjectures on Special Values of L-Functions]]_, Perspectives in Mathematics **4**, Academic Press, Inc. (1988) &lbrack;ISBN:978-0-12-581120-0, [[EsnaultViehweg-DeligneBeilinsonCohomology.pdf:file]]&rbrack;

* {#Voisin02} [[Claire Voisin]], section 12 of _[[Hodge theory and Complex algebraic geometry]] I,II_,  Cambridge Stud. in Adv. Math. __76, 77__, 2002/3

* {#ArapuraOh97} Donu Arapura, Kyungho Oh. _On the Abel-Jacobi map for non-compact varieties_. Osaka Journal of Mathematics 34 (1997), no. 4, 769--781. [Project Euclid](http://projecteuclid.org/euclid.ojm/1200787781).

* {#KLMS04} Matt Kerr, James Lewis, Stefan M&#252;ller-Stach, _The Abel-Jacobi map for higher Chow groups_, 2004, [arXiv:0409116](http://arxiv.org/abs/math/0409116).

* Wikipedia, _[Abel-Jacobi map](http://en.wikipedia.org/wiki/Abel&#8211;Jacobi_map)_

Remarks on generalization to the more general context of [[anabelian geometry]] are in

* [[Minhyong Kim]], _Galois Theory and Diophantine geometry, 2009 ([pdf](http://www.ucl.ac.uk/~ucahmki/cambridgews.pdf))

Refinement of the [[Abel-Jacobi map]] to [[Hodge filtration|Hodge filtered]] [[differential cobordism cohomology theory|differential]] [[MU]]-[[cobordism cohomology theory]]:

* [[Gereon Quick]], *An Abel-Jacobi invariant for cobordant cycles*,
Documenta Mathematica **21** (2016) 1645–1668 &lbrack;[arXiv:1503.08449](https://arxiv.org/abs/1503.08449)&rbrack;

* [[Knut B. Haus]], [[Gereon Quick]], *Geometric Hodge filtered complex cobordism* &lbrack;[arXiv:2210.13259](https://arxiv.org/abs/2210.13259)&rbrack;

Introduction and survey:

* [[Gereon Quick]], *Geometric Hodge filtered complex cobordism*, [talk at](Center+for+Quantum+and+Topological+Systems#QuickMar2023) *[[CQTS]]* (March 2023) &lbrack;video:[YT](https://www.youtube.com/watch?v=pMu0gT5kIBo)&rbrack;




[[!redirects Abel-Jacobi maps]]

[[!redirects Abel-Jacobi theorem]]
[[!redirects Abel-Jacobi theorems]]