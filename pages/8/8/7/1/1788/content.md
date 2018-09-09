Test

+-- {: .num_defn #RepresentableAutomorphismGroup}
###### Definition

We say that a functor

$$
  \underline{Aut}(\omega)
   \;\colon\;
  Aff(sVect)^{op}
    =
  CMon(sVect)
     \longrightarrow
  Grp
$$

is **[[representable functor|representable]]** if there exists a [[supercommutative Hopf algebra]] $H$, hence an affine [[algebraic group]] $Spec(H)$ (def. \ref{Supergroup}) and a [[natural isomorphism]] with the [[hom functor]] into $Spec(H)$:


$$
  \underline{Aut}(\omega)
  \simeq
  Hom_{CMon(sVect)}(H,-)
    =
  Hom_{Aff(sVect)}(-,Spec(H))
  \,.
$$


=--

+-- {: .num_defn #AutomorphismGroupOfFiberFunctor}
###### Definition

Let $\omega \colon \mathcal{A} \to \mathcal{B}$ be a  [[fiber functor]]  (def \ref{FiberFunctor}).

For $A \in CMon(\mathcal{B})$ a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}), write

$$
  \omega_A
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  \mathcal{B}
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(\mathcal{B})
$$

for its image under [[extension of scalars]] along $1 \to A$ to $A$ (prop. \ref{ExtensionOfScalars}).

With this, the **automorphism group** of $\omega$

$$
  \underline{Aut}(\omega)
  \in
  PSh(Aff(\mathcal{B}))
$$

is defined to be the functor which on objects assigns the [[discrete group]] of [[natural automorphisms]] of the image $\omega_A$ of $\omega$ under [[extension of scalars]] as above

$$
  \underline{Aut}(\omega)(Spec(A))
   \coloneqq
  Aut(\omega_{A})
$$

and which to a homomorphism of algebras

$$
  \phi \;\colon\; A_1 \longrightarrow A_2
$$

assigns the action of the [[extension of scalars]]-functor along $\phi$:

$$
  \phi_\ast
    \;\colon\;
  Aut(\omega_{A_1})
    \longrightarrow
  Aut(\omega_{A_2})
  \,.
$$

This is clearly a presheaf, by [[functor|functoriality]] of [[extension of scalars]].


=--

Specializing def. \ref{AutomorphismGroupOfFiberFunctor} to $\mathcal{B} = $ [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}), where a commutative monoid is a [[supercommutative superalgebra]] (def. \ref{SupercommutativeSuperalgebra}) it reads as follows:

+-- {: .num_example #AutomorphismSuperGroupOfSuperFiberFunctor}
###### Example

Let $\omega \colon \mathcal{A} \to sVect$ be a  [[fiber functor|super fiber functor]]  (def \ref{FiberFunctor}).

For $A \in CMon(sVect)$ a [[commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}), write

$$
  \omega_A
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  sVect
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(sVect)
$$


For $A \in CMon(sVect)$ a [[supercommutative algebra]], write

$$
  \omega_A
   \;\colon\;
  \mathcal{A}
    \stackrel{\omega}{\longrightarrow}
  sVect
   \stackrel{A \otimes(-)}{\longrightarrow}
  A Mod(sVect)
$$

for its image under [[extension of scalars]] to $A$ (prop. \ref{MonoidModuleOverItself}).

With this, the **automorphism super-group** of $\omega$

$$
  \underline{Aut}(\omega)
  \in
  PSh(Aff(sVect))
$$

is defined by

$$
  \underline{Aut}(\omega)(Spec(A))
   \coloneqq
  Aut(\omega_{A})
  \,.
$$

=--



+-- {: .num_prop #AutomorphismSupergroupOfFiberFunctorIsRepresentable}
###### Proposition

For $k$ an [[algebraically closed field]] of [[characteristic zero]], and for $\mathcal{A}$ a $k$-[[tensor category]] equipped with a [[fiber functor|super fiber functor]] $\omega$, then its automorphism supergroup (def. \ref{AutomorphismSuperGroupOfSuperFiberFunctor}) is [[representable functor|representable]] (def. \ref{RepresentableAutomorphismGroup}): there exists a [[supercommutative Hopf algebra]] $H_\omega$ and a [[natural isomorphism]]

$$
  \underline{Aut}(\omega)
    \simeq
  Hom_{CMon(sVect)}(H_\omega,-)
   =
  Hom_{Aff(sVect)}(-, Spec(H_\omega))
  \,,
$$

which, with the [[Yoneda embedding]] understood, we write simply as

$$
  \underline{Aut}(\omega)
    \simeq
  Spec(H_\omega)
  \,.
$$

=--

([Deligne 90, prop. 8.11](#Deligne90))

The following says that in fact all homomorphisms between fiber functors are necessarily [[isomorphisms]]:

+-- {: .num_lemma #MonoidalTransformationBetweenFiberFunctorIsIso}
###### Lemma

Every [[monoidal natural transformation]] (def. \ref{LaxMonoidalFunctor}) between two [[fiber functors]] (def. \ref{FiberFunctor}) is an [[isomorphism]] (i.e. a [[natural isomorphism]]).

=--

([Deligne 90, 8.11 (ii)](#Deligne90), [Deligne 02, lemma 3.2](#Deligne02))


+-- {: .num_defn #FundamentalSupergroup}
###### Definition

Let $\mathcal{A}$ be a [[tensor category]] and regard the [[identity]] functor on it as a fiber functor (def. \ref{FiberFunctor}). Then the automorphism group of $id_{\mathcal{A}}$ according to def. \ref{AutomorphismSuperGroupOfSuperFiberFunctor} is called the **fundamental group** of $\mathcal{A}$, denoted:

$$
  \pi(\mathcal{A})
   \coloneqq
  \underline{Aut}(id_{\mathcal{A}})
$$


=--

([Deligne 90, 8.12, 8.13](#Deligne90))

+-- {: .num_example #FundamentalGroupOfCategoryOfSuperVectorSpaces}
###### Example

The fundamental group (def. \ref{FundamentalSupergroup}) of the [[category of super vector spaces]] [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}) is $\mathbb{Z}/2$:

$$
  \pi(sVect)
    \simeq
  \mathbb{Z}/2
  \,.
$$

The non-trivial element in $\pi(sVect)$ acts on any super-vector space as the [[endomorphism]] which is the identity on even graded elements, and multiplication by $(-1)$ on odd graded elements.

=--

([Deligne 90, 8.14 iv)](#Deligne90))

+-- {: .num_prop #AutOfFibFuncIsImagUnderFibFuncOfFundamentalGroup}
###### Proposition

For $\mathcal{A}$ a $k$-[[tensor category]] equipped with a [[fiber functor|super fiber functor]] $\omega \colon \mathcal{A} \to sVect$ (def. \ref{FiberFunctor}), then the automorphism supergroup of $\omega$ is the image under the super fiber functor $\omega$ of the fundamental group of $\mathcal{A}$, according to def. \ref{FundamentalSupergroup}:

$$
  \underline{Aut}(\omega)
    \simeq
  \omega(\pi(\mathcal{A}))
  \,.
$$

Here on the right we are using that $\omega$ is a [[strong monoidal functor]] so that it preserves
[[commutative monoids]] as well as [[comonoids]] by prop. \ref{MonoidsPreservedByLaxMonoidalFunctor},
hence preserves [[commutative Hopf algebras]].


=--

([Deligne 90 (8.13.1)](#Deligne90))


+-- {: .num_prop #HomomorphismFromPiT2ToEtaPiT1}
###### Proposition

Let $\mathcal{A}_1, \mathcal{A}_2$ be two $k$-[[tensor categories]] and let

$$
  \eta \;\colon\; \mathcal{A}_1 \longrightarrow \mathcal{A}_2
$$

be a [[functor]] which is $k$-linear, [[strong monoidal functor|monoidal]] and [[exact functor]]. Then there is induced a canonical group homomorphism


$$
  \pi(\mathcal{A}_2)
   \longrightarrow
  \eta(\pi(\mathcal{A}_1))
$$

from the fundamental group of $\mathcal{A}_1$ (def. \ref{FundamentalSupergroup}) to the image under $\eta$ of the fundamental group of $\mathcal{A}_2$.

=--

([Deligne 90, 8. 15. 2](#Deligne90))





### Super-exterior powers and Schur functors

A [[finite dimensional vector space]] $V$ has the property that a high enough [[alternating power]] of it vanishes $\wedge^n V = 0$, namely this is the case for all $n \gt dim(V)$, and hence this vanishing is just another reflection of the finiteness of the [[dimension]] of $V$. For a [[super vector space]] $V$ of degreewise finite dimension an analog statement is still true, but one needs to form not just alternating powers but also [[symmetric powers]] (prop. \ref{SchurFunctorAnnihilatingFiniteDimensionalSuperVectorSpace} below), in fact one needs to apply a generalization of both of these constructions, a _[[Schur functor]]_.


The operation of forming [[symmetric powers]] and [[alternating powers]] makes sense in every [[tensor category]]. Moreover, these operations are the two extreme cases of the more general concept of [[Schur functors]]: Given any [[object]] $X$ and given any choice of [[irreducible representation]] $V_\lambda$ of the [[symmetric group]] $\Sigma_n$, then one consider the [[subobject]] $S_\lambda(X^{\otimes^n})$ of the $n$-fold [[tensor power]] that is [[invariant]] under this action.

The first step in the proof of the main theorem (theorem \ref{TheTheorem} below) is the proposition (prop. \ref{LengthOfObjectIsBounded} below) that all objects that have subexponential growth of length (def. \ref{SubexponentialGrowth}) are actually annihilated by some [[Schur functor]] for the [[symmetric group]].


+-- {: .num_defn #SchurFunctor}
###### Definition

For $(\mathcal{A},\otimes)$ a $k$-[[tensor category]] as in def.\ref{TensorCategory}, for $X \in \mathcal{A}$ an [[object]], for $n \in \mathbb{N}$ and $\lambda$ a [[partition]] of $n$, regarded as a [[Young diagram]] and hence as a [[representation]] of the [[symmetric group]] $V_\lambda$, say that the value of the [[Schur functor]] $S_\lambda$ on $X$ is

$$
  \begin{aligned}
    S_{\lambda}(X)
      & \coloneqq
    (V_\lambda \otimes X^{\otimes_n})^{S_n}
    \\
    & =
    \left(
      \frac{1}{n!}
      \underset{g\in S_n}{\sum}
      \rho(g)
    \right)
    \left(
      V_\lambda \otimes X^{\otimes_n}
    \right)
  \end{aligned}
$$

where

* $(-)^{S_n}$ is the subobject of [[invariants]];

* $S_n$ is the [[symmetric group]] on $n$ elements;

* $V_\lambda$ is the [[irreducible representation]] of $S_n$ corresponding to $\lambda$;

* $\rho$ is [[diagonal action]] of $S_n$ on $V_\lambda \otimes X^{\otimes_n}$, coming from the canonical [[permutation]] action on $X^{\otimes_n}$;

* $(-)^{S_n}$ denotes the subspace of [[invariants]] under the action $\rho$

* the second expression just rewrites the invariants as the image of all elements under [[group averaging]].

=--

([Deligne 02, 1.4](#Deligne02))

+-- {: .num_example}
###### Example

For $\lambda = (n)$, then $V_{(n)} = k$ equipped with the trivial action of the symmetric group. In this case the corresponding [[Schur functor]] (def. \ref{SchurFunctor}) forms the $n$th [[symmetric power]]

$$
  S_{(n)}(X) = Sym^n(X)
  \,.
$$

For the dual case where $\lambda = (1,1, \cdots, 1)$ then $V_{(1,1,\cdots, 1)} = k$ equipped with the action by multiplication with the [[signature of a permutation]] and the corresponding [[Schur functor]] forms the [[alternating power]]

$$
  S_{(1,1, \cdots, 1)}(X) = \wedge^n X
  \,.
$$

=--

+-- {: .num_prop #SchurFunctorAnnihilatingFiniteDimensionalSuperVectorSpace}
###### Proposition

Let $V = V_{even} \oplus V_{odd}$ be a [[super vector space]] of degreewise finite dimension $d_{even}, d_{odd} \in \mathbb{N}$. Then there exists a [[Schur functor]] $S_\lambda$ (def. \ref{SchurFunctor}) that annihilates $V$:

$$
  S_\lambda(V) \simeq 0
  \,.
$$

Specifically, this is the case precisely if the corresponding [[Young tableau]] $[\lambda]$ satifies

$$
  [\lambda] \subset \left\{ (i,j)\;\vert\; i \leq d_{even}, j \leq d_{odd} \right\}
  \,.
$$

=--

([Deligne 02, corollary 1.9](#Deligne02))


## Statement of the theorem
 {#Statement}


+-- {: .num_theorem #TheTheorem}
###### Theorem

Every $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) such that

1. $k$ is an [[algebraically closed field]] of [[characteristic zero]] (e.g. the field of [[complex numbers]])

1. $\mathcal{A}$ is of subexponential growth according to def. \ref{SubexponentialGrowth}

then $\mathcal{A}$ is a neutral super [[Tannakian category]] (def. \ref{TannakianCategory}) and  there exists

1. an affine algebraic [[supergroup]] $G$ (def. \ref{Supergroup}) whose [[algebra of functions]] $\mathcal{O}(G)$ is a [[finitely generated object|finitely generated]] $k$-algebra.

1. a tensor-[[equivalence of categories]]

   $$
     \mathcal{A}
        \simeq
     Rep(G,\epsilon)
     \,.
   $$

   between $\mathcal{A}$ and the [[category of representations]] of $G$ of finite dimension, according to def. \ref{Superrepresentation} and prop. \ref{RegularTensorCategoriesOfSuperrepresentations}.

=--

([Deligne 02, theorem 0.6](#Deligne02))


## Proof

We outline key steps of the proof of theorem \ref{TheTheorem}, given in [Deligne 02](#Deligne02).


Throughout, let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).


The proof proceeds in three main steps:

1. **Proposition \ref{LengthOfObjectIsBounded}** states that in a $k$-[[tensor category]] an object $X$ is of subexponential growth (def. \ref{SubexponentialGrowth}) precisely if there exists a [[Schur functor]] that annihilates it, hence if some power of $X$, skew-symmetrized in sme variables and symmetrized in others, vanishes.

   This proposition is where the [[symmetric group]] and its [[permutation]] [[action]] on [[tensor powers]] appears, from just a kind of finite-dimensionality assumption.

1. **Proposition \ref{SchurFinitenessImpliesExistenceOfSuperFiberFunctor}** in turn says that if every object in $\mathcal{A}$ is annihilated by some [[Schur functor]], then there exists a super [[fiber functor]] on $\mathcal{A}$ over some [[supercommutative superalgebra]] $R$, hence then every object of $\mathcal{A}$ has underlying it a [[super vector space]] with some extra structure.

   This proposition is where [[superalgebra]] proper appears.

1. **Proposition \ref{DeligneTannakaReconstruction}** states that every $k$-[[tensor category]] equipped with a super fiber functor $\omega \colon \mathcal{A} \to sVect$, is equivalent to the category of super-representations of the automorphism supergroup of $\omega$.

   This proposition is the instance of general [[Tannaka reconstruction]] applied to the case of fiber functors with values in super vector spaces. This is where the "supersymmetry" supergroup is extracted.


+-- {: .num_prop #LengthOfObjectIsBounded}
###### Proposition

For $\mathcal{A}$ a $k$-[[tensor category]] (def. \ref{TensorCategory}), then the following are equivalent:

1. the category $\mathcal{A}$ has subexponential growth (def. \ref{SubexponentialGrowth});

1. for every object $X \in \mathcal{A}$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, on $X$ vanishes: $S_\lambda(X) = 0$.

=--

([Deligne 02, prop. 05](#Deligne02))


+-- {: .num_prop #SchurFinitenessImpliesExistenceOfSuperFiberFunctor}
###### Proposition

If for every object of a $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) there exists a [[Schur functor]] (def. \ref{SchurFunctor}) that annihilates it, then there exists a [[fiber functor|super fiber functor]] (def. \ref{FiberFunctor}) over $k$,
hence then $\mathcal{A}$ is a neutral super [[Tannakian category]] (def. \ref{TannakianCategory}).

$$
  \omega
    \;\colon\;
  \mathcal{A}
    \longrightarrow
  sVect
  \,.
$$

=--

([Deligne 02, prop. 2.1 "r&#233;sultat cl&#233; de l'article", together with prop. 4.5](#Deligne02))

+-- {: .proof}
###### Proof idea

First ([Deligne 02, middle of p. 16](#Deligne02)) consider the [[tensor category]]

$$
  s \mathcal{A}
    \coloneqq
  (\mathcal{A}^{\mathbb{Z}/2}, \tau_{super} )
$$

which is that of $\mathbb{Z}/2$-graded objects of $\mathcal{A}$, and whose [[braiding]] is given on objects $X,Y$ of homogeneous degree by that of $\mathcal{A}$ multiplied with $(-1)^{deg(X) deg(Y)}$.

Write $1$ and $\overline{1}$ for the [[tensor unit]] of $\mathcal{A}$, regarded in even degree and in odd degree in $s \mathcal{A}$, respectively.

For $A \in CMon(\mathcal{A})$ a [[commutative monoid]], write

$$
  \mathcal{A}
  \simeq
  1 Mod(\mathcal{A})
     \underoverset{\underset{U}{\longleftarrow}}{\overset{(-)_A \coloneqq F}{\longrightarrow}}
 {}
  A Mod(\mathcal{A})
$$

for the [[extension of scalars]] operation $A \otimes(-)$, [[left adjoint]] to [[restriction of scalars]] (prop. \ref{ExtensionOfScalars}).

Show then that the condition that an object $X$ is annihilated by some [[Schur functor]] is equivalent to the existence of an algebra $A$ such that

$$
  X_A \simeq 1^p \oplus \overline{1}^q
$$

for some $p,q \in \mathbb{N}$, hence that each such object is _$A$-locally_ a [[super vector space]].

([Deligne 02, prop. 2.9](#Deligne02)).

Moreover, for each [[short exact sequence]]

$$
  0 \to X \to Y \to Z \to 0
$$

in $s \mathcal{A}$, there exists an algebra $A$ such that

$$
  0 \to X_A \to Y_A \to Z_A \to 0
$$

is a [[split exact sequence]], (hence every short exact sequence is _locally_ split).

([Deligne 90, 7.14](#Deligne90), [Deligne 02, rappel 2.10](#Deligne 02))

Now ([Deligne 02, middle of p. 17](Deligne02)) let $A$ be the commutative monoid which is the [[tensor product]] of commutative monoids (example \ref{TensorProductOfTwoCommutativeMonoids}) over all [[isomorphism classes]] of [[objects]] and of [[short exact sequences]] in $\mathcal{A}$ of choices of commutative monoids for which these objects/exact sequencs are locally split, as above.

Then for an $A$-module $N$, write $\rho(N)$ for the [[subobject]] of $N$ inside $sVect \simeq Ind\langle 1, \overline{1}\rangle \hookrightarrow s \mathcal{A}$.

Check ([Deligne 02, bottom of p. 17](Deligne02)) that $\rho(A)$ inherits the structure of a commutative monoid, and that $\rho(N)$ inherits the structure of a module over $\rho(N)$.

Set

$$
  R \coloneqq \rho(A)
  \,.
$$

Hence for every object $X$, then

$$
  \omega(X)
    \coloneqq
  \rho(X_A)
$$

has the structure of an $R$-module. By $A$-local splitness of all short exact sequence, $\omega$ is an [[exact functor]].

Hence

$$
  \omega \;\colon\; s \mathcal{A} \longrightarrow R Mod(sVect)
$$

is a super fiber functor on $s\mathcal{A}$ over $R$. This restricts to a super fiber functor over $R$ on  $\mathcal{A}$, regarded as the sub-category of even-graded objects in $s \mathcal{A}$:

$$
  \mathcal{A}
    \hookrightarrow
  s \mathcal{A}
   \overset{\omega}{\longrightarrow}
  R Mod(sVect)
  \,,
$$

Finally check ([Deligne 02, prop. 4.5](#Deligne02)) that
if a $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) admits a [[fiber functor|super fiber functor]] (def. \ref{FiberFunctor}) over a [[supercommutative superalgebra]] $R$ over $k$

$$
  \mathcal{A}
    \longrightarrow
  R Mod(sVect)
$$

then it also admits a super fiber functor over $k$ itself, i.e. a fiber functor to [[sVect]]

$$
  \mathcal{A}
    \longrightarrow
  k Mod(sVect)
  \simeq
  sVect
  \,.
$$

This is argued by expressing $R$ as an [[inductive limit]]

$$
  R = \underset{\longrightarrow}{\lim}_\beta R_\beta
$$

over [[supercommutative superalgebras]] $R_\beta$ of finite type over $k$ and observing (...) that there exists $\beta$ such that $\omega_\beta$ is still a fiber functor and such that there exists an algebra homomorphism $R_\beta \to k$.

Finally then the fiber functor in question is

$$
  \omega_\beta \otimes_{R_\beta} k
   \;\colon\;
  \mathcal{A}
    \longrightarrow
  sVect_k
  \,.
$$

=--

+-- {: .num_prop #DeligneTannakaReconstruction}
###### Proposition

For every $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) and a [[fiber functor|super fiber functor]] over $k$ (def. \ref{FiberFunctor})

$$
  \omega
    \;\colon\;
   \mathcal{A}
     \longrightarrow
   sVect_k
$$

then $\omega$ induces an [[equivalence of categories]]

$$
  \mathcal{A}
     \stackrel{\simeq}{\longrightarrow}
   Rep( \underline{Aut}(\omega),\epsilon)
$$

of $\mathcal{A}$ with the [[category of representations|category of finite dimensional representations]], according to def. \ref{Superrepresentation} and prop. \ref{RegularTensorCategoriesOfSuperrepresentations}, of the automorphism supergroup $\underline{Aut}(\omega)$ (example. \ref{AutomorphismSuperGroupOfSuperFiberFunctor}, prop. \ref{AutomorphismSupergroupOfFiberFunctorIsRepresentable}) of the super fiber functor, where $\epsilon$ is te image of the unique nontrivial element in

$$
  \underline{Aut}(sVect) \simeq \mathbb{Z}/2
$$

(according to example \ref{FundamentalGroupOfCategoryOfSuperVectorSpaces}) under the group homomorphism

$$
  \pi(sVect) \longrightarrow \omega(\pi(\mathcal{A}))
  \simeq \underline{Aut}(\omega)
$$

from prop. \ref{HomomorphismFromPiT2ToEtaPiT1} and using the isomorphism from prop. \ref{AutOfFibFuncIsImagUnderFibFuncOfFundamentalGroup}.

=--


This is the main [[Tannaka reconstruction]] theorem ([Deligne 90, 8.17](#Deligne90))
specialized to super fiber functors ([Deligne 90, 8.19](#Deligne90)).


## References

The theorem is due to

* {#Deligne02} [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

building on the general results on [[Tannakian categories]] in

* {#Deligne90} [[Pierre Deligne]], _[[Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp. 111-195 ([pdf](https://publications.ias.edu/sites/default/files/60_categoriestanna.pdf))

which are reviewed and further generalized in

* {#DeligneMilne12} [[Pierre Deligne]] [[James Milne]], _Tannakian categories_, 2012 ([pdf](http://www.jmilne.org/math/xnotes/tc.pdf))

Review is in

* {#Ostrik04} [[Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))

* {#EGNO15} [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], section 9.11 in _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))

Further discussion in view of the theory of [[triangular Hopf algebras]] is in

* {#EtingofGelaki02} [[Pavel Etingof]], [[Shlomo Gelaki]], _The classification of finite-dimensional triangular Hopf algebras over an algebraically closed field of characteristic 0_ ([arXiv:0202258](http://de.arxiv.org/abs/math/0202258))


Tannaka duality for ordinary compact groups regarded as supergroups (hence equipped with "inner parity", def. \ref{InnerParity}, here just being an involutive central element) is discussed in

* {#Mueger06} [[Michael Müger]], _Abstract Duality Theory for Symmetric Tensor $*$-Categories_ appendix ([pdf](http://www.math.ru.nl/~mueger/PDF/16.pdf)), in [[Hans Halvorson]],  _Algebraic quantum field theory_ ([arXiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036)), in J. Butterfield & J. Earman (eds.) _Handbook of Philosophy and Physics_

as a proof of [[Doplicher-Roberts reconstruction]]

Commutative algebra internal to symmetric monoidal categories is discussed in

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], _Rings, modules and algebras in stable homotopy theory_, AMS 1997, 2014

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))

and specifically for [[commutative Hopf algebroids]] in

* {#Ravenel86} [[Doug Ravenel]], chapter 2 and appendix A.1 of  _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))

(These authors are motivated by the application of the general theory of algebra in monoidal categories
to "[[higher algebra]]" ("[[brave new algebra]]") in [[stable homotopy theory]].
This happens to also be a version of [[supercommutative superalgebra]], see at
_[[Introduction to Stable homotopy theory]]_ the section [1-2 Homotopy commutative ring spectra](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyRingSpectra).)

For an attempt to generalize Deligne's theorem to positive characteristic, see

* [[Victor Ostrik]], _On symmetric fusion categories in positive characteristic_, ([arXiv:1503.01492](https://arxiv.org/abs/1503.01492))

Discussion relating to [[2-rings]] and the [[spin-statistics theorem]] is in

* {#JohnsonFreyd15} [[Theo Johnson-Freyd]], _Spin, statistics, orientations, unitarity_, Algebraic and Geometric Topology ([arXiv:1507.06297](https://arxiv.org/abs/1507.06297))

[[!redirects Deligne theorem on tensor categories]]

[[!redirects Deligne reconstruction theorem]] 



