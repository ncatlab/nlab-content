
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

The notion of _nerve_ is part of a notion of pairs of [[adjoint functors]]. For the general abstract theory behind this see

* [[nerve and realization]].

***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

As soon as any [[locally small category]] $C$ comes equipped with a [[simplicial object|cosimplicial object]]

$$
  \Delta_C : \Delta \to C
$$

that we may think of as determining a [[geometric realization|realization]] of the standard $n$-[[simplex]] in $C$, we make every [[object]] of $C$ [[space and quantity|probeable]] by [[simplex|simplices]] in that there is now a way to find the set 

$$
  N(A)_n := Hom_C(\Delta_C[n],A)
$$

of ways to map the $n$-[[simplex]] into a given object $A$.

These collections of sets evidently organize into a [[simplicial set]]

$$
  N(A) : \Delta^{op} \to Set
  \,.
$$

This [[simplicial set]] is called the _nerve_ of $A$ (with respect to the chosen [[geometric realization|realization]] of the standard simplicies in $C$).

There various obvious generalizations of this procedure, some of which described below.

## Definition ##

> (notice that for the moment the following gives just one particular case of the more general notion of nerve)

Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] $G$, the [[simplex category]] $\Delta$, the [[cube category]] $\Box$, the [[cycle category]] $\Lambda$ of Connes, or certain category $\Omega$ related to trees whose corresponding presheaves are [[dendroidal set|dendroidal sets]].

If $C$ is any [[locally small category|locally small]] category or, more generally, a $V$-[[enriched category]] equipped with a [[functor]]
$$
  i : S \to C
$$
we obtain a functor
$$
  N : C \to V^{S^{op}}
$$
from $C$ to [[globular sets]] or [[simplicial sets]] or [[cubical sets]], respectively, (or the corresponding $V$-objects) given on an [[object]] $c \in C$ by
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

## Examples ##

### Ordinary nerve of a category ###

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



**example: bar construction ** Let $A$ be a [[monoid]] (for instance a [[group]]) and write $\mathbf{B} A$ for the corresponding one-object [[category]] with $Mor(\mathbf{B} A) = A$. Then the nerve $N(\mathbf{B} A)$ of $\mathbf{B}A$ is the simplicial set which is the usual [[bar construction]] of $A$
  $$
    N(\mathbf{B}A)
    =
    \left(
       \cdots
       A \times A \times A \stackrel{\to}{\stackrel{\to}{\to}} 
       A \times A \stackrel{\to}{\to} A \to {*}
    \right)
  $$
  In particular, when $A = G$ is a discrete group, then the [[geometric realization]] $|N(\mathbf{B} G)|$ of the nerve of $\mathbf{B}G$ is the [[classifying space|classifying]] [[topological space]] $ \cdots \simeq B G$ for $G$-[[principal bundles]].


#### Properties of the nerve of a category {#PropNerveCat}

The following lists some characteristic properties of simplicial sets that are nerves of categories.

+-- {: .un_prop}
###### Proposition

A [[simplicial set]] is the nerve of a category precisely if all _inner_ [[horn]]s have _unique_ fillers.

=--

See [[inner fibration]] for details on this.


+-- {: .un_prop}
###### Proposition

A [[simplicial set]] is the nerve of a groupoid precisely if all [[horn]]s have _unique_ fillers.

=--


+-- {: .un_prop}
###### Proposition

The nerve $N(C)$ of a category is [[coskeleton|2-coskeletal]].

=--

Hence all [[horn]] inclusions $\Lambda[n]_i \hookrightarrow \Delta[n]$ have unique fillers for $n \gt 3$, and all boundary inclusions $\partial \Delta[n] \hookrightarrow \Delta[n]$ have unique fillers for $n \heq 3$.

Here the point as compared to the previous statements is that in particular all the outer horns have fillers for $n \gt 3$.

+-- {: .un_prop}
###### Proposition

The nerve $N(C)$ of a locally small category 
is a [[Kan complex]] if and only if $C$ is a [[groupoid]].

=--

The existence of [[inverse]] morphisms in $D$ corresponds to the fact that in the [[Kan complex]] $N(D)$ the "outer" [[horns]]

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

It is in this sense that a simplicial set that is a [[Kan complex]] but which does not necessarily have the above pullback property that makes it a nerve of an ordinary groupoid models an [[∞-groupoid]].




+-- {: .un_prop}
###### Proposition

The nerve functor

$$
  N : Cat \to SSet
$$

is a [[full and faithful functor]].

=--

So  [[functors]] between [[locally small category|locally small categories]] are in [[bijection]] with morphisms of [[simplicial sets]] between their nerves.




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

This characterization of categories in terms of nerves directly leads to the model of [[(∞,1)-category]] in terms of [[complete Segal spaces]] by replacing in the above discussion sets by [[topological spaces]] (or something similar, like [[Kan complexes]]) and pullbacks by [[homotopy pullback|homotopy pullbacks]].



### Nerve of a 2-category ###

For [[2-categories]] modeled as [[bicategories]] the nerve operation is calledd the [[Duskin nerve]].


+-- {: .un_prop}
###### Proposition

A simplicial set is the [[Duskin nerve]] of a [[bigroupoid]] precisely if it is a 2-[[hypergroupoid]]: a [[Kan complex]] such that the horn fillers in dimension $\geq 3$ are _unique_ .  

=--

This is theorem 8.6 in ([Duskin](#http://www.tac.mta.ca/tac/volumes/9/n10/9-10abs.html))

For a [[2-category]], regarded as a [[Cat]]-[[internal category]] one can apply the nerve operation for categories in stages, to obtain the [[double nerve]].

### Nerve of an $\omega$-category ###

* For [[strict omega-category|strict omega-categories]] there is a nerve induced by the [[orientals]]. see [[omega-nerve]].


### Nerve of chain complexes ###

Let $Ch_+$ be the [[category of chain complexes]]
of abelian groups. 

Then there is a [[simplicial object|cosimplicial chain complex]]

$$
  C_\bullet : \Delta \to Ch_+
$$

given by sending the standard $n$-simplex $\Delta[n]$ first to the free [[simplicial group]] $F(\Delta[n])$ over it and then that to the normalized [[Moore complex]]. This is a small version of the ordinary [[homology]] [[chain complex]] of the standard $n$-[[simplex]].

The nerve induced by this cosimplicial object was first considered in 

* D. Kan, _Functors involving c.s.s complexes_, Transactions of the American Mathematical Society, Vol. 87, No. 2 (Mar., 1958), pp. 330--346 ([jstor](http://www.jstor.org/stable/1993103))

The nerve/[[geometric realization|realization]] adjunction induced from this is the [[Dold?Kan correspondence]]. See there for more details.


## Remarks ## 

###Geometric realization###
Often the operation of taking the nerve of a (higher) category is followed by forming the [[geometric realization]] of the corresponding cellular set.

###Nerves and higher categories###
For many purposes it is convenient to conceive categories and especially [[∞-categories]] entirely in terms of their nerves: those simplicial sets that arise as certain nerves are usually characterized by certain properties. So one can turn this around and _define_ an [[∞-category]] as a simplicial set with certain properties. This is the strategy of a [[geometric definition of higher category]]. Examples for this are [[complicial set|complicial sets]], [[Kan complex|Kan complexes]], [[quasi-category|quasi-categories]], [[simplicial T-complex|simplicial T-complexes]],...

###Internal nerve###
A variant of the nerve construction can also be applied _internally_ within a category, to any internal category, see the discussion at [[internal category]].

##References##

* [Dwyer Kan 1984]
W. G. Dwyer, D. M. Kan, Singular functors and realization functors, Nederl. Akad. Wetensch. Indag. Math. 46 (1984), no. 2, 147--153. [pdf](http://www.nd.edu/~wgd/Dvi/SingularAndRealization.pdf)

* [Isbell 1960] J. R. Isbell, Adequate subcategories, Illinois J. Math. 4, 541--552 (1960)

* [[Tom Leinster]], _Higher operads, higher categories_ , London Mathematical Society Lecture Note Series, 298. Cambridge Univ. Press 2004. xiv+433 pp. ISBN: 0-521-53215-9, [arXiv:math.CT/0305049](http://front.math.ucdavis.edu/0305.5049)

* [Street 1987] [[Ross Street]], The algebra of oriented simplexes,
J. Pure Appl. Algebra 49 (1987), no. 3, 283--335.


[[!redirects nerves]]
[[!redirects simplicial nerve]]
[[!redirects simplicial nerves]]