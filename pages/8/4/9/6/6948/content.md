
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
 {#Idea}

In [[first-order logic]], the _universal quantifier_ "$\forall$" is the [[quantifier]] used to express --- given a [[predicate]] $P$ with a [[free variable]] $t$ of [[type]] $T$ --- the [[proposition]] denoted

$$
  \underset{
    t \colon T  
  }
  {\forall} P(t)
  \,,
$$

which is meant to be [[true]] if and only if $P(t)$ holds true for ALL possible [[elements]] $t$ of $T$ (all [[terms]] of [[type]] $T$) --- whence the notation "A" (even if upside-down) for this quantifier.

This notion is "dual" (in fact *[[adjoint functor|adjoint]]*, see [below](#InTermOfAdjunctions)) to the [[existential quantifier]] "$\exists$" which asserts that $P(t)$ holds true for *some* $t$.

But beware that is quite possible that $P(t)$ may be provable (in a given [[context]]) for every *[[term]]* $t$ of type $T$ that can actually be constructed in that context, and yet 
$  
  \underset{
    t \colon T  
  }
  {\forall} \phi(t)
$ 
cannot be proved: The proper internal definition of universal quantification is as a [[right adjoint]] to [[context extension]] as brought out by the definition (eq:FirstDefinition) below and expanded on [further below](#InTermOfAdjunctions).
 



## Definition
 {#Definition}

We work in a [[logic]] in which we are concerned with which [[propositions]] entail which other propositions (in a given [[context]]); in particular, two propositions which entail each other are considered [[logical equivalence|logically equivalent]], denoted by "$\Leftrightarrow$".

Let 

* $\Gamma$ be an arbitrary [[context]],

* $T$ a [[dependent type]] in $\Gamma$,

so that 

* $\Delta \coloneqq \Gamma, T$ is the [[context extension]] of $\Gamma$ by a [[free variable]] $t$ of [[type]] $T$.  

We assume that we have a [[weakening rule]] that allows us to interpret any proposition $Q$ in $\Gamma$ as  

* $T^\ast Q$ being a proposition in $\Delta$.  

Then for

* $P$ a [[proposition]] in $\Delta$, which we think of as a [[predicate]] in $\Gamma$ with the [[free variable]] of type $T$, 

its __universal quantification__ is any proposition $\underset{T}{\forall} P$ in $\Gamma$ such that, *given any proposition $Q$ in $\Gamma$*, we have:

\[
  \label{FirstDefinition}
  Q \;\vdash_{\Gamma}\; 
  \underset{
    T
  }{\forall} 
  \;
  P
  \;\;\;\;\;\;\;
    \Leftrightarrow
  \;\;\;\;\;\;\;
  T^\ast Q \;\vdash_{\Gamma, T}\; P
  \,.
\] 

It is then a theorem that universal quantification of $P$, if it exists, is unique.  The existence is typically asserted as an [[axiom]] in a particular logic, but this may be also be deduced from other principles (as in the topos-theoretic discussion [below](#InTermOfAdjunctions)).

Often one makes the appearance of the [[free variable]] in $P$ explicit by thinking of $P$ as a [[propositional function]] and writing $P(t)$ instead.  Then the rule appears as follows:

\[
  Q \;\vdash_{\Gamma}\;
  \underset{
    t \colon T
  }{\forall}  P(t)
  \;\;\;\;\;\;
    \Leftrightarrow
  \;\;\;\;\;\;
  T^\ast Q \;\vdash_{\Gamma, t \colon T}\; P(t)
  \,.
\]


In terms of [[semantics]] (as for example topos-theoretic semantics; see [below](#InTermOfAdjunctions)), the [[context extension]] from $Q$ to $T^\ast Q$ corresponds to [[pullback|pulling back]] along a [[product]] projection $\sigma(T) \times A \to A$, where $\sigma(T)$ is the interpretation of the type $T$, and $A$ is the interpretation of $\Gamma$. In other words, if a statement $Q$ read in context $\Gamma$ is interpreted as a [[subobject]] of $A$, then the statement $Q$ read in context $\Delta = \Gamma, t \colon T$ is interpreted by pulling back along the [[projection]], obtaining a subobject of $\sigma(T) \times A$. 

As observed by [[Lawvere]], we are not particularly constrained to product projections; we can pull back along any map $f \colon B \to A$. (Often we have a class of [[display maps]] and require $f$ to be one of these.) Alternatively, any pullback functor $f^\ast\colon Set/A \to Set/B$ can be construed as pulling back along an object $X = (f \colon B \to A)$, i.e., along the unique map $!\colon X \to 1$ corresponding to an object $X$ in the slice $Set/A$, since we have the identification $Set/B \simeq (Set/A)/X$. 

In [[natural deduction]] the [[inference rules]] for the universal quantifier are given as 

$$\frac{\Gamma, x:A \vdash P(x) \; \mathrm{prop}}{\Gamma \vdash \forall x:A.P(x) \; \mathrm{prop}} \qquad \frac{\Gamma, x:A \vdash P(x) \; \mathrm{true}}{\Gamma \vdash \forall x:A.P(x) \; \mathrm{true}} \qquad \frac{\Gamma \vdash \forall x:A.P(x) \; \mathrm{true}}{\Gamma, x:A \vdash P(x) \; \mathrm{true}}$$

## Internal universal quantifier in set theory

In [[set theory]], recall that a [[predicate]] on a [[set]] $A$ in the [[internal logic of set theory]] is represented by the [[preimage]] $i^*(a)$ of an [[injection]] $i:B \hookrightarrow A$. Because $i$ is an [[injection]], each preimage $i^*(a)$ is a [[subsingleton]] for all $a \in A$, which represents the internal [[propositions]] of the [[set theory]]. The **internal universal quantifier** is represented by the [[Cartesian product]] of the family of sets $(i^*(a))_{a \in A}$:

$$\forall a \in A.i^*(a) \coloneqq \prod_{a \in A} i^*(a)$$


## In topos theory / in terms of adjunctions
 {#InTermOfAdjunctions}

In terms of the [[internal logic]] in some ambient [[topos]] $\mathcal{E}$, 

* a [[type]] $X$ is given by an [[object]] $X \in \mathcal{E}$, 

* the [[predicate]] $\phi$ is a [[(-1)-truncated]] object of the [[over-topos]] $\mathcal{E}/X$;

* a [[truth value]] is a [[(-1)-truncated]] object of $\mathcal{E}$ itself.

Universal quantification is essentially the restriction of the [[direct image]] [[right adjoint]] of a canonical [[étale geometric morphism]] $X_\ast$, 

$$
    \mathcal{E}/X
    \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
    \mathcal{E} 
  \,,
$$

where $X^\ast$ is the functor that takes an object $A$ to the [[product]] projection $\pi \colon X \times A \to X$, where $X_! = \Sigma_X$ is the [[dependent sum]] (i.e., forgetful functor taking $f \colon A \to X$ to $A$) that is left adjoint to $X^\ast$, and where $X_\ast = \Pi_X$ is the [[dependent product]] operation that is right adjoint to $X^\ast$. 

The dependent product operation restricts to [[propositions]] by pre- and postcomposition with the [[truncated|truncation]] [[adjunctions]]

$$
  \tau_{\leq -1} \mathcal{E}
  \stackrel{\overset{\tau_{\leq -1}}{\leftarrow}}{\underset{}{\hookrightarrow}}
  \mathcal{E}
$$

to give universal quantification over the domain (or context) $X$: 

$$
  \array{
    \mathcal{E}/X
    & 
    \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
    &
    \mathcal{E}
    \\
    {}^\mathllap{\tau_{\leq_{-1}}}\downarrow \uparrow
    &&
    {}^\mathllap{\tau_{\leq_{-1}}}\downarrow \uparrow
    \\
    \tau_{\leq_{-1}} 
    \mathcal{E}/X
    &
     \stackrel{\overset{\exists_X}{\to}}{\stackrel{\overset{}{\leftarrow}}{\underset{\forall_X}{\to}}}
    &
    \tau_{\leq_{-1}}\mathcal{E}
  }
  \,.
$$

Dually, the extra [[left adjoint]] $\exists_X$, obtained from the dependent sum $X_!$ by pre- and post-composition with the truncation adjunctions, expresses the [[existential quantifier]].  (The situation with the universal quantifier is somewhat simpler than for the existential one, since the dependent product automatically preserves $(-1)$-truncated objects (= subterminal objects), whereas the dependent sum does not.)

The same makes sense, verbatim, also in the [[(∞,1)-logic]] of any [[(∞,1)-topos]].

This interpretation of universal quantification as the right adjoint to context extension is also used in the notion of _[[hyperdoctrine]]_.

## In dependent type theory

In [[dependent type theory]], the universal quantifier is the [[propositional truncation]] of the [[dependent product type]] of a family of [[h-propositions]]:

$$\forall (x:A).B(x) \coloneqq \left[\prod_{x:A} B(x)\right]$$

The axiom of [[function extensionality]] or [[weak function extensionality]] implies that the dependent product type of a family of h-propositions is always an h-proposition. 

One doesn't need all [[dependent product types]] to define universal quantifiers. The [[isProp]] types are definable without all dependent product types, by use of [[center of contraction]], which are also definable without all dependent product types. 

Formation rules for the universal quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isProp}(B(x))}{\Gamma \vdash \forall (x:A).B(x) \; \mathrm{type}}$$

Introduction rules for the universal quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isProp}(B(x)) \quad \Gamma, x:A \vdash b(x):B(x)}{\Gamma \vdash \lambda(x:A).b(x):\forall (x:A).B(x)}$$

Elimination rules for the universal quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isProp}(B(x)) \quad \Gamma \vdash f:\forall (x:A).B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash f(a):B[a/x]}$$

Computation rules for the universal quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isProp}(B(x)) \quad \Gamma, x:A \vdash b(x):B(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_\forall:\lambda(x:A).b(x)(a) =_{B[a/x]} b[a/x]}$$

Uniqueness rules for the universal quantifier:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isProp}(B(x)) \quad \Gamma \vdash f:\forall (x:A).B(x)}{\Gamma \vdash \eta_\forall:f =_{\forall (x:A).B(x)} \lambda(x).f(x)}$$

Closure of universal quantifiers under h-propositions rule:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash p(x):\mathrm{isProp}(B(x))}{\Gamma \vdash \mathrm{weakfunext}:\mathrm{isProp}(\forall (x:A).B(x))}$$

This means that one could define the type-theoretic internal logic of a [[Heyting category]] or [[Boolean category]] which are not [[locally cartesian closed]], for [[strongly predicative mathematics]]. 

## Examples

Let $\mathcal{E} = $ [[Set]], let $X = \mathbb{N}$ be the set of [[natural number]]s and let $\phi \coloneqq 2\mathbb{N} \hookrightarrow \mathbb{N}$ be the [[subset]] of even natural numbers. This expresses the [[proposition]] $\phi(x) \coloneqq IsEven(x)$. 

Then the [[dependent product]] 

$$
  (\phi \in Set/{\mathbb{N}})
  \mapsto 
  (\prod_{x\colon X} \phi(x) \in Set)
$$

is the set of [[section]]s of the [[bundle]] $2 \mathbb{N} \hookrightarrow \mathbb{N}$. But since over odd numbers the [[fiber]] of this bundle is the [[empty set]], there is no possible value of such a section and hence the set of sections is itself the [[empty set]], so the statement "all natural numbers are even" is, indeed, [[false]].

## Related concepts

* [[necessity]], [[example]]

* [[existential quantifier]]

* [[generalized quantifier]]

[[!include logic symbols -- table]]


## References

The observation that [[substitution]] forms an [[adjoint pair]]/[[adjoint triple]] with the existential/universal quantifiers is due to

* {#Lawvere69} [[William Lawvere]], _Adjointness in Foundations_, ([tac:16](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

* [[William Lawvere]], _Quantifiers and sheaves_, Actes, Congr&#232;s intern, math., 1970. Tome 1, p. 329 &#224; 334 ([pdf](http://www.mathunion.org/ICM/ICM1970.1/Main/icm1970.1.0329.0334.ocr.pdf))

and further developed in 

* [[William Lawvere]], _Equality in hyperdoctrines and
comprehension schema as an adjoint functor_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14.



[[!redirects universal quantifier]]
[[!redirects universal quantifiers]]
[[!redirects universal quantification]]
[[!redirects universal quantifications]]

[[!redirects every]]

