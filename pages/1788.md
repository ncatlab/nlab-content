
### Conner-Floyd Chern classes
 {#ConnerFloydChernClasses}

**Idea.** For $E$ a [[complex oriented cohomology theory]], then the generators of the $E$-[[cohomology groups]] of the [[classifying space]] $B U$ are called the _[[Conner-Floyd Chern classes]]_, in $E^\bullet(B U)$.

Using basic properties of the classifying space $B U(1)$ via its incarnation as the infinite [[complex projective space]] $\mathbb{C}P^\infty$, one finds that the [[Atiyah-Hirzebruch spectral sequences]]

$$
  H^p(\mathbb{C}P^n, \pi_q(E)) \Rightarrow H^\bullet(\mathbb{C}P^n)
$$

collapse right away, and that the [[inverse system]] which they form satisfies the [[Mittag-Leffler condition]]. Accordingly the [[Milnor exact sequence]] gives that the ordinary [[first Chern class]] $c_1$ generates,  over $\pi_\bullet(E)$, all Conner-Floyd classes over $B U(1)$:

$$
  E^\bullet(B U(1)) \simeq \pi_\bullet(E) [ [ c_1 ] ]
  \,.
$$

This is the key input for the discussion of [[formal group laws]] [below](#FormalGroupLaws).

Combining the [[Atiyah-Hirzebruch spectral sequence]] with the [[splitting principle]] as for ordinary Chern classes [above](#ChernClasses) yields, similarly, that in general Conner-Floyd classes are generated, over $\pi_\bullet(E)$, from the ordinary Chern classes.

Finally one checks that Conner-Floyd classes canonically serve as [[Thom classes]] for $E$-cohomology of the [[universal complex vector bundle]], thereby showing that [[complex oriented cohomology theories]] are indeed canonically [[orientation in generalized cohomology|oriented]] on ([[spherical fibrations]] of) [[complex vector bundles]].

**Literature.** ([Kochman 96, section 4.3](#Kochman96) [Adams 74, part I.4, part II.2 II.4, part III.10](#Adams74), [Lurie 10, lecture 5](#Lurie10))

+-- {: .num_prop #ConnerFloyedClasses}
###### Proposition

Given a [[complex oriented cohomology theory]] $E$ with complex orientation $c_1^E$, then the $E$-[[generalized cohomology]] of the [[classifying space]] $B U(n)$ is freely generated over the [[graded commutative ring]] $\pi_\bullet(E)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)) by classes $c_k^E$ for $0 \leq \leq n$ of degree $2k$, these are called the **[[Conner-Floyd-Chern classes]]**

$$
  E^\bullet(B U(n))
    \;\simeq\;
  \pi_\bullet(E)[ [ c_1^E, c_2^E, \cdots, c_n^E ] ]
  \,.
$$

Moreover, pullback along the canonical inclusion $B U(n) \to B U(n+1)$ is the identity on $c_k^E$ for $k \leq n$ and sends $c_{n+1}^E$ to zero.

For $E$ being [[ordinary cohomology]], this reduces to the ordinary [[Chern classes]] of prop. \ref{GeneratorsOfCohomologyOfBunChernClasses}.

=--

For details see ([Pedrotti 16, prop. 3.1.14](#Pedrotti16)).



### Formal group laws of first CF-Chern classes
 {#FormalGroupLaws}

**Idea.** The [[classifying space]] $B U(1)$ for [[complex line bundles]] is a [[homotopy type]] canonically equipped with commutative group structure ([[infinity-group]]-structure), corresponding to the [[tensor product]] of [[complex line bundles]]. By the above, for $E$ a [[complex oriented cohomology theory]] the first [[Conner-Floyd Chern class]] of these complex line bundles generates the $E$-cohomology of $B U(1)$, it follows that the [[cohomology ring]] $E^\bullet(B U(1)) \simeq \pi_\bullet(E)[ [ c_1 ] ]$ behaves like the ring of $\pi_\bullet(E)$-valued functions on a 1-dimensional commutative [[formal group]] equipped with a canonical [[coordinate]] function $c_1$. This is called a _[[formal group law]]_ over the [[graded commutative ring]] $\pi_\bullet(E)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)).

On abstract grounds it follows that there exists a commutative ring $L$ and a universal (1-dimensional commutative) formal group law $\ell$ over $L$. This is called the _[[Lazard ring]]_. [[Lazard's theorem]] identifies this ring concretely: it turns out to simply be the [[polynomial ring]] on generators in every even degree.

Further below this has profound implications on the structure theory for complex oriented cohomology. The [[Milnor-Quillen theorem on MU]] identifies the Lazard ring as the cohomology ring of the [[Thom spectrum]] [[MU]], and then the [[Landweber exact functor theorem]], implies that there are lots of complex oriented cohomology theories.

**Literature.** ([Kochman 96, section 4.4](#Kochman96), [Lurie 10, lectures 1 and 2](#Lurie10))




#### Formal group laws

+-- {: .num_defn #AdicRing}
###### Definition

An (commutative) [[adic ring]] is a ([[commutative ring|commutative]]) [[topological ring]] $A$ and an ideal $I \subset A$ such that

1. the [[topological space|topology]] on $A$ is the $I$-[[adic topology]];

1. the canonical morphism

   $$
     A \longrightarrow \underset{\longleftarrow}{\lim}_n (A/I^n)
   $$

   to the [[limit]] over [[quotient rings]] by powers of the ideal is an [[isomorphism]].

A [[homomorphism]] of adic rings is a ring [[homomorphism]] that is also a [[continuous function]] (hence a function that preserves the filtering $A \supset \cdots \supset A/I^2 \supset A/I $). This gives a category $AdicRing$ and a subcategory $AdicCRing$ of commutative adic rings.

The [[opposite category]] of $AdicRing$ (on [[Noetherian rings]]) is that of affine [[formal schemes]].

Similarly, for $R$ any fixed [[commutative ring]], then adic rings under $R$ are _adic $R$-algebras_. We write $Adic A Alg$ and $Adic A CAlg$ for the corresponding categories.

=--

+-- {: .num_example #PowerSeriesAlgebra}
###### Example

For $R$ a [[commutative ring]] and $n \in \mathbb{N}$ then the [[formal power series ring]]

$$
  R[ [ x_1, x_2, \cdots, x_n ] ]
$$

in $n$ [[variables]] with [[coefficients]] in $R$ and equipped with the ideal

$$
  I = (x_1, \cdots , x_n)
$$

is an adic ring (def. \ref{AdicRing}).

=--

+-- {: .num_prop }
###### Proposition

There is a [[fully faithful functor]]

$$
  AdicRing \hookrightarrow ProRing
$$

from [[adic rings]] (def. \ref{AdicRing}) to [[pro-rings]], given by

$$
  (A,I) \mapsto ( (A/I^{\bullet}))
  \,,
$$

i.e. for $A,B \in AdicRing$ two adic rings, then there is a [[natural isomorphism]]

$$
  Hom_{AdicRing}(A,B)
    \simeq
   \underset{\longleftarrow}{\lim}_{n_2}
   \underset{\longrightarrow}{\lim}_{n_1}
   Hom_{Ring}(A/I^{n_1},B/I^{n_2})
  \,.
$$

=--

+-- {: .num_defn #GroupObjectFormalGroupLaw}
###### Definition

For $R \in CRing$ a [[commutative ring]] and for $n \in \mathbb{N}$, a **formal group law** of dimension $n$ over $R$ is the structure of a [[group object]] in the category $Adic R CAlg^{op}$ from def. \ref{AdicRing} on the object $R [ [x_1, \cdots ,x_n] ]$ from example \ref{PowerSeriesAlgebra}.

Hence this is a morphism

$$
  \mu
  \;\colon\;
  R[ [ x_1, \cdots, x_n ] ]
   \longrightarrow
  R [ [ x_1, \cdots, x_n, \, y_1, \cdots, y_n ] ]
$$

in $Adic R CAlg$ satisfying unitality, associativity.

This is a **commutative formal group law** if it is an abelian group object, hence if it in addition satisfies the corresponding commutativity condition.

=--

This is equivalently a set of $n$ power series $F_i$ of $2n$ variables $x_1,\ldots,x_n,y_1,\ldots,y_n$ such that (in notation $x=(x_1,\ldots,x_n)$, $y=(y_1,\ldots,y_n)$, $F(x,y) = (F_1(x,y),\ldots,F_n(x,y))$)

$$
  F(x,F(y,z))=F(F(x,y),z)
$$

$$
  F_i(x,y) = x_i+y_i+\,\,higher\,\,order\,\,terms
$$


+-- {: .num_example #Commutative1DimFormalGroupLaw}
###### Example

A 1-dimensional commutative formal group law according to def. \ref{GroupObjectFormalGroupLaw} is equivalently a [[formal power series]]

$$
  \mu(x,y)
  =
  \underset{i,j \geq 0}{\sum} a_{i,j} x^i y^j
$$

(the image under $\mu$ in $R[ [ x,y ] ]$ of the element $t \in R [ [ t ] ]$) such that


1. (unitality)

   $$
     \mu(x,0) = x$ and $\mu(0,x) = x
     \,;
   $$

1. (associativity)

   $$
     \mu(x,\mu(y,z)) = \mu(\mu(x,y),z)
     \,;
   $$

1. (commutativity)

   $$
     \mu(x,y) = \mu(y,x)
     \,.
   $$

The first condition means equivalently that

$$
  a_{i,0}
    =
  \left\{
    \array{
      1 & if i = 0
      \\
      0 & otherwise
    }
  \right.
  \;\;\;\;\,,
  \;\;\;\;\;
  a_{0,i}
    =
  \left\{
    \array{
      1 & if i = 0
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

Hence $\mu$ is necessarily of the form

$$
  \mu(x,y)
   \;=\;
   x + y + \underset{i,j \geq 1}{\sum} a_{i,j} x^i y^j
  \,.
$$

The existence of inverses is no extra condition: by [[induction]] on the index $i$ one finds that there exists a unique

$$
  \iota(x) = \underset{i \geq 1}{\sum} \iota(x)_i x^i
$$

such that

$$
  \mu(x,iota(x)) = x
  \;\;\;\,,
  \;\;\;
  \mu(\iota(x),x) = x
  \,.
$$

Hence 1-dimensional formal group laws over $R$ are equivalently [[monoids]] in $Adic R CAlg^{op}$ on $R[ [ x ] ]$.

=--



