
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In [[type theory]] a _product type_ of two [[types]] $A$ and $B$ is the type whose [[terms]] are [[ordered pairs]] $(a,b)$ with $a\colon A$ and $b\colon B$.

In a [[model]] of the type theory in [[categorical semantics]], this is a [[product]]. In [[set theory]], it is a [[cartesian product]]. In [[dependent type theory]], it is a special case of a [[dependent sum]].

Note that a [[dependent product type]] is something different (a generalization of a [[function type]]).

## Overview
 {#Overview}

\linebreak

\begin{imagefromfile}
    "file_name": "ProductTypeInferenceRules-221230.jpg",
    "width": 650,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

> (table taken from [[schreiber:Topological Quantum Gates in Homotopy Type Theory|Myers et al.]])


## Definition

Like any type constructor in [[type theory]] (see at [[natural deduction]]), a product type is specified by rules saying when we can introduce it as a type, how to construct terms of that type, how to use or "eliminate" terms of that type, and how to compute when we combine the constructors with the eliminators.


### In natural deduction

We assume that our product types have typal [[conversion rules]], as those are the most general of the conversion rules. Both the propositional and judgmental conversion rules imply the typal conversion rules by the structural rules for propositional and judgmental equality respectively. 

The formation and introduction rules are the same for both the positive and negative product types

Formation rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

Introduction rules for product types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash (x, y):A \times B}$$

#### As a positive type 

* Elimination rules for product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[(x, y)/z]}{\Gamma, z:A \times B \vdash \mathrm{ind}_{A \times B}^C(c):C}$$

* Computation rules for product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[(x, y)/z]}{\Gamma, x:A, y:B \vdash \beta_{A \times B}^C(c):\mathrm{ind}_{A \times B}^C(c)[(x, y)/z] =_{C[(x, y)/z]} c}$$

* Uniqueness rules for product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash B \; \mathrm{type} \quad \Gamma, z:A \times B \vdash C \; \mathrm{type} \quad \Gamma, x:A, y:B \vdash c:C[(x, y)/z] \quad \Gamma, z:A \times B \vdash u:C \quad \Gamma, x:A, y:B \vdash i_{(-,-)}(u):u[(x, y)/z] =_{C[(x, y)/z]} c}{\Gamma, z:A \times B \vdash \eta_{A \times B}^C(c):u =_{C} \mathrm{ind}_{A \times B}^C(c)}$$

Given a [[pointed type|pointed]] [[h-proposition]] $(A, a)$, the positive product type results in $(a,-)$ being an [[equivalence of types]]. 

#### As a negative type

* Elimination rules for product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \pi_2(z):B}$$

* Computation rules for product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma\vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \beta_{\times 1}(x, y):\pi_1((x, y)) =_A x} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, x:A, y:B \vdash \beta_{\times 2}(x, y):\pi_2((x, y)) =_{B} y}$$

* Uniqueness rules for product types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type}}{\Gamma, z:A \times B \vdash \eta_{\times}(z):z =_{A \times B} (\pi_1(z), \pi_2(z))}$$

Given a [[pointed type|pointed]] [[h-proposition]] $(A, a)$, the negative product type results in $\pi_2(a,-)$ being a [[quasi-inverse function]] of $(a,-)$, rather than an [[equivalence of types]]. Thus, the positive definition is preferred to the negative definition. Alternatively, the negative product type should be defined as a [[coinductive type]] rather than an [[inductive type]]. 

#### As a special case of the dependent sum

In [[dependent type theory]] a product type $A \times B$ is the special case the [[dependent sum]] over $a : A$ for the special case that $B$ is regarded as an $A$-[[dependent type]] that actually happens to be $A$-independent. The rules are given as follows:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, a:A, b:A \vdash B[a/x] \equiv B[b/x] \; \mathrm{type}}{\Gamma \vdash A \times B \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B \; \mathrm{type} \quad \Gamma, a:A, b:A \vdash B[a/x] \equiv B[b/x] \; \mathrm{type}}{\Gamma \vdash A \times B \equiv \sum_{x:A} B\; \mathrm{type}}$$

#### As a special case of the dependent product

In [[dependent type theory]] given types $A$ and $B$, one could define a type family $C$ indexed by elements of the [[two-valued type]] $\mathbb{2}$ by $C(0) \coloneqq A$ and $C(1) \coloneqq B$. A product type $A \times B$ is a special case of the [[dependent product type]]

$$A \times B \coloneqq C(0) \times C(1) \coloneqq \prod_{x:\mathbb{2}} C(x)$$

and is given by the following rules:

Formation rules for product types:
$$\frac{\Gamma, x:\mathbb{2} \vdash C \; \mathrm{type}}{\Gamma \vdash C(0) \times C(1) \; \mathrm{type}}$$

Introduction rules for product types:
$$\frac{\Gamma, x:\mathbb{2} \vdash c:C}{\Gamma \vdash \lambda(x:\mathbb{2}).c(x):C(0) \times C(1)}$$

Elimination rules for product types:
$$\frac{\Gamma \vdash z:C(0) \times C(1) \quad \Gamma \vdash p:\mathbb{2}}{\Gamma \vdash z(p):C[p/x]}$$

Computation rules for product types:
$$\frac{\Gamma, x:\mathbb{2} \vdash c:C \quad \Gamma \vdash p:\mathbb{2}}{\Gamma \vdash \beta_\Pi(p):\lambda(x:\mathbb{2}).c(x)[p/x] =_{C[p/x]} c[p/x]}$$

Uniqueness rules for product types:
$$\frac{\Gamma \vdash z:C(0) \times C(1)}{\Gamma \vdash \eta_\Pi(z):z =_{C(0) \times C(1)} \lambda(x).z(x)}$$

#### Properties

Suppose $A$ and $B$ are types and $A \times B$ is the negative product type of $A$ and $B$. Then for all elements $c:A \times B$ and $c':A \times B$, there is a function 
$$\mathrm{ap}_{(\pi_1, \pi_2)}(c, c'):(c =_{A \times B} c') \to \left((\pi_1(c) =_A \pi_1(c')) \times (\pi_2(c) =_B \pi_2(c'))\right)$$ 
There are functions $\mathrm{ap}_{\pi_1}(c, c'):(c =_{A \times B} c') \to (\pi_1(c) =_A \pi_1(c'))$ and $\mathrm{ap}_{\pi_2}(c, c'):(c =_{A \times B} c') \to (\pi_2(c) =_B \pi_2(c'))$ which are the [[function application to identities]] for the product projections $\pi_1$ and $\pi_2$, which means for all identities $p:c =_{A \times B} c'$, there are identities 
$$\mathrm{ap}_{\pi_1}(c, c')(p):\pi_1(c) =_A \pi_1(c')$$ 
$$\mathrm{ap}_{\pi_2}(c, c')(p):\pi_2(c) =_A \pi_2(c')$$ 
Then, by the introduction rule for products, one could form the pair 
$$(\mathrm{ap}_{\pi_1}(c, c')(p), \mathrm{ap}_{\pi_2}(c, c')(p))$$
with identites
$$\delta(c, c', p):\mathrm{ap}_{(\pi_1, \pi_2)}(c, c')(p) =_{(\pi_1(c) =_A \pi_1(c')) \times (\pi_2(c) =_B \pi_2(c'))} (\mathrm{ap}_{\pi_1}(c, c')(p), \mathrm{ap}_{\pi_2}(c, c')(p))$$ 
for all $p:c =_{A \times B} c'$. 

Similarly, for all elements $a:A$, $a':A$, $b:B$, $b':B$, the [[binary function application to identities]] for $(-, -)$ defined in the [[introduction rule]] for product types is given by
$$\mathrm{apbinary}_{(-,-)}(a, a', b, b'):\left(a =_A a') \times (b =_B b')\right) \to ((a, b) =_{A \times B} (a', b')$$
inductively defined by the identities 
$$\beta_{\mathrm{apbinary}_{(-,-)}}(a, b):\mathrm{apbinary}_{(-,-)}(a, a, b, b)(\mathrm{refl}_{A}(a), \mathrm{refl}_{B}(b)) =_{(a, b) =_{A \times B} (a, b)} \mathrm{refl}_{A \times B}((a, b)))$$

For all elements $c:A \times B$ and $c':A \times B$, the composition of functions 
$$\mathrm{apbinary}_{(-,-)}(\pi_1(c), \pi_1(c'), \pi_2(c), \pi_2(c')) \circ \mathrm{ap}_{(\pi_1, \pi_2)}(c, c')$$ 
has domain $c =_{A \times B} c'$ and codomain $(\pi_1(c), \pi_2(c)) =_{A \times B} (\pi_1(c'), \pi_2(c'))$. 

By the uniqueness rule for the negative product type, there are identities $\eta_{\times}(c):c =_{A \times B} (\pi_1(c), \pi_2(c))$ and $\eta_{\times}(c'):c' =_{A \times B} (\pi_1(c'), \pi_2(c'))$, and thus, for all identities $p:c =_{A \times B} c'$, there are identities

$$
  \array{& c & \overset{\eta_{\times}(c)}= & (\pi_1(c), \pi_2(c)) & \\
          p & \Vert & \rightarrow & \Vert & \mathrm{apbinary}_{(-,-)}(\pi_1(c), \pi_1(c'), \pi_2(c), \pi_2(c'))(\mathrm{ap}_{(\pi_1, \pi_2)}(c, c')(p))\\
          &c' & \underset{\eta_{\times}(c')}= & (\pi_1(c'), \pi_2(c')) & \\
}$$

For all elements $a:A$, $a':A$, and $b:B$, $b':B$, the composition of functions 
$$\mathrm{ap}_{(\pi_1, \pi_2)}((a, b), (a', b')) \circ \mathrm{apbinary}_{(-,-)}(a, a', b, b')$$ 
has domain $(a =_A a') \times (b =_B b')$ and codomain $(\pi_1((a, b)) =_A \pi_1((a', b'))) \times (\pi_2((a, b)) =_B \pi_2((a', b')))$. 

By the computation rules of the negative product type, there are identities $\beta_{\times 1}(a, b):\pi_1((a, b)) =_A a$, $\beta_{\times 2}(a, b):\pi_2((a, b)) =_A b$, $\beta_{\times 1}(a', b'):\pi_1((a', b')) =_A a'$, and $\beta_{\times 2}(a', b'):\pi_2((a', b')) =_A b'$, and for all pairs of identities $q:(a =_A a') \times (b =_B b')$, there are identities

$$
  \array{& \pi_1((a, b)) & \overset{\beta_{\times 1}(a, b)}= & a & \\
          \pi_1(\mathrm{ap}_{(\pi_1, \pi_2)}((a, b), (a', b'))(\mathrm{apbinary}_{(-,-)}(a, a', b, b')(q))) & \Vert & \leftarrow & \Vert & \pi_1(q) \\
          & \pi_1((a', b')) & \underset{\beta_{\times 1}(a', b')}= & a' & \\
}$$

$$
  \array{& \pi_2((a, b)) & \overset{\beta_{\times 2}(a, b)}= & b & \\
          \pi_2(\mathrm{ap}_{(\pi_1, \pi_2)}((a, b), (a', b'))(\mathrm{apbinary}_{(-,-)}(a, a', b, b')(q))) & \Vert & \leftarrow & \Vert & \pi_2(q) \\
          & \pi_2((a', b')) & \underset{\beta_{\times 2}(a', b')}= & b' & \\
}$$

Both of these square are in general not [[commutative squares]]. 

### In lambda-calculus

There are actually two ways to present product types, as a [[negative type]] or as a [[positive type]].  In both cases the [[type formation rule]]
is the following:

$$
  \frac{A\colon Type \qquad B\colon Type}{A\times B\colon Type} 
$$

but the constructors and eliminators may be different.

#### As a negative type

When presented negatively, primacy is given to the [[term elimination rule|eliminators]].  We specify that there are two ways to eliminate a term of type $A\times B$: by projecting out the first component, or by projecting out the second.

$$ \frac{p \colon A\times B}{\pi_1 p\colon A} \qquad \frac{p\colon A\times B}{\pi_2 p\colon B}$$

This then determines the form of the [[term introduction rule|constructors]]: in order to construct a term of type $A\times B$, we have to specify what value that term should yield when all the eliminators are applied to it.  In other words, we have to specify a pair of elements, one of $A$ (to be the value of $\pi_1 p$) and one of $B$ (to be the value of $\pi_2 p$).

$$ \frac{a\colon A \qquad b\colon B}{(a,b)\colon A\times B} $$

Finally, we have [[computation rules]] which say that the relationship between the constructors and the eliminators is as we hoped.  We always have [[beta reduction]] rules

$$ \pi_1(a,b) \to_\beta a \qquad \pi_2(a,b) \to_\beta b $$

and we may or may not choose to have an [[eta reduction]] rule

$$ (\pi_1 p, \pi_2 p) \to_\eta p $$

#### As a positive type

When presented positively, primacy is given to the constructors.  We specify that the way to construct something of type $A\times B$ is to give something of type $A$ and something of type $B$:

$$ \frac{a\colon A \qquad b\colon B}{(a,b)\colon A\times B} $$

Of course, this is the same as the constructor obtained from the negative presentation.  However, the eliminator is different.  Now, in order to say how to *use* something of type $A\times B$, we have to specify how we should behave for all possible ways that it could have been constructed.  In other words, we have to say, *assuming* that $p$ were of the form $(a,b)$, what we want to do.  Thus we end up with the following rule:

$$ \frac{p\colon A\times B \qquad x\colon A, y\colon B \vdash c\colon C}{let (x,y) = p in c \;\colon C} $$

We need a term $c$ in the context of two variables of types $A$ and $B$, and the destructor or match "binds those variables" to the two components of $p$.  Note that the "ordered pair" $(x,y)$ in the destructor is just a part of the syntax; it is not an instance of the *constructor* ordered pair.  In [[dependent type theory]], this elimination rule must be generalized to allow the type $C$ to depend on $A\times B$.

Now we have [[beta reduction]] rule:

$$ let (x,y) = (a,b) \,in c \;\to_\beta\; c[a/x, b/y] $$

In other words, if we build an ordered pair and then break it apart, what we get is just the things we put into it.  (The notation $c[a/x, b/y]$ means to substitute $a$ for $x$ and $b$ for $y$ in the term $c$).

And (if we wish) the [[eta reduction]] rule, which is a little more subtle:

$$ let (x,y) = p in c[(x,y)/z] \;\to_\eta\; c[p/z] $$

This says that if we break something of type $A\times B$ into its components, but then we only use those two components by way of putting them back together into an ordered pair, then we might as well just not have broken it down in the first place.

Positively defined products are naturally expressed as [[inductive types]].  For instance, in [[Coq]] syntax we have

    Inductive prod (A B:Type) : Type :=
    | pair : A -> B -> prod A B.

(Coq then implements beta-reduction, but not eta-reduction.  However, eta-equivalence is provable with the internally defined [[identity type]], using the dependent eliminator mentioned above.)

Arguably, negatively defined products should be naturally expressed as [[coinductive type]]s, but this is not exactly the case for the presentation of coinductive types used in Coq.


#### Positive versus negative

In ordinary "nonlinear" type theory, the positive and negative product types are equivalent.  They manifestly have the same constructor, while we can define the eliminators in terms of each other as follows:

$$
\begin{aligned}
  \pi_1 p &\;\coloneqq\; let (x,y) = p in x\\
  \pi_2 p &\;\coloneqq\; let (x,y) = p in y\\
  let (x,y) = p in c &\;\coloneqq\; c[\pi_1 p / x, \pi_2 p / y]
\end{aligned}
$$

It is obvious that the $\beta$-reduction rules in the two cases correspond; see below for $\eta$-conversion.

In dependent type theory, in order to recover the *dependent* eliminator for the positive product type from the eliminators for the negative product type, we need the latter to satisfy the $\eta$-conversion rule so as to make the above definition well-typed.  It is sufficient to have the $\eta$-conversion up to [[propositional equality]], however, if we are willing to insert a substitution along such an equality in the definition of the dependent eliminator.  Conversely, the dependent eliminator for the positive product allows us to prove a propositional version of the negative $\eta$-conversion (without assuming the positive $\eta$-conversion).  See [propositional eta-conversions](/nlab/show/eta-conversion#Propositional).

Now from $\eta$-conversion for the negative product, we can also derive

$$
\begin{aligned}
  let (x,y) = p in c[(x,y)/z]
  &\;\coloneqq\; c[(\pi_1 p,\pi_2 p)/z]\\
  &\;\to_\eta\; c[p/z]
\end{aligned}
$$

so the defined positive product also satisfies its $\eta$-conversion, which will be definitional or propositional according to that of the negative product.

On the other hand, if the positive product has a definitional $\eta$-conversion, then for the defined negative product we have

$$
\begin{aligned}
  (\pi_1 p, \pi_2 p)
  &\;\coloneqq\; (let (x,y) = p in x, let (x,y) = p in y)\\
  &\;\leftarrow_\eta\; (let (x',y') = p in \;( let (x,y) = (x',y') in x , let (x,y) = (x',y') in y )\\
  &\;\to_\beta\; let (x',y') = p in (x',y')\\
  &\;\to_\eta\; p
\end{aligned}
$$

Note that this involves a beta-reduction step and also a "backwards" $\eta$-reduction step.  So from positive $\eta$ *reduction* we cannot derive negative $\eta$-reduction, only negative $\eta$-equivalence.  (However, the directionality of $\eta$-reduction is somewhat questionable anyway.)

In conclusion, we have:

* In non-dependent type theory, positive and negative products are equivalent, as are their definitional $\beta$-reduction rules.

* In dependent type theory with [[identity types]], improving the positive eliminator to a *dependent* eliminator is equivalent to asserting [propositional](/nlab/show/eta-conversion#Propositional) versions of either $\eta$-conversion rule.

* In any case, the two *definitional* $\eta$-conversion rules also correspond.

It is of importance to note that these translations require the [[contraction rule]] and the [[weakening rule]]; that is, they duplicate and discard terms.  In [[linear logic]] these rules are disallowed, and therefore the positive and negative products become different.  The positive product becomes "tensor" $A\otimes B$, and the negative product becomes "with" $A \& B$.

## Categorical interpretation

Under [[categorical semantics]], product types satisfying both beta and eta conversions correspond to [[products]] in a [[category]].  More precisely:

* categorical products may be used to interpret product types that validate both beta and eta rules, while

* the [[syntactic category]] of a type theory with product types has categorical products, as long as the type theory satisfies both beta and eta rules.

Of course, the categorical notion of product matches the *negative* definition of a product most directly.  In linear logic, therefore, the categorical product interprets "with" $\&$, while an additional [[monoidal category|monoidal structure]] interprets "tensor" $\otimes$.  On the other hand, in a representable [[cartesian multicategory]], the product has a "from the left" universal property which matches the *positive* definition.

There is also another interpretation in category theory of the product type $A$ and $B$, as the [[initial]] $A$-indexed family of [[parallel morphisms]] with [[source]] $B$, the object $A \times B$ with a family of morphisms 

$$\mathrm{in}_A(x):B \to A \times B$$

such that for any other object $C$ with a family of morphisms $f(x):B \to C$, there exists a unique morphism $u_C:A \times B \to C$ such that 

$$u_C \circ \mathrm{in}_A(x) = f(x)$$

This corresponds to the positive product types. 

## Related concepts

* [[sum type]]

* [[dependent sum type]]

* [[dependent product type]]

## References

A textbook account in the context of [[programming languages]] is in section 11 of 

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_

On product types as [[inductive types]]:

* Kajetan Söhnen, §2.4.3 in : *Higher Inductive Types in Homotopy Type Theory*, Munich (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Soehnen.pdf), [[Soehnen-HigherInductiveTypes.pdf:file]]&rbrack;


[[!redirects product type]]
[[!redirects product types]]

[[!redirects pair type]]
[[!redirects pair types]]
