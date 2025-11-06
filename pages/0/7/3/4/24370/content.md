

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


\tableofcontents


## Definition

An *anti-unitary operator* $\Theta$ on a [[Hilbert space]] $\mathscr{H}$ is an [[anti-linear map]] $\mathscr{H} \longrightarrow \mathscr{H}$ which preserves the [[Hermitian inner product|Hermitian]] [[inner product]] $\langle-,-\rangle$ up to [[complex conjugation]]:

$$
  \langle
    \Theta - 
    ,\,
    \Theta -
  \rangle
  =
  \overline{
    \langle
      -
      ,\,
      -
    \rangle
  }
  \,.
$$

This means equivalently, with respect to the Hermitian conjugate $(-)^\dagger$ of anti-linear maps (see [there](antilinear+map#HermitianConjugate)), that an [[anti-linear map]] is anti-unitary iff 

$$
  \Theta^\dagger = \Theta^{-1}
  \,,
$$

which characterization is structurally identical to that of ordinary [[unitary operators]].


## Related concepts

* [[antilinear map]], [[anti-dual linear space]]

* [[time-reversal symmetry]]

* [[Wigner's theorem]]

## References

* {#Uhlmann2016} [[Armin Uhlmann]], around (112) in: *Anti- (Conjugate) Linearity*, Sci. China Phys. Mech. Astron. **59** (2016) 630301  &lbrack;[arXiv:1507.06545](https://arxiv.org/abs/1507.06545), [doi:10.1007/s11433-015-5777-1](https://doi.org/10.1007/s11433-015-5777-1)&rbrack;


See also:

* Wikipedia, *[Antiunitary operator](https://en.wikipedia.org/wiki/Antiunitary_operator)* 

and see the references at *[[Wigner's theorem]]*.

[[!redirects antiunitary operators]]

[[!redirects anti-unitary operator]]
[[!redirects anti-unitary operators]]



