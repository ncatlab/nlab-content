
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### (0,1)-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *lattice-ordered abelian group* or *l-group* is an [[ordered abelian group]] whose [[order]] forms a [[lattice]]. (Here we assume that lattices do not need to have [[top]] or [[bottom]] elements, because otherwise the only such object is the [[trivial group]].)

## Definition

### Classical definition

A __lattice-ordered abelian group__ or __abelian l-group__ is an [[ordered group|ordered abelian group]] $(G,\le)$ such that every [[pair]] of [[elements]] $a,b \in G$ admits a [[meet]] $a \wedge b$ in the [[underlying]] [[poset]] ([Gilmer 1992](#Gilmer92), p. 158). 

### With the join operation

A __lattice-ordered abelian group__ or __abelian l-group__ is an [[abelian group]] $G$ with a binary [[join]] operation $(-)\vee(-)\colon G \times G \to G$ such that $(G, \vee)$ is a [[commutative magma|commutative]] [[idempotent]] [[semigroup]], and 

* for all $a \in G$, $b \in G$, $c \in G$, $a \vee b = b$ implies that $(a + c) \vee (b + c) = b + c$ and $(c + a) \vee (c + b) = c + b$

The meet is defined as 

$$
  a \wedge b \coloneqq -(-a \vee -b),
$$

the ramp function is defined as 

$$
  ramp(a) \coloneqq a \vee 0, 
$$

and the [[absolute value]] is defined as 

$$
  \vert a \vert \coloneqq a \vee -a
  \,.
$$

The order relation is defined as in all pseudolattices: $a \leq b$ if $a = a \wedge b$. 

### With the ramp function 

The following [[algebraic theory|algebraic]] definition is from [[Peter Freyd]]:

A __lattice-ordered abelian group__ or __l-group__ is an [[abelian group]] $G$ with a function $ramp:G \to G$ such that for all $a$ and $b$ in $G$,

$$
  a = ramp(a) - ramp(-a)
$$

and

$$
  ramp(a - ramp(b)) = ramp(ramp(a) - ramp(b))
$$

The [[join]] $(-)\vee(-):G \times G \to G$ is defined as

$$
  a \vee b \coloneqq a + ramp(b - a)
$$

the [[meet]] $(-)\wedge(-):G \times G \to G$ is defined as

$$
  a \wedge b \coloneqq a - ramp(a - b)
$$

and the absolute value is defined as 

$$
  \vert a \vert \coloneqq ramp(a) + ramp(-a)
$$

The order relation is defined as $a \leq b$ if $ramp(a - b) = 0$. 

## Examples

- All [[total order|totally ordered]] abelian groups, such as the [[integers]], the [[rational numbers]], and the [[real numbers]], are lattice-ordered abelian groups. 

- An example of a lattice-ordered abelian group that is not totally ordered is the abelian group of [[Gaussian integers]] with $ramp(1) \coloneqq 1$ and $ramp(i) \coloneqq i$. 

- Let $R$ be an integral domain, $F(R)$ its field of fraction and $U(R)$ its group of units. The *group of divisibility* of $R$ ([Gilmer 1992](#Gilmer92), p.174), denoted $D(R)$, is defined as 
$$
D(R) = \frac{F(R) \backslash \{0\}}{U(R)}
$$
The abelian group $D(R)$ becomes an ordered abelian group if we define an order as follows: for every $rU(R),sU(R) \in D(R)$, we say that $rU(R) \le sU(R)$ iff $sr^{-1} \in R$.

\begin{proposition}[ [Gilmer 1992](#Gilmer92), p.174 ]
Let $R$ be an integral domain. Then $D(R)$ is a lattice-ordered abelian group iff $R$ is a [[GCD domain]].
\end{proposition}

## Jaffard-Ohm-Kaplansky theorem

\begin{theorem}[ [Gilmer 1992](#Gilmer92), p.215 ]
Every lattice-ordered abelian group $G$ is order-isomorphic to the group of divisibility of a [[Bézout domain]] i.e. there exists a Bézout domain $R$ and a group isomorphism $f:G \rightarrow D(R)$ such that $g \le h \Leftrightarrow f(g) \le f(h)$. 
\end{theorem}

## Related concepts

* [[abelian group]]

* [[ordered abelian group]]

* [[lattice]]

* [[totally ordered abelian group]]

* [[prelattice-ordered abelian group]]

* [[lattice-ordered ring]]

## References

* [[Peter Freyd]], *Algebraic real analysis*, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Gilmer92}[[Robert Gilmer]]: *Multiplicative Ideal Theory*, Queen's Papers in Pure and Applied Mathematics (1992)

[[!redirects abelian l-group]]
[[!redirects abelian l-groups]]

[[!redirects lattice-ordered abelian group]]
[[!redirects lattice-ordered abelian groups]]

[[!redirects lattice ordered abelian group]]
[[!redirects lattice ordered abelian groups]]

[[!redirects pseudolattice-ordered abelian group]]
[[!redirects pseudolattice-ordered abelian groups]]

[[!redirects pseudolattice ordered abelian group]]
[[!redirects pseudolattice ordered abelian groups]]