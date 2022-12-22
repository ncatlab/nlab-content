+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The [[type theory|type-theoretic]] version of the fact that in [[set theory]] [[functions]] preserve [[equality]] between [[elements]] in [[sets]]. 

## Definition ##

In [[Martin-Löf type theory]], given [[types]] $A$ and $B$ and a [[function]] $x:A \vdash f(x):B$, there is a dependent [[function]] 
$$a:A, b:A, p:a =_A b \vdash \mathrm{ap}_f(a, b)(p):f(a) =_B f(b)$$ 
called the **action on [[identifications]]/[[identities]]/[[equalities]]/[[paths]] of $f$** or the **application of $f$ to identifications/identities/equalities/paths**, inductively defined by 
$$a:A \vdash \mathrm{ap}_{f}(a, a)(\mathrm{refl}_{A}(a)) \equiv \mathrm{refl}_{B}(f(a)):\Omega(B, f(a))$$
where $\Omega(A, a)$ is the [[loop space type]] $a =_A a$ of $A$ at $a:A$. 

### Binary actions on identities

Given types $A$, $B$, and $C$ and a [[binary function]] $x:A, y:B \vdash f(x, y):C$, there is a dependent function 
$$a:A, a':A, b:B, b':B, p:a =_A a', q:b =_B b' \vdash \mathrm{apbinary}_f(a, a', b, b')(p, q):f(a, b) =_C f(a', b')$$ 
called the **binary action on identities**, inductively defined by 
$$a:A, b:B \vdash \mathrm{apbinary}_{f}(a, a, b, b)(\mathrm{refl}_{A}(a), \mathrm{refl}_{B}(b)) \equiv \mathrm{refl}_{C}(f(a, b)):\Omega(C, f(a, b))$$
where $\Omega(A, a)$ is the [[loop space type]] $a =_A a$ of $A$ at $a:A$. 

Binary actions on identities are used in proving [[product extensionality]] for [[product types]]. 

### Finitary actions on identities

Let $n$ be a natural number, let $A$ be a family of types indexed by the [[finite type]] with $n$ elements $\mathrm{Fin}(n)$, and let $B$ be a type. Then given a function 
$$n:\mathbb{N}, x:\left(\prod_{i:\mathrm{Fin}(n)} A(i)\right) \vdash f(x):B$$ 
there is a dependent function 
$$n:\mathbb{N}, a:\prod_{i:\mathrm{Fin}(n)} A(i), b:\prod_{i:\mathrm{Fin}(n)} A(i) \vdash \mathrm{ap}_f(n)(a, b):\left(\prod_{i:\mathrm{Fin}(n)} a(i) =_{A(i)} b(i)\right) \to f(a) =_{B} f(b)$$

## See also ##

* [[identification]]
* [[identity type]]

## References ##

* [[Univalent Foundations Project]], [[Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

Binary actions on paths were defined in section 19.5 of:

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

[[!redirects action on identifications]]
[[!redirects action on paths]]
[[!redirects action on identities]]
[[!redirects action on equalities]]

[[!redirects application of a function to identifications]]
[[!redirects application of a function to paths]]
[[!redirects application of a function to identities]]
[[!redirects application of a function to equalities]]

[[!redirects binary action on identifications]]
[[!redirects binary action on paths]]
[[!redirects binary action on identities]]
[[!redirects binary action on equalities]]
