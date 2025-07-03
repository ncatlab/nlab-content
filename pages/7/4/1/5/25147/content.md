
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], given types $A$ and $B$ and a family of elements $x:A \vdash f(x):B$, the [[function application to identifications]] for $f(x)$ is the family of elements
$$a:A, b:A, p:a =_A b \vdash \mathrm{ap}_f(a, b, p):f(a) =_B f(b)$$ 

A dependent function application to identifications is like an function application to identifications, but hwere we allow $B$ to depend on $x:A$ and similarly the [[identity type]] $f(a) =_B f(b)$ to be a [[indexed heterogeneous identity type]] and depend on the identification $p:a =_A b$. 

## Definition

In [[dependent type theory]], given a type $A$ and a type family $x:A \vdash B(x)$ and a family of elements $x:A \vdash f(x):B(x)$, the **dependent function application to identifications** or **dependent action on identifications** for $f(x)$ is the family of elements
$$a:A, b:A, p:a =_A b \vdash \mathrm{apd}_f(a, b, p):\mathrm{hId}_{B}(a, b, p, f(a), f(b))$$ 
inductively defined by 
$$a:A \vdash \mathrm{apd}_f(a, a, \mathrm{refl}_A(a)) \coloneqq \mathrm{hrefl}_A(a, f(a)):\mathrm{hId}_{B}(a, a, \mathrm{refl}_A(a), f(a), f(a))$$ 
where $\mathrm{hId}_{B}(a, b, p, f(a), f(b))$ is a [[indexed heterogeneous identity type]]. 

### Using functions from the interval type

If dependent identification types are defined in terms of function types from the interval type; i.e. 
$$p:\mathbb{I} \to A, x:B(p(0)), y:B(p(1)) \vdash \mathrm{apd}_f(p):\mathrm{hId}_{B}(p, x, y)$$
then dependent function application is defined slightly differently. 

By the recursion rule of the [[interval type]], one could use a function $p:\mathbb{I} \to A$ instead of elements $a:A$, $b:A$, and identification $p:a =_A b$. Then given a type $A$ and a type family $x:A \vdash B(x)$ and a family of elements $x:A \vdash f(x):B(x)$, the **dependent function application to identifications** or **dependent action on identifications** for $f(x)$ is the family of elements
$$p:\mathbb{I} \to A \vdash \mathrm{apd}_f(p):\mathrm{hId}_{B}(p, f(p(0)), f(p(1)))$$ 
inductively defined using the induction principle of the path type $\mathbb{I} \to A$ by 
$$a:A \vdash \mathrm{apd}_f(\lambda i:\mathbb{I}.a) \coloneqq \mathrm{hrefl}_A(a, f(a)):\mathrm{hId}_{B}(\lambda i:\mathbb{I}.a, f(a), f(a))$$ 

### Using transport

In addition, there are two other families of elements which could be considered dependent function applications to identifications, which use [[transport]] and the inverse of transport rather than indexed heterogeneous identity types:

$$a:A, b:A, p:a =_A b \vdash \mathrm{apdl}_f(a, b, p):f(a) =_{B(a)} \mathrm{tr}_B(a, b, p)^{-1}(f(b))$$ 
$$a:A, b:A, p:a =_A b \vdash \mathrm{apdr}_f(a, b, p):\mathrm{tr}_B(a, b, p)(f(a)) =_{B(b)} f(b)$$ 

Having one of the three notions of dependent function application to identifications means that one could define all three of them, because the types $f(a) =_B^p f(b)$, $f(a) =_{B(a)} \mathrm{tr}_B(a, b, p)^{-1}(f(b))$, and $\mathrm{tr}_B(a, b, p)(f(a)) =_{B(b)} f(b)$ are all [[equivalence of types|equivalent]] to each other. 

## For identifications of arbitrary arity

One can also consider dependent function application to [[identification#OfArbitraryArity|identifications of arity]] $I$, $p:\mathrm{Id}_{I, A}(\overline{x})$, given a family of elements $\overline{x}:I \to A$ indexed by type $I$. We have, for a dependent function $f:\prod_{x:A} B(x)$, a reflexive family 

$$x:A \vdash \mathrm{hrefl}_{I, A, B}(x, f(x)):\mathrm{hId}_{I, A, B}(\lambda t.x, \mathrm{refl}_{I, A}(x), \lambda t.f(x))$$

and thus by [[identification induction]] of the [[indexed heterogeneous identity type#OfArbitraryArity|indexed heterogeneous identity type of arity]] $I$, we have a function 

$$\mathrm{apd}_{I, A, B}(f, \overline{x}):\prod_{p:\mathrm{Id}_{I, A}(\overline{x})} \mathrm{Id}_{I, B}(\overline{x}, p, \lambda t.f(\overline{x}(t)))$$

called the **application** of the dependent function $f$ to identifications of arity $I$ or the **action** of dependent function $f$ on identifications of arity $I$, such that for all $x:A$, 

$$\mathrm{apd}_{I, A, B}(f, \overline{x}, \mathrm{refl}_{I, A}(x)) \equiv \mathrm{hrefl}_{I, A, B}(x, f(x)):\mathrm{hId}_{I, A, B}(\lambda t.x, \mathrm{refl}_{I, A}(x), \lambda t.f(x))$$

## Related concepts

* [[dependent function]]
* [[dependent function application]]
* [[function application to identifications]]
* [[identity type]]
* [[indexed heterogeneous identity type]]
* [[bridge type]]
* [[indexed heterogeneous bridge type]]
* [[higher inductive type]]
* [[equivalence type]]
* [[transport]]

## References

* {#UFP13} [[Univalent Foundations Project]], §2.3 in: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], §5.4 in: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

For dependent function application to [[bridges]] in [[Narya]], see

* *Observational higher dimensions*, [[Narya]] documentation. ([web](https://narya.readthedocs.io/en/latest/observational.html)) 

[[!redirects dependent function application to identities]]
[[!redirects dependent function application to identifications]]
[[!redirects dependent function application to paths]]
[[!redirects dependent function application to equalities]]

[[!redirects application of a dependent function to identities]]
[[!redirects application of a dependent function to identifications]]
[[!redirects application of a dependent function to paths]]
[[!redirects application of a dependent function to equalities]]

[[!redirects dependent action on identities]]
[[!redirects dependent action on identifications]]
[[!redirects dependent action on paths]]
[[!redirects dependent action on equalities]]