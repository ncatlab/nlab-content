
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

For $\mathbf{H}$ an [[(∞,1)-topos]] and $X \in \mathbf{H}$ any [[object]], the [[over-(∞,1)-category]] $\mathbf{H}/X$ is itself an $(\infty,1)$-topos: the _over-$(\infty,1)$-topos_ .

If we think of $\mathbf{H}$ as a [[big topos]], then for $X \in \mathbf{H}$ we may think of $\mathbf{H}/X \in $ [[(∞,1)-topos]] as the [[little topos]]-incarnation of $X$. The [[object]]s of $\mathbf{H}/X$ we may think of as [[(∞,1)-sheaves]] on $X$.

This corespondence between objects of $X$ and their little-topos incarnation is entirly natural: $\mathbf{H}$ is equivalently recovered as the [[(∞,1)-category]] whose objects are over-$(\infty,1)$-toposes $\mathbf{H}/X$ and whose morphisms are [[(∞,1)-geometric morphism]]s _over_ $\mathbf{H}$.

## Definition


+-- {: .un_prop}
###### Proposition

For $\mathbf{H}$ an [[(∞,1)-topos]] and $X \in \mathbf{H}$ an [[object]] also the [[over-(∞,1)-category]] $\mathbf{H}/X$ is an $(\infty,1)$-topos. This is the **over-$(\infty,1)$-topos** of $\mathbf{H}$ over $X$.

=--

This is [[Higher Topos Theory|HTT, prop 6.3.5.1 1)]].

## Properties

### Base change to the point


+-- {: .un_prop}
###### Proposition

There is canonical am [[(∞,1)-geometric morphism]]

$$
  \mathbf{H}/X 
    \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
  \mathbf{H}
$$

where the extra [[left adjoint]] $X_!$ is the obvious projection $X_! : (Y \to X) \mapsto X$, and $X_*$ is given by forming the [[(∞,1)-limit|(∞,1)-product]] with $X$.

=--

This is called an [[etale geometric morphism]]. See there for more details.


+-- {: .proof}
###### Proof

The fact that $(X_! \dashv X^*)$ follows from the universal property of the products. The fact that $X^*$ preserves [[(∞,1)-colimit]]s and hence has a further [[right adjoint]] $X_*$ by the [[adjoint (∞,1)-functor theorem]] follows from that fact that $\mathbf{H}$ has [[universal colimits]].

=--




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

### General base change

See [[base change geometric morphism]].


## Examples

+-- {: .un_prop}
###### Proposition

For $\mathbf{H} = $ [[∞Grpd]] we have that for $X \in \infty Grp$ any [[∞-groupoid]] the corresponding over-$(\infty,1)$-topos is equivalent to the [[(∞,1)-category of (∞,1)-presheaves]] on $X$:

$$
  \infty Grpd/X \simeq [X^{op}, \infty Grpd]
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is a special case of the [[(∞,1)-Grothendieck construction]]. See the section <a href="http://ncatlab.org/nlab/show/(infinity,1)-Grothendieck+construction#GrpdFibsOverGrpds">(∞,0)-fibrations over ∞-groupoids</a>.

=--

## References

Section 6.3.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects over-(∞,1)-topos]]
