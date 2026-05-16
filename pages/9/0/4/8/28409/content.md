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

The *3/2 conjecture* arises from the still not fully answered question, which symmetric unimodular bilinear forms are the [[intersection forms]] of [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifolds]]. 

According to [[Donaldson's theorem]], a definite form is the [[intersection form]] of an [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifolds]] if and only if it's either $\oplus n[-1]$ or $\oplus n[+1]$, with both realized by the even [[simply connected]] examples $\#n\mathbb{C}P^2$ or $\#n\overline{\mathbb{C}P^2}$. According to Serre's classification theorem, an indefinite odd form is isomorphic to $\oplus m[-1]\oplus n[+1]$, which are all realized by the even [[simply connected]] examples $\#m\mathbb{C}P^2\#m\overline{\mathbb{C}P^2}$. (According to [[Freedman's theorem]], all these [[simply connected]] examples are even unique up to [[homeomorphism]].)

Left over is, which indefinite even forms are realized. It comes down to the forms:
$$
\pm 2mE_8\oplus nH
$$
according to Serre's classification theorem with [[Rokhlin's theorem]] requiring an even number of definite $\pm E_8$ and indefiniteness requiring $n\geq 1$. [[Simon Donaldson]] furthermore showed, that if $m\neq 0$, then $n\geq 3$.

## Statement

The open 3/2 conjecture assumes: Every irreducible (not splitting in a non-trivial [[connected sum]]) [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifold]] $M$ with indefinite even [[intersection form]] fulfills:
$$
\chi(M)
\geq\frac{3}{2}|\sigma(M)|.
$$
Alternatively, for the above structure of the [[intersection form]], the 3/2 conjecture is equivalent to:
$$
n\geq 4|m|-1.
$$
This follows from:
$$
\chi(M)
=b_2(M)+2
=16|m|+2n+2;
$$
$$
|\sigma(M)|
=16|m|.
$$

([Scorpan 05, p. 247](#Scorpan05))

## References

* {#Scorpan05} [[Alexandru Scorpan]], _The Wild World of 4-Manifolds_, American Mathematical Society (2005) &lbrack;[ISBN 978-1470468613](https://bookstore.ams.org/fourman)&rbrack;

[[!redirects 3/2 problem]]