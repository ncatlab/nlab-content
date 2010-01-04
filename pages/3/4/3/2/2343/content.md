
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _cotangent complex_ is a generalization to [[higher category theory]] and [[higher algebra]] of the notion of [[cotangent bundle]] in the sense of [[Kähler differential]]s.

For $C =$ [[Ring]] the ordinary category of commutative rings, the cotangent complex functor is the [[section]] 

$$
  \Omega_K : Ring \to Mod
$$

of the canonical [[bifibration]] $Mod \to Ring$ of [[module]]s over [[ring]]s that is on objects given by forming the module of [[Kähler differential]]s. 

This generalizes to the case where [[Ring]] is replaced by any [[(∞,1)-category]] $C$: the cotangent complex functor for $C$ is here the [[left adjoint]] [[section]] 

$$
  \Omega : C \to T_C
$$

of the [[tangent (∞,1)-category]] projection $T_C \to C$. 

In particular, when $C = ...$, then the cotangent complex assigns ... .

For more background see [[deformation theory]].

## Motivation

The construction of [[moduli space]]s depends strongly on local properties like smoothness and [[transversal map|transversality]] of intersections when trying to [[representable functor|represent]] the [[functor]] of assigning families of objects to the varying base of family. When passing to the classes of equivalent objects, one faces the problem of having nontrivial [[automorphism]]s. 

At the [[infinitesimal object|infinitesimal]] level [[automorphism]]s correspond to the [[derivation]]s. Taking derivations is represented by the [[module]] of relative [[Kähler differential]]s which sufficies in good cases. Its correct [[derived algebraic geometry|derived]] replacement is the **cotangent complex** of Grothendieck-Illusie. 

## References

* [[Alexander Grothendieck]], _Cat&#233;gories cofibr&#233;es additives et complexe cotangent relatif_, Lec. Notes in Math. __79__

* L. Illusie, _Complexe cotangent et d&#233;formations I_, Lec. Notes Math. __239__, Springer 1971, xv+355 pp.; _II_, LNM __283__, Springer 1972. vii+304 xv+355 pp. 

* Kai Behrend, B. Fantechi, _The intrinsic normal cone_, Invent. Math. __128__ (1997), no. 1, 45--88, MR1437495 (98e:14022) [arXiv:alg-geom/9601010](http://arxiv.org/abs/alg-geom/9601010)

* B. Fantechi, M. Manetti, _Obstruction calculus for functors of Artin rings I_, J. Algebra __202__ (1998), no. 2, 541--576, MR1617687 (99f:14004).

* [[Jacob Lurie]], [[Deformation Theory]], ([arXiv:0709.3091](http://arxiv.org/abs/0709.3091))

* S. Schwede, _Spectra in model categories and applications to the algebraic cotangent complex_, J. Pure Appl. Alg. __120__, 77--104 (1997) (<a href="http://dx.doi.org/10.1016/S0022-4049(96)00058-8">doi</a>)