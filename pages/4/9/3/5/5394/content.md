
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### General

For $A$ a an [[associative algebra]], not necessatily commutative, its collection $ComSub(A)$ of commutative subalgebras $B \hookrightarrow A$ is naturally a [[poset]] under inclusion of subalgebras. Moreover, $ComSub(A)$ is a complete [[semilattice]].

### As a site for noncommutative geometry

Various authors have proposed ([Butterfield-Hamilton-Isham](#ButterfieldHamiltonIsham), [D&#246;ring-Isham](#DoeringIsham), 
[Heunen-Landsmann-Spitters](#HeunenLandsmanSpitters)) that for the case that $A$ is a [[C-star algebra]] the [[noncommutative geometry]] of the [[Isbell duality|formal dual]] [[space]] $\Sigma(A)$ of $A$ may be understood as a commutative [[geometry]] [[internalization|internal]] to a [[sheaf topos]] $\mathcal{T}_A$ over $ComSub(A)$ or its [[opposite category|opposite]] $ComSub(A)^{op}$. An advantage of the latter is that $\Sigma$ becomes a [[compact locale|compact]] [[regular locale]].

### As a site for noncommutative phase spaces

Specifically, consider the case that the algebra $A = B(\mathcal{H})$ is that of [[bounded operator]]s on a [[Hilbert space]].

Notice that if we think of $A$ as being the [[C-star algebraic deformation quantization]] of a [[symplectic manifold]] then

* commutative subalgebras correspond to [[isotropic subspace]]s;

* maximal commutative subalgebras correspond to [[Lagrangian subspace]]s,

Applying Bohrification to this situation, one finds that the [[locale]] $\Sigma(A)$ internal to $\mathcal{T}_A$ behaves like the noncommutative [[phase space]] of a system of [[quantum mechanics]], which however internally looks like an ordinary commutative geometry. Various statements about [[operator algebra]] then have geometric analogs in $\mathcal{T}_A$. 

Notably the [[Kochen-Specker theorem]] says that $\Sigma(B(\mathcal{H}))$, while nontrivial, has no [[point]]s/no [[global element]]s. (This topos-theoretic geometric reformulation of the Kochen-Specker theorem had been the original motivation for considering $ComSub(A)$ in the first place in [ButterfieldIsham](#ButterfieldIsham)).

Moreover, inside $\mathcal{T}_A$ the [[quantum mechanics|quantum mechanical]] kinematics encoded by $B(\mathcal{H})$ looks like [[classical mechanics]] kinematics internal to $\mathcal{T}_A$ ([HeunenLandsmannSpitters](#HeunenLandsmanSpitters), following [D&#246;ringIsham](#DoeringIsham)):

1. the [[open subset]]s of $\Sigma(A)$ are identified with the quantum [[state]]s on $A$. Their collection forms the [[Heyting algebra]] of quantum logic.

1. [[observable]]s are morphisms of internal [[locale]]s $\Sigma(A) \to IR$, where $IR$ is the [[interval domain]].

The assignment to a noncommutative algebra $A$ of a [[locale]] $\underline{\Sigma}_A$ internal to $\mathcal{T}_A$ has been called [[Bohrification]], in honor of [[Nils Bohr]] whose heuristic writings about the nature of [[quantum mechanics]] as being probed by classical (= commutative) context one may argue is being formalized by this construction.

## Properties

### Relation to Jordan algebras {#RelationToJordanAlgebras}

For $A$ an [[associative algebra]] write $A_J$ for its corresponding [[Jordan algebra]], where the commutative product $\circ : A_J \otimes A_J \to A_J$ is the symmetrization of the product in $A$: $a \circ b = \frac{1}{2}(a b + b a)$.

+-- {: .un_lemma}
###### Observation

There exist von Neumann algebras $A$, $B$ such that there exists a Jordan algebra isomorphism $A_J \to B_J$ but not an algebra isomorphism $A \to B$.

=--

+-- {: .proof}
###### Proof

By 

* [[Alain Connes]], _A factor not anti-isomorphic to itself_, Annals of Mathematics, 101 (1962), no. 3, 536&#8211;554. ([JSTOR](http://www.jstor.org/stable/1970940))

there is a [[von Neumann algebra factor]] $A$ with no algebra isomorphism to its opposite algebra $A^{op}$. But clearly $A_J \simeq (A^{op})_J$.

=--

+-- {: .un_prop}
###### Proposition

Let $A, B$ be [[von Neumann algebra]]s without a type $I_2$-[[von Neumann algebra factor]]-summand and let $ComSub(A)$, $ComSub(B)$ be their posets of commutative sub-von Neumann algebras. 

Then every [[isomorphism]] $ComSub(A) \to ComSub(B)$ of [[poset]]s comes from a unique Jordan algebra isomorphism $A_j \to B_j$. 

=--

This is the theorem in ([HardingD&#246;ring](#HardingDoering)).



### The presheaf topos over $ComSub(A)^{op}$

+-- {: .un_def}
###### Definition

For $A$ a [[C-star algebra]], write $ComSub(A)$ for its [[poset]] of sub-$C^*$-algebras. Write 

$$
  \mathcal{T}_A := [ComSub(A),Set]
$$ 

for the [[presheaf topos]] on $ComSub(A)^{op}$. 

=--

+-- {: .un_remark}
###### Remark

This opposite order on commutative subalgebras may be seen as the information order from [[Kripke semantics]]: a larger subalgebra contains more information. In this light the presheaf topos on $ComSub(A)$, as used by [DoeringIsham](#DoeringIsham) and co-workers, may be seen as the co-Kripke model. This model give the so-called coarse-graining semantics of physics.

=--

+-- {: .un_lemma}
###### Observation

The topos $\mathcal{T}_A$ is a [[localic topos]]. 

=--

Because $ComSub(A)$ is a [[posite]].


### The locale $\Sigma(A)$


+-- {: .un_prop}
###### Proposition


The [[presheaf]]

$$
  (\mathbb{A} : B \mapsto U(B)) \;\; \in \mathcal{T}_A
  \,,
$$

where $U(B)$ is the underlying [[set]] of the commutative subalgebra $B$, is canonically a commutative $C^*$-algebra [[internalization|internal]] to $\mathcal{T}_A$.

=--

This is ([HeunenLandsmanSpitters, theorem 5](#HeunenLandsmanSpitters)).

+-- {: .un_cor}
###### Corollary

By the [[constructive Gelfand duality theorem]] there is uniquely a [[locale]] $\Sigma(A)$ internal to $\mathcal{T}_A$ such that $\mathbb{A}$ is the internal commutative $C^*$-algebra of functions on $\Sigma(A)$.

=--

This observation is amplified in ([HeunenLandsmanSpitters](#HeunenLandsmanSpitters)).


+-- {: .un_prop}
###### Proposition

If $A = \mathcal{B}(H)$ is the algebra of [[bounded operator]]s on a [[Hilbert space]] $H$ of [[dimension]] $\gt 2$, then then [[Kochen-Specker theorem]] implies that $\Sigma(A)$ has no points/no [[global element]].

=--

This is ([HeunenLandsmanSpitters, theorem 6](#HeunenLandsmanSpitters)), following ([ButterfieldIsham](#ButterfieldIsham)).



## References

The proposal that the the noncommutative geometry of $A$ is fruitfully studied via the commutative geometry over $ComSub(A)$ goes back to 

* [[Jeremy Butterfield]],  [[John Hamilton]], [[Chris Isham]], _A topos perspective on the Kochen-Specker theorem_ 

  _I. quantum states as generalized valuations_ International Journal of Theoretical Physics,
37(11):2669&#8211;2733, 1998.

  _II. conceptual aspects and classical analogues_ International Journal of Theoretical Physics,
38(3):827&#8211;859, 1999

  _III. Von Neumann algebras as the base category_ International Journal of
Theoretical Physics, 39(6):1413&#8211;1436, 2000.
  {#ButterfieldHamiltonIsham}

The proposal that the non-commutativity of the [[phase space]] in [[quantum mechanics]] is fruitfully understood in the light of this has been amplified in a series of articles

* [[Andreas Döring]], [[Chris Isham]], _A topos foundation for theories of physicsJournal of Mathematical Physics (2008)
{#DoeringIsham}

See also [[higher category theory and physics]].

The relation of $ComSub(A)$ to Jordan algebras is discussed in

* [[John Harding]], [[Andreas Döring]], _Abelian subalgebras and the Jordan structure of a von Neumann algebra_ ([arXiv:1009.4945](http://arxiv.org/abs/1009.4945))
{#HardingDoering}


The presheaf topos on $ComSub(A)^{op}$ and its internal localic Gelfand dual to $A$ is discussed in

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _A topos for algebraic quantum theory_ ([arXiv:0709.4364](http://arxiv.org/abs/0709.4364))
{#HeunenLandsmanSpitters}
{#HeunenLandsmanSpitters}
