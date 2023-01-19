
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

In [[dependent type theory]], given [[types]] $A$ and $B$ and a [[function type|function]] $x  \colon A \vdash f(x) \colon B$, there is induced a [[dependent function]] between the corresponding [[identity types]]

$$
  a \colon A
  ,\,\;
  b\colon A 
  ,\,\;
  p 
    \,\colon\, 
  a =_A b 
  \;\;\;\vdash\;\;\; 
  \mathrm{ap}_f(a, b)(p)
  \;\colon\;
  f(a) =_B f(b)
$$ 

defined by [[Id-induction]] from 

$$
  ap_f\big(refl_a\big) \,\equiv\, refl_{f(a)}
$$


and called the **application** or **action** of $f$ to/on [[identities]]/[[identifications]]/[[equalities]]/[[paths]] &lbrack;e.g. [UFP (2013, p. 69)](#UFP13), [Rijke (2022, §5.3)](#Rijke22)&rbrack;.

### As the non-dependent version of the dependent function application to identities

The function application to identities is a special case of the [[dependent function application to identities]] for which the type family $x:A \vdash B$ is a constant type family, and thus the [[dependent identity type]] $f(a) =_B^p f(b)$ doesn't depend on the path $p:a =_A b$ and is thus a normal identity type $f(a) =_B f(b)$. 

### Inductive definition

If the function application to identities is inductively defined, then it comes with rules saying that the following judgment can be formed 
$$a:A \vdash \mathrm{ap}_{f}(a, a)(\mathrm{refl}_{A}(a)) \equiv \mathrm{refl}_{B}(f(a)):\Omega(B, f(a))$$
where $\Omega(A, a)$ is the [[loop space type]] $a =_A a$ of $A$ at $a:A$. 

### Binary function applications to identities

Given types $A$, $B$, and $C$ and a [[binary function]] $x:A, y:B \vdash f(x, y):C$, there is a dependent function 
$$a:A, a':A, b:B, b':B, p:a =_A a', q:b =_B b' \vdash \mathrm{apbinary}_f(a, a', b, b')(p, q):f(a, b) =_C f(a', b')$$ 
called the **binary function application to identities** or **binary action on identities** ([Rijke (2022), §19.5](#Rijke22)), inductively defined by 
$$a:A, b:B \vdash \mathrm{apbinary}_{f}(a, a, b, b)(\mathrm{refl}_{A}(a), \mathrm{refl}_{B}(b)) \equiv \mathrm{refl}_{C}(f(a, b)):\Omega(C, f(a, b))$$
where $\Omega(A, a)$ is the [[loop space type]] $a =_A a$ of $A$ at $a:A$. 

Binary function applications to identities are used in proving [[product extensionality]] for [[product types]]. 

### Finitary function application to identities

Let $n$ be a natural number, let $A$ be a family of types indexed by the [[finite type]] with $n$ elements $\mathrm{Fin}(n)$, and let $B$ be a type. Then given a function 
$$n:\mathbb{N}, x:\left(\prod_{i:\mathrm{Fin}(n)} A(i)\right) \vdash f(x):B$$ 
there is a dependent function 
$$n:\mathbb{N}, a:\prod_{i:\mathrm{Fin}(n)} A(i), b:\prod_{i:\mathrm{Fin}(n)} A(i) \vdash \mathrm{ap}_f(n)(a, b):\left(\prod_{i:\mathrm{Fin}(n)} a(i) =_{A(i)} b(i)\right) \to f(a) =_{B} f(b)$$

## See also ##

* [[dependent function application to identities]]

* [[identification]]

* [[identity type]]

## References ##

* {#UFP13} [[Univalent Foundations Project]], §2.2 in: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], §5.3 in: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))


[[!redirects function application to identities]]
[[!redirects function application to identifications]]
[[!redirects function application to paths]]
[[!redirects function application to equalities]]

[[!redirects application of a function to identities]]
[[!redirects application of a function to identifications]]
[[!redirects application of a function to paths]]
[[!redirects application of a function to equalities]]

[[!redirects action on identities]]
[[!redirects action on identifications]]
[[!redirects action on paths]]
[[!redirects action on equalities]]

[[!redirects binary function application to identities]]
[[!redirects binary function application to identifications]]
[[!redirects binary function application to paths]]
[[!redirects binary function application to equalities]]

[[!redirects application of a binary function to identities]]
[[!redirects application of a binary function to identifications]]
[[!redirects application of a binary function to paths]]
[[!redirects application of a binary function to equalities]]

[[!redirects binary action on identities]]
[[!redirects binary action on identifications]]
[[!redirects binary action on paths]]
[[!redirects binary action on equalities]]

[[!redirects happly]]
