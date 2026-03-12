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

\tableofcontents

## Idea

*Principal SO(5)-bundles* are special [[principal bundles]] with the fifth [[special orthogonal group]] [[SO(5)]] as [[structure group]] ([[gauge group]]).

## Characteristic classes

\begin{proposition}
A principal SO(5)-bundle $P$ fulfills:
$$
w_2^2(P)
\equiv p_1(P) \mod 2;
$$
$$
w_4^2(P)
\equiv p_2(P) \mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_{2k}^2(P)\equiv p_k(P) \mod 2$ for $2k\leq n$.)
\end{proposition}

([Milnor & Stasheff 74, Prob. 15-A](#MilnorStasheff74), [Gompf & Stipsicz 99, Ex. 1.4.21 d](#GompfStipsicz99), [Hatcher 17, Prop. 3.15 a](#Hatcher17))

\begin{proposition}
A principal SO(5)-bundle $P$ fulfills:
$$
w_5(P)
\equiv e(P) \mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_n(P)\equiv e(P) \mod 2$.)
\end{proposition}

([Milnor & Stasheff 74, Prop. 9.5](#MilnorStasheff74), [Hatcher 17, Prop. 3.13 c](#Hatcher17))

\begin{proposition}
A principal SO(5)-bundle $P$ fulfills:
$$
e(P)
=W_5(P)
=\beta w_4(P).
$$
with the fifth [[integral Stiefel-Whitney class]] and the [[Bockstein homomorphism]] $\beta\colon H^4(M,\mathbb{Z}_2)\rightarrow H^5(M,\mathbb{Z})$ of the [[short exact sequence]] $0\rightarrow\mathbb{Z}\hookrightarrow\mathbb{Z}\twoheadrightarrow\mathbb{Z}_2\rightarrow 0$. (In general, a principal $SO(2n+1)$-bundle $P$ fulfills $e(P)=W_{2n+1}(P)=\beta w_{2n}(P)$.)
\end{proposition}

([Milnor & Stasheff 74, Prob. 15-D](#MilnorStasheff74), [Hatcher 17, Ch. 3, Ex. 3](#Hatcher17))

## Liftings

\begin{proposition}
A principal SO(5)-bundle $f\colon X\rightarrow B SO(5)$ lifts to a [[principal Sp(2)-bundle]] $\widehat{f}\colon X\rightarrow B Sp(2)$ if and only if its second [[Stiefel-Whitney class]] vanishes, hence the composition $w_2\circ f\colon X\rightarrow K(\mathbb{Z}_2,2)$ is [[nullhomotopic]].
\end{proposition}

## Examples

* One has $S^n\cong SO(n+1)/SO(n)$, hence there is a principal SO(5)-bundle $SO(6)\twoheadrightarrow S^5$. Such [[principal bundles]] are classified by:
$$
\pi_5B SO(5)
\cong\pi_4 SO(5)
\cong\mathbb{Z}_2^2.
$$

## Related concepts

[[!include particular principal bundles -- table]]

## References

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

* {#GompfStipsicz99} [[Robert Gompf]] and [[András Stipsicz]], _4-Manifolds and Kirby Calculus_ (1999), Graduate Studies 
in Mathematics, Volume 20 &lbrack;[ISBN: 978-0-8218-0994-5](https://www.ams.org/books/gsm/020), [doi:10.1090/gsm/020](https://www.ams.org/books/gsm/020)&rbrack;

* {#Hatcher17} [[Allen Hatcher]]: _Vector bundles and K-Theory_, book draft (2017) &lbrack;[webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf)&rbrack;

[[!redirects principal SO(5)-bundles]]
[[!redirects SO(5)-principal bundle]]
[[!redirects SO(5)-principal bundles]]