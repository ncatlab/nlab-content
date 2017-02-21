


#Contents#
* table of contents
{:toc}

## Projective model structure on Non-negatively graded cochain dgc-algebras

We discuss the projective model structure on 
[[differential graded-commutative algebras|differential non-negatively graded-commutative algebras]]. This was originally introduced in [Bousfield-Gugenheim 76](#BousfieldGugenheim76) as a [[model category]] for [[Dennis Sullivan]]'s approach to [[rational homotopy theory]].

### Definition 

+-- {: .num_defn #dgcCochainAlgebrasInNonNegativeDegrees}
###### Definition


For $k$ a [[field]] of [[characteristic zero]], write 

$$
  dgcAlg^{\geq 0}_{k}
$$ 

for the [[category]] of [[differential graded-commutative algebras]] over $k$ in non-negative degrees, equivalently the category of [[commutative monoids]] in the [[symmetric monoidal category]] $Ch^{\geq 0}(k)$ of [[cochain complexes]] in non-negative degrees, equipped with the [[tensor product of chain complexes]].

=--

+-- {: .num_defn #dgcCochainAlgebraInNonNegDegreeOfFiniteType}
###### Definition
**(finite type)**

Say that a [[dgc-algebra]] $A \in dgcAlg^{\geq 0}_k$ (def. \ref{dgcCochainAlgebrasInNonNegativeDegrees}) is of _[[finite type]]_ if its [[forgetful functor|underlying]] [[chain complex]] is in each degree of [[finite number|finite]] [[dimension]] as a $k$-[[vector space]].

=--

+-- {: .num_defn #ProjectiveModelStructureOnCdgAlg}
###### Definition

Write $(dgcAlg^{\geq 0}_k)_{proj}$ for the catgory of [[dgc-algebras]] from def. \ref{dgcCochainAlgebrasInNonNegativeDegrees} equipped with the following [[classes]] of morphisms:

* _weak equivalences_ are those [[homomorphisms]] of dg-algebras whose underlying [[chain map]] is  [[quasi-isomorphism]];

* _fibrations_ are those [[homomorphisms]] which are degreewise [[surjections]];

=--

+-- {: .num_prop #IndeedProjectiveModelStructureOnCdgAlg}
###### Proposition

The category $(dgcAlg^{\geq 0}_k})_{proj}$ from def. \ref{ProjectiveModelStructureOnCdgAlg} is a [[model category]], to be called the _projective model structure_.


=--

([Bousfield-Gugenheim 76, theorem 4.3](#BousfieldGugenheim76))


+-- {: .num_remark }
###### Remark
**(category of fibrant objects)**

Evidently every object in $(dgcAlg^{\geq 0}_k)_{proj}$ (def. \ref{ProjectiveModelStructureOnCdgAlg}, prop. \ref{IndeedProjectiveModelStructureOnCdgAlg}) is fibrant. Therefore these model categories structures are in particular also structures of a [[category of fibrant objects]].

=--

The nature of the cofibrations is discussed [below](#SullivanAlgebras).


### Properties

#### Cofibrations and Sullivan algebras
 {#SullivanAlgebras}

+-- {: .num_defn }
###### Definition
**(sphere and disk algebras)**

Write $k[n]$ for the graded vector space which is the ground field $k$ in degree $n$ and 0 in all other degrees. For $n \in \mathbb{N}$, consider the [[semifree dgc-algebras]]

$$
  S(n) \coloneqq (\wedge^\bullet k[n], 0)
$$ 

and for $n \geq 1$ the [[semifree dgc-algebras]]

$$
  D(n) 
   \coloneqq
   \left\lbrace
     \array{
         0 & (n = 0)
         \\
        (\wedge^\bullet (k[n] \oplus k[n-1]), 0) & (n \gt 0)
     }
   \right.
$$ 

for which the differential sends the generator of $k[n-1]$ to that of $k[n]$

Write

$$
  i_n \colon S(n) \to D(n)
$$

for the obvious morphism that takes the generator in degree $n$ to the generator in degree $n$ (and for $n = 0$ it is the unique morphism from the [[initial object]] $(0,0)$).

For $n \gt 0$ write

$$
  j_n \colon k[0] \to D(n)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition
**(generating cofibrations)**

The sets

$$
  I = \{i_n \}_{n \geq 1} \cup \{k[0] \to S(0), S(0) \to k[0]\}
$$

and 

$$
  J = \{j_n \}_{n \gt 1} 
$$

are sets of generating cofibrations and acyclic cofibrations, respectively, exhibiting the model category $(dgcAlg^{\geq 0}_k)_{proj}$ from prop. \ref{IndeedProjectiveModelStructureOnCdgAlg} as a [[cofibrantly generated model category]].


=--

review includes ([Hess 06, p. 6](#Hess06))


In this section we describe the cofibrations in the model structure on $(dgcalg^{\geq 0}_k)_{proj}$ (def. \ref{ProjectiveModelStructureOnCdgAlg}, prop. \ref{IndeedProjectiveModelStructureOnCdgAlg}). Notice that it is these that are in the image of the dual [[monoidal Dold-Kan correspondence]].

Before we characterize the cofibrations, first some notation.

For $V$ a $\mathbb{Z}$-[[graded vector space]] write 
$\wedge^\bullet V$ for the [[Grassmann algebra]] over it. Equipped with the trivial differential $d = 0$ this is a [[semifree dga]] $(\wedge^\bullet V, d=0)$.

With $k$ our ground field we write $(k,0)$ for the corresponding dg-algebra, the tensor unit for the standard [[monoidal category|monoidal structure]] on $dgAlg$. This is the [[Grassmann algebra]] on the 0-vector space
$(k,0) = (\wedge^\bullet 0, 0)$.


+-- {: .num_defn }
###### Definition
**(Sullivan algebras)**

A **[[relative Sullivan algebra]]** is a [[morphism]] of dg-algebras that is an inclusion

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

This is called a **minimal** [[relative Sullivan algebra]] if in addition the condition

$$
  (\alpha \lt \beta) \Rightarrow (deg v_\alpha  \leq deg v_\beta)
$$

holds. For a Sullivan algebra $(k,0) \to (\wedge^\bullet V, d)$ relative to the tensor unit we call the [[semifree dga]] $(\wedge^\bullet V,d)$ simply a **Sullivan algebra**.  And a **minimal Sullivan algebra** if $(k,0) \to (\wedge^\bullet V, d)$ is a minimal relative Sullivan algebra.

=--

+-- {: .num_remark }
###### Remark

Sullivan algebras were introduced by [[Dennis Sullivan]] in his development of [[rational homotopy theory]]. This is one of the key application areas of the model structure on dg-algebras.

=--

+-- {: .num_remark }
###### Remark
**($L_\infty$-algebras)**

Because they are [[semifree dgas]], Sullivan dg-algebras $(\wedge^\bullet V,d)$ are (at least for degreewise finite dimensional $V$) [[Chevalley-Eilenberg algebra]]s of [[L-∞-algebra]]s.

The co-commutative differential co-algebra encoding the corresponding [[L-∞-algebra]] is the free cocommutative algebra $\vee^\bullet V^*$ on the degreewise dual of $V$ with differential $D = d^*$, i.e. the one given by the formula

$$
  \omega(D(v_1 \vee v_2 \vee \cdots v_n)) =
  - (d \omega) (v_1, v_2, \cdots,  v_n)
$$

for all $\omega \in V$ and all $v_i \in V^*$.

=--


+-- {: .num_prop }
###### Proposition
**(cofibrations are relative Sullivan algebras)**

The cofibration in $(dgcAlg^{\geq 0}_{k})_{proj}$ are precisely the [[retract]]s of [[relative  Sullivan algebras]] $(A,d) \to (A\otimes_k \wedge^\bullet V, d')$.

Accordingly, the cofibrant objects in $(dgcAlg^{\geq 0}_{k})_{proj}$ are precisely the Sullivan algebras $(\wedge^\bullet V, d)$

=--


#### Hom-complexes
 {#HomComplexes}

We discuss [[simplicial set|simplicial]] [[mapping spaces]] between [[dgc-algebras]]. These _almost_ make the projective model structure $(dgcAlg^{\geq 0}_k)_{proj}$ from prop. \ref{IndeedProjectiveModelStructureOnCdgAlg} into a [[simplicial model category]], except that the [[tensoring]]/[[powering]] [[isomorphism]] holds only for [[finite set|finite]] [[simplicial sets]] or else on [[dgc-algebras]] of [[finite type]]. Still, this has useful implications, for instance it implies that the [[reduced suspension]] and [[loop space]] [[adjunction]] on [augmended algebras|augmented]] [[dg-algebras]] is a [[Quillen adjunction]].


+-- {: .num_defn #MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees}
###### Definition
**(simplicial mapping spaces)**

For $A,B \in dgcAlg^{\geq 0}_k$ (def. \ref{dgcCochainAlgebrasInNonNegativeDegrees}), let 

$$
  Maps(A,B)
  \in 
  sSet
$$

be the [[simplicial set]] whose [[n-simplices]] are the dg-algebra [[homomorphisms]] from $A$ into the [[tensor product]] of $B$ with the de Rham complex of [[polynomial differential forms on the n-simplex]] $\Omega_{poly}^\bullet(\Delta^n)$.

$$
  Maps(A,B)_n
   \;\coloneqq\;
  Hom_{dgcAlg^{\geq 0}_k}
  \left(
    A, \; \Omega^\bullet_{poly}(\Delta^n) \otimes_k B 
  \right)
$$

and whose face and degeneracy maps are the obvious ones induced from the fact that $\Omega_{poly}^\bullet \colon \Delta^{op} \to dgcAlg^{\geq 0}_k$ is canonically a [[simplicial object]] in dgc-algebras.

We also call this the _simplicial [[mapping space]]_ from $A$ to $B$. This construction naturally extends to a [[functor]]

$$
  Maps(-,-)
  \;\colon\;
  (dgcAlg^{\geq 0}_k)^{op}
  \times
  dgcAlg^{\geq 0}_k
    \longrightarrow
   dgcAlg^{\geq 0}_k
$$

from the [[product category]] of the [[opposite category]] of [[dgc-algebras]] with the category itself.

Observe that 

$$
  Hom_{dgcAlg^{\geq 0}_k}
  \left(
    A, \; \Omega^\bullet_{poly}(\Delta^n) \otimes_k B 
  \right)
  \;\simeq\;
  {}_{\Omega^\bullet_{poly}}Hom_{dgcAlg^{\geq 0}_k}
  \left(
     \Omega^\bullet_{poly}(\Delta^n) \otimes_k A
     \,,\,
     \Omega^\bullet_{poly}(\Delta^n) \otimes_k B
  \right)  
  \,,
$$

where on the right we have those dg-algebra homomorphism which in addition preserves the left [[dg-module]] structure over $\Omega^\bullet_{poly}(\Delta^n)$. This induces for any three $A,B,C \in dgcAlg^{\geq 0}_k$ a [[composition]] homomorphism of [[simplicial sets]] out of the [[Cartesian product]] of mapping spaces

$$
  \circ^{sSet}_{A,B,C}
  \;\colon\;
  Maps(A,B) \times Maps(B,C)
    \longrightarrow
  Maps(A,C)
  \,.
$$


=--

([Bousfield-Gugenheim 76, 5.1](#BousfieldGugenheim76))

+-- {: .num_remark}
###### Remark

The set of 0-simplices of of the [[mapping space]] $Maps(A,B)$ in def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees} is [[natural isomorphism|naturally isomorphic]] to the ordinary [[hom-set]] of dg-algebras:


$$
  Maps(A,B)_0 \simeq Hom_{dgcAlg^{\geq 0}_k}(A,B)
$$

and under this identification the two notions of [[composition]] agree.

=--

Definition \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees} makes $dgcAlg^{\geq 0}_k$ an [[sSet]]-[[enriched category]] ("[[simplicial category]]"). The follows says that it is also [[powering|powered]], not over all of $sSet$, but over finite simplicial sets: 

+-- {: .num_prop #PoweringOfdgcCchainAlgebrasInNonNegativeDegreeOverFiniteSimplicialSets}
###### Proposition
**(powering over finite simplicial sets)**

For $A, B \in dgcAlg^{\geq 0}_k$ and $S \in $ [[sSet]], there is a [[natural transformation]]

$$
  Hom_{dgcAlg^{\geq}_k}(A, \Omega^\bullet_{poly}(S) \otimes_k B)
   \longrightarrow
  Hom_{sSet}( S, Maps(A,B) )
$$

from the [[hom-set]] of [[dgc-algebras]] into the [[tensor product]] with the [[polynomial differential forms on n-simplices]] from def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees} to the [[hom-set]] in [[simplicial sets]] into the simplicial [[mapping space]] from def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees}. 

Moreover, this morphism is an [[isomorphism]] if one of the following conditions holds:

* $S$ is a [[finite set|finite]] [[simplicial set]];

* $B$ is of [[finite type]] (def. \ref{dgcCochainAlgebraInNonNegDegreeOfFiniteType}).

=--

([Bousfield-Gugenheim 76, lemma 5.2](#BousfieldGugenheim76))

+-- {: .num_prop}
###### Proposition
**(pullback powering axiom)**

Let $i \colon V \to W$ and $p \colon X \to Y$ be two [[morphisms]] in $dgcAlg^{\geq 0}_k$. Then their [[pullback power]] with respect to the simplicial [[mapping space]] functor (def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees})

$$
  p^i
  \;\colon\;
  Maps(W,X)
   \longrightarrow
  Maps(V,X)
   \underset{Maps(V,Y)}{\times}
  Maps(W,Y)
$$

is 

1. a [[Kan fibration]] if $i$ is a cofibration and $p$ a fibration in the projective [[model category]] structure from prop. \ref{IndeedProjectiveModelStructureOnCdgAlg};

1. in addition a [[weak homotopy equivalence]] (i.e. a weak equivalence in the [[classical model structure on simplicial sets]]) if at least one of $i$ or $p$ is a weak equivalence in the projective model structure from prop. \ref{IndeedProjectiveModelStructureOnCdgAlg}.

=--

([Bousfield-Gugenheim 76, prop. 5.3](#BousfieldGugenheim76))

+-- {: .num_remark}
###### Remark

Prop. \ref{PoweringOfdgcCchainAlgebrasInNonNegativeDegreeOverFiniteSimplicialSets} _would_ say that $(dgcAlg^{\geq 0}_k)_{proj}$ is a [[simplicial model category]] with respect to the simplicial enrichment from def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees} were it not for the fact that prop. \ref{PoweringOfdgcCchainAlgebrasInNonNegativeDegreeOverFiniteSimplicialSets} gives the [[powering]] only over finite simplicial sets.

=--


#### Commutative vs. non-commutative dg-algebras 
 {#CommVsNoncomm}

> this needs harmonization

+-- {: .num_prop }
###### Proposition


The [[forgetful functor]]

$$
  F dgcAlg_k \to dgAlg_k
$$

from (graded-)commutative [[dg-algebra]]s to dg-algebras is the [[right adjoint]] part of a [[Quillen adjunction]]

$$
  Ab
  \colon
  dgAlg 
   \stackrel{\leftarrow}{\to}
  CdgAlg
  :
  F
$$

=--

> boundedness?

+-- {: .proof}
###### Proof

The forgetful functor clearly preserves fibrations and cofibrations. It has a [[left adjoint]], the free abelianization functor $Ab$, which sends a [[dg-algebra]] $A$ to its quotient $A/[A,A]$.

=--


+-- {: .num_theorem }
###### Theorem

Let the ground [[ring]] $k$ be a [[field]] of [[characteristic zero]]. Then every [[dg-algebra]] $A$ which has the structure of an [[algebra over an operad|algebra over]] the [[E-k-operad|E-∞ operad]] has a [[dg-algebra]] morphism $A \to A_c$ to a commutative dg-algebra $A_c$  which is

* a morphism of [[E-k-operad|E-∞ algebras]] (where $A_c$ has the obvious [[E-k-operad|E-∞ algebras]] structure)

* a weak weak equivalence in the model structure on dg-algebras (i.e. a [[quasi-isomorphism]] of the underlying cochain complexes).

=--

This is in ([Kriz-May 95, II.1.5](#KrizMay95)).

So this says that the weak equivalence classes of the commutative dg-algebras in the model category of all dg-algebras already exhaust the most general non-commutative but  homotopy-commutative dg-algebras.

+-- {: .num_remark #HomotopyFaithfulnessOfforgettingCommutativity}
###### Remark

Discussion of a restricted kind of homotopy-faithfulness of the forgetful functor from the homotopy theory of commutative to not-necessarily commutative dg-algebras is in ([Amrani 14](#Amrani14)).

=--


