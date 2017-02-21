
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


> under construction

#Contents#
* table of contents
{:toc}


## Idea

It is a classical fact that the [[rationalization]] of classical [[homotopy theory]] (of [[topological spaces]] or [[simplicial sets]]) -- called _[[rational homotopy theory]]_ -- is considerably more tractable than general [[homotopy theory]], as exhibited by the existence of small concrete [[dg-algebra|dg-algebraic]] models for [[rational homotopy types]]: [[minimal Sullivan algebras]]. A similar statement holds for [[stable homotopy theory]], i.e. the [[homotopy theory]] of [[spectra]] (of [[topological spaces]] or [[simplicial sets]]): rational spectra are equivalent to rational [[chain complexes]], i.e. to [[dg-modules]] over $\mathbb{Q}$, see at _[[rational stable homotopy theory]]_.

Now classical [[homotopy theory]] and [[stable homotopy theory]] are unified and jointly generalized in [[parameterized stable homotopy theory]], whose [[objects]] are [[parameterized spectra]], parameterized over a classical [[homotopy type]]. The _rational parameterized stable homotopy theory_ to be discussed here is supposed to be the rationalization of this joint generalization, unifiying and jointly generalizing the algebraic model of [[rational topological spaces]] by [[Sullivan algebras]] and of $H \mathbb{Q}$-[[module spectra]] by [[chain complexes]].

Here we (intend to) show that, accordingly, rational parameterized homotopy theory is presented by the the [[opposite category|opposite]] of the [[homotopical category]] of [[dg-modules]] over cochain [[differential graded-commutative algebras]] in non-negative degrees. 

> under construction


## Preliminaries

+-- {: .num_defn #ChainComplexes}
###### Definition

Write 

* $Ch_{\bullet,\mathbb{Q}}$ for the [[category of chain complexes]] of [[modules]]/[[vector spaces]] over $\mathbb{Q}$ (i.e. [[differential]] of degree -1)

* $Ch^{\bullet}_{\mathbb{Q}}$ for the category of [[cochain complexes]] (i.e. differential of degree +1).

For $n \in \mathbb{N}$ write

* $Ch_{\geq n, \mathbb{Q}} \hookrightarrow Ch_{\bullet,\mathbb{Q}}$ for the [[full subcategory]] of the [[chain complexes]] concentrated in degree $\geq n$;

* $Ch^{\geq n}_{\mathbb{Q}} \hookrightarrow Ch^\bullet_{\mathbb{Q}}$ for the [[full subcategory]] of the [[cochain complexes]] concentrated in degree $\geq n$.

For $V \in \mathbb{Q} Mod$ a rational [[vector space]], and for $n \in \mathbb{N}$, we write $V[n]$ both for the [[chain complex]] as well as for the [[cochain complex]] concentrated on $V$ in degree $n$. 


=--

+-- {: .num_defn #dgcAlgebras}
###### Definition

Write $dgcAlg^{\geq 0}_{\mathbb{q}}$ for the [[category]] of cochain [[dgc-algebras]] over the [[rational numbers]] concentrated in non-negative degrees.

Say that a [[morphism]] in this category is

1. a _weak equivalence_ if it is a  [[quasi-isomorphisms]] on the [[forgetful functor|underlying]] [[chain complexes]];

1. a _fibration_ if it is degreewise [[surjection]];

1. a _cofibration_ it it is a [[relative Sullivan algebra]] inclusion,

We write 

$$
  (dgcAlg^{\geq 0}_{\mathbb{Q}})_{proj}
$$

for the category $dgcAlg^{\geq 0}_{\mathbb{Q}}$ equipped with these three [[classes]] of morphisms.


=--

+-- {: .num_prop #dgcAlgProjectiveModelStructure}
###### Proposition

The [[homotopical category]] $(dgcAlg^{\geq 0}_{\mathbb{Q}})_{proj}$ from def. \ref{dgcAlgebras} is a [[model category]], to be called the _[[projective model structure on dgc-algebras]] in non-negative degrees_.

=--

([Bousfield-Gugenheim 76, theorem 4.3](#BousfieldGugenheim76))

+-- {: .num_example #DifferentialFormsPolynomial}
###### Example

For $S \in sSet$ a [[simplicial set]], write 

$$
  \Omega^\bullet_{poly}(S)
   \in
  dgcAlg^{\geq 0}_{\mathbb{Q}}
$$ 

for the [[polynomial differential forms]] with [[rational number|rational]] [[coefficients]] on $S$.

=--

([Bousfield-Gugenheim 76, def. 2.1](#BousfieldGugenheim76))


+-- {: .num_defn #SliceModelStructureOnAugmenteddgcalg}
###### Definition

Write $\mathbb{Q}[0] \coloneqq (\mathbb{Q}[0], d = 0)$ for the [[dgc-algebra]] concentrated on the [[ground field]] in degree 0, necessarily with vanishing [[differential]]. This is the [[initial object]] in $dgcAlg^{\geq 0}_{\mathbb{Q}}$.

Write

$$
  (dgcAlg^{\geq 0}_{\mathbb{Q}})_{/\mathbb{Q}[0]}
$$

for the [[slice category]] of that of all [[dgc-algebras]] (def. \ref{dgcAlgebras}) over $\mathbb{Q}[0]$. Hence an [[object]] in this category is a pair consisting of a [[dgc-algebra]] $A$ and a dg-algebra [[homomorphism]] of the form

$$
  \epsilon_A \;\colon\; A \longrightarrow \mathbb{Q}[0]
  \,.
$$


This is equivalently called a _$\mathbb{Q}[0]$-[[augmented algebra|augmented]] dgc-algebra_. The [[kernel]] of the augmentation map $\epsilon$
 
$$
  ker_{\epsilon_{A}} \in Ch^{\geq 0}_{\mathbb{Q}}
$$

is the _[[augmentation ideal]]_ of $(A,\epsilon)$.

Since $\mathbb{Q}[0] \in dgcAlg^{\geq 0}_{\mathbb{Q}}$ carries a unique augmentation $\epsilon = id$, we still write $\mathbb{Q}[0]$ for the [[ground field]] regarded as an augmented dgc-algebra. As such this is now a [[zero object]].


Furthermore write

$$
  \left(
   (dgcAlg^{\geq 0}_{\mathbb{Q}})_{/\mathbb{Q}[0]}
  \right)_{proj}
$$

for the [[slice model structure]] induced on this by the [[projective model structure on dgc-algebras]] according to prop. \ref{dgcAlgProjectiveModelStructure}.


=--

See also [Bousfield-Gugenheim 76, 4.11](#BousfieldGugenheim76)



## Statement 

We want to claim the following: 

For every $A \in dgcAlg^{\geq 0}_{\mathbb{Q}}$
there is a [[Quillen equivalence]]

$$
  SeqSpec\left(
    (A Mod^{\geq 0})^{op}_{proj}
  \right)_{stable}
    \underoverset
      {\underset{SeqSpec((Sym)^{op})}{\longrightarrow}}
      {
        \overset{SeqSpec( ker_{\epsilon(-)}^{op} )}{\longleftarrow}
      }
      {\simeq_{Qu}}
  SeqSpec\left(
    \left((dgcAlg^{\geq 0}_{A})_{/A}\right)^{op}_{proj}
  \right)_{stable}
$$

Idea of proof: the analogous statement for rational [[dgc-algebras]] $dgcAlg^{\geq 0}_{\mathbb{Q}}$ replaced by rational [[simplicial algebras]] $cAlg_{\mathbb{A}}^{\Delta^{op}}$ is [Schwede 97, theorem 3.2.3](#Schwede97). While $(dgcAlg^{\geq 0}_{\mathbb{Q}})_{proj}$ does not satisfy all the assumptions made in [Schwede 97](#Schwede97), we check that it satisfies enough properties for this proof still to go through.

Moreover, we want to claim there is n [[Quillen equivalence]]

$$
  (A Mod^{\bullet})_{proj}^{op}
    \underoverset
      {\underset{}{\longrightarrow}}
      {\overset{}{\longleftarrow}}
      {\simeq_{Qu}}
  SeqSpec\left(
    (A Mod^{\geq 0})_{proj}^{op}
  \right)_{stable}
$$


idea of proof: in the special case that $A = \mathbb{Q}[0]$ and dualizing, then this is part of [Shipley 02, prop 4.7](#Shipley02). The generalization should go through.

combined this gives the desired Quillen equivalence


$$
  (A Mod^{\bullet})_{proj}^{op}
    \underoverset
      {\underset{}{\longrightarrow}}
      {\overset{}{\longleftarrow}}
      {\simeq_{Qu}}
  SeqSpec\left(
    \left((dgcAlg^{\geq 0}_{A})_{/A}\right)^{op}_{proj}
  \right)_{stable}
$$

## Related concepts

* [[rational homotopy theory]]

* [[rational stable homotopy theory]]

* [[rational equivariant homotopy theory]]

* [[rational equivariant stable homotopy theory]] 

## References

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], V. K. A. M. Gugenheim, _On PL deRham theory and rational homotopy type_ , Memoirs of the AMS, vol. 179 (1976)


* {#Schwede97} [[Stefan Schwede]], section 3 of _Spectra in model categories and applications to the algebraic cotangent complex_, Journal of Pure and Applied Algebra 120 (1997) 104 ([pdf](http://www.math.uni-bonn.de/people/schwede/modelspec.pdf))

* {#Shipley02} [[Brooke Shipley]], _$H \mathbb{Z}$-algebra spectra are differential graded algebras_ , Amer. Jour. of Math. 129 (2007) 351-379. ([arXiv:math/0209215](http://arxiv.org/abs/math/0209215))


