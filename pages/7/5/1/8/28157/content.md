## Idea

The category of small additive presheaves of abelian groups on an additive category contains
a subcategory of finitely presented (that is [[compact object|compact]]) objects. This subcategory
has a nice universal property.

## Definition

### Freyd's definition

Let $C$ be an additive subcategory. An additive presheaf is finitely presented if it is a cokernel of a morphism of representables. The full subcategory of object parts of these cokernels is $A(C)$, the Freyd's abelianization of $C$.

Thus, an object $x$ of $A(C)$ is a presheaf such that there exist an exact sequence of presheaves of abelian groups of the form
$$
Hom(-,a)\to Hom(-,b) \to x \to 0
$$
where $a,b$ are objects in $C$.

### Verdier's definition

Verdier has reformulated $A(C)$ without a recourse to presheaves. He considers the (additive) arrow category $Arr(C)$ of $C$ and inside it, the morphisms which he calls negligible.
A morphism $(g:X\to Y,h:X'\to Y'):(f:X\to X')\to(g:Y\to Y')$ is negligible if the compositions $h f = f' g = 0$
are null morphisms. For any pair $(f,f')$ of arrows, the negligible morphisms $f\to f'$ form a subgroup.

Now the objects of $A(C)$ are the objects of the arrow category, while the morphisms are the morphisms among the arrows modulo the negligible morphisms (that is the elements of the quotient group). Now, $C$ embeds in $Arr(C)$ as $X\mapsto id_X$ which projects $Hom$-wise to $A(C)$. For any fixed additive category $E$, the functor $C\to A(C)$ induces a functor
$$
Additive(A(C),E)\to Additive(C,E).
$$

## Literature

* Freyd 1966, Verdier 1967, Neeman


(under construction)

