
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



## Definition

+-- {: .num_defn}
###### Definition

For $\mathcal{T}$ a [[topos]], a **Cisinski model structure** on $\mathcal{T}$ is a [[model category]] structure on $\mathcal{T}$ such that

1. the [[cofibrations]] are precisely the [[monomorphisms]];

1. it is a [[cofibrantly generated model category]].

=--


## Properties

### General existence

+-- {: .num_defn #Localizer}
###### Definition

Say a class $W \in Mor(\mathcal{T})$ is a **localizer** on $\mathcal{T}$ if it is a class of [[weak equivalences]] in a Cisinski model structure on $\mathcal{T}$.

=--

+-- {: .num_prop}
###### Proposition

Every [[small set]] of [[morphisms]] $\Sigma in Mor(\mathcal{T})$ is contained in a smallest localizer, def. \ref{Localizer}, $W(\Sigma)$. 

=--

One says that $W(\Sigma)$ is the 
localiser _generated_ by $\Sigma$.

So in particular a Cisinski model structure always exists.


### On presheaf toposes
 {#OnPresheafToposes}

We discuss how on a [[presheaf topos]] equipped with a suitable notion of [[interval objects]] Cisinski model structures can be characterized fairly explicitly. After some preliminaries, the main statement is theorem \ref{ModelStructureFromHomotopicalStructure} below. 

(This follows section 1.3 of [Cisinski 06](#Cisinski06)).

Let $A$ be a [[small category]]. Write $PSh(A)$ or $[A^{op}, Set]$ for the [[category of presheaves]] over $A$.

+-- {: .num_defn #FunctorialCylinder}
###### Definition

For $X$ in $PSh(A)$,  **cylinder** on $X$ in the following means a [[cylinder object]], denoted $I \otimes X$, factoring the [[codiagonal]]

$$
  X \coprod X \stackrel{(\partial_X^0, \partial_X^1)}{\to} I \otimes X \stackrel{\sigma_X}{\to} X
  \,,
$$

such that the first morphism is a [[monomorphism]]. 

A morphism of cyclinders is a pair of morphisms $X \to Y$ and $I \otimes X \to I \otimes Y$ in $PSh(A)$, makind the evident squares commute. This defines a category $Cyl(A)$ of cylinder objects on presheaves on $A$, equipped with a [[forgetful functor]] $Cyl(A) \to PSh(A)$ that sends a cylinder $I \otimes X$ to its underlying object $X$.

A **functorial cylinder object** over $A$ is a [[section]] of this functor.

=--

This is ([Cisinski 06, def. 1.3.1](#Cisinski06)).

In the following, let $J : PSh(A) \to Cyl(A)$ be a choice of functorial cylinder object.

+-- {: .num_defn}
###### Definition

For $f,g : X \to Y$ two morphisms in $PSh(A)$, we say an **elementary $J$-homotopy** $f \Rightarrow g$ from $f$ to $g$ is [[left homotopy]] from $f$ to $g$ with respect to the chosen cylinder object $J$, hence a morphism $\eta : I \otimes X \to Y$ fitting into a diagram

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

Write $Ho_J(A)$ for the category whose objects are those of $PSh(A)$, and whose morphisms are $J$-homotopy equivalence classes of morphisms in $PSh(A)$. Write

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

+-- {: .num_prop}
###### Proposition

Every trivial fibration in $PSh(A)$ is a $J$-homotopy equivalence, for every choice of interval $J$.

More is true: every trivial fibration $p : X \to Y$

1. has a [[section]] $s : Y \to X$;

1. which is also a $J$-homotopy left inverse;

1. by an elementary $J$-homotopy $h : id \Rightarrow s \circ p$ which satisfies
   $p \circ h = p \circ \sigma_X$



=--

([Cisinski 06, lemma 1.3.5](#Cisinski06)).

+-- {: .proof}
###### Proof

The existence of the section $s : Y \to X$ follows by right lifting against the monomorphism $\emptyset \to Y$ (out of the [[initial object]]).

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

An **elementary homotopical datum** on $(PSh(A)$ is a functorial cylinder $J$ such that 

1. the functor $X \mapsto I \otimes X$ commutes with small [[colimits]];

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

is also a monomorphism, usually written as the morphism out of the [[union]]

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

Regarding a functorial cyclinder object $J$ as a functor $I \otimes(-) : PSh(A) \to PSh(A)$, let 

$$
  \partial^\epsilon : \{\epsilon\}\otimes(-) \hookrightarrow I \otimes(-)
  \,,
$$

for $\epsilon = 0,1$, be the subfunctor which is the [[image]] of $\partial^\epsilon : Id_{PSh(A)} \to I \otimes (-)$.

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

is a [[pullback]] square (here $\emptyset$ is the [[initial object]] in $PSh(A)$). This induces a functorial sylinder by the assignment

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

The interval commutes with colimits as these and the product are computed objectwise, and products in [[Set]] commute with colimits. More abstractly: by the [[Giraud theorem]] valid in the [[presheaf topos]] $PSh(A)$ we have "[[universal colimits]]": they are preserved by pullback, and in particular by cartesian product.

Similarly, the second axiom of def. \ref{ElementaryHomotopicalDatum} holds because [[limits]] commute over each other.

=--

+-- {: .num_example}
###### Example

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

1. there exists a [[small set]] $S$ with 

   $$
     AnExt = LLP(RLP(S))
   $$
  
1. for $K \hookrightarrow L$ a monomorphism, the [[pushout-product axiom|pushout product]] morphisms

   $$
     (J \otimes K) \cup (\{e\} \otimes L) \to J \otimes L
   $$

   are in $AnAxt$, for $e \in \{0,1\}$;

1. if $K \to L$ is in $AnExt$, then so is

   $$   
     J \otimes K \cup (\partial J) \otimes L 
    \to 
     J \otimes L
     \,.
   $$

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

By the examples at _[[accessible category]]_ the functor co-represented by $X \in PSh(A)$, is commutes with $|Mor(A/X)|$-[[filtered colimits]]. Therefore the set $\Lambda$ admits a [[small object argument]], which shows the first statement (see there).

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

factored through the top pushout square, as indicated. Here $j'$ is anodyne, being a pushout of an anodyne morphism, and $k$ is anodyne by the second clause in def. \ref{PropertiesOfAnodyneExtensions}. Therefore also their composite $I \otimes j$ is anodyne.

=--


+-- {: .num_defn #HomotopicalStructure}
###### Definition

A **homotopical structure** on $PSh(A)$ is a choice of elementary homotopical datum $J$, def. \ref{ElementaryHomotopicalDatum} and a corresponding choice of a class of anodyne extensions $AnExt$, def. \ref{AnodyneExtensions}.

=--

([Cisinski 06, def. 1.3.14](#Cisinski06)).


+-- {: .num_defn #ModelStructureMorphismsFromHomotopicalStructure}
###### Definition

Let $A$ be a [[small category]] and $(J, AnExt)$ a homotopical structure on $PSh(A)$. Define the following classes of objects and morphisms in $PSh(A)$:

* the **cofibrations** are the [[monomorphisms]];

* the **fibrant objects** are those $X \in PSh(A)$ for which  the [[terminal object|terminal]] morphism $X \to *$ has the [[right lifting property]] against the anodyne extensions (the morphisms in $AnExt$);

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

+-- {: .num_prop }
###### Proposition

The [[homotopy category]] of this model category is [[equivalence of categories|equivalent]] to the [[full subcategory]] of the $J$-homotopy category, def. \ref{JHomotopyCategory}, on the fibrant objects

=--

Before coming to the proof of this statement, the following two statements say that the terminology introduced so far is indeed consistent with the meaning of this theorem.

+-- {: .num_prop }
###### Proposition

The morphisms called _acyclic fibrations_ in def. \ref{AcyclicFibration} are indeed precisely the acyclic fibration with respect to the model structure of theorem \ref{ModelStructureFromHomotopicalStructure}.

=--

([Cisinski 06, theorem 1.3.27](#Cisinski06)).

+-- {: .num_prop }
###### Proposition

Every anodyne extension, def. \ref{AnodyneExtensions}, is a weak equivalence in the model structure of theorem \ref{ModelStructureFromHomotopicalStructure}.

=--

Now we collect lemmas to prove theorem \ref{ModelStructureFromHomotopicalStructure}.


+-- {: .num_lemma }
###### Lemma

Every $J$-homotopy equivalence, def. \ref{JHomotopyEquivalence}, is a weak equivalence.

Every morphism that becomes invertible in the [[homotopy category]] is a weak equivalence.

In particular, therefore, the weak equivalences satisfy the [[two-out-of-three]]-property and are stable under [[retracts]].

=--

([Cisinski 06, remark 1.3.24](#Cisinski06)).

+-- {: .proof}
###### Proof

The first statement holds by definition of $Ho_J$. 

(...)

=--

## Examples

* The archetypical and motivating example is the standard [[model structure on simplicial sets]], which is a Cisinski model structure on the [[presheaf topos]] on the [[simplex category]].

* The [[model structure on dendroidal sets]] is not exactly a Cisinki model structure, but is [[transferred model structure|transferred]] from one that is.

## References

The original articles are

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 {#Cisinski06}

* [[Denis-Charles Cisinski]] , _Th&#233;ories homotopiques
dans les topos_, JPAA, Volume 174 (2002), p.43-82

Further developments are in

* [[Rick Jardine]], _Categorical homotopy theory_ (2003) ([K-theory](http://www.math.uiuc.edu/K-theory/0669/)) 

* [[Marc Olschok]], _On constructions of left determined model structures_ PhD thesis (2009) ([pdf](http://is.muni.cz/th/183259/prif_d/diss.pdf)) 

See also

* [[André Joyal]], _[[joyalscatlab:Cisinski's theory]]_


[[!redirects Cisinski model structures]]
