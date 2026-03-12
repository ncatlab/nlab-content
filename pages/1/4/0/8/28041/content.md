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

*Principal SU(3)-bundles* are special [[principal bundles]] with the third [[special unitary group]] [[SU(3)|$SU(3)$]] as [[structure group]]/[[gauge group]]. Applications include [[quantum chromodynamics]], in which $SU(3)$ arises as the gauge group from the three color charges.

Principal SU(3)-bundles induce [[principal SU(2)-bundles]] and are induced by [[principal SU(4)-bundles]] using the canonical inclusions $SU(2)\hookrightarrow SU(3)\hookrightarrow SU(4)$.

## Characteristic classes

\begin{proposition}
A principal SU(3)-bundle $P$ fulfills:
$$
e(P)
\equiv c_3(P).
$$
(In general, a principal $SU(n)$-bundle $P$ fulfills $e(P)=c_n(P)$.)
\end{proposition}

([Hatcher 17, Prop. 3.13 c](#Hatcher17))

## Adjoint vector bundle

\begin{proposition}
For a principal $SU(3)$-bundle, the first [[Pontrjagin class]] of its [[adjoint bundle]] is given by:
$$
p_1Ad(P)
=-6c_2(P).
$$
\end{proposition}

(This relation holds in general for principal $SU(n)$-bundles with $p_1 Ad(P)=-2nc_2(P)$.)

## Examples

* One has $S^{2n+1}\cong SU(n+1)/SU(n)$, hence there is a principal SU(3)-bundle $SU(4)\twoheadrightarrow S^7$. Such [[principal bundles]] are classified by:
$$
\pi_7B SU(3)
\cong\pi_6 SU(3)
\cong\mathbb{Z}_6.
$$
([Mimura & Toda 63](#MimuraToda63))

* [[G₂/SU(3) is the 6-sphere]], hence there is a principal SU(3)-bundle $G_2\twoheadrightarrow S^6$. Such principal bundles are classified by:
$$
\pi_6B SU(3)
\cong\pi_5 SU(3)
\cong\mathbb{Z}.
$$
([Mimura & Toda 63](#MimuraToda63))

## Related concepts

[[!include particular principal bundles -- table]]

## References

* {#MimuraToda63} [[Mamoru Mimura]] and [[Hiroshi Toda]], _Homotopy Groups of SU(3), SU(4) and Sp(2)_ (1963), Journal of Mathematics of Kyoto University. **3** (2), p. 217–250, [doi:10.1215/kjm/1250524818](https://projecteuclid.org/journals/kyoto-journal-of-mathematics/volume-3/issue-2/Homotopy-Groups-of-SU3-SU4-and-Sp2/10.1215/kjm/1250524818.full)

* {#DonaldsonKronheimer97} [[Simon Donaldson]], [[Peter Kronheimer]]: _The Geometry of Four-Manifolds_ (1990, revised 1997), Oxford University Press and Claredon Press, &lbrack;[oup:52942](https://academic.oup.com/book/52942), [doi:10.1093/oso/9780198535539.001.0001](https://doi.org/10.1093/oso/9780198535539.001.0001), ISBN:978-0198502692, ISSN:0964-9174&rbrack;

* {#Hatcher17} [[Allen Hatcher]]: _Vector bundles and K-Theory_, book draft (2017) &lbrack;[webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf)&rbrack;

[[!redirects principal SU(3)-bundles]]
[[!redirects SU(3)-principal bundle]]
[[!redirects SU(3)-principal bundles]]