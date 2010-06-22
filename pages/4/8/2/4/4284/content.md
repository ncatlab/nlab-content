* tic
{: .toc}

Initial import of counterexamples taken from [this MO question](http://mathoverflow.net/questions/29006/counterexamples-in-algebra).


###Group Theory###

1. A non-[[abelian group]], all of whose subgroups are [[normal subgroup|normal]]:

   $$
   Q \coloneqq \langle a, b | a^4 = 1, a^2 = b^2, a b = b a^3 \rangle
   $$

1. A finitely presented, infinite, simple group

   Thomson's group T.

1. A [[group]] that is not the [[fundamental group]] of any [[3-manifold]].

   $$
   \mathbb{Z}^4
   $$

1. Two finite non-isomorphic groups with the same order profile.

   $$
   C_4 \times C_4, \qquad C_2 \times \langle a, b, | a^4 = 1, a^2 = b^2, a b = b a^3 \rangle
   $$

1. A [[quasigroup]] that is not isomorphic to any [[loop].

   $\{a, b, c\}$ with multiplication table:

   $$
   \begin{matrix}
   * & a & b & c \\
   a & a & c & b \\
   b & c & b & a \\
   c & b & a & c
   \end{matrix}
   $$

1. A counterexample to the converse of Lagrange's theorem.

   The alternating group $A_4$ has order $12$ but no subgroup of order $6$.

1. A finite group in which the product of two commutators is not a commutator.

   $$
   G = \langle (a c)(b d), (e g)(f h), (i k)(j l), (m o)(n p), (a c)(e g)(i k), (a b)(c d)(m o), (e f)(g h)(m n)(o p), (i j)(k l)\rangle \subseteq S_{16}
   $$

###Ring Theory###

1. A ring that is right [[Notherian ring|Notherian]] but not left Notherian:

   Matrices of the form $\begin{bmatrix} a & b \\ 0 & c \end{bmatrix}$ where $a \in \mathbb{Z}$ and $b,c \in \mathbb{Q}$.

1. A ring that is local commutative Noetherian but not Cohen-Macaulay

   $$
   k[x,y]/(x^2, x y)
   $$

1. A number ring that is a [[principal ideal domain]] that is not Euclidean.

   $$
   \mathbb{Q}(\sqrt{-19})
   $$

1. An [[epimorphism]] of [[rings]] that is not [[surjective]].

   $$
   \mathbb{Z} \to \mathbb{Q}
   $$

1. A [[ring]] whose [[spec]] has non-open connected components.

   $$
   \prod_{n=1}^\infty \mathbb{F}_2
   $$

1. A non-[[Noetherian]] [[ring]] $A$ such that all local rings on $Spec(A)$ are Noetherian.

   $$
   \prod_{n=1}^\infty \mathbb{F}_2
   $$

1. A number field whose ring of integers is Euclidean but not norm-Euclidean.

   $$
   \mathbb{Q}(\sqrt{69})
   $$

###Hopf Algebras###

1. A non-commutative and non-cocommutative [[Hopf algebra]]

   $$
   \begin{aligned}
   H &\coloneqq &\langle x, g | g^2 = 1, x^2 = 0, g x g = -x\rangle \\
   \Delta(g) &= &g \otimes g, \\
   \Delta(x) &= &x \otimes 1 + g \otimes x, \\
   \epsilon(g) &=& 1, \\
   \epsilon(x) &=& 0, \\
   S(g) &= &g, \\
   S(x) &= &- g x
   \end{aligned}
   $$

###Homological Algebra###

1. An [[exact sequence]] that does not split:

   $$
   0 {\times 2 \atop \to} \mathbb{Z} \to \mathbb{Z} \to \mathbb{Z}/2\mathbb{Z} \to 0
   $$

###Galois Theory###

1. A polynomial, solvable in radicals, whose splitting field is not a radical extension of $\mathbb{Q}$.

   Take any cyclic cubic; that is, any cubic with rational coefficients, irreducible over the rationals, with Galois group cyclic of order $3$.
