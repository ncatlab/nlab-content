## Idea

In what follows, all rings are assumed to be commutative and unital. 

Since the ring $\mathbb{Z}[x]$ of integer polynomials in one variable is the free ring on $1$, we have an isomorphism $R \stackrel \sim \to \mathsf{Ring}(\mathbb{Z}[x], R)$ which sends an element $r \in R$ to evaluation at $r$, $p(x) \mapsto p(r)$. If we let $R$ also be $\mathbb{Z}[x]$, this gives exactly "substitution" or "composition" of polynomials. A plethory is a ring which carries a substitution structure. The ring $\Lambda$ of [[symmetric functions]] is another example.

The data of a plethory is also what is needed to represent a "natural operation" on the category of rings. For example $\mathsf{Ring}(\mathbb{Z}[x],-)$ is the identity functor on $\mathsf{Ring}$, and $\mathsf{Ring}(\Lambda,-)$ sends every ring to its [[ring of Witt vectors]].

## Definitions

A [[biring]] is a (commutative) ring object in $\mathsf{Ring}^{op}$. The category of birings is $\mathsf{Ring}(\mathsf{Ring}^{op})^{op}$. The extra op ensures that a biring homomorphism is a ring homomorphism, not a reversed ring homomorphism.

The category of birings is equivalent to $\mathsf{LAdj}(\mathsf{Ring},\mathsf{Ring})$, the category of left adjoints $\mathsf{Ring} \to \mathsf{Ring}$, and also to $\mathsf{RAdj}(\mathsf{Ring},\mathsf{Ring})^{op}$, opposite of the category of right adjoints $\mathsf{Ring} \to \mathsf{Ring}$. Under this equivalence, the category of birings inherits a monoidal structure induced from endofunctor composition. The monoidal product is called the *substitution product*, denoted by $\odot$. The unit object is the ring of polynomials $\mathbb{Z}[x]$. A generators-and-relations description of $\odot$ can be found in ([TW70](#TW70)).

A **plethory** is a monoid in $(\mathsf{Biring}, \odot, \mathbb{Z}[x])$. Equivalently, a plethory is a right adjoint comonad $\mathsf{Ring} \to \mathsf{Ring}$.  Equivalently, a plethory is a left adjoint monad $\mathsf{Ring} \to \mathsf{Ring}$. 

### Plethory over a ring

For any (commutative) ring $k$, a $k$-**plethory** is a [[monoid object]] in the [[monoidal category]] of $k$-$k$-[[biring|birings]], with respect to the composition product. That is, it is a biring $P$ equipped with an associative map of birings $\circ: P \odot_k P \to P$ and unit $k \langle e \rangle \to P$.

In other words, 

>a $k$-plethory is a commutative k-algebra together with a comonad structure on the covariant functor it represents, much as a k-algebra is the same as a $k$-module that represents a comonad. So, just as a $k$-algebra is exactly the structure that knows how to act on a $k$-module, a $k$-plethory is the structure that knows how to act on a commutative $k$-algebra. ([BW05](#BW05))

## Related concepts

* [[biring]]

* [[Tall-Wraith monoid]]

* [[2-plethory]]

##References

The idea was introduced here, where it was called a "biring triple":

* {#TW70} D. Tall and [[Gavin Wraith|G. Wraith]], Representable functors and operations on rings, _Proc. London Math. Soc._ **3** (1970), 619--643.

The term "plethory" was introduced here:

* {#BW05} [[James Borger]], [[Ben Wieland]],  Plethystic algebra, _Advances in Mathematics_ **194** (2005), 246--283.  ([web](http://wwwmaths.anu.edu.au/~borger/papers/03/paper03.html))

* {#BMT21} [[John Baez]], [[Joe Moeller]], [[Todd Trimble]], Schur functors and categorified plethysm, [arXiv:2106.00190](https://arxiv.org/abs/2106.00190)

[[!redirects plethories]] 
[[!redirects biring triple]] 