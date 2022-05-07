
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


The _nerve_ is the right adjoint of a pair of [[adjoint functors]] that exists in many situations.  For the general abstract theory behind this see

* [[nerve and realization]].


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

This [[simplicial set]] is called the _nerve_ of $A$ (with respect to the chosen [[geometric realization|realization]] of the standard simplices in $C$).  Typically the nerve defines a functor $N \colon C \to Set^{\Delta^op}$ that has a left adjoint $|\cdot| \colon Set^{\Delta^op} \to C$ called [[realization]].

There are many generalizations of this procedure, some of which are described below.

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
from $C$ to [[globular sets]] or [[simplicial sets]] or [[cubical sets]], respectively, (or the corresponding $V$-objects) given on an [[object]] $c \in C$ by the [[restricted Yoneda embedding]]
$$
  N_i(c) : S^{op} \stackrel{i}\to C^{op} 
    \stackrel{C(-,c)}{\to}
    V
  \,.
$$

This $N_i(c)$ is the **nerve** of $c$ with respect to the chosen $i : S \to C$. In other words, $N = i^* \circ Y$ where $Y: C \to [C^{op}, V]$ is the curried Hom functor; if $V=\mathsf{Sets}$ then $Y$ is the [[Yoneda embedding]].

Typically, one wants that $i$ is [[dense functor]], i.e. that every object $c$ of $C$ is canonically a colimit of a diagram of objects in $M$, more precisely,
$$
\mathrm{colim}((i/c)\stackrel{\mathrm{pr}_S}{\longrightarrow} S \stackrel{i}{\to} C) = c,
$$
which is equivalent to the requirement that the corresponding nerve functor is [[full and faithful functor|fully faithful]] (in other words, if $i$ is inclusion then $S$ is a left adequate subcategory of $C$ in terminology of [Isbell 60](#Isbell60)). 
The nerve functor may be viewed as a [[singular functor]] of the functor $i$.

## Examples ##

### Nerve of a 1-category 
 {#NerveOfACategory}

For fixing notation, recall that the source and target maps of a small  [[category#OneCollectionOfMorphisms|category]] form a [[span]] in the category $Span(Set)$ where composition [[span#categories_of_spans|is given by a pullback]] (fiber product). The pairs of composable morphisms of a category are then obtained composing its source/target span with itself.

+-- {: .num_defn #SmallCategory}
###### Definition

A _[[small category]]_ $\mathcal{C}_\bullet$ is

* a pair of [[sets]] $\mathcal{C}_0 \in Set $ (the set of [[objects]]) and $\mathcal{C}_1 \in Set$ (the set of [[morphisms]])

* equipped with [[functions]]

  $$
    \array{
      \mathcal{C}_1 \times_{\mathcal{C}_0} \mathcal{C}_1
      &\stackrel{\circ}{\to}&
      \mathcal{C}_1
      & \stackrel{\overset{t}{\to}}{\stackrel{\overset{i}{\leftarrow}}{\underset{s}{\to}}}&
      \mathcal{C}_0
    }\,,
  $$

  where the [[fiber product]] on the left is that over $\mathcal{C}_1 \stackrel{t}{\to} \mathcal{C}_0 \stackrel{s}{\leftarrow} \mathcal{C}_1$, 

such that

* $i$ takes values in [[endomorphisms]];

  $$
    t \circ i = s \circ i =   id_{\mathcal{G}_0}, \;\;\; 
  $$

* $\circ$ defines a partial [[composition]] operation which is [[associativity|associative]] and [[unitality|unital]] for $i(\mathcal{C}_0)$ the [[identities]]; in particular

  $s (g \circ f) = s(f)$ and $t (g \circ f) = t(g)$.

=--

#### Definition

+-- {: .num_defn #NerveOfSmallCategory}
###### Definition

For $\mathcal{C}_\bullet$ a [[small category]], def. \ref{SmallCategory}, 
its _simplicial nerve_ $N(\mathcal{C}_\bullet)_\bullet$ is 
the [[simplicial set]] with 

$$
  N(\mathcal{C}_\bullet)_n \coloneqq \mathcal{C}_1^{\times_{\mathcal{C}_0}^n}
$$ 

the set of sequences of composable morphisms of length $n$, for $n \in \mathbb{N}$;

with face maps

$$
  d_k \colon N(\mathcal{C}_\bullet)_{n+1} \to N(\mathcal{C}_\bullet)_{n}
$$

being

* for $n = 0$, $d_0= target:arr(\mathcal{C})\to ob(\mathcal{C})$, whilst $d_1$ is similarly the domain /  source function; 

* for $n \geq 1$ 

  * the two outer face maps $d_0$ and $d_{n+1}$ are given by forgetting the first and the last morphism in such a sequence, respectively; 

  * the $n$ inner face maps $d_{0 \lt k \lt n+1}$ are given by composing the $k$th morphism with the $k+1$st in the sequence.

The degeneracy maps

$$
  s_k \colon N(\mathcal{C}_\bullet)n \to N(\mathcal{C}_\bullet)_{n+1}
  \,.
$$

are given by inserting an [[identity]] morphism on $x_k$.


=--

+-- {: .num_remark}
###### Remark

Spelling this out in more detail: write

$$
  \mathcal{C}_n = 
  \left\{
    x_0 
      \stackrel{f_{0,1}}{\to} 
    x_1
      \stackrel{f_{1,2}}{\to}
    x_2
      \stackrel{f_{2,3}}{\to}
    \cdots
      \stackrel{f_{n-1,n}}{\to}
    x_n
  \right\}
$$

for the set of sequences of $n$ composable morphisms. Given any element of 
this set and $0 \lt k \lt n $, write 

$$
  f_{i-1,i+1} \coloneqq f_{i,i+1} \circ f_{i-1,i}
$$

for the composition of the two morphism that share the $i$th vertex. 

With this, face map $d_k$ acts simply by "removing the index $k$":

$$
  d_0
  \colon 
  (x_0 \stackrel{f_{0,1}}{\to}  x_1 \stackrel{f_{1,2}}{\to} x_{2} \cdots \stackrel{f_{n-1,n}}{\to} x_n )
  \mapsto
  (x_1 \stackrel{f_{1,2}}{\to} x_{2} \cdots \stackrel{f_{n-1,n}}{\to} x_n )  
$$

$$
  d_{0\lt k \lt n}
   \colon
  (
    x_0 
    \cdots 
    \stackrel{}{\to}
    x_{k-1}
    \stackrel{f_{k-1,k}}{\to}
    x_k
    \stackrel{f_{k,k+1}}{\to}
    x_{k+1}
    \stackrel{}{\to}
    \cdots
    x_n
  )
  \mapsto
  (
    x_0 
    \cdots 
    \stackrel{}{\to}
    x_{k-1}
    \stackrel{f_{k-1,k+1}}{\to}
    x_{k+1}
    \stackrel{}{\to}
    \cdots
    x_n
  )  
$$

$$
  d_n 
  \colon
  (
    x_0 \stackrel{f_{0,1}}{\to}
    \cdots
    \stackrel{f_{n-2,n-1}}{\to} 
    x_{n-1}
    \stackrel{f_{n-1,n}}{\to}
    x_n
  )
  \mapsto
  (
    x_0 \stackrel{f_{0,1}}{\to}
    \cdots
    \stackrel{f_{n-2,n-1}}{\to} 
    x_{n-1}
  )
  \,.
$$


Similarly, writing

$$
  f_{k,k} \coloneqq id_{x_k}
$$

for the identity morphism on the object $x_k$, 
then the degeneracy map acts by "repeating the $k$th index"

$$
  s_k
  \colon
  (
    x_0 \stackrel{}{\to}
    \cdots 
    \to
    x_k
    \stackrel{f_{k,k+1}}{\to}
    x_{k+1}
    \to
    \cdots
  )
  \mapsto
  (
    x_0 \stackrel{}{\to}
    \cdots 
    \to
    x_k
     \stackrel{f_{k,k}}{\to}
    x_k
    \stackrel{f_{k,k+1}}{\to}
    x_{k+1}
    \to
    \cdots
  )
  \,.
$$

This makes it manifest that these functions organise into a [[simplicial set]].

=--

More abstractly, this construction is described as follows. Recall that 

+-- {: .num_defn}
###### Definition

The [[nLab:simplex category|simplex category]] $\Delta$ is equivalent to the [[full subcategory]] 
$$
  i \colon \Delta \hookrightarrow Cat
$$
of [[Cat]] on non-empty finite [[linear orders]] regarded as categories, meaning that the object $[n] \in Obj(\Delta)$ may be identified with the category $[n] = \{0 \to 1 \to 2 \to \cdots \to n\}$. The morphisms of $\Delta$ are all functors between these total linear categories.

=--

+-- {: .num_defn}
###### Definition

For $\mathcal{C}$ a [[small category]] its _nerve_ 
$N(\mathcal{C})$ is the [[simplicial set]] given by


$$
  N(\mathcal{C}) 
  \colon 
  \Delta^{op} 
     \hookrightarrow
     Cat^{op}
    \stackrel{Cat(-,\mathcal{C})}{\to}
    Set
  \,,
$$
where [[Cat]] is regarded as a [[1-category]] with objects locally small categories, and morphisms being [[functors]] between these.

=--

So the set $N(\mathcal{C})_n$ of $n$-[[simplices]] of the nerve is the set of functors $\{0 \to 1 \to \cdots \to n\} \to \mathcal{C}$. This is clearly the same as the set of sequences of composable morphisms in $\mathcal{C}$ of length $n$ obtained by iterated fiber product (as [above](#NerveOfACategory) for pairs of composables):

$$
  N(\mathcal{C})_n = 
  \underbrace{
     Mor(\mathcal{C}) \times_{Obj(\mathcal{C})} Mor(\mathcal{C}) 
     \times_{Obj(\mathcal{C})} \cdots \times_{Obj(\mathcal{C})} Mor(\mathcal{C}) 
  }_{n \medspace factors}
$$

The collection of all functors between linear orders
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
   \delta^n_i : [n-1] \to [n]
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

* for $(d_0 \stackrel{f_1}{\to} d_1, d_1 \stackrel{f_2}{\to} d_2, d_2 \stackrel{f_3}{\to} d_3) \in N(D)_3$ the image under $d_1 := N(\mathcal{C})(\delta_1) : N(\mathcal{C})_3 \to N(\mathcal{C})_2$ is obtained by composing the first two morphisms in this sequence: $(d_0 \stackrel{f_2 \circ f_1}{\to} d_2, d_2 \stackrel{f_3}{\to} d_3) \in N(\mathcal{C})_2$

* for $(d_0 \stackrel{f_1}{\to} d_1) \in N(\mathcal{C})_1$ the image under $s_1 := N(\mathcal{C})(\sigma_1) : N(\mathcal{C})_1 \to N(\mathcal{C})_2$ is obtained by inserting an identity morphism: 
$(d_0 \stackrel{f_1}{\to} d_1, d_1 \stackrel{Id_{d_1}}{\to} d_1) \in N(\mathcal{C})_2$.

In this way, generally the face and degeneracy maps of the nerve of a category come from composition of morphisms and from inserting identity morphisms.

In particular in light of their generalization to nerves of higher categories, discussed below, the cells in the nerve $N(\mathcal{C})$ have the following interpretation:

* $N(\mathcal{C})_0 = \{d | d \in Obj(\mathcal{C})\} $ is the collection of [[objects]] of $\mathcal{C}$;

* $N(\mathcal{C})_1 = Mor(\mathcal{C}) = \{d \stackrel{f}{\to} d' | f \in Mor(D)\}$ is the collection of [[morphisms]] of $D$;

* $N(\mathcal{C})_2 = \left\{
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
  \right\}$ is the collection of composable morphisms in $\mathcal{C}$ as in the diagram
  \begin{imagefromfile}
      "file_name": "2-simplex-1-cat-nerve.svg",
      "width": 150
  \end{imagefromfile}
  The 2-cell itself is to be read as the _composition operation_, which is unique for an  ordinary category (there is just one way to compose two morphisms);

* $N(\mathcal{C})_3 = \left\{
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
  $ is the collection of triples of composable morphisms as in the diagram
  \begin{imagefromfile}
      "file_name": "3-simplex-1-cat-nerve.svg",
      "width": 450
  \end{imagefromfile}
  to be read as the unique associators that relate one way to compose three morphisms using the above 2-cells to the other way.

#### Examples

+-- {: .num_example}
###### Example
**(bar construction)** 

Let $A$ be a [[monoid]] (for instance a [[group]]) with multiplication $m$, and write $\mathbf{B} A$ for the corresponding one-object [[category]] with $Mor(\mathbf{B} A) = A$. Then the nerve $N(\mathbf{B} A)$ of $\mathbf{B}A$ is the simplicial set which is given by a [[two-sided bar construction]] of $A$, namely $B(1, A, 1)$: 
  $$
    N(\mathbf{B}A)
    =
    \left(
       \cdots
       A \times A \stackrel{\to}{\stackrel{\to}{\to}} 
       A \stackrel{\to}{\to} {*}
    \right)
  $$
where for example the three parallel face maps on display are $\pi_1, m, \pi_2: A \times A \to A$. 

  In particular, when $A = G$ is a discrete group, then the [[geometric realization]] $|N(\mathbf{B} G)|$ of the nerve of $\mathbf{B}G$ is the [[classifying space|classifying]] [[topological space]] $ \cdots \simeq B G$ for $G$-[[principal bundles]].

=--

#### Properties
 {#PropNerveCat}

The following lists some characteristic properties of simplicial sets that are nerves of categories.

+-- {: .num_prop}
###### Proposition

A simplicial set is the nerve of a category precisely if it satisfies the [[Segal condition]].

=--

See at _[[Segal condition]]_ for more on this.

+-- {: .num_prop}
###### Proposition

A [[simplicial set]] is the nerve of a [[small category]] precisely if all _inner_ [[horns]] have _unique_ fillers.

=--

See [[inner fibration]] for details on this.


+-- {: .num_prop}
###### Proposition

A [[simplicial set]] is the nerve of a [[groupoid]] precisely if _all_ [[horns]] of dimension $\gt 1$ have _unique_ fillers.

=--


+-- {: .num_prop}
###### Proposition

The nerve $N(C)$ of a category is [[coskeleton|2-coskeletal]].

=--

Hence all [[horn]] inclusions $\Lambda[n]_i \hookrightarrow \Delta[n]$ have unique fillers for $n \gt 3$, and all boundary inclusions $\partial \Delta[n] \hookrightarrow \Delta[n]$ have unique fillers for $n \geq 3$.

Here the point as compared to the previous statements is that in particular all the outer horns have fillers for $n \gt 3$.

+-- {: .num_prop}
###### Proposition

The nerve $N(C)$ of a [[small category]] 
is a [[Kan complex]] precisely if $C$ is a [[groupoid]].

=--

The existence of [[inverse]] morphisms in $C$ corresponds to the fact that in the [[Kan complex]] $N(C)$ the "outer" [[horns]]

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

It suggests the sense that  a Kan complex  models an [[∞-groupoid]]. The possible lack of uniqueness of fillers in general gives the 'weakness' needed, whilst the lack of a [[coskeletal]] property requirement means that the homotopy type it represents has enough generality, not being constrained to be a 1-type.

+-- {: .num_prop}
###### Proposition

The nerve functor

$$
  N : Cat \to SSet
$$

is a [[full and faithful functor]].

=--

So  [[functors]] between [[locally small category|locally small categories]] are in [[bijection]] with morphisms of [[simplicial sets]] between their nerves.




+-- {: .num_prop}
###### Proposition

A [[simplicial set]] $S$ is the nerve of a locally small category $C$ precisely if it satisfies the [[Segal conditions]]:  precisely if all the commuting squares

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

For [[2-categories]] modeled as [[bicategories]] the nerve operation is called the [[Duskin nerve]].


+-- {: .num_prop}
###### Proposition

A simplicial set is the [[Duskin nerve]] of a [[bigroupoid]] precisely if it is a 2-[[hypergroupoid]]: a [[Kan complex]] such that the horn fillers in dimension $\geq 3$ are _unique_.

=--

This is theorem 8.6 in ([Duskin](http://www.tac.mta.ca/tac/volumes/9/n10/9-10abs.html))

For a [[2-category]], regarded as a [[Cat]]-[[internal category]] one can apply the nerve operation for categories in stages, to obtain the [[double nerve]].

### Nerve of a 3-category ###

One also has a nerve operation for [[3-categories]] modeled as [[tricategories]]: the [[Street nerve]].

+-- {: .num_prop}
###### Proposition

A simplicial set is the [[Street nerve]] of a [[trigroupoid]] precisely if it is a 3-[[hypergroupoid]]: a [[Kan complex]] such that the horn fillers in dimension $\geq 4$ are _unique_.

=--

This is the main result of ([Carrasco, 2014](#Carrasco2014)).

### Nerve of an $\omega$-category ###

* For [[strict omega-category|strict omega-categories]] there is a nerve induced by the [[orientals]]; see [[omega-nerve]].


### Nerve of chain complexes ###

Let $Ch_+$ be the [[category of chain complexes]]
of abelian groups, then there is a [[simplicial object|cosimplicial chain complex]]

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



## Related concepts

* [[monad with arities]]

* [[Duskin nerve]]

* [[Street nerve]]

* [[∞-nerve]]

* [[homotopy coherent nerve]]

* [[dg-nerve]]


## References

### For covers

The notion of the nerve of an [[cover]] (in modern parlance: of its [[Cech groupoid]]) appears in: 

* [[Paul Alexandroff]], Section 9 of: _Über den allgemeinen Dimensionsbegriff und seine Beziehungen zur elementaren geometrischen Anschauung_, Mathematische Annalen 98 (1928), 617–635 ([doi:10.1007/BF01451612](https://doi.org/10.1007/BF01451612)).


### For categories

The notion of the nerve of a general category already appears in Proposition 4.1 of

* [[Alexander Grothendieck]], _TECHNIQUES DE CONSTRUCTION ET THÉORÈMES D’EXISTENCE EN GÉOMÉTRIE ALGÉBRIQUE.  III : PRÉSCHEMAS QUOTIENTS_, Séminaire BOURBAKI, 13e année, 1960/61, no. 212, February 1961.  [PDF](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf).

Another early appearance in print is

* [[Graeme Segal]], Section 2 of: _Classifying spaces and spectral sequences_,  Publications Mathématiques de l'IHÉS, Volume 34  (1968), p. 105-112  ([numdam:PMIHES_1968__34__105_0](http://www.numdam.org/item/PMIHES_1968__34__105_0/))

  > (in the context of constructing [[classifying spaces]] for [[principal bundles]] in [[algebraic topology]])

Review and exposition:

* [[Tom Leinster]], p. 117 onwards in: _Higher operads, higher categories_ , London Mathematical Society Lecture Note Series, 298. Cambridge Univ. Press 2004. xiv+433 pp. ISBN: 0-521-53215-9 ([arXiv:math.CT/0305049](https://arxiv.org/abs/math/0305049))

* [[Tom Leinster]], *[How I learned to love the nerve construction](https://golem.ph.utexas.edu/category/2008/01/mark_weber_on_nerves_of_catego.html)*, $n$-Category Caf&#233;, January 6, 2008.

  > (an explanation of how the simplex category and the nerve construction arise canonically from the free category monad)


See also:

* {#Isbell60} [[John Isbell]], *Adequate subcategories*, Illinois J. Math. 4, 541--552 (1960) ([doi:10.1215/ijm/1255456274](https://www.projecteuclid.org/journals/illinois-journal-of-mathematics/volume-4/issue-4/Adequate-subcategories/10.1215/ijm/1255456274.full))

* [[W. G. Dwyer]], [[D. M. Kan]], Singular functors and realization functors, Nederl. Akad. Wetensch. Indag. Math. 46 (1984), no. 2, 147--153. [pdf](http://www.nd.edu/~wgd/Dvi/SingularAndRealization.pdf)


### For higher categories

For [[strict omega-categories]]:

* [[Ross Street]], _The algebra of oriented simplexes_, J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf), <a href="https://doi.org/10.1016/0022-4049(87)90137-X">doi:10.1016/0022-4049(87)90137-X</a>).

For [[2-categories]]:

* [[Paul Bressler]], Alexander Gorokhovsky, [[Ryszard Nest]], [[Boris Tsygan]], _Formality for algebroids I: Nerves of two-groupoids_ ([arxiv/1211.6603](http://arxiv.org/abs/1211.6603))

For [[3-categories]]:

* {#Carrasco2014} Pilar Carrasco, _Nerves of Trigroupoids as Duskin-Glenn’s $3$-Hypergroupoids_, Applied Categorical Structures 23.5 (2015): 673-707 ([doi:10.1007/s10485-014-9374-7](https://doi.org/10.1007/s10485-014-9374-7))




[[!redirects nerves]]
[[!redirects nerve functor]]
[[!redirects nerve functors]]
[[!redirects simplicial nerve]]
[[!redirects simplicial nerves]]
[[!redirects simplicial nerve functor]]
[[!redirects simplicial nerve functors]]

[[!redirects nerve of a category]]
[[!redirects nerves of a categories]]