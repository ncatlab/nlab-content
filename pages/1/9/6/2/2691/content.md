
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

By the dual [[Dold-Kan correspondence]] cochain complexes in non-negative degree are equivalent to [[cosimplicial object|cosimplicial]] abelian groups. Moreover, the [[monoidal Dold-Kan correspondence]] maps [[cosimplicial algebra]]s to [[dg-algebra]]s, but this is no longer an equivalence of ordinary categories. It should, however, be an equivalence of the full [[(∞,1)-category|(∞,1)-categories]] of these objects. This, in turn, should be modeled by a [[model category]] structures.

The model structure on dg-algebras is such a model.

## General

The category of [[dg-algebra]]s is that of [[monoid]]s in a [[category of chain complexes]]. Accordingly general results on a [[model structure on monoids in a monoidal model category]] apply.  

Below we spellout special cases, such as restricting to commutative monoids when working over a field of characteristic 0, or restricting to non-negatively graded cochain dg-algebras.

## Non-negatively graded cochain dg-algebras

### Definition 

Write $dgAlg$ for the [[category]] of cochain [[dg-algebra]]s in non-negative degree over a [[field]] $k$ of characteristic 0. Write $C dgAlg \subset dgAlg$ for the [[subcategory]] of (graded-)commutative dg-algebras.

+-- {: .un_defn}
###### Definition

The  **projective** [[model category]] structure on $C dgAlg$ and on $dgAlg$ is given by setting:

* weak equivalences are the [[quasi-isomorphism]]s

* fibrations are the degreewise [[epimorphism|surjections]].

=--

+-- {: .un_prop }
###### Proposition

This indeed defines a [[model category]]. 

At least on $C dgAlg$ this is a [[cofibrantly generated model category]].

=--

+-- {: .proof}
###### Proof

See the references below.

=--

+-- {: .un_remark }
###### Remark
**(category of fibrant objects)**

Evidently every object in $dgAlg$ and in $C dgAlg$ is fibrant. Therefore these model categories structures are in particular also structures of a [[category of fibrant objects]].

=--

The nature of the cofibrations is discussed below.


### Properties

#### Cofibrations: Sullivan algebras {#SullivanAlgebras}

In this section we describe the cofibrations in the model structure on $C dgAlg_\mathbb{N}$ of **non-negatively graded** dg-algebras. Notice that it is these that are in the image of the dual [[monoidal Dold-Kan correspondence]].

Before we characterize the cofibrations, first some notation.

For $V$ a $\mathbb{Z}$-[[graded vector space]] write 
$\wedge^\bullet V$ for the [[Grassmann algebra]] over it. Equipped with the trivial differential $d = 0$ this is a [[semifree dga]] $(\wedge^\bullet V, d=0)$.

With $k$ our ground field we write $(k,0)$ for the corresponding dg-algebra, the tensor unit for the standard [[monoidal category|monoidal structure]] on $dgAlg$. This is the [[Grassmann algebra]] on the 0-vector space
$(k,0) = (\wedge^\bullet 0, 0)$.


+-- {: .un_def }
###### Definition
**(Sullivan algebras)**

A **relatived Sullivan algebra** is a [[morphism]] of dg-algebras that is an inclusion

$$
  (A,d) \to (A \otimes_k \wedge^\bullet V, d')
$$

for $(A,d)$ some dg-algebra and for $V$ some graded vector space, such that 

* there is a [[well ordered set]] $J$

* indexing a basis $\{v_\alpha \in V| \alpha \in J\}$ of $V$;

* such that with $V_{\lt \beta} = span(v_\alpha | \alpha \lt \beta)$ for all basis elements $v_\beta$ we have that 

  $$
    d' v_\beta \in A \otimes \wedge^\bullet V_{\lt \beta}
    \,.
  $$

This is called a **minimal** relative Sullivan algebra if in addition the condition

$$
  (\alpha \lt \beta) \Rightarrow (deg v_\alpha  \leq deg v_\beta)
$$

holds. For a Sullivan algebra $(k,0) \to (\wedge^\bullet V, d)$ relative to the tensor unit we call the [[semifree dga]] $(\wedge^\bullet V,d)$ simply a **Sullivan algebra**.  And a **minimal Sullivan algebra** if $(k,0) \to (\wedge^\bullet V, d)$ is a minimal relative Sullivan algebra.

=--

+-- {: .un_remark }
###### Remark

Sullivan algebras were introduced by [[Dennis Sullivan]] in his development of [[rational homotopy theory]]. This is one of the key application areas of the model structure on dg-algebras.

=--

+-- {: .un_remark }
###### Remark
**($L_\infty$-algebras)**

Because they are [[semifree dga]]s, Sullivan dg-algebras $(\wedge^\bullet V,d)$ are (at least for degreewise finite dimensional $V$) [[Chevalley-Eilenberg algebra]]s of [[L-∞-algebra]]s.

The co-commutative differential co-algebra encoding the corresponding [[L-∞-algebra]] is the free cocommutative algebra $\vee^\bullet V^*$ on the degreewise dual of $V$ with differential $D = d^*$, i.e. the one given by the formula

$$
  \omega(D(v_1 \vee v_2 \vee \cdots v_n)) =
  - (d \omega) (v_1, v_2, \cdots,  v_n)
$$

for all $\omega \in V$ and all $v_i \in V^*$.

=--


+-- {: .un_prop }
###### Proposition
**(cofibrations are relative Sullivan algebras)**

The cofibration in $C dgAlg_{\mathbb{N}}$ are precisely the [[retract]]s of relative  Sullivan algebras $(A,d) \to (A\otimes_k \wedge^\bullet V, d')$.

Accordingly, the cofibrant objects in $C dgAlg$ are precisely the Sullivan algebras $(\wedge^\bullet V, d)$

=--

+-- {: .un_def }
###### Definition
**(sphere and disk algebras)**

Write $k[n]$ for the graded vector space which is the ground field $k$ in degree $n$ and 0 in all other degrees. For $n \in \mathbb{N}$, consider the [[semifree dga]]s

$$
  S(n) := (\wedge^\bullet k[n], 0)
$$ 

and for $n \geq 1$ the [[semifree dga]]

$$
  D(n) := 
   \left\lbrace
     \array{
         0 & (n = 0)
         \\
        (\wedge^\bullet (k[n+1] \oplus k[n]), 0) & (n \gt 0)
     }
   \right.
  \,.
$$ 

Write

$$
  i_n : S(n) \to D(n)
$$

for the obvious morphism that takes the generator in degree $n$ to the generator in degree $n$ (and for $n = 0$ it is the unique morphism from the [[initial object]] $(0,0)$).

For $n \gt 0$ write

$$
  j_n : 0 \to D(n)
  \,.
$$

=--

+-- {: .un_def }
###### Definition
**(generating cofibrations)**

The sets

$$
  I = \{i_n \}_n \cup \{S(0) \to 0\}
$$

and 

$$
  J = \{j_n \}_{n \gt 0} 
$$

are sets of generating cofibrations and acyclic cofibrations, respectively, exhibiting $C dgAlg$ as a [[cofibrantly generated model category]].


=--


#### Commutative vs. non-commutative dg-algebras {#CommVsNoncomm}

+-- {: .un_prop }
###### Observation


The [[stuff, structure, property|forgetful functor]]

$$
  F :  CdgAlg \to dgAlg
$$

from (graded-)commutative [[dg-algebra]]s to dg-algebras is the [[right adjoint]] part of a [[Quillen adjunction]]

$$
  Ab
  :
  dgAlg 
   \stackrel{\leftarrow}{\to}
  CdgAlg
  :
  F
$$

=--

+-- {: .proof}
###### Proof

The forgetful functor clearly preserves fibrations and cofibrations. It has a [[left adjoint]], the free abelianization functor $Ab$, which sends a [[dg-algebra]] $A$ to its quotient $A/[A,A]$.

=--


+-- {: .un_theorem }
###### Theorem

Let the ground [[ring]] $k$ be a [[field]] of characteristic 0. Then every [[dg-algebra]] $A$ which has the structure of an [[algebra over an operad|algebra over]] the [[E-k-operad|E-∞ operad]] has a [[dg-algebra]] morphism $A \to A_c$ to a commutative dg-algebra $A_c$  which is

* a morphism of [[E-k-operad|E-∞ algebras]] (where $A_c$ has the obvious [[E-k-operad|E-∞ algebras]] structure)

* a weak weak equivalence in the model structure on dg-algebras (i.e. a [[quasi-isomorphism]] of the underlying cochain complexes).

=--

So this says that the weak equivalence classes of the commutative dg-algebras in the model category of all dg-algebras already exhaust the most general non-commutative but  homotopy-commutative dg-algebras.

+-- {: .proof}
###### Proof

This is in II.1.5 of 

* [[Igor Kriz]] and [[Peter May]], _Operads, algebras, modules and motives_ , Ast&#233;risque No 233 (1995)

=--


## Unbounded dg-algebras {#Unbounded}

### Definition


+-- {: .un_theorem }
###### Theorem

For $k$ a [[field]] of [[characteristic]] 0 let $dgcAlg$ be the category of undounded commutative dg-algebras. With fibrations the degreewise surjections and weak equivalences the [[quasi-isomorphism]]s this is a 

* [[model category]]

which is

* [[proper model category|proper]];

* [[combinatorial model category|combinatorial]].

=--

Discussion of this is in ([To&#235;nVezzosi](#ToenVezzosi)):

* in lemma 2.3.1.1 they state that $cdgAlg_+$ constitutes the first two items in a triple which they call an _HA context_ .

* this implies their assumption 1.1.0.4 which asserts properness and
  combinatoriality



## References



The cofibrantly generated model structure on **commutative** [[dg-algebra]]s is surveyed usefully for instance on p. 6 of 

* [[Kathryn Hess]], _Rational homotopy theory: a brief introduction_ ([arXiv](http://arxiv.org/abs/math.AT/0604626))

This makes use of the general discussion in section 3 of 

* [[Paul Goerss]], [[Kirsten Schemmerhorn]], _Model categories and simplicial methods_ Notes from lectures given at the University of Chicago, August 2004 ([arXiv](http://arxiv.org/abs/math.AT/0609537))



that obtains the model structure from the [[model structure on chain complexes]].

A standard textbook reference is section V.3 of

* [[Sergei Gelfand]], [[Yuri Manin]], _Methods of homological algebra_,  transl. from the 1988 Russian (Nauka Publ.) original. Springer 1996. xviii+372 pp. 2nd corrected ed. 2002.

An original reference seems to be

* A. Bousfield, V. Gugenheim, _On PL deRham theory and rational homotopy type_ Memoirs of the AMS 179 (1976)


For general **non-commutative** (or rather: not necessarily graded-commutative) dg-algebras a model structure is given in

* J.F. Jardine, _[[JardineModelDG.pdf:file]]_ , Cyclic Cohomology and Noncommutative Geometry, Fields Institute Communications, Vol. 17, AMS (1997), 55-58. 

This is also the structure used in 

* J.L. Castiglioni G. Corti&#241;as, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0306289v2))

where aspects of its relation to the [[model structure on cosimplicial rings]] is discussed. (See [[monoidal Dold-Kan correspondence]] for
more on this).

Disucssion of the model structure on unbounded dg-algebras over a field of characteristic 0 is in 

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _HAG II, geometric stacks and applicatons_ ([arXiv:math/0404373v4](http://arxiv4.library.cornell.edu/abs/math/0404373v4))
{#ToenVezzosi}

[[!redirects model structure on dg-rings]]
[[!redirects model structure on dg-algebra]]
[[!redirects Sullival algebra]]
[[!redirects model structures on dg-algebras]]