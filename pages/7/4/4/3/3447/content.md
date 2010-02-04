
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Recall that a [[locally constant sheaf]] (of sets) is a section of the [[constant stack]] with fiver the [[groupoid]] $Core(FinSet)$, the [[core]] of the [[category]] [[FinSet]].

This extends to a general pattern:

a **locally constant $\infty$-stack** is a section of the [[constant ∞-stack]] that is constant on the [[∞-groupoid]] $Core(Fin\infty Grpd)$.

## Definition

We propose a definition of locally constant $\infty$-stacks inside any [[(∞,1)-topos]].

+-- {: .query}
[[Urs Schreiber]]: sanity-check the following.
=--


Let $C$ be some [[site]] and let $\mathbf{H} = Sh_{(\infty,1)}(C)$ be the [[(∞,1)-topos]] of [[∞-stack]]s over $C$. We think of objects $X \in \mathbf{H}$ as generalized [[space]]s modeled on $C$.

We have a squence of [[adjunction]]s

$$
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{L}{\leftarrow}}{\hookrightarrow}
  PSh_{(\infty,1)}(C)
  \stackrel{\overset{const}{\leftarrow}}{\to}
  PSh_{(\infty,1)}(*)
  =
  \infty Grpd 
  :
  LConst
$$

where on the left we have the defining adjunction of the [[(∞,1)-category of (∞,1)-sheaves]] -- $L$ is [[∞-stackification]] -- and on the right the [[geometric morphism]] that is induced from the canonical morphism of [[site]]s $C \to {*}$ (to the [[terminal object|terminal]] site).



Let 

$$
  \infty FinBund := LConst(Core(Fin \infty Grpd)) \in \mathbf{H}
$$

be the [[constant ∞-stack]] that is constant on the [[∞-groupoid]] which is the [[core]] of the [[(∞,1)-category]] of _finite_ [[∞-groupoid]]s. We think of this as the **$\infty$-stack of $\infty$-bundles with finite fibers** -- the generalization of the notion of [[covering space]] to the context $\mathbf{H}$. 

This is naturally a [[pointed object]] with point

$$
  ({*} \to \infty FinBund) \;:=\; LConst({*} \to Core(\infty FinGrpd))
$$

the [[∞-stackification]] of the inclusion of constant [[(∞,1)-presheaf|∞-presheaves]] induced from the canonical inclusion ${*} \hookrightarrow $ [[∞Grpd]], identifying the terminal [[∞-groupoid]].

For $X \in \mathbf{H}$ any object, the following terminology is suggestive:

* the $\infty FinBund$-[[principal ∞-bundle]] 
  [[homotopy fiber|classified by]] a [[cocycle]] $X \to \infty FinBund$ 
  is a **covering $\infty$-bundle** of $X$;

* the [[∞-groupoid]]

  $$
    \infty FinBund(X) := \mathbf{H}(X,\infty FinBund)
  $$

  is the $\infty$-groupoid of covering $\infty$-bundles on $X$;

* hence the [[cohomology]] $H(X,\infty FinBund) = \pi_0\mathbf{H}(X,\infty FinBund)$ is the set of equivalence classes of covering $\infty$-bundles of $X$.

If the [[left adjoint]] $LConst$ is also a [[right adjoint]]

$$
  Sh_{(\infty,1)}(C)
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Pi}{\to}}
  \infty Grpd   
$$

then we have

$$
  \infty FinBund(X) \simeq Func(\Pi(X),\infty FinGrpd)
  \,.
$$

## References

A discussion of locally constant $\infty$-stacks over [[topological space]]s is in

* [[Bertrand Toen]], _Toward a Galoisian interpretation of homotopy theory_ ([arXiv:0007157](http://arxiv1.library.cornell.edu/abs/math/0007157))


[[!redirects locally constant ∞-stack]]
