
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[modal logic]] a [[modality]] expresses a "way of being true" and a modal proposition (or [[stable proposition]]) is a [[proposition]] which is indeed [[true]] in the given way (for instance being [[necessity|necessarily]] true or [[possibility|possibly]] true, in [[S4 modal logic]] ).

As one passes from [[logic]] to ([[homotopy type theory|homotopy]]) [[type theory]] and hence from [[modal logic]] to [[modal type theory]], then being [[true]] is just the lowest stage of a hierarchy of [[truncated object of an (infinity,1)-category|truncated]] types ("[[h-level]]"). Hence for a general [[type]]/[[homotopy type]] then a [[modality]] expresses just a "way of being".

For instance if $C$ is a discrete finite [[type]] ([[h-set]]) thought of as a type of "colors" and one [[term]] $g \colon C$ of it is thought of as the color "green", then the $C$-[[dependent type|dependent types]] may be thought of as colored types; and so there is a [[modal operator]] whose modal types are those which are unicolored in green. Hence here the "way of being" expressed by the modality is "being green". (Formally, $g: 1 \to C$ induces $g^{\ast}: \mathbf{H}/C \to \mathbf{H}$ selecting the $g$-fiber of a $C$-colored type. Then composition with its left adjoint, [[dependent sum]], $\sum_g: \mathbf{H} \to \mathbf{H}/C$, yields the comonadic modal operator, $\sum_g \cdot g^{\ast}$, on $\mathbf{H}/C$, which acts on a colored type to filter out non-green entities.)

More practical examples arise for instance in [[cohesive homotopy type theory]], where for instance the [[flat modality]] expresses the "way of being [[discrete object|geometrically discrete]]" and the [[sharp modality]] expresses the "way of being [[codiscrete object|codiscrete]]".

If one also regards non-idempotent (co-)monads as [[modal operators]] then the "way of being" expressed by them may involve [[structure]] and not just [[property]]. For instance the modal types of the [[maybe monad]] are the [[pointed objects]] and hence the maybe modality expresses the "way of being pointed".

## Definition

Given a [[modal type theory]], hence [[type theory]] equipped with a [[closure operator]] [[modality]] $\Diamond$ ([[idempotent monad|idempotent]] [[monad|monadic]]) or $\Box$ ([[idempotent comonad|idempotent]] [[comonad|comonadic]]), a [[type]] $X$ is _modal_ with respect to $\Diamond$/$\Box$ if 

* the [[unit of an adjunction|unit]] $\eta \colon X \to \Diamond X$

* or the counit $\epsilon \colon \Box X \to X$

is an [[equivalence]]. 

The collection of modal types forms the _closure_ of the given closure operator. 

Under [[propositions as types]] a [[proposition]] that is modal is also called a _[[stable proposition]]_.

By the discussion at _[idempotent monad -- Properties -- Eilenberg-Moore category of algebra](idempotent+monad#AlgebrasForAnIdempotentMonad)_ the modal types over an idempotent (co-)modality are precisely the types which are (co-)[[algebras over a monad|algebras]] over the given (co-)monad. Hence more generally it makes sense to regard a not-necessarily idempotent (co-)monad as a modal operator and regard its [[algebra over a monad|algebras]] as the corresponding modal types.

## Examples

## Related concepts

* [[modality]]

* [[reflective subcategory]]

* [[reflective sub-(∞,1)-category]]

* [[modal type theory]]

* [[reflective subuniverse]]

[[!redirects modal types]]

[[!redirects modal object]]
[[!redirects modal objects]]

[[!redirects modale]]
[[!redirects modales]]


