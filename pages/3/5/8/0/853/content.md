
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The notion of a _constant morphism_ in a [[category]] generalises the notion of [[constant function]].


## Definition

+-- {: .num_defn #ConstMorph}
###### Definition
A __constant morphism__ in a [[category]] $\mathcal{C}$ is a [[morphism]] $c\colon B \to C$ with the property that if $f,g\colon A \to B$ are morphisms in $\mathcal{C}$ then $c \circ f = c \circ g$.  In other words, for every object $A$, *at most* one morphism from $A$ to $C$ factors through $c$.
=--

Thus, $c$ is a constant morphism if the function $c_* \colon \mathcal{C}(A,B) \to \mathcal{C}(A,C)$ given by composition with $c$ is a [[constant function]] for every object $A$.

Another definition that is sometimes used is the following.

+-- {: .num_defn #ConstTerm}
###### Definition
If $\mathcal{C}$ has a [[terminal object]], then $c:B\to C$ is __constant__ iff it factors through this terminal object.

If $\mathcal{C}$ does not have a terminal object, then we can reformulate this by saying that the image of $c$ under the [[Yoneda embedding]], $(c\circ -) \colon \mathcal{C}(-,B)\to \mathcal{C}(-,C)$, factors through the [[terminal object|terminal]] [[presheaf]].  In elementary terms, this means that we can choose for each object $X$ a morphism $f_X:X\to C$ such that (1) $f_B=c$ and (2) the $f_X$ are natural in $X$, i.e. for any $g:Y\to X$ we have $f_X g = f_Y$.
=--

This second definition implies the first, but they are not equivalent in general.  In the [[category of sets]], the first implies the second if the set $B$ is [[inhabited set|inhabited]], or if the set $B$ is [[empty set]] and the set $C$ is inhabited.  (By [[excluded middle]], $B$ is either inhabited or empty, so it suffices to assume that $C$ is inhabited with no assumption about $B$.)

More generally, if $c\colon B \to C$ is a morphism in a category $\mathcal{C}$, then the two definitions are equivalent if $\mathcal{C}(A,B)$ is inhabited for every $A$, since we can then define $f_X = c g$ for some (hence any) $g:A\to B$.  If $\mathcal{C}$ has a terminal object $1$, then this is equivalent to the existence of a [[global section]] $b\colon 1 \to B$.

See the [forum](https://nforum.ncatlab.org/discussion/2689/constant-morphism/) for further discussion of this.


## Relation to (sub)terminal objects

The [[identity morphism]] on an object $B$ satisfies definition 1 if and only if $B$ is [[subterminal object|subterminal]]; it satisfies definition 2 iff $B$ is [[terminal object|terminal]].  In particular, the identity function on the [[empty set]] satisfies definition 1 but not definition 2.


## Examples

Using the two-point set, it is simple to show that the constant morphisms in [[Set]] are precisely the constant functions.

## Results

Using the first definition:

- If $f$ is constant, then also $g \circ f$ is constant (whenever this composition is defined).
- If $f$ is constant, then also $f \circ g$ is constant (whenever this composition is defined).
- Any [[right adjoint functor]] preserves constant morphisms.
- A [[representable functor]] maps constant morphisms to constant maps.
- In a category with [[zero morphisms]], constant morphisms coincide with the zero morphisms.

## Dual concept

As usual, we may [[duality|dualize]] the concept: A morphism $c\colon A \to B$ is __coconstant__ if for all pairs of morphisms $f,g \colon B \to C$ we have $f \circ c = g \circ c$.

The results on constant morphisms dualize to results on coconstant morphisms. For example, any morphism that factors through an [[initial object]] is coconstant.

For a concrete example, the evaluation homomorphism $\mathbb{Z}[X] \to \mathbb{Z}$, $f \mapsto f(0)$ from the polynomial ring is coconstant in the [[category of rings]].

In a category with zero morphisms, coconstant morphisms agree with the zero morphisms (which also coincide with the constant morphisms).

A morphism that is both constant and coconstant is a [[zero morphism]].

## Related concepts

* [[constant function]]

* [[steady function]]

* [[global element]]

[[!redirects constant morphism]]
[[!redirects constant morphisms]]
[[!redirects coconstant morphism]]
[[!redirects coconstant morphisms]]
