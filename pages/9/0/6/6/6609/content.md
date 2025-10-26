
> This is about tensor quantities in the sense of [[multilinear algebra]], [[differential geometry]] and [[physics]], as in [[tensor calculus]]. For the different notion of a tensor in [[enriched category theory]] see under _[[copower]]_. 

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition


Generally, a _tensor_ is an [[element]] of a [[tensor product]].

Traditionally this is considered in [[differential geometry]] for the following case:

for $X$ a [[manifold]], $T X$ the [[tangent bundle]], $T^* X$ the [[cotangent bundle]], $\Gamma(T X)$, $\Gamma(T^* X)$ their [[spaces of sections]] and $C(X)$ the [[associative algebra]] of [[functions]] on $X$, a **[[rank]]-$(p,q)$ tensor** or **tensor field** on $X$ is an element of the [[tensor product of modules]] over $C(X)$

$$
  t \in \Gamma(T X)^{\otimes_{C(X)}^p} \otimes_{C(X)} \Gamma(T^* X)^{\otimes^q_{C(X)}}
  \,.
$$

A rank $(p,0)$-tensor is also called a **covariant tensor** and a rank $(0,q)$-tensor a **contravariant tensor**. 

## Examples

### General

(...)

### In differential geometry

* A [[vector field]] is a rank $(1,0)$-tensor field.

* A [[Riemannian metric]] is a symmetric rank $(0,2)$-tensor.

* A [[differential form]] of  degree $n$ is a skew-symmetric rank $(0,n)$-tensor.

* A [[Poisson tensor]] is a skew-symmetric tensor of rank $(2,0)$.


## Related concepts

* [[tensor calculus]], [[tensor network]], [[string diagram]]

* [[decomposable tensor]]

* [[field (physics)]]

* [[hypermatrix]]

## References

Historical discussion:

* [[Élie Cartan]] (translated by Vladislav Goldberg from Cartan's lectures at the Sorbonne in 1926–27): Chapter 8 of: *Riemannian Geometry in an Orthogonal Frame*, World Scientific (2001) &lbrack;[doi:10.1142/4808](https://doi.org/10.1142/4808), [pdf](https://softbank.iust.ac.ir/MathBooks/c/Cartan%20-%20Riemannian%20Geometry%20in%20an%20Orthogonal%20Frame.pdf)&rbrack;

Textbook account aimed at [[physics|physicists]]:

* [[Helmut Eschrig]], section 4 of: *Topology and Geometry for Physics*, Lecture Notes in Physics, Springer (2011) \[<a href="https://doi.org/10.1007/978-3-642-14700-5">doi:10.1007/978-3-642-14700-5</a>\] 


Monograph:

* Joseph M. Landsberg: *Tensors: Geometry and Applications* (2011) &lbrack;ISBN:978-0-8218-6907-9, [ams:gsm-128](https://bookstore.ams.org/gsm-128)&rbrack;

Discussion with an eye towards application in ([[particle physics|particle]]) [[physics]]:

* [[Theodore Frankel]], section 2.4 in: _[[The Geometry of Physics - An Introduction]]_

* [[Howard Georgi]], §10  in: *Lie Algebras In Particle Physics*, Westview Press (1999), CRC Press (2019) &lbrack;[doi:10.1201/9780429499210](https://doi.org/10.1201/9780429499210)&rbrack;





[[!redirects tensors]]

[[!redirects tensor field]]
[[!redirects tensor fields]]

[[!redirects covariant tensor]]
[[!redirects contravariant tensor]]
[[!redirects covariant tensors]]
[[!redirects contravariant tensors]]

