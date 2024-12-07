


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The analog in the context of [[(∞,1)-topos]] theory of a [[local geometric morphism]] in [[topos theory]].


## Definition

+-- {: .num_defn }
###### Definition

A **local (∞,1)-geometric morphism** $f : \mathbf{H} \to \mathbf{S}$ between [[(∞,1)-topos]]es $\mathbf{H},\mathbf{S}$ is 

* an [[(∞,1)-geometric morphism]]

  $$
    (f^* \dashv f_*) 
     : 
      \mathbf{H} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}
    {\to}}  \mathbf{S}
  $$

* such that 

  1. a further [[right adjoint]] 
     $f^! : \mathbf{S} \to \mathbf{H}$ 
     to the [[direct image]] functor exists:

     $$
       (f^* \dashv f_* \dashv f^!) : 
       \mathbf{H}
        \stackrel{\overset{f^*}{\leftarrow}}
        {\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}
       \mathbf{S}  
     $$

   1. and $f$ is a [[∞-connected (∞,1)-geometric morphism]].

If $f : \mathbf{H} \to \mathbf{S}$ is the [[global section]] [[(∞,1)-geometric morphism]] in the [[over-(∞,1)-category]] [[Topos]]$/\mathbf{S}$, then we say that $\mathbf{H}$ is a **local $(\infty,1)$-topos** over $\mathbf{S}$.

=--

+-- {: .num_remark }
###### Remark


If $\mathbf{S} = $ [[∞Grpd]] then the extra condition that $f$ is [[∞-connected (∞,1)-geometric morphism]] is automatic (see [Properties -- over ∞Grpd](#OverInfGrpd)).

=--

## Properties {#Properties}




### Over $\infty Grpd$ {#OverInfGrpd}

+-- {: .num_prop }
###### Proposition

Every local $(\infty,1)$-topos over [[∞Grpd]] has [[homotopy dimension]] $\leq 0$.

=--

See [[homotopy dimension]] for details.


+-- {: .num_prop }
###### Proposition

If an [[(∞,1)-geometric morphism]] $f : \mathbf{H} \to $ [[∞Grpd]] has an extra [[right adjoint]] $f^!$ to its [[direct image]], then $\mathbf{H}$ is an [[∞-connected (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

By the general properties of [[adjoint (∞,1)-functor]]s it is sufficient to show that $f_! f^* \simeq Id$. To see this, we use that every [[∞-groupoid]] $S \in $ [[∞Grpd]] is the [[(∞,1)-colimit]] (as discussed there) over itself of the [[(∞,1)-functor]] constant on the point: $S \simeq {\lim_\to}_{S} *$.

The [[left adjoint]] $f^*$ preserves all [[(∞,1)-colimit]]s, but if $f_*$ has a right adjoint, then it does, too, so that for all $S$ we have

$$
  f_* f^* {\lim_\to}_S  * \simeq {\lim_\to}_S f_* f^* *
  \,.
$$

Now $f_*$, being a [[right adjoint]] preserves the [[terminal object in an (∞,1)-category|terminal object]] and so does  $f^*$ by definition of [[(∞,1)-geometric morphism]]. Therefore

$$
  \cdots \simeq {\lim_\to}_S * \simeq S
  \,.
$$


=--



### Concrete objects

Every local $(\infty,1)$-geometric morphism induces a notion of [[concrete (∞,1)-sheaves]]. See there for more (also see [[cohesive (∞,1)-topos]]).



## Examples

### Local over-$(\infty,1)$-toposes


+-- {: .num_prop }
###### Proposition

Let $\mathbf{H}$ be any [[(∞,1)-topos]] (over [[∞Grpd]]) and let $X \in \mathbf{H}$ be an [[object]] that is [[small-projective]]. Then the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is local.

=--

+-- {: .proof}
###### Proof

We check that the [[global section]] [[(∞,1)-geometric morphism]] $\Gamma : \mathbf{H}/X \to $ [[∞Grpd]] preserves [[(∞,1)-colimit]]s. 

The functor $\Gamma$ is given by the [[hom-functor]] out of the [[terminal object]] of $\mathcal{H}/X$, this is $(X \stackrel{Id}{\to} X)$:

$$
  \Gamma : (A \stackrel{f}{\to} X) \mapsto Hom_{\mathbf{H}/X}(Id_X, f)
  \,.
$$

The [[derived hom-space|hom-∞-groupoid]]s in the [[over-(∞,1)-category]] are (as discussed there) [[homotopy fiber]]s of the hom-sapces in $\mathbf{H}$: we have an [[(∞,1)-pullback]] diagram

$$
  \array{
      \mathbf{H}/X(Id_X, (A \to X)) &\to&
       \mathbf{H}(X,A)
      \\
      \downarrow && \downarrow^{f_*}
      \\
      * &\stackrel{Id_X}{\to}& \mathbf{H}(X,X)
  }
  \,.
$$

Overserve that [[(∞,1)-colimit]]s in the [[over-(∞,1)-category]] $\mathbf{H}/X$ are computed in $\mathbf{H}/X$.

$$
  {\lim_{\to}}_i (A_i \stackrel{f_i}{\to} X)
  \simeq
  ({\lim_\to}_i A_i) \to X
  \,.
$$

If $X$ is [[small-projective]] then by definition we have

$$
  \mathbf{H}(X, {{\lim}_\to}_i A_i)
  \simeq
  {\lim_\to}_i \mathbf{H}(X, A_i)
  \,,
$$

Inserting all this into the above $(\infty,1)$-pullback gives the $(\infty,1)$-pullback

$$
  \array{
      \mathbf{H}/X(Id_X, {\lim_\to}_i (A_i \to X)) &\to&
       {\lim_\to}_i \mathbf{H}(X, A_i)
      \\
      \downarrow && \downarrow^{f_*}
      \\
      * &\stackrel{Id_X}{\to}& \mathbf{H}(X,X)
  }
  \,.
$$

By [[universal colimits]] in the [[(∞,1)-topos]] [[∞Grpd]], this [[(∞,1)-pullback]] of an  [[(∞,1)-colimit]] is the $(\infty,1)$-colimit of the separate pullbacks, so that

$$
  \Gamma({\lim_\to}_i (A_i \to X)))
  \simeq
  \mathbf{H}/X(Id_X, {\lim_\to}_i (A_i \to X))
   \simeq
  {\lim_\to}_i \mathbf{H}/X(Id_X,(A_i \to X))
  \simeq
  {\lim_\to}_i \Gamma(A_i \to X)
  \,.
$$

So $\Gamma$ does commute with colimits if $X$ is [[small-projective]]. Since all [[(∞,1)-topos]]es are [[locally presentable (∞,1)-categories]] it follows by the [[adjoint (∞,1)-functor]] that $\Gamma$ has a [[right adjoint|right]] [[adjoint (∞,1)-functor]]. 

=--

### Pyknotic $\infty$-groupoids

The $(\infty,1)$-topos of [[pyknotic infinity-groupoid|pyknotic $\infty$-groupoids]] is a local $(\infty,1)$-topos, according to [Zhu 2023](#Zhu23). 

## Related concpepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / **local (∞,1)-topos**.

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]], [[(∞,1)-cohesive site]]


## References

The 1-categorical notion is discussed in

* [[Peter Johnstone]], [[Ieke Moerdijk]], _Local maps of toposes_  Proc. London Math. Soc.  (1989)   s3-58  (2):  281-305.  ([pdf](http://plms.oxfordjournals.org/content/s3-58/2/281.full.pdf+html))

That pyknotic $\infty$-groupoids (note the author uses "condensed" to mean "pyknotic") form a local $(\infty,1)$-topos:

* {#Zhu23} [[Qi Zhu]], *Fractured Structure on Condensed Anima*, MSc thesis (2023) &lbrack;[pdf](https://1429cecd-24a0-4223-8b7c-1ebf47aa12e2.filesusr.com/ugd/8e912a_fe1c2f8e90094d0fa065fb8129687963.pdf), [[QiZhu-FracturedCondensed.pdf:file]]&rbrack;


[[!redirects local (∞,1)-geometric morphisms]]
[[!redirects local (∞,1)-topos]]
[[!redirects local (∞,1)-toposes]]
[[!redirects local (∞,1)-topoi]]


[[!redirects local (infinity,1)-topos]]
[[!redirects local (infinity,1)-toposes]]
