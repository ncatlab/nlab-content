
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

This entry describes the [[higher geometry]]/[[derived geometry]] modeled on [[(∞,1)-site]]s of formal duals of [[dg-algebra]]s, bounded or unbounded, over a [[field]] of [[characteristic]] 0.

The corresponding [[(∞,1)-topos]] is the context for classical [[rational homotopy theory]], which arises by forming [[function algebras on ∞-stacks]] over [[constant ∞-stack]]s. It is also the context in which classical and higher order [[Hochschild homology]] of algebras and dg-algebras arises naturally as the function $\infty$-algebra on [[free loop space object]]s.

## The $(\infty,1)$-toposes 

We discuss some basic aspects of the [[(∞,1)-topos]]es over [[(∞,1)-site]]s of formal duals of cdg-algebras and of cdg-algebras of functions on its objects.


### Over formal duals of non-positively graded cdg-algebras

Let $k$ be a [[field]] of [[characteristic]] 0, or more generally a commutative $\mathbb{Q}$-[[associative algebra|algebra]].


#### Definition

+-- {: .num_defn}
###### Proposition/Definition 

Write 

* $cdgAlg_k$ for the category of graded-commutative cochain [[dg-algebra]]s (meaning: with [[differential]] of degree +1) in arbitrary degree;

* $cdgAlk_k^-$ for the full [[subcategory]] on objects with vanishing [[cochain cohomology]] in positive degree, $H^{\bullet \geq 1}(-) = 0$.

There are the standard projective [[model structures on dg-algebras]] on these categories, whose weak equivalences are the [[quasi-isomorphism]]s and whose fibrations are the degreewise surjections. 

=--

This is considered in ([To&#235;n-Vezzosi, 2.3.1](#ToenVezzosiStacks))

+-- {: .num_defn}
###### Proposition/Definition 

Let

$$
  C \hookrightarrow ((cdgAlg_k^-)^{op})^\circ
$$

be a [[small (∞,1)-category|small]] full [[sub-(∞,1)-category]] of the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by this model structure, and let $C$ be equipped with the structure of a [[subcanonical coverage|subcanonical]] [[(∞,1)-site]].

Write

$$
  \mathbf{H} := Sh_{(\infty,1)}(C)
$$

for the [[(∞,1)-category of (∞,1)-sheaves]] on $C$. We have a derived [[Isbell duality]] 

$$
  (\mathcal{O} \dashv j) 
    : 
  (cdgAlg_k^{op})^\circ
   \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{j}{\to}}
  \mathbf{H}
$$

where the [[left adjoint|left]] [[adjoint (∞,1)-functor]] $\mathcal{O}$ is the [[Yoneda extension]] of the inclusion $cdgAlg^+_k \hookrightarrow cdgAlg_k$. 

=--

This is considered in ([Ben-ZviNadler](#Ben-ZviNadler)). See [[function algebras on ∞-stacks]] for details.


#### Properties

+-- {: .un_prop}
###### Proposition

The inclusion

$$
  cdgAlg^-_k \hookrightarrow cdgAlg_k
$$

is a _homotopical context_ in the sense of ([To&#235;nVezzosi, def. 1.1.0.11](#ToenVezzosiStacks)).


=--

This is ([To&#235;nVezzosi, lemma 2.3.11](#ToenVezzosiStacks)). We record the following implications of this statement

+-- {: .num_cor}
###### Corollary

$(cdgAlg_k, \otimes_k)$ is a [[symmetric monoidal category|symmetric]] [[monoidal model category]].

=--

+-- {: .num_cor}
###### Corollary

For $B \in (dgcAlg_k)_{proj}$ a cofibrant object, the [[tensor product]] with $B$ preserves weak equivalences.

=--

This follows from ([To&#235;nVezzosi, assumption 1.1.0.4](#ToenVezzosiStacks)).



+-- {: .num_cor #cdgAlgInclusionPreservesLimits}
###### Corollary

The inclusion

$$
  (cdgAlg_k^-)^{op} \hookrightarrow (cdgAlg_k)^{op}
$$

preserves [[homotopy limit]]s, hence the induced inclusion

$$
  ((cdgAlg_k^-)^{op})^\circ \hookrightarrow ((cdgAlg_k)^{op})^\circ
$$

preserves [[(∞,1)-limit]]s.

=--

This follows from ([To&#235;nVezzosi, assumption 1.1.0.6](#ToenVezzosiStacks)).

+-- {: .num_defn}
###### Definition

For $A \in cdgAlg_k$ a [[nLab:dg-algebra]], write

* $A Mod$ for its [[nLab:model structure on dg-modules|category of dg-modules]];

  This is naturally a [[nLab:symmetric monoidal category]].

* $cdgAlg_A := CMon(A Mod)$ for the [[category of commutative monoids]] in $A Mod$, the category of **cdg-$A$-algebras**.

=--

+-- {: .num_cor #ModelStructureOndgAAlgebras}
###### Corollary

For any $A\in cdgAlg_k$ say a morphism in $cdgAlg_A$ is

* a weak equivalence precisely if it is a [[nLab:quasi-isomorphism]];

* a fibration precisely if it is degreewise surjective.

This makes $cdgAlg_A$ into a [[model category]] that is

* [[combinatorial model category|combinatorial]];

* [[proper model category|proper]].

There is an [[equivalence of categories]] with the [[under category]] of cdg-algebras under $A$

$$
  cdgAlg_A \simeq A/cdgAlg_k
$$

which is a [[Quillen equivalence]] with respect to the standard [[model structure on an under category]] on the right.

=--

This is ([To&#235;nVezzosi, assumption 1.1.0.4, remark on p. 18](#ToenVezzosiStacks)).

+-- {: .num_cor}
###### Corollary

For $B \in cdgAlg_A$ cofibrant with respect to the model structure in
cor \ref{ModelStructureOndgAAlgebras}, the [[tensor product]] ([[base change]]) functor

$$
  B \otimes_A (-) : A Mod \to B Mod
$$

preserves weak equivalences.

=--

This is ([To&#235;nVezzosi, assumption 1.1.0.4](#ToenVezzosiStacks)).


+-- {: .num_prop}
###### Proposition

The [[monoidal Dold-Kan correspondence]] provides a [[Quillen equivalence]]

$$
  (\Gamma^{cmon} \dashv N_\bullet)
  : 
  cAlg_k^{\Delta^{op}}  
    \stackrel{\overset{\Gamma^{cmon}}{\leftarrow}}{\underset{N_\bullet}{\to}}
  cdgAlg_k^+ 
$$

(since $k$ is assumed to be of characteristic 0). Under this equivalence we have that $U \in cAlg_k \hookrightarrow cAlg_k^{\Delta^{op}} \hookrightarrow \mathbf{H}$ is $\mathcal{O}$-perfect:

$$
  \mathcal{O} (X^{K}) \simeq K \cdot \mathcal{O}(X)
$$ 

and this recovers the constructions discussed above in [The Hochschild chain complex of an associative algebra](#HochschildChainComplex).

=--

+-- {: .proof}
###### Proof

Since the [[(∞,1)-Yoneda embedding]] $y$ commutes with [[(∞,1)-limit]]s we have that the powering $(y(U))^{K} \simeq y(U^K)$ is still representable. Therefore 

$$
  \mathcal{O} ((y(U))^K) \simeq \mathcal{O}(U^K) \;\; 
  \in (cdgAlg_k^-)^{op} \hookrightarrow (cdgAlg_k)^{op}
$$

is simply the formal dual of $U^K$, which is $K \cdot \mathcal{O}(U)$ formed in $cdgAlg_k$  by formal duality. By the [above proposition](cdgAlgInclusionPreservesLimits) the inclusion 
$cdgAlg_k^- \hookrightarrow cdgAlg_k$ preserves this $(\infty,1)$-colimit.

=--


### Over formal duals of general cdg-algebras


(...)


## Applications

* [[Hochschild cohomology]]: section <a href="http://nlab.mathforge.org/nlab/show/Hochschild+cohomology#OvercdgAlgs">Higher order HH modeled on cdg-algebras</a>;

* [[rational homotopy theory]]: [[function algebras on ∞-stacks]]

* [[perfect ∞-stack]]s and their [[geometric ∞-function theory]]

* [[BRST-BV complex]]

## References

Various [[model category]] presentations of dg-geometry are presented in 

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications _ ([arXiv](http://arxiv.org/abs/math/0404373))
{#ToenVezzosiStacks}

The [[geometric ∞-function theory]] of [[perfect ∞-stack]]s in dg-geometry, and the corresponding [[Hochschild cohomology]] is considered in

* [[David Ben-Zvi|Ben-Zvi]], [[John Francis]],  [[David Nadler]], _Integral transforms and Drinfeld centers in derived algebraic geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))
{#Ben-ZviFrancisNadler}

The $(\mathcal{O} \dashv Spec)$-adjunction for dg-geometry is studied in 

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv:1002.3636](http://arxiv.org/abs/1002.3636))
{#Ben-ZviNadler}

The basic reference for the [[model structure on dg-algebras]] (see there for more details) for the commutative case over a field of characteristic 0 is

* [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))
{#Hinich}

Details on the use of this [[model category]] structure for modelling dg-spaces are in

* [[Kai Behrend]], _Differential graded schemes I: prefect resolving algebras_ ([arXiv:0212225](http://arxiv.org/abs/math/0212225))

* [[Kai Behrend]], _Differential Graded Schemes II: The 2-category of Differential Graded Schemes_ ([arXiv:0212226](http://arxiv.org/abs/math/0212226))

