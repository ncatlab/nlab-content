
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

## Idea

In the same way that one could define [[equivalence types]] as types of [[one-to-one correspondences]] and [[function types]] as types of [[anafunctions]], one could define partial function types as types of [[partial anafunctions]]. 

Partial anafunctions are [[type families]] $x\colon A, y \colon B \vdash R(x, y) \; \mathrm{type}$ which comes with a family of witnesses 
$$x \colon A \vdash p(x) \colon \mathrm{isProp}\left(\sum_{y:B} R(x, y) \right)$$
that for each [[term|element]] $x\colon A$, the [[dependent sum type]] $\sum_{y \colon B} R(x, y)$ is a [[mere proposition]]. From every partial anafunction, one could derive the [[partial function]] 
$$x:A, p:\sum_{y:B} R(x, y) \vdash f(x, p):B$$
and for every [[mere proposition]]-valued type family $x:A \vdash P(x)$ and every [[partial function]] $x:A, p:P(x), \vdash f(x, p):B$, one could define the [[partial anafunction]] $x:A, y:B \vdash R(x, y)$ as
$$R(x, y) \coloneqq \sum_{p:P(x)} f(x, p) =_B y$$

Defining partial function types requires both [[identity types]] and [[indexed heterogeneous identity types]] being defined first, which we shall write as $a =_A b$ and $x =_{B}^{p} y$ respectively for $a:A$, $b:A$, $p:a =_A b$, $x:B(a)$, and $y:B(b)$. We use the notation $A \rightharpoonup B$ to represent the type of partial functions between $A$ and $B$. 

## Rules for partial function types

The rules for partial function types are as follows:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \rightharpoonup B \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \rightharpoonup B, x:A, y:B \vdash \mathcal{P}_{A, B}(f, x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{type} \quad \Gamma, x:A, p:P(x), q:P(x) \vdash \tau_{-1}(x, p, q):p =_{P(x)} q \quad \Gamma, x:A, p:P(x) \vdash f(x, p):B}{\Gamma \vdash (x, p) \mapsto f(x, p):A \rightharpoonup B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{type} \quad \Gamma, x:A, p:P(x), q:P(x) \vdash \tau_{-1}(x, p, q):p =_{P(x)} q \quad \Gamma, x:A, p:P(x) \vdash f(x, p):B}{\Gamma, x:A, p:P(x) \vdash \alpha(x, p):\mathcal{P}_{A, B}((x, p) \mapsto f(x, p), x, f(x, p))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{type} \quad \Gamma, x:A, p:P(x), q:P(x) \vdash \tau_{-1}(x, p, q):p =_{P(x)} q}{\Gamma, f:A \rightharpoonup B, x:A, p:P(x) \vdash \mathrm{ev}(f, x, p):B}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, x:A \vdash P(x) \; \mathrm{type} \quad \Gamma, x:A, p:P(x), q:P(x) \vdash \tau_{-1}(x, p, q):p =_{P(x)} q}{\Gamma, f:A \rightharpoonup B, x:A, p:P(x) \vdash \beta(f, x, p):\mathcal{F}_{A, B}(f, x, \mathrm{ev}(f, x, p))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \rightharpoonup B, x:A, y:B, u:\mathcal{P}_{A, B}(f, x, y), z:B, v:\mathcal{P}_{A, B}(f, x, z) \vdash \kappa(f, x, y, u, z, v):y =_B z}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \rightharpoonup B, x:A, y:B, u:\mathcal{P}_{A, B}(f, x, y), z:B, v:\mathcal{P}_{A, B}(f, x, z) \vdash \eta(f, x, y, u, z, v):u =_{\mathcal{P}_{A, B}(f, x)}^{\kappa(f, x, y, u, z, v)} v}$$

By the rules for [[dependent sum types]] and [[dependent product types]], one could derive that 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, f:A \rightharpoonup B \vdash \eta(f):\prod_{x:A} \mathrm{isProp}\left(\sum_{y:B} \mathcal{P}_{A, B}(f, x, y) \right)}$$

which is precisely the statement that $\mathcal{P}_{A, B}(f)$ is a [[partial anafunction]] for all [[partial functions]] $f:A \rightharpoonup B$. 

## See also

* [[partial function]], [[partial anafunction]]
* [[function type]], [[dependent function type]]
* [[equivalence type]]

[[!redirects partial function type]]
[[!redirects partial function types]]