[[!redirects constant coefficients]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

The [[cohomology]] of an [[object]] $X$ in an [[(∞,1)-topos]] $\mathbf{H}$ with coefficients in another object $A$ is the set of connected components of the [[hom-space]] from $X$ to $A$.

Notice that for every [[(∞,1)-sheaf (∞,1)-topos]] there is the terminal [[global section]] [[(∞,1)-geometric morphism]]


$$
 (LConst \dashv \Gamma) : \mathbf{H} 
  \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
 \infty Grpd
  \,.
$$ 


+-- {: .un_defn}
###### Definition

In the case that $A = LConst \mathcal{A}$ for $\mathcal{A} \in $ [[∞Grpd]]  we say that 

$$
  H(X,\mathcal{A}) := \pi_0 \mathbf{H}(X, LConst \mathcal{A})
  \,.
$$

the **cohomology of $X$ with constant coefficients**, constant on $\mathcal{A}$

=--

+-- {: .un_remark}
###### Remark


For $\mathbf{H}$ the [[(∞,1)-sheaf (∞,1)-topos]] over an [[(∞,1)-site]] $C$, we have that $LConst \mathcal{A}$ is the [[constant ∞-stack]] over $C$. Notice that this is the [[∞-stackification]] of the [[(∞,1)-presheaf]] that is literally constant (as an [[(∞,1)-functor]]) on $\mathcal{A}$. So unless over $C$ constant presheaves already satisfy [[descent]] (as for instance over an [[(∞,1)-cohesive site]]) the object $LConst \mathcal{A}$ is not itself given by a constant functor on $C^{op}$.

=--

## Properties

+-- {: .un_lemma}
###### Observation

If $\mathbf{H}$ is a [[locally ∞-connected (∞,1)-topos]] in that we have a further [[left adjoint|left]] [[adjoint (∞,1)-functor]] $\Pi$ to $LConst$

$$
  (\Pi \dashv LConst \dashv \Gamma) : \mathbf{H} \to \infty Grpd
$$

then by the [[adjunction]] hom-equivalence $\mathbf{H}(X, LConst \mathcal{A}) \simeq \infty Grpd(\Pi(X), \mathcal{A})$ we have that cohomology with constant coefficients in $\mathbf{H}$ is equivalently the cohomology of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] $\Pi(X)$ in [[∞Grpd]] with coefficients in $\mathcal{A}$.

A [[cocycle]] 

$$
  (\tilde \nabla : X \to LConst \mathcal{A}) \sim (\nabla : \Pi(X) \to \mathcal{A})
$$

in this cohomology may then be identified with what is called a [[local system]] on $X$ with coefficients in $\mathcal{A}$. So in this case we have

* _Cohomology with constant coefficients classifies local systems._

=--

## Examples

The relation between cohomology with local coefficients cohomology in [[∞Grpd]] $\simeq$ [[Top]] is discussed at [[nonabelian cohomology]] in the section <a href="http://ncatlab.org/nlab/show/nonabelian+cohomology#NonabelianSheafCohomology">nonabelian sheaf cohomology</a>.

