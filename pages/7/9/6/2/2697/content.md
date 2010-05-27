
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

+-- {: .un_lemma}
###### Observation

All [[geometric morphism]]s $X \to Y$ out of a hypercomplete $(\infty,1)$-topos $X$ factor through the hypercompletion $\hat Y$ of $Y$:

the inclusion $\hat Y \hookrightarrow Y$ induces an equivalence

$$
  Geom(X,\hat Y) \stackrel{\simeq}{\to}
  Geom(X,Y)
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 6.5.2.13]].




## Models

### In terms of model category theory

Hypercomplete [[∞-stack]] [[(∞,1)-topos]]es are precisely those that are [[presentable (∞,1)-category|presented]] by the local [[Andre Joyal|Joyal]]-Jardine [[model structure on simplicial presheaves]], where weak equivalences of simplicial presheaves are those morphisms that induce isomorphisms on homotopy sheaves. In these models the fibrant objects are those simplical presheaves that satisfy [[descent]] over all [[hypercover]]s.

If the underlying ordinary [[category of sheaves|sheaf]] [[topos]] has [[point of a topos|enough points]], then this are equivalently the morphisms that induce [[stalk]]wise weak equivalences in the standard [[model structure on simplicial sets]].

Contrary to that one can consider local models by [[Bousfield localization of model categories|left Bousfield localization]] of the global [[model structure on simplicial presheaves]] only at [[Cech cover]]s. This yield in general a non-hypercomplete [[(∞,1)-categories of (∞,1)-sheaves]].


+-- {: .un_prop}
###### Proposition

For $C$ [[site]], write $[C^{op}, sSet]_{inj,loc}$ for the Joyal-Jardine [[local model structure on simplicial presheaves]] (whose weak equivalence are morphisms that induce isomorphisms on homotopy-sheaves).

The $(\infty,1)$-topos that this presents is the [[hypercompletion]] of the [[(∞,1)-category of (∞,1)-sheaves]] on $C$:

$$
  ([C^{op}, sSet]_{inj,loc})^\circ
  \simeq
  \widehat{ Sh_{(\infty,1)}(C)}
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 6.5.2.14]].


+-- {: .proof}
###### Proof

As discussed at [[(∞,1)-category of (∞,1)-presheaves]] we have that the global model structure presents the $(\infty,1)$-presheaves:

$$
  ([C^{op}, sSet]_{inj})^\circ \simeq PSh_{(\infty,1)}(C)
  \,.
$$

For $\{U_i \to U\}$ a [[covering]] of an object in $C$, write $S(\{U_i\}) \hookrightarrow j(U)$ for the corresponding [[sieve]]/subfunctor, regarded as a simplicially constant simplicial presheaf.

Observe that 

1. every simplicially constant object is fibrant in $[C^{op}, sSet]_{inj}$ ;

1. hence since every object is cofibrant, the morphism $S(\{U_i\}) \to j(U)$
   is in $([C^{op}, sSet]_{inj})^\circ$;

1. under the abocve identification it is an [[monomorphism in an (∞,1)-category|(∞,1)-monomorphism]] in $PSh_{(\infty,1)}(C)$.

Therefore the [[topological localization]] of $PSh_{(\infty,1)}(C)$ at these monomorphisms, i.e. the [[(∞,1)-category of (∞,1)-sheaves]] on $C$ is presented by the [[Bousfield localization of model categories|left Bousfield localizaiton]] $[C^{op}, sSet]_{inj,cov}$ of $[C^{op}, sSet]_{inj}$ at these covering subfunctors.

Next observe that every [[sieve]] inclusion $S(\{U_i\}) \to j(U)$ induces an isomorphism on homotopy sheaves: all homotopy sheaves in positive degree are trivial anyway, and in degree 0 they are equal, precisely because under (ordinarty) [[sheafification]] the subfunctor $S(\{U_i\})$ becomes isomorphic to $j(U)$). So these subfunctors form a proper subset of the class of weak equivalences of $[C^{op}, sSet]_{inj,loc}$.

Therefore the [[Bousfield localization of model categories|left Bousfield localization]] at isos on homotopy sheaves can be done (if it exists, and we know it exists) in two steps, first localizing at just the covers, then at the isos on homotopy sheaves.

The crucial observation now is that under the above identification, isos on homotopy sheaves in $[C^{op}, sSet]_{inj,loc}$ are precisely identified with the $\infty$-[[connected]] morphisms in $PSh_{(\infty,1)}(C)$. (...details...) 


So in total we obatain the picture

$$
  \array{
    \widehat{Sh_{(\infty,1)}(C)}
    &
     \stackrel{\overset{lex}{\leftarrow}}{\underset{}{\hookrightarrow}}
    &
    Sh_{(\infty,1)}(C)
    &
     \stackrel{\overset{lex}{\leftarrow}}{\underset{}{\hookrightarrow}}
    &
    PSh_{(\infty,1)}(C)
    \\
    \uparrow^{\mathrlap{\simeq}}
    &&
    \uparrow^{\mathrlap{\simeq}}
    &&
    \uparrow^{\mathrlap{\simeq}}
    \\
    ([C^{op}, sSet]_{inj,loc})^\circ
    &
    \stackrel{\overset{\mathbb{L} Id}{\leftarrow}}{\underset{\mathbb{R}Id}{\to}}
    &
    ([C^{op}, sSet]_{inj,cov})^\circ
    &
    \stackrel{\overset{\mathbb{L} Id}{\leftarrow}}{\underset{\mathbb{R}Id}{\to}}
    &
    ([C^{op}, sSet]_{inj})^\circ
  }
  \,.
$$


=--


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
