
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Truncated objects
* table of contents
{: toc}

## Idea

A **$k$-truncated object** in an [[n-category]] is an object which "behaves internally like a $k$-category".  More precisely, since an object of an $n$-category can behave at most like an $(n-1)$-category, a $k$-truncated object behaves like a $min(k,n-1)$-category.  More generally, a **$(k,m)$-truncated object** in an [[(n,r)-category]] is an object which behaves internally like a $min((k,m),(n-1,r-1))$-category.


## Definition

Let $C$ be an $(n,r)$-category, where $n$ and $r$ can range from $-2$ to $\infty$ inclusive.  An object $x\in C$ is **$(k,m)$-truncated** if for all objects $a\in C$, the $(n-1,r-1)$-category $C(a,x)$ is in fact a $(k,m)$-category.


## Examples

* In a [[1-category]]:
  * every object is $0$-truncated, 
  * the $(-1)$-truncated objects are the [[subterminal objects]], and
  * the $(-2)$-truncated objects are the [[terminal objects]].

* In a [[2-category]]:
  * every object is $1$-truncated,
  * the $0$-truncated objects are the [[discrete object in a 2-category|discrete objects]],
  * the $(1,0)$-truncated objects are the __groupoidal objects__, and
  * the $(0,1)$-truncated objects are the __posetal objects__.

* In an $(\infty,1)$-category, the $k$-truncated objects (which are automatically $(k,0)$-truncated) are also called **$k$-types**.  See [[n-truncated object of an (∞,1)-category]].


## Properties

### Reflectivity

If the $(n,r)$-category has sufficient [[familial regularity and exactness|exactness properties]], then the $(k,m)$-truncated objects form a [[reflective subcategory]].  More generally, in such a case there is a [[orthogonal factorization system|factorization system]] $(E,M)$ such that $M/1$ is the category of $(k,m)$-truncated objects.  (Note that this is *not* a [[reflective factorization system]], but it is often a [[stable factorization system]].)  For example:

* In any category with a [[terminal object]], the subcategory of terminal objects is reflective, and corresponds to the factorization system $E = $ all morphisms, $M=$ [[isomorphisms]].

* In a [[regular category]], the category of [[subterminal objects]] is reflective, and corresponds to the factorization system $E=$ [[regular epimorphisms]], $M=$ [[monomorphisms]].

* In a [[regular 2-category]], the same holds true, where $E$ is the class of regular $1$-epimorphisms ([[eso morphisms]]) and $M$ the class of $1$-monomorphisms ([[ff morphisms]]).  With additional exactness conditions, the categories of $0$-truncated, $(1,0)$-truncated, and $(0,1)$-truncated objects are also reflective; see [[michaelshulman:truncation in an exact 2-category|here]].

* In an [[(∞,1)-topos]], the $n$-truncated objects are reflective and we have the [[(n-connected, n-truncated) factorization system]].

## Related concepts

* [[(n+1,1)-category of n-truncated objects]]

* [[n-truncated object of an (∞,1)-category]]

* [[n-truncation modality]]

[[!redirects truncated]]
[[!redirects truncated object]]
[[!redirects truncated objects]]
[[!redirects truncated object in an n-category]]
[[!redirects truncated objects in an n-category]]
[[!redirects truncation]]
[[!redirects truncations]]
[[!redirects (-2)-truncated]]
[[!redirects (-1)-truncated]]
[[!redirects (-2)-truncated]]
[[!redirects (-2)-truncated object]]
[[!redirects (-2)-truncated objects]]
[[!redirects (-2)-truncation]]
[[!redirects (-2)-truncations]]
[[!redirects (-1)-truncated]]
[[!redirects (-1)-truncated object]]
[[!redirects (-1)-truncated objects]]
[[!redirects (-1)-truncation]]
[[!redirects (-1)-truncations]]
[[!redirects 0-truncated]]
[[!redirects 0-truncated object]]
[[!redirects 0-truncated objects]]
[[!redirects 0-truncation]]
[[!redirects 0-truncations]]
[[!redirects 1-truncated]]
[[!redirects 1-truncated object]]
[[!redirects 1-truncated objects]]
[[!redirects 1-truncation]]
[[!redirects 1-truncations]]
[[!redirects 2-truncated]]
[[!redirects 2-truncated object]]
[[!redirects 2-truncated objects]]
[[!redirects 2-truncation]]
[[!redirects 2-truncations]]
[[!redirects 3-truncated]]
[[!redirects 3-truncated object]]
[[!redirects 3-truncated objects]]
[[!redirects 3-truncation]]
[[!redirects 3-truncations]]
[[!redirects 4-truncated]]
[[!redirects 4-truncated object]]
[[!redirects 4-truncated objects]]
[[!redirects 4-truncation]]
[[!redirects 4-truncations]]
[[!redirects n-truncated]]
[[!redirects n-truncated object]]
[[!redirects n-truncated objects]]
[[!redirects n-truncation]]
[[!redirects n-truncations]]
[[!redirects k-truncated]]
[[!redirects k-truncated object]]
[[!redirects k-truncated objects]]
[[!redirects k-truncated object in an n-category]]
[[!redirects k-truncated objects in an n-category]]
[[!redirects k-truncation]]
[[!redirects k-truncations]]
[[!redirects (k,m)-truncated object in an (n,r)-category]]
[[!redirects (k,m)-truncated objects in an (n,r)-category]]

[[!redirects groupoidal object]]
[[!redirects groupoidal objects]]
[[!redirects groupoidal object in a 2-category]]
[[!redirects groupoidal objects in a 2-category]]

[[!redirects posetal object]]
[[!redirects posetal objects]]
[[!redirects posetal object in a 2-category]]
[[!redirects posetal objects in a 2-category]]
