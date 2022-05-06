
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

An _octonion_ or _Cayley number_ is a kind of [[number]] similar to a [[quaternion number]] but with seven instead of just three [[square roots]] of unity adjoined, and satisfying certain relations.

The __octonions__, usually denoted $\mathbb{O}$, form the largest of the four [[normed division algebras]] over the [[real numbers]].

## Definition

+-- {: .num_defn #ComponentDefinition}
###### Definition

The _octonions_ $\mathbb{O}$ is the [[nonassociative algebra]] over the [[real numbers]] which is [[generators and relations|generated]] from seven generators $\{e_1, \cdots, e_7\}$ subject to the [[generators and relations|relations]]

1. for all $i$ 

   $e_i^2 = -1$

1. for $e_i \to e_j \to e_k$ an edge or circle in the following diagram (a labeled version of the [[Fano plane]]) the relations
 
   1. $e_i e_j  = e_k$ 

   1. $e_j e_i  = -e_k$

{#FanoPlaneDiagram} $\,$

<img src="https://ncatlab.org/nlab/files/OctonionMultiplicationTable.jpg" width="400" alt="octonion multiplication table">

> (graphics grabbed from [Baez 02](#Baez02))

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

* [[split octonion]]

[[!include exceptional spinors and division algebras -- table]]


## References

Textbook account:

* {#SpringerVeltkamp00} [[Tonny Springer]], [[Ferdinand Veldkamp]], _Octonions, Jordan Algebras, and Exceptional Groups_, Springer Monographs in Mathematics, 2000


A survey is in

* {#Baez02} [[John Baez]], _The Octonions_,  Bull. Amer. Math. Soc. 39 (2002), 145-205. ([web](http://math.ucr.edu/home/baez/octonions/octonions.html)) 

The concept of "special triples" or ("basic triples") used above seems to go back to 

* {#Whitehead71} [[George Whitehead]], appendix A in _Homotopy Theory_, MIT press 1971

Relation to the [[Leech lattice]]:

* {#Wilson09} [[Robert A. Wilson]], _Octonions and the Leech lattice_, Journal of Algebra
Volume 322, Issue 6, 15 September 2009, Pages 2186-2190, ([pdf](http://www.maths.qmul.ac.uk/~raw/pubs_files/octoLeech1.pdf), [slides](http://www.maths.qmul.ac.uk/~raw/talks_files/Cambridge09.pdf))

[[!redirects octonion]]
[[!redirects octonions]]
[[!redirects octonion algebra]]
