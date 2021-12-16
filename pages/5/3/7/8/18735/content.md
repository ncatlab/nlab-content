

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


A _convolution product_ is the binary operation on [[ring]]-valued (or more generally [[magma]]-valued) [[functions]] $f$ on a [[group]] $G$ or more generally on the set of [[morphisms]] $\mathcal{G}$ of a [[groupoid]], which is given by [[sum|summing]] or more generally [[integration|integrating]] products of values on complementary elements of the schematic form

$$
  (f_1 \star f_2)(g) \;=\; \sum_{h \in G} f_1(h)\cdot f_2( g \cdot h^{-1} ) 
$$

where $h^{-1}$ denotes the [[inverse element]] or more generally the [[inverse morphism]] of $h$.

For example if $G$ is a [[finite group]], then this defines the [[group algebra]], or more generally if $G$ is a suitable [[topological group]] or [[Lie group]] or more generally a suitably [[topological groupoid]] or [[Lie groupoid]], then an [[integral]]-version of this formula defines the _[[groupoid convolution algebra]]_.

Often the convolution product is considered in [[analysis]] for suitably [[integrable functions]] $f \colon \mathbb{R} \to \mathbb{R}$ on the [[real line]] $\mathbb{R}^1$ regarded as a [[group]] with respect to [[addition]] of [[real numbers]]:

$$
  (f_1 \star f_2)(x)
  \;\coloneqq\;
  \int_{t \in\mathbb{R}} f_1(t) f_2(x-t) \, d t
  \,.
$$

This generalizes to a [[convolution product of distributions]].
These convolution products play a central role in [[Fourier analysis]]

A [[categorification]] of the concept of convolution is the concept of _[[Day convolution]]_.

[[!redirects convolution products]]

[[!redirects convolution]]
[[!redirects convolutions]]

category: disambiguation