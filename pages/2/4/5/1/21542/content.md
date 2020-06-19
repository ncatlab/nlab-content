
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


[[!redirects theory of $\mathbb{T}-model homomorphisms]]
[[!redirects theory of T-model homomorphisms]]
[[!redirects theory of homomorphism]]

#Contents#
* table of contents
{:toc}

##Idea
For any [[geometric theory]] $\mathbb{T}$ there exists a geometric theory $\mathbb{T}^2$, the **theory of $\mathbb{T}$-model homomorphisms**, whose models in a [[Grothendieck topos]] $\mathcal{E}$ are precisely the homomorphisms between $\mathbb{T}$-models in $\mathcal{E}$.

## Definition

Let $\mathbb{T}$ be a [[geometric theory]] over the [[signature]] $\Sigma$.

Let $\Sigma^2$ be the signature containing a pair of new sort symbols $X^0$, $X^1$ and a new function symbol $f_X:X^0\to X^1$ for any sort symbol $X$ in $\Sigma$, as well, as pairs $g^0:X_1^0\times\dots\times X_n^0\to Y^0$, $g^1:X_1^1\times\dots\times X_n^1\to Y^1$ of new functions symbols (resp. pairs $r^0\rightarrowtail X_1^0\times\dots\times X_n^0$, $r^1\rightarrowtail X_1^1\times\dots\times X_n^1$ of new relation symbols) for any function symbol $g:X_1\times\dots\times X_n\to Y$ (resp. relation symbol $r\rightarrowtail X_1\times\dots\times X_n$) in $\Sigma$.

The **theory of $\mathbb{T}$-model homomorphisms** is the theory $\mathbb{T}^2$ over the signature $\Sigma^2$ with the following sequents:

 A pair of sequents $\varphi^0\vdash \psi^0$, $\varphi^1\vdash \psi^1$ for any sequent $\varphi\vdash \psi$ in $\mathbb{T}$ where the new sequents result from replacing the function and relation symbols in $\varphi\vdash \psi$ with their 0-indexed, resp. 1-indexed pendants. Plus a sequent

:$\top\vdash f_Y(g^0(x_1,\dots,x_n))=g^1(f_{X_1}(x_1),\dots,f_{X_n}(x_n))$

resp.

:$r^0(x_1,\dots,x_n)\vdash r^1(f_{X_1}(x_1),\dots,f_{X_n}(x_n))$

for any pair $g^0$, $g^1$ of function symbols (corresponding to $g:X_1\times\dots\times X_n\to Y$ in $\Sigma$), resp. any pair $r^0$, $r^1$ of relation symbols (corresponding to $r\rightarrowtail X_1\times\dots\times X_n$ in $\Sigma$), in $\Sigma^2$.



## Properties

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a [[Grothendieck topos]]. Then

$$Mod_{\mathbb{T}^2}(\mathcal{E})=Mod_\mathbb{T}(\mathcal{E})^2=Mod_\mathbb{T}(\mathcal{E}^2)\quad.$$
=--

Cf. Johnstone ([1977](#J77), p. 203), Mac Lane-Moerdijk ([1994](#MM94), ex.X.5 p.572).

## Examples

* Let $\mathbb{T}^\emptyset_\emptyset$ and $\mathbb{T}^\emptyset_1$ be the [[empty theory]], resp., the inconsistent theory, over the empty signature. Then $\mathbb{T}^{\emptyset 2}_\emptyset=\mathbb{T}^\emptyset_\emptyset$ and $\mathbb{T}^{\emptyset 2}_1=\mathbb{T}^\emptyset_1$ in accordance with the fact that these theories have only empty models whence all model homomorphisms are [[identity|identity morphisms]] of empty models. In other words, squaring theories obeys the laws of arithmetics at 0 and 1.

* Let $\mathbb{O}$ be the [[theory of objects]] i.e. the theory with no sequents over the signature with one sort symbol $O$. Then $\mathbb{O}^2$ is the theory with no sequents over the signature with two sort symbols $O^0$, $O^1$ and a function symbol $f_O:O^0\to O^1$.

## Related Entries

* [[geometric theory]]

* [[theory of objects]]

* [[theory of decidable objects]]

* [[exponentiable topos]]

* [[Sierpinski topos]]

## References


* {#J77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York (1977). (Also available as Dover Reprint, Mineola 2014)

* {#MM94} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _Sheaves in Geometry and Logic_ , Springer Heidelberg 1994.

