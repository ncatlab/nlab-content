<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>


+-- {: .standout}

This is a sub-entry of [[geometric models for elliptic cohomology]] and [[A Survey of Elliptic Cohomology]] 

See there for background and context.

This entry here is about the definition of $(2|1)$-dimensional [[super-cobordism]] categories $(2|1)$-dimensional [[FQFT]]s given by functors on these.

=--

Let [[SDiff]] be the [[category]] of [[supermanifold]]s.

We will define a [[stack]]/[[fibered category]] on $SDiff$ called $E Bord_{2|1}$ whose morphisms are smooth families of (2|1)-dimensional [[super-cobordism]]s, and a [[stack]]/[[fibered category]] $sTV^{fam}$ of topological super vector bundles.

#Super-algebra#

**definition** The category [[SVect]] of [[super vector space]]s is the [[symmetric monoidal category]] which as a [[monoidal category]] is the ordinary monoidal category of $\mathbb{Z}_2$-graded vector spaces for which

$$
  (V \otimes W)^{ev} := V^{ev}\otimes W^{ev} \oplus
    V^{odd} \otimes W^{odd}
$$

and

$$
  (V \otimes W)^{odd} := V^{ev}\otimes W^{odd} \oplus
    V^{odd} \otimes W^{ev}
$$


but equipped with the _unique non-trivial_ symmetric monoidal structure 

$$
  V \otimes W \stackrel{\sigma_{V,W}}{\to}
  W \otimes V
$$

that is given on homogeneously graded elements $v,w$ of degree $|v|, |w| \in \mathbb{Z}_2$ as


$$
  v \otimes w \mapsto (-1)^{|v| |w|} w \otimes v
  \,.
$$

**example** A [[super algebra]] $A$ is a [[monoid]] in $S Vect$. A commutative [[super algebra]] is a comutative [[monoid]].

For instance the [[Grassmann algebra]] $\wedge^\bullet(V)$ over any [[vector space]] $V$ is a super algebra.

**exercise** Define [[derivation]]s on $A$ and define [[super Lie algebra]]s

**example* let $E \to M$ be a finite rank [[vector bundle]]

and let $$\Gamma(\wedge^\bullet E^*)$$ be the [[Grassmann algebra]] (over $C^\infty(M)$) of sections of the fiberwise dual bundle. Then this is a commutative [[super algebra]]. In fact, doing this construction for each open subset of $M$ yields a [[sheaf]] of commutative [[super algebra]]s on the [[category of open subsets]] of $M$.

Notice that this is locally always of the form

$$
  \Gamma(\wedge^\bullet U \times \mathbb{R}^q)
  \simeq
  C^\infty(U)
  \otimes \wedge^\bullet(\mathbb{R}^q)
  \,.
$$

This leads over to the definition of [[supermanifold]]. See there for details.