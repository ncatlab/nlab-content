
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


### As $(\infty,1)$-sheaves on the big $(\infty,1)$-site of an object {#SheavesOnBigSite}

We spell out how $\mathbf{H}/X$ is the [[(∞,1)-category of (∞,1)-sheaves]] over the [[big site]] of $X$.

+-- {: .un_prop}
###### Proposition
**(forming overcategories commutes with passing to presheaves)**

Let $C$ be a [[small (∞,1)-category]] and $X : K \to C$
a [[diagram]]. Write $C_{/X}$ 
and $PSh(C)/_{X}$ for the corresponding [[over (∞,1)-categories]], where 
-- notationally implicitly -- we use the [[(∞,1)-Yoneda embedding]] $C \to PSh(C)$.

Then we have an [[equivalence of (∞,1)-categories]]

$$
  PSh(C/X) \stackrel{\simeq}{\to} PSh(C)/X
  \,.
$$

=--

This appears as [[Higher Topos Theory|HTT, 5.1.6.12]]. For more on this see [[(∞,1)-category of (∞,1)-presheaves]].

+-- {: .un_remark}
###### Remark

Here we may think of $C/X$ as the [[big site]] of the object $c \in PSh(C)$, hence of $PSh(C/X)$ as presheaves on $X$.

=--

+-- {: .un_prop}
###### Proposition

Let $C$ be equipped with a [[subcanonical coverage]], let $X \in C$ and regard $C/X$ as an [[(∞,1)-site]] with the [[big site]]-[[coverage]]. Then we have

$$
  Sh(C/X) \simeq Sh(C)/X
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion of <a href="http://ncatlab.org/nlab/show/adjoint+(infinity%2C1)-functor#OnSlices">adjoint (∞,1)-functors on over-(∞,1)-categories</a> [[adjoint (∞,1)-functor]]s we have that the adjunction

$$
  (F \dashv i) : Sh(C) \stackrel{\overset{F}{\leftarrow}}{\hookrightarrow}
  PSh(C)
$$

passes to an adjunction on the [[over-(∞,1)-categories]]

$$
  (F/X \dashv i/X) : Sh(C)/X \stackrel{\overset{F}{\leftarrow}}{\hookrightarrow}
  PSh(C)/X
  \,,
$$

(where we are using that $F  i X \simeq X$ by the assumption that the coverage is subcanonical, so that the representable $X$ is a [[(∞,1)-sheaf]]), such that $i/X$ is still a [[full and faithful (∞,1)-functor]] (where we are using that the unit $X \to F i X$ is an equivalence, since $X$ is a sheaf). 

Since moreover the [[(∞,1)-limit]]s in $Sh(C)/X$ are computed as limits in $Sh(C)$ over diagrams with a bottom element adjoined (as discussed at <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#InOvercategories">limits in over-(∞,1)-categories</a>) it follows that with $F$ preserving all finite limits, so does $F/X$.

In summary we have that $(F/X \dashv i/X)$ is a [[reflective sub-(∞,1)-category]] of $PSh(C/X)$ hence is the [[(∞,1)-category of (∞,1)-sheaves]] on the category $C/X$ for _some_ [[(∞,1)-site]]-structure. But since $F/X$ inverts precisely those morphisms that are inverted by $F$ under the projection $PSh(C)/X \to PSh(C)$, it follows that this is the [[big site]] structure on $C/X$ (this is the defining property of the big site).


=--

Specifically for the $(\infty,1)$-topos $\mathbf{H} = $ [[∞Grpd]] we also have the following characterization.

+-- {: .un_prop}
###### Proposition

For $\mathbf{H} = $ [[∞Grpd]] we have that for $X \in \infty Grp$ any [[∞-groupoid]] the corresponding over-$(\infty,1)$-topos is equivalent to the [[(∞,1)-category of (∞,1)-presheaves]] on $X$:

$$
  \infty Grpd/X \simeq PSh(X) \simeq [X, \infty Grpd]
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
