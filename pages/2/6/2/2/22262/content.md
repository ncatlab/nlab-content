

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}



## Idea

In [[category theory]], there's often the sense that 'things just work', and that details can be skipped as everything is well behaved. Unfortunately, this is not quite true.

The counterexamples here should serve as specimens of possible pittfalls in category theory, and give an idea of what could go wrong.

## List

1. Sending an [[object]] $x \in \mathcal{C}$ of a [[category]] $\mathcal{C}$ to its [[automorphism group]] $Aut_{\mathcal{C}}(x)$  (or its [[endomorphism monoid]] $End_{\mathcal{C}}(x)$ ) does not in general extend to a [[functor]] from $\mathcal{C}$ to [[Groups]]. 

   It does however extend to a [[functor]] on the [[core]] of $\mathcal{C}$ (the maximal [[groupoid]] inside it, keeping only the [[isomorphisms]] of $\mathcal{C}$), where it sends [[morphisms]] (now constrained to be [[isomorphisms]]) to their [[conjugation action]]:

   $$
     \array{
       Core(\mathcal{C})   
       &
       \overset{
         \;\;\;
         Aut_{\mathcal{C}}
         \;\;\;
       }{
         \longrightarrow
       }
       &
       Groups
       \\
       x
       &
       &
       Aut_{\mathcal{C}}(x)
       \\
       {}^{{}_{\mathllap{
         \simeq
       }}}
       \big\downarrow
       {}^{{}_{\mathrlap{
         \gamma
       }}}
       &
       \mapsto
       &
       \big\downarrow
       {}^{{}_{\mathrlap{
         ad_\gamma 
         \colon
         g \mapsto \gamma \circ g \circ \gamma^{-1}
       }}}
       &
       \\
       y
       &
       &
       Aut_{\mathcal{C}}(y)  
       \,.
     }
   $$

   For example, if $\mathcal{C} = \Pi_1(\mathcal{X})$ is the [[fundamental groupoid]] of a [[topological space]] (which thus coincides with its [[core]] already), then the [[automorphism groups]] of its objects $x \in X$ are the [[fundamental groups]] $\pi_1(X,x)$ at these basepoints, which famously *are* functorial under conjugation by paths in $X$.


1. Forming the [[center]] of a [[group]] does not extend to a [[functor]] from [[Groups]] to [[AbelianGroups]]. 

   It does extend to a functor on the [[core]], though:

   $$
     \array{
       Core(Groups)
       &
       \overset{
         Center
       }{
         \longrightarrow
       }
       &
       AbelianGroups
       \,.
     }
   $$

   Notice that this example is really a special case of the previous one (forming [[automorphism groups]]), or rather of a [[2-category theory|2-category theoretic]] version of it: The [[center]] of a [[group]] is the [[automorphism group]] in the [[endofunctor|endo]]-[[functor category]]  of the [[identity functor]] on the one-object [[delooping]]-[[groupoid]] $\mathbf{B}G$ of $G$:

   $$
     Center(G)
     \;\simeq\;
     Aut_{{}_{End(\mathbf{B}G)}}
     \big(
       id_{\mathbf{B}G}
     \big)
   $$


1. Composing a [[monadic functor]] with another monadic functor need not be monadic. For example, Torsion-free abelian groups are monadic over abelian groups, which are monadic over sets, but torsion-free abelian groups are not monadic over sets. 

1. Taking the skeleton of a [[monoidal category]] does not in general result in a [[strict monoidal category]]. The argument in the case of Set is given in [this MO answer](https://mathoverflow.net/a/128629). In particular, one cannot in general replace a monoidal category with an equivalent category that is simultaneously  strict monoidal and skeletal. 

1. The category of topological spaces and [[local homeomorphism | local homeomorphisms]] is [[locally cartesian closed category | locally cartesian closed]] but not [[cartesian closed category | cartesian closed]] since it does not have a terminal object.

1. There are functors $D:Aff\to Vect$ (taking the vector space of displacements) and $A:Vect \to Aff$ (taking the underlying affine space) between the categories of [[vector spaces]] and [[affine spaces]], and we have $D(A(V)) \cong V$ for any $V\in Vect$, and for any $U\in Aff$ there exists some isomorphism $A(D(U)) \cong U$ (after choosing a point in $U$ to serve as the origin), but the categories are not [[equivalence of categories|equivalent]] --- the second isomorphisms cannot be chosen naturally, not even after restricting to the [[core|cores]].

1. The opposite of the category of commutative [[von Neumann algebra | von Neumann algebras]] has a [[subobject classifier]] and it's [[finitely complete category | finitely complete]], but is not a topos since it is not [[cartesian closed]]. See [this MO question](https://mathoverflow.net/questions/384346/is-the-opposite-category-of-commutative-von-neumann-algebras-a-topos).

1. There is a 'wrong right adjoint' to the functor $F : Petri \to CMC$ (as described in [[Petri nets#semantics]]) which sends a [[commutative monoidal category]] $C$ to the [[Petri net]] whose source and target are $\eta \circ s : Mor(C) \to \mathbb{N}[Ob(C)]$ and $\eta \circ t : Mor(C) \to \mathbb{N}[Ob(C)]$ where $s$ and $t$ are the source and target of $C$ and $\eta$ is the unit for the monad $\mathbb{N}[-]$. In words, $C$ is sent to the [[Petri net]] whose source and target are the [[source]] and [[target]] of $C$ composed with $\eta$. The natural choice of isomorphism $Hom(FA, B) \cong Hom(A, GB)$, where $G$ is the functor just described, turns out not to yield well-defined morphisms of [[Petri nets]]. See Remark 4.4 in [Master 2020](#PN)

1. Let $C$ be a category without an [[initial object]] and let $R : C \to 1$ be the unique functor from $C$ into the [[terminal category]]. Then $R$ preserves all limits but does not have a left adjoint because this left adjoint would have to send the unique object of 1 to an initial object. 

1.  Consider the functor $U\colon Group \to Set$ that sends a group $G$
to the set $\prod_{i\in I} hom(S_i, G)$,
where the groups $S_i$ are simple for all $i\in I$,
$I$ is the [[class]] of all [[ordinals]],
and the cardinality of $S_i$ eventually becomes bigger than any fixed cardinal as $i$ increases.
This is a limit-preserving functor between [[locally presentable categories]].
However, it does not have a [[left adjoint]].

1. [[dense functor | Dense functors]] are not closed under composition. For example, $\Delta_{\lt 2}$ is dense in the [[simplex category]] $\Delta$ and $\Delta$ is dense in $\mathbf{Cat}$, but $\Delta_{\lt 2}$ is not dense in $\mathbf{Cat}$.


## See also

* [[counterexamples in algebra]]

## References

The initial import of counterexamples in this entry was taken from [this Zulip discussion](https://mattecapu.github.io/ct-zulip-archive/stream/229111-general/topic/Counterexamples.20in.20Category.20Theory.html).

* {#PN} [[Jade Master]], 2020, _[Petri nets based on Lawvere theories](https://www.cambridge.org/core/journals/mathematical-structures-in-computer-science/article/petri-nets-based-on-lawvere-theories/9E0F011860A1285DDC498B740774FBDC)_, Mathematical Structures in Computer Science, 30(7), 833-864
