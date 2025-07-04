
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contractible types
* table of contents
{: toc}

## Idea

In [[homotopy type theory]], the notion of **contractible [[type]]** is an internalization of the notion of [[contractible space]] / [[(-2)-truncated]] object.

Contractible types are also called of **[[h-level]] $0$**. They represent the notion _[[true]]_ in homotopy type theory.


## Definition

We work in [[intensional type theory|intensional]] [[type theory]] with [[dependent sums]], [[dependent products]], and [[identity types]], 

\begin{definition}
For $X$ a [[type]], let

$$
  isContr(X) \coloneqq \sum_{x\colon X} \prod_{y\colon X} (y=x)
$$

be the [[dependent sum]] in one [[variable]] $x : X$ over the [[dependent product]] on the other [[variable]] $y \colon X$ of the $x,y$-[[dependent type|dependent]] [[identity type]] $(x = y)$.

We say that $X$ is a **contractible type** if $isContr(X)$ is an [[inhabited type]].
\end{definition}

\begin{remark}
In [[propositions as types]] language, this can be pronounced as "there exists a point $x\colon X$ such that every other point $y\colon X$ is equal to $x$."  

Under the [[homotopy theory|homotopy-theoretic]] interpretation, it should be thought of as the type of *contractions* of $X$ --- since the dependent product describes *continuous* functions, the paths from $y$ to $x$ depend continuously on $y$ and thus exhibit a contraction of $X$ to $x$.
\end{remark}

\begin{definition}
A provably [[equivalence in homotopy type theory|equivalent]] definition is
the [[product type]] of $X$ with the [[isProp]]-type of $X$:

$$
  isContr(X) \coloneqq X \;\times\; isProp(X) 
  \,.
$$
\end{definition}

(Here of course we have to use a definition of [[isProp]] which doesn't refer to $isContr$).  

\begin{remark}
This now says that $X$ is contractible iff $X$ is a **[[pointed type|pointed]] [[h-proposition]]**.
\end{remark}

There is a third definition of a contractible type, provably equivalent to the others. 

\begin{definition}\label{SingletonInduction}
Let $(A, a:A)$ be a [[pointed type]]. $A$ satisfies **singleton induction** if for every [[type family]] $B$ over $A$ the dependent function 
$$\mathrm{evpt}(a):\left(\prod_{x:A} B(x)\right) \to B(a)$$
has a [[section]]. A **contractible type** is a pointed type which satisfies singleton induction. 
\end{definition}

### Rules for isContr

If the [[dependent type theory]] only has rules for [[identity types]] and [[dependent identity types]], one could define the isContr modality by the following rules:

Formation rules for isContr types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{isContr}(A) \; \mathrm{type}}$$

Introduction rules for isContr types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma, x:A \vdash \tau(x):a =_A x}{\Gamma \vdash w(a, \lambda x.\tau(x)):\mathrm{isContr}(A)}$$

Elimination rules for isContr types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathrm{isContr}(A) \vdash \mathrm{pt}(p):A} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathrm{isContr}(A), x:A \vdash c(p, x):\mathrm{pt}(p) =_A x}$$

Computation rules for isContr types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma, x:A \vdash \tau(x):a =_A x}{\Gamma \vdash \beta_{\mathrm{isContr}(A)}^\mathrm{pt}(a):\mathrm{pt}(w(a, \lambda x.\tau(x))) =_A a}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma, x:A \vdash \tau(x):a =_A x}{\Gamma, x:A \vdash \beta_{\mathrm{isContr}(A)}^w(x):c(w(a, \lambda x.\tau(x)))(x) =_{(-) =_A x}^{\beta_{\mathrm{isContr}(A)}^\mathrm{pt}(a)} \tau(x)}$$

Uniqueness rules for isContr types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:\mathrm{isContr}(A) \vdash \eta_{\mathrm{isContr}(A)}(p):w(\mathrm{pt}(p), \lambda x.c(p, x)) =_{\mathrm{isContr}(A)} p}$$

## Properties

\begin{proposition}
For any type $A$, the type $isContr(A)$ is an [[h-proposition]].  In particular, we can show $isContr(A) \to isContr(isContr(A))$: if a type is contractible, then its space of contractions is also contractible.
\end{proposition}

\begin{proposition}
A type is contractible if and only if it is [[equivalence in homotopy type theory|equivalent]] to the [[unit type]].
\end{proposition}

### Relation to dependent sum types and equivalences

A family of elements $x:A \vdash f(x):B$ is an [[equivalence of types]] if its family of [[fiber types]] $y:B \vdash \sum_{x:A} f(x) =_B y$ is a family of [[contractible types]]. 

The [[dependent sum type]] of a family of contractible types $x:A \vdash B(x)$ with witnesses $x:A \vdash p(x):\mathrm{isContr}(B(x))$ is equivalent to the index type $A$ itself given by the first pair projection:

$$z:\sum_{x:A} B(x) \vdash \pi_1(z):A$$

$$x:A \vdash p(x):\mathrm{isContr}\left(\sum_{z:\sum_{x:A} B(x)} \pi_1(z) =_A x\right)$$

This is due to the fact that for any family of types $x:A \vdash B(x)$, there is an equivalence 

$$x:A \vdash q(x):\left(\sum_{z:\sum_{x:A} B(x)} \pi_1(z) =_A x\right) \simeq B(x)$$

which means that if $B(x)$ is contractible, then 
$$\sum_{z:\sum_{x:A} B(x)} \pi_1(z) =_A x$$ 
is contractible. 

## Categorical semantics
 {#CategoricalSemantics}

We discuss the [[categorical semantics]] of contractible types.

Let $\mathcal{C}$ be a [[locally cartesian closed category]] with [[categorical semantics of homotopy type theory|sufficient structure]] to intepret all the above type theory.  This means that $\mathcal{C}$ has a [[weak factorization system]] with [[stable path objects]], and that [[acyclic cofibrations]] are preserved by pullback along fibrations between fibrant objects.  (We ignore questions of [[coherence]], which are not important for this discussion.)

In this [[categorical semantics]], the interpretation of a type $\vdash A : Type$ is a [[fibrant object]] $[\vdash A : Type]$, which for short we will just write $A$. The interpretation of the [[identity type]] $x,y : A \vdash (x = y) : Type$ is as the [[path space object]] $A^I \to A \times A$.
The interpretation of $isContr(A)$ is the object obtained by taking the [[dependent product]] of the [[path space object]] along one [[projection]] $p_2 : A\times A\to A$ and then forgetting the remaining morphism to $A$.

$$
  [isContr(A)]
  \;\;
  =
  \;\;
  \array{
    \prod_{p_2} A^I
    \\
    \downarrow
    \\
    A
    \\
    \downarrow
    \\
    *
  }
  \,.
$$

The interpretation $[\hat a : isContr(A)]$ of a [[term]] of $isContr(A)$ is precisely a morphism $\hat a : * \to \prod_{p_2} A^I$.

\begin{proposition}
Let $\mathcal{C}$ be a [[type-theoretic model category]]. Write $[isContr(A)]$ for the [[categorical semantics|interpretation]] of $isContr(A)$ in $\mathcal{C}$. Then:

Global points $* \to [isContr(A)]$ in $\mathcal{C}$ are in bijection with [[contraction]] [[right homotopies]] of the object $A$, hence to [[diagrams]] in $\mathcal{C}$ of the form

$$
  \array{
    A &\stackrel{\eta}{\to}& A^I
    \\
    & {}_{\mathllap{(id, const_a)}}\searrow & \downarrow
    \\
    && A \times A
  }
  \,,
$$

where $const_a$ is a morphism of the form $A \to * \stackrel{a}{\to} A$ and where $A^I$ is the [[path space object]] of $A$ in $\mathcal{C}$.
\end{proposition}

\begin{proof}
Given a global point $\hat a : * \to \prod_{p_2} A^I$, write $a : * \to A$ for the corresponding composite

$$
  \array{
     * &\stackrel{\hat a}{\to} & \prod_{p_2} A^I
     \\
     &{}_{\mathllap{a}}\searrow & \downarrow
     \\
     && A
  }
  \,.
$$

in $\mathcal{C}$. This is an element in the [[hom set]] $\mathcal{C}_{/A}(a, \prod_{p_2} A^I)$ of the [[slice category]] over $A$. By the ([[base change]] $\dashv$ [[dependent product]])-[[adjunction]] this is equivalently an element in $\mathcal{C}_{/A \times A}( p_2^* a, A^I )$.

Notice that the pullback $p_2^* a$ is the left morphism in

$$
  \array{
    A &\to& *
    \\
    {}^{\mathllap{(id,const_a)}}\downarrow && \downarrow^{\mathrlap{a}}
    \\
    A \times A &\stackrel{p_2}{\to}& A 
  }
  \,.
$$

Therefore a morphism $p_2^* a \to  A^I$ in $\mathcal{C}_{/A \times A}$ is
equivalently in $\mathcal{C}$ a diagram of the form

$$
  \array{
    A &&\stackrel{\eta}{\to}&& A^I
    \\
    & {}_{\mathllap{(id,const_a)}}\searrow && \swarrow
    \\
    && A \times A
  }
  \,.
$$

This is by definition a [[contraction]] right [[homotopy]] of $A$.
\end{proof}

\begin{remark}
Thus if $isContr(A)$, then 
$A\to 1$ is a (right) [[homotopy equivalence]], and hence (since $A$ is [[fibrant]]) an [[acyclic fibration]].

Conversely, if $\mathcal{C}$ is a [[model category]], $A$ and $1$ are cofibrant, and $A\to 1$ is an acyclic fibration, then $A\to 1$ is a right homotopy equivalence, and hence $isContr(A)$ has a global element.  Thus, in most cases, the existence of a global element of $isContr(A)$ (which is unique up to homotopy, since $isContr(A)$ is an [[h-proposition]]) is equivalent to $A\to 1$ being an acyclic fibration.

More generally, we may apply this locally.  Suppose that $A\to B$ is a fibration, which we can regard as a dependent type
$$x\colon B \vdash A(x)\colon Type.$$
Then we have a dependent type
$$x\colon B \vdash isContr(A(x))\colon Type$$
represented by a fibration $isContr(A)\to B$.  By applying the above argument in the [[slice category]] $\mathcal{C}/B$, we see that (if $\mathcal{C}$ is a model category, and $A$ and $B$ are cofibrant) $isContr(A)\to B$ has a [[section]] exactly when $A\to B$ is an acyclic fibration.

We can also construct the type
$$\prod_{x\colon B} isContr(A(x))$$
in global context, which has a global element precisely when $isContr(A)\to B$ has a section.  Thus, a global element of this type is also equivalent to $A\to B$ being an acyclic fibration.
\end{remark}

## Examples

* The [[unit type]] is a contractible type. 

* The [[interval type]] is a contractible type. 

* Every [[cone type]] is a contractible type, of which the unit type (cone type of the empty type) and the interval type (cone type of the unit type) are examples of cone types. 

## Related concepts

[[!include homotopy n-types - table]]

* [[isEquiv]]

* **isContr**

* [[isProp]]

* [[uniqueness quantifier]]

* [[contractible space]], [[contractible chain complex]]

* [[empty type]], [[falsehood]]

* [[center of contraction]]

* [[propositional equality]]

## References

The notion of contractible types (and with it the modern notion of [[equivalence in homotopy type theory]]) originates around:

* {#Voevodsky10} [[Vladimir Voevodsky]], p. 8, 10 of: *Univalent Foundations Project* (2010) &lbrack;[pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/univalent_foundations_project.pdf), [[Voevodsky-UFP2010.pdf:file]]&rbrack;

Textbook account:


* {#UFP13} [[Univalent Foundations Project]], §3.11 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


[[Coq]]-code for contractible types:

* [HoTT repository](https://github.com/HoTT/HoTT/blob/master/Coq/Contractible.v)


[[!redirects singleton induction]]


[[!redirects pointed proposition]]
[[!redirects pointed propositions]]

[[!redirects pointed mere proposition]]
[[!redirects pointed mere propositions]]

[[!redirects pointed h-proposition]]
[[!redirects pointed h-propositions]]

[[!redirects contractible type]]
[[!redirects contractible types]]
[[!redirects h-level 0]]
[[!redirects h-level 0 type]]
[[!redirects (-2)-truncated type]]
[[!redirects (-2)-truncated types]]
[[!redirects type of contractions]]
[[!redirects h-contractible type]]
[[!redirects isContr]]

[[!redirects singleton contractibility]]
