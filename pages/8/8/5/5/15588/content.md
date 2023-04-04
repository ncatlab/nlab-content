
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _uniformization theorem_ for [[principal bundles]] over [[algebraic curves]] $X$ (going back to [[André Weil]]) expresses the [[moduli stack of principal bundles]] on $X$ as a double [[quotient stack]] of the $G$-valued [[Laurent series]] around finitely many points by the product of the $G$-valued [[formal power series]] around these points and the $G$-valued functions on the complement of theses points. 

If a single point $x$ is sufficient and if $D$ denotes the [[formal disk]] around that point and $X^\ast, D^\ast$ denote the complements of this point, respectively then the theorem says for suitable [[algebraic group]] $G$ that there is an equivalence of [[stacks]]

$$
   [X^\ast, G] \backslash [D^\ast, G] / [D,G]
   \simeq
   Bun_X(G)
 \,,
$$

between the double [[quotient stack]] of $G$-valued functions ([[mapping stacks]]) as shown on the left and the [[moduli stack of G-principal bundles]] over $X$, as shown on the right.

The theorem is based on the fact that $G$-bundles on $X$ trivialize on the complement of finitely many points  and that this double quotient then expresses the $G$-[[Cech cohomology]] with respect to the cover given by the complement of the points and the [[formal disks]] around them.

For details see at _[moduli stack of bundles -- over curves](http://ncatlab.org/nlab/show/moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence)_.

## Applications

The theorem is a key ingredient in the [[function field analogy]] where for $K$ a [[global field]] the nonabelian generalization of quotients of the [[idele class group]] by [[integral adeles]] 

$$
  GL_n(K) \backslash GL_n(\mathbb{A}_K) / GL_n(\mathcal{O}_K)
$$

are analogous to the moduli stack of $G$-bundles. This motivates notably the [[geometric Langlands correspondence]] as a geometric analog of the number-theoretic [[Langlands correspondence]].

## Related concepts

* [[differential cohesion and idelic structure]]

## References

Review is for instance

* {#Sorger99} [[Christoph Sorger]], _Lectures on moduli  of principal $G$-bundles over algebraic curves_, 1999 ([pdf](http://users.ictp.it/~pub_off/lectures/lns001/Sorger/Sorger.pdf))

See also

* [[Jochen Heinloth]], _Uniformization of $\mathcal{G}$-Bundles_ ([pdf](https://dare.uva.nl/search?identifier=35a7a6fe-9e92-4e37-8c2c-4b357709cc6f))

For more references see at _[[moduli stack of bundles]]_.

[[!redirects Weil uniformization]]