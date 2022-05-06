+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea
In [[Pursuing Stacks]], [[Grothendieck]] introduced the idea of a test category. These are by definition small categories on which the presheaves of sets are models for homotopy types of CW-complexes, thus generalising the situation for the category of simplices, for which the category of presheaves is that of [[simplicial sets]]. The resulting theory was completed and generalised by Cisinki.

## General

+-- {: .num_defn}
###### Definition

For $\mathcal{T}$ a [[topos]], a **Cisinski model structure** on $\mathcal{T}$ is a [[model category]] structure on $\mathcal{T}$ such that

1. the [[cofibrations]] are precisely the [[monomorphisms]];

1. it is a [[cofibrantly generated model category]].

=--

+-- {: .num_remark}
###### Remark

Since every [[topos]] is a [[locally presentable category]], a Cisinski model structure is in particular a [[combinatorial model category]] structure.

=--

+-- {: .num_remark}
###### Remark

Since every [[topos]] is an [[adhesive category]], monomorphisms are automatically preserved by [[pushout]].

=--

+-- {: .num_defn #Localizer}
###### Definition

Say a class $W \subset Mor(\mathcal{T})$ is an accessible **[[localizer]]** on $\mathcal{T}$ if it is a class of [[weak equivalences]] in a Cisinski model structure on $\mathcal{T}$.

=--

+-- {: .num_prop}
###### Proposition

Every [[small set]] of [[morphisms]] $\Sigma \subset Mor(\mathcal{T})$ is contained in a smallest localizer, def. \ref{Localizer}, $W(\Sigma)$. 

=--

One says that $W(\Sigma)$ is the 
localiser _generated_ by $\Sigma$.

So in particular a Cisinski model structure always exists.


## On presheaf toposes
 {#OnPresheafToposes}

We discuss how on a [[presheaf topos]] equipped with a suitable notion of [[cylinder objects]] Cisinski model structures can be characterized fairly explicitly. After some [preliminaries](#PreliminaryNotions)_, the main statement is theorem \ref{ModelStructureFromHomotopicalStructure} below. 

(This follows sections 1.2 and 1.3 of [Cisinski 06](#Cisinski06)).





### Preliminary notions
 {#PreliminaryNotions}

Let $A$ be a [[small category]]. Write $PSh(A)$ or $[A^{op}, Set]$ for the [[category of presheaves]] over $A$. We introduce here, culminating in def. \ref{HomotopicalStructure} below, the ingredients of a _homotopical structure_ on $PSh(A)$, which is a choice of functorial [[cylinder object]] together with a compatible notion of _[[anodyne extensions]]_. Further below in def. \ref{ModelStructureMorphismsFromHomotopicalStructure} this defines a [[model category]] structure on $PSh(A)$.


+-- {: .num_defn #FunctorialCylinder}
###### Definition

For $X$ in $PSh(A)$, a **cylinder** on $X$ in the following means a [[cylinder object]], denoted $I \otimes X$, factoring the [[codiagonal]]

$$
  X \coprod X \stackrel{(\partial_X^0, \partial_X^1)}{\to} I \otimes X \stackrel{\sigma_X}{\to} X
$$

such that the first morphism is a [[monomorphism]]. 

A [[homomorphism]] of such cyclinders is a pair of morphisms $X \to Y$ and $I \otimes X \to I \otimes Y$ in $PSh(A)$, making the evident squares commute. This defines a category $Cyl(A)$ of cylinder objects on presheaves on $A$, equipped with a [[forgetful functor]] $Cyl(A) \to PSh(A)$ that sends a cylinder $I \otimes X$ to its underlying object $X$.

A **functorial cylinder object** over $A$ is a [[section]] of this functor.

=--

This is ([Cisinski 06, def. 1.3.1](#Cisinski06)).

In the following, let $J : PSh(A) \to Cyl(A)$ be a choice of functorial cylinder object. Equivalently, this is a choice of endofunctor

$$
  I \otimes (-) : PSh(A) \to PSh(A) 
$$

equipped with [[natural transformations]]

$$
  (\partial I)\otimes (-)
  \stackrel{(\partial^0_{(-)}, \partial^1_{(-)})}{\to} 
  I \otimes (-)
  \to 
  Id
$$

where $(\partial I) \otimes X := X \coprod X$, such that the composite is the functorial codiagonal, and where the first transformation is a monomorphism.



+-- {: .num_defn #ElementaryJHomotopy}
###### Definition

For $f,g : X \to Y$ two morphisms in $PSh(A)$, we say an **elementary $J$-homotopy** $f \Rightarrow g$ from $f$ to $g$ is a [[left homotopy]] from $f$ to $g$ with respect to the chosen cylinder object $J$, hence a morphism $\eta : I \otimes X \to Y$ fitting into a diagram

$$
  \array{
    X &&
    \\
    \downarrow^{\mathrlap{\partial^0_X}} & \searrow^f
    \\
    I \otimes X &\stackrel{\eta}{\to}& Y
    \\
    \uparrow^{\mathrlap{\partial^1_X}} & \nearrow_g
    \\
    X
  }
  \,.
$$

We say **$J$-homotopy** for the [[equivalence relation]] _generated_ by this.

=--

([Cisinski 06, def. 1.3.3](#Cisinski06)).

+-- {: .num_prop}
###### Proposition

$J$-homotopy is compatible with composition in $PSh(A)$. 

=--

+-- {: .proof}
###### Proof

It is sufficient to show that elementary $J$-homotopies are compatible with 
composition.

So for 

$$
  \array{
    X &&
    \\
    \downarrow & \searrow^f
    \\
    I \otimes X &\stackrel{\eta}{\to}& Y
    \\
    \uparrow & \nearrow_g
    \\
    X
  }
$$

an elementary $J$-homotopy $f \Rightarrow g$, and for

$$
  \array{
    Y &&
    \\
    \downarrow & \searrow^{f'}
    \\
    I \otimes Y &\stackrel{\eta}{\to}& Z
    \\
    \uparrow & \nearrow_{g'}
    \\
    Y
  }
$$

one $f' \Rightarrow g'$, we obtain an elementary homotopy $f' \circ f \Rightarrow g' \circ f$ by forming

$$
  \array{
    X & \stackrel{f}{\to} & Y &&
    \\
    \downarrow && \downarrow & \searrow^{f'}
    \\
    I \otimes X &\stackrel{I \otimes f}{\to}& I \otimes Y &\stackrel{\eta}{\to}& Z
    \\
    \uparrow && \uparrow & \nearrow_{g'}
    \\
    X &\stackrel{f}{\to}& Y
  }
$$

and then an elementary $J$-homotopy $g' \circ f \Rightarrow g '\circ g$ by forming

$$
  \array{
    X &&
    \\
    \downarrow & \searrow^f
    \\
    I \otimes X &\stackrel{\eta}{\to}& Y &\stackrel{g'}{\to}& Z
    \\
    \uparrow & \nearrow_g
    \\
    X
  }
  \,.
$$

Together this generates a $J$-homotopy $f' \circ f \Rightarrow g' \circ g$.

=--


Hence the following is well defined.

+-- {: .num_defn #JHomotopyCategory}
###### Definition

Write $Ho_J(A)$ for the category whose objects are those of $PSh(A)$, and whose morphisms are $J$-homotopy equivalence classes of morphisms in $PSh(A)$ -- the **$J$-homotopy category**. Write

$$
  Q : PSh(A) \to Ho_J(A)
$$

for the projection functor.

=--

+-- {: .num_defn #JHomotopyEquivalence}
###### Definition

A morphism $f : X \to Y$ in $PSh(A)$ is called a **$J$-homotopy equivalence** if it is sent by $Q$ to an [[isomorphism]].

An object $X \in PSh(A)$ is called **$J$-contractible** if $X \to *$ is a $J$-homotopy equivalence.

=--

([Cisinski 06, def. 1.3.4](#Cisinski06)).

+-- {: .num_defn #AcyclicFibration}
###### Definition

A morphism $f : X \to Y$ in $PSh(A)$ is called an **acyclic fibration** if it has the [[right lifting property]] against all monomorphisms.

=--

([Cisinski 06, def. 1.2.18](#Cisinski06)).

+-- {: .num_prop #SomePropertiesOfAcyclicFibrations}
###### Proposition

Every acyclic fibration in $PSh(A)$ is a $J$-homotopy equivalence.

More is true: every trivial fibration $p : X \to Y$

1. has a [[section]] $s : Y \to X$;

1. which is also a $J$-homotopy left inverse;

1. by an elementary $J$-homotopy $h : id \Rightarrow s \circ p$ which satisfies
   $p \circ h = p \circ \sigma_X$.


=--

([Cisinski 06, lemma 1.3.5](#Cisinski06)).

+-- {: .proof}
###### Proof

The existence of the section $s : Y \to X$ follows by right lifting against the monomorphism $\emptyset \to Y$ (out of the [[initial object]])

$$
  \array{
     \emptyset &\to& X
     \\
     \downarrow &\nearrow_s& \downarrow^{\mathrlap{p}}
     \\
     Y &\stackrel{=}{\to}& Y
  }
  \,.
$$

The $J$-homotopy $h$ is obtained by lifting in the diagram

$$
  \array{
     X \coprod X &\stackrel{(id_X, s \circ p)}{\to}& X 
     \\
     {}^{\mathllap{(\partial^0_X, \partial^1_X)}}\downarrow
     &&
     \downarrow^{\mathrlap{p}}
     \\
     I \otimes X
     &\stackrel{p \circ \sigma_X}{\to}& Y
  }
  \,.
$$

=--

+-- {: .num_defn #ElementaryHomotopicalDatum}
###### Definition

An **elementary homotopical datum** on $PSh(A)$ is a functorial cylinder $J$, def. \ref{FunctorialCylinder}, such that 

1. the functor $I \otimes (-)$ commutes with small [[colimits]] and preserves monomorphisms;

1. for all [[monomorphisms]] $f : K \to L$ the [[diagrams]]

   $$
     \array{
       K &\stackrel{(id, f)}{\to}& L
       \\
       {}^{\mathllap{(e,id)}}\downarrow && \downarrow^{\mathrlap{(e,id)}}
       \\
       I \otimes K &\stackrel{I \otimes f}{\to}& I \otimes L
     } 
   $$
   
   for $e \in \{0,1\}$ is a [[pullback]] square.

=--

([Cisinski 06, def. 1.3.6](#Cisinski06)).

+-- {: .num_remark #PullbackOfMonosAndUnions}
###### Remark

For

$$
  \array{
    R &\to & S
    \\
    \downarrow && \downarrow
    \\
    T &\to& U 
  }
$$

a [[pullback]] square in $PSh(A)$ of two monomorphisms $S \hookrightarrow U$ and $T \hookrightarrow U$, the universal morphism out of the [[pushout]]

$$
  T \coprod_R S \to U
$$

is also a monomorphism, usually written as the morphism out of the _[[union]]_

$$
  T \cup S \hookrightarrow U
  \,.
$$


=--

+-- {: .proof}
###### Proof

All this follows, for instance, from the corresponding statements in [[Set]], over each object of $A$.

=--

+-- {: .num_defn}
###### Definition

Let 

$$
  \partial^\epsilon : \{\epsilon\}\otimes(-) \hookrightarrow I \otimes(-)
  \,,
$$

for $\epsilon = 0,1$, be the [[subfunctor]] which is the [[image]] of $\partial^\epsilon : Id_{PSh(A)} \to I \otimes (-)$.

This way for any $X \in PSh(A)$ the boundary inclusions $\partial^\epsilon_X : X \to I \otimes X$ are identified with 

$$
  \partial^\epsilon \otimes id_X : \{\epsilon\} \otimes X \to I \otimes X
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

The second condition on an _elementary homotopical datum_, def. \ref{ElementaryHomotopicalDatum} implies that the canonical morphism

$$
  J \otimes K \cup (\partial J) \otimes L \to J \otimes L
$$

is a [[monomorphism]].

=--

([Cisinski 06, remark 1.3.7](#Cisinski06)).

+-- {: .proof}
###### Proof

The condition implies that 

$$
  \array{
    \{\epsilon\} \otimes K &\stackrel{id_\{\epsilon\} \otimes j}{\to}&
    \{\epsilon\} \otimes L
    \\
    {}^{\mathllap{\partial^\epsilon \otimes id_K}}\downarrow && \downarrow^{\mathrlap{\partial^\epsilon \otimes id_L}}
    \\
    I \otimes K &\stackrel{(id_I) \otimes j}{\to}& I \otimes L
  }
$$

is a pullback, for $\epsilon = 0,1$, hence that 

$$
  \array{
    \partial I \otimes K &\stackrel{id_{\partial I} \otimes j}{\to}&
    \partial I \otimes L
    \\
    {}^{\mathllap{i \otimes id_K}}\downarrow && \downarrow^{\mathrlap{i \otimes id_L}}
    \\
    I \otimes K &\stackrel{(id_I) \otimes j}{\to}& I \otimes L
  }
$$

is a pullback. So the statement follows with remark \ref{PullbackOfMonosAndUnions}.

=--

+-- {: .num_example #SegmentObject}
###### Example

Let $I \in PSh(A)$ be any object equipped with two points (global sections) $\partial^0, \partial^1 : * \to I$ which are disjoint in that

$$
  \array{
    \emptyset &\to& *
    \\
    \downarrow && \downarrow^{\mathrlap{\partial^0}}
    \\
    * &\stackrel{\partial^1}{\to}& I
  }
$$

is a [[pullback]] square (here $\emptyset$ is the [[initial object]] in $PSh(A)$). This induces a functorial cylinder by the assignment

$$
  X \mapsto I \times X
  \,,
$$

where on the right we have the cartesian product.

This defines an _elementary homotopical datum_ in the sense of def. \ref{ElementaryHomotopicalDatum}.

=--

([Cisinski 06, example 1.3.8](#Cisinski06)).

+-- {: .proof}
###### Proof


The disjointness of the two points ensures that $* \coprod * \stackrel{(\partial^0, \partial^1)}{\to} I$ is a monomorphism.

The interval commutes with colimits as these and the product are computed objectwise, and products in [[Set]] commute with colimits. More abstractly: by the [[Giraud theorem]] valid in the [[presheaf topos]] $PSh(A)$ we have "[[universal colimits]]": they are preserved by pullback, and in particular by cartesian product. Therefore the first clause of def. \ref{ElementaryHomotopicalDatum} is satisfied.

Similarly, the second axiom of def. \ref{ElementaryHomotopicalDatum} holds because [[limits]] commute over each other.

=--

+-- {: .num_example #LawvereCylinder}
###### Example
**(Lawvere cylinder)**

Let $I := \Omega$ be the [[subobject classifier]] in the [[presheaf topos]] $PSh(A)$. This is the presheaf which to an object $U$ of $A$ assigns the set of [[subobjects]] of the [[representable functor]] given by $U$ (the [[sieves]] on $U$)

$$
  \Omega : U \mapsto Sub(U)
$$

and which to a morphism $f : U_1 \to U_2$ assigns the [[pullback]] functor $f^* : Sub(U_2) \to Sub(U_1)$.

Let then 

$$
  \partial^0, \partial^1 := \top, \bot: * \to \Omega
$$

be the morphisms that classify [[top]] and [[bottom]], respectively, the terminal and the initial subobject of the [[terminal object]].

This is a segment object in the sense of example \ref{SegmentObject} (the "[[Bill Lawvere|Lawvere]]-segment").

=--

([Cisinski 06, example 1.3.9](#Cisinski06)).

+-- {: .proof}
###### Proof

That the two points are separated, in that 

$$
  \array{
    \emptyset &\to& *
    \\
    \downarrow && \downarrow^{\mathrlap{\top}}
    \\
    * &\stackrel{\bot}{\to}& \Omega
  }
$$

is a pullback, is the defining property of the [[subobject classifier]].

=--

+-- {: .num_defn #AnodyneExtensions}
###### Definition

For $J$ an elementary homotopical datum on $PSh(A)$, a **[[class]] of [[anodyne extensions]]** is a class $AnExt \subset Mor(PSh(A))$ such that

1. there exists a [[small set]] of monomorphisms $S$ with 

   $$
     AnExt = LLP(RLP(S))
   $$
  
1. for $K \hookrightarrow L$ a monomorphism, the [[pushout-product axiom|pushout product]] morphisms

   $$
     (I \otimes K) \cup (\{e\} \otimes L) \to I \otimes L
   $$

   (by [[Joyal-Tierney calculus]] to be thought of as "$(K \to L) \bar \otimes (\{e\} \to I)$")   

   are in $AnExt$, for $e \in \{0,1\}$;

1. if $K \to L$ is in $AnExt$, then so is

   $$   
     (I \otimes K) \cup ((\partial I) \otimes L) 
    \to 
     I \otimes L
     \,.
   $$


   (hence "$(K \to L) \bar \otimes (\partial I \to I)$").

=--

([Cisinski 06, def. 1.3.10](#Cisinski06)).

+-- {: .num_prop #PropertiesOfAnodyneExtensions}
###### Proposition

A class of anodyne extensions 

* is generated under [[pushouts]], [[transfinite composition]] and [[retracts]] from the morphisms in $\Lambda$;

* is a subclass of the [[monomorphisms]]; 

* contains all morphisms of the form $e : K \to (I \otimes K)$;

* is closed under $I\otimes(-)$;

=--

([Cisinski 06, remark. 1.3.11](#Cisinski06)).

+-- {: .proof}
###### Proof

By prop. \ref{PresheavesAreCompact}, 
$X \in PSh(A)$ is $|Mor(A/X)|$-[[compact object|compact]]. Therefore the set $\Lambda$ admits a [[small object argument]], which shows the first statement (see there).

Since monomorphisms are closed under these operations, the second statement follows.

The third statement follows by choosing the morphism in the second item of def. \ref{AnodyneExtensions} to be $\emptyset \to K$ and using that by def. \ref{ElementaryHomotopicalDatum} the interval commutes with colimits, so that $I \otimes \emptyset \simeq \emptyset$.

Finally, to see that with $j : K \to L$ also $I \otimes j : I \otimes L \to I \otimes L$ is anodyne, consider the naturality diagram of the endpoint inclusion 

$$
  \array{
    K &\stackrel{j}{\to}& L 
    \\
    \downarrow^{\mathrlap{\partial^0_k}} && \downarrow
    \\
    I \otimes K &\stackrel{j'}{\to}& (I \otimes K) \cup \{0\}\otimes L
    \\
    & {}_{I \otimes j} \searrow & \downarrow^{\mathrlap{k}}
    \\
    && I \otimes L
  }
  \,,
$$

factored through the top pushout square, as indicated. Here $j'$ is anodyne, being a pushout of an anodyne morphism, and $k$ is anodyne by the second clause in def. \ref{AnodyneExtensions}. Therefore also their composite $I \otimes j$ is anodyne.

=--


+-- {: .num_defn #HomotopicalStructure}
###### Definition

A **homotopical structure** on $PSh(A)$ is a choice of elementary homotopical datum $J$, def. \ref{ElementaryHomotopicalDatum} and a corresponding choice of a class of anodyne extensions $AnExt$, def. \ref{AnodyneExtensions}.

=--

([Cisinski 06, def. 1.3.14](#Cisinski06)).

\begin{defn} \label{DefinitionHomotopicalDatum} A _homotopical datum_, or _donnée homotopique_, on $PSh(A)$ is a choice of elementary homotopical datum (Definition \ref{ElementaryHomotopicalDatum}) together with a set of [[monomorphisms]] in $PSh(A)$. \end{defn}

([Cisinski 06, def. 1.3.14](#Cisinski06)).

\begin{rmk} A homotopical datum $(J, S)$ _generates_ a homotopical structure for which $AnExt$ is the smallest class of anodyne extensions relative to $J$ which contains $S$. \end{rmk}

### The model structure

+-- {: .num_defn #ModelStructureMorphismsFromHomotopicalStructure}
###### Definition

Let $A$ be a [[small category]] and $(J, AnExt)$ a homotopical structure, def. \ref{HomotopicalStructure}, on $PSh(A)$. Define the following classes of objects and morphisms in $PSh(A)$:

* the **cofibrations** are the [[monomorphisms]];

* the **fibrant objects** are those $X \in PSh(A)$ for which  the [[terminal object|terminal]] morphism $X \to *$ has the [[right lifting property]] against the anodyne extensions (the morphisms in $AnExt$, def. \ref{AnodyneExtensions});

* the **weak equivalences** are those morphisms $f : A \to B$, such that for all fibrant objects $X$ the induced morphism in the $J$-homotopy category, def. \ref{JHomotopyCategory},

  $$
    Ho_J(f,X) : Ho_J(B,X) \to Ho_J(A, X)
  $$

  is an [[isomorphism]] (a [[bijection]] of sets).

=--

([Cisinski 06, def. 1.3.21](#Cisinski06)).


+-- {: .num_theorem #ModelStructureFromHomotopicalStructure}
###### Theorem

With the classes of morphisms as in def. \ref{ModelStructureMorphismsFromHomotopicalStructure}, $PSh(A)$ is a [[cofibrantly generated model category]].

=--

([Cisinski 06, theorem 1.3.22](#Cisinski06)).

+-- {: .proof}
###### Proof

The retract properties are clear, as is the 2-out-of-3 property for weak equivalences, see lemma \ref{JHomotopyEquivsAreWeakEquivs} below.

The lifting properties hold by prop. \ref{AcyclicFibrationsAreAcyclicFibrations} below, the proof of which is in the section _[Lifting](#Lifting)_ below.

The factorization properties hold by cor. \ref{FirstFactorizationEstablishes} and cor. \ref{FactorizationAcyclicCofibFib} below, which are in the section _[Factorization](#Factorization)_ below.

The existence of a set of generating cofibrations is prop. \ref{CellularStructuresExist} below, that of generating acyclic cofibrations is prop. \ref{GeneratingAcyclicCofibrationsExist} below.

=--

+-- {: .num_prop #HomotopyCatIsFullSubcatgOfJHo}
###### Proposition

The [[homotopy category]] of $(PSh(A), W)$ is (up to [[equivalence of categories|equivalence]]) the [[full subcategory]] of $Ho_J$, def. \ref{JHomotopyCategory}, on the fibrant objects.

=--

([Cisinski 06, 1.3.23](#Cisinski06)).



Before coming to the proof of these lemmas, the following two statements say that the terminology introduced so far is indeed consistent with the meaning of this theorem.

+-- {: .num_prop #AcyclicFibrationsAreAcyclicFibrations}
###### Proposition

The morphisms called _acyclic fibrations_ in def. \ref{AcyclicFibration} are indeed precisely the acyclic fibrations with respect to the model structure of theorem \ref{ModelStructureFromHomotopicalStructure}.

=--

([Cisinski 06, theorem 1.3.27](#Cisinski06)).

+-- {: .num_prop #EveryAnodyneExtensionIsWeakEquivalence}
###### Proposition

Every anodyne extension, def. \ref{AnodyneExtensions}, is a weak equivalence in the model structure of theorem \ref{ModelStructureFromHomotopicalStructure}.

=--

+-- {: .num_remark }
###### Remark

What is not true in general is the converse of prop. \ref{EveryAnodyneExtensionIsWeakEquivalence}, that every acyclic cofibration is an anodyne extension. (A counterexample derives from chapter XI, remark 2.4 in [[Paul Goerss|Goerss]], [[Rick Jardine|Jardine]] _[[Simplicial homotopy theory]]_.)

=--

([Cisinski 06, remark 1.3.46](#Cisinski06)).


+-- {: .num_prop #ConditionsForCompleteness}
###### Proposition

For the model structure from theorem \ref{ModelStructureFromHomotopicalStructure}, the 
following are equivalent:

1. every acyclic cofibration is an anodyne extension;

1. every morphism with right lifting against anodyne extensions is a fibration;

1. every weak equivalence with right lifting against anodyne extensions is an acyclic fibration;

1. every morphism with right lifting against anodyne extensions factors as an anodyne extension followed by a fibration.

=--

([Cisinski 06, prop. 1.3.47](#Cisinski06)).

+-- {: .num_defn }
###### Definition

A homotopical structure, def. \ref{HomotopicalStructure}, on a presheaf category
is called **complete** if the model structure from theorem \ref{ModelStructureFromHomotopicalStructure} satisfies the equivalent conditions of prop. \ref{ConditionsForCompleteness}.

=--

([Cisinski 06, def. 1.3.48](#Cisinski06)).

We discuss the proof of prop. \ref{ConditionsForCompleteness} below in _[Completeness](#Completeness)_.


### Proof


We collect lemmas to prove theorem \ref{ModelStructureFromHomotopicalStructure} and related statements. A little bit of work is required for demonstrating the lifting axioms, which we do below in _[Lifting](#Lifting)_. A little bit more work is required for demonstrating the factorization axioms, which we do below in _[Factorization](#Factorization)_. Finally, the proof of the equivalence of the conditions of completeness is in _[Completeness](#Completeness)_.


+-- {: .num_lemma #JHomotopyEquivsAreWeakEquivs}
###### Lemma

Every $J$-homotopy equivalence, def. \ref{JHomotopyEquivalence}, is a weak equivalence.

The weak equivalences satisfy the [[two-out-of-three]]-property and are stable under [[retracts]].

=--

([Cisinski 06, remark 1.3.24](#Cisinski06)).

+-- {: .proof}
###### Proof

The first statement holds by definition of $Ho_J$. 

The second statement also follows directly from the definition. If for $A \stackrel{f}{\to} B \stackrel{g}{\to} C$ and fibrant $X$ in the composite

$$
  Ho_J(C,X) \stackrel{g^*}{\to} Ho_J(B,X) \stackrel{f^*}{\to} Ho_J(A,X)
$$

two of three are isomorphisms, then so is the third. 

=--

#### Lifting
 {#Lifting}

We discuss the lifting properties in the model structure of def. \ref{ModelStructureMorphismsFromHomotopicalStructure}. 

Since fibrations are defined to be the morphisms satisfying the [[right lifting property]] against acyclic cofibration, we only need to show that the fibrations which are also weak equivalences have the right lifting property against the monomorphisms. For this it is sufficient to show prop. \ref{AcyclicFibrationsAreAcyclicFibrations}. This we do now, after a lemma.

+-- {: .num_defn #DualDeformationRetract}
###### Definition

A _[[deformation retract]]_ $f : X \to Y$ in $PSh(A)$ is a [[retract]] with retraction $g : Y \to X$, which is also a [[section]] of $f$ up to a $J$-homotopy $h : id_Y \Rightarrow f \circ g$. It is _strong_ if $h \circ (I \otimes f) = \sigma_Y \circ (I \otimes f)$.

A _dual deformation restract_ $f : X \to Y$ has a [[section]] by a morphism $g : Y \to X$ and is also a retract up to a $J$-homotopy $k : id_X \Rightarrow g \circ f$. Is is _strong_ if $f \circ k = f \circ \sigma_X$.

=--

+-- {: .num_lemma #SectionsOfAcyclicFibrationsAreDefRetracts}
###### Lemma

Every acyclic fibration is a dual [[strong deformation retract]], def. \ref{DualDeformationRetract}.

Every [[section]] of an acyclic fibration is a [[strong deformation retract]]. 

=--

([Cisinski 06, prop. 1.3.26](#Cisinski06)).

+-- {: .proof}
###### Proof

The first statement is a direct consequence of prop \ref{SomePropertiesOfAcyclicFibrations}.

For the second statement, let $p : X \to Y$ be an acyclic fibration, and let $s : Y \to X$ be a [[section]]. This induces a commuting square

$$
  \array{
    (I \otimes Y) \cup ((\partial I) \otimes X) 
    &\stackrel{(s\circ \sigma_Y,(id_X, s \circ p))}{\to}& X
    \\
    \downarrow &\nearrow_{h}& \downarrow^{\mathrlap{p}}
    \\
    I \otimes X
    &\stackrel{ p \circ \sigma_X}{\to}& Y
  }
  \,,
$$

where the lift $h$ exists by assumption on $p$ ($s$ is necessarily a [[monomorphism]], being a [[section]]).

The resulting component triangle

$$
  \array{
    (\partial I) \otimes X
    &\stackrel{(id_X, s \circ p)}{\to}& X
    \\
    \downarrow &\nearrow_{h}&
    \\
    I \otimes X
  }
$$

exhibits $s$ as a [[deformation retract]], and the other resulting component triangle

$$
  \array{
    I \otimes Y
    &\stackrel{s\circ \sigma_Y}{\to}& X
    \\
    \downarrow^{\mathrlap{I \otimes s}} &\nearrow_{h}
    \\
    I \otimes X
  }
$$

says that $h\circ (I \otimes s) = s \circ \sigma_Y$, hence by [[natural transformation|naturality]] of cylinders $\cdots = \sigma_X \circ (I \otimes s)$, hence that the deformation retract is indeed strong.

=--

+-- {: .proof}
###### Proof 
**of prop. \ref{AcyclicFibrationsAreAcyclicFibrations}**

First to see that the acyclic fibrations of def. \ref{AcyclicFibration} are indeed fibrations and weak equivalences:

By lemma \ref{SectionsOfAcyclicFibrationsAreDefRetracts} every acyclic fibration is in particular a $J$-homotopy equivalence, hence by lemma \ref{JHomotopyEquivsAreWeakEquivs} a weak equivalence. Moreover, by def. \ref{AcyclicFibration} the acyclic fibrations right-lift against monomorphisms, hence in particular against the acyclic cofibrations, hence are fibrations.

Conversely, let $p : X \to Y$ be a fibration which is also a weak equivalence. We need to show that it has the right lifting property against all monomorphisms.

By prop. \ref{CellularStructuresExist}, proven below, we may apply the [[small object argument]] to factor $p = q \circ j$ as a monomorphism $j$ followed by an acyclic fibration $q$. By the previous argument, $q$ is a weak equivalence, and so by lemma \ref{JHomotopyEquivsAreWeakEquivs} so is $j$. 
Therefore, since $p$ is a fibration, we have a lift $\sigma$ in  

$$
  \array{
    &\stackrel{id}{\to}&
    \\
    \downarrow^{\mathrlap{j}}
    & \nearrow_\sigma&
    \downarrow^{p}
    \\
    &\stackrel{q}{\to}&
  }
  \,.
$$

This equivalently exhibits $p$ as a [[retract]] of $q$

$$
  \array{
     &\stackrel{j}{\to} & & \stackrel{\sigma}{\to} &
   \\
   \downarrow^{\mathrlap{p}} && \downarrow^{\mathrlap{q}}
    && \downarrow^{\mathrlap{p}}
   \\
   & \stackrel{id}{\to} & & \stackrel{id}{\to} &
  }
  \,.
$$

So by lemma \ref{PropertiesOfAnodyneExtensions} with $q$ also $p$ is an acyclic fibration.

=--




([Cisinski 06, remark 1.3.28](#Cisinski06)).


#### Factorization 
 {#Factorization}

We discuss the two factorization axioms for the [[model category]] structure from def. \ref{ModelStructureMorphismsFromHomotopicalStructure} to be established. First for factorizations into [cofibrations followed by acyclic fibrations](#CofibrationFollowedByAcyclicFibration), then for factorizations into [acyclic cofibrations followed by fibrations](AcyclicCofibrationFollowedByFibration).

##### Cofibration followed by acyclic fibration
 {#CofibrationFollowedByAcyclicFibration}

Every [[partial map classifier]] is an injective object, and so we have a functoral factorization of $X \to Y$ into $X \to X_\bot \times Y \to Y$. However, we can say more by appealing to general machinery.

For showing that every morphism factors as a monomorphism followed by an acyclic fibration, it is by prop. \ref{AcyclicFibrationsAreAcyclicFibrations} sufficient to show that the monomorphisms are generated by a [[small set]] that admits the [[small object argument]]. This we do now.

This section follows ([Cisinski 06, section 1.2](#Cisinski06)).

We start with some entirely general statements about [[compact objects]].

+-- {: .num_prop #LimitsOverASmallDiagramAreCompact}
###### Proposition

For $A$ a [[small category]], let $\alpha = {\vert Mor(A)\vert}$ be the smallest [[regular cardinal]] $\geq$ the [[cardinality]] of the set of morphisms of $A$. Then the [[limit]] functor

$$
  \lim_\leftarrow : Func(A,Set) \to Set
$$

commutes with $\alpha$-[[filtered colimits]] / $\alpha$-[[directed colimits]]. 

=--

([Cisinski 06, prop. 1.2.9](#Cisinski06)).


+-- {: .num_prop #CompactnessOfColimitsOverCompacts}
###### Proposition

Let $C$ be a category with all small [[colimits]], let $\alpha$ be a [[cardinal]], let $A$ be a [[small category]] and finally let
$F : A \to C$ be a functor with values in $\alpha$-[[compact objects]] in $C$. Then the [[colimit]] $\lim_\to F$ is  $\lambda$-compact object, for $\lambda$ the [[maximum]] of $\alpha$ and the [[cardinality]] ${\vert Mor A\vert}$ of the set of morphisms of $A$.

=--

([Cisinski 06, prop. 1.2.10](#Cisinski06)).


+-- {: .proof}
###### Proof

Let $G : I \to C$ be a $\lambda$-[[filtered category|filtered diagram]].

Then by prop. \ref{LimitsOverASmallDiagramAreCompact} we have [[natural isomorphisms]]

$$
  \begin{aligned}
    \lim_{\underset{I}{\to}}
    C(\lim_{\underset{A}{\to}} F, G)
    & \simeq
  \lim_{\underset{I}{\to}}
  \lim_{\underset{A}{\leftarrow}} 
  C(F, G)
   \\
  & \simeq
  \lim_{\underset{A}{\leftarrow}} 
  \lim_{\underset{I}{\to}}
  C(F, G)
  \end{aligned}
  \,,
$$

because the $\lambda$-filtered diagram is at least ${\vert Mor(A)\vert}$-filtered and hence, by prop. \ref{LimitsOverASmallDiagramAreCompact}, its colimit commutes with the limit over $A$.

Now since each $F(a)$ is assumed to be $\alpha$-compact and hence is also $\lambda$-compact, we conclude with the natural isomorphisms

$$
  \begin{aligned}
    \cdots & 
    \simeq   
   \lim_{\underset{A}{\leftarrow}} 
    C(F, \lim_{\underset{I}{\to}} G)
    \\
    & \simeq
    C(\lim_{\underset{A}{\to}} F, \lim_{\underset{I}{\to}} G)
  \end{aligned}
  \,.
$$

=--

For $X \in PSh(A)$, write $A/X$ for the [[category of elements]] of $X$. Write ${\vert Mor(A/X)\vert}$ for the [[cardinality]] of the set of morphisms of the category of elements (throughout assuming $A$ to be a [[small category]]).

+-- {: .num_prop #PresheavesAreCompact}
###### Proposition

For $X \in PSh(A)$ any object, the [[hom functor]] $Hom(X, -) : PSh(A) \to Set$ preserves ${\vert Mor(A/X)\vert}$-[[filtered colimits]].

In other words: $X$ is a ${\vert Mor(A/X)\vert}$-[[compact object]].

=--

([Cisinski 06, cor. 1.2.11](#Cisinski06)).

+-- {: .proof}
###### Proof

By the [[co-Yoneda lemma]] $X$ is the [[colimit]] over its elements

$$
  X \simeq \lim_\to (A/X \to PSh(A))
 \,.
$$

Since the image of the functor $A/X \to PSh(A)$ is in representables, which are maximally compact, the stament follows with prop. \ref{CompactnessOfColimitsOverCompacts}.

=--

+-- {: .num_defn #CellularModel}
###### Definition

A **[[cellular model]]** on $PSh(A)$ is a choice of a [[small set]] $I \subset Mor(PSh(A))$ of [[monomorphisms]], such that the [[class]] of all monomorphisms is generated from it

$$
  Monos = LLP(RLP(I))
  \,.
$$

=--

([Cisinski 06, def. 1.2.26](#Cisinski06)).



+-- {: .num_remark }
###### Remark

By prop. \ref{PresheavesAreCompact} we may apply the [[small object argument]] in $PSh(A)$ and so it follows that $LLP(RLP(I))$ is the smallest class containing $I$ that is closed under [[pushout]], [[retract]] and [[transfinite composition]].

=--

The following lemma will be used to show that cellular structures always exist.

+-- {: .num_lemma #LemmaForGenerationOfMonos}
###### Lemma

Let $C \subset Mor(PSh(A))$ be a class of morphisms, and $D \subset PSh(A)$ a [[small set]] of objects, such that

1. $C$ is closed under [[pushouts]], [[retracts]] and [[transfinite composition]];

1. if $f,g \in Mor(PSh(A))$ are two composable morphisms with $f$ and $g \circ f$ in $C$, then also $g$ is in $C$;

1. every $X \in PSh(A)$ is the [[union]] of those of its [[sub-objects]] isomorphic to an object in $D$;

1. for every $X \to Y$ in $C$ and every sub-object $Z$ of $Y$ in $D$, there is a sub-object $T \hookrightarrow Y$ from $D$, which contains $Z$ and such that $T \cap X \to T$ is in $C$.

Then the [[small set]] $I \subset Mor(PSh(A))$ of morphisms in $C$ with codomain in $D$, generates $C$ as

$$
  C = LLP(RLP(I))
  \,.
$$

=--

([Cisinski 06, lemma. 1.2.24](#Cisinski06)).

+-- {: .proof}
###### Proof

A bit of work...

=--

+-- {: .num_prop #CellularStructuresExist}
###### Proposition

There exists a cellular structure, def. \ref{CellularModel}, on $PSh(A)$. 

The set $I$ can be chosen to consist of morphisms into [[quotient objects]] of [[representable functors|representables]].

=--

([Cisinski 06, prop. 1.2.27](#Cisinski06)), also sketched at [[cellular model]].

+-- {: .proof}
###### Proof

Take in lemma \ref{LemmaForGenerationOfMonos} $C$ to be the class of monomorphisms
and $D$ to be the class of quotients of representables.

=--

+-- {: .num_cor #FirstFactorizationEstablishes}
###### Corollary

There exists a functorial factorization of morphisms in $PSh(A)$ into a monomorphism followed by an acyclic fibration.

=--

([Cisinski 06, cor. 1.2.28](#Cisinski06)).

+-- {: .proof}
###### Proof

By prop. \ref{PresheavesAreCompact} every object is $\alpha$-[[compact object|small]],
for some $\alpha$. Therefore by prop. \ref{CellularStructuresExist} we can 
apply the [[small object argument]].

=--


##### Acyclic cofibration followed by fibration
 {#AcyclicCofibrationFollowedByFibration}

We show now for def. \ref{ModelStructureMorphismsFromHomotopicalStructure} that every morphism factors as an acyclic cofibration followed by a fibration. Since the fibrations are defined by right lifting against acylcic cofibrations, for this it is sufficient to establish a set of [[cofibrantly generated model category|generating acyclic cofibrations]]. This is the statement of prop. \ref{GeneratingAcyclicCofibrationsExist} below. Establishing this takes a few technical lemmas.

+-- {: .num_lemma #FactorAnodyneFollowedByRLPAnodyne}
###### Lemma

Every morphism admits a factorization into an anodyne extension, followed by a morphism having the right lifting property against anodyne extensions.

=--

([Cisinski 06, remark 1.3.29](#Cisinski06)).

+-- {: .proof}
###### Proof

By the [[small object argument]], in view of prop. \ref{PropertiesOfAnodyneExtensions}.

=--

+-- {: .num_lemma #ElementaryJHomotopyIntoFibIsEquivRel}
###### Lemma

If $T \in PSh(A)$ is fibrant, then for any $K \in PSh(A)$ elementary $J$-homotopy, def. \ref{ElementaryJHomotopy}, is already an equivalence relation on $Hom_{PSh(A)}(K,T)$ and coincides with $J$-homotopy.

=--

([Cisinski 06, lemma 1.3.30](#Cisinski06)).

+-- {: .num_prop #EveryAnodyneExtensionIsWeakEquivalence}
###### Proposition

Every anodyne extension is a weak equivalence.

=--

([Cisinski 06, lemma 1.3.31](#Cisinski06)).


+-- {: .proof}
###### Proof

For $j : K \to L$ an anodyne extension and $T$ a fibrant object, we need to show that 

$$
  Ho_J(j,T) :  Ho_J(L,T) \to Ho_J(K,T)
$$

is a bijection. 

It is surjective by the defining lifting property, which provides $\sigma$ in 

$$
  \array{
    K &\stackrel{}{\to}& T
    \\
    \downarrow^{\mathrlap{j}}
    & \nearrow_{\mathrlap{\sigma}}
    \\
    L
  }
  \,.
$$

To see injectivity, let $l_0, l_1 : L \to T$ be two morphisms such that $l_0 \circ j$ and $l_1 \circ j$ coincide in $Ho_J$. By lemma \ref{ElementaryJHomotopyIntoFibIsEquivRel} this is the case precisely if there is an elementary $J$-homotopy $h : I \otimes K \to T$ relating them. This induces the horizontal morphism in the diagram

$$
  \array{
    (I \otimes K) \cup ((\partial I) \otimes L)
    &\stackrel{(h,(l_0,l_1))}{\to}&
    T
    \\
    \downarrow & \nearrow_{\mathrlap{\eta}}
    \\
    I \otimes L
  }
  \,,
$$

where the left morphism is anodyne, by the second clause of def. \ref{AnodyneExtensions}, so that the lift denoted $\eta$ exists. This lift exhibits a $J$-homotopy $l_0 \Rightarrow l_1$, hence shows that $l_0$ was already equal to $l_1$ in $Ho_J$, hence that $j^*$ is injective.

=--

+-- {: .num_lemma #WeakEquivalencesBetweenFibrantObjects}
###### Lemma

A morphism between fibrant objects is a weak equivalence precisely if it is a $J$-homotopy equivalence, def. \ref{JHomotopyEquivalence}. 

=--

([Cisinski 06, lemma 1.3.32](#Cisinski06)).

+-- {: .proof}
###### Proof

Is is clear that every $J$-homotopy is a weak equivalence. Conversely, let $f : X \to Y$ be a weak equivalence between fibrant objects. Write $Ho_J^{fib} \hookrightarrow Ho_J$ for the [[full subcategory]] of $Ho_J$, def. \ref{JHomotopyEquivalence} on the fibrant objects. The localization $Q(f)$ is by definition in $Ho_J^{fib}$ and for all objects $T \in Ho_J^{fib}$ the morphism $Ho_J^{fib}(Q(f), T)$ is an [[isomorphism]]. By the [[Yoneda lemma]], therefore, $Q(f)$ itself is an isomorphism in $Ho_J^{fib}$, hence also in $Ho_J$, hence is a weak equivalence.

=--

+-- {: .num_lemma #NaiveFibAndDualStrongDefRetractIsAcyclFib}
###### Lemma

If a morphism has the [[right lifting property]] against the anodyne extensions, then it is an acyclic fibration precisely if it is a dual [[strong deformation retract]].

=--

([Cisinski 06, lemma 1.3.33](#Cisinski06)).

+-- {: .proof}
###### Proof

That the former implies the latter was the statement of lemma \ref{SectionsOfAcyclicFibrationsAreDefRetracts}. Conversely, let $p$ be a dual strong deformation retract, meaning that there is $s : Y \to X$ with $p \circ s = id$,  as well as a morphism $k : I \otimes X \to X$ exhibiting a $J$-homotopy $id \Rightarrow s \circ p$. This being _strong_ means that $p \circ k = p \circ \sigma_X$. 

We need to show that this implies for 

$$
  \array{
    K &\stackrel{a}{\to}& X
    \\
    \downarrow^{\mathrlap{i}} && \downarrow^{\mathrlap{p}}
    \\
    L &\stackrel{b}{\to}& Y
  }
$$

a commuting diagram with $i$ a monomorphism, there is a lift. To this end, observe that the given structures induce a morphism

$$
  (I \otimes K) \cup (\{1\} \otimes L) \to X
$$

such that 

$$
  \array{
    (I \otimes K) \cup (\{1\} \otimes L) 
    &&\stackrel{(k \circ (I \otimes a), s \circ b)}{\to}&&
    X
    \\
    \downarrow^{\mathrlap{j}} && && \downarrow^{\mathrlap{p}}
    \\
    I \otimes L &\stackrel{\sigma_L}{\to}& L
    &\stackrel{b}{\to}& Y
  }
  \,.
$$

By the second clause of def. \ref{AnodyneExtensions} the morphism on the left is an anodyne extension, and so this diagram admits a lift $h : I \otimes L \to X$. One see that $l := h \circ \partial^0_L$ is a lift of the original square above.

=--

+-- {: .num_lemma #NaiveFibIntoFibIsWeakEquivIffItIsAcyclicFib}
###### Lemma

A morphism into a fibrant object with [[right lifting property]] against anodyne extensions is a weak equivalence precisely if it is an acyclic fibration.

=--

([Cisinski 06, lemma 1.3.34](#Cisinski06)).

+-- {: .proof}
###### Proof

We already know from prop. \ref{AcyclicFibrationsAreAcyclicFibrations} that acyclic fibrations are weak equivalences.

So let $Y$ be fibrant and let $p : X \to Y$ be a weak equivalence that has rlp against anodyne extensions. We need to show that $p$ is an acyclic fibration. By lemma \ref{NaiveFibAndDualStrongDefRetractIsAcyclFib} it is sufficient to show that it is a dual strong deformation retract.


By lemma \ref{WeakEquivalencesBetweenFibrantObjects} $p$ is also a $J$-homotopy equivalence. By lemma \ref{ElementaryJHomotopyIntoFibIsEquivRel} this is exhibited by an elementary $J$-homotopy $k : I \otimes Y \to Y$, which in particular gives a commuting diagram

$$
  \array{
    Y &\stackrel{t}{\to}& X
    \\
    \downarrow^{\mathrlap{\partial^1_Y}} && \downarrow^{\mathrlap{p}}
    \\
    I \otimes Y &\stackrel{k}{\to}& Y
  }
  \,,
$$

from which we obtain a lift $k' : I \otimes Y \to X$. Set then 

$$
  s := k' \circ \partial^0_Y
  \,.
$$

One finds then $p \circ s = id_Y$.
As $p$ is a $J$-homotopy equivalence, it follows that $s$ is its homotopic inverse, in particular, there is a $J$-homotopy $h : id_X \Rightarrow s \circ p$.

Next we lift the trivial $J$-homotopy $p \Rightarrow p$
to transform $h$ into a dual stronf deformation:
$$
\array{
  \partial I \otimes I \otimes X \cup I \otimes \{1\} \otimes X &
  \stackrel{([h, s \circ p \circ h], s \circ p \circ \sigma_X)}{\to} & X \\
  \downarrow & H \nearrow & \downarrow^{\mathrlap{p}} \\
  I \otimes I \otimes X &
  \stackrel{p \circ h \circ \sigma_{I \otimes X}}{\to} &
  Y
}
$$
Now $H \circ (I \otimes \partial^0_{X})$ is a $J$-homotopy showing that $p$ is a dual strong deformation retract.

=--

+-- {: .num_cor }
###### Corollary

A cofibration into a fibrant object is a weak equivalence precisely if it is an anodyne extension.

=--

([Cisinski 06, cor 1.3.35](#Cisinski06)).

+-- {: .proof}
###### Proof

By lemma \ref{EveryAnodyneExtensionIsWeakEquivalence} we already know that every anodyne extension is a weak equivalence. So we need to show that a cofibration $i : A \to T$ into a fibrant object $T$ which is a weak equivalence is also an anodyne extension. By prop. \ref{FactorAnodyneFollowedByRLPAnodyne} we may factor this as $i = q \circ j$, with $j$ an anodyne extension and $Q$ having RLP against anodyne extensions. Since $j$ is a weak equivalence, by 2-out-of-3 so is $q$. By lemma \ref{NaiveFibIntoFibIsWeakEquivIffItIsAcyclicFib} $q$ is an acyclic fibration.

Therefore we have a lift $s$ in 

$$
  \array{
     &\stackrel{id}{\to}&
    \\
    \downarrow^{\mathrlap{q}}
    &\nearrow_s&
    \downarrow^{\mathrlap{i}}
    \\
    &\stackrel{j}{\to}&
  }
$$

and this exhibits $i$ as a [[retract]] of $j$. Hence with $j$ also $i$ is an anodyne extension. 

=--

+-- {: .num_prop }
###### Proposition

A cofibration is a weak equivalence precisely if it has the [[left lifting property]] against morphisms into a fibrant object that have the right lifting property against anodyne extensions.

=--

([Cisinski 06, prop.  1.3.36](#Cisinski06)).

+-- {: .proof}
###### Proof

(...)

=--

+-- {: .num_cor }
###### Corollary

The acyclic cofibrations are stable under [[transfinite composition]] and [[pushouts]]

=--

([Cisinski 06, cor.  1.3.37](#Cisinski06)).

+-- {: .num_lemma }
###### Lemma

Every [[strong deformation retract]] is an anodyne extension.

=--

([Cisinski 06, cor.  1.3.38](#Cisinski06)).

+-- {: .num_lemma }
###### Lemma

Every anodyne extension between fibrant objects is a [[strong deformation retract]].

=--

([Cisinski 06, lemma  1.3.39](#Cisinski06)).


+-- {: .num_prop }
###### Proposition

Pour tout cardinal assez grand $\alpha$, si on pose $\beta = 2^\alpha$, pour toute cofibration triviale $i : C \to D$, et pour tout [[subobject|sous-objet]] $\beta$-accessible $J$ de $D$, il
existe un sous-objet $\beta$-accessible $K$ de $D$, qui contient $J$, tel que l'inclusion canonique $C \cap K  \to K$ soit une 
cofibration triviale.

=--

([Cisinski 06, prop.  1.3.40](#Cisinski06)).

+-- {: .proof}
###### Proof

Three pages of work...

=--

+-- {: .num_prop #GeneratingAcyclicCofibrationsExist}
###### Proposition

There exists a set of generating acyclic cofibrations.

=--

([Cisinski 06, prop.  1.3.42](#Cisinski06)).

+-- {: .proof}
###### Proof

Use lemma \ref{LemmaForGenerationOfMonos} with $C$ the class of acyclic cofibrations and $D = Acc_\alpha(A)$ the set of $\alpha$-accessible presheaves for a sufficiently large cardinal $\alpha$. 

=--

+-- {: .num_cor #FactorizationAcyclicCofibFib}
###### Corollary

There is a functorial factorization of every morphism into an acyclic cofibration followed by a fibration.

=--

([Cisinski 06, cor.  1.3.43](#Cisinski06)).

+-- {: .proof}
###### Proof

By prop. \ref{GeneratingAcyclicCofibrationsExist} and prop. \ref{PresheavesAreCompact} we may apply the [[small object argument]].

=--

#### Completeness
 {#Completeness} 

We list lemmas to show prop. \ref{ConditionsForCompleteness}.

(...)

### Localizers
 {#ALocalizers}

Continuing to let $A$ be a [[small category]], write $PSh(A)$ for its [[category of presheaves]].

+-- {: .num_defn #ALocalizer}
###### Definition

An **$A$-localizer** is a [[class]] of morphisms $W \subset Mor(PSh(A))$ satisfying the following axioms

1. [[2-out-of-3]];

1. every acyclic fibration, def. \ref{AcyclicFibration}, is in $W$;

1. The class of [[monomorphisms]] that is in $W$ is stable under [[pushout]] and [[transfinite composition]].

The elements of $W$ we call **$W$-equivalences**. For $S \subset Mor(PSh(A))$ a [[class]] of morphisms, the smallest $A$-localizer containing $S$ is called the $A$-localized **generated** by $S$. If an $A$-localizer is generated from a [[small set]], we call it **accessible**. The **minimal $A$-localizer** is $W(\emptyset)$. 

=--

([Cisinski 06, def. 1.4.1](#Cisinski06)))

+-- {: .num_prop}
###### Proposition

For $(J,AnExt)$ a homotopical structure, def. \ref{HomotopicalStructure} on $PSh(A)$, the class $W$ of weak equivalences of the induced model category structure of theorem \ref{ModelStructureFromHomotopicalStructure} is an $A$-localizer.

If $\Lambda$ is a small set generating the anodyne extensions, $AnExt = LLP(RLP(\Lambda))$, then $W = W(\Lambda)$. 

=--

([Cisinski 06, prop. 1.4.2](#Cisinski06)))

\begin{thm} \label{TheoremCharacterisationOfAccessibleLocalisersForPresheafCategories} Let $W \subset Mor(PSh(A))$. The following are equivalent.

1. $W$ is an accessible $A$-localizer, def. \ref{ALocalizer};

1. There is a set $S \subset Mor(PSh(A))$ of monomorphisms, such that $W$ is the class of weak equivalences of the model structure induced by theorem \ref{ModelStructureFromHomotopicalStructure} from the homotopical structure, def. \ref{HomotopicalStructure}, given by the Lawvere cylinder, def. \ref{LawvereCylinder}, and $AnExt := S$.

1. There is some homotopical structure, def. \ref{HomotopicalStructure}, on $PSh(A)$, such that $W$ is the class of weak equivalences of the model structure corresponding to it by theorem \ref{ModelStructureFromHomotopicalStructure}.

1. There exists a [[cofibrantly generated model category]] on $PSh(A)$ such that $W$ is its class of weak equivalences, and such that the cofibrations are the monomorphisms.

In particular, $PSh(A)$ admits a model structure whose cofibrations are the monomorphisms and whose weak equivalences are the minimal localizer, $W(\emptyset)$. This is called the **minimal model structure** on $PSh(A)$. It is generated from the homotopical datum given by the Lawvere cylinder, example \ref{LawvereCylinder} and the empty set.

\end{thm}

([Cisinski 06, theorem 1.4.3](#Cisinski06))

+-- {: .num_remark}
###### Remark

This may be compared to [[Jeff Smith's theorem]], which constructs a model structure on a [[locally presentable category]]. 

=--

([Cisinski 06, scholie 1.4.6](#Cisinski06)))

### Simplicial completion
 {#SimplicialCompletion}

Give a localizer $W$ on $PSh(A)$, there is a localizer $W_{horiz}$ on $PSh(A \times \Delta)$

$$
  W_{horiz} \coloneqq
  \{
    X \times q^* (\Delta_1) \to X
  \}
  \,.
$$

(...)

See ([Ara, p. 9](#Ara)).

## Examples
 {#Examples}

* The archetypical and motivating example is the [[classical model structure on simplicial sets]], which is a Cisinski model structure on the [[presheaf topos]] over the [[simplex category]] ([Cisinski 06, section 2](#Cisinski06)).

* Accordingly, the _injective_ [[model structure on simplicial presheaves]] over a site $C$ is a Cisinski model structure, namely on the [[presheaf topos]] $PSh(C \times \Delta)$. Moreover, every [[Bousfield localization of model categories|left Bousfield localization]] of such a model structure is still a Cisinski model structure, since left Bousfield localization preserves the class of cofibrations.

  Notice that, as discussed there, every [[presentable (infinity,1)-category]] has a presentation by such a localization, hence by a Cisinski model structure.

* Also the [[model structure for quasi-categories]] is a Cisinski model structure on [[sSet]], induced by the localizer given by the [[spine]] inclusions.

  Moreover, the [[model structure for complete Segal spaces]] is the [simplicial completion](#SimplicialCompletion) of this model structure. (see [Ara](#Ara)).

* As a [[cellular set]]-variant of this, the _[[model structure on cellular sets]]_ is a Cisinski model structure on the category of presheaves over the [[Theta category]] restricted to $n$-cells.

* The [[model structure on dendroidal sets]] is not exactly a Cisinki model structure, but is [[transferred model structure|transferred]] from one that is.

* For any small category $A$, the homotopical datum (Definition \ref{DefinitionHomotopicalDatum}) given by the $(J, \emptyset)$, where $J$ is the Lawvere cylinder (Definition \ref{LawvereCylinder}), generates a Cisinki model structure on the category of presheaves on $A$. By  ([Cisinski 06, rem. 1.3.15](#Cisinski06)), a set of generating anodyne extensions is $A\times \Omega \cup_A B \to B \times \Omega$ where $A \to B$ are generators for the class of monomorphisms. This is sometimes known as the [[minimal Cisinski model structure]]. See also Theorem \ref{TheoremCharacterisationOfAccessibleLocalisersForPresheafCategories}.


## Properties

### Properness

+-- {: .num_theorem #RightProper}
###### Theorem
If $W(\Sigma)$ is the localizer generated by a set $\Sigma$ in a Grothendieck topos, then (the Cisinski model structure whose weak equivalences are) $W(\Sigma)$ is [[right proper model category|right proper]] if and only if pullback along fibrations between fibrant objects in this model structure takes morphisms in $\Sigma$ to weak equivalences.
=--

This is [Cisinski 02, Th&#233;or&#232;me 4.8](#Cisinski02). This is closely related to (but not a consequence of) a theorem of Bousfield that applies to any model category whatsoever; see [[proper model category#FibrationsBetweenFibrantObjectsSuffice|this proposition]].

We can use this to prove that a [[locally presentable (∞,1)-category]] is [[locally cartesian closed (∞,1)-category]] if and only if it has a presentation by a right proper Cisinski model structure.  See [[locally cartesian closed (∞,1)-category]] for details.


## Related concepts

* [[test topos]]

## References
 {#References}

The original articles are

* {#Cisinski02} [[Denis-Charles Cisinski]] , _Th&#233;ories homotopiques dans les topos_, JPAA, Volume 174 (2002), p.43-82
 

* {#Cisinski06} [[Denis-Charles Cisinski]], _Les préfaisceaux comme types d'homotopie|Les préfaisceaux comme modèles des types d'homotopie_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([numdam:AST_2006__308__R1_0](http://www.numdam.org/item/?id=AST_2006__308__R1_0) [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 
A more recent, English presentation of much of this material appears in section 2.4 of

* {#Cisinski20} [[Denis-Charles Cisinski]], _Higher category theory and homotopical algebra_ ([pdf](http://www.mathematik.uni-regensburg.de/cisinski/CatLR.pdf))

Further developments are in

* [[Rick Jardine]], _Categorical homotopy theory_ (2003) ([K-theory](http://www.math.uiuc.edu/K-theory/0669/)) 

* [[Marc Olschok]], _On constructions of left determined model structures_, PhD thesis (2009) ([pdf](http://is.muni.cz/th/183259/prif_d/diss.pdf))

* [[Simon Henry]], _Minimal model structures_, [arXiv:2011.13408](https://arxiv.org/abs/2011.13408).

Some work on generalizing from presheaf toposes to all toposes is in

* [[Denis-Charles Cisinski]], _Faisceaux localement asphériques_ (preliminary version), 2003, [pdf](http://www.mathematik.uni-regensburg.de/cisinski/mtest2.pdf)

See also

* [[André Joyal]], _[[joyalscatlab:Cisinski's theory]]_

* [[Dimitri Ara]], _Higher quasi-categories vs higher Rezk spaces_ ([arXiv:1206.4354](http://arxiv.org/abs/1206.4354))
 {#Ara}

[[!redirects Cisinski model structures]]

[[!redirects Cisinski model category]]
[[!redirects Cisinski model categories]]
