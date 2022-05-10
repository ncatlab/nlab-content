
> This page is about the [[associative unital algebra]] and [[N-graded module|$\mathbb{N}$-graded module]] that is isomorphic to a [[Clifford algebra]]. For the book by [[Emil Artin]] see instead at _[[Geometric Algebra]]_.

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Geometry
+-- {: .hide}
[[!include higher geometry - contents]]
=--
#### Super-Algebra and Super-Geometry
+-- {: .hide}
[[!include supergeometry - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

This definition is a modified version of the one given in [Aragón, Aragón, Rodríguez (1997)](#AragonEtAl97)

Given a [[commutative ring]] $R$, a **geometric algebra** is an [[N-graded module|$\mathbb{N}$-graded]] $R$-[[module]] $A$ with an [[associative unital algebra|associative unital]] [[bilinear function]] $(-)(-):A \times A \to A$ and a ring [[isomorphism]] $j:\langle A \rangle_0 \cong R$ such that 

* for natural numbers $m:\mathbb{N}$ and $n:\mathbb{N}$, the product of every $m$-multivector and $n$-multivector is an $(m+n)$-multivector: for all $a \in \vert A \vert_m$ and $b \in \vert A \vert_n$, there exists $c \in \vert A \vert_{m+n}$ such that $a b = c$

* the product of every $1$-vector with itself is a $0$-vector: for all $a \in \langle A \rangle_1$ there exists $c \in \langle A \rangle_0$ such that $a^2 = c$. 

The $0$-vectors are typically called **scalars** and $1$-vectors are just called **vectors**. An **$n$-blade** is an $n$-vector which could be written as a product of $n$ $1$-vectors. 

## Relation to Clifford algebras

The [[categories]] of $R$-geometric algebras and $R$-[[Clifford algebras]] are [[equivalence of categories|equivalent]], similar to how the categories of [[abelian groups]] and $\mathbb{Z}$-[[modules]] are equivalent. As a result, geometric algebras and Clifford algebras are isomorphic algebras, and the two terms are interchangeable with each other. In fact, Clifford originally named Clifford algebras "geometric algebras", and it was later mathematicians who started using the term "Clifford algebra" for this object. 

### In physics

The use of the term "geometric algebra" rather than "Clifford algebra" for this object continues in physics in a school of thought following [Hestenes 66](#Hestenes66) that emphasizes the usefulness of making this abstract algebra explicit in the exposition of geometry and physics, such as on 2- and 3-[[dimensional]] [[Cartesian spaces]] and on [[Minkowski spacetime]], and in physics, "geometric algebra" also refers to this school of thought. 

In physics, geometric algebra may be seen as a third style of exposition and notation, in between 1) the traditional physics style of regarding the Clifford algebra in terms of [[matrix]] [[representations]], and 2) the traditional mathematics style of defining them as [[quotients]] of [[tensor algebras]] by ideals defined by [[quadratic forms]]. The idea is that while the former approach (1) suffers from its basis-dependency, the latter approach (2) tends to make the subject look more complicated to the novice and working physicist than it really is. 

In textbooks on geometric algebra, the algebra is instead introduced without choosing matrix representations, but highlighting the obvious [[generators and relations]]-presentation over the definition via [[quotients]] of [[tensor algebras]]. (The general theory of Clifford algebras, including core results such as [[Bott periodicity]], is typically not mentioned in textbooks on geometric algebra). While the difference may seem inessential to the trained mathematician, it turns out that this perspectives helps open the subject to many working physicists. The enthusiasm about this perspective that [[David Hestenes]] reports to have experienced when he understood Clifford algebra in physics this way, back as a student, is what made geometric algebra become the school of thought that is today.

One point being made here is that the traditional physics textbook emphasis on the special geometry of the [[Cartesian space]] $\mathbb{R}^3$ with its exceptional [[vector product]] structure is outdated and contra-productive and can be replaced by a more elegant and more universal description in terms of [[bivector]] calculus (which canonically embeds into the [[Clifford algebra]]). In this respect geometric algebra may be thought of as a streamlined exposition of the geometry of [[rotation]] and [[spin]]. 

## Related concepts

* [[spin geometry]], 

  [[spinor]], [[spin representation]]

* [[Dirac equation]]

* [[N-graded module]]

* [[non-associative geometric algebra]]

## References

On the definition of geometric algebras

* {#AragonEtAl97} G. Aragón, J.L. Aragón, M.A. Rodríguez (1997), Clifford Algebras and Geometric Algebra, _Advances in Applied Clifford Algebras_ Vol. 7 No. 2, pg 91–102, doi:10.1007/BF03041220, S2CID:120860757

The original account:

* {#Hestenes66}[[David Hestenes]],  _Space-time Algebra_. New York 1966, reprinted at Birkh&auml;user 2015 ([doi:10.1007/978-3-319-18413-5](https://www.springer.com/de/book/9783319184128))

Other accounts:

* {#Doran94} [[Chris Doran]], _Geometric Algebra and its Application to Mathematical Physics_, 1994 ([pdf](http://geometry.mrao.cam.ac.uk/wp-content/uploads/2015/02/DoranThesis.pdf))

* {#Sobczyk13} Garrett Sobczyk, _New Foundations in Mathematics: The Geometric Concept of Number_. New York (2013)

A textbook on [[mechanics]] written in this style is

* [[Chris Doran]], Anthony Lasenby, _Geometric algebra for physicists_, Cambridge University Press (2003) ([pdf](http://catdir.loc.gov/catdir/samples/cam033/2002035182.pdf))



See also 

* Wikipedia, _[Geometric algebra](https://en.wikipedia.org/wiki/Geometric_algebra)_ 

[[!redirects geometric algebras]]