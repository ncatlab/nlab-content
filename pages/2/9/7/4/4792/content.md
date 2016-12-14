
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The __octonions__, usually denoted $\mathbb{O}$, form the largest of the four [[normed division algebras]] over the [[real numbers]].

## Definition

+-- {: .num_defn}
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

## Properties

### Non-associativity

The octonions are _not_ an [[associative algebra]]. The _non-zero_ octonions and the _unit_ octonions form [[Moufang loops]].

### Automorphisms

The [[automorphism group]] of the octonions is [[G2]].

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


## Related concepts

* [[associative 3-form]]

* [[Fano plane]]

* [[Cayley plane]]

* [[octonionic Hopf fibration]]

[[!include exceptional spinors and division algebras -- table]]


## References

A survey is in

* {#Baez02} [[John Baez]], _The Octonions_,  Bull. Amer. Math. Soc. 39 (2002), 145-205. ([web](http://math.ucr.edu/home/baez/octonions/octonions.html)) 

The concept of "special triples" or ("basic triples") used above seems to go back to 

* {#Whitehead71} [[George Whitehead]], appendix A in _Homotopy Theory_, MIT press 1971

[[!redirects octonion]]
[[!redirects octonions]]
[[!redirects octonion algebra]]
