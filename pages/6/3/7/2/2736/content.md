
See [[Understanding Constructions in Categories]]

## Idea

[[Set]]...

* [[Objects]] are [[sets]]
* [[Morphisms]] are [[functions]]

***

## Limits

[[limits]]

#### Terminal Object

Any [[singleton]] (a one-element set) is a [[terminal object]] in $Set$.  To be definite, let $\bullet$ be a singleton, and let $*$ be the element of $\bullet$.

To prove this, let $C$ be any set (any object).  Then there is a function $!_C\colon C \to \bullet$, defined by
$$ !_C(z) = * $$
for any element $z$ of $C$.

Now let $v\colon C \to \bullet$ be any function (any morphism).  Notice that, for any element $z$ of $C$, $v(z) = *$ since every element of $\bullet$ is equal to $*$.  Then
$$ v(z) = * = !_C(z) $$
for any element $z$ of $C$, so $v = !_C$.

Therefore, $\bullet$ is a terminal object in $Set$.

#### Binary Products

Given two sets $A$ and $B$, recall that the [[cartesian product]] $A \times B$ of $A$ and $B$ is the set of [[ordered pairs]] $\langle{x,y}\rangle$ for $x$ in $A$ and $y$ in $B$.  There is a [[product]] of $A$ and $B$ in $Set$ that consists of
*  $A \times B$,
*  the left projection $\pi_{A,B}\colon A \times B \to A$ given by $\pi_{A,B} (\langle{x,y}\rangle) = x$, and
*  the right projection $\rho_{A,B}\colon A \times B \to B$ given by $\rho_{A,B} (\langle{x,y}\rangle) = y$.

To prove this, let $C$ be any set, and let $f\colon C \to A$ and $g\colon C \to B$ be functions.  Then there is a function $\langle{f,g}\rangle\colon C \to A \times B$ (the [[pairing]] of $f$ and $g$), defined by
$$ \langle{f,g}\rangle(z) = \langle{f(z),g(z)}\rangle $$
for any element $z$ of $C$.  Notice that $\pi_{A,B} \circ \langle{f,g}\rangle = f$, because
$$ \pi_{A,B}(\langle{f,g}\rangle(z)) = \pi_{A,B}(\langle{f(z),g(z)}) = f(z) $$
for any element $z$ of $C$, and $\rho_{A,B} \circ \langle{f,g}\rangle = g$, because
$$ \rho_{A,B}(\langle{f,g}\rangle(z)) = \rho_{A,B}(\langle{f(z),g(z)}\rangle) = g(z) $$
for any element $z$ of $C$.

Now let $v\colon C \to A \times B$ be any function such that $\pi_{A,B} \circ v = f$ and $\rho_{A,B} \circ v = g$.  Notice that, for any element $z$ of $G$, $v(z) = \langle{x,y}\rangle$ for some $x$ in $A$ and $y$ in $B$, since every element of $A \times B$ takes this form.  Then
$$ x = \pi_{A,B}(\langle{x,y}\rangle) = \pi_{A,B}(v(z)) = f(z) $$
and
$$ y = \rho_{A,B}(\langle{x,y}\rangle) = \rho_{A,B}(v(z)) = g(z) ,$$
so
$$ v(z) = \langle{x,y}\rangle = \langle{f(z),g(z)}\rangle = \langle{f,g}\rangle(z) $$
for every element $z$ of $C$, so $v = \langle{f,g}\rangle$.

Therefore, $A \times B$, when equipped with the projections $\pi_{A,B}\colon A \times B \to A$ and $\rho_{A,B}\colon A \times B \to B$, is a product of $A$ and $B$ in $Set$.

#### Arbitrary Small Products

Given a [[family]] of sets $\langle{A_i}\rangle_i$, recall that the [[cartesian product]] $\prod_i A_i$ of $\langle{A_i}\rangle_i$ is the set of [[tuples]] $\langle{x_i}\rangle_i$ with, for each index $i$, $x_i$ in $A_i$.  There is a [[product]] of $\langle{A_i}\rangle_i$ in $Set$ that consists of
*  $\prod_i A_i$ and,
*  for each index $j$, the $j$th projection $\pi_j\colon \prod_i A_i \to A_j$ given by $\pi_j (\langle{x_i}\rangle_i) = x_i$.

To prove this, let $C$ be any set, and, for each index $i$, let $f_i\colon C \to A_i$ be a function.  Then ...

+-- {: .query}
I\'ll let you finish this one, Eric.  You can use the binary product as a guide.  Or you can first rewrite the binary product in a way that you like better, then use that as a guide here.  ---Toby
=--

#### Equalizers

The [[equalizer]] of two [[parallel morphisms|parallel functions]] $f,g:X\to Y$ is the subset of $X$ on which both functions coincide, i.e.

$$
  Eq(f,g)
  = 
  \left\{
     s \in c | 
     f(s) = g(s)
  \right\}
  \,.
$$

Why?

#### Pullbacks

The [[pullback]] of two functions of sets is the set of pairs $(x,y)$ such that $f(x)=g(y)$.

Why?

#### Fibred Products

[[fibred products]]

***

## Colimits

[[colimits]]

#### Initial Object

The empty set $\emptyset$ is the [[initial object]] in Set.

Why?

#### Binary Coproducts

 binary [[coproducts]]

#### Arbitray Small Coproducts

arbitrary (but small) [[coproducts]]

#### Coequalizers
 
[[coequalisers]]

#### Pushouts

[[pushouts]]

#### Cofibred Products

[[cofibred coproducts]]

***

## Other Constructions ##

#### Exponential Objects

[[exponential objects]]

#### Dependent Products

[[dependent products]]

#### Power Objects

[[power objects]]


[[!redirects Understanding Set]]
[[!redirects Understanding Constructions on Set]]
[[!redirects understanding constructions in Set]]
[[!redirects understanding Set]]
[[!redirects understanding constructions on Set]]
