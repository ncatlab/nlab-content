
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In ([[perturbative quantum field theory|perturbative]]) [[quantum field theory]] a _hidden sector_ is a subspace of the space of [[field (physics)|fields]] whose only [[interaction]] with the remaining fields is via [[gravity]].

If one interprets the remaining fields as constituting a [[model (physics)|model]] for [[phenomenology]], then in the world this describes the fields in the subspace are literally hidden, they can only bee "seen" via their gravitational pull (or via [[gravitational waves]]).

Hidden sectors as a model for the real world remain hypothetical. They have been postulated notably as a means to explain [[supersymmetry breaking]] (see [below](#SupersymmetryBreaking)). They appear generically in [[perturbative string theory vacua]] (further [below](#InStringTheory)) after [[KK-compactification]].

## Definition

Specifically in [[Lagrangian field theory]] this means that the [[field bundle]] $E \overset{fb}{\to} \Sigma$ over [[spacetime]] $\Sigma$ is a [[fiber product]]

$$
  E \underoverset{\simeq}{(p_1,P_2)}{\longrightarrow} E_{1} \times_\Sigma E_2
$$

such that the [[interaction]] [[Lagrangian density]] $\mathbf{L}_{int}$ is of the form

$$
  \mathbf{L}_{int}
  =
  p_1^\ast \mathbf{L}_{int,1}
  +
  p_2^\ast \mathbf{L}_{int,2}
  + 
  \mathbf{L}_{grav}
$$

where the first two summands are [[pullback of differential forms|pullbacks]] of interactions of the fields in $E_1$ and $E_2$ separately, while the last summand is the interaction term of [[gravity]] coupled to the respective fields jointly.

In this case $E_2$ is a _sector hidden from_ $E_1$, and conversely.

## Examples

### In supersymmetry breaking
 {#SupersymmetryBreaking}

The concept of [[gravity-mediated supersymmetry breaking]] resulted from study of [[gaugino condensation]] in a hidden sector. ([Nilles 01](#Nilles01))


### In string theory
  {#InStringTheory}

In [[string theory]] hidden sectors appear naturally in various ways.

[[Hořava-Witten theory]] at finite interval length gives rise to a copy of [[heterotic supergravity]] at each of the "endpoints", which, as [[gauge theories]], interact with each others only via [[bulk]] gravity. 


In [[model (physics)|models]] of [[M-theory on G2-manifolds]] such as the [[G2-MSSM]], the 4d gauge-field content arises under [[KK-compactification]] from 3-cycles in the [[G2-manifold]] [[fiber bundle|fiber]], and if two such do not intersect, they give rise to hidden sectors in the 4d physics. (e.g. [Kane 17, section 4.4](#Kane17))





## References

Discussion in the context of [[supersymmetry breaking]] is in

* {#Nilles01} [[Hans-Peter Nilles]], _Hidden Sector Supergravity Breakdown_, Nucl. Phys. Proc. Suppl. 101 (2001) 237-250 ([arXiv:hep-ph/0106063](https://arxiv.org/abs/hep-ph/0106063))

Discussion specifically in the context of the [[G2-MSSM]] is in

* {#Kane17} [[Gordon Kane]], section 4.4 of _String theory and the real world_, Morgan & Claypool, 2017 (<a href="http://iopscience.iop.org/book/978-1-6817-4489-6">doi:0.1088/978-1-6817-4489-6</a>)


[[!redirects hidden sectors]]
