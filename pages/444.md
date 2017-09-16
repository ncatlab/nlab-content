#Definition#

Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] $G$, the [[simplex category]] $\Delta$, the [[cube category]] $\Box$, the [[cycle category]] $\Lambda$ of Connes, or certain category $\Omega$ related to trees whose corresponding presheaves are [[dendroidal set]]s.

If $C$ is any [[locally small category|locally small]] category or, more generally, a $V$-[[enriched category]] equipped with a [[functor]]
$$
  i : S \to C
$$
we obtain a functor
$$
  N : C \to V^{S^{op}}
$$
from $C$ to [[globular set]]s or [[simplicial set]]s or [[cubical set]]s, respectively, (or the corresponding $V$-objects) given on an [[object]] $c \in C$ by
$$
  N_i(c) : S^{op} \stackrel{i}\to C^{op} 
    \stackrel{C(-,c)}{\to}
    V
  \,.
$$

This $N_i(c)$ is the **nerve** of $c$ with respect to the chosen $i : S \to V$.

Typically, one wants that $i$ is [[dense functor]], i.e. that every object $c$ of $C$ is canonically a colimit of a diagram of objects in $M$, more precisely,
$$
\mathrm{colim}((i/c)\stackrel{\mathrm{pr}_S}{\longrightarrow} S \stackrel{i}{\to} C) = c,
$$
which is equivalent to the requirement that the corresponding nerve functor is [[full and faithful functor|fully faithful]] (in other words, if $i$ is inclusion then $S$ is a left adequate subcategory of $C$ in terminology of \[Isbell 1960\]). 
The nerve functor may be viewed as a [[singular functor]] of the functor $i$.

#Examples#

## ordinary nerve of a category ##

Recall that the [[nLab:simplex category|simplex category]] $\Delta$ is equivalent to the full subcategory 
$$
  i : \Delta \hookrightarrow Cat
$$
of [[nLab:Cat|Cat]] on linear [[nLab:quiver|quivers]], meaning that the object $[n] \in Obj(\Delta)$ can be identified with the category $[n] = \{0 \to 1 \to 2 \to \cdots \to n\}$. The morphisms of $\Delta$ are all functors between these "linear quiver" categories.

For $D$ any [[nLab:locally small category|locally small category]], the **nerve** $N(D)$ of $D$ is the [[nLab:simplicial set]] given by

$$
  N(D) : \Delta^{op} 
     \hookrightarrow
     Cat
    \stackrel{Cat(-,D)}{\to}
    Set
  \,,
$$
where [[nLab:Cat|Cat]] is regarded as an ordinary 1-category with objects locally small categories, and morphisms being [[nLab:functor|functors]] between these.

So the set $N(D)_n$ of $n$-[[nLab:simplex|simplices]] of the nerve is the set of functors $\{0 \to 1 \to \cdots \to n\} \to D$. This is clearly the same as the set of sequences of composable morphisms in $D$ of length $n$:

$$
  N(D)_n = 
   \underbrace{
   Mor(D) {}_t \times_s Mor(D) {}_t \times_s \cdots
   {}_t \times_s Mor(D)}_{n factors}
$$

The collection of all functors between linear quivers 
$$
  \{
    0 \to 1 \to \cdots \to n
  \}
  \to
  \{
    0 \to 1 \to \cdots \to m
  \}
$$
is generated from those that map almost all generating morphisms $k \to k+1$ to another generating morphism, except at one position, where they

* map a single generating morphism to the composite of two generating morphisms 
  $$
   \delta^n_i : [n-1] \to n
  $$
  $$
    \delta^n_i : ((i-1) \to i) \mapsto ((i-1) \to i \to (i+1))
  $$

* map one generating morphism to an identity morphism
  $$
   \sigma^n_i : [n+1] \to [n]
  $$
  $$
    \sigma^n_i : (i \to i+1) \mapsto Id_i
  $$

It follows that, for instance

* for $(d_0 \stackrel{f_1}{\to} d_1, d_1 \stackrel{f_2}{\to} d_2, d_2 \stackrel{f_3}{\to} d_3) \in N(D)_3$ the image under $d_1 := N(D)(\delta_1) : N(D)_3 \to N(D)_2$ is obtained by composing the first two morphisms in this sequence: $(d_0 \stackrel{f_2 \circ f_1}{\to} d_2, d_2 \stackrel{f_3}{\to} d_3) \in N(D)_2$

* for $(d_0 \stackrel{f_1}{\to} d_1) \in N(D)_1$ the image under $s_1 := N(D)(\sigma_1) : N(D)_1 \to N(D)_2$ is obtained by inserting an identity morphism: 
$(d_0 \stackrel{f_1}{\to} d_1, d_1 \stackrel{Id_{d_1}}{\to} d_1) \in N(D)_2$.

In this way, generally the face and degeneracy maps of the nerve of a category come from composition of morphisms and from inserting identity morphisms.

In particular in light of their generalization to nerves of higher categories, discussed below, the cells in the nerve $N(D)$ have the following interpretation:

* $S_0 = \{d | d \in Obj(D)\} $ is the collection of objects of $D$;

* $S_1 = Mor(D) = \{d \stackrel{f}{\to} d' | f \in Mor(D)\}$ is the collection of morphisms of $D$;

* $S_2 = \left\{
    \left.
    \array{
      && d_1
      \\
      & {}^{f_1}\nearrow &\Downarrow^{\exists !}& \searrow^{f_2}
      \\
      d_0 &&\stackrel{f_2 \circ f_1}{\to}&& d_2
    }
    \right|
    (f_1, f_2) \in Mor(D) {}_t \times_s Mor(D)
  \right\}$ is the collection of composable morphisms in $D$: the 2-cell itself is to be read as the _composition operation_, which is unique for an  ordinary category (there is just one way to compose to morphisms);

* $S_3 =
    \left\{
      \left.
        \array{
          d_1 &\stackrel{f_2}{\to}& d_2
          \\
          {}^{f_1}\uparrow &
            {}^{f_2 \circ f_1}\nearrow
          & \downarrow^{f_3}
          \\
          d_0 &\stackrel{f_3\circ (f_2\circ f_1)}{\to}&
          d_3
        }
        \;\;\;\;\;\stackrel{\exists !}{\Rightarrow}
        \;\;\;\;\;
        \array{
          d_1 &\stackrel{f_2}{\to}& d_2
          \\
          {}^{f_1}\uparrow &
            \searrow^{f_3\circ f_2}
          & \downarrow^{f_3}
          \\
          d_0 &\stackrel{(f_3\circ f_2) \circ f_1}{\to}&
          d_3
        }
      \right|
      (f_3,f_2, f_1) \in
      Mor(D) {}_t \times_s Mor(D) {}_t \times_s Mor(D)
    \right\}
  $ is the collection of triples of composable morphisms, to be read as the unique associators that relate one way to compose three morphisms using the above 2-cells to the other way.

### properties of the nerve of a category ###

+-- {: .un_prop}
###### Proposition

A [[simplicial set]] $S$ is the nerve of a locally small category $C$ if and only if all the commuting squares

$$
  \array{
    S_{n+m} &\stackrel{\cdots \circ d_0 \circ d_0}{\to}& S_m
    \\
    {}^{\cdots d_{n+m-1}\circ d_{n+m}}\downarrow && \downarrow
    \\
    S_n &\stackrel{d_0 \circ \cdots d_0}{\to}& S_0
  }
$$

are [[pullback]] diagrams.

=--

Unwrapping this definition inductively in $(n+m)$, this says that a simplicial set is the nerve of a category if and only if all its cells in degree $\geq 2$ are unique compositors, associators, pentagonators, etc of composition of 1-morphisms. No non-trivial such structure cells appear and no further higher cells appear.

This characterization of categories in terms of nerves directly leads to the model of [[(infinity,1)-category]] in terms of [[complete Segal space]]s by replacing in the above discussion sets by [[topological space]]s (or something similar, like [[Kan complex]]es) and pullbacks by [[homotopy pullback]]s.

+-- {: .un_prop}
###### Proposition

The nerve functor

$$
  N : Cat \to SSet
$$

is a [[full and faithful functor]].

=--

So  [[functor]]s between [[locally small category|locally small categories]] are in bijections with morphisms of [[simplicial set]]s between their nerves.



+-- {: .un_prop}
###### Proposition

The nerve $N(C)$ of a locally small category 
is a [[Kan complex]] if and only if $C$ is a [[groupoid]].

=--

The existence of [[inverse]] morphisms in $D$ corresponds to the fact that in the [[Kan complex]] $N(D)$ the "outer" [[horn]]s

$$
  \array{
    && d_0
    \\
    & && \searrow^{f}
    \\
    d_1 &&\stackrel{Id_{d_1}}{\to} && d_1
  }
  \;\;\; 
  \;\;\; 
  and
  \;\;\; 
  \;\;\; 
  \array{
    && d_1
    \\
    & {}^f\nearrow &&     
    \\
    d_0 &&\stackrel{Id_{d_0}}{\to} && d_1
  }
$$

have fillers 

$$
  \array{
    && d_0
    \\
    & {}^{f^{-1}}\nearrow&& \searrow^{f}
    \\
    d_1 &&\stackrel{Id_{d_1}}{\to} && d_1
  }
  \;\;\; 
  \;\;\; 
  and
  \;\;\; 
  \;\;\; 
  \array{
    && d_1
    \\
    & {}^f\nearrow && \searrow^{f^{-1}}
    \\
    d_0 &&\stackrel{Id_{d_0}}{\to} && d_0
  }
$$

(even unique fillers, due to the above).

It is in this sense that a simplicial set that is a [[Kan complex]] but which does not necessarily have the above pullback property that makes it a nerve of an ordinary groupoid models an [[infinity-groupoid]].

## nerve of an $\omega$-category ##

* This previous example is the restriction to [[1-category|1-categories]] of the nerve ("$\omega$-nerve") on [[strict omega-category|strict omega-categories]] which is induced by the [[oriental]]s $i := O : \Delta \to \omega Cat$. This nerve is not fully faithful.

* When $C$ is the strict 1-category of [[2-category|2-categories]] or of [[bicategory|bicategories]] and homomorphisms of bicategories, and $S=\Delta$ the corresponding nerve is called the _Duskin nerve_.

#Remarks# 

##Geometric realization##
Often the operation of taking the nerve of a (higher) category is followed by forming the [[geometric realization]] of the corresponding cellular set.

##Nerves and higher categories##
For many purposes it is convenient to conceive categories and especially [[infinity-category|infinity-categories]] entirely in terms of their nerves: those simplicial sets that arise as certain nerves are usually characterized by certain properties. So one can turn this around and _define_ an [[infinity-category]] as a simplicial set with certain properties. This is the strategy of a [[geometric definition of higher category]]. Examples for this are [[complicial set|complicial sets]], [[Kan complex|Kan complexes]], [[quasi-category|quasi-categories]], [[simplicial T-complex|simplicial T-complexes]],...

##Internal nerve##
A variant of the nerve construction can also be applied _internally_ within a category, to any internal category, see the discussion at [[internal category]].

##Literature##

* [Dwyer Kan 1984]
W. G. Dwyer, D. M. Kan, Singular functors and realization functors, Nederl. Akad. Wetensch. Indag. Math. 46 (1984), no. 2, 147--153. [pdf](http://www.nd.edu/~wgd/Dvi/SingularAndRealization.pdf)

* [Isbell 1960] J. R. Isbell, Adequate subcategories, Illinois J. Math. 4, 541--552 (1960)

* [Leinster 2004] T. Leinster, Higher operads, higher categories, London Mathematical Society Lecture Note Series, 298. Cambridge Univ. Press 2004. xiv+433 pp. ISBN: 0-521-53215-9, [arXiv:math.CT/0305049](http://front.math.ucdavis.edu/0305.5049)

* [Street 1987] R. Street, The algebra of oriented simplexes,
J. Pure Appl. Algebra 49 (1987), no. 3, 283--335.  