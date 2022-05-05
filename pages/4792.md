
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

<img src="https://ncatlab.org/nlab/files/OctonionMultiplicationTable.jpg" width="400" alt="octonion multiplication table">

> (graphics grabbed from [Baez 02](#Baez02))

=--


+-- {: .num_example #ProductOfImaginaryOctonions}
###### Example

The product of all the imaginary quaternions with each other, bracketed to the left, is

$$
  e_1 e_2 e_3 e_4 e_5 e_6 e_7
  \;=\;
  -1
$$

=--

+-- {: .proof}
###### Proof

By iteratively using the multiplication table in def. \ref{ComponentDefinition} we obtain:

$$
  \begin{aligned}
    & \underset{e_4}{\underbrace{e_1 e_2}} e_3 e_4 e_5 e_6 e_7
    \\
    & = \underset{- e_6}{\underbrace{e_4 e_3}} e_4 e_5 e_6 e_7
    \\
    & = - \underset{-e_3}{\underbrace{ e_6 e_4 }} e_5 e_6 e_7
    \\
    & = + \underset{e_2}{\underbrace{ e_3 e_5 }} e_6 e_7
    \\
    & = + \underset{ e_7 }{\underbrace{ e_2 e_6 }} e_7
    \\
    & = e_7 e_7 
    \\
    & = - 1
  \end{aligned}
$$

=--


## Properties

### General

* The octonions are _not_ an [[associative algebra]]. The _non-zero_ octonions and the _unit_ octonions form [[Moufang loops]].

* The [[automorphism group]] of the octonions is [[G2]].

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

A survey is in

* {#Baez02} [[John Baez]], _The Octonions_,  Bull. Amer. Math. Soc. 39 (2002), 145-205. ([web](http://math.ucr.edu/home/baez/octonions/octonions.html)) 

The concept of "special triples" or ("basic triples") used above seems to go back to 

* {#Whitehead71} [[George Whitehead]], appendix A in _Homotopy Theory_, MIT press 1971

[[!redirects octonion]]
[[!redirects octonions]]
[[!redirects octonion algebra]]
