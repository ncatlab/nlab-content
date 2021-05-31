
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

In [[logic]], the _existential quantifier_ (or _particular quantifier_) "$\exists$" is a [[quantifier]] used to express, given a [[predicate]] $\phi$ with a [[free variable]] $x$ of [[type]] $T$, the [[proposition]]

$$
  \exists\, x\colon T, \phi x
  \,,
$$

which is intended to be [[true]] if and only if $\phi a$ is true for at least one object $a$ of type $T$.

Note that it is quite possible that $\exists\, x\colon T, \phi x$ may be [[proof|provable]] (in a given [[context]]) yet $\phi a$ cannot be proved for any [[term]] $a$ of type $T$ that can actually be constructed in that context.  Therefore, we cannot define the quantifier by taking the idea literally and applying it to terms.


## Definition

### In logic

We work in a [[logic]] in which we are concerned with which [[propositions]] entail which propositions (in a given [[context]]); in particular, two propositions which entail each other are considered equivalent.

Let $\Gamma$ be an arbitrary [[context]] and $T$ a [[type]] in $\Gamma$ so that $\Delta \coloneqq \Gamma, x\colon T$ is $\Gamma$ extended by a [[free variable]] $x$ of type $T$.  We assume that we have a [[weakening rule]] that allows us to interpret any proposition $Q$ in $\Gamma$ as a proposition $Q[\hat{x}]$ in $\Delta$.  Fix a proposition $P$ in $\Delta$, which we think of as a [[predicate]] in $\Gamma$ with the free variable $x$.  Then the __existential quantification__ of $P$ is any proposition $\exists\, x\colon T, P$ in $\Gamma$ such that, given any proposition $Q$ in $\Gamma$, we have

*  $\exists\, x\colon T, P \vdash_{\Gamma} Q$ if and only if $P \vdash_{\Gamma, x\colon T} Q[\hat{x}]$.

It is then a theorem that the existential quantification of $P$, if it exists, is unique.  The existence is typically asserted as an axiom in a particular logic, but this may be also be deduced from other principles (as in the topos-theoretic discussion below).

Often one makes the appearance of the free variable in $P$ explicit by thinking of $P$ as a [[propositional function]] and writing $P(x)$ instead; to go along with this one usually conflates $Q$ and $Q[\hat{x}]$.  Then the rule appears as follows:

*  $\exists\, x\colon T, P(x) \vdash_{\Gamma} Q$ if and only if $P(x) \vdash_{\Gamma, x\colon T} Q$.


### In type theory

In [[type theory]] under the identification of [[propositions as types]], the existential quantifier is given by the [[bracket type]] of the [[dependent sum type]]. Existential quantifier types in general could be regarded as a particular sort of [[higher inductive type]]. In [[Coq]] syntax: 

    Inductive existquant (T:Type) (P:T->Type) : Type :=
    | exist : forall (x:T), P x -> existquant T P
    | contr0 : forall (p q : existquant T P) p == q

## Properties

### Categorical semantics

The [[categorical semantics]] of existential quantification is given by the [[n-truncated object of an (infinity,1)-category|(-1)-truncation]] of the [[dependent sum]]-construction along the [[projection]] morphism that projects out the [[free variable]] over which the existental quantifier quantifies. 

Notice that the [[categorical semantics]] of the [[context extension]] from $Q$ to $Q[\hat{x}]$ corresponds to [[base change]]/[[pullback]] along the [[product]] [[projection]] $\sigma(T) \times A \to A$, where $\sigma(T)$ is the interpretation of the type $T$, and $A$ is the interpretation of $\Gamma$. In other words, if a statement $Q$ read in context $\Gamma$ is interpreted as a [[subobject]] of $A$, then the statement $Q$ read in context $\Delta = \Gamma, x \colon T$ is interpreted by pulling back along the projection, obtaining a subobject of $\sigma(T) \times A$. 

(Often we have a class of [[display maps]] and require $f$ to be one of these.) Alternatively, any pullback functor $f^\ast\colon Set/A \to Set/B$ can be construed as pulling back along an object $X = (f \colon B \to A)$, i.e., along the unique map $!\colon X \to 1$ corresponding to an object $X$ in the slice $Set/A$, since we have the identification $Set/B \simeq (Set/A)/X$. 


Therefore in terms of the [[internal logic]] of a suitable category $\mathcal{E}$ (with sufficient pullbacks) 

* a [[type]] $X$ is given by an [[object]] $X \in \mathcal{E}$, 

* the [[predicate]] $\phi$ is a [[(-1)-truncated]] object of the [[over-topos]] $\mathcal{E}/X$;

* a [[truth value]] is a [[(-1)-truncated]] object of $\mathcal{E}$ itself.

Existential quantification is essentially the restriction of the extra [[left adjoint]] of a canonical [[étale geometric morphism]] $X_\ast$, 

$$
    (X_!\dashv X^*\dashv X_*):\mathcal{E}/X
    \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
    \mathcal{E} 
  \,,
$$

where $X^\ast$ is the functor that takes an object $A$ to the [[product]] projection $\pi \colon X \times A \to X$, where $X_! = \Sigma_X$ is the [[dependent sum]] (i.e., forgetful functor taking $f \colon A \to X$ to $A$) that is left adjoint to $X^\ast$, and where $X_\ast = \Pi_X$ is the [[dependent product]] operation that is right adjoint to $X^\ast$.

The dependent sum operation restricts to [[propositions]] by pre- and postcomposition with the [[truncated|truncation]] [[adjunctions]]

$$
  \tau_{\leq -1} \mathcal{E}
  \stackrel{\overset{\tau_{\leq -1}}{\leftarrow}}{\underset{}{\hookrightarrow}}
  \mathcal{E}
$$

to give existential quantification over the domain (or context) $X$:

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
      \stackrel{\overset{\exists}{\to}}{\stackrel{\overset{}{\leftarrow}}{\underset{\forall}{\to}}}
    &
    \tau_{\leq_{-1}} \mathcal{E}
  }
  \,.
$$

In other words, we obtain the existential quantifier by applying the [[dependent sum]], then $(-1)$-[[truncated|truncating]] the result.  This is equivalent to constructing the [[image]] as a [[subobject]] of the [[codomain]].

Dually, the [[direct image functor]] $\forall$ (dependent product) expresses the [[universal quantifier]].  (In this case, it is somewhat simpler, since the dependent product automatically preserves $(-1)$-truncated objects; no additional truncation step is necessary.)

The same makes verbatim sense also in the [[(∞,1)-logic]] of any [[(∞,1)-topos]].

This interpretation of existential quantification as the left adjoint to context extension is also used in the notion of _[[hyperdoctrine]]_.


### Frobenius reciprocity

The extential quantifier and [[context extension]] is related via [[Frobenius reciprocity]]: if $\psi$ does not have $x$ as a [[free variable]] then

$$
  \exists_x (\phi \wedge \psi)
  \Leftrightarrow
  (\exists_x \phi) \wedge \psi
  \,.
$$

## Examples

Let $\mathcal{E} = $ [[Set]], let $X = \mathbb{N}$ be the set of [[natural number]]s and let $\phi \coloneqq 2\mathbb{N} \hookrightarrow \mathbb{N}$ be the [[subset]] of even natural numbers. This expresses the [[proposition]] $\phi(x) \coloneqq IsEven(x)$. 

Then the [[dependent sum]] 

$$
  (\phi \in Set/{\mathbb{N}})
  \mapsto 
  (\sum_{x\colon X} \phi(x) \in Set)
$$

is simply the set $2 \mathbb{N} \in Set$ of even natural numbers. Since this is [[inhabited]], its [[truncated|(-1)-truncation]] is therefore the singleton set, hence the [[truth value]] _[[true]]_. Indeed, there exists an even natural number!

Notice that before the $(-1)$-truncation the operation remembers not just _that_ there is an even number, but it remembers "all proofs that there is one", namely every example of an even number.

## Related concepts

* [[possibility]]

* [[universal quantifier]]

* [[elimination of quantifiers]]

* [[generalized quantifier]]

[[!include logic symbols -- table]]


## References

The observation that [[substitution]] forms an [[adjoint pair]]/[[adjoint triple]] with the existantial/universal quantifiers is due to

* [[William Lawvere]], _[[Adjointness in Foundations]]_, ([TAC](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

* [[William Lawvere]] _Quantifiers and sheaves_, Actes, Congr&#232;s intern, math., 1970. Tome 1, p. 329 &#224; 334 ([pdf](http://www.mathunion.org/ICM/ICM1970.1/Main/icm1970.1.0329.0334.ocr.pdf))


and further developed to the notion of [[hyperdoctrines]] in

* [[William Lawvere]], _Equality in hyperdoctrines and
comprehension schema as an adjoint functor_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14.



[[!redirects existential quantifier]]
[[!redirects existential quantifiers]]
[[!redirects existential quantification]]
[[!redirects existential quantifications]]
[[!redirects particular quantifier]]
[[!redirects particular quantifiers]]
[[!redirects particular quantification]]
[[!redirects particular quantifications]]

[[!redirects existence]]

