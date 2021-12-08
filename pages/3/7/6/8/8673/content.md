
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **finite abelian group** is a [[group]] which is both [[finite group|finite]] and [[abelian group|abelian]].

## Properties

As any [[finite group]], a finite abelian group is [[torsion subgroup|pure torsion]].

+-- {: .num_prop}
###### Proposition

If a finite abelian group $A$ has [[order of a group|order]] ${\vert A \vert} = p$ a [[prime number]], then it is the [[cyclic group]] $\mathbb{Z}_p$.

=--

+-- {: .num_prop}
###### Proposition

If $A$ is a finite abelian group and $p \in \mathbb{N}$ is a [[prime number]] that divides the [[order of a group|order]] ${\vert A \vert}$, then equivalently

* $A$ has an element of [[order of an element|order]] $p$;

* $A$ has a [[subgroup]] of [[order of a group|order]] $p$.

=--

This is [[Cauchy's theorem]] restricted to abelian groups.

+-- {: .proof}
###### Proof

We prodeed by [[induction]] on the [[order of a group|order]] of $A$. For ${\vert A \vert} = 2$ we have that $A = \mathbb{Z}_2$ is the unique [[group of order 2]] and the statement holds for $p =2$. 

Assume then that the statement has been show for groups of order $\lt n$ and let ${\vert A \vert} = n$. 

If $A$ has no non-trivial proper [[subgroup]] then $n$ must be prime and $A = \mathbb{Z}_n$ a [[cyclic group]] and the statement follows.

If $A$ does have a non-trivial proper [[subgroup]] $H \hookrightarrow A$ then $p$ divides either ${\vert H \vert}$ or $\vert A/H\vert$. 

In the first case by [[induction]] assumption $H$ has an element of order $p$ which is therefore also an element of $G$ of order $p$.

In the second case there is by induction assumption an element $a \in A$ such that $a + H \in A/H$ has order $p$. Since the order of $a + H \in A/H$ divides the order of $a \in A$ it follows that $a$ has order $k p$ for some $k \in \mathbb{N}$. Then $k a$ has order $p$.

=--

+-- {: .num_theorem #FiniteAbelianGroupIsDirectSumOfCyclics}
###### Theorem
**([[fundamental theorem of finite abelian groups]])**

Every finite abelian group is the [[direct sum of abelian groups|direct sum]] of [[cyclic groups]] of [[order of a group|order]] $p^k$ for a [[prime number]] $p \in \mathbb{N}$ (its [[p-primary groups]]).

=--

See for instance ([Sullivan](#Sullivan)).

## References

A new proof of the [[fundamental theorem of finite abelian groups]] was given in 

* {#Navarro03} Gabriel Navarro, _On the fundamental theorem of finite abelian groups_, Amer. Math. Monthly, February 2003

reviewed in

* {#Sullivan} John Sullivan, _Classification of finite abelian groups_ ([pdf](http://www.isama.org/jms/m317/handouts/finabel.pdf))
 

[[!redirects finite abelian groups]]
