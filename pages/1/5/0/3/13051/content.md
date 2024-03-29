
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

For $(X,\omega)$ a [[Kähler manifold]] the operation of forming the wedge product with the [[symplectic form]] $\omega \in \Omega^{1,1}(X)$ induces on [[de Rham cohomology]] the _Lefschetz operator_

$$
  L \;\colon\; H^k(X) \longrightarrow H^{k+2}(X)
  \,.
$$

The **hard Lefschetz theorem** asserts that if $X$ is [[compact topological space|compact]] with complex [[dimension]] $dim_{\mathbb{C}}(X)= d$, then for all $k \geq 0$ the $k$th power of the $L$-operation induces an [[isomorphism]]

$$
  L^k \;\colon\; H^{d-k}(X) \stackrel{\simeq}{\longrightarrow} H^{d+k}(X)
  \,.
$$

Using that $\omega$ is a $(1,1)$-form this means equivalently in terms of [[Dolbeault cohomology]] that for all $(p+q) \leq d$ we have an isomorphism

$$
  L^{d-(p+q)}
  \;\colon\;
  H^{p,q}(X) \stackrel{\simeq}{\longrightarrow} H^{d-q,d-p}(X)
  \,.
$$

This exhibits the symmetry of the [[Hodge diamond]] under reflection about the horizontal diagonal.

The hard Lefschetz theorem induces the _[[Lefschetz decomposition]]_ (see there) of the de Rham cohomology of $X$.

The hard Leftschetz theorem also applies to other objects, for instance, to [[matroids]] (see [Huh 22](#Huh22)).

## References

* {#Voisin02} [[Claire Voisin]], section 6 of _[[Hodge theory and Complex algebraic geometry]] I,II, Cambridge Stud. in Adv. Math. 76, 77, 2002/3

* _Notes on Lefschetz decomposition_ [pdf](http://www.math.sunysb.edu/~azinger/mat545/LDnotes.pdf)


* MO discussion _[Intuition for primitive cohomology](http://mathoverflow.net/a/14727/381)_
[[!redirects Lefschetz decompositions]]

In the generality of [[matroids]]:

* {#Huh22} [[June Huh]], _Combinatorics and Hodge theory_, Proc. Int. Cong. Math. **1** (2022)
 &lbrack;[doi:10.4171/ICM2022/205](), [pdf](https://www.mathunion.org/fileadmin/IMU/Prizes/Fields/2022/jh.pdf), [[Huh-CombinatoricsAndHodgeTheory.pdf:file]]&rbrack;

[[!redirects Lefschetz operator]]
[[!redirects Lefschetz operators]]
