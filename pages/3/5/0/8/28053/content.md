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

$U(2)$ is the [[unitary group]] in dimension 2. It is used to describe [[almost complex structures]] on [[4-manifolds]].

## Properties

\begin{proposition}
One has [[exceptional isomorphisms]] between $U(2)$ and the [[spinᶜ group]] in dimension 3 as well as the [[spinʰ group]] in dimension 2:
$$
  U(2)
    \cong 
  Spin^\mathrm{c}(3)
   \cong 
  Spin^\mathrm{h}(2).
$$
\end{proposition}

([Gompf & Stipsicz 99, Ex. 2.4.14](#gompfstipsicz99), [Nicolaescu 00, Ex. 1.3.9](#nicolaescu00))

\begin{proof}
Using the [[exceptional isomorphism]] $Spin(3)\cong SU(2)$ yields:
$$
Spin^\mathrm{c}(3)
\cong(Spin(3)\times U(1))/\mathbb{Z}_2
=(SU(2)\times U(1))/\mathbb{Z}_2
\cong U(2)
$$
Using the [[exceptional isomorphism]] $Spin(2)\cong U(1)$ as well as $Sp(1)\cong SU(2)$ yields:
$$
Spin^\mathrm{h}(2)
\cong(Spin(2)\times Sp(1))/\mathbb{Z}_2
=(SU(2)\times U(1))/\mathbb{Z}_2
\cong U(2)
$$
(In general, one has $(SU(n)\times U(1))/\mathbb{Z}_n\cong U(n)$ using the [[homomorphism theorem]] on the [[group homomorphism]] $SU(n)\times U(1)\rightarrow U(n),(U,z)\mapsto U \cdot z$, which is surjective and has $\{(\zeta_n^k\mathbf{1}_n,\zeta_n^{-k})|[k]\in\mathbb{Z}_n \}\cong\mathbb{Z}_n$ as [[kernel]].)
\end{proof}

## Related concepts

* [[Spinᶜ(4)]]

* [[Spinᶜ(6)]]

## References

* {#GompfStipsicz99} [[Robert Gompf]] and [[András Stipsicz]], _4-Manifolds and Kirby Calculus_ (1999), Graduate Studies 
in Mathematics, Volume 20 &lbrack;[ISBN: 978-0-8218-0994-5](https://www.ams.org/books/gsm/020), [doi:10.1090/gsm/020](https://www.ams.org/books/gsm/020)&rbrack;

* {#Nicolaescu00} [[Liviu Nicolaescu]], *Notes on Seiberg-Witten theory*, American Mathematical Society (2000) &lbrack;[ISBN:978-0-8218-2145-9](https://bookstore.ams.org/GSM/28), [pdf](https://www3.nd.edu/~lnicolae/new1.pdf)&rbrack;

[[!redirects Spinᶜ(3)]]
[[!redirects Spin^c(3)]]
[[!redirects Spinc3]]
[[!redirects Spin^c3]]
[[!redirects Spinᶜ3]]

[[!redirects Spinʰ(2)]]
[[!redirects Spin^h(2)]]
[[!redirects Spinh2]]
[[!redirects Spin^h2]]
[[!redirects Spinʰ4]]