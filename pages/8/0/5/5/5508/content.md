
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

## Definition

+-- {: .num_defn}
###### Definition

An [[(∞,1)-topos]] $\mathcal{X}$ has **homotopy dimension** $\leq n \in \mathbb{N}$ if every [[n-connected|(n-1)-connected]] [[object]] $A$ has a [[global element]], a [[morphism]]  $* \to A$ from the 
[[terminal object in an (∞,1)-category|terminal object]] into it.

=--

This appears as [[Higher Topos Theory|HTT, def. 7.2.1.1]].


+-- {: .num_defn}
###### Definition

An [[(∞,1)-topos]] $\mathcal{X}$ is **locally of homotopy dimension** $\leq n \in \mathbb{N}$ if there exists a collection $\{U_i \in \mathcal{X}\}$ of [[object]]s such that 

* the $\{U_i\}$ generate $\mathcal{X}$ under [[(∞,1)-colimit]]s;

* each [[over-(∞,1)-topos]] $\mathcal{X}/U_i$ has homotopy dimension $\leq n$.

=--

This appears as [[Higher Topos Theory|HTT, def. 7.2.1.8]].


## Properties

+-- {: .num_prop}
###### Proposition

If an [[(∞,1)-topos]] $\mathcal{X}$ is locally of homotopy dimension $\leq n$ for some $n \in \mathbb{N}$ then it is a [[hypercomplete (∞,1)-topos]].

=--

This appears as [[Higher Topos Theory|HTT, cor. 7.2.1.12]].

+-- {: .num_prop}
###### Proposition

If $\mathcal{X}$ has homotopy dimension $\leq n$ then it also has [[cohomological dimension]] $\leq n$.

The converse holds if $\mathcal{X}$ has finite homotopy dimension and $n \geq 2$. 

=--

This appears as [[Higher Topos Theory|HTT, cor. 7.2.2.30]].


+-- {: .num_prop #RecognitionByGlobalSections}
###### Proposition

An [[(∞,1)-topos]] $\mathcal{X}$ has homotopy dimension $\leq n$ precisely if the [[global section]] [[(∞,1)-geometric morphism]]

$$
  (\Delta \dashv \Gamma) : \mathcal{X} 
    \stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\to}} 
  \infty Grpd
$$

has the property that $\Gamma$ sends $(k\geq n)$-[[n-connective|connective]] morphisms to $(k-n)$-[[n-connective|connective]] morphisms.

=--

This is [[Higher Topos Theory|HTT, lemma 7.2.1.7]]

## Examples

+-- {: .num_prop}
###### Proposition

Up to [[equivalence in an (∞,1)-category|equivalence]], the unique [[(∞,1)-topos]] of homotopy dimension $\leq -1$ is the the [[terminal category]] $ * \simeq Sh_{(\infty,1)}(\emptyset)$. 

=--

This is [[Higher Topos Theory|HTT, example. 7.2.1.2]].

+-- {: .proof}
###### Proof

An object $X \in \mathcal{X}$ is $(-1)$-[[connected]] if the morphism $X \to *$to the [[terminal object in an (∞,1)-category]] is. This is the case if it is an [[effective epimorphism]]. 

Since the [[global section]] [[(∞,1)-functor]] is corepresented by the terminal object, $X$ is 0-connective precisely if $\Gamma(X) \to \Gamma(*) = *$ is an epimorphism on connected components. By the discussion at [[effective epimorphism]], this is the case precisely if $\Gamma(X) \to *$ is an effective epimorphism in [[∞Grpd]].

So $\mathcal{X}$ has homotopy dimension $\leq 0$ if $\Gamma$ preserves effective epimorphisms. This is the case if it preserves [[finite limit|finit]] [[(∞,1)-limit]]s (the [[(∞,1)-pullback]]s defining a [[Cech nerve]]) and all [[(∞,1)-colimit]]s (over the resulting Cech nerve). being a [[right adjoint|right]] [[adjoint (∞,1)-functor]] $\Gamma$ always preserves [[(∞,1)-limit]]s.  If $\mathcal{X}$ is [[local (∞,1)-topos|local]] then $\Gamma$ is by definition also a [[left adjoint]] and hence also preserves [[(∞,1)-colimit]]s.

 
=--


+-- {: .num_prop #LocalToposesHaveHomotopDimension0}
###### Proposition

Every [[local (∞,1)-topos]] has homotopy dimension $\leq 0$.

=--

+-- {: .proof}
###### Proof

Let 

$$
  (\Delta \dashv \Gamma \dashv \nabla)
  : 
  \mathbf{H} \to \infty Grpd
$$

be [[generalized the|the]] [[global section geometric morphism|terminal geometric morphism]] of the local $(\infty,1)$-topos, with $\nabla$ being the extra [[right adjoint]] to the [[global section]] [[(∞,1)-geometric morphism]] functor that characterizes locality. 

By prop \ref{RecognitionByGlobalSections} it is sufficient to show that $\Gamma$ send [[(-1)-connected]] morphisms to (-1)-connected morphisms, hence [[effective epimorphism in an (∞,1)-category|effective epimorphisms]] to effective epimorphisms.

By the existence of $\nabla$ we have that $\Gamma$ preserves not only [[(∞,1)-limit]]s but also [[(∞,1)-colimit]]s. Since effective epimorphisms are defined as certain colimits over diagrams of certain limits, $\Gamma$ preserves effective epimorphisms.

=--

So in particular for $C$ any [[(∞,1)-category]] with a [[terminal object in an (∞,1)-category|terminal object]], the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$ is an [[(∞,1)-topos]] of homotopy dimension $\leq 0$. Notably [[Top]] $\simeq$ [[∞Grpd]] $\simeq PSh_{(\infty,1)}(*)$ has homotopy dimension $\leq 0$.

This is [[Higher Topos Theory|HTT, example. 7.2.1.3]].





+-- {: .num_prop}
###### Proposition

Every [[(∞,1)-category of (∞,1)-presheaves]] is an [[(∞,1)-topos]] of local homotopy dimension $\leq 0$.

=--

This appears as [[Higher Topos Theory|HTT, example. 7.2.1.9]].

+-- {: .num_theorem}
###### Theorem

If a [[paracompact topological space]] $X$ has [[covering dimension]] $\leq n$, then the [[(∞,1)-category of (∞,1)-sheaves]] $Sh_{(\infty,1)}(X) := Sh_{(\infty,11)}(Op(X))$ is an [[(∞,1)-topos]] of homotopy dimension $\leq n$.

=--

This is [[Higher Topos Theory|HTT, theorem 7.2.3.6]].


+-- {: .num_prop}
###### Proposition

For $X \in $ [[∞Grpd]] $\simeq$ [[Top]] an object, the [[over-(∞,1)-topos]] $\infty Grpd/X$ has homotopy dimension $\leq n$ precisely if $X \in Top$ a [[retract]] in the [[homotopy category of an (∞,1)-category|homotopy category]] $Ho(Top)$ of a [[CW-complex]] of [[dimension]] $\leq n$.

=--

This is [[Higher Topos Theory|HTT, example 7.2.1.4]].


## Related concepts

[[!include notions of dimension -- contents]]


## References

The [[(∞,1)-topos theory|(∞,1)-topos theoretic]] notion is discuss in section  7.2.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_