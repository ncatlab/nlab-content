+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Wess-Zumino-Witten theory
+--{: .hide}
[[!include infinity-Wess-Zumino-Witten theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **Wess-Zumino-Witten model** (or **WZW model** for short, also called  **Wess-Zumino-Novikov-Witten** model, or short **WZNW** model) is a 2-dimensional [[sigma-model]] [[quantum field theory]] whose target space is a [[Lie group]].

This may be regarded as the boundary theory of [[Chern-Simons theory]] for Lie group $G$.

The [[vertex operator algebra]]s corresponding to the WZW model are [[current algebra]]s.

## Action functional

For $G$ a [[Lie group]], the [[configuration space]] of the WZW over a 2-[[dimension]]al [[manifold]] $\Sigma$ is the space of [[smooth function]]s $g : \Sigma \to G$.

The [[action functional]] of the WZW [[sigma-model]] is the sum of two terms, a kinetic term and a topological term

$$
  S_{WZW} = S_{kin} + S_{top}
  \,.
$$



### Kinetic term

The Lie group canonically carries a [[Riemannian metric]] and the kinetic term is the standard one for [[sigma-model]]s on Riemannian [[target space]]s.


### Topological term -- WZW term

Let $G$ be [[compact space|compact]] and [[simply connected space|simply connected]]. 

Then by [[infinity-Chern-Weil theory]] the [[Killing form]] [[invariant polynomial]] on the [[Lie algebra]] $\mathfrak{g}$ induces a [[circle n-bundle with connection|circle 3-bundle with connection]] on the smooth [[moduli stack]] $\mathbf{B}G_{conn}$ of $G$-[[principal bundle]]s with [[connection on a bundle|connection]]. 

$$
  CS_{\mathbf{c}} : \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}
  \,.
$$

This is the [[Lagrangian]] for $G$-[[Chern-Simons theory]]. By [[loop space object|looping]] this, including a differential twist, there is induced canonically a [[circle n-bundle with connection|circle 2-bundle with connection]] 

$$
  WZW_{\mathbf{c}} : G \to \mathbf{B}^2 U(1)_{conn}
  \,.
$$

The [[higher holonomy|surface holonomy]] of this is the topological part of the WZW action functional:

$$
  \exp(i S_{top}(g))
  = 
  hol_{\Sigma}( g^* WZW_{\mathbf{c}} )
  \,.
$$

## Properties

### Holography

By Chern-Simons [[holography]] (see there for more details) the 2d WZW [[CFT]] on $G$ is related to $G$-[[Chern-Simons theory]] in $3d$.


## References

A useful account of the WZW model that encompasses both its [[action functional]] and [[path integral]] quantization as well as the [[current algebra]] aspects of the QFT is in

* [[Krzysztof Gawedzki]], _Conformal field theory: a case study_ in Y. Nutku, C. Saclioglu, T. Turgut (eds.) _Frontier in Physics_ 102, Perseus Publishing (2000) ([hep-th/9904145](http://xxx.lanl.gov/abs/hep-th/9904145))

This starts in section 2 as a warmup with describing the 1d QFT of a particle propagating on a group manifold. Thee [[Hilbert space]] of [[state]]s is expressed in terms of the [[Lie theory]] of $G$ and its [[Lie algebra]] $\mathfrak{g}$.

In section 4 the quantization of the 2d WZW model is discussed in analogy to that. In lack of a full formalization of the quantization procedure, the author uses the loop algebra $\mathcal{l} \mathfrak{g}$ --  the [[affine algebra]] -- of $\mathfrak{g}$ as the evident analog that replaces $\mathfrak{g}$ and discusses the Hilbert space of states in terms of that. He also indicates how this may be understood as a space of sections of a [[line bundle]] over the loop group.

More detailed textbook introduction can be found in

* P. Di Francesco, P. Mathieu, D. S&#233;n&#233;chal, _Conformal field theory_, Springer 1997

The abstract perspective on the WZW term is discussed in section 2.3.18 and section 4.7 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ .

[[!redirects WZW model]]
[[!redirects WZW-model]]

[[!redirects Wess-Zumino-Witten-model]]

[[!redirects WZW models]]
[[!redirects WZW-models]]

[[!redirects Wess-Zumino-Witten-models]]

[[!redirects Wess-Zumino model]]
[[!redirects Wess-Zumino-model]]

[[!redirects Wess-Zumino models]]
[[!redirects Wess-Zumino-models]]





[[!redirects WZW theory]]
[[!redirects WZW-theory]]
[[!redirects WZNW model]]
[[!redirects WZNW-model]]
[[!redirects WZNW theory]]
[[!redirects WZNW-theory]]

[[!redirects Wess-Zumino-Witten-theory]]

[[!redirects WZW theories]]
[[!redirects WZW-theories]]

[[!redirects Wess-Zumino-Witten-theories]]

[[!redirects Wess-Zumino theory]]
[[!redirects Wess-Zumino-theory]]

[[!redirects Wess-Zumino theories]]
[[!redirects Wess-Zumino-theories]]