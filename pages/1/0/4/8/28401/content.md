+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

\tableofcontents

## Idea

*Furuta's theorem* (also called *10/8 theorem*) describes which indefinite even [[intersection forms]] arise from [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifolds]]. (According to [[Freedman's classification]], all can from [[simply connected]] [[oriented]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifolds]], which makes smoothness the crucial property.) It comes down to the forms:
$$
\pm 2mE_8\oplus nH
$$
according to Serre's classification theorem with [[Rokhlin's theorem]] requiring an even number of definite $\pm E_8$ and indefiniteness requiring $n\geq 1$. [[Simon Donaldson]] furthermore showed, that if $m\neq 0$, then $n\geq 3$.

It's assumed that Furuta's theorem can be improved, which is known as the [[11/8 conjecture]]. For this reason, Furuta's theorem is also called 10/8 conjecture and not 5/4 conjecture.

## Statement

\begin{proposition}
Every [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifold]] $M$ with indefinite even [[intersection form]] fulfills:
$$
b_2(M)
\geq\frac{10}{8}|\sigma(M)|+2.
$$
Hence, if $\sigma(M)\geq 0$, then $9b_2^-(M)\geq b_2^+(M)$. If $\sigma(M)\leq 0$, then $9b_2^+(M)\geq b_2^-(M)$. Without loss of generality, Furuta's theorem can be restricted to one of these cases by reversing [[orientation]] with $b_2(\overline{M})=b_2 (M)$ and $\sigma(\overline{M})=-\sigma(M)$.

Alternatively, for the above structure of the [[intersection form]], the 3/2 conjecture is equivalent to:
$$
n\geq 2|m|+1.
$$
This follows from:
$$
b_2(M)
=16|m|+2n;
$$
$$
|\sigma(M)|
=16|m|.
$$
\end{proposition}

([Scorpan 05, p. 248](#Scorpan05))

For $|m|=1$ with $n\geq 3$, Furata's theorem is exactly Donaldson's prior work. For $m=|2|$ with $n\geq 5$, it was later concluded that Furuta's theorem doesn't give the best possible lower bound, as is generally assumed by the [[11/8 conjecture]]:

\begin{proposition}
The indefinite even intersection form $\pm 4E_8\oplus 5H$ isn't the [[intersection form]] of a [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifold]].
\end{proposition}

([Scorpan 05, p. 248](#Scorpan05))

## References

* {#Furuta95} [[Mikio Furuta]]: *Monopole Equation and the 11/8-Conjecture*, Mathematical Research Letters **8** (2001) 279-291 &lbrack;[doi:10.4310/MRL.2001.v8.n3.a5](https://doi.org/10.4310/MRL.2001.v8.n3.a5)&rbrack;

* {#Scorpan05} [[Alexandru Scorpan]], _The Wild World of 4-Manifolds_, American Mathematical Society (2005) &lbrack;[ISBN 978-1470468613](https://bookstore.ams.org/fourman)&rbrack;

[[!redirects Furuta lemma]]
[[!redirects Furuta's lemma]]
[[!redirects Furuta's theorem]]
[[!redirects 10/8 lemma]]
[[!redirects 10/8 theorem]]