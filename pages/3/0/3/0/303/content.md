Given two categories $C, D$ enriched in a monoidal category $V$, an <i>enriched functor</i> $F: C \to D$ consists of 

<ul>
<li>
A function $F_0: C_0 \to D_0$ between the underlying collections of objects; 
</li>
<li>
A $(C_0 \times C_0)$-indexed collection of morphisms of $V$, 

$$F_{x, y}: C(x, y) \to D(F_0x, F_0y)$$ 

[where $C(x, y)$ denotes the hom-object $\hom_C(x, y)$ in $V$], compatible with the enriched identities and compositions of $C$ and $D$. 
</li>
</ul>

For more information, see Max Kelly's <a href="http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html">Basic Concepts of Enriched Category Theory</a>. 

+--{.query}
For some reason, the latex within the bulleted items didn't render. Did I do something wrong?
=--