
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[vector bundle]], its _dual_ is the vector bundle obtained by passing [fiber-wise](topological+vector+bundle#FiberwiseOperations) to the [[dual vector space]].

## Examples

* Given a [[smooth manifold]] $X$ with [[tangent bundle]] $T X$, the dual vector bundle is the [[cotangent bundle]] $T^\ast X$.

+-- {: .num_prop #FinitrRankBundleHomomorphismIsSectionOfTensorProductWithDual}
###### Proposition

Let $X$ be a [[topological space]] and let $E_i \overset{p_i}{\to} X$ be two [[topological vector bundles]] over $X$, of [[finite number|finite]] [[rank of a vector bundle]]. Then a [[homomorphism]] of vector bundles

$$
  f \;\colon\; E_1 \rightarrow E_2
$$

is equivalently a [[section]] of the [[tensor product of vector bundles]] of $E_2$ with the dual vector bundle of $E_1$.


$$
  Hom_{Vect(X)}(E_1, E_2)
   \;\simeq\;
  \Gamma_X( E_1^\ast \otimes_X E_2 )
  \,.
$$

Moreover, this section is a trivializing section ([this example](topological+vector+bundle#FiberwiseLinearlyIndependentSectionsTrivialize)) precisely if the corresponding morphism is an [[isomorphism]].


=--


## Related concepts

* [[direct sum of vector bundles]]

* [[tensor product of vector bundles]], [[external tensor product of vector bundles]]

* [[tensor category]]


## Related concepts

* [[Max Karoubi]], §4.8 in: _K-Theory -- An introduction_, Grundlehren der mathematischen Wissenschaften **226** Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3)&rbrack;




[[!redirects dual vector bundes]]
