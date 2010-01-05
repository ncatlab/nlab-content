
#Contents#
* automatic table of contents goes here
{:toc}

## Motivation

The construction of [[moduli space]]s depends strongly on local properties like smoothness and [[transversal map|transversality]] of intersections when trying to [[representable functor|represent]] the [[functor]] of assigning families of objects to the varying base of family. When passing to the classes of equivalent objects, one faces the problem of having nontrivial [[automorphism]]s. 

At the [[infinitesimal object|infinitesimal]] level [[automorphism]]s correspond to the [[derivation]]s. Taking derivations is represented by the [[module]] of relative [[Kähler differential]]s which sufficies in good cases. Its correct [[derived algebraic geometry|derived]] replacement is the **cotangent complex** of Grothendieck-Illusie. One can typically split the information about a map of higher rings into its "discrete part" and infinitesimal obstruction theory governed by the cotangent complex. 

##Quillen's definition

Using the module of K&#228;hler differentials is not appropriate in general; instead we need to take its derived version. To talk about the nonabelian derived functors, Quillen introduced a model category structure on the category of simplicial commutative rings. Given a morphism $f: A\to B$ of rings, which makes $B$ an $A$-algebra, the category $AbGr(A$-$Alg/B)$ of abelian group objects in the slice category $A$-$Alg/B$ of $A$-algebras over $B$ is equivalent both to the category of $B$-modules and the trivial (= square zero) extensions of $A$ by $B$-modules. In particular we can consider the forgetful functor $AbGr(A$-$Alg/B)\to A$-$Alg/B$ which has a left adjoint $Ab_{B/A} : A$-$Alg/B\to AbGr(A$-$Alg/B)\cong {}_B Mod$. All said is true for simplicial commutative rings as well. Now the **relative cotangent complex** $L_{B/A}$ is the value on $B$ of the left [[derived functor]] $\mathbb{L} Ab_{B/A}(B)$. Regarding that the left adjoint at the nonderived level (and for usual rings) can be expressed via K&#228;hler differentials, this explains the phrase "derived version of the module K&#228;hler differentials".

## $(\infty,1)$-categorical viewpoint

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

##Further properties and applications 

For more background see [[deformation theory]].

Apart from simplicial rings we can consider $E_\infty$-rings. A map of connective $E_\infty$-rings is an equivalence, if it induces an isomorphism at the level of $\pi_0$ plus a condition on the relative cotangent complex.
Similarly, one can express the descent properties of higher stacks via the usual gluing at the bottom level plus the obstruction theory for relative cotangent complex. Study of an appropriate version of the [[Postnikov tower]] is a systematic way to do this. 

## References

* [[Alexander Grothendieck]], _Cat&#233;gories cofibr&#233;es additives et complexe cotangent relatif_, Lec. Notes in Math. __79__

* L. Illusie, _Complexe cotangent et d&#233;formations I_, Lec. Notes Math. __239__, Springer 1971, xv+355 pp.; _II_, LNM __283__, Springer 1972. vii+304 xv+355 pp. 

* Kai Behrend, B. Fantechi, _The intrinsic normal cone_, Invent. Math. __128__ (1997), no. 1, 45--88, MR1437495 (98e:14022) [arXiv:alg-geom/9601010](http://arxiv.org/abs/alg-geom/9601010)

* B. Fantechi, M. Manetti, _Obstruction calculus for functors of Artin rings I_, J. Algebra __202__ (1998), no. 2, 541--576, MR1617687 (99f:14004).

* [[Jacob Lurie]], [[Deformation Theory]], ([arXiv:0709.3091](http://arxiv.org/abs/0709.3091))

* S. Schwede, _Spectra in model categories and applications to the algebraic cotangent complex_, J. Pure Appl. Alg. __120__, 77--104 (1997) (<a href="http://dx.doi.org/10.1016/S0022-4049(96)00058-8">doi</a>)