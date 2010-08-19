
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


## Definition

Let $Ab^{\Delta}$ be the [[category of cosimplicial objects]] in the category [[Ab]] of [[abelian group]]s.

Write $N : Ab^{\Delta} \to Ch^\bullet_+$ for the normalized cochain complex [[Dold-Kan correspondence]] functor to non-negatively graded [[cochain complex]]es.

Say that a morphism $f$ in $Ab^{\Delta}$ is

* a _fibration_ if it is degreewise a [[surjection]];

* a _weak equivalence_ if $N(f)$ is a [[quasi-isomorphism]].



+-- {: .un_prop}
###### Proposition

With these definitions, cosimplicial abelian groups form a [[model category]] $Ab^\Delta_{proj}$.

With respect to the canonical [[sSet]]-[[enriched category]]-structure on $Ab^{\Delta}$ (described at [[category of cosimplicial objects]]) this is a [[simplicial model category]].

=--

+-- {: .proof}
###### Proof

(...)

To show the structure of an [[sSet]]-[[enriched model category]] we need to show that for $i : C \to C'$ any cofibration in the standard [[model structure on simplicial sets]] and $j : X \to Y$ a fibration of cosimplcial abelian groups the morphism 

$$
  k : X^{C'} \to X^C \times_{Y^C} Y^{C'}
$$ 

induced by the [[power]]ind is a fibration, which is acyclic if $i$ or $j$ is.

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


=--


## Properties

Under the dual [[Dold-Kan correspondence]] the model structure on cosimplicial groups is equivalent to the [[model structure on chain complexes|model structure on cochain complexes]] in non-negative degree.



## References

The [[model structure on cosimplicial algebras]] is discussed in detail in

* [[Bertrand Toen]], _Champs affine_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))

The above proof that $Ab^\Delta_{proj}$ is a simplicial model category mimics the proof on page 41 there. Indeed, the claim is that the model structure on cosimplicial algebras is the [[transferred model structure]] induced by the above from the evident forgetful functor.