
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

Let $G$ be a [[group]]. For the following this is often assumed to be (though is not necessarily) an [[abelian group]]. Hence we write here the group operation with a plus-sign

$$
  + : G \times G \to G
  \,.
$$

For $\mathbb{N}$ the [[natural numbers]], there is a [[function]]

$$
  (-)\cdot (-) : \mathbb{N} \times G \to G
$$

which takes a group element $g$ to 

$$
  n \cdot g \coloneqq \underbrace{g + g + \cdots + g}_{n \; summands}
  \,.
$$


+-- {: .num_defn }
###### Definition

A [[group]] $G$ is called **divisible** if for every [[natural number]] $n$ (hence for every [[integer]]) we have that for every element $g \in G$ there is an element $h \in G$ such that 

$$
  g = n \cdot h
  \,.
$$

=--

In other words, if for every $n$ the 'multiply by $n$' map $G \stackrel{n}{\to} G$ is a [[surjection]].

+-- {: .num_defn }
###### Definition

For $p$ a [[prime number]] a group is **$p$-divisible** if the above formula holds for all $n$ of the form $p^k$ for $k \in \mathbb{N}$. 

=--

+-- {: .num_remark }
###### Remark

There is also an abstract notion of $p$-[[p-divisible group|divisible group]] in terms of [[group schemes]].

=--

## Properties

### Equivalent characterization

+-- {: .num_prop }
###### Proposition

Let $A$ be an [[abelian group]].

Assuming the [[axiom of choice]], the following are equivalent:

1.  $A$ is divisible

1.  $A$ is [[injective object]] in the the [[category]] [[Ab]] of [[abelian groups]] 

1. the [[hom functor]] $Hom_{Ab}(-,A) : Ab^{op} \to Ab$ is [[exact functor|exact]].

=--

This is for instance in ([Tsit-YuenMoRi,Proposition 3.19] (#Tsit-YuenMoRi)). It follows for instance from using [[Baer's criterion]].

### Vector space structure

+-- {: .num_prop }
###### Proposition

The [[torsion-free]] and divisible abelian groups are precisely the $\mathbb{Q}$-vector spaces, i.e. if $A$ is torsion-free and divisible, then it carries a unique vector space structure.

=--

### Stability under various operations

+-- {: .num_prop }
###### Proposition

The [[direct sum]] of divisible groups is itself divisible.

=--

+-- {: .num_prop #QuotientOfDivisibleIsDivisible}
###### Proposition

Every [[quotient group]] of a divisible group is itself divisible.

=--

## Examples

+-- {: .num_example }
###### Example

The additive group of [[rational number]] $\mathbb{Q}$ is divisible.
Hence also that underlying the [[real numbers]] $\mathbb{R}$ and the [[complex numbers]].

=--

Hence:

+-- {: .num_example }
###### Example

The underlying abelian group of any $\mathbb{Q}$-[[vector space]] is divisible.

=--

Also, by prop. \ref{QuotientOfDivisibleIsDivisible}, 

+-- {: .num_example #CircleGroupExample}
###### Example

The [[quotient groups]] $\mathbb{Q}/\mathbb{Z}$ and $\mathbb{R}/\mathbb{Z}$ are divisible (the latter is also written $U(1)$ (for _[[unitary group]]_) or $S^1$ (for _[[circle group]]_)).

=--

+-- {: .num_remark }
###### Remark

What is additionally interesting about example \ref{CircleGroupExample} is that it provides an [[injective object|injective]] [[cogenerator]] for the [[category]] [[Ab]] of abelian groups. Similarly, $\mathbb{R}/\mathbb{Z}$  is an injective cogenerator. 

=--

+-- {: .num_example }
###### Counter-Example

The following groups are **not** divisible:

* the additive group of [[integers]] $\mathbb{Z}$.

* the [[cyclic group]] $\mathbb{Z}_n$ for $n \geq 1 \in \mathbb{N}$.

=--


## References

* {#Tsit-YuenMoRi}  [[Tsit-Yuen Lam]], _Lectures on modules and rings_, Graduate Texts in Mathematics No. 189, Berlin, New York (1999) ([doi:10.1007/978-1-4612-0525-8](https://link.springer.com/book/10.1007/978-1-4612-0525-8))
  

