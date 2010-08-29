The __Godement product__ of two [[natural transformations]] between appropriate [[functors]] is their [[horizontal composition]] as 2-cells in the [[2-category]] [[Cat]] of [[categories]], functors and natural transformations:
: ![codecogs](http://latex.codecogs.com/gif.latex?\xymatrix{A\ar@/^/[rr]^{F_1}\ar@/_/[rr]_{G_1}%26\Downarrow\alpha%26B\ar@/^/[rr]^{F_2}\ar@/_/[rr]_{G_2}%26\Downarrow\beta%26C}\quad\mapsto\quad\xymatrix{A\ar@/^/[rr]^{F_1;F_2}\ar@/_/[rr]_{G_1;G_2}%26\Downarrow\alpha\ast\beta%26C})

For categories $A,B,C$, if $\alpha\colon F_1\to G_1\colon A\to B$ and $\beta\colon F_2\to G_2\colon B\to C$ are natural transformations of functors, the components $(\alpha * \beta)_M$ of the Godement product $\alpha * \beta\colon F_1 ; F_2 \to G_1 ; G_2$ (or $\beta \circ \alpha\colon F_2\circ F_1\to G_2\circ G_1$) are defined by any of the two equivalent formulas:
$$
(\beta\circ\alpha)_M = \beta_{G_1(M)}\circ F_2(\alpha_M)
$$
$$
(\beta\circ\alpha)_M = G_2(\alpha_M)\circ \beta_{F_1(M)}
$$
that is:
$$
  \array{
    F_2(F_1(M))
    &
    \stackrel{F_2(\alpha_M)}{\to}
    &
    F_2(G_1(M))
    \\
    \beta_{F_1(M)}\downarrow
    &
    \searrow^{(\beta\circ\alpha)_M}
    &
    \downarrow \beta_{G_1(M)}
    \\ G_2(F_1(M))
    &
    \stackrel{G_2(\alpha_M)}{\to} & G_2(G_1(M))
  }
  \,.
$$

The Godement product is strictly associative (so that $Cat$ is a [[strict 2-category]]).

The [[interchange law]] in (general) $2$-categories (which in the case of $Cat$ boils down to assertion that the two formulas above are equivalent) is also sometimes called _Godement interchange law_.


[[!redirects Godement product]]
[[!redirects Godement products]]

[[!redirects horizontal composite of natural transformations]]
[[!redirects horizontal composites of natural transformations]]
[[!redirects horizontal composition of natural transformations]]
[[!redirects horizontal compositions of natural transformations]]
