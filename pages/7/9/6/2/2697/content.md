
<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Definition

An [[(∞,1)-topos]] is **hypercomplete** if the [[Whitehead theorem]] is valid in it.

Equivalently: if all its object are [[hypercomplete object]]s.

Every[[(∞,1)-topos]] has a [[hypercompletion]], the [[reflective sub-(∞,1)-category]] on its [[hypercomplete object]]s.

## Properties

+-- {: .un_lemma}
###### Observation

An $(\infty,1)$-topos that has [[point of a topos|enough points]] is hypercomplete.

=--

This is [[Higher Topos Theory|HTT, remark 6.5.4.7]].

+-- {: .proof}
###### Proof

Recall that a [[point of a topos|point of an (∞,1)-topos]] $\mathbf{H}$ is a [[geometric morphism]]  $p : \infty Grpd \stackrel{\overset{p^*}{\leftarrow}}{\underset{p_*}{\to}} \mathbf{H}$.

And by definition $\mathbf{H}$ has _enough points_ if a morphism $F : X \to Y$ in $\mathbf{H}$ is an [[equivalence in a quasi-category|equivalence]] if for all points $p$, the [[stalk]] $p^* f$ is an equivalence in [[? Grpd]].

But if $f$ is $\infty$-[[connected]] in $\mathbf{H}$, then so is $p^* f$ in [[∞Grpd]], which is hypercomplete, by [[Whitehead's theorem]], so that $p^* f$ is an equivalence.

So in an $(\infty,1)$-topos with enough points all $\infty$-connected morphisms are equivalences.

=--



## Models

### In terms of model category theory

Hypercomplete [[∞-stack]] [[(∞,1)-topos]]es are precisely those that are [[presentable (∞,1)-category|presented]] by the local [[Andre Joyal|Joyal]]-Jardine [[model structure on simplicial presheaves]], where weak equivalences of simplicial presheaves are those morphisms that induce isomorphisms on homotopy sheaves. In these models the fibrant objects are those simplical presheaves that satisfy [[descent]] over all [[hypercover]]s.

If the underlying ordinary [[category of sheaves|sheaf]] [[topos]] has [[point of a topos|enough points]], then this are equivalently the morphisms that induce [[stalk]]wise weak equivalences in the standard [[model structure on simplicial sets]].

Contrary to that one can consider local models by [[Bousfield localization of model categories|left Bousfield localization]] of the global [[model structure on simplicial presheaves]] only at [[Cech cover]]s. This yield in general a non-hypercomplete $(\infty,1)$-topos.

### In classical topos theory

In classical [[topos theory]] literature frequently [[simplicial object]]s in an ordinary [[topos]] are considered, with acyclic fibrations taken to be those morphisms $Y_\bullet \to X_\bullet$ such that for all [[horn]] inclusions the induced morphism

$$
  (X^{\Delta[n]} \to X^{\partial \Delta[n]} \times_{Y^{\partial \Delta[n]}} Y^{\Delta[n]})
$$

is an [[epimorphism]] in the [[topos]]. 

See for instance page 17 of

* [[Ieke Moerdijk]], _Classifying spaces and classifying topoi_ (LNM 1616)

> (and it looks like this is the discussion planned for part E of the [[Elephant]]).


For [[Grothendieck topos|sheaf toposes]] epimorphism means [[stalk]]-wise epimorphism. Therefore this amounts to using on simplicial sheaves the structure of a [[category of fibrant objects]] as defined in [[BrownAHT]], where acyclic fibrations are the stalkwise acyclic [[Kan fibration]]s.

The [[homotopy category]] of this [[homotopical category]] is the same as that of the Joyal-Jardine [[model structure on simplicial presheaves]] in the presence of enough points (since in both cases weak equivalences are the stalkwise weak equivalences), hence is the same as the [[homotopy category of an (infinity,1)-category|homotopy category of the hypercomplete (∞,1)-topos]].

For more discussion of how this classical definition interplays with other definitions see also [[homotopy groups in an (∞,1)-topos]].
 
## References

The notion of hypercompleteness appears as **$t$-completeness** in 

* [[Bertrand Toen]] and [[Gabriele Vezzosi]], _Segal topoi and stacks over Segal categories_ , Proceedings of the
Program Stacks, Intersection theory and Non-abelian Hodge Theory, MSRI, Berkeley, January-May 2002 ([arxiv:math/0212330](http://arxiv.org/abs/math/0212330)).

The notion of hypercomplete $(\infty,1)$-toposes is the topic of  section 6.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects hypercomplete (∞,1)-topos]]
