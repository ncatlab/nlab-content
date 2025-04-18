
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

(Compare the [[formal duality|dual]] notion of "[[free products]]" of groups, which are really their [[category theory|category theoretic]] *[[coproducts]]*.)


## Properties

### Representations
 {#Representations}

+-- {: .num_prop #IrrepsOfDirectProductsAreExternalTensorProductsOfIrreps}
###### Proposition
**([[irreps]] of [[direct product groups]] are [[external tensor products]] of [[irreps]])**

Let $G_1, G_2$ be two [[groups]]. Then, over an [[algebraically closed field|algebraically closed]] [[ground field]], every [[irreducible representation]] $\rho \in (G_1 \times G_2) Rep_{irr}$ of their [[direct product group]] $G_1 \times G_2$ is the [[external tensor product]] of [[irreducible representations]] $\rho_i \in G_i Rep_{irr}$ of the two groups separately:

$$
  \rho \;=\; \rho_1 \boxtimes \rho_2
  \,.
$$

Here the [[external tensor product]] has as [[underlying]] [[vector space]] the corresponding [[tensor product of vector spaces]], equipped with the evident [[action]]

$$
  (g_1, g_2)( (v_1 \otimes v_2) ) 
    \;=\; 
  \big( 
    g_1(v_1) \otimes g_2(v_2) 
  \big)
  \,.
$$

=--

(cf. [Fulton & Harris 1991 Ex. 2.36](#FultonHarris91))

+-- {: .proof}
###### Proof

By [[Schur's lemma]] see e.g. [here](https://math.stackexchange.com/a/2503141/58526).

=--


+-- {: .num_remark }
###### Remark

The statement of Prop. \ref{IrrepsOfDirectProductsAreExternalTensorProductsOfIrreps} is in general false if the ground field is not algebraically closed. A counterexample is given im [Kowalski 13, Example 2.7.31](#Kowalski13).

Also the converse to Prop. \ref{IrrepsOfDirectProductsAreExternalTensorProductsOfIrreps} is _false_ in general. The [[external tensor product]] of irreducible representations need not be irreducible itself. For more see [Fein 67](#Fein67).

=--


## Related concepts

* [[semidirect product group]]

* [[central product of groups]]

* [[free product of groups]]

## References

* {#Fein67} Burton Fein, _Representations of direct products of finite groups_, Pacific J. Math. **20** 1 (1967) 45-58 &lbrack;[euclid:1102992967](https://projecteuclid.org/euclid.pjm/1102992967)&rbrack;

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]]: _Representation Theory: a First Course_, Springer (1991) &lbrack;[doi:10.1007/978-1-4612-0979-9](https://link.springer.com/book/10.1007/978-1-4612-0979-9)&rbrack;

* {#Kowalski13} E. Kowalski, around p. 41 of _Representation theory_ (2013) &lbrack;[[KowalskiReptheory2013.pdf:file]]&rbrack;


* Wikipedia, _[Direct product of groups](https://en.wikipedia.org/wiki/Direct_product_of_groups)_

[[!redirects direct product groups]]

[[!redirects product group]]
[[!redirects product groups]]


[[!redirects direct product of groups]]
[[!redirects direct products of groups]]
