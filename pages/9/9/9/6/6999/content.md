
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $\Gamma : \mathcal{E} \to \mathcal{B}$ a [[functor]] we say that it _has [[codiscrete object]]s_ if it has a  [[full and faithful functor|full and faithful]] [[right adjoint]] $coDisc : \mathcal{B} \hookrightarrow \mathcal{E}$. 

This is for instance the case for the [[global section]] [[geometric morphism]] of a [[local topos]] $ (Disc \dashv \Gamma \dashv coDisc) \;\colon\; \mathcal{E} \to \mathcal{B}$. 

In this situation, we say that a  **concrete object** $X \in \mathcal{E}$ is one for which the $(\Gamma \dashv coDisc)$-[[unit of an adjunction]] is a [[monomorphism]].

If $\mathcal{E}$ is a [[sheaf topos]], this is called a [[concrete sheaf]].

If $\mathcal{E}$ is a [[cohesive (∞,1)-topos]] then this is called a [[concrete (∞,1)-sheaf]] or the like.

The dual notion is that of a [[co-concrete object]].

## Properties

$\Gamma$ is a [[faithful functor]] on [[morphisms]] whose [[codomain]] is concrete. 

### Concretification factorization

+-- {: .num_prop #ConcretificationFactorization}
###### Proposition

For $\mathbf{H}$ a [[local topos]], write

$$
  \mathbf{H}_{conc} 
  \overset{ \phantom{AAAA} }{\hookrightarrow}
  \mathbf{H}
$$

for its [[full subcategory]] of [[concrete objects]].

Then there is a sequence of [[reflective subcategory]]-inclusions that factor the $(\Gamma \dashv coDisc)$-adjunction as

$$
  \Gamma \;\dashv\; coDisc
  \;\;\colon\;\;
  \mathbf{H}
  \array{
    \overset{\phantom{AA} conc \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA} \iota_{conc} \phantom{AA}}{\hookleftarrow}
  }
  \mathbf{H}_{conc}
  \array{
    \overset{\phantom{AAA}}{\longrightarrow}
    \\
    \overset{\phantom{AAA}}{\hookleftarrow}
  }
  Set
$$

=--


+-- {: .proof}
###### Proof

For the adjunction on the right, we just need to observe that for every [[set]] $S \in Set$, the [[codiscrete object]] $coDisc(S)$ is [[concrete object|concrete]], which is immediate by [[idempotent monad|idempotency]] of $\sharp$ and the fact that every [[isomorphism]] is also a [[monomorphism]].

For the adjunction on the left we claim that the [[left adjoint]] $conc$ ([[concretification]]), is given by sending each [[object]] to the [[image]] of its $(\Gamma \dashv coDisc)$ [[adjunction unit]] $\eta^\sharp$:

$$
  conc \;\colon\; X \mapsto im(\eta^\sharp_X)
  \,.
$$

The [[adjunction unit]] of $(conc \dashv \iota_{conc})$ is provided by the [[epimorphism]] in the [[(epi, mono) factorization system|epi/mono-factorization]], which, being [[orthogonal factorization system|orthogonal]], is [[functorial factorization|functorial]]:

\[
  \label{NaturalitySquareForConcretificationUnit}
  \array{
    X_1 
      &\underoverset{epi}{\eta^{conc}_{X_1}}{\longrightarrow}& 
    im(\eta^\sharp_{X_1})
      &\underset{mono}{\longrightarrow}&
    \sharp X_1
    \\
    \big\downarrow && \big\downarrow && \big\downarrow
    \\
    X_2 
      &\underoverset{epi}{\eta^{conc}_{X_2}}{\longrightarrow}& 
    im(\eta^\sharp_{X_2})
      &\underset{mono}{\longrightarrow}&
    \sharp X_2
  }
\]

To see this, it is sufficient, to show that $\eta^{conc}$ is a [[universal morphism]] in the sense discussed at _[[adjoint functors]]_. Hence consider any morphism $f \;\colon\; X_1 \to X_2$ with $X_2 \in \mathbf{H}_{conc} \hookrightarrow \mathbf{H}$. Then we need to show that there is a unique diagonal morphism as below, that makes the following _top left triangle_ [[commuting diagram|commute]]:

$$
  \array{
    X_1 
      &\overset{\phantom{AA} f \phantom{AA}}{\longrightarrow}& 
    X_2
    \\
    {}^{\mathllap{epi}}\big\downarrow^{\mathrlap{\eta^{conc}_{X_1}}} 
      &{}^{\mathllap{\exists !}}\nearrow& 
    \big\downarrow^{\mathrlap{mono}}
    \\
    im(\eta^\sharp_{X_1}) 
      &\underset{}{\longrightarrow}& 
    \sharp X_2
  }
$$

Now, from (eq:NaturalitySquareForConcretificationUnit), we have a [[commuting square]] as shown. Here the left morphism is an [[epimorphism]] by construction, while the right morphism is a [[monomorphism]] by assumption on $X_2$. With this, the [[(epi, mono) factorization system|epi/mono-factorization]] says that there is a diagonal [[lift]] which makes _both_ triangles [[commuting diagram|commute]].

It remains to see that the lift is unique with the property of making (just) the top left triangle commute. But this is equivalently the statement that the left morphism is an [[epimorphism]].

=--



## Related concepts

* [[concretification]]

[[!include cohesion - table]]


## References

* [[Mike Shulman]], _Discreteness, Concreteness, Fibrations, and Scones_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/discreteness_concreteness_fibr.html))
 {#Shulman}

[[!redirects concrete objects]]