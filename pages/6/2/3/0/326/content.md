For any [[category]] $C$ and any [[object]] $c \in C$, the **hom-functor**
$$ hom(-,c) : C^{op} \to Set $$ 
is the [[functor]] from $C^{op}$ to [[Set]] sending any object $x \in C$ to the [[hom-set]] $hom(x,c)$.

To fully describe this functor we must also say what it does to morphisms in $C^{op}$; only this explains why we need $C^{op}$ rather than $C$ here.   We hope that someone reading this will be sufficiently motivated to include this information.

There is also a **hom-functor**
$$ hom(c,-) : C \to Set $$
sending any object $x \in C$ to the hom-set $hom(c,x)$.

And indeed, both the hom-functors just mentioned can easily be obtained from the more general functor, also called a **hom-functor**:
$$ hom : C^{op}\times C \to Set, $$
sending any object $(x,y) \in C^{op}\times C$ to the hom-set $hom(x,y)$.