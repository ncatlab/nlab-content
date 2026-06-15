
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition


An __automorphism__ of an [[object]] $x$ in a [[category]] $C$ is an [[isomorphism]] $f : x \to x$.  In other words, an automorphism is an [[endomorphism]] that is an [[isomorphism]].


## Automorphism group

Given an object $x$, the automorphisms of $x$ form a [[group]] under [[composition]], the __automorphism group__ of $x$, which is a submonoid of the [[endomorphism monoid]] of $x$:
$$
  Aut_C(x) = End_C(x) \cap Iso(C) = Iso_C(x,x)
,$$
which may be written $Aut(x)$ if the category $C$ is understood.  Up to equivalence, every group is an automorphism group; see [[delooping]].

For any [[category]] $C$, there exists a [[covariant functor]] $Aut : Core(C) \to Grp$ from the [[core groupoid|core]] to [[Grp]], which maps each object $A$ to an automorphism group $Aut(A)$ and each morphism $f$ to a conjugate as follows.

$$
\begin{array}{rl}
\mathrm{Aut}(f) : \mathrm{Aut}(A) & \longrightarrow \mathrm{Aut}(B) \\
a & \mapsto f \circ a \circ f^{-1} \\
\end{array}
$$

The [[contravariant functor|contravariant form]] can be obtained by changing the order of the conjugate as $f^{-1} \circ a \circ f$.

## Examples

* [[permutation|permutations]] are automorphisms in [[FinSet]]. 

* [[automorphism group of a Lie algebra]]

* [[automorphism of a vertex operator algebra]]


## Related concepts

* **automorphism group**

  * [[inner automorphism group]]

  * [[outer automorphism group]]

  * [[automorphism Lie group]]

* [[automorphism 2-group]]

* [[automorphism ∞-group]]


## References

* [[Marshall Hall]], §6 in: *The Theory of Groups*, Macmillan (1959), AMS Chelsea (1976), Dover (2018) &lbrack;[ISBN:978-0-8218-1967-8](https://bookstore.ams.org/view?ProductCode=CHEL/288), [ISBN:9780486816906](https://store.doverpublications.com/products/9780486816906)&rbrack;

Discussion of automorphism groups [[internalization|internal]] to [[sheaf toposes]] ("automorphism sheaves"):

* [[Robert Friedman]], [[John W. Morgan]], §2.1 in: *Automorphism sheaves, spectral covers, and the Kostant and Steinberg sections*, Contemporary Mathematics **322** (2003)  217-244 &lbrack;[arXiv:math/0209053](https://arxiv.org/abs/math/0209053)&rbrack;

* [[Simon Henry]] (2017) &lbrack;[MO:a/262687](https://mathoverflow.net/a/262687/381)&rbrack;


[[!redirects automorphisms]]
[[!redirects automorphism group]]
[[!redirects automorphism groups]]


[[!redirects group of automorphisms]]
[[!redirects groups of automorphisms]]
