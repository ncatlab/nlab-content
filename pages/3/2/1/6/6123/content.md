
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

+-- {: .num_defn}
###### Definition

For $R$ a [[ring]], its _group of units_, denoted $R^\times$ or $GL_1(R)$, is the [[group]] whose elements are the elements of $R$ that are invertible under the product, and whose group operation is the multiplication in $R$.

=--

+-- {: .num_remark}
###### Remark

$GL_1(R)$ is an [[affine variety]] (in fact an affine [[algebraic group]]) over $R$, namely $\{(x, y) \in R^2: x y = 1\}$. 

=--

This leads us to the following alternative perspective: 

+-- {: .num_defn}
###### Definition

In a [[category]] with [[finite limits]], with $R$ a [[ring object]] therein, the _group of units_ of $R$ is the [[equalizer]] of the two maps $m, c_1: R \times R \to R$, where $m$ is the ring multiplication and $c_1$ is the [[constant map]] with value the multiplicative identity.  
=--

Cf. Example \ref{idele} below.



## Properties

### Relation to the multiplicative group

+-- {: .num_prop}
###### Proposition

The group of units of $R$ is equivalently the collection of [[morphisms]]
from $Spec R$ into the [[group of units]] $\mathbb{G}_m$

$$
  GL_1(R) = R^\times \simeq Hom(Spec R, \mathbb{G}_m)
  \,.
$$

=--





### Relation to the group ring

+-- {: .num_remark}
###### Remark

There is an [[adjunction]]

$$
  (R[-]\dashv (-)^\times)
  \colon 
  Alg_R \stackrel{\overset{R[-]}{\leftarrow}}{\underset{(-)^\times}{\to}} Grp
$$

between the [[category]] of [[associative algebras]] over $R$ and that of [[groups]], where $R[-]$ forms the [[group algebra]] over $R$ and where $(-)^\times$ assigns to an $R$-algebra its group of units.

=--

## Examples

+-- {: .num_example}
###### Example

The multiplicative group of the [[ring]] of [[integers]] modulo $n$ is the  _[[multiplicative group of integers modulo n]]_.

=--

+-- {: .num_example #idele}
###### Example

The group of units of the [[ring of adeles]] $\mathbb{A}$ is the [[group of ideles]]. The topology on the idele group $\mathbb{I}$ arises by considering $\mathbb{I}$ as an affine variety in $\mathbb{A}^2$ as above, and giving it the subspace topology. This is _not_ the subspace topology induced by the inclusion $\mathbb{I} \hookrightarrow\mathbb{A}$ into the ring of adeles. 

=--

+-- {: .num_example} 
###### Example 
The group of units of the $p$-adic integers $\mathbb{Z}_p$ fits in an [[exact sequence]] 

$$1 \to 1 + p \mathbb{Z}_p \hookrightarrow \mathbb{Z}_p^\times \to (\mathbb{Z}/(p))^\times \to 1$$ 

where the [[quotient]] is isomorphic to the [[cyclic group]] $\mathbb{Z}/(p-1)$ (see [[root of unity]]) and the [[kernel]] is, at least when $p \gt 2$, isomorphic to the *additive group* $\mathbb{Z}_p$. Explicitly, for such $p$ the formal [[exponential map]] $\exp(x) = \sum_{n \geq 0} \frac{x^n}{n!}$ converges when $x \in p \mathbb{Z}_p$ and maps $p \mathbb{Z}_p$ isomorphically onto the multiplicative group $1 + p \mathbb{Z}_p$. The formal logarithm $\log(x) = \sum_{n \geq 1} \frac{(-1)^{n-1} (x - 1)^n}{n}$ is also [[convergence|convergent]] for $x \in 1 + p \mathbb{Z}_p$ and provides the [[inverse]]. 

By [[Henselian ring|Hensel's lemma]], the group of units $\mathbb{Z}_p^\times$ has $(p-1)^{th}$ [[roots of unity]] and therefore the exact sequence above [[split exact sequence|splits]]. This splitting descends to the quotient ring $\mathbb{Z}/(p^n)$ and its group of units, giving an isomorphism $GL_1(\mathbb{Z}/(p^n)) \cong \mathbb{Z}/(p^{n-1}) \oplus \mathbb{Z}/(p-1)$. 
=-- 



## Related concepts

* **group of units**/[[multiplicative group]], [[Picard group]], [[Brauer group]]

* [[multiplicative submonoid of cancellative elements]]

* [[∞-group of units]]

* [[multiplicative group]]

* [[exponential sequence]], [[Kummer sequence]]

## References

For instance:

* [[Anthony Knapp]], p. 143 in: *Basic Algebra*, Springer (2006) &lbrack;[doi:10.1007/978-0-8176-4529-8](https://doi.org/10.1007/978-0-8176-4529-8), [pdf](https://www.math.mcgill.ca/darmon/courses/19-20/algebra2/knapp.pdf)&rbrack;




[[!redirects groups of units]]