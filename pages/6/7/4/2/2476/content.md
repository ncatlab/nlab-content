
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[morphism]] $f : X \to Y$ of [[stack]]s over a [[site]] $C$ is called **representable** if for all [[representable functor|representable objects]] $U \in C \stackrel{Y}{\hookrightarrow} Stacks(C)$ and all [[morphism]]s $U \to Y$ the [[homotopy pullback]] $X \times_Y U$ in

$$
  \array{
    X \times_Y U &\to& X
    \\
    \downarrow &{}^{\simeq}\swArrow& \downarrow^f
    \\
    U &\to& Y
  }
$$

is again representable.

## Properties

### Push-forward in generalized cohomology

Along representable morphisms $f$ of stacks over [[smooth manifolds]] ([[smooth infinity-groupoids]]) is induced a [[push-forward in generalized cohomology]] operation.

## Related concepts

* [[representable morphism]].

## References

The general definition appears for instance as def. 38.5 in 

* [[Aise Johan de Jong]],  _[[The Stacks Project]] -- Categories_ ([pdf](http://stacks.math.columbia.edu/download/categories.pdf))

(there with stacks perceived equivalently and dually under the [[Grothendieck construction]] as [[fibered categories]]).

Applications of [[push-forward in generalized cohomology]] along representable morphisms appear for instance in 

* [[Johannes Ebert]], [[Jeffrey Giansiracusa]], _Pontrjagin&#8211;Thom maps and the homology of the moduli stack of stable curves_, Math. Ann. (2011) 349:543&#8211;575 ([arXiv:0712.0702](http://arxiv.org/abs/0712.0702))

[[!redirects representable morphisms of stacks]]
