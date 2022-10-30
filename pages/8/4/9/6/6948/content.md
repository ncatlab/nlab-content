+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[logic]], the _universal quantifier_ "$\forall$" is the [[quantifier]] used to express, given a [[proposition]] $\phi$ about [[terms]] $x$ of [[type]] $X$, the proposition

$$
  \forall x : X, \phi x
  \,,
$$

which asserts that for each term $x$ the proposition $\phi(x)$ is [[true]].

## Definition

In terms of the [[internal logic]] in some ambient [[topos]] $\mathcal{E}$, 

* a [[type]] $X$ is given by an [[object]] $X \in \mathcal{E}$, 

* the [[proposition]] $\phi$ is a [[(-1)-truncated]] object of the [[over-topos]] $\mathcal{E}/X$;

* a [[truth value]] is a [[(-1)-truncated]] object of $\mathcal{E}$ itself.

Universal quantification is essentially the [[direct image]] [[right adjoint]] of the canonical [[étale geometric morphism]]

$$
    \mathcal{E}/X
    \stackrel{\overset{\exists}{\to}}{\stackrel{\overset{- \times X}{\leftarrow}}{\underset{\forall}{\to}}}
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
    \stackrel{\overset{\exists}{\to}}{\stackrel{\overset{- \times X}{\leftarrow}}{\underset{\forall}{\to}}}
    &
    \mathcal{E}
    \\
    \mathllap{\tau_{\leq_{-1}}}\downarrow \uparrow
    &&
    \mathllap{\tau_{\leq_{-1}}}\downarrow \uparrow
    \\
    \tau_{\leq_{-1}} 
    \mathcal{E}/X
    &&
    \tau_{\leq_{-1}}\mathcal{E}
  }
  \,.
$$

Dually, the extra [[left adjoint]] $\exists$ expresses the [[existential quantifier]].  (The situation with the universal quantifier is somewhat simpler than for the existential one, since the dependent product automatically preserves (-1)-truncated objects, whereas the dependent sum does not.)

The same makes verbatim sense also in the [[(∞,1)-logic]] of any [[(∞,1)-topos]].

## Examples

Let $\mathcal{E} = $ [[Set]], let $X = \mathbb{N}$ be the set of [[natural number]]s and let $\phi := 2\mathbb{N} \hookrightarrow \mathbb{N}$ be the [[subset]] of even natural numebrs. This expresses the [[proposition]] $\phi(x) := IsEven(x)$. 

Then the [[dependent product]] 

$$
  (\phi \in Set/{\mathbb{N}})
  \mapsto 
  (\prod_{x : X} \phi(x) \in Set)
$$

is the set of [[section]]s of the [[bundle]] $2 \mathbb{N} \hookrightarrow \mathbb{N}$. But since over odd numbers the [[fiber]] of this bundle is the [[empty set]], there is no possible value of such a section and hence the set of sections is itself the [[empty set]], so the statement "all natural numbers are even" is, indeed, [[false]].

[[!redirects universal quantifier]]
[[!redirects universal quantifiers]]
[[!redirects universal quantification]]
[[!redirects universal quantifications]]
