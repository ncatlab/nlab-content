
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition

A [[symmetric monoidal (∞,1)-category]] $(C,\otimes)$ is **closed** if for each [[object]] $X \in C$ the [[(∞,1)-functor]]

$$
  X \otimes (-) : C \to C
$$

given by forming the [[tensor product]] with $C$ has a [[right adjoint|right]] [[adjoint (∞,1)-functor]]

$$
  (X \otimes(-)\dashv [X,-] ) : C \stackrel{\overset{X \otimes (-)}{\leftarrow}}{\underset{[X,-]}{\to}} C
  \,.
$$

(In cases where the monoidal structure is not assumed symmetric, the property of possessing a right adjoint to tensoring on the left (resp. right) is called *left* (resp. *right*) *closed*, while *closed* is used for the properties jointly (Def. Definition 4.1.1.15 of [[Higher Algebra]]).)
=--

## Examples

* Every [[(∞,1)-topos]] with its structure of a [[cartesian monoidal (∞,1)-category]] is closed. See there for details.

* The [[(∞,1)-category of (∞,1)-modules]] over an [[E-∞ ring]] is closed.

## Related concepts

* [[monoidal category]], [[monoidal (∞,1)-category]]

* [[symmetric monoidal category]], [[symmetric monoidal (∞,1)-category]]

* [[closed monoidal category]],  **closed monoidal $(\infty,1)$-category**

* [[trace-class map]]

[[!redirects closed monoidal (∞,1)-category]]

[[!redirects closed monoidal (infinity,1)-categories]]
[[!redirects closed monoidal (∞,1)-categories]]
