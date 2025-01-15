> This page is about the notion in [[homotopy type theory|homotopy]] [[type theory]]. For *[[parallel transport]]* via [[connections]] in [[differential geometry]] see there. For the relation see [below](#RelationToParallelTransport).

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##
 {#Idea}

[[Gottfried Leibniz]] said (in translation from [Lewis 1918, p. 373](#Lewis18) with original Latin terms in parenthesis; see also [Cartwright 1971, p. 119](#Cartwright71) and [Gries & Schneider 1998](#GriesSchneider98))

> Two terms are the same (eadem) if one can be substituted for the otherwithout altering the truth of any statement (salva veritate). If we have $P$ and $Q$, and $P$ enters into some true proposition, and the substitution of $Q$ for $P$ wherever it appears results in a new proposition that is likewise true, and if this can be done for every proposition, then $P$ and $Q$ are said to be the same; conversely, if $P$ and $Q$ are the same, they can be substituted for one another.

The converse mentioned at the end of the last sentence is known as the **principle of substitution** or the **indiscernibility of identicals**. In any simply typed first-order theory, given a predicate $P$ on $T$, this principle is formalized as the following

$$
  \forall_{x,y\colon T} (x =_T y) \implies (P(x) \iff P(y))
$$

In the interpretation of [[propositions as types]] in [[type theory]], [[propositions]] are interpreted as [[types]], and the above statement has a generalization from the types which are propositions to all types: the [[universal quantifier]] becomes a [[dependent product type]], the [[predicate]] becomes a [[type family]], [[implication]] becomes a [[function type]], and [[logical equivalence]] of [[propositions]] becomes an [[equivalence type]]. This results in what is known as *transport* in type theory, which for the type $T$ and the type family $x:T \vdash P(x)$ results in the [[dependent function]]:

\[
  \label{TheTransportFunctions}
  \mathrm{tr}_P
  \;\colon\;
  \prod_{x,y:T} (x =_T y) \to (P(x) \simeq P(y))
  \,.
\]

## Definitions

There are actually two notions of transport in dependent type theory. One notion of transport is transport across the identification $p:a =_A b$ for elements $a:A$ and $b:A$. The other notion of transport is transport across the path $p:\mathbb{I} \to A$. These two are interchangeable through the [[recursion principle]] and uniqueness principle of the [[interval type]]. 

Similarly, there are multiple notions of [[equivalence types]] in [[dependent type theory]], which can be used for a definition of univalence for a [[type universe]] $U$; these include

* [[definitional isomorphism types]]
* various notions of (weak) [[equivalence types]]
  * the type of [[functions]] with [[contractible type|contractible]] [[fiber type|fibers]]
  * the type of [[spans]] with contractible fibers
  * the type of [[multivalued partial functions]] which are single-valued and [[total function|total]] and have contractible fibers
  * the type of [[one-to-one correspondences]]
* type of $U$-small equivalences, given a type universe $U$ and a definition of equivalence above

The transport equivalence is called **strict transport** **definitional transport** or **judgmental transport** if the equivalence type is a [[definitional isomorphism type]]. It is called **(weak) transport** if the equivalence type is a (weak) [[equivalence type]]. 

### Transport across paths

#### Inductive definition

Given any notion of [[equivalence type]] $A \simeq B$ between types $A$ and $B$, let $\mathrm{id}_A^\simeq$ denote the [[identity equivalence]] on $A$. 

Transport across paths is inductively defined using [[path induction]] for function types $\mathbb{I} \to A$ out of the interval type. Path induction states that 

\begin{theorem}
Given any type $A$, and any type family $C(p)$ indexed by paths $p:\mathbb{I} \to A$ in $A$, and given any dependent function $t:\prod_{x:A} C(\lambda i:\mathbb{I}.x)$ which says that for all elements $x:A$, there is an element of the type defined by substituting the constant path of $x:A$ into $C$, $C(\lambda i:\mathbb{I}.x)$, one can construct a dependent function $\mathrm{ind}_{\mathbb{I} \to A}(t):\prod_{z:\mathbb{I} \to A} C(z)$ such that for all $x:A$, $\mathrm{ind}_{\mathbb{I} \to A}(t, \lambda i:\mathbb{I}.x) \equiv t(x):C(\lambda i:\mathbb{I}.x)$. 
\end{theorem}

Now, given a type family $B(x)$ indexed by $x:A$, there exists a dependent function called **transport** 

$$\mathrm{tr}_{\underline{ }.B(-)}^{(-)}:\prod_{p:\mathbb{I} \to A} B(p(0)) \simeq B(p(1))$$

This is inductively defined by path induction, where for all $x:A$, 

$$\mathrm{tr}_{\underline{ }.B(-)}^{\lambda i:\mathbb{I}.x} \equiv \mathrm{id}_{B(x)}^{\simeq}:B(x) \simeq B(x)$$

#### Using function application and Russell universes

Suppose that the dependent type theory uses a sequence of [[Russell universes]] $U_i$ to define types, instead of a separate type [[judgment]]. Then, given a path $p:\mathbb{I} \to A$, [[transport]] across the type family $B:A \to U_i$ can be defined as the evaluation of the inductively defined function 
$$\mathrm{idtoequiv}(B(p(0)), B(p(1))):(B(p(0)) =_{U_i} B(p(1))) \to (B(p(0)) \simeq B(p(1)))$$
at the function application of $B$ to the path $p$, $\mathrm{ap}_{U_i}(B, p):B(p(0)) =_{U_i} B(p(1))$:

$$\mathrm{transport}(B, p) \equiv \mathrm{idtoequiv}(B(p(0)), B(p(1)))(\mathrm{ap}_{U_i}(B,p)):B(p(0)) \simeq B(p(1))$$

### Transport across identifications

#### Inductive definition

Given any notion of [[equivalence type]] $A \simeq B$ between types $A$ and $B$, let $\mathrm{id}_A^\simeq$ denote the [[identity equivalence]] on $A$. 

Transport across identification is inductively defined using the [[J-rule]]. The J-rule states that 

\begin{theorem}
Given a type $A$ and given a type family $C(x, y, p)$ indexed by $x:A$, $y:A$, and $p:x =_A y$, and a dependent function $t:\prod_{x:A} C(x, x, \mathrm{refl}_A(x))$, one can construct a dependent function

$$\mathrm{ind}_{=, A}(t):\prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} C(x, y, p)$$

such that for all $x:A$, 

$$J(t, x, x, \mathrm{refl}_A(x)) \equiv t(x)$$
\end{theorem}

Now, given a type family $B(x)$ indexed by $x:A$, there exists a dependent function called **transport** 

$$\mathrm{tr}_{\underline{ }.B(-)}^{(-, -, -)}:\prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} B(x) \simeq B(y)$$

This is inductively defined by path induction, where for all $x:A$, 

$$\mathrm{tr}_{\underline{ }.B(-)}^{(x, x, \mathrm{refl}_A(x))} \equiv \mathrm{id}_{B(x)}^{\simeq}:B(x) \simeq B(x)$$

#### Using function application and Russell universes

Suppose that the dependent type theory uses a sequence of [[Russell universes]] $U_i$ to define types, instead of a separate type [[judgment]]. Then, given elements $a:A$, $b:A$, and identification $p:a =_A b$, [[transport]] across the type family $B:A \to U_i$ can be defined as the evaluation of the inductively defined function 
$$\mathrm{idtoequiv}(B(a), B(b)):(B(a) =_{U_i} B(b)) \to (B(a) \simeq B(b))$$
at the function application of $B$ to the identification $p$, $\mathrm{ap}_{U_i}(B, a, b, p):B(a) =_{U_i} B(b)$:

$$\mathrm{transport}(B, a, b, p) \equiv \mathrm{idtoequiv}(B(a), B(b))(\mathrm{ap}_{U_i}(B, a, b, p)):B(a) \simeq B(b)$$

## Properties

### Transport across paths

The type of families of transport functions on a [[type family]] $x:A \vdash B(x)$ is given by the type 

$$\prod_{p:\mathbb{I} \to A} \sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$

where $x =_{x:A.B(x)}^{p} y$ is a [[heterogeneous identity type]] defined using paths. 

In general, a family of transport functions is an element of this type. However, any element of the type of families of transport functions is unique up to identification:

\begin{theorem}
The type of families of transport functions 

$$\prod_{p:\mathbb{I} \to A} \sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$

is a [[contractible type]].
\end{theorem}

\begin{proof}
We first show that the type 

$$\sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$

is contractible for all $p:\mathbb{I} \to A$. By [[path induction]], it suffices to show that the type 

$$\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{x:A.B(x)}^{\lambda i:\mathbb{I}.a} f(x)$$

is contractible for all $a:A$. There is an equivalence of types

$$(x =_{x:A.B(x)}^{\lambda i:\mathbb{I}.a} f(x)) \simeq (x =_{B(a)} f(x))$$

and thus by the typal congruence rules for dependent function types and dependent pair types, there is an equivalence of types 

$$\left(\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{x:A.B(x)}^{\lambda i:\mathbb{I}.a} f(x)\right) \simeq \left(\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{B(a)} f(x)\right)$$

Now, 

$$\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{B(a)} f(x)$$

is just the [[type of identity functions]] on $B(a)$, and is thus always contractible, which implies that 

$$\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{x:A.B(x)}^{\lambda i:\mathbb{I}.a} f(x)$$

is contractible for all $a:A$. By induction on identity types, the type 

$$\sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$

is contractible for all paths $p:\mathbb{I} \to A$. By [[weak function extensionality]], this implies that 

$$\prod_{p:\mathbb{I} \to A} \sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$

is contractible.
\end{proof} 

Thus, it makes sense to refer to the canonical family of transport functions 

$$\mathrm{transport}_{x:A.B(x)}:\prod_{p:\mathbb{I} \to A} \sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$ 

inductively defined by 

$$\mathrm{transport}_{x:A.B(x)}(\lambda i:\mathbb{I}.a) \equiv \left(\lambda x:B(a).x, \lambda x:B(a).\mathrm{idTohId}(x, (\lambda x:B(a).x)(x), \beta_{B(a) \to B(a)}^{x:B(a).x}(x))\right)$$

for all $a:A$ as *[[generalized the|the]]* transport function on the type family $x:A \vdash B(x)$.

\begin{theorem}
Given a family of transport functions 
$$t:\prod_{p:\mathbb{I} \to A} \sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$
for all $p:\mathbb{I} \to A$, the function $\pi_1(t(p^{-1}))$ is a [[quasi-inverse function]] of $\pi_1(t(p))$, where $p^{-1}$ is the inverse path of $p$. 
$$p^{-1} \coloneqq \mathrm{rec}_\mathbb{I}^A(p(1), p(0), \mathrm{ap}_p(\mathcal{p}^{-1}))$$
\end{theorem}

\begin{proof}
For all paths $p:\mathbb{I} \to A$ and for all $x:B(p(0))$, we have 
$$\pi_2(t(p))(x):x =_{x:A.B(x)}^{p} \pi_1(t(p))(x)$$ 
and for all $y:B(p(1))$ we have
$$\pi_2(t(p^{-1}))(x):x =_{x:A.B(x)}^{p^{-1}} \pi_1(t(p^{-1}))(x)$$ 

Thus, we have
$$\pi_2(t(p))(\pi_1(t(p^{-1}))(y)):\pi_1(t(p^{-1}))(y) =_{x:A.B(x)}^{p} \pi_1(t(p))(\pi_1(t(p^{-1}))(y))$$ 
and 
$$\pi_2(t(p^{-1}))(\pi_1(t(p))(x)):\pi_1(t(p)(x)) =_{x:A.B(x)}^{p^{-1}} \pi_1(t(p^{-1}))(\pi_1(t(p))(x))$$ 

By concatenating heterogeneous identifications, we get
$$\pi_2(t(p))(x) \bullet \pi_2(t(p^{-1}))(\pi_1(t(p))(x)):x =_{x:A.B(x)}^{\mathrm{rec}_\mathbb{I}^A(p(0), p(0), \mathrm{fill}(p,  p^{-1}, \mathrm{refl}_{A}(p(1))} \pi_1(t(p^{-1}))(\pi_1(t(p))(x))$$
and
$$\pi_2(t(p^{-1}))(y) \bullet \pi_2(t(p))(\pi_1(t(p^{-1}))(y)):y =_{x:A.B(x)}^{\mathrm{rec}_\mathbb{I}^A(p(1), p(1), \mathrm{fill}(p^{-1},  p, \mathrm{refl}_{A}(p(0))} \pi_1(t(p))(\pi_1(t(p^{-1}))(y))$$

where 

$$p \bullet p^{-1} \coloneqq \mathrm{rec}_\mathbb{I}^A(p(0), p(0), \mathrm{ap}_p(\mathcal{p}) \bullet \mathrm{ap}_p(\mathcal{p}^{-1}))$$

$$p^{-1} \bullet p \coloneqq \mathrm{rec}_\mathbb{I}^A(p(1), p(1), \mathrm{ap}_p(\mathcal{p}^{-1}) \bullet \mathrm{ap}_p(\mathcal{p}))$$

Since $p \bullet p^{-1} \equiv \lamba i:\mathbb{I}.a$ and $p^{-1} \bullet p \equiv \lamba i:\mathbb{I}.b$, we thus have
$$\pi_2(t(p))(x) \bullet \pi_2(t(p^{-1}))(\pi_1(t(p))(x)):x =_{x:A.B(x)}^{p \bullet p^{-1}} \pi_1(t(p^{-1}))(\pi_1(t(p))(x))$$
and
$$\pi_2(t(p^{-1}))(y) \bullet \pi_2(t(p))(\pi_1(t(p^{-1}))(y)):y =_{x:A.B(x)}^{p^{-1} \bullet p} \pi_1(t(p))(\pi_1(t(p^{-1}))(y))$$

By converting heterogeneous identifications over constant paths, one gets
$$\mathrm{hIdToId}(x, \pi_1(t(p^{-1}))(\pi_1(t(p))(x)), \pi_2(t(p))(x) \bullet \pi_2(t(p^{-1}))(\pi_1(t(p)(x))))):x =_{B(p(0))} \pi_1(t(p^{-1}))(\pi_1(t(p))(x))$$
and
$$\mathrm{hIdToId}(y, \pi_1(t(p))(\pi_1(t(p^{-1}))(y)), \pi_2(t(p^{-1}))(y) \bullet \pi_2(t(p))(\pi_1(t(p^{-1}))(y))):y =_{B(b)} \pi_1(t(p))(\pi_1(t(p^{-1}))(y))$$

Thus, we have shown that $\pi_1(t(p^{-1}))$ is a quasi-inverse function of $\pi_1(t(p))$ for all paths $p:\mathbb{I} \to A$. 
\end{proof}

We define the dependent functions

$$\mathrm{linv}(t, p) \equiv \lambda x:B(p(0)).\mathrm{hIdToId}(x, \pi_1(t(p^{-1}))(\pi_1(t(p))(x)), \pi_2(t(p))(x) \bullet \pi_2(t(p^{-1}))(\pi_1(t(p)(x)))))$$

in type $\prod_{x:B(p(0))} x =_{B(p(0))} \pi_1(t(p^{-1}))(\pi_1(t(p))(x))$

and 

$$\mathrm{rinv}(t, p) \equiv \lambda y:B(p(1)).\mathrm{hIdToId}(y, \pi_1(t(p))(\pi_1(t(p^{-1}))(y)), \pi_2(t(p^{-1}))(y) \bullet \pi_2(t(p))(\pi_1(t(p^{-1}))(y)))$$

in type $\prod_{y:B(p(1))} y =_{B(p(1))} \pi_1(t(p))(\pi_1(t(p^{-1}))(y))$

for all $p:\mathbb{I} \to A$. 

\begin{theorem}
Given a family of transport functions 
$$t:\prod_{p:\mathbb{I} \to A} \sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$
for all $p:\mathbb{I} \to A$, the function $\pi_1(t(p))$ is bi-invertible. 
\end{theorem}

\begin{proof}
We construct the element 

$$((\pi_1(t(p^{-1})), \mathrm{linv}(t, p)), (\pi_1(t(p^{-1})), \mathrm{rinv}(t, p))$$

in the type 

$$\left(\sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{B(p(0))} f(\pi_1(t(p))(x))\right) \times \left(\sum_{g:B(p(1)) \to B(p(0))} \prod_{y:B(p(1))} y =_{B(p(1))} \pi_1(t(p))(g(y))\right)$$

indicating that $\pi_1(t(p))$ is bi-invertible for all $p:\mathbb{I} \to A$. 
\end{proof}

By definition, it follows that:

\begin{corollary}
Given a family of transport functions 
$$t:\prod_{p:\mathbb{I} \to A} \sum_{f:B(p(0)) \to B(p(1))} \prod_{x:B(p(0))} x =_{x:A.B(x)}^{p} f(x)$$
for all $p:\mathbb{I} \to A$, the function $\pi_1(t(p))$ is an [[equivalence of types]]. 
\end{corollary}

Hence, in [[dependent type theory]], transport functions are also called **transport equivalences**.

### Transport across identifications

The type of families of transport functions on a [[type family]] $x:A \vdash B(x)$ is given by the type 

$$\prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} \sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$

where $x =_{x:A.B(x)}^{(a, b, p)} y$ is a [[heterogeneous identity type]] defined using identifications. 

In general, a family of transport functions is an element of this type. However, any element of the type of families of transport functions is unique up to identification:

\begin{theorem}
The type of families of transport functions 

$$\prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} \sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$

is a [[contractible type]].
\end{theorem}

\begin{proof}
We first show that the type 

$$\sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$

is contractible for all $a:A$, $b:A$, and $p:a =_A b$. By induction on identity types, it suffices to show that the type 

$$\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, a, \mathrm{refl}_A(a))} f(x)$$

is contractible for all $a:A$. There is an equivalence of types

$$(x =_{x:A.B(x)}^{(a, a, \mathrm{refl}_A(a))} f(x)) \simeq (x =_{B(a)} f(x))$$

and thus by the typal congruence rules for dependent function types and dependent pair types, there is an equivalence of types 

$$\left(\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, a, \mathrm{refl}_A(a))} f(x)\right) \simeq \left(\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{B(a)} f(x)\right)$$

Now, 

$$\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{B(a)} f(x)$$

is just the [[type of identity functions]] on $B(a)$, and is thus always contractible, which implies that 

$$\sum_{f:B(a) \to B(a)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, a, \mathrm{refl}_A(a))} f(x)$$

is contractible for all $a:A$. By induction on identity types, the type 

$$\sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$

is contractible for all $a:A$, $b:A$, and $p:a =_A b$. By [[weak function extensionality]], this implies that 

$$\prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} \sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$

is contractible.
\end{proof} 

Thus, it makes sense to refer to the canonical family of transport functions 

$$\mathrm{transport}_{x:A.B(x)}:\prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} \sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$ 

inductively defined by 

$$\mathrm{transport}_{x:A.B(x)}(a, a, \mathrm{refl}_A(a)) \equiv \left(\lambda x:B(a).x, \lambda x:B(a).\mathrm{idTohId}(x, (\lambda x:B(a).x)(x), \beta_{B(a) \to B(a)}^{x:B(a).x}(x))\right)$$

for all $a:A$ as *[[generalized the|the]]* transport function on the type family $x:A \vdash B(x)$.

\begin{theorem}
Given a family of transport functions 
$$t:\prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} \sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$
for all $a:A$, $b:A$, and $p:a =_A b$, the function $\pi_1(t(b, a, p^{-1}))$ is a [[quasi-inverse function]] of $\pi_1(t(a, b, p))$. 
\end{theorem}

\begin{proof}
For all $a:A$, $b:A$, and $p:a =_A b$ and for all $x:B(a)$, we have 
$$\pi_2(t(a, b, p))(x):x =_{x:A.B(x)}^{(a, b, p)} \pi_1(t(a, b, p))(x)$$ 
and for all $y:B(b)$ we have
$$\pi_2(t(b, a, p^{-1}))(x):x =_{x:A.B(x)}^{(b, a, p^{-1})} \pi_1(t(b, a, p^{-1}))(x)$$ 

Thus, we have
$$\pi_2(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y)):\pi_1(t(b, a, p^{-1}))(y) =_{x:A.B(x)}^{(a, b, p)} \pi_1(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y))$$ 
and 
$$\pi_2(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x)):\pi_1(t(a, b, p)(x)) =_{x:A.B(x)}^{(b, a, p^{-1})} \pi_1(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x))$$ 

By concatenating heterogeneous identifications, we get
$$\pi_2(t(a, b, p))(x) \bullet \pi_2(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x)):x =_{x:A.B(x)}^{(a, a, p \bullet p^{-1})} \pi_1(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x))$$
and
$$\pi_2(t(b, a, p^{-1}))(y) \bullet \pi_2(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y)):y =_{x:A.B(x)}^{(b, b, p^{-1} \bullet p)} \pi_1(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y))$$

Since $p \bullet p^{-1} \equiv \mathrm{refl}_{A}(a)$ and $p^{-1} \bullet p \equiv \mathrm{refl}_{A}(b)$, we thus have
$$\pi_2(t(a, b, p))(x) \bullet \pi_2(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x)):x =_{x:A.B(x)}^{(a, a, p \bullet p^{-1})} \pi_1(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x))$$
and
$$\pi_2(t(b, a, p^{-1}))(y) \bullet \pi_2(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y)):y =_{x:A.B(x)}^{(b, b, p^{-1} \bullet p)} \pi_1(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y))$$

By converting heterogeneous identifications over reflexivity to homogeneous identifications, one gets
$$\mathrm{hIdToId}(x, \pi_1(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x)), \pi_2(t(a, b, p))(x) \bullet \pi_2(t(b, a, p^{-1}))(\pi_1(t(a, b, p)(x))))):x =_{B(a)} \pi_1(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x))$$
and
$$\mathrm{hIdToId}(y, \pi_1(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y)), \pi_2(t(b, a, p^{-1}))(y) \bullet \pi_2(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y))):y =_{B(b)} \pi_1(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y))$$

Thus, we have shown that $\pi_1(t(b, a, p^{-1}))$ is a quasi-inverse function of $\pi_1(t(a, b, p))$ for all $a:A$, $b:A$, and $p:a =_A b$. 
\end{proof}

We define the dependent functions

$$\mathrm{linv}(t, a, b, p) \equiv \lambda x:B(a).\mathrm{hIdToId}(x, \pi_1(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x)), \pi_2(t(a, b, p))(x) \bullet \pi_2(t(b, a, p^{-1}))(\pi_1(t(a, b, p)(x)))))$$

in type $\prod_{x:B(a)} x =_{B(a)} \pi_1(t(b, a, p^{-1}))(\pi_1(t(a, b, p))(x))$

and 

$$\mathrm{rinv}(t, a, b, p) \equiv \lambda y:B(b).\mathrm{hIdToId}(y, \pi_1(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y)), \pi_2(t(b, a, p^{-1}))(y) \bullet \pi_2(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y)))$$

in type $\prod_{y:B(b)} y =_{B(b)} \pi_1(t(a, b, p))(\pi_1(t(b, a, p^{-1}))(y))$

for all $a:A$, $b:A$, and $p:a =_A b$. 

\begin{theorem}
Given a family of transport functions 
$$t:\prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} \sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$
for all $a:A$, $b:A$, and $p:a =_A b$, the function $\pi_1(t(a, b, p))$ is bi-invertible. 
\end{theorem}

\begin{proof}
We construct the element 

$$((\pi_1(t(b, a, p^{-1})), \mathrm{linv}(t, a, b, p)), (\pi_1(t(b, a, p^{-1})), \mathrm{rinv}(t, a, b, p))$$

in the type 

$$\left(\sum_{f:B(b) \to B(a)} \prod_{x:B(a)} x =_{B(a)} f(\pi_1(t(a, b, p))(x))\right) \times \left(\sum_{g:B(b) \to B(a)} \prod_{y:B(b)} y =_{B(b)} \pi_1(t(a, b, p))(g(y))\right)$$

indicating that $\pi_1(t(a, b, p))$ is bi-invertible for all $a:A$, $b:A$, and $p:a =_A b$. 
\end{proof}

By definition, it follows that:

\begin{corollary}
Given a family of transport functions 
$$t:\prod_{a:A} \prod_{b:A} \prod_{p:a =_A b} \sum_{f:B(a) \to B(b)} \prod_{x:B(a)} x =_{x:A.B(x)}^{(a, b, p)} f(x)$$
for all $a:A$, $b:A$, and $p:a =_A b$, the transport function $\pi_1(t(a, b, p))$ is an [[equivalence of types]]. 
\end{corollary}

Hence, in [[dependent type theory]], transport functions are also called **transport equivalences**.

## Examples and applications

### Univalent Tarski universes

Tarski universes are types which behave like internal models of [[dependent type theory]] inside of the type theory itself. We use a very general notion of Tarski universe: a Tarski universe merely consists of a type of encodings for types $\mathcal{U}$ and a universal type family $\mathcal{T}_\mathcal{U}$. Given an encoding $A:\mathcal{U}$, an internal type family indexed by $A$ is a function $B:\mathcal{T}_\mathcal{U}(A) \to \mathcal{U}$. 

There are two ways to say that $A:\mathcal{U}$ and $B:\mathcal{U}$ are the same, by way of the [[identity type]] of the Tarski universe $A =_\mathcal{U} B$, and by way of the [[equivalence in homotopy type theory|type of equivalences]] between the type reflections of $A:\mathcal{U}$ and $B:\mathcal{U}$, $\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B)$. By [[transport]], there is a canonical function 
$$\mathrm{trans}^{\mathcal{T}_\mathcal{U}}(A, B):(A =_\mathcal{U} B) \to (\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B))$$
The Tarski universe $\mathcal{U}$ is then said to be a [[univalent universe]] if the transport function $\mathrm{trans}^{\mathcal{T}_\mathcal{U}}(A, B)$ is an equivalence of types
$$\mathrm{trans}^{\mathcal{T}_\mathcal{U}}(A, B):(A =_\mathcal{U} B) \simeq (\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B))$$
for all encodings $A:\mathcal{U}$ and $B:\mathcal{U}$. 

One could also internalize the type of equivalences inside of the Tarski universe $\mathcal{U}$, but that requires the Tarski universe be closed under [[identity types]],  [[dependent product types]], and [[dependent sum types]].

A Tarski universe $\mathcal{U}$ is weakly closed under identity types if it has an internal encoding of identity types in the Tarski universe: Given an element $A:\mathcal{U}$, there is a function $\mathrm{Id}_A^\mathcal{U}:\mathcal{T}_\mathcal{U}(A) \times \mathcal{T}_\mathcal{U}(A) \to \mathcal{U}$ and for all elemments $a:\mathcal{T}_\mathcal{U}(A)$ and $b:\mathcal{T}_\mathcal{U}(A)$ an equivalence 
$$\mathrm{canonical}_{\mathrm{Id}_A}(a, b):\mathcal{T}_\mathcal{U}(\mathrm{Id}_A^\mathcal{U}(a, b)) \simeq (a =_{\mathcal{T}_\mathcal{U}(A)} b)$$

A Tarski universe $\mathcal{U}$ is weakly closed under dependent product types if it has an internal encoding of dependent product types in the Tarski universe: given an element $A:\mathcal{U}$ and a function $B:\mathcal{T}_\mathcal{U}(A) \to \mathcal{U}$, there is an element $\Pi_\mathcal{U}(x:A).B(x):\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_\Pi(A, B):\mathcal{T}_\mathcal{U}(\Pi_\mathcal{U}(x:A).B(x)) \simeq \prod_{x:\mathcal{T}_\mathcal{U}(A)} \mathcal{T}_\mathcal{U}(B(x))$$

A Tarski universe $\mathcal{U}$ is weakly closed under dependent sum types if it has an internal encoding of dependent sum types in the Tarski universe: given an element $A:\mathcal{U}$ and a function $B:\mathcal{T}_\mathcal{U}(A) \to \mathcal{U}$, there is an element $\Sigma_\mathcal{U}(x:A).B(x):\mathcal{U}$, and an equivalence
$$\mathrm{canonical}_\Sigma(A, B):\mathcal{T}_\mathcal{U}(\Sigma_\mathcal{U}(x:A).B(x)) \simeq \sum_{x:\mathcal{T}_\mathcal{U}(A)} \mathcal{T}_\mathcal{U}(B(x))$$

Every Tarski universe $\mathcal{U}$ which is weakly closed under identity types, dependent product types, and dependent sum types types has an internal encoding of type of equivalences $A \simeq_\mathcal{U} B$, defined for all $A:\mathcal{U}$ and $B:\mathcal{U}$ as
$$A \simeq_\mathcal{U} B \coloneqq \Sigma_\mathcal{U}(f:A \to_\mathcal{U} B).\mathrm{isEquiv}_\mathcal{U}(f)$$
with $\mathrm{isEquiv}_\mathcal{U}$ defined by whatever suitable definition of [[equivalence in homotopy type theory]]. 

Thus, there is a third way to say that $A:\mathcal{U}$ and $B:\mathcal{U}$ are the same, by way of the type reflection of the internal encoding of the type of equivalences: $\mathcal{T}_\mathcal{U}(A \simeq_\mathcal{U} B)$. It could be proven, from the closure of the universe under identity types, dependent product types, and dependent sum types, that there is an equivalence 
$$\mathrm{canonical}_\simeq(A, B):\mathcal{T}_\mathcal{U}(A \simeq_\mathcal{U} B) \simeq (\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B))$$

There is a more common definition of a univalent Tarski universe: a  Tarski universe $\mathcal{U}$ is a [[univalent universe]] if the canonical function 
$$\mathrm{idtoequiv}(A, B):(A =_\mathcal{U} B) \to \mathcal{T}_\mathcal{U}(A \simeq_\mathcal{U} B)$$
is an equivalence
$$\mathrm{idtoequiv}(A, B):(A =_\mathcal{U} B) \simeq \mathcal{T}_\mathcal{U}(A \simeq_\mathcal{U} B)$$
These two definitions of univalent universes are the same. In order to show that the two definitions are the same, we need to show that there is an identification 
$$i(p):\mathrm{canonical}_\simeq(A, B)(\mathrm{idtoequiv}(A, B)(p)) =_{\mathcal{T}_\mathcal{U}(A) \simeq \mathcal{T}_\mathcal{U}(B)}  \mathrm{trans}^{\mathcal{T}_\mathcal{U}}(A, B)(p)$$
for all identifications $p:A =_\mathcal{U} B$. By the J rule it is enough to show that $\mathrm{canonical}_\simeq(A, A)$ maps the identity function of $\mathcal{T}_\mathcal{U}(A \to_\mathcal{U} A)$ to the identity function of $\mathcal{T}_\mathcal{U}(A) \to \mathcal{T}_\mathcal{U}(A)$. Since the identity function in $\mathcal{T}_\mathcal{U}(A \to_\mathcal{U} A)$ is just $\mathrm{canonical}_\simeq^{-1}(A, A)(id_A)$ the above statement is always true. Thus, the second definition of a univalent universe is equivalent to the definition by transport. 

These results apply to strictly Tarski universes as well, which are strictly closed rather than weakly closed (the equivalences become [[definitional equality]]): since $A \equiv B$ implies that $A \simeq B$ for types $A$ and $B$, every strictly Tarski universe is weakly Tarski. 

### Relation to parallel transport

\begin{remark}\label{RelationToParallelTransport}
**(relation to parallel transport -- [[schreiber:differential cohomology in a cohesive topos|dcct §3.8.5]], [ScSh12 §3.1.2](cohesive+homotopy+type+theory#SchreiberShulman2012))**
\linebreak
  In [[cohesive homotopy type theory]] the [[shape modality]] $\esh$ has the [[shape via cohesive path ∞-groupoid|interpretation]] of turning any cohesive type $X$ into its [[path infinity-groupoid|path $\infty$-groupoid]] $\esh X$: The [[1-morphisms]] $p \colon (x =_{\esh X} y)$ of $\esh X$ have the [[shape via cohesive path ∞-groupoid|interpretation]] of being (whatever identities existed in $X$ composed with) cohesive (e.g. [[continuous function|continuous]] or [[smooth function|smooth]]) *[[paths]]* in $X$, and similarly for the higher order paths-of-paths.

Accordingly, an [[shape modality|$\esh X$]]-[[dependent type]] $B$ has the interpretation of being a "[[local system]]" of $B$-[[coefficients]] over $X$, namely a $B(x)$-[[fiber infinity-bundle|fiber $\infty$-bundle]] equipped with a [[flat infinity-connection|flat $\infty$-connection]]. 

In this case, the identity transport (eq:TheTransportFunctions) along paths in [[shape modality|$\esh X$]] has the interpretation of being the *[[parallel transport]]* (in the original sense of [[differential geometry]]) with respect to this [[flat infinity-connection|flat $\infty$-connection]] (and the [[higher parallel transport]] when applied to paths-of-paths).
\end{remark}

## See also ##

* [[identity type]]

* [[dependent identity type]]

* [[identity of indiscernibles]]

* [[identity function]]

## References ##

The traditional notion of the "transport" in [[algebraic topology]] (via the [[fundamental theorem of covering spaces]] and more generally via the notion of [[Serre fibrations]]): 

* {#tomDieck2008} [[Tammo tom Dieck]],  §3.2 and §5.6 in: _Algebraic topology_, European Mathematical Society, Zürich (2008) &lbrack;[doi:10.4171/048](https://www.ems-ph.org/books/book.php?proj_nr=86), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/diecktop.pdf)&rbrack;

The notion in [[homotopy type theory]]:

* [[Univalent Foundations Project|UVP]], [§2.3 "Type families and fibrations"](https://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf#page=81) in: *[[Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

* [[Egbert Rijke]]: §5.4 in: *[[Introduction to Homotopy Type Theory]]* Cambridge University Press (2023) &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;

* [[Egbert Rijke]], pp. 18 in: *Homotopy Type Theory* (2012) &lbrack;[pdf](https://studenttheses.uu.nl/bitstream/handle/20.500.12932/11704/hott.pdf?sequence=1)&rbrack;

and in [[cubical type theory]]:

* [[Cyril Cohen]], [[Thierry Coquand]], [[Simon Huber]], [[Anders Mörtberg]]: Section 4.6 of *Cubical Type Theory: a constructive interpretation of the univalence axiom* &lbrack;[arXiv:1611.02108](https://arxiv.org/abs/1611.02108)&rbrack;

* [[Thierry Coquand]], [[Simon Huber]], [[Anders Mörtberg]]: Def. 3 in: *On Higher Inductive Types in Cubical Type Theory* &lbrack;[arXiv:1802.01170](https://arxiv.org/abs/1802.01170)&rbrack;


Implementation in [[Agda]]:

* [[Martín Hötzel Escardó]] pp 20 in: *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580), [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/)&rbrack;

and in [cubical Agda](Agda#CubicalAgda):

* [[1lab]], *Transport* &lbrack;[#12111](https://1lab.dev/1Lab.Path.html#12111)&rbrack;

* {#MyersRiley24} [[David Jaz Myers]], [[Mitchell Riley]], [lecture 2.5](https://github.com/CQTS/introduction-to-cubical/blob/master/lectures/2--Paths-and-Identifications/2-5--Transport.lagda.md) of course notes for *Introduction to Cubical Agda* at [[CQTS]] @ NYU Abu Dhabi (2023, 24) &lbrack;[github](https://github.com/CQTS/introduction-to-cubical/tree/master/lectures)&rbrack;


[[Gottfried Leibniz|Leibniz]]'s original paragraph (from an unpublished manuscript probably written after 1683) is reproduced in the Latin original in:

* {#Gerhard1890} K. Gerhard (ed.), Section XIX, [p. 228](https://archive.org/details/diephilosophisc00gerhgoog/page/228/mode/2up) in: *Die philosophischen Schriften von Gottfried Wilhelm Leibniz*, Siebenter Band, Weidmannsche Buchhandlung (1890) &lbrack;[archive.org](https://archive.org/details/diephilosophisc00gerhgoog/page/n7/mode/2up)&rbrack;

and in English translation in:

* {#Lewis18} [[Clarence I. Lewis]], Appendix (p. 373) of: *A Survey of Symbolic Logic*, University of California (1918) &lbrack;[[LewisAppendix-LeibnizIndiscernibles.pdf:file]]&rbrack;

and further discussed in:

* {#Cartwright71} [[Richard Cartwright]], *Identity and Substitutivity*, p. 119-133 of: Milton Munitz (ed.) *Identity and Individuation*, New York University Press (1971) &lbrack;[[Cartwright-IdentityAndSubstitutivity.pdf:file]]&rbrack;

* {#GriesSchneider98} David Gries, Fred Schneider, *Formalizations Of Substitution Of Equals For Equals* (1998) &lbrack;[pdf](https://ecommons.cornell.edu/bitstream/handle/1813/7340/98-1686.pdf?sequence=1&isAllowed=y), [ecommons:1813/7340](https://ecommons.cornell.edu/handle/1813/7340)

The understanding of transport in HoTT as expressing [[Leibniz]]'s principle of "[[indiscernibility of identicals]]" (aka "substitution of equals", "substitutivity") has been made explicit in:

* {#LadymanPresnell15} [[James Ladyman]], [[Stuart Presnell]], §6.3 in: *Identity in Homotopy Type Theory, Part I: The Justification of Path Induction*, Philosophia Mathematica **23** 3 (2015) 386–406 &lbrack;[doi:10.1093/philmat/nkv014](https://doi.org/10.1093/philmat/nkv014), [pdf](http://philsci-archive.pitt.edu/11079/1/Identity_in_HTT_public.pdf)&rbrack;

* [[Benedikt Ahrens]], [[Paige Randall North]], §3.1 in: *Univalent foundations and the equivalence principle*, in: *Reflections on the Foundations of Mathematics*, Synthese Library **407** Springer (2019)  &lbrack;[arXiv:2202.01892](https://arxiv.org/abs/2202.01892), [doi:10.1007/978-3-030-15655-8](https://doi.org/10.1007/978-3-030-15655-8)&rbrack;

The converse implication of [[path induction]] from transport (together with the uniqueness principle for id-types) is made explicit in:

* [Ladyman & Presnell 2015, §6.3](#LadymanPresnell15)

* Lennard Götz, §4.2 of: *Martin-Löf's J-rule*, LMU (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Goetz.pdf)&rbrack; 

For the role of transport in defining an equivalent notion of [[univalence]] in [[weakly Tarski universes]], see:

* Madeleine Birchfield, Valery Isaev, *Univalence for weakly Tarski universes*, MathOverflow, ([web](https://mathoverflow.net/q/431723))

[[!redirects transport]]
[[!redirects transports]]

[[!redirects weak transport]]
[[!redirects weak transports]]

[[!redirects strict transport]]
[[!redirects strict transports]]

[[!redirects judgmentally strict transport]]
[[!redirects judgmentally strict transports]]

[[!redirects propositionally strict transport]]
[[!redirects propositionally strict transports]]

[[!redirects definitional transport]]
[[!redirects definitional transports]]

[[!redirects judgmental transport]]
[[!redirects judgmental transports]]

[[!redirects transporting]]

[[!redirects identity transport]]
[[!redirects identity transports]]

[[!redirects type transport]]
[[!redirects type transports]]

[[!redirects transport equivalence]]
[[!redirects transport equivalences]]

[[!redirects transport function]]
[[!redirects transport functions]]

[[!redirects transport functor]]
[[!redirects transport functors]]

[[!redirects type of transport functions]]
[[!redirects types of transport functions]]

[[!redirects indiscernibility of identicals]]

[[!redirects principle of substitutivity]]
[[!redirects principle of substitution]]
[[!redirects principle of substitution of equals for equals]]
[[!redirects principle of substituting equals for equals]]