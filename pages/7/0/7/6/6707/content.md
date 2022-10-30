
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

### Topological

For $n \in \mathbb{N}$ the [[Lie group]] $Spin^c(n)$ is a [[central extension]] 

$$
  U(1) \to Spin^c(n) \to SO(n)
$$

of the [[special orthogonal group]] by the [[circle group]]. This comes with a long [[fiber sequence]]

$$
  \cdots \to B U(1) \to B Spin^c(n)  \to B SO(n) \stackrel{W_3}{\to} B^2 U(1)
  \,,
$$

where $W_3$ is the _third integral [[Stiefel-Whitney class]]_ . 

By the definition at [[twisted cohomology]], for a given class $[c] \in H^3(X, \mathb{Z})$, a **$c$-twisted $spin^c$-structure** is a choice of [[homotopy]]

$$
  \eta : c \stackrel{\simeq}{\to} W_3(T X)
  \,.
$$

The [[space]]/[[∞-groupoid]] of all twisted $Spin^c$-structures on $X$ is the [[homotopy fiber]] $W_3 Struc_{tw}(T X)$ in the [[pasting diagram]] of [[homotopy pullback]]s

$$
  \array{
    W_3 Struc_{tw}(T X) &\to& W_3 Struc_{tw}(X) &\stackrel{tw}{\to}& H^3(X, \mathbb{Z})
    \\
    \downarrow && \downarrow && \downarrow 
    \\
    * &\stackrel{T X}{\to}& Top(X, B SO(n)) 
    &\stackrel{W_3}{\to}&
    Top(X, B^2 U(1))
  }
  \,,
$$

where the right vertical morphism is the canonical [[effective epimorphism]] that picks one point in each connected component.

### Smooth

Since $U(1) \to Spin^c \to SO$ is a sequence of [[Lie group]]s, the above may be lifted from the [[(∞,1)-topos]] [[Top]] $\simeq$ [[∞Grpd]] to [[Smooth∞Grpd]].

More precisely, by the discussion at [[Lie group cohomology]] (and [[smooth ∞-groupoid -- structures]]) the characteristic map $W_3 : B SO \to B^2 U(1)$ in $\infty Grpd$ has, up to equivalence, a unique lift

$$
  \mathbf{W}_3 : \mathbf{B} SO \to \mathbf{B}^2 U(1)
$$

to [[Smooth∞Grpd]], where on the right we have the [[delooping]] of the smooth [[circle n-group|circle 2-group]]. 

By the general definition at _[[twisted differential c-structure]]_ , the [[2-groupoid]] of _smooth twisted $spin^c$-structures_ $\mathbf{W}_3 Struc_{tw}(X)$ is the joint [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{W}_3 Struc_{tw}(T X) &\to& \mathbf{W}_3 Struc_{tw}(X) &\stackrel{tw}{\to}& H_{smooth}^2(X, U(1))
    \\
    \downarrow && \downarrow && \downarrow 
    \\
    * &\stackrel{T X}{\to}& Smooth \infty Grpd(X, \mathbf{B} SO(n)) 
    &\stackrel{\mathbf{W}_3}{\to}&
    Smooth \infty Grpd(X, \mathbf{B}^2 U(1)
  }
  \,.
$$

## Applications

### Anomaly cancellation in physics

The existence of an ordinary [[spin structure]] on a space $X$ is, as discussed there, the condition for $X$ to serve as the [[target space]] for the [[spinning particle]] [[sigma-model]], in that the existence of this structure is precisely the condition that the corresponding fermionic [[quantum anomaly]] on the [[worldline]] vanishes.

Twisted $spin^c$-structures appear similarly as the conditions for the analogous quantum anomaly cancellation, but now of the open [[type II superstring]] ending on a [[D-brane]]. This is also called the **Freed-Witten anomaly cancellation**. 

More precisely, in these applications the class of $W_3(TX) - H$ need not vanish, it only needs to be $n$-[[torsion]] if there is moreover a [[twisted bundle]] of rank $n$ on the $D$-brane.

See the [references below](ReferencesAnomalyCancellation) for details.

## Related concepts

* [[twisted differential c-structure|(twisted differential) c-structures]]

  * [[orientation]]

  * [[spin structure]], [[twisted spin structure]]

    [[spin^c structure]], **twisted $spin^c$ structure**

  * [[string structure]], [[differential string structure]]

  * [[fivebrane structure]], [[differential fivebrane structure]]


## References

### General

The notion of twisted $Spin^c$-structures as such were apparently first discussed in section 5 of 

* [[Christopher Douglas]], _On the Twisted K-Homology of Simple Lie Groups_ ([arXiv:0402082](http://arxiv.org/abs/math/0402082))

More discussion appears in section 3 of

* [[Bai-Ling Wang]], _Geometric cycles, index theory and twisted K-homology_ ([arXiv:0710.1625](http://arxiv.org/abs/0710.1625)) 

The refinement to smooth twisted structures is discussed in section 4.1 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

### In physics
 {#ReferencesAnomalyCancellation}

The need for twisted $Spin^c$-structures as [[quantum anomaly]]-cancellaton condition on the [[worldvolume]] of [[D-brane]]s in [[string theory]] was first discussed in

* [[Daniel Freed]], [[Edward Witten]], _Anomalies in String Theory with D-Branes_ ([arXiv:hep-th/9907189](http://arxiv.org/abs/hep-th/9907189))

More details are in 

* [[Anton Kapustin]], _D-branes in a topologically nontrivial B-field_ , Adv. Theor. Math. Phys.
4, no. 1, pp. 127&#8211;154 (2000), ([arXiv:hep-th/9909089](http://arxiv.org/abs/hep-th/9909089))

A clean review is provided in

* Kim Laine, _Geometric and topological aspects of Type IIB D-branes_ ([arXiv:0912.0460](http://arxiv.org/abs/0912.0460))

[[!redirects twisted spin^c structures]]

[[!redirects twisted spin^c-structure]]
[[!redirects twisted spin^c-structures]]


[[!redirects Freed-Witten anomaly]]
[[!redirects Freed-Witten anomaly cancellation]]