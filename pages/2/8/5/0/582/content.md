
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[monomorphism]] is _regular_ if it behaves like an [[embedding]].

* [[effective epimorphism]] $\Rightarrow$ [[regular epimorphism]] $\Leftrightarrow$ [[covering]]

* [[effective monomorphism]] $\Rightarrow$ [[regular monomorphism]] $\Leftrightarrow$ [[embedding]] .

The universal factorization through an embedding is the [[image]].


## Definition

A **regular monomorphism** is a [[morphism]] $f : c \to d$ in some [[category]] which occurs as the [[equalizer]] of _some_ parallel pair of morphisms $d \stackrel{\to}{\to} e$, i.e. for which a [[limit]] diagram

$$
  c \stackrel{f}{\to} d \stackrel{\to}{\to} e
$$

exists.

From the defining universal property of the [[limit]] it follows directly that a regular monomorphism is automatically a [[monomorphism]].

The dual concept is that of a [[regular epimorphism]].

### Relation to effective monomorphisms 

Recall that a monomorphism $i: A \to B$ is [[effective monomorphism|effective]] if the [[pushout]]

$$\array{
A & \stackrel{i}{\to} & B \\
i \downarrow & & \downarrow i_1 \\
B & \underset{i_2}{\to} & B +_A B
}$$ 

exists and $i$ is the equalizer of the pair of coprojections $i_1, i_2: B \stackrel{\to}{\to} B +_A B$. Obviously effective monomorphisms are regular. 

+-- {: .un_prop} 
######Proposition
In a category with [[finite limit]]s and [[finite colimit]]s, every regular monomorphism $i: A \to B$ is effective. 
=-- 

+-- {: .proof} 
######Proof 
Suppose $i: A \to B$ is the equalizer of a pair of morphisms $f, g: B \to C$, and with notation as above, let $j: E \to B$ be the equalizer of the pair of coprojections $i_1, i_2$. Since $f \circ i = g \circ i$, there exists a unique map $\phi: B +_A B \to C$ such that $\phi \circ i_1 = f$ and $\phi \circ i_2 = g$. Then, since 
$$f j = \phi i_1 j = \phi i_2 j = g j$$ 
and since $i: A \to B$ is the equalizer of the pair $(f, g)$, there is a unique map $k: E \to A$ such that $j = i k$. Since $i_1 i = i_2 i$, there is a unique map $l: A \to E$ such that $i = j l$. The maps $k$, $l$ are mutually inverse. 
=-- 

## Examples

* In [[Set]], or more generally in any [[pretopos]], every [[monomorphism]] is regular.

* Similarly, in [[Ab]], and more generally any [[abelian category]], every monomorphism is regular.

* In [[Grp]], the monics are (up to [[isomorphism]]) the inclusions of [[subgroup]]s, and every monomorphism is regular, though this is more difficult to prove than in the preceding cases.  (See exercise 7H of Adamek, Herrlich, Strecker, _Abstract and Concrete Categories_.)  In contrast, the [[normal monomorphisms]] (where one of the morphisms $d \to e$ is required to be the [[zero morphism]]) are the inclusions of [[normal subgroups]].

* In [[Top]], the monics are the injective functions, while the regular monos are the embeddings (that is, the injective functions whose sources have the [[induced topology|topologies induced]] from their targets); these are in fact all of the [[extremal monomorphism]]s.

## In an $(\infty,1)$-category {#Infty1Version}

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

**Warning** The same warning as at [[regular epimorphism]] applies: with this definition of regular monomorphism in an [[(∞,1)-category]] these may fail to satisfy various definitions of plain monomorphisms that one might think of. 

[[!redirects regular monomorphism]]
[[!redirects regular monomorphisms]]
[[!redirects regular subobject]]
[[!redirects regular subobjects]]
[[!redirects regular mono]]
[[!redirects regular monos]]
[[!redirects regular monic]]
[[!redirects regular monics]]
