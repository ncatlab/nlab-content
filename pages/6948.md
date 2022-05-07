
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

In [[logic]], the _universal quantifier_ "$\forall$" is the [[quantifier]] used to express, given a [[predicate]] $\phi$ with a [[free variable]] $x$ of [[type]] $T$, the [[proposition]]

$$
  \forall\, x\colon T, \phi x
  \,,
$$

which is intended to be [[true]] if and only if $\phi a$ is true for every possible element $a$ of $T$.

Note that it is quite possible that $\phi a$ may be provable (in a given [[context]]) for every *[[term]]* $a$ of type $T$ that can actually be constructed in that context yet $\forall x\colon T, \phi x$ cannot be proved.  Therefore, we cannot define the quantifier by taking the idea literally and applying it to terms.


## Definition

We work in a [[logic]] in which we are concerned with which [[propositions]] entail which propositions (in a given [[context]]); in particular, two propositions which entail each other are considered equivalent.

Let $\Gamma$ be an arbitrary [[context]] and $T$ a [[type]] in $\Gamma$ so that $\Delta \coloneqq \Gamma, x\colon T$ is $\Gamma$ extended by a [[free variable]] $x$ of type $T$.  We assume that we have a [[weakening rule]] that allows us to interpret any proposition $Q$ in $\Gamma$ as a proposition $Q[\hat{x}]$ in $\Delta$.  Fix a proposition $P$ in $\Delta$, which we think of as a [[predicate]] in $\Gamma$ with the free variable $x$.  Then the __universal quantification__ of $P$ is any proposition $\forall\, x\colon T, P$ in $\Gamma$ such that, given any proposition $Q$ in $\Gamma$, we have

*  $Q \vdash_{\Gamma}\forall\, x\colon T, P$ if and only if $Q[\hat{x}] \vdash_{\Gamma, x\colon T} P$.

It is then a theorem that the universal quantification of $P$, if it exists, is unique.  The existence is typically asserted as an axiom in a particular logic, but this may be also be deduced from other principles (as in the topos-theoretic discussion below).

Often one makes the appearance of the free variable in $P$ explicit by thinking of $P$ as a [[propositional function]] and writing $P(x)$ instead; to go along with this one usually conflates $Q$ and $Q[\hat{x}]$.  Then the rule appears as follows:

*  $Q \vdash_{\Gamma}\forall\, x\colon T, P(x)$ if and only if $Q \vdash_{\Gamma, x\colon T} P(x)$.


In terms of [[semantics]] (as for example topos-theoretic semantics; see the next section), the weakening from $Q$ to $Q[\hat{x}]$ corresponds to [[pullback|pulling back]] along a [[product]] projection $\sigma(T) \times A \to A$, where $\sigma(T)$ is the interpretation of the type $T$, and $A$ is the interpretation of $\Gamma$. In other words, if a statement $Q$ read in context $\Gamma$ is interpreted as a [[subobject]] of $A$, then the statement $Q$ read in context $\Delta = \Gamma, x \colon T$ is interpreted by pulling back along the projection, obtaining a subobject of $\sigma(T) \times A$. 

As observed by [[Lawvere]], we are not particularly constrained to product projections; we can pull back along any map $f \colon B \to A$. (Often we have a class of [[display maps]] and require $f$ to be one of these.) Alternatively, any pullback functor $f^\ast\colon Set/A \to Set/B$ can be construed as pulling back along an object $X = (f \colon B \to A)$, i.e., along the unique map $!\colon X \to 1$ corresponding to an object $X$ in the slice $Set/A$, since we have the identification $Set/B \simeq (Set/A)/X$. 


## In topos theory / in terms of adjunctions

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

* [[necessity]]

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
