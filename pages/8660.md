
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $R$ a [[ring]], an [[associative algebra]] over $R$ is a [[ring]] $A$ equipped with a ring inclusion $R \hookrightarrow A$. 

+-- {: .num_defn}
###### Definition

If the $R$-algebra $A$ is equipped with an $R$-algebra homomorphism the other way round, 

$$
  \epsilon \colon A \to R
$$

then it is called an _augmented algebra_.

=--

+-- {: .num_remark}
###### Remark

In [Cartan-Eilenberg](#CartanEilenberg) this is called a _supplemented algebra_.

=--

+-- {: .num_defn}
###### Definition

The [[kernel]] of $\epsilon$ is called the corresponding [[augmentation ideal]] in $A$.

=--




## Examples

+-- {: .num_example}
###### Example

An augmentation of a bare [[ring]] itself, being an [[associative algebra]] over the ring of [[integers]] $\mathbb{Z}$, is a ring homomorphism to the integers

$$
  \epsilon \colon R \to \mathbb{Z}
$$

=--

+-- {: .num_example}
###### Example

Every [[group algebra]] $R[G]$ is canonically augmented, the augmentation map being the operation that forms the sum of [[coefficients]] of the canonical basis elements.

=--

+-- {: .num_example}
###### Example

If $X$ is a variety over an algebraically closed field $k$ and $x\in X(k)$ is a closed point, then the local ring $\mathcal{O}_{X,x}$ naturally has the structure of an augmented $k$-algebra. The augmentation map $\mathcal{O}_{X,x}\rightarrow k$ is the evaluation map, and the augmentation ideal is the maximal ideal of $\mathcal{O}_{X,x}$.

=--

## Related concepts

* [[augmentation]]

* [[augmented A-∞ algebra]]

## References

* [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_
 {#CartanEilenberg}


[[!redirects augmented algebras]]
[[!redirects augmentation map]]
[[!redirects augmentation maps]]
