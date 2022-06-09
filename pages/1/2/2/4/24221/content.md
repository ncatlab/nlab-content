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

The invertible version of the [[A3-space]] up to homotopy, without any higher coherences for inverses.

## Definition ##
A __grouplike $A_3$-space__ or __grouplike $A_3$-algebra in homotopy types__ or __H-group__ consists of

* A type $A$,
* A basepoint $e:A$
* A binary operation $\mu : A \to A \to A$
* A unary operation $\iota: A \to A$
* A left unitor 
$$\lambda_u:\prod_{(a:A)} \mu(e,a)=a$$ 
* A right unitor 
$$\rho_u:\prod_{(a:A)} \mu(a,e)=a$$
* An asssociator 
$$\alpha:\prod_{(a:A)} \prod_{(b:A)} \prod_{(c:A)} \mu(\mu(a, b),c)=\mu(a,\mu(b,c))$$
* A left invertor 
$$l:\prod_{(a:A)} \mu(\iota(a), a)=e$$ 
* A right invertor 
$$r:\prod_{(a:A)} \mu(a,\iota(a))=e$$

One could also speak of grouplike $A_3$-spaces where the existence of left and right inverses are mere property rather than structure, which is a grouplike $A_3$-space as defined above with additional structure specifying that the types $\prod_{(a:A)} \mu(\iota(a), a)=e$ and $\prod_{(a:A)} \mu(a,\iota(a))=e$ are [[contractible]]: 

$$c_l: \sum_{l:\prod_{(a:A)} \mu(\iota(a), a)=e} \prod_{b:\prod_{(a:A)} \mu(\iota(a), a)=e} l = b$$
$$c_r: \sum_{r:\prod_{(a:A)} \mu(a,\iota(a))=e} \prod_{b:\prod_{(a:A)} \mu(a,\iota(a))=e} r = b$$

or equivalently,

$$c_l:\prod_{(a:A)} \sum_{(l:\mu(\iota(a), a)=e)} \prod_{(b:\mu(\iota(a), a)=e)} l = b$$ 
$$c_r:\prod_{(a:A)} \sum_{(r:\mu(a,\iota(a))=e)} \prod_{(r:\mu(a,\iota(a))=e)} r = b$$

## Examples ##

* The [[integers]] are an grouplike $A_3$-space. 

* Every [[loop space]] is naturally an grouplike $A_3$-space with [[path]] concatenation as the operation. In fact every [[loop space]] is a $\infty$-group.

* A [[group]] is a 0-truncated grouplike $A_3$-space. 

## See also ##

* [[higher algebra]]
* [[A3-space]]
* [[group]]