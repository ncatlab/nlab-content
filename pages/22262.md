## Idea
In [[category theory]], there's often the sense that 'things just work', and that details can be skipped as everything is well behaved. Unfortunately, this is not quite true.

The counterexamples here should serve as specimens of possible pittfalls in category theory, and give an idea of what could go wrong.

## List

1. Taking the center of a group does not a define a functor from groups to abelian groups. 

1. Sending an object of a category to its [[automorphism]] group (or its [[endomorphism]] monoid) is not in general functorial.

1. Composing a [[monadic functor]] with another monadic functor need not be monadic. For example, Torsion-free abelian groups are monadic over abelian groups, which are monadic over sets, but torsion-free abelian groups are not monadic over sets. 

1. Taking the skeleton of a [[monoidal category]] does not in general result in a [[strict monoidal category]]. The argument in the case of Set is given in [this MO answer](https://mathoverflow.net/a/128629) In particular, one cannot in general replace a monoidal category with an equivalent category that is siss and tt are the source and target of CC and η\eta is the unit for the monad ℕ[−]\mathbb{N}[-]. In words, CC is sent tmultaneously  strict monoidal and skeletal. 

1. The category of topological spaces and [[local homeomorphism | local homeomorphisms]] is [[locally cartesian closed category | locally cartesian closed]] but not [[cartesian closed category | cartesian closed]] since it does not have a terminal object.

1. There are functors $D:Aff\to Vect$ and $A:Vect \to Aff$ between the categories of [[vector spaces]] and [[affine spaces]], and we have $D(A(V)) \cong V$ for any $V\in Vect$ and $A(D(U)) \cong U$ for any $U\in Aff$, but the categories are not [[equivalence of categories|equivalent]] --- the second isomorphism is not natural.

1. The opposite of the category of commutative [[von Neumann algebra | von Neumann algebras]] has a [[subobject classifier]] and it's [[finitely complete category | finitely complete]], but is not a topos since it is not [[cartesian closed]]. See [this MO question](https://mathoverflow.net/questions/384346/is-the-opposite-category-of-commutative-von-neumann-algebras-a-topos).

1. There is a 'wrong right adjoint' to the functor $F : Petri \to CMC$ (as described in [[Petri nets#semantics]]) which sends a [[commutative monoidal category]] $C$ to the [[Petri net]] whose source and target are $\eta \circ s : Mor(C) \to \mathbb{N}[Ob(C)]$ and $\eta \circ t : Mor(C) \to \mathbb{N}[Ob(C)]$ where $s$ and $t$ are the source and target of $C$ and $\eta$ is the unit for the monad $\mathbb{N}[-]$. In words, $C$ is sent to the [[Petri net]] whose source and target are the [[source]] and [[target]] of $C$ composed with $\eta$. The natural choice of isomorphism $Hom(FA, B) \cong Hom(A, GB)$, where $G$ is the functor just described, turns out not to yield well-defined morphisms of [[Petri nets]]. See Remark 4.4 in [Master 2020](#PN)

1. Let $C$ be a category without an [[initial object]] and let $R : C \to 1$ be the unique functor from $C$ into the [[terminal category]]. Then $R$ preserves all limits but does not have a left adjoint because this left adjoint would have to send the unique object of 1 to an initial object. 
.
## See also

* [[counterexamples in algebra]]

## References

The initial import of counterexamples in this entry was taken from [this Zulip discussion](https://mattecapu.github.io/ct-zulip-archive/stream/229111-general/topic/Counterexamples.20in.20Category.20Theory.html).

* {#PN} [[Jade Master]], 2020, _[Petri nets based on Lawvere theories](https://www.cambridge.org/core/journals/mathematical-structures-in-computer-science/article/petri-nets-based-on-lawvere-theories/9E0F011860A1285DDC498B740774FBDC)_, Mathematical Structures in Computer Science, 30(7), 833-864
