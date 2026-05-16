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

The *11/8 conjecture* arises from the still not fully answered question, which symmetric unimodular bilinear forms are the [[intersection forms]] of [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifolds]].

According to [[Donaldson's theorem]], a definite form is the [[intersection form]] of an [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifolds]] if and only if it's either $\oplus n[-1]$ or $\oplus n[+1]$, with both realized by the even [[simply connected]] examples $\#n\mathbb{C}P^2$ or $\#n\overline{\mathbb{C}P^2}$. According to Serre's classification theorem, an indefinite odd form is isomorphic to $\oplus m[-1]\oplus n[+1]$, which are all realized by the even [[simply connected]] examples $\#m\mathbb{C}P^2\#m\overline{\mathbb{C}P^2}$. (According to [[Freedman's theorem]], all these [[simply connected]] examples are even unique up to [[homeomorphism]].)

Left over is, which indefinite even forms are realized. It comes down to the forms:
$$
\pm 2mE_8\oplus nH
$$
according to Serre's classification theorem with [[Rokhlin's theorem]] requiring an even number of definite $\pm E_8$ and indefiniteness requiring $n\geq 1$. [[Simon Donaldson]] furthermore showed, that if $m\neq 0$, then $n\geq 3$.

Currently, the strongest result approaching the 11/8 conjecture is [[Furuta's theorem]], which is also called 10/8 theorem.

## Statement

The open 11/8 conjecture assumes: Every [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifold]] $M$ with indefinite even [[intersection form]] fulfills:
$$
b_2(M)
\geq\frac{11}{8}|\sigma(M)|.
$$
Hence, if $\sigma(M)\geq 0$, then $19b_2^-(M)\geq 3b_2^+(M)$. If $\sigma(M)\leq 0$, then $19b_2^+(M)\geq 3b_2^-(M)$. Without loss of generality, the 11/8 conjecture can be restricted to one of these cases by reversing [[orientation]] with $b_2(\overline{M})=b_2 (M)$ and $\sigma(\overline{M})=-\sigma(M)$.

Alternatively, for the above structure of the [[intersection form]], the 3/2 conjecture is equivalent to:
$$
n\geq 3|m|.
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

([Scorpan 05, p. 247](#Scorpan05))

Both reformulations of the 11/8 conjecture show, that the difference to [[Furuta's theorem]] or 10/8 theorem is bigger than the small difference between the fractions makes it seem.

If the 11/8 conjecture holds for two [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifolds]] $M$ and $N$ with indefinite even [[intersection form]], then it automatically holds for their [[connected sum]] when additionally using the triangle inequality:
$$
\frac{11}{8}|\sigma(M\# N)|
=\frac{11}{8}|\sigma(M)
+\frac{11}{8}\sigma(N)|
\leq b_2(M)
+b_2(N)
=b_2(M\# N).
$$
But that doesn't mean, that it's sufficient to prove the 11/8 conjecture just for irreducible (not splitting in a non-trivial [[connected sum]]) [[oriented]] [[closed manifold|closed]] [[smooth manifold|smooth]] [[4-manifolds]] with indefinite even [[intersection form]]. While all other properties reduce back to the splittings, indefiniteness doesn't. For example, a [[connected sum]] of manifolds with a positive and negative definite [[intersection form]] has indefinite [[intersection form]]. Definite forms are extremely numeruous and therefore lack a simple classification.

## Example

Further improvement of the 11/8 conjecture isn't possible as shown by the [[simply connected]] [[oriented]] [[closed manifold|closed]] [[K3 surface]] $K3\coloneqq V(z_0^3+z_1^3+z_2^3+z_3^3)\subset\mathbb{C}P^3$ with [[intersection form]]:
$$
Q_{K3}
=-2E_8
\oplus 3H.
$$
It therefore has $b_2(K3)=22$ and $\sigma(K3)=16$, meaning the 11/8 conjecture is an equality for it. Taking [[connected sums]] $\#m K3$ including reversing [[orientation]] (corresponding to flipping the sign of $m$) furthermore produces examples for equalities for every $m\in\mathbb{Z}$.

## Related entries

[[!include four-dimensional geometry and topology -- table]]

## References

* {#Scorpan05} [[Alexandru Scorpan]], _The Wild World of 4-Manifolds_, American Mathematical Society (2005) &lbrack;[ISBN 978-1470468613](https://bookstore.ams.org/fourman)&rbrack;

[[!redirects 11/8 problem]]