
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

An [[orthogonal factorization system]] $(E,M)$ on a [[category]] $C$ with [[pullbacks]] is called **stable** if $E$ is [[stability under pullback|stable under pullback]].

## Properties

### In terms of indexed left adjoints
 {#InTermsOfIndexedLeftAdjoints}

For a general (orthogonal) factorization system $(E,M)$, the factorizations show that for all [[objects]] the [[full subcategory|full inclusion]] $M/x \to C/x$ (where $M/x$ consists of morphisms in $M$ with [[target]] $x$) has a 
[[left adjoint]], hence is a [[reflective subcategory]].  

The factorization system is stable if and only if these left adjoints form an [[indexed functor]] --- that is, they commute with the [[base change|pullback functors]] $f^* \colon C/y \to C/x$.

### Stable reflective factorization systems
 {#StableReflectiveFactorizationSystems}

A [[reflective factorization system]] on a finitely [[complete category]] is stable if and only if its corresponding [[reflector]] preserves [[finite limits]] (is a [[left exact functor]]).  

The analogous statement also holds in [[(∞,1)-category theory]], or rather at least in [[locally cartesian closed (∞,1)-categories]]. A discussion of this and formal proof in terms of [[homotopy type theory]] is in ([Shulman](#Shulman)).

A stable reflective factorization system is sometimes called **local**.


## Examples

* In an a [[topos]], [[epimorphism]] are stable under [[pullback]] and hence the [[(epi, mono) factorization system]] in a topos is stable.

  More generally, in an [[(∞,1)-topos]] for all $n \in \mathbb{N}$ the [[(n-epi, n-mono) factorization system]] (see there for more details) is a stable [[orthogonal factorization system in an (∞,1)-category]]. 

## Related concepts

* [[reflective factorization system]]

* [[closure operator]]

## References

The relation between stable factorization systems and the Beck-Chevalley condition of the associated fibrations is discussed in

* J. Hughes and [[Bart Jacobs]], _Factorization systems and fibrations: Toward a fibred Birkhoff variety
theorem_, Electr. Notes in Theor. Comp. Sci., 69 (2002)

The notion appears also for instance in

* [[Max Kelly]], _A note on relations relative to a factorization system_, Lecture Notes in Mathematics, 1991, Volume 1488 (1991)

* Stefan Milius, _Relations in categories_, PhD thesis ([pdf](http://www.iti.cs.tu-bs.de/~milius/thesis/thesis_a4.pdf))

Discussion of epimorphisms in toposes is for instance in 

* [[Stephen Lack]], Pawel Soboc&#237;nski, _Toposes are adhesive_ ([pdf](http://users.ecs.soton.ac.uk/ps/papers/toposesAdhesive.pdf))
 {#LackSobocisnski}

Discussion of reflective stable factorization systems in the context of [[(∞,1)-category theory]] (and with an eye towards [[cohesive homotopy type theory]]) is in 

* [[Mike Shulman]], _Axiomatic cohesion in HoTT_ (2011) ([web](http://homotopytypetheory.org/author/mikeshulman/))
 {#Shulman}

[[!redirects stable factorization systems]]
[[!redirects local factorization system]]
[[!redirects local factorization systems]]
