[[!redirects II.5, the Frobenius and the Verschiebung morphism]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)
 
Let $k$ be a field with prime characteristic $p$.

The [[Frobenius morphism]] $F_G: G\to G^{(p)}$ commutes with finite products and hence if $G$ is a [[k-group-functor]] $G^{(p)}$ is a $k$-group functor, too, and $F_G$ is a $k$-group morphism.

We abbreviate $F_G^n:G\to G^{(p^n)}$.

The same is true for $k$-formal groups.

Let $G$ be a commutative affine $k$-group. Then for the [[Cartier duality|Cartier dual]] $D(-)$ we have

$$D(G^{(p)})=D(G)^{(p)}$$

By Cartier duality we obtain the [[Verschiebung morphism]] $V_G:G^{(p)}\to G$ for which holds $\hat D(V_G)=F_{\hat D(G)}$. We abbreviate $V_G^n:G^{(p^n)}\to G$.

Let $f:G\to H$ be a morphism of commutative affine $k$-groups. The the following diagram is commutative

$$\array{
G^{(p)}
&\stackrel{V_G}{\to}&
G
&\stackrel{F_G}{\to}&
G^{(p)}
\\
\downarrow^{f^{(p)}}&&\downarrow^f&&\downarrow^{f^{(p)}}
\\
F^{(p)}
&\stackrel{V_H}{\to}&
H
&\stackrel{F_H}{\to}&
H^{(p)}
}$$

Moreover we have

$$V_G\circ F_G=p id_G$$

and

$$F_G\circ V_G=p id_{G^{(p)}}$$

## Examples

$V_{\mu_k}$ is the identity and $V_{\alpha_k}$ is zero.

This follows since $F$ is an epimorphism and $p id_{\mu_k}=F_{\mu_k}$ and $p id_{\alpha_k}=0$