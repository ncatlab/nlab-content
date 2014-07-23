
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A [[sheaf topos]] $\mathcal{E}$ is called **strongly connected** if it is a [[locally connected topos]]

$$
  (\Pi_0 \dashv \Delta \dashv \Gamma) : \mathcal{E} \stackrel{\overset{\Pi_0}{\longrightarrow}}{\stackrel{\overset{\Delta}{\longleftarrow}}{\underset{\Gamma}{\longrightarrow}}} Set
$$

such that the extra [[left adjoint]] $\Pi_0$ in addition preserves finite [[product]]s (the [[terminal object]] and binary products).

This means it is in particular also a [[connected topos]].

If $\Pi_0$ preserves even all [[finite limit]]s then $\mathcal{E}$ is called a [[totally connected topos]].

If a strongly connected topos is also a [[local topos]], then it is a [[cohesive topos]].

## Terminology
 {#Terminology}

The "strong" in "strongly connected" may be read as referring to $f_! \dashv f^*$ being a [[strong adjoint functor|strong adjunction]] in that we have a [[natural isomorphism]] for the [[internal homs]] in the sense that

$$
  [f_! X, A] \simeq f_* [X, f^* A]  
  \,.
$$

This follows already for $f$ [[connected geometric morphism|connected]] and [[essential geometric morphism|essential]] if $f_!$ preserves products, because this already implies the equivalent [[Frobenius reciprocity]] isomorphism. See [here](http://ncatlab.org/nlab/show/locally%20connected%20geometric%20morphism#StrongAdjunctions) for more.



## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * **strongly connected topos** / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]]



[[!redirects strongly connected toposes]]
[[!redirects strongly connected topoi]]
[[!redirects strongly connected geometric morphism]]

