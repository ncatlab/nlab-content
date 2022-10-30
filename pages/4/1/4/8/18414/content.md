
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Statement

A basic statement in [[homotopy theory]]:

+-- {: .num_prop}
###### Proposition

The [[fundamental group]] $\pi_1$ of the [[circle]] $S^1$ is the additive group of [[integers]]:


$$
  \pi_1(S^1) \overset{\simeq}{\longrightarrow} \mathbb{Z}
$$ 

and the isomorphism is given by assigning [[winding number]].

=--

Here in the context of [[topological homotopy theory]] the [[circle]] $S^1$ is the [[topological subspace]] $S^1 = \{x \in \mathbb{R}^2 \,\vert\, x_1^2 + x_2^2 = 1 \} \subset \mathbb{R}^2$ of the [[Euclidean plane]] with its [[metric topology]], or any [[topological space]] of the same [[homotopy type]]. More generally, the circle in question is, as a [[homotopy type]], the [[homotopy pushout]] 

$$
  S^1 \simeq \ast \underset{\ast \sqcup \ast}{\coprod} \ast
  \,,
$$

hence the [[homotopy type]] with the [[universal property]] that it makes a homotopy commuting diagram of the form

$$
  \array{
    \ast \sqcup \ast &\longrightarrow& \ast
    \\
    \downarrow &\swArrow& \downarrow
    \\
    \ast &\longrightarrow& S^1
  }
  \,.
$$

## Proofs


### In topological homotopy theory
 {#ProofInTopologicalHomotopyTheory}

We discuss the classical proof in [[topological homotopy theory]].

Let 

$$
  S^1 \coloneqq \{ x \in \mathbb{R}^2  \vert x^2 = 1\}
$$

be the topological [[circle]] equipped with its [[subspace topology]] of the [[Euclidean plane]] with its [[metric topology]].

Proof strategy:

1. The [[universal covering space]] $\widehat{S^1}$ of $S^1$ is the [[real line]] $\exp(2 \pi i(-)) \colon \mathbb{R}^1 \to S^1$;

1. the [[continuous functions]] $\mathbb{R}^1 \to \mathbb{R}^1$ which cover the projection $\exp(2\pi i(-))$ are translations by integers, hence

   $$
     Aut_{Cov(S^1)}( \widehat{S^1} ) \simeq \mathbb{Z}
   $$

1. the [[fundamental theorem of covering spaces]] gives

   $$
     \pi_1(S^1) \simeq Aut_{Cov(S^1)}( \widehat{S^1} )
     \,.
   $$

### In homotopy type theory
 {#ProofInHomotopyTypeTheory}

There is also a proof in [[homotopy type theory]] ([UF, corollary 8.1.10](#UF)).

## References

### In topological homotopy theory

Lecture notes on the classical discussion include

* {#Waldhausen} [[Friedhelm Waldhausen]], p. 63-77 of  _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

* {#Moller11} [[Jesper Møller]], theorem 3.1 in _The fundamental group and covering spaces_ (2011) ([pdf](http://www.math.ku.dk/~moller/f03/algtop/notes/covering.pdf))


### In homotopy type theory

The proof in [[homotopy type theory]] is discussed in

* [[Daniel Licata]], [[Michael Shulman]], _Calculating the Fundamental Group of the Circle in Homotopy Type Theory_,  ([arXiv:1301.3443](https://arxiv.org/abs/1301.3443))
 
* {#UF} [[UF-IAS-2012|Univalent Foundations Project]], section 8.1 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

the HoTT-[[Coq]]-code is at

* {#Shulman} [[Mike Shulman]], _[P1S1.v](https://github.com/HoTT/HoTT/blob/master/Coq/HIT/Pi1S1.v)_
