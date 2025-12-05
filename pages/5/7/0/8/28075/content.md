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

*Principal SU(3)-bundles* are special [[principal bundles]] with the third [[special unitary group]] [[SU(3)]] as [[structure group]] ([[gauge group]]).

## Characteristic classes

\begin{proposition}
A principal U(3)-bundle $P$ fulfills:
$$
e(P)
\equiv c_3(P).
$$
(In general, a principal $U(n)$-bundle $P$ fulfills $e(P)=c_n(P)$.)
\end{proposition}

([Hatcher 17, Prop. 3.13 c](#Hatcher17))

## Associated vector bundle

For principal $U(3)$-bundles $P\twoheadrightarrow X$, there is an [[associated bundle|associated]] complex plane bundle $E=P\times_{U(3)}\mathbb{C}^3\twoheadrightarrow X$ using the [[balanced product]]. If $Q$ is the induced [[principal SU(4)-bundle]] (using the canonical inclusion $U(3)\hookrightarrow SU(4),U\mapsto diag(U,det(U)^{-1})$), then its [[adjoint bundle]] is given by:
$$
Ad(P)
\cong Ad(Q)\oplus(det(E)\otimes E)_\mathbb{R}.
$$
If $P$ reduces to a [[principal SU(3)-bundle]], this reduces to:
$$
Ad(P)
\cong Ad(Q)\oplus E_\mathbb{R}\oplus\underline{\mathbb{R}}.
$$
Both relations hold in general for the maps $SU(n)\hookrightarrow U(n)\rightarrow SU(n+1)$.

([Donaldson & Kronheimer 91, p. 205](#donaldsonkronheimer91))

## Examples

* One has $S^{2n+1}\cong U(n+1)/U(n)$, hence there is a principal U(3)-bundle $U(4)\twoheadrightarrow S^7$. Such [[principal bundles]] are classified by:
$$
\pi_7B U(3)
\cong\pi_6 U(3)
\cong\mathbb{Z}_6.
$$

## Related concepts

Particular [[principal bundles]]:

* [[double cover]] (principal O(1)-bundle)
* [[principal O(2)-bundle]]
* [[principal U(1)-bundle]] (principal SO(2)-bundle)
* [[principal U(2)-bundle]] (principal $Spin^\mathrm{c}(3)$-bundle, principal $Spin^\mathrm{h}(2)$-bundle)
* **principal U(3)-bundle**
* [[principal SO(3)-bundle]]
* [[principal SO(4)-bundle]]
* [[principal SO(5)-bundle]]
* [[principal SO(6)-bundle]]
* [[principal SO(7)-bundle]]
* [[principal SO(8)-bundle]]
* [[principal SU(2)-bundle]] (principal Sp(1)-bundle, principal Spin(3)-bundle)
* [[principal SU(3)-bundle]]
* [[principal SU(4)-bundle]] (principal Spin(6)-bundle)
* [[principal Sp(2)-bundle]] (principal Spin(5)-bundle)

## References

* {#DonaldsonKronheimer97} [[Simon Donaldson]], [[Peter Kronheimer]]: _The Geometry of Four-Manifolds_ (1990, revised 1997), Oxford University Press and Claredon Press, &lbrack;[oup:52942](https://academic.oup.com/book/52942), [doi:10.1093/oso/9780198535539.001.0001](https://doi.org/10.1093/oso/9780198535539.001.0001), ISBN:978-0198502692, ISSN:0964-9174&rbrack;

* {#Hatcher17} [[Allen Hatcher]]: _Vector bundles and K-Theory_, book draft (2017) &lbrack;[webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf)&rbrack;

[[!redirects principal U(3)-bundles]]
[[!redirects U(3)-principal bundle]]
[[!redirects U(3)-principal bundles]]