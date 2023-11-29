
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

An [[orthogonal factorization system]] $(E,M)$ on a [[category]] $C$ with [[pullbacks]] is called **stable** if also the left class $E$ is [[stability under pullback|stable under pullback]].

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


The notion appears for instance in

* [[Max Kelly]], _A note on relations relative to a factorization system_, Lecture Notes in Mathematics, 1991, Volume 1488 (1991)

* Stefan Milius, _Relations in categories_, PhD thesis ([pdf](https://www8.cs.fau.de/ext/milius/thesis/thesis_a4.pdf))

On the relation between stable factorization systems and the [[Beck-Chevalley condition]] of the associated fibrations:

* J. Hughes and [[Bart Jacobs]], _Factorization systems and fibrations: Toward a fibred Birkhoff variety
theorem_, Electr. Notes in Theor. Comp. Sci., 69 (2002)

Discussion of the example [[(epi, mono) factorization system]] in [[toposes]] (for more see at *[[regular category]]*, [here](regular+category#ToposesAreRegular)):

* {#LackSobocínski06} [[Stephen Lack]], [[Pawel Sobocínski]], Lemma 18 in:  *Toposes are adhesive*, in: *Graph Transformations* ICGT 2006,  Lecture Notes in Computer Science **4178**, Springer (2006) 184-198 &lbrack;[doi:10.1007/11841883_14](https://doi.org/10.1007/11841883_14), [pdf](http://users.ecs.soton.ac.uk/ps/papers/toposesAdhesive.pdf)&rbrack;
 

Discussion of reflective stable factorization systems in the context of [[(∞,1)-category theory]] (and with an eye towards [[cohesive homotopy type theory]]):

* {#Shulman} [[Mike Shulman]], _Axiomatic cohesion in HoTT_ (2011) ([web](http://homotopytypetheory.org/2011/11/02/axiomatic-cohesion-in-hott/))

Stable factorisation systems are called **complete factorisation systems** in the following, where they are related to [[comprehension schemes]]:

* [[Clemens Berger]], [[Ralph M. Kaufmann]], *Comprehensive Factorization Systems*, Tbilisi Math. J. 10 (2017), 255-277 ([doi:10.1515/tmj-2017-0112](https://projecteuclid.org/journals/tbilisi-mathematical-journal/volume-10/issue-3/Comprehensive-factorisation-systems/10.1515/tmj-2017-0112.short))
 

[[!redirects stable factorization systems]]
[[!redirects local factorization system]]
[[!redirects local factorization systems]]