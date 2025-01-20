
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of _geometric $\infty$-stack_ is the refinement to [[∞-stack]] of that of _[[geometric stack]]_.

There is an intrinsic definition which iterates that of geometric stacks and says inductively that a geometric $n$-stack is one which has an $n$-[[atlas]] and such that its [[diagonal]] is $(n-1)$-representable ([To&#235;n-Vezzosi 04, def. 1.3.3.1](#ToenVezzosi04)).

Then there is a result which says that such geometric $n$-stacks are equivalently those represented by suitable [[Kan complex]]-objects in the given [[site]] ("[[internal infinity-groupoids]]" in the site) ([Pridham 09](Pridham09)).

(There is also a definition of "geometric $\infty$-stack" in ([To&#235;n 00, definition 4.1.4](#Toen00)), which is however different.)


## Definition




## Properties

### Presentation by Kan-fibrant simplicial objects

A presentation of geometric $\infty$-stacks, in some generality, by suitably  Kan-fibrant [[simplicial objects]] is in ([Pridham 09](#Pridham09)). See also at _[[Kan-fibrant simplicial manifold]]_.


## Examples


* Every object in the image of $Spec : T Alg_\infty^{op} \to \mathbf{H}$ is a geometric $\infty$-stack.

* Over the [[étale site]] an [[algebraic stack]] that is a [[geometric stack]] is also a geometric $\infty$-stack.

* Every [[schematic homotopy type]] is given by a geometric $\infty$-stack.

* [[Kan-fibrant simplicial manifolds]]  serve to present geometric $\infty$-stacks in [[higher differential geometry]], the [[Lie infinity-groupoids]]

## Toen 00

> The text below follows ([To&#235;n 00](#Toen00)). Needs to be connected to the rest of the entry.

We consider the [[higher geometry]] encoded by a [[Lawvere theory]] $T$ via [[Isbell duality]]. Write $T Alg$ for the category of [[algebras over a Lawvere theory]] and write $T Alg^{\Delta}$ for the [[(∞,1)-category]] of [[cosimplicial object|cosimplicial]] $T$-algebras .

Consider a [[site]] $T \subset C \subset T Alg^{op}$ that satisfies the assumptions described at [[function algebras on ∞-stacks]]. Then, by the discussion given there, we have a pair of [[adjoint (∞,1)-functor]]s

$$
  (\mathcal{O} \dashv Spec) :  (T Alg^{\Delta})^{op}
   \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{Spec}{\to}}
  Sh_\infty(C) =: \mathbf{H}
  \,,
$$

where $\mathbf{H} := Sh_\infty(C)$ is the [[(∞,1)-category of (∞,1)-sheaves]] over $C$, the [[big topos]] for the [[higher geometry]] over $C$.

+-- {: .num_defn}
###### Definition

An object $X \in \mathbf{H}$ is called a **geometric $\infty$-stack** over $C$ if there is it is the [[(∞,1)-colimit]] 

$$
  X \simeq {\lim_\to} K_\bullet
$$

over a [[groupoid object in an (∞,1)-category|groupoid object]] $K_\bullet : \Delta \to \mathbf{H}$ in $\mathbf{H}$ such that

1. $K_0$ and $K_1$ are in the image of $Spec : (T Alg^{\Delta})^{op} \to \mathbf{H}$;

1. the target map $d_1 : K_1 \to K_0$ is lisse.

=--

For $T$ the theory of commutative [[associative algebra]]s over a commutative ring $k$ and $C$ the [[fpqc topology]] this appears as  ([To&#235;n 00, definition 4.1.4](#Toen00)).

+-- {: .num_prop}
###### Proposition

Geometric $\infty$-stacks are stable under [[(∞,1)-pullback]]s along morphism in the image of $Spec$.

=--

+-- {: .proof}
###### Proof

Use that in the [[(∞,1)-topos]] $\mathbf{H}$ we have [[universal colimits]] and that $Spec$ is [[right adjoint]].

=--


## Related concepts

* [[geometric stack]]

* **geometric $\infty$-stack**, [[function algebras on ∞-stacks]]

* [[Artin-Lurie representability theorem]]


## References

The notion of geometric $\infty$-stack as a weak quotient of affine $\infty$-stacks is considered in section 4 of


* {#Toen00} [[Bertrand Toën]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))

More general theory in the context of [[derived algebraic geometry]] is in

* {#ToenVezzosi04} [[Bertrand Toën]], [[Gabriele Vezzosi]] _Homotopical Algebraic Geometry II: geometric stacks and applications_ ([arXiv:math/0404373](http://arxiv.org/abs/math/0404373))

and specifically in [[E-∞ geometry]] in 

* {#Lurie} [[Jacob Lurie]], _[[Representability Theorems]]_

* {#Pridham10} [[Jonathan Pridham]], _Representability of derived stacks_ ([arXiv:1011.2189](http://arxiv.org/abs/1011.2189))

Discussion of presentation of geometric $\infty$-stacks by Kan-fibrant [[simplicial objects]] in the [[site]] is in 

* {#Pridham09} [[Jonathan Pridham]], _Presenting higher stacks as simplicial schemes_, Advances in Mathematics, Volume 238, Pages 184-245 ([arXiv:0905.4044](http://arxiv.org/abs/0905.4044))

[[!redirects geometric ∞-stack]]

[[!redirects geometric ∞-stacks]]
[[!redirects geometric infinity-stacks]]

