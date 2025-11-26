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

*Principal SO(3)-bundles* are [[principal bundles]] with the third [[special orthogonal group]] [[SO(3)|$SO(3)$]] as [[structure group]]/[[gauge group]]. Applications include the [[frame bundle]] of an [[orientable]] [[3-manifold]] as well as the (anti) self-dual bundles $\Lambda_\pm^2T X$ for an [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]] $X$, resulting from the splitting $\mathfrak{so}(4)\cong\mathfrak{so}(3)\oplus\mathfrak{so}(3)$.

Principal $SO(3)$-bundles are in particular induced by [[principal SU(2)-bundles]] using the [[double cover]] $SU(2)\cong Spin(3)\twoheadrightarrow SO(3)$ and [[principal U(2)-bundles]] using the canonical projection $U(2)\cong Spin^\mathrm{c}(3)\cong Spin^\mathrm{h}(2)\rightarrow SO(3)$. In fact the latter example generalizes to every $Spin^\mathrm{h}(n)$-bundle using the [[double cover]] of the former example:
$$
Spin^\mathrm{h}(n)
\cong(Spin(n)\times SU(2))/\mathbb{Z}_2
\rightarrow SU(2)/\mathbb{Z}_2
\cong SO(3).
$$
Principal SO(3)-bundles also induce [[principal SO(2)-bundles]] and are induced by [[principal SO(4)-bundles]] and [[principal SO(6)-bundles]] using the canonical inclusions $SO(2)\hookrightarrow SO(3)\hookrightarrow SO(4)\hookrightarrow SO(6)$.

Principal SO(3)-bundles also arise from any principal $G$-bundle with a three-dimensional real [[Lie group]] $G$ using its [[adjoint representation]] $Ad\colon G\rightarrow SL_3(\mathbb{R})$, which induces a map $\mathcal{B}Ad\colon\mathcal{B}G\rightarrow B SO(3)$.

## Properties

\begin{proposition}
A principal SO(3)-bundle $P$ fulfills:
$$
w_2^2(P)
\equiv p_1(P) mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_{2k}^2(P)\equiv p_k(P) mod 2$ for $2k\leq n$.)
\end{proposition}

([Gompf & Stipsicz 99, Ex. 1.4.21 d](#GompfStipsicz99))

\begin{proposition}
Let $X$ be a [[4-manifold]]. Two principal SO(3)-bundles $P,Q\twoheadrightarrow X$ are isomorphic if and only if their second [[Stiefel-Whitney class]] and first [[Pontrjagin class]] are equal:
$$
w_2(P)
=w_2(Q)
\in H^2(X,\mathbb{Z}_2);
$$
$$
p_1(P)
=p_1(Q)
\in H^4(X,\mathbb{Z}).
$$
(But the classes are not independent from each other according to the previous proposition.)
\end{proposition}

([Dold & Whitney 59, Thrm. 1 a](#DoldWhitney59), [Gompf & Stipsicz 99, Thrm. 1.4.20](#GompfStipsicz99))

Certain [[4-manifolds]] yield simplifcations when the [[singular cohomology]] [[groups]] vanish. For example, for principal SO(3)-bundles over the [[4-sphere]] the second [[singular cohomology]] vanishes and therefore the condition of equal second [[Stiefel-Whitney classes]] becomes trivial. In this case one has a [[group]] [[isomorphism]]:
$$
p_1\colon
\pi_4 B SO(3)
\cong\pi_3 SO(3)
\xrightarrow\cong\mathbb{Z}.
$$
An abstract way to obtain this [[group]] [[isomorphism]] is the [[exceptional isomorphism]] $Spin(3)\cong SU(2)\cong S^3$, which double covers $SO(3)$ and therefore has the same higher [[homotopy groups]] (beyond the [[fundamental group]]). Therefore $\pi_3 SO(3)\cong\pi_3(S^3)\cong\mathbb{Z}$. (Just the result is also stated in [Dold & Whitney 59, Eq. (2)](#DoldWhitney59).)

\begin{proposition}
Let $X$ be a $4$-manifold. For every $(w_2,p_1)\in H^2(X,\mathbb{Z}_2)\times H^4(X,\mathbb{Z})$ with $p_1=Pont(w_2) mod 4$, there exists a principal SO(3)-bundle $P\twoheadrightarrow X$ with $w_2(P)=w_2$ and $p_1(P)=p_1$.
\end{proposition}

([Gompf & Stipsicz 99, Thrm. 1.4.20](#GompfStipsicz99))

## Liftings

\begin{proposition}
A principal SO(3)-bundle $f\colon X\rightarrow B SO(3)$ lifts to a [[principal SU(2)-bundle]] $\widehat{f}\colon X\rightarrow B SU(2)\cong\mathbb{H}P^\infty$ if and only if its second [[Stiefel-Whitney class]] vanishes, hence the composition $w_2\circ f\colon X\rightarrow K(\mathbb{Z}_2,2)$ is [[nullhomotopic]].
\end{proposition}

Let $P$ be a principal $SU(2)$-bundle and $Q$ be the associated principal $SO(3)$-bundle. One then has:
$$
p_1(Q)
=p_1 Ad(P)
=-4c_2(P);
$$
$$
w_2(Q)
=w_2Ad(P)
=0.
$$

([Uhlenbeck & Freed 91, Appendix E.6](#UhlenbeckFreed91))

\begin{proposition}
A principal SO(3)-bundle $f\colon X\rightarrow B SO(3)$ lifts to a [[principal U(2)-bundle]] $\widehat{f}\colon X\rightarrow B U(2)$ if and only if its third [[integral Stiefel-Whitney class]] vanishes, hence the composition $W_3\circ f\colon X\rightarrow K(\mathbb{Z},2)$ is [[nullhomotopic]]. If the second [[Stiefel-Whitney class]] $w_2\circ f\colon X\rightarrow K(\mathbb{Z}_2,2)$ lifts to an integral class $c\colon X\rightarrow K(\mathbb{Z},2)$, then it is exactly the first [[Chern class]] of the lift with $c_1\circ\widehat{f}=c$.
\end{proposition}

([Donaldson & Kronheimer 91, p. 42](#donaldsonkronheimer91))

In the situation of this lemma, it is often more useful to consider the [[exceptional isomorphism]] $SO(3)\cong PU(2)$ to the [[projective unitary group]].

## (Anti) self-dual bundles

Using the [[exceptional isomorphisms]] $Spin(3)\cong SU(2)$ and $Spin(4)\cong SU(2)\times SU(2)$, matrices in [[SO(3)]] and [[SO(4)]] can be represented by matrices in [[SU(2)]]. In particular there are maps:
$$
\phi\colon
SO(3)\rightarrow SO(4)
[U]\mapsto[(U,U)];
$$
$$
\psi_-\colon
SO(4)\rightarrow SO(3),
[(U_-,U_+)]\mapsto[U_-];
$$
$$
\psi_+\colon
SO(4)\rightarrow SO(3),
[(U_-,U_+)]\mapsto[U_+]
$$
with $\psi_\pm\circ\phi=id$ and so that there is a [[Lie algebra]] [[isomorphism]]:
$$
(\psi_-',\psi_+')\colon
\mathfrak{so}(4)\xrightarrow\cong\mathfrak{so}(3)\oplus\mathfrak{so}(3)
$$
\begin{proposition}
For an [[orientable]] [[Riemannian manifold|Riemannian]] [[4-manifold]] $X$, one has $\Lambda_\pm^2T X=(\psi_\pm)_*T X$ with characteristic classes:
$$
w_2(\Lambda_+^2T X)
=w_2(X);
$$
$$
p_1(\Lambda_+^2T X)
=p_1(X)
+2e(X).
$$
\end{proposition}

([Gompf & Stipsicz 99, Thrm. 1.4.20](#GompfStipsicz99))

According to the first equation, $\Lambda_+^2T X$ lifts to a [[principal SU(2)-bundle]] if and only if $T X$ lifts to a pair of [[principal SU(2)-bundles]] (being $Spin(3)$ and $Spin(4)$ structures repsectively). Or just taking the weaker implied equality of the third [[integral Stiefel-Whitney classes]], $\Lambda_+^2T X$ lifts to a [[principal U(2)-bundle]] if and only if $T X$ lifts to a pair of [[principal U(2)-bundles]] with same first [[Chern class]] (being $Spin^\mathrm{c}(3)$ and $Spin^\mathrm{c}(4)$ structures respectively).

According to the second equation, using the [[fundamental class]] $[X]\in H_4(X,\mathbb{Z})\cong\mathbb{Z}$ induced by the orientation as well as [[Hirzebruch's signature theorem]], one has:
$$
\big\langle p_1(\Lambda_+^2T X),[X]\big\rangle
=\big\langle p_1(X),[X]\big\rangle
+2\big\langle e(X),[X]\big\rangle
=3\sigma(X)
+2\chi(X)
$$
This expression appears both in the virtual dimension of the [[Seiberg-Witten moduli space]] ([Gompf & Stipsicz 99, Thrm. 2.4.24](#GompfStipsicz99)) and Noether's formula for [[almost complex structures]]. ([Gompf & Stipsicz 99, Thrm. 1.4.15](#GompfStipsicz99))

## Examples

* One has $S^n\cong SO(n+1)/SO(n)$, hence there is a principal SO(3)-bundle $SO(4)\twoheadrightarrow S^3$. Such [[principal bundles]] are classified by:
$$
\pi_3B SO(3)
\cong\pi_2 SO(3)
\cong 1.
$$

## Related concepts

Particular [[principal bundles]]:

* [[double cover]] (principal O(1)-bundle)
* [[principal O(2)-bundle]]
* [[principal U(1)-bundle]] (principal SO(2)-bundle)
* [[principal U(2)-bundle]] (principal $Spin^\mathrm{c}(3)$-bundle, principal $Spin^\mathrm{h}(2)$-bundle)
* [[principal U(3)-bundle]]
* **principal SO(3)-bundle**
* [[principal SO(4)-bundle]]
* [[principal SO(5)-bundle]]
* [[principal SO(6)-bundle]]
* [[principal SO(7)-bundle]]
* [[principal SO(8)-bundle]]
* [[principal SU(2)-bundle]] (principal Sp(1)-bundle, principal Spin(3)-bundle)
* [[principal SU(3)-bundle]]
* [[principal SU(4)-bundle]] (principal Spin(6)-bundle)
* [[principal Sp(2)-bundle]]

## References

* {#DoldWhitney59} [[Albrecht Dold]] and [[Hassler Whitney]], _Classification of oriented sphere bundles over a 4-complex_ (1959), Annals of Mathematics Vol. 69 No. 3 &lbrack;[doi:10.2307/1970030](https://doi.org/10.2307/1970030) &rbrack; 

* {#HirzebruchHopf58} [[Friedrich Hirzebruch]], [[Heinz Hopf]], _Felder von Flächenelementen in 4-dimensionalen Mannigfaltigkeiten_ (1958)
* {#DoldWhitney59} [[Albrecht Dold]] and [[Hassler Whitney]], _Classification of oriented sphere bundles over a 4-complex_ (1959)

* {#UhlenbeckFreed91} [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8]
(https://link.springer.com/book/10.1007/978-1-4613-9703-8))

* {#DonaldsonKronheimer97} [[Simon Donaldson]], [[Peter Kronheimer]]: _The Geometry of Four-Manifolds_ (1990, revised 1997), Oxford University Press and Claredon Press, &lbrack;[oup:52942](https://academic.oup.com/book/52942), [doi:10.1093/oso/9780198535539.001.0001](https://doi.org/10.1093/oso/9780198535539.001.0001), ISBN:978-0198502692, ISSN:0964-9174&rbrack;

* {#GompfStipsicz99} [[Robert Gompf]] and [[András Stipsicz]], _4-Manifolds and Kirby Calculus_ (1999), Graduate Studies 
in Mathematics, Volume 20 &lbrack;[ISBN: 978-0-8218-0994-5](https://www.ams.org/books/gsm/020), [doi:10.1090/gsm/020](https://www.ams.org/books/gsm/020)&rbrack;

* {#Lobb17} [[Andrew Lobb]], _The Dold-Whitney theorem and the Sato-Levine invariant_ (2017), &lbrack;[arxiv:1709.09922](https://arxiv.org/abs/1709.09922) [pdf](https://maths.dur.ac.uk/users/andrew.lobb/mod4slicing.pdf)&rbrack;
 
[[!redirects principal SO(3)-bundles]]
[[!redirects SO(3)-principal bundle]]
[[!redirects SO(3)-principal bundles]]