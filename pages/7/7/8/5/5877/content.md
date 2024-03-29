
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

### General

Generally in [[category theory]] a _projection_ is one of the canonical [[morphisms]] $p_i$ out of a (categorical) [[product]]:

$$
  p_i \colon \prod_j X_j \to X_i
  \,.
$$


or, more generally out of a [[limit]] 

$$
  p_i \colon \underset{\leftarrow_j}{\lim} X_j \to X_i
  \,.
$$

Hence a projection is a component of a [[limit|limiting]] _[[cone]]_ over a given [[diagram]].


In fact, in older literature the [[filtered category|filtered diagrams]] of spaces or algebraic systems (usually in fact indexed by a codirected set) were called [[projective systems]] (or [[inverse systems]]).

Dually, for colimits the corresponding maps in the opposite direction are sometimes caled _[[coprojection]]s_.


### In linear algebra

In [[linear algebra]] an [[idempotent]] [[linear operator]] $P:V\to V$ is called a projection onto its [[image]]. See at _[[projector]]_. 

  In [[functional analysis]], one sometimes requires additionally that this idempotent is in fact [[self-adjoint operator|self-adjoint]]; or one can use the slightly different terminology _[[projection operator]]_. 

  This relates to the previous notion as follows: the existence of the [[projector]] $P \colon V \to V$ canonically induces a decomposition of $V$ as a [[direct sum]] $V \simeq ker(V) \oplus im(V)$ and in terms of this $P$ is the [[composition]]

  $$
    P \colon V \simeq im(V) \oplus ker(V)\to im(V) \hookrightarrow V
  $$

  of the _projection_ (in the above sense of maps out of [[products]]) out of the [[direct sum]] $im(V) \oplus ker(V) \simeq im(V) \times ker(V)$ followed by the [[subobject]] inclusion of $im(V)$. Hence: 

  _A projector is a projection followed by an inclusion_.


## Related concepts

A different concept of a similar name is _[[projection formula]]_.


[[!redirects projection]]
[[!redirects projections]]

[[!redirects product projection]]
[[!redirects product projections]]
[[!redirects projection morphism]]
[[!redirects projection morphisms]]

[[!redirects projection map]]
[[!redirects projection maps]]
