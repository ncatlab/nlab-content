
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Given a [[C*-algebra]] $A$ thought of as the [[algebra of observables]] of a [[quantum mechanical system]], write $ComSub(A)$ for its [[poset of commutative subalgebras]]. Then the [[presheaf topos]] over $ComSub(A)$ with its canonical [[spectral presheaf]] as well as the [[presheaf topos]] over the [[opposite category]] $ComSub(A)^{op}$ canonically regarded as a [[ringed topos]] -- the "[[Bohr topos]]", might both be regarded as [[topos theory|topos-theoretic]] incarnations of the [[phase space]] of the given [[quantum mechanical system]]. By standard [[quantum mechanics]] every [[self-adjoint operator]] $a \in A_{sa}$ is to be regarded as an "[[observable]] on phase space", in some sense. Hence one may ask if $a$ induces in a precise sense a function on the phase space [[internalization|internal]] to these toposes.

A construction from each $a \in A_{sa}$ of a [[clopen subset]] $\delta^o(a) \subset \Sigma_A$ of the [[spectral presheaf]] $\Sigma$ of $A$ has been given in ([Isham-D&#246;ring 07](#IshamDoering07)) for [[von Neumann algebras]] $A$. There this is called the "daseinisation" of $a$. An analogous construction for the [[Bohr toposes]] of [[C*-algebras]] has been given in ([Heunen-Landsman-Spitters 09](#HeunenLandsmanSpitters09)). A direct identification of [[quantum observables]] with homorphisms of [[ringed toposes]] out of the Bohr topos is discussed at _[Bohr topos -- The observables](Bohr+topos#TheObservables)_.


## References 

* [[Andreas Döring]], [[Chris Isham]], _A Topos Foundation for Theories of Physics_  ([arXiv:quant-ph/0703060](http://arxiv.org/abs/quant-ph/0703060), [arXiv:quant-ph/0703062](http://arxiv.org/abs/quant-ph/0703062), [arXiv:quant-ph/0703066](http://arxiv.org/abs/quant-ph/0703066))
  {#IshamDoering07}

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _A Topos for Algebraic Quantum Theory_ Communications in Mathematical Physics 291. 63-110. 2009
  {#HeunenLandsmanSpitters09}


[[!redirects daseinisation]]
[[!redirects daseinization]]
