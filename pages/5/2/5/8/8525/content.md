+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

For $H  \hookrightarrow G$ a [[subgroup]] inclusion, its _index_ is the number  ${\vert G: H\vert}$ of $H$-[[cosets]] in $G$, hence roughly is the number of copies of $H$ that appear in $G$.


## Definition

+-- {: .num_defn}
###### Definition

For $H  \hookrightarrow G$ a [[subgroup]], its **index** is the [[cardinality]] 

$$
  {\vert G : H\vert} \coloneqq {\vert G/H\vert}
$$

of the set $G/H$ of [[cosets]].

=--


## Properties

### Multiplicativity

If $H$ is a subgroup of $G$, the coset projection $-H: G\to G/H$ sends an element $g$ of $G$ to its orbit $gH$. 

If $s : G/H\to G$ is a section of the coset projection $-H: G\to G/H$, then $G/H \times H \to G$ given by $( g H , h )\mapsto s( g H ) h^{-1}$ is a bijection. Its inverse is given by the set map $G\to G/H \times H$ given by $g\mapsto ( g H , g^{-1} s( g H ) )$. Note that the induced product projections $G\to G/H$ conincides with the coset projection.

This argument can be internalized to a group object $G$ and a subgroup object $G$ in a category $C$. In this case, the coset projection $-H: G\to G/H$ is the coequalizer of the action on $G$ by multiplication of $H$. The coset projection need not have a section. However, in case such sections exist, each section $s$ of the coset projection, the above argument internalized yields an isomorphism 
$$
G/H \times H \overset{\simeq}\rightarrow G
\, .
$$ 

Even more generally, if $H \hookrightarrow K \hookrightarrow G$ is a sequence of [[subgroup]] objects, then each section of the projection $G/H \to G/K$ yields an isomorphism 
$$
  G/K \,\times \, K/H \stackrel{\simeq}{\to} G/H
\, .
$$

Returning to the case of ordinary groups, i.e. group objects internal to $Set$, where the external axiom of choice is assumed to hold, the coset projection, being a coequalizer and hence an epimorphism, has a section. This gives the multiplicative property of the indices of a sequence $H \hookrightarrow K \hookrightarrow G$ of [[subgroups]] 

$$
  {\vert G : K\vert} \dot {\vert K : H\vert}
  = 
  {\vert G : H\vert}
  \,.
$$

### Finite groups

The concept of index is meaningful especially for finite groups, i.e. groups internal to [[FinSet]]. See, for example, its role in the [[classification of finite simple groups]]. 

Multiplicativity of the index has the following corollary, which is known as **[[Lagrange's theorem]]**: If $G$ is a [[finite group]], then the index of any subgroup is the quotient

$$
  {\vert G : H\vert} = \frac{{\vert G\vert}}{\vert H\vert}
$$

of the [[order of a group|order]] ([[cardinality]] = number of elements) of $G$ by that of $H$.



## Examples

* For $n \in \mathbb{N}$ with $n \geq 1$ and $\mathbb{Z} \stackrel{\cdot n}{\hookrightarrow} \mathbb{Z}$ the subgroup of the [[integers]] given by those that are multiples of $n$, the index is $n$.


[[!redirects finite-index subgroup]]
[[!redirects finite-index subgroups]]
[[!redirects finite index subgroup]]
[[!redirects finite index subgroups]]

[[!redirects index of a subgroup]]
[[!redirects indexes of a subgroup]]
[[!redirects indices of a subgroup]]
[[!redirects indexes of subgroups]]
[[!redirects indices of subgroups]]

