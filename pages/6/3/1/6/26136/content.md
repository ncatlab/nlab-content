
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

## Idea

A form of [[heterogeneous equality]] in [[dependent type theory]].

## Definition
 {#Definition}

Given a [[type]] $A$ and an $A$-[[dependent type]] $a \colon A \;\vdash\; B(a)$, the *fibered heterogeneous identity type*  is the [[dependent type]] indexed by

1. a pair of parameters

   $$
     a ,\, a' \;\colon\;  A
   $$ 

   indexing a [[pair]] of [[fibers]] of $B$,

1. a pair of terms of these fiber types

   $$
     b \;\colon\; B(a) 
     ,\;\;\;\;
     b' \;\colon\; B(a')
   $$ 

   whose "[[heterogeneous identity type|heterogeneous]]" [[identification]] is to be witnessed,

and defined equivalently as follows:

* &lbrack;[Winterhalter 2023](#Winterhalter23), [p. 30](https://dutchcats.github.io/Weak_type_theories/slides_winterhalter.pdf#page=30)&rbrack; as the [[dependent sum type]] 

  $$
    fhId(a, b; a', b') 
    \;\coloneqq\; 
    \sum_{p \colon \mathrm{Id}_A(a, a')} 
    \mathrm{hId}(b, p, b')
  $$

  of the [[heterogeneous identity types]] 
  
  $$
   hId(b, p, b') 
   \;\equiv\; 
   \mathrm{Id}_{B(b)}\big(
     p_\ast(b)
     ,\, 
     b'
   \big)
   \,,
  $$ 

  over all [[identifications]] $p \colon \mathrm{Id}_A(a, a')$, where 

  $$
    p_\ast \,\colon\, B(a) \overset{\sim}{\to} B(a')
  $$

  denotes the [[type transport]] along $p$;


* as the [[identification type]] of [[dependent pairs]] in the [[dependent sum type]] $\sum_{x:A} B(x)$

  $$
    fhId(a, b; a', b') 
    \;\coloneqq\; 
    \mathrm{Id}_{\sum_{x:A} B(x)}
    \big(
      (a, b)
      ,\, 
      (a', b')
    \big)
    \mathrlap{\,.}
  $$

The two definitions are [[equivalence of types|equivalent]]
due to the [extensionality property](dependent+sum+type#ExtensionalityPrinciple) of [[dependent sum types]].

### Inference rules with UIP
 {#InferenceRulesWithUIP}

When the type theory has a [[set truncation axiom]] such as [[UIP]] or [[axiom K]], one could use one of the following [[inference rules]] to define fibered heterogeneous identity types: 

#### McBride's axiomatization

The axioms given in [McBride 1999](#McBride99) are in [[OLEG]] [[pseudocode]], use [[Russell universes]], and interpret relations impredicatively as functions into a [[type of all propositions]]. Here, the axioms are written as [[inference rules]] in a [[deduction system]], modified slightly to use [[Tarski universes]] instead of [[Russell universes]], as well as interpreting [[relations]] [[predicative mathematics|predicatively]] as prop-valued type families instead of functions into a [[type of all propositions]]. The axioms are as follows:

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(B)}{\Gamma \vdash \mathrm{fhId}(A, B, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(B)}{\Gamma, p:\mathrm{fhId}(A, B, u, v), q:\mathrm{fhId}(A, B, u, v) \vdash \mathrm{propTruncfhId}(A, B, u, v, p, q):\mathrm{Id}_{\mathrm{fhId}(A, B, u, v)}(p, q)}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash u:\mathrm{El}(A)}{\Gamma \vdash \mathrm{refl}(A, u):\mathrm{fhId}(A, A, u, u)}$$

$$\frac{\Gamma, A:U, B:U, u:\mathrm{El}(A), v:\mathrm{El}(B), e:\mathrm{fhId}(A, B, u, v) \vdash \Phi(A, B, u, v, e) \; \mathrm{type}}{\Gamma, t:\prod_{X:U} \prod_{x:\mathrm{El}(X)} \Phi(X, X, x, x, \mathrm{refl}(X, x)), A:U, B:U, u:\mathrm{El}(A), v:\mathrm{El}(B), e:\mathrm{fhId}(A, B, u, v) \vdash \mathrm{eqIndElim}(t, A, B, u, v, e):\Phi(A, B, u, v, e)}$$

$$\frac{\Gamma, A:U, B:U, u:\mathrm{El}(A), v:\mathrm{El}(B), e:\mathrm{fhId}(A, B, u, v) \vdash \Phi(A, B, u, v, e) \; \mathrm{type}}{\Gamma, t:\prod_{X:U} \prod_{x:\mathrm{El}(X)} \Phi(X, X, x, x, \mathrm{refl}(X, x)), A:U, u:\mathrm{El}(A) \vdash \mathrm{eqIndElim}(t, A, A, u, u, \mathrm{refl}(A, u)) \equiv t(a, u):\Phi(A, A, u, u, \mathrm{refl}(A, u))}$$

The use of Tarski universes instead of Russell universes makes it clear that fibered heterogeneous identity types could be defined using inference rules for any type family $x:A \vdash B(x)$ instead of just the Tarski universe type family $X:U \vdash \mathrm{El}(X)$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(b)}{\Gamma \vdash \mathrm{fhId}(a, b, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(b)}{\Gamma, p:\mathrm{fhId}(a, b, u, v), q:\mathrm{fhId}(a, b, u, v) \vdash \mathrm{propTruncfhId}(a, b, u, v, p, q):\mathrm{Id}_{\mathrm{fhId}(a, b, u, v)}(p, q)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash u:B(a)}{\Gamma \vdash \mathrm{refl}(a, u):\mathrm{fhId}(a, a, u, u)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, a:A, b:A, u:B(a), v:B(b), e:\mathrm{fhId}(a, b, u, v) \vdash \Phi(a, b, u, v, e) \; \mathrm{type}}{\Gamma, t:\prod_{x:A} \prod_{y:B(a)} \Phi(x, x, y, y, \mathrm{refl}(x, y)), a:A, b:A, u:B(a), v:B(b), e:\mathrm{fhId}(a, b, u, v) \vdash \mathrm{eqIndElim}(t, a, b, u, v, e):\Phi(a, b, u, v, e)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, a:A, b:A, u:B(a), v:B(b), e:\mathrm{fhId}(a, b, u, v) \vdash \Phi(a, b, u, v, e) \; \mathrm{type}}{\Gamma, t:\prod_{x:A} \prod_{y:B(a)} \Phi(x, x, y, y, \mathrm{refl}(x, y)), a:A, u:B(a) \vdash \mathrm{eqIndElim}(t, a, a, u, u, \mathrm{refl}(a, u)) \equiv t(a, u):\Phi(a, a, u, u, \mathrm{refl}(a, u))}$$

#### Winterhalter's axiomatization

The axioms given in [Winterhalter 2023](#Winterhalter23) are in [[Coq]] [[pseudocode]] and use [[Russell universes]]. Here, the axioms are written as [[inference rules]] in a [[deduction system]] and modified slightly to use [[Tarski universes]] instead of [[Russell universes]]. The axioms are as follows:

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(B)}{\Gamma \vdash \mathrm{fhId}(A, B, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash u:\mathrm{El}(A)}{\Gamma \vdash \mathrm{hrefl}(A, u):\mathrm{fhId}(A, B, u, v)}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(A) \quad \Gamma \vdash p:\mathrm{Id}_{\mathrm{El}(A)}(u, v)}{\Gamma \vdash \mathrm{eqToHeq}(A, u, v, p):\mathrm{fhId}(A, A, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash u:\mathrm{El}(A) \quad \Gamma \vdash v:\mathrm{El}(A) \quad \Gamma \vdash p:\mathrm{fhId}(A, A, u, v)}{\Gamma \vdash \mathrm{heqToEq}(A, u, v, p):\mathrm{Id}_{\mathrm{El}(A)}(u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma \vdash p:\mathrm{Id}_{U}(A, B) \quad \Gamma \vdash t:\mathrm{El}(A)}{\Gamma \vdash \mathrm{heqTransport}(A, B, p, t):\mathrm{fhId}(A, B, t, \mathrm{transport}_{X:U.\mathrm{El}(X)}(A, B, p, t))}$$

The use of Tarski universes instead of Russell universes makes it clear that fibered heterogeneous identity types could be defined using inference rules for any type family $x:A \vdash B(x)$ instead of just the Tarski universe type family $X:U \vdash \mathrm{El}(X)$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(b)}{\Gamma \vdash \mathrm{fhId}(a, b, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash u:B(a)}{\Gamma \vdash \mathrm{hrefl}(a, u):\mathrm{fhId}(a, b, u, v)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(a) \quad \Gamma \vdash p:\mathrm{Id}_{B(a)}(u, v)}{\Gamma \vdash \mathrm{eqToHeq}(a, u, v, p):\mathrm{fhId}(a, a, u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash u:B(a) \quad \Gamma \vdash v:B(a) \quad \Gamma \vdash p:\mathrm{fhId}(a, a, u, v)}{\Gamma \vdash \mathrm{heqToEq}(a, u, v, p):\mathrm{Id}_{B(a)}(u, v) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash p:\mathrm{Id}_{A}(a, b) \quad \Gamma \vdash t:B(a)}{\Gamma \vdash \mathrm{heqTransport}(a, b, p, t):\mathrm{fhId}(a, b, t, \mathrm{transport}_{x:A.B(x)}(a, b, p, t))}$$

### Inference rules without UIP

It should be possible to take McBride's axiomatization of fibered heterogeneous identity types above and simply remove the requirement that fibered heterogeneous identity types be a proposition-valued type family. 

Then, the inference rules for forming fibered heterogeneous identity types and terms are as follows.  First the inference rule that defines the fibered heterogeneous identity type itself, as a [[dependent type]], in some [[context]] $\Gamma$.

Formation rule for fibered heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b)
    \end{array}
  }{\Gamma \vdash \mathrm{fhId}_{x:A.B(x)}(a, b, y, z) \; \mathrm{type}}$$ 

Now the basic "introduction" rule, which says that everything is equal to itself in a canonical way.

Introduction rule for fibered heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma \vdash a:A \quad \Gamma \vdash y:B(a)
    \end{array}
  }{\Gamma \vdash \mathrm{refl}_{x:A.B(x)}(a, y):\mathrm{fhId}_{x:A.B(x)}(a, a, y, y)}$$ 

Next we have the "elimination" rule: 

Elimination rule for fibered heterogeneous identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, y:B(a), z:B(b), p:\mathrm{fhId}_{x:A.B(x)}(a, b, y, z) \vdash C(a, b, y, z, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{a:A} \prod_{y:B(a)} C(a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)) \\
      \Gamma \vdash a:A \quad \Gamma \vdash b:A \quad \Gamma \vdash y:B(a) \quad \Gamma \vdash z:B(b) \quad \Gamma \vdash p:\mathrm{fhId}_{x:A.B(x)}(a, b, y, z)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{fhId}_{x:A.B(x)}}(t, a, b, y, z, p):C(a, b, y, z, p)}$$

The elimination rule then says that if:

1. for any elements $a:A$ and $b:A$, any elements $y:B(a)$ and $z:B(b)$, and any fibered heterogeneous identification $p:\mathrm{fhId}_{x:A.B(x)}(a, b, y, z)$ we have a type $C(a, b, y, z, p)$, and
1. we have a specified dependent function 
$$t:\prod_{a:A} \prod_{y:B(a)} C(a,a,y,y,\mathrm{refl}_{x:A.B(x)}(a, y))$$

then we can construct a canonically defined term called the *eliminator*
$$\mathrm{ind}_{\mathrm{hId}_{x:A.B(x)}}(t,a,b,y,z,q):C(a,b,y,z,q)$$ 
for *any* $a$, $b$, $y$, $z$, and $q$. 

Then, we have the [[computation rule]] or [[beta-reduction]] rule. This says that for all elements $a:A$ and $y:B(a)$, substituting the dependent function $t:\prod_{a:A} \prod_{y:B(a)} C(a,a,y,y,\mathrm{refl}_{x:A.B(x)}(a, y))$ into the eliminator along [[reflexive relation|reflexivity]] for $a$ and $y$ yields an element equal to $t(a, y)$ itself.  Normally "equal" here means [[judgmental equality]] (a.k.a. definitional equality), but it is also possible for it to mean [[propositional equality]] (a.k.a. typal equality), so there are two possible computation rules.

Computation rules for fibered heterogeneous identity types:

* Judgmental computational rule
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, y:B(a), z:B(b), p:\mathrm{fhId}_{x:A.B(x)}(a, b, y, z) \vdash C(a, b, y, z, p) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{a:A} \prod_{y:B(a)} C(a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)) \quad \Gamma \vdash a:A \quad \Gamma \vdash y:B(a)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{fhId}_{x:A.B(x)}}(t, a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)) \equiv t(a, y):C(a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y))}$$

* Propositional computational rule
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \\
      \Gamma, a:A, b:A, y:B(a), z:B(b), p:\mathrm{fhId}_{x:A.B(x)}(a, b, y, z) \vdash C(a, b, y, z, p) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{a:A} \prod_{y:B(a)} C(a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)) \quad \Gamma \vdash a:A \quad \Gamma \vdash y:B(a)
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{fhId}_{x:A.B(x)}}(t, a, y):\mathrm{Id}_{C(a, a, y, y, \mathrm{hrefl}_{x:A.B(x)}(a, y))}(\mathrm{ind}_{\mathrm{fhId}_{x:A.B(x)}}(t, a, a, y, y, \mathrm{refl}_{x:A.B(x)}(a, y)), t(a, y))}$$

Finally, one might consider a [[uniqueness rule]] or [[eta-conversion]] rule.  But similar to the case for [[identity types]], a judgmental uniqueness rule for fibered heterogeneous identity types implies that the type theory is an [[extensional type theory]], in which case there is not much need for fibered heterogeneous identity types, so such a rule is almost never written down.  And as for identity types and other inductive types, the propositional/typal uniqueness rule is provable from the other four inference rules, so we don't write it out explicitly.

## Related concepts

* [[heterogeneous identity type]]

## References

* {#McBride99} [[Conor McBride]], §5.1.3 in: *Dependently Typed Functional Programs and their Proofs*, (1999) &lbrack;[pdf](https://www.lfcs.inf.ed.ac.uk/reports/00/ECS-LFCS-00-419/ECS-LFCS-00-419.pdf)&rbrack;

  > (who speaks of "John Major equality" [McBride 1999 ](#McBride99) with reference to British political discussion of that times)

* {#Winterhalter23} [[Théo Winterhalter]], *A conservative and constructive translation from extensional type theory to weak type theory*, Strength of Weak Type Theory, [[DutchCATS]], 11 May 2023. ([slides](https://dutchcats.github.io/Weak_type_theories/slides_winterhalter.pdf))

[[!redirects John Major equality]]

[[!redirects fibred heterogeneous identity]]
[[!redirects fibred heterogeneous identities]]

[[!redirects fibered heterogeneous identity]]
[[!redirects fibered heterogeneous identities]]

[[!redirects fibred dependent identity]]
[[!redirects fibred dependent identities]]

[[!redirects fibered dependent identity]]
[[!redirects fibered dependent identities]]

[[!redirects fibred heterogeneous identity type]]
[[!redirects fibred heterogeneous identity types]]

[[!redirects fibered heterogeneous identity type]]
[[!redirects fibered heterogeneous identity types]]

[[!redirects fibred dependent identity type]]
[[!redirects fibred dependent identity types]]

[[!redirects fibered dependent identity type]]
[[!redirects fibered dependent identity types]]

[[!redirects fibred heterogeneous equality]]
[[!redirects fibred heterogeneous equalities]]

[[!redirects fibered heterogeneous equality]]
[[!redirects fibered heterogeneous equalities]]

[[!redirects fibred dependent equality]]
[[!redirects fibred dependent equalities]]

[[!redirects fibered dependent equality]]
[[!redirects fibered dependent equalities]]

[[!redirects fibred heterogeneous equality type]]
[[!redirects fibred heterogeneous equality types]]

[[!redirects fibered heterogeneous equality type]]
[[!redirects fibered heterogeneous equality types]]

[[!redirects fibred dependent equality type]]
[[!redirects fibred dependent equality types]]

[[!redirects fibered dependent equality type]]
[[!redirects fibered dependent equality types]]

[[!redirects fibred heterogeneous path]]
[[!redirects fibred heterogeneous paths]]

[[!redirects fibered heterogeneous path]]
[[!redirects fibered heterogeneous paths]]

[[!redirects fibred dependent path]]
[[!redirects fibred dependent paths]]

[[!redirects fibered dependent path]]
[[!redirects fibered dependent paths]]

[[!redirects fibred heterogeneous path type]]
[[!redirects fibred heterogeneous path types]]

[[!redirects fibered heterogeneous path type]]
[[!redirects fibered heterogeneous path types]]

[[!redirects fibred dependent path type]]
[[!redirects fibred dependent path types]]

[[!redirects fibered dependent path type]]
[[!redirects fibered dependent path types]]

[[!redirects fibred heterogeneous identification]]
[[!redirects fibred heterogeneous identifications]]

[[!redirects fibered heterogeneous identification]]
[[!redirects fibered heterogeneous identifications]]

[[!redirects fibred dependent identification]]
[[!redirects fibred dependent identifications]]

[[!redirects fibered dependent identification]]
[[!redirects fibered dependent identifications]]

[[!redirects fibred heterogeneous identification type]]
[[!redirects fibred heterogeneous identification types]]

[[!redirects fibered heterogeneous identification type]]
[[!redirects fibered heterogeneous identification types]]

[[!redirects fibred dependent identification type]]
[[!redirects fibred dependent identification types]]

[[!redirects fibered dependent identification type]]
[[!redirects fibered dependent identification types]]

