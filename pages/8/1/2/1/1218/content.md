{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A **diffeological spaces** is a type of [[generalized smooth space]].  As with the other variants, it subsumes the notion of [[smooth manifold]] but also naturally captures other spaces that one would like to think of as smooth spaces but aren't manifolds; for example, the space of all smooth maps between two smooth manifolds can be made into a diffeological space. (These mapping spaces are rarely manifolds themselves, see [[manifolds of mapping spaces]].)

In a little more detail, a **diffeology**, $\mathcal{D}$ on a set $X$ is a [[presheaf]] on the category of open subsets of Euclidean spaces with smooth maps as morphisms.  To each open set $U \subseteq \mathbb{R}^n$, it assigns a subset of $\Set(U,X)$.  The functions in $\Set(U,X)$ are to be regarded as the "smooth functions" from $U$ to $X$.  A **diffeological space** is then a set together with a diffeology on it.

Diffeological spaces were originally described by J.M. Souriau in 1980. They have subsequently been developed by [[Patrick Iglesias-Zemmour]] who is writing a textbook on the subject.

## Definition

+-- {: mynumdef #DiffSp}
###### Definition
Let $\mathcal{Op}$ denote the [[site]] whose objects are the open subsets of the Euclidean spaces $\mathbb{R}^n$  and whose morphisms are [[smooth map]]s between these.

A **diffeological space** is a pair $(X,\mathcal{D})$ where 

* $X$ is a set 

* and $\mathcal{D} \in Sh(\mathcal{Op})$ is a **[[diffeology]]** on $X$:

  * a [[subobject|subsheaf]] of the sheaf $U \mapsto Hom_{Set}(U,X)$ with $\mathcal{D}(*) = X$

  * equivalently: a [[concrete sheaf]] on the [[site]] $\mathcal{Op}$ such that $\mathcal{D}(*) = X$.

A morphism of diffeological spaces is a morphism of the corresponding sheaves.

=--

For $(X,\mathcal{D})$ a diffeological space, and for any $U \in \mathcal{Op}$, the set $\mathcal{D}(U)$ is also called the set of **plots** in $X$ on $U$. This is to be thought of as the set of ways of mapping $U$ smoothly into the would-be space $X$. This assignment _defined_ what it means for a map $U \to X$ of sets to be smooth. 

For some comments on the reasoning behind this kind of definition of generalized [[space]]s see [[motivation for sheaves, cohomology and higher stacks]].

A sheaf on the site $\mathcal{Op}$ of open subsets of Euclidean spaces is completely specified by its restriction to [[CartSp]], the full subcategory of Euclidean spaces.  Therefore in the sequel we shall often restrict our attention to [[CartSp]].

One may define a "very general smooth space" to be _any_ sheaf of [[CartSp]] and identify the [[sheaf topos]] $Sh(CartSp)$ as the category of very general smooth spaces.

A diffeological space precisely a [[concrete sheaf]] on the [[concrete site]] [[CartSp]]. The [[full subcategory]]

$$
  DiffeologicalSpace \hookrightarrow Sh(CartSp)
$$

on all concrete sheaves is not a [[topos]], but is a [[quasitopos]].


The concreteness condition on the sheaf is a reiteration of the fact that a diffeological space is a subsheaf of the sheaf $U \mapsto X^{|U|}$.  In this way, one does not have to explicitly mention the underlying set $X$ as it is determined by the sheaf on the one-point open subset of $\mathbb{R}^0$.


## Examples

* Every [[smooth manifold]] $X$, i.e. every object of [[Diff]], becomes a diffeological space by defining the plots on $U \in CartSp$ to be the ordinary [[smooth function]]s from $U$ to $X$, i.e. the morphisms in [[Diff]]:

  $$  
    X : U \mapsto Hom_{Diff}(U,X)
    \,.
  $$

* For $X$ and $Y$ two diffeological spaces, their [[product]] as sets $X \times Y$ becomes a diffeological space whose plots are pairs consisting of a plot into $X$ and one into $Y$

  $$
    X \times Y : U \mapsto Hom_{DiffSp}(U,X) \times Hom_{DiffSp}(U,Y)
    \,.
  $$

* Given any two diffeological spaces $X$ and $Y$, the set of 
  morphisms $Hom_{DiffSp}(X,Y)$ becomes a smooth space by taking 
  the plots on some $U$ to be the smooth morphisms $X \times U \to Y$, 
  i.e. the smooth $U$-parameterized families of smooth maps from $X$ to $Y$:

  $$
    [X,Y] : U \mapsto Hom_{DiffSp}(X \times U, Y)
    \,.
  $$

  In this formula we regard $U \in CartSp \hookrightarrow Diff$ 
  as a diffeologiical space according to the above example. 
  In fact, we apply secretly here the [[Yoneda embedding]] 
  and use the general formula for the 
  cartesian [[closed monoidal structure on presheaves]].

## Properties

The category $DiffSp \coloneqq ConSh(Cart)$ of diffeological spaces is a [[quasitopos]]. This means in particular that it is 

* [[cartesian closed category]] [[closed monoidal category]].


### Connectedness {#Connectedness}

The full [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]] in that the terminal [[global section]] [[geometric morphism]] to [[Set]] is an [[essential geometric morphism]]:

$$
  Sh(CartSp)
  \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{L Const}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
$$

The extra [[left adjoint]] $\Pi_0 : Sh(CartSp) \to Set$ sends diffeological spaces to the set of path-[[connected]] components of their underlying [[topological space]]s.


+-- {: .un_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is a [[locally connected topos]].

=--

+-- {: .proof}
###### Proof

The following argument works for every [[site]] $C$ which is such that constant presheaves on $C$ are already sheaves.

Notice that this is the case for $C = CartSp$ because every Cartesian space is connected: for $S \in Set$ a compatible family of elements of $Const S$ on a cover $\{U_i \to \mathbb{R}^n\}$ of some $\mathbb{R}^n$ is an element of $S$ on each patch, such that their restriction maps to intersections of patches coincide. But the restriction maps are all identities, so this says that all these elements coincide. Therefore the set of compatible families is just the set $S$ itself, hence the presheaf $Const S$ is a sheaf.

So with $L : PSh(C) \to Sh(C)$ the [[sheafification]] functor we have that $L Const S \simeq Const S$.

Whenever this is the case the [[left adjoint]] to the constant presheaf functor, which always exists for presheaves and is given by the [[colimit]] functor, is also left adjoint on the level of sheaves, because for each $X \in Sh(C)$ and $S \in Set$ we have natural bijections

$$
  \begin{aligned}
    Hom_{Sh(C)}(X, L Const S)
    & =
    Hom_{PSh(C)}(X, L Const S)
    \\
    & \simeq
    Hom_{PSh(C)}(X, Const S)
    \\
    & \simeq
    Hom_{Set}(\lim_\to X, S)
  \end{aligned}
  \,.
$$

=--

+-- {: .un_def}
###### Definition

Write $\Pi_0 := \lim_\to : Sh(CartSp) \to Set$
for the [[left adjoint]] to $LConst : Set \stackrel{Const}{\to} PSh(C) \stackrel{L}{\to} Sh(C)$.

=--

+-- {: .un_prop}
###### Proposition

For $X \in Sh(C)$ a diffeological space, $\Pi_0(X)$ is the set of path-connected components of the topological space underlying $X$.

=--

+-- {: .proof}
###### Proof

By the [[co-Yoneda lemma]] we may write 

$$
  X = {\lim_\to}_{(U \to X) \in y/X} U
$$

and since $\Pi_0$ commutes with colimits we have

$$
  \Pi_0(X) \simeq 
  \Pi_0 {\lim_\to}_{(U \to X)} U
  \simeq
  {\lim_\to}_{(U \to X)} \Pi_0(U)
  \,.
$$

But also by the co-Yoneda lemma we have that the [[colimit]] over any [[representable functor|representable]] is the singleton set, hence our expression

$$
  \cdots \simeq 
  {\lim_\to}_{(U \to X)} *
$$

is the colimit over the category of plots of $X$ of the functor that is constant on the point. This colimit is the [[coproduct]] of points over the connected components of the [[diagram]] category.

The connected components of the category of plots $y/X$ are the path-connected (or "plot-connected") components of the underlying topological space of $X$.



=--


+-- {: .un_prop}
###### Proposition

The [[sheaf topos]] $Sh(CartSp)$ on [[CartSp]] is actually a [[connected topos]].

=--

+-- {: .proof}
###### Proof

Since $CartSp$ is a [[connected category]] it is immediate that $Const \colon Set \to PSh(CartSp)$ is a [[full and faithful functor]]. By the above this equals $L Const$, which is hence also full and faithful.

By the discussion at [[connected topos]] we could equivalently convince ourselves that $\Pi_0$ preserves the terminal object. The terminal object of $Sh(CartSp)$ is $y(\mathbb{R}^0)$, hence representable. By the above, $\Pi_0$ sends all representable objects to the singleton set, which is the terminal object of $Set$. 

=--

## References 

For a discussion on how diffeological spaces relate to the other notions of [[generalised smooth space]], see:

* [[Andrew Stacey]], _Comparative Smootheology_ ([arXiv:0802.2225](http://arxiv.org/abs/0802.2225))

A textbook on diffeological spaces is

* [[Patrick Iglesias-Zemmour]],
_Diffeology_
([web](http://math.huji.ac.il/~piz/Site/The%20Book/The%20Book.html), [pdf](http://math.huji.ac.il/~piz/documents/Diffeology.pdf))

The thesis

* [[Patrick Iglesias-Zemmour]], _Fibrations diff&#233;ologie et Homotopie_,  PhD thesis [pdf](http://math.huji.ac.il/~piz/documents/TheseEtatPI.pdf)

contains some useful material that hasn't yet made it into the book. The article 

* [[John Baez]], [[Alexander Hoffnung]], _Convenient Categories of Smooth Spaces_ ([arXiv](http://arxiv.org/abs/0807.1704))

amplifies the point that diffeological spaces are [[concrete sheaves]] on the category of (subsets of) [[cartesian space]]s.

See also the original article wherein diffeological spaces were introduced:

* [Groupes diff\'erentiels](http://www.ams.org/mathscinet-getitem?mr=607688)



[[!redirects diffeological spaces]]
