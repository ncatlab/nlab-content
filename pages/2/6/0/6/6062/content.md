
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There exists a [[model category]] structure on a [[category]] of [[dg-coalgebra]]s whose fibrant objects are precisely [[L-∞ algebra]]s.

## Definitions and Quillen equivalences

By definition [[L-∞ algebras]] are the [[∞-algebras]] in the [[category of chain complexes]] over the [[Lie operad]]. As such they carry a [[model structure on algebras over an operad]]. There is a strictification which leads equivalently to a [[model structure on dg-Lie algebras]].

One succinct way to present [[L-∞ algebras]] (as discussed there) is as [[dg-coalgebras]]:

+-- {: .num_defn }
###### Definition

An [[L-∞ algebra]] $(\mathfrak{g}, [-], [-,-], [-,-,-], \cdots)$ structure on a [[graded vector space]] $\mathfrak{g}$ is equivalently a [[dg-coalgebra]] structure on the graded-commutative [[cofree coalgebra]] over $\mathfrak{g}$.

Conversely, the [[category]] of [[L-∞ algebras]] (and general "weak" morphisms between them) is the [[full subcategory]] of that of counital cocommutative [[dg-coalgebras]] on those whose underlying bare graded-commutative [[coalgebra]] (forgetting the codifferential) is free

$$
  L_\infty Alg \hookrightarrow dgCoCAlk
  \,.
$$

=--

Accordingly it is of interest to have a also [[model structure on dg-coalgebras]] which presents $L_\infty$-algebras.


### On dg-Lie algebras

Let $k$ be a [[field]] of [[characteristic]] 0.

+-- {: .num_defn }
###### Definition

Write $dgLie_k \in Cat$ for the [[category]] of [[dg-Lie algebras]]
over $k$.

=--

+-- {: .num_prop #ModelStructureOnDgLieAlgebras}
###### Proposition

The category $dgLie_k$ carries a 
[[cofibrantly generated model category|cofibrantly generated]] 
[[model category]] structure in which

* [[fibrations]] are the degreewise [[surjective maps]];

* [[weak equivalences]] are the [[quasi-isomorphisms]]

on the underlying [[chain complexes]]. This is the 
[[transferred model structure]] of the corresponding 
[[model structure on chain complexes]] along the [[forgetful functor]]
to the [[category of chain complexes]].

=--

([Pridham, lemma 3.24](#Pridham))

We call this the **[[model structure on dg-Lie algebras]]**.


+-- {: .num_defn #SendingDGLieAlgebraToDgCoalgebra}
###### Definition

Write 

$$
  \mathcal{C} \;\colon\;  dgLie_k \to dgCoCAlg_k
$$

for the [[functor]] which sends a [[dg-Lie algebra]] $(\mathfrak{g},d,[-,-])$ to the [[dg-coalgebra]] whose underlying [[coalgebra]] is free on the underlying [[graded vector space]] $\mathfrak{g}$ and whose [[coderivation]] is given by

$$
  \delta \colon v_1 \mapsto d v_1
$$

$$  
  \delta \colon (v_1, v_2) \mapsto [v_1, v_2]
$$

and then extended as a coderivation.

=--

+-- {: .num_remark}
###### Remark

spring

=--


+-- {: .num_defn #SendingDGLieAlgebraToDgCoalgebra}
###### Definition

spring

=--

+-- {: .num_prop #LeftAdjointFromDgCoAlgToDgAlg}
###### Proposition

The functor from def. \ref{SendingDGLieAlgebraToDgCoalgebra} has 
a [[left adjoint]]

$$
  \mathcal{L} \;\colon\;   dgCoCAlg_k \to dgLie_k
  \,.
$$

=--

([Quillen, App. B6](#Quillen)) ([Hinich, 1.2.1, 2.2.5](#Hinich)) See also ([Pridham, def. 3.23](#Pridham)).

+-- {: .num_remark}
###### Remark

If one thinks of a [[dg-coalgebra]] as presenting a
a derived formal space, as discuss [below](#SheavesOverCosimplicialInfinitesimallyThickenedPoints)
then its image under $\mathcal{L}$, prop. \ref{LeftAdjointFromDgCoAlgToDgAlg}, 
may be thought of as its
_tangen dg-Lie algebra_. Therefore $\mathcal{L}$
is also called the **tangent Lie algebra functor**.

=--

([Hinich, 1.2.1](#Hinich))

### On dg-coalgebras

Let $k$ be a [[field]] of [[characteristic]] 0.

+-- {: .num_defn DGCoalgebrasCategory}
###### Definition

Write $dgCoCAlg_k \in Cat$ for the [[category]] of 
cocommutative counital $\mathbb{Z}$-[[graded object|graded]]
[[dg-coalgebras]] over $k$.

=--

+-- {: .num_prop #ModelStructureOnCocommutativeDGCoalgebras}
###### Proposition

There exists a [[model category]] structure on $dgCoCAlg_k$
for which

* the [[cofibrations]] are the morphisms that are degreewise [[injections]];

* the [[weak equivalences]] are the morphisms $f$ whose corresponding morphisms of [[dg-Lie algebras]] $\mathcal{L}(f)$, prop. \ref{LeftAdjointFromDgCoAlgToDgAlg}, is a [[quasi-isomorphism]] on the underlying [[chain complexes]].

=--

([Hinich, theorem 3.1](#Hinich)) See also ([Pridham, lemma 3.25](#Pridham)).

We call this the **[[model structure on dg-coalgebras]]**.

+-- {: .num_prop}
###### Proposition

The pair of [[adjoint functors]]

$$
  (\mathcal{L} \dashv \mathcal{C})
  \;\colon\;
  dgLie_k
   \stackrel{\overset{\mathcal{L}}{\leftarrow}}{\underset{\mathcal{C}}{\to}}
  dgCoCAlg_k
$$

from prop. \ref{LeftAdjointFromDgCoAlgToDgAlg} constitutes a [[Quillen equivalence]] between the [[model structure on dg-Lie algebras]], prop. \ref{ModelStructureOnDgLieAlgebras}, and the [[model structure on dg-coalgebras]], prop. \ref{ModelStructureOnCocommutativeDGCoalgebras}.

=--

([Hinich, theorem 3.2](#Hinich))

+-- {: .num_remark}
###### Remark

Since every object in $dgCoCAlg_k$ is a [[cofibrant object]] and every object in $dgLie_k$ is a [[fibrant object]], the composite

$$
  \mathcal{C}\mathcal{L}
  \colon
  dgCoCAlg_k
  \to 
  dgCocAlg_k
$$

is already its [[derived functor]] and the [[unit of an adjunction|unit]]

$$
  \mathfrak{g} \to \mathcal{C}\mathcal{L}\mathfrak{g}
$$

is a [[weak equivalence]] that exhibits $\mathcal{C}\mathcal{L}\mathfrak{g}$ as a [[fibrant resolution]] and moreover, if $\mathfrak{g}$ was already fibrant, hence by prop. \ref{spring} an [[L-∞ algebra]], as a **strictification** of $\mathfrak{g}$, by remark \ref{spring}.

=--



### $(\infty,1)$-Sheaves over cosimplicial infinitesimally thickened points
 {#SheavesOverCosimplicialInfinitesimallyThickenedPoints}


+-- {: .num_defn }
###### Definition

Write 

$$
  InfThPoint \hookrightarrow Alg^{op}
$$

for the category of [[infinitesimally thickened points]], the [[full subcategory]] of the [[opposite category]] of 
[[Artin algebras]] ("Weil alebras" in the language of [[synthetic differential geometry]]). The category of _[[infinitesimally thickened points]]_.

Write

$$
  cInfThPoint \hookrightarrow sAlg^{op} \simeq (Alg^{op})^{\Delta}
$$

for the [[full subcategory]] of the [[opposite category]] on [[simplicial algebras]] on those which are [[Artin algebra|Artinian]] (or "Weil" ): the category of [[cosimplicial object|cosimplicial]] [[infinitesimally thickened points]].

=--

+-- {: .num_defn }
###### Definition

Write

$$
  FormalSpace \coloneqq Fun^{lex}(InfThPoints^{op}, Set)
$$

for the [[full subcategory]] of the [[category of presheaves]] over [[infinitesimally thickened points]] on those given by [[left exact functors]].

=--

In ([Pridham](#Pridham)) this is def. 1.18.

+-- {: .num_defn }
###### Definition

Write

$$
  DerivedFormalSpace \coloneqq Fun^{lex}(cInfThPoints^{op}, sSet)
$$

for the [[full subcategory]] of the category of [[simplicial presheaves]] over [[cosimplicial object|cosimplicial]] infinitesimally thickened points on those given by [[left exact functors]].

=--

In ([Pridham](#Pridham)) this is def. 1.32.


+-- {: .num_theorem }
###### Theorem 

There exists a [[cofibrantly generated model category|cofibrantly generated]] [[model category]] structure on $DerivedFormalSpace$ whose

* [[weak equivalences]] are those morphisms $f \colon X \to Y$ which are [[local morphisms]] with respect to quasi-smooth maps $p \colon E \to Y$ in the [[homotopy category]] of the [[slice category]] over $Y$.

(...)

=--

This is ([Pridham, def. 2.7, theorem 2.14](#Pridham))

+-- {: .num_prop }
###### Proposition

Between quasi-smooth objects in $DerivedFormalSpace$ the weak equivalences are precisely the morphisms which are [[weak homotopy equivalences]] of simplicial sets over each object in $cInfThPoint$.

=--

This is ([Pridham, cor. 2.16](#Pridham)).


### dg infinitesimally thickened points

+-- {: .num_prop }
###### Proposition

If $k$ is of [[characteristic]] 0 then there is a [[zig-zag]] of [[Quillen equivalences]] between
$DerivedFormalSpace$ and $dgFormalSpace$.

=--

This is ([Pridham, cor. 4.49](#Pridham)).

+-- {: .num_prop }
###### Proposition

There is a [[Quillen equivalence]]

$$
  dgLie_k \stackrel{\simeq}{\to} dgFormalSpace
$$

=--

([Pridham, theorem 4.55](#Pridham))

+-- {: .num_prop }
###### Proposition

The inclusion

$$
  dgFormalSpace \to dgCoCAlg_k
$$

is the [[left adjoint]] part of a [[Quillen equivalence]].

=--

([Pridham, cor. 4.56](#Pridham))

## Properties


+-- {: .num_prop #QuillenEquivalence}
###### Proposition

There is a [[Quillen equivalence]]

$$
  dgCoAlg(k) \simeq DG_{\mathbb{Z}}Sp(k)
  \,.
$$

=--

([Pridham](#Pridham))

+-- {: .num_prop #RightProperness}
###### Proposition

The model category $DG_{\mathbb{Z}}Sp(k)$, def. \ref{DGSp}, is a [[right proper model category]].

=--

This observation has been communicated privatly by [[Jonathan Pridham]]

+-- {: .proof}
###### Proof

We need to show that the [[pullback]] of a weak equivalence $w$ along a fibration $f$ is again a weak equivalence. If $w$ is a fibration, this is automatic, so by factorisation we reduce to the case where $w$ is a cofibration. Now, every trivial cofibration is $Spf$ of a composition of acyclic small extensions, so we may take $w$ to be $Spf$ of an acyclic small extension $A \to B$ with [[kernel]] $I$. Then $f$ is $Spf$ of a quasi-free map $A \to R$, so the pullback is $Spf$ of $R \to R/IR$, and $IR =I\hat{\otimes}_A R$, so $R \to R/IR$ is also an acyclic small extension.

=--

## Related concepts

* [[model structure on dg-coalgebras]]

* [[model structure on dg-Lie algebras]]

## References

Precursors for 2-reduced dg-algebras are dicussed in 

* [[Dan Quillen]], _Rational homotopy theory_, Annals of Math., 90(1969), 205&#8211;295.
 {#Quillen}

The full model structure on dg-coalgebras (in characteristic 0) and the Quillen equivalence of dg-Lie algebras as well as the interpretation in terms of formal $\infty$-stacks is due to

* [[Vladimir Hinich]], _DG coalgebras as formal stacks_ ([arXiv:9812034](http://arxiv.org/abs/math/9812034))
 {#Hinich}

In 

* [[Jacob Lurie]], _[[Formal Moduli Problems]]_
 {#Lurie}

the relation to $\infty$-stacks is discussed more in detail.

More model category theoretic developments relating various of the previous approaches and generalizing to arbitrary characteristic are in

* [[Jonathan Pridham]], _Unifying derived deformation theories_, Adv. Math. 224 (2010), no.3, 772-826 ([arXiv:0705.0344](http://arxiv.org/abs/0705.0344))
 {#Pridham}


[[!redirects model structure for L-∞ algebras]]
