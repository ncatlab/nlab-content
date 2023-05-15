
#Contents#
* table of contents
{:toc}

## Idea

The __center of an [[additive category]]__ $A$ is the [[endomorphism ring]] of the [[identity functor]] $Id_A$ (cf. with [[center]]). 

In general, the center is not functorial, but it is functorial in some important special circumstances, like some reconstruction theorems in the commutative setup.  (It is also functorial on [[equivalence of categories|equivalences]].)

## Example

Let $R Mod$ be the category of modules for a commutative ring $R$.  Then the center of $R Mod$ is $R$.  To see this, first note that for any $r \in R$, multiplication by $r$ acts as an endomorphism of each $R$-module (because $R$ is commutative), and this endomorphism is natural.   This gives a ring homomorphism from $R$ to the center of $R Mod$.  This homomorphism is injective because distinct elements of $r$ act differently as multiplication on the $R$-module given by $R$ itself.   To see it is surjective, suppose $\alpha$ is a natural transformation of the identity functor on $R \Mod$.  Then $\alpha_R \colon R \to R$ must be multiplication by some $r \in R$, since every endomorphism of the $R$-module $R$ is given by multiplication by some $r \in R$.  More generally, for any module $M$ and any $m \in M$ there is a module homomorphism $f \colon R \to M$ with $f(1) = m$, and then
by naturality
$$\alpha_M (m) = \alpha_M f(1) = f (\alpha_R 1) = f(r) = r m$$
so $\alpha_M$ is multiplication by $r$.

## Related concepts

* [[center]]

* [[Drinfeld center]]

## References

An early occurence of the definition of the center of an additive category is in section 5.d of 

* [[Pierre Gabriel]], [[Des catégories abéliennes]], Bulletin de la Soci&#233;t&#233; Math&#233;matique de France __90__ (1962), 323-448 ([numdam](http://www.numdam.org/item?id=BSMF_1962__90__323_0))

[[!redirects center of an abelian category]]
