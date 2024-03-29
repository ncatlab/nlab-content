
\tableofcontents

#Idea#

[[Nils Baas]] has been emphasizing for many years, in print and in private communication, the conviction that the usual  notions of [[n-category]], [[infinity-category]] [[omega-category]] in [[higher category theory]] are __not__ naturally suited for describing

* [[extended cobordisms]] such as appearing in 

  * the [[generalized tangle hypothesis|tangle hypothesis]]

  * in [[FQFT|extended quantum field theory]]

* hierarchical systems such as appearing in

  * complex systems;

  * biology.

The point is essentially that the _directedness_ of morphisms and --- related to that --- the binary notion of [[source]] and [[target]] in categories and higher categories are notions alien to these contexts, which in applications have to and are essentially removed again in a second step by adding extra structure and requiring further properties, such as various monoidal structures and dualities, which allow to change the direction of morphisms, to collect objects together, etc.

In contrast to that, Baas pointed out that more naturally the above situations are thought of from the beginning in terms of hierarchies of what he calls _bonds_, where, quite generally, a bond is an object equipped with information of how a collection of sub-bonds sits inside it, _bound by the bond_.

A sketch of a generic such a situation of hierarchical bonds is a diagram 

$$
  \array{
     \beta_2 &&=&& \beta_2 && \beta_4
     \\
     \downarrow && && \downarrow & \swarrow
     \\
     b_1 &\to& B &\leftarrow& b_2
     \\
     \uparrow && \uparrow  && \uparrow 
     \\
     \beta_1 && b_3 && \beta_3
     \\
     && \uparrow
     \\
     && \beta_5
  }
$$

where a bond $B$ binds sub-bonds $b_1, b_2$ and $b_3$ which in turn bind sub-bonds $\beta_i$.

For instance $B$ might be an [[extended cobordism]] with three boundary components $b_1, b_2, b_3$ which in turn have pieces of boundary components $\beta_i$.

Nils Baas has made, in print and in private communication, suggestions for a formalization of such systems of hierarchical bonds and coined the term __hyperstructures__ for these. Some references are

* Nils A. Baas, _On Higher Order Structures_, [arXiv:1509.00403](http://arxiv.org/abs/1509.00403) (2015), 15 pp.

* Nils A. Baas, _Higher order architecture of collections of objects_, International Journal of General Systems vol. 44 (1), pp. 55-75, 2015. [arXiv:1409.0344](http://arxiv.org/abs/1409.0344)

* Nils A. Baas, N.C. Seeman and A. Stacey, _Synthesising topological links_, Journal of Mathematical Chemistry, vol. 53, pp. 183-199, 2015.

* Nils A. Baas, D.V. Fedorov, A.S. Jensen, K. Riisager, A.G. Volosniev and N.T. Zinner, _Higher-Order Brunnian Structures and Possible Physical Realizations_, Physics of Atomic Nuclei, vol. 77(3), pp. 336-343, 2014. [arXiv:1205.0746](http://arxiv.org/abs/1205.0746)

* Nils A. Baas, _New states of matter suggested by new topological structures_, International Journal of General Systems, vol. 42 (2), pp. 137-169, 2012. [arXiv:1012.2698](http://arxiv.org/abs/1012.2698)

* Nils A. Baas, _On structure and organization: an organizing principle_, International Journal of General Systems, vol. 42 (2), pp. 170-196, 2012. [arXiv:1201.6228](http://arxiv.org/abs/1201.6228)

* Nils A. Baas and N.C. Seeman, _On the chemical synthesis of new topological structures_, Journal of Mathematical Chemistry, vol. 50 (1), pp. 220-232, 2012.

* Nils A. Baas, _New structures in complex systems_, The European Physical Journal Special Topics, vol. 178 (1), pp. 25-44, 2010.

* Nils A. Baas, _Hyperstructures, Topology and Datasets_, Axiomathes, vol. 19 (3), pp. 281-295, 2009.

* Nils A. Baas, _Hyperstructures as Abstract Matter_, Advances in Complex Systems, vol. 9 (3), pp. 157-182, 2006.

* Nils A. Baas, A. Ehresmann and J.-P. Vanbremeersch, _Hyperstructures and Memory Evolutive Systems_, International Journal of General Systems, vol. 33 (5), pp. 553-568, 2004.

* Nils A. Baas, _Higher order cognitive structures and processes_. In _Toward a Science of Consciousness_, S.R. Hameroff, A.W.Kaszniak and A.C.Scott (editors), MIT Press, pp. 633-648, 1996.

* Nils A. Baas, _Hyper-structures as a tool in nanotechnology_, Nanobiology, vol. 3 (1), pp. 49-60, 1994.

#Remarks#

* The notion of replacing morphisms by _bonds_ is familiar and concretely realized at least in a hierarchy of depth 2 in the context of [[groupoidification]] and [[geometric function theory]], where morphisms are replaced by [[spans]]. Regarding these as [[cospans]] in the [[opposite category]] produces diagrams like the above sketch of a generic bond system. 

* Accordingly, the notion of [[multispan]] and [[multi-cospan]] may come close to exhibiting some crucial aspects of the idea that motivated the concept of hyperstructures.

#Blog discussion#

* David Corfield, [Category Theory and Biology](http://golem.ph.utexas.edu/category/2007/11/category_theory_and_biology.html)

  * The birth of the idea of [[multispans]] as a formalization of hyperstructures is mentioned in [this comment](http://golem.ph.utexas.edu/category/2007/11/category_theory_and_biology.html#c013165). 
Its application to the description of extended cobordisms and the [[generalized tangle hypothesis]] is topic of some thought chatted about at [this entry](http://golem.ph.utexas.edu/category/2008/05/hopkinslurie_on_baezdolan.html#c021486).

+--{.query}

[[Mike Shulman|Mike]]: Shouldn't we allow "oriented bonds" as well?  I am thinking of the case of, say, rings and modules, where a module $M$ that has right actions by rings $R$ and $S$ and a left action by $T$ should have $R,S,T$ as "sub-bonds" but with different "orientations."  And the "gluing" operation is tensor product, which only works if one module is a left module and the other is a right module.  This example also goes up in dimension, for instance modules over algebras over rings.  However, it seems that one would also needs this for cobordisms; aren't you only allowed to glue cobordisms along boundaries whose orientations match?

[[Urs Schreiber|Urs]]: right, the module example currently does not really fit yet. The reason seems to be that the would-be [[dagger category|dagger]] functor is not the identity on objects here, but sends objects to their opposites.

Concerning the cobordisms: in the cospan picture, every boundary component explicitly comes with its embedding into the cobordism. If two boundary components are equal as unembedded objects, then the pushout will automatically glue the corresponding cobordisms in the right way by identifying the components as embedded pieces. Do you see what I mean. Maybe I am mixed up about this.

[[Mike Shulman|Mike]]: Yes, the point is that a lot of these examples aren't really dagger at all, only [[compact closed category|compact closed]] (which I would prefer to call "autonomous").  My point about cobordisms has to do with orientations.  If $M$ and $N$ are two manifolds sharing a boundary component $B$, then I can glue them along it, but if they are _oriented_ then the gluing will only inherit an orientation if $M$'s boundary component is $B$ and $N$'s boundary component is $B^{op}$.  So it's just like rings; the category of oriented cobordisms is not dagger, only compact closed.  An oriented cobordism from $A$ to $B$ is not the same as an oriented cobordism from $B$ to $A$, but it is an oriented cobordism from $B^{op}$ to $A^{op}$.

[[Urs Schreiber|Urs]]: True. I am not sure about the best answer yet, but have thought about the following:

Suppose we have a span

$$
  A \leftarrow C \to B 
$$

and want to think of its index objects $A$ and $B$ to carry an orientation which gets reversed when we flip the legs around to 

$$
  B \leftarrow C \to A 
  \,.
$$

We might be able to emulate this within the setting described below by supposing that there are two different dummy objects $\bullet$ and $\circ$ around which behave at least to some extent like initial objects and that the original span was secretly really the multispan:

$$
  \array{
     && \bullet
     \\
     & \swarrow && \searrow
     \\
     A &\leftarrow& C &\to& B
     \\
     & \nwarrow && \nearrow
     \\
     && 
     \circ
  }
  \,.
$$

Now, if in this multispan we want to exchange the original two legs, we could for instance rotate the entire multispan by a half turn to get

$$
  \array{
     && \circ
     \\
     & \swarrow && \searrow
     \\
     B &\leftarrow& C &\to& A
     \\
     & \nwarrow && \nearrow
     \\
     && 
     \bullet
  }
  \,.
$$

This would introduce the desired orientation on objects, as the second multispan behaves like:

$$
  B^{op} \leftarrow C \to A^{op}
  \,.
$$

For this to work out as desired, we would of course have to concentrate on planar multispans and disallow identification of multispans that can be turned into each other by reflections at lines in the plane. 

_Mike_: It seems as though restricting to planar multispans would be quite a serious thing to do.

=--

***

#Laboratory section#

+--{.query}
[[Urs Schreiber|Urs]]: I am thinking about a way to formalize the idea of hyperstructure with a concrete application to extended quantum field theory and the Baez-Dolan hypothesis in mind. I would like to develop this in the following here on this page. If things work out as hoped for, this should eventually become an entry in its own right. If not, this should eventually be discarded. 

[[Ronnie Brown|Ronnie]] In this connection I would like to draw attention here to 


* D.W.Jones,  Polyhedral $T$-complexes, University of Wales PhD Thesis, 1984; published as  A general theory of polyhedral sets and their corresponding $T$-complexes, Diss. Math. 266, 1988. 

The idea here was to give expression to the notion of: what is wrong with pentagons? Or rhombic dodecahedra? as part of the basic models. Two major problems were solved: 

1. What should be the basic cells, and the polyhedral category?  

1. How should one orient or more the basic cells? 


The answer to the first question is given in terms of cells with polyhedral boundary and in which there is  a shellability condition. The answer to the second question is in terms of each cell has a marked face. This turns out to imply orientation, but is more of a homotopy condition than a homology condition, i.e. is stronger than the latter. There a relation to certain posets studied by Bjorner. 

On the other hand this theory is probably more group than category oriented, there is a tendency to imply inverses. 

The algebra comes in by defining _poly-$T$-complexes_, i.e. poly sets with [[thin element]]s.  


=--

##Idea##

**Motivation**

A _bond system_ or _hyperstructure_ as intended in the following should be

* a conglomerate of _cells_ each of which is equipped with a prescribed collection of _sub-cells_, which in turn have their prescribed collection of subcells, etc;

* such that whenever two such cell complexes coincide on any one part of their sub-cell complex, there exists a cell which can be regarded as gluing the two cells along this sub-cell complex.

The idea is hence akin to the [[geometric definition of higher category]], but differs in two crucial aspects:

1. there is no fixed choice of [[geometric shapes for higher structures]] (such as [[globe]]s, [[simplex|simplices]], [[cube]]s, etc.) out of which the entire structure consists, instead _all_ possible sub-cell complexes are admitted;

2. there is no notion of directionality imposed on the cell complexes, and in particular _no ordering_ on the sub-cells of a given cell, neither binary into source and target cells as in [[globe category|globular]] higher categories, nor linearly into indexed faces as in [[simplex category|simplicial]] higher categories.

The idea is that a hyperstructure is like a **$\infty$-[[dagger category|dagger]] [[infinity-category]]** but capturing this notion more directly than an $\infty$-category equipped with an $\infty$-dagger-operation would (which amounts to first introducing directionality only to remove it in a second step). Notice that in this context that categories of ordinary [[span]]s are always dagger-categories, where the dagger operation is nothing but the re-labelling of the legs of the span into source and target.  Hyperstructures in particular generalize categories of spans (as described below) and their special nature is supposed to intrinsically realize the dagger-structure.


**Formalization**

To formalize this,  the idea is to observe that every _cell_ with its complex of sub-cells should naturally form a [[partial order|poset]] under inclusions of sub-cells. Since for any collection of sub-cells which share a common collection of sub-sub-cells the result of gluing these sub-cells along their common sub-sub-cells should again be a sub-cell, this poset should be closed under [[colimit]]s.

Therefore a _bond system_ or _hyperstructure_ should in particular assign to every poset with colimits a collection to be interpreted as the collection of cells whose sub-cell structure is of the form given by the poset. Such an assignment would naturally allow to restrict any cell to any of its sub-cells along an inclusion of posets to obtain another cell, and to extend any cell to a cell with richer but degenerate sub-cell structure along a surjection of posets. This clearly suggests that the _bond system_ or _hyperstructure_ is a [[presheaf]] on the [[category]] of [[partial order|poset]]s with [[colimit]]s.

Given this, the **gluing condition** or **sewing condition** that for any collection of cells which match on a part of their sub-cell complex there exists a cell obtained by gluing the cells along their common sub-cells can be formulated in a way analogous to the horn-filling condition in a [[Kan complex]] by requiring that the obvious map from the collection of cells which have the right shape of being glued cells to the collection of cells that admit gluing is an [[epimorphism]].


**Examples**

The archetypical example of a _bond system_ or _hyperstructure_ as intended in the following is supposed to be the collection $MultiCoSpans(C)$ of [[multispan|multi co-span]]s in a category $C$ with colimits. Since a [[multispan|multi co-span]] in $C$ is supposed to be nothing but the image of a poset in $C$, this means that the _bond structure_ of [[multispan|multi co-span]]s should be the presheaf on $Posets$ [[representable functor|represented]] by $C$. This does satisfy the _gluing condition_ in that for all multi-cospans which coincide in parts there exists in $C$ the colimit over their joint diagram. For ordinary [[cospan]]s this is supposed to reproduce the ordinary composition of [[cospan]]s by pushout over a joint leg.


**The hyperstructure of hyperstructures**

As there is a canonical notion of homo[[morphism]]s of 
[[presheaf|presheaves]] we naturally obtain a [[category]] of _bond systems_ or _hyperstructures_. By the above example this in turn naturally induces a hyperstructure of hyperstructures consisting of the multi-cospans in the category of presheaves on posets.


This allows then finally to formalize one of the situations motivating the notion of hyperstructure in the first place, that of [[FQFT|extended quantum field theory]]: for instance for _topological_ QFT this is expected to be a morphism (or more general span) of hyperstructures
$$
  \array{
     ExtendedCobordisms :=
     MultiCoSpans(Top) &\to& MultiSpans(S)
     =:  
     \infty Vect_S
  }
  \,,
$$
where multi-cospans in the category [[Top]] are thought of as modelling [[extended cobordism]]s as described for instance at [[Cospans in Algebraic Topology]], while multi-spans in some suitable category $S$ (multi co-spans in the [[opposite category]] $S^{op}$) are thought of as modelling morphisms between higher vector spaces as in [[groupoidification]].




##Definitions##


First recall some basics of [[partial order|poset]]s to fix our notation.

We write $2 = \{\bottom \to \top\}$ for the category with two objects and a single nontrivial morphism between them. 
Recall that a [[partial order|poset]] is a [[enriched category|category enriched]] over $(2,\otimes, I = \top)$, where the canonical tensor product on $2$ is has tensor unit $\top$ and $\bottom \otimes \bottom = \bottom$.


+-- {: .un_defn}
###### Definition

Write $Posets$ for the (1-)category of small [[partial order|poset]]s
and $\overline{Posets} \subset Posets$ for the sub-category of small posets with all [[colimit]]s.

=--

Recall that for $D$ a poset the [[Yoneda embedding]] 
$Y_D : D \to 2^{D^{op}}$ is the free cocompletion of $D$ and notice that for every poset $D$ also the [[presheaf]] category $2^{D^{op}}$ is again a poset. This yields a functor

$$
  \overline{(-)} := Y  : Posets \to \overline{Posets}
$$

which sends posets to their free cocompletion.

+-- {: .un_defn}
###### Definition

A **bond system** or **hyperstructure** $K$ is 

* a [[Set]]-valued [[presheaf]] on $\overline{Posets}$
$$
  K : \overline{Posets}^{op} \to Set
$$

* which satisfies the following **gluing condition** or **sewing condition**: for every diagram
$$
  D_1 \leftarrow D_{glue} \to D_2
$$
in $\overline{Posets}$ the unique morphism $\phi$
$$
  \array{
     K(\overline{D_1 \sqcup_{D_{glue}} D_2} )
     &&&\stackrel{K(Y)}{\to}& K(D_1 \sqcup_{D_{glue}} D_2)
     \\
     & \searrow^{\phi} &&& \downarrow
     \\
     &&
     K(D_1) \times_{K(D_{glue})} D(D_2) &\to& K(D_2)
     \\
     \downarrow^{K(Y)}
     &&
     \downarrow && \downarrow
     \\
     K(D_1 \sqcup_{D_{glue}} D_2)
     &\to&
     K(D_1) &\to& K(D_{glue})
  }
$$
is an [[epimorphism]].

For $\Gamma$ a hyperstructure and $D \in \overline{Posets}$ we call $\Gamma(D)$ the collection 
of **cell**s of $\Gamma$ of **shape** $D$.

=--


+-- {: .un_defn}
###### Definition

For $C$ a category with colimits let
$$
  MultiCoSpan(C) := Cat(-,C) : \overline{Posets} \to Set
$$
be the presheaf which assigns to any poset $D$ the set $Cat(D,C) = Funct(D,C)$ of [[functor]]s  from $D$ to $C$.

=--

+-- {: .un_lemma }
###### Lemma

For $C$ a category with colimits,
$MultiCoSpan(C)$ is a bond structure.

=--

+-- {: .proof}
###### Proof

We have to check the sewing condition. First notice that for $K := Cat(-,C)_\sim$ we have a natural bijection
$$
  K(D_1) \times_{K(D_{glue})} K(D_2)
  \simeq
  K(D_1 \sqcup_{D_{glue}} D_2)
  \,.
$$
Then recall from the discussion at [[Yoneda embedding]] that every functor $F \in K(D_1 \sqcup_{D_{glue}} D_2)$,
$F : D_1 \sqcup_{D_{glue}} D_2 \to C$ canonically extends to a functor $\hat F \in K(\overline{D_1 \sqcup_{D_{glue}} D_2})$ given by the [[end|coend]]
$$
  \hat F(-) = \int^{d \in D_1 \sqcup_{D_{glue}} D_2}
    hom(d,-)\cdot F(d)
$$
in that $\phi = K(Y_{D_1 \sqcup_{D_{glue}} D_2} ) : 
\hat F \mapsto F$. This says that $\phi$ is epi.

=--

+-- {: .un_defn}
###### Definition

For $C$ a category with colimits we call 
the cells of $MultiCoSpans(C)$ the **multi co-span**s in
$C$, call all of $MultiCoSpans(C)$ the 
**hyperstructure of multi-cospans** in $C$. Dually,
for $C^{op}$ a category with colimits we 
write
$$
  MultiSpan(C) := MultiCoSpan(C^{op})
$$
for the **hyperstructure of multi-spans** in $C$.
=--

+-- {: .un_defn}
###### Definition

We write
$$
  Hyperstructures := MultiCoSpans(Set^{\overline{Posets}^{op}})
$$
for the **hyperstructure of hyperstructures**.

=--


=--


##Examples##

### Composition of ordinary cospans ###

The above general definition in particular reproduces the ordinary composition of [[cospan]]s.

Let $C$ be a category with colimits.
The cells of the hyperstructure $MultiCoSpan(C)$
of shape the [[pullback]] poset
$$
  D = 
  \left\{
  \array{
     && top
    \\
    & \nearrow && \nwarrow
    \\
    a &&&& b
  }
  \right\}
$$
are the ordinary [[cospan]]s $c \in MultiCoSpan(C)(D)$ in $C$. Let $D_{glue} = pt = \{\bullet\}$ and consider the functors
$\alpha : D_{glue} \to D : \bullet \mapsto a$ and
$\beta : D_{glue} \to D : \bullet \mapsto b$ in the diagram
$$
  D_1 := D \stackrel{\beta}{\leftarrow}
  D_{glue}
  \stackrel{\alpha}{\to}
  D =: D_2 
$$
as above.

Then 
$$
  D_1 \sqcup_{D_{glue}} D_2 =
  \left\{
    \array{
       && t_1 &&&& t_2
       \\
       & \nearrow && \nwarrow && \nearrow && \nwarrow
       \\
       a &&&& b &&&& c
    }
  \right\}
$$
and
$MultiCoSpans(C)(D) \times_{MultiCoSpans(C)(D_{glue})}  
 MultiCoSpans(C)(D) 
 \simeq 
  MultiCoSpans(C)(D_1 \sqcup_{D_{glue}} D_2)
 $ 
is the collection of pullback-diagrams in $C$ which share one leg. The cocompletion of $D_1 \sqcup_{D_{glue}} D_2$ looks in parts like
$$
  \overline{D_1 \sqcup_{D_{glue}} D_2}
  =
  \left\{
    \array{
       &&&& \top = t_1 \sqcup t_2
       \\
       &&& \nearrow && \nwarrow
       \\
       && t_1 &&\cdots&& t_2
       \\
       & \nearrow &\uparrow& \nwarrow && \nearrow 
       &\uparrow& \nwarrow
       \\
       a &\rightarrow& a \sqcup b& \leftarrow& b 
       &\rightarrow& b \sqcup c& \leftarrow& c
       \\
       & \nwarrow &&& \uparrow &&& \nearrow
       \\
       &&&& \bottom
    }
  \right\}
  \,,
$$
where the important point is that it contains the terminal object $\top$. Given any two cospans in $C$ that coincide on one foot

$$
  F(D)
  =
  \left\{
  \array{
    && F(t_1)
    \\
    & \nearrow && \nwarrow
    \\
    F(a) &&&& F(b)=F'(b)
  }
  \right\}
  \;\;\;\;\;\;\;\;
  F'(D)
  =
  \left\{
  \array{
    && F'(t_2)
    \\
    & \nearrow && \nwarrow
    \\
    F(b)= F'(b) &&&& F'(c)
  }
  \right\}
$$ 

they induce the element

$$
  F \sqcup_{b} F'(D_1 \sqcup_{D_{glue}} D_2)
  =
  \left\{
  \array{
    && F(t_1) &&&& F'(t_2)
    \\
    & \nearrow && \nwarrow && \nearrow && \nwarrow
    \\
    F(a) &&&& F(b)=F'(b) &&&& F'(c)
  }
  \right\}
$$

whose lift to $\overline{D_1 \sqcup_{D_{glue}} D_2}$
is given on $\top$ by

$$
 \begin{aligned}
  \widehat{F \sqcup_b F'}(\top)
  &=
  \int^{d \in D_1 \sqcup_{D_{glue}} D_2}
  hom(d,\top)\cdot (F \sqcup_b F')(d)
  \\
  &=
  \int^{d \in D_1 \sqcup_{D_{glue}} D_2}
  (F \sqcup_b F')(d)  
  \\
  &=
  colim_{d \in D_1 \sqcup_{D_{glue}} D_2} 
  (F \sqcup_b F')(d)
 \end{aligned}
  \,.
$$

This is indeed the ordinary composite of the two [[cospan]]s $F$ and $F'$.

+--{.query}
[[Mike Shulman|Mike]]: It seems to me that this definition doesn't contain enough information.  Yes, the ordinary composite of the two cospans is _one_ lift to $\overline{D_1 \sqcup_{D_{glue}} D_2}$, but there are plenty of other lifts, and there doesn't seem to be anything in the presheaf you've described that can characterize that particular lift as the "correct" gluing (in particular, its universal property in $C$ seems to have been forgotten).

[[Urs Schreiber|Urs]]: I was thinking of next defining "non-flabby" $MultiCoSpans(C)$ as the presheaf of co-continuous functors from a given poset into $C$, so that the above lifts are the only ones (right?). Then I want to say that a morphism of hyperstructures from the bordism hyperstructure defined below to a non-flabby multicospan hyperstructure is fixed by its value on the point if it regards the interval as weakly equivalent to the point.

I am thinking of the difference between the above "flabby" version and the non-flabby version as the difference between general Kan complexes and those that are the nerve of an $n$-groupoid for which above $n$ the fillers are unique.

[[Mike Shulman|Mike]]: Using cocontinuous functors will make the lifts unique, at least up to isomorphism.  It doesn't seem that you've included any information about isomorphisms, but perhaps that can be remedied with higher spans or with presheaves of groupoids or categories.  But I don't see the "flabby" version as very much like a Kan complex; in a Kan complex the fillers of horns _are_ unique up to homotopy, because of the higher-dimensional horn-filling conditions, but I don't see anything like that going on here.

[[Urs Schreiber|Urs]]: But we have these higher filling conditions here automatically, too: if there are two different multispans which glue two given ones, they share these two given ones and can be glued along them. This should say that any two fillers are themselves connected by a filler.

_Mike_: It seems as though if you're considering two multispans to be equivalent if they can be connected by a filler, and your horn-filling conditions stipulate that all fillers exist, then your structure is fairly trivial: everything is equivalent to everything else.

=--

### Bordism hyperstructure ###

Let 
$$
  I :=
  \left(
  \array{
    && [0,1]
    \\
    & {}^{in}\nearrow && \nwarrow^{out}
    \\
    pt &&&& pt
  }
  \right)
$$
be the standard [[interval object]] in [[Top]], regarded as a [[cospan]].

+-- {: .un_defn}
###### Definition

Let $ExtendedCobordisms$, the **hyperstructure of extended cobordisms**, be the smallest sub-hyperstructure of $MultiCospans(Top)$ which contains the interval object $I$ and is closed under cartesian product $\times$ of multi-cospans in $Top$.

=--

+--{.query}
[[Mike Shulman|Mike]]: In order for that to make sense, you need there to be a smallest sub-hyperstructure such that (blah).  But I don't see any reason for that to exist; the intersection of sub-hyperstructures need not be a hyperstructure.  Even in a simplicial set the intersection of sub-Kan-complexes need not be a Kan complex; if $X$ contains one filler for a given horn and $Y$ contains a different filler, then $X\cap Y$ may contain no filler at all.

[[Urs Schreiber|Urs]]: I agree that it is not a priori clear that some smallest hyperstructure with a given property exists. But I am not sure that I see what this has to do with intersections. Shouldn't we we be looking at _inclusions_?

But in the particular case at hand, it feels that this smallest hyperstructure should certainly exist, no? I should think about formalizing it, but heuristically it should be given by the colimit over inclusions of the following steps for building it:

* start with the interval cospans and take all ways to glue the interval with copies of itself.

1. then include for everey multi-cospan obtained so far also its product with the interval cospans;

2. then form all composites of multi-cospans obtained so far

3. then continue with 1. .


_Mike_: In general, there are two ways to construct the smallest sub-widget of $X$ such that (blah):

* Take the intersection of all sub-widgets of $X$ such that (blah).
* Start with (blah) and close it up, iteratively, under all the operations that define a sub-widget.

Usually, if one works the the other does too.  Occasionally one fails where the other succeeds due to set-theoretic technicalities.  But here I think the problem is intrinsic and will rear its head wearing a different mask in either case.

It definitely does not feel to me as though the smallest hyperstructure should exist.  The problem with your proposal is when you say "form all composites."  Since composites are not an _operation_, this can't mean "for any $x$ and $y$ already in our sub-hyperstructure, add in _the_ composite of $x$ and $y$."  If we just arbitrarily pick some particular composite of $x$ and $y$ to add, then there might be other sub-hyperstructure that chose a different composite, so what we end up with won't be the smallest (in the "minim<i>um</i>" sense) sub-hyperstructure such that (blah).  We might be able to construct a minim<i>al</i> sub-hyperstructure, but it wouldn't be uniquely determined, so we couldn't talk about [[generalized the|the]] hyperstructure of extended cobordisms.

_Toby_:  And then, you might have to rely on Zorn\'s Lemma (the [[axiom of choice]]) to prove that even such a minimal structure exists!
=--

This means that multi-cospans in $ExtendedCobordisms$ arise from iteratively tensoring with the interval and forming pushouts, which amounts to foming [[co-span co-trace]]s.

For instance with the interval $I$ there is also the circle $S^1$ in $ExtendedCobordisms$, arising as the composition of the interval with itself over both legs
$$
  \array{
    && I
    \\
    & \nearrow &\downarrow& \nwarrow
    \\
    pt &&S^1&& pt 
    \\
    & \searrow &\uparrow& \swarrow
    \\
    && I
  }
  \,.
$$

With the circle there is then also the cylinder

$$
  \left(
  \array{
    && S^1
    \\
    & \nearrow && \nwarrow
    \\
    \emptyset &&&& \emptyset
  }
  \right)
  \times
  \left(
  \array{
    && I
    \\
    & {}^{in}\nearrow && \nwarrow^{out}
    \\
    pt &&&& pt
  }
  \right)
  =
  \left(
  \array{
    && S^1 \times I 
    \\
    & {}^{in}\nearrow && \nwarrow^{out}
    \\
    S^1 &&&& S^1
  }
  \right)  
  \,.
$$

With the cylinder there is also the torus

$$
  \array{
    && S^1 \times I
    \\
    & \nearrow &\downarrow& \nwarrow
    \\
    S^1 &&T^2&& S^1 
    \\
    & \searrow &\uparrow& \swarrow
    \\
    && S^1 \times I
  }
  \,.
$$

Etc. Then there are the extended cobordisms proper, which have deeper layers of sub-cells. For instance the product of the interval with itself gives the disk regarded as an extended cobordisms

$$
  \left(
  \array{
    && I
    \\
    & {}^{in}\nearrow && \nwarrow^{out}
    \\
    pt &&&& pt
  }
  \right)
  \times
  \left(
  \array{
    && I
    \\
    & {}^{in}\nearrow && \nwarrow^{out}
    \\
    pt &&&& pt
  }
  \right)
  =
  \left(
  \array{
    pt &\to& I &\leftarrow& pt
    \\
    \downarrow && \downarrow && \downarrow
    \\
    I &\to&  I^2  &\leftarrow& I
    \\
    \uparrow && \uparrow && \uparrow
    \\
    pt &\to& I &\leftarrow& pt
  }
  \right)  
$$

with four 1-dimensional and four 0-dimensional boundary components.

+--{.query}
[[Mike Shulman|Mike]]: I'm not sure if this is intentional or not, because I don't know what your goal is, but even if the definition makes sense, these "extended cobordisms" include things that aren't very manifold-like.  For instance, if you glue the interval-with-endpoints to another copy of the interval-with-endpoints along one of the endpoints, you get a cell like
$$
    \array{
       &&&& [0,2]
       \\
       &&& \nearrow && \nwarrow
       \\
       && [0,1] &&\cdots&& [1,2]
       \\
       & \nearrow &\uparrow& \nwarrow && \nearrow 
       &\uparrow& \nwarrow
       \\
       \{0\} &\rightarrow& \{0,1\}& \leftarrow& \{1\}
       &\rightarrow& \{1,2\}& \leftarrow& \{2\}
       \\
       & \nwarrow &&& \uparrow &&& \nearrow
       \\
       &&&& \bottom
    }
$$
and now restricting along a suitable inclusion of posets, we get
$$ \array{ [0,2] \\ \uparrow \\ \{1\}}$$
and we can now glue this to another interval along the point $1$, obtaining a wedge of three copies of the interval.  I think the things you glue along should somehow be "canceled out" and no longer appear as sub-cells of the glued result (this is certainly what happens in the case of modules).

[[Urs Schreiber|Urs]]: true. I need to think about a nice way to formalize such a cancellation.

[[Z|Z]]: I'd like to know more about composition of bonds as described on p.8 of "Higher Order Architecture of Collections of Objects" (Nils Baas). Can someone please clarify the rules on this page? 
=--

[[!redirects hyperstructural]]
[[!redirects hyperstructures]]