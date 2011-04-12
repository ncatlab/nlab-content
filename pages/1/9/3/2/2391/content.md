
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _$Q$-category_ is nothing but a [[coreflective subcategory]] and a _$Q^\circ$-category_ is nothing but a [[reflective subcategory]]. Since both of these encode reflective [[localization]]s, following [Rosenberg](#Rosenberg) the "Q" is for _quotient_ and is to indicate that in this context one is interested in notions similar to, but different from, the standard notion of [[sheaves]]:

for $\mathbb{C} := (C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\hookrightarrow}} \bar C)$ a $Q^\circ$-category there is canonically induced a quadruple of [[adjoint functor]]s between the corresponding [[presheaf categories]]

$$
  PSh(\bar A)
   \stackrel{\overset{u_!}{\to}}{\stackrel{}{\stackrel{\overset{u^*}{\leftarrow}}{\stackrel{\overset{u_*}{\to}}{\underset{u^!}{\leftarrow}}}}}
  PSh(A) 
$$

and a presheaf $F \in PSh(A)$ is called an _$\mathbb{A}$-sheaf_ if the canonical morphism

$$
  u^* F \to u^! F
$$

is an [[isomorphism]] in $PSh(\bar A)$. More generally, there are generalizations of this condition where presheaves of sets can be replaced with presheaves with values in other categories, notably in [[abelian categories]].

In a central motivating class of examples $\bar C$ is a category of [[sieve]]s on objects in a [[small category]] $C$ that are regarded as being [[covering]] but which do not necessarily satisfy the axioms of a [[Grothendieck topology]] and not even of a [[coverage]].


## Motivation

The [[Yoneda embedding]] is continuous but not cocontinuous functor. Hence the Grothendieck topologies are used to define smaller image than the category of presheaves such that for that embedding some covering cones will stay covering cones. In one case the cones correspond to the Grothendieck topology but more general families of diagrams may be involved. The important properties of categories of diagrams for doing the sheaf theory can be expressed in terms of certain adjoint pairs of functors. As one application this generalization of sheaf theory can also rephrase categorically properties like formal smoothness and formal etaleness of functors, and as another puts the sheafification in a framework for which another special case is a construction of the Gabriel-type noncommutative localization. 

## Definition

+-- {: .num_defn #QCategory}
###### Definition

An __almost quotient category__, or a __$Q$-category__ is 

* a pair of [[adjoint functor]]s

  $$
    Q: A\leftrightarrow\bar{A}: I
    \,,
  $$

  with $Q$ the [[left adjoint]];

* such that $Q$ is [[full and faithful functor|full and faithful]] 

In other words, $A$ is equipped with an equivalence with a [[coreflective subcategory]] of $\bar{A}$. 

=--

+-- {: .num_note #QTerminology}
###### Note

Such an adjoint situation appears often, however the term _$Q$-category_ is used only when the pair is used in a specific meaning useful to constructions like (generalized) sheaf theory (similarly like presheaf of objects in $D$ and contravariant functor to $D$ are synonyms, but a different word refers to a different context and intuition).

=--


+-- {: .num_defn #QopCategory}
###### Definition

A $Q^\circ$-category is a pair of functors $Q: A\leftrightarrow\bar{A}: I$,
where $Q$ is fully faithful and right adjoint to $I$. In other words, $A$ is equipped with an equivalence with a [[reflective subcategory]] of $\bar{A}$.

=--

Morphisms...

## Examples

### Presheaves on a $Q$-category

The [[category of presheaves]] over any $Q$-category canonically inherits itself the structure of a Q-category. 

+-- {: .num_prop #PresheafQCategories}
###### Proposition

Let $\mathbb{A} = \bar A \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} A$ be a $Q$-category. 
Let $C$ be any category.

Then forming [[copresheaves]] with values in $C$ yields a Q-category of the form

$$
  [\mathbb{A},C] :
   [\bar A, C]
     \stackrel{\overset{C^R = (-)\circ R}{\leftarrow}}{\underset{C^L = (-)\circ L}{\to}}
   [A,C]
  \,.
$$


=--

+-- {: .proof}
###### Proof

The $(C^R \dashv C^L)$-[[unit of an adjunction|unit]] is the dual $C^\eta$  of the original counit $\eta$

$$
  C^{\eta} : Id_{C^A} \to C^L \circ C^R = C^{L R}
$$ 

and the counit is the dual of the original unit

$$
  C^\epsilon : C^R\circ C^L = C^{R L}\to Id_{C^{\bar{A}}}
  \,.
$$ 

Since the [[left adjoint]] being a [[full and faithful functor]] is equivalent to the unit of the [[adjunction]] being an [[isomorphism]], it follows from $L$ being full and faithful that $C^R$ is full and faithful.

=--

This appears as ([Rosenberg, 2.7](#Rosenberg)).

+-- {: .num_defn #SubcategoryOfPresheafQCategories}
###### Proposition

Any subcategory $B\subset C^{\bar{A}}$ containing $Im(C^R)$ determines a Q-subcategory $C^A\leftrightarrow B$. 

=--

### Almost quotient category of cones

Let $C$ be a category and $LC$ be the category whose objects are [[cones]] $\alpha: x\to d$ over (small) diagrams $d: D\to C$ where $D$ are variable small categories; and the morphisms from $x\stackrel{\alpha}\to d$ to $x'\stackrel{\alpha'}\to d'$ are triples of the form $(f,\rho,\bar{f})$ where $f:x\to x'$ is a morphism in $C$, $\rho : D\to D'$ is a diagram (= functor), and $\bar{f}:d\circ\rho\to d'$ is a morphism of diagrams (= natural transformation) such that 
$$\array{
x & \stackrel{f}\to & x'\\
\alpha\star\rho\downarrow && \downarrow\alpha'\\
d\circ \rho &\stackrel{\bar{f}}\to & d'
}$$
commutes and $\alpha\star \rho$ denotes the horizontal (= Godement) composition of natural transformations. 

Then one defines composition of morphisms by the formula
$$
(f_1, \rho_1,\bar{f_1})\circ(f_2, \rho_2,\bar{f_2})
\stackrel{def}{=}(f_1\circ f_2, \bar{f_1}\rho_2\circ\rho_1\f_2, \bar{f_1}\circ\bar{f_2}).
$$

There is a fully faithful functor $Q_C:C\to LC$ that to any $x\in C$ assigns the trivial cone $id_x :x\to x$ and to any morphism the corresponding morphism of trivial cones. Its right adjoint is the morphism $I_C:LC\to C$ defined by sending the cone $\alpha: x\to d$ over a diagram $d:D\to C$ its vertex $x$ and to a cone morphism $(f,\rho,\bar{f})$, the morphism of vertices $f$. Then $I_C\circ Q_C = Id_C$. The identity transformation can be thus taken as the unit of the adjunction. The counit of the adjunction $\epsilon: Q_C\circ I_C \to Id_{LC}$ is constructed as follows: to a cone $\alpha:x\to d$ assign the morphism $(1_x, const, \alpha)$ where $const: D\to C$ is the constant diagram which is the unique diagram from $D = dom(d)$ to the final category $1=\{\star\}$. One can check that these data indeed define an adjoint pair $Q_C\dashv I_C$ of functors. 
$Q_C: C\leftrightarrow I_C: LC$ is therefore a Q-category, and it is called the __Q-category of cones__. 

If $\mathcal{L}\subset Cat$ is a family of small categories, then one considers the full subcategory $L_{\mathcal{L}}C$ of cones whose domains are in $\mathcal{L}$; the rest of the construction restricts to obtain a Q-category $Q^{\mathcal{L}}_C : C\leftrightarrow L_{\mathcal{L}}C : I_C^{\mathcal{L}}$. 

The most classical case is when $\mathcal{L}$ is the (say skeletal) category $Dis$ of small discrete categories (=just identity morphisms), one obtains then the Q-category $Q^{Dis}_C: C\leftrightarrow L_{Dis}C$. 
A __semicosite__ (or semicositus pl. semicositi) is a Q-category of the form $C\leftrightarrow \bar{C}$ where $\bar{C}$ is a full subcategory of $L_{Dis}C$ and the adjoint pair is obtained by the restriction. A semicosite is a __precosite__ (=Grothendieck precotopology) if 

(i) $id_x\in Ob(\bar{C})$ whenever $x\in Ob(C)$.

(ii) $\{x\stackrel{\phi_i}\to x_i\}_{i\in I}\in Ob(\bar{C})$ and $\{x_i\stackrel{\phi_{ij}}\to x_{ij}\}_{j\in J_i}\in Ob(\bar{C})$ then $\{x\stackrel{\phi_{ij}\circ\phi_i}\to x_{ij}\}\in Ob(\bar{A})$

(iii) $\{x\to x_i\}_{i\in I}\in Ob(\bar{C})$ and $g\in C(x,y)$, then the family of pushouts $\{y\mapsto x_i\coprod_x y\}_{i\in I}$ exists and belongs to $Ob(\bar{C})$.

An example of a cosite is a cosite of closed sets of a topological space. 


### Sieves



The $Q$-category of [[sieves]].

The $Q$-subcategory of the $Q$-category of (all) sieves corresponding to the subcategory of sieves corresponding to the Grothendieck topology...

(needs explanation)

## $\mathbb{A}$-Sheaves

We discuss the notion of a _$\mathbb{A}$-sheaves_ on a Q-category $\mathbb{A}$ and various equivalent reformulations.


+-- {: .num_defn #BareSheafCondition}
###### Definition

Let $\mathbb{A} = (\bar A \stackrel{\overset{u^*}{\leftarrow}}{\underset{u_*}{\to}}A)$ be a [Q-category](#QCategory). An object $x \in A$ is called an **$\mathbb{A}$-sheaf** if the canonical morphism

$$
  \bar A(y, u^*(x)) \to A(u_*(y), x)
$$

is an [[isomorphism]].

This morphism is given by

$$
  g \mapsto \eta_x^{-1} \circ u_*(g)
$$

where $\eta_x : u_* u^*(x) \to x$ is the $x$-component of the $(u^* \dashv u_*)$-[[unit of an adjunction|counit]] (which is an [[isomorphism]] because $u^*$ is a [[full and faithful functor]]).


=--

This appears as ([Rosenberg, 3.1.1](#Rosenberg)).


The object $x$ is called an **$\mathbb{A}$-monopresheaf** is this canonical morphism is just a [[monomorphism]].

+-- {: .num_prop #SheafConditionByExtraRightAdjoint}
###### Proposition

Let $\mathbb{A}$ be a Q-category with an extra [[right adjoint]] $u^! : A \to \bar A$

$$
  \mathbb{A}
  : 
  \bar A
    \stackrel{\overset{u^*}{\leftarrow}}{\stackrel{\overset{u_*}{\to}}{\underset{u^!}{\leftarrow}}}
  A
  \,.
$$

Then an object $x \in A$ is an $\mathbb{A}$-sheaf in the sense of def. \ref{BareSheafCondition} precisely if the canonical morphism

$$
  u^*(x) \to u^!(x)
$$

is an [[isomorphism]] in $\bar A$. It is a monopresheaf precisely if this is a [[monomorphism]].

=--

This appears as ([Rosenberg, 3.1.3](#Rosenberg)).

+-- {: .proof}
###### Proof

Using the $(u_* \dashv u^!)$-[[adjunction]]-[[isomorphism]] we have that the canonical morphism from def. \ref{BareSheafCondition} is isomorphic to

$$
  \bar A(y, u^* x) \to A(u_* y, x) \stackrel{\simeq}{\to}
   \bar A(y, u^! y)
$$

for all $y \in \bar A$.

=--

+-- {: .num_note #PresheafSheafCondition}
###### Note

Let $\mathbb{A} : \bar A \stackrel{\overset{u^*}{\leftarrow}}{\underset{u_*}{\to}} A$ be a Q-category for $A$ a [[small category]], let $C$ be a category with all small [[limit]]s. Then the Q-category of presheaves from prop \ref{PresheafQCategories} has an extra right adjoint $u^!_C := Ran_{u^*}$

$$
  C^{\mathbb{A}} : 
   C^{\bar A} 
    \stackrel{\overset{f^* := C^{u_*}}{\leftarrow}}{\stackrel{\underset{f_* := C^{u^*}}{\to}}{\underset{f^! := u^!_C}{\leftarrow}}}
   C^{A}
$$

given by the right [[Kan extension]] along $u^*$, which exists by the assumption that $C$ has all small limits.

Therefore by prop. \ref{SheafConditionByExtraRightAdjoint} a presheaf $F \in C^{A}$ is a $C^{\mathbb{A}}$-sheaf, def. \ref{BareSheafCondition}, precisely if the canonical morphism

$$
  f^* F \to f^! F
$$

is an [[isomorphism]].

=--

This appears as ([Rosenberg, 3.5](#Rosenberg)).


## Sheafification versus the Gabriel localization $G_{\mathcal{F}} = H^2_{\mathcal{F}}$

(...)

## References

The term _$Q$-category_ originally was short for _almost quotient category_ , presumably because of its role in the theory of [[Gabriel localization]]. The sheaf formalism in terms of $Q$-categories has been introduced in the mimeographed notes

* [[Alexander Rosenberg]], _Q-categories, sheaves and localization_, (in Russian) Seminar on supermanifolds __25__, Leites ed. Stockholms Universitet 1988 (there is a recent partial English translation)
 {#Rosenberg}

The formalism has been recently used (and shortly surveyed) in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenbergSpaces}

and also used in the general definition of "noncommutative" stacks in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative stacks_, preprint MPI-2004-37 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305))
 {#KontsevichRosenbergStacks}


The [[epipresheaf]] condition for the Q-category of nilpotent (infinitesimal) thickenings is in the Kontsevich-Rosenberg paper interpreted as [[formally smooth morphism|formal smoothness]] what is further studied in 

* [[T. Brzeziński]], _Notes on formal smoothness_, *in*: Modules and Comodules (series _Trends in Mathematics_). T Brzezi&#324;ski, JL Gomez Pardo, I Shestakov, PF Smith (eds), Birkh&#228;user, Basel, 2008, pp. 113-124 ([doi](http://dx.doi.org/10.1007/978-3-7643-8742-6), [arXiv:0710.5527](http://arxiv.org/abs/0710.5527))
 {#Brzezinski}

[[!redirects Q-categories]]