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

The concept of a _(left/right) cancellative category_ is the generalization of the concept of [[cancellative monoid]] from [[monoids]] to [[categories]].

## Definition

In [[category theory]], a category $\mathcal{C}$ is **left cancellative** if all [[morphisms]] in $\mathcal{C}$ are [[monomorphisms]] (for arbitrary morphisms $f,h_0,h_1$ of $\mathcal{C}$, if $f\circ h_0=f\circ h_1$, then $h_0=h_1$). $\mathcal{C}$ is **right cancellative** if all [[morphisms]] in $\mathcal{C}$ are [[epimorphisms]] (for arbitrary morphisms $f,h_0,h_1$ of $\mathcal{C}$, if $h_0 \circ f=h_1\circ f$, then $h_0=h_1$). $\mathcal{C}$ is **cancellative** if it is both left cancellative and right cancellative.

The following was observed by [[Zhen Lin]] on [MathOverflow](https://math.stackexchange.com/a/4694679).

**Proposition.**
The following are equivalent for a category $\mathcal{C}$.

- Every morphism in $\mathcal{C}$ is a monomorphism.
- Every slice category $\mathcal{C}/X$ is a [[preorder]].
- There exists a preorder $\mathcal{D}$ and a surjective [[discrete fibration]] $\mathcal{D} \to \mathcal{C}$.
- (Assuming $\mathcal{C}$ is small.) The presheaf topos $[\mathcal{C}^{\text{op}}, \text{Set}]$ is an [[étendue]], i.e. there exists a presheaf $D : \mathcal{C}^{\text{op}} \to \text{Set}$ such that the unique morphism $D \to 1$ is an epimorphism and the slice $[\mathcal{C}^{\text{op}}, \text{Set}]_{/ D}$ is a localic topos.
- $\mathcal{C}$ is the codescent category of a preordered groupoid whose domain and codomain maps are discrete fibrations.

## Examples

### Cancellative categories

 * any [[cancellative monoid]], regarded as a category with a single object

 * any [[groupoid]]

 * any [[poset]], or indeed any [[preorder]]  

### Left cancellative categories
 
 * the category [[Field]] of [[fields]] (with [[ring]] [[homomorphisms]] as the morphisms)

 * the category of nontrivial [[vector spaces]] (over the field of [[real numbers]] or [[complex numbers]]) equipped with positive definite [[inner products]]  

## Related concepts

* [[cancellative monoid]]

## References

* M. V. Lawson and A. R. Wallis, A categorical description of Bass-Serre theory ([arXiv:1304.6854v5](https://arxiv.org/abs/1304.6854))

* M. V. Lawson, "Ordered Groupoids and Left Cancellative Categories"
Semigroup Forum, Volume **68**, Issue 3, (2004),  458&#8211;-476 

[[!include oidification - table]]

[[!redirects cancellative categories]]

[[!redirects left cancellative category]]
[[!redirects left cancellative categories]]
[[!redirects left-cancellative category]]
[[!redirects left-cancellative categories]]

[[!redirects right cancellative category]]
[[!redirects right cancellative categories]]
[[!redirects right-cancellative category]]
[[!redirects right-cancellative categories]]

[[!redirects all morphisms monic]]
[[!redirects all arrows monic]]
[[!redirects all morphisms epic]]
[[!redirects all arrows epic]]

[[!redirects all morphisms monic and epic]]
[[!redirects all arrows monic and epic]]
[[!redirects all morphisms epic and monic]]
[[!redirects all arrows epic and monic]]