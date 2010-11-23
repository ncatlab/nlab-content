## Definition

A __Gel'fand triple__ is datum of the form

$$
B\stackrel{J}\hookrightarrow H \stackrel{K}\hookrightarrow B^*
$$

where $H$ is a [[separable Hilbert space]], $B$ is a [[Banach space]], $B^*$ is a Banach dual of $B$, $J:B\hookrightarrow H$ is an injective [[bounded operator]] with dense image, and $K$ is the composition of the canonical isomorphism $H\cong H^*$ determined by the inner product (i.e. given by Riesz theorem) and of the Banach transpose (dual) $J^*: H^*\to B^*$ of the operator $J$. The fact that $J(B)$ is dense in $H$ implies that $J^*$ (hence also $K$)  is injective as well. 

More specifically this variant is called *Banach Gel'fand triple*, there are some other variants involving more general [[topological vector space]]s. In some cases one also uses the terminology *rigged Hilbert space*. Nuclear Gel'fand triples are very common. In Russian literature the term *enriched* Hilbert space is used (&#1086;&#1089;&#1085;&#1072;&#1097;&#1077;&#1085;&#1085;&#1086;&#1077; &#1075;&#1080;&#1083;&#1100;&#1073;&#1077;&#1088;&#1090;&#1086;&#1074;&#1086; &#1087;&#1088;&#1086;&#1089;&#1090;&#1088;&#1072;&#1085;&#1089;&#1090;&#1074;&#1086;). 

## Basic examples

A typical example is $B = \mathcal{S}(\mathbb{R}^n)$ (Schwarz space), $H = L^2(\mathbb{R}^n)$ and $B^* = \mathcal{S}'(\mathbb{R}^n)$ (the space of tempered (Schwarz) distributions). One of the basic facts on Fourier transform is that this Gel'fand triple is preserved by the Fourier transform.

Another natural example is $\mathcal{l}^1\hookrightarrow \mathcal{l}^2\hookrightarrow \mathcal{l}^\infty$. 

## Isomorphisms

An isomorphism of Gelfand triples $(B_1,H_1,B^*_1)\to (B_2,H_2,B^*_2)$ is a unitary isomorphism $H_1\to H_2$ which restricts to an isomorphism of Banach spaces $B_1\to B_2$, and which extends to a weak$*$- and norm-preserving continuous isomorphism $B_1^*\to B_2^*$. 

## Links and references

* wikipedia [rigged Hilbert space](http://en.wikipedia.org/wiki/Rigged_Hilbert_space)

* MathOverflow question: [good-references-for-rigged-hilbert-spaces](http://mathoverflow.net/questions/43313/good-references-for-rigged-hilbert-spaces)

* Feichtinger: A Banach Gelfand Triple Framework for
Regularization and Approximation [slides pdf](http://www.univie.ac.at/nuhag-php/dateien/talks/1086_eucetifeislides.pdf)


[[!redirects Gelfand triple]]