
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A _sifted colimit_ is a [[colimit]] of a [[diagram]] $D \to C$ where $D$ is a [[sifted category]] (in analogy with a [[filtered colimit]], involving diagrams of shape a [[filtered category]]). Such colimits [[limits commuting with colimits|commute]] with finite [[products]] in [[Set]], by definition.

## Examples

+-- {: .num_example}
###### Example

A motivating example is a [[reflexive coequalizer]]. In fact, sifted colimits can "almost" be characterized as combinations of [[filtered colimits]] and reflexive coequalizers. ([Adamek-Rosicky-Vitale 10](#AdamekRosickyVitale10))

=--

+-- {: .num_example #CategoriesWithFiniteProductsAreCosifted}
###### Example
**([[categories with finite products are cosifted]]**

Let $\mathcal{C}$ be a [[small category]] which has [[finite products]]. Then $\mathcal{C}$ is a _[[cosifted category]]_, equivalently its [[opposite category]] $\mathcal{C}^{op}$ is a _[[sifted category]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] are _[[sifted colimits]]_, equivalently [[colimits]] over $\mathcal{C}^{op}$ with values in [[Set]] _[[limits commuting with colimits|commute]] with [[finite products]]_, as follows:

For $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ to [[functors]] on the [[opposite category]] of $\mathcal{C}$ (hence two [[presheaves]] on $\mathcal{C}$) we have a [[natural isomorphism]]

$$
  \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
  \left(
    \mathbf{X} \times \mathbf{Y}
  \right)
  \;\simeq\;
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{X}
  \right)
  \times
  \left(
    \underset{\underset{\mathcal{C}^{op}}{\longrightarrow}}{\lim}
    \mathbf{Y}
  \right)
  \,.
$$ 

=--


## Properties

See at _[[distributivity of products and colimits]]_.


## See also

* [[sifted (infinity,1)-colimit|sifted $(\infty,1)$-colimit]]

* [[finite product]]

## References

* {#GabrielUlmer71} [[Pierre Gabriel]], [[Friedrich Ulmer]], _Lokal pr&#228;sentierbare Kategorien_, Springer LNM
221, Springer-Verlag 1971

*  {#AdamekRosickyVitale10} [[Jiri Adamek]], [[Jiri Rosicky]], [[Enrico Vitale]], _What are sifted colimits?_, TAC **23** (2010) pp. 251&#8211;260. ([web](http://www.tac.mta.ca/tac/volumes/23/13/23-13abs.html)) 


[[!redirects sifted colimit]]
[[!redirects sifted colimits]]