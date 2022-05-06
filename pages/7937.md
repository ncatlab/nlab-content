

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the contect of [[geometric quantization]] a _prequantum operator_ is a [[linear operator]] is a canonical [[action]] of a [[Hamiltonian]] [[observable]] on the [[space of sections]] of the [[prequantum line bundle]]. After a choice of [[polarization]], if this restricts to the subspace of polarized sections, hence to the actual [[space of states (in geometric quantization)|space of quantum states]] ("[[wavefunctions]]") then this is the operator that [[representation|represents]] the given [[observable]].

More in detail, the [[quantomorphism group]] $\mathbf{Aut}(\mathbf{c}_{conn})$ naturally acts on the [[space of sections]] $\mathbf{\Gamma}_X(E)$ of the [[prequantum line bundle]]. 

$$
  \widehat {(-)} : \mathbf{\Gamma}_X(E) \times \mathbf{Aut}(\mathbf{c}_{conn}) \to \mathbf{\Gamma}_X(E)
  \,.
$$

For $O \in \mathbf{Aut}(\mathbf{c}_{conn})$ a given [[Hamiltonian symplectomorphism]] with [[Hamiltonian]], the corresponding map

$$
  \widehat{O} : \mathbf{\Gamma}_X(E) \to \mathbf{\Gamma}_X(E)
$$

is the _prequantum operator that quantizes $O$_.

Given a choice of [[polarization]] the actual _quantum operator_ corresponding to this is the restriction, if it exists, to the sub-space of polarized sections.

Typically this is considered for [[infinitesimal]] elements of the [[quantomorphism group]], hence for elements of the [[Poisson bracket Lie algebra]] (which then typically end up as [[unbounded operators]]), see def. \ref{PrequantumOperator} below.

## Definition

### For ordinary phase spaces

Let $(X,\omega)$ be a [[presymplectic manifold]].

Let $\nabla : X \to \mathbf{B} U(1)_{conn}$ be a
[[prequantum line bundle]] $E \to X$ [[connection on a bundle|with connection]] for $\omega$. Write $\Gamma_X(E)$ for its space of smooth [[sections]], the _[[prequantum space of states]]_.




+-- {: .num_defn #PrequantumOperator}
###### Definition
**([[prequantum operators]])**

For $f \in C^\infty(X, \mathbb{C})$ a function on phase space, the corresponding **[[quantum operator (in geometric quantization)|quantum operator]]** is the linear map

$$
  \hat f \colon \Gamma_X(E) \to \Gamma_X(E)
$$

given by

$$
  \label{FormulaForPrequantumOperator}
  \psi \mapsto -i \nabla_{v_f} \psi + f \cdot \psi
  \,,
$$

where 

* $v_f$ is the [[Hamiltonian vector field]]
corresponding to $f$;

* $\nabla_{v_f} : \Gamma_X(E) \to \Gamma_X(E)$ is the [[covariant derivative]] of sections along $v_f$ for the given choice of prequantum connection;

* $f \cdot (-) : \Gamma_X(E) \to \Gamma_X(E)$ is the operation of degreewise multiplication pf sections.

=--

+-- {: .num_remark #OriginOfTheFormulaForPrequantumOperators}
###### Remark
**(origin of the formulas for [[prequantum operators]])*+

The formula (eq:FormulaForPrequantumOperator) may look a bit mysterious on first sight. The correction term to the [[covariant derivative]] appearing in this formula is ultimately due to the fact that with $v$ the [[Hamiltonian vector field]] corresponding to a [[Hamiltonian]] $H_v$ via

$$
  \iota_v \omega = d H_v
$$

then the [[Lie derivative]] of $\theta$ (the symplectic potentiation, related by $d \theta = \omega$) is

$$
  \mathcal{L}_v \theta = d \tilde H_v
$$

for 

$$
  \tilde H_v = H_v + \iota_v \theta
  \,.
$$

Here the second term on the right is what yields the [[covariant derivative]] in (eq:FormulaForPrequantumOperator), while the first summand is the correction term in (eq:FormulaForPrequantumOperator).

A derivation of these formulas from first principles is given in ([Fiorenza-Rogers-Schreiber 13a](#FiorenzaRogersSchreiber13a), example 3.2.3 and remark 3.3.16).

=--

## Related concepts

[[!include states and observables -- content]]



## References


* {#FiorenzaRogersSchreiber13a} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]],  _[[schreiber:Higher geometric prequantum theory|Higher U(1)-gerbe connections in geometric prequantization]]_, Reviews in Mathematical Physics, Volume 28, Issue 06, July 2016 ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))

* {#FiorenzaRogersSchreiber13b} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]]  _[[schreiber:L-∞ algebras of local observables from higher prequantum bundles]]_, Homology, Homotopy and Applications, Volume 16 (2014) Number 2, p. 107  142 ([arXiv:1304.6292](http://arxiv.org/abs/1304.6292))


[[!redirects prequantum operators]]

[[!redirects prequantum operator]]
