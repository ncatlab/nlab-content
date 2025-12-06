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

*Principal SO(6)-bundles* are special [[principal bundles]] with the sixth [[special orthogonal group]] [[SO(6)|$SO(6)$]] as [[structure group]]/[[gauge group]]. Applications include the [[frame bundle]] of an [[orientable]] 6-manifold.

Principal SO(6)-bundles in particular are induced by [[principal SU(4)-bundles]] using the canonical projection $SU(4)\cong Spin(6)\hookrightarrow SO(6)$. Principal SO(6)-bundles also induce [[principal SO(2)-bundles]], [[principal SO(3)-bundles]] and principal SO(6)-bundles using the canonical inclusions $SO(2)\hookrightarrow SO(3)\hookrightarrow SO(4)\hookrightarrow SO(6)$.

Principal SO(6)-bundles also arise from any principal $G$-bundle with a six-dimensional [[Lie group]] $G$ using its [[adjoint representation]] $Ad\colon G\rightarrow SL_6(\mathbb{R})$, which induces a map $\mathcal{B}Ad\colon\mathcal{B}G\rightarrow B SO(6)$.

## Characteristic classes

\begin{proposition}
A principal SO(6)-bundle $P$ fulfills:
$$
w_2^2(P)
\equiv p_1(P) \mod 2;
$$
$$
w_4^2(P)
\equiv p_2(P) \mod 2;
$$
$$
w_6^2(P)
\equiv p_3(P) \mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_{2k}^2(P)\equiv p_k(P) \mod 2$ for $2k\leq n$.)
\end{proposition}

([Milnor & Stasheff 74, Prob. 15-A](#MilnorStasheff74), [Gompf & Stipsicz 99, Ex. 1.4.21 d](#GompfStipsicz99), [Hatcher 17, Prop. 3.15 a](#Hatcher17))

\begin{proposition}
A principal SO(6)-bundle $P$ fulfills:
$$
p_3(P)
=e^2(P).
$$
(In general, a principal $SO(2n)$-bundle $P$ fulfills $p_n(P)=e^2(P)$.)
\end{proposition}

([Milnor & Stasheff 74, Crl. 15.8](#MilnorStasheff74), [Hatcher 17, Prop. 3.15 b](#Hatcher17))

The two previous propositions together imply $w_6^2(P)\equiv e^2(P) \mod 2$ and one even has:

\begin{proposition}
A principal SO(6)-bundle $P$ fulfills:
$$
w_6(P)
\equiv e(P) \mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_n(P)\equiv e(P) \mod 2$.)
\end{proposition}

([Milnor & Stasheff 74, Prop. 9.5](#MilnorStasheff74), [Hatcher 17, Prop. 3.13 c](#Hatcher17))

## Liftings

\begin{proposition}
A principal SO(6)-bundle $f\colon X\rightarrow B SO(6)$ lifts to a [[principal SU(4)-bundle]] $\widehat{f}\colon X\rightarrow B SU(4)$ if and only if its second [[Stiefel-Whitney class]] vanishes, hence the composition $w_2\circ f\colon X\rightarrow K(\mathbb{Z}_2,2)$ is [[nullhomotopic]].
\end{proposition}

## Examples

* One has $S^n\cong SO(n+1)/SO(n)$, hence there is a principal SO(6)-bundle $SO(7)\twoheadrightarrow S^6$. Such [[principal bundles]] are classified by:
$$
\pi_6B SO(6)
\cong\pi_5 SO(6)
\cong\mathbb{Z}.
$$

## Related concepts

Particular [[principal bundles]]:

* [[double cover]] (principal O(1)-bundle)
* [[principal O(2)-bundle]]
* [[principal U(1)-bundle]] (principal SO(2)-bundle)
* [[principal U(2)-bundle]] (principal $Spin^\mathrm{c}(3)$-bundle, principal $Spin^\mathrm{h}(2)$-bundle)
* [[principal U(3)-bundle]]
* [[principal SO(3)-bundle]]
* [[principal SO(4)-bundle]]
* [[principal SO(5)-bundle]]
* **principal SO(6)-bundle**
* [[principal SO(7)-bundle]]
* [[principal SO(8)-bundle]]
* [[principal SU(2)-bundle]] (principal Sp(1)-bundle, principal Spin(3)-bundle)
* [[principal SU(3)-bundle]]
* [[principal SU(4)-bundle]] (principal Spin(6)-bundle)
* [[principal Sp(2)-bundle]] (principal Spin(5)-bundle)

## References

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

* {#GompfStipsicz99} [[Robert Gompf]] and [[András Stipsicz]], _4-Manifolds and Kirby Calculus_ (1999), Graduate Studies 
in Mathematics, Volume 20 &lbrack;[ISBN: 978-0-8218-0994-5](https://www.ams.org/books/gsm/020), [doi:10.1090/gsm/020](https://www.ams.org/books/gsm/020)&rbrack;

* {#Hatcher17} [[Allen Hatcher]]: _Vector bundles and K-Theory_, book draft (2017) &lbrack;[webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf)&rbrack;

[[!redirects principal SO(6)-bundles]]
[[!redirects SO(6)-principal bundle]]
[[!redirects SO(6)-principal bundles]]