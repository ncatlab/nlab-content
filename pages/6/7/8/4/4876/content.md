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
 {#ActionFunctional}

For $G$ a [[Lie group]], the [[configuration space]] of the WZW over a 2-[[dimension]]al [[manifold]] $\Sigma$ is the space of [[smooth function]]s $g : \Sigma \to G$.

The [[action functional]] of the WZW [[sigma-model]] is the sum of two terms, a kinetic term and a topological term

$$
  S_{WZW} = S_{kin} + S_{top}
  \,.
$$



### Kinetic term
 {#KineticTerm}

The Lie group canonically carries a [[Riemannian metric]] and the kinetic term is the standard one for [[sigma-model]]s on Riemannian [[target space]]s.


### Topological term -- WZW term
 {#TopologicalTerm}

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

The construction of the canonical morphism $WZW_{\mathbf{c}}$ goes as follows. Consider, inside $\mathbf{B}G_{conn}$ the substack $\mathbf{B}G_{\flat dR}$ of _trivialized_ principal $G$-bundles with _flat_ connections. The morphism $CS_{\mathbf{c}}$, restricted to $\mathbf{B}G_{\flat dR}$, factors as 

$$
\mathbf{B}G_{\flat dR}\to \Omega^3(-) \to \mathbf{B}^3 U(1)_{conn}
$$

where $\Omega^3(-)$ is identified with the 3-stack of trivialized circle bundles with connection whose connection form lives entirely in degree 3. Since $\mathbf{B}G_{\flat dR}\to \mathbf{B}G_{conn}$ factors through the stack $\flat\mathbf{B}G$ of principal $G$-bundles with flat conenctions, we have a homotopy commutative diagram

$$
\array{
\mathbf{B}G_{\flat dR}&\to^{CS_{\mathbf{c}}}& \Omega^3(-)\\
\downarrow && \downarrow\\
\flat\mathbf{B}G& \to & \mathbf{B}^3 U(1)_{conn}
}
$$ 

and so a canonically induced morphism $WZW_{\mathbf{c}}$ between the homotopy fibers over the distinguished points. Since we have homotopy pullbacks

$$
\array{
G&\to& \mathbf{B}G_{\flat dR}\\
\downarrow && \downarrow\\
{*}& \to & \flat\mathbf{B}G
}
$$ 

and

$$
\array{
\mathbf{B}^2 U(1)_{conn}&\to & \Omega^3(-)\\
\downarrow && \downarrow\\
{*}& \to & \mathbf{B}^3 U(1)_{conn}
},
$$ 

the morphism $WZW_{\mathbf{c}}$ can naturally be seen as a morphism from $G$ (as a smooth manifold) to the 2-stack $\mathbf{B}^2 U(1)_{conn}$ of [[circle n-bundle with connection|circle 2-bundles with connection]]. In other words, if $G$ is a compact simply connected simple Lie group, the differential refinement $CS_{\mathbf{c}}$ of the degree 4 characteristic class $\mathbf{c}$ provided by Chern-Simons theory naturally induces a  circle 2-bundle with connection over the smooth manifold underlying the Lie group $G$.


The [[higher holonomy|surface holonomy]] of this is the topological part of the WZW action functional:

$$
  \exp(i S_{top}(g))
  = 
  hol_{\Sigma}( g^* WZW_{\mathbf{c}} )
  \,.
$$

## Properties
 {#Properties}

### Holography

By Chern-Simons [[holography]] (see there for more details) the 2d WZW [[CFT]] on $G$ is related to $G$-[[Chern-Simons theory]] in $3d$.

## Related concepts

* [[coset WZW model]]

* [[higher dimensional WZW model]]

* [[Green-Schwarz action functional]]

## References

### General

A useful account of the WZW model that encompasses both its [[action functional]] and [[path integral]] quantization as well as the [[current algebra]] aspects of the QFT is in

* [[Krzysztof Gawedzki]], _Conformal field theory: a case study_ in Y. Nutku, C. Saclioglu, T. Turgut (eds.) _Frontier in Physics_ 102, Perseus Publishing (2000) ([hep-th/9904145](http://xxx.lanl.gov/abs/hep-th/9904145))

This starts in section 2 as a warmup with describing the 1d QFT of a particle propagating on a group manifold. Thee [[Hilbert space]] of [[state]]s is expressed in terms of the [[Lie theory]] of $G$ and its [[Lie algebra]] $\mathfrak{g}$.

In section 4 the quantization of the 2d WZW model is discussed in analogy to that. In lack of a full formalization of the quantization procedure, the author uses the loop algebra $\mathcal{l} \mathfrak{g}$ --  the [[affine algebra]] -- of $\mathfrak{g}$ as the evident analog that replaces $\mathfrak{g}$ and discusses the Hilbert space of states in terms of that. He also indicates how this may be understood as a space of sections of a [[line bundle]] over the loop group.

More detailed textbook introduction can be found in

* P. Di Francesco, P. Mathieu, D. S&#233;n&#233;chal, _Conformal field theory_, Springer 1997

Other references

* L. Feh&#233;r, L. O'Raifeartaigh, P. Ruelle, I. Tsutsui, A. Wipf, _On Hamiltonian reductions of the Wess-Zumino-Novikov-Witten theories_, Phys. Rep. __222__ (1992), no. 1, 64 pp. [MR93i:81225](http://www.ams.org/mathscinet-getitem?mr=1192998), <a href="http://dx.doi.org/10.1016/0370-1573(92)90026-V">doi</a>

### Relation to gerbes and Chern-Simons theory

* [[Alan Carey]], Stuart Johnson, [[Michael Murray]], [[Danny Stevenson]], [[Bai-Ling Wang]], _Bundle gerbes for Chern-Simons and Wess-Zumino-Witten theories_ 	Commun.Math.Phys. 259 (2005) 577-613 ([arXiv:math/0410013](http://arxiv.org/abs/math/0410013))

* [[Konrad Waldorf]], _Multiplicative Bundle Gerbes with Connection_ , 	Differential Geom. Appl. 28(3), 313-340 (2010) ([arXiv:0804.4835](http://arxiv.org/abs/0804.4835))

Section 2.3.18 and section 4.7 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_  ([pdf slides](http://ncatlab.org/schreiber/files/Erlangen2011Schreiber.pdf)).



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

Would someone translate the Topological term for an aging algebraic topologist? B^3U(1) aka K(Z,3) or is it 4? sub conn denotes the classifying space for bundles with connection? The morphism from G to B^2 is strict or up to homotopy?