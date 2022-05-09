## Definition

A __Hilbert W\*-module__ is a [[Hilbert C*-module]] $M$
over a [[von Neumann algebra]] $A$
such that:

* $M$ admits a [[predual]] $M_{\ast}$ as a [[Banach space]];

* for all $m \in M$, the map $\langle m, - \rangle_{A}: M \to A$ is normal (i.e. the dual of some map $A_{*} \to M_{*}$),

where $\langle -,- \rangle_{A}: \overline{M} \times M \rightarrow A$ is the 
$A$-valued inner product on $M$, and $A_{*}$ is the predual of $A$.

The above definition is equivalent to the definitions using a notion of self-duality (See [Blecher-Merdy, Lemma 8.5.4](#BlecherMerdy2004)).

## Properties

For any [[von Neumann algebra]] $A$,
the category of [[Hilbert W*-modules]] over $A$ is equivalent to the category of [[W*-representations]] of $A$.

The equivalence is implemented by the following functors.

Given a [[Hilbert W*-module]] $M$,
we send it to the [[completion]] of $M\otimes_A L^2(A)$,
where $L^2(A)$ is the Haagerup standard form of $A$.

Given a [[W*-representation]] $R$,
we send it to the [[internal hom]] $Hom_A(L^2(A), R)$,
which is a [[Hilbert W*-module]] over $A$.

## Related concepts

* [[measurable field of Hilbert spaces]]

* [[Serre-Swan theorem]]

* [[W*-representation]]

* [[Hilbert C*-module]]

* [[von Neumann algebra]]

* [[duality between geometry and algebra]]


## References

{#Paschke1973} [[William Paschke]], _Inner Product Modules over $B^\ast$-algebras_, Trans. Amer. Math. Soc., 182, 1973 ([link](https://www.ams.org/journals/tran/1973-182-00/S0002-9947-1973-0355613-0/S0002-9947-1973-0355613-0.pdf))

{#Blecher1997} [[David Blecher]], _On Selfdual Hilbert Modules_, Fields Institute Communications, 13, 1997

{#BlecherMerdy2004} [[David Blecher]], [[Christian Le Merdy]], _Operator and Their Modules---an operator space approach_, Vol. 30, London Mathematical Society Mongraphs

[[!redirects Hilbert W*-modules]]
[[!redirects W*-modules]]
[[!redirects W*-module]]
