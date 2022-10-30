
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $\mathcal{C}$ a [[category]] and $X, Y \in \mathcal{C}$ two [[objects]], the _internal hom_ $[X,Y] \in \mathcal{C}$ from $X$ to $Y$ is, if it exists, another [[object]] of $\mathcal{C}$ which behaves like the "object of [[morphisms]]" from $X$ to $Y$.
In other words it is, if it exists, an [[internalization|internal version]] of the ordinary [[hom set]]  $\mathcal{C} \in Set$ or more generally [[hom object]] $\mathcal{C}(X, Y) \in \mathcal{V}$ of a [[locally small category]] or $\mathcal{V}$-[[enriched category]].

One way to make this precise is to mimic the basic property of a [[function set]] $[X,Y] = \{f : X \to Y\}$ of [[functions]] between two [[sets]] $X$ and $Y$: that is uniquely characterizes by the fact that for any other set $S$ the functions $S \to [X,Y]$ are in [[natural bijection]] with the functions $S \times   \to Y$ out of the [[cartesian product]] of $S$ with $X$. Formally this says that the [[functor]] $X\times (-)$ of taking the cartesian product with the set $S$ has a [[right adjoint]] given by the construction $[X,-]$.

This, then, is, generally, the definition of _internal hom_ in any [[cartesian monoidal category]] or in fact in any [[monoidal category]] $(\mathcal{C}, \otimes)$: the [[right adjoint]] $[X,-]$ to the given [[tensor product]] functor $(-)\otimes X$ for all objects $X$. It may or may not exist. If it exists, one says that $(\mathcal{C}, \otimes)$ is a _[[closed monoidal category|closed]]_ [[monoidal category]]. Explicity, the condition is that there is an [[isomorphism]]([[bijection]])
$$
  \mathcal{C}(A, [X,Z]) \stackrel{\simeq}{\to} \mathcal{C}(A \otimes X, Z)
$$
which is [[natural isomorphism|natural]] in all three [[variables]].  (The rightward map here is often called __[[currying]]__, especially in a [[closed monoidal category]] (and more especially for the $\lambda$-[[lambda-calculus|calculus]]).)

In particular this implies that in a closed monoidal category the external hom is re-obtained from the internal hom as its set of [[generalized elements]] out of the [[unit object|tensor unit]] $I \in \mathcal{C}$ in that

$$
  \frac{I \to [X,Y]}{X \to Y}
$$

using that $I \otimes X \simeq X$ by definition of the tensor unit.

Here "closed" in "[[closed monoidal category]]" is in the sense that forming "hom-sets" does not lead "out of the category". In fact the internal hom of a [[cartesian monoidal category]] is indeed the hom as see in the _[[internal logic]]_ of that category (the _[[function type]]_).

More generally, one can consider objects that satisfy some basic [[universal properties]] that an internal hom should satisfy even in the absense of a [[monoidal category|monoidal structure]]. If such exists one speaks therefore just of a _[[closed category]]_. Every [[closed category]] may be seen as a category [[enriched category|enriched]] over itself.  Accordingly, an internal hom is after all a special case of a [[hom-object]], for the special case of this enrichment over itself.

## Definition

+-- {: .num_defn}
###### Definition

Let $(\mathcal{C}, \otimes)$ be a [[monoidal category]]. An **internal hom** in $\mathcal{C}$ is a [[functor]]

$$
  [-,-] : \mathcal{C}^{op} \times \mathcal{C} \to \mathcal{C}
$$

such that for every [[object]] $X \in \mathcal{C}$ we have a pair of [[adjoint functors]]

$$
  ((-) \otimes X \vdash [X, -]) : \mathcal{C} \to \mathcal{C}
  \,.
$$

=--

If this exists, $(\mathcal{C}, \otimes)$ is called a _[[closed monoidal category]]_.

## Properties

### Evaluation map
 {#EvaluationMap}

Let $(\mathcal{C}, \otimes)$ be a [[closed monoidal category]].

+-- {: .num_defn #EvalMap}
###### Definition

For $X,Y \in \mathcal{C}$ two [[objects]], the
**[[evaluation map]]**

$$
  eval_{X,Y} : [X,Y] \otimes X \to Y
$$

is the $((-)\otimes X \vdash [X,-])$-[[adjunct]] of the [[identity]] $id_{[X,Y]} : [X,Y] \to [X,Y]$.

=--

+-- {: .num_remark}
###### Remark

If $\mathcal{C}$ is specifically a [[locally cartesian closed category]], then in terms of the [[type theory]] [[internal language]] of $\mathcal{C}$
the [[evaluation map]] is the [[categorical semantics]] of the [[dependent type]] which in [[type theory]] [[syntax]] is

$$
  f \colon X \to Y,\; x \colon X 
    \;\vdash\; 
   f(x) \colon Y
  \,,
$$

with _[[function application]]_ on the right.

=--

### Composition map
 {#CompositionMap}

Let $(\mathcal{C}, \times)$ be a [[closed monoidal category]].

+-- {: .num_defn #CompositionMorphism}
###### Definition

For $X, Y, Z \in \mathcal{C}$ three [[objects]], the 
**[[composition]] morphism**

$$
  \circ_{X,Y,Z} : 
  [Y, Z]
  \times
  [X, Y]
  \to 
  [X, Z]
$$

is the $((-)\times X \vdash [X,-])$-[[adjunct]] of the following composite of two [[evaluation maps]], def. \ref{EvalMap}:

$$
  [Y, Z] \times [X , Y] \times X 
    \stackrel{(id_{[Y,Z]}, eval_{X,Y})}{\to}
  [Y,Z] \times Y
    \stackrel{eval_{Y,Z}}{\to}
  Z
  \,.
$$

=--

## Examples
 {#Examples}


### In $Set$

In the category [[Set]] of [[sets]], regarded as a [[cartesian monoidal category]], the internal hom is given by [[function sets]]. This exists, by the discussion there, as soon as the [[foundations|foundational]] [[axioms]] are strong enough, for instance as soon as there are [[power objects]], which is the special case of a function set into the 2-element set.

### In a sheaf topos or $(\infty,1)$-sheaf $(\infty,1)$-topos
 {#InASheafTopos}


Let $C$ be a [[site]]. Let $\mathbf{H} = Sh(C)$ be the [[sheaf topos]]
over $C$ or in fact the [[(∞,1)-sheaf (∞,1)-topos]]. We discuss the internal hom of this regard as a [[cartesian monoidal category]]/[[cartesian monoidal (∞,1)-category]].

+-- {: .num_prop}
###### Proposition

The sheaf topos $\mathbf{H}$ is a [[cartesian closed category]] / [[cartesian closed (∞,1)-category]]. In fact it is a [[locally cartesian closed category]] / [[locally cartesian closed (∞,1)-category]].

=--

Hence the internal hom exist.

=--

+-- {: .num_prop #InternalHomInSheaves}
###### Proposition

For $X, Y \in \mathbf{H}$ two [[objects]], the internal hom-object

$$
  [X,Y] \in \mathbf{H}
$$

is the [[sheaf]]/[[(∞,1)-sheaf]] given by the assignment

$$
  [X,Y] : U \mapsto \mathbf{H}(U \times X, Y)
  \,,
$$

for all objects $U \in C$ which on the right we regard under the [[Yoneda embedding]]/[[(∞,1)-Yoneda lemma|∞-Yoneda embedding]] $U \in C \stackrel{Yoneda}{\hookrightarrow} \mathbf{H}$.

Here

* $U \times X \in \mathbf{H}$ is the [[cartesian product]] if $U$ with $X$

* $\mathbf{H}(-,-)$ is the [[hom set]]-[[functor]] / [[derived hom-space|hom space]]-[[(∞,1)-functor]] of $\mathbf{H}$.

=--

See also at _[[closed monoidal structure on presheaves]]_.


+-- {: .proof}
###### Proof

By the [[Yoneda lemma]]/[[(∞,1)-Yoneda lemma]] we have [[natural equivalences]]

$$
  [X,Y](U) \simeq \mathbf{H}(U , [X,Y])
$$

and by the defining $((-)\times X \vdash [X,-])$[[adjunction]] this is naturally equivalent to 

$$
  \cdots \simeq \mathbf{H}(U \times X, Y)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

In the ([[homotopy type theory|homotopy]]-)[[type theory]] [[syntax]] of the [[internal language]] of $\mathbf{H}$ the internal hom $[X, Y] \in \mathbf{H}$ is the [[categorical semantics]] of the [[function type]]

$$
  \vdash (X \to Y) : Type
  \,.
$$

=--


+-- {: .num_prop #EvaluationOfInternalFunctionsInSheafTopos}
###### Proposition

For $X, Y \in \mathbf{H}$, the [[evaluation map]], def. \ref{EvalMap},

$$
  eval_{X,Y} : [X,Y] \times X \to Y
$$

is the morphism of sheaves which over each $U \in C$ sends a  morphism of sheaves $\theta : \mathbf{H}(-,U) \times X(-) \to Y(-)$ (which is the first component by prop. \ref{InternalHomInSheaves}) and an $x \in \mathbf{H}(U,X)$ to 

$$
  eval_{X,Y}(U) : (\theta, x) \mapsto \theta_U(id_U, x) \in Y(U)
  \,.
$$

=--

See ([MacLane-Moerdijk, p. 46](#MacLane-Moerdijk)).

+-- {: .num_prop #CompositionOfInternalFunctionsInSheafTopos}
###### Proposition

For $X, Y, Z \in \mathbf{H}$ three [[objects]] of $\mathbf{H}$, the canonical [[composition]] [[morphism]], def. \ref{CompositionMorphism},

$$
  \circ_{X,Y,Z} : 
  [Y, Z] \times [X, Y] \to [X, Z]
$$

is given by the morphism of [[presheaves]]/[[(∞,1)-presheaves]] whose component over $U \in C$ is the morphism of [[sets]]/[[∞-groupoids]]

$$
  \circ_{X,Y,Z}(U)
  : 
  \mathbf{H}(U \times X, Y)
  \times
  \mathbf{H}(U \times Y, Z)
  \to 
  \mathbf{H}(U \times X, Z)
$$

which sends a pair $(f : U \times X \to Y, g : U \times Y \to Z)$ to the composite

$$
  \circ_{X,Y,Z}(U)(f,g)
  = 
  U \times X 
  \stackrel{(\Delta_U, id_X)}{\to}
  U \times U \times X
  \stackrel{(id_U, f)}{\to}
  U \times Y 
  \stackrel{g}{\to}
  Z
  \,,
$$

where $\Delta_U : U \to U \times U$ is the [[diagonal]] morphism on $U$.

=--

+-- {: .proof}
###### Proof

By definition \ref{CompositionMorphism} the morphism is the [[adjunct]] of the double [[evaluation map]]

$$
  [Y,Z] \times [X,Y] \times X \to Z
  \,.
$$

Since the [[cartesian product]] of two sheaves $A, B \in \mathbf{H}$ is computed objectwise

$$
  A \times B : U \mapsto A(U) \times B(U)
$$

it follows that over each $U \in C$ this double evaluation map is the morphism of sets/$\infty$-groupoids

$$
  [Y,Z](U) \times [X,Y](U) \times X(U) \to Z(U)
$$

hence by prop. \ref{InternalHomInSheaves}

$$
  \mathbf{H}(U \times Y, Z) \times \mathbf{H}(U \times X, Y) \times 
  \mathbf{H}(U,X) \to \mathbf{H}(U,Z)
  \,,
$$

where now by prop. \ref{...} this is the external evaluation.



=--

+-- {: .num_remark}
###### Remark

Intuitively this says that the composite of a $U$-parameterized family of maps $\{f(u) :  X \to Y| u \in U\}$ with a $U$-parameterized family of maps ${g(u) : Y \to Z| u \in U}$ is the $U$-family given by the parameter-wise composite $\{g(u)\circ f(u) | u \in U\}$.

=--

+-- {: .num_example #InternalAutomorphismGroup}
###### Example

The internal [[automorphism group]]/[[automorphism ∞-group]] of an [[object]] $X \in \mathbf{H}$ is the [[subobject]]

$$
  \mathbf{Aut}(X) \hookrightarrow [X,X]
$$

of the internal hom which is maximal subject to the property that the composition of prop. \ref{CompositionOfInternalFunctionsInSheafTopos} becomes invertible.

The ([[homotopy type theory|homotopy]]-)[[type theory]] [[syntax]] for this is given by the [[type]] of [[equivalences in homotopy type theory]]

$$
  \vdash (X \stackrel{\simeq}{\to} X) : Type
  \,.
$$

=--



### For smooth spaces and smooth $\infty$-groupoids

Consider the [[site]] $C = $ [[SmthMfd]] of [[smooth manifolds]] (and the [[open cover]] [[coverage]]) or equivalently over the [[dense subsite]] [[CartSp]] of [[Cartesian spaces]] and [[smooth functions]] between these.


The [[sheaf topos]]/[[(∞,1)-sheaf (∞,1)-topos]] $\mathbf{H} = Sh(C)$ is that of [[smooth spaces]]/[[smooth ∞-groupoids]]. So the discussion of internal homs here is a special case of the above discussion _[In a sheaf topos](#InASheafTopos)_.


+-- {: .num_example}
###### Example

For $X , Y \in SmthMfd \hookrightarrow \mathbf{H}$ two [[smooth manifolds]], the [[internal hom]] $[X,Y] \in \mathbf{H}$ is the [[mapping space]] between them regarded as a [[diffeological space]].

See at _[[manifold structure of mapping spaces]]_ for when this internal hom is [[representable functor|representable]] again by a [[smooth manifold]].

=--


+-- {: .num_example}
###### Example

For $X \in SmthMfd \hookrightarrow \mathbf{H}$ the internal automorphism group, example \ref{InternalAutomorphismGroup}, of $X$ is the [[diffeomorphism group]] of $X$, regarded as a [[diffeological space|diffeological]] group

$$
  \mathbf{Aut}(X) = \mathbf{Diff}(X)
  \,.
$$

=--




### For chain complexes

* [[internal hom of chain complexes]]

### For super vector spaces

The category $SVect$ of [[super vector space]]s has objects $\mathbb{Z}/2$-[[graded vector space]]s with morphisms being _even_ linear maps between them (linear maps which send even things to even things and odd things to odd things):
$$
 Hom_SVect (V, W) = Even Lin(V,W).
$$
This convention allows one nicely to capture the concepts of superalgebra and so on in succinct categorical terms. But occasionally one does need to refer to the _odd_ linear maps. This is the function of the internal hom:
$$
 hom_SVect (V, W) = Lin(V,W).
$$
Note that $hom_{SVect}$ is indeed a super vector space, with the even elements being those maps which preserve the grading and the odd elements being those which change it. One uses this definition to turn SVect into a [[closed monoidal category]]. 


### For Banach spaces

A similar thing happens in the category $Ban$ of [[Banach spaces]] and [[short linear operators]].  The external hom consists of only the *short* linear maps (those bounded by $1$):
$$ Hom_Ban(V,W) = \{ f\colon Lin(V,W) \;|\; {\|f\|} \leq 1 \} .$$
This definition of morphism recovers the most specific notion of [[isomorphism]] of Banach spaces, as well as defining the [[product]] and [[coproduct]] as the [[direct sum]] completed with $p = \infty$ or $p = 1$ respectively.

But the internal hom is the Banach space of *all* bounded linear maps:
$$ hom_Ban(V,W) = \{ f\colon Lin(V,W) \;|\; {\|f\|} \lt \infty \} .$$
This is a Banach space and makes $Ban$ into a [[closed category]].

## Related concepts

* [[function type]]

* [[power object]]

* [[closed category]], [[cartesian closed category]]

* [[strong adjoint functor]]

## References


* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 {#MacLaneMoerdijk}


A discussion query (R. Brown, T. Bartels, M. Shulman) about internal hom is at $n$Forum [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=3372&Focus=27648).


[[!redirects internal hom]]
[[!redirects internal homs]]
[[!redirects inner hom]]
[[!redirects inner homs]]
[[!redirects internal-hom]]
[[!redirects internal-homs]]

[[!redirects mapping space]]
[[!redirects mapping spaces]]