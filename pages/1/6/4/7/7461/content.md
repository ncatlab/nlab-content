
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The notion of a _classifying (∞,1)-topos_ is the [[vertical categorification]] of the notion of [[classifying topos]] to the context of [[(∞,1)-category]] theory.

Any (∞,1)-topos $K$ by definition classifies the ∞-geometric morphisms into it in that it is the representing object of $geom(-,K)$.

## Examples

### For objects and pointed objects
 {#ForObjectsAndPointedObjects}

Write $\infty Grpd_{fin}$ for the [[(∞,1)-category]] of [[finite homotopy types]] and write $\infty Grpd_{fin}^{\ast/}$ for its [[pointed objects]].

For $\mathbf{H}$ any [[base (∞,1)-topos]], the [[(∞,1)-presheaf (∞,1)-topos]] 

$$
  \mathbf{H}[X] \coloneqq PSh(\infty Grpd_{fin}^{op}, \mathbf{H}) 
$$ 

is the classifying $\infty$-topos for [[objects]], and

$$
  \mathbf{H}[X_\ast] \coloneqq PSh((\infty Grpd_{fin}^{\ast/})^{op}, \mathbf{H}) 
$$ 

is the classifying $\infty$-topos for [[pointed objects]].

For $K \in \infty Grpd_{fin}^{\ast/}$, write $R(K) \in (\infty Grpd_{fin}^{\ast/})^{op} \hookrightarrow \mathbf{H}[X_\ast]$ for its [[formal dual]] under [[(∞,1)-Yoneda embedding]].  The generic pointed object in $\mathbf{H}[X_\ast]$ is that [[representable functor|represented]] by the [[0-sphere]]:

$$
  X_\ast = R(S^0)
  \,.
$$



### For local structures

A special case of this is the notion of a classifying (∞,1)-topos for a geometry in the sense of [[geometry (for structured (∞,1)-toposes)|structured spaces]]:

The geometry $\mathcal{G}$ is the [[(∞,1)-category]] that plays role of the syntactic theory. For $\mathcal{X}$ an [[(∞,1)-topos]], a model of this theory is a limits and covering-preserving [[(∞,1)-functor]]

$$
  \mathcal{G} \to \mathcal{X}
  \,.
$$

The [[Yoneda embedding]] followed by [[∞-stackification]] 


$$
  \mathcal{G} \stackrel{Y}{\to} PSh_{(\infty,1)}(\mathcal{G})
  \stackrel{\bar(-)}{\to} Sh_{(\infty,1)}(\mathcal{G})
$$

constitutes a model of $\mathcal{G}$ in the (Cech) [[∞-stack]] [[(∞,1)-topos]] $Sh_{(\infty,1)}(\mathcal{G})$ and exhibits it as the classifying topos for such models (geometries):

This is _[[Structured Spaces]]_ [prop 1.4.2](http://arxiv.org/PS_cache/arxiv/pdf/0905/0905.0459v1.pdf#page=26).

[[!redirects classifying (∞,1)-topos]]
[[!redirects classifying (∞,1)-toposes]]

[[!redirects classifying (∞,1)-topoi]]

[[!redirects classifying (infinity,1)-topos]]
[[!redirects classifying (infinity,1)-toposes]]
[[!redirects classifying (infinity,1)-topoi]]


category: higher topos theory
