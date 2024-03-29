
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

An unbounded [[chain complex]] $X_\bullet \in Ch_\bullet$

$$
  \cdots \to X_2 \stackrel{\partial}{\to} X_1 \stackrel{\partial}{\to} X_0 \stackrel{\partial}{\to} X_{-1} \stackrel{\partial}{\to} X_{-2} \stackrel{\partial}{\to} \cdots   
$$

is called _connective_ if it has no nontrivial [[homology groups]] in negative degree. Often one means more strictly that it is connective if it is concentrated in non-negative degree, hence if $X_{-n} \simeq 0$ for all $n \geq 1$, hence if it is of the form

$$
  \cdots \to X_2 \stackrel{\partial}{\to} X_1 \stackrel{\partial}{\to} X_0 \stackrel{\partial}{\to} 0 \stackrel{\partial}{\to} 0 \stackrel{\partial}{\to} \cdots   
  \,.
$$

Such connective chain complexes are the [[connective objects]] in the [[(infinity,1)-category of chain complexes|$\infty$-category of chain complexes]]. Rearding under the [[stable Dold-Kan correspondence]] as $H R$-[[module spectra]] they are the *[[connective spectra]]*. 

Hence a connective chain complex is in particular a [[bounded chain complex]], bounded from below.


## Examples

* The [[singular chain complex]] of a [[topological space]] is connective. This is directly related to the fact that the [[homotopy groups]] of topological spaces are in non-negative degree, as opposed to their [[stabilization]] by [[spectra]], which may have homotopy groups also in negative degrees.

## Properties

### Relation to simplicial abelian groups

The [[Dold-Kan correspondence]] asserts that connective chain complexes of [[abelian groups]] are equivalent to [[abelian group|abelian]] [[simplicial groups]]. 

## Related concepts

* [[connective object]], [[connective spectrum]]

* [[category of chain complexes]]

  * [[chain complex]]

  * [[chain map]], [[quasi-isomorphism]]

  * [[chain homotopy]]

  * [[model structure on chain complexes]]

  * [[elliptic chain complex]]

* [[cochain complex]]

* [[bounded chain complex]]

* [[filtered chain complex]]

* [[perfect chain complex]]


[[!redirects connective chain complex]]
[[!redirects connective chain complexes]]
