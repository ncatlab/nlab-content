For any [[locally small category]] $C$ and any [[object]] $c \in C$, the **covariant hom-functor**
$$ hom(c,-) : C \to Set $$
is the [[functor]] from $C$ to [[Set]] sending any object $x \in C$ to the [[hom-set]] $hom(c,x)$.

To fully describe this functor we must also say what it does to morphisms in $C$: $f: x \to y$ is sent to the morphism $f_*: hom(c,x) \to hom(c,y)$, which maps $\varphi$ to $f \circ \varphi$.

There is also a **contravariant hom-functor**
$$ hom(-,c) : C^{op} \to Set, $$
where $C^{op}$ is the [[opposite category]] to $C$, which sends any object $x \in C^{op}$ to the hom-set $hom(x,c)$.

And indeed, both the hom-functors just mentioned can easily be obtained from the more general functor, also called a **hom-functor**:
$$ hom : C^{op} \times C \to Set, $$
where $C^{op} \times C$ is the [[product category]] of $C^{op}$ and $C$, which sends any object $(x,y) \in C^{op} \times C$ to the hom-set $hom(x,y)$.

[[!redirects hom-functors]]