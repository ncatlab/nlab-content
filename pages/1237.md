
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Reduced suspension
* table of contents
{: toc}


## Idea

For $(X,x)$ a [[pointed topological space]], then its *reduced suspension* $\Sigma X$ is equivalently the following:

* obtained from the standard [[cylinder]] $I\times X$ ([[product topological space]] with the [[closed interval]] $I = [0,1]$) by identifying the [[subspace]] $(\{0,1\}\times X) \cup (I\times \{x\})$ to a point, i.e. the [[quotient space]] ([this example](quotient+space#QuotientBySubspace))

  $$
     (X \times [0,1])/ ( ( X \times \{0,1\} ) \cup ([0,1] \times \{x\}) )
  $$  

  (Think of crushing the two ends of the cylinder and the line through the base point to a point.) 

* obtained from the plain [[suspension]] 

  $$
    S X = (X \times [0,1])/( X \times \{0,1\})
  $$ 

  of $X$ by passing to the [[quotient space]] which collapses $\{x\} \times I$ to a point ([this example](quotient+space#QuotientBySubspace))

  $$
    \Sigma X \simeq S X / (  \{x\} \times I )
  $$

  For the purposes of [[generalized (Eilenberg-Steenrod) cohomology]] theory typoically it does not matter whether one evaluates on the standard suspension or the reduced suspension. For example for [[topological K-theory]] since $\{x\} \times I$ is a [[contractible topological space|contractible]] [[closed subspace]], then [this prop.](topological+vector+bundle#VectorBundlesOverQuotientByContractibleSubspaceAreEquivalentToVectorBundlesOnTotalSpace) says that [[topological vector bundles]] do not see a difference as long as $X$ is a [[compact Hausdorff space]].



* obtained from the [[reduced cylinder]] by collapsing the two ends, i.e. the [[cofiber]]

  $$
    \Sigma X \simeq cofib(X \vee X \to X \wedge (I_+))
  $$

* the [[mapping cone]] in [[pointed topological spaces]] formed with respect to the [[reduced cylinder]] $X \wedge (I_+)$ of the map $X \to \ast$;

* the [[smash product]] $S^1\wedge X$, of $X$ with the [[circle]] (based at some point) with $X$.

  $$
    \Sigma X \simeq S^1 \wedge X
    \,.
  $$


## Properties

### Relation to suspension

For [[CW-complexes]] $X$ that are also [[pointed topological space|pointed]], with the point identified with a 0-cell, then their reduced suspension is [[weak homotopy equivalence|weakly homotopy equivalent]] to the ordinary suspension: $\Sigma X \simeq S X$.

### Cogroup structure

[[suspensions are H-cogroup objects]]

## Example

### Spheres

Up to [[homeomorphism]], the reduced suspension of the $n$-[[sphere]] is the $(n+1)$-sphere

$$
  \Sigma S^n \simeq S^{n+1}
  \,.
$$

See at _[one-point compactification -- Examples -- Spheres](one-point+compactification#ExamplesSpheres)_ for details.


## Related concepts

* [[loop space object]], [[free loop space object]],

  * [[delooping]]

  * [[loop space]], [[free loop space]], [[derived loop space]]

* [[suspension object]]

  * [[suspension]], **reduced suspension**

    * [[Freudenthal suspension theorem]]

    * [[Spanier-Whitehead category]]

    * [[suspension isomorphism]]

    * [[suspension of a chain complex]]

    * [[Sullivan model of a suspension]]

[[!redirects reduced suspensions]]
