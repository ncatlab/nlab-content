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

*Freedman's classification* is a deep connection between topology and algebra, providing the full classification of [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifolds]] by their [[intersection form]] and their [[Kirby-Siebenmann invariant]]. It allows any symmetric unimodular [[bilinear form]] to be represented by such a manifold and translates isomorphism of these forms into [[homeomorphisms]] of such manifolds (for equal [[Kirby-Siebenmann invariant]] when it's odd). It in particular expanded the topological [[h-cobordism theorem]] to four dimensions and solved the topological [[Poincaré conjecture]] in four dimensions.

Freedman's classification was published by [[Michael Freedman]] in [1982](#Freedman82) and earned him a Fields Medal in 1986. His proof was expanded in the collaborative textbook *The Disc Embedding Theorem*, on which multiple mathematicians began working on in 2013 and which was eventually published in 2021.

## Statement

Every symmetric unimodular [[bilinear form]] can be realized as the [[intersection form]] of a [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifold]].

* If the form is even, then there exists exactly one such manifold up to [[homeomorphism]].

* If the form is odd, then there exist exactly two such manifolds up to [[homeomorphism]], which have different binary [[Kirby-Siebenmann invariant]], in particular implying that at most one of them is smoothable.

([Scorpan 05, p. 240](#Scorpan74))

Often, these results are rephrased as:

* If two [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifolds]] have the same even [[intersection form]], they're [[homeomorphic]].

* If two [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifolds]] have the same odd [[intersection form]] and [[Kirby-Siebenmann invariant]], they're [[homeomorphic]]. In particular, if both are smoothable, they're [[homeomorphic]].

## Examples

Freedman's classification allows to translate purely algebraic isomorphisms of symmetric unimodular [[bilinear forms]] into [[homeomorphisms]] of [[closed manifold|closed]] [[simply connected]] [[topological manifold|topological]] [[4-manifolds]].

For example, $S^2\times S^2$ and $\mathbb{C}P^2\#\overline{\mathbb{C}P^2}$ have [[intersection forms]] of same signature $0$ and rank $2$:
$$
Q_{S^2\times S^2}
=\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix};
$$
$$
Q_{\mathbb{C}P^2\#\overline{\mathbb{C}P^2}}
=\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}.
$$
But since the former form is even, while the latter is odd, they cannot be isomorphic and hence there cannot be a [[homeomorphism]] $S^2\times S^2\cong\mathbb{C}P^2\#\overline{\mathbb{C}P^2}$. But an expansion of the form or equivalently a [[connected sum]] can untangle the form and yield a [[homeomorphism]]:
$$
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}\oplus[-1]
\cong[+1]\oplus 2[-1]
\Rightarrow
\left(S^2\times S^2\right)\#\overline{\mathbb{C}P^2}
\cong\mathbb{C}P^2\# 2\overline{\mathbb{C}P^2} 
$$
$$
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}\oplus[+1]
\cong 2[+1]\oplus[-1]
\Rightarrow
\left(S^2\times S^2\right)\#\mathbb{C}P^2
\cong 2\mathbb{C}P^2\#\overline{\mathbb{C}P^2}
$$

There is an isomorphism of forms:
$$
E_8\oplus -E_8
\cong 8\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}.
$$
$M_{E_8}\#\overline{M_{E_8}}$ and $# 8(S^2\times S^2)$ both have this as their even [[intersection form]] and are both smoothable, so Freedman's classifciation gives a [[homeomorphism]]:
$$
M_{E_8}\#\overline{M_{E_8}}
\cong# 8(S^2\times S^2)
$$

([Scorpan 05, p. 240](#Scorpan74))

There is an isomorphism of forms:
$$
E_8\oplus[-1]
\cong 8[+1]\oplus[-1].
$$
$M_{E_8}\#\overline{\mathbb{C}P^2}$ and $8\mathbb{C}P^2 \#\overline{\mathbb{C}P^2}$ both have this as their odd [[intersection form]], but different [[Kirby-Siebenmann invariant]]. A way around is using the [[fake second complex projective space]] to flip it and obtain a [[homeomorphism]]:
$$
M_{E_8}\# *\overline{\mathbb{C}P^2}
\cong 8\mathbb{C}P^2\#\overline{\mathbb{C}P^2}.
$$

There is an isomorphism of forms:
$$
-E_8\oplus[+1]
\cong [+1]\oplus 8[-1].
$$
$\overline{M_{E_8}}\#\mathbb{C}P^2$ and $\mathbb{C}P^2 \# 8\overline{\mathbb{C}P^2}$ both have this as their odd [[intersection form]], but different [[Kirby-Siebenmann invariant]]. Again using the [[fake second complex projective space]] yields a [[homeomorphism]]:
$$
\overline{M_{E_8}}\# *\mathbb{C}P^2
\cong\mathbb{C}P^2 \# 8\overline{\mathbb{C}P^2}.
$$

([Scorpan 05, p. 242-243](#Scorpan74))

## Corollaries

A strong corollary of Freedman's classification is that it fully describes the splittings of [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifold]] into [[connected sums]], which breaks down for [[smooth manifold|smooth]] [[4-manifolds]]:
\begin{proposition}
If the [[intersection form]] of a [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifold]] $M$ splits:
$$
Q_M
\cong Q_1\oplus Q_2,
$$
then there are [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifolds]] $N_1$ and $N_2$ with them as [[intersection forms]] and a corresponding [[connected sum]]:
$$
M
\cong N_1#N_2
\cong *N_1#*N_2.
$$
\end{proposition}

Another strong corollary of Freedman's classification is that it allows to untangle the entire topological structure of a [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifold]]: A [[connected sum]] with either $\mathbb{C}P^2$ or $\overline{\mathbb{C}P^2}$ always makes the [[intersection form]] odd. A [[connected sum]] with $\mathbb{C}P^2\#\overline{\mathbb{C}P^2}$ furthermore always makes it indefinite. In this case, Serre's classification theorem or the Hesse-Minkowski theorem give an isomorphism to a direct sum of $[+1]$ and $[-1]$, which can be also be realized by a [[connected sum]] of $\mathbb{C}P^2$ and $\overline{\mathbb{C}P^2}$.
\begin{proposition}
For a [[simply connected]] [[closed manifold|closed]] [[topological manifold|topological]] [[4-manifold]] $M$, there is a [[homeomorphism]]:
$$
M\#\mathbb{C}P^2\#\overline{\mathbb{C}P^2}
\cong\left(b_2^+(M)+1\right)\mathbb{C}P^2\#\left(b_2^-(M)+1\right)\overline{\mathbb{C}P^2}.
$$
\end{proposition}

([Scorpan 05, p. 238](#Scorpan74))

## Connection with Donaldson's theorem

Freedman's classification can be combined with [[Donaldson's theorem]], which causes both to be restricted: Freedman's classification requires [[simply connected|simple connectedness]] and [[Donaldson's theorem]] requires [[smooth structure|smoothness]], both of which are not required for the respective other result. (Initially, [[simply connected|simple connectedness]] was required for [[Donaldson's theorem]] when first published in 1983, but it was improved to work without in 1987.)

\begin{proposition}
A [[simply connected]] [[compact]] [[oriented]] [[smooth manifold|smooth]] [[4-manifold]] $M$ with definite [[intersection form]] is [[homeomorphic]] to $\# b_2^+(M)\mathbb{C}P^2$ if it's positive definite or [[homeomorphic]] to $\# b_2^-(M)\overline{\mathbb{C}P^2}$ if it's negative definite.
\end{proposition}
\begin{proof}
According to [[Donaldson's theorem]], $M$ has a diagonal [[intersection form]], which is $\oplus b_2^+(M)(+1)$ if it's positive definite or $\oplus b_2^-(M)(-1)$ if it's negative definite. $\# b_2^+(M)\mathbb{C}P^2$ with $Q_{\mathbb{C}P^2}=(+1)$ and $\# b_2^-(M)\overline{\mathbb{C}P^2}$ with $Q_{\overline{\mathbb{C}P^2}}=(-1)$ also have these respective intersection forms and are simply connected due to $\pi_1(\mathbb{C}P^2)\cong\pi_1(\overline{\mathbb{C}P^2})\cong 1$, so are [[homeomorphic]] according to Freedman's classification. (Required here is that for two [[topological manifold|topological]] [[4-manifolds]] $M$ and $N$, one has $Q_{M# N}\cong Q_M\oplus Q_N$ and $\pi_1(M# N)\cong\pi_1(M)*\pi_1(N)$.)
\end{proof}

## References

* {#Freedman82} [[Michael Freedman]], _The topology of 4-manifolds_, J. Differential Geometry **17** 3 (1982), pp. 357–453 &lbrack;[doi:10.4310/jdg/1214437136](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-17/issue-3/The-topology-of-four-dimensional-manifolds/10.4310/jdg/1214437136.full) [ISSN 0022-040X](ttps://search.worldcat.org/de/search?q=n2:0022-040X) [MR 0679066](https://mathscinet.ams.org/mathscinet/relay-station?mr=0679066)&rbrack;

* {#FreedmanQuinn90} [[Michael Freedman]], [[Frank Quinn]], _Topology of 4-Manifolds_ (1990) &lbrack;[doi:10.1515/9781400861064](https://doi.org/10.1515/9781400861064)&rbrack;

* {#Scorpan05} [[Alexandru Scorpan]], _The Wild World of 4-Manifolds_, American Mathematical Society (2005) &lbrack;[ISBN 978-1470468613](https://bookstore.ams.org/fourman)&rbrack;

[[!redirects Freedman's classification]]
[[!redirects Freedman theorem]]
[[!redirects Freedman's theorem]]