
> This page discusses the general concept of mapping spaces and internal homs. For mapping spaces in topology, see at _[[compact-open topology]]_.

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
In other words it is, if it exists, an [[internalization|internal version]] of the ordinary [[hom set]]  $\mathcal{C}(X, Y) \in Set$ or more generally [[hom object]] $\mathcal{C}(X, Y) \in \mathcal{V}$ of a [[locally small category]] or $\mathcal{V}$-[[enriched category]].

One way to make this precise starts by mimicking a property of the [[function set]] $[X,Y] = \{f : X \to Y\}$ of [[functions]] between two [[sets]] $X$ and $Y$: this set is characterized by the fact that for any other set $S$, the functions $S \to [X,Y]$ are in [[natural bijection]] with the functions $S \times X \to Y$ out of the [[cartesian product]] of $S$ with $X$. 
That is: for each set $X$, the [[functor]] $(-) \times X$ has a [[right adjoint]], given by the construction $[X,-]$.

One can verbalize this thus: *taking the cartesian product with the set $X$* is left-adjoint to *taking the set of all functions with domain $X$*.

This, then, is, generally, the definition of _internal hom_ in any [[cartesian monoidal category]] or in fact in any [[monoidal category]] $(\mathcal{C}, \otimes)$: the [[right adjoint]] $[X,-]$ to the given [[tensor product]] functor $(-)\otimes X$ for all objects $X$. It may or may not exist. If it exists, one says that $(\mathcal{C}, \otimes)$ is a _[[closed monoidal category|closed]]_ [[monoidal category]]. Explicity, the condition is that there is an [[isomorphism]]([[bijection]])
$$
  \mathcal{C}(A, [X,Z]) \stackrel{\simeq}{\to} \mathcal{C}(A \otimes X, Z)
$$
which is [[natural isomorphism|natural]] in all three [[variables]].  (The leftward map here is often called __[[currying]]__, especially in a [[closed monoidal category]] (and more especially for the $\lambda$-[[lambda-calculus|calculus]]).)

In particular this implies that in a closed monoidal category the external hom is re-obtained from the internal hom as its set of [[generalized elements]] out of the [[unit object|tensor unit]] $I \in \mathcal{C}$ in that

$$
  \frac{I \to [X,Y]}{X \to Y}
$$

using that $I \otimes X \simeq X$ by definition of the tensor unit.

Here "closed" in "[[closed monoidal category]]" is in the sense that forming "hom-sets" does not lead "out of the category". In fact the internal hom of a [[cartesian monoidal category]] is indeed the hom as seen in the _[[internal logic]]_ of that category (the _[[function type]]_).

More generally, one can consider objects that satisfy some basic [[universal properties]] that an internal hom should satisfy even in the absence of a [[monoidal category|monoidal structure]]. If such objects exist one speaks therefore just of a _[[closed category]]_. Every [[closed category]] may be seen as a category [[enriched category|enriched]] over itself.  Accordingly, an internal hom is after all a special case of a [[hom-object]], for the special case of this enrichment over itself.

## Definition

+-- {: .num_defn #ClosedMonoidalCategory}
###### Definition
**(internal hom)**

Let $(\mathcal{C}, \otimes)$ be a [[symmetric monoidal category|symmetric]] [[monoidal category]]. An **internal hom** in $\mathcal{C}$ is a [[functor]]

$$
  [-,-] : \mathcal{C}^{op} \times \mathcal{C} \to \mathcal{C}
$$

such that for every [[object]] $X \in \mathcal{C}$ we have a pair of [[adjoint functors]]

$$
  ((-) \otimes X \dashv [X, -]) : \mathcal{C} \to \mathcal{C}
  \,.
$$

If this exists, $(\mathcal{C}, \otimes)$ is called a _[[closed monoidal category]]_.

=--

+-- {: .num_remark}
###### Remark

If the monoidal category $\mathcal{C}$ in Def. \ref{ClosedMonoidalCategory} is not [[symmetric monoidal category|symmetric]], there is instead a concept of left- and right-internal hom.

=--

### Evaluation map
 {#EvaluationMap}

Let $(\mathcal{C}, \otimes)$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}).

+-- {: .num_defn #EvalMap}
###### Definition

For $X,Y \in \mathcal{C}$ two [[objects]], the
**[[evaluation map]]**

$$
  eval_{X,Y} : [X,Y] \otimes X \to Y
$$

is the $((-)\otimes X \dashv [X,-])$-[[adjunct]] of the [[identity]] $id_{[X,Y]} : [X,Y] \to [X,Y]$.

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

Let $(\mathcal{C}, \times)$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory})

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

is the $((-)\times X \dashv [X,-])$-[[adjunct]] of the following composite of two [[evaluation maps]], def. \ref{EvalMap}:

$$
  [Y, Z] \times ([X , Y] \times X) 
    \stackrel{(id_{[Y,Z]}, eval_{X,Y})}{\to}
  [Y,Z] \times Y
    \stackrel{eval_{Y,Z}}{\to}
  Z
  \,.
$$

=--

## Properties


### Basic properties
 {#BasicProperties}

The internal homs in a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] (Def. \ref{ClosedMonoidalCategory}) happen to share all the key abstract properties of ordinary ("external") [[hom-functors]], even though this is not completely manifest from Def. \ref{ClosedMonoidalCategory}:


+-- {: .num_prop #InternalHomBifunctor}
###### Proposition
**([[internal hom]] [[bifunctor]])**

Let $\mathcal{C}$ be a [[symmetric monoidal category]] such that for each object $X \in \mathcal{C}$ the  functor $X \otimes (-)$ has a [[right adjoint]] $[X,-]$. Then this is already equivalent to Def. \ref{ClosedMonoidalCategory}, in that there is a unique functor out of the [[product category]] of $\mathcal{C}$ with its [[opposite category]]

$$
  [-,-]
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
    \longrightarrow
  \mathcal{C}
$$

such that for each $X \in \mathcal{C}$ it coincides with the [[internal hom]] $[X,-]$ as a functor in the second variable, and such that there is a [[natural isomorphism]]

$$
  Hom(X, [Y,Z])
  \;\simeq\;
  Hom(X \otimes Y, Z)
$$

which is natural not only in $X$ and $Z$, but also in $Y$.

=--

+-- {: .proof}
###### Proof

We have a natural isomorphism for each fixed $Y$, and hence in particular for fixed $Y$ and fixed $Z$. With this the statement follows directly by [this prop.](https://ncatlab.org/nlab/show/adjoint%20functor#AdjointFunctorFromObjectwiseRepresentingObject) at _[[adjoint functor]]_.

=--


In fact the 3-variable adjunction from Prop. \ref{InternalHomBifunctor} even holds internally:


+-- {: .num_prop #TensorHomAdjunctionIsoInternally}
###### Proposition
**(internal tensor/hom-adjunction)**

In a [[closed monoidal category]] (def. \ref{ClosedMonoidalCategory}) there are [[natural isomorphisms]]

$$
  [X \otimes Y, Z]
   \;\simeq\;
  [X, [Y,Z]]
$$

whose image under $Hom_{\mathcal{C}}(1,-)$  are the defining [[natural bijections]] of Prop. \ref{InternalHomBifunctor}.

=--

+-- {: .proof}
###### Proof

Let $A \in \mathcal{C}$ be any object. By applying the natural bijections from Prop. \ref{InternalHomBifunctor}, there are composite [[natural bijections]]

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(A , [X \otimes Y, Z])
    & \simeq
    Hom_{\mathcal{C}}(A \otimes (X \otimes Y), Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}((A \otimes X)\otimes Y, Z)
    \\
    & \simeq
    Hom_{\mathcal{C}}(A \otimes X, [Y,Z])
    \\
    & \simeq
    Hom_{\mathcal{C}}(A, [X, [Y,Z]])
  \end{aligned}
$$

Since this holds for all $A$, the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]] says that there is an isomorphism $[ X\otimes Y, Z ] \simeq [X, [Y,Z]]$. Moreover, by taking $A = 1$ in the above and using the left [[unitor]] isomorphisms $A \otimes (X \otimes Y) \simeq X \otimes Y$ and $A\otimes X \simeq X$  we get a [[commuting diagram]]

$$
  \array{
    Hom_{\mathcal{C}}(1, [X\otimes Y, Z ])
      &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(1, [X, [Y,Z]])
    \\
    {}^{\mathllap{\simeq}}\downarrow
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    Hom_{\mathcal{C}}(X \otimes Y, Z)
     &\overset{\simeq}{\longrightarrow}&
    Hom_{\mathcal{C}}(X, [Y,Z])
  }
  \,.
$$

=--

Also the key respect of [[hom-functors]] for [[limits]] is inherited by [[internal hom]]-functors:

+-- {: .num_prop #InternalHomPreservesLimits}
###### Proposition
**([[internal hom-functor preserves limits]])**

Let $\mathcal{C}$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with [[internal hom]]-[[bifunctor]] $[-,-]$ (Prop. \ref{InternalHomBifunctor}). Then this bifunctor preserves [[limits]] in the second variable, and sends colimits in the first variable to limits:

$$
  [X, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} Y(j)]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [X, Y(j)]
$$

and

$$
  [\underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j),X]
  \;\simeq\;
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j),X]  
$$


=--


+-- {: .proof}
###### Proof

For $X \in \mathcal{C}$ any object, $[X,-]$ is a [[right adjoint]] by definition, and hence preserves limits by _[[adjoints preserve (co-)limits]]_.

For the other case, let $Y \;\colon\; \mathcal{L} \to \mathcal{C}$ be a [[diagram]] in $\mathcal{C}$, and let $C \in \mathcal{C}$ be any object. Then there are isomorphisms

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(C, [ \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X ] )
    & \simeq
    Hom_{\mathcal{C}}( C \otimes \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X )
    \\
    & \simeq
    Hom_{\mathcal{C}}( \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} (C \otimes Y(j)), X )   
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( (C \otimes Y(j)), X )    
    \\
    & \simeq
    \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim}
    Hom_{\mathcal{C}}( C, [Y(j), X] )    
    \\
    & \simeq
    Hom_{\mathcal{C}}( C, \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] )    
  \end{aligned}
$$

which are [[natural isomorphism|natural]] in $C \in \mathcal{C}$, where we used that the ordinary [[hom-functor]] respects (co)limits as shown (see at _[[hom-functor preserves limits]]_), and that the [[left adjoint]] $C \otimes (-)$ preserves colimits (see at _[[adjoints preserve (co-)limits]]_).

Hence by the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]], there is an isomorphism

$$
  \left[ \underset{\underset{j \in \mathcal{J}}{\longrightarrow}}{\lim} Y(j), X \right]  
  \overset{\simeq}{\longrightarrow}
  \underset{\underset{j \in \mathcal{J}}{\longleftarrow}}{\lim} [Y(j), X] 
  \,.
$$


=--



### Relation to function types

The internal hom is the [[categorical semantics]] of what in [[type theory]] are [[function types]]

[[!include function type natural deduction - table]]

### Induced monad (state monad)

For each object $S$ the (internal hom $\dashv$ [[tensor product]])-[[adjunction]] induces a [[monad]] $[S, S \otimes (-)]$. In [[computer science]] this [[monad (in computer science)]] is called the _[[state monad]]_.

### Stable splitting
  {#StableSplitting}

In [[topology]] the [[stabilization]]/[[suspension spectrum]] $\Sigma^\infty  Maps(X,A)$ of  [[mapping spaces]] $Maps(X,A)$ between suitable [[CW-complexes]] $X, A$ happens to decompose as a [[direct sum]] of [[spectra]] in a useful way, related to the expression of the [[Goodwillie derivatives]] of the functor $Maps(X,-)$. 

For more on this see at _[[stable splitting of mapping spaces]]_.

## Examples
 {#Examples}


### In sets

In the category [[Set]] of [[sets]], regarded as a [[cartesian monoidal category]], the internal hom is given by [[function sets]]. This exists, by the discussion there, as soon as the [[foundations|foundational]] [[axioms]] are strong enough, for instance as soon as there are [[power objects]], which is the special case of a function set into the 2-element set.

### In simplicial sets

In the category [[sSet]] of [[simplicial sets]], the internal hom between two [[simplicial sets]] $X,Y$ is given by the formula

$$
  [X,Y]_n = Hom_{sSet}(X\times \Delta[n],Y)
  \,,
$$

where $\Delta[n]$ is the simplicial [[n-simplex]]. This $[X,Y] \in sSet$ is also called the _[[function complex]]_ between $X$ and $Y$.

Since $sSet \simeq PSh(\Delta)$ is the  [[category of presheaves]] over the [[simplex category]], this is a special case of internal homs in sheaf toposes, discussed [below](#InASheafTopos).

### In a sheaf topos or $(\infty,1)$-sheaf $(\infty,1)$-topos
 {#InASheafTopos}


Let $C$ be a [[site]]. Let $\mathbf{H} = Sh(C)$ be the [[sheaf topos]]
over $C$ or in fact the [[(∞,1)-sheaf (∞,1)-topos]]. We discuss the internal hom of this regard as a [[cartesian monoidal category]]/[[cartesian monoidal (∞,1)-category]].

+-- {: .num_prop}
###### Proposition

The sheaf topos $\mathbf{H}$ is a [[cartesian closed category]] / [[cartesian closed (∞,1)-category]]. In fact it is a [[locally cartesian closed category]] / [[locally cartesian closed (∞,1)-category]].

=--

Hence the internal hom exist.


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

* $U \times X \in \mathbf{H}$ is the [[cartesian product]] of $U$ with $X$

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


### In slice categories
 {#ExampleInSliceCategories}

Let $\mathbf{H}$ be a [[locally cartesian closed category]]. This means that for each object $X \in \mathbf{H}$ the [[slice category]] $\mathbf{H}_{/X}$ is a [[cartesian closed category]]. The [[product]] in the slice is given by the [[fiber product]] over $X$ computed in $\mathbf{H}$. Fairly detailed discussion of constructions of the internal hom in such slices $\mathbf{H}_{/X}$ is at _[locally cartesian closed category -- cartesian closure in terms of base change and dependent product](locally%20cartesian%20closed%20category#EquivalentCharacterizations)_.

We record some further properties

+-- {: .num_prop #InverseImageBaseChangeIsCartesianClosed}
###### Proposition

For $\mathcal{C}$ a [[locally cartesian closed category]] and $f \colon X \to Y$ any morphism in $\mathcal{C}$, the [[inverse image]] $f^*$ of the corresponding [[base change]] [[adjunction]]

$$
  \mathcal{C}_{/X}
   \stackrel{\overset{\sum_f}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{\prod_f}{\to}}}
  \mathcal{C}_{/Y}
$$

is a [[cartesian closed functor]]. 

=--

This is discussed in more detail at _[cartesian closed functor -- Examples](cartesian+closed+functor#Examples)_.

So for $A,B \in \mathcal{C}_{/Y}$ we have [[isomorphisms]]

$$
  f^* \left[A,B\right] \stackrel{\simeq}{\to} \left[f^* A , f^* B\right]
$$

between the image of the internal hom under $f^*$ and the internal hom of the images of $A$ and $B$ separately. 

+-- {: .num_prop #MorphismFromDepProductOfFuncTypeToFuncTypeOfDepSum}
###### Proposition

For $\mathbf{H}$ a [[locally cartesian closed category]], $f \colon X \to Y$ any [[morphism]], and $A, B \in \mathbf{H}_{/X}$ two objects in the slice over $X$, there is a natural morphism (not in general an isomorphism)

$$
  \prod_f \left[A,B \right] \to \left[ \sum_f A, \sum_f B\right]
  \,.
$$

=--

Here are two ways to get this morphism:

+-- {: .proof}
###### Proof/Construction 1

For any object $U \in \mathbf{H}_{/Y}$ we have a canonical morphism of [[hom sets]]

$$
  \begin{aligned}
     \mathbf{H}_{/Y}( U, \prod_f [A,B] )
     & \simeq
     \mathbf{H}_{/X}( f^* U, [A,B] )
     \\
     & \simeq
     \mathbf{H}_{/X}(f^* U \times A, B)
     \\
     & \stackrel{}{\to}
    \mathbf{H}_{/Y}( \sum_f( f^* U \times A ), \sum_f B )
    \\
     & \stackrel{Frob.Rec.}{\simeq}
     \mathbf{H}_{/Y}( U \times \sum_f A , \sum_f B )
     \\
     & \simeq
    \mathbf{H}_{/Y}(U, [\sum_f A , \sum_f B])
  \end{aligned}
$$

where the first and the last steps use [[adjunction]] properties, where the morphism in the middle is the component of the [[dependent sum]] functor, and where "Frob.Rec." is [[Frobenius reciprocity]]. 

Since this is [[natural transformation|natural]] in $U$, the [[Yoneda lemma]] implies the claimed morphism.

=--

+-- {: .proof}
###### Proof/Construction 2

There is the composite morphism

$$
  \left(f^\ast \prod_f [A, B]\right) \times A \stackrel{counit \times id_A}{\to} [A, B] \times A \stackrel{eval}{\to} B \stackrel{unit}{\to} f^\ast \sum_f B$$ 

of the [[unit of an adjunction|adjunction (co)units]] and the [[evaluation map]] of the internal hom. Its hom-[[adjunct]] is


$$
  A \to [f^\ast \prod_f [A, B], f^\ast \sum_f B] \cong f^\ast [\prod_f [A, B], \sum_f B]
  \,,
$$ 

using prop. \ref{InverseImageBaseChangeIsCartesianClosed} on the right. The hom-adjunct of that in turn is


$$\sum_f A \to [\prod_f [A, B], \sum_f B]$$ 

and by symmetry the morphism that we are after:

$$
  \prod_f [A, B] \to [\sum_f A, \sum_f B]
  \,.
$$ 

=--



+-- {: .num_remark #RememberingTopMorphismInHomInSlice}
###### Remark

If $Y$ is the [[terminal object]] (for simplicity), then the morphism of prop. \ref{MorphismFromDepProductOfFuncTypeToFuncTypeOfDepSum} can be understood as follows: a [[global element]] of the [[dependent product]] $\prod_f [A,B]$ is given by a [[commuting diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    \sum_f A &&\to&& \sum_f B
    \\
     & \searrow && \swarrow
     \\
     && X
  }
  \,.
$$

The map in prop. \ref{MorphismFromDepProductOfFuncTypeToFuncTypeOfDepSum} picks out the top horizontal morphism in this diagram.

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

The category $sVect$ of [[super vector spaces]] is the category of $\mathbb{Z}/2$-[[graded vector spaces]].  Thus, its objects are pairs of vector spaces $(V_+,V_-)$, with $V_+$ called the *even* part and $V_-$ the *odd* part.  The morphisms in $sVect$ are likewise pairs of linear maps, i.e. we define $sVect$ to be $Vect \times Vect = Vect^{\mathbb{Z}/2}$, as usual for any sort of graded object.  With this definition of the category $sVect$, we capture the concepts of superalgebra and so on in succinct categorical terms.

Because the morphisms in $sVect$ send even things to even things and odd things to odd things, they are sometimes called _even_ linear maps, and one may write
$$
 sVect(V, W) = Even Lin(V,W).
$$
Note that $sVect$ is [[enriched category|enriched]] over $Vect$, i.e. these hom-sets are vector spaces.

Occasionally, however, one does need to refer to the _odd_ linear maps, which send even things to odd things and odd things to even things.  That is, an odd linear map $V\to W$ is a pair of linear maps $V_+ \to W_-$ and $V_-\to W_+$.  The internal-hom in $sVect$ allows us to capture these as well: it is the following super vector space:
$$
  [V,W]_+ = Even Lin(V,W) \qquad
  [V,W]_- = Odd Lin(V,W).
$$
With this definition, $sVect$ becomes a [[closed monoidal category]].

We can equivalently regard a super vector spaces $(V_+,V_-)$ as being the [[direct sum]] vector space $V_+ \oplus V_-$ equipped with this direct sum decomposition.  If we view the internal-hom $[V,W]$ in this way as well, then we have
$$
 [V, W] = Even Lin(V,W) \oplus Odd Lin(V,W) = Lin(V,W).
$$
In other words, any linear map between these "summed" super vector spaces decomposes uniquely as the sum of an even linear map and an odd one.


### For Banach spaces

A similar thing happens in the category $Ban$ of [[Banach spaces]] and [[short linear operators]].  The external hom consists of only the *short* linear maps (those bounded by $1$):
$$ Ban(V,W) = \{ f\colon Lin(V,W) \;|\; {\|f\|} \leq 1 \} .$$
This definition of morphism recovers the most specific notion of [[isomorphism]] of Banach spaces, as well as defining the [[product]] and [[coproduct]] as the [[direct sum]] completed with $p = \infty$ or $p = 1$ respectively.

But the internal hom is the Banach space of *all* bounded linear maps:
$$ [V,W] = \{ f\colon Lin(V,W) \;|\; {\|f\|} \lt \infty \} .$$
This is a Banach space and makes $Ban$ into a [[closed category]].



## Related concepts

* [[hom-set]], [[hom-object]]

* [[hom-functor]]

* [[enriched hom-functor]]

* [[derived hom-functor]]

* [[function type]]

  * [[implication]], [[linear implication]]

* [[power object]], [[exponential object]]

* [[function monad]]

* [[exponential law for spaces]]

* [[closed category]], [[cartesian closed category]]

* [[strong adjoint functor]]

* [[mapping stack]]

* [[space of sections]]

* [[pointed mapping space]]

* [[distributions are the smooth linear functionals]]

* [[Sullivan model of mapping space]]

* [[residual]]

## References

See any reference on [[closed categories]] and [[closed monoidal categories]].

Also for instance:

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 



[[!redirects internal homs]]
[[!redirects inner hom]]
[[!redirects inner homs]]
[[!redirects internal-hom]]
[[!redirects internal-homs]]

[[!redirects mapping object]]
[[!redirects mapping objects]]


[[!redirects exponential law]]
[[!redirects exponential laws]]

[[!redirects internal hom-functor]]
[[!redirects internal hom-functors]]
[[!redirects internal hom functor]]
[[!redirects internal hom functors]]



