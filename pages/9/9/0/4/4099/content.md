
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--

# Discrete morphisms
* table of contents
{: toc}

## Definition

A [[morphism]] $f\colon A\to B$ in a [[2-category]] $K$ is called **discrete** if it is representably [[faithful morphism|faithful]] and [[conservative morphism|conservative]], i.e. if for any [[object]] $X$ the [[hom functor|induced]] [[functor]]

$$ 
  K(X,A) \to K(X,B) 
$$

is [[faithful functor|faithful]] and [[conservative functor|conservative]].

An object $A$ is called a **[[discrete object]]** if for any $X$, the category $K(X,A)$ is ([[equivalence of categories|equivalent to]]) a [[discrete category]], i.e. a [[set]].  If $K$ has a ([[2-limit|2-]])[[terminal object]] $1$, this is equivalent to saying that the unique map $A\to 1$ is a discrete morphism.


### Caveat

**NB:** it is more common to define these concepts in the other order: to first define an object to be discrete, as we have done, and then say that $f\colon A\to B$ is a discrete morphism if is a discrete object in the [[slice 2-category]] $K/B$.  In general this does *not* result in the same notion of "discrete morphism" as the definition we have given.  For instance, if $B$ is the [[interval category]] $(0\to 1)$ and $A$ is the free [[parallel pair]] $(0 \rightrightarrows 1)$, then the obvious functor $A\to B$ is a discrete object of $Cat/B$, but is not faithful.

However, the two definitions do coincide for [[fibration in a 2-category|fibrations]], opfibrations, and [[two-sided fibration]]s.  That is, if $f\colon A\to B$ is a fibration or an opfibration in $B$, then it is faithful and conservative if and only if it is a discrete object of $K/B$, and similarly if $A\leftarrow E \to B$ is a two-sided fibration, then $E\to A\times B$ is faithful and conservative if and only if it is a discrete object of $K/(A\times B)$.  Since this is usually the case of most interest (giving rise to [[discrete fibrations]] and, dually, [[codiscrete cofibrations]]), the difference between the two definitions is usually unimportant.

+-- {: .query}
[[Mike Shulman]]: I believe that in cases when the two are different, it is the one given above (faithful and conservative) that is often the better one; hence my proposal in writing this page to change terminology slightly.  Disagreements are welcome.
=--

## Examples

### Discrete categories

A discrete object in the [[2-category]] [[Cat]] is, of course, a [[discrete category]].

### Discrete groupoids

A discrete object in the [[(2,1)-category]] [[Grpd]] of [[groupoids]] is also called a [[0-truncated]] object or [[0-groupoid]] or [[homotopy n-type|homotopy 0-type]] or just [[h-level|0-type]] or [[h-set]].

See also the discussion at [[discrete space]] and [[discrete groupoid]].


## Factorization systems and discrete reflections

Discrete morphisms are often the right class of a [[factorization system in a 2-category|factorization system]].  This factorization system, or one related to it, plays a role in the construction of a [[proarrow equipment]] from [[codiscrete cofibrations]].


[[!redirects discrete morphism]]
[[!redirects discrete morphisms]]

[[!redirects discrete object in a 2-category]]