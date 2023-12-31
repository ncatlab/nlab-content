
\tableofcontents

## Idea

There are a few different types which can be called *path types* or *path space types* in [[dependent type theory]]:

* The [[identity type]] $x =_A y$ for type $A$ and elements $x:A$ and $y:A$, which is the type of paths between $x:A$ and $y:A$;

* The [[dependent sum type]] $\sum_{x:A} \sum_{y:A} x =_A y$, which is the type of all paths in $A$; reflexivity is given by the [[diagonal function]];

* The [[function type]] $\mathbb{I} \to A$ from the [[interval type]] $\mathbb{I}$ to type $A$; reflexivity is given by the [[constant functions]] in $\mathbb{I} \to A$ - this parallels the topological definition of [[path spaces]] as continuous functions out of the [[unit interval]];

* In [[cubical type theory]], the [[cubical path type]] $\mathrm{path}_A(x, y)$ for type $A$ and elements $x:A$ and $y:A$ - this is notated similarly to the identity type but also behaves as function types from the predefined interval primitive in addition to the behavior of identity types. 

In this article, we shall talk about path types in the second and third senses, as the other two notions of path type have their own articles in [[identity type]] and [[cubical path type]]. Both the dependent sum type $\sum_{x:A} \sum_{y:A} x =_A y$ and the function type $\mathbb{I} \to A$ are [[copies]] of the type $A$, and one could thus present either as a positive or negative copy of $A$, and then prove the [[J-rule]] for identity types $x =_A y$. 

## Path types as dependent sum types

### As a positive copy

For the dependent sum type $\sum_{x:A} \sum_{y:A} x =_A y$, path induction is just the [[uncurrying]] of the J-rule, which states that $\sum_{x:A} \sum_{y:A} x =_A y$ is a [[positive copy]] of $A$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} \sum_{y:A} x =_A y \vdash C(z) \; \mathrm{type} \quad t:\prod_{x:A} C(\Delta_A(x))}{\Gamma \vdash \mathrm{ind}_{\sum_{x:A} \sum_{y:A} x =_A y}(t):\prod_{z:\sum_{x:A} \sum_{y:A} x =_A y} C(z)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\sum_{x:A} \sum_{y:A} x =_A y \vdash C(z) \; \mathrm{type} \quad t:\prod_{x:A} C(\Delta_A(x))}{\Gamma, x:A \vdash \mathrm{ind}_{\sum_{x:A} \sum_{y:A} x =_A y}(t, \Delta_A(x)) \equiv t(x):C(\Delta_A(x))}$$

### As a negative copy

Since the path type of $A$ are positive copies of $A$, one could equivalently present path types as [[negative copy types]] of $A$, and prove path induction:

* For dependent sum types $\sum_{x:A} \sum_{y:A} x =_A y$, the inference rules are given as follows:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\sum_{x:A} \sum_{y:A} x =_A y \vdash \Delta_A^{-1}(p):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \Delta_A^{-1}(\Delta_A(x)) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\sum_{x:A} \sum_{y:A} x =_A y \vdash \Delta_A(\Delta_A^{-1}(p)) \equiv p:\sum_{x:A} \sum_{y:A} x =_A y}$$

## Path types as function types

### As a positive copy

For function types from the interval type, path induction says that the function type $\mathbb{I} \to A$ is a [[positive copy]] of $A$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathbb{I} \to A \vdash C(z) \; \mathrm{type} \quad t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)}{\Gamma \vdash \mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{z:\mathbb{I} \to A} C(z)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, z:\mathbb{I} \to A \vdash C(z) \; \mathrm{type} \quad t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)}{\Gamma, x:A \vdash \mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)}$$

These versions of path induction are provable from each other: 

\begin{theorem}
Suppose that path induction for function types out of the interval type is true. Then the J-rule is true: given a type $A$ and given a type family $C(x, y, p)$ indexed by $x:A$, $y:A$, and $p:x =_A y$, and a dependent function $t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))$, one could construct a dependent function

$$\mathrm{ind}_{=, A}(t):\prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} C(x, y, p)$$

such that for all $x:A$, 

$$J(t, x, x, \mathrm{refl}_A(x)) \equiv t(x)$$
\end{theorem}

\begin{proof}
By path induction on the type family $C(f(0), f(1), \mathrm{toeq}_A(f))$ indexed by $f:\mathbb{I} \to A$, we can construct a dependent function

$$\mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{f:\mathbb{I} \to A} C(f(0), f(1), \mathrm{toeq}_A(f))$$

such that for all $x:A$,

$$\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)$$ 

since by definition of constant function and reflexivity, one has

$$(\lambda i:\mathbb{I}.x)(0) \equiv x \quad (\lambda i:\mathbb{I}.x)(1) \equiv x \quad \mathrm{ap}_{\lambda i:\mathbb{I}.x}(\mathcal{p}) \equiv \mathrm{refl}_A(x)$$

We define 

$$J(t, x, y, p) \equiv \mathrm{ind}_{\mathbb{I} \to A}(t, \mathrm{rec}_\mathbb{I}^A(x, y, p))$$

since by interval recursion one has a path $\mathrm{rec}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$ such that

$$\mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(0) \equiv x \quad \mathrm{rec}_{\mathbb{I}}^{A}(x, y, p)(1) \equiv y \quad \mathrm{ap}_{\mathrm{rec}_\mathbb{I}^{A}(x, y, p)}(0, 1, \mathcal{p}) \equiv p$$
\end{proof}

### As a negative copy

Since the path type of $A$ are positive copies of $A$, one could equivalently present path types as [[negative copy types]] of $A$, and prove path induction:

* For function types $\mathbb{I} \to A$, the inference rules are given as follows:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \mathrm{const}_{\mathrm{I}, A}^{-1}(p):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \mathrm{const}_{\mathrm{I}, A}^{-1}(\lambda i:\mathbb{I}.x) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathbb{I} \to A \vdash \lambda i:\mathbb{I}.\mathrm{const}_{\mathrm{I}, A}^{-1}(p) \equiv p:\mathbb{I} \to A}$$

\begin{theorem}
Suppose that the path type $\mathbb{I} \to A$ is a negative copy of $A$. 

Then path induction holds: given any type $A$, and any type family $C(p)$ indexed by paths $p:\mathbb{I} \to A$ in $A$, and given any dependent function $t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)$ which says that for all elements $x:A$,  there is an element of the type defined by substituting the constant path of $x:A$ into $C$, $C(\lambda i:\mathbb{I}.x)$, one could construct a dependent function $\mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{z:\mathbb{I} \to A} C(z)$ such that for all $x:A$, $\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)$. 
\end{theorem}

$\mathrm{ind}_{\mathbb{I} \to A}(t)$ is defined to be

$$\mathrm{ind}_{\mathbb{I} \to A}(t) \equiv \lambda p:\mathbb{I} \to A.t(\mathrm{const}_{\mathbb{I}, A}^{-1}(p))$$

and by the computation rules of path types as negative copies, one has that for all $x:A$, 

$$\mathrm{const}_{\mathbb{I}, A}^{-1}(\lambda i:\mathbb{I}.x) \equiv x$$

and so by definition of $\mathrm{ind}_{\mathbb{I} \to A}(t)$ and the judgmental congruence rules for substitution, one has

$$\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(\mathrm{const}_{\mathbb{I}, A}^{-1}(\lambda i:\mathbb{I}.x)) \equiv t(x)$$

### Constructing identity types from path types

Usually, the [[recursion principle]] of the [[interval type]] is interpreted as a way to construct paths $p:\mathbb{I} \to A$ from elements $x:A$ and $y:A$ and identification $p:x =_A y$. Interpreted another way, the recursion principle of the interval type are the negative elimination and computation rules for [[identity types]], allowing one to define identity types as negative types:

* The formation rule of equality types state that given a type $A$ and elements $x:A$ and $y:A$, one could form the equality type $x =_A y$. 

* The introduction rule of equality types state that given a type $A$ and a path $p:\mathbb{I} \to A$, one could construct an equality $\mathrm{toeq}_A(f):f(0) =_A f(1)$. Normally, this would be [[function application to identifications|function application]] to the canonical identification $\mathcal{p}:0 =_\mathbb{I} 1$, but here we haven't defined $\mathcal{p}$ yet since we haven't defined the identity type yet, and with this rule one could define said identification to be the equality of the identity function on the interval type
$$\mathcal{p} \equiv \mathrm{toeq}_A(\mathrm{id}_\mathbb{I})$$

* The elimination rule of equality types state that given a type $A$, elements $x:A$ and $y:A$, and equality $p:x =_A y$, one could construct a path $\mathrm{topath}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$. This is just another name for the recursor of the interval type $\mathrm{rec}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A$

* The three computation rules of equality types state that given a type $A$, elements $x:A$ and $y:A$, and equality $p:x =_A y$, 
$$\mathrm{topath}_\mathbb{I}^A(x, y, p)(0) \equiv x \quad \mathrm{topath}_\mathbb{I}^A(x, y, p)(1) \equiv y \quad \mathrm{toeq}_{A}(\mathrm{topath}_\mathbb{I}^A(x, y, p)) \equiv p$$

* The uniqueness rule of equality types state that given a type $A$ and a path $p:\mathbb{I} \to A$,
$$\mathrm{topath}_\mathbb{I}^A(p(0), p(1), \mathrm{toeq}_A(p)) \equiv p$$

Syntactically, this is given by the following [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A, y:A \vdash x =_A y \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:\mathbb{I} \to A}{\Gamma \vdash \mathrm{toeq}_A(f):f(0) =_A f(1)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p):\mathbb{I} \to A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p)(0) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(x, y, p)(1) \equiv y:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A \quad \Gamma \vdash y:A \quad \Gamma \vdash p:x =_A y}{\Gamma \vdash \mathrm{toeq}_{A}(\mathrm{topath}_\mathbb{I}^A(x, y, p)) \equiv p:x =_A y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:\mathbb{I} \to A}{\Gamma \vdash \mathrm{topath}_\mathbb{I}^A(f(0), f(1), \mathrm{toeq}_A(f)) \equiv f:\mathbb{I} \to A}$$

## Categorical semantics

The [[categorical semantics]] of path types in any of the above forms is the [[path space object]]. 

## Related concepts

* [[heterogeneous path type]] 

* [[identity type]]

* [[cubical path type]]

[[!redirects path type]]
[[!redirects path types]]

[[!redirects weak path type]]
[[!redirects weak path types]]
[[!redirects strict path type]]
[[!redirects strict path types]]

[[!redirects path space type]]
[[!redirects path space types]]

[[!redirects weak path space type]]
[[!redirects weak path space types]]
[[!redirects strict path space type]]
[[!redirects strict path space types]]

[[!redirects path induction]]
[[!redirects path elimination]]
[[!redirects path computation]]