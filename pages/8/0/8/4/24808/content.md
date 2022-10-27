+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--

\tableofcontents

## Idea

Russell universes or universes à la Russell are types whose terms are types. In [[type theories]] without a separate type [[judgment]] $A \; \mathrm{type}$, only typing judgments $a:A$, what would have been type judgments are represented by typing judgments that $A$ is a term of a Russell universe $U$, $A:U$. Russell universes without a separate type judgment are used in many places in type theory, including in the [[HoTT book]], in [[Coq]], and in [[Agda]]. 

## Formal definition

### Without a separate type judgment

Russell universes are formally defined in a [[two-level type theory]]. The first level consists of a basic dependent type theory consisting of a type judgment, [[identity types]], and a [[natural numbers type]]. The second level only contains term judgments, and is the dependent type theory where the Russell universes live in. To distinguish between the two layers, we shall call the types in the first layer "metatypes", as the first layer behaves as a metatheory or external theory. 

We begin with the formal rules of the first layer. The first layer consists of three judgments: metatype judgments $A \; \mathrm{metatype}$, where we judge $A$ to be a metatype, metatyping judgments, where we judge $a$ to be an element of $A$, $a \in A$, and metacontext judgments, where we judge $\Xi$ to be a metacontext, $\Xi \; \mathrm{metactx}$. Metacontexts are lists of metatyping judgments $a \in A$, $b \in B$, $c \in C$, et cetera, and are formalized by the rules for the empty metacontext and extending the metacontext by a metatyping judgment

$$\frac{}{() \; \mathrm{metactx}} \qquad \frac{\Xi \; \mathrm{metactx} \quad \Xi \vdash A \; \mathrm{metatype}}{(\Xi, a \in A) \; \mathrm{metactx}}$$

The three standard structural rules, the [[variable rule]], the [[weakening rule]], and the [[substitution rule]], are also included in the theory. Let $\mathcal{J}$ be any arbitrary judgment. Then we have the following rules:

* The variable rule:

$$\frac{\Xi, a \in A, \Omega \; \mathrm{metactx}}{\vdash \Xi, a \in A, \Omega \vdash a \in A}$$

* The weakening rule:

$$\frac{\Xi, \Omega \vdash \mathcal{J} \quad \Xi \vdash A \; \mathrm{metatype}}{\Xi, a \in A, \Omega \vdash \mathcal{J}}$$

* The substitution rule:

$$\frac{\Xi \vdash a \in A \quad \Xi, b \in A, \Omega \vdash \mathcal{J}}{\Xi, \Omega[a/b] \vdash \mathcal{J}[a/b]}$$

In addition, there are identity metatypes: the [[natural deduction]] rules for identity metatypes are as follows

$$\frac{\Xi \vdash A \; \mathrm{metatype}}{\Xi, a \in A, b \in A \vdash a =_A b \; \mathrm{metatype}} \qquad \frac{\Xi \vdash A \; \mathrm{metatype}}{\Xi, a \in A \vdash \mathrm{refl}_A(a)  \in  a =_A a}$$

$$\frac{\Xi, x \in A, y \in A, p \in x =_A y \vdash C \; \mathrm{metatype} \quad \Xi, z \in A \vdash t \in C[z/x, z/y, \mathrm{refl}_A(z)/p] \quad \Xi \vdash a \in A \quad \Xi \vdash b \in A \quad \Xi \vdash q \in a =_A b}{\Xi \vdash J(x.y.p.C, z.t, x, y, p) \in C[a/x, b/y, q/p]}$$

$$\frac{\Xi, x \in A, y \in A, p \in x =_A y \vdash C \; \mathrm{metatype} \quad \Xi, z \in A \vdash t:C[z/x, z/y, \mathrm{refl}_A(z)/p] \quad \Xi \vdash a:A}{\Xi \vdash \beta_{=_A}(a) \in J(x.y.p.C, z.t, a, a, \mathrm{refl}_A(a)) =_{C[a/x, a/y, \mathrm{refl}_A(a)/p]} t[a/z]}$$

Finally, we have the natural numbers metatype, given by the following [[natural deduction]] rules:

$$\frac{\Xi \; \mathrm{metactx}}{\Xi \vdash \mathcal{N} \; \mathrm{metatype}} \qquad \frac{\Xi \; \mathrm{metactx}}{\Xi \vdash 0_{\mathcal{N}} \in \mathcal{N}} \qquad \frac{\Xi \vdash n \in \mathcal{N}}{\Xi \vdash s_\mathcal{N}(n) \in \mathcal{N}}$$

$$\frac{\Xi, x \in \mathcal{N} \vdash C \; \mathrm{metatype} \quad \Xi \vdash c_{0_\mathcal{N}} \in C[0_\mathcal{N}/x] \quad \Xi, x \in \mathcal{N}, c \in C \vdash c_{s_\mathcal{N}} \in C[s_\mathcal{N}(x)/x] \quad \Xi \vdash n \in \mathbb{N}}{\Gamma \vdash \mathrm{ind}_\mathcal{N}^C(n, c_{0_\mathcal{N}}, c_{s_\mathcal{N}}) \in C[n/x]}$$

$$\frac{\Xi, x \in \mathcal{N} \vdash C \; \mathrm{metatype} \quad \Xi \vdash c_{0_\mathcal{N}} \in C[0_\mathcal{N}/x] \quad \Xi, x \in \mathcal{N}, c \in C \vdash c_{s_\mathcal{N}} \in C[s_\mathcal{N}(x)/x]}{\Xi \vdash \beta_\mathcal{N}^{0_\mathcal{N}} \in \mathrm{ind}_\mathcal{N}^C(0_\mathcal{N}, c_{0_\mathcal{N}}, c_{s_\mathcal{N}}) =_{C[0_\mathcal{N}/x]} c_{0_\mathcal{N}}}$$

$$\frac{\Xi, x \in \mathcal{N} \vdash C \; \mathrm{metatype} \quad \Xi \vdash c_{0_\mathcal{N}} \in C[0_\mathcal{N}/x] \quad \Xi, x \in \mathcal{N}, c \in C \vdash c_{s_\mathcal{N}} \in C[s_\mathcal{N}(x)/x]}{\Gamma \vdash \beta_\mathcal{N}^{s_\mathcal{N}(n)} \in \mathrm{ind}_\mathcal{N}^C(s_\mathcal{N}(n), c_{0_\mathcal{N}}, c_{s_\mathcal{N}}) =_{C[s_\mathcal{N}(n)/x]} c_{s_\mathcal{N}}(n, \mathrm{ind}_\mathcal{N}^C(n, c_{0_\mathcal{N}}, c_{s_\mathcal{N}}))}$$

Now, we introduce the second layer, which consists of a type theory with only one judgment, the typing judgment $a:A$, which says that $a$ is a term of the type $A$. Instead of type judgments, we introduce a special kind of type called a **Russell universe** or **universe à la Russell**, whose terms are the types themselves. Russell universes are formalized with the following rules:

$$\frac{\Xi \vdash i \in \mathcal{N}}{\Xi \vdash U_i:U_{s_\mathcal{N}(i)}} \quad \frac{\Xi \vdash i \in \mathcal{N} \quad \Xi \vdash A:U_i}{\Xi \vdash \mathrm{Lift}_i(A):U_{s_\mathcal{N}(i)}}$$

Contexts are defined as a metacontext with a list of typing judgments, with the metacontext always preceding the list of typing judgments:

$$\frac{\Xi \; \mathrm{metactx}}{\Xi \vert () \; \mathrm{ctx}} \qquad \frac{\Xi \vert \Gamma \vdash A:U_i}{\Xi \vert (\Gamma, a:A) \; \mathrm{ctx}}$$

The general rules for Russell universes then follows:

$$\frac{\Xi \vert \Gamma \vdash i \in \mathcal{N}}{\Xi \vert \Gamma \vdash U_i:U_{s_\mathcal{N}(i)}} \quad \frac{\Xi \vert \Gamma \vdash i \in \mathcal{N} \quad \Xi \vert \Gamma \vdash A:U_i}{\Xi \vert \Gamma \vdash \mathrm{Lift}_i(A):U_{s_\mathcal{N}(i)}}$$

### With a separate type judgment

If the type theory has a separate type judgment $A \; \mathrm{type}$, the rules for Russell universes become simpler, as one doesn't have to assume infinitely many Russell universes and a second level to house the natural numbers type used to index the universes. Instead, we merely have

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash U \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:U}{\Gamma \vdash A \; \mathrm{type}}$$

Furthermore, the separate type judgment amounts to collapsing the two levels in the theory above into one level: Instead of defining the identity type and the type of natural numbers as external to the type theory, we instead define it as normal types internal to the type theory. Then the rules for the infinite tower of Russell universes are as follows:

$$\frac{\Gamma \vdash i:\mathbb{N}}{\Gamma \vdash U(i):U(s(i))} \qquad \frac{\Gamma \vdash i:\mathbb{N} \quad \Gamma \vdash A:U(i)}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \vdash i:\mathbb{N} \quad \Gamma \vdash A:U(i)}{\Gamma \vdash \mathrm{Lift}(i)(A):U(s(i))}$$

## See also

* [[Tarski universe]]
* [[two-level type theory]]

[[!redirects Russell universe]]
[[!redirects Russell universes]]