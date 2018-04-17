
$\,$

$\,$

## Checking spinor conventions for $Pin$-Reps

We check what it takes to get a [[Pin group]]-representation when using the spinor conventions from [[Supergravity and Superstrings - A Geometric Perspective|CDF, II.7.1]].

We need the following facts:

(Numbered pointers in the following are to _[[geometry of physics -- supersymmetry]]_, which, in the relevant spots, is just recalling [[Supergravity and Superstrings - A Geometric Perspective|CDF]].)

**Dirac representation.** From [Prop. 2.18](geometry+of+physics+--+supersymmetry#CliffordAlgebraRepresentation) we have

\[
  \label{GammaHermiticity}
  \Gamma_0^\dagger = + \Gamma_0
  \phantom{AAAA}
  \Gamma_{a}^\dagger = - \Gamma_{a}
  \phantom{AAA}
  \text{for} \; a \; \text{spatial}
\]

**Charge conjugation matrix.** From [Prop. 2.22](geometry+of+physics+--+supersymmetry#ChargeConjugationMatrices) and [Remark 2.23](geometry+of+physics+--+supersymmetry#TransposeChargeConjugation) we get for $d = 11$ (see the table there) that the charge conjugation matrix satisfies

\[
  \label{ChargeConjugation}
  \Gamma_a^T C = - C \Gamma_a
\]

**Majorana condition.** From [Prop. 2.29](geometry+of+physics+--+supersymmetry#TheMajoranaConditionInComponents) we have that the Majroana condition on $\psi$ is equivalent to

\[
  \label{MajoranaCondition}
  C \Gamma_a = - \Gamma_a^T C
\]

+-- {: .num_prop }
###### Claim

In the above conventions, multiplication by $\Gamma_{a}$ does not preserves the Majorana condition. But multiplication by $i \Gamma_{a}$ does.

=--

+-- {: .proof}
###### Proof

First assume that the index is spatial. Suppose $\psi$ is Majorana, then we compute as follows:

$$
  \begin{aligned}
    (\Gamma_a \psi)^T C
    & =
    \psi^T \Gamma_a^T C
    \\
    & = 
    - \psi^T C \Gamma_a
    \\
    & =
    -  \psi^\dagger \Gamma_0 \Gamma_a
    \\
    & =
    +  \psi^\dagger \Gamma_a \Gamma_0 
    \\
    & =
    -  \psi^\dagger \Gamma_a^\dagger \Gamma_0 
    \\
    & =  
    - (\Gamma_a \psi)^\dagger \Gamma_0  
  \end{aligned}
$$

Here

* the first equality is that transposition is an algbra anti-homomorphism,

* the second equality is the charge conjugation relation (eq:ChargeConjugation),

* the third equality is the Majorana condition (eq:MajoranaCondition) on $\psi$,

* the fourth equality is the Clifford relation $\{\Gamma_0,\Gamma_{a}\} = 0$,

* the fifth equality is the anti-hermiticity (eq:GammaHermiticity),

* the sixth equality is that $\dagger$ is algebra anti-homomorphism.

In conclusion, the overall minus sign between the first and the last term means that $\Gamma_{a} \psi$ fails the Majorana condition (eq:MajoranaCondition).

But with $i \Gamma_{a}$ instead of $\Gamma_{a}$, the same computation applies, except that there is one extra sign when $\dagger$ is applied, from $i^\dagger = i^\ast = -i$. Hence this fixes the sign.

Finally, in the case that $a = 0$ the same computation goes through once more, except for _two_ extra signs: One from the difference of sign under $\dagger$ from (eq:GammaHermiticity), the other due to the difference of sign in commuting through $\Gamma_0$. Hence the conclusion remains the same.

=--
