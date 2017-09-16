#The Idea#

Just as we can convolve [[function|functions]] $f : M \to \mathbb{C}$ where $M$ is a [[group]], or more generally a [[monoid]], we can convolve [[functor|functors]] $f: M \to Set$ where $M$ is a [[monoidal category]].  So, for any monoidal category $M$, the [[functor category]] $Set^M$ becomes a monoidal category in its own right.  The tensor product in $Set^M$ is called **Day convolution**, named after [[Brian Day]].

We can generalize this idea by replacing [[Set]] with a more general [[cocomplete category|cocomplete]] [[symmetric monoidal category]] $V$. The technical condition is that the tensor product $u \otimes v$ must preserve colimits in the separate arguments $u$ and $v$; that is, that the functors $u \otimes -$ and $- \otimes v$ must preserve colimits. This occurs when for instance $V$ is symmetric monoidal closed (so that these functors are left adjoints). 

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

* There is an obvious monoidal structure on the [[cube category]]. By Day convolution this induces a monoidal structure on [[cubical set|cubical sets]]. This in turn induces a monoidal structure on [[strict omega-category|strict omega-categories]].

#Blog resources#

* Todd Trimble on Day convolution [here](http://golem.ph.utexas.edu/category/2008/01/the_concept_of_a_space_of_stat.html#c014365)

#Discussion#

_[[Eric Forgy|Eric]] says_: When I see "convolution", I think "Fourier transform". Is Day convolution somehow related to a categorified version of Fourier transforms?

_[[Todd Trimble|Todd]] says_: Yes, something like that. I talk a little about this in the article on [[operad|operads]], in the detailed theoretical section. 

The usual Fourier transform (for periodic functions) passes between Fourier coefficients $a_n$ and functions $\sum_n a_n z^n$ on $S^1$. One way of categorifying this is to pass from the category of functors $a: \mathbb{N} \to Set$ (considered as a monoidal category with respect to Day convolution) to their so-called "analytic functors" $\hat{a}: Set \to Set$, mapping a set $x$ to $\hat{a}(x) = \sum_n a_n \cdot x^n$. The "categorified Fourier transform" $a \mapsto \hat{a}$ takes Day convolution products to (pointwise) cartesian products. 

If the "Fourier transform" is properly formulated (using enriched tensor products), then the same holds for any monoidal category in place of the discrete monoidal category $\mathbb{N}$. 

_[[AnonymousCoward]] says_: The passage to analytic functors eems more like a z-transform or Laplace transform. In the particular case of species, it is the Laplace transform formula that applies to the analytic functor of a derivative of a species, not the Fourier transform one involving multiplication by the imaginary unit.
The use of hom above is reminiscent of the Dirac delta. Is there a connection?