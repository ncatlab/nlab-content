
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[Cartesian product]] in the [[category]] of [[groups]] is often called the _direct product_ of groups. For [[abelian groups]] and a [[finite number]] of factors, this is also the [[direct sum]] of groups.


## Properties

### Representations
 {#Representations}

+-- {: .num_prop #IrrepsOfDirectProductsAreExternalTensorProductsOfIrreps}
###### Proposition
**([[irreps]] of [[direct product groups]] are [[external tensor products]] of [[irreps]])**


Let $G_1, G_2$ be two [[groups]]. Then every [[irreducible representation]] $\rho \in (G_1 \times G_2) Rep_{irr}$ of their [[direct product group]] $G_1 \times G_2$ is the [[external tensor product]] of [[irreducible representations]] $\rho_i \in G_i Rep_{irr}$ of the two groups separately:

$$
  \rho \;=\; \rho_1 \boxtimes \rho_2
  \,.
$$

Here the [[external tensor product]] has as underlying [[vector space]] the corresponding [[tensor product of vector spaces]], equipped with the evident [[action]]

$$
  (g_1, g_2)( (v_1 \otimes v_2) ) \;=\; ( g_1(v_1) \otimes g_2(v_2) )
  \,.
$$

=--

+-- {: .proof}
###### Proof


By [[Schur's lemma]] see e.g. [here](https://math.stackexchange.com/a/2503141/58526).

=--

+-- {: .num_remark }
###### Remark

The converse to Prop. \ref{IrrepsOfDirectProductsAreExternalTensorProductsOfIrreps} is _false_ in general. The [[external tensor product]] of irreducible representations need not be irreducible itself. For more see [Fein 67](#Fein67).

=--


## Related concepts

* [[semidirect product group]]

## References

* {#Fein67} Burton Fein, _Representations of direct products of finite groups_,     Pacific J. Math. Volume 20, Number 1 (1967), 45-58 ([Euclid:1102992967](https://projecteuclid.org/euclid.pjm/1102992967))
See also

* Wikipedia, _[Direct product of groups](https://en.wikipedia.org/wiki/Direct_product_of_groups)_

[[!redirects direct product groups]]

[[!redirects product group]]
[[!redirects product groups]]


[[!redirects direct product of groups]]
[[!redirects direct products of groups]]
