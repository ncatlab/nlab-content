
[[!redirects H-monoid]]
[[!redirects H-monoids]]
[[!redirects A3 space]]
[[!redirects A3 spaces]]
[[!redirects A3-space]]
[[!redirects A3-spaces]]

[[!redirects homomorphism of H-monoids]]
[[!redirects homomorphisms of H-monoids]]
[[!redirects H-monoid homomorphism]]
[[!redirects H-monoid homomorphisms]]

[[!redirects homomorphism of A3-spaces]]
[[!redirects homomorphisms of A3-spaces]]
[[!redirects A3-space homomorphism]]
[[!redirects A3-space homomorphisms]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
=--
=--

## Contents ##
* table of contents
{:toc}

## Idea ##

Sometimes we can equip a [[type]] with a certain structure, called an $A_3$-algebra structure, allowing us to derive some nice properties about the type and 0-truncate it to form [[monoid|monoids]]. 

## Definition ##

### In classical mathematics

An __$A_3$-space__ is a homotopy associative [[H-space]] (but no coherence is required of the associator).

An __$H$-monoid__ is a [[monoid]] [[internalization|internal to]] the [[classical homotopy category]] of [[topological spaces]] [[Ho(Top)]], or in the homotopy category $Ho(Top)_*$ of [[pointed topological spaces]], which has a [[unit]] up to [[homotopy]]. 

### In homotopy type theory

Both notions coincide in [[homotopy type theory]]. An __$A_3$-space__ or __H-monoid__ consists of

* A type $A$,
* A basepoint $e:A$
* A binary operation $\mu : A \to A \to A$
* A left unitor 
$$\lambda:\prod_{(a:A)} \mu(e,a)=a$$ 
* A right unitor 
$$\rho:\prod_{(a:A)} \mu(a,e)=a$$
* An asssociator 
$$\alpha:\prod_{(a:A)} \prod_{(b:A)} \prod_{(c:A)} \mu(\mu(a, b),c)=\mu(a,\mu(b,c))$$

### Homomorphisms of $A_3$-spaces ###
A __homomorphism of $A_3$-spaces__ between two $A_3$-spaces $A$ and $B$ consists of 

* A function $\phi:A \to B$ such that 
  * The basepoint is preserved
$$\phi(e_A) = e_B$$
  * The binary operation is preserved
$$\prod_{(a:A)} \prod_{(b:A)} \phi(\mu_A(a, b)) = \mu_B(\phi(a),\phi(b))$$

* A function 

$$\phi_\lambda:\left(\prod_{(a:A)} \mu(e_A,a)=a\right) \to \left(\prod_{(b:B)} \mu(e_B,b)=b\right)$$

such that the left unitor is preserved:

$$\phi_\lambda(\lambda_A) = \lambda_B$$

* A function 

$$\phi_\rho:\left(\prod_{(a:A)} \mu(a, e_A)=a\right) \to \left(\prod_{(b:B)} \mu(b, e_B)=b\right)$$

such that the right unitor is preserved:

$$\phi_\rho(\rho_A) = \rho_B$$

* A function 

$$\phi_\alpha:\left(\prod_{(a_1:A)} \prod_{(a_2:A)} \prod_{(a_3:A)} \mu(\mu(a_1, a_2),a_3)=\mu(a_1,\mu(a_2,a_3))\right) \to \left(\prod_{(b_1:B)} \prod_{(b_2:B)} \prod_{(b_3:B)} \mu(\mu(b_1, b_2),b_3)=\mu(b_1,\mu(b_2,b_3))\right)$$

such that the associator is preserved:

$$\phi_\alpha(\alpha_A) = \alpha_B$$

## Examples ##

* The [[integers]] are an $A_3$-space. 

* Every [[loop space]] is naturally an $A_3$-space with [[path]] concatenation as the operation. In fact every [[loop space]] is a $\infty$-group.

* The type of endofunctions $A \to A$ has the structure of an $A_3$-space, with basepoint $id_A$, operation function composition.

* A [[monoid]] is a 0-truncated $A_3$-space. 

## See also ##

* [[higher algebra]]
* [[H-space]]
* [[monoid]]
* [[ring]]
* [[H-category]]
* [[An-space]]
* [[grouplike A3-space]]