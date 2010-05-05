{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of **diffeological spaces** -- or **Chen smooth spaces** -- is a notion of [[generalized smooth space]] that subsumes the notion of [[smooth manifold]] but also for instance naturally captures the space of all smooth maps between two smooth manifolds as a smooh space. (Whereas these mapping spaces are rarely manifolds themselves, see [[manifolds of mapping spaces]].)

A diffeological space $(X,\mathcal{D})$ is a [[set]] $X$, together with a rule $\mathcal{D}$ that determines which maps of sets $\mathbb{R}^n \to X$ from a [[Cartesian space]] in $X$ count as smooth.

Diffeological spaces were originally described by J.M. Souriau in 1980. They were also studied intensively by Chen in his work on differential forms on mapping spaces. They have subsequently been developed by [[Patrick Iglesias-Zemmour]] who is writing a textbook on the subject.

## Definition

+-- {: mynumdef #DiffSp}
###### Definition
Let [[CartSp]] denote the [[site]] whose objects are the [[smooth manifold]]s $\mathbb{R}^n$  and whose morphisms are [[smooth map]]s between these.

A **diffeological space** is a pair $(X,\mathcal{D})$ where 

* $X$ is a set 

* and $\mathcal{D} \in Sh(CartSp)$ is a **[[diffeology]]** on $X$:

  * a [[subobject|subsheaf]] of the sheaf $U \mapsto Hom_{Set}(U,X)$ with $\mathcal{D}(*) = X$

  * equivalently: a [[concrete sheaf]] on the [[site]] [[CartSp]] such that $\mathcal{D}(*) = X$.

A morphism of diffeological spaces is a morphism of the corresponding sheaves.

=--

For $(X,\mathcal{D})$ a diffeological space, and for any $U \in CartSp$, the set $\mathcal{D}(U)$ is also called the set of **plots** in $X$ on $U$. This is to be thought of as the set of ways of mapping $U$ smoothly into the would-be space $X$. This assignment _defined_ what it means for a map $U \to X$ of sets to be smooth. 

For some comments on the reasoning behind this kind of definition of generalized [[space]]s see [[motivation for sheaves, cohomology and higher stacks]].

One may define a "very general smooth space" to be _any_ sheaf of [[CartSp]] and identify the [[sheaf topos]] $Sh(CartSp)$ as the category of very general smooth spaces.

A diffeological space precisely a [[concrete sheaf]] on the [[concrete site]] [[CartSp]]. The [[full subcategory]]

$$
  DiffeologicalSpace \hookrightarrow Sh(CartSp)
$$

on all concrete sheaves is not a [[topos]], but still a [[quasitopos]].


The concreteness condition on the sheaf is a reiteration of the fact that a diffeological space is a subsheaf of the sheaf $U \mapsto X^{|U|}$.  In this way, one does not have to explicitly mention the underlying set $X$ as it is determined by the sheaf on the one-point open subset of $\mathbb{R}^0$.


## Examples

* Every [[smooth manifold]] $X$, i.e. every object of [[Diff]] becomes a diffeological space by defining the plots on $U \in CartSp$ to be the ordinary [[smooth function]]s from $U$ to $X$, i.e. the morphisms in [[Diff]]:

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

The category $DiffSp := ConSh(Cart)$ of diffeological spaces is a [[quasitopos]]. This means in particular that it is 

* [[cartesian closed category]] [[closed monoidal category]].



## References 

The original articles by Chen can and other related references can be found referenced in 

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

See also

* [Groupes diff\'erentiels](http://www.ams.org/mathscinet-getitem?mr=607688)



[[!redirects diffeological spaces]]

[[!redirects Chen space]]
[[!redirects Chen spaces]]
[[!redirects Chen smooth space]]
[[!redirects Chen smooth spaces]]