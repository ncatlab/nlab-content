
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Idea
 {#Idea}

In ([[dependent type theory|dependent]]) [[type theory]] and in particular in [[homotopy type theory]], two [[types]] $D$, $C$ are called (homotopy-)*[[isomorphism|isomorphic]]* 

> &lbrack;[Rittri (1989)](#Rittri89), [Cosmo (1995, §1.8)](#Cosmo95), [Hofmann & Streicher (1998, §5.4)](#HofmannStreicher98), [Kapulkin & Lumsdaine (2012, 2021, Def. 3.1.1)](#KapulkinLumsdaine21), but see [below](#HistoricalNote)&rbrack; 

or *[[equivalence|equivalent]]* &lbrack;[UFP13, §4](#UFP13)&rbrack; (for fine-print see the definitions [below](#Definition)) if there exists a transformation $D \to C$ which may be [[inverse|inverted]] (up to the relevant re-[[identification type|indentifications]]), hence if any program operating on data of type $A$ may be transformed into a program operating on data of type $B$, and vice versa (see practical examples referenced [below](#ApplicationsInProofReuse)).


Alternatively, a [[function type|function]] $D \to C$ may be called a *[[bijection]]* if all its [[pre-images]] are essentially unique, namely if all its [[fiber types]] are [[contractible types]]. In the [[categorical semantics]] this is called a *[[weak homotopy equivalence]]*, whence this term is also used for the type-theoretic notion &lbrack;[Voevodsky (2010), p. 8, 10](#Voevodsky10)&rbrack;.

<img src="https://ncatlab.org/nlab/files/TypeEquivalence-230128b.jpg" width="800">

These two notions are in fact equivalent &lbrack;[UFP13, around Thm. 4.4.5](#UFP13)&rbrack;.

<img src="https://ncatlab.org/nlab/files/TypeBijectionIsEquivalence-230128.jpg" width="750">


In the special case of [[0-truncated]] types ([[h-sets]]), hence in [[dependent type theories]] with *[[axiom K]]* or the axiom imposing *[[uniqueness of identity proofs]]*, the notion of  type equivalence corresponds essentially to the notion of *[[bijection]]* or *[[one-to-one correspondence]]* in [[set theory]]. 

In the special case of [[1-truncated]] types ([[h-groupoids]]), type equivalence corresponds essentially to the notion of *[[equivalence of groupoids]]* in [[category theory]].

In full [[homotopy type theory]] the [[categorical semantics]] of type equivalence is *[[homotopy equivalence]]* and that of type bijection is *[[weak homotopy equivalence]]*. That these notions coincide corresponds to the [[categorical semantics]] of types being as [[cofibrant object|co]]-/[[fibrant objects]], on which [[weak homotopy equivalences]] coincide with [[homotopy equivalences]] (by the [[Whitehead theorem]]).

Finally, the notion of equivalence/bijection of types is *a priori* different from that of *[[identification type|identification]]* of types in the [[type universe]]. To assert that the two notions do agree after all is to impose the [[univalence axiom]].


## Definitions
 {#Definition}

In [[dependent type theory]], a [[type]] $A$ is a [[contractible type]] if it comes with an element $a:A$ and a family of identities $x:A \vdash c(x):a =_A x$ indicating that $a$ is a [[center of contraction]]. A type family $x:A \vdash B(x)$ is [[uniquely quantified]] if the [[dependent sum type]] $\sum_{x:A} B(x)$ is a [[contractible type]]. In dependent type theory with [[identity types]] and [[dependent sum types]], an **equivalence** between types $A$ and $B$ could be defined as

* a [[function]] with contractible fibers, a family of elements $x:A \vdash f(x):B$ for which the type family $x:A \vdash f(x) =_B y$ is [[uniquely quantified]] for all $y:B$
* a [[span]] $(C; z:C \vdash g(z):A; z:C \vdash h(z):B)$ for which the type family $z:C \vdash g(z) =_A x$ is [[uniquely quantified]] for all $x:A$ and the type family $z:C \vdash h(z) =_B y$ is [[uniquely quantified]] for all $y:B$
* a [[multivalued partial function]] $(x:A \vdash P(x); x:A, p:P(x) \vdash f(x, p):B)$ for which the dependent type $P(x)$ is a [[contractible type]] for all $x:A$ and the type family $x:A \vdash \sum_{p:P(x)} f(x, p) =_B y$ is [[uniquely quantified]] for all $y:B$
* a [[one-to-one correspondence]], a [[correspondence]] $x:A, y:B \vdash R(x, y)$ for which the type family $y:B \vdash R(x, y)$ is [[uniquely quantified]] for all $x:A$ and the type family $x:A \vdash R(x, y)$ is [[uniquely quantified]] for all $y:B$
* an element of the [[equivalence type]] $f:A \simeq B$, in dependent type theories with [[equivalence types]] given directly by rules. 
* a *bi-invertible function* or *homotopy isomorphism*, a family of elements $x:A \vdash f(x):B$ with families of elements $y:B \vdash g(y):A$ and $y:B \vdash h(y):A$ and families of identities $x:A \vdash G(x):g(f(x)) =_A x$ and $y:B \vdash H(y):f(h(y)) =_B y$. 
* a *coherently invertible function* or *half adjoint equivalence*, a family of elements $x:A \vdash f(x):B$ with a family of elements $y:B \vdash g(y):A$ and families of identities $x:A \vdash G(x):g(f(x)) =_A x$; $y:B \vdash H(y):f(g(y)) =_B y$; and $x:A \vdash K(x):\mathrm{ap}_f(H(x)) =_{g(f(x)) =_A x} G(f(x))$. 
* a *quasi-invertible function* or *homotopy equivalence*, a family of elements $x:A \vdash f(x):B$ with a family of elements $y:B \vdash g(y):A$ and families of identities $x:A \vdash G(x):g(f(x)) =_A x$ and $y:B \vdash H(y):f(g(y)) =_B y$. 
* A function $f:A \to B$ which satisfies [[copy induction]], which makes the type $B$ satisfy the [[universal property]] of a [[copy]] of $A$. 

### The isEquiv type family and equivalence types

{#OutlookOnEquivalenceOfDefinitions} As (eventually to be) discussed in the *[Properties](#Properties)*-section below,
the evident types formed by these definitions are co-inhabited: we have a function from any one of them to any of the others.  Moreover, at least if we assume [[function extensionality]], the evident types of "homotopy isomorphisms" and of functions with contractible fibers are equivalent and are [[h-propositions]].
This is only true for the evident type of homotopy equivalences if we assume [[axiom K]] or [[uniqueness of identity proofs]] (as discussed [below](#TheIssueWithQuasiInverses)); in [[dependent type theories]] without either axiom, the isEquiv type family is not in general a [[mere proposition]] for homotopy equivalences. However, often the most convenient way to show that $f$ is an equivalence is by exhibiting it as a term of the type of homotopy equivalences.

#### Rules for isEquiv

Given types $A$ and $B$ and [[function]] $f:A \to B$, $f$ is an [[equivalence of types]] if $f$ has a [[quasi-inverse function]] and $B$ satisfies the [[universal property]] of a [[copy type]] of $A$ with copy function $f:A \to B$. This means that one could define the family of [[h-propositions]] $f:A \to B \vdash \mathrm{isEquiv}(f)$ using very similar natural deduction rules to the rules for [[copy types]], but where the [[introduction rule]] states that given a function $f:A \to B$ and evidence that $f$ has a quasi-inverse function, one could form a witness of $\mathrm{isEquiv}(f)$:

Defining 

$$f:A \to B \vdash \mathrm{qInv}(f) \equiv \sum_{g:B \to A} \left(\prod_{y:B} \mathrm{Id}_B(f(g(y)), y)\right) \times \left(\prod_{x:A} \mathrm{Id}_A(g(f(x)), x)\right)$$

and 

$$\mathrm{isProp}(A) \equiv \prod_{x:A} \prod_{y:A} x =_A y$$

the formation and introduction rules for isEquiv state that that the type family $f:A \to B \vdash \mathrm{isEquiv}(f)$ comes with 

* a family of functions 
$$f:A \to B \vdash \mathrm{qinvtoisEquiv}(f):\mathrm{qInv}(f) \to \mathrm{isEquiv}(f)$$

* a family of identifications
$$f:A \to B \vdash \mathrm{proptruncisEquiv}(f):\mathrm{isProp}(\mathrm{isEquiv}(f))$$

Formation rules for isEquiv:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B}{\Gamma \vdash \mathrm{isEquiv}(f) \; \mathrm{type}}$$

Introduction rules for isEquiv:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B}{\Gamma \vdash \mathrm{qInvToIsEquiv}(f):\mathrm{qInv}(f) \to \mathrm{isEquiv}(f)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B}{\Gamma \vdash \mathrm{proptruncisEquiv}(f):\mathrm{isProp}(\mathrm{isEquiv}(f))}$$

The elimination, computation, and uniqueness rules depend upon whether $B$ behaves like a [[positive copy type]] or a [[negative copy type]]:

##### As a negative type

Elimination rules for isEquiv:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B}{\Gamma \vdash f^{-1}:B \to A}$$

Computation rules for isEquiv:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B}{\Gamma, y:B \vdash \beta_{\mathrm{isEquiv}(f)}(y):f(f^{-1}(y)) =_B y}$$

Uniqueness rules for isEquiv:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash f:A \to B}{\Gamma, x:A \vdash \eta_{\mathrm{isEquiv}(f)}(x):f^{-1}(f(x)) =_A x}$$

Using [[dependent sum types]] and [[product types]], this could be reduced to the following inference rule

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \to B \vdash \mathrm{isEquivtoqinv}(f):\mathrm{isEquiv}(f) \to \mathrm{qInv}(f)}$$

##### As a positive type

Elimination rules for isEquiv:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \\
      \Gamma, y:B \vdash C(y) \; \mathrm{type} \quad \Gamma \vdash c_f:\prod_{x:A} C(f(x)) \quad \Gamma \vdash b:B
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(f, p, c_f, b):C(b)}$$

Computation rules for isEquiv:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \\
      \Gamma, y:B \vdash C(y) \; \mathrm{type} \quad \Gamma \vdash c_f:\prod_{x:A} C(f(x)) \quad \Gamma \vdash a:A
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{isEquiv}(f)}(f, p, c_f, a):\mathrm{ind}_{\mathrm{isEquiv}(f)}^C(f, p, c_f, f(a)) =_{C(f(a))} c_f(a)}$$

Uniqueness rules for isEquiv:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, f:A \to B \quad \Gamma \vdash p:\mathrm{isEquiv}(f) \\
      \Gamma, y:B \vdash C(y) \; \mathrm{type} \quad \Gamma \vdash c:\prod_{y:B} C(y) \quad \Gamma \vdash b:B
    \end{array}
  }{\Gamma \vdash \eta_{\mathrm{isEquiv}(f)}(f, p, c, b):c(b) =_{C(b)} \mathrm{ind}_{\mathrm{isEquiv}(f)}^C(f, p, c, b)}$$

#### Defining isEquiv from other type formers

In dependent type theories with [[dependent product types]], the [[isContr]] modality is defined as
$$\mathrm{isContr}(A) \coloneqq \sum_{x:A} \prod_{y:A} x =_A y$$
and the [[uniqueness quantifier]] on a type family $x:A \vdash B(x)$, is defined as 
$$\exists!x:A.B(x) \coloneqq \mathrm{isContr}\left(\sum_{x:A} B(x)\right)$$

Assuming [[function extensionality]], one could define $\mathrm{isEquiv}$ type family and the [[equivalence type]] for the first and fifth definition:

* We define the property that a function $f:A \to B$ is an equivalence as the property that the function has contractible fibers:
$$f:A \to B \vdash \mathrm{isEquiv}(f) \coloneqq \prod_{y:B} \exists!x:A.f(x) =_B y$$
  and the [[equivalence type]] for the first definition: 
$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}(f)$$

* We define the property that an equivalence $f:A \simeq B$ is an equivalence as true, represented in dependent type theory by the [[unit type]], because $f:A \simeq B$ is always an equivalence:
$$f:A \simeq B \vdash \mathrm{isEquiv}(f) \coloneqq \mathbb{1}$$
  and there is no need to define $A \simeq B$ because the type is already defined. However, there is an equivalence between the types
$$\delta:(A \simeq B) \simeq \sum_{f:A \simeq B} \mathrm{isEquiv}(f)$$

If the dependent type theory came with a [[Tarski universe]] $(U, \mathrm{El})$, one could additionally define the $\mathrm{isEquiv}_U$ type family and the locally $U$-small [[equivalence type]] for the second, third, and fourth definitions above, but only for $U$-small structures:

* The type of $U$-small [[spans]] between $A$ and $B$ is the type
$$\mathrm{Span}_U(A, B) \coloneqq \sum_{C:U} (\mathrm{El}(C) \to A) \times (\mathrm{El}(C) \to B)$$
We define the property that a $U$-small span $f:\mathrm{Span}_U(A, B)$ is an equivalence as the property that both functions $\pi_1(\pi_2(f)):\mathrm{El}(C) \to A$ and $\pi_2(\pi_2(f)):\mathrm{El}(C) \to B$ have contractible fibers:
$$f:\mathrm{Span}_U(A, B) \vdash \mathrm{isEquiv}_U(f) \coloneqq \left(\prod_{x:A} \exists!z:\mathrm{El}(C).\pi_1(\pi_2(f))(z) =_A x\right) \times \left(\prod_{y:B} \exists!z:\mathrm{El}(C).\pi_2(\pi_2(f))(z) =_B y\right)$$
The locally $U$-small [[equivalence type]] is defined as
$$A \simeq_U B \coloneqq \sum_{f:\mathrm{Span}_U(A, B)} \mathrm{isEquiv}(f)$$

* The type of $U$-small [[multivalued partial functions]] between $A$ and $B$ is the type
$$\mathrm{MultiPartFunc}_U(A, B) \coloneqq \sum_{P:A \to U} \left(\sum_{x:A} \mathrm{El}(P(x))\right) \to B$$
We define the property that a $U$-small multivalued partial function $f:\mathrm{MultiPartFunc}_U(A, B)$ is an equivalence as the property that the dependent type $\mathrm{El}(\pi_1(f)(x))$ is a [[contractible type]] for all $x:A$ and the function $\pi_2(f)$ has contractible fibers for all $y:B$:
$$f:\mathrm{MultiPartFunc}_U(A, B) \vdash \mathrm{isEquiv}_U(f) \coloneqq \left(\prod_{x:A} \mathrm{isContr}\left(\mathrm{El}(\pi_1(f)(x))\right)\right) \times \left(\prod_{y:B} \exists!x:A.\sum_{p:\mathrm{El}(\pi_1(f)(x))} \pi_2(f)(x, p) =_B y\right)$$
The locally $U$-small [[equivalence type]] is defined as
$$A \simeq_U B \coloneqq \sum_{f:\mathrm{MultiPartFunc}_U(A, B)} \mathrm{isEquiv}(f)$$

* The type of $U$-small [[correspondences]] between $A$ and $B$ is the type 
$$\mathrm{Corr}_U(A, B) \coloneqq A \times B \to U$$
We define the property that a $U$-small correspondence $R:\mathrm{Corr}_U(A, B)$ is an equivalence as being a [[one-to-one correspondence]]:
$$R:\mathrm{Corr}_U(A, B) \vdash \mathrm{isEquiv}_U(R) \coloneqq \left(\prod_{x:A} \exists!y:B.\mathrm{El}(R(x,y))\right) \times \left(\prod_{y:B} \exists!x:A.\mathrm{El}(R(x,y))\right)$$
The locally $U$-small [[equivalence type]] is defined as
$$A \simeq_U B \coloneqq \sum_{f:\mathrm{Corr}_U(A, B)} \mathrm{isEquiv}(f)$$

If the dependent type theory also has [[function extensionality]], then one could define the $\mathrm{isEquiv}$ type family and the [[equivalence type]] for the sixth and seventh definitions above:

* For homotopy isomorphisms, given a function $f:A \to B$, we define the $\mathrm{isEquiv}(f)$ type family as the product type of the type of [[sections]] of $f$ and the type of [[retractions]] of $f$. 
$$f:A \to B \vdash \mathrm{isEquiv}(f) \coloneqq \left(\sum_{g:B \to A} \prod_{x:A} g(f(x)) =_A x\right) \times \left(\sum_{h:B \to A} \prod_{y:B} f(h(y)) =_B y\right)$$
* For half adjoint equivalences, given a function $f:A \to B$, we define the $\mathrm{isEquiv}(f)$ type family as the type of quasi-inverse functions with a coherence condition. 
$$f:A \to B \vdash \mathrm{isEquiv}(f) \coloneqq \sum_{g:B \to A} \sum_{H:\prod_{x:A} g(f(x)) =_A x} \sum_{G:\prod_{y:B} f(g(y)) =_B y} \prod_{x:A} \mathrm{ap}_f(H(x)) =_{g(f(x)) =_A x} G(f(x))$$
* For invertible functions, given a function $f:A \to B$, we define the $\mathrm{isEquiv}(f)$ type family as the proposition that the function merely has a [[quasi-inverse function]]:
$$f:A \to B \vdash \mathrm{isEquiv}(f) \coloneqq \exists g:B \to A.(\Pi x:A.g(f(x)) =_A x) \times (\Pi y:B.f(g(y)) =_B y)$$
  and the [[equivalence type]] for the first definition: 
$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}(f)$$

Finally, if the dependent type theory has [[axiom K]] or [[uniqueness of identity proofs]], then one could define the $\mathrm{isEquiv}$ type family and the [[equivalence type]] directly for homotopy equivalences above; the coherence condition follows from the fact that the type $g(f(x)) =_A x$ is always a [[mere proposition]] in the presence of axiom K or UIP:
$$f:A \to B \vdash \mathrm{isEquiv}(f) \coloneqq \sum_{g:B \to A} \left(\prod_{x:A} g(f(x)) =_A x\right) \times \left(\prod_{y:B} f(g(y)) =_B y\right)$$

In all three cases, by [[function extensionality]] for the first two and additionally by [[axiom K]] or [[UIP]] for the third case, the $\mathrm{isEquiv}(f)$ type family is a [[mere proposition]] for all $f:A \to B$. Thus, we can define the [[equivalence type]] as 
$$A \simeq B \coloneqq \sum_{f:A \to B} \mathrm{isEquiv}(f)$$

### Historical note
 {#HistoricalNote}

The first attempt at a definition of an equivalence of type was the definition of a quasi-invertible function by [Hofmann & Streicher (1998), §5.4](#HofmannStreicher98). In the absence of [[axiom K]] or [[uniqueness of identity proofs]], this definition suffers from a subltety in the construction of equivalence types, see [below](#TheIssueWithQuasiInverses). 

Later on, the following definitions of equivalences were constructed: 

* as a function with contractible fibers, first proposed by [Voevodsky (2010), p. 8, 10](#Voevodsky10)

* as a homotopy isomorphism, first proposed by [[André Joyal]] in a 2011 Oberwolfach meeting, recorded in [Kapulkin & Lumsdaine (2012, 2021), Def. 3.1.1](#KapulkinLumsdaine21), 

* as a one-to-one correspondence, first proposed in [Shulman 2022](#Shulman22)

However, these definitions are only equivalent to one another in the presence of [[function extensionality]].

## Properties
 {#Properties}

\linebreak

Most of the following claims may be found proven in [UFP13, §2.4 & §4](#UFP13).

### Functions with contractible fibers and one-to-one correspondences

We define an [[anafunction]] to be a type family $R :A \times B \to \mathcal{U}$ with a witness

$$p:\prod_{a:A} \exists!b:B.R(a,b)$$

The [[principle of unique choice]] holds in [[dependent type theory]]. This means that given any anafunction $R :A \times B \to \mathcal{U}$, there is function $f:A \to B$. Similarly, for any function $f:A \to B$, there is an anafunction $R :A \times B \to \mathcal{U}$ defined by $R(a,b) \coloneqq f(a) =_B b$. 

A function with contractible fibers comes with a witness 

$$q:\prod_{b:B} \exists!a:A.f(a) =_A b$$

while an one-to-one correspondence is an anafunction which comes with a witness 

$$q:\prod_{b:B} \exists!a:A.R(a, b)$$

Since we established that the types $f(a) =_A b$ and $R(a, b)$ are the same for function $f$ and anafunction $R$, functions with contractible fibers are equivalent to one-to-one correspondences. 

### The issue with two-sided quasi-inverses
 {#TheIssueWithQuasiInverses}

The definition of equivalences as two-sided [[quasi-inverse functions]] (Def. \ref{FunctionWithTwoSidedInverse}) suffers from the drawback that the type 

$$
  f \colon A \to B
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  qinv(f)
  \coloneqq
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
  \,,
$$

which may naively look like it merely detects whether $f$ is an equivalence, is in fact *not* a [[mere proposition]] ([UFP13, Thm. 4.1.3](#UFP13)).

This means that the type

\[
  \label{TheSubtlyWrongTypeOfEquivalences}
  \underset{
    f \colon A \to B
  }{\sum}  
  \;
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
\]

is --- despite its possible superficial appearance (cf. &lbrack;[Hofmann & Streicher (1998),  §5.4](#HofmannStreicher98)&rbrack;) -- *not* in fact equivalent to the correct type of equivalences $Equiv(A,B)$, which is instead obtained from this expression by including a [[0-truncation]] $[-]_{0}$:

$$
  Equiv(A,B)
  \;\simeq\;
  \underset{
    f \colon A \to B
  }{\sum}  
  \Bigg[
  \underset{
    \overline{f} \colon B \to A
  }{\sum}
  \;\;
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
  \Bigg]_0
  \,.
$$

\linebreak

One could also use [[propositional truncations]] instead of [[0-truncation]]; this turns the [[dependent sum type]] in the definition into an [[existential quantifier]], and is the proper translation of one of the definitions of [[bijection]] in [[set theory]] into type theory in the [[propositions as some types]]: A function $f:A \to B$ is an equivalence if there (merely) exists a function $\overline{f}:B \to A$ such that $\overline{f} \circ f$ is equal to $(a \mapsto a)$ and $f \circ \overline{f}$ is equal to $(b \mapsto b)$:

$$
  Equiv(A,B)
  \;\simeq\;
  \underset{
    f \colon A \to B
  }{\sum}  
  \exists \overline{f} \colon B \to A.
  Id_{(A \to A)}
  \big(
    \overline{f} \circ f 
    ,\,
    (a \mapsto a)
  \big)
  \;\times\;
  Id_{(B \to B)}
  \big(
    f \circ \overline{f} 
    ,\,
    (b \mapsto b)
  \big)
  \,.
$$

### Constructing the inverse function
 {#ConstructingTheInverseFunction}

For every function $f \colon A \to B$ with contractible fibers (Def. \ref{FunctionWithContractibleFiber}), 
there exists a function $g \colon B \to A$ which is an [[inverse function]]. 

The [[principle of unique choice]] implies that given a function $f:A \to B$, if for all $b:B$ the fiber of $f$ at $b$ is contractible, then for all $b:B$ there is an element $g(b):\mathrm{fiber}(f, b)$. 

$$\prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} f(a) =_A b\right) \to \prod_{b:B} \sum_{a:A} f(a) =_A b$$

The [[type theoretic axiom of choice]] then states that for all elements $b:B$ one has the structure of an element $a:A$ such that $f(a) =_A b$, then one has a function $g:B \to A$ such that $f(g(b)) =_A b$. 

$$\prod_{b:B} \sum_{a:A} f(a) =_A b \to \sum_{g:B \to A} \prod_{b:B} f(g(b)) =_A b$$

There is also another definition of contractible type, which uses the notion of [[center of contraction]]; namely, that a type $A$ is a contractible type if it comes with a element $a:A$ and a witness that for all elements $b:A$, $a =_A b$

$$\prod_{b:A} a =_A b$$

Since the fiber of $f$ at $b$ is contractible, $g(b)$ is the [[center of contraction]] for the fiber of $f$ at $b$. 

Thus, for all elements $a:A$ and $b:B$ and a witness $q(a, b):f(a) =_B b$, there is a witness $r(a, b, q(a, b)):a =_A g(b)$. Since the type $a =_A g(b)$ doesn't depend on $q(a, b)$, by the rules of [[function types]], the latter condition is the same as for all elements $a:A$ and $b:B$, a function $r(a, b):f(a) =_B b \to a =_A g(b)$. 

...

still to prove: that the function above is an equivalence of types for all $a:A$ and $b:B$. 

## Semantics
 {#Semantics}

We discuss the [[categorical semantics]] of equivalences in homotopy type theory.

Let $\mathcal{C}$ be a [[locally cartesian closed category]] which is a [[model category]], in which the (acyclic cofibration, fibration) [[weak factorization system]] has [[stable path objects]], and acyclic cofibrations are preserved by pullback along fibrations between fibrant objects.  (We ignore questions of coherence, which are not important for this discussion.) For instance $\mathcal{C}$ could be a [[type-theoretic model category]].

### Of $isEquiv(-)$

+-- {: .num_prop }
###### Proposition

For $A, B$ two [[cofibrant object|cofibrant]]-[[fibrant objects]] in $\mathcal{C}$,
a morphism $f\colon A\to B$ is a [[weak equivalence]] or equivalently a [[homotopy equivalence]] in $\mathcal{C}$ precisely when the interpretation of $isEquiv(f)$ has a [[generalized element|global point]] $* \to hasContrFibers(f)$.

=--

+-- {: .proof}
###### Proof

For $f\colon A\to B$, the [[categorical semantics]] of the [[dependent type]]

$$
  b\colon B 
   \;\vdash\; 
  hfiber(f,b)\colon Type
$$ 

is by the rules for the [[categorical semantics|interpretation]] of [[identity types]] and [[substitution]]
the [[mapping path space]] construction $P f$, given by the [[pullback]]

$$
  \array{
    [b : B \vdash  hfiber(f,b)] &\coloneqq & P f  &\to& A
    \\
    && \downarrow && \downarrow^{\mathrlap{f}}
    \\
    && B^I &\to& B
    \\
    && \downarrow
    \\
    && B
  }
$$

which, by the [[factorization lemma]], is one way to factor $f$ as an [[acyclic cofibration]] followed by a [[fibration]]

$$
  f : A \stackrel{\simeq}{\to} P f \to B
  \,.
$$

By definition and the semantics of [[contractible types]], therefore, if $A$ and $B$ are cofibrant, then $isEquiv(f)$ has a [[global element]] 

$$
  * \to \prod_{b} isContr(hfiber(f,b))
$$


precisely when in this factorization, the fibration $P f \to B$ is an acyclic fibration.  (See for instance ([Shulman, page 49](http://www.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=49)) for more details.)


But by the [[2-out-of-3 property]], this is equivalent to $f$ being a weak equivalence --- and hence a homotopy equivalence, since it is a map between fibrant-cofibrant objects.


=--

+-- {: .num_remark #InterpretationIfIsEquivAsDependentType}
###### Remark

In the above we fixed one function $f : A \to X$. But the type $isEquiv$ is actually a [[dependent type]]

$$
  f : A \to B \vdash isEquiv(f)
$$

on the [[function type|type of all functions]]. To obtain the [[categorical semantics]] of this general dependent $hasContrFibers$-construction, first notice that the interpretation of

$f : A \to B,\; a : A,\; b : B \;\vdash\; (f(a) = b)  \colon Type$

is by the rules for interpretation of [[identity types]], [[evaluation]] and [[substitution]] the left vertical morphism in the [[pullback]] [[diagram]]

$$
  \array{  
    Q &\to&  B^I
    \\
    \downarrow && \downarrow
    \\
    [A,B] \times A \times B &\stackrel{(eval, id_B)}{\to}& B \times B
  }
  \,,
$$

where $eval : [A, B] \times A \to B$ is the [[evaluation map]] for the [[internal hom]].
This means that the interpretation of further [[dependent sum]] yielding $hfib$

$$
  f : A \to B,\; b : B 
   \; \vdash \;  
  \left(
    \sum_{a : A } (f(a) = b) 
  \right)
  \colon Type
$$

is the composite left vertical morphism in

$$
  \array{  
    Q &\to& B^I
    \\
    \downarrow && \downarrow
    \\
    [A,B] \times A \times B &\stackrel{(eval, id_B)}{\to}& B \times B
    \\
    \downarrow^{\mathrlap{p_{1,3}}}
    \\
    [A,B] \times B
  }
$$

=--

### Of $Equiv(-)$


(...)


## Related concepts

* **isEquiv**

* [[isContr]]

* [[isProp]]

* [[homotopy equivalence]]

  * [[weak homotopy equivalence]]

  * [[stable weak homotopy equivalence]]

* [[equivalence type]]

* [[embedding in type theory]]

* [[definitional isomorphism]]

## References
 {#References}

### General

The notion of two-sided homotopy equivalence of types in [[homotopy type theory]] appears (together with the formulation of the [[univalence axiom]]) already in

* {#HofmannStreicher98} [[Martin Hofmann]], [[Thomas Streicher]], §5.4 of:  _The groupoid interpretation of type theory_, in: [[Giovanni Sambin]] et al. (eds.), *Twenty-five years of constructive type theory*, Proceedings of a congress, Venice, Italy, October 19-21, 1995. Oxford: Logic Guides. **36**, Clarendon Press (1998) 83-111 &lbrack;[ISBN:9780198501275](https://global.oup.com/academic/product/twenty-five-years-of-constructive-type-theory-9780198501275), [ps](http://www.mathematik.tu-darmstadt.de/~streicher/venedig.ps.gz), [[HofmannStreicherGroupoidInterpretation.pdf:file]]&rbrack;

except that these authors refer to the subtly incorrect type (eq:TheSubtlyWrongTypeOfEquivalences) of all such equivalences.

The notion of equivalences as [[function type|functions]] with [[contractible type|contractible]] [[fiber type|homotopy fibers]] (and thereby the fix of the [[univalence axiom]] of [Hofmann & Streicher (1998), §5.4](#HofmannStreicher98)) is due to:

* {#Voevodsky10} [[Vladimir Voevodsky]], p. 10 of: *Univalent Foundations Project* (2010) &lbrack;[pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/univalent_foundations_project.pdf), [[Voevodsky-UFP2010.pdf:file]]&rbrack;

The notion of "homotopy isomorphisms" (functions with left- and right-quasi inverses) was proposed by [[André Joyal]] in a 2011 Oberwolfach meeting, recorded in:

* {#KapulkinLumsdaine21} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], Def. 3.1.1 in: *The Simplicial Model of Univalent Foundations (after Voevodsky)*, Journal of the European Mathematical Society **23** (2021) 2071–2126  &lbrack;[arXiv:1211.2851](https://arxiv.org/abs/1211.2851), [doi:10.4171/jems/1050](https://doi.org/10.4171/jems/1050)&rbrack;

The notion of equivalences as [[one-to-one correspondences]] is due to:

* {#Shulman22} [[Mike Shulman]], Towards a Third-Generation HOTT Part 1 ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

Introduction and exposition:

* [[Andrej Bauer]], *HoTT equivalences*, talk (2011) &lbrack;[webpage](https://math.andrej.com/2011/12/07/hott-equivalences/), [video](https://www.youtube.com/watch?v=V3YUsZx_fmo)&rbrack;

* {#Shulman} [[Mike Shulman]], from [slide 60 of part 2](https://home.sandiego.edu/~shulman/hottminicourse2012/02hott.pdf#page=60), [slide 49 of part 3](https://home.sandiego.edu/~shulman/hottminicourse2012/03models.pdf#page=49) in: _Minicourse in homotopy type theory_ (2012) &lbrack;[web](https://home.sandiego.edu/~shulman/hottminicourse2012/)&rbrack;

* [[Andrej Bauer]], *Equivalences* &lbrack;[video](https://www.youtube.com/watch?v=BuI62-o3Ds8)&rbrack;, Part 4 of: *[Introduction to homotopy type theory](https://www.youtube.com/playlist?list=PL-47DDuiZOMCRDiXDZ1fI0TFLQgQqOdDa)*, lecture series (2019)


Textbook account:

* {#UFP13} [[Univalent Foundations Project]], §2.4 and §4 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


Implementation of equivalences in [[proof assistants]]:

in [[Coq]]:

* [github.com/HoTT/HoTT/blob/master/theories/Basics/Equivalences.v](https://github.com/HoTT/HoTT/blob/master/theories/Basics/Equivalences.v)

in [[Agda]]:

* [agda.github.io/agda-stdlib/v1.1/Function.Equivalence.html](https://agda.github.io/agda-stdlib/v1.1/Function.Equivalence.html)

On equivalences as one-to-one correspondences in homotopy type theory:

* Mike Shulman, *Towards a Third-Generation HOTT* Part 1 &lbrack;[slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA)&rbrack;


### Applications
 {#ApplicationsInProofReuse}

Origin of the notion of type isomorphy in and application to [[programming language]]-theory and -practice:

* {#Rittri89} Mikael Rittri, *Using types as search keys in function libraries*, in: *FPCA '89: Proceedings of the fourth international conference on Functional programming languages and computer architecture* (1989) 174–183 &lbrack;[doi:10.1145/99370.99384](https://doi.org/10.1145/99370.99384), [pdf](https://dl.acm.org/doi/pdf/10.1145/99370.99384)&rbrack;

* {#Cosmo95} [[Roberto Di Cosmo]], *Isomorphisms of Types -- from $\lambda$-calculus to information retrieval and language design*, Progress in Theoretical Computer Science, Birkhäuser (1995) &lbrack;[doi:10.1007/978-1-4612-2572-0](https://doi.org/10.1007/978-1-4612-2572-0)&rbrack;

* [[Gilles Barthe]], [[Olivier Pons]], *Type Isomorphisms and Proof Reuse in Dependent Type Theory*, in *Foundations of Software Science and Computation Structures. FoSSaCS 2001*, Lecture Notes in Computer Science **2030**, Springer (2001) &lbrack;[doi:10.1007/3-540-45315-6_4](https://doi.org/10.1007/3-540-45315-6_4)&rbrack;

* [[Roberto Di Cosmo]], *A short survey of isomorphisms of types*, Mathematical Structures in Computer Science **15** 5  (2005) 825-838 &lbrack;[doi:10.1017/S0960129505004871](https://doi.org/10.1017/S0960129505004871), [pdf](https://www.dicosmo.org/Articles/mscs-survey.pdf)&rbrack;

* [[Talia Ringer]], RanDair Porter, Nathaniel Yazdani, John Leo, Dan Grossman, *Proof Repair across Type Equivalences* &lbrack;[arXiv:2010.00774](https://arxiv.org/abs/2010.00774)&rbrack;

* [[Talia Ringer]], *Proof repair along type equivalences*, §4 in: *Proof Repair*, Univ. Washington (2021) &lbrack;[proquest:2568297410](https://www.proquest.com/docview/2568297410), [video](https://www.youtube.com/watch?v=_BkTrp44uBU)&rbrack;

[[!redirects equivalence of types]]
[[!redirects equivalences of types]]

[[!redirects weak equivalence of types]]
[[!redirects weak equivalences of types]]

[[!redirects isEquiv]]

[[!redirects equivalence in homotopy type theory]]
[[!redirects equivalences in homotopy type theory]]
[[!redirects equivalence in type theory]]
[[!redirects equivalences in type theory]]
[[!redirects equivalence in HoTT]]
[[!redirects equivalences in HoTT]]

[[!redirects adjoint equivalence in homotopy type theory]]
[[!redirects adjoint equivalences in homotopy type theory]]
[[!redirects adjoint equivalence in type theory]]
[[!redirects adjoint equivalences in type theory]]
[[!redirects adjoint equivalence in HoTT]]
[[!redirects adjoint equivalences in HoTT]]

[[!redirects weak equivalence in homotopy type theory]]
[[!redirects weak equivalences in homotopy type theory]]
[[!redirects weak equivalence in type theory]]
[[!redirects weak equivalences in type theory]]
[[!redirects weak equivalence in HoTT]]
[[!redirects weak equivalences in HoTT]]

[[!redirects homotopy isomorphism]]
[[!redirects h-isomorphism]]

[[!redirects type equivalence]]
[[!redirects type equivalences]]

[[!redirects equivalence in type theory]]
[[!redirects equivalences in type theory]]