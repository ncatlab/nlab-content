
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

To every [[quantum mechanical system]] is associated its _Bohr topos_ : a [[ringed topos]] which plays the role of the quantum [[phase space]]. The idea of this construction -- _Bohrification_ -- is that it naturally captures the [[geometry|geometric]] and [[logic|logical]] aspects of [[quantum physics]] in terms of [[higher geometry]]/[[topos theory]].

One way to understand Bohrification is as a generalization of the construction of the [[Gelfand spectrum]] of a commutative [[C-star algebra]]s to a context of _noncommutative_ $C^*$-algebras. It assigns to a noncommutative $C^*$-algebra $A$ a generalized [[Gelfand spectrum]] in the form of a [[locale]] $\underline{\Sigma}_A$ [[internalization|internal]] to the [[sheaf topos]] $\mathcal{T}_A$ over the [[semilattice of commutative subalgebras]] of $A$, or  equivalently its externalization $\Sigma_A \to \mathcal{C}(A)$ regarded as a [[locale]] [[over category|over]] the locale of open subalgebras.

When applied to subalgebras of [[bounded operator]]s on a [[Hilbert space]] this construction has been suggested to formalize faithfully and usefully a heuristic that has goes back to [[Nils Bohr]] and is known as the _doctrine of classical concepts_ ([Scheibe](#Scheibe)) in [[quantum mechanics]]. This states that  nonclassical/noncommutative as the [[logic]]/[[geometry]] of quantum mechanics may be, it is to be probed and detected by classical/commutative logic/geometry. In _Bohrification_ this heuristics is formalized by the [[semilattice of commutative subalgebras]] and various entities induced by this [[posite]]. The internal [[locale]] $\underline{\Sigma}_A$ may be thought of as an incarnation of the quantum [[phase space]] encoded by $A$.

One thing that is nice about [[Bohrification]] is that it makes the following statement true: "[[quantum mechanics|quantum]] [[states]] on a quantum algebra $A$ are precisely [[classical mechanics|classical]] states [[internalization|internal]] to the Bohrified ringed topos corresponding to $A$".

This is essentially a direct re-interpretation of [[Gleason's theorem]]: this theorem says that quantum states on $A$ are already fixed by demanding them to be maps on $A$ that are (positive, normed) linear functions on all commutative subalgebras of $A$. Now, the immediate formalization of a map $A \to \mathbb{C}$ that is required to preserve certain structure on all commutative subalgebras is a fully structure-preserving function, but _internal_ to the [[presheaf topos]] over the comutative subalgebras. That presheaf topos is the "Bohrification" of $A$.

## Outline

The discussion below proceeds in the following steps (following ([Nuiten11](#Nuiten)))

1. [Bohr topos of a quantum mechanics system](#BohrToposOfQMSystem)

   This discusses the Bohr topos incarnation of a [[quantum mechanical system]] -- the topos-theoretic quantum [[phase space]] -- and its [[functor]]iality.

1. [Kinematics on a Bohr topos](#KinematicsOnBohrTopos)

   This discusses how the classical [[kinematics]] [[internalization|internal to]] a Bohr topos is the external quantum kinematics of the underlying quantum mechanical system.

1. [(Pre-)Sheaf of Bohr toposes of a quantum field theory](#SheafOfBohrToposesOfQFT)

   This discusses how the [[presheaves]] of Bohr toposes obtained by applying Bohrification to a [[local net of observables]] of a [[quantum field theory]].

## Bohr topos of a quantum mechanical system
 {#BohrToposOfQMSystem}

### Definition

#### $C^*$-algebras

+-- {: .num_defn}
###### Definition

A [[C-star algebra]] is (...)

=--

+-- {: .num_defn}
###### Definition

For $A$ a [[star-algebra]], an element $a \in A$ is called a **[[normal operator|normal element]]** if $a^* a = a a^*$.

=--

+-- {: .num_remark}
###### Remark

Every element of a $C^*$-algebra is the sum of two normal elements, because

$$
  a = \frac{1}{2} \left( \left( a + a^* \right) + \left( a - a^*  \right) \right)
  \,.
$$

This means whenever a linear morphism between the vector spaces underlying two  $C^*$-algebras is defined on normal elements, it is already defined on all elements. This will be used in several of the arguments below.

=--

+-- {: .num_defn #PartialCStar}
###### Definition

A **partial $C^\ast$-algebra is a [[set]] $A$ equipped with

* a symmetric and reflexive binary [[relation]] $C \subset A \times A$;

* elements $0,1 \in A$;

* an [[involution]] $\ast : A \to A$;

* a [[function]] $(-)\cdot (-) : \mathbb{C} \times A \to A$;

* a [[function]] $\Vert-\Vert : A \to \mathbb{R}$;

* (partial) binary operations $+, \times : C \to A$

such that every set $S \subset A$ of elements that are pairwise in $C$ is contained in a set $T \subset A$ whose elements are also pairwise in $C$ and on which the above operations yield the structure of a commutative [[C-star algebra]].

A [[homomorphism]] of partial $C^\ast$-algebra is a function preserving this structure. This defines a [[category]] $PCstar$ of partial $C^\ast$ algebras.

=--

This appears as ([vdBergHeunen, def. 11,12](#vdBergHeunen)).


+-- {: .num_defn #PartialAlgebraOfNormalOperators}
###### Definition

For $A$ a [[C-star algebra]], write 

$$
  N(A) := \{a \in A | a a^* = a^* a\}
$$

for its set of [[normal operator]]s. This is naturally a [partial C-star algebra](#PartialCStar) with $C \subset N(A) \times N(A)$ the set of pairs of elements that commute in $A$.

=--


#### The Bohr site
 {#BohrSite}

+-- {: .num_defn #PosetOfCommutativeSubalgebras}
###### Definition

For $A$ a [partial C-star algebra](#PartialCStar) write $\mathcal{C}(A)$ for the [[poset]] of total (not partial) commutative sub [[C-star algebra]]s. We call this the [[poset of commutative subalgebras]].

This extends to a functor

$$
  \mathcal{C} : C^* Alg \to Poset
  \,.
$$

Write $Alex(\mathcal{C}(A))$ for the [[Alexandroff space]] associated with $\mathcal{C}(A)$.

$$
  Alex \mathcal{C} : C^* Alg \stackrel{\mathcal{C}}{\to}
    Poset \underoverset{\simeq}{Alex}{\to}
  AlexandrofvTop 
  \hookrightarrow 
  Top
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

A morphism $f : A \to B$ in $C^* Alg$ is called **commutativity reflecting** if for all $a_1, a_2 \in A$ we have that if $f(a_1)$ commutes with $f(a_2)$ in $B$ then already $a_1$ commutes with $a_2$ in $A$.

Write

$$
  C^* Alg_{cr} \subset C^* Alg
$$

for the [[subcategory]] of [[C-star algebra]]s on the commutativity-reflecting morphisms.

=--

+-- {: .num_remark }
###### Remark

Every [[monomorphism]] $A \hookrightarrow B$ in $C^* Alg$ is commutativity reflecting.

=--

+-- {: .num_prop }
###### Proposition

A morphism $f : A \to B$ in $C^* Alg$ is commutativity reflecting precisely if the morphism $Alex \mathcal{C} (f) : Alex \mathcal{C}(A) \to Alex \mathcal{C}(B)$  in $AlexandrovTop$ has a [[left adjoint]]

$$
  Alex \mathcal{C}(A)
   \stackrel{L_f}{\underset{Alex \mathcal{C}(f)}{\to}}
  Alex \mathcal{C}(B)
  \,.
$$

=--

This appears as ([Nuiten, lemma 2.6](#Nuiten)).

+-- {: .num_defn }
###### Definition

Write 

$$
  C^* Alg_{inc}
  \subset 
  C^* Alg_{cr}
  \subset
  C^* Alg
$$

for the subcategories of $C^* Alg$ on the monomorphisms and on the commutativity-reflecting morphisms, respectively.

=--


#### The Bohr topos
 {#BohrTopos}


+-- {: .num_defn #TheSheafTopos}
###### Definition

Let 

$$
  \begin{aligned}
    Sh(Alex(\mathcal{C}(A)))
    \simeq
    [\mathcal{C}(A), Set]
  \end{aligned}
$$ 

be the [[sheaf topos]] over the [Bohr site](#BohrSite) of $A$, equivalently regarded as the [[presheaf topos|copresheaf topos]] over the [[poset of commutative subalgebras]], or as the [[sheaf topos]] on the corresponding [[Alexandrov topology]].

Moreover, write

$$
  Sh_{\not \not}(\mathcal{C}(A)^{op}) \hookrightarrow [\mathcal{C}(A), Set]
$$

the [[sheaf topos]] for the [[double negation topology]].

=--

+-- {: .num_defn #TheRingedSheafTopos}
###### Definition


Both of these are naturally [[ringed topos]]es with ring object 

$$
  \underline{A} : C \mapsto U(C)
$$ 

(where $U : CStar \to Set$ is the underlying set functor) that is naturally equipped with the structure an [[internalization|internal]] commutative $C^*$-algebra. 

=--

+-- {: .num_prop }
###### Proposition

This construction extends to a [[functor]]

$$
  Bohr : C^* Alg_{cr}^{op} \to C^* TopSpace
$$

=--

This is ([Nuiten, lemma 2.7](#Nuiten)).

+-- {: .proof}
###### Proof

To $f : A \to B$ with

$$
  ( L_f \dashv Alex \mathcal{C}(f)) : 
  Alex \mathcal{C}(A)
  \stackrel{\overset{L_f}{\leftarrow}}{\underset{Alex \mathcal{C}(f)}{\to}}
  Alex \mathcal{C}(B)
$$

we assing the [[geometric morphism]]

$$
  (f^* \dashv f_*)
  :=
  [\mathcal{C}(B), Set]
   \stackrel{\overset{(-)\circ L_f}{\leftarrow}}{\underset{Ran_{L_f}}{\to}}
  [\mathcal{C}(A), Set]
$$

equipped with the evident morphism of internal $C^*$-algebras

$$
  f^* \underline{A} \to \underline{B}
$$

which over $C \in \mathcal{C}(B)$ is the restriction

$$
  (f^* \underline{A})(C) = L_f(C) \stackrel{f|_{L_f C}}{\to} C
$$

of $f$ to $L_f C$. This indeed lands in $C$ due to the $(f \dashv L_f)$-[[unit of an adjunction|counit]] (on posets)

$$
  f(L_f(D)) \hookrightarrow D
  \,.
$$

=--


## Kinematics on a Bohr topos
 {#KinematicsOnBohrTopos}



### The internal phase space locale

+-- {: .num_defn #TheInternalLocale}
###### Definition


Write $\underline{\Sigma}_A$ and $\Sigma_A^{\not \not}$, respectively for the corresponding [[internal locale]]s associated to $\underline{A}$ by internal [[constructive Gelfand duality]]. Write 

$$
  \Sigma_A \to \mathcal{C}(A)
$$ 

and

$$
  \Sigma^{\not \not}_A \to \mathcal{C}(A)
$$ 

for the corresponding external locale, given under the [[equivalence of categories]]

$$
  Loc(Sh(\mathcal{C}(A))) \simeq Loc/\mathcal{C}(A)
$$

discussed at [[internal locale]].

=--

+-- {: .num_defn #Bohrification}
###### Definition

For $A$ a (noncommutative) [[C-star algebra]], the assignment

$$
  A \mapsto \Sigma_{A}
$$

or 

$$
  A \mapsto \Sigma^{\not \not}_{A}
$$

is called the **Bohrification** of $A$.

=--


+-- {: .num_prop #TheInternalLocale}
###### Proposition

Let $\underline{\Sigma}(\underline(A))$ be the [[internal locale]] from def. \ref{TheInternalLocale}.

Regarded as an object 

$$
  (\Sigma_A \to \mathcal{C}(A))
  \in
  Loc/\mathcal{C}(A)
$$ 

of external locales over $\mathcal{C}(A)$, this is the [[topological space]] whose underlying set is given by the disjoint union

$$
  \Sigma_A = \coprod_{C \in \mathcal{C}(A)} \Sigma(C)
$$

over all commutative $C^*$-subalgebras of $A$ of the ordinary [[Gelfand spectrum|Gelfand spectra]] $\Sigma(C)$ of these commutative $C^*$-algebras, and whose [[open subset]]s are defined to be those $\mathcal{U} \subset \Sigma_A$ for which

1. $\mathcal{U}|_C \in \mathcal{O}(\Sigma(C))$ for all commutative subalgebras $C$;

1. For all $C \hookrightarrow D$, if $\lambda \in \mathcal{U}|_C$ and $\lambda' \in \Sigma(D)$ such that   $\lambda'|_C = \lambda$, then $\lambda' \in \mathcal{U}|_D$.

Regarded equivalently as an [[internal locale]] in $Sh(\mathcal{C}(A))$ this  

As a [[presheaf]] on the poset $\mathcal{C}(A)$ this is given by

$$
  \underline{\Sigma}(\underline{A})
  :
  U \mapsto \Sigma_U
  \,,
$$

where for $U \in \mathcal{O}(\mathcal{C}(A))$ we set

$$
  \Sigma_U := \coprod_{C \in U} \Sigma(C)
$$

with the relative topology inherited from $\Sigma_A$.


=--

This appears as ([HLSW, theorem 1](#HLSW)).

### Properties of the internal locale

+-- {: .num_prop #BohrificationDependsOnNormalElementsOnly}
###### Proposition

The Bohrification of $A \in ncCStar$ only depends on its [partial C-star algebra](#PartialCStar) $N(A)$ of normal elements

$$
  \Sigma_A \simeq \Sigma_{N(A)}
  \,.
$$

=--

This is highlighted in ([vdBergHeunen](#vdBergHeunen)).

+-- {: .num_prop #ReproducingOrdinaryGelfandDuality}
###### Proposition

For $A$ a commutative $C^\ast$-algebra and $\Sigma_A^{Gelf} \in $ [[Loc]] its ordinary [[Gelfand spectrum]], we have that Bohrification in the double negation topology reproduces this ordinary Gelfand spectrum:

$$
  \Sigma^{\not \not}_A \simeq \Sigma_A^{Gel}
  \,.
$$

=--

This is ([Spitters06, theorem 9, corollary 10](#Spitters06)).

+-- {: .num_prop #FunctorToRingedToposes}
###### Proposition

Then the construction of the [[ringed topos]] over the [[poset of commutative subalgebras]]

$$
  A \mapsto ([\mathcal{C}(A), Set], \underline{A})
$$

extends to a functor

$$
  C^* Alg_{incl} \to C^*TopSpace \hookrigharrow C^* Topos
  \,,
$$


where on the right the morphisms of internal rings are even morphisms of internal [[C-star algebra]]s.

=--

+-- {: .proof}
###### Proof

With the components of the morphism of internal rings the evident objectwise inclusions, this is directly checked.

=--

+-- {: .num_prop #BohrificationFunctorToLoc}
###### Proposition

Let $Cstar_{inc}$ be the [[category]] of [[C-star algebra]]s and inclusions. Then [Bohrification](#Bohrification) extends to a [[functor]]

$$
  \Sigma_{(-)} : CStar_{inc}^{op} \to Loc
  \,.
$$

=--

This is effectively the functoriality of the internal [[constructive Gelfand duality]] applied to the [above observation](#FunctorToRingedToposes). The statement appears as ([vdBergHeunen, theorem 35](#vdBergHeunen)). 




## (Pre-)Sheaf of Bohr toposes of a quantum field theory
 {#SheafOfBohrToposesOfQFT}


Notice that in the context of [[AQFT]] a [[quantum field theory]] is encoded by a [[local net]] of [[C-star algebra]]s on [[spacetime]].

+-- {: .num_note #PresheavesFromLocalNets}
###### Note

Let $X$ be a [[Lorentzian manifold]] and 

$$
  A : \mathcal{O}(X) \to C^* Alg_{inc}
$$

be a [[local net]] of algebras. Notice that by definition this indeed takes values in $C^\ast$-algebras and _inclusions_ . Then postcomposition with the [Bohr topos](#BohrTopos)-functor yields a presheaf of ringed spaces

$$
  Bohr(A) : \mathcal{O}(X)^{op} 
    \to 
  C^* Alg_{inc}^{op}
   \hookrightarrow 
  C^* Alg_{cr}^{op}
   \stackrel{Bohr}{\to}
  C^* TopSpace
   \hookrightarrow
  C^* Topos
  \,.
$$

=--

This appears as ([Nuiten, def. 17](#Nuiten)).

(...)


## References

[[Niels Bohr]]'s views on quantum mechanics that give the construction of _Bohrification_ its name are reviewed i

* Erhard Scheibe, _The logical analysis of quantum mechanics_ . Oxford: Pergamon Press, 1973.
{#Scheibe}

The term _Bohrification_ and the investigations associated with it are initiated in

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _Bohrification of operator algebras and quantum logic_ ([arXiv:0905.2275](http://arxiv.org/abs/0905.2275))

The computation of the internal Gelfand spectrum $\underline{\Sigma}$ was initiated in 

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]] _A topos for algebraic quantum theory_, Comm. Math. Phys. 291:63&#8211;110, 2009, ([arXiv:0709.4364](http://arxiv.org/abs/0709.4364), [doi](http://dx.doi.org/10.1007/s00220-009-0865-6))

with some results in section 5 and 6 of 

* Martijn Caspers, _Gelfand spectra of $C^*$-algebras in topos theory_ ([pdf](http://www.math.ru.nl/~landsman/scriptieMartijn.pdf))

and completed in 

* Sander Wolters, _Contravariant vs covariant quantum logic: A comparison of two topos-theoretic approaches to quantum theory_ ([arXiv:1010.2031](http://arxiv.org/abs/1010.2031))

An complete outline of the full proof is given in 

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], Sander Wolters, _The Gelfand spectrum of a noncommutative $C^\ast$-algebra: a topos-theoretic approach_, [arxiv:1010.2050](http://arxiv.org/abs/1010.2050)
 {#HLSW}

Applications and examples for $A$ a [[matrix]] algebra are discussed in 

* Martijn Caspers, [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _Intuitionistic Quantum Logic of an $n$-level System_ ([pdf](http://www.math.ru.nl/~landsman/CHLS.pdf))

The [[functor|functoriality]] of Bohrification is observed in 

* [[Benno van den Berg]], [[Chris Heunen]], _Noncommutativity as a colimit_ ([arXiv:1003.3618](http://arxiv.org/abs/1003.3618))
{#vdBergHeunen}

The application of the [[double negation topology]] to make Bohrification coinicide with ordinary [[Gelfand duality]] on commutative $C^*$-algebras is discussed in 

* [[Bas Spitters]], _The space of measurement outcomes as a spectrum for non-commutative algebras_ in Cooper, Kashefi, Panangaden (eds.) _Developments in computational models_ (DCM 2010)([arXiv:1006.1432](http://arxiv.org/abs/1006.1432))
{#Spitters06}

The generalization of Bohrification from [[quantum mechanics]] to [[quantum field theory]] ([[AQFT]]) is discussed in

* Joost Nuiten, _[[schreiber:bachelor thesis Nuiten|Bohrification of local nets]]_ 
 {#Nuiten11}