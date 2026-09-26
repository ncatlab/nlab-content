

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An algorithm is a computational system that, for a given class of mathematical problems, allows one to arrive at a solution "record" $B$ from a problem condition record $A$. The process from $A$ to $B$ is an entirely mechanical, determined sequence of operations.

## Formal definition

We define $\mathfrak{T}$ as a [[natural number | naturally]] ordered set of classes $T_{0}, T_{1}, T_{2}, \dots, T_{r}$. The states of the algorithm are constructed from the "elements" of which these classes consist; each class $T_{i}$ has what is described as an "unlimited volume," that is, infinitely many elements of that type. These classes are mutually disjoint, and we denote the union of these classes simply as $T$, that is, $T := \bigcup_{i = 0}^{r}\,{T_{i}}$.

We also say that an element of class $T_{i}$ is an element of "type $T_{i}$" and we denote this (prototypical) element as a circle with the number $i$ within it: ⓘ.

We define a "complex over the set $\mathfrak{T}$" as an "ordinary one-dimensional complex with vertices from $\mathfrak{T}$." Explicitly, given $K_{0}$ to be a finite set $\{O_{\alpha}\}$ consisting of certain elements from $\mathfrak{T}$ (corresponding to the complex's vertices) and $K_{1}$ to be a finite set consisting of pairs of elements from $K_{0}$ (corresponding to the "segments" of the complex), we may define a complex $K$ over the set $\mathfrak{T}$ as the union $K := K_{0} \cup K_{1}$.

Given that $S$ is a complex as defined above, we define the "active part" $U(S)$ to be the subcomplex of $S$ consisting of all vertices and segments belonging to chains of length $\lambda \leq N$ which contain/start from the initial vertex ($N$ is an arbitrarily fixed number for a given algorithm $\Gamma$).

States are constructed as complexes over $\mathfrak{T}$, wherein calculations, step-by-step, physically alter the active part of the state strictly based on predefined immediate processing rules, a finite list of graph transformation rules determining explicitly how $\Omega_{\Gamma}$ operates on $S$ to transform it into subsequent $S^*$.

The rules are specified with a fixed set of paired states: $U_{1} \to W_{1}, U_{2} \to W_{2}, \dots, U_{r} \to W_{r}$. Each of the algorithm's conditions, each $U_{i}$, is a valid active part, i.e., $U(U_{i}) = U_{i}$ (the operator $U$ does not alter or remove anything from its argument). To make sure the algorithm is deterministic, we must have that $U_{i} \not\cong U_{j}$ for all $1 \leq i, j \leq r$. Each state replacement, each (arbitrary) $W_{i}$, replaces its corresponding active part $U_{i}$. Each pair ($U_{i}$, $W_{i}$) has a corresponding isomorphism $\varphi_{i} : L(U_{i}) \to \tilde{L}(W_{i})$ where $\tilde{L}(W_{i})$ denotes a certain, specific subcomplex of $W_{i}$ (i.e., $\tilde{L}(W_{i}) \subseteq W_{i}$). $L(U_{i}) = U(U_{i}) \cap V(U_{i})$ denotes the boundary of $U_{i}$ where $V(S)$ denotes the external part of $S$, the subcomplex of $S$ consisting of vertices that *cannot* be connected to initial vertex by chains shorter than $N$ (i.e., chains $\lambda \lt N$), as well as segments that *enter* the chains of length $\lambda \leq N$ that contain the initial vertex.

Finally, we may formally define an algorithm (à la Kolmogorov and Uspenskii): an algorithm $\Gamma$ is a state transition operator $S^* := \Omega_{\Gamma}(S)$, from a computational state $S$ to a subsequent state $S^*$.

For a (current) state $S$, $\Gamma$ checks if $U(S) \cong U_{i}$ for some $U_{i}$ (some predefined complex in the fixed rule set of paired states); if a match is found, then we now have that the state is within the domain of the algorithm, denoted $\mathfrak{D}(\Gamma)$. Since the complexes, $U(S)$ and $U_{i}$, are connected, the isomorphism $U(S) \cong U_{i}$ induces a unique isomorphism $L(S) \cong L(U_{i})$. The algorithm will then create a new complex $\tilde{W}$ ($\cong W_{i}$); however, the paper does not provide a step-by-step process for this complex, instead positing that "obviously, one can form a complex $\tilde{W}$ isomorphic to complex $W_{i}$" with the following conditions:

1. $\tilde{W} \cap V(S) = L(S)$: wherein $\tilde{W}$ and $V(S)$ are disjoint sans $L(S)$ or, in other words, $\tilde{W}$ and $V(S)$ only share the boundary vertices.
2. Isomorphism extension: the composition of $L(S) \cong L(U_{i})$ with the (predefined) $\varphi_{i}$ induces a unique boundary-oriented isomorphism $G_{i}^{S} : L(S) \overset{\cong}{\longrightarrow} \tilde{L}(W_{i})$. $\Gamma$ has it that $\tilde{W} \cong W_{i}$ must be a direct extension of the induced $G_{i}^{S}$.

The final stage of the algorithm, upon the definition of $\tilde{W}$ using the previous conditions, defines the subsequent state $S^*$ of the current state $S$: $S^* = \tilde{W} \cup V(S)$.

## Applications

* [[effective homology]]

## Related concepts

* [[quantum algorithm]]

* [[program]]

* [[programming language]]

* [[computation]]

* [[experimental mathematics]]

* [[long division]]

## References

* [[A. M. Turing]]. _On Computable Numbers, with an Application to the Entscheidungs problem_), Proceedings of the London Mathematical Society. 2 (1937) 42: 230&#8211;265. ([pdf](https://www.cs.virginia.edu/~robins/Turing_Paper_1936.pdf))

* [[A. N. Kolmogorov]] and V. A. Usp&#233;nski. On the definition of an algorithm. Uspehi Mat. Nauk. 13 (1958), 3-28. English translation in American Mathematical Society Translations, Series II, Volume 29 (1963), pp. 217&#8211;245. ([math-net.ru](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=rm&paperid=7453&option_lang=eng)). Also see JSL review by Elliott Mendelson on [jstor](http://www.jstor.org/stable/2272011). 

See also

* Wikipedia, _[Algorithm](http://en.wikipedia.org/wiki/Algorithm)_

[[!redirects algorithms]]

