
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $\mathbf{H}$ an [[(∞,1)-topos]] and $X \in \mathbf{H}$ any [[object]], the _over-$(\infty,1)$-topos_ $\mathbf{H}/X$ is the object $X$ itself regarded as an $(\infty,1)$-topos.

In fact $\mathbf{H}$ is equivalently recovered as the [[(∞,1)-category]] whose objects are over-$(\infty,1)$-toposes $\mathbf{H}/X$ and whose morphisms are [[(∞,1)-geometric morphism]]s _over_ $\mathbf{H}$.

## Definition

+-- {: .un_def}
###### Definitioon

For $\mathbf{H}$ an [[(∞,1)-topos]] and $X \in \mathbf{H}$ an [[object]] also the [[over-(∞,1)-category]] $\mathbf{H}/X$ is an $(\infty,1)$-topos. This is the **over-$(\infty,1)$-topos** of $\mathbf{H}$ over $X$.

=--

## Properties

+-- {: .un_prop}
###### Proposition

There is canonical am [[(∞,1)-geometric morphism]]

$$
  \mathbf{H}/X 
    \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
  \mathbf{H}
$$

where the extra [[left adjoint]] $X_!$ is the obvious projection $X_! : (Y \to X) \mapsto X$.

=--

This is called an [[etale geometric morphism]]. See there for more details.


+-- {: .un_cor}
###### Corollary

If $\mathbf{H}$ is a [[locally ∞-connected (∞,1)-topos]] then for all $X \in \mathbf{H}$ also the over-$(\infty,1)$-topos $\mathbf{H}/X$ is locally $\infty$-connected.

=--

+-- {: .proof}
###### Proof

The composite of [[(∞,1)-geometric morphism]]s 

$$
  \mathbf{H}/X 
    \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
  \mathbf{H}
  \stackrel{\overset{\Pi_{\mathbf{H}}}{\to}}{\stackrel{\overset{LConst_{\mathbf{H}}}{\leftarrow}}{\underset{\Gamma_{\mathbf{H}}}{\to}}}
  \infty Grpd
$$

is itself a geometric morphism. Since [[∞Grpd]] is the [[terminal object]] in [[(∞,1)Topos]] this must be the [[global section]] geometric morphism for $\mathbf{H}/X$. Since it has the extra left adjoint $\Pi \circ X_!$ it is locally $\infty$-connected.

=--

+-- {: .un_prop}
###### Proposition

Let $((\infty,1)Topos/\mathbf{H})_{et} \subset (\infty,1)Topos/\mathbf{H}$ be the full [[sub-(∞,1)-category]] on the [[etale geometric morphism]]s $\mathbf{H}/X \to \mathbf{H}$. Then there is an [[equivalence in an (∞,1)-category|equivalence]]

$$
  ((\infty,1)Topos/\mathbf{H})_{et}
  \simeq
  \mathbf{H}
$$

=--

See [[etale geometric morphism]] for more details.


[[!redirects over-(∞,1)-topos]]
