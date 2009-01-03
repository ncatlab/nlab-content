#The Idea#

Just as we can convolve [[function|functions]] $f : M \to \mathbb{C}$ where $M$ is a [[group]], or more generally a [[monoid]], we can convolve [[functor|functors]] $f: M \to Set$ where $M$ is a [[monoidal category]].  So, for any monoidal category $M$, the [[functor category]] $Set^M$ becomes a monoidal category in its own right.  The tensor product in $Set^M$ is called **Day convolution**, named after Brian Day.

We can generalize this idea by replacing [[Set]] with a more general [[cocomplete category|cocomplete]] [[symmetric monoidal category]].

#Definition#

For $(C, \otimes)$ a [[monoidal category]] and $F, G : C^{op} \to Set$ two [[presheaf|presheaves]] on $C$, their _Day convolution product_ $F \star G$ is the presheaf given by the [[end|coend]]

$$
  F \star G
  :=
  \int^{c,d \in C}
  F(c) \times G(d) \times Hom_C(-, c \otimes d)
  \,.
$$



#Examples#

* Let $C$ be a [[discrete category]] over a set, which is hence a [[monoid]] (for instance a [[group]]) with product $\cdot$. Then 
 $F \star G : e \mapsto \oplus_{c \cdot d = e} F(c) \times F(d)$. Notice that if we regard the presheaves $F$ and $G$ here as [[vertical categorification|categorifications]] of $\mathbb{N}$-valued functions $|F|, |G| : C \to \mathbb{N}$ then this reproduces precisely the ordinary convolution product of these $\mathbb{N}$-valued functions
$|F \star G| : e \mapsto \sum_{c \cdot d = e} |F(c)| \cdot |F(d)|$.

* There is an obvious monoidal structure on the [[cubical category]]. By Day convolution this induces a monoidal structure on [[cubical set|cubical sets]]. This in turn induces a monoidal structure on [[omega-category|omega-categories]].

#Blog resources#

* Todd Trimble on Day convolution [here](http://golem.ph.utexas.edu/category/2008/01/the_concept_of_a_space_of_stat.html#c014365)

#Discussion#

_[[Eric Forgy|Eric]] says_: When I see "convolution", I think "Fourier transform". Is Day convolution somehow related to a categorified version of Fourier transforms?