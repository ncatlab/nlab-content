
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Effective epimorphisms
* table of contents
{:toc}

## Idea

An _effective epimorphism_ is a [[morphism]] $c\to d$ in a [[category]] which behaves in the way that a [[covering]] is expected to behave, in the sense that "$d$ is the union of the parts of $c$, identified with each other in some specified way".

A morphism with a [[kernel pair]] (such as any morphism in a category with [[pullbacks]]) is an effective epimorphism if and only if it is a [[regular epimorphism]] and a [[strict epimorphism]].  For morphisms without kernel pairs, the notion of effective epimorphism is of questionable usefulness.


## Definition 

An **effective epimorphism** in a [[category]] $C$ is a [[morphism]] $f : c \to d$ that has a [[kernel pair]] $c \times_d c$ and is the [[quotient object]] of this kernel pair, in that 

$$
  c \times_d c \;\rightrightarrows\; c \overset{f}{\to} d
$$

is a [[colimit]] diagram (a [[coequalizer]]).

In other words, this says that $f : c \to d$ is effective if $d$ is the [[coimage]] of $f$.

Sometimes we say that such morphism $f$ is an [[effective quotient]].

The [[duality|dual]] concept is that of [[effective monomorphism]].

## Properties

### Relation to other notions of epimorphism

Every effective epimorphism is, of course, a [[regular epimorphism]] and hence a [[strict epimorphism]].  Conversely, a strict epimorphism which *has* a kernel pair is necessarily an effective epimorphism.  (This is a special case of the theory of [[generalized kernels]].)  For this reason, some writers use "effective epimorphism" in general to mean what is here called a [[strict epimorphism]].


## Examples

* In [[Set|the category of sets]], every [[epimorphism]] is effective.  Thus, it can be hard to know, when generalising concepts from $\Set$ to other categories, what kind of epimorphism to use.  In particular, one may define a [[projective object]] (and hence the [[axiom of choice]]) using effective epimorphisms.

* More generally, in any [[pretopos]], hence in particular in every [[topos]], every [[epimorphism]] is an effective epimorphism.  See, for instance, ([MacLane-Moerdijk, theorem IV.7.8](#MacLaneMoerdijk)).

* In an [[(∞,1)-topos]] the bare notion of epimorphism disappears, and [[effective epimorphism in an (∞,1)-category]] becomes the default notion of epiness. A morphism in an $(\infty,1)$-topos is effective epi precisely if its [[n-truncated object in an (∞,1)-category|0-truncation]] is an epimorphism (hence an effective epimorphism) in the underlying 1-topos. This is Proposition 7.2.1.14 in Higher Topos Theory.


## Related concepts

* [[epimorphism]], [[regular epimorphism]], **effective epimorphism**

* [[effective epimorphism in an (∞,1)-category]]

## References

* {#Grothendieck61} [[Alexander Grothendieck]], p. 101 (4 of 21) in: _Techniques de construction et théorèmes d'existence en géométrie algébrique III: préschémas quotients_, Séminaire Bourbaki: années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf))


In [[toposes]] effective epimorphisms are considered in 

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], section IV.7  of _[[Sheaves in Geometry and Logic]]_
 

Discussion in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], section 7.6 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_



[[!redirects effective epi]]
[[!redirects effective epimorphism]]
[[!redirects effective epimorphisms]]
