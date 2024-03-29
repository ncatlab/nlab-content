
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of **cotangent complex** is a _derived_  or [[(∞,1)-category|(∞,1)-categorical]] refinement of the notion of [[Kähler differential]]s.

Traditionally this has been conceived in terms of [[model category]] presentations. This we discuss in the section

* [Model category presentation](#ModCat).

From the [[nPOV]], the notion of cotangent complex has a more intrinsic description as being the [[left adjoint]] to the [[tangent (∞,1)-category]] projection. This we discuss in the section

* [(∞,1)-Categorical description](#InfCat)

### Motivation

The construction of [[moduli space]]s depends strongly on local properties like smoothness and [[transversal map|transversality]] of intersections when trying to [[representable functor|represent]] the [[functor]] of assigning families of objects to the varying base of family. When passing to the classes of equivalent objects, one faces the problem of having nontrivial [[automorphism]]s. 

At the [[infinitesimal object|infinitesimal]] level [[automorphism]]s correspond to the [[derivation]]s. Taking derivations is represented by the [[module]] of relative [[Kähler differential]]s which sufficies in good cases. Its correct [[derived algebraic geometry|derived]] replacement is the **cotangent complex** of Grothendieck-Illusie. One can typically split the information about a map of higher rings into its "discrete part" and infinitesimal obstruction theory governed by the cotangent complex. 


## Model category presentation {#ModCat}

### Quillen's definition: left derived functor of K&#228;hler differentials 
 {#LeftDerivedFunctorOfKaehlerDifferentials}

The **cotangent complex** functor is effectively the left [[derived functor]] of the [[Kähler differential]]s assignment.

To talk about the nonabelian derived functors, Quillen introduced a [[simplicial ring|model structure on the category of simplicial commutative rings]].

Given a morphism $f: A\to B$ in [[CRing]], which makes $B$ an $A$-algebra, the fiber of the [[tangent category]] $AbGr(A Alg/B)$ of abelian group objects in the slice category $A Alg/B$ of $A$-algebras over $B$ is equivalent both to the category of $B$-modules and the trivial (= square zero) extensions of $A$ by $B$-modules. 

In particular we can consider the forgetful functor $AbGr(A Alg/B)\to A Alg/B$ which has a [[left adjoint]] $\Omega_{A/B} Ab_{B/A} : A Alg/B\to AbGr(A Alg/B)\cong {}_B Mod$. This is the [[Kähler differential]]s functor.

All said is true for [[simplicial ring|simplicial commutative rings]] as well. 

+-- {: .num_defn}
###### Definition

The **relative cotangent complex** functor is the left [[derived functor]]

$$
  \mathbb{L} \Omega_{B/A} : 
   s A Alg/B\to s AbGr(A Alg/B)\cong s B Mod
$$


Its value on $B$ is the relative cotangent complex $L_{B/A}$ 

=--

The [[André-Quillen cohomology]] of $R$ is the [[cohomology]] of $\mathbb{L}\Omega(R)$.

### Explicit resolutions

Here is one way to compute the required cofibrant [[resolution]] 
for the construction of the left [[derived functor]] for the case that $A = k$ is a [[field]].

Let $P : CAlg \to CAlg$ be the [[comonad]] induced by the [[adjunction]] 

$$
  U : CAlg \to Set : k[-]
$$

that sends a commutative $k$-algebra $R$ to the polynomial algebra on its underlying set. 

Let $P_\bullet R$ be the corresponding [[bar construction]] [[simplicial ring|simplicial algebra]]. The canonical morphism $P_\bullet R \to R$ with $R$ on the right regarded as a constant simplicial object is a resolution of $R$.

Forming degreewise the module of [[Kähler differential]]s on this yields the simplicial object $\Omega_{k}(P_\bullet R)$, which is a $P_\bullet R$-module. 

+-- {: .num_prop}
###### Proposition

The cotangent complex of $R$ is equivalent to 

$$
  (\mathbb{L} \Omega_{/k}) (R) \simeq
  R \otimes_{P_\bullet R} \Omega_k(P_\bullet R)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Notice that the universal property of the [[Kähler differential]]s is that for $R$ a ring and $N$ an $R$-module, we have

$$
  Hom(\Omega(R), N) \simeq Der(R,N)
  \,.
$$

Accordingly, it follows that the [[André-Quillen cohomology]] of $R$ with values in $N$, which is the cohomology of the cosimplicial object 

$$
  Hom((\mathbb{L}\Omega)(R), N)
$$

is equivalently the cohomology of the object

$$
  \begin{aligned} 
    \cdots & \simeq
    Hom(R \otimes_{P_\bullet R} \Omega_k(P_\bullet R), N)
    \\
    & \simeq 
    Hom_{P_\bullet R}( \Omega_k(P_\bullet R), N)
    \\
    & \simeq
    Der(P_\bullet R, N)
  \end{aligned}
  \,.
$$

In particular we have the the degree-0 cohomology of this complex is the module of ordinary derivations

$$
  H^0(Der(P_\bullet R, N)) \simeq Der(R,N)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition


If in the above $k$ is [[field]] of characteristic 0, then 
[[André-Quillen cohomology]] of the $k$-algebra $R$ with coefficients in a [[module]] $N$ is a [[direct sum]]mand of the corresponding [[Hochschild cohomology]]:

$$
  H^q(Hom(\mathbb{L} \Omega (R)), N)
  \simeq
  HH^{q+1}_{(1)}(R,N)
  \,,
$$

where the subscript refers to [[Hodge decomposition]] of [[Hochschild cohomology]].

=--

This is in section 8.8 of

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_ 


## $(\infty,1)$-categorical description {#InfCat}

The _cotangent complex_ is a generalization to [[higher category theory]] and [[higher algebra]] of the notion of [[cotangent bundle]] in the sense of [[Kähler differential]]s.

Recall from above that for $C =$ [[CRing]] the ordinary category of commutative rings, the cotangent complex functor is the [[section]] 

$$
  \Omega_K : Ring \to Mod
$$

of the canonical [[bifibration]] $Mod \to Ring$ of [[module]]s over [[ring]]s that is on objects given by forming the module of [[Kähler differential]]s. 

This generalizes to the case where [[CRing]] is replaced by any [[(∞,1)-category]] $C$: the cotangent complex functor for $C$ is here the [[left adjoint]] [[section]] 

$$
  \Omega : C \to T_C
$$

of the [[tangent (∞,1)-category]] projection $dom : T_C \to C$. 

In particular, when $C = ...$, then the cotangent complex assigns ... .



## Further properties and applications 

### Characterization via universal properties

See [[cotangent complex in derived geometry]]


### Application: lifting properties of classical rings to derived rings

For more background see [[deformation theory]].

Apart from simplicial rings we can consider $E_\infty$-rings. A map of connective $E_\infty$-rings is an equivalence, if it induces an isomorphism at the level of $\pi_0$ plus a condition on the relative cotangent complex.
Similarly, one can express the descent properties of higher stacks via the usual gluing at the bottom level plus the obstruction theory for relative cotangent complex. Study of an appropriate version of the [[Postnikov tower]] is a systematic way to do this. 

## Related concepts

* [[deformation theory]], [[derived deformation theory]]

* [[tangent complex]], [[André-Quillen cohomology]], [[Hochschild cohomology]]

* **cotangent complex**, [[André-Quillen homology]], [[Hochschild homology]]

* [[topological André-Quillen homology]], [[topological Hochschild homology]]

## References

See also [[deformation theory]] and references therein.

* [[Alexander Grothendieck]], _Cat&#233;gories cofibr&#233;es additives et complexe cotangent relatif_, Lec. Notes in Math. __79__

* [[Luc Illusie]], _Complexe cotangent et d&#233;formations I_, Lec. Notes Math. __239__, Springer 1971, xv+355 pp.; _II_, LNM __283__, Springer 1972. vii+304 xv+355 pp. 

* [[Kai Behrend]], [[Barbara Fantechi]], _The intrinsic normal cone_, Invent. Math. __128__ (1997), no. 1, 45--88, MR1437495 (98e:14022) [arXiv:alg-geom/9601010](http://arxiv.org/abs/alg-geom/9601010)

* [[Barbara Fantechi]], M. Manetti, _Obstruction calculus for functors of Artin rings I_, J. Algebra __202__ (1998), no. 2, 541--576, MR1617687 (99f:14004).

* [[Jacob Lurie]], [[Deformation Theory]], ([arXiv:0709.3091](http://arxiv.org/abs/0709.3091))

* [[Stefan Schwede]], _Spectra in model categories and applications to the algebraic cotangent complex_, J. Pure Appl. Alg. __120__, 77--104 (1997) (<a href="http://dx.doi.org/10.1016/S0022-4049(96)00058-8">doi</a>)

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_ section 8.8.

* [[Gabriele Vezzosi]], _A note on the cotangent complex in derived algebraic geometry_, [arxiv/1008.0601](http://arxiv.org/abs/1008.0601)


* [[The Stacks Project]], _The cotangent complex_ ([pdf](http://stacks.math.columbia.edu/download/cotangent.pdf))

A short exposition (from the point of view of [[formal schemes]]) is in

* chapter 5 (5.29-5.31) in Luc Illusie, _Grothendieck's existence theorem in formal geometry_, in [[FGA explained]] (179--233) MR2223409; (draft version [pdf](http://cdsagenda5.ictp.it//askArchive.php?categ=a0255&id=a0255s3t3&ifd=15021&down=1&type=lecture_notes)) 

The cotangent complex for a general [[algebra over an operad]] in [[chain complexes]] is discussed in section 7 of

* {#Hinich} [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))


In terms of [[model category]] presentations for [[tangent (infinity,1)-categories]]:

* [[Yonatan Harpaz]], [[Joost Nuiten]], [[Matan Prasma]], _Tangent categories of algebras over operads_ ([arXiv:1612.02607](https://arxiv.org/abs/1612.02607))

* _The abstract cotangent complex and Quillen cohomology of enriched categories_ ([arXiv:1612.02608](https://arxiv.org/abs/1612.02608))


[[!redirects cotangent complexes]]