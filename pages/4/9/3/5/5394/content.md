
#Contents#
* table of contents
{:toc}

## Idea

For $A$ a an [[associative algebra]], not necessatily commutative, its collection $ComSub(A)$ of commutative subalgebras $B \hookrightarrow A$ is naturally a [[poset]] under inclusion of subalgebras. Moreover, $ComSub(A)$ is a complete [[semilattice]].

Various authors have proposed that for the case that $A$ is a [[C-star algebra]] the [[noncommutative geometry]] encoded by the formal dual of $A$ is to be understood as commutative geometry inside a [[topos]] over $ComSub(A)$ or its [[opposite category|opposite]] $ComSub(A)^{op}$. For instance the [[Kochen-Specker theorem]] turns into a geometric statement about the topos-theoretic space dual to $A$ (namely saying that it has no [[point]]s.)

## Properties



+-- {: .un_prop}
###### Proposition

Let $A, B$ be [[von Neumann algebra]]s without a type $I_2$-[[von Neumann algebra factor]]-summand and let $ComSub(A)$, $ComSub(B)$ be their posets of commutative sub-von Neumann algebras. Let $A_J$ and $B_J$ be the canonical [[Jordan algebra]] structures on $A$ and $B$ (with product the symmetrization of the product in $A,B$). 

Then every [[isomorphism]] $ComSub(A) \to ComSub(B)$ of posets comes from a unique Jordan algebra isomorphism $A_j \to B_j$. 

=--

This is the theorem in ([HardingD&#246;ring](#HardingDoering)).


+-- {: .un_prop}
###### Proposition

For $A$ a [[C-star algebra]], write $ComSub(A)$ for its [[poset]] of sub-$C^*$-algebras. Write $\mathcal{T}_A := [ComSub(A),Set]$ for the [[presheaf topos]] on $ComSub(A)^{op}$.

The presheaf

$$
  (\mathbb{A} : B \mapsto U(B)) \;\; \in \mathcal{T}_A
  \,,
$$

where $U(B)$ is the underlying [[set]] of the commutative subalgebra $B$, is canonically a commutive $C^*$-algebra [[internalization|internal]] to $\mathcal{T}_A$.

=--

This is ([HeunenLandsmanSpitters, theorem 5](#HeunenLandsmanSpitters)).

+-- {: .un_prop}
###### Proposition

By the [[constructive Gelfand duality theorem]] there is a [[locale]] $\Sigma(A)$ internal to $\mathcal{T}_A$ canonically associated with $\mathbb{A}$.

If $A = \mathcal{B}(H)$ is the algebra of [[bounded operator]]s on a [[Hilbert space]] $H$ of [[dimension]] $\gt 2$, then then [[Kochen-Specker theorem]] implies that $\Sigma(A)$ has no points.

=--

This is ([HeunenLandsmanSpitters, theorem 5](#HeunenLandsmanSpitters)).



## References

The proposal that the the noncommutative geometry of $A$ is fruitfully studied via the commutative geometry over $ComSub(A)$ goes back to 

* [[Jeremy Butterfield]],  [[John Hamilton]], [[Chris Isham]], _A topos perspective on the Kochen-Specker theorem_ 

  _I. quantum states as generalized valuations_ International Journal of Theoretical Physics,
37(11):2669&#8211;2733, 1998.

  _II. conceptual aspects and classical analogues_ International Journal of Theoretical Physics,
38(3):827&#8211;859, 1999

  _III. Von Neumann algebras as the base category_ International Journal of
Theoretical Physics, 39(6):1413&#8211;1436, 2000.


The proposal that the non-commutativity of the [[phase space]] in [[quantum mechanics]] is fruitfully understood in the light of this has been amplified in a series of articles

* [[Andreas Döring]], [[Chris Isham]], _A topos foundation for theories of physicsJournal of Mathematical Physics (2008)

See also [[higher category theory and physics]].

The relation of $ComSub(A)$ to Jordan algebras is discussed in

* [[John Harding]], [[Andreas Döring]], _Abelian subalgebras and the Jordan structure of a von Neumann algebra_ ([arXiv:1009.4945](http://arxiv.org/abs/1009.4945))
{#HardingDoering}


The presheaf topos on $ComSub(A)^{op}$ and its internal localic Gelfand dual to $A$ is discussed in

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _A topos for algebraic quantum theory_ ([arXiv:0709.4364](http://arxiv.org/abs/0709.4364))
{#HeunenLandsmanSpitters}

