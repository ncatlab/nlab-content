
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

\tableofcontents


## Idea

An _[[action]]_ or _[[representation]]_ of an algebraic object such as a [[group]] or an [[algebra]] is _faithful_ when the action of two elements being equal implies that these two elements are already equal. When the representation of a group $G$ on some $V$ is thought of as a [[functor]] $\mathbf{B}G \to \mathbf{B}Aut(V)$, then it is faithful precisely if this functor is a [[faithful functor]].

A [[representation]] of an algebraic object, such as a [[group]] or an [[algebra]], is a way of studying it by making it act on some object.  The hope being that the behaviour of the object makes it easier to see the structure of the acting object.  Another way of thinking of such a representation is that it is a [[homomorphism]] of the acting object into some other object that is (presumably) better understood.  Making a group or algebra act on a [[vector space]] is the same as giving a homomorphism into the corresponding [[general linear group]] or [[endomorphism algebra]], making a group act on a set maps it into the corresponding [[permutation group]].

When studying an object via its representation then we really only "see" that part of the object that the representation sees.  Thus there is the potential for forgetting information when passing to a representation.  This can be a good thing, but it might not be.  It is important to classify the possible scenarios and the label **faithful representation** is used for when no information is lost.  This is in line with other uses of the word [[faithful]].

Thus when we have a faithful representation, we can distinguish two elements of the acting object by their actions: if they always do the same thing then they were the same element.


## Definition

### Traditional
 {#Traditional}

Let $(\mathcal{C}, \otimes)$ be a  [[closed monoidal category]], $A$ a [[monoid object]] in $\mathcal{C}$ and 

$$
  \rho \;\colon\; A \otimes V \longrightarrow V
$$

an [[action]]/[[representation]] on some $V \in \mathcal{C}$. Equivalently this is given by its $((V \otimes -) \dashv [V,-] )$-[[adjunct]] $\tilde \rho$ ("[[currying]]"), which is a [[homomorphism]]

$$
 \tilde \rho \colon A \longrightarrow [V,V]
$$

from $A$ to the object of [[endomorphism]] of $V$ (the [[internal hom]]).


+-- {: .num_defn #faithrep}
###### Definition

The representation $\rho$ is called _faithful_ if its adjunct $\tilde \rho$ is a [[monomorphism]].

=--

### For $\infty$-Actions
 {#ForInfinityActions}

Let $\mathbf{H}$ be an [[(∞,1)-topos]], $G \in Grp(\mathbf{H})$ be an [[∞-group]] object and $\rho$ an [[∞-action]] on some $V \in \mathbf{H}$. By the discussion at _[[∞-action]]_ this is equivalently a [[homotopy fiber sequence]] of the form

$$
  \array{
     V &\longrightarrow& V/G
     \\
     && \downarrow
     \\
     && \mathbf{B}G
  }
  \,.
$$ 

Suppose that $V$ is $\kappa$-[[compact object]] for some [[cardinal]] $\kappa$. By the existence of the $\kappa$-small [[object classifier]] $Obj_\kappa \in \mathbf{H}$ the above homotopy fiber sequence is itself the [[homotopy pullback]] of the universal fibration $\widehat {Obj}_\kappa \to Obj_\kappa$ along some morphism $\mathbf{B}G \longrightarrow \mathbf{B}\mathbf{Aut}(V) \hookrightarrow Obj_\kappa$ to the [[delooping]] of the [[automorphism ∞-group]] of $V$

$$
  \array{
     V &\longrightarrow& V/G &\longrightarrow& V/\mathbf{Aut}(V) &\longrightarrow& \widehat{Obj}_\kappa
     \\
     && \downarrow && \downarrow && \downarrow
     \\
     && \mathbf{B}G &\longrightarrow& \mathbf{B}\mathbf{Aut}(V) &\hookrightarrow& Obj_\kappa
  }
  \,.
$$ 

There is the corresponding $\infty$-group homomorphism  (see at [[looping and delooping]])

$$
  \tilde \rho \colon G \longrightarrow \mathbf{Aut}(V)
  \,.
$$

If this is an [[n-monomorphism]] for some $n$ one might call the action "$n$-faithful". If $G$ and $V$ are [[0-truncated]] then any [[∞-action]] of $G$ on $V$ is an ordinary [[action]] in the underlying 1-[[topos]] and this is faithful in the traditional sense if it is $n$-faithful for $n = 1$ in this higher sense.


## Properties
 {#Properties}

### Existence

+-- {: .num_prop }
###### Proposition

If $G$ is a [[compact Lie group]], then there exists a finite-dimensional faithful representation of $G$.

=--

E.g. [Kowalski 14, proof of theorem 6.1.2](#Kowalski14)

+-- {: .num_prop #AlgebraicGroupHasFinDimFaithfulRepresentations}
###### Proposition

For $G$ any [[algebraic group]], then the [[regular representation]] is faithful. Moreover, it has finite-dimensional faithful sub-representations.

=--

(e.g. [Milne 12, IX, theorem 9.1](#Milne12))


### Subquotients


+-- {: .num_prop #AnyFinDimRepOfAffineAlgebraicGroupOverFieldIsSubquotientsOfFaithfulRep}
###### Proposition

If $V$ is a [[finite number|finite]] [[dimension|dimensional]] [[representation]] of an affine [[algebraic group]] $G$ over a [[field]] $k$, then every finite dimensional representation of $G$ is [[isomorphism|isomorphic]] to a [[subquotient]] of $\otimes^n(V \oplus V^\ast)$, where $V^\ast$ is the [[dual representation]].

=--

(e.g. [Milne 12, VIII, theorem 11.7](#Milne12))

## Examples
 {#Examples}

+-- {: .num_example}
###### Example

Let $G$ be a [[discrete group]] and $V$ a [[set]] (hence $\mathcal{C} = $ [[Set]] with its [[Cartesian product]]). The [[adjunct]] of an action map $\rho \colon G \times V \to V$ is a function

$$
  \tilde \rho \colon G \longrightarrow End(V)
$$

from $G$ to the set of [[endofunctions]] of $V$.

The action is faithful if this function $\tilde \rho$ is [[injective]]. 

Observe that $G$ being a group and $\rho$ being an action means that $\tilde \rho$ factors through the inclusion of the [[automorphism group]] $Aut(V) \hookrightarrow End(V)$. (If $V$ is a [[finite set]] then this is a [[symmetric group]]).

So, equivalently the action is faithful if 

$$
  \tilde \rho \colon G \longrightarrow Aut(V)
$$

is injective, hence is a [[monomorphism]] of [[groups]].

More specifically, if $V$ is equipped with the structure of a [[vector space]] and the action is by [[linear functions]], hence is a [[linear representation]], then this means that $\tilde \rho$ factors through the [[general linear group]] $GL(V)$ of $V$ through a group [[homomorphism]]

$$
  \tilde \rho \colon G \longrightarrow GL(V)
  \,.
$$

Again, $\tilde \rho$ is faithful if this is an injection, hence a group monomorphism.

The same applies when $G$ is equipped with extra geometric structure, such as being a [[topological group]] or [[Lie group]].

=--

+-- {: .num_example}
###### Example

A [[Lie groupoid]] is called  _[[effective Lie groupoid|effective]]_ when the [[action]] of all its [[automorphism groups]] of objects on their [[germs]] is faithful. See at _[[effective Lie groupoid]]_ for more on this.

=--

## Related concepts

* [[linear group]]


## References

* {#Milne12} [[James Milne]], _Basic theory of affine group schemes_, 2012 ([pdf](http://jmilne.org/math/CourseNotes/AGS.pdf))

* {#Kowalski} Kowalski, _An introduction to the representation theory of groups_, 2014


[[!redirects faithful representation]]
[[!redirects faithful representations]]

[[!redirects faithful action]]
[[!redirects faithful actions]]

[[!redirects faithful ∞-action]]
[[!redirects faithful ∞-actions]]
[[!redirects faithful infinity-action]]
[[!redirects faithful infinity-actions]]
