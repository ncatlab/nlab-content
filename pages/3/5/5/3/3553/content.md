
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **algebra over an endo-[[profunctor]]** ($C$-$C$-[[bimodule]]) is a joint generalization of the notions [[algebra for an endofunctor]] and [[coalgebra for an endofunctor]].

## Definition

For a category $C$ and a $C$-$C$ [[bimodule]] $H : C^{op} \times C \to Set$, an __algebra__ for $H$ is an object $X$ in $C$ and an element $\alpha \in H(X, X)$. ($X$ is called the __carrier__ of the algebra; the element $\alpha$ can be thought of as further structure placed on $X$)

A morphism between two algebras $(X, \alpha)$ and $(Y, \beta)$ of $H$ is a morphism $m : X \to Y$ in $C$ such that $H(id_x, m) (\alpha) = H(m, id_y) (\beta)$ \[these both being elements of $H(X, Y)$\]. Composition of such morphisms of algebras is given by composition of the underlying morphisms in $C$. There is an an obvious [[forgetful functor]] into $C$ from the category of algebras for $H$, which sends each algebra to its carrier and each algebra morphism to its underlying morphism in $C$; among other properties, this functor is always [[faithful]] and [[conservative functor|conservative]].

##Examples

* [[algebra for an endofunctor|Algebras]] and [[coalgebra for an endofunctor|coalgebras]] for [[endofunctor|endofunctors]] are special cases of algebras for bimodules; specifically, an algebra for an endofunctor $F$ is an algebra for the bimodule $Hom(F(-), ?)$, while a coalgebra for $F$ is an algebra for the bimodule $Hom(-, F(?))$.

* A [[natural transformation]] between functors $F$ and $G$ from $C$ to $D$ is a [[section]] of the forgetful functor into $C$ from the category of algebras for the $C-C$ bimodule $Hom_D(F(-), G(?))$.  That is, it gives every object of $C$ the structure of an algebra for $Hom_D(F(-), G(?))$ in such a way as that every morphism of $C$ has the property of being an algebra morphism between the algebras on its domain and codomain.

* A [[natural numbers object]] (in the weak, unparametrized sense) in a category $C$ with terminal object $1$ is an initial object in the category of algebras for the bimodule $Hom_C(1, ?) \times Hom_C(-, ?)$.  If $C$ has binary coproducts, then this is of course the same as an initial algebra for the endofunctor $1+(-)$.

[[!redirects algebra for an endo-profunctor]]
[[!redirects algebra for an endoprofunctor]]
