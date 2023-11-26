
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* this block creates the table of contents, leave as is
{: toc}


## Idea
The **Para construction** is a variety of strictly related functorial constructions that produce a category of parametric morphisms.

In the simplest case, one starts with a monoidal category $\mathcal{C}$ and builds a category $\mathbf{Para}(\mathcal{C})$ whose morphisms $A \to B$ are pairs $(P,f)$ where $P:\mathcal{C}$ is a _parameter_ and $f: A \otimes P \to B$ is a morphism in $\mathcal{C}$.

Such a morphism might be visualised using the [[string diagram|graphical]] language of monoidal categories (below, left). However, this notation does not emphasise the special role played by $P$, which is part of the data of the morphism itself. Parameters and data in [[machine learning]] have different semantics; by separating them on two different axes, we obtain a graphical language which is more closely tied to these semantics (below, right).

<img src="/nlab/files/standard_vs_para.png" width="500"/>

This gives us an intuitive way to compose parameterised maps:

<img src="/nlab/files/para_comp2.gif" width="500"/>

The Para construction is of relevance in categorical cybernetics, since controlled processes such as machine learning models, economic agents and Bayesian reasoners are straightforwardly modeled as parametric processes of some kind.

Indeed, the notation $\mathbf{Para}(\mathcal{C})$ was originally introduced in ([Fong, Spivak and Tuyeras 2019](#FongSpivakTuyeras2019)), and then successively refined in ([Gavranovic 2019](#Gavranovic19)) and ([Cruttwell et al. 2021](#Cruttwell2021)) for applications to machine learning.  ([Capucci et al. 2020](#Capucci2020)) generalized the construction from monoidal categories to [[actegories]], in order to capture examples from other areas of categorical cybernetics.  A still further generalization and systematization of the Para construction is being developed by [[David Jaz Myers]] and [[Matteo Capucci]], see ([Myers 2022](#Myers22)) and ([Capucci 2023](#Capucci23)).

Nonetheless, the 1-categorical version of Para already appears e.g. in ([Hermida & Tennent 2012](#HermidaTennent2012)), with precursors in ([Pavlovic 1997](#Pavlovic1997)).
Also, [Baković  2008, Thm. 13.2](#Bakovic2008) introduces Copara (under a different name) in the very general context of actions of [[bicategories]].

## Definition

### For monoidal categories

\begin{definition}
For $(\mathcal{C}, I, \otimes)$ a [[monoidal category]], $\mathbf{Para}(\mathcal{C})$ is the [[bicategory]] given by the following data:

* Its [[objects]] are the objects of $\mathcal{C}$.

* A [[1-morphism]] $A \to B$ is a choice of a parameter object $P \colon \mathcal{C}$ and a morphism in $\mathcal{C}$ of the form

  $$
    f \colon A \otimes P \to B
    \,.
  $$

* A [[2-morphism]] $(P, f) \Rightarrow (Q, g)$ is a morphism $r \colon P \to Q$ in $\mathcal{C}$ such that the following [[commuting diagram|diagram commutes]]:

\begin{tikzcd}
  {A \otimes P} 
  \\
  {A \otimes Q} & B
  \arrow["{A \otimes r}", from=1-1, to=2-1]
  \arrow["f", from=1-1, to=2-2]
  \arrow["g"', from=2-1, to=2-2]
\end{tikzcd}

* Identity morphisms are given by the right [[unitors]]:

  $$
    (I, \rho) \colon X \otimes I 
      \xrightarrow{\rho_X} 
    X
    \,.
  $$

* The composite of a map $f \colon A \otimes P \to B$ and $g \colon B \otimes Q \to C$ is given by the animation above. In symbols, this is the $P \otimes Q$-parameterised map defined as

  $$
    A \otimes P \otimes Q 
      \xrightarrow{f \otimes Q} 
    B \otimes Q \xrightarrow{g} C
  $$

* The data of [[associators]] and [[unitors]] for the bicategory, as well as their coherence diagrams, are defined using those of $\mathcal{C}$.

\end{definition}

If $\mathbf{C}$ is strict monoidal, then $\mathbf{Para}(\mathcal{C})$ is a [[2-category]].
One can show that if $\mathbf{C}$ is [[commutative monoidal category|commutative]], then $\mathbf{Para}(\mathcal{C})$ is symmetric monoidal, since commutativity of $\otimes$ allows one to exhibit an interchange.
It is believe this still holds if $\mathbf{C}$ is just symmetric, making $\mathbf{Para}(\mathcal{C})$ a [[symmetric monoidal bicategory]].

### For actegories

\begin{definition}
Let $(\mathcal{M}, I, \otimes)$ be a [[monoidal category]] and let $(\mathcal{C}, \odot)$ be a right $\mathcal{M}$-[[actegory]]. Then $\mathbf{Para}(\odot)$ is a [[bicategory]] with the following data:

* Its 0-cells are the objects of $\mathcal{C}$.
* A 1-cell $A \to B$ is a choice of a parameter object $P : \mathcal{M}$ and a morphism
$$
f : A \odot P \to B
$$
in $\mathcal{C}$.
* A 2-cell $(P, f) \Rightarrow (Q, g)$ is a morphism $r : P \to Q$ in $\mathcal{M}$ such that the following commutes:

\begin{tikzcd}
	{A \odot P} \\
	{A \odot Q} & B
	\arrow["{A \odot r}"', from=1-1, to=2-1]
	\arrow["f", from=1-1, to=2-2]
	\arrow["g"', from=2-1, to=2-2]
\end{tikzcd}


* Identity morphisms are given by the unitors:
$$
(I, \eta) : X \odot I \xrightarrow{\eta_X} X
$$
* The composition of a map $f : A \odot P \to B$ and $g : B \odot Q \to C$ is defined as
$$
A \odot (P \otimes Q) \cong (A \odot P) \odot Q \xrightarrow{f \odot Q} B \odot Q \xrightarrow{g} C
$$
* The data of associators and unitors for the bicategory, as well as their coherence diagrams, are defined using those of $\mathcal{M}$ and $\odot$.

\end{definition}

Again, it is folklore that this bicategory is symmetric monoidal when $\odot$ is a *symmetric monoidal action*, meaning $\mathcal{C}$ is monoidal, $\mathcal{M}$ is symmetric and $\odot$ is a symmetric monoidal functor.

Also, this construction is 2-functorial from $\mathcal{M}\mathbf{Act}$ to $\mathbf{Bicat}$.

### Dual construction: copara and bipara
Given a *left* $\mathcal{M}$-actegory, one can produce a bicategory of *coparametric morphisms* $f: A \to P \odot B$ by dualizing the above construction in the obvious way.
This is known as $\mathbf{Copara}(\odot)$.

Likewise, given an $\mathcal{M}$-[[biactegory]] there is a bicategory $\mathbf{Bipara}(\odot, \odot')$ whose 1-cells are *biparametric morphisms* $f: A \odot P \to Q \odot B$, whose composition rule uses the bimodulator of the biactegory.

### Generalizations

As described in ([Myers 2022](#Myers22)), the Para construction naturally generalizes in four different ways:

{#AsADoubleCategory} **(1.)** Move from bicategories to [[double categories]] (in the weak sense): $\mathbf{Para}(\mathcal{C})$ is usefully thought of as a [[double category]] whose [[tight map|tight category]] is still $\mathcal{C}$, whose [[loose map|loose maps]] are parametric morphisms, and whose squares are reparametrizations that commute suitably:

\begin{tikzcd}[sep=20pt]
  A
  \ar[
    rr,
    "{ (P,f) }",
    "{\ }"{name=s, pos=.9, swap}
  ]
  \ar[  
    dd, "{ h }"{swap}
  ]
  &&
  B
  \ar[
    dd, "{ k }"
  ]
  &&
  A \odot P
  \ar[
    rr,
    "{ f }"
  ]
  \ar[
    dd,
    "{ h \odot r }"{swap}
  ]
  &&
  B
  \ar[  
    dd,
    "{ k }"
  ]
  \\
  &&&
  :=
  \\
  A' 
  \ar[
    rr,
    "{ (P', f') }"{swap},
    "{\ }"{name=t, pos=.1}
  ]
  &&
  B'
  \ar[
    from=s,
    to=t,
    Rightarrow,
    shorten=10pt,
    "{ r }"
  ]
  &&
  A' \odot P'
  \ar[
    rr,
    "{ f' }"{swap}
  ]
  &&
  B'
\end{tikzcd}


**(2.)** Allow for *colax actions*. This includes [[comonads]] (and [[graded monad|graded comonads]] more generally), since they are colax actions of the terminal monoidal category; and applying Para to a comonad yields a double categorical version of the [[coKleisli category]] of the comonad.

**(3.)** Allow for "dependent parameters", i.e. for situation in which the parameter $P$ of a parametric morphism $f: A \odot P \to B$ actually depends on $A$, thus allowing for $f$ of the form $f: (a:A) \times P(a) \to B$ (notation is suggestive). This makes double categories such as [[span|$\mathbf{Span}(\mathcal{C})$]] instances of the Para construction (where the left leg encodes the parameter dependency and the right leg is the parametric morphism itself).


**(4.)** Have the construction take place in [[complete category|complete]] 2-categories, as opposed to $\mathbf{Cat}$. This allows to describe Para for structured categories and to apply it to different 2-categorical structures (e.g. indexed categories).


## In categorical cybernetics

Para has been developed to model effectively the compositional structure of controlled processes, such as those involving agents. The examples better developed are in [[deep learning]] and [[game theory]], see ([Capucci et al. 2020](#Capucci2020)).

The idea that agents are parametric functions is quite old. In fact, agents take in an input $A$ and produce an output $B$. However, they have additional inputs/outputs not available to the "outside world", i.e. not part of their composition interface.
These can be the _weights_ (or _parameters_) of a neural network (or a more general ML model), the _strategies_ of a player in an economic game, the control signal of a controlled ODE or a Markov decision process.

Thus agents are naturally modelled as parametric morphisms.

## Examples

* The [[Cayley graph]] of a monoid action (together with its category structure) is a low-dimensional example of a Para construction for actegories.

* When the base category is set to be the category of [[optics (in computer science)|optics]], then $\mathbf{Para(\mathbf{Optic(\mathcal{C})})}$ recovers the category of [[neural networks]] defined in ([Capucci et al. 2020](#Capucci2020)).

* The "monoidal indeterminates" construction of [Hermida and Tennent](#HermidaTennent2012) is a Para construction for actegories. Hermida and Tennent consider a symmetric monoidal functor $j:\mathbf{\Sigma}\to \mathcal{C}$ (hence: a symmetric monoidal action of $\mathbf{\Sigma}$ on $\mathcal{C}$) and provide a symmetric monoidal bicategory $\mathcal{C}(\mathbf{x}:j)$ and ordinary monoidal category $\mathcal{C}[\mathbf{x}:j]$. 
The morphisms $X\to Y$ in $\mathcal{C}(\mathbf{x}:j)$ are pairs $(w,f)$ where $w$ is in $\mathbf{\Sigma}$ and $f:X\otimes j(w)\to Y$ in $\mathcal{C}$.

* If we quotient $\mathbf{Para}(\mathcal{C})$ to get a 1-category by equating connecting components of 1-cells, this is a [[semicartesian monoidal category|semicocartesian]] monoidal category. In fact it is the semicocartesian [[reflection]] of $\mathcal{C}$. (See ([Hermida and Tennent](#HermidaTennent2012), Corollary 2.13).) Similarly, quotienting $\mathbf{CoPara}(\mathcal{C})$
gives the semicartesian reflection of $\mathcal{C}$. 

* In particular, if we start from the category $\mathbf{FdIsometry}$ of [[finite-dimensional vector space|finite dimensional]] [[Hilbert spaces]] and [[isometry|isometries]], the 1-cells of $\mathbf{CoPara}(\mathbf{FdIsometry})$ are [[Stinespring factorization theorem|Stinespring dilations]] of [[quantum channels]], and the quotiented 1-category is equivalent to the category of [[quantum channels]] (see ([Huot and Staton 2018](#HuotStaton2018))).

## Related concepts 

* [[action of a monoidal category]]
* [[lens (in computer science)]]

## References

The Para construction first appears (though not under that name) in:

* {#HermidaTennent2012} [[Claudio Hermida]], [[Robert Tennent]]. _Monoidal indeterminates and categories of possible worlds_. Theoretical Computer Science vol 430. 2012. Preliminary version in MFPS 2009. [doi:j.tcs.2012.01.001](https://doi.org/10.1016/j.tcs.2012.01.001)

* {#Pavlovic1997} [[Duško Pavlović]], _Categorical logic of names and abstraction in action calculi_. Math. Structures Comput. Sci. 7 (6) (1997) 619–637. [pdf](https://www.kestrel.edu/people/pavlovic/papers/clna-MSCS97.pdf)

* {#Bakovic2008} [[Igor Baković ]], _Bigroupoid 2-torsors_. Dissertation, LMU München: Faculty of Mathematics, Computer Science and Statistics, ([pdf](https://edoc.ub.uni-muenchen.de/9209/1/Bakovic_Igor.pdf))

The terminology "Para construction" first appears in:

* {#FongSpivakTuyeras2019} [[Brendan Fong]], [[David Spivak]], Rémy Tuyéras, _Backprop as Functor: A compositional perspective on supervised learning_, 34th Annual ACM/IEEE Symposium on Logic in Computer Science (LICS) 2019, pp. 1-13, 2019. ([arXiv:1711.10455](https://arxiv.org/abs/1711.10455), [LICS'19](https://ieeexplore.ieee.org/abstract/document/8785665))

It has then be developed for the purposes of machine learning in:

* {#Gavranovic2019} Bruno Gavranović, _Compositional Deep Learning_, ([arXiv:1907.08292](https://arxiv.org/abs/1907.08292))

* {#Cruttwell2021} [[G.S.H. Cruttwell]], [[Bruno Gavranović]], [[Neil Ghani]], Paul Wilson, Fabio Zanasi, _Categorical Foundations of Gradient-Based Learning_, ([arXiv:2103.01931](https://arxiv.org/abs/2103.01931))

and generalized further to [[actegories]] for the purposes of categorical cybernetics in:

* {#Capucci2020} Matteo Capucci, [[Bruno Gavranović]], [[Jules Hedges]], Eigil Fjeldgren Rischel, _Towards Foundations of Categorical Cybernetics_, ([arXiv:2015.06332](https://arxiv.org/pdf/2105.06332.pdf))

The generalization of the Para construction being developed by [[David Jaz Myers]] and [[Matteo Capucci]] is expounded in the following talks:

* {#Myers22} [[David Jaz Myers]], _The Para construction as a distributive law_, talk at the Virtual Double Categories Workshop, 2022 ([slides](https://bryceclarke.github.io/virtual-double-categories-workshop/slides/david-jaz-myers.pdf), [video](https://www.youtube.com/watch?v=zB_ifewP8Yk))

* {#Capucci23} [[Matteo Capucci]], _Constructing triple categories of cybernetic processes_, ([slides](https://zenodo.org/record/8221550/files/main.pdf), [video](https://www.youtube.com/watch?v=jYxnUy1vH7Q&pp=ygUmY2FwdWNjaSBjb25zdHJ1Y3RpbmcgdHJpcGxlIGNhdGVnb3JpZXM%3D))

The view of quantum channels via CoPara is in

* {#HuotStaton2018} Mathieu Huot, Sam Staton, _Universal properties in quantum theory_ (QPL 2018) ([pdf](https://www.mathstat.dal.ca/qpl2018/papers/QPL_2018_paper_68.pdf)).


[[!redirects copara construction]]
[[!redirects bipara construction]]