

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


### Base change geometric morphisms {#GeometricMorphism}

+-- {: .un_prop}
###### Proposition


For $\mathbf{H}$ is a [[topos]] (or [[(∞,1)-topos]], etc.) $f : X \to Y$ a [[morphism]] in $\mathbf{H}$, then base change induces an [[essential geometric morphism]] betwen over-toposes/[[over-(∞,1)-topos]]es

$$
  (f_! \dashv f^* \dashv f_*) : \mathbf{H}/X 
   \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
 \mathbf{H}/Y
$$ 

where $f_!$ is given by postcomposition with $f$ and $f^*$ by [[pullback]] along $f$.

=--

+-- {: .proof}
###### Proof

That we have [[adjoint functor]]s/[[adjoint (∞,1)-functor]]s $(f_! \dashv f^*)$ follows directly from the universal property of the pullback. The fact that $f^*$ has a further [[right adjoint]] is due to the fact that it preserves all small [[colimit]]s/[[(∞,1)-colimit]]s by the fact that in a topos we have [[universal colimits]] and then by the [[adjoint functor theorem]]/[[adjoint (∞,1)-functor theorem]].

=--

+-- {: .un_def}
###### Definition

In the case $Y = *$ is the  [[terminal object]], the base change geometric morphism is called an **[[etale geometric morphism]]**. See there for more details

=--

## Applications

Base change geoemtric morphisms may be interpreted in terms of [[fiber integration]]. See [[integral transforms on sheaves]] for more on this.

## References

* [[Peter Johnstone]],  _[[Elephant]]_ , Example A.4.1.2


[[!redirects change of base]]

[[!redirects base change geometric morphism]]
