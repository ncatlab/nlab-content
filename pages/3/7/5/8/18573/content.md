
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## History

[Brandt (1927)](#Brandt27) introduced (long before the notion of *[[category]]* was formulated) a class of partial binary algebraic structures and called them *[[groupoids]]* (German: *Gruppoide*). 

Following [[Øystein Ore]], all binary algebraic structures were soon called *groupoids* (now we say either *binary algebraic structure* or, following [[Bourbaki]]: *[[magma]]*), hence *Brandt groupoids* are in general algebra often viewed as a class of partial groupoids. 

Contemporary notion of a _[[connected groupoid|connected]]_ [[groupoid]] is informationally equivalent to a Brandt groupoid. Hence Brandt groupoids in the new categorical format, and usually without the connectedness assumption, took over the name in mainstream mathematics, regarding the importance of the notion. Wikipedia simply now redirects Brandt groupoid to [groupoid](https://en.wikipedia.org/wiki/Groupoid).

+--{: .num_remark #DifferingTerminology}
###### Remark
**(usage of the terminology)**
In older literature, the specific class of groupoids, a [[codiscrete groupoid]] of a set $X$ is also sometimes called a Brandt groupoid (as mentioned in da Silva, Weinstein, Geometric models of noncommutative algebras).

=--

## Definition

A __Brandt groupoid__ $(M,\cdot)$ is a set with a partially defined binary operation $\cdot$ such that

1. (associativity) If $a\cdot b$ and $b\cdot c$ are defined then $(a\cdot b)\cdot c$ and $a\cdot (b\cdot c)$ are defined and they are equal
1. for each $a\in M$ there are unique elements $e,f\in M$ such that $e\cdot a = a\cdot f = a$, called respectively its left and right unit
1. if the left units of $a$ and $b$ agree then there is $x\in M$ such that $a \cdot x = b$; if the right units of $c$ and $d$ agree then there is $y\in M$ such that $y\cdot c = d$
1. (connectedness) if $e$ and $f$ are idempotents, then there is $m$ such 
that $e\cdot m\cdot f$ is defined

## Properties

The first three properties imply that the idempotents $e$ in $M$ are precisely the left units of all elements $a$ such that $e\cdot a$ is defined; they are also precisely the right units of all elements $b$ such that $b\cdot e$ is defined.

If $(M,\cdot)$ is a Brandt groupoid then the set $M\coprod \{0\}$ can be made into an [[inverse semigroup]] by extending $\cdot$ so that the multiplication of any element with $0$ is $0$ and the product of any two elements in $M$ whose product was undefined is also $0$. Semigroups of that kind are called Brandt semigroups. 

## Literature

* {#Brandt27} [[Heinrich Brandt]], _Über eine Verallgemeinerung des Gruppenbegriffes_, Mathematische Annalen **96** 1 (1927) 360-366 &lbrack;[doi:10.1007/BF01209171](https://doi.org/10.1007%2FBF01209171)&rbrack;

* G. B. Preston, _Congruences on Brandt semigroups_, Mathematische Annalen __139__:2 (1959) 91-94 &lbrack;[doi:10.1007/BF01354867](http://dx.doi.org/10.1007/BF01354867)&rbrack;


* A. H. Clifford, _Matrix representations of completely simple semigroups_
Amer. J. Math. 64, 327--342 (1942). 

[[!redirects Brandt groupoids]]

[[!redirects Brandt semigroup]]

