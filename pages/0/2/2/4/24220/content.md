
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

## Idea

In [[dependent type theory]], an *associative [[H-space]]* (cf. [BCFR23](#BCFR23)) or *$A_3$-space* is a naive translation of the notion of [[monoid]]. If the underlying type is an [[h-set]] (such as if the type theory is [[extensional type theory|extensional]]), then it yields a correct notion of monoid.  Otherwise, it is only a "partly-coherent" notion of "homotopy monoid": a type-theoretic version of the notion of $A_3$-[[An-space|space]] from homotopy theory.

## Definition

Similar to the definition of [[H-spaces]], there are coherent and non-coherent versions of associative H-spaces:

### Non-coherent associative H-spaces

A **non-coherent associative H-space** or **non-coherent $A_3$-space** consists of

* A type $A$,
* A basepoint $e:A$
* A binary operation $\mu : A \to A \to A$
* A left unitor 
$$\lambda:\prod_{x:A} \mu(e,x)=x$$ 
* A right unitor 
$$\rho:\prod_{x:A} \mu(x,e)=x$$
* An asssociator 
$$\alpha:\prod_{x:A} \prod_{y:A} \prod_{z:A} \mu(\mu(x, y),z)=\mu(x,\mu(y,z))$$

### Coherent associative H-spaces

A **coherent associative H-space** or **coherent $A_3$-space** is a non-coherent associative H-space $A$ which additionally has the coherence condition

$$\mu_{\lambda \rho}:\lambda(e) = \rho(e)$$

since $\lambda(e)$ and $\rho(e)$ are elements of the identity type $\mu(e, e) = e$. 

## Homomorphisms of associative H-spaces

There are also two different notions of homomorphisms between associative H-spaces, depending on whether the H-space is coherent or not. 

### Homomorphisms of non-coherent associative H-spaces

A **homomorphism of non-coherent associative H-spaces** between two non-coherent associative H-spaces $A$ and $B$ is a function $\phi:A \to B$ such that 

* The basepoint is preserved, i.e. there is a specified identification
$$\phi_e:\phi(e_A) = e_B$$

* The binary operation is preserved, i.e. there is a specified dependent function
$$\phi_\mu:\prod_{x:A} \prod_{y:A} \phi(\mu_A(x, y)) = \mu_B(\phi(x),\phi(y))$$

* The left unitor is preserved, i.e. there is a specified homotopy identifying the concatenation of identifications 
$$\phi_\mu(e_A, x):\phi(\mu_A(e_A,x)) = \mu_B(\phi(e_A),\phi(x))$$ 
$$\mathrm{ap}_{\lambda y:B.\mu_B(y,\phi(x))}(\phi_e):\mu_B(\phi(e_A),\phi(x)) = \mu_B(e_B,\phi(x))$$ 
$$\lambda_B(\phi(x)):\mu_B(e_B,\phi(x)) = \phi(x)$$ 
with the image $\mathrm{ap}_{\phi}(\lambda_A(x)):\phi(\mu_A(e_A,x)) = \phi(x)$ of the left unitor of $A$.
$$\phi_\lambda:\prod_{x:A} \phi_\mu(e_A, x) \bullet \mathrm{ap}_{\lambda y:B.\mu_B(y,\phi(x))}(\phi_e) \bullet \lambda_B(\phi(x)) = \mathrm{ap}_{\phi}(\lambda_A(x))$$

* Similarly, the right unitor is preserved, i.e. there is a specified homotopy identifying the concatenation of identifications 
$$\phi_\mu(x, e_A):\phi(\mu_A(x,e_A)) = \mu_B(\phi(x),\phi(e_A))$$ 
$$\mathrm{ap}_{\lambda y:B.\mu_B(\phi(x),y)}(\phi_e):\mu_B(\phi(x),\phi(e_A)) = \mu_B(\phi(x),e_B)$$ 
$$\rho_B(\phi(x)):\mu_B(\phi(x),e_B) = \phi(x)$$ 
with the image $\mathrm{ap}_{\phi}(\rho_A(x)):\phi(\mu_A(x,e_A)) = \phi(x)$ of the right unitor of $A$.
$$\phi_\rho:\prod_{x:A} \phi_\mu(x, e_A) \bullet \mathrm{ap}_{\lambda y:B.\mu_B(\phi(x),y)}(\phi_e) \bullet \rho_B(\phi(x)) = \mathrm{ap}_{\phi}(\rho_A(x))$$

* The associator is preserved in an analogous way.

### Homomorphisms of coherent associative H-spaces

A **homomorphism of coherent associative H-spaces** between two coherent associative H-spaces $A$ and $B$ is a homomorphism of non-coherent associative H-spaces $\phi:A \to B$ in which the coherence condition is preserved.

## Examples

* The [[integers]] are an associative H-space under addition, as are the [[natural numbers type|natural numbers]]. More generally, as noted above, any [[h-set]] monoid is an associative H-space

* Every [[loop space]] type $\Omega_x(X) \equiv (x=_X x)$ is naturally an associative H-space, with [[path]] concatenation as the operation.  In this case, the operation is in fact coherent, and indeed every loop space is a $\infty$-group (although this is difficult to express in type theory).

* The type of endofunctions $A \to A$ has the structure of an associative H-space, with basepoint $id_A$, operation function composition.  Once again the operation is coherent, so this is an $\infty$-monoid (inverses need not exist).

* The type of coherent H-space structures on a central type is a coherent associative H-space. 

## Related concepts

* [[higher algebra]]
* [[H-space]]
* [[monoid]]
* [[ring]]
* [[H-category]]
* [[An-space]]
* [[grouplike A3-space]]

## References

* {#BCFR23} [[Ulrik Buchholtz]], [[J. Daniel Christensen]], [[Jarl G. Taxerås Flaten]], [[Egbert Rijke]], *Central H-spaces and banded types* &lbrack;[arXiv:2301.02636](https://arxiv.org/abs/2301.02636)&rbrack;

[[!redirects associative H-space]]
[[!redirects associative H-spaces]]
[[!redirects associative H space]]
[[!redirects associative H spaces]]

[[!redirects non-coherent associative H-space]]
[[!redirects non-coherent associative H-spaces]]
[[!redirects non-coherent associative H space]]
[[!redirects non-coherent associative H spaces]]

[[!redirects coherent associative H-space]]
[[!redirects coherent associative H-spaces]]
[[!redirects coherent associative H space]]
[[!redirects coherent associative H spaces]]

[[!redirects associative H-space type]]
[[!redirects associative H-space types]]
[[!redirects associative H space type]]
[[!redirects associative H space types]]

[[!redirects non-coherent associative H-space type]]
[[!redirects non-coherent associative H-space types]]
[[!redirects non-coherent associative H space type]]
[[!redirects non-coherent associative H space types]]

[[!redirects coherent associative H-space type]]
[[!redirects coherent associative H-space types]]
[[!redirects coherent associative H space type]]
[[!redirects coherent associative H space types]]

[[!redirects A3-type]]
[[!redirects A3-types]]
[[!redirects A3 type]]
[[!redirects A3 types]]

[[!redirects non-coherent A3-type]]
[[!redirects non-coherent A3-types]]
[[!redirects non-coherent A3 type]]
[[!redirects non-coherent A3 types]]

[[!redirects coherent A3-type]]
[[!redirects coherent A3-types]]
[[!redirects coherent A3 type]]
[[!redirects coherent A3 types]]

[[!redirects A3-space]]
[[!redirects A3-spaces]]
[[!redirects A3 space]]
[[!redirects A3 spaces]]

[[!redirects non-coherent A3-space]]
[[!redirects non-coherent A3-spaces]]
[[!redirects non-coherent A3 space]]
[[!redirects non-coherent A3 spaces]]

[[!redirects coherent A3-space]]
[[!redirects coherent A3-spaces]]
[[!redirects coherent A3 space]]
[[!redirects coherent A3 spaces]]

[[!redirects A3-space type]]
[[!redirects A3-space types]]
[[!redirects A3 space type]]
[[!redirects A3 space types]]

[[!redirects non-coherent A3-space type]]
[[!redirects non-coherent A3-space types]]
[[!redirects non-coherent A3 space type]]
[[!redirects non-coherent A3 space types]]

[[!redirects coherent A3-space type]]
[[!redirects coherent A3-space types]]
[[!redirects coherent A3 space type]]
[[!redirects coherent A3 space types]]