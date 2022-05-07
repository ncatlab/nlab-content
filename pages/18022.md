
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
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

It is a classical fact that the [[rationalization]] of classical [[homotopy theory]] (of [[topological spaces]] or [[simplicial sets]]) -- called _[[rational homotopy theory]]_ -- is considerably more tractable than general [[homotopy theory]], as exhibited by the existence of small concrete [[dg-algebra|dg-algebraic]] models for [[rational homotopy types]]: [[minimal Sullivan algebras]] or equivalently their [[dual]] [[dg-coalgebras]]. A similar statement holds for the rationalization of [[stable homotopy theory]] i.e. the [[homotopy theory]] of [[spectra]] (of [[topological spaces]] or [[simplicial sets]]): rational spectra are equivalent to rational [[chain complexes]], i.e. to [[dg-modules]] over $\mathbb{Q}$. This is a dg-model for _[[rational stable homotopy theory]]_ compatible with that of classical rational homotopy theory in tat the [[stabilization]] adjunction that connects classical [[homotopy theory]] to [[stable homotopy theory]] is, under these identifications, modeled by the [[forgetful functor]] from dg-(co-)algebras to [[chain complexes]]

$$
  \array{
    & \text{classical homotopy theory}
     &&
    \text{stable homotopy theory}
    \\
    & spaces & \underoverset{\underset{\Sigma^\infty}{\longrightarrow}}{\overset{\Omega^\infty}{\longleftarrow}}{} & spectra
    \\
    & & \text{stabilization}
    \\
    \text{rationally}
    &
    \text{dg(co)algebras}
    &
     \underoverset{\underset{underlying}{\longrightarrow}}{\overset{free}{\longleftarrow}}{}
    &
    \text{chain complexes}
  }
$$


Classical [[homotopy theory]] and [[stable homotopy theory]] are unified and jointly generalized in [[parameterized stable homotopy theory]], whose [[objects]] are [[parameterized spectra]], parameterized over a classical [[homotopy type]]. The _rational parameterized stable homotopy theory_ to be discussed here is supposed to be the rationalization of this joint generalization, unifiying and jointly generalizing the algebraic model of [[rational topological spaces]] by [[Sullivan algebras]] and of $H \mathbb{Q}$-[[module spectra]] by [[chain complexes]].

$$ 
  \array{
    & \text{stable homotopy theory}
    && 
    \text{parameterized stable homotopy theory}
    &&
    \text{classical homotopy theory}
    \\
    &
    \text{spectra}
     &\overset{\phantom{\text{include}}}{\longrightarrow}&
    \text{parameterized spectra}
     &\overset{\phantom{\text{project}}}{\longrightarrow}&
    \text{spaces}
    \\
    &
    &\text{include}&
    &\text{project}&
    \\
    \text{rationally}
    &
    \text{chain complexes}
    &\overset{\phantom{\text{include}}}{\longrightarrow}&
    \text{dg-modules}
    &\overset{\phantom{\text{project}}}{\longrightarrow}&
    \text{dg(co)algebras}
  }
$$

Here we (intend to) show that, accordingly, rational parameterized homotopy theory is presented by the the [[opposite category|opposite]] of the [[homotopical category]] of [[dg-modules]] over cochain [[differential graded-commutative algebras]] in non-negative degrees. 

> under construction


## Preliminaries


### Chain complexes

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



### dg-Algebras

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

### Simplicial Lie algebras

$$
  (LieAlg_k)^{\Delta^{op}}_{proj}
    \underoverset
      {\underset{N}{\longrightarrow}}
      {\overset{N^\ast}{\longleftarrow}}
      {\bot}
  (dgLieAlg_k)_{proj}
    \underoverset
      {\underset{CE}{\longrightarrow}}
      {\overset{\mathcal{L}}{\longleftarrow}}
      {\bot}
  dgcoAlg_k
$$

(...)


## Statement 

We want to claim the following: 

For every $\mathfrak{g} \in (LieAlg_{\mathbb{Q}})^{\Delta^{op}}$
there is a [[Quillen equivalence]]

$$
  SeqSpec\left(
    \mathfrak{g}Mod
  \right)_{stable}
    \underoverset
      {\underset{SeqSpec((Sym)^{op})}{\longrightarrow}}
      {
        \overset{SeqSpec( ker_{\epsilon(-)}^{op} )}{\longleftarrow}
      }
      {\simeq_{Qu}}
  SeqSpec\left(
    \mathfrak{g} / (LieAlg_{\mathbb{Q}})^{\Delta^{op}} / \mathfrak{g}
  \right)_{stable}
$$

Idea of proof: the analogous statement for simplicial Lie algebras replaced by rational [[simplicial algebras]] $cAlg_{\mathbb{A}}^{\Delta^{op}}$ is [Schwede 97, theorem 3.2.3](#Schwede97). Apart from the connectivity of the $Sym$-construction, all that this proof uses is that simplicial commutative algebras form a [[proper model category|right proper]] [[simplicial model category]]. But also the [[model structure on simplicial Lie algebras]] is right proper and simplicial.



## Related concepts

* [[rational model for a suspension]]

* [[rational homotopy theory]]

* [[rational stable homotopy theory]]

* [[rational parametrized homotopy theory]]

* [[rational equivariant homotopy theory]]

* [[rational equivariant stable homotopy theory]] 

## References

A classical reference on plain [[rational homotopy theory]] is

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], V. K. A. M. Gugenheim, _On PL deRham theory and rational homotopy type_ , Memoirs of the AMS, vol. 179 (1976)

The equivalence between $H R$-module spectra (unparametrized) and $R$-chain complexes is due to

* {#Schwede97} [[Stefan Schwede]], section 3 of _Spectra in model categories and applications to the algebraic cotangent complex_, Journal of Pure and Applied Algebra 120 (1997) 104 ([pdf](http://www.math.uni-bonn.de/people/schwede/modelspec.pdf))

* {#Shipley02} [[Brooke Shipley]], _$H \mathbb{Z}$-algebra spectra are differential graded algebras_ , Amer. Jour. of Math. 129 (2007) 351-379. ([arXiv:math/0209215](http://arxiv.org/abs/math/0209215))

Discussion of rational fiberwise [[suspension spectra]] is in

* Michael Charles Crabb, [[Ioan James]], around Prop. 15.8 of _Fibrewise Homotopy Theory_, Springer Monographs in Mathematics, 1998

* [[Yves Félix]], Aniceto Murillo [[Daniel Tanré]], _Fibrewise stable rational homotopy_, Journal of Topology, Volume 3, Issue 4, 2010, Pages 743–758 ([doi:10.1112/jtopol/jtq023]( https://doi.org/10.1112/jtopol/jtq023))


A discussion of full-blown rational parametrized stable homotopy theory is due to

* [[Vincent Braunack-Mayer]], _[[schreiber:thesis Braunack-Mayer|Rational parameterized stable homotopy theory]]_, Zurich, 2018
  
* [[Vincent Braunack-Mayer]], _Strict algebraic models for rational parametrised spectra I_,  Algebraic & Geometric Topology 21 (2021) 917–1019 ([arXiv:1910.14608](https://arxiv.org/abs/1910.14608), [doi:10.2140/agt.2021.21.917](https://doi.org/10.2140/agt.2021.21.917))

Application to mathematical analysis of [[duality between M-theory and type IIA string theory]]:

* [[Vincent Braunack-Mayer]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Gauge enhancement of Super M-Branes|Gauge enhancement of Super M-Branes rational parameterized stable homotopy theory]]_, Communications in Mathematical Physics 371: 197 (2019) ([arXiv:1806.01115](https://arxiv.org/abs/1806.01115), [doi:10.1007/s00220-019-03441-4](https://doi.org/10.1007/s00220-019-03441-4))


* [[Vincent Braunack-Mayer]], _[[schreiber:Parametrised homotopy theory and gauge enhancement]]_, talk at _[Higher Structures in M-Theory](http://www.maths.dur.ac.uk/lms/109/index.html)_ Durham Symposium 2018 , Fortschritte der Physik (2019) ([doi:10.1002/prop.201910003](https://onlinelibrary.wiley.com/doi/abs/10.1002/prop.201910003)m [arXiv:1903.02862](https://arxiv.org/abs/1903.02862))

  



[[!redirects rational parametrized stable homotopy theory]]

[[!redirects parametrized rational stable homotopy theory]]


