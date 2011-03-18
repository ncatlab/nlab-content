
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

The construction called _Bohrification_ by some authors is a generalization of the [[Gelfand spectrum]] for commutative [[C-star algebra]]s to a context of _noncommutative_ $C^*$-algebras. It assigns to a noncommutative $C^*$-algebra $A$ a generalized [[Gelfand spectrum]] in the form of a [[locale]] $\underline{\Sigma}_A$ [[internalization|internal]] to the [[sheaf topos]] $\mathcal{T}_A$ over the [[semilattice of commutative subalgebras]] of $A$, or  equivalently its externalization $\Sigma_A \to \mathcal{C}(A)$ regarded as a [[locale]] [[over category|over]] the locale of open subalgebras.

When applied to subalgebras of [[bounded operator]]s on a [[Hilbert space]] this construction has been suggested to formalize faithfully and usefully a heuristic that has goes back to [[Nils Bohr]] and is known as the _doctrine of classical concepts_ ([Scheibe](#Scheibe)) in [[quantum mechanics]]. This states that  nonclassical/noncommutative as the [[logic]]/[[geometry]] of quantum mechanics may be, it is to be probed and detected by classical/commutative logic/geometry. In _Bohrification_ this heuristics is formalized by the [[semilattice of commutative subalgebras]] and various entities induced by this [[posite]]. The internal [[locale]] $\underline{\Sigma}_A$ may be thought of as an incarnation of the quantum [[phase space]] encoded by $A$.

## Definition

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

+-- {: .num_defn}
###### Definition

For $A$ a [[C-star algebra]], write 

$$
  N(A) := \{a \in A | a a^* = a^* a\}
$$

for its set of [[normal operator]]s. This is naturally a [partial C-star algebra](#PartialCStar) with $C \subset N(A) \times N(A)$ the set of pairs of elements that commute in $A$.

=--

+-- {: .num_defn}
###### Definition

For $A$ a [partial C-star algebra](#PartialCStar) write $\mathcal{C}(A)$ for the [[poset]] of total (not partial) commutative sub [[C-star algebra]]s. We call this the [[semilattice of commutative subalgebras]].

Let 

$$
  [\mathcal{C}(A), Set]
$$ 

be the [[presheaf topos]] over this poset and

$$
  Sh_{\not \not}(\mathcal{C}(A)^{op}) \hookrightarrow [\mathcal{C}(A), Set]
$$

the [[sheaf topos]] for the [[double negation topology]].

Both of these are naturally [[ringed topos]]es with ring object 
$\underline{A} : C \mapsto U(C)$ (where $U : CStar \to Set$ is the underlying set functor) that is actually a [[internalization|internal]] commutative $C^*$-algebra. Write $\underline{\Sigma}_A$ and $\Sigma_A^{\not \not}$, respectively for the corresponding [[internal locale]]s associated to $\underline{A}$ by internal [[constructive Gelfand duality]]. Write 

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

## Properties



+-- {: .num_prop}
###### Proposition


The [[locale]] in $Loc/\Sigma_A$ may be directly expressed as

$$
  \Sigma_A := 
  \{
    F : \mathcal{C}(A) \to Set | F(C) open in \Sigma(C), F monotone
  \}
$$

=--

(...)

+-- {: .num_prop}
###### Proposition

The Bohrification of $A \in ncCStar$ only depends on its [partial C-star algebra](#PartialCStar) $N(A)$ of normal elements

$$
  \Sigma_A \simeq \Sigma_{N(A)}
  \,.
$$

=--

This is highlighted in ([vdBergHeunen](#vdBergHeunen)).

+-- {: .num_prop}
###### Proposition

For $A$ a commutative $C^\ast$-algebra and $\Sigma_A^{Gelf} \in $ [[Loc]] its ordinary [[Gelfand spectrum]], we have that Bohrification in the double negation topology reproduces this ordinary Gelfand spectrum:

$$
  \Sigma^{\not \not}_A \simeq \Sigma_A^{Gel}
  \,.
$$

=--

This is [Spittes06, theorem 9, corollary 10](#Spitters06).

+-- {: .num_prop #FunctorToRingedToposes}
###### Proposition

Let $Cstar_{inc}$ be the [[category]] of [[C-star algebra]]s and inclusions. Then the construction of the [[ringed topos]] over the [[semilattice of commutative subalgebras]]

$$
  A \mapsto ([\mathcal{C}(A), Set], \underline{A})
$$

extends to a functor

$$
  Cstar_{incl} \to RingedTopos
$$

and even to

$$
  Cstar_{incl} \to CstarTopos
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


## Applications 

Notice that in the context of [[AQFT]] a [[quantum field theory]] is encoded by a [[local net]] of [[C-star algebra]]s on [[spacetime]].

+-- {: .num_note}
###### Note

Let $X$ be a [[Lorentzian manifold]] and 

$$
  A : \mathcal{O}(X) \to CStar_{inc}
$$

be a [[local net]] of algebras. Notice that by definition this indeed takes values in $C^\ast$-algebras and _inclusions_ . Then postcomposition with the [Bohrification functor](#BohrificationFunctorToLoc) yield a [[presheaf]]

$$
  \Sigma_A : \mathcal{O}(X)^{op} \to Loc \to Set
$$

that assigns to each [[open subset]] of $X$ regarded as [[spacetime]] an object to be regarded as the quantum [[phase space]] of the [[AQFT]] encoded by $A$ restricted to that open subset.

=--

(...)


## References

[[Niels Bohr]]'s views on quantum mechanics that give the construction of _Bohrification_ its name are reviewed in

* Erhard Scheibe. _The logical analysis of quantum mechanics_ . Oxford: Pergamon Press, 1973.
{#Scheibe}

The term _Bohrification_ and the investigations associated with it are initiated in

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _Bohrification of operator algebras and quantum logic_ ([arXiv:0905.2275](http://arxiv.org/abs/0905.2275))

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], [[Sander Wolters]], _The Gelfand spectrum of a noncommutative $C^\ast$-algebra: a topos-theoretic approach_ ([arxiv:1010.2050](http://arxiv.org/abs/1010.2050))

The [[functor|functoriality]] of Bohrification is observed in 

* [[Benno van den Berg]], [[Chris Heunen]], _Noncommutativity as a colimit_ ([arXiv:1003.3618](http://arxiv.org/abs/1003.3618))
{#vdBergHeunen}

The application of the [[double negation topology]] to make Bohrification coinicide with ordinary [[Gelfand duality]] on commutative $C^*$-algebras is discussed in 

* [[Bas Spitters]], _The space of measurement outcomes as a spectrum for non-commutative algebras_ in Cooper, Kashefi, Panangaden (eds.) _Developments in computational models_ (DCM 2010)([arXiv:1006.1432](http://arxiv.org/abs/1006.1432))
{#Spitters06}
