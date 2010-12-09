
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

A [[model category]] structure on a category of [[dg-algebra]]s tends to present an [[(∞,1)-category]] of [[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]]. 

For dg-algebras bounded in negative or positive degrees, the [[monoidal Dold-Kan correspondence]] asserts that their model category structures are [[Quillen equivalence|Quillen equivalent]] to the corresponding [[model structure on simplicial algebras|model structure on (co)simplicial algebras]]. This case plays a central role in [[rational homotopy theory]].

The case of model structures on unbounded dg-algebras may be thought of as induced from this by passage to the [[derived geometry]] modeled on formal duaals of the bounded dg-algebras. This is described at [[dg-geometry]].


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

For $k$ a [[field]] of [[characteristic]] 0 let 

$$
  cdgAlg = CMon(Ch_\bullet(k))
$$ 

be the category of undounded commutative dg-algebras. With fibrations the degreewise surjections and weak equivalences the [[quasi-isomorphism]]s this is a 

* [[model category]]

which is

* [[proper model category|proper]];

* [[combinatorial model category|combinatorial]].

=--

The existence of the model structure follows from the general discussion at [[model structure on dg-algebras over an operad]]. 

Properness and combinatoriality is discussed in ([To&#235;nVezzosi](#ToenVezzosi)):

* in lemma 2.3.1.1 they state that $cdgAlg_+$ constitutes the first two items in a triple which they call an _HA context_ .

* this implies their assumption 1.1.0.4 which asserts properness and
  combinatoriality

### Properties

#### Derived tensor product

Let $cdgAg_k$ be the projective model structure on commutative unbounded dg-algebras from above

+-- {: .un_prop }
###### Proposition

For cofibrant $A \in cdgAlg_k$, the functor

$$
  A\otimes_k (-) : k Mod \to A Mod
$$

preserves [[quasi-isomorphism]]s.

For $A,B \in cdgAlg_k$, their [[derived functor|derived]] [[coproduct]] in $k Mod$ coincides in the [[homotopy category]] with the derived [[tensor product]] in $k Mod$: the morphism

$$
  A \coprod_k^{L} B \stackrel{}{\to} A \otimes_k^L B
$$

is an isomorphism in $Ho(k Mod)$.

=--

This follows by the above with ([To&#235;nVezzosi, assumption 1.1.0.4, and page 8](#ToenVezzosi)).


#### Derived hom-functor {#SimplicialHomObjects}

The model structure on unbounded dg-algebras is _almost_ $sSet_{Quillen}$-enriched. See the section <a href="http://ncatlab.org/nlab/show/model+structure+on+dg-algebras+over+an+operad#SimplicialEnrichment">simplicial enrichment</a> at [[model structure on dg-algebras over an operad]] for details.


+-- {: .un_def }
###### Definition

Let $k$ be a [[field]] of [[characteristic]] 0. Let 
$\Omega^\bullet_{poly} : sSet \to cdgAlg_k$ be the functor that assigns polynomial [[differential forms on simplices]].

For $A,B \in dgcAlg_k$ define the [[simplicial set]]

$$
cdgAlg_k(A,B) : ([n] \mapsto Hom_{cdgAlg_k})(A, B \otimes_k \Omega^\bullet_{poly}(\Delta[n]))
  \,.
$$

This extends to a functor

$$
  cdgAlg_k(-,-) : cdgAlg_k^{op} \times cdgAlg_k \to sSet
  \,.
$$

=--

+-- {: .un_prop }
###### Proposition

The functor $cdgAlg_k(-,-)$ satisfies the duall of the [[pushout-product axiom]]: for $i : A \to B$ any cofibration in $cdgAlg_k$ and $p : X \to Y$ any fibration, the canonical morphism

$$
  (i^*, p_*) : cdgalg_k(A,B) \to 
    cdgAlg_k(A,X)
      \times_{cdgAlg_k(A,Y)} cdgAlg_k(B,Y)
$$

is a [[Kan fibration]], which is acyclic if $i$ or $p$ is.

=--

This follows ([BousfieldGugenheim, prop. 5.3](#BousfieldGugenheim)). See also the discussion at [[model structure on dg-algebras over an operad]].

+-- {: .un_prop }
###### Proposition

For $A \in cdgAlg$ cofibant, $cdgAlg_k(A,B)$ is the correct [[derived hom-space]]


$$
  cdgAlg_k(A,B)
  \simeq
  \mathbb{R}Hom(A,B)   
  \,.
$$

=--

> The following proof needs to be scrutinized.

+-- {: .proof}
###### Proof

By the assumption that $A$ is cofibrant and according to the facts discussed at [[derived hom-space]], we need to show that

$$
  s B : [n] \mapsto B\otimes_k \Omega^\bullet_{poly}(\Delta[n])
$$

is a [[simplicial resolution|resolution]], or _simplicial frame_ for $B$. (Notice that every object is fibrant in $cdgAlg_k$).

Since polynomial differential forms are acyclic on simplices (discussed [here](http://nlab.mathforge.org/nlab/show/differential+forms+on+simplices)) it follows that 

$$
  const B \to s B
$$

is degreewise a weak equivalence. It remains to show that $s A$ is fibrant in the [[Reedy model structure]] $[\Delta^{op}, cdgAlg_k]_{Reedy}$. 

One finds that the matching object is given by

$$
  (match s B)_k = B \otimes \Omega^\bullet_{poly}(\partial \Delta[k])
  \,.
$$

Therefore $s B$ is Reedy fibrant if in each degree the morphism 

$$
  (s B_k \to (match s B)_k ) = (\Omega^\bullet_{poly}(\partial \Delta[k] \hookrightarrow \Delta[k]))
$$

is a fibration. But this follows from the fact that $\Omega^\bullet_{poly} : sSet \to cdgAlg_k^{op}$ is a left [[Quillen adjunction|Quillen functor]] (as discussed at [[differential forms on simplices]]).
=--

#### Derived copowering over $sSet$ {#DerivedCopowering}

We discuss a concrete model for the $(\infty,1)$-copowering of 
$(cdgAlg_k)^\circ$ over [[∞Grpd]] in terms of the ordinary [[copowering]] of the [[category of chain complexes]] $Ch^\bullet(k)$ over [[sSet]].

+-- {: .un_prop}
###### Proposition

The [[(∞,1)-limit|(∞,1)-copowering]] of $(dgcAlg_k)^\circ$ over [[∞Grpd]] is modeled by the ordinary [[copowering]] of the underlying [[category of chain complexes]] over [[sSet]].

=--



+-- {: .proof}
###### Proof

This follows from ([GinotTradlerZeinalian, theorem 4.2.7](#GinotTradlerZeinalian)), which asserts that the [[derived functor]] of this tensoring is the unique [[(∞,1)-functor]], up to equivalence, satisfying the axioms of $(\infty,1)$-copowering.

> here is something that is almost an alternative proof, to be polished or to be discarded

Pass to the [[Quillen equivalence|Quillen equivalent]] [[simplicial model category]] $[\Delta^{op}, dgcAlg_k]$ whose weak equivalences are those morphisms that become weak equivalences in $dgcAlg_k$ under [[homotopy colimit]] over $\Delta^{op}$ (described at [[simplicial model category]]). In that structure $(\infty,1)$-copowering is modeled by the [[derived functor]] of the ordinary copowering (as discussed at [[(∞,1)-colimit|(∞,1)-copowering]]). 

Along the line of the rectification theorems at [[model structure on algebras over an operad]] we shouldd have that the model structure on the [[category of monoids|model structure on commutative monoids]] $dgCAlg_k = CMon(Ch_\bullet(k))$ [[presentable (∞,1)-category|presents]] the [[(∞,1)-category]] of [[commutative monoids in a symmetric monoidal (∞,1)-category]].

As described there, $(\infty,1)$-colimits of such commutative monoids over [[sifted (∞,1)-categories]] are computed in the underlying symmetric monoidal $(\infty,1)$-category.

By a result discussed at [[sifted (∞,1)-category]] the opposite of the [[simplex category]] is a sifted $(\infty,1)$-category.

So finally we have that the homotopy colimit over simplicial cdg-algebras is computed in the model structure of the underlying chain complexes.

=--

+-- {: .un_prop}
###### Observation

This 1-categorical copowering of the chain complexes underlying a dgc-algebra is what is described in ([GinotTradlerZeinalian, def 3.1.1](#GinotTradlerZeinalian)):

(...)


=--

+-- {: .un_prop}
###### Corollary


This 1-categorical [[copowering]] model of the $(\infty,1)$-categorical copowering preserves [[homotopy colimit]]s of simplicial sets.

=--

+-- {: .proof}
###### Proof


Given all of the above, this is ([GinotTradlerZeinalian, theorem 4.2.2 (3)](#GinotTradlerZeinalian)) .


=--


+-- {: .un_prop}
###### Proposition

The copowering

$$
  sSet \times cdgAlg_k \to cdgAlg_k
$$

preserves weak equivalences in both arguments.

=--

This is essentially due to ([Piashvili](#Pirashvili)). The full statement is ([GinotTradlerZeinalian, prop. 4.2.1](#GinotTradlerZeinalian)).


+-- {: .un_remark}
###### Remark

This means that the assumption of section [Pirashvili's higher Hochschild homology](#PirashviliHigherOrder) is satisfied, and that we may compute higher order Hochschild homology in $\mathbf{H}$ by copowering in $cdgAlg$ over $sSet$.

=--


#### Derived powering over $sSet$ {#DerivedPowering}


+-- {: .un_prop}
###### Claim

Let $S \in \infty Grpd$ be presented by a degreewise finite [[simplicial set]] (which we denote by the same symbol).

Then the [[homotopy limit]] in $cdgAlg_k$ over the $S$-shaped diagram constant on $k$ is given by $\Omega^\bullet_{poly}(S)$.

$$
  \mathbb{R}{\lim_{\leftarrow}}_S const k \simeq \Omega^\bullet_{poly}(S) 
  \,.
$$

=--

Here is a rough writeup of the proof, to be polished:

+-- {: .proof}
###### Proof

We show dually that for degreewise finite $S$ the assignment $(S, Spec A) \mapsto Spec (\Omega^\bullet_{poly}(S) \otimes A)$ models the $\infty$-copowering in $cdgAlg_k^{op}$.

By the discussion at <a href="http://nlab.mathforge.org/nlab/show/limit+in+a+quasi-category#Tensoring">(∞,1)-copowering</a> it is sufficient to to establish an equivalence

$$
  (dgcAlg_{k}^{op})^\circ(Spec (\Omega^\bullet_{poly}(S) \otimes A), Spec B)
  \simeq
   \infty Grpd(S, (dgcAlg_{k}^{op})^\circ(Spec A, Spec B))
$$

natural in $B$. Consider a cofibrant model of $B$, which we denote by the same symbol. The we compute (1-categorically)

$$
  \begin{aligned}
    sSet(S, cdgAlg_k^{op}(Spec A,Spec B))
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot Hom_{sSet}(S \times \Delta[r], 
        cdgAlg_k^{op}(Spec A, Spec B))
   \\
   & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
      \int_{[k] \in \Delta}
       Hom_{Set}(S_k \times \Delta[k,r], 
        Hom_{cdgAlg_k^{op}}(Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))   
   \\
   & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
      \int_{[k] \in \Delta} 
        Hom_{cdgAlg_k^{op}}((S_k \times \Delta[k,r]) \cdot Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))   
    \\
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
        Hom_{cdgAlg_k^{op}}(\int^{[k] \in \Delta} 
 (S_k \times \Delta[k,r]) \cdot Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))       
    \\
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
        Hom_{cdgAlg_k^{op}}(Spec \Omega^\bullet_{poly}(S \times \Delta[r]) \times Spec A, Spec B))       
  \end{aligned}
  \,,
$$

where all steps are isomorphisms and the dot denotes the ordinary 1-categorical [[copower]]ing of the category $cdgAlg^{op}$ over $Set$. In the last step we are using that the tensor product commutes with finite limits of dg-algebras. (This is where the finiteness assumption is needed). 

Now we use that by Eilenberg-Zilber etc. pp. (see for instance Hess, page 12) we have a quasi-isomorphism

$$
  \Omega^\bullet_{poly}(S \times \Delta[r])
  \simeq
  \Omega^\bullet_{poly}(S) \otimes \Omega_{poly}^\bullet(\Delta[r])
  \,.
$$

This being a weak equivalence between fibrant objects and since $B$ is assumed cofibrant, we have by the [above discussion](#SimplicialHomObjects) of the derived hom-functor (and using the [[factorization lemma]]) a weak equivalence

$$
  \cdots \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
        Hom_{cdgAlg_k^{op}}(Spec \Omega^\bullet_{poly}(S) \times Spec \Omega^\bullet_{poly}\Delta[r]) \times Spec A, Spec B))       
  \,.
$$

This being natural in $B$, this proves the claim. 

=--


## Related concepts

* [[model structure on dg-operads]]

* [[model structure on dg-algebras over an operad]]

  * **model structure on dg-algebras**

  * [[model structure on dg-categories]]


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
{#BousfieldGugenheim}

For general **non-commutative** (or rather: not necessarily graded-commutative) dg-algebras a model structure is given in

* J.F. Jardine, _[[JardineModelDG.pdf:file]]_ , Cyclic Cohomology and Noncommutative Geometry, Fields Institute Communications, Vol. 17, AMS (1997), 55-58. 

This is also the structure used in 

* J.L. Castiglioni G. Corti&#241;as, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0306289v2))

where aspects of its relation to the [[model structure on cosimplicial rings]] is discussed. (See [[monoidal Dold-Kan correspondence]] for
more on this).

Disucssion of the model structure on unbounded dg-algebras over a field of characteristic 0 is in 

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _HAG II, geometric stacks and applicatons_ ([arXiv:math/0404373v4](http://arxiv4.library.cornell.edu/abs/math/0404373v4))
{#ToenVezzosi}

A general discussion of algebras over an operad in unbounded chain complexes is in

* [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))
{#Hinich}

The derived copowering of unbounded commutative dg-algebras over $sSet$ is discussed (somewhat implicitly) in

* [[Grégory Ginot]], Thomas Tradler, Mahmoud Zeinalian, _Derived higher Hochschild homology, topological chiral homology and factorization algebras_, ([arxiv/1011.6483](http://arxiv.org/abs/1011.6483))
{#GinotTradlerZeinalian}


For more see [[model structure on dg-algebras over an operad]].

[[!redirects model structure on dg-rings]]
[[!redirects model structure on dg-algebra]]
[[!redirects Sullival algebra]]
[[!redirects model structures on dg-algebras]]