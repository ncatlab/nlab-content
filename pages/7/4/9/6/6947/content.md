
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

In [[logic]], the _existential quantifier_ "$\exists$" (or _particular quantifier_) is a [[quantifier]] used to express, given a [[predicate]] $\phi$ with a [[free variable]] $x$ of [[type]] $T$, the [[proposition]]

$$
  \exists\, x\colon t, \phi x
  \,,
$$

which is intended to be [[true]] if and only if $\phi a$ is true for at least one element $a$ of $T$.


## Definition

It is quite possible that $\exists\, x\colon T, \phi x$ can be proved (in a given [[context]]) but $\phi a$ cannot be proved for any [[term]] $a$ of type $T$ that can actually be constructed in that context.

Therefore, we must define the quantifiers more carefully; one way to do this is as follows:

*  $\exists\, x\colon T, P(x) \vdash_{\Gamma} Q$ if and only if $P(x) \vdash_{\Gamma, x\colon T} Q$.

Here, $\Gamma$ is an arbitrary context, and $\Gamma, x\colon T$ is that context supplemented by a free variable $x$ of type $T$.  Note that $Q$ is (a priori) a statement in the context $\Gamma$ but also needs to make sense in the context $\Gamma, x\colon T$; therefore, our logic needs an appropriate [[weakening rule]] for this to make sense.  This definition also presumes that a statement (in any given context) can be identified precisely by placing it within the [[poset]] of statements (in that context) under entailment ($\vdash$), which is true for ordinary first-order logic.


## In topos theory

In terms of the [[internal logic]] in some ambient [[topos]] $\mathcal{E}$, 

* a [[type]] $X$ is given by an [[object]] $X \in \mathcal{E}$, 

* the [[predicate]] $\phi$ is a [[(-1)-truncated]] object of the [[over-topos]] $\mathcal{E}/X$;

* a [[truth value]] is a [[(-1)-truncated]] object of $\mathcal{E}$ itself.

Existential quantification is essentially the extra [[left adjoint]] of the canonical [[étale geometric morphism]]

$$
    \mathcal{E}/X
    \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
    \mathcal{E} 
  \,,
$$

where $(-) \times X$ is the functor that forms the [[product]] with $X$, $\exists$ is the [[dependent sum]] and $\forall$ is the [[dependent product]] operation.

This operation restricts to [[propositions]] by pre- and postcomposition with the [[truncated|truncation]] [[adjunctions]]

$$
  \tau_{\leq -1} \mathcal{E}
  \stackrel{\overset{\tau_{\leq -1}}{\leftarrow}}{\underset{}{\hookrightarrow}}
  \mathcal{E}
$$

to give

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

## Examples

Let $\mathcal{E} = $ [[Set]], let $X = \mathbb{N}$ be the set of [[natural number]]s and let $\phi \coloneqq 2\mathbb{N} \hookrightarrow \mathbb{N}$ be the [[subset]] of even natural numebrs. This expresses the [[proposition]] $\phi(x) \coloneqq IsEven(x)$. 

Then the [[dependent sum]] 

$$
  (\phi \in Set/{\mathbb{N}})
  \mapsto 
  (\sum_{x\colon X} \phi(x) \in Set)
$$

is simply the set $2 \mathbb{N} \in Set$ of even natural numebrs. Since this is [[inhabited]], its [[truncated|(-1)-truncation]] is therefore the singleton set, hence the [[truth value]] _[[true]]_. Indeed, there exists an even natural number!

Notice that before the $(-1)$-truncation the operation remembers not just _that_ there is an even number, but it remembers "all proofs that there is one", namely every example of an even number.


[[!redirects existential quantifier]]
[[!redirects existential quantifiers]]
[[!redirects existential quantification]]
[[!redirects existential quantifications]]
[[!redirects particular quantifier]]
[[!redirects particular quantifiers]]
[[!redirects particular quantification]]
[[!redirects particular quantifications]]
