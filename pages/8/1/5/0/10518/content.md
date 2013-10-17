
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

A ([[schreiber:∞-Wess-Zumino-Witten theory|higher]]) [[WZW model]] is an $n$-dimensional [[sigma-model]] [[field theory]] whose [[target space]] is a [[group]] $G$ and whose [[interaction]]-part of the [[action functional]] is the [[higher holonomy]] of a [[circle n-bundle with connection]] 

$$
  \mathcal{L}_{WZW}
  \;\colon\;
  G \longrightarrow 
  \mathbf{B}^n U(1)_{conn}
$$

(whose [[curvature]] is given by the global [[Maurer-Cartan form]] on $G$).

If one has a $G$-[[principal bundle]] 

$$
  \array{
    G &\hookrightarrow& X
    \\
    && \downarrow
    \\
    && B
  }
$$

over some base space $B$ which admits a [[lift of the structure group]] to the [[Heisenberg n-group]] of $\mathcal{L}_{WZW}$ regarded as a [[prequantum n-bundle]], then the [[fiber]]-wise copies of $G$ and $\mathcal{L}_{WZW}$ glue to a single [[circle n-bundle with connection]] 

$$
  \mathcal{L}_{WZW}^X \;\colon\; X \longrightarrow \mathbf{B}^n U(1)_{conn}
$$

on the total space $X$ of this bundle. This hence yields what one may think of as a coherent collection of [[WZW models]] _parameterized_ over base space $B$.

## Details

Given an ambient [[differential cohesion|differentially]] [[cohesive (∞,1)-topos]] $\mathbf{H}$ and an [[∞-group]] $G \in Grp(\mathbf{H})$, then (the [[interaction]] part of) an $n$-dimensional [[schreiber:∞-Wess-Zumino-Witten theory]] [[sigma-model]] over $G$ is determined ([Fiorenz-Sati-Schreiber 13](#FiorenzaSatiSchreiber13)) by a [[circle n-bundle with connection]] on $G$, hence by a morphism

$$
  \mathcal{L}_{WZW} \;\colon\; G \longrightarrow \mathbf{B}^n U(1)_{conn}
$$

to the [[higher moduli stack]] of [[circle n-bundle with connection]].

This may be regarded equivalently as the [[prequantum n-bundle]] of the higher [[WZW model]]. From this perspective, there is the _[[Heisenberg n-group]]_ $Heis(\mathcal{L}_{WZW})$ which is the group of [[∞-automorphisms]] of $\mathcal{L}_{WZW}$ covering the [[∞-action]] of $G$ on itself, hence the [[cohesive]] [[automorphism ∞-group]]

$$
  Heis(\mathcal{L}_{WZW})
  \hookrightarrow
  \underset{\mathbf{B}^n U(1)_{conn}}{\prod}
  [\mathcal{L}_{WZW},\mathcal{L}_{WZW}]_{/\mathbf{B}^n U(1)_{conn}}^\simeq
$$

of $\mathcal{L}_{WZW}$ regarded as an object of the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}^n ((1)_{conn}}$ (the full [[∞-group]] on the right is the [[quantomorphism n-group]]).

By ([Fiorenza-Rogers-Schreiber 13](#FiorenzaRogersSchreiber13)) this [[∞-group]] is (for connected $\Pi(X)$, without restriction of generality) a $\mathbf{B}^{n-1}U(1)$-[[∞-group extension]] of $G$, and by construction it is precisely such that a lift of a $G$-[[cocycle]] $B \longrightarrow \mathbf{B}G$ modulating a $G$-[[principal ∞-bundle]] $X \to B$ to a $Heis(\mathcal{L}_{WZW})$ cocycle

$$
  \array{
    && \mathbf{B}Heis(\mathcal{L}_{WZW})
    \\
    & \nearrow & \downarrow
    \\
    B &\longrightarrow& \mathbf{B}G
  }
$$

is a single global WZW term 

$$
  \mathcal{L}^X_{WZW} \;\colon\; X \longrightarrow \mathbf{B}^n U(1)_{conn}
$$

which restricts on each [[fiber]] to $\mathcal{L}_{WZW}$.

But the [[Heisenberg n-group]] [[∞-group extension]] is itself classified by an [[∞-group cohomology|∞-group cocycle]] 

$$
  \chi \;\colon\; \mathbf{B}G \longrightarrow \mathbf{B}^n U(1)
$$

and so this is the [[universal characteristic class]] which measures the [[obstruction]] for such a lift to exist.

## Examples

### The heterotic string

The [[heterotic string]] [[worldsheet]] [[theory (physics)|theory]] is a [[sigma model]] on [[spacetime]] $X$ combined with a chiral $G$-[[WZW model]] for $G = Spin \times E_8 \times E_8$ or similar and with the [[WZW term]] being the difference between the differentially twisted [[looping]] of the [[universal Chern-Simons circle 3-bundle|universal Chern-Simons 3-connection]] of $Spin$ with that of $E_8 \times E_8$. 

By ([Fiorenza-Rogers-Schreiber 13, section 2.6.1](#FiorenzaRogersSchreiber13)) we find in this case that the [[Heisenberg 2-group]] is the [[string 2-group]]

$$
  Heis(\mathcal{L}_{WZW^{het}})
  \simeq
  String(G)
  \,.
$$

It follows thus from the above discussion that a consistent heterotic [[sigma model]] requires that the underlying $G$-[[principal bundle]] on [[spacetime]] admits a [[string structure]]. This is the famous [[Green-Schwarz anomaly]] cancellation condition, re-expressed as a consistency condition for parameterized WZW models.

On the level of [[action functionals]] in [[codimension]] 0 this observation is due to ([Distler-Sharpe 10, section 7](#DistlerSharpe10)).


### The Green-Schwarz super $p$-branes on curved super spacetime

By [Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13) the super-[[branes]] of [[string theory]]/[[M-theory]] on [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1;N}$ classified by the [[brane scan]]/[[schreiber:The brane bouquet]] are [[schreiber:∞-Wess-Zumino-Witten theory]] [[sigma-model]]

$$
  \mathcal{L}_{WZW^{brane}}
  \;\colon\;
  \mathbb{R}^{d-1,1;N} \longrightarrow \mathbf{B}^{p+1}(\mathbb{R}/\Gamma)_{conn}
  \,,
$$

where $\Gamma$ is the group of [[periods]] of the defining [[super L-∞ algebra]] [[L-∞ algebra cohomology|L-∞ cocycle]]

$$
  \mathbf{B} sIso_N(d-1,d) \longrightarrow \mathbf{B}^{p+2}(\mathbb{R}/\Gamma)
  \,.
$$

In order to extend this construction from [[super Minkowski spacetime]] to [[supermanifolds]] $X$ that are more general curved solutions to [[supergravity]], we may consider the corresponding parameterized WZW model on each [[tangent space]] 

$$
  T_x X \simeq \mathbb{R}^{d-1,1;N}
$$

separately, using the fact that by [[higher Cartan geometry]] a configuration of [[supergravity]] is encoded in an an $sIso(d-1,1;N)$-[[principal bundle]] and using that the [[super Poincare group]] is a [[semidirect product]]

$$
  sIso_N(d-1,1) \simeq O(d-1,1) \ltimes \mathbb{R}^{d-1,1;N}
$$

of [[super Minkowski spacetime]] (regarded as a [[super translation group]]) with the [[Lorentz group]].

This means that whenever $X$ admits a "higher super-brane structure" in that there is a trivialization of the [[obstruction]]

$$
  X \stackrel{\tau_X}{\longrightarrow} \mathbf{B} sIso(d-1,1;N)
  \stackrel{}{\longrightarrow}
  \mathbf{B}^{p+2}(\mathbb{R}/\Gamma)
$$

then the [[Green-Schwarz action functional]] refined to a [[local prequantum field theory]] datum $\mathcal{L}_{WZW^{brane}}$ globalizes to the [[tangent bundle]] of [[super spacetime]]

$$
  \mathcal{L}_{WZW^{brane}}
  \;\colon\;
  T X
  \longrightarrow 
  \mathbf{B}^{p+1} (\mathbb{R}/\Gamma)_{conn}
  \,.
$$

(For [[branes]] on which other branes may end, such as the [[D-branes]] and the [[M5-brane]], here [[super Minkowski spacetime]] is replaced by a [[extended Minkowski super spacetime]], as discussed in ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13))).

Now in this case where the [[infinity-group]] in question is linear, we have the 0-[[section]]

$$
  \sigma_0 \;\colon\; X \longrightarrow T X
$$

embedding [[super spacetime]] into its [[tangent bundle]]. This allows to pull-back the parameterized WZW model on the [[tangent bundle]] to obtain one on [[spacetime]]

$$
  \mathcal{L}^{X}_{WZW^{brane}}
  \;\colon\;
  X \stackrel{\sigma_0}{\longrightarrow}
  T X
   \stackrel{\mathcal{L}^{T X}_{WZW^{brane}}}{\longrightarrow}
 \mathbf{B}^{p+1}(\mathbb{R}/\Gamma)_{conn}
  \,.
$$

This is now the [[interaction]] term for the correspomnding [[brane]] [[sigma-model]] on the curved [[super spacetime]].

## Related concdepts

* [[gauged WZW model]]

## References

Parameterized WZW models as [[target spaces]] in [[heterotic string theory]] are discussed in section 7 of

* [[Jacques Distler]], [[Eric Sharpe]], _Heterotic compactifications with principal bundles for general groups and general levels_, Adv. Theor. Math. Phys. 14:335-398, 2010 ([arXiv:hep-th/0701244](http://arxiv.org/abs/hep-th/0701244))
  {#DistlerSharpe10}

The corresponding [[elliptic genera]] had been considered in 

* [[Matthew Ando]], _The sigma orientation for analytic circle-equivariant elliptic cohomology_, Geom. Topol. 7 (2003) 91-153 ([arXiv:math/0201092](http://arxiv.org/abs/math/0201092))

The discussion of the relevant [[Heisenberg n-group]] theory is in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_, 2013 ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))
  {#FiorenzaRogersSchreiber13}

General [[schreiber:∞-Wess-Zumino-Witten theory]] is set up in section 6 of

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_, 2013 ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))
  {#FiorenzaSatiSchreiber13}

[[!redirects parameterized WZW models]]
[[!redirects parameterized Wess-Zumino-Witten model]]
[[!redirects parameterized Wess-Zumino-Witten models]]

[[!redirects fibered WZW model]]
[[!redirects fibered WZW models]]
[[!redirects fibered Wess-Zumino-Witten model]]
[[!redirects fibered Wess-Zumino-Witten models]]