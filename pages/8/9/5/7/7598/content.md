
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $\mathcal{C}$ be a ([[cofibrantly generated model category|cofibrantly generated]]) [[model category]] and let $\mathcal{D}$ be any [[category]], regarded as a [[diagram]]-shape in the following.

Write $[\mathcal{D}, \mathcal{C}]_{proj}$ for the [[projective model structure]] on the [[functor category]] of [[functors]] from $\mathcal{D}$ to $\mathcal{C}$, hence of $\mathcal{D}$-[[diagrams]] in $\mathcal{C}$.

+-- {: .num_defn #ProjectivelyCofibrantDiagram}
###### Definition

A functor/diagram $X : \mathcal{D} \to \mathcal{C}$ is a **projectively cofibrant diagram** in $\mathcal{C}$ if it is a [[cofibrant object]] in the [[projective model structure]] $[\mathcal{D}, \mathcal{C}]_{proj}$.

=--

+-- {: .num_remark}
###### Remark


We unwind the condition in def. \ref{ProjectivelyCofibrantDiagram}.


 First of all it says of course that a [[diagram]] $X \colon \mathcal{D}\to \mathcal{C}$ is projectively cofibrant precisely if the inclusion $\emptyset \to X$ of the [[initial object|initial]] diagram has the [[left lifting property]] with respect to [[natural transformations]] of diagrams

$$
  (A \stackrel{p}{\to} B) : \mathcal{C} \to \mathcal{D}
$$

which are projective acyclic fibrations, hence which are such that for each $c \in \mathcal{C}$ the component $\eta_c : A(c) \to B(c)$ is an acyclic fibration in $\mathcal{C}$.

This in turn means that $F$ is projectively cofibrant precisely if for every diagram of natural transformations

$$
 \array{
  &&A
  \\
  &
  &\downarrow^{\mathrlap{p}}
  \\
  X
  &\to&
  B
}
$$

with $p$ as above, there exists a lift $\sigma$ in 

$$
 \array{
  &&A
  \\
  &
  {}^{\mathllap{\sigma}}\nearrow &\downarrow^{\mathrlap{p}}
  \\
  X
  &\to&
  B
}
 \;\;\;\;\;\;
 \in [\mathcal{D}, \mathcal{C}]
  \,.
$$

making the triangle commute. 

=--

## Properties

The main point of projectively cofibrant diagrams is that the ordinary [[colimit]] over them is a presentation of the [[homotopy colimit]]:

because the ([[colimit]] $\dashv$ constant diagram)-[[adjunction]]

$$
 (\underset{\longrightarrow}{\lim} \dashv const)
  :
  \mathcal{C} \stackrel{\overset{\underset{\longrightarrow}{\lim}}{\leftarrow}}{\underset{const}{\to}}
  [\mathcal{C}, \mathcal{D}]
$$

is a [[Quillen adjunction]] (because $const$ is by the very definition of the [[projective model structure]] a [[right Quillen functor]]), the [[homotopy colimit]], being the left [[derived functor]] $\mathbb{L}\underset{\longrightarrow}{\lim}$ of the [[colimit]], is computed as the ordinary colimit evaluated on a cofibrant resolution $Q X$ of a diagram $X : \mathcal{D} \to \mathcal{C}$:

$$
  (\mathbb{L} \underset{\longrightarrow}{\lim})(X)
  \simeq
  \underset{\longrightarrow}{\lim})(Q X)
  \,.
$$

## Examples

### For specific diagram shapes

+-- {: .num_example}
###### Example

A _[[span]]_ diagram $X_1 \leftarrow X_0 \to X_2$ is projectively cofibrant precisely if the two morphisms are cofibrations in $\mathcal{D}$ and $X_0$, hence all three objects, are cofibrant.

The colimit over such a diagram is the [[homotopy pushout]] of the span.


=--



+-- {: .num_example #CofibrantCotowerDiagram}
###### Example

A _cotower_ diagram

$$
  X_0 \to X_1 \to X_2 \to \cdots
$$

is projectively cofibrant precisely if every morphism is a cofibration and if the first object $X_0$, and hence all objects, are cofibrant in $\mathcal{D}$.

The colimit over such a diagram is a homotopy [[sequential colimit]].

=--

+-- {: .num_example}
###### Example

A _[[parallel morphisms]]_ diagram

$$
  X_0 \stackrel{\overset{f}{\to}}{\underset{g}{\to}} X_1
$$

is projectively cofibrant precisely if $X_0$ is cofibrant, and if the morphism
$(f,g) : X_0 \coprod X_0 \to X_1$ is a cofibration.

This implies that also $f$ and $g$ are cofibrations and hence that $X_1$ is cofibrant. 

=--

The colimit over such a diagram is a homotopy [[coequalizer]].

### For specific ambient model categories

Let $\mathcal{C} = $ [[sSet]]${}_{Quillen}$ be the standard [[model structure on simplicial sets]]. Then $[\mathcal{D}, \mathcal{C}]_{proj}$ is the projective [[model structure on simplicial presheaves]]. 

For the following see at _[[model structure on simplicial presheaves]]_ the section _[Cofibrant objects](model+structure%20on%20simplicial%20presheaves#CofibrantObjects)_ for more details (due to [[Dan Dugger]], see also [Richard Garner's answer on
MathOverflow](https://mathoverflow.net/questions/97690/necessary-conditions-for-cofibrancy-in-global-projective-model-structure-on-simp/127187#127187)).


+-- {: .num_prop}
###### Proposition

A necessary and sufficient condition for a diagram $X : \mathcal{D} \to sSet$ to be projectively cofibrant is:

1. $X$ is degreewise a coproduct of [[retracts]] of [[representable functor|representables]]
   $$
    X_n = \coprod_{i} U^n_i \;\;\;\;  \{U^n_i \in \mathcal{C} \hookrightarrow [\mathcal{C}, Set]\}
   $$

1. Each simplicial level, as a presheaf of sets, can be presented as the [[coproduct]] of two presheaves of sets, one of which is the presheaf of degenerate simplices:
   $$
      X_n = NonDegenerate_n \coprod Degenerate_n
      \,.
   $$

=--

+-- {: .num_example}
###### Example

A _[[split hypercover]]_ is of this form.

=--

+-- {: .num_prop}
###### Proposition

For $X : \mathcal{D} \to sSet$ any simplicial presheaf, a cofibrant [[resolution]] is given by
$$
  (Q X)_n : \coprod_{U_0 \to \cdots \to U_n \to X_n} U_0
  \,, 
$$
where the coproduct runs over all sequences of morphisms between representables $U_i$, as indicated.

=--

## References

See the references at _[[homotopy colimit]]_ and generally at _[[model category]]_.

Related discussion is at

* MathOverflow _[When are "diagrams of cofibrations" projectively cofibrant](http://mathoverflow.net/questions/70612/when-are-diagrams-of-cofibrations-projectively-cofibrant)_

Related discussion is for instance also in

*  Urs Schreiber, _[[schreiber:differential cohomology in a cohesive topos]]_

where cofibrant cotowers are mentioned as example 2.3.15.

[[!redirects projectively cofibrant diagrams]]