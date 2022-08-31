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

An $A_3$-type is a naive translation of the notion of [[monoid]] into [[dependent type theory]], such as [[homotopy type theory]].  If the underlying type is an [[h-set]] (such as if the type theory is [[extensional type theory|extensional]]), then it yields a correct notion of monoid.  Otherwise, it is only a "partly-coherent" notion of "homotopy monoid": a type-theoretic version of the notion of $A_3$-[[An-space|space]] from homotopy theory.

## Definition ##

An __$A_3$-type__ consists of

* A type $A$,
* A basepoint $e:A$
* A binary operation $\mu : A \to A \to A$
* A left unitor 
$$\lambda:\prod_{(a:A)} \mu(e,a)=a$$ 
* A right unitor 
$$\rho:\prod_{(a:A)} \mu(a,e)=a$$
* An asssociator 
$$\alpha:\prod_{(a:A)} \prod_{(b:A)} \prod_{(c:A)} \mu(\mu(a, b),c)=\mu(a,\mu(b,c))$$

### Homomorphisms of $A_3$-types ###

A __homomorphism of $A_3$-types between two $A_3$-types $A$ and $B$ is a function $\phi:A \to B$ such that 

* The basepoint is preserved, i.e. there is a specified identification
$$\phi(e_A) = e_B$$

* The binary operation is preserved, i.e. there is a specified function
$$\prod_{(a:A)} \prod_{(b:A)} \phi(\mu_A(a, b)) = \mu_B(\phi(a),\phi(b))$$

* The left unitor is preserved, i.e. there is a specified homotopy identifying the concatenation $ \phi(\mu_A(e_A,x)) = \mu_B(\phi(e_A),\phi(x)) = \mu_B(e_B,\phi(x)) = \phi(x)$ (which involves the left unitor of $B$) with the image $\phi(\mu_A(e_A,x)) = \phi(x)$ of the left unitor of $A$.

* Similarly, the right unitor is preserved.

* The associator is preserved in an analogous way.

## Examples ##

* The [[integers]] are an $A_3$-type under addition, as are the [[natural numbers type|natural numbers]].  More generally, as noted above, any [[h-set]] monoid is an $A_3$-type.

* Every [[loop space]] type $\Omega_x(X) \equiv (x=_X x)$ is naturally an $A_3$-type, with [[path]] concatenation as the operation.  In this case, the operation is in fact coherent, and indeed every loop space is a $\infty$-group (although this is difficult to express in type theory).

* The type of endofunctions $A \to A$ has the structure of an $A_3$-type, with basepoint $id_A$, operation function composition.  Once again the operation is coherent, so this is an $\infty$-monoid (inverses need not exist).

## See also ##

* [[higher algebra]]
* [[H-space]]
* [[monoid]]
* [[ring]]
* [[H-category]]
* [[An-space]]
* [[grouplike A3-space]]