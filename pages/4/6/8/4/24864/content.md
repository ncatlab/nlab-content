
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

Book HoTT is the [[dependent type theory]] which appears in the [[HoTT book]]. It is notable in that, unlike most other dependent type theories which have been formally written in [[natural deduction]], it does not have a separate [[type]] [[judgment]]. Instead, it only has term judgments, and an infinite sequence of [[Russell universes]] indexed by a [[natural numbers]] primitive. Types are represented by terms of a Russell universe. 

However, when formally defining the natural numbers primitive, in order to ensure that the dependent type theory does not have a separate type judgment, one has to define the natural numbers primitive in a separate [[layer]], meaning that formal book HoTT is a [[layered type theory]]. There are many different ways to define the layer containing the natural numbers primitive: 

* One could define the [[first-order theory]] of a [[category]] with [[finite products]] and a parameterized [[natural numbers object]], and use the [[hom-set]] $\mathrm{Hom}(1, \mathbb{N})$ to index the [[Russell universes]]. 
* One could define the simply typed first order theory of [[ZFC]], and use the von Neumann natural numbers or the Zermelo natural numbers to index the Russell universes. 
* One could define the simply typed first order theory of [[Peano arithmetic]], and use the natural numbers in Peano arithmetic to index the Russell universes. 
* One could define a separate [[dependent type theory]] with a [[natural numbers type]], such as the [[extensional type theory]] in [[two-level type theory]], and use the natural numbers type $\mathbb{N}$ to index the Russell universes. 

## Formal presentation

The presentation of formal book HoTT we have chosen is a two-[[layered type theory]]. The first level consists of a basic [[objective type theory]] consisting only of type judgments, term judgments, [[identity types]], and a [[natural numbers type]]. The second level is the [[homotopy type theory]], and contains term judgments and [[judgmental equality]] of terms, [[Russell universes]], and all the other type formers in [[homotopy type theory]]. To distinguish between the two layers, we shall call the types in the first layer "metatypes", as the first layer behaves as a metatheory or external theory. 

### First layer

#### Judgments and contexts

We begin with the formal rules of the first layer. The first layer consists of three judgments: metatype judgments $A \; \mathrm{metatype}$, where we judge $A$ to be a metatype, metatyping judgments, where we judge $a$ to be an element of $A$, $a \in A$, and metacontext judgments, where we judge $\Xi$ to be a metacontext, $\Xi \; \mathrm{metactx}$. Metacontexts are lists of metatyping judgments $a \in A$, $b \in B$, $c \in C$, et cetera, and are formalized by the rules for the empty metacontext and extending the metacontext by a metatyping judgment

$$\frac{}{() \; \mathrm{metactx}} \qquad \frac{\Xi \; \mathrm{metactx} \quad \Xi \vdash A \; \mathrm{metatype}}{(\Xi, a \in A) \; \mathrm{metactx}}$$

#### Structural rules

The three standard structural rules, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]], are also included in the theory. Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

* The variable rule:

$$\frac{\Xi, a \in A, \Omega \; \mathrm{metactx}}{\vdash \Xi, a \in A, \Omega \vdash a \in A}$$

* The weakening rule:

$$\frac{\Xi, \Omega \vdash \mathcal{J} \quad \Xi \vdash A \; \mathrm{metatype}}{\Xi, a \in A, \Omega \vdash \mathcal{J}}$$

* The substitution rule:

$$\frac{\Xi \vdash a \in A \quad \Xi, b \in A, \Omega \vdash \mathcal{J}}{\Xi, \Omega[a/b] \vdash \mathcal{J}[a/b]}$$

#### Identity metatypes

In addition, there are identity metatypes: the [[natural deduction]] rules for identity metatypes are as follows

$$\frac{\Xi \vdash A \; \mathrm{metatype}}{\Xi, a \in A, b \in A \vdash a =_A b \; \mathrm{metatype}} \qquad \frac{\Xi \vdash A \; \mathrm{metatype}}{\Xi, a \in A \vdash \mathrm{refl}_A(a)  \in  a =_A a}$$

$$\frac{\Xi, x \in A, y \in A, p \in x =_A y \vdash C \; \mathrm{metatype} \quad \Xi, z \in A \vdash t \in C[z/x, z/y, \mathrm{refl}_A(z)/p] \quad \Xi \vdash a \in A \quad \Xi \vdash b \in A \quad \Xi \vdash q \in a =_A b}{\Xi \vdash J(x.y.p.C, z.t, x, y, p) \in C[a/x, b/y, q/p]}$$

$$\frac{\Xi, x \in A, y \in A, p \in x =_A y \vdash C \; \mathrm{metatype} \quad \Xi, z \in A \vdash t:C[z/x, z/y, \mathrm{refl}_A(z)/p] \quad \Xi \vdash a:A}{\Xi \vdash \beta_{=_A}(a) \in J(x.y.p.C, z.t, a, a, \mathrm{refl}_A(a)) =_{C[a/x, a/y, \mathrm{refl}_A(a)/p]} t[a/z]}$$

#### Natural numbers primitive

Finally, we have the natural numbers primitive, given by the following [[natural deduction]] rules:

$$\frac{\Xi \; \mathrm{metactx}}{\Xi \vdash \mathcal{N} \; \mathrm{metatype}} \qquad \frac{\Xi \; \mathrm{metactx}}{\Xi \vdash 0_{\mathcal{N}} \in \mathcal{N}} \qquad \frac{\Xi \vdash n \in \mathcal{N}}{\Xi \vdash s_\mathcal{N}(n) \in \mathcal{N}}$$

$$\frac{\Xi, x \in \mathcal{N} \vdash C \; \mathrm{metatype} \quad \Xi \vdash c_{0_\mathcal{N}} \in C[0_\mathcal{N}/x] \quad \Xi, x \in \mathcal{N}, c \in C \vdash c_{s_\mathcal{N}} \in C[s_\mathcal{N}(x)/x] \quad \Xi \vdash n \in \mathbb{N}}{\Gamma \vdash \mathrm{ind}_\mathcal{N}^C(n, c_{0_\mathcal{N}}, c_{s_\mathcal{N}}) \in C[n/x]}$$

$$\frac{\Xi, x \in \mathcal{N} \vdash C \; \mathrm{metatype} \quad \Xi \vdash c_{0_\mathcal{N}} \in C[0_\mathcal{N}/x] \quad \Xi, x \in \mathcal{N}, c \in C \vdash c_{s_\mathcal{N}} \in C[s_\mathcal{N}(x)/x]}{\Xi \vdash \beta_\mathcal{N}^{0_\mathcal{N}} \in \mathrm{ind}_\mathcal{N}^C(0_\mathcal{N}, c_{0_\mathcal{N}}, c_{s_\mathcal{N}}) =_{C[0_\mathcal{N}/x]} c_{0_\mathcal{N}}}$$

$$\frac{\Xi, x \in \mathcal{N} \vdash C \; \mathrm{metatype} \quad \Xi \vdash c_{0_\mathcal{N}} \in C[0_\mathcal{N}/x] \quad \Xi, x \in \mathcal{N}, c \in C \vdash c_{s_\mathcal{N}} \in C[s_\mathcal{N}(x)/x]}{\Gamma \vdash \beta_\mathcal{N}^{s_\mathcal{N}(n)} \in \mathrm{ind}_\mathcal{N}^C(s_\mathcal{N}(n), c_{0_\mathcal{N}}, c_{s_\mathcal{N}}) =_{C[s_\mathcal{N}(n)/x]} c_{s_\mathcal{N}}(n, \mathrm{ind}_\mathcal{N}^C(n, c_{0_\mathcal{N}}, c_{s_\mathcal{N}}))}$$

### Second layer

#### Judgments, contexts, and Russell universes

Now, we introduce the second layer, which consists of a dependent type theory with two judgments, the typing judgment $a:A$, which says that $a$ is a term of the type $A$, and [[judgmental equality]] $a \equiv a':A$, which says that $a$ and $a'$ are judgmentally equal terms of the type $A$. Instead of type judgments, we introduce a special kind of type called a [[Russell universe]], whose terms are the types themselves. We also assume cumulativity for the Russell universes. Russell universes are formalized with the following rules:

$$\frac{\Xi \vdash i \in \mathcal{N}}{\Xi \vdash U_i:U_{s_\mathcal{N}(i)}} \quad \frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vdash A:U_i}{\Xi \vdash A:U_{s_\mathcal{N}(i)}}$$

Contexts are defined as a metacontext with a list of typing judgments, with the metacontext always preceding the list of typing judgments:

$$\frac{\Xi \; \mathrm{metactx}}{\Xi \vert () \; \mathrm{ctx}} \qquad \frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i}{\Xi \vert (\Gamma, a:A) \; \mathrm{ctx}}$$

The general rules for Russell universes then follows:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \; \mathrm{ctx}}{\Xi \vert \Gamma \vdash U_i:U_{s_\mathcal{N}(i)}} \quad \frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i}{\Xi \vert \Gamma \vdash A:U_{s_\mathcal{N}(i)}}$$

In addition, if there is a term $a:A$ of a type $A$, then the type $A$ is a term of some Russell universe $U_i$. 

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash A:U_{i}}$$

#### Structural rules

There are three structural rules in dependent type theory, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]]. 

The variable rule states that we may derive a typing judgment if the typing judgment is in the context already:

$$\frac{\Xi \vert \Gamma, a:A, \Delta \; \mathrm{ctx}}{\Xi \vert \Gamma, a:A, \Delta \vdash a:A}$$

Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

The weakening rule:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma, \Delta \vdash \mathcal{J}}{\Xi \vert \Gamma, a:A, \Delta \vdash \mathcal{J}}$$

The substitution rule:

$$\frac{\Xi \vert \Gamma \vdash a:A \quad \Xi \vert \Gamma, b:A, \Delta \vdash \mathcal{J}}{\Xi \vert \Gamma, \Delta[a/b] \vdash \mathcal{J}[a/b]}$$

The weakening and substitution rules are admissible rules: they do not need to be explicitly included in the type theory as they could be proven by induction on the structure of all possible derivations. 

#### Structural rules for judgmental equality

Judgmental equality has its own structural rules: introduction rules for judgmentally equal terms, reflexivity, symmetry, transitivity, the principle of substitution, and the variable conversion rule. 

* Introduction rules for judgmentally equal terms
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash a \equiv b:A}{\Xi \vert \Gamma \vdash a:A}$$
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash a \equiv b:A}{\Xi \vert \Gamma \vdash b:A}$$

* Reflexivity of judgmental equality
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash a \equiv a:A}$$

* Symmetry of judgmental equality
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash a \equiv b:A}{\Xi \vert \Gamma \vdash b \equiv a:A}$$

* Transitivity of judgmental equality
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash a \equiv b:A \quad \Xi \vert \Gamma \vdash b \equiv c:A}{\Xi \vert \Gamma \vdash a \equiv c:A}$$

* Principle of substitution:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash a \equiv b : A \quad \Xi \vert \Gamma, x:A, \Delta \vdash c:B}{\Xi \vert \Gamma, \Delta[b/x] \vdash c[a/x] \equiv c[b/x]: B[b/x]}$$

* Variable conversion rule:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A \equiv B:U_i \quad \Xi \vert \Gamma, x:A, \Delta \vdash \mathcal{J}}{\Xi \vert \Gamma, x:B, \Delta \vdash \mathcal{J}}$$


#### Dependent product types

* Formation rules for dependent product types:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma, x:A \vdash B:U_i}{\Xi \vert \Gamma \vdash \prod_{x:A} B(x):U_i}$$

* Introduction rules for dependent product types:

$$\frac{\Xi \vert \Gamma, x:A \vdash b:B}{\Xi \vert \Gamma \vdash \lambda(x:A).b(x):\prod_{x:A} B(x)}$$

* Elimination rules for dependent product types:

$$\frac{\Xi \vert \Gamma \vdash f:\prod_{x:A} B(x) \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash f[a/x]:B[a/x]}$$

* Computation rules for dependent product types:

$$\frac{\Xi \vert \Gamma, x:A \vdash b:B \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \lambda(x:A).b(x)[a/x] \equiv b[a/x]:B[a/x]}$$

* Uniqueness rules for dependent product types:

$$\frac{\Xi \vert \Gamma \vdash f:\prod_{x:A} B(x)}{\Xi \vert \Gamma \vdash f \equiv \lambda(x).f(x):\prod_{x:A} B(x)}$$

#### Dependent sum types

* Formation rules for dependent sum types:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Gamma, x:A \vdash B:U_i}{\Xi \vert \Gamma \vdash \sum_{x:A} B(x):U_i}$$

* Introduction rules for dependent sum types:

$$\frac{\Xi \vert \Gamma, x:A \vdash b:B \quad \Xi \vert \Gamma \vdash a:A \quad \Xi \vert \Gamma \vdash b:B[a/x]}{\Xi \vert \Gamma \vdash (a, b):\sum_{x:A} B(x)}$$

* Elimination rules for dependent sum types:

$$\frac{\Xi \vert \Gamma \vdash z:\sum_{x:A} B(x)}{\Xi \vert \Gamma \vdash \pi_1(z):A} \qquad \frac{\Xi \vert \Gamma \vdash z:\sum_{x:A} B(x)}{\Xi \vert \Gamma \vdash \pi_2(z):B[\pi_1(z)/x]}$$

* Computation rules for dependent sum types:

$$\frac{\Xi \vert \Gamma, x:A \vdash b:B \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \pi_1(a, b) \equiv a:A} \qquad \frac{\Xi \vert \Gamma, x:A \vdash b:B \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \pi_2(a, b) \equiv b:B[\pi_1(a, b)/x]}$$

* Uniqueness rules for dependent sum types:

$$\frac{\Xi \vert \Gamma \vdash z:\sum_{x:A} B(x)}{\Xi \vert \Gamma \vdash z \equiv (\pi_1(z), \pi_2(z)):\sum_{x:A} B(x)}$$

#### Sum types

* Formation rules for sum types:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash B:U_i}{\Xi \vert \Gamma \vdash A + B:U_i}$$

* Introduction rules for sum types:

$$\frac{\Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \mathrm{inl}(a):A + B} \qquad \frac{\Xi \vert \Gamma \vdash b:B}{\Xi \vert \Gamma \vdash \mathrm{inr}(b):A + B}$$

* Elimination rules for sum types:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, z:A + B \vdash C:U_i \quad \Xi \vert \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Xi \vert \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Xi \vert \Gamma \vdash e:A + B}{\Xi \vert \Gamma \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, e):C[e/z]}$$

* Computation rules for sum types:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, z:A + B \vdash C:U_i \quad \Xi \vert \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Xi \vert \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, \mathrm{inl}(a)) \equiv c[a/x]:C[\mathrm{inl}(a)/z]}$$
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, z:A + B \vdash C:U_i \quad \Xi \vert \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Xi \vert \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Xi \vert \Gamma \vdash b:A}{\Xi \vert \Gamma \vdash \mathrm{ind}_{A + B}(z.C, x.c, y.d, \mathrm{inr}(b)) \equiv d[b/x]:C[\mathrm{inr}(b)/z]}$$

#### Empty type

* Formation rules for the empty type:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \; \mathrm{ctx}}{\Xi \vert \Gamma \vdash \mathbb{0}:U_i}$$

* Elimination rules for the empty type:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, x:\mathbb{0} \vdash C:U_i \quad \Gamma \vdash p:\mathbb{0}}{\Gamma \vdash \mathrm{ind}_\mathbb{0}(x.C, p):C[p/x]}$$

#### Unit type

* Formation rules for the unit type:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \; \mathrm{ctx}}{\Xi \vert \Gamma \vdash \mathbb{1} \; \mathrm{type}}$$

* Introduction rules for the unit type:

$$\frac{\Xi \vert \Gamma \; \mathrm{ctx}}{\Xi \vert \Gamma \vdash *:\mathbb{1}}$$

* Elimination rules for the unit type:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, x:\mathbb{1} \vdash C:U_i \quad \Gamma, y:\mathbb{1} \vdash c[y/x]:C[y/x] \quad \Gamma \vdash p:\mathbb{1}}{\Gamma \vdash \mathrm{ind}_\mathbb{1}(x.C, y.c, p):C[p/x]}$$

* Computation rules for the unit type:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, x:\mathbb{1} \vdash C:U_i \quad \Gamma, y:\mathbb{1} \vdash c[y/x]:C[y/x]}{\Gamma \vdash \mathrm{ind}_\mathbb{1}(x.C, y.c, *) \equiv c[*/x]:C[*/x]}$$

#### Natural numbers

* Formation rules for the natural numbers:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \; \mathrm{ctx}}{\Xi \vert \Gamma \vdash \mathbb{N}:U_i}$$

* Introduction rules for the natural numbers:
$$\frac{\Xi \vert \Gamma \; \mathrm{ctx}}{\Xi \vert \Gamma \vdash 0:\mathbb{N}} \qquad \frac{\Xi \vert \Gamma \vdash n:\mathbb{N}}{\Xi \vert \Gamma \vdash s(n):\mathbb{N}}$$

* Elimination rules for the natural numbers:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, x:\mathbb{N} \vdash C:U_i \quad \Xi \vert \Gamma \vdash c_0:C[0/x] \quad \Xi \vert \Gamma, x:\mathbb{N}, y:C \vdash c_s:C[s(x)/x] \quad \Xi \vert \Gamma \vdash n:\mathbb{N}}{\Xi \vert \Gamma \vdash \mathrm{ind}_\mathbb{N}(x.C, c_0, x.y.c_s, n):C[n/x]}$$

* Computation rules for the natural numbers:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, x:\mathbb{N} \vdash C:U_i \quad \Xi \vert \Gamma \vdash c_0:C[0/x] \quad \Xi \vert \Gamma, x:\mathbb{N}, y:C \vdash c_s:C[s(x)/x]}{\Xi \vert \Gamma \vdash \mathrm{ind}_\mathbb{N}(x.C, c_0, x.y.c_s, 0) \equiv c_0:C[0/x]}$$

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, x:\mathbb{N} \vdash C:U_i \quad \Xi \vert \Gamma \vdash c_0:C[0/x] \quad \Xi \vert \Gamma, x:\mathbb{N}, y:C \vdash c_s:C[s(x)/x]}{\Xi \vert \Gamma \vdash \mathrm{ind}_\mathbb{N}(x.C, c_0, x.y.c_s, s(n) \equiv c_s(n, \mathrm{ind}_\mathbb{N}(x.C, c_0, x.y.c_s, n)):C[s(n)/x]}$$

#### Identity types

There is another version of equality in book HoTT, called [[typal equality]]. Typal equality is represented by the [[identity type]]. 

* Formation rule for identity types:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash a:A \quad \Xi \vert \Gamma \vdash b:A}{\Xi \vert \Gamma \vdash a =_A b:U_i}$$

* Introduction rule for identity types:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \mathrm{refl}_A(a) : a =_A a}$$

* Elimination rule for identity types:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, x:A, y:A, p:a =_A b \vdash C:U_i \quad \Xi \vert \Gamma, z:A \vdash t:C[z/a, z/b, \mathrm{refl}_A(z)/p] \quad \Xi \vert \Gamma \vdash a:A \quad \Xi \vert \Gamma \vdash b:A \quad \Xi \vert \Gamma \vdash q:a =_A b}{\Xi \vert \Gamma \vdash J(x,y,p.C, z.t, a, b, q):C[a, b, q/x, y, p]}$$

* Computation rules for identity types:
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma, x:A, y:A, p:a =_A b \vdash C:U_i \quad \Xi \vert \Gamma, z:A \vdash t:C[z/a, z/b, \mathrm{refl}_A(z)/p] \quad \Xi \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash J(x.y.p.C, z.t, a, a, \mathrm{refl}(a)) \equiv t:C[a, a, \mathrm{refl}_A(a)/x, y, p]}$$

#### Univalence

Given types $A:U_i$ and $B:U_i$, a function $f:A \to B$ is an [[equivalence of types]] if the fiber of $f$ at each element of $B$ has exactly one element. The property of the type $A$ having exactly one element is represented by the [[isContr]] modality which states that the type $A$ is contractible. The fiber of $f$ at an element $b:B$ is given by the type
$$\sum_{b:B} f(a) =_B b$$

We formally define the property of $R$ being a one-to-one correspondence or an equivalence of types as the type:

$$\mathrm{isEquiv}_{A, B}(f) \coloneqq \prod_{b:B} \mathrm{isContr}\left(\sum_{a:A} f(a) =_B b\right)$$

We define the type of equivalences from $A$ to $B$ in $U_i$ as 

$$(A \simeq_{U_i} B) \coloneqq \sum_{R : (A \times B) \to U_i} \mathrm{isEquiv}_{A, B}(R)$$

The principle of [[univalence]] is the principle that the identity type between two types in a universe is the same as the type of equivalences between the two types, and is given by the following rules:

$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash B:U_i \quad \Xi \vert \Gamma \vdash R:A \simeq_{U_i} B}{\Xi \vert \Gamma \vdash \mathrm{equivtoid}(R):A =_{U_i} B}$$ 
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash B:U_i  \quad \Xi \vert \Gamma \vdash P:A =_{U_i} B}{\Xi \vert \Gamma \vdash \mathrm{idtoequiv}(P):A \simeq_U B}$$ 
$$\frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i \quad \Xi \vert \Gamma \vdash B:U_i  \quad \Xi \vert \Gamma \vdash R:A \simeq_{U_i} B}{\Xi \vert \Gamma \vdash \mathrm{idtoequiv}(\mathrm{equivtoid}(R)) \equiv R \; \mathrm{type}}$$

## See also

* [[dependent type theory]]

* [[homotopy type theory]]

## References

* *Homotopy Type Theory: Univalent Foundations of Mathematics*,
The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

The rules for univalence are adapted from 

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))