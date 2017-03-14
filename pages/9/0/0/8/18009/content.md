
#Contents#
* table of contents
{:toc}

## Idea

Any [[free loop space]] $\mathcal{L}X$ has a canonical [[action]] ([[infinity-action]]) of the [[circle group]] $S^1$. The [[homotopy quotient]] $\mathcal{L}(X)/S^1$ of this action might be called the _cyclic loop space_ of $X$. 

If $X = Spec(A)$ is an [[affine variety]] regarded in [[derived algebraic geometry]], then $\mathcal{O}(\mathcal{L}Spec(A))$ is the [[Hochschild homology]] of $A$ and $\mathcal{O}((\mathcal{L}Spec(A))/S^1)$ the corresponding [[cyclic homology]], see the discussion at _[[Hochschild cohomology]]_.

If $X = Y//G$ is the [[homotopy quotient]] of a [[topological space]] by a [[topological group]] action, regarded as a locally constant $\infty$-stack, so that the $S^1$-action on $\mathcal{L}(X//G)$ is an $B \mathbb{Z}$-action, then the restriction of the cyclic loop space to the constant loops $\mathcal{L}_{const}Y//G \to \mathcal{L}(Y//G)$ has been called the _twisted loop space_ in ([Witten 88](#Witten88)). This terminology has been widely adopted, for example in the context of the [[transchromatic character]] map ([Stapleton 11](#Stapleton11))

## Properties

### As right base change along $\ast \to \mathbf{B} S^1$

The cyclic loop space $\mathcal{L}X/S^1$ is equivalently the right [[base change]]/[[dependent product]] along the canonical point inclusion $\ast \to B S^1$ ([this prop.](base+change#CyclicLoopSpace)). See also at _[[double dimensional reduction]]_.

### Ordinary cohomology of $\mathcal{L}X/S^1$ on cyclic cohomology of $X$

Let $X$ be a [[simply connected topological space|simply connected]] [[topological space]]. 

The [[ordinary cohomology]] $H^\bullet$ of its [[free loop space]] is the [[Hochschild homology]] $HH_\bullet$ of its [[singular cohomology|singular chains]] $C^\bullet(X)$:

$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( C^\bullet(X) )
  \,.
$$

Moreover the $S^1$-equivariant cohomology of the loop space, hence the ordinary cohomology of the cyclic loop space $\mathcal{L}X/^h S^1$ is the [[cyclic homology]] $HC_\bullet$ of the singular chains:

$$
  H^\bullet(\mathcal{L}X/^h S^1)
    \simeq
  HC_\bullet( C^\bullet(X) )
$$

([Loday 11](#Loday11))

If the [[coefficients]] are [[rational numbers|rational]], and $X$ is of [[finite type]] then this may be computed by the _[[Sullivan model for free loop spaces]]_, see there the section on _[Relation to Hochschild homology](Sullivan+model+of+free+loop+space#RelationToHochschildHomology)_.


In the special case that the [[topological space]] $X$ carries the structure of a [[smooth manifold]], then the singular cochains on $X$ are equivalent to the [[dgc-algebra]] of [[differential forms]] (the [[de Rham algebra]]) and hence in this case the statement becomes that 


$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( \Omega^\bullet(X) )
  \,.
$$

$$
  H^\bullet(\mathcal{L}X/^h S^1)
    \simeq
  HC_\bullet( \Omega^\bullet(X) )
  \,.
$$

This is known as _[[Jones' theorem]]_ ([Jones 87](#Jones87))

An [[(infinity,1)-category theory|infinity-category theoretic]] proof of this fact is indicated at _[Hochschild cohomology -- Jones' theorem](Hochschild+cohomology#JonesTheorem)_.






### Rational Sullivan model

See at _[[Sullivan model for free loop space]]_

## Related concepts

* [[double dimensional reduction]]

## References

* {#Jones87} [[John D.S. Jones]], _Cyclic homology and equivariant homology_, Invent. Math. __87__, 403-423 (1987) ([pdf](https://math.berkeley.edu/~nadler/jones.pdf))


* {#Witten88} [[Edward Witten]], _The index of the Dirac operator in loop space_. In Elliptic curves and modular forms in algebraic topology (Princeton, NJ, 1986), volume 1326 of Lecture Notes in Math., pages 161&#8211;181. Springer, Berlin, 1988.


* {#Loday11} [[Jean-Louis Loday]], _Free loop space and homology_ ([arXiv:1110.0405](https://arxiv.org/abs/1110.0405))


* {#Stapleton11} [[Nathaniel Stapleton]], _Transchromatic generalized character maps_, Algebr. Geom. Topol. 13 (2013) 171-203 ([arXiv:1110.3346](https://arxiv.org/abs/1110.3346))

[[!redirects cyclic loop spaces]]

[[!redirects twisted loop space]]
[[!redirects twisted loop spaces]]
