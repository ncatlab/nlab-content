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

$Spin^\mathrm{c}(4)$ is the fourth [[spinᶜ group]]. It is used to describe [[spinᶜ structures]] on [[orientable]] [[4-manifolds]], which are studied in [[Seiberg-Witten theory]].

## Properties

\begin{proposition}
One has an [[exceptional isomorphism]]:
$$
Spin^\mathrm{c}(4)
\cong U(2)\times_{U(1)}U(2)
=\{(U_-,U_+)\in U(2)\times U(2)|det(U_-)=det(U_+)\}.
$$
\end{proposition}

\begin{proof}
Using the [[exceptional isomorphism]] $Spin(4)\cong SU(2)\times SU(2)$ yields:
$$
Spin^\mathrm{c}(6)
\cong(SU(2)\times SU(2)\times U(1))/\mathbb{Z}_2
\twoheadrightarrow U(2)\times_{U(1)}U(2),
(U_-,U_+,z)\mapsto(U_-z,U_+z)
$$
(In general, one has $(SU(n)\times U(1))/\mathbb{Z}_n\cong U(n)$ using the [[homomorphism theorem]] on the [[group homomorphism]] $SU(n)\times U(1)\rightarrow U(n),(U,z)\mapsto Uz$, which is surjective and has $\{(\zeta_n^k\mathbf{1}_n,\zeta_n^{-k})|[k]\in\mathbb{Z}_n \}\cong\mathbb{Z}_n$ as [[kernel]].)
\end{proof}

## Related concepts

* [[U(2)]] (Spinᶜ(3), Spinh(2))
* [[Spinᶜ(6)]]

## References

* {#Nicolaescu00} [[Liviu Nicolaescu]], *Notes on Seiberg-Witten theory*, American Mathematical Society (2000) &lbrack;[ISBN:978-0-8218-2145-9](https://bookstore.ams.org/GSM/28), [pdf](https://www3.nd.edu/~lnicolae/new1.pdf)&rbrack; 

[[!redirects Spinᶜ(4)]]
[[!redirects Spin^c(4)]]
[[!redirects Spinc4]]
[[!redirects Spin^c4]]
[[!redirects Spinᶜ4]]