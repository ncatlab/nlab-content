
## abc


+-- {: .num_remark #AmbiguityInCliffordConjugation}
###### Remark

Since the [[reflections]], [[rotations]] and [[boosts]] in example \ref{CliffordConjugtionReflectionAndRotation}
are given by [[conjugation actions]], there is a crucial ambiguity in the Clifford elements that
induce them:

1. the conjugation action by $\Gamma_a$ coincides precisely with the conjugation action by $-\Gamma_a$;

1. the [[conjugation action]] by $\exp(\tfrac{\alpha}{4} \Gamma_{a b})$ coincides precisely with the
   conjugation action by $-\exp(\tfrac{\alpha}{4}\Gamma_{a b})$.

=--


+-- {: .num_defn #SpinGroup}
###### Definition

For $d \in \mathbb{N}$, the **[[spin group]]** $Spin(d-1,1)$ is the group of
even graded elements of the Clifford algebra $Cl(\mathbb{R}^{d-1},1)$ (def. \ref{CliffordAlgebra})
which are [[unitary operator|unitary]] with respect to $\overline{(-)}$ (def. \ref{BarConjugationOnCliffordAlgebra}):

$$
  Spin(d-1,1)
   \;\coloneqq\;
  \left\{
    A \in Cl(\mathbb{R}^{d-1,1})_{even}
    \;\vert\;
    \overline{A} A = 1
  \right\}
  \,.
$$

=--

+-- {: .num_prop #SpinDoubleCover}
###### Proposition

The [[function]]

$$
  Spin(d-1,1)
    \longrightarrow
  End(Cl(\mathbb{R}^{d-1,1}))
$$

from the [[spin group]] (def. \ref{SpinGroup}) to the [[general linear group]] in $d$-dimensions
given by sending $A \in Spin(d-1,1) \hookrightarrow Cl(\mathbb{R}^{d-1,1})$ to the
[[conjugation action]]

$$
  \overline{A}(-) A
  \,,
$$

is

1. a [[group]] [[homomorphism]] onto the [[proper orthochronous Lorentz group]] (def. \ref{LorentzGroup}):

   $$
     Spin(d-1,1) \longrightarrow SO^+(d-1,1)
   $$

   (where we are identifying Minkowski spacetime as the subspace of the [[Clifford algebra]]
containing the [[linear combinations]] of the generators, according to remark \ref{VectorsInsideCliffordAlgebra})

1. exhibiting a $\mathbb{Z}/2$-[[central extension]].

=--

+-- {: .proof}
###### Proof

That the function is a group homomorphism into the [[general linear group]], hence that it acts by [[linear transformations]]
on the generators follows by using that it clearly lands in [[automorphisms]] of the Clifford algebra.

That the function lands in the [[Lorentz group]] $O(d-1,1) \hookrightarrow GL(d)$ follows from remark \ref{VectorsInsideCliffordAlgebra}:

$$
  \begin{aligned}
    \eta(\overline{A}v_1A , \overline{A} v_2 A)
    &=
    \tfrac{1}{2}
    \left(
    \left(\overline{A} \hat v_1 A\right) \left(\overline{A}\hat v_2 A\right)
    +
    \left(\overline{A} \hat v_2 A\right) \left(\overline{A} \hat v_1 A\right)
    \right)
    \\
    & =
    \tfrac{1}{2}
    \left(
    \overline{A}(\hat v_1 \hat v_2 + \hat v_2 \hat v_1) A
    \right)
    \\
    & =
    \overline{A} A \tfrac{1}{2}\left( \hat v_1 \hat v_2 + \hat v_2 \hat v_1\right)
    \\
    & =
    \eta(v_1, v_2)
  \end{aligned}
  \,.
$$

That it moreover lands in the [[proper Lorentz group]] $SO(d-1,1)$ follows from
observing (example \ref{CliffordConjugtionReflectionAndRotation}) that every reflection is given by the [[conjugation action]] by
a linear combination of generators, which are excluded from the group $Spin(d-1,1)$
(as that is defined to be in the even subalgebra).


To see that the homomorphism is surjective, use that all elements of $SO(d-1,1)$
are products of [[rotations]] in hyperplanes. If a hyperplane is spanned by
$(\omega^{a b})$, then such a rotation is given, via example \ref{CliffordConjugtionReflectionAndRotation}
by the conjugation action by
$$
  \exp(\tfrac{\alpha}{4} \omega^{a b}\Gamma_{a b})
$$

for some $\alpha$, hence is in the image.

That the [[kernel]] is $\mathbb{Z}/2$ is clear from the fact that the only even Clifford elements which commute
with all vectors are the multiples $a \in \mathbb{R} \hookrightarrow Cl(\mathbb{R}^{d-1,1})$ of the identity.
For these $\overline{a} = a$ and hence
the condition $\overline{a} a = 1$ is equivalent to $a^2 = 1$. It is clear that these two elements
$\{+1,-1\}$ are in the [[center]] of $Spin(d-1,1)$. This
kernel reflects the ambiguity from remark \ref{AmbiguityInCliffordConjugation}.

=--





\ref{AmbiguityInCliffordConjugation}

\ref{SpinGroup}

