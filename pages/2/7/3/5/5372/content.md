
#Contents#
* table of contents
{:toc}

## Idea

Let $C$ be any [[small category]], write $PSh(C) = [C^{op}, Set]$ for its [[category of presheaves]] and let

$$
  \Omega^\bullet_C : C^{op} \to dgAlg
$$

be _any_ functor to the category of [[dg-algebra]]s. Following the logic of [[space and quantity]], we may think of the objects of $C$ as being _test spaces_ and the functor $\Omega^\bullet_C$ as assigning to each test space its [[deRham complex|deRham dg-algebra]].

An example of this construction that is natural from the point of view of [[differential geometry]] appears in the study of [[diffeological space]]s, where $C$ is some subcategory of the category [[Diff]] of smooth [[manifold]]s, and $\Omega^\bullet_C$ is the restriction of the ordinary assignment of [[differential form]]s to this. But in the application to topological spaces, in the following, we need a choice for $C$ and $\Omega^\bullet_C$ that is non-standard from the point of view of [[differential geometry]]. Still, it follows the same general pattern.

After postcomposing with the [[forgetful functor]] that sends each [[dg-algebra]] to its underlying [[set]], the functor $\Omega^\bullet_C$ becomes itself a [[presheaf]] on $C$. For $X \in PSh(C)$ any other presheaf, we extend the notation and write 

$$
  \Omega^\bullet_C(X) := Hom_{PSh(C)}(X, \Omega^\bullet_C)
$$

for the [[hom-set]] of presheaves. One checks that this set naturally inherits the structure of a [[dg-algebra]] itself, where all operations are given by applying "pointwise" for each $p : U \to X$ with $U \in C$ the operations in $\Omega^\bullet_C(U)$. This way we get a functor

$$
  \Omega^\bullet_C : PSh(C) \to dgAlg^{op}
$$

to the [[opposite category]] of that of [[dg-algebra]]s. We may think of $\Omega^\bullet_C(X)$ as the deRham complex of the presheaf $X$ as seen by the functor $\Omega^\bullet_C : C \to dgAlg^{op}$.

By [[category theory|general abstract nonsense]] this functor has a [[right adjoint]] $K_C : dgAlg^{op} \to PSh(C)$, that sends a dg-algebra $A$ to the [[presheaf]]

$$
  K_C(A) : U \mapsto Hom_{dgAlg}(\Omega^\bullet_C(U), A)
  \,.
$$

The [[adjunction]]

$$
  \Omega^\bullet_C : PSh(C) \stackrel{\leftarrow}{\to} : dgAlg^{op} : K_C
$$

is an example for the adjunction induced from a [[dualizing object]].


## Examples

### Differential forms on simplicial sets

There are various variant of [[differential forms on simplices]]. Each gives rise to a notion of differential forms on [[simplicial set]]s. This is also known as the [[Sullivan construction]] in [[rational homotopy theory]].




[[!redirects differential forms on simplicial sets]]