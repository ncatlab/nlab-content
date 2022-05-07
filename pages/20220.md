
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[M-theory]] [[KK-compactification|compactified]] on 8-dimensional [[compact topological space|compact]] [[fibers]] $X^{(8)}$ (see _[[M-theory on 8-manifolds]]_) [[tadpole cancellation]] for the [[supergravity C-field]] has been argued ([Sethi-Vafa-Witten 96](#SethiVafaWitten96), [Becker-Becker 96](#BeckerBecker96), [Dasgupta-Mukhi 97](#DasguptaMukhi97)) to be the condition

$$
  N_{M2}
  \;+\;
  \tfrac{1}{2} \big( G_4[X^{(8)}]\big)^2
  \;=\;
  \underset{
    I_8(X^8)
  }{
    \underbrace{
      \tfrac{1}{48}\big( p_2 - (\tfrac{1}{2}p_1)^2  \big)[X^{8}]
    }
  }
  \;\;\;\;
  \overset{!}{\in}
  \mathbb{Z}
  \,,
$$

where

1. $N_{M2}$ is the net number of [[M2-branes]] in the spacetime (whose [[worldvolume]] appears as points in $X^{(8)}$);

1. $G_4$ is the [[field strength]]/flux of the [[supergravity C-field]]

1. $p_1$ is the [[first Pontryagin class]] and $p_2$ the [[second Pontryagin class]] combining to [[I8]], all regarded here in [[rational homotopy theory]].

If $X^{8}$ has 

* [[Spin(7)-structure]] (hence in particular if it is a [[Calabi-Yau manifold]], which has $SU(4) = $ [[Spin(6)]]-structure) 

or 

* [[Sp(2).Sp(1)-structure]] 

then

$$
  \tfrac{1}{2}\big( p_2 - \tfrac{1}{4}(p_1)^2  \big)
  \;=\;
  \chi
$$

is the [[Euler class]] (see [this Prop.](Spin7-manifold#CharacteristicClassesForSpinStructure) and [this Prop.](quaternion-Kähler+manifold#CharacteristicClassesForSpin5Spin3Structure), respectively), hence in these cases the condition is equivalently

\[
  \label{DasguptaMukhiConditionInTermsOfEuler}
  N_{M2}
  \;=\;
  -
  \tfrac{1}{2} \big( G_4[X^{(8)}]\big)^2
  \;+\;
  \tfrac{1}{24}\chi[X^8]
  \;\;\;\;
  \in
  \mathbb{Z}
  \,,
\]

where $\chi[X]$ is the [[Euler characteristic]] of $X$.

## Properties

### Integrality on $K3 \times K3$
 {#IntegralityOnK3TimesK3}

That (eq:DasguptaMukhiConditionInTermsOfEuler) should be an [[integer]] is a highly non-trivial condition on the manifold $X^8$.

One case where this is satisfied is for $X^8$ being the [[product space]] of [[K3]] with itself.

To see this, one needs the [[shifted C-field flux quantization]]-condition

\[
  \label{ShiftedCFieldFluxQuantization}
  [\tilde G_4]
  \;\in\;
  H^4(X^8, \mathbb{Z})
  \to
  H^4(X^8, \mathbb{R})
\]

for

\[
  \label{ShiftedCFieldFLux}
  \tilde G_4
  \;\coloneqq\;
  G_4 + \tfrac{1}{4}p_1(\nabla_{T X^8})
\]

+-- {: .num_prop }
###### Proposition

With the [[shifted C-field flux quantization]] (eq:ShiftedCFieldFLux), the Dasgupta-Mukhi-expression (eq:DasguptaMukhiConditionInTermsOfEuler) for the number of [[M2-branes]] is indeed an [[integer]] on the [[product space]] $X^8 = K3 \times K3$ of [[K3]] with itself:

\[
  \tfrac{1}{24}\chi[K3 \times K3]
  -
  \tfrac{1}{2} \big( G_4[K3 \times K3]\big)^2
  \;\in\;
  \mathbb{Z}
  \,,
\]

=--

+-- {: .proof}
###### Proof

After replacing $G_4$ by $\widetilde G_4$ (eq:ShiftedCFieldFLux) the expression becomes

\[
  \label{ExpressingDasgupteMukhInTildeG4}
  \begin{aligned}
    & 
    \tfrac{1}{24}\chi
    -
    \tfrac{1}{2} \big( G_4\big)^2
    \\
    & =
    \tfrac{1}{24}\chi
    -
    \tfrac{1}{2}\big( \tfrac{1}{4} p_1 \big)^2
    -
    \underset{
      \in \mathbb{Z}
    }{
    \underbrace{
      \tfrac{1}{2} 
      \widetilde G_4 \cdot \big( \widetilde G_4 - \tfrac{1}{2}p_1\big)
    }
    }   
    \,,
  \end{aligned}
\]

where the summand over the brace is an integral class (by [this Corollary](Wu+class#DivisibilityOfCupSquare)), because $K3$ is a [[spin manifold]] so that $\tfrac{1}{2}p_1$ is the [[Wu class]] $\nu_4$ (by [this Prop.](Wu+class#InTermsOfPontryagin)).

Hence it is now sufficient to show that the first two summands on the right of (eq:ExpressingDasgupteMukhInTildeG4) are both [[integers]], when evaluated on $K3 \times K3$.

But we have

1. $\chi[K3\times K3] \;=\; 24^2$ (by [this Prop.](K3+surface#EulerCharacteristicOfK3TimesK3))

1. $ p_1[K3 \times K3] \;=\; - 2 \times 48$ (by [this Prop.](K3+surface#FirstPontryaginClassOfK3TimesK3))

Hence 

$$
  \begin{aligned}
    \tfrac{1}{24}\chi[K3 \times K3] 
    & = \tfrac{1}{24} 24^2 
    \\
    & = 24 \;\in\; \mathbb{Z}
  \end{aligned}
$$

and

$$
  \begin{aligned}
    \tfrac{1}{32} (p_1[K3 \times K3])^2
    & = 
    \tfrac{1}{32} \times 
    (
      \underset{
        \mathclap{
          = 3 \times 32
        }
      }
      {
        \underbrace{ 2 \times 48}
      }
    )^2
    \\
    & =
    9 \times 32
    \;\in\;
    \mathbb{Z}
  \end{aligned}
$$

=--



## Related concepts

* [[RR-field tadpole cancellation]] in [[type II string theory]]

* [[shifted C-field flux quantization]] in [[M-theory]]

* [[24 branes transverse to K3]] in [[F-theory]] and [[HET-theory]]


## References
 {#References}


The C-field tadpole cancellation condition is claimed in

* {#SethiVafaWitten96} [[Savdeep Sethi]], [[Cumrun Vafa]], [[Edward Witten]], p. 2 of: _Constraints on Low-Dimensional String Compactifications_, Nucl. Phys. B480:213-224, 1996 ([arXiv:hep-th/9606122](https://arxiv.org/abs/hep-th/9606122))

referring for proof to the computation in

* [[Cumrun Vafa]], [[Edward Witten]], p. 11 (12 of 14) of: _A One-Loop Test Of String Duality_, Nucl. Phys. B480:213-224, 1996 ([arxiv:hep-th/9505053](https://arxiv.org/abs/hep-th/9505053))

A comment is also in

* [[Edward Witten]], p. 3 of _On Flux Quantization In M-Theory And The Effective Action_, J. Geom. Phys. 22:1-13, 1997 ([arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122))

Another condition appears in

* {#BeckerBecker96} [[Katrin Becker]], [[Melanie Becker]], around (2.58) in _M-Theory on Eight-Manifolds_, Nucl. Phys. B477 (1996) 155-167 ([arXiv:hep-th/9605053](https://arxiv.org/abs/hep-th/9605053))

The formulas of [Sethi-Vafa-Witten 96](#SethiVafaWitten96) and [Becker-Becker 96](#BeckerBecker96) have been plugged together in

* {#DasguptaMukhi97} Keshav Dasgupta, [[Sunil Mukhi]], equation (1) in _A Note on Low-Dimensional String Compactifications_, Phys. Lett. B398:285-290, 1997 ([arXiv:hep-th/9612188](https://arxiv.org/abs/hep-th/9612188))

Further discussion:

* [[Sergei Gukov]], [[Cumrun Vafa]], [[Edward Witten]], _CFT's From Calabi-Yau Four-folds_, Nucl. Phys. B584:69-108, 2000; Erratum-ibid.B608:477-478, 2001 ([arXiv:hep-th/9906070](https://arxiv.org/abs/hep-th/9906070))

* Keshav Dasgupta, Govindan Rajesh, [[Savdeep Sethi]], _M Theory, Orientifolds and G-Flux_, JHEP 9908 (1999) 023 ([arXiv:hep-th/9908088](https://arxiv.org/abs/hep-th/9908088))

Lecture notes:

* [[Timo Weigand]], p. 86 of _TASI Lectures on F-theory_ ([arXiv:1806.01854](https://arxiv.org/abs/1806.01854))

Application in [[dualities in string theory]]:

* {#Sethi07} [[Savdeep Sethi]], around (2) in _A Note on Heterotic Dualities via M-theory_, Phys. Lett. B659:385-387, 2008 ([arXiv:0707.0295](https://arxiv.org/abs/0707.0295))

Application in [[string phenomenology]]

* [[Mirjam Cvetic]], [[James Halverson]], Ling Lin, Muyang Liu, Jiahua Tian, equation (9) in _A Quadrillion Standard Models from F-theory_ ([arXiv:1903.00009](https://arxiv.org/abs/1903.00009))

[[!redirects C-field tadpole cancellation condition]]
[[!redirects tadpole cancellation condition for the supergravity C-field]]
