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

*Principal SO(8)-bundles* are special [[principal bundles]] with the eighth [[special orthogonal group]] [[SO(8)]] as [[structure group]] ([[gauge group]]).

## Characteristic classes

\begin{proposition}
A principal SO(8)-bundle $P$ fulfills:
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
\equiv p_3(P) \mod 2;
$$
$$
w_8^2(P)
\equiv p_4(P) \mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_{2k}^2(P)\equiv p_k(P) mod 2$ for $2k\leq n$.)
\end{proposition}

([Milnor & Stasheff 74, Prob. 15-A](#MilnorStasheff74), [Gompf & Stipsicz 99, Ex. 1.4.21 d](#GompfStipsicz99), [Hatcher 17, Prop. 3.15 a](#Hatcher17))

Let $X$ be an [[orientable]] [[8-manifold]] (with [[fundamental class]] $[X]\in H^8(X,\mathbb{Z})\cong\mathbb{Z}$) and $P=Fr_{SO}TX$ be the [[frame bundle]] of its [[tangent bundle]] (which doesn't change [[characteristic classes]]). Using [[Hirzebruch's signature theorem]] connects one of its [[Stiefel-Whitney numbers]] with its [[signature genus|signature]]:
$$
w_4^2[X]-w_2^4[X]
=(p_2-p_1^2)[X] mod 2
=\sigma(X) mod 2
$$

\begin{proposition}
A principal SO(8)-bundle $P$ fulfills:
$$
p_4(P)
=e^2(P).
$$
(In general, a principal $SO(2n)$-bundle $P$ fulfills $p_n(P)=e^2(P)$.)
\end{proposition}

([Milnor & Stasheff 74, Crl. 15.8](#MilnorStasheff74), [Hatcher 17, Prop. 3.15 b](#Hatcher17))

The two previous propositions together imply $w_8^2(P)\equiv e^2(P) mod 2$ and one even has:

\begin{proposition}
A principal SO(8)-bundle $P$ fulfills:
$$
w_8(P)
\equiv e(P) mod 2.
$$
(In general, a principal $SO(n)$-bundle $P$ fulfills $w_n(P)\equiv e(P) mod 2$.)
\end{proposition}

([Milnor & Stasheff 74, Prop. 9.5](#MilnorStasheff74), [Hatcher 17, Prop. 3.13 c](#Hatcher17))

## Examples

* One has $S^n\cong SO(n+1)/SO(n)$, hence there is a principal SO(8)-bundle $SO(9)\twoheadrightarrow S^8$. Such [[principal bundles]] are classified by:
$$
\pi_8B SO(8)
\cong\pi_7 SO(8)
\cong\mathbb{Z}^2.
$$

## Related concepts

[[!include particular principal bundles -- table]]

## References

* {#MilnorStasheff74} [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

* {#GompfStipsicz99} [[Robert Gompf]] and [[András Stipsicz]], _4-Manifolds and Kirby Calculus_ (1999), Graduate Studies 
in Mathematics, Volume 20 &lbrack;[ISBN: 978-0-8218-0994-5](https://www.ams.org/books/gsm/020), [doi:10.1090/gsm/020](https://www.ams.org/books/gsm/020)&rbrack;

* {#Hatcher17} [[Allen Hatcher]]: _Vector bundles and K-Theory_, book draft (2017) &lbrack;[webpage](https://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html), [pdf](https://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf)&rbrack;

[[!redirects principal SO(8)-bundles]]
[[!redirects SO(8)-principal bundle]]
[[!redirects SO(8)-principal bundles]]