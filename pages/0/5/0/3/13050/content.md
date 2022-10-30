
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
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

On a [[Kähler manifold]] $(X,\omega)$, the _Lefschetz decomposition_ is a decomposition of the [[de Rham cohomology]] into [[differential forms]] which are annihilted by wedge product with some power of the K&#228;hler form $\omega$ times some other power of the 2-form.


## Definition

For $(X,\omega)$ a [[Kähler manifold]] the operation of forming the wedge product with the [[symplectic form]] $\omega \in \Omega^{1,1}(X)$ induces on [[de Rham cohomology]] a function

$$
  L \;\colon\; H^k(X) \longrightarrow H^{k+2}(X)
  \,.
$$

The _[[hard Lefschetz theorem]]_ asserts that if $X$ is [[compact topological space|compact]] with complex [[dimension]] $dim_{\mathbb{C}}(X)= d$, then for all $k \geq 0$ the $k$th power of the $L$-operation induces an [[isomorphism]]

$$
  L^k \;\colon\; H^{d-k}(X) \stackrel{\simeq}{\longrightarrow} H^{d+k}(X)
  \,.
$$

Define the _primitive cohomology_ of $X$ in degree $d-k$ to be the [[kernel]]

$$
  P^{d-k}(X) 
   \coloneqq 
  ker\left(
   H^{d-k}(X) \stackrel{L^{k+1}}{\longrightarrow} H^{d+k+2}(X)
  \right)
  \,.
$$

The [[hard Lefschetz theorem]] then implies the follows [[isomorphism]], which is the **Lefschetz decomposition**

$$
  H^{d}(X,\mathbb{C})
  \simeq
  \underset{k}{\oplus}
  L^k P^{d-2k}(X)
  \,.
$$

## Related concepts

* [[Hodge structure]]

* [[hard Lefschetz theorem]]

## References

* {#Voisin02} [[Claire Voisin]], section 6 of _[[Hodge theory and Complex algebraic geometry]] I,II, Cambridge Stud. in Adv. Math. 76, 77, 2002/3

* _Notes on Lefschetz decomposition_ [pdf](http://www.math.sunysb.edu/~azinger/mat545/LDnotes.pdf)

* MO discussion _[Intuition for primitive cohomology](http://mathoverflow.net/a/14727/381)_
[[!redirects Lefschetz decompositions]]

[[!redirects primitive cohomology]]