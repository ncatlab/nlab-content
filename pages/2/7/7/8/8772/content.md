
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[linear algebra]] a _projector_ is a [[linear map]] $e \colon V \to V$ that "squares to itself" in that its [[composition]] with itself is again itself: $e \circ e = e$. 

A projector $e$ leads to a decomposition of the [[vector space]] $V$ that it acts on into a [[direct sum]] of its [[kernel]] and its [[image]]:

$$
  V \simeq ker(e) \oplus im(e)
  \,.
$$

The notion of projector is the special case of that of [[idempotent]] [[morphism]].

In [[functional analysis]], one sometimes requires additionally that this idempotent is in fact [[self-adjoint operator|self-adjoint]]; or one can use the slightly different terminology __projection operator__.


## Properties

Projectors relate to the notion of [[projections]] in [[category theory]] as follows: the existence of the projector $P \colon V \to V$ canonically induces a decomposition of $V$ as a [[direct sum]] $V \simeq ker(V) \oplus im(V)$ and in terms of this $P$ is the [[composition]]

$$
  P \colon V \simeq im(v) \oplus ker(V)\to im(V) \hookrightarrow V
$$

of the [[projection]] (in the sense of maps out of [[products]]) out of the [[direct sum]] $im(V) \oplus ker(V) \simeq im(V) \times ker(V)$ followed by the [[subobject]] inclusion of $im(V)$. Hence: 

_A projector is a projection followed by an inclusion_.


## Related concepts

* [[projection]]


[[!redirects projector]]
[[!redirects projectors]]

[[!redirects projection operator]]
[[!redirects projection operators]]
