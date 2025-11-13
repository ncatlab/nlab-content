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

## Related concepts

* [[U(2)]] (Spinᶜ(3), Spinʰ(2))

* [[Spinᶜ(4)]]

[[!redirects Spinc(6)]]
[[!redirects Spin^c(6)]] 
[[!redirects Spinc6]]
[[!redirects Spin^c6]] 
[[!redirects Spinᶜ6]]