
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

For $G$ a [[smooth group]], and $A$ an [[abelian group|abelian]] smooth group, a [[central extension]] $\hat G$ of $G$ by $A$ is equivalently a [[homotopy fiber sequence]] of [[smooth groupoid]] [[moduli stacks]] of the form

$$
  \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G \stackrel{c}{\to} \mathbf{B}^2 A
  \,.
$$

Here $c$ is the smooth [[group cohomology]] [[cocycle]] that classifies the extension.

If here we allow the connected [[smooth groupoid]] $\mathbf{B}G$ by any [[smooth groupoid]] $\mathcal{G}_\bullet$, then a homotopy fiber sequence of the form

$$
  \mathbf{B}A \to \widehat {\mathcal{G}} \to \mathcal{G} \stackrel{c}{\to} \mathbf{B}^2 A
$$

exhibits $\widehat \mathcal{G}$ as a central $A$-extension of $\mathcal{G}$. 

Equivalently, such a central extension $\widehat {\mathcal{G}} \to \mathcal{G}$ is a $(\mathbf{B}A)$-[[principal 2-bundle]].

In traditional literature this is mostly considered for [[Lie groupoids]]. Specifically, for $A$ a [[Lie group]] and for $C(\mathcal{U})$ the [[Cech groupoid]] of a [[good open cover]] $\mathcal{U}$ of a [[smooth manifold]] $X$, morphisms of [[smooth stacks]] $X \to \mathbf{B}^2 A$ are equivalently given by actual morphism of Lie groupoids $C(\mathcal{U}) \to \mathbf{B}^2 A$, which are equivalently degree-2 $A$-[[cocycles]] in the [[Cech cohomology]] of $X$. The corresponding incarnation $\widehat \mathcal{G}$ of the $\mathbf{B}A$-principal 2-bundle classified by this is known as the $A$-[[bundle gerbe]] over $C(\mathcal{U})$.

## Properties

### Twisted convolution algebra and twisted K-theory

A central extension of a Lie groupoid induces a [[twisted groupoid convolution algebra]]. The corresponding [[operator K-theory]] is the [[twisted K-theory]] of the [[differentiable stack]] of the base groupoid. See at _[[KK-theory]]_ for more on this.

## Related concepts

* [[central extension]]

* [[infinity-group extension]]

[[!redirects centrally extended groupoids]]

[[!redirects central extension of groupoids]]
[[!redirects central extensions of groupoids]]

[[!redirects centrally extended Lie groupoid]]
[[!redirects centrally extended Lie groupoids]]
