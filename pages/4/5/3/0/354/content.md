
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

A _Kan complex_ is an abstraction of the combinatorial structure found in the [[singular simplicial complex]] of a [[topological space]]. There, the existence of [[retractions]] of any geometric [[simplex]] to any of its [[horns]] -- simplices missing one face and their interior -- means that all [[horns]] in the singular simplicial complex can be filled with genuine simplices. This is the _Kan filler condition_.

At the same time, a Kan complex is an abstraction of the structure found in the [[nerve]] of a [[groupoid]], the [[Duskin nerve]] of a [[2-groupoid]] and generally (almost by definition, see at _[[cobordism hypothesis]]_) the nerves of [[n-groupoids]] for all $n \leq \infty$. In other words, Kan complexes constitute a [[geometric definition of higher category|geometric model]] for [[∞-groupoids]]/[[homotopy types]] which is based on the [[geometric shapes for higher structures|shape]] given by the [[simplex category]] (as opposed to, say, the [[globe category]], as for what are usually called [[∞-groupoids]]). Thus, Kan complexes serve to support [[homotopy theory]].

In more detail, a Kan complex is a collection of $k$-[[simplex]]-shaped [[k-morphism]]s for all $k \in \mathbb{N}$, such that for all composable $k$-morphisms a composite does exist (not necessarily uniquely) and  such that all $k$-morphisms are invertible under this composition.


Specifically for the [[nerve]] $N(\mathcal{G}_\bullet)$ of a [[groupoid]] $\mathcal{G}_\bullet$, a $k$-cell is given by a sequence of [[morphisms]] of the form $\{0\to 1\to \ldots \to k\}$, thought of as a $k$-[[simplex]] by taking its $(k-1)$-faces to be the the sequences obtained from this by deleting the first or the last morphism or by composing two consecutive morphisms in the sequence. 

Hence, in a Kan complex, a $k$-face of a $(k+1)$-[[simplex]] may be thought of as the [[composition]] of the remaining faces, all regarded as [[k-morphisms]]. But, unless the Kan complex is the [[nerve]] of a [[groupoid]] (a [[1-groupoid]]), the composite of a morphism is not generally unique. Indeed, _choosing_ one of the fillers of each horn in a Kan complex to be _the_ composite means passing from Kan complexes to an [[algebraic definition of higher category|algebraic model]] for [[∞-groupoids]], _[[algebraic Kan complexes]]_.

Among all [[∞-groupoids]], the [[strict ∞-groupoids]] correspond to [[crossed complexes]] and various other related algebraic models, all or most of which have a [[full subcategory|faithful embedding]] into Kan complexes under a suitable [[nerve]] operation. One of these are the [[simplicial T-complexes]], the nerves of crossed complexes. There, all horns have unique 'thin' fillers, so these are Kan complexes corresponding to a strict form of higher-dimensional groupoid. 


 

## Definition


+-- {: .num_defn #KanComplexes}
###### Definition

A _Kan complex_ is a [[simplicial set]] $S$ that satisfies the _Kan condition_, which says that 

* all [[horns]] of $S$ have [[filler]]s (that is, extend to [[simplices]]);

* equivalently, the unique homomorphism $S \to pt$ from $S$ to the [[point]] (the [[terminal object|terminal]] [[simplicial set]]) is a [[Kan fibration]];

* equivalently, for all [[diagrams]] of the form

  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && 
    \\
    \Delta[n] 
  }
  $$

  there exists a diagonal morphism

  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& 
    \\
    \Delta[n] 
  }
  $$

  completing this to a [[commuting diagram]];

* equivalently, the map from $n$-simplices to $(n,i)$-horns is an [[epimorphism]]
$$
  [\Delta[n], S]\, \twoheadrightarrow \,[\Lambda^i[n],S]
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

The last characterization in def. \ref{KanComplexes} is 
sometimes taken to induce the generalization to [[internalization|internal]] 
Kan complexes in ambient geometric contexts. 
For instance, the generalization of [[Lie groupoids]] to
"Lie Kan complexes" 
might be defined to be given by [[simplicial objects]] in 
the [[category]] [[SmoothMfd]] of [[smooth manifolds]] 
such that the morphisms

$$
  [\Delta[n], S] \to [\Lambda^i[n],S]
$$

are _[[surjective submersions]]_.

While this is useful for some purposes, one should beware that this naive generalization, if taken at face value, may break the [[homotopy theory|homotopy-theoretic]] interpretation of (say, smooth) Kan complexes as models for (say, [[smooth infinity-groupoid|smooth]]) [[∞-groupoids]]. A homotopy-good theory of Lie Kan complexes is discussed in ([NSS, section 4.2](#NSSb)).
See at _[[internal ∞-groupoid]]_ for more.

=--

+-- {: .num_remark}
###### Remark

Some special cases of def. \ref{KanComplexes} go by their own terminology:

* a Kan complex such that, for every $k \gt n+1$, every $k$-[[boundary]] $\partial \Delta$ has a unique [[filler]] is called $(n+1)$-[[simplicial skeleton|coskeletal]];

* a Kan complex that is $(n+1)$-[[coskeleton|coskeletal]] such that, in addition, the $(n+1)$-[[horns]] and $(n+2)$-[[horns]] have a unique filler are also called _[[hypergroupoid|n-hypergroupoids]]_.

These $(n+1)$-coskeletal Kan complexes are models for [[n-groupoids]]/[[homotopy n-types]]/[[n-truncated object in an (infinity,1)-category|n-truncated]] [[∞-groupoids]].

=--



## As models for $\infty$-groupoids
 {#AsGrpds}

Here, we discuss aspects of how _Kan complexes_ serve as a model (a "[[geometric definition of higher categories|geometric model]]") for [[groupoids]], [[2-groupoids]], ... [[n-groupoids]] and generally _[[∞-groupoids]]_ or _[[homotopy types]]_. 


First, we survey the general idea in 

* [Heuristics on composition and inverses](#HeuristicsOnCompositionAndInverses).

Then, we recall 1-[[groupoids]] as Kan complexes via their [[nerves]] in

* [1-Groupoids as Kan complexes](#1GroupoidsAsKanComplexes).

Then, we discuss basic aspects of the

* [Homotopy theory of ∞-groupoids as Kan complexes](#HomotopyTheoryOfKanComplexes).


+-- {: .num_remark}
###### Remark

This is a special case of how [[weak Kan complexes]] ([[quasi-categories]]) are a model for [[(∞,1)-categories]].

=--

+-- {: .num_remark}
###### Remark

The horn filling condition from this point of view is read as guaranteeing that:

for all collections of $k-1$ composable [[k-morphisms]] (given by a horn $\Lambda^k[n]$), there exists a [[k-morphism]] -- their _composite_ -- and an $(n+1)$-morphism connecting the original $n-1$ $n$-cells with their composite. Depending on $k$, this interpretation in terms of composition implies that one thinks of all cells as being reversible. 

For illustrations of the horn-[[filler]] conditions see also at [[Kan fibration]].


=--



+-- {: .num_remark}
###### Remark

Whatever other definition of [[∞-groupoid]] one considers, it is expected (and in most cases has been shown) to map to a Kan complex under the [[nerve]]. See at _[[homotopy hypothesis]]_ for more on this.

=--

+-- {: .num_remark}
###### Remark

Of all the models for [[∞-groupoids]] known in the literature, Kan complexes are probably the most widely used, certainly in [[homotopy theory]] and related "geometric" approaches to [[higher category]] (such as in terms of [[n-fold complete Segal spaces]] etc.), less so in "algebraic" approaches to [[higher category theory]]. To a large extent, this is because the category of Kan complexes -- particularly when thought of as the full sub-[[category of fibrant objects]] inside the standard [[model structure on simplicial sets]] -- lends itself usefully to many computations. To some extent, it is maybe a historical coincidence that the theory was worked out in such detail for this model specifically. Maybe if [[Daniel Kan|Kan]] -- who first tried [[cubical sets]] and then rejected them in favor of [[simplicial sets]] due to some technical issues -- had tried [[connection on a cubical set|cubical sets with connection]] first, things would have developed differently. See at _[[cubical set]]_ for discussion of this issue.

But, in any case, it seems clear that there is no "fundamental" conceptual reason to prefer Kan complexes over other models for [[∞-groupoids]]. Instead, in view of modern developments, it seems right to regard the abstract concept of [[homotopy type]] (not as an [[equivalence class]], but as a representative) as fundamental, and everything else to be "just a model" for this, which may or may not be useful for a particular computation. This point of view is formalized by the [[univalent foundations]] of mathematics in terms of [[homotopy type theory]]. There, the [[theory]] of [[homotopy types]] is given as an abstract foundational notion, and then [[Kan complexes]] and related structures are shown to be a [[model]]. For more on this, see at _[[homotopy type theory]]_.


=--

### Heuristics on composition and inverses
 {#HeuristicsOnCompositionAndInverses}

An [[∞-groupoid]] is primarily supposed to be a structure that consists of [[k-morphism]]s for all $k \in \mathbb{N}$, which, for $k \geq 1$, go between $(k-1)$-morphisms. 

In the context of Kan complexes, the tool for organizing such collections of [[k-morphisms]] is the notion of a _[[simplicial set]]_, which models $k$-morphisms as being of the [[geometric shape for higher structures|shape]] of $k$-[[simplices]] -- a [[vertex]] for $k = 0$, an [[edge]] for $k = 1$, a [[triangle]] for $k = 2$, a [[tetrahedron]] for $k = 3$, and so on. 

This means that a simplicial set $K_\bullet$ is a sequence of [[sets]] $\{K_n\}_{n \in \mathbb{N}}$ (sets of $k$-simplex shaped $k$-morphisms for all $k$) equipped with [[functions]] $d_i \colon K_{k+1} \to K_{k}$ that send a $(k+1)$-simplex to its $i$-th face, and functions $s_i \colon K_k \to K_{k+1}$ that, over a $k$-simplex, "erects a flat $(k+1)$-simplex" in all possible ways (hence which inserts "[[identities]]" called "degeneracies" in this context).

If we write $\Delta$ for the [[category]] whose [[objects]] are abstract cellular [[simplices]] and whose morphisms are all cellular maps between these, then such a simplicial set is equivalently a [[functor]] of the form

$$
  K \colon \Delta^{op} \to Set
$$

Hence, we think of this as assigning

* a set $[0] \mapsto K_0$ of [[objects]];

* a set $[1] \mapsto K_1$ of [[morphism]];

* a set $[2] \mapsto K_2$ of [[2-morphism]];

* a set $[3] \mapsto K_3$ of [[3-morphism]];

and generally

* a set $[k] \mapsto K_k$ of [[k-morphism]]s,

as well as specifying

* functions $([n] \hookrightarrow [n+1]) \mapsto (K_{n+1} \to K_n)$
  that send $n+1$-morphisms to their boundary $n$-morphisms;

* functions $([n+1] \to [n]) \mapsto (K_{n} \to K_{n+1})$
  that send $n$-morphisms to [[identity]] $(n+1)$-morphisms
  on them.

The fact that $K$ is supposed to be a [[functor]] enforces that these assignments of sets and functions satisfy conditions that make consistent our interpretation of them as sets of $k$-morphisms and source and target maps between these. 
These are called the _[[simplicial identities]]_.

But, apart from this source-target matching, a generic simplicial set does not yet encode a notion of [[composition]] of these morphisms. 

For instance, for $\Lambda^1[2]$ the simplicial set consisting of two attached 1-cells 

$$
  \Lambda^1[2] = \left\{
    \array{
       && 1
       \\
       & \nearrow && \searrow
       \\
       0 &&&& 2
    }
  \right\}
$$

and for $(f,g) : \Lambda^1[2] \to K$ an image of this situation in $K$, hence a pair $x_0 \stackrel{f}{\to} x_1 \stackrel{g}{\to} x_2$ of two _composable_ 1-morphisms in $K$, we want to demand that there exists a third 1-morphism in $K$ that may be thought of as the [[composition]] $x_0 \stackrel{h}{\to} x_2$ of $f$ and $g$. But since we are working in [[higher category theory]] (and to adhere to the [[principle of equivalence]]), we want to identify this composite only up to a [[2-morphism]] equivalence

$$
    \array{
       && x_1
       \\
       & {}^{\mathllap{f}}\nearrow &\Downarrow^{\mathrlap{\simeq}}& 
       \searrow^{\mathrlap{g}}
       \\
       x_0 &&\stackrel{h}{\to}&& x_2
    }
  \,.
$$

From the picture, it is clear that this is equivalent to demanding that, for $\Lambda^1[2] \hookrightarrow \Delta[2]$ the obvious inclusion of the two abstract composable 1-morphisms into the 2-simplex, we have a diagram of morphisms of simplicial sets

$$
  \array{
    \Lambda^1[2] &\stackrel{(f,g)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists h}}
    \\
    \Delta[2]
  }
  \,.
$$

A simplicial set where, for all such $(f,g)$, a corresponding such $h$ exists may be thought of as a collection of higher morphisms that is equipped with a notion of composition of adjacent 1-morphisms. 

For the purpose of describing [[groupoid]]al composition, we now want this composition operation to have all [[inverse]]s. For that purpose, notice that for 

$$
  \Lambda^2[2] = \left\{
    \array{
       && 1
       \\
       & && \searrow
       \\
       0 &&\to&& 2
    }
  \right\}
$$

the simplicial set consisting of two 1-morphisms that touch at their end, hence for 

$$
  (g,h) : \Lambda^2[2] \to K
$$

two such 1-morphisms in $K$, if $g$ had an inverse $g^{-1}$, then we could use the above composition operation to compose that with $h$ and thereby find a morphism $f$ connecting the sources of $h$ and $g$. This being the case is evidently equivalent to the existence of diagrams of morphisms of simplicial sets of the form

$$
  \array{
    \Lambda^2[2] &\stackrel{(g,h)}{\to}& K
    \\
    \downarrow & \nearrow_{\mathrlap{\exists f}}
    \\
    \Delta[2]
  }
  \,.
$$

Demanding that all such diagrams exist is therefore demanding that we have an invertible composition operation on 1-morphisms in $K$. 

In order for this to qualify as an $\infty$-groupoid, this composition operation needs to satisfy an [[associativity law]] up to [[coherent]] [[2-morphisms]], which means that we can find the relevant [[tetrahedron|tetrahedra]] in $K$. These, in turn, need to be connected by _pentagonators_, and so on.  It is a nontrivial but true and powerful fact that all these [[coherence]] conditions are captured by generalizing the above conditions to all dimensions as in the definition of Kan complexes.

In order to conceive of the $k$-[[simplices]] for higher $k$ as "[[globular set|globular]] [[k-morphism|k-morphisms]]" going from a source to a target, one needs a bit of combinatorics. This is provided by the _[[orientals]]_ (due to [[Ross Street]]).

{#Oriental} The $k$-[[oriental]] $O(k)$ is precisely the prescription for how exactly to think of a $k$-[[simplex]] as being a [[k-morphism]] in an [[omega-category]]. 






[[!include the first few orientals]]






In fact, the [[omega-nerve]] $N(K)$ of an [[omega-category]] $K$ is the [[simplicial set]] whose collection of $k$-cells $N(K)_k := Hom(O(k),K)$ is precisely the collection of images of the $k$th oriental $O(k)$ in $K$.

Here is the fully formal prescription of how to think of a Kan complex as an $\infty$-groupoid:

* The Kan complex $C$ is the [[omega-nerve]] of an [[omega-category]] in which all morphism are invertible;

* The $k$-cells in  $C_k$ are precisely the $k$-morphisms in the omega-category of shape the $k$th [[oriental]] $O(k)$;

* The [[horn]]-filler conditions satisfied by these cells are precisely a reflection of the fact that

  1. there exists a notion of composition of adjacent k-morphisms in the [[omega-category]]; and

  1. under this composition, all $k$-morphisms have an inverse.

This is easy to see in low dimensions: 

* a 1-cell $\phi \in C_1$ in the [[simplicial set]] $C$ has a single source 0-cell $x := d_1 \phi$ and a single target 0-cell $y := d_0 \phi$, and thus may be pictured as a [[morphism]]

  $$
    x \stackrel{\phi}{\to} y
    \,.
  $$

* a 2-cell $\phi \in C_2$ in the [[simplicial set]] $C$ has two incoming 1-cells $d_2 \phi, d_0 \phi \in C_1$ and one outgoing 1-cell $d_1 \phi \in C_1$, and if we think of the two incoming 1-cells as representing the composite of the corresponding 1-morphisms, we may picture the 2-cell $\phi$ as a globular 2-morphism

  $$
    \array{
      && x_1
      \\
      & {}^{\mathllap{d_2 \phi}}\nearrow &\Downarrow^\phi& \searrow^{\mathrlap{d_0 \phi}}
      \\
      x_0 &&\underset{d_1 \phi}{\to}&& x_2
    }
    \,.
  $$

In more detail, one may think of the two adjacent incoming $1$-cells _not_ as being the composite of these two morphisms, but just as a [[composable pair]], and one should think of the 2-morphism $\phi$ as being a **compositor** in a [[bicategory]] that shows how the composable pair is composed to the morphism $d_1 \phi$.

So, if an $\infty$-groupoid is thought of as a [[geometric shapes for higher structures|globular]] [[Batanin ∞-category| ∞-category]] in which all [[k-morphism]]s are invertible, then the corresponding Kan complex is the [[nerve]] (or rather the [[∞-nerve]]) of this [[∞-category]].

Notably, if $C$ is to be regarded as (the nerve of) an ordinary [[groupoid]], then every composable pair of morphisms has a unique composite, and hence there should be a _unique_ 2-cell

  $$
    \array{
      && x_1
      \\
      & {}^{f}\nearrow &\Downarrow& \searrow^{g}
      \\
      x_0 &&\underset{h = g \circ f}{\to}&& x_2
    }
  $$

that is the unique **identity 2-morphism**

$$
  g \circ f \stackrel{=}{\Rightarrow} h
  \,.
$$

More generally, in a [[2-groupoid]], there may be non-identity 2-morphisms, and hence, for any 1-morphism $k \colon x_0 \to x_2$ 2-isomorphic to $h$, there may be many 2-morphisms $g \circ f \Rightarrow k$, and hence many 2-cells

$$
  \array{
    && x_1
    \\
    & {}^{f}\nearrow &\Downarrow^{\simeq}& \searrow^{g}
    \\
    x_0 &&\underset{k }{\to}&& x_2
  }
  \,.
$$

All we can say for sure is that _at least_ one such 2-cell exists, and that the 2-cells themselves may be composed in some way. This is precisely what the horn filler conditions in a Kan complex encode.

We have already seen in low dimension how the existence of composites in an $\omega$-category is reflected by the fact that, in a Kan-complex, certain 2-simplices exist, and how the non-uniqueness of these 2-simplices reflects the existence of nontrivial 2-morphisms.

To see in a similar fashion that the Kan condition ensures the existence of _inverses_, consider an _outer horn_ in $C$, a diagram of 1-cells of the form

$$
  \array{
    && x_1
    \\
    & {}^{\mathllap{f}}\nearrow
    \\
    x_0 &&\underset{h}{\to}&& x_2
  }
  \,.
$$

In general, given such a diagram in a [[category]], there is no guarantee that the corresponding triangle as above will exist in its [[nerve]]. But, if the category is a [[groupoid]], then it is guaranteed that the missing 1-face can be chosen to be the [[inverse]] of $f$ composed with the morphism $h$, and there is at least one 2-morphism

$$
  \array{
    && x_1
    \\
    & {}^{\mathllap{f}}\nearrow
    &\Downarrow^{\simeq}& \searrow^{\mathrlap{h \circ f^{-1}}}
    \\
    x_0 &&\underset{h}{\to}&& x_2
  }
  \,.
$$

A similar analysis for higher dimensional cells shows that the fact that a Kan complex has all horn fillers encodes precisely the fact that it is the [[omega-nerve]] of an [[omega-category]] in which _all_ [[k-morphism]]s for all $k$ are composable if adjacent and have a weak inverse.


### 1-Groupoids as Kan complexes
 {#1GroupoidsAsKanComplexes}

We review how [[1-groupoids]] are incarnated as Kan complexes via their [[nerve]].

+-- {: .num_defn #Groupoid}
###### Definition

A ([[small category|small]]) _[[groupoid]]_ $\mathcal{G}_\bullet$ is

* a pair of [[sets]] $\mathcal{G}_0 \in Set $ (the set of [[objects]]) and $\mathcal{G}_1 \in Set$ (the set of [[morphisms]])

* equipped with [[functions]]

  $$
    \array{
      \mathcal{G}_1 \times_{\mathcal{G}_0} \mathcal{G}_1
      &\stackrel{\circ}{\to}&
      \mathcal{G}_1
      & \stackrel{\overset{t}{\to}}{\stackrel{\overset{i}{\leftarrow}}{\underset{s}{\to}}}&
      \mathcal{G}_0
    }\,,
  $$

  where the [[fiber product]] on the left is that over $\mathcal{G}_1 \stackrel{t}{\to} \mathcal{G}_0 \stackrel{s}{\leftarrow} \mathcal{G}_1$, 

such that

* $i$ takes values in [[endomorphisms]];

  $$
    t \circ i = s \circ i =   id_{\mathcal{G}_0}, \;\;\; 
  $$

* $\circ$ defines a partial [[composition]] operation which is [[associativity|associative]] and [[unitality|unital]] for $i(\mathcal{G}_0)$ the [[identities]]; in particular

  $s (g \circ f) = s(f)$ and $t (g \circ f) = t(g)$;

* every morphism has an [[inverse]] under this composition.

=--


+-- {: .num_defn #NerveOfGroupoid}
###### Definition

For $\mathcal{G}_\bullet$ a [[groupoid]], def. \ref{Groupoid}, we write

$$
  \mathcal{G}_n \coloneqq \mathcal{G}_1^{\times_{\mathcal{G}_0}^n}
$$ 

for the set of sequences of composable morphisms of length $n$, for $n \in \mathbb{N}$; schematically:

$$
  \mathcal{G}_n = 
  \left\{
    x_0 
      \stackrel{f_1}{\to} 
    x_1
      \stackrel{f_2}{\to}
    x_2
      \stackrel{f_2}{\to}
    \cdots
      \stackrel{f_n}{\to}
    x_n
  \right\}
  \,.
$$

For each $n \geq 1$, the two maps $d_0$ and $d_n$ that forget the first and the last morphism in such a sequence and the $n-1$ maps $d_k$ that form the composition of the $k$th morphism in the sequence with the next one constitute $(n+1)$ [[functions]] denoted

$$
  d_k \colon \mathcal{G}_n \to \mathcal{G}_{n-1}
  \,.
$$

Moreover, the assignments $s_i$ that insert an [[identity]] morphism in position $i$ constitute [[functions]] denoted

$$
  s_i \colon \mathcal{G}_{n-1} \to \mathcal{G}_n
  \,.
$$

=--

+-- {: .num_prop #NerveOfGroupoidIsKanComplex}
###### Proposition

These collections of maps in def. \ref{NerveOfGroupoid} satisfy the [[simplicial identities]], and hence make the [[nerve]] $\mathcal{G}_\bullet$ into a [[simplicial set]]. Moreover, this simplicial set is a Kan complex where each $n \geq 2$-[[horn]] has a _unique_ filler (extension to a [[simplex]]).

=--

(A 2-[[simplicial coskeleton|coskeletal]] Kan complex.)


+-- {: .num_prop }
###### Proposition

The [[nerve]] operation constitutes a [[full and faithful functor]]

$$
  N \colon Grpd \to KanCplx \hookrightarrow sSet
  \,.
$$


=--


### Homotopy theory of $\infty$-groupoids as Kan complexes
 {#HomotopyTheoryOfKanComplexes}


+-- {: .num_defn }
###### Definition

Write 

$$
  KanCplx \hookrightarrow sSet
$$

for the [[category]] of Kan complexes, which is the [[full subcategory]] of that of [[simplicial sets]] on the Kan complexes.

=--

+-- {: .num_remark }
###### Remark

This means that, for $X_\bullet,Y_\bullet \in KanCplx$ two Kan complexes, an element $f_\bullet \colon X_\bullet \to Y_\bullet$ in the [[hom-set]] $Hom_{KanCplx}(X_\bullet,Y_\bullet)$ is 

* a sequence of [[functions]] $f_n \colon X_n \to Y_n$ for all $n \in \mathbb{N}$;

such that

* these respect all the face maps $d_k$ and the degeneracy maps $s_k$.

=--


+-- {: .num_defn #MappingObjectOfKanComplexes}
###### Definition

For $X_\bullet,Y_\bullet \in KanCplx$ two Kan complexes, their [[mapping space]]

$$
  Maps(X_\bullet,Y_\bullet)_\bullet \in KanCplx
$$

is the [[simplicial set]] given by 

$$
  Maps(X_\bullet,Y_\bullet) \colon [n] \mapsto Hom_{sSet}(X_\bullet \times \Delta^n_\bullet, Y_\bullet)
  \,.
$$

=--


+-- {: .num_prop }
###### Proposition

The construction in def. \ref{MappingObjectOfKanComplexes} defines an [[internal hom]] of Kan complexes. 

=--

+-- {: .num_remark }
###### Remark

As such, it is also common to write $Y^X$ for $Maps(X,Y)$, as well as $[X,Y]$. Notice that the latter notation is sometimes used instead for just the set of [[connected components]] of $Maps(X,Y)$.

=--

+-- {: .num_example #PathSpaceObjectOfKanComplexes}
###### Example

Write 

$$
  I_\bullet \coloneqq \{0 \stackrel{\simeq}{\to} 1\}
$$

for the Kan complex which is a [[1-groupoid]] with two objects and one nontrivial morphism and its inverse between them. This comes with two inclusions

$$
  i_0, i_1 \colon \ast \to I
$$

of its endpoints.

Then, for $X_\bullet \in KanCplx$ any other Kan complex, the [[mapping space]] $[I,X]_\bullet$ from def. \ref{MappingObjectOfKanComplexes} is the [[path space object]] of $X_\bullet$. 

$$
  X_\bullet \stackrel{[i_0,X_\bullet]}{\leftarrow} [I_\bullet,X_\bullet]_\bullet \stackrel{[i_1,X]}{\to} X_\bullet
  \,.
$$

=--

A 1-cell in the mapping Kan complex $[X_\bullet, Y_\bullet]_\bullet$ is a [[homotopy]] between two morphisms of Kan complexes:

+-- {: .num_defn }
###### Definition

For $f_\bullet, g_\bullet \colon X_\bullet \to Y_\bullet$ two morphisms between two Kan complexes, hence $f_\bullet,g_\bullet \in Hom_{KanCplx}(X,Y)$, a (right-)[[homotopy]] $\eta \colon f \Rightarrow g$ is a morphism $\eta_\bullet \colon X_\bullet \to [I_\bullet,X_\bullet]_\bullet$ into the [[path space object]] of def. \ref{PathSpaceObjectOfKanComplexes} such that we have a [[commuting diagram]]

$$
  \array{
    && Y_\bullet
    \\
    & {}^{\mathllap{f_\bullet}}\nearrow & \uparrow^{\mathrlap{[i_0, X_\bullet]_\bullet}}
    \\
    X_\bullet &\stackrel{\eta_\bullet}{\to}& [I_\bullet, Y_\bullet]   
    \\
    & {}_{\mathllap{g_\bullet}}\searrow & \downarrow_{\mathrlap{[i_1, X_\bullet]_\bullet}}
    \\
    &&  Y \bullet
  }
  \,.
$$

=--

It follows that the category $KanCplx$ is naturally [[enriched category|enriched]] over itself. 

We may write [[∞Grpd]] for $KanCplx$ regarded as a $KanCplx$-[[enriched category]], hence as a fibrant [[sSet-enriched category]]. We write $X$ (without the subscript) for a Kan complex $X_\bullet$ regarded as an object of $\infty Grpd$.




## Properties

### Model category

Kan complexes are the [[fibrant objects]] in the _[[model structure on simplicial sets|model structures on simplicial sets]]_ for which the fibrations are [[Kan fibration|Kan fibrations]].

In this context, a weak equivalence between Kan complexes is a morphism of simplicial sets that induces an [[isomorphism]] on the [[simplicial homotopy groups]] of the two Kan complexes: a _[[weak homotopy equivalence]]_.



## Examples

### Kan complexes from nerves of $n$-groupoids 

+-- {: .un_prop}
###### Proposition

The [[nerve]] $N(C)$ of a [[small category]] 
is a Kan complex if and only if $C$ is a [[groupoid]].

=--

The existence of [[nLab:inverse|inverse]] morphisms in $D$ corresponds to the fact that, in the [[Kan complex]] $N(D)$, the "outer" [[horns]]

$$
  \array{
    && d_0
    \\
    & && \searrow^{f}
    \\
    d_1 &&\stackrel{Id_{d_1}}{\to} && d_1
  }
  \;\;\; 
  \;\;\; 
  and
  \;\;\; 
  \;\;\; 
  \array{
    && d_1
    \\
    & {}^f\nearrow &&     
    \\
    d_0 &&\stackrel{Id_{d_0}}{\to} && d_0
  }
$$

have fillers 

$$
  \array{
    && d_0
    \\
    & {}^{f^{-1}}\nearrow&& \searrow^{f}
    \\
    d_1 &&\stackrel{Id_{d_1}}{\to} && d_1
  }
  \;\;\; 
  \;\;\; 
  and
  \;\;\; 
  \;\;\; 
  \array{
    && d_1
    \\
    & {}^f\nearrow && \searrow^{f^{-1}}
    \\
    d_0 &&\stackrel{Id_{d_0}}{\to} && d_0
  }
$$

(even unique fillers, due to the properties of the [[nerve]] of an ordinary category).

This is one way to see and motivate that a simplicial set that is a [[Kan complex]] but which does not necessarily have unique fillers models an [[∞-groupoid]].

Accordingly

+-- {: .un_prop}
###### Proposition

The [[nerve]] $N(C)$ of a [[strict ∞-category]] 
is a Kan complex if and only if $C$ is a [[strict ∞-groupoid]].

=--


### Kan complexes from simplicial groups

The underlying simplicial set of a [[simplicial group]] (see there) is a Kan complex. 

In particular, via the [[Dold-Kan correspondence]] (see there)

$$
  Ch_{\bullet \geq 0}
  \underoverset{\simeq}{DK}{\to}
  sAb
  \stackrel{forget}{\to}
  KanCplx
  \hookrightarrow 
  sSet
$$

every [[chain complex]] (of abelian groups, in non-negative degree) is equivalent to a [[simplicial abelian group]] and this has an underlying Kan complex. This way, [[homological algebra]] becomes a special case of the study of [[homotopy theory]] (of Kan complexes).


### Simplicial models of Mal'cev theories 

Generalizing the example of simplicial groups: if $T$ is any [[Mal'cev theory]], i.e., a [[Lawvere theory]] which admits a Mal'cev operation $t$, then any $T$-algebra in simplicial sets, given by a [[product-preserving functor]] $A: T \to Set^{\Delta^{op}}$, is a Kan complex. ([Source](http://www.tac.mta.ca/tac/reprints/articles/12/tr12.pdf#270)) 

For example, the [[subobject classifier]] $\Omega$ in simplicial sets is a Kan complex because it is an internal [[Heyting algebra]], and the theory of Heyting algebras is Mal'cev. 

It is not hard to imagine how the proof might go, by adapting the proof in the special case of simplicial groups, replacing occurrences of elements of the form $x y^{-1} z$ by values $t(x, y, z)$ of a chosen Mal'cev operation. 

+-- {: .num_remark} 
###### Remark 
Somewhat more generally, for any [[Mal'cev category]] $C$, a simplicial object $\Delta^{op} \to C$ satisfies the Kan condition. This was shown by [Carboni, Kelly, and Pedicchio](#CKP). 
=-- 


### Singular simplicial complexes / fundamental $\infty$-groupoids

For $X$ a [[topological space]], its _[[singular simplicial complex]]_ is the [[simplicial set]] $\Pi(X)$ (often denoted  $S(X)$ or $Sing(X)$) whose set of $n$-simplices is the [[hom-set]]

$$
  \Pi(X)_n := Top(\Delta^n_{Top}, X)
$$

in [[Top]] of continuous maps from the standard topological $n$-simplex $\Delta^n_{Top}$ into $X$.

Using the fact that the $\Delta^n_{Top}$'s arrange themselves into a [[simplicial object|cosimplicial space]]

$$
  \Delta_{Top} : \Delta \to Top
$$

in the obvious way, the $\Pi(X)_n$'s form a [[simplicial set]] in the corresponding obvious way. For instance, the face maps are induced by restricting maps to $X$ along the face inclusions $\delta^i : \Delta^{n-1} \hookrightarrow \Delta^n$.

That $\Pi(X)$ is indeed a Kan complex is intuitively clear. Technically, it follows from the fact that the inclusions ${{\Lambda^n}_{Top}}_k \hookrightarrow \Delta^n_{Top}$ of topological horns into topological simplices are 
[[retracts]], in that there are continuous maps $\Delta^n_{Top} \to {{\Lambda^n}_{Top}}_k$ given by "squashing" a topological $n$-simplex onto parts of its boundary such that
$$
  ({{\Lambda^n}_{Top}}_k \to \Delta^n_{Top} \to
  {{\Lambda^n}_{Top}}_k)
  =
  Id
  \,.
$$
Therefore, the map
$[\Delta^n, \Pi(X)] \to [\Lambda^n_k,\Pi(X)]$ is an epimorphism, since it is equal to the map $Top(\Delta^n, X) \to Top(\Lambda^n_k, X)$ which has a right inverse $Top(\Lambda^n_k, X) \to Top(\Delta^n, X)$.


The [[∞-groupoid]] represented by the Kan complex $\Pi(X)$ is called the [[fundamental ∞-groupoid]] of $X$.

This example is the universal one: up to [[model structure on simplicial sets|weak equivalence of Kan complexes]], every Kan complex is the fundamental $\infty$-groupoid of a (compactly generated, weakly Hausdorff) [[topological space]].

This is the statement of the [[homotopy hypothesis]] (which is a theorem for $\infty$-groupoids modeled as Kan complexes.

## Cubical analogue

The simplicial notion of a Kan complex has an analogue for [[cubical set | cubical sets]], discussed at: [[cubical Kan complex]].

## Related concepts

* A slight weakening of the Kan condition, the _weak Kan condition_ leads to the definition of _[[quasi-category]]_.

Other concepts:

* [[∞-groupoid]]

* [[Eilenberg subcomplex]]

* [[weak Kan complex]]

* [[Kan fibration]]

[[Kan objects]] can be defined in any [[category]],
see there for more information.


## References

Originally, Kan complexes were defined in a [[cubical set|cubical setting]],
where Kan introduced the extension property for cubical horns
and established the elementary properties of cubical homotopy groups:

* [[Daniel M. Kan]], _Abstract homotopy.  I_, Proceedings of the National Academy of Sciences 41:12 (1955), 1092-1096.  [doi](http://dx.doi.org/10.1073/pnas.41.12.1092).

The second paper in the series proves that the cubical singular complex functor yields cubical Kan complexes:

* [[Daniel M. Kan]], _Abstract homotopy.  II_, Proceedings of the National Academy of Sciences 42:5 (1956), 255-258.  [doi](http://dx.doi.org/10.1073/pnas.42.5.255).

The third paper introduces simplicial Kan complexes (as “c.s.s. complexes which satisfy the extension condition”), and defines and studies the [[Kan fibrant replacement]] functor:

* [[Daniel M. Kan]], _Abstract homotopy.  III_, Proceedings of the National Academy of Sciences 42:7 (1956), 419-421.  [doi](http://dx.doi.org/10.1073/pnas.42.7.419).

The fourth paper proves that [[simplicial groups]] are Kan complexes and studies their properties, including the [[Kan loop group]] functor:

* [[Daniel M. Kan]], _Abstract homotopy.  IV_, Proceedings of the National Academy of Sciences 42:8 (1956), 542-544.  [doi](http://dx.doi.org/10.1073/pnas.42.8.542).

The details for Part III above appeared in the paper

* [[Daniel M. Kan]], _On c.s.s. complexes_, American Journal of Mathematics 79:3 (1957), 449–476.  [doi](http://dx.doi.org/10.2307/2372558)

[[John C. Moore]] in his review of this paper for [[Mathematical Reviews]] indicates that the term “Kan complex” was already in use at the time:

> For such complexes, usually called Kan complexes, homotopy groups may be defined, and, further, the notion of homotopy between maps of an arbitrary semi-simplicial complex into a Kan complex is an equivalence relation. 

The details for Part IV above are given in the following paper:

* [[Daniel M. Kan]], _A Combinatorial Definition of Homotopy Groups_, The Annals of Mathematics 67:2 (1958), 282–312.  [doi](http://dx.doi.org/10.2307/1970006).


Exposition:

* {#Friedman08} [[Greg Friedman]], Section 7 of: _An elementary illustrated introduction to simplicial sets_, Rocky Mountain J. Math. 42(2): 353-423 (2012) ([arXiv:0809.4221](http://arxiv.org/abs/0809.4221), [doi:10.1216/RMJ-2012-42-2-353](https://projecteuclid.org/journals/rocky-mountain-journal-of-mathematics/volume-42/issue-2/Survey-Article-An-elementary-illustrated-introduction-to-simplicial-sets/10.1216/RMJ-2012-42-2-353.full))

Textbook accounts:

* {#GabrielZisman67} [[Pierre Gabriel]], [[Michel Zisman]], chapter IV.3 of _[[Calculus of fractions and homotopy theory]]_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 35, Springer (1967)  ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf))

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section I.3 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

See also:

* Wikipedia, *[Kan fibration](https://en.wikipedia.org/wiki/Kan_fibration)*

For Kan complexes as such, see also the references at _[[simplicial set]]_ and at *[[classical model structure on simplicial sets]]*.

For Kan complexes as $\infty$-groupoids, see, for instance, section 1.2.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

* [[Kerodon]], *Kan complexes* ([00SY](https://kerodon.net/tag/00SY))

An early mention of this idea was in 

* [[Tim Porter]],  Letter to [[Grothendieck]], dated 16/6/1983 ([[16-06-1983.pdf|pdf:file]])

For background on the general relation of simplicial- and globular sets, see also the references at [[oriental]]. 

Discussion of the [[homotopy theory]] of [[smooth ∞-groupoids]] presented by "Lie-Kan complexes" is in section 4.2 of

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _Principal $\infty$-bundles - Presentations_ ([arXiv:1207.0249](http://arxiv.org/abs/1207.0249))
  {#NSSb}

* [[Aurelio Carboni|A. Carboni]], [[Max Kelly|G.M. Kelly]], and M.C. Pedicchio, _Some remarks on Maltsev and Goursat categories_, Applied Categorical Structures, Volume 1, Issue 4 (December 1993), 385-421. ([Springer link](http://link.springer.com/article/10.1007%2FBF00872942)) 
 {#CKP}


[[!redirects Kan complexes]]

[[!redirects KanCplx]]
