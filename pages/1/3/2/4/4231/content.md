
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

We discuss how on a [[presheaf topos]] equipped with a suitable notion of [[interval objects]] Cisinski model structures can be characterized fairly explicitly. 

(This follows section 1.3 of [Cisinski 06](#Cisinski06)).

Let $A$ be a [[small category]]. Write $PSh(A)$ or $[A^{op}, Set]$ for the [[category of presheaves]] over $A$.

+-- {: .num_defn #FunctorialCylinder}
###### Definition

For $X$ in $PSh(A)$,  **cylinder** on $X$ in the following means a [[cylinder object]]

$$
  X \coprod X \to I \otimes X \to X
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

one $f' \Rightarrow g'$, consider the functorial cyclinder of the former [[pasting diagram|pasted]] to the latter

$$
  \array{
    && X
    \\
    & & \downarrow & \searrow^{\mathrlap{f}}
    \\
    & \swarrow& I \otimes X && Y
    \\
    && \downarrow & \searrow^{\mathrlap{I \otimes f}} & \downarrow & \searrow^{\mathrlap{f'}}
    \\
    I \otimes X &\stackrel{}{\to}&
    I \otimes I \otimes X &\stackrel{I \otimes \eta}{\to}& I \otimes Y
   &\stackrel{\eta'}{\to}& Z
    \\
    && \uparrow & \nearrow_{\mathrlap{I \otimes g}} & \uparrow & \nearrow_{\mathrlap{g'}}
    \\
    & \nwarrow & I \otimes X  && Y
    \\
    && \uparrow & \nearrow_{\mathrlap{g}}
    \\
    && X 
  }
  \,.
$$

This exhibits an elementary $J$-homotopy $f' \circ f \Rightarrow g' \circ g$.

=--


It follows that the following is well defined.

+-- {: .num_defn}
###### Definition

Write $Ho_J(A)$ exists for the category whose objects are those of $PSh(A)$, and whose morphisms are $J$-homotopy equivalence classes of morphisms in $PSh(A)$. Write

$$
  Q : PSh(A) \to Ho_J(A)
$$

for the projection functor.

=--

+-- {: .num_defn}
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

Every trivial fibration in $PSh(A)$ is a $J$-homotopy equivalence.

More is true: every trivial fibration $p : X \to Y$

1. has a [[section]] $s : Y \to X$;

1. which is also a $J$-homotopy left inverse;

1. by an elementary $J$-homotopy $h : id \Rightarrow s \circ p$ which satisfies
   $p \circ h = p \circ \sigma_X$.

=--

([Cisinski 06, lemma 1.3.5](#Cisinski06)).

+-- {: .proof}
###### Proof

(...)

=--

+-- {: .num_defn}
###### Definition

An **elementary homotopical datum** on $(PSh(A)$ is a functorial cylinder $J$ such that 

1. the functor $X \mapsto J \otimes X$ commutes with small [[colimits]];

1. for all [[monomorphisms]] $f : K \to L$ the [[diagrams]]

   $$
     \array{
       K &\stackrel{(id, f)}{\to}& L
       \\
       {}^{\mathllap{(e,id)}}\downarrow && \downarrow^{\mathrlap{(e,id)}}
       \\
       J \otimes K &\stackrel{J(f)}{\to}& J \otimes L
     } 
   $$
   
   for $e \in \{0,1\}$ is a [[pullback]] square.

=--

([Cisinski 06, def. 1.3.6](#Cisinski06)).

+-- {: .num_remark}
###### Remark

The second condition is equivalent to the canonical morphism

$$
  J \otimes K \cup (\partial J) \otimes L \to J \otimes L
$$

being a [[monomorphism]].

=--

([Cisinski 06, remark 1.3.7](#Cisinski06)).


+-- {: .num_defn #AnodyneExtensions}
###### Definition

For $J$ an elementary homotopical datum on $PSh(A)$, a **[[class]] of [[anodyne extensions]]** is a class $AnExt \subset Mor(PSh(A))$ such that

1. there exists a [[small set]] $S$ with 

   $$
     AnExt = LLP(RLP(S))
   $$
  
1. for $K \hookrightarrow L$ a monomorphism, the [[pushout-product axiom|pushout product]] morphism

   $$
     J \otimes K \cup \{e\} \otimes L \to J \otimes L
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

+-- {: .num_prop}
###### Proposition

A class of anodyne extensions 

* is closed under [[pushouts]], [[transfinite composition]] and [[retracts]];

* admits a [[small object argument]];

* is a subclass of the [[monomorphisms]]; 

* contains all morphisms of the form $e : K \to J \otimes K$;

* is closed under $J\otimes(-)$;

=--

([Cisinski 06, remark. 1.3.11](#Cisinski06)).

+-- {: .num_defn #HomotopicalStructure}
###### Definition

A **homotopical structure** on $PSh(A)$ is a choice of elementery homotopical datum $J$, and a corresponding choice of a class of anodyne extensions $AnExt$.

=--

([Cisinski 06, def. 1.3.14](#Cisinski06)).


+-- {: .num_defn #ModelStructureFromHomotopicalStructure}
###### Definition

Let $A$ be a [[small category]] and $(J, AnExt)$ a homotopical structure on $PSh(A)$. Define the following classes of objects and morphisms in $PSh(A)$:

* the **cofibrations** are the [[monomorphisms]];

* the **fibrant objects** are those $X \in PSh(A)$ for which  the [[terminal object|terminal]] morphism $X \to *$ has the [[right lifting property]] against the anodyne extensions (the morphisms in $AnExt$);

* the **weak equivalences** are those morphisms $f : A \to B$, such that for all fibrant objects $X$ the induced morphism

  $$
    Ho_J(f,X) : Ho_J(B,X) \to Ho_J(A, X)
  $$

  is an [[isomorphism]] (a [[bijection]] of sets).

=--

([Cisinski 06, def. 1.3.21](#Cisinski06)).


+-- {: .num_theorem #ModelStructureFromHomotopicalStructure}
###### Theorem

With the classes of morphisms as in def. \ref{ModelStructureFromHomotopicalStructure}, $PSh(A)$ is a [[cofibrantly generated model category]].

=--

([Cisinski 06, theorem 1.3.22](#Cisinski06)).

The following two statements say that the terminology introduced so far is indeed consistent with the meaning of this theorem.

+-- {: .num_prop }
###### Proposition

The morphisms called _acyclic fibrations_ in def. \ref{AcyclicFibration} are indeed precisely the acyclic fibration with respect to the model structure of theorem \ref{ModelStructureFromHomotopicalStructure}.

=--

([Cisinski 06, theorem 1.3.27](#Cisinski06)).

+-- {: .num_prop }
###### Proposition

Every anodyne extension, def. \ref{AnodyneExtensions}, is a weak equivalence in the model structure of theorem \ref{ModelStructureFromHomotopicalStructure}.

=--
## Examples

* The archetypical and motivating example is the standard [[model structure on simplicial sets]], which is a Cisinski model structure on the [[presheaf topos]] on the [[simplex category]].

* The [[model structure on dendroidal sets]] is not exactly a Cisinki model structure, but is [[transferred model structure|transferred]] from one that is.

## References

* [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 {#Cisinski06}

* [[Denis-Charles Cisinski]] , _Th&#233;ories homotopiques
dans les topos_, JPAA, Volume 174 (2002), p.43-82

* [[André Joyal]], _[[joyalscatlab:Cisinski's theory]]_

* [[Rick Jardine]], _Categorical homotopy theory_ ([K-theory](http://www.math.uiuc.edu/K-theory/0669/)) 

[[!redirects Cisinski model structures]]
