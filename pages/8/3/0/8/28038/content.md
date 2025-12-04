+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

*Principal SO(4)-bundles* are special [[principal bundles]] with the fourth [[special orthogonal group]] [[SO(4)|$SO(4)$]] as [[structure group]]/[[gauge group]]. Applications include the [[frame bundle]] of an [[orientable]] [[4-manifold]] and [[John Milnor]]'s construction of [[exotic 7-spheres]].

Principal SO(4)-bundles in particular are induced by pairs of [[principal SU(2)-bundles]] using the canonical projection $SU(2)\times SU(2)\cong Spin(4)\twoheadrightarrow SO(4)$. Principal SO(4)-bundles also induce [[principal SO(2)-bundles]] and [[principal SO(3)-bundles]] and are induced by [[principal SO(6)-bundles]] using the canonical inclusions $SO(2)\hookrightarrow SO(3)\hookrightarrow SO(4)\hookrightarrow SO(6)$.

Principal SO(4)-bundles also arise from any principal $G$-bundle with a four-dimensional real [[Lie group]] $G$ using its [[adjoint representation]] $Ad\colon G\rightarrow SL_4(\mathbb{R})$, which induces a map $\mathcal{B}Ad\colon\mathcal{B}G\rightarrow B SO(4)$. 

## Properties

\begin{proposition}
A principal SO(4)-bundle $P$ fulfills:
$$
w_2^2(P)
\equiv p_1(P) mod 2;
$$
$$
w_4^2(P)
\equiv p_2(P) mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_{2k}^2(P)\equiv p_k(P) mod 2$ for $2k\leq n$.)
\end{proposition}

([Gompf & Stipsicz 99, Ex. 1.4.21 d](#GompfStipsicz99), [Hatcher 17, Prop. 3.15 a](#Hatcher17))

\begin{proposition}
A principal SO(4)-bundle $P$ fulfills:
$$
p_2(P)
=e^2(P).
$$
(In general, a principal $SO(2n)$-bundle $P$ fulfills $p_n(P)=e^2(P)$.)
\end{proposition}

([Hatcher 17, Prop. 3.15 b](#Hatcher17))

The two previous propositions together imply $w_4^2(P)\equiv e^2(P) mod 2$ and one even has:

\begin{proposition}
A principal SO(4)-bundle $P$ fulfills:
$$
w_4(P)
\equiv e(P) mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_n(P)\equiv e(P) mod 2$.)
\end{proposition}

([Hatcher 17, Prop. 3.13 c](#Hatcher17))

## Classification over 4-manifolds by characteristic classes

\begin{proposition}
Let $X$ be a [[4-manifold]]. Two principal SO(4)-bundles $P,Q\twoheadrightarrow X$ are isomorphic if and only if their second [[Stiefel-Whitney class]], first [[Pontrjagin class]] and [[Euler class]] are all equal:
$$
w_2(P)
=w_2(Q)
\in H^2(X,\mathbb{Z}_2);
$$
$$
p_1(P)
=p_1(Q)
\in H^4(X,\mathbb{Z});
$$
$$
e(P)
=e(Q)
\in H^4(X,\mathbb{Z}).
$$
(But the classes are not independent from each other according to a previous proposition.)
\end{proposition}

([Dold & Whitney 59, Thrm. 1 a](#DoldWhitney59), [Gompf & Stipsicz 99, Thrm. 1.4.20](#GompfStipsicz99))

Certain [[4-manifolds]] yield simplifcations when the [[singular cohomology]] [[groups]] vanish. For example, for principal SO(4)-bundles over the [[4-sphere]], used in [[John Milnor]]'s construction of [[exotic 7-spheres]], the second [[singular cohomology]] vanishes and therefore the condition of equal second [[Stiefel-Whitney classes]] becomes trivial. In this case one has a [[group]] [[isomorphism]]:
$$
\left(e,-\frac{1}{4}(p_1+2e)\right)\colon
\pi_4 B SO(4)
\cong\pi_3 SO(4)
\xrightarrow\cong\mathbb{Z}\oplus\mathbb{Z}.
$$

([Bais 24, Eq. 1](#Bais24)) 

An abstract way to obtain this [[group]] [[isomorphism]] is the [[exceptional isomorphism]] $Spin(4)\cong SU(2)\times SU(2)\cong S^3\times S^3$, which double covers $SO(4)$ and therefore has the same higher [[homotopy groups]] (beyond the [[fundamental group]]). Therefore $\pi_3 SO(4)\cong\pi_3(S^3\times S^3)\cong\mathbb{Z}\oplus\mathbb{Z}$. (Just the result is also stated in [Dold & Whitney 59, Eq. (2)](#DoldWhitney59).)

\begin{theorem}
(**Dold-Whitney theorem**)
A closed [[orientable]] [[4-manifold]] $X$ is [[parallelizable]] if and only if its its second [[Stiefel-Whitney class]] $w_2(X)\in H^2(X,\mathbb{Z})$, first [[Pontrjagin class]] $p_1(X)\in H^4(X,\mathbb{Z})$ and [[Euler class]] $e(X)\in H^4(X,\mathbb{Z})$ all vanish.
\end{theorem}

([Bais 24, Thrm. 1](#Bais24))

All three conditions can be interpreted geometrically. Let therefore $[X]\in H_4(X,\mathbb{Z})\cong\mathbb{Z}$ be the [[fundamental class]] induced by the orientation with the [[Kronecker pairing]] $\langle-,[X]\rangle\colon H^4(X,\mathbb{Z})\xrightarrow\cong\mathbb{Z}$ being a [[group]] [[isomorphism]].

* $w_2(X)=0$ is equivalent to $X$ being a [[spin manifold]]. ([Gompf & Stipsicz 99, Prop. 1.4.25](#GompfStipsicz99))

* $p_1(X)=0$ is equivalent to a vanishing [[signature]] $\sigma(X)=0$ using [[Hirzebruch's signature theorem]] ([Gompf & Stipsicz 99, Thrm. 1.4.12](#GompfStipsicz99)): 
$$
  \sigma(X)
    \;=\;
  \frac{1}{3}\big\langle p_1(X), [X] \big\rangle
  \mathrlap{\,.}
$$
Since the signature is a [[group]] [[isomorphism]] $\sigma\colon\Omega_4^SO\xrightarrow\cong\mathbb{Z}$, having $\sigma(X)=0$ is equivalent to the $X$ being the boundary of an [[orientable]] [[5-manifold]].

* $e(X)=0$ is equivalent to a vanishing [[Euler characteristic]] $\chi(X)=0$ using:
$$
  \chi(X)
    \;=\;
  \big\langle e(X), [X] \big\rangle
  \mathrlap{\,.}
$$
Equivalently, $X$ has a nowhere vanishing vector field.

## Liftings

\begin{proposition}
A principal SO(4)-bundle $f\colon X\rightarrow B SO(4)$ lifts to a pair of [[principal SU(2)-bundles]] $\widehat{f}_1,\widehat{f}_2\colon X\rightarrow B SU(2)$ if and only if its second [[Stiefel-Whitney class]] vanishes, hence the composition $w_2\circ f\colon X\rightarrow K(\mathbb{Z}_2,2)$ is [[nullhomotopic]].
\end{proposition}

## Examples

* One has $S^n\cong SO(n+1)/SO(n)$, hence there is a principal SO(4)-bundle $SO(5)\twoheadrightarrow S^4$. Such [[principal bundles]] are classified by:
$$
\pi_4B SO(4)
\cong\pi_3 SO(4)
\cong\mathbb{Z}^2.
$$

## Related concepts

Particular [[principal bundles]]:

* [[double cover]] (principal O(1)-bundle)
* [[principal O(2)-bundle]]
* [[principal U(1)-bundle]] (principal SO(2)-bundle)
* [[principal U(2)-bundle]] (principal $Spin^\mathrm{c}(3)$-bundle, principal $Spin^\mathrm{h}(2)$-bundle)
* [[principal U(3)-bundle]]
* [[principal SO(3)-bundle]]
* **principal SO(4)-bundle**
* [[principal SO(5)-bundle]]
* [[principal SO(6)-bundle]]
* [[principal SO(7)-bundle]]
* [[principal SO(8)-bundle]]
* [[principal SU(2)-bundle]] (principal Sp(1)-bundle, principal Spin(3)-bundle)
* [[principal SU(3)-bundle]]
* [[principal SU(4)-bundle]] (principal Spin(6)-bundle)
* [[principal Sp(2)-bundle]] (principal Spin(5)-bundle)

## References

* {#DoldWhitney59} [[Albrecht Dold]] and [[Hassler Whitney]], _Classification of oriented sphere bundles over a 4-complex_ (1959), Annals of Mathematics Vol. 69 No. 3 &lbrack;[doi:10.2307/1970030](https://doi.org/10.2307/1970030) &rbrack;

* {#GompfStipsicz99} [[Robert Gompf]] and [[András Stipsicz]], _4-Manifolds and Kirby Calculus_ (1999), Graduate Studies 
in Mathematics, Volume 20 &lbrack;[ISBN: 978-0-8218-0994-5](https://www.ams.org/books/gsm/020), [doi:10.1090/gsm/020](https://www.ams.org/books/gsm/020)&rbrack;

* {#Hatcher17} [[Allen Hatcher]]: _Vector bundles and K-Theory_, book draft (2017) &lbrack;[webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf)&rbrack;

* {#Bais24} Valentina Bais, _On Dold-Whitney's parallelizability of 4-manifolds_ (2024) &lbrack;[arxiv:2410.22117](https://arxiv.org/abs/2410.22117) &rbrack;

[[!redirects principal SO(4)-bundles]]
[[!redirects SO(4)-principal bundle]]
[[!redirects SO(4)-principal bundles]]