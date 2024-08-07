
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #Filtration}
###### Definition

Given a [[category]] $\mathcal{C}$,  then a **filtered object** is an [[object]] $X$ of $\mathcal{C}$ equipped with a _filtration_: 

A **descending filtration** or **decreasing filtrations** of $X$ is a sequence of [[morphisms]] (often required to be [[monomorphisms]]) of the form

  $$
    \cdots
     \longrightarrow
    X_{n+1}
     \longrightarrow
    X_n
     \longrightarrow
    X_{n-1}
      \longrightarrow
    \cdots
      \longrightarrow
    X
  $$


An **ascending filtration** or **increasing filtration** of $X$ is of the form

  $$
    X 
      \longrightarrow
    \cdots
      \longrightarrow
    X_{n-1}
      \longrightarrow
    X_n
      \longrightarrow
    X_{n+1}
      \longrightarrow
    \cdots
  $$

=--

(In more generality, it is also possible to index using any [[ordered group|ordered abelian group]].)

+-- {: .num_defn #ExhaustiveHausdorffAndCompleteFiltrations}
###### Definition

A decreasing filtration $\{X_s\}_s$ of $X$ (def. \ref{Filtration}) is called

* **exhaustive** if $\underset{\longrightarrow}{\lim}_s X_s \simeq X$ ($X$ is the [[colimit]] of the filter stages)

* **Hausdorff** if $\underset{\longleftarrow}{\lim}_s X_s \simeq 0$ (the [[limit]] of the the filter stages is [[initial object|initial]] ([[zero object|zero]] in the case of an [[abelian category]]))

and for a filtration of [[abelian groups]]:

* **complete** if $\underset{\longleftarrow}{\lim}^1_s X_n = 0$ (also the first [[derived functor|derived]] [[limit]] ([[lim^1]]) vanishes)

=--

([Boardman 99, def. 2.1](#Boardman99), see also [Rognes 12, section 2.1](#Rognes12))

+-- {: .num_remark }
###### Remark

Beware that for decreasing filtrations (def. \ref{Filtration}) often exhaustiveness (def. \ref{ExhaustiveHausdorffAndCompleteFiltrations}) is understood by default, and often it is even assumed by default that $X_s = X$ for $s \leq 0$.

=--

## Properties

+-- {: .num_prop #ReconstructingAbelianGroupFromExhaustiveCompleteHausdorffFiltering}
###### Proposition

If a decreasing filtration (def. \ref{Filtration}) of [[abelian groups|abelian]] [[subgroups]]  

$$
  \cdots \hookrightarrow A_{n+1} \hookrightarrow A_n \hookrightarrow A_{n-1} \hookrightarrow \cdots \hookrightarrow A
$$

is exhaustive and complete Hausdorff (def. \ref{ExhaustiveHausdorffAndCompleteFiltrations}) then $A$ may be reobtained from the subquotients of the filtering as the [[limit]]/[[colimit]]

$$
  \begin{aligned}
    A 
      & \simeq
    \underset{\longleftarrow}{\lim}_s (A/A_s)
    \\
    &
      \simeq
    \underset{\longleftarrow}{\lim}_s 
    (\underset{\longrightarrow}{\lim}_t
     ( A_t / A_s ))
  \end{aligned}
  \,.
$$

=--

([Boardman 99, prop. 2.5](#Boardman99))


## Related concepts

[[!include filtered objects -- contents]]

## References

* {#Boardman99} [[Michael Boardman]], section I.2 of _Conditionally convergent spectral sequences_, 1999 ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/boardman-conditionally-1999.pdf))

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner 09](Adams+spectral+sequence#Bruner09)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

* [[Paolo Perrone]], _Starting Category Theory_, World Scientific, 2024, Section 3.2.7. ([website](https://www.worldscientific.com/worldscibooks/10.1142/13670))


[[!redirects filtered objects]]

[[!redirects filtration]]
[[!redirects filtrations]]

[[!redirects filtering]]
[[!redirects filterings]]

[[!redirects exhaustive filtering]]
[[!redirects exhaustive filterings]]

[[!redirects Hausdorff filtering]]
[[!redirects Hausdorff filterings]]

[[!redirects complete filtering]]
[[!redirects complete filterings]]

[[!redirects exhaustive filtration]]
[[!redirects exhaustive filtrations]]

[[!redirects Hausdorff filtration]]
[[!redirects Hausdorff filtrations]]

[[!redirects complete filtration]]
[[!redirects complete filtrations]]

[[!redirects complete Hausdorff filtration]]
[[!redirects complete Hausdorff filtrations]]

