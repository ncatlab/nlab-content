+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

$Spin^\mathrm{c}(6)$ is the fourth [[spinᶜ group]]. It is used to describe [[spinᶜ structures]] on [[orientable]] 6-manifolds.

## Properties

\begin{proposition}
One has a canonical [[double cover]] of the [[unitary group]] in dimension 4:
$$
  Spin^\mathrm{c}(6)
    \twoheadrightarrow 
  U(4).
$$
\end{proposition}

\begin{proof}
Using the [[exceptional isomorphism]] $Spin(6)\cong SU(4)$ yields:
$$
Spin^\mathrm{c}(6)
\cong(Spin(6)\times U(1))/\mathbb{Z}_2
=(SU(4)\times U(1))/\mathbb{Z}_2
\twoheadrightarrow(SU(4)\times U(1))/\mathbb{Z}_4
\cong U(4).
$$
(In general, one has $(SU(n)\times U(1))/\mathbb{Z}_n\cong U(n)$ using the [[homomorphism theorem]] on the [[group homomorphism]] $SU(n)\times U(1)\rightarrow U(n),(U,z)\mapsto Uz$, which is surjective and has $\{(\zeta_n^k\mathbf{1}_n,\zeta_n^{-k})|[k]\in\mathbb{Z}_n \}\cong\mathbb{Z}_n$ as [[kernel]].)
\end{proof}
A [[double cover]] is the same as an [[principal bundle|principal O(1)-bundle]] and corresponds uniquely to a real [[line bundle]] $Spin^\mathrm{c}(6)\times_{O(1)}\mathbb{R}\twohearightarrow U(4)$ with the [[balanced product]]. Both are classified uniquely by the first [[Stiefel-Whitney class]] $w_1(Spin^\mathrm{c}(6))\in H^1(U(4),\mathbb{Z}_2)$, as it is a [[group isomorphism]] over [[CW complexes]] like $U(4)$. Using the [[universal coefficient theorem]] and the [[Hurewicz theorem]] yields:
$$
H^1(U(4),\mathbb{Z}_2)
\cong Hom(H_1(U(4),\mathbb{Z}),\mathbb{Z}_2)
\cong Hom(\pi_1^\mathrm{ab}(U(4)),\mathbb{Z}_2)
\cong Hom(\mathbb{Z},\mathbb{Z}_2)
\cong\mathbb{Z}_2.
$$
($\pi_1^\mathrm{ab}(U(4))\cong\mathbb{Z}$ follows from the [[determinant]] $det\colon U(4)\rightarrow U(1)$ inducing a [[group isomorphism]] on the [[fundamental group]].) Now there are two possibilities for the above first [[Stiefel-Whitney class]], which are the trivial and the unique non-trivial one. Since the former would lead to the [[Lie group isomorphism]] $Spin^\mathrm{c}(6)\cong U(4)\times O(1)$ between a [[connected]] and not [[connected]] space, it has to be the latter. Its [[classifying map]] can also be stated easily:
$$
i\circ det\colon
U(4)\twoheadrightarrow U(1)\cong S^1\cong\mathbb{R}P^1\hookrightarrow\mathbb{R}P^\infty\cong BO(1)
$$
The first [[pullback]] along the canonical inclusion $i\colon S^1\hookrightarrow BO(1)$ is the real [[Hopf fibration]] $i^*S^\infty\cong i^*EO(1)\cong S^1\twoheadrightarrow S^1$ with unique non-trivial first [[Stiefel-Whitney class]] $w_1(S^1)\in H^1(S^1,\mathbb{Z}_2)\cong\mathbb{Z}_2$. (Or better denoted as that of the [[tautological line bundle]] $\gamma_{\mathbb{R}}^{1,1}=S^1\times_{O(1)}\mathbb{R}$, since the identically denoted first [[Stiefel-Whitney class]] of the [[tangent bundle]] is trivial.) The second [[pullback]] along the [[determinant]] (which is not the [[determinant line bundle]]) preserves this. Now there is an alternative description:
$$
Spin^\mathrm{c}(6)
\cong\{(U,z)\in U(4)\times U(1)|det(U)=z^2\}.
$$
and the [[double cover]] can be easily spotted in the missing sign of the complex number.

## Related concepts

* [[U(2)]] (Spinᶜ(3), Spinʰ(2))

* [[Spinᶜ(4)]]

[[!redirects Spinc(6)]]
[[!redirects Spin^c(6)]] 
[[!redirects Spinc6]]
[[!redirects Spin^c6]] 
[[!redirects Spinᶜ6]]