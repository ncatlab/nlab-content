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
$Q_C: C\leftrightarrow I_C: LC$ is therefore a Q-category, and it is called the __Q-category of cones__. 

If $\mathcal{L}\subset Cat$ is a family of small categories, then one considers the full subcategory $L_{\mathcal{L}}C$ of cones whose domains are in $\mathcal{L}$; the rest of the construction restricts to obtain a Q-category $Q^{\mathcal{L}}_C : C\leftrightarrow L_{\mathcal{L}}C : I_C^{\mathcal{L}}$. 

The most classical case is when $\mathcal{L}$ is the (say skeletal) category $Dis$ of small discrete categories (=just identity morphisms), one obtains then the Q-category $Q^{Dis}_C: C\leftrightarrow L_{Dis}C$. 
A __semicosite__ (or semicositus pl. semicositi) is a Q-category of the form $C\leftrightarrow \bar{C}$ where $\bar{C}$ is a full subcategory of $L_{Dis}C$ and the adjoint pair is obtained by the restriction. A semicosite is a __precosite__ (=Grothendieck precotopology) if 

(i) $id_x\in Ob(\bar{C})$ whenever $x\in Ob(C)$.

(ii) $\{x\stackrel{\phi_i}\to x_i\}_{i\in I}\in Ob(\bar{C})$ and $\{x_i\stackrel{\phi_{ij}}\to x_{ij}\}_{j\in J_i}\in Ob(\bar{C})$ then $\{x\stackrel{\phi_{ij}\circ\phi_i}\to x_{ij}\}\in Ob(\bar{A})$

(iii) $\{x\to x_i\}_{i\in I}\in Ob(\bar{C})$ and $g\in C(x,y)$, then the family of pushouts $\{y\mapsto x_i\coprod_x y\}_{i\in I}$ exists and belongs to $Ob(\bar{C})$.

An example of a cosite is a cosite of closed sets of a topological space. 

#Q-categories of functors into a fixed category

If $\mathbb{A} = (Q: A\leftrightarrow\bar{A}: I)$ is a $Q$-category, and $E$ a category, then there is an induced $Q$-category of $E^{\mathbb{A}}:(E^Q: E^{A}\leftrightarrow E^{\bar{A}}):E^I$; the new adjunction has unit $E^{\eta} : Id_{E^A} \to E^Q\circ E^I = E^{IQ}$ and counit $E^\epsilon : E^I\circ E^Q = E^{QI}\to Id_{E^{\bar{A}}}$. 

Any subcategory $B\subset E^{\bar{A}}$ containing $Im(E^I)$ determines a Q-subcategory $E^A\leftrightarrow B$. 

#Other examples

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