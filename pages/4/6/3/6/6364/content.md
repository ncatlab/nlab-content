
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The _unitalization_ of a non-unital [[algebra]] is a unital algebra with a "unit" (an [[identity]] element) [[free construction|freely]] adjoined.

This is a [[free functor]]: [[Rng]] $\to$ [[Ring]].

## Definitions

### For (non)associative algebras

For $R$ a [[commutative ring]] write $R Alg_{\mathrm{u}}$ for the [[category]] of [[nonassociative algebra]]s with unit over $R$ and unit-preserving [[homomorphisms]], and write $R Alg_{\mathrm{nu}}$ for nonunital nonassociative $R$-algebras.  Note that $R Alg_{\mathrm{u}}$ is a [[subcategory]] of $R Alg_{\mathrm{nu}}$, as we use both 'non-unital' and 'non-associative' in accordance with the [[red herring principle]].

The [[inclusion functor]] $U\colon R Alg_{\mathrm{u}} \to R Alg_{\mathrm{nu}}$ has a [[left adjoint]] $(-)^+\colon R Alg_{\mathrm{u}} \to R Alg{\mathrm{u}}$. For $A \in R Alg_{\mathrm{nu}}$ we say $A^+$ is the **unitalization** of $A$.

Explicitly, $A^+ = A \oplus R$ as an $R$-[[module]], with product given by
$$ (a_1, 0) (a_2, 0) = (a_1 a_2, 0) ,$$
$$ (0, r_1) (0, r_2) = (0, r_1 r_2) ,$$
$$ (a,0) (0,r) = (0,r) (a,0) = (r a, 0) ,$$
or in general
$$ (a_1, r_1) (a_2, r_2) = (a_1 a_2 + r_2 a_1 + r_1 a_2, r_1 r_2) .$$
We often write $(a, r)$ as $a + r$ or $a \oplus r$, which makes the above formulas obvious.

If $A$ is an [[associative algebra]], then $A^+$ will also be associative; if $A$ is a [[commutative algebra]], then $A^+$ will also be commutative.


### For other (special) cases

See 

* _[[unitisation of rings]]_;

* _[[unitisation of C*-algebras]]_.


### Properties

The unitalization functor is not a [[conservative functor]].
\cite{Andruszkiewicz}

However, it does become conservative when restricted
to the full subcategory of nonunital algebras
over a [[field]] $k$
that do not admit a surjective homomorphism to $k$.
\cite{Andruszkiewicz}

### For $\mathbb{E}_k$-algebra

Unitisation in the generality of [[Ek-algebra]] -- hence for [[nonunital Ek-algebras]] -- unitalization is the content of ([Lurie, prop. 5.2.3.13](#Lurie)).


## Related concepts

* [[unit]]

* [[unitality]]


## References

* {#Lurie} [[Jacob Lurie]], section 5.2.3 of _[[Higher Algebra]]_

* [[Ryszard R. Andruszkiewicz]], _Surprise at Adjoining an Identity to an Algebra_, Vietnam Journal of Mathematics, [doi](https://doi.org/10.1007/s10013-020-00437-9).

[[!redirects unitalization]]
[[!redirects unitalizations]]
[[!redirects unitalisation]]
[[!redirects unitalisations]]
[[!redirects unitization]]
[[!redirects unitizations]]
[[!redirects unitisation]]
[[!redirects unitisations]]
