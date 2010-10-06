
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

The **slice category** or **over category** $\mathbf{C}/c$ of a [[category]] $\mathbf{C}$ over an object $c \in \mathbf{C}$ has 
* objects that are all arrows $f \in \mathbf{C}$ such that $cod(f) = c$, and
* morphisms $g: X \to X' \in \mathbf{C}$ from $f:X \to c$ to $f': X' \to c$ such that $f' \circ g = f$.

$$
  C/c
  =
  \left\lbrace
    \array{
       X &&\stackrel{g}{\to}&& X'
       \\
       & {}_f \searrow && \swarrow_{f'}
       \\   
       && c
    }
  \right\rbrace
$$


The slice category is a special case of a [[comma category]].

There is a [[forgetful functor]] $U_c: \mathbf{C}/c \to \mathbf{C}$ which maps an object $f:X \to c$ to its domain $X$ and a morphism $g: X \to X' \in \mathbf{C}/c$ (from $f:X \to c$ to $f': X' \to c$ such that $f' \circ g = f$) to the morphism $g: X \to X'$.

The [[duality|dual]] notion is an [[under category]].


## Examples 

* If $\mathbf{C} = \mathbf{P}$ is a [[partial order|poset]] and $p \in \mathbf{P}$, then the slice category $\mathbf{P}/p$ is the [[down set]] $\downarrow (p)$ of elements $q \in \mathbf{P}$ with $q \leq p$. 

* If $1$ is a [[terminal object]] in $\mathbf{C}$, then $\mathbf{C}/1$ is isomorphic to $\mathbf{C}$.

## Properties

### Relation to codomain fibration

The assignment of overcategories $C/c$ to objects $c \in C$ extends to a [[functor]]

$$
  C/(-) : C \to Cat
  \,,
$$

Under the [[Grothendieck construction]] this functor corresponds the the [[codomain fibration]]

$$
  cod : [I,C] \to C
$$

from the [[arrow category]] of $C$.


### Presheaves on over-categories and over-categories of presheaves {#RelWithPresheaves}

Let $C$ be a [[category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. Write
$PSh(C/c) = [(C/C)^{op}, Set]$ for the [[category of presheaves]] on $C/c$ and write
$PSh(C)/Y(y)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(c)$ is the [[Yoneda embedding]]. 

+-- {: .un_prop}
###### Proposition


There is an [[equivalence]] of categories

$$
  e : PSh(C/c) \stackrel{\simeq}{\to} PSh(C)/Y(c)
  \,.
$$

=--


+-- {: .proof}
###### Proof

The functor $e$ takes $F \in PSh(C/c)$ to the presheaf
$F' : d \mapsto \sqcup_{f \in C(d,c)} F(f)$ which is equipped with the natural transformation $\eta : F' \to Y(c)$ with component map $\eta_d \sqcup_{f \in C(d,c)} F(f) \to C(d,c)$.

A weak inverse of $e$ is given by the functor 
$$
  \bar e : PSh(C)/Y(c) \to PSh(C/c)
$$
which sends
$
  \eta : F' \to Y(C))
$ to $F \in PSh(C/c)$ given by
$$
  F : (f : d \to c) \mapsto F'(d)|_c
  \,,
$$
where $F'(d)|_c$ is the [[pullback]]
$$
  \array{
     F'(d)|_c &\to& F'(d)
     \\
     \downarrow && \downarrow^{\eta_d}
     \\
     pt &\stackrel{f}{\to}& C(d,c)
  }
  \,.
$$ 

=--


+-- {: .un_example}
###### Example

Suppose the presheaf $F \in PSh(C/c)$ does not actually depend on the morphsims to $C$, i.e. suppose that it factors through the forgetful functor from the [[over category]] to $C$:
$$
  F : (C/c)^{op} \to C^{op} \to Set
  \,.
$$

Then
$
  F'(d) = \sqcup_{f \in C(d,c)} F(f)
  = \sqcup_{f \in C(d,c)} F(d)
  \simeq
  C(d,c) \times F(d) 
$
and hence $F ' = Y(c) \times F$ with respect to the [[closed monoidal structure on presheaves]].

=--

See also [[functors and comma categories]].

For the analog statement in [[(∞,1)-category]] theory see

* <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-category+of+(infinity%2C1)-presheaves#interaction_with_forming_overcategories_19">(∞,1)-category of (∞,1)-presheaves -- Interaction with overcategories</a>

at [[(∞,1)-category of (∞,1)-presheaves]].



## In higher category theory

The notion of over category applicable to [[(infinity,1)-category|(∞,1)-categories]] is discussed at [[over quasi-category]].

Similarly, there is a notion of [[model structure on an over category]].


[[!redirects over category]]
[[!redirects over categories]]
[[!redirects over-category]]
[[!redirects over-categories]]
[[!redirects overcategories]]
[[!redirects slice category]]
[[!redirects slice categories]]
