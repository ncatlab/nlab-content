
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}
 
## Idea {#Idea}

The definition of _cohesive topos_ or _category of cohesion_ aims to axiomatize properties of a [[topos]] that make it a [[gros topos]] of [[space]]s inside of which [[geometry]] may take place.

The idea behind the term is that a _geometric space_ is roughly something consisting of points or pieces that are _held together_ by some cohesion - for instance by [[topology]], by [[smooth structure]], etc.

The canonical [[global section]] geometric morphism $\Gamma : \mathcal{E} \to Set$ of a cohesive topos over [[Set]] may be thought of as sending a space $X$ to its underlying set of points $\Gamma(X)$. Here $\Gamma(X)$ is $X$ with all _cohesion forgotten_ (for instance with the topology or the smooth structure forgotten)

Conversely, the [[left adjoint]] and [[right adjoint]] of $\Gamma$

$$
  \mathcal{E} 
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  Set
$$

send a set $S$ either to the [[discrete space]] $Disc(S)$ with _discrete_ cohesive structure (for instance with [[discrete topology]]) or to the [[codiscrete space]] $Codisc(S)$ with the _codiscrete_ cohesive structure (for instance with [[codiscrete topology]]) .

Moreover, the idea is that cohesion makes points lump together to _connected pieces_ . This is modeled by one more functor $\Pi_0 : \mathcal{E} \to Set$ [[left adjoint]] to $Disc$. In the context of 1-[[topos theory]] this sends a cohesive space to its [[connected topos|connected components]] $(\Pi = \pi_0)$. More generally in an [[(n,1)-topos]]-theory context, $\Pi$ sends a cohesive space $X$ to the $(n-1)$-[[truncated|truncation]] of its [[geometric homotopy groups in an (∞,1)-topos|geometric fundamental ∞-groupoid]] $\Pi(X)$. See [[cohesive (∞,1)-topos]].

In total this gives an [[adjoint quadruple]]

   $$
    (\Pi_0 \dashv Disc \dashv \Gamma \dashv Codisc) : 
    \mathcal{E}
     \stackrel{\stackrel{\overset{\Pi}{\to}}{\overset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
    Set
    \;
   $$

A cohesive topos is a topos whose terminal [[geometric morphism]] admits an extenson to such a quadruple of adjoints, satisfying some further properties.

Notice that most objects in a cohesive topos are far from being just sets with extra structure: while the functor $\Gamma$ does produce the set of points underlying an object $X$ in the cohesive topos, it may happen that $X$ is very non-trivial but that nevertheless $\Gamma(X)$ has very few [[global element|points]] (possibly none, with the axioms so far). The [[subcategory]] of objects in $E$ that we may think of as point sets equipped with extra structure is the [[quasitopos]] $Conc_\Gamma(E)$ of the [[concrete sheaves]] inside $E$

$$
  Set 
   \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\hookrightarrow}}
  Conc_\Gamma(\mathcal{E}) 
    \stackrel{\overset{Conc}{\leftarrow}}{\hookrightarrow}
  \mathcal{E}
  \,.
$$

It is the fact that $\mathcal{E}$ is a [[local topos]] that allows to identify $Conc_\Gamma(E)$.

To ensure that there is a minimum of points, one can add further axioms. From the above adjunctions one gets a canonical natural morphism

$$
  \Gamma X \to \Pi_0 X
$$

from the points of $X$ to the set of connected pieces of $X$. Demanding this to be an [[epimorphism]] is demanding that _each piece has at least one point_ .

Moreover, one can demand that the cohesive pieces of product or power spaces are the products of the cohesive pieces of the factors.  For powers of a single space, this is demanding that for all $S \in Set$ the following canonical map is an [[isomorphism]]:

$$
  \Pi_0(X^S) \xrightarrow{\simeq} (\Pi_0(X))^S
  \,.
$$

For more general products, it would be a similar map $\Pi_0(\prod_i X_i) \to \prod_i \Pi_0(X_i)$.  See the examples at [[cohesive site]] for concrete illustrations of these ideas.


## Definition


+-- {: .num_defn #CohesiveTopos}
###### Definition

A [[topos]] $\mathcal{E}$ over some base topos $\mathcal{S}$, i.e. equipped with a [[geometric morphism]]

$$
  (f^* \dashv f_*) : \mathcal{E} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  \mathcal{S}
$$

is **cohesive** if it is a

* [[strongly connected topos]]

* and a [[local topos]].

In detail this means that it has the following [[stuff, structure, property|properties]]:

1. it is a [[locally connected topos]]: there exists a further [[left adjoint]] $(f_! \dashv f^*)$ satisfying a suitable condition;

1. it is a [[connected topos]]: the functor $f_!$ preserves the [[terminal object]], or equivalently $f^*$ is [[fully faithful functor|fully faithful]];

1. it is _[[strongly connected topos|strongly connected]]_ : $f_!$ preserves even all [[finite]] [[product]]s;

1. it is a [[local topos]]: there exists a further [[right adjoint]] $(f_* \dashv f^!)$ (this is sufficient for $f$ to be local, since we have already assumed it to be connected);

In summary $\mathcal{E}$ is cohesive over $\mathcal{S}$ if we have a quadruple of [[adjoint functor]]s
   
$$
 (f_! \dashv f^* \dashv f_* \dashv f^!) : 
 \mathcal{E}
  \stackrel{\stackrel{\overset{f_!}{\to}}{\overset{f^*}{\hookleftarrow}}}{\stackrel{\underset{f_*}{\to}}{\underset{f^!}{\hookleftarrow}}}
  \mathcal{S}
$$

such that $f_!$ preserves finite products.

=--

+-- {: .num_remark}
###### Remark

With $f^*$ being a [[full and faithful functor]] also $f^!$ is, as indicated (for instance by the discussion at [[adjoint triple]]). 

Hence the definition of cohesion specifies two [[full subcategories]], equivalent to each other, both [[coreflective subcategory|coreflective]] and one also [[reflective subcategory|reflective]].

Since a [[topos]] is a [[cartesian closed category]] it follows with the
discussion [here](http://ncatlab.org/nlab/show/reflective+subcategory#ReflectiveSubcategoriesOfCartesianClosedCategotries) that both of these are [[exponential ideals]]. In fact the condition that the $f^*$-inclusion is an exponential ideal is equivalent to the condition that $f_!$ preserves finite products. 

=--

To reflect the geometric interpretation of these axioms we will here and in related entries often name these functors as follows

$$
 (\Pi_0 \dashv Disc \dashv \Gamma \dashv coDisc) : 
 \mathcal{E}
  \stackrel{\stackrel{\overset{\Pi_0}{\to}}{\overset{Disc}{\hookleftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{coDisc}{\hookleftarrow}}}
  \mathcal{S}
  \,.
$$

+-- {: .num_remark #AdjointTriple}
###### Remark

The above [[adjoint quadruple]] canonically induces an [[adjoint triple]] of endofunctors on $\mathcal{E}$

$$
  (\mathbf{\Pi}_0 \dashv \mathbf{\flat} \dashv \mathbf{#})
  : 
  \mathcal{E}
   \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}}
  \mathcal{S}
  \stackrel{\overset{Disc}{\to}}{\stackrel{\overset{\Gamma}{\leftarrow}}{\underset{coDisc}{\to}}}
  \mathcal{E} 
  \,.
$$

These endofunctors play a role in the internal characterization of cohesion.

=--

There are several further axioms that one may want to impose in order to formalize the concept of cohesion.

+-- {: .num_defn #PiecesHavePoints}
###### Definition

For $f : \mathcal{E} \to \mathcal{S}$ a cohesive topos, we say that **pieces have points** in $\mathcal{E}$ if the [[natural transformation]]

$$
  f_* X \stackrel{}{\to} f_* f^* f_! X \stackrel{\simeq}{\to} f_! X 
$$

is an [[epimorphism]] for all $X \in \mathcal{E}$.

=--

This is equivalent to the following condition (see the [proposition below](PiecesHavePointsEquivalentToDiscreteObjectsAreConcrete)):

+-- {: .num_defn #DiscreteObjectsAreConcrete}
###### Definition

We say that **[[discrete objects]] are [[concrete object|concrete]]** in $\mathcal{E}$ if the transformation

$$
  f^* S \to f^! f_* f^* S \stackrel{\simeq}{\to} f^! S
$$

is a [[monomorphism]] for all $S \in \mathcal{S}$ .

=--

+-- {: .num_defn }
###### Definition

We say **pieces of powers are powers of pieces** if for all $S \in \mathcal{S}$ and $X \in E$ the natural morphism

$$
  f_! (X^{f^* S}) \stackrel{\simeq}{\to} (f_!(X))^S
$$

is an [[isomorphism]].

=--

+-- {: .num_remark }
###### Remark

This morphism is the [[internal hom]]-[[adjunct]] of 

$$
  S \times f_!(X^{f^* S}) 
   \stackrel{\simeq}{\to}
  f_!f^*(S) \times f_!(X^{f^* S})
   \stackrel{\simeq}{\to}
  f_!(f^*(S) \times X^{f^* S})
  \to
  f_!(X)
$$

where we use that by definition $f^*$ is [[full and faithful functor|full and faithful]] and then that $f_!$ preserves [[product]]s).

=--


These extra axioms are proposed in ([Lawvere, Axiomatic cohesion](#LawvereAxiomatic)). 

+-- {: .num_defn}
###### Definition

For $f : \mathcal{E} \to \mathcal{S}$ a cohesive topos, we say that 
its **subobject classifier is contractible** if for the [[subobject classifier]] $\Omega \in \mathcal{E}$ we have

$$
  f_!(\Omega) \simeq *
  \,.
$$

This implies that for all $X \in \mathcal{E}$ also $f_! \Omega^X \simeq *$.


=--

This appears as axiom 2 in ([Lawvere, Categories of spaces](#LawvereCatsOfSpaces)).

+-- {: .num_remark}
###### Remark

There is some overlap between the structures and conditions appearing here and those considered in the context of [[Q-categories]]. See there for more details.

=--

## Properties 
  {#Properties}

We discuss properties of cohesive toposes. We start in

* [Adjoint quadruples](#AdjointQuadruples)

with some generalities on situations where a sequence of four adjoint functors is given. Then in 

* [Relations between the axioms](#RelationsBetweenTheAxioms)

we comment on the interdependency of the collection of axioms on a cohesive topos. In

* [Quasitopos of concrete objects](#ConcreteObjects)

we discuss the induced notion of concrete objects that comes with every cohesive topos and in

* [Objects with one point per cohesive piece](#ObjectsWithOnePointPerCohesivePiece)

the induced subcategory of objects with one point per piece.

Some of these phenomena have a natural 

* [Modality interpretation](#Modality).

For a long list of further structures that are canonically present in a cohesive context see

* [[cohesive (∞,1)-topos -- structures]]

* [[cohesive (∞,1)-topos -- infinitesimal cohesion]] .

### Adjoint quadruples
  {#AdjointQuadruples}

Let $(p_! \dashv p^* \dashv p_*\dashv p^!) : \mathcal{E} \to \mathcal{S}$ be an  [[adjoint quadruple]] of [[adjoint functor]]s such that $p^*$ and $p^!$ are [[full and faithful functor]]s. We record some general properties of such a setup.

We write 

$$
  \iota : id \to p^* p_!
$$

etc. for [[unit of an adjunction|units]] and

$$
  \eta : p_! p^* \to id
$$

etc. for counits.

+-- {: .num_prop #TheCanonicalMorphisms}
###### Proposition/Definition

We have [[commuting diagram]]s, [[natural transformation|natural]] in $X \in \mathcal{E}$, $S \in \mathcal{S}$

$$
  \array{
    p_*X  &\stackrel{\eta_{p^* X}^{-1}}{\to}& p_! p^* p_*X
    \\
    {}^{\mathllap{p_*(i_X)}}\downarrow 
    &\searrow^{\mathrlap{\theta_X}}& 
    \downarrow^{\mathrlap{p_!(\eta_X)}}
    \\
    p_* p^* p_! X &\stackrel{\iota_{p_!X}^{-1}}{\to}& p_! X
  }
$$

and

$$
  \array{
    p^* S &\stackrel{\iota_{p^* S}}{\to}& p^! p_* p^* S
    \\
    {}^{\mathllap{p^* \epsilon_S^{-1}}}\downarrow 
    &\searrow^{\mathrlap{\phi_X}}& \downarrow^{\mathrlap{p^!(\iota_S^{-1})}}
    \\
    p^* p_* p^!S  &\stackrel{{\epsilon}_{p_!S }}{\to}& p^!S
  }
  \,.
$$

where the diagonal morphisms

$$
  \theta_X : p_* X \to p_! X
$$

and 

$$
  \phi_S : p^* S \to p^! S
$$

are defined to be the equal composites of the sides of these diagrams.

=--

This appears as ([Johnstone, lemma 2.1, corollary 2.2](#Johnstone)).

+-- {: .num_prop #TheEpiAndTheMono}
###### Proposition

The following conditions are equivalent:


* for all $X \in \mathcal{E}$ the morphism $\theta_X : p_*X \to p_! X$ is an [[epimorphism]];

* for all $S \in \mathcal{S}$,, the morphism $\phi_S : p^*S \to p^! S$ 
  is a [[monomorphism]];

* $p_*$ is [[faithful functor|faithful]] on morphisms of the form $A \to p^* S$.

=--

This appears as ([Johnstone, lemma 2.3](#Johnstone)).



+-- {: .proof}
###### Proof

By the above definition, $\phi_S$ is a [[monomorphism]] precisely if $\iota_{p^* S} : p^* S \to p^! p_* p^* S$ is. This in turn is so (see [[monomorphism]]) precisely if the first [[function]] in

$$  
    \mathcal{E}(A,p^* X) 
     \stackrel{(\iota_{p^* X}) \circ (-)}{\to} 
    \mathcal{E}(A, p^! p_* p^* S)
     \stackrel{\simeq}{\to}
    \mathcal{S}(p_* A, p_* p^* S)
$$

and hence the composite is a monomorphism in [[Set]].

By definition of [[adjunct]] and using the $(p_* \dashv p^!)$-[[zig-zag identity]], this is equal to the action of $p_*$ on morphisms

$$
  (\iota_{p^* X}) \circ (-)  : 
  (A \to p^* S) \mapsto p_*(A \to p^* S)  
  \,.
$$

Similarly, by the above definition the morphism $\theta_X$ is an epimorphism precisely if $p_!(\eta_X) : p_! p^* p_* X \to p_! X$ is so, which is the case precisely if the top morphism in

$$
  \array{
    \mathcal{S}(p_! X, S) 
      &\stackrel{(-) \circ p_!(\eta_X)}{\to} &
    \mathcal{S}(p_! p^* p_* X, S)
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    && \mathcal{E}(p^* p_* X, p^* S)
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    \mathcal{E}(X, p^* S) &\stackrel{p_*}{\to}& \mathcal{S}(p_* X, p_* p^* S)
  }
$$

and hence the bottom morphism is a monomorphism in [[Set]],
where again the commutativity of this diagram follows from the 
definition of [[adjunct]] and the 
$(p_! \dashv p^*)$-[[zig-zag identity]].

=--

### Relations between the axioms
  {#RelationsBetweenTheAxioms}

We record some relations between the various axioms characterizing cohesive toposes.

+-- {: .num_prop #PiecesHavePointsEquivalentToDiscreteObjectsAreConcrete}
###### Proposition

The axioms [pieces have points](#PiecesHavePoints) and [discrete objects are concrete](#DiscreteObjectsAreConcrete) are equivalent.

=--

This is just a reformulation of the [above proposition](#TheEpiAndTheMono).

+-- {: .num_prop}
###### Proposition

A [[sheaf topos]] that

1. is [[locally connected topos|locally connected]] and [[connected topos|connected]];

1. satisfies [pieces have points](#PiecesHavePoints)

also is

1. [[local topos|local]];

1. [[hyperconnected topos|hyperconnected]];

1. [[strongly connected topos|strongly locally connected]]

1. [cohesive](#CohesiveTopos).

=--

The statement of the first items appears as ([Johnstone, prop. 1.6](#Johnstone)). The last item is then a consequence by definition.

+-- {: .num_prop #HyperconnectivityAndPiecesHavePoints}
###### Proposition

For a [[sheaf topos]] the condition that it

1. is [[locally connected topos|locally connected]];

1. is [[connected topos|connected]];

1. satisfies [pieces have points](#PiecesHavePoints)

is equivalent to the condition that it

1. is [[locally connected topos|locally connected]];

1. is [[hyperconnected topos|hyperconnected]];

1. is [[local topos|local]].

=--

This is ([Johnstone, theorem 3.4](#Johnstone)).

### Subcategories of discrete and codiscrete objects

+-- {: .num_prop }
###### Proposition

The [[reflective subcategories]] of [[discrete objects]] and of [[codiscrete objects]] are both [[exponential ideals]].

=--

+-- {: .proof}
###### Proof

By the discussion at [[exponential ideal]] a reflective subcategories of a [[cartesian closed category]] is an exponential ideal precisely if the [[reflector]] preserves [[products]]. For the [[codiscrete objects]] the reflector $\Gamma$ preserves even all [[limits]] and for the [[discrete objects]] the reflector $\Pi$ does so by assumotion of strong connectedness.

=--

### Quasitoposes of concrete objects 
  {#ConcreteObjects}

A cohesive topos comes canonically with various [[subcategories]], sub-[[quasi-toposes]] and [[subtopos]]es of interest. We discuss some of these.


+-- {: .num_lemmaa}
###### Observation

For $(\Pi \dashv \Disc \dashv \Gamma \dashv coDisc) :  \mathcal{E} \to Set$ a cohesive topos, $(\Gamma \dashv coDisc)$ exhibits $Set$ as a [[subtopos]]

$$
  (\Gamma \dashv \coDisc) : Set \stackrel{\leftarrow}{\hookrightarrow}
  \mathcal{E}
  \,.
$$

=--

+-- {: .proof}
###### Proof

By general properties of [[local topos]]es. See there.

=--

+-- {: .num_lemma}
###### Observation

The category $Set$ is equivalent to the full [[subcategory]] of $\mathcal{E}$ on those objects $X \in \mathcal{E}$ for which the $(\Gamma \dashv coDisc)$ [[unit of an adjunction|unit]]

$$
  X \to coDisc \Gamma X
$$

is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

By general properties of [[reflective subcategories]]. See there for details.

=--

+-- {: .num_defn}
###### Definition

An object $X$ of the cohesive topos $\mathcal{E}$ for which $X \to coDisc \Gamma X$ is a [[monomorphism]] we call a **concrete object**. 


Write 

$$Conc(\mathcal{E}) \hookrightarrow \mathcal{E}$$

for the [[full subcategory]] on concrete objects.

=--

+-- {: .num_prop}
###### Proposition

The functor $\Gamma : \mathcal{E} \to Set$ is a [[faithful functor]] on morphisms $(X \to Y) \in \mathcal{E}$ precisely if $Y$ is a concrete object.

In particular, the restriction $\Gamma : Conc(\mathcal{E}) \to Set$ makes the category of concrete objects a [[concrete category]].

=--

+-- {: .proof}
###### Proof

Observe that the composite morphism

$$
  F 
  : 
  \mathcal{E}(X,Y) \stackrel{\Gamma}{\to} \mathcal{S}(\Gamma X, \Gamma Y)
  \stackrel{\simeq}{\to}
  \mathcal{E}(X, coDisc \Gamma Y)
$$

is given (see [[adjunct]]) by postcomposition with the $(\Gamma \dashv coDisc)$-[[unit of an adjunction|unit]] $\iota_Y : Y \to coDisc \Gamma Y$

$$
  \array{
    X &\to& Y
    \\
    \downarrow && \downarrow
    \\
    coDisc \Gamma X &\to& coDisc \Gamma Y
  }
  \,.
$$

The condition that $Y$ is a concrete object, hence that $Y \to coDisc \Gamma Y$ is a [[monomorphism]] is therefore equivalent (see there) to the condition that $F$ is a monomorphism, which is equivalent to $F$ being a [[faithful functor]].

=--

+-- {: .num_remark}
###### Remark

This means that in the formal sense discussed at [[stuff, structure, property]] we may regard $Conc(\mathcal{E})$ as a category of sets _equipped with cohesive structure_ .

=--


+-- {: .num_prop}
###### Proposition


The category $Conc(\mathcal{E})$ is a [[quasitopos]] and a [[reflective subcategory]] of $\mathcal{E}$.

=--

+-- {: .proof}
###### Proof


Let $(C,J)$ be a [[site]] of definition for $\mathcal{E}$ with [[coverage]] $J$, so that $\mathcal{E} = Sh_J(C) \hookrightarrow PSh(C)$. Since $Set \stackrel{CoDisc}{\hookrightarrow} \mathcal{E}$ is a subtopos, we have that $Set$ is itself a [[category of sheaves]] on $C$

$$
  Set \simeq Sh_K(C) \stackrel{CoDisc}{\hookrightarrow} Sh_J(C) \hookrightarrow PSh(C)
$$

which must correspond to another [[coverage]] $K$:  $Set \simeq Sh_K(C)$. Since we have this sequence of inclusions, we have an inclusion of coverages $J \subset K$. We observe that the concrete objects in $\mathcal{E}$ are precisely the $(J,K)$-[[biseparated presheaves]] on $C$. The claim then follows by standard facts of quasitoposes of biseparated presheaves.

=--

+-- {: .num_prop}
###### Proposition

Precisely if the cohesive topos $\mathcal{E}$ satisfies the axiom _[[discrete objects]] are [[concrete object|concrete]]_ (saying that for all $S \in Set$ the canonical morphism $Disc S \to coDisc \Gamma Disc S \simeq coDisc S$ is a [[monomorphism]]) then $Conc(\mathcal{E})$ is a **cohesive quasitopos** in that we have a quadrupled of [[adjoint functor]]s.

$$
   Conc(\mathcal{E})
    \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{coDisc}{\leftarrow}}}}
  Set
  \,.
$$

=--

+-- {: .proof}
###### Proof

The axiom says precisely that the functor $Disc : Set \to \mathcal{E}$ factors through $Conc(\mathcal{E})$. Also $coDisc : Set \to \mathcal{E}$ clearly factors through $Conc(\mathcal{E})$. Since $Conc(\mathcal{E})$ is a [[full subcategory]] therefore the restriction of $\Gamma$ and $\Pi$ to  $Conc(\mathcal{E})$ yields a quadruple of adjunctions as indicated.


Since by reflectivity [[limit]]s in $Conc(\mathcal{E})$ may be computed in $\mathcal{E}$, $\Pi$ preserves finite products on $Conc(\mathcal{E})$.



=--

### Objects with one point per cohesive piece
 {#ObjectsWithOnePointPerCohesivePiece}

+-- {: .num_theorem}
###### Theorem


Let $(\Pi \dashv Disc \dashv \Gamma \dashv Codisc) :  \mathcal{E} \to \mathcal{S}$ be a cohesive topos with $\Gamma X \to \Pi X$ an [[epimorphism]] for all $X$.

Let $s^* : \mathcal{L} \hookrightarrow \mathcal{E}$ be the [[full subcategory]] on those objects $X$ for which $\Gamma X \to \Pi X$ is an [[isomorphism]]. Then

1. $\mathcal{L}$ is a [[reflective subcategory]] and a [[coreflective subcategory]]

   $$
     (s_! \dashv s^* \dashv s_*)
     : 
     \mathcal{E}
       \stackrel{\overset{s_!}{\to}}{\stackrel{\overset{s^*}{\leftarrow}}{\underset{s_*}{\to}}}
     \mathcal{L} 
   $$

1. $s_*$ preserves [[coproduct]]s.

1. the components of the reflector $X \to s_! s^* X$ are [[epimorphism]]s.

=--

This is [theorem 2](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf#page=5) in ([Lawvere](#Lawvere)).

+-- {: .proof}
###### Proof

Since $\Gamma$ is a [[left adjoint]] it preserves [[colimit]]s, as does of course $\Pi$. Therefore the collection of objects for which $\Gamma X \to \Pi X$ is an isomorphism is closed under colimits and hence $\mathcal{L}$ has all colimits and the inclusion $s^* : \mathcal{L} \hookrightarrow \mathcal{E}$ obviously preserves them. 

To apply the [[adjoint functor theorem]] to deduce that therefore $s^*$ has a right adjoint $s_*$ it is sufficient to argue that $\mathcal{L}$ is a [[locally presentable category]]. To see this, notice that $\mathcal{L} \hookrightarrow \mathcal{E}$ is the [[inverter]] of $\Gamma \to \Pi$, a certain [[2-limit]] in [[Cat]].  Since the 2-category of [[accessible categories]] and [[accessible functors]] is closed under (non-strict) [[2-limit]]s in [[Cat]], it follows that $\mathcal{L}$ is accessible. Since we already know that it is also cocomplete it follows that it must be locally presentable.

Since $\Pi$ by assumption preserves finite products and $\Gamma$ preserves all products, it follows that $L$ is also closed under finite products and in particular contains the [[terminal object]] $*$. Since $\mathcal{E}$, being a [[topos]], is an [[extensive category]], it follows that $s_*$ preserves coproducts.

(...details...)

Using that $\Gamma X \to \Pi X$ is an epi, we find that $\mathcal{L}$ is also closed under [[subobject]]s: if $Y \hookrightarrow X$ is a [[monomorphism]] then if in

$$
  \array{
     \Gamma Y &\to& \Gamma X
     \\
     \downarrow && \downarrow^{\mathrlap{\simeq}}
     \\
     \Pi Y &\to& \Pi X
  }
$$

the right vertical morphism is an iso, then so is the left vertical one.

(...details...).

It then also follows that $\mathcal{L}$ is closed under arbitrary products.

(...details...)

This implies the existence of $s_!$ and the fact that $X \to s^* s_! X$ is epi.

(...details...)

=--


### Internal modal logic
  {#Modality}

Every [[topos]] $\mathcal{E}$ comes with its [[internal logic]]. From this internal perspective, the existence of extra external functors on $\mathcal{E}$ -- such as the $\Pi_0$ and the $coDisc$ on a cohesive topos -- is manifested by the existence of extra internal logical operators. These may be understood as _modalities_ equipping the internal logic with a structure of a [[modal logic]].

For the case of [[local toposes]], of which cohesive toposes are a special case, this internal modal interpretation of the extra external functor $coDisc$ has been noticed in ([AwodeyBirkedal, section 4.2](#AwodeyBirkedal)). (Beware that in that reference the symbols "$\flat$" and "#" are used precisely oppositely to their use here).

+-- {: .num_defn #DiscreteModality}
###### Definition


For $\phi \hookrightarrow A$ a [[monomorphism]] in a cohesive topos, hence a [[proposition]] of [[type]] $A$ in the [[internal logic]], we say that it is  _discretely true_ if the [[pullback]]  $# \phi|_A \to A$ in

$$
  \array{
    #\phi |_A &\to& # \phi
    \\  
    \downarrow && \downarrow
    \\
    A &\to& # A
  }
$$

is an [[isomorphism]], where $A \to # A$ is the $(\Gamma\dashv coDisc)$-[[unit of an adjunction|unit]] on $A$.

=--

+-- {: .num_remark }
###### Remark

If a proposition $\phi$ is true over all discrete objects, then it is discretely true. More precisely,
if for $X = \mathbf{\flat} X$ any discrete object we have that 

$$
  \mathcal{E}(X, \phi)
  \to 
  \mathcal{E}(X, A)
$$

is an isomorphism, then $\phi$ is discretely true.

Because if so, then 

$$
  \mathcal{E}(\flat X , \phi)
  \to
  \mathcal{E}(\flat X , A)  
$$

is an isomorphism and hence 

$$
  \mathcal{E}(\Gamma X , \Gamma \phi)
  \to
  \mathcal{E}(\Gamma X , \Gamma A)  
$$

is for all $X$. Therefore in this case $\Gamma \phi \to \Gamma A$ is an isomorphism and hence so is $# \phi \to # A$.

=--

+-- {: .num_example }
###### Example

For $\mathcal{E} = Sh(CartSp)$ the [[sheaf topos]] over [[CartSp]]${}_{smooth}$ ([[smooth infinity-groupoid|smooth spaces]]) and $\Omega^n_{cl}(-) \hookrightarrow \Omega^n(-)$ the inclusion of all closed $n$-[[differential forms]] into all $n$-forms, the proposition is "the $n$-form $\omega$ is closed". This is of course not true generally, but it is discretely true: over a [[discrete space]] every form is closed.

=--

## Examples

### Over a discrete site

We discuss some cohesive toposes over [[sites]] $C$ with trivial [[coverage]]/[[Grothendieck topology|topology]], so that the [[category of sheaves]] is the [[category of presheaves]]

$$
  Sh(C) \simeq PSh(C)
  \,.
$$

#### Families of sets -- the Sierpinksi topos
  {#FamiliesOfSets}

We discuss an example of a cohesive topos over a [[cohesive site]] that is about the simplest non-trivial example that there is: the [[Sierpinski topos]]. Simple as it is, it does serve to already illustrate some key points. The following site is in fact also an [[∞-cohesive site]] and hence there is a corresponding example of a [[cohesive (∞,1)-topos]].

Consider the site given by the [[interval category]] 

$$
  C = \{\emptyset \to *\}
$$

equipped with trivial [[Grothendieck topology|topology]]. This evidently has an [[initial object]] $\emptyset$ (which makes it [[cosifted category|cosifted]]) and a [[terminal object]] $*$.

The [[category of sheaves]] = [[category of presheaves|presheaves]] on this is the [[arrow category]] 

$$
  Sh(\{\emptyset \to *\})
  \simeq
   PSh(\{\emptyset \to *\})
  \simeq
  Arr(Set)
$$

since a presheaf $X$ on $C$ is given by a morphism

$$
  X : (\emptyset \to *) \mapsto (I \leftarrow S)
$$

in [[Set]]. We find

* $\Gamma : (I \leftarrow S) \mapsto S$

* $\Pi_0 : (I \leftarrow S) \mapsto I$.

Trivial as this is, it does provide some insight into the interpretation of cohesiveness: by decomposing $S$ into its [[fiber]]s, an object $(I \leftarrow S)$ is an $I$-indexed family of sets: $S = \coprod_i S_i$. The "cohesive pieces" are the $S_i$ and there are $|I|$-many of them. This is what $\Pi_0$ computes, which clearly preserves products.

Moreover we find for $K \in Set$:

* $Disc : K \mapsto (K \stackrel{Id}{\leftarrow} K)$;

* $CoDisc : K \mapsto (* \stackrel{}{\leftarrow} K)$

(and evidently both these functors are full and faithful).

This matches the interpretation we just found: $Disc K$ is the collection of elements of $K$ with no two of them lumped together by cohesion, while $Codisc K$ is all elements of $K$ lumped together.

The canonical morphism 

$$
  \Gamma (I \leftarrow S) \to \Pi_0 (I \leftarrow S)
$$

is

$$
  \Gamma Disc \Gamma (I \leftarrow S) \to \Gamma (I \leftarrow S) \to \Gamma Disc \Pi_0 (I \leftarrow S)
  \,.
$$

Plugging in the above this is just

$$
  S \to I
$$

itself. Indeed, by the above interpretation, this sends each point to its cohesive component. It is not an epimorphism in general, because the fiber $S_i$ over an element $i$ may be empty: the cohesive component $i$ may have no points.


#### Over a site with initial and terminal object

The [above](#FamiliesOfSets) example is the simplest special case of a more general but still very simple class of examples. 

First notice that for $C$ any [[small category]], we have the left and right [[Kan extension]] of presehaves $F : C^{op} \to Set$ along the [[functor]] $C^{op} \to *$. By definition, this are the [[colimit]] and [[limit]] functors

$$
  (\lim_\to \dashv Const \dashv \lim_\leftarrow) :
  PSh(C) \stackrel{\overset{\lim_{\to}}{\to}}{\stackrel{\overset{Const}{\leftarrow}}{\underset{\lim_\leftarrow}{\to}}}
  Set
  \,.
$$

+-- {: .num_lemma}
###### Observation

If $C$ has a [[terminal object]] $*$ then 

* the colimit is given by evaluation on this object;

* there is a further [[right adjoint]] $(\lim_\leftarrow \dashv CoConst)$

  given by

  $$
    CoConst : S \mapsto (c \mapsto Set(C(*,c), S)
    \,.
  $$

=--

+-- {: .proof}
###### Proof

The terminal object of $C$ is the [[initial object]] of the [[opposite category]] $C^{op}$ and therefore the limit over any functor $F : C^{op} \to Set$ is given by evaluation on this object

$$
  \lim_\leftarrow (C^{op} \stackrel{F}{\to} Set) \simeq F(*)
  \,.
$$

To see that we have a pair of [[adjoint functor]]s $(\lim_\to \dashv CoConst)$
we check the natural [[hom-set]] equivalence 
$PSh_C(F, CoConst S ) \simeq Set(\lim_\to F , S)$ by computing

$$
  \begin{aligned}
    PSh_C(F , CoConst S) 
     & \simeq 
      \int_{c \in C} Set(F(c), Set(C(*,c), S))
    \\
    & \simeq
        \int_{c \in C} Set(F(c) \times C(*,c), S)
    \\
     & \simeq 
         Set( \int^{c \in C} F(c) \times C(*,c) , \; S)
    \\
     & \simeq Set(F(*), S)
  \end{aligned}
  \,,
$$

Here the first step is the expression of [[natural transformation]]s by [[end]]-calculus, the second uses the fact that [[Set]] is a [[cartesian closed category]], the third uses that any [[hom-functor]] sends [[coend]]s in the first argument to ends, and the last one uses the [[co-Yoneda lemma]].

=--

The formal dual of this statement is the following.

+-- {: .num_lemma}
###### Corollary

If $C$ has an [[initial object]] $\emptyset$ then 

* the limit is given by evaluation on this object;

* there is a further [[left adjoint]] $(L \dashv \lim_\to)$,

  so that $\lim_\to$ preserves all small limits and in particular
  all finite products.

=--

In summary we have

+-- {: .num_lemma}
###### Proposition

If $C$ has both an [[initial object]] $\emptyset$ as well as a [[terminal object]] $*$ then there is a quadruple of adjoint functors

$$
  (\Pi_0 \dashv Disc \dashv \Gamma \dashv CoDisc)
   :
   PSh(C) \to Set
  \,,
$$

where

* $\Gamma$ is given by evaluation on $*$;

* $\Pi_0$ is given by evaluation of $\emptyset$ and preserves products.

=--

The above interpretation of the cohesiveness encoded by $C = \{\emptyset \to *\}$ still applies to the general case: a general object $X \in PSh(C)$ is, by restriction to the unique morphism $\emptyset \to *$ in $C$ a set-indexed  family of sets

$$
  X(\emptyset \to *) = (\Pi_0(X) = X(\emptyset) \leftarrow  X(*) = \Gamma(X))
$$

and $\Gamma$ picks out the total set of points, while $\Pi_0$ picks of the indexing set ("of cohesive components"). The extra information for general $C$ with initial and terminal object is that for every object $c \in C$ these cohesive lumps of points are refined to a hierarchy of lumps and lumps-of-lumps

$$
  X(\emptyset \to c \to *) = (\Pi_0(X) \leftarrow X(c) \leftarrow \Gamma(X))
  \,.
$$ 



#### Reflexive directed graphs {#Graphs}

+-- {: .num_prop}
###### Proposition

The category $RDGraph$ of reflexive [[directed graphs]] is a cohesive topos. 

The category $DGraph$ of just directed graphs, not necessarily reflexive, is _not_ a cohesive topos.

=--

This example was considered in ([Lawvere, Categories of spaces](#LawvereCatsOfSpaces)) as a simple test case for two very similar toposes, one of which is cohesive, the other not. 

We spell out some details on the cohesive topos of reflexive directed graphs.

+-- {: .num_defn}
###### Definition

Let $\mathbf{B}End(\Delta[1])$ be the one-object category coming from the [[monoid]] with three [[idempotent]] elements $\{Id, \sigma, \tau\}$

* $\sigma \circ  \sigma = \sigma$

* $\tau \circ  \tau = \tau$

* $ \tau \circ \sigma = \tau$

* $ \sigma \circ \tau = \sigma$

=--

A prehseaf $X : C^{op} \to Set$ on this is a _reflexive [[directed graph]]_ : the set $X(\bullet)$ is the set of all edges and vertices regarded as identity edges, the projection

$$
  s := X(\sigma) : X \to X
$$

sends each edge to its source and the projection

$$
  t := X(\tau) : X \to X
$$

sends each edge to its target. The identities

$$
  s \circ t = t
$$

and

$$
  t \circ s = s
$$

express the fact that source and target are identity edges. 

Equivalently, this is a presheaf on the full [[subcategory]] $\Delta_{\leq [1]} \subset \Delta$ of the [[simplex category]] on the objects $[0]$ and $[1]$

$$
  \Delta_{\leq [1]} = ([1] \stackrel{\overset{\tau}{\leftarrow}}{\stackrel{\to}{\underset{\sigma}{\leftarrow}}} [0])
  \,.
$$

In fact this is the [[Cauchy completion]] of $\mathbf{B}End(\Delta[1])$, obtained by [[split idempotent|splitting the idempotents]].

In summary this shows that

+-- {: .num_prop}
###### Observation

We have an [[equivalence of categories]]

$$
  RDGraph \simeq PSh(\mathbf{B} End(\Delta[1])) \simeq PSh(\Delta_{\leq [1]})
  \,.
$$

=--

To see that this presheaf topos is cohesive, notice that the terminal geometric morphism

$$
  (Disc \dashv \Gamma) : Psh(C) \to Set
$$

$Disc S$ is the reflexive directed graph with set of vertices $S$ and no non-identity morphisms and $\Gamma X$ is the set of vertices = identity edges.

The extra left adjoint $\Pi_0 : PSh(C) \to Set$ sends a graph to its set of connected components, the [[coequalizer]] of the source and target maps

$$
  X_1 \stackrel{\overset{t}{\to}}{\underset{s}{\to}} X_0 \to \Pi_0 X
  \,.
$$

Since this is a [[reflexive coequalizer]] (by the existence of the unit map $X([1] \to [0])$) it does preserve products (as discussed there). This is the property that fails for the topos $DGraph$ of all directed graphs: a general coequalizer does not preserve products.

And $CoDisc : Set \to PSh(C)$ sends a set $S$ to the reflexive graph with vertices $S$ and one edge for every ordered pair of vertices (the [[indiscrete category|indiscrete]] or _chaotic_ graph).

The canonical morphism $\Gamma X \to \Pi_0 X$ sends each vertex to its connected component. Evidently this is epi, hence in $RDGraphs$ _cohesive pieces have points_ .

#### Simplicial sets {#SimplicialSets}

Reflexive directed graphs are equivalently [[simplicial skeleton|skeleta]] of 
[[simplicial set]]s.

+-- {: .num_prop}
###### Proposition

The category [[sSet]] of simplicial sets is a cohesive topos in which _cohesive pieces have points_ . 

=--

Let $C = \Delta$ be the [[simplex category]], regarded as a [[site]] with the trivial [[coverage]].

The corresponding [[sheaf topos]] $Sh(\Delta)$ is the [[presheaf topos]] $E = PSh(\Delta) = $ [[sSet]] of [[simplicial set]]s. 

We have for $X \in sSet$

* $\Gamma : X \mapsto X_0$;

* $\Pi_0 : X \mapsto \pi_0(X) = X_0/X_1$, the set of [[simplicial homotopy group|connected components]].

And for $S \in Set$:

* $Disc S$ the constant simplicial set on $S$;

* $Codisc S$ the simplicial set which in degree $k$ has the set of $(k+1)$-tuples of elements of $S$.


If $X, Y \in sSet$ are [[Kan complex]]es, then $\Pi_0(Y^X)$ is the set of [[simplicial homotopy]]-classes of maps $X \to Y$. We can therefore write the [[homotopy category]] of Kan complexes as

$$
  Ho_{KanCplx}(X,Y) = \Pi_0(Y^X)
  \,.
$$


### Over a cohesive site

A class of examples is obtained from toposes over a [[cohesive site]]:

+-- {: .num_theorem}
###### Theorem

Let $C$ be a [[cohesive site]]. The [[sheaf topos]] $Sh(C)$ is cohesive.

=--

See [[cohesive site]] for examples.

#### Diffeological spaces

+-- {: .num_prop}
###### Proposition

The site [[CartSp]] with the standard [[open cover]] [[coverage]] is a [[cohesive site]] and even an [[(∞,1)-cohesive site]]. 

=--

+-- {: .num_prop}
###### Proposition

The quasitopos $Conc(Sh(CartSp))$ of [concrete objects](#ConcreteObjects)
in the cohesive topos over $CartSp$ is the category of [[diffeological space]]s.

=--

+-- {: .proof}
###### Proof

A sheaf $X$ on $CartSp$ is a [[separated presheaf]] with respect to the further localization given by $CoDisc$ precisely if the canonical morphism (the [[unit of an adjunction|unit]] of $(\Gamma \dashv CoDisc)$)

$$
  X \to CoDisc \Gamma X
$$

is a [[monomorphism]]. Monomorphisms of sheaves are tested objectwise, so that this is equivalent to 

$$
  Hom(U,X) \simeq X(U) \to Hom(U,CoDisc \Gamma X)
$$

being a monomorphism for all $U \in C$ (where in the first step we used the [[Yoneda lemma]]). By the adjunction relation this is equivalently

$$
  X(U) \to Set(\Gamma(U), \Gamma(X))
  \,.
$$

This being a monomorphism is precisely the condition on $X$ being a [[concrete sheaf]] on $CartSp$ that singles out diffeological spaces among all sheaves on $CartSp$.

=--


#### Smooth toposes

+-- {: .num_prop}
###### Proposition

The site [[ThCartSp]] with the standard [[open cover]] [[coverage]] is a [[cohesive site]] and even an [[(∞,1)-cohesive site]]. 

=--


The corresponding cohesive topos is the [[Cahiers topos]] $ \simeq Sh(ThCartSp)$. This is a [[smooth topos]] that models the axioms of 
[[synthetic differential geometry]].



### Cohesive over-toposes

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a cohesive topos and $X \in \mathcal{E}$ an object. 

A necessary conditions that the [[over topos]] $\mathcal{E}/X$ is a [[connected topos]] is that

1. $X$ is contractible $\Pi_0(X) \simeq *$;

Sufficient condition for $\mathcal{E}/X$ to be a [[local topos]] is that

1. $X$ is a [[tiny object]].


=--

### Infinitesimal thickening and formal smoothness

See the section <a href="http://nlab.mathforge.org/nlab/show/Q-category#FormalSmoothness">Formal smoothness</a> at [[Q-category]].

### Counter-examples {#CounterExamples}

+-- {: .num_example}
###### Counter-Example

Let $G$ be a non-trivial [[finite group]] of [[cardinality]] $n$. Write $\mathbf{B}G = \{\bullet \stackrel{g}{\to} \bullet | g \in G\}$ for its [[delooping]] [[groupoid]]. The [[presheaf topos]]

$$
  PSh(\mathbf{B}G) \simeq G Set
$$

is the category of [[permutation representation]]s of $G$. It comes with a triple of adjoint functors

$$
  (\Pi_0 \dashv Const \dashv \lim_\leftarrow) : G Set 
    \stackrel{\overset{\lim_\to}{\to}}{\stackrel{\overset{Const}{\leftarrow}}{\underset{\lim_\leftarrow}{\to}}}
   Set
  \,.
$$


The colimit over a representation $(V, \rho) : \mathbf{B}G \to Set$ is [[quotient]] set $V/\rho(G)$. So we have

$$
  \Pi_0(G) \simeq *
$$

but

$$
  \Pi_0(G \times G) \simeq \bar n
  \,,
$$

where $G$ denotes the fundamental representation of $G$ on itself. Therefore $\Pi_0$ does not preserve products in this case.

=--



## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

  * [[connected topos]] / [[∞-connected (∞,1)-topos]]

  * [[strongly connected topos]] / [[strongly ∞-connected (∞,1)-topos]]

  * [[totally connected topos]] / [[totally ∞-connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* **cohesive topos** / [[cohesive (∞,1)-topos]]

and

* [[locally connected site]], [[locally ∞-connected site]]

* [[connected site]]

* [[local site]]

* [[cohesive site]]



## References
 {#References}

The axioms for a cohesive topos originate in

* [[Bill Lawvere]], _Categories of spaces may not be generalized spaces, as exemplified by directed graphs_ , preprint, State University of New York at Buffalo, (1986) Reprints in Theory and Applications of Categories, No. 9, 2005, pp. 1&#8211;7 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.144.6357&rep=rep1&type=pdf))
{#LawvereCatsOfSpaces}

where however the term "cohesive topos" was not yet used. 

This appears maybe first in

* [[Bill Lawvere]] _Cohesive toposes and Cantor's "lauter Einsen"_ Philosophia Mathematica (3) Vol. 2 (1994), pp. 5-15. ([[LawvereCohesiveToposes.pdf:file]])

Under the name _categories of cohesion_ a formal axiomatization is given in

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))
 {#LawvereAxiomatic}

(This does demand the conditions that "cohesive piece have points" and "pieces of powers are powers of pieces" as part of the definition of "category of cohesion".)

This builds on a series of precursors of attempts to identify axiomatics for [[gros topos]]es.

In

* [[Bill Lawvere]], _[[Some Thoughts on the Future of Category Theory]]_ [[Como]] (1990)

the term _category of Being_ is used for a notion resembling that of a cohesive topos (with an [[adjoint quadruple]] but not considering _pieces have points_ or _discrete objects are concrete_). 

In 

* [[Bill Lawvere]], _Categories of space and quantity_ in: J. Echeverria et al (eds.), _The Space of mathematics_ , de Gruyter, Berlin, New York (1992)

a proposal for a general axiomatization of [[homotopy]]/[[homology]]-like "extensive quantities" and [[cohomology]]-like "intensive quantities") as covariant and contravariant functors out of a distributive category are considered.

The left and right adjoint to the global section functor as a means to identify discrete spaces and codiscrete space is mentioned

* [[Bill Lawvere]] _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

on [page 14](http://www.tac.mta.ca/tac/reprints/articles/8/tr8.pdf#page=14).

The precise term _cohesive topos_ apparently first appeared publically in the lecture 

* [[Bill Lawvere]], _[[Cohesive Toposes -- Combinatorial and Infinitesimal Cases]]_ Como (2008)

(with first remarks on [[cohesive topos|cohesion]])

The notion of "cohesion" was explored earlier in

* [[Bill Lawvere]] _Volterra's functionals and covariant cohesion of space_ Perugia Studies in Mathematics (Proceedings of the May 1997 Meeting in Perugia) ([pdf](http://www.acsu.buffalo.edu/~wlawvere/Volterra.pdf))

where (on p. 9) it is suggested that "almost any" [[extensive category]]  may be called a "species of cohesion".

An analysis of the interdependency of the axioms on a cohesive topos is in

* [[Peter Johnstone]], _Remarks on punctual local connectedness_ ([tac](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))
{#Johnstone}

A good deal of the structure of cohesive toposes is also considered in 

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenbergSpaces}

under the name _[[Q-categories]]_ .

The [[internal logic]] of [[local toposes]] is discussed in 

* [[Steve Awodey]], [[Lars Birkedal]], _Elementary axioms for local maps of toposes_ Journal of Pure and Applied Algebra, 177(3):215-230, (2003) ([ps](http://www.itu.dk/people/birkedal/papers/elealm.ps.gz))
  {#AwodeyBirkedal}


[[!redirects cohesive topos]]
[[!redirects cohesive toposes]]
[[!redirects cohesive topoi]]

[[!redirects category of cohesion]]
[[!redirects categories of cohesion]]
