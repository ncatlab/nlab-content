
#Contents#
* automatic table of contents goes here
{:toc}

## Definition ##

A **regular monomorphism** is a [[morphism]] $f : c \to d$ in some [[category]] which occurs as the [[equalizer]] of _some_ parallel pair of morphisms $d \stackrel{\to}{\to} e$, i.e. for which a [[limit]] diagram

$$
  c \stackrel{f}{\to} d \stackrel{\to}{\to} e
$$

exists.

From the defining universal property of the [[limit]] it follows directly that a regular monomorphism is automatically a [[monomorphism]].

## Remarks ## 

The dual concept is that of a [[regular epimorphism]].

## Examples ##

* In [[Set]], or more generally in any [[pretopos]], every [[monomorphism]] is regular.

* Similarly, in [[Ab]], and more generally any [[abelian category]], every monomorphism is regular.

* In [[Top]], the monics are the injective functions, while the regular monos are the embeddings (that is, the injective functions whose sources have the [[weak topology|topologies induced]] from their targets); these are in fact all of the [[extremal monomorphism]]s.

* In [[Grp]], the monics are (up to [[isomorphism]]) the inclusions of [[subgroup]]s, while the regular monics are the inclusions of _[[normal subgroup|normal]]_ subgroups.

## Higher categorial version ##

In the context of [[higher category theory]]
the ordinary [[limit]] diagram $c \stackrel{f}{\to} d \stackrel{\to}{\to} e $ may be thought of as the beginning of a [[homotopy limit]] diagram over a [[cosimplicial object|cosimplicial]] diagram

$$
  c \stackrel{f}{\to} d_0 \stackrel{\to}{\to} d_1
  \stackrel{\to}{\stackrel{\to}{\to}}
  d_2
  \cdots
  \,.
$$

Accordingly, it is not unreasonable to define a regular monomorphism for instance in an [[(∞,1)-category]], to be a morphism which is the [[limit in a quasi-category]] of a cosimplicial diagram.

In practice this is of particular relevance for the $\infty$-version of [[regular epimorphism]]s: with the analogous definition as described there, a morphism $f : c \to d$ is a [[regular epimorphism]] in an [[(∞,1)-category]] $C$ if for all objects $e \in C$ the induced morphism $f^* : C(d,e) \to C(c,e)$ is a [[regular monomorphism]] in [[∞Grpd]] (for instance [[model structure on simplicial sets|modeled]] by a [[homotopy limit]] over a cosimplicial diagram in [[SSet]]).

**Warning** The same warning as at [[regular monomorphism]] applies: with this definition of regular monomorphism in an [[(∞,1)-category]] these may fail to satisfy various definitions of plain monomorphisms that one might think of. But the idea is that the only sensible notion of monomorphism in an [[(∞,1)-category]] is in fact that of regular monomorphism.


[[!redirects regular monomorphisms]]
[[!redirects regular subobject]]
[[!redirects regular subobjects]]
[[!redirects regular mono]]