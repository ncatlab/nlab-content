
\tableofcontents

## Idea

The **principle of [[interval type]] localization** states that for all types $A$, $A$ is $\mathbb{I}$-[[localization of a type|local]], or equivalently that the function 
$$\mathrm{const}_{A, \mathbb{I}} \equiv \lambda x:A.\lambda i:\mathbb{I}.x:A \to (\mathbb{I} \to A)$$
is an [[equivalence of types]].

There is also a **definitional interval type localization** which says that the function
$$\mathrm{const}_{A, \mathbb{I}} \equiv \lambda x:A.\lambda i:\mathbb{I}.x:A \to (\mathbb{I} \to A)$$
is a [[definitional isomorphism]]. The usual notion of interval type localization can be called **propositional interval type localization**. 

One has the following analogies between localization at a specific type and the type theoretic letter rule that it proves:

| localization rule | type theoretic letter rule |
|-------------------|----------------------------|
| [[I-localization|$\mathbb{I}$-localization]] | [[J-rule]] |
| [[S1-localization|$S^1$-localization]] | [[K-rule]] |

## Axiom of interval type localization

In [[Martin-Löf type theory]], interval type localization is a provable statement from the [[J-rule]] and the [[recursion principle]] of the [[interval type]]. However, in other dependent type theories where [[identity types]] are defined in terms of the interval type, **interval type localization** can be added as a separate axiom to the type theory as an alternative to the [[J-rule]], because it implies the [[J-rule]]. 

Suppose that one has an [[interval type]] $\mathbb{I}$, with elements $0:\mathbb{I}$ and $1:\mathbb{I}$. 

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathbb{I} \; \mathrm{type}}$$

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 0:\mathbb{I}} \quad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash 1:\mathbb{I}}$$

Usually, the [[recursion principle]] of the [[interval type]] is interpreted as a way to construct, from elements $x:A$ and $y:A$ and identification $p:x =_A y$, paths $p:\mathbb{I} \to A$, aka functions from the interval type to $A$. Interpreted another way, the recursion principle of the interval type are the negative elimination and computation rules for [[identity types]], allowing one to define identity types as [[negative types]]. 

* The formation rule of identity types state that given a type $A$ and elements $x:A$ and $y:A$, one can form the identity type $x =_A y$. Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, y:A \vdash x =_A y \; \mathrm{type}}$$

* The introduction rule of identity types state that given a type $A$ and a path $p:\mathbb{I} \to A$, one can construct an [[identification]] $\mathrm{toId}_A(f):f(0) =_A f(1)$. Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:\mathbb{I} \to A}{\Gamma \vdash \mathrm{toId}_A(f):f(0) =_A f(1)}$$

Normally, this would be [[function application to identifications|function application]] to the canonical identification $\mathcal{p}:0 =_\mathbb{I} 1$, but here we haven't defined $\mathcal{p}$ yet since we haven't defined the identity type yet, and with this rule one can define said identification to be the identification of the identity function on the interval type
$$\mathcal{p} \equiv \mathrm{toId}_\mathbb{I}(\mathrm{id}_\mathbb{I}):0 =_\mathbb{I} 1$$
In addition, reflexivity of an element $x:A$ is given by sending the constant path of $x:A$ to its equality

$$\mathrm{refl}_A(x) \equiv \mathrm{toId}_{A}(\lambda i:\mathbb{I}.x):x =_A x$$

* The elimination rule of identity types state that given a type $A$, elements $x:A$ and $y:A$, and identification $p:x =_A y$, one can construct a path $\mathrm{topath}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$. Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A}$$

This is just another name for the recursor of the interval type $\mathrm{rec}_\mathbb{I}^A(x, y, p) \equiv \mathrm{topath}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$.

* The three computation rules of identity types state that given a type $A$, elements $x:A$ and $y:A$, and identification $p:x =_A y$, 
$$\mathrm{topath}_\mathbb{I}^A(x, y, p)(0) \equiv x \quad \mathrm{topath}_\mathbb{I}^A(x, y, p)(1) \equiv y \quad \mathrm{toId}_{A}(\mathrm{topath}_\mathbb{I}^A(x, y, p)) \equiv p$$
Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p)(0) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p)(1) \equiv y:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{toId}_{A}(\mathrm{topath}_\mathbb{I}^A(x, y, p)) \equiv p:x =_A y}$$

* The uniqueness rule of identity types state that given a type $A$ and a path $p:\mathbb{I} \to A$,
$$\mathrm{topath}_\mathbb{I}^A(p(0), p(1), \mathrm{toId}_A(p)) \equiv p$$

Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:\mathbb{I} \to A}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(f(0), f(1), \mathrm{toId}_A(f)) \equiv f:\mathbb{I} \to A}$$

Then **$\mathrm{I}$-localization** is given by the following axiom:

$$\prod_{A:\mathrm{type}} \sum_{g:(\mathbb{I} \to A) \to A} \left(\prod_{x:A} g(\lambda i:\mathbb{I}.x) =_A x\right) \times \left(\prod_{p:\mathbb{I} \to A} \lambda i:\mathbb{I}.g(p) =_{\mathbb{I} \to A} p\right)$$

While this states that $\mathrm{const}_{A, \mathbb{I}}$ is only a [[quasi-invertible function]], it is well known that every quasi-invertible function can be made into a [[coherently invertible function]] by constructing a new [[section]] or [[retraction]] which satisfies a suitable family of [[naturality squares]]. 

If the dependent type theory does not have [[type universes]], then the axiom of $\mathrm{I}$-localization needs to be expressed as an inference rule:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \sum_{g:(\mathbb{I} \to A) \to A} \left(\prod_{x:A} g(\lambda i:\mathbb{I}.x) =_A x\right) \times \left(\prod_{p:\mathbb{I} \to A} \lambda i:\mathbb{I}.g(p) =_{\mathbb{I} \to A} p\right)}$$

and if the dependent type theory does not have [[dependent sum types]], then this would have to be expressed as three separate rules:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \mathrm{const}_{A, \mathrm{I}}^{-1}(p):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \beta_{\mathbb{I} \to A}(x):\mathrm{const}_{A, \mathrm{I}}^{-1}(\lambda i:\mathbb{I}.x) =_{A} x}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \eta_{\mathbb{I} \to A}(p):\lambda i:\mathbb{I}.\mathrm{const}_{A, \mathrm{I}}^{-1}(p) =_{\mathbb{I} \to A} p}$$

**Definitional $\mathrm{I}$-localization** is given by the following rules:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \mathrm{const}_{A, \mathrm{I}}^{-1}(p):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \mathrm{const}_{A, \mathrm{I}}^{-1}(\lambda i:\mathbb{I}.x) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \lambda i:\mathbb{I}.\mathrm{const}_{A, \mathrm{I}}^{-1}(p) \equiv p:\mathbb{I} \to A}$$

This makes $\mathrm{const}_{A, \mathbb{I}}$ into a [[definitional isomorphism]], which is always a coherently invertible function.

### Interval type localization implies the J-rule

The [[function application to identifications]] can be defined without the use of path induction:

\begin{theorem}
Given types $A$ and $B$, a a function $f:A \to B$, elements $x:A$ and $y:A$ and an identification $p:x =_A y$, one can construct the identification $\mathrm{ap}_f(x, y, p):f(x) =_B f(y)$. 
\end{theorem}

This is defined through the inference rules for identity types and function composition: 

$$\mathrm{ap}_f(x, y, p) \equiv \mathrm{toId}_B(f \circ \mathrm{rec}_\mathbb{I}^A(x, y, p)):f(x) =_B f(y)$$

\begin{theorem}
Suppose that every type $A$ is definitionally $\mathbb{I}$-local.

Then path induction for function types out of the interval type holds: given any type $A$, and any type family $C(p)$ indexed by paths $p:\mathbb{I} \to A$ in $A$, and given any dependent function $t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)$ which says that for all elements $x:A$,  there is an element of the type defined by substituting the constant path of $x:A$ into $C$, $C(\lambda i:\mathbb{I}.x)$, one can construct a dependent function $\mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{z:\mathbb{I} \to A} C(z)$ such that for all $x:A$, $\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)$. 
\end{theorem}

\begin{proof}
$\mathrm{ind}_{\mathbb{I} \to A}(t)$ is defined to be

$$\mathrm{ind}_{\mathbb{I} \to A}(t) \equiv \lambda p:\mathbb{I} \to A.t(\mathrm{const}_{A, \mathrm{I}}^{-1}(p))$$

and by the computation rules of path types as negative copies, one has that for all $x:A$, 

$$\mathrm{const}_{A, \mathrm{I}}^{-1}(\lambda i:\mathbb{I}.x) \equiv x$$

and so by definition of $\mathrm{ind}_{\mathbb{I} \to A}(t)$ and the judgmental congruence rules for substitution, one has

$$\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(\mathrm{const}_{A, \mathrm{I}}^{-1}(\lambda i:\mathbb{I}.x)) \equiv t(x)$$
\end{proof}

\begin{theorem}
Suppose that path induction for function types out of the interval type is true. 

Then the J-rule is true: given a type $A$ and given a type family $C(x, y, p)$ indexed by $x:A$, $y:A$, and $p:x =_A y$, and a dependent function $t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))$, one can construct a dependent function

$$\mathrm{ind}_{=, A}(t):\prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} C(x, y, p)$$

such that for all $x:A$, 

$$J(t, x, x, \mathrm{refl}_A(x)) \equiv t(x)$$
\end{theorem}

\begin{proof}
By path induction on the type family $C(f(0), f(1), \mathrm{toId}_A(f))$ indexed by $f:\mathbb{I} \to A$, we can construct a dependent function

$$\mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{f:\mathbb{I} \to A} C(f(0), f(1), \mathrm{toId}_A(f))$$

such that for all $x:A$,

$$\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)$$ 

since by definition of constant function and reflexivity, one has

$$(\lambda i:\mathbb{I}.x)(0) \equiv x \quad (\lambda i:\mathbb{I}.x)(1) \equiv x \quad \mathrm{ap}_{\lambda i:\mathbb{I}.x}(\mathcal{p}) \equiv \mathrm{refl}_A(x)$$

We define 

$$J(t, x, y, p) \equiv \mathrm{ind}_{\mathbb{I} \to A}(t, \mathrm{rec}_\mathbb{I}^A(x, y, p))$$

since by interval recursion one has a path $\mathrm{rec}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$ such that

$$\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(0) \equiv x \quad \mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(1) \equiv y \quad \mathrm{ap}_{\mathrm{rec}_\mathbb{I}^{A}(x, y, p)}(0, 1, \mathcal{p}) \equiv p$$
\end{proof}

## Related concepts

* [[identity type]], [[J-rule]]

* [[loop space type]], [[K-rule]], [[circle type localization]]

[[!redirects interval type localization]]
[[!redirects I localization]]
[[!redirects I-localization]]

[[!redirects axiom of interval type localization]]
[[!redirects axiom of I localization]]
[[!redirects axiom of I-localization]]