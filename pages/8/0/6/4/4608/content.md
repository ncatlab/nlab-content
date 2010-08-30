
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Let $Ab^{\Delta}$ be the [[category of cosimplicial objects]] in the category [[Ab]] of [[abelian group]]s -- the category of _cosimplicial abelian groups_ .

This entry discusses structures of [[model categories]] on $Ab^\Delta$.

By the dual [[Dold-Kan correspondence]] there is an [[equivalence of categories]] $Ab^\Delta \stackrel{\overset{\Xi}{\leftarrow}}{\underset{N}{\to}} Ch^\bullet_+(Ab)$ with the [[category of cochain complexes]] in non-negative degree. Since [[Ab]] is an [[abelian category]], we have by general results various <a href="http://ncatlab.org/nlab/show/model+structure+on+chain+complexes#CochainNonNeg">model structures on cochain complexes</a>. Via the Dold-Kan equivalence, all of these induce model structures on $Ab^\Delta$.



## Properties

### Simplicial enrichment of the projective structure {#SimplicialEnrichmentOfProjective}

Since [[Ab]] has all [[limit]]s and [[colimit]]s, the [[category of cosimplicial objects]] (as described there) $Ab^\Delta$ inherits canonically the structure of an [[sSet]]-[[enriched category]] which is [[power]]ed and [[copower]]ed. 

Write $Ab^\Delta_{proj}$ for the model structure that is induced by the dual [[Dold-Kan correspondence]] $Ab^\Delta \simeq Ch^\bullet_+(Ab)$ from the [[model structure on cochain complexes]] whose fibrations are the _degreewise surjections_ (and weak equivalences the usual [[quasi-isomorphism]]s). This is described in detail <a href="http://ncatlab.org/nlab/show/model+structure+on+chain+complexes#CochainNonNegProj">here</a>.
So this induces the model structure $Ab^\Delta_{proj}$ whose fibrationns are also the degreewise surjections in $Ab$ (using that the [[Moore complex|normalized cochain complex]]-functor preserves surjections.) 

+-- {: .un_prop}
###### Proposition

The canonical $sSet$-enrichement of $Ab^\Delta$ is compatible with the model category structure $Ab^\Delta_{proj}$  in that the combination gives $Ab^\Delta$ the structure of a [[simplicial model category]].

=--

+-- {: .proof}
###### Proof


We need check the [[pushout-product axiom]] of an [[enriched model category]] of the standard [[model structure on simplicial sets]] $sSet_{Quillen}$

So we need to show that for $i : C \to C'$ any cofibration in $sSet_{Quillen}$ and $j : X \to Y$ a fibration of cosimplcial abelian groups (degreewise surjection) the morphism 

$$
  k : X^{C'} \to X^C \times_{Y^C} Y^{C'}
$$ 

induced by the [[power]]ing $(-)^(-) : Ab^\Delta \times sSet \to Ab^\Delta$ is a fibration, which is acyclic if $i$ or $j$ is.

That $k$ is a fibration is easily checked. To see acyclicity we first notice the following 

**Lemma.** If $i : C \to C'$ is a weak equivalence then for every cosimplicial abelian group $A$ we have $A^i$ is a weak equivalence.

To see this observe that $A^C$ is the diagonal of an evident [[bisimplicial object|bisimplicial abelian group]] and that $A^i$ is then in one argument a degreewise [[quasi-isomorphism]]. Since forming total complexes preserves degreewise equivalences, the lemma follows.

To continue the main proof, notice that we have a [[short exact sequence]]

$$
  0 \to X^C \times_{Y^C} Y^{C'} \to X^C \oplus Y^{C'} \stackrel{f}{\to}
  Y^C \to 0
$$

with $f : (x,y) \mapsto j^C(x) - Y^i(y)$. This induces a [[fiber sequence|long exact sequence in cohomology]]

$$
  \cdots \to 
  H^p(X^C \times_{Y^C} Y^{C'})
  \to 
  H^p(X^C) \oplus H^i(Y^{C'})
  \to
  H^p(Y^C) 
  \to
  H^{p+1}(X^C \times_{Y^C} Y^{C'})
  \to 
  \cdots
  \,.
$$

If $i$ is a weak equivalence, then by the above lemma we have that 

$$
  ker(H^p(X^C) \oplus H^p(Y^{C'}) \to H^p(Y^C))
  \simeq
  H^p(X^C)
  \,.
$$

Inspection of the [[connecting homomorphism]] then shows that $H^p(Y^C) \to H^{p+1}(X^C \times_{Y^C} Y^{C'})$ is the 0-map. In total this implies that we have an [[isomorphism]]

$$
  H^p(X^C \times_{Y^C} Y^{C'}) \stackrel{\simeq}{\to}
  H^p(X^C)
$$

for all $p$, and hence that 

$$
  X^C \times_{Y^C} Y^{C'} \to  X^C
$$

is a weak equivalence. Since by the above lemma also $X^i : X^{C'} \to X^C$ is a weak equivalence, it follows by [[category with weak equivalences|2-out-of-3]] that the morphism $k$ is indeed a weak equivalence if $i$ is.

An analogous argument shows that $k$ is a weak equivalence if $j$ is.

This argument is essentially that on page 41 of ([To&euml;n](#Toen))

=--



## References

The [[model structure on cosimplicial algebras]] is discussed in detail in

* [[Bertrand Toën]], _Champs affine_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))
{#Toen}

The above proof that $Ab^\Delta_{proj}$ is a simplicial model category mimics the proof on page 41 there. Indeed, the claim is that the model structure on cosimplicial algebras is the [[transferred model structure]] induced by the above from the evident forgetful functor.