
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

In type theory, a conversion rule is a rule which constrains the result of combining [[term introduction]] with [[term elimination]]. Conversion rules come in two types: **[[beta conversion]] rules** or **computation rules**, and **[[eta conversion]] rules** or **uniqueness rules**. Computation rules in particular are important, because they are used in [[inductive definitions]]. For example, the rules for [[addition]] of [[natural numbers]] has two computation rules, which derive from the two computation rules of the [[natural numbers type]]. 

Moreover, conversion rules use [[equality]]. The usage of equality in this manner is called **conversional equality**, and in the context of beta conversion rules is also called **computational equality**. In [[type theory]], there are three notions of equality, [[judgmental equality]], [[propositional equality]], and [[typal equality]], all of which could be used for conversional equality. 

For example, the [[beta conversion]] rule for the [[dependent product type]] could be expressed in judgmental, propositional, and typal equality:

* Judgmental beta conversion rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) = b[a/x]:B[a/x]}$$

* Propositional beta conversion rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \lambda(x:A).b(x)(a) =_{B[a/x]} b[a/x] \; \mathrm{true}}$$

* Typal beta conversion rules for dependent product types:

$$\frac{\Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_\Pi:\lambda(x:A).b(x)(a) =_{B[a/x]} b[a/x]}$$

Similarly, the [[eta-conversion]] rule for the [[sum type]] could be expressed in judgmental, propositional, and typal equality:

* Judgmental eta conversion rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B \quad \Gamma, z:A + B \vdash u:C \quad \Gamma, a:A \vdash u[\mathrm{inl}(a)/z] \equiv c[a/x]:C[\mathrm{inl}(a)/z] \quad \Gamma, b:B \vdash u[\mathrm{inr}(b)/z] \equiv d[b/y]:C[\mathrm{inr}(b)/z]}{\Gamma \vdash u[e/z] \equiv \mathrm{ind}_{A + B}^C(c[\mathrm{inl}(e)/x], d[\mathrm{inr}(e)/y], e):C[e/z]}$$

* Propositional eta conversion rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B \quad \Gamma, z:A + B \vdash u:C \quad \Gamma, a:A \vdash u[\mathrm{inl}(a)/z] \equiv_{C[\mathrm{inl}(a)/z]} c[a/x] \; \mathrm{true} \quad \Gamma, b:B \vdash u[\mathrm{inr}(b)/z] \equiv_{C[\mathrm{inr}(b)/z]} d[b/y] \; \mathrm{true}}{\Gamma \vdash u[e/z] \equiv_{C[e/z]} \mathrm{ind}_{A + B}^C(c[\mathrm{inl}(e)/x], d[\mathrm{inr}(e)/y], e) \; \mathrm{true}}$$

* Typal eta conversion rules for sum types:

$$\frac{\Gamma, z:A + B \vdash C \; \mathrm{type} \quad \Gamma, x:A \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B \quad \Gamma, z:A + B \vdash u:C \quad \Gamma, a:A \vdash i_\mathrm{inl}(u):u[\mathrm{inl}(a)/z] =_{C[\mathrm{inl}(a)/z]} c[a/x] \quad \Gamma, b:B \vdash i_\mathrm{inr}(u):u[\mathrm{inr}(b)/z] =_{C[\mathrm{inr}(b)/z]} d[b/y]}{\Gamma \vdash \eta_{A + B}(u, e):u[e/z] =_{C[e/z]} \mathrm{ind}_{A + B}^C(c[\mathrm{inl}(e)/x], d[\mathrm{inr}(e)/y], e)}$$

The paradigmatic example of conversional equality is a pair of terms like "$(\lambda x. x+x)(2)$" and "$2+2$", where the second is obtained by $\beta$-reduction from the first.  In a type theory that includes definitions by [[recursion]], expansion of a recursor is also computational equality. For instance, if addition is defined by recursion, then "$2+2$" (that is, $s(s(0))+s(s(0))$) reduces via this rule to "$4$" (that is, $s(s(s(s(0))))$).

## Contextual conversion rules

There are also **contextual conversion rules**. These differ from the usual beta-conversion rules in that in that there is an additional context member $\Delta$ attached to the end of the context $\Gamma, x:A$ so that the full context becomes $\Gamma, x:A, \Delta$. By definition, $\Delta$ is dependent upon $x:A$, and the conclusion usually involves substituting $x:A$ by some given term $a:A$ in the context, becoming $\Gamma, \Delta[a/x]$. 

For example, using the example of the [[beta-conversion]] rule for the [[dependent product type]], the contextual beta-conversion rules are given by the following:

* Judgmental contextual beta-conversion rules for dependent product types:

$$\frac{\Gamma, x:A, \Delta \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma, \Delta[a/x] \vdash \lambda(x:A).b(x)(a) \equiv b[a/x]:B[a/x]}$$

* Propositional contextual beta-conversion rules for dependent product types:

$$\frac{\Gamma, x:A, \Delta \vert \Phi \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma, \Delta[a/x] \vert \Phi[a/x] \vdash \lambda(x:A).b(x)(a) \equiv_{B[a/x]} b[a/x] \; \mathrm{true}}$$

* Typal contextual beta-conversion rules for dependent product types:

$$\frac{\Gamma, x:A, \Delta \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma, \Delta[a/x] \vdash \beta_\Pi:\lambda(x:A).b(x)(a) =_{B[a/x]} b[a/x]}$$

Similarly, one could define contextual eta-conversion rules for the [[sum type]]:

* Judgmental contextual eta-conversion rules for sum types:

$$\frac{\Gamma, z:A + B, \Delta \vdash C \; \mathrm{type} \quad \Gamma, x:A, \Delta[\mathrm{inl}(x)/z] \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B, \Delta[\mathrm{inr}(y)/z] \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B \quad \Gamma, z:A + B, \Delta \vdash u:C \quad \Gamma, a:A, \Delta[\mathrm{inl}(a)/z] \vdash u[\mathrm{inl}(a)/z] \equiv c[a/x]:C[\mathrm{inl}(a)/z] \quad \Gamma, b:B, \Delta[\mathrm{inr}(b)/z] \vdash u[\mathrm{inr}(b)/z] \equiv d[b/y]:C[\mathrm{inr}(b)/z]}{\Gamma, \Delta[e/z] \vdash u[e/z] \equiv \mathrm{ind}_{A + B}^C(c[\mathrm{inl}(e)/x], d[\mathrm{inr}(e)/y], e):C[e/z]}$$

* Propositional contextual eta-conversion rules for sum types:

$$\frac{\Gamma, z:A + B, \Delta \vert \Phi \vdash C \; \mathrm{type} \quad \Gamma, x:A, \Delta[\mathrm{inl}(x)/z] \vert \Phi[\mathrm{inl}(x)/z] \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B, \Delta[\mathrm{inr}(y)/z] \vert \Phi[\mathrm{inr}(y)/z] \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B \quad \Gamma, z:A + B, \Delta \vert \Phi \vdash u:C \quad \Gamma, a:A, \Delta[\mathrm{inl}(a)/z] \vert \Phi[\mathrm{inl}(a)/z] \vdash u[\mathrm{inl}(a)/z] \equiv_{C[\mathrm{inl}(a)/z]} c[a/x] \; \mathrm{true} \quad \Gamma, b:B, \Delta[\mathrm{inr}(b)/z] \vert \Phi[\mathrm{inr}(b)/z] \vdash u[\mathrm{inr}(b)/z] \equiv_{C[\mathrm{inr}(b)/z]} d[b/y] \; \mathrm{true}}{\Gamma, \Delta[e/z] \vert \Phi[e/z] \vdash u[e/z] \equiv_{C[e/z]} \mathrm{ind}_{A + B}^C(c[\mathrm{inl}(e)/x], d[\mathrm{inr}(e)/y], e) \; \mathrm{true}}$$

* Typal contextual eta-conversion rules for sum types:

$$\frac{\Gamma, z:A + B, \Delta \vdash C \; \mathrm{type} \quad \Gamma, x:A, \Delta[\mathrm{inl}(x)/z] \vdash c:C[\mathrm{inl}(x)/z] \quad \Gamma, y:B, \Delta[\mathrm{inr}(y)/z] \vdash d:C[\mathrm{inr}(y)/z] \quad \Gamma \vdash e:A + B \quad \Gamma, z:A + B, \Delta \vdash u:C \quad \Gamma, a:A, \Delta[\mathrm{inl}(a)/z] \vdash i_\mathrm{inl}(u):u[\mathrm{inl}(a)/z] =_{C[\mathrm{inl}(a)/z]} c[a/x] \quad \Gamma, b:B, \Delta[\mathrm{inr}(b)/z] \vdash i_\mathrm{inr}(u):u[\mathrm{inr}(b)/z] =_{C[\mathrm{inr}(b)/z]} d[b/y]}{\Gamma, \Delta[e/z] \vdash \eta_{A + B}(u, e):u[e/z] =_{C[e/z]} \mathrm{ind}_{A + B}^C(c[\mathrm{inl}(e)/x], d[\mathrm{inr}(e)/y], e)}$$

## See also

* [[formation rule]], [[introduction rule]], [[elimination rule]]
* [[beta-conversion]], [[eta-conversion]]
* [[inductive definition]]
* [[equality]]

## References

Contextual dependent product types and contextual identity types are defined in the appendix of:

* [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

where the computation rules are contextual computation rules. 

[[!redirects conversion rule]]
[[!redirects conversion rules]]
[[!redirects computation rule]]
[[!redirects computation rules]]
[[!redirects uniqueness rule]]
[[!redirects uniqueness rules]]

[[!redirects contextual conversion rule]]
[[!redirects contextual conversion rules]]
[[!redirects contextual computation rule]]
[[!redirects contextual computation rules]]
[[!redirects contextual uniqueness rule]]
[[!redirects contextual uniqueness rules]]

[[!redirects conversional identity]]
[[!redirects conversional identities]]
[[!redirects conversional equality]]
[[!redirects conversional equalities]]

[[!redirects computational identity]]
[[!redirects computational identities]]
[[!redirects computational equality]]
[[!redirects computational equalities]]