

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[equivariant cohomology]] version of [[KK-theory]].

## Definition

Let $G$ be a [[locally compact topological space|locally compact]] [[topological group]].



+-- {: .num_defn }
###### Definition

$KK_G$ is the [[category]]...

=--

([Blackadar, section 20.2](#Blackadar)) The [[composition]] is in ([Blackadar, theorem 20.3.1](#Blackadar)) .

+-- {: .num_defn #KKTheoreticRepresentationRing}
###### Definition

The KK-theoretic [[representation ring]] of $G$ is the [[ring]]

$$
  R(G) \simeq KK_G(\mathbb{C}, \mathbb{C})
  \,.
$$


=--

([Blackadar def. 20.4.2](#Blackadar))

## Properties

The [[Green-Julg theorem]]:

+-- {: .num_theorem #GreenJulgTheorem}
###### Theorem
**(Green-Julg theorem)**

Let $G$ be a [[topological group]] acting on a [[C*-algebra]] $A$.

1. If $G$ is a [[compact topological group]] then the descent map

   $$
     KK^G(\mathbb{C}, A) \to KK(\mathbb{C},G\ltimes A) 
   $$

   is an [[isomorphism]], identifying the [[equivariant operator K-theory]] of $A$ with the ordinary [[operator K-theory]] of the [[crossed product C*-algebra]] $G \ltimes A$.

1. if $G$ is a [[discrete group]] then the descent map

   $$
     KK^G(A, \mathbb{C}) \to KK(G \ltimes A, \mathbb{C})
   $$

   is an [[isomorphism]], identifying the equivariant [[K-homology]] of $A$ with the ordinary [[K-homology]] of the [[crossed product C*-algebra]] $G \ltimes A$.

=--

([Blackadar, 20.2.7](#Blackadar)). 

+-- {: .num_prop }
###### Proposition

If $G$ is a [[compact topological group]], then the KK-theoretic representation ring, def. \ref{KKTheoreticRepresentationRing} coincides with the ordinary [[representation ring]] of $G$.

=--

([Blackadar, prop. 20.4.4](#Blackadar))


## Related concepts

* [[Baum-Connes conjecture]]

## References

Section 20 of

* [[Bruce Blackadar]], _[[K-Theory for Operator Algebras]]_
 {#Blackadar}

