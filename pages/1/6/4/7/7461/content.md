## Idea

The notion of a _classifying (∞,1)-topos_ is the [[vertical categorification]] of the notion of [[classifying topos]] to the context of [[(∞,1)-category]] theory.

Any (∞,1)-topos $K$ by definition classifies the ∞-geometric morphisms into it in that it is the representing object of $geom(-,K)$.

## Examples
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

category: higher topos theory
