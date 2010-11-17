#Discussion#

The following observation of Conduch&#233; is very useful when working with [[simplicial groupoid|simplicial groupoids]].

+--{.un_prop}
######Proposition
If $G$  is a simplicial group(oid), then $G_n$ decomposes as a multiple [[semidirect product]]:

$$G_n \cong NG_n \rtimes  s_0NG_{n-1}\rtimes  s_1NG_{n-1}\rtimes  s_1s_0NG_{n-2}
\rtimes  s_2NG_{n-1}\rtimes  \ldots s_{n-1}s_{n-2}\ldots s_0NG_0$$
=--

The order of the terms corresponds to a lexicographic ordering of the indices
$\emptyset$; 0; 1; 1,0; 2; 2,0; 2,1; 2,1,0; 3; 3,0; $\ldots$ and so on, the
term corresponding to $i_1 \gt \ldots \gt i_p$ being $s_{i_1}\ldots s_{i_p}NG_{n-p}$. The actions involved are clear once the following lemma is examined.

The proof  of the result is an induction based on a simple lemma, which is  easy to prove.

+--{.un_lemma}
######Lemma
If $G$ is a simplicial group(oid), then $G_n$ decomposes as a
semidirect product:
$$G_n \cong Ker d^n_n \rtimes  s^{n-1}_{n-1}(G_{n-1}).$$
=--

This decomposition generalises the one used in the classical [[Dold-Kan correspondence]]. It is extremely useful when analysing the [[Moore complex]] of a simplicial group and the relationship between that complex and the original simplicial group. It plays a crucial role in the theory of [[hypercrossed complexes]].

#Reference#
D. Conduch&#233;, _Modules crois&#233;s g&#233;n&#233;ralis&#233;s de longueur 2_ , J. Pure Appl. Alg., 34, (1984), 155--178.

[[!redirects Conduché decomposition theorem]]