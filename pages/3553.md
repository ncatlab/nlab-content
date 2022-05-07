
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of **algebra over an endo-[[profunctor]]** ($C$-$C$-[[bimodule]]) is a joint generalization of the notions [[algebra for an endofunctor]] and [[coalgebra for an endofunctor]].


## Definition

For a category $C$ and a $C$-$C$ [[bimodule]] $H : C^{op} \times C \to Set$, an **algebra** for $H$ is given by a [[functor]] $X \colon D \to C$ and an [[extranatural transformation]] $\ast \to H(X,X)$, where $\ast \colon \mathbf{1} \to Set$ is constant at the [[point]].  $X$ is called the **carrier** of the algebra.  A morphism $(X, \alpha) \to (Y, \beta)$ of $H$-algebras is given by a [[natural transformation]] $\phi \colon X \Rightarrow Y$ such that $H(X,\phi) \circ \alpha = H(\phi,Y) \circ \beta$.

If $D$ is the one-object category, an algebra $(X,\alpha)$ is given by an object $X$ in $C$ and an element $\alpha \in H(X, X)$.  A morphism between two algebras $(X, \alpha)$ and $(Y, \beta)$ is then a morphism $m : X \to Y$ in $C$ such that $H(X, m) (\alpha) = H(m, Y) (\beta)$, these both being elements of $H(X, Y)$.

There is an an obvious [[forgetful functor]] into $C$ from the category of algebras for $H$, which sends each algebra to its carrier and each algebra morphism to its underlying morphism in $C$; among other properties, this functor is always [[faithful]] and [[conservative functor|conservative]].

In fact, the category $Alg(H)$, together with its forgetful functor $U\colon Alg(H)\to C$, has the universal property of an [[Eilenberg-Moore object]], namely that of being the _universal_ $H$-algebra.  Specifically, it is a [[terminal object]] in the category whose objects are functors $G\colon D\to C$ equipped with an [[extranatural transformation]] $\ast \to H(G-,G?)$.  For such an extranatural transformation consists of, for every $d\in D$, an element $\xi_d \in H(G d,G d)$, such that for every morphism $v\colon d\to e$ in $D$, we have $H(id_d,v)(\xi_d) = H(v,id_e)(\xi_e)$.  This is precisely the data of a functor $D\to Alg(H)$ lying over $C$.

## Coalgebras in Prof

One version of [[Yoneda lemma|Yoneda's lemma]] says that for a profunctor $H \colon C &#8696; C$ there is a bijection between extranatural transformations $\ast \to H$ and natural transformations $\hom_C \to H$.  So there are bijections
$$
\array{
  \ast \: {\ddot\to} \: H(X,X) \\
  \hom_D \Rightarrow H(X,X) \\
  C(1,X) \Rightarrow H \circ C(1,X)
}
$$
where the last holds by the usual properties of representable profunctors (see e.g. [[proarrow equipment]]).  This exhibits each $H$-algebra on $X$ in the above sense as a $H$-[[algebra for an endomorphism|coalgebra]] in $Prof$ with carrier $C(1,X)$.

## Examples

* [[algebra for an endofunctor|Algebras]] and [[coalgebra for an endofunctor|coalgebras]] for [[endofunctor|endofunctors]] are special cases of algebras for bimodules; specifically, an algebra for an endofunctor $F$ is an algebra for the bimodule $Hom(F(-), ?)$, while a coalgebra for $F$ is an algebra for the bimodule $Hom(-, F(?))$.

* A [[natural transformation]] between functors $F$ and $G$ from $C$ to $D$ is a [[section]] of the forgetful functor into $C$ from the category of algebras for the $C-C$ bimodule $Hom_D(F(-), G(?))$.  That is, it gives every object of $C$ the structure of an algebra for $Hom_D(F(-), G(?))$ in such a way as that every morphism of $C$ has the property of being an algebra morphism between the algebras on its domain and codomain.

* A [[natural numbers object]] (in the weak, unparametrized sense) in a category $C$ with terminal object $1$ is an initial object in the category of algebras for the bimodule $Hom_C(1, ?) \times Hom_C(-, ?)$.  If $C$ has binary coproducts, then this is of course the same as an initial algebra for the endofunctor $1+(-)$.

## Related concepts

* [[algebra over a monad]], [[algebra over an endofunctor]], [[coalgebra over an endofunctor]]


[[!redirects algebra for an endo-profunctor]]
[[!redirects algebra for an endoprofunctor]]
[[!redirects algebra for a bimodule]]
[[!redirects algebra for a C-C bimodule]]

[[!redirects algebra over a profunctor]]