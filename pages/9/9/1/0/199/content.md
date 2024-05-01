
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a [[field]] $k$, the _category of $k$-vector spaces_ **$Vect_k$**  is the [[category]] whose

1. [[object|objects]] are [[vector space|vector spaces]],

1. [[morphisms]] are [[linear maps]].

If the field $k$ is understood, one often just writes $Vect$.

Via [[direct sum]] and [[tensor product of vector spaces]] $\otimes_k$, this becomes a [[symmetric monoidal category]] in two compatible ways, making it a [[distributive monoidal category]], in particular a [[rig category]].

The study of $Vect$ is called _[[linear algebra]]_.

## Properties

### General

For any field $k$, the category $Vect_k$ is [[complete category|complete]], [[cocomplete category| cocomplete]] and [[closed monoidal category|closed monoidal]] with respect to the [[tensor product of vector spaces]].



### Splitting lemma

Assuming the [[axiom of choice]] (and essentially by the [[basis theorem]]):
\begin{proposition}\label{ShortExactSequencesSplit}
In $Vect$ every [[short exact sequence]] [[split short exact sequence|splits]].
\end{proposition}
(See [there](split+exact+sequence#SESOfVectorSpacesSplits).)

\begin{remark}
On [[FinDimVect]] this is a [[categorification]] of the [[rank-nullity theorem]].
\end{remark}

## Related categories

### Finite-dimensional vector spaces

The [[full subcategory]] of Vect consisting of [[finite-dimensional vector spaces]] may be denoted **[[FinDimVect]]**.

This is a [[compact closed category]] (see [here](finite-dimensional+vector+space#CompactClosure)).

$FinDimVect$ is where most of ordinary [[linear algebra]] lives, although much of it makes sense in all of $Vect$.  See also at _[[quantum information theory in terms of dagger-compact categories]]_.
 
On the other hand, anything involving transposes or [[inner products]] really takes place in $Fin$ [[Hilb]].

### Modules

More generally, for $R$ any [[ring]] (not necessarily a [[field]]) then the analog of $Vect$ is the category $R$[[Mod]] of $R$-[[modules]] and module homomorphisms between them.


### Vector bundles 

For $X$ a suitable [[space]] of sorts, there is the category [[Vect(X)]] of [[vector bundles]] over $X$. Specifically for $X$ a [[topological space]], there is the category of [[topological vector bundles]] over $X$. For $X = \ast$ the [[point space]], then this is [[equivalence of categories|equivalently]] the category of plain vector spaces:

$$
  Vect(\ast) \simeq Vect
  \,.
$$

### Topological vector spaces

There are various categories of [[topological vector spaces]], for instance [[bornological topological vector spaces]].





category: category

[[!redirects category of vector spaces]]
[[!redirects categories of vector spaces]]

[[!redirects category of vector bundles]]
[[!redirects categories of vector bundles]]

[[!redirects VectorSpaces]]

