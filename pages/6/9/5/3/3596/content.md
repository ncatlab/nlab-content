
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
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

> {#FirstLawOfThought} The [[first original law of thought]] ([WdL &#167;875](Science+of+Logic#875)): everything is identical with itself ([WdL &#167;863](Science+of+Logic#863)), no two things are like each other ([WdL &#167;903](Science+of+Logic#903)).

## Idea

In [[intensional type theory]] under the [[propositions as types]] paradigm, an **identity type** (or **equality type**) is the incarnation of [[equality]].  That is, for any [[type]] $A$ and any [[terms]] $x,y:A$, the type $Id_A(x,y)$ is "the type of [[proofs]] that $x=y$" or "the type of reasons why $x=y$".

To contrast with "computational" or [[definitional equality]], inhabitation of an identity type is sometimes called **propositional equality**.  The identity type $Id_A(x,y)$ is sometimes written $Eq_A(x,y)$ or just $(x=y)$, but in this article we reserve the latter for definitional equality.

In *[[set-level type theory]]*, such as that modeled in the [[internal logic]] of a 1-category, equality is an [[h-proposition]], and hence each $Id_A(x,y)$ is a [[subsingleton]].  However, in higher type theories, which are the internal type theory of [[higher category theory|higher categories]], identity types represent [[path objects]] and are highly nontrivial. In the [[internal logic of an (∞,1)-topos]], one speaks of _[[homotopy type theory]]_. In these cases, identity types are also known as __path types__ or __path space types__ and are sometimes written as $Path_A(x,y)$ instead of $Id_A(x,y)$.

There are many different notions of identity type appearing in the type theory literature. This includes the following: 

* Martin-Löf identity types

* [[cubical path types]]

* Swan identity types

* (higher) observational identity types

The key factors distinguishing these identity types from other type families is the fact that given a term $x:A$, each type $Id_A(x,x)$ of the type family has a term $\mathrm{refl}(x):Id_A(x,x)$, and satisfy what is called the **J-rule**, **path induction** or **identification elimination**. In [[dependent type theory]] with [[dependent product types]] the J-rule states that given any type family $C(x, y, p)$ indexed by $x:A$, $y:A$ and $p:Id_A(x,y)$, and an element $c(x):C(x, x, \mathrm{refl}(x))$ for each $x:A$, there is an element $J(x, y, p):C(x, y, p)$ for all $x:A$, $y:A$ and $p:Id_A(x,y)$, such that $J(x, x, \mathrm{refl}(x))$ is equal to $c(x)$. 

However, since there are two notions of [[equality]] in type theory, there are similarly two notions of the J-rule in type theory. The **definitional J-rule** states that $J(x, x, \mathrm{refl}(x))$ is definitionally equal to $c(x)$ (i.e. $J(x, x, \mathrm{refl}(x)) = c(x)$). The **propositional J-rule** or **typal J-rule** states that there is a dependent term 
$$q(x):Id_{C(x,x,\mathrm{refl}(x))}(J(x, x, \mathrm{refl}(x)), c(x))$$
Identity types which satisfy the definitional J-rule could be called **strict identity types**, while identity types which only satisfy the propositional J-rule could be called **weak identity types**, in parallel with similar definitions for a (weak and strict) [[Tarski universe]]. Martin-Löf identity types come in both strict and weak flavours. However, most other identity types in the literature, such as cubical path types and higher observational identity types, are only weak identity types.

Each kind of identity type also has one or more corresponding notions of [[dependent identity type]].  In some cases, such as cubical path types and higher observational identity types, the ordinary identity type is exactly a special case of the dependent one, where the dependence is constant or the base path is reflexivity.  In other cases, such as some versions of the Martin-Lof dependent identity type, one or both of these degenerate forms of dependent identity type don't reduce definitionally to the simple one, but are only equivalent to it.

## Definition in Martin-Löf type theory
 {#Definition}

The definition of identity types was originally given in explicit form by [[Per Martin-Löf|Martin-Löf]], in terms of introduction and elimination rules.  Later, it was realized that this was a special case of the general notion of [[inductive type]].  We will discuss both formulations.

* [with introduction and elimination rules](#ExplicitDefinition).

* [in terms of inductive types](#InTermsOfInductiveTypes) 

### With introduction and elimination rules
 {#ExplicitDefinition}

The rules for forming identity types and terms are as follows (expressed in [[sequent calculus]]).  First the rule that defines the identity type itself, as a [[dependent type]], in some [[context]] $\Gamma$.

**[[type formation]]**

$$\frac{\Gamma \vdash A:Type}
{\Gamma, x:A, y:A \vdash Id_A(x,y):Type}$$


Now the basic "introduction" rule, which says that everything is equal to itself in a canonical way.

**[[term introduction]]**

$$\frac{\Gamma \vdash A:Type}
{\Gamma, x:A \vdash r(x) : Id_A(x,x)}$$

To a category theorist, it might be more natural to call this $1_X$.  The traditional notation $r(x)$ indicates that this is a canonical proof of the *[[reflexive relation|reflexivity]]* of equality.

Then we have the "elimination" rule, which is easily the most subtle and powerful.

**[[term elimination]]**

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, \Delta(x,x,r(x)) \vdash t : C(x,x,r(x))}
{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash J(t;x,y,p) : C(x,y,p)}$$

Ignore the presence of the additional context $\Delta$ for now; it is unnecessary if we also have [[dependent product type]]s.  The elimination rule then says that if:

1. for any $x,y:A$ and any reason $p:Id_A(x,y)$ why they are the same, we have a type $C(x,y,p)$, and
1. if $x$ and $y$ are actually identical and $p:Id_A(x,x)$ is the reflexivity proof $r(x)$, then we have a specified term $t:C(x,x,r(x))$,

then we can construct a canonically defined term $J(t;x,y,p):C(x,y,p)$ for *any* $x$, $y$, and $p:Id_A(x,y)$, by "[[transport|transporting]]" the term $t$ along the proof of equality $p$.  In homotopical or categorical models, this can be viewed as a "path-lifting" property, i.e. that the [[display map]]s are some sort of [[fibration]].  This can be made precise with the [[identity type weak factorization system]].

A particular case is when $C$ is a term representing a proposition according to the propositions-as-types philosophy.  In this case, the elimination rule says that in order to prove a statement is true about all $x,y,p$, it suffices to prove it in the special case for $x,x,r(x)$.

Finally, we have the "computation" or [[β-reduction]] rule.  This says that if we substitute along a [[reflexive relation|reflexivity]] proof, nothing happens. There are two possible computation rules, which result in strict and weak identity types respectively

**[[computation rule]] for strict identity types**

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, \Delta(x,x,r(x)) \vdash t : C(x,x,r(x))}
{\Gamma, x:A, \Delta(x,x,r(x)) \vdash J(t;x,x,r(x)) = t}$$

Note that the equality $=$ in the conclusion of this computation rule is [[definitional equality]], not an instance of the identity/equality type itself.

**[[computation rule]] for weak identity types**

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, \Delta(x,x,r(x)) \vdash t : C(x,x,r(x))}
{\Gamma, x:A, \Delta(x,x,r(x)) \vdash q(x):Id_{C(x,x,r(x))}(J(t;x,x,r(x)) ,t)}$$

These rules may seem a little ad-hoc, but they are actually a particular case of the general notion of [[inductive type]].

### In terms of inductive types
 {#InTermsOfInductiveTypes}

Using [[inductive types]] the notion of identity types is encoded in a single line (see [Licata 11](#Licata11), [Shulman 12](#Shulman12)). 

In [[Coq]] notation we can say

    Inductive id {A} : A -> A -> Type := idpath : forall x, id x x.   

In other words, the identity type of $A$ is inductively generated by [[reflexive relation|reflexivity]] $x = x$ (the "[[first law of thought]]"), in the same way that the [[natural numbers]] are inductively generated by [[zero]] and [[successor]].  From this, the above introduction, elimination, and computation rules are all derived automatically.

This is the approach to Martin-Lof identity types taken by implementations of [[homotopy type theory]] in [[proof assistants]] such as [[Coq]] or [[Agda]].  See, for instance, [Overture.v](#Overturev)

An essentially equivalent way to give the definition, due to Paulin-Mohring, is

    Inductive id {A} (x:A) : A -> Type := idpath : id x x.   

The difference here is that now $x$ is a *parameter* of the inductive definition rather than an *index*.  In other words, the first definition says "for each type $A$, we have a type $Id_A$ dependent on $A\times A$, inductively defined by a constructor $idpath$ which takes an element $x\colon A$ as input and yields output in $Id_A(x,x)$" while the second definition says "for each type $A$ and each element $x\colon A$, we have a type $Id_A(x)$ dependent on $A$, inductively defined by a constructor $idpath$ which takes *no* input and yields output in $Id_A(x)(x)$."  The two formulations can be proven equivalent, but sometimes one is more convenient than the other.


### Extensionality and $\eta$-conversion
 {#EtaConversion}

Almost all types in type theory can be given both [[β-reduction]] and [[η-reduction]] rules.  $\beta$-reduction specifies what happens when we apply an eliminator to a term obtained by a constructor; $\eta$-reduction specifies the reverse.  Above we have formulated only the $\beta$-reduction rule for identity types; the $\eta$-conversion rule would be the following:

$$\frac{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash C(x,y,p):Type \qquad
\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,x,r(x)) \vdash t : C(x,y,p)}
{\Gamma, x:A, y:A, p:Id_A(x,y), \Delta(x,y,p) \vdash J(t[x/y, r(x)/p];x,y,p) = t}$$

This says that if $C$ is a type which we can use the eliminator $J$ to construct a term of, but we already *have* a term $t$ of that type, then if we restrict $t$ to [[reflexive relation|reflexivity]] inputs and then apply $J$ to construct a term of type $C$, the result is the same as the term $t$ we started with.  As in the $\beta$-reduction rule, the $=$ in the conclusion refers to [[definitional equality]].

This $\eta$-conversion rule has some very strong consequences.  For instance, suppose $x\colon A$, $y\colon A$, and $p\colon Id_A(x,y)$, and let $C \coloneqq A$.  Then with $t=x$, the $\eta$-conversion rule tells us that $x = J(x[x/y,r(x)/p];x,y,p)$.  And with $t=y$, the $\eta$-conversion rule tells us that $y = J(y[x/y,r(x)/p];x,y,p)$.  But substituting $x$ for $y$ (and $r(x)$ for $p$) in the term $y$ simply yields the term $x$, which is the same as the result of substituting $x$ for $y$ and $r(x)$ for $p$ in the term $x$.  Thus, we have

$$x = J(x;x,y,p) = y$$

In other words, if $Id_A(x,y)$ is inhabited (that is, $x$ and $y$ are propositionally equal) then in fact $x$ and $y$ are definitionally equal.  Moreover, by a similar argument we can show that

$$p = J(p[x/y, r(x)/p];x,y,p) = J(r(x)[x/y,r(x)/p];x,y,p) = r(x).$$

(Here we are eliminating into the type $C(x,y,p) \coloneqq Id_A(x,y)$.  The term $r(x)$ may be regarded as belonging to this type, because we have already shown that $x$ and $y$ are *definitionally* equal.)

Thus, the definitional $\eta$-conversion rule for identity types implies that the type theory is [[extensional type theory|extensional]] in a very strong sense.  (This was observed already in ([Streicher](#Streicher)).)  For this reason, in [[homotopy type theory]] we do not assume the $\eta$-conversion rule for identity types.

This sort of extensionality in type theory is also problematic for non-homotopical reasons: since type-checking in dependent type theory depends on definitional equality, but the above rule implies that definitional equality depends on inhabitation of identity types, this makes definitional equality and hence type-checking *undecidable* in the formal computational sense.  Thus, $\eta$-conversion for identity types is often omitted (as in [[Coq]]).

On the other hand, it is possible to prove a *propositional* version of $\eta$-conversion using only the identity types as defined above without definitional $\eta$-conversion.  In other words, given the hypotheses of the above $\eta$-conversion rule, we can construct a term belonging to the type

$$ Id_{C(x,y,p)}(J(t[x/y, r(x)/p];x,y,p), t). $$

This has none of the bad consequences of definitional $\eta$-conversion, and in particular does not imply that the type theory is extensional.  The argument that $p\colon Id_A(x,y)$ implies $x=y$ becomes the tautologous statement that if $p\colon Id_A(x,y)$ then $p\colon Id_A(x,y)$, while the subsequent argument that $p= r(x)$ fails because $x$ and $y$ are no longer *definitionally* equal, so $r(x)$ does not have type $Id_A(x,y)$.  We can *[[transport]]* it along $p$ to obtain a term of this type, but then we obtain only that $p$ is equal to the transport of $r(x)$ along $p$, which is a perfectly intensional/homotopical statement.

## Definition in observational type theory

Identity types in [[observational type theory]] and [[higher observational type theory]] are defined in a different manner than they are in [[Martin-Löf type theory]]. 

In higher observational type theory, identity types have the same formation rule as Martin-Löf identity types do:

$$\frac{\Gamma \vdash A:Type}
{\Gamma, x:A, y:A \vdash Id_A(x,y):Type}$$

However, it does not have global elimination or computation rules. Instead, it has a local computation rule for each particular type. For example, the identity type of the product type $A \times B$ has the following computation rule:

$$Id_{A \times B} (s, t) \equiv Id_A(\pi_1 s, \pi_1 t) \times Id_B (\pi_2 s, \pi_2 t)$$

### For types in universes 

We are working in a [[dependent type theory]] with Tarski-style [[universes]].

The [[identity types]] in a universe in higher observational type theory have the following formation rule:

$$\frac{A:\mathcal{U} \quad a:\mathcal{T}_\mathcal{U}(A) \quad b:\mathcal{T}_\mathcal{U}(A)}{\mathrm{id}_A(a, b):\mathcal{U}}$$

We define a general congruence term called ap

$$\frac{x:A \vdash f:B \quad p:\mathrm{id}_A(a, a^{'})}{\mathrm{ap}_{x.f}(p):\mathrm{id}_B(f[a/x], f[a^{'}/x])}$$

and the reflexivity terms:

$$\frac{a:A}{\mathrm{refl}_{a}:\mathrm{id}_A(a, a)}$$

and computation rules for identity functions

$$\mathrm{ap}_{x.x}(p) \equiv p$$

and for constant functions $y$

$$\mathrm{ap}_{x.y}(p) \equiv \mathrm{refl}_{y}$$

Thus, ap is a higher dimensional explicit substitution. There are definitional equalities

$$\mathrm{ap}_{x.f}(\mathrm{refl}_{a}) \equiv \mathrm{refl}_{f[a/x]}$$

$$\mathrm{ap}_{y.g}(\mathrm{ap}_{x.f}(p)) \equiv \mathrm{ap}_{x.g[f/y]}(p)$$

$$\mathrm{ap}_{x.t}(p) \equiv \mathrm{refl}_{t}$$

for constant term $t$. 

### For universes

Let $A \cong_\mathcal{U} B$ be the type of [[bijective correspondences]] between two terms of a universe $A:\mathcal{U}$ and $B:\mathcal{U}$, and let $\mathrm{id}_\mathcal{U}(A, B)$ be the identity type between two terms of a universe $A:\mathcal{U}$ and $B:\mathcal{U}$. Then there are rules

$$\frac{R:A \cong_\mathcal{U} B}{\Delta(R):\mathrm{id}_\mathcal{U}(A, B)} \qquad \frac{P:\mathrm{id}_\mathcal{U}(A, B)}{\nabla(P):A \cong_\mathcal{U} B} \qquad \frac{R:A \cong_\mathcal{U} B}{\nabla(\Delta(R)) \equiv R}$$

### Identity types in universes and singleton contractibility ###

Given a term of a universe $A:\mathcal{U}$

$$\mathrm{id}_{\mathcal{T}_\mathcal{U}(A)} \equiv \pi_1(\nabla(\mathrm{refl}_A))$$

with terms representing [[singleton contractibility]]. 

$$\pi_1(\pi_2(\nabla(\mathrm{refl}_A)):\prod_{a:\mathcal{T}_\mathcal{U}(A)} \mathrm{isContr}\left(\sum_{b:\mathcal{T}_\mathcal{U}(A)} \mathrm{id}_{\mathcal{T}_\mathcal{U}(A)}(a, b)\right)$$

$$\pi_2(\pi_2(\nabla(\mathrm{refl}_A))):\prod_{b:\mathcal{T}_\mathcal{U}(A)} \mathrm{isContr}\left(\sum_{a:\mathcal{T}_\mathcal{U}(A)} \mathrm{id}_{\mathcal{T}_\mathcal{U}(A)}(a, b)\right)$$

## Definition in cubical type theory

The primary identity types are the nondependent [[cubical path types]] in [[cubical type theory]]. Like the identity types in higher observational type theory, they do not satisfy the definitional version of identification elimination; only the propositional version of identification elimination. See [[cubical path type]] for more information on the construction of the cubical path types. 

Some cubical type theories include a second identity type which satisfies the definitional version of identification elimination. This is called [[Swan's identity type]], and is defined by the following rules:

Identity types in [[cubical type theory]] are called **path types** and are defined using a primitive interval.  

## Categorical semantics

We discuss the [[categorical semantics]] for identity types in the extensional case, and identity types in the [[categorical semantics of homotopy type theory]] in the intensional case.


In categorical models of [[extensional type theory]], generally every [[morphism]] of the category is allowed to represent a [[dependent type]], and the extensional identity types are represented by [[diagonal]] maps $A\to A\times A$.

By contrast, in models of [[intensional type theory]], there is only a particular class of [[display maps]] or [[fibrations]] which are allowed to represent dependent types, and intensional identity types are represented by [[path objects]] $P A \to A \times A$.

Both of these cases apply in particular to models in the [[category of contexts]] of the type theory itself, i.e. the [[term model]].

### Prerequisites

By the standard construction of [[mapping path spaces]] out of 
[[path space objects]], the existence of identity types allows one to construct a [[weak factorization system]].

Conversely, since any weak factorization system gives rise to [[path objects]] by factorization of [[diagonal maps]], one may hope to construct a [[model]] of type theory with identity types in a category equipped with a WFS $(L,R)$.  There are four obstacles in the way of such a construction.

1. In order to handle the additional [[context]] $\Delta$ in the explicit definition above, it turns out to be necessary to assume that $L$-maps are preserved by [[pullback]] along $R$-maps between $R$-objects.  (Such a condition is also necessary in order to interpret type-theoretic [[dependent products]] in a [[locally cartesian closed category]].)

1. This enables us to define identity types with their elimination and computation rules "locally", i.e. for each type individually.  However, every construction in type theory is stable under [[substitution]].  This means that if $y\colon Y\vdash A(y)\colon Type$ is a dependent type and $f\colon X\to Y$ is a morphism, then the identity type $x\colon X \vdash Id_{A(f(x))}(-,-)\colon Type$ is the same whether we first construct $Id_{A(y)}$ and then substitute $f(x)$ for $y$, or first substitute $f(x)$ for $y$ to obtain $A(f(x))$ and then construct its identity type.  In order for this to hold up to isomorphism, we need to require that the WFS have *stable path objects* --- a choice of path object data in each slice category which is preserved by pullback.  In [Warren 2008](#Warren08) it is shown that any [[simplicial model category]] in which the [[cofibrations]] are the [[monomorphisms]] can be equipped with stable path objects, while [Garner & van den Berg 2011](#vdBergGarner11) it is shown that the presence of internal path-categories also suffices.

1. The eliminator term $J$ of identity types in type theory is also preserved by substitution.  This imposes an additional *[[coherence]]* requirement which is tricky to obtain categorically.  See [Warren 2008](#Warren08) and [Garner & van den Berg 2011](#vdBergGarner11) for methods that ensure this, such as by invoking an [[algebraic weak factorization system]].  It can also be handled *a la* [[Vladimir Voevodsky|Voevodsky]] by using a (possibly [[univalence axiom|univalent]]) [[universe]].

1. Finally, substitution in type theory is strictly functorial/[[associativity|associative]], whereas it is modeled categorically by pullback which is generally not strictly so.  This is a general issue with the categorical interpretation of [[dependent type theory]], not something specific to identity types.  It can be resolved by passing to a [[split fibration]] which is equivalent to the [[codomain fibration]], or by making use of a [[universe]].  See [[categorical model of dependent types]].

### Interpretation in a type-theoretic model category

Assume then that a category $\mathcal{C}$ with suitable WFSs has been chosen, for instance a [[type-theoretic model category]]. Then

* The interpretation of a type $ \vdash A : Type$ is as a [[fibrant object]] $[\vdash A : Type]$ which we will just write "$A$" for short. 

* **type formation** 
  
  The identity type $a, b : A \vdash Id_A(a,b) : Type$ is interpreted as [[generalized the|the]] [[path space object]] [[fibration]] 
  
  $$
    \array{
       A^I
       \\
       \downarrow
       \\
       A \times A
    }
  $$

* **term introduction**

  By definition of [[path space object]], there exists a lift $\sigma$ in 
  
  $$
    \array{
       && A^I
       \\
       & {}^{\mathllap{\sigma}}\nearrow& \downarrow
       \\
       A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  By the [[universal property]] of the [[pullback]] this is equivalently a [[section]] of the [[pullback]] of the path space object along the [[diagonal]] morphism $(id,id) : A \to A \times A$.

  $$
    \array{
       && (id,id)^* A^I &\to& A^I
       \\
       &{}^{\mathllap{\sigma}}\nearrow& \downarrow & & \downarrow
       \\
       A &=& A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  Since $(id, id)^* A^I$ is the interpretation of the [[substitution]]  
  $a : A \vdash Id_A (a,a) : Type$ in this sense $\sigma$ is now the interpretation of a term $a : A \vdash r_A : Id_A (a,a)$. 

* **term elimination**

  A type depending on an identity type

  $$
    a, b : A, p : Id_A(a,b) \vdash C(a,b,p)
  $$

  is interpreted as a [[fibration]]

  $$
    \array{
      C
      \\
      \downarrow
      \\
      A^I
    }
    \,.
  $$

  The [[substitution]] $C(a,a,r_a)$ is interpreted by the [[pullback]]

  $$
    \array{
      (id,id)^* C &\to& C
      \\
      \downarrow && \downarrow
      \\
      A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  Therefore a [[term]] $t : C(a,a,r_a)$ is interpreted as a [[section]] of this pullback

  $$
    \array{
      && (id,id)^* C &\to& C
      \\
      &{}^{\mathllap{t}}\nearrow& \downarrow && \downarrow
      \\
      A &=& A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  By the [[universal property]] of the pullback, this is equivalently a morphism $t$ in 

  $$
    \array{
      && C
      \\
      & {}^{\mathllap{t}}\nearrow & \downarrow
      \\
      A &\stackrel{(id,id)}{\to}& A \times A
    }
    \,.
  $$

  The elimination rule says that given such $t$, there exists a compatible section of $C \to A^I$. If we redraw the previous diagram as a square, then this section is a _[[lifting problem|lift]]_ in that diagram

  $$
    \array{   
      A &\to& C
      \\
      {}^{\mathllap{r}}\downarrow &\nearrow& \downarrow
      \\
      A^I &=& A^I
    }
    \,.
  $$

  In particular, if $C$ itself is the pullback of a fibration $D \to B$ along a morphism $A^I \to B$, then $r$ has the left lifting property also against that fibration

  $$
    \array{   
      A &\to& C &\to& D
      \\
      {}^{\mathllap{r}}\downarrow &\nearrow& \downarrow && \downarrow
      \\
      A^I &=& A^I &\to& B
    }
    \,.
  $$

  So the term elimination rule says that the interpretaton $A \to A^I$ of $a : A \vdash r(a) : Id_A (a,a)$ has the [[left lifting property]] against all fibrations, hence that $A \to A^I$ is to be interpreted as an acyclic cofibration.

 

### Weak $\omega$-groupoids

Some of the first work noticing the homotopical / higher-categorical interpretation of identity types (see below) focused on the fact that the tower of iterated identity types of a type has the structure of an internal *[[algebraic definition of higher categories|algebraic]]* [[∞-groupoid]].

In retrospect, this is roughly an algebraic version of the standard fact that every object of a model category (or more generally a [[category of fibrant objects]] or a category with a weak factorization system) admits a [[simplicial resolution]] which is an [[internalization|internal]] [[Kan complex]], i.e. a nonalgebraic $\infty$-groupoid.  Note, however, that the first technical condition above (stability of $L$-maps under pullback along $R$-maps) seems to be necessary for the algebraic version of the result to go through.

## Related concepts

* [[identity of indiscernibles]]

* [[intensional type theory]], [[extensional type theory]]

* [[transport]]

* [[action on identifications]]

* [[dependent identity type]]

* [[axiom K]]

* [[uniqueness of identity proofs]]

* [[identity system]]

* [[cocylinder]]

* [[observational equality]]

* [[loop space type]]

* [[encode-decode method]]


## References
 {#References}

### Explicit definition
 {#ReferencesExplicitDefinition}

The [[induction principle]] for identity types (also known as "path induction" or the "[[J-rule]]") is first stated in

* {#MartinLof75} [[Per Martin-Löf]], §1.7 and p. 94 of: _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80** Pages 73-118,  Elsevier 1975 (<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926))

and in the modern form of [[inference rules]] in 

* Bengt Nordström, Kent Petersson, Jan M. Smith, §8.1 of: *Programming in Martin-Löf's Type Theory*, Oxford University Press (1990) &lbrack;[webpage](https://www.cse.chalmers.se/research/group/logic/book/), [pdf](https://www.cse.chalmers.se/research/group/logic/book/book.pdf), [[NordstromPeterssonSmith-TypeTheory.pdf:file]]&rbrack;

with early survey in §1.0.1 of: 

* {#Warren08} [[Michael Warren]], *Homotopy theoretic aspects of constructive type theory*, PhD thesis (2008) &lbrack;[pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf), [[Warren-HomotopyTypeTheory.pdf:file]]&rbrack;


See also (?):

* [[Per Martin-Löf]], p. 169 (17 of 23) in: *Constructive Mathematics and Computer Programming*, Studies in Logic and the Foundations of Mathematics Volume 104, 1982, Pages 153-175 (<a href="https://doi.org/10.1016/S0049-237X(09)70189-2">doi:10.1016/S0049-237X(09)70189-2</a>)

* [[Per Martin-Löf]], p. 31-34 in: _Intuitionistic type theory_, Lecture notes Padua 1984 (notes by [[Giovanni Sambin]]), Bibliopolis, Napoli (1984) ([pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]])


The observation that the Id-induction principle (the J-rule) is equivalent to [[transport]] ("[[salva veritate]]") together with [[contractible type|contractibility]] of the type of identifications ("by reversal of identifications") is stated in:

* [[Thierry Coquand]], slides 26-28 of: *Equality and dependent type theory* (2011) &lbrack;[pdf](https://www.cse.chalmers.se/~coquand/equality.pdf), [[Coquand-EqualityAndDependentTypeTheory.pdf:file]]&rbrack;

further highlighted in

* {#LadymanPresnell15} [[James Ladyman]], [[Stuart Presnell]], §6.3 of: *Identity in Homotopy Type Theory, Part I: The Justification of Path Induction*, Philosophia Mathematica **23** 3 (2015) 386–406 &lbrack;[doi:10.1093/philmat/nkv014](https://doi.org/10.1093/philmat/nkv014), [pdf](http://philsci-archive.pitt.edu/11079/1/Identity_in_HTT_public.pdf)&rbrack;

and the proof of the equivalence is spelled out in:

* Lennard Götz, §4.2 of: *Martin-Löf's J-rule*, LMU (2018) &lbrack;[pdf](https://www.math.lmu.de/~petrakis/Goetz.pdf)&rbrack; 


  
Discussion of issues of [[extensional type theory|extensional]]/[[intensional type theory]]:

* {#Hofmann95} [[Martin Hofmann]], _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh, (1995) ([ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]])

* {#Streicher} [[Thomas Streicher]], _Investigations Into Intensional Type Theory_, Habilitationsschrift ([pdf](http://www.mathematik.tu-darmstadt.de/~streicher/HabilStreicher.pdf))
 
The observation that Id



### As inductive types
 {#ReferencesByInductiveTypes}

* {#Licata11} [[Dan Licata]], _[Understanding Identity Elimination in Homotopy Type Theory](https://homotopytypetheory.org/2011/04/10/just-kidding-understanding-identity-elimination-in-homotopy-type-theory/)_, 2011

* {#Shulman12} [[Mike Shulman]], _Inductive types and identity types_, 2012 ([pdf](https://home.sandiego.edu/~shulman/hottseminar2012/03induction-handout1up.pdf))

* {#Overture.v} [https://github.com/HoTT/HoTT/blob/master/theories/Basics/Overture.v](https://github.com/HoTT/HoTT/blob/master/theories/Basics/Overture.v#L169-L170)

### In (higher) observational type theory

* [[Thorsten Altenkirch]] and [[Conor McBride]], _Towards observational type theory_ ([pdf](http://strictlypositive.org/ott.pdf))

* [[Conor McBride]], [Hier Soir, an OTT Hierarchy](http://mazzo.li/epilogue/index.html%3Fp=1098.html)

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 2* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-05.pdf), [video](https://www.youtube.com/watch?v=5ciDNfmvMdU))

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 3* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-05-12.pdf), [video](https://www.youtube.com/watch?v=9pDddxB7LbE))

### Weak factorization systems

* [[Michael Warren]], _Homotopy theoretic aspects of constructive type theory_, PhD thesis (2008) ([pdf](http://www.andrew.cmu.edu/user/awodey/students/warren.pdf))

* [[Steve Awodey]] and [[Michael Warren]], _Homotopy theoretic models of identity types_, [arXiv](http://arxiv.org/abs/0709.0248).

* [[Nicola Gambino]], [[Richard Garner]], _The identity type weak factorisation system_, [arXiv](http://arxiv.org/abs/0803.4349)

* [[Richard Garner]], [[Benno van den Berg]], _Topological and simplicial models of identity types_, [arXiv](http://arxiv.org/abs/1007.4638).

### Types as $\infty$-groupoids

The observation that identity types witness [[groupoid]] and [[infinity-groupoid]]-structure:

* {#HofmannStreicher98} [[Martin Hofmann]], [[Thomas Streicher]]  _The groupoid interpretation of type theory_, in: [[Giovanni Sambin]] et al. (eds.), _Twenty-five years of constructive type theory_, Proceedings of a congress, Venice, Italy, October 19&#8212;21, 1995. Oxford: Clarendon Press. Oxf. Logic Guides. 36, 83-111 (1998).  ([ISBN:9780198501275](https://global.oup.com/academic/product/twenty-five-years-of-constructive-type-theory-9780198501275), [ps](http://www.mathematik.tu-darmstadt.de/~streicher/venedig.ps.gz) [[HofmannStreicherGroupoidInterpretation.pdf:file]])


* {#AwodeyWarren07} [[Steve Awodey]], [[Michael Warren]], _Homotopy theoretic models of identity type_,  Mathematical Proceedings of the Cambridge Philosophical Society vol 146, no. 1 (2009) ([arXiv:0709.0248](http://arxiv.org/abs/0709.0248))

For more see the references at _[[homotopy type theory]]_.

See also

* [Using Yoneda rather than J to present the identity type](https://www.cs.bham.ac.uk/~mhe/yoneda/yoneda.html)
 
* {#vdBergGarner11}[[Benno van den Berg]], [[Richard Garner]], *Types are weak $\omega$-groupoids*, Proceedings of the London Mathematical Society **102** 2 (2011) 370-394 &lbrack;[arXiv:0812.0298](http://arxiv.org/abs/0812.0298), [doi:10.1112/plms/pdq026](https://doi.org/10.1112/plms/pdq026)&rbrack;
 
* [[Peter LeFanu Lumsdaine]], _Weak $\omega$-categories from intensional type theory_ , ([arXiv:0812.0409](http://arxiv.org/abs/0812.0409))



[[!redirects identity types]]
[[!redirects equality type]]
[[!redirects equality types]]
[[!redirects path type]]
[[!redirects path types]]
[[!redirects path space type]]
[[!redirects path space types]]
[[!redirects stable path object]]
[[!redirects stable path objects]]
[[!redirects propositional equality]]
[[!redirects propositionally equal]]

[[!redirects intensional identity type]]
[[!redirects intensional identity types]]
[[!redirects extensional identity type]]
[[!redirects extensional identity types]]
[[!redirects identical]]

[[!redirects J-rule]]
[[!redirects path induction]]

