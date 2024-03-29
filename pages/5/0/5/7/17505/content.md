# 2-dinatural transformations

* table of contents
{: toc}

## Idea

A *2-dinatural transformation* is a [[categorification]] of a [[dinatural transformation]].  It is more complicated since there are three kinds of [[opposite 2-category]], and also because it could be [[lax natural transformation|lax]], colax, or pseudo as well as strict.

## Definition

Let $C$ and $D$ be [[2-categories]] and let
$$F,G: C^{coop}\times C^{op}\times C^{co} \times C\to D$$
be [[2-functors]].  A **lax 2-dinatural transformation** $\alpha:F\to G$ consists of

1. For each $x\in C$, a 1-morphism component
   $$ \alpha_x : F(x,x,x,x) \to G(x,x,x,x) $$

2. For each 1-morphism $f:x\to y$ in $C$, a 2-morphism component from the composite
   $$ F(y,y,x,x) \xrightarrow{F(f,f,1,1)} F(x,x,x,x) \xrightarrow{\alpha_x} G(x,x,x,x) \xrightarrow{G(1,1,f,f)} G(x,x,y,y) $$
   to the composite
   $$ F(y,y,x,x) \xrightarrow{F(1,1,f,f)} F(y,y,y,y) \xrightarrow{\alpha_y} G(y,y,y,y) \xrightarrow{G(f,f,1,1)} G(x,x,y,y).$$
   (This is a generalization of the hexagon identity for an ordinary [[dinatural transformation]].)

3. For any 2-morphism $\mu:f\to g:x\to y$ in $C$, the two composites
   $$ G(1,1,g,f)\circ \alpha_x \circ F(g,f,1,1)
   \xrightarrow{G(1,1,\mu,1) \ast 1 \ast F(\mu,1,1,1)}
   G(1,1,f,f) \circ \alpha_x \circ F(f,f,1,1)
   \xrightarrow{\alpha_f}
   G(f,f,1,1) \circ \alpha_y \circ F(1,1,f,f)
   \xrightarrow{G(1,\mu,1,1) \ast 1 \ast F(1,1,1,\mu)}
   G(f,g,1,1) \circ \alpha_y \circ F(1,1,f,g)
   $$
   and
   $$ G(1,1,g,f)\circ \alpha_x \circ F(g,f,1,1)
   \xrightarrow{G(1,1,1,\mu) \ast 1 \ast F(1,\mu,1,1)}
   G(1,1,g,g) \circ \alpha_x \circ F(g,g,1,1)
   \xrightarrow{\alpha_g}
   G(g,g,1,1) \circ \alpha_y \circ F(1,1,g,g)
   \xrightarrow{G(\mu,1,1,1) \ast 1 \ast F(1,1,\mu,1)}
   G(f,g,1,1) \circ \alpha_y \circ F(1,1,f,g)
   $$
   are equal.

4. Each 2-morphism component $\alpha_{1_x}$ is the identity $1_{\alpha_x}$.

5. For any composable 1-morphisms $x\xrightarrow{f} y \xrightarrow{g} z$, the composite of $\alpha_f$ and $\alpha_g$ (together with two functoriality commutative squares for $F$ and $G$) is equal to $\alpha_{g f}$.

## Examples

If one of $F$ and $G$ is constant and the other depends only on $C^{op}\times C$, we obtain a notion of **2-extranatural transformation**.

If $F$ and $G$ each depend on only one factor in $C^{coop}\times C^{op}\times C^{co} \times C$, we obtain a notion of strict 2-natural transformation from a 2-functor of any arbitrary variance to a 2-functor of any other arbitrary variance.  For example, if $F:C^{co}\to D$ and $G:C^{op}\to D$, then a lax 2-dinatural transformation $\alpha:F\to G$ consists of an $\ob(\mathbf{C})$-indexed family of $1$-morphisms $FX\stackrel{\alpha_X}{\to} GX$ in $\mathbf{D}$, and for each two objects $X,Y$ of $\mathbf{C}$, an $\ob[X,Y]$-indexed family of $2$-morphisms $\alpha_f$, so that for every $2$-morphism $f\stackrel{\gamma}{\Rightarrow} g$, we have the commutative diagram of $2$-morphisms in $\mathbf{D}$:
$$
\array{
&&FX&\stackrel{Ff}{\rightarrow}&FY\\
&&\alpha_X\downarrow&\stackrel{\alpha_f}{\Rightarrow}&\downarrow\alpha_Y&&FX\\
&&GX&\stackrel{Gf}{\leftarrow}&GY&&\downarrow Ff\\
FX&\stackrel{id}{\neArrow}&&&& \stackrel{G\gamma.(\alpha_Y\circ Ff)}{\seArrow}&FY\\
\alpha_X\downarrow&&&&&&\downarrow\alpha_Y\\
FY&\stackrel{id}{\seArrow}&&&&\stackrel{(Gg\circ\alpha_Y).F\gamma}{\neArrow}&GY\\
&&FX&\stackrel{Fg}{\rightarrow}&FY&&\downarrow Gg\\
&&\alpha_X\downarrow&\stackrel{\alpha_g}{\Rightarrow}&\downarrow\alpha_Y&&GX\\
&&GX&\stackrel{Gg}{\leftarrow}&GY
}$$
where . is whiskering/horizontal composition. Furthermore, given composable $1$-morphisms $X\stackrel{f}{\rightarrow}Y\stackrel{h}{\rightarrow} Z$, the $2$-morphisms $\alpha_X\stackrel{\alpha_f}{\Rightarrow}Gf\circ\alpha_Y\circ Ff$ and $\alpha_Y\stackrel{\alpha_h}{\Rightarrow}Gh\circ\alpha_Z\circ Fh$ are related via the formula $\alpha_{h\circ f}=(Gf.\alpha_h.Ff)\circ\alpha_f$, which says that the [[pasting diagram]] of $2$-morphisms:
$$
\array{
FX&\stackrel{Ff}{\rightarrow}&FY&\stackrel{Fh}{\rightarrow}&FZ\\
\alpha_X\downarrow&\stackrel{\alpha_f}{\Rightarrow}&\downarrow\alpha_Y&\stackrel{\alpha_h}{\Rightarrow}&\downarrow\alpha_Z\\
GX&\stackrel{Gf}{\leftarrow}&GY&\stackrel{Gh}{\leftarrow}&GZ
}$$
reduces to
$$
\array{
FX&\stackrel{Fh\circ Ff}{\rightarrow}&FZ\\
\alpha_X\downarrow&\stackrel{\alpha_{h\circ f}}{\Rightarrow}&\downarrow\alpha_Z\\
GX&\stackrel{Gh\circ Gf}{\leftarrow}&GZ
}$$

This sort of transformation appears in the [[category of V-enriched categories]], which is a $2$-category which comes with a [[unit enriched category]] $\mathcal{I}$ and either a lax natural transformation $[\mathcal{I},-]^{op}\Rightarrow[[\mathcal{I},-],V_0]$ (in the case of $\mathcal{V}$ a [[monoidal category|monoidal structure]] on $V$), or a lax natural transformation $[\mathcal{I},-]^{op}\Rightarrow[-,V^e]$ (in the case of $\mathcal{V}$ a [[closed category|closed structure]] on $[\mathcal{I},V^e]\cong V_0$).

[[!redirects 2-dinatural transformations]]
[[!redirects strict 2-dinatural transformation]]
[[!redirects strict 2-dinatural transformations]]
[[!redirects lax 2-dinatural transformation]]
[[!redirects lax 2-dinatural transformations]]
[[!redirects pseudo 2-dinatural transformation]]
[[!redirects pseudo 2-dinatural transformations]]
[[!redirects colax 2-dinatural transformation]]
[[!redirects colax 2-dinatural transformations]]
