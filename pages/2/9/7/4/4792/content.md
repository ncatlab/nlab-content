
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Exceptional structures
+-- {: .hide}
[[!include exceptional structures -- contents]]
=--
=--
=--

# Octonions
* table of contents
{: toc}

## Idea

The _octonions_ or _Cayley numbers_ $\mathbb{O}$ ([Cayley 1845](#Cayley1845)) is a [[non-associative algebra|non-associative]] [[real numbers|real]] [[star-algebra]] similar to the [[complex numbers]] and the [[quaternions]] but with seven [[imaginary number|imaginary]] [[units]] adjoined, satisfying certain relations: 

The octonions arise from the [[quaternions]] in analogy -- namely: by the [[Dickson double construction]] ([Dickson 1919, (6)](#Dickson1919)) -- of how the [[quaternions]] arise from the [[complex numbers]], and the [[complex numbers]] from the [[real numbers]]. These are precisely the [[normed division algebras]] over the [[real numbers]], the octonions being the largest of the four. While the further [[Dickson double]] of the quaternions exists, called the _[[sedenions]]_, it is no longer a [[normed division algebra]].

In continuation of how the [[complex numbers]] and [[quaternions]] control [[spin groups]], [[real spin representations]] and [[supersymmetry]] up to [[dimension]] 7, the octonions control these up to the maximal dimension 11:

[[!include exceptional spinors and division algebras -- table]]

For more on this see at _[[supersymmetry and division algebras]]_.

Generally, the algebra of octonions shows up, in one way or another, behind most, if not all, [[exceptional structures]] in [[group theory]], [[Lie theory]] and [[differential geometry]]. See also at _[[universal exceptionalism]]_ for more on this.

## Definition

The following definition is in the style of [Dickson 1919](#Dickson1919), [Baez 02, second half of Section 2.2](#Baez02):

+-- {: .num_defn #QuaternionCompatibleComponentDefinition}
###### Definition

The _octonions_ $\mathbb{O}$ are the elements of the [[nonassociative algebra|non-associative]] [[star-algebra]] over the [[real numbers]] which is the [[Cayley-Dickson double]] of the [[star-algebra]] of [[quaternions]] $\mathbb{H}$ (with $\overline{(-)}$ denoting the conjugation-operation).



This means (see [there](Cayley-Dickson+construction#DefinitionByGeneratorsAndRelations)) that if $i, j, k \in \mathbb{H}$ denote an [[orthonormal basis]] of [[imaginary number|imaginary]] unit-[[quaternions]]

\begin{imagefromfile}
    "file_name": "QuaternionOctonionMultiplicationTableII.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": ""
\end{imagefromfile}


$$
  \begin{aligned}
     & i^2 = j^2 = k^2 = -1
     \\
     &
     i j = k, \, j i = - k \;\;\;\text{and cyclic}
  \end{aligned}
$$

then the algebra $\mathbb{O}$ of octonions is [[generators and relations|generated]] from these $i, j , k$ and from one more element $\ell$, subject to these [[generators and relations|relations]]:

$$
  \begin{aligned}
  \ell^2 \;=\; -1
  \,,
  \phantom{AAA}
  \overline{\ell}
  \;=\;
  - \ell
  \end{aligned}
$$

and

$$
  \begin{aligned}
  q (\ell q') 
  = 
  \ell (\overline{q} q')
  \\
  (q \ell) q' 
  = 
  (q \overline{q}') \ell
  \\
  (\ell q) (q' \ell)
  = 
  - \overline{q q'}
  \end{aligned}
$$

for all [[quaternions]] $q_1, q_2 \in \mathbb{H}$.

This gives the multiplication table on the right, where any two consecutive arrows $a \to b \to c$ mean that $a b = c$, $c a = b$, $b c = a$ and $b a = -c$.

=--

+-- {: .num_example #FixedLocusOfe4e5e6e7}
###### Example

The following computation shows the operation of consecutive left multiplication by the generators $\mathrm{e}_4$, $\mathrm{e}_5$, $\mathrm{e}_6$ $\mathrm{e}_7$ (according to Def. \ref{QuaternionCompatibleComponentDefinition}) on any octonion
$x = q + p \ell$ ($q,p \in \mathbb{H}$) is by reversal of the sign of the $\ell$-component, hence has as [[fixed point|fixed]] [[linear subspace]] the [[quaternions]] (see [HSS 18, Lemma 4.13](#HSS18) for application of this fact to [[M-branes]]):

$$
  \begin{aligned}
    \mathrm{e}_4
    \Big(
    \mathrm{e}_5
    \big(
      \mathrm{e}_6
      (\mathrm{e}_7 x)
    \big)
    \Big)
    & =
    \ell
    \bigg(
    (i \ell)
    \Big(
      (j \ell)
      \big(
        (k \ell)
        x
      \big)
    \Big)
    \bigg)
    \\
    & =
    \ell
    \bigg(
    (i \ell)
    \Big(
      (j \ell)
      \big(
        (k \overline{x})
        \ell
      \big)
    \Big)
    \bigg)
    \\
    & =
    \ell
    \Big(
      (i \ell)
      \big(
        (x k) j
      \big)
    \Big)
    \\
    & =
    \ell
    \bigg(
      \Big(
        i
        \big(
          j
          (k \overline{x}
        \big)
      \Big)
    \ell
    \bigg)
    \\
    & =
    \big(
      (
       \underset{
         \mathclap{
           q + p \ell
         }
       }{
         \underbrace{
           x 
         }
       }
      k)
      j
    \big)
    i
    \\
    & =
    q k j i
    + 
    \Big(
      \big( 
        (q \ell) k
      \big) 
      j
    \Big) 
    i
    \\
    & = 
    q
    \underset{
      = 1
    }{ 
    \underbrace{
      k j i
    }
    }
    -
    (p
      \underset{
        = 1
      }{
        \underbrace{
          k j i
        }
      }
    ) \ell
    \\
    & =
    q - p \ell
    \,.
  \end{aligned}
$$

=--



\linebreak

\linebreak

Of course the labels of the generators is not fixed. Here is another version:


+-- {: .num_defn #ComponentDefinition}
###### Definition

The _octonions_ $\mathbb{O}$ is the [[nonassociative algebra]] over the [[real numbers]] which is [[generators and relations|generated]] from seven generators $\{e_1, \cdots, e_7\}$ subject to the [[generators and relations|relations]]

1. for all $i$ 

   $e_i^2 = -1$

1. for $e_i \to e_j \to e_k$ an edge or circle in the following diagram (a labeled version of the [[Fano plane]]) the relations
 
   1. $e_i e_j  = e_k$ 

   1. $e_j e_i  = -e_k$

{#FanoPlaneDiagram} $\,$


\begin{imagefromfile}
    "file_name": "OctonionMultiplicationTable.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "graphics from [Baez 02](#Baez02)"
\end{imagefromfile}

This becomes a [[star-algebra]] with star [[involution]]

\[
  \label{StarInvolution}
  \overline{(-)} \;\colon\; \mathbb{O} \longrightarrow \mathbb{O}
\]

which is the [[antihomomorphism]] $\overline{a b} = \overline{b} \overline{a}$ that is  given on the above generators by

$$
  \overline{e_i} \coloneqq - e_i 
  \phantom{AAAA}
  i \in \{1, \cdots, 7\}
 \,.
$$

=--

+-- {: .num_example #ProductOfImaginaryOctonions}
###### Example

The product of all the generators with each other, bracketed to the right, is

$$
  e_7 (e_6 (e_5 (e_4 (e_3 ( e_2 (e_1 1 ))))))
  \;=\;
  + 1
$$

=--

+-- {: .proof}
###### Proof

By iteratively using the multiplication table in def. \ref{ComponentDefinition} we compute as follows:


$$
  \begin{aligned}
   & e_7 (e_6 (e_5 (e_4 (e_3 (\underset{-e_4}{\underbrace{e_2 e_1}})))))
   \\
   & =
   - e_7 (e_6 (e_5 (e_4 (\underset{e_6}{\underbrace{e_3 e_4}}))))
   \\
   & =
   - e_7 (e_6 (e_5 (\underset{e_3}{\underbrace{e_4 e_6}})))
   \\
   & =
   - e_7 (e_6 (\underset{-e_2}{\underbrace{e_5 e_3}}))
   \\
   & =
   + e_7 (\underset{-e_7}{\underbrace{e_6 e_2}})
   \\
   & =
   - \underset{= -1}{\underbrace{e_7 e_7}}
   \\
   & =
   + 1
  \end{aligned}
$$

=--


+-- {: .num_defn #RealAndImaginary}
###### Definition
**(real and imaginary octonions)**

As for the [[complex numbers]] one says that 

* an _imaginary octonion_ is an $a \in \mathbb{O}$ shuch that under the star involution (eq:StarInvolution) it is sent to its negative:

  $$
    \overline{a} = -a
  $$

* a _real octonions_ is an $a \in \mathcal{O}$ shuch that under the star involution (eq:StarInvolution) it is sent to itself

  $$
    \overline{a} = a
  $$

Accordingly every octonion decomposes into a [[real part]] and an [[imaginary part]]:

$$
  Re(a) \coloneqq \tfrac{1}{2}(a + \overline{a})
  \phantom{AA}
  Im(a) \coloneqq \tfrac{1}{2}(a - \overline{a})
  \,.
$$

=--


## Properties

### General

+-- {: .num_prop}
###### Proposition

The octonions are _not_ an [[associative algebra]]. But the _non-zero_ octonions and the _unit_ octonions form [[Moufang loops]].

=--

+-- {: .num_prop #Alternativity}
###### Proposition
**(octonions are alternative)**

The octonions form an [[alternative algebra]]

=--

+-- {: .proof}
###### Proof

By linearity it is sufficient to check this on generators.
So let $e_i \to e_j \to e_k$ be a circle or a cyclic permutation of an edge in the [[Fano plane]] as in Def. \ref{ComponentDefinition}.
Then by definition of the octonion multiplication we have

$$
  \begin{aligned}
    (e_i e_j) e_j
    &=
    e_k e_j
    \\
    &=
    - e_j e_k
    \\
    & =
    -e_i
    \\
    & =
    e_i (e_j e_j)
  \end{aligned}
$$

and similarly

$$
  \begin{aligned}
    (e_i e_i ) e_j
    &=
    - e_j
    \\
    &=
    - e_k e_i
    \\
    &=
    e_i e_k
    \\
    &=
    e_i (e_i e_j)
  \end{aligned}
  \,.
$$

=--

### Automorphisms

+-- {: .num_prop #AutomorphismsOfOctonionAlgebraIsG2}
###### Proposition

The [[automorphism group]] of the octonions, as a real algebra, is the [[exceptional Lie group]] [[G2]].

=--

See also at _[normed division algebra -- automorphism](normed+division+algebra#Automorphisms)_


### Left multiplication by imaginary octonions


+-- {: .num_defn #LeftMultiplicationAction}
###### Definition

Given any octonion $o$, then the operation of left multiplication by $o$

$$
  \array{
    \mathbb{O} &\overset{L_o}{\longrightarrow}& \mathbb{O}
    \\
    a &\mapsto& o a
  }
$$

is an $\mathbb{R}-$[[linear map]]. Under [[composition]] of linear maps, this defines an _[[associativity|associative]]_ [[monoid]] [[action|acting]] linearly on $\mathbb{O}$.

=--


+-- {: .num_prop #CliffordActionOfImaginaryOctonions}
###### Proposition
**(Clifford action of imaginary octonions)**

Consider the [[Clifford algebra]]

$$
  Cl(Im(\mathbb{O}), -{\vert -\vert}^2)
$$

on the underlying [[real vector space]] of that of the imaginary octonions (Def. \ref{RealAndImaginary}) regarded as an [[inner product space]] via the [[quadratic form]] given by the _negative_ square norm.

Then the operation of left multiplication on $\mathbb{O}$ (def. \ref{LeftMultiplicationAction}) induces a [[representation]] of this Clifford algebra on $\mathbb{R}^8 \simeq_{\mathbb{R}} \mathbb{O}$.


=--

+-- {: .proof}
###### Proof

By [[alternative algebra|alternativity]] (Prop. \ref{Alternativity}) we have for every $v \in Im(\mathbb{O})$ and every $a \in \mathbb{O}$

$$
  \begin{aligned}
    L_v L_v (a)
    & \coloneqq
    v (v a)
    \\
    & =
    (v v) a 
    \\
    & =
    - {\vert v\vert}^2 a
    \\
    & =
    L_{- {\vert v\vert}^2} (a)
  \end{aligned}
$$

=--

+-- {: .num_prop #ConsecutiveLeftActionByImaginaryGenerators}
###### Proposition
**(consecutive left action by imaginary generators is unity)**

The consecutive left multiplication action (Def. \ref{LeftMultiplicationAction}) by all the imaginary octonion generators $e_i$ (Def. \ref{ComponentDefinition}) is $\pm$ the [[identity function]] on the octonions. Specifically, if one acts in increasing order of the labels in Def. \ref{ComponentDefinition}, then it is +1:

$$
  L_{e_7} L_{e_6} L_{e_5} L_{e_4} L_{e_3} L_{e_2} L_{e_1}
  \;=\;
  + Id_{\mathbb{O}}
$$ 

=--

+-- {: .proof}
###### Proof

All the generators $e_i$ are imaginary octonions (Def. \ref{RealAndImaginary}). By Prop. \ref{CliffordActionOfImaginaryOctonions} their left action on $\mathbb{O}$ [[representation|represents]] a [[Clifford algebra]]-action of $Cl(Im(\mathbb{O}), -{\vert-\vert}^2) \simeq Cl_{0,7}$ on $\mathbb{R}^{8} \simeq_{\mathbb{R}} \mathbb{O}$.

By the [classification of real Clifford algebras](Clifford+algebra#ClassificationOverTheRealNumbers), $Cl_{0,7}$ has, up to [[isomorphism]], two different [[irreducible representation|irreducible]] [[modules]]. Their underlying vector space is $\mathbb{R}^8$ in both cases, and so the left action of imaginary octonions we have must be one of the two. The two irreps may be distinguished by the action of the "volume element" $\Gamma_7 \Gamma_6 \cdots \Gamma_1$: On one of the two it acts as the identity, on the other as minus the identity.

Hence we may check the remaining sign by acting on any one octonion, for instance on the unit $1 \in \mathbb{O}$. Then the claim follows with the computation in Example \ref{ProductOfImaginaryOctonions}:

$$
  \begin{aligned}
    L_{e_7} L_{e_6} L_{e_5} L_{e_4} L_{e_3} L_{e_2} L_{e_1} (1)
    & =
    e_7 (e_6 (e_5 (e_4 (e_3 ( e_2 (e_1 1 ))))))
    \\
    & =
    + 1
    \,.
  \end{aligned}
$$



=--



### Basic triples
 {#ElementaryTriples}

+-- {: .num_defn #BasicTriple}
###### Definition

A _special triple_ or _basic triple_ is a [[triple]] $(e_1, e_2, e_3) \in \mathbb{O}^3$ of three octonions such that

* $e_i^2 = -1$

* $e_i e_j = - e_j e_i$.

=--

([Whitehead 71, p. 691](#Whitehead71))

+-- {: .num_remark}
###### Remark

The choice of $e_1$ identifies an inclusion of the [[complex numbers]] $\mathbb{R} \hookrightarrow \mathbb{C} \hookrightarrow \mathbb{O}$.

Then the choice of $e_2$ on top of that identifies a compatible inclusion of the [[quaternions]] $\mathbb{R} \hookrightarrow \mathbb{C}\hookrightarrow \mathbb{H} \hookrightarrow \mathbb{O}$.

Finally the choice of $e_3$ on top of that induces a basis for all of $\mathbb{O}$.

=--

+-- {: .num_prop #BasicTriplesFormAutomorphism}
###### Proposition

The set of basic triples, def. \ref{BasicTriple}, forms a [[torsor]] over the [[automorphism group]] [[G2]] $= Aut(\mathbb{O})$.

=--

(e.g. [Baez 02, 4.1](#Baez02))

### Relation to quaternions


+-- {: .num_prop #InvolutionProjectingOutH}
###### Proposition

Let 

$$
  \mathbb{H} = \langle 1, i, j, k\rangle
$$ 

be the [[quaternions]] equipped with canonical [[linear basis|basis]] elements, and let 

\[
  \label{ForProjectionStatementOcotonionsDirectSumUnderCayleyDickson}
  \mathbb{O} = \mathbb{H} \oplus \ell \mathbb{H}
\]

be the octonions equipped with the linear basis induced by the [[Cayley-Dickson construction]] (via [this def.](Cayley-Dickson+construction#CayleyDicksonDoubleByAdjoiningFurtherGenerator)). 

Then the linear map 

$$
  L_{\ell} L_{\ell i} L_{\ell j} L_{\ell k}
  \;\colon\;
  \mathbb{O} \longrightarrow \mathbb{O}
$$

is an [[involution]] whose +1 [[eigenspace]] is $\ell \mathbb{H}$ and whose -1 eigenspace is $\mathbb{H}$, under the above identification (eq:ForProjectionStatementOcotonionsDirectSumUnderCayleyDickson).

(Here $L_{(-)}$ denotes the linear map on $\mathbb{O}$ given by left multiplication in $\mathbb{O}$.)

=--

+-- {: .proof}
###### Proof

We use the Cayley-Dickson relations ([this def.](Cayley-Dickson+construction#CayleyDicksonDoubleByAdjoiningFurtherGenerator))

$$
  a (\ell b) = \ell (\overline{a} b)
  \,,
  \phantom{AA}
  a(\ell b) = (a \overline{b}) \ell
  \,,
  \phantom{AA}
  (\ell a) (b \ell^{-1}) = \overline{a b}
$$

that hold in $\mathbb{O}$ for all $a,b \in \mathbb{H}$, as well as

$$
  \ell e = - e \ell
$$

for all imaginary elements $e \in \mathbb{H}$.

With this we compute

$$
  \begin{aligned}
    & L_{\ell} L_{\ell i} L_{\ell j} L_{\ell k} ( a)
    \\
    & =  \ell( (\ell i) ( (\ell j) ( (\ell k) a ) ) )
    \\
    & = - \ell( (\ell i) ( (\ell j) ( (k \ell) a ) ) )
    \\
    & = - \ell( (\ell i) ( (\ell j) ( (k \overline{a}) \ell ) ) )
    \\
    & = + \ell( (\ell i) ( (\ell j) ( (k \overline{a}) \ell^{-1} ) ) )
    \\
    & = + \ell( (\ell i) ( \overline{j (k \overline{a})} ) )
    \\
    & = + \ell( (\ell i) ( \overline{i \overline{a}} ) )
    \\
    & = - \ell( (i \ell) ( \overline{i \overline{a}} ) )
    \\
    & = - \ell( ( i i \overline{a}  ) \ell )
    \\
    & = + \ell( \overline{a}  \ell )
    \\
    & = - \ell( \overline{a} \ell^{-1} )
    \\
    & = - a
  \end{aligned}
$$

and

$$
  \begin{aligned}
    & L_{\ell} L_{\ell i} L_{\ell j} L_{\ell k} ( \ell a)
    \\
    & = \ell( (\ell i) ( (\ell j) ( (\ell k) (\ell a) ) ) )
    \\
    & =
      \ell( (\ell i) ( (\ell j) ( (\ell k) ( \overline{a} \ell) ) ) )
    \\
    & =
      -
      \ell( (\ell i) ( (\ell j) ( \overline{k {\overline{a}}} ) ) )
    \\
    & =
      + \ell( (\ell i) ( (j \ell) ( \overline{k {\overline{a}}} ) ) )
    \\
    & =
      + \ell( (\ell i) ( (j k {\overline{a}}) \ell ) )
    \\
    & =
      - \ell( (\ell i) ( (j k {\overline{a}}) \ell^{-1} ) )
    \\
    & =
      - \ell( \overline{ i j k {\overline{a}} } )
    \\
    & =
      + \ell( \overline{ {\overline{a}} } )
    \\
    & =
      + \ell a 
  \end{aligned}
$$

=--



## Related concepts

* [[associative 3-form]]

* [[Fano plane]]

* [[Cayley plane]]

* [[octonionic Hopf fibration]]

* [[octonionic projective space]]

* [[split octonion]]

[[!include exceptional spinors and division algebras -- table]]


## References

### General

The definition is originally due to 

* {#Cayley1845} [[Arthur Cayley]], _On certain results relating to quaternions_,  The London, Edinburgh, and Dublin Philosophical Magazine and Journal of Science Series 3 Volume 26, 1845 - Issue 171 ([doi:10.1080/14786444508562684](https://doi.org/10.1080/14786444508562684))

The formulation as the [[Dickson double construction]] is due to

* {#Dickson1919} [[Leonard Dickson]], _On Quaternions and Their Generalization and the History of the Eight Square Theorem_, 
Annals of Mathematics, Second Series, Vol. 20, No. 3 (Mar., 1919), pp. 155-171 ([jstor:1967865](https://www.jstor.org/stable/1967865))

Review:

* {#Baez02} [[John Baez]], _The Octonions_,  Bull. Amer. Math. Soc. 39 (2002), 145-205. ([web](http://math.ucr.edu/home/baez/octonions/octonions.html), [pdf](http://math.ucr.edu/home/baez/octonions/octonions.pdf) [doi:10.1090/S0273-0979-01-00934-X](https://doi.org/10.1090/S0273-0979-01-00934-X)) 

Textbook accounts:

* {#SpringerVeltkamp00} [[Tonny Springer]], [[Ferdinand Veldkamp]], _Octonions, Jordan Algebras, and Exceptional Groups_, Springer Monographs in Mathematics, 2000 ([doi:10.1007/978-3-662-12622-6](https://doi.org/10.1007/978-3-662-12622-6))

* [[Tevian Dray]], [[Corinne Manogue]], _The Geomety of Octonions_, World Scientific 2015 ([doi:10.1142/8456](https://doi.org/10.1142/8456))

The concept of "special triples" or ("basic triples") used above seems to go back to 

* {#Whitehead71} [[George Whitehead]], appendix A in _Homotopy Theory_, MIT press 1971

Relation to the [[Leech lattice]]:

* {#Wilson09} [[Robert A. Wilson]], _Octonions and the Leech lattice_, Journal of Algebra
Volume 322, Issue 6, 15 September 2009, Pages 2186-2190, ([pdf](http://www.maths.qmul.ac.uk/~raw/pubs_files/octoLeech1.pdf), [slides](http://www.maths.qmul.ac.uk/~raw/talks_files/Cambridge09.pdf))

### Relation to 10d/11d spin geometry 

Application of [[octonion]]-algebra to analysis of [[spin representations]] and [[spin geometry]] specifically in 11d (for general discussion in other dimensions see at _[[supersymmetry and division algebras]]_):

* {#HSS18} [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_, Comm. Math. Phys. 371: 425. (2019) ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))


[[!redirects octonion]]
[[!redirects octonions]]
[[!redirects octonion algebra]]
