

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Topos theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $f : X \to Y$ a [[morphism]] in a [[category]] $C$ with [[pullback]]s, there is an induced [[functor]]

$$
  f^* : C/Y \to C/X
$$

of [[over-categories]]. This is the _base change_ morphism. If $C$ is a [[topos]], then this refines to an [[essential geometric morphism]]

$$
  (f_! \dashv f^* \dashv f_*) : C/X \to C/Y
  \,.
$$

The [[duality|dual]] concept is [[cobase change]].


## Definition

### Pullback

For $f : X \to Y$ a [[morphism]] in a [[category]] $C$ with [[pullback]]s, there is an induced [[functor]]

$$
  f^* : C/Y \to C/X
$$

of [[over-categories]].  It is on objects given by [[pullback]]/[[fiber product]]

$$
  (p : K \to Y)
  \mapsto
  \left(
  \array{
    X \times_Y K &\to & K
    \\
    {}^{\mathllap{p^*}}\downarrow && \downarrow
    \\
    X &\to& Y 
  }
  \right)
  \,.
$$


### In a fibered category

The concept of base change generalises from this case to other [[fibered category|fibred categories]].


### Base change geometric morphisms 
  {#GeometricMorphism}

+-- {: .num_prop #BaseChangeIsEssentialGeometricMorphism}
###### Proposition


For $\mathbf{H}$ is a [[topos]] (or [[(∞,1)-topos]], etc.) $f : X \to Y$ a [[morphism]] in $\mathbf{H}$, then base change induces an [[essential geometric morphism]] betwen over-toposes/[[over-(∞,1)-topos]]es

$$
  (\sum_f \dashv f^* \dashv \prod_f) : \mathbf{H}/X 
   \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
 \mathbf{H}/Y
$$ 

where $f_!$ is given by postcomposition with $f$ and $f^*$ by [[pullback]] along $f$.

=--

+-- {: .proof}
###### Proof

That we have [[adjoint functor]]s/[[adjoint (∞,1)-functor]]s $(f_! \dashv f^*)$ follows directly from the universal property of the pullback. The fact that $f^*$ has a further [[right adjoint]] is due to the fact that it preserves all small [[colimit]]s/[[(∞,1)-colimit]]s by the fact that in a topos we have [[universal colimits]] and then by the [[adjoint functor theorem]]/[[adjoint (∞,1)-functor theorem]].

=--

+-- {: .num_prop}
###### Proposition

$f^*$ is a [[logical functor]]. Hence $(f^* \dashv f_*)$ is also an [[atomic geometric morphism]].

=--

This appears for instance as ([MacLaneMoerdijk, theorem IV.7.2](#MacLaneMoerdijk)).

+-- {: .proof}
###### Proof

By prop. \ref{BaseChangeIsEssentialGeometricMorphism} $f^*$ is a [[right adjoint]] and hence preserves all [[limit]]s, in particular [[finite limit]]s.

Notice that the [[subobject classifier]] of an [[over topos]] $\mathbf{H}/X$ is $(p_2 : \Omega_{\mathbf{H}} \times X \to X)$. This [[product]] is preserved by the [[pullback]] by which $f^*$ acts, hence $f^*$ preserves the subobject classifier.

To show that $f^*$ is logical it therefore remains to show that it also preserves [[exponential object]]s.  (...)

=--

+-- {: .num_defn}
###### Definition

A (necessarily essential and atomic) geometric morphism of the form $(f^* \dashv \prod_f)$ is called the **base change geometric morphism** along $f$.

The [[right adjoint]] $f_* = \prod_f$ is also called the [[dependent product]] relative to $f$.

The [[left adjoint]] $f_! = \sum_f$ is also called the [[dependent sum]] relative to $f$.

In the case $Y = *$ is the  [[terminal object]], the base change geometric morphism is also called an **[[etale geometric morphism]]**. See there for more details

=--


## Applications

Base change geometric morphisms may be interpreted in terms of [[fiber integration]]. See [[integral transforms on sheaves]] for more on this.

## References

Around Example A.4.1.2 of

* [[Peter Johnstone]],  _[[Sketches of an Elephant]]_ 
 {#Johnstone}

Around theorem IV.7.2 in 

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
  {#MacLaneMoerdijk}

Section 6.3.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

See also 

* A. Carboni, G. Kelly, R. Wood, _A 2-categorical approach to change of base and geometric morphisms I_ ([numdam](http://po-start.com/reyes/wp-content/uploads/2007/01/metrics.pdf))

[[!redirects change of base]]

[[!redirects base change geometric morphism]]
[[!redirects base change geometric morphisms]]
