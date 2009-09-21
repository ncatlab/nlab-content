#Idea

$Q$-categories and $Q^\circ$-categories serve as generalizations of (a structure induced by) [[Grothendieck topology|Grothendieck topologies]] and cotopologies. Formally they correspond to the [[localization]]s having a left or right [[adjoint functor|adjoint]] and are motivated by similar adjoint pairs involving (co)[[sieves]].

#Motivation

The [[Yoneda embedding]] is cocontinuous but not continuous functor. Hence the Grothendieck topologies are used to define smaller image than the category of presheaves such that for that embedding some cones will be preserved. In one case the cones correspond to the Grothendieck topology but more general families of diagrams may be involved. The important properties of categories of diagrams for doing the sheaf theory can be expressed in terms of certain adjoint pairs of functors. As one application this generalization of sheaf theory can also rephrase categorically properties like formal smoothness and formal etaleness of functors, and as another puts the sheafification in a framework for which another special case is a construction of the Gabriel-type noncommutative localization. 

#Definition

An __almost quotient category__, or a __$Q$-category__ is a pair of functors
$Q: A\leftrightarrow\bar{A}: I$,
where $Q$ is fully faithful and left adjoint to $I$. In other words, $A$ is equipped with an equivalence with a [[coreflective subcategory]] of $\bar{A}$. Such an adjoint situation appears often, however the word $Q$-category is used only when the pair is used in a specific meaning useful to constructions like (generalized) sheaf theory (similarly like presheaf of objects in $D$ and contravariant functor to $D$ are synonyms, but a different word refers to a different context and intuition).

A $Q^\circ$-category is a pair of functors $Q: A\leftrightarrow\bar{A}: I$,
where $Q$ is fully faithful and right adjoint to $I$. In other words, $A$ is equipped with an equivalence with a [[reflective subcategory]] of $\bar{A}$.

Morphisms...

#Almost quotient category of cones

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


#Other examples

If $Q: A\leftrightarrow\bar{A}: I$ is a $Q$-category, then there is an induced $Q$-category $\hat{Q}: A^{Set^\circ}\leftrightarrow\hat{\bar{A}}$.

The $Q$-category of sieves 

The $Q$-subcategory of the $Q$-category of (all) sieves corresponding to the subcategory of sieves corresponding to the Grothendieck topology...

(needs explanation)

#Sheaves

...

#Sheafification versus the Gabriel localization $G_{\mathcal{F}} = H^2_{\mathcal{F}}$

#Terminology and history

$Q$-category originally standed as "almost quotient category", presumably because of its role in the theory of Gabriel localization. The sheaf formalism in terms of $Q$-categories has been introduced in the mimeographed
notes

* A. Rosenberg, _Q-categories, sheaves and localization_, (in Russian) Seminar on supermanifolds __25__, Leites ed. Stockholms Universitet 1988 (there is a recent partial English translation)

The formalism has been recently used (and shortly surveyed) in

* M. Kontsevich, A. Rosenberg, _Noncommutative spaces_, preprint MPI-2004-35 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))

and also used in the general definition of "noncommutative" stacks in

* M. Kontsevich, A. Rosenberg, _Noncommutative spaces_, preprint MPI-2004-37 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305))

The epipresheaf condition for the Q-category of nilpotent (infinitesimal) thickenings is in the Kontsevich-Rosenberg paper interpreted as [[formally smooth morphism|formal smoothness]] what is further studied in 

* T. Brzezi&#324;ski, _Notes on formal smoothness_, *in*: Modules and Comodules (series _Trends in Mathematics_). T Brzezi&#324;ski, JL Gomez Pardo, I Shestakov, PF Smith (eds), Birkh&#228;user, Basel, 2008, pp. 113-124 ([doi](http://dx.doi.org/10.1007/978-3-7643-8742-6), [arXiv:0710.5527](http://arxiv.org/abs/0710.5527))

[[!redirects Q-categories]]