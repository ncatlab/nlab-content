
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _continuum_ is in general something opposite to a [[discrete object|discrete]]. 
There are several notions of continuum in mathematics:

* Often **the continuum** is taken to refer to the [[real line]]; consequently the *cardinality of the continuum* referse to the [[cardinality]] of the [[set]] of [[real numbers]]. There is a related **[[continuum hypothesis]]** in [[set theory]]. 

* A **metric continuum** is any [[compact space|compact]] [[connected space|connected]] [[metric space]]. Often in [[general topology]], a **continuum** is taken to mean a compact [[separation axiom|Hausdorff]] connected space. 

In [[physics]] one may also mean by _a continuum_ a medium which spreads the physical quantities spatially with some finite density, unlike the physics of a system of [[particles]], where an infinite ([[delta-distribution]]-like) density is attached to a discrete system of points. See at _[[geometry of physics]]_ for more on the relation of the continuum in form of the real line to physics.

## In cohesive homotopy type theory
 {#InCohesiveHomotopyTypeTheory}

One can [[axiom|axiomatize]] aspects of the notion of _line continuum_ in [[cohesive homotopy type theory]]. There the idea of an [[object]] $\mathbb{A}^1$ all whose [[generalized element|points]] are, while different, connectable by _[[continuous function|continuous]]_ [[path groupoid|paths]] (and uniquely so, up to suitable [[homotopy]]) is encoded in asking that after applying the [[fundamental infinity-groupoid in a locally infinity-connected (infinity,1)-topos|fundamental ∞-groupoid functor]] $\mathbf{\Pi}$ to it, the result is something [[(-1)-connected|contractible]]

$$
  \mathbf{\Pi}(\mathbb{A}^1) \simeq *
  \,.
$$

+-- {: .num_example #RealLineExhibitsSmoothCohesion}
###### Example

In the [[model]] of [[cohesive homotopy type theory]] called [[Smooth∞Grpd]] we have a [[full and faithful functor|full and faithful]] embedding of [[smooth manifolds]]. Therefore we can embed the [[integers]] $\mathbb{Z}$, the [[rational numbers]] $\mathbb{Q}$ as well as the [[real numbers]] $\mathbb{R}$, all equipped with their canonical [[smooth manifold]] structure. This is [[discrete object|discrete]] for the first two, but not for the last one, and homotopy cohesion can detect this:

$$
  \mathbf{\Pi}(\mathbb{Z}) \simeq \mathbb{Z}
  \,;
$$

$$
  \mathbf{\Pi}(\mathbb{Q}) \simeq \mathbb{Q}
  \,;
$$

but

$$
  \mathbf{\Pi}(\mathbb{R}) \simeq *
  \,.
$$

This reflects the fact that the points of $\mathbb{R}$ form a continuum, but those of $\mathbb{Z}$ and $\mathbb{Q}$ do not.

Also the [[complex numbers]] $\mathbb{C}$ with their canonical manifold structure of course form a continuum in this sense

$$
  \mathbf{\Pi}(\mathbb{C}) \simeq *
  \,.
$$

But the [[real line]] in fact "exhibits the cohesion" (in the sense of [this definition](cohesive+%28infinity%2C1%29-topos#A1ExhibitingCohesion) by [this discussion](cohesive+%28infinity%2C1%29-topos+--+structures#RealLineIsTheContinuum)) in that the [[shape modality]] $\Pi$ is equivalent to [[localization of an (infinity,1)-category|localization]] at $(-) \times \mathbb{R}^1 \longrightarrow (-)$

$$
  \Pi \simeq L_{\mathbb{R}^1}
  \,.
$$

This is not true in smooth cohesion for $\mathbb{R}^1$ replaced by $\mathbb{C}^1$ and in this sense $\mathbb{R}^1$ is "the real continuum" here (in both sense of the word "real").

=--

+-- {: .num_prop #ContractibilityOfAFromThatOfI}
###### Proposition

For a [[ring object]] $\mathbb{A}^1$ to be geometrically contractible, $\Pi(\mathbb{A}^1) \simeq *$, it is sufficient that there be a map $i$ from a [[bi-pointed object]] $(left, right, I)$ to the bipointed object $(0, 1, \mathbb{A}^1)$ such that $I$ is geometrically contractible. 

Hence in words: "If in the ring $\mathbb{A}^1$ the elements 0 and 1 are path-connected, then $\mathbb{A}^1$ is already contractible, hence is a line continuum."

=--

+-- {: .proof}
###### Proof

Under the given assumptions we obtain a [[commuting diagram]] of the form

$$
  \array{
    \mathbb{A}^1
    \\
    \downarrow & \searrow^{\mathrlap{ 0}}
    \\
    I \times \mathbb{A}^1 &\stackrel{ mult\circ (i,id)}{\to}& \mathbb{A}^1
    \\
    \uparrow & \nearrow_{\mathrlap{id}}
    \\
    \mathbb{A}^1
  }
  \,.
$$

Since $\Pi$ preserves products, it sends this to a diagram of the form

$$
  \array{
      & \nearrow \searrow^{\mathrlap{0}}
     \\
    \Pi(\mathbb{A}^1) &\Downarrow_{\simeq}& \Pi(\mathbb{A}^1)
    \\
    & \searrow \nearrow_{\mathrlap{id}}
  }
  \,,
$$

which exhibits a contracting [[homotopy]] of $\Pi(\mathbb{A}^1)$.

=--

+-- {: .num_example}
###### Example

The standard unit intervals $[0,1] \hookrightarrow \mathbb{R} \in $ [[TopMfd]] $\hookrightarrow$ [[ETop∞Grpd]] and $[0,1] \hookrightarrow \mathbb{R} \in $ [[SmthMfd]] $\hookrightarrow$ [[Smooth∞Grpd]]
satisfy the assumptions of prop. \ref{ContractibilityOfAFromThatOfI}.

=--

+-- {: .num_remark}
###### Remark

The $I$ of prop. \ref{ContractibilityOfAFromThatOfI} is in general not an [[interval type]], but only its image $\Pi(I)$ is. See the discussion _[Geometric spaces and their cohesive homotopy types](cohesive%20homotopy%20type%20theory#GeometricSpacesAndTheirHomotopyTypes)_ at _[[cohesive homotopy type theory]]_ for more on this.

=--


## References
 {#References}

* {#Johnstone08} [[Peter Johnstone]], _Topos-theoretic models of the continuum_ 2008 ([slides](http://www.cs.ox.ac.uk/quantum/slides/clap2-peterjohnstone.pdf), [lecture video](https://www.youtube.com/watch?feature=player_embedded&v=pKWYa9sc5UI))


[[!redirects continua]]

[[!redirects metric continuum]]
[[!redirects metric continua]]