
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

* [[group cohomology]]

  * [[nonabelian group cohomology]], **groupoid cohomology**

* [[group extension]]

* [[Lie group cohomology]] 

  * [[∞-Lie groupoid cohomology]]

***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

_Groupoid cohomology_ is the [[cohomology]] specifically of ordinary [[groupoids]], more generally that of [[internal groupoid]]s.

Groupoid cohomology generalizes [[group cohomology]], which is the cohomology of [[delooping]] groupoids of groups. Analogously to abelian and [[nonabelian group cohomology]] there is abelian and [[nonabelian groupoid cohomology]].

Under the [[homotopy hypothesis]] theorem, plain (non-internal) groupoid cohomology is the same as the cohomology of [[homotopy n-type|homotopy 1-type]]s. 

A common special case of groupoid cohomology is the cohomology of [[action groupoid]]s: this is (Borel)-[[equivariant cohomology]].

General groupoid cohomology may be regarded as a generalization of equivariant cohomology exactly analogous to the passge from global action groupoids to [[orbifold]]s.

## Details

Let $\mathbf{H} = $ [[∞Grpd]] be the [[(∞,1)-topos]] of [[∞-groupoid]]s. Let $X \in \mathbf{H}$ be an ordinary 1-[[groupoid]]. Let $A \in \mathbf{H}$ be an arbitrary $\infty$-groupoid. Then the cohomology of $X$ with coefficients in $A$ is 

$$ 
  H(X,A) := \pi_0 \mathbf{H}(X,A)
  \,.
$$ 

Concrete formulas for this work exactly as described in detail at [[group cohomology]], only wherever there we have the unique object $\bullet$, now there may be arbitrary objects.

## Examples

* The [[Liouville cocycle]] is a 1-cocycle on the [[action groupoid]] of the action of conformal resclings on the space of [[Riemannian metric]]s on a surface.