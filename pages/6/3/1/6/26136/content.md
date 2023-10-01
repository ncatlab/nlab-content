
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given a type $A$ and a type family $x:A \vdash B(x)$, **John Major equality** or **heterogeneous equality** is a type family indexed by $a:A$, $b:A$, $y:B(a)$, and $z:B(b)$ representing the notion of equality between elements $y$ and $z$ over the type family $x:A \vdash B(x)$. There are a few different ways to define John Major equality: 

* as the [[dependent sum type]] of the [[heterogeneous identity type]] 
$$\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \equiv \mathrm{Id}_{B(b)}(\mathrm{transport}_{x:A.B(x)}(a, b, p)(y), z)$$ 
over all [[identifications]] $p:\mathrm{Id}_A(a, b)$. 

$$\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \coloneqq \sum_{p:\mathrm{Id}_A(a, b)} \mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$$

* as the [[identity type]] of [[dependent pairs]] in the [[dependent sum type]] $\sum_{x:A} B(x)$

$$\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \coloneqq \mathrm{Id}_{\sum_{x:A} B(x)}\left(\mathrm{pair}(a, y), \mathrm{pair}(b, z)\right)$$

By the extensionality property of [[dependent sum types]], these two definitions are equivalent. 

Usually, these are defined for a [[Tarski universe]] $(U, \mathrm{El})$ or a [[Russell universe]] $(U)$. Suppressing the annotations in John Major equality above, the type becomes $\mathrm{JMEq}(a, b, y, z)$, defined as one of 

$$\mathrm{JMEq}(A, B, x, y) \coloneqq \sum_{p:\mathrm{Id}_U(A, B)} \mathrm{hId}(A, B, p, y, z)$$

$$\mathrm{JMEq}(A, B, x, y) \coloneqq \mathrm{Id}_{\sum_{X:U} X}\left(\mathrm{pair}(x, A), \mathrm{pair}(y, B)\right)$$

for [[Russell universes]]

### Inference rules with UIP

When the type theory has a [[set truncation axiom]] such as [[UIP]] or [[axiom K]], one could use one of the following [[inference rules]] to define John Major equality: 

#### McBride's axiomatization

The axioms given in [McBride 1999](#McBride99) are in [[OLEG]] [[pseudocode]], use [[Russell universes]], and interpret relations impredicatively as functions into a [[type of all propositions]]. Here, the axioms are written as [[inference rules]] in a [[deduction system]], modified slightly to use [[Tarski universes]] instead of [[Russell universes]], as well as interpreting [[relations]] [[predicative mathematics|predicatively]] as prop-valued type families instead of functions into a [[type of all propositions]]. The axioms are as follows:

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(B)}{\Gamma \vdash \mathrm{JMEq}(A, B, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(B)}{\Gamma, p:\mathrm{JMEq}(A, B, u, v), q:\mathrm{JMEq}(A, B, u, v) \vdash \mathrm{propTruncJMEq}(A, B, u, v, p, q):\mathrm{Id}_{\mathrm{JMEq}(A, B, u, v)}(p, q)}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash u:\mathrm{El}(A)}{\Gamma \vdash \mathrm{refl}(A, u):\mathrm{JMEq}(A, A, u, u)}$$

$$\frac{\Gamma, A:U, B:U, u:\mathrm{El}(A), v:\mathrm{El}(B), e:\mathrm{JMEq}(A, B, u, v) \vdash \Phi(A, B, u, v, e) \; \mathrm{type}}{\Gamma, t:\prod_{X:U} \prod_{x:\mathrm{El}(X)} \Phi(X, X, x, x, \mathrm{refl}(X, x)), A:U, B:U, u:\mathrm{El}(A), v:\mathrm{El}(B), e:\mathrm{JMEq}(A, B, u, v) \vdash \mathrm{eqIndElim}(t, A, B, u, v, e):\Phi(A, B, u, v, e)}$$

$$\frac{\Gamma, A:U, B:U, u:\mathrm{El}(A), v:\mathrm{El}(B), e:\mathrm{JMEq}(A, B, u, v) \vdash \Phi(A, B, u, v, e) \; \mathrm{type}}{\Gamma, t:\prod_{X:U} \prod_{x:\mathrm{El}(X)} \Phi(X, X, x, x, \mathrm{refl}(X, x)), A:U, u:\mathrm{El}(A) \vdash \mathrm{eqIndElim}(t, A, A, u, u, \mathrm{refl}(A, u)) \equiv t(a, u):\Phi(A, A, u, u, \mathrm{refl}(A, u))}$$

The use of Tarski universes instead of Russell universes makes it clear that John Major equality could be defined using inference rules for any type family $x:A \vdash B(x)$ instead of just the Tarski universe type family $X:U \vdash \mathrm{El}(X)$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(b)}{\Gamma \vdash \mathrm{JMEq}(a, b, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(b)}{\Gamma, p:\mathrm{JMEq}(a, b, u, v), q:\mathrm{JMEq}(a, b, u, v) \vdash \mathrm{propTruncJMEq}(a, b, u, v, p, q):\mathrm{Id}_{\mathrm{JMEq}(a, b, u, v)}(p, q)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash u:B(a)}{\Gamma \vdash \mathrm{refl}(a, u):\mathrm{JMEq}(a, a, u, u)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, a:A, b:A, u:B(a), v:B(b), e:\mathrm{JMEq}(a, b, u, v) \vdash \Phi(a, b, u, v, e) \; \mathrm{type}}{\Gamma, t:\prod_{x:A} \prod_{y:B(a)} \Phi(x, x, y, y, \mathrm{refl}(x, y)), a:A, b:A, u:B(a), v:B(b), e:\mathrm{JMEq}(a, b, u, v) \vdash \mathrm{eqIndElim}(t, a, b, u, v, e):\Phi(a, b, u, v, e)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, a:A, b:A, u:B(a), v:B(b), e:\mathrm{JMEq}(a, b, u, v) \vdash \Phi(a, b, u, v, e) \; \mathrm{type}}{\Gamma, t:\prod_{x:A} \prod_{y:B(a)} \Phi(x, x, y, y, \mathrm{refl}(x, y)), a:A, u:B(a) \vdash \mathrm{eqIndElim}(t, a, a, u, u, \mathrm{refl}(a, u)) \equiv t(a, u):\Phi(a, a, u, u, \mathrm{refl}(a, u))}$$

#### Winterhalter's axiomatization

The axioms given in [Winterhalter 2023](#Winterhalter23) are in [[Coq]] [[pseudocode]] and use [[Russell universes]]. Here, the axioms are written as [[inference rules]] in a [[deduction system]] and modified slightly to use [[Tarski universes]] instead of [[Russell universes]]. The axioms are as follows:

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(B)}{\Gamma \vdash \mathrm{JMEq}(A, B, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash u:\mathrm{El}(A)}{\Gamma \vdash \mathrm{hrefl}(A, u):\mathrm{JMEq}(A, B, u, v)}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(A) \quad \Gamma \vdash p:\mathrm{Id}_{\mathrm{El}(A)}(u, v)}{\Gamma \vdash \mathrm{eqToHeq}(A, u, v, p):\mathrm{JMEq}(A, A, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(A) \quad \Gamma \vdash p:\mathrm{JMEq}(A, A, u, v)}{\Gamma \vdash \mathrm{heqToEq}(A, u, v, p):\mathrm{Id}_{\mathrm{El}(A)}(u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma \vdash p:\mathrm{Id}_{U}(A, B) \quad \Gamma \vdash t:\mathrm{El}(A)}{\Gamma \vdash \mathrm{heqTransport}(A, B, p, t):\mathrm{JMEq}(A, B, t, \mathrm{transport}_{X:U.\mathrm{El}(X)}(A, B, p, t))}$$

The use of Tarski universes instead of Russell universes makes it clear that John Major equality could be defined using inference rules for any type family $x:A \vdash B(x)$ instead of just the Tarski universe type family $X:U \vdash \mathrm{El}(X)$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(b)}{\Gamma \vdash \mathrm{JMEq}(a, b, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash u:B(a)}{\Gamma \vdash \mathrm{hrefl}(a, u):\mathrm{JMEq}(a, b, u, v)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(a) \quad \Gamma \vdash p:\mathrm{Id}_{B(a)}(u, v)}{\Gamma \vdash \mathrm{eqToHeq}(a, u, v, p):\mathrm{JMEq}(a, a, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(a) \quad \Gamma \vdash p:\mathrm{JMEq}(a, a, u, v)}{\Gamma \vdash \mathrm{heqToEq}(a, u, v, p):\mathrm{Id}_{B(a)}(u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_{A}(a, b) \quad \Gamma \vdash t:B(a)}{\Gamma \vdash \mathrm{heqTransport}(a, b, p, t):\mathrm{JMEq}(a, b, t, \mathrm{transport}_{x:A.B(x)}(a, b, p, t))}$$

### Inference rules without UIP

It should be possible to take McBride's axiomatization of John Major equality above and simply remove the requirement that John Major equality be a proposition-valued type family. 

Then, the inference rules for forming John Major equality and terms are as follows.  First the inference rule that defines the John Major equality itself, as a [[dependent type]], in some [[context]] $\Gamma$.

Formation rule for John Major equality:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b)
    \end{array}
  }{\Gamma \vdash \mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \; \mathrm{type}}$$ 

Now the basic "introduction" rule, which says that everything is equal to itself in a canonical way.

Introduction rule for John Major equality:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash a:A \quad \Gamma \vdash y:B(a)
    \end{array}
  }{\Gamma \vdash \mathrm{refl}_{x:A.B(x)}(a, y):\mathrm{JMEq}_{x:A.B(x)}(a, a, y, y)}$$ 

Next we have the "elimination" rule: 

Elimination rule for John Major equality:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, y:B(a), z:B(b), p:\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \vdash C(a, b, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{a:A} \prod_{y:B(a)} C(a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \quad \Gamma \vdash p:\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{JMEq}_{x:A.B(x)}}(t, a, b, y, z, p):C(a, b, y, z, p)}$$

The elimination rule then says that if:

1. for any elements $a:A$ and $b:A$, any elements $y:B(a)$ and $z:B(b)$, and any John Major equality $p:\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z)$ we have a type $C(a, b, y, z, p)$, and
1. we have a specified dependent function 
$$t:\prod_{a:A} \prod_{y:B(a)} C(a,a,y,y,\mathrm{refl}_{x:A.B(x)}(a, y))$$

then we can construct a canonically defined term called the *eliminator*
$$\mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t,a,b,y,z,q):C(a,b,y,z,q)$$ 
for *any* $a$, $b$, $y$, $z$, and $q$. 

Then, we have the [[computation rule]] or [[beta-reduction]] rule. This says that for all elements $a:A$ and $y:B(a)$, substituting the dependent function $t:\prod_{a:A} \prod_{y:B(a)} C(a,a,y,y,\mathrm{refl}_{x:A.B(x)}(a, y))$ into the eliminator along [[reflexive relation|reflexivity]] for $a$ and $y$ yields an element equal to $t(a, y)$ itself.  Normally "equal" here means [[judgmental equality]] (a.k.a. definitional equality), but it is also possible for it to mean [[propositional equality]] (a.k.a. typal equality), so there are two possible computation rules.

Computation rules for John Major equality:

* Judgmental computational rule
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, y:B(a), z:B(b), p:\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \vdash C(a, b, y, z, p) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{a:A} \prod_{y:B(a)} C(a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)) \quad \Gamma \vdash a:A \quad \Gamma \vdash y:B(a)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{JMEq}_{x:A.B(x)}}(t, a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)) \equiv t(a, y):C(a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y))}$$

* Propositional computational rule
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, y:B(a), z:B(b), p:\mathrm{JMEq}_{x:A.B(x)}(a, b, y, z) \vdash C(a, b, y, z, p) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{a:A} \prod_{y:B(a)} C(a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)) \quad \Gamma \vdash a:A \quad \Gamma \vdash y:B(a)
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{JMEq}_{x:A.B(x)}}(t, a, y):\mathrm{Id}_{C(a, a, y, y, \mathrm{hrefl}_{x:A.B(x)}(a, y))}(\mathrm{ind}_{\mathrm{JMEq}_{x:A.B(x)}}(t, a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)), t(a, y))}$$

Finally, one might consider a [[uniqueness rule]] or [[eta-conversion]] rule.  But similar to the case for [[identity types]], a judgmental uniqueness rule for John Major equality implies that the type theory is an [[extensional type theory]], in which case there is not much need for John Major equality, so such a rule is almost never written down.  And as for identity types and other inductive types, the propositional/typal uniqueness rule is provable from the other four inference rules, so we don't write it out explicitly.

## Related concepts

* [[heterogeneous identity type]]

## References

For better or worse, the terminology "John Major equality" was coinded in [McBride 1999 §5.1.3](#McBride99) with reference to British political discussion of that times:

* {#McBride99} [[Conor McBride]], *Dependently Typed Functional Programs and their Proofs*, (1999) &lbrack;[pdf](https://www.lfcs.inf.ed.ac.uk/reports/00/ECS-LFCS-00-419/ECS-LFCS-00-419.pdf)&rbrack;

* {#Winterhalter23} [[Théo Winterhalter]], *A conservative and constructive translation from extensional type theory to weak type theory*, Strength of Weak Type Theory, [[DutchCATS]], 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_winterhalter.pdf))

