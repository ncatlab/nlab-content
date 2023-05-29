+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _homotopy coherent nerve_ (also called _simplicial nerve_) of a [[simplicially enriched category]] is a [[simplicial set]] which includes information about all the higher homotopies present in the hom-spaces.  It generalizes the ordinary [[nerve]] of an ordinary [[category]].

The homotopy coherent nerve operation

$$
  N \colon sSet\text{-}Cat \longrightarrow sSet
  \,.
$$

is induced, by the general machinery of [[nerve and realization]], by a  [[cosimplicial object|cosimplicial]] [[simplicially enriched category]], namely a [[functor]]

$$
  \Delta \longrightarrow sSet\text{-}Cat
$$

from the [[simplex category]] to the category of 
[[simplicially enriched categories]] which regards each
$n$-[[simplex]] as a [[sSet]]-[[enriched category]]
with $n$ objects analogous to how the [[orientals]]
regard the $n$-simplex as an [[strict omega-category|strict $n$-category]].



## Definitions

### The cosimplicial $sSet$-category

We here describe the cosimplicial [[sSet]]-[[enriched category]] 

$$
  S \colon \Delta \longrightarrow sSet\text{-}Cat
$$

that induces the homotopy coherent nerve.

### A categorical description 

Recall that a [[graph]], $\Gamma$, is _[[reflexive graph|reflexive]]_ if for each [[vertex]] $v$ it is equipped with a (specified) [[edge]] $v \to v$. Similarly, a **reflexive [[directed graph]]** has a specified identity edge $i_X \colon X \to X$ on each object (vertex) $X$.

The [[free category]] on a reflexive directed graph has 

* as [[objects]] the [[vertices]] of the graph,

* [[identity morphisms]] corresponding to the identity edges, 

* non-identity morphisms consisting of sequences of non-identity edges. 

The [[free category]]-construction extends to a [[functor]]

$$
  F
  \;\colon\;
  ReflxDGraph \longrightarrow Cat 
$$
and as such 
is [[left adjoint]] to the [[forgetful functor]]

$$
  F
  \;\colon\;
  Cat \longrightarrow ReflxDGraph 
  \,.
$$

Hence the composite $G = F U \colon Cat\to Cat$ constitutes a [[comonad]] on $Cat$. 

The [[simplicial resolution]] of this comonad gives an augmented simplicial [[endofunctor]] $S \colon \Delta \longrightarrow sSet\text{-}Cat$ with natural augmentation $S\to Id$, and which is a [[cofibrant replacement]]-construction in the [[Bergner model structure]] on $sSet-Cat$ ("model structure for simplicially enriched categories"). 

\begin{remark}
Some *words of caution*, as always with simplicial resolutions, there are two conventions which differ by being the opposite simplicial object of each other.  In the original paper, Cordier uses a different one of these conventions from some of the other sources mentioned here. A similar problem occurs in the following combinatorial description as some sources use 'reverse inclusion' where others just use 'inclusion' for the partial order on the poset. This corresponds more or less exactly to the distinction between 'op-lax' and 'lax' functors in the theory of 2-categories. 

Because of this, it is always important to test the definition being used on a simple example, $[2]$ will do, before commiting to the use of any specific formulae. We will see this again in another Remark later on in this entry.
\end{remark}


### A combinatorial description

For $[n]$ the finite [[ordinal number|ordinal]] $[n] \coloneqq \{0 \lt 1 \lt  \cdots \lt n\}$ and for $\Delta[n]$ be  standard [[simplicial set|simplicial]] [[simplex|$n$-simplex]], define the [[sSet-enriched category]] $S[n]$ as follows:

* the [[objects]] of $S[n]$ are $\{0,1, \cdots, n\}$;

* the [[hom-objects]] $S[n]_{i,j} \in sSet$ for $i, j \in \{0,1,\cdots, n\}$ are the [[nerves]]

  $$
    S[n](i,j) \coloneqq N(P_{i,j})
  $$ 

  of the [[poset]] $P_{i,j}$ which is equivalently

  1. the [[poset]] of [[subsets]] of $[i,j]$ that contain both $i$ and $j$ (so in particular if $i \gt j$ then $P(i,j)$ is [[empty set|empty]] and hence so is its nerve) with the partial order is given by reverse inclusion.

   1. the poset of [[path category|paths]] in $[n]$ that start at $i$ and finish at $j$ (hence is empty if $i\gt j$), the order relation is given by 'subdivision', i.e. path $a$ is less than path $b$ in $P(i,j)$ if $a$ visits all the vertices that $b$ does ... and perhaps some others as well.

      Of course, the way you go between the two descriptions is that a path corresponds to the set of vertices it visits and _vice versa_.


Notice that the simplicial set $N(P_{i,j})$ is [[isomorphism|isomorphic]] to the $j-i-1$ cube in $sSet$:

$$
  N(P_{i,j}) = (\Delta[1])^{\times (j-i-1)}
  \,.
$$ 

Under this isomorphism for instance the vertex $(0,0,1,0,1) \in (\Delta[1])^{\times (j-i-1)}$ corresponds to the subset $\{i,i+3,i+5,j\} \subset [i,j]$ and to the path $i \to i+3 \to i+5 \to j=i+6$. 

(We will look at an example after this definition.)

* the [[composition]] operation on hom-objects

  $$
    \circ_{i,j,k} : S[n]_{i,j} \times S[n]_{j,k} \to S[n]_{i,k}
  $$

  is induced by 'concatenation of the corresponding paths' and thus essentially by union of the sets involved.

+-- {: .num_remark}
###### Remark

The choice to order paths by reverse inclusion agrees with constructions such as the [[Duskin nerve]]. However, the other convention where they are ordered by inclusion also appears in the literature, such as [[Higher Topos Theory]] definition 1.1.5.1., and corresponds to the convention used in the original paper by Cordier (see earlier Remark). The resulting theory is more or less equivalent in as much as the results true when using one convention have analogous results when using the other.

=--


### The homotopy coherent nerve

The **homotopy coherent nerve** functor

$$
  N 
    \coloneqq 
  Hom_{sSet Cat}(S[\bullet],-) 
  \colon sSet Cat \longrightarrow sSet
$$

is the [[nerve]] defined by the [[cosimplicial object|cosimplicial]] [[sSet-enriched category]] $S \colon \Delta \to sSet Cat$ defined above.

For $C \in sSet Cat$ any [[sSet-enriched category]], the homotopy coherent nerve  $N(C)$ is the [[simplicial set]] uniquely characterized as giving a [[natural isomorphism]] of the form

$$ 
  Hom_{SSet}\big(\Delta[n], N(C)\big) 
   \;\simrq\; 
  Hom_{SSet Cat}\big(S[n], C\big)
  \,.
$$

By the general logic of [[nerve and realization]], this functor has a [[left adjoint]]

$$
  S(-) \colon SSet \to SSet Cat
$$

the **realization** functor given by the [[coend]] formula

$$
  S(X) 
  \coloneqq 
  \int^{[n] \in \Delta} X_n \cdot S[n]
  \,,
$$

also known as the operation of *[[rigidification of quasi-categories]]*.

This functor does extend the functor $S : \Delta \to sSet Cat$  in that there is a canonical isomorphism

$$
  S(\Delta[n]) \cong S[n]
$$

and hence may consistently be named $S$.



## Examples and illustrations

### For the cosimplicial $sSet$-category {#IllustratOfCosimpSSetCat}

We illustrate here the nature of the cosimplicial $sSet$-category $S : [n] \mapsto S[n]$, viewed from the combinatoiral viewpoint above.

We will examine the lowest dimensional cases. 

For $n = 0$ there is nothing of note.

For $n = 1$ we have that

$$
  P_{0,1} = \left\{ (0,1) \right\} = \Delta[0] = \Delta[1]^0
$$

is the poset with a single object.


For $n = 2$, there are unique paths in $[2]$ from $[0]$ to $[1]$, and $[1]$ to $[2]$, so the corresponding homs in $S[2]$ are copies of $\Delta[0]$ (or, if you prefer, of $\Delta[1]^0$!). Things are slightly more interesting for $S[2](0,2)$. Looking at this from the 'subsets' viewpoint, as above, there clearly are two subsets of $\{0,1,2\}$ containing both $0$ and $2$, one corresponds to the direct route in $[2]$ from $0$ to $2$, the other goes via $1$ so is $0\to 1\to 2$. 

$$
  P_{0,2} = 
  \left\{
    (0,1,2) \to (0,2)
  \right\}
  = 
  \Delta[1]
  \,,
$$

so in $S[2](0,2)$, there is a 1-simplex $k$ starting at $\{0,1,2\}$ and ending at $\{0,2\}$.  

\begin{center}\begin{xymatrix} &1\ar[dr]^{(1,2)}&\\
 0\ar[ur]^{(0,1)} \ar[rr]_{(0,2)}\ar@{}[rr]<3ex>^{\Large{\Downarrow} (0,1,2)}&&2\end{xymatrix}\end{center}


Since $(0,1,2)$ is a product of $(0,1)$ and $(1,2)$, this simplex can also be depicted as $(1,2) \cdot (0,1) \Rightarrow (0,2)$.


Everything else, in higher dimensions, is degenerate, so $S[2](0,2)\cong \Delta[1]$. Sometimes it is useful to think of this 1-simplex as 'rewriting' the direct path to that via 1, all this happening in the free category on the underlying graph of the poset $[2]$. (The construction of $S[n]$ in general has a nice interpretation in terms of higher dimensional [[rewriting]]. This can be given using the language of [[polygraph]]s or [[computad]]s.)

In this example there are no significant compositions. To see examples of those, you need to look at $n = 3$. In $S[3]$, the simplicial hom-sets $S[3](i,j)$ for $(i,j) \neq (0,3)$, can all be analysed by the same sort of argument to the above.  The new features occur in $S[3](0,3)$.  The vertices of this simplicial set are the subsets 
corresponding to the direct path $0\to 3$ and then the three others. Rewriting the direct path can be done in two immediate ways, to go via the left or via the right route. Each of these can be 'rewritten' to give the longest path /  largest subset.  There is also, of course, an inclusion of the smallest to the largest of these, so that in total the poset here looks like:

$$
  P_{0,3}
  =
  \left\{
    \array{
       \{0,1,2,3\}&\rightarrow & \{0,1,3\}
       \\  
       \downarrow & \searrow &\downarrow\\
       \{0,2,3\}&\rightarrow &\{0,3\}
     }
  \right\}
  =
  \Delta[1]^{\times 2}
  \,.
$$

In addition, there will be 2-simplexes filling the two triangles, coming from the chains $\{0,1,2,3\}\subset \{0,1,3\}\subset \{0,3\}$ and $\{0,1,2,3\}\subset \{0,2,3\}\subset \{0,3\}$ in the poset. 

$$
  \array{
    & \nearrow && \searrow^{\mathrlap{\{0,3\}}}
    \\
    & & \Uparrow
    \\
    0  &&\stackrel{\{0,1,3\}}{\to}&& 3
    \\
    && \Uparrow
    \\
    & \searrow && \nearrow_{\mathrlap{\{0,1,2,3\}}}
  }
  \;\;\;\;\;
  \;\;\;\;\;
  \;\;\;\;\;
  \,,
  \;\;\;\;\;
  \;\;\;\;\;
  \;\;\;\;\;
  \array{
    & \nearrow && \searrow^{\mathrlap{\{0,3\}}}
    \\
    & & \Uparrow
    \\
    0  &&\stackrel{\{0,2,3\}}{\to}&& 3
    \\
    && \Uparrow
    \\
    & \searrow && \nearrow_{\mathrlap{\{0,1,2,3\}}}
  }
  \,.
$$



We thus get $S[3](0,3) \cong \Delta[1]^2$, a square. 

The composition maps

$$S[3](1,3)\times S[3](0,1)\to S[3](0,3)$$

and similarly for the one with 1 replaced by 2, *are* now fairly obvious.  



For $n = 4$, the corresponding diagram for $S[4](0,4)$ gives a cube 
but here there is an interesting feature.  

Five of the six faces of the cube $|N(P_{0,4})|$ correspond to the  associativity of composition of triples of composable morphisms in $[4]$. These correspond to the 5 faces of the 4-simplex $\Delta[4]$, as depicted for instance at [[oriental]] and at [[monoidal category]].

But the cube has one more face

$$
  \array{
    (0,1,2,3,4) &\to& (0,1,2,4)
    \\
    \downarrow &\searrow& \downarrow
    \\
    (0,2,3,4) &\to& (0,2,4)
  }
$$

which does not correspond to associativity: instead, this encodes the [[exchange law]]


$$
  \array{
    && 1 &&&& 3
    \\
    & \nearrow &\Downarrow& \searrow && \nearrow && \searrow
    \\
    0 &&\to&& 2 &&  && 4
    \\
    &&  &&&& 3
    \\
    & && && \nearrow &\Downarrow& \searrow
    \\
    0 &&\to&& 2 && \to && 4  
  }
  \;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;
  \array{
    && 1 &&&& 3
    \\
    & \nearrow && \searrow && \nearrow &\Downarrow& \searrow
    \\
    0 &&&& 2 && \to && 4
    \\
    && 1 &&&& 
    \\
    & \nearrow &\Downarrow& \searrow &&  && 
    \\
    0 &&\to && 2 && \to && 4  
  }
$$

or, if preferred, to the fact that

$$S[4](2,4)\times S[4](0,2)\to S[4](0,4)$$

is to be a simplicial map.




A similar phenomenon occurs in higher dimensions.  There are two 'extra faces' in $S[5](0,5)$, and so on.

### For other simplicial sets

The description of $S[n]$ works more generally for the [[nerve]] of a [[poset]]. Explicitly, if $P$ is a poset, $S(NP)$ is isomorphic to the simplicially enriched category with the structure

   * The objects of $S(NP)$ are the elements of $P$
   * The [[hom-object]] $S(NP)(x,y)$ is the nerve of the poset of [[chains]] $S \subseteq P$ with $\min(S) = x$ and $\max(S) = y$, ordered by reverse inclusion
   * Composition is given by taking unions


The simplicially enriched categories constructed from spheres and [[inner horns]] also have simple descriptions.

For $(i,j) \neq (0,n)$, the hom-objects are the same as the ambient simplex: $S(\Lambda^n_k)(i,j) = S(\partial \Delta^n)(i,j) = S(\Delta^n)(i,j)$.

For the remaining hom-object, while $S(\Delta^n)(0,n) \cong \square^{n-1}$ is the $(n-1)$-cube, $S(\partial \Delta^n)(0,n) = \partial \square^{n-1}$ is the boundary, and $S(\Lambda^n_k)(0,n)$ further omits the corresponding face.

To see this, observe that the nondegenerate simplices of $S(\Delta^n)(0,n)$ are either decomposable (i.e. the product of two or more simplices from other hom-sets) or are the image of a top simplex of $S(\Delta^m)(0,m) \to S(\Delta^n)(0,n)$ for some monomorphism $\Delta^m \to \Delta^n$ preserving top and bottom elements, depending on whether the simplex contains the top vertex $(0,n)$.

Thus, the decomposable faces of $S(\Delta^n)(0,n)$ are the ones omitting the top vertex $(0,n)$, and the remaining faces come from inner faces $\Delta^{n-1} \to \Delta^n$.


### For the homotopy coherent nerve

*  Any [[2-category]] gives a simplicially enriched category using the embedding of [[Cat]] into [[sSet]] via the usual [[nerve]] functor. The homotopy coherent nerve of a 2-category considered in this way is, sometimes, called the [[geometric nerve]] of the 2-category. The [[Duskin nerve]] of a [[bicategory]] is an extension of this construction. 

   A particular case of this nerve is the nerve of a [[2-group]] [[delooping|considered as]] a 2-category.


## Properties {#Properties}

* If $C \in sSet Cat$ is such that all [[hom-object]]s $C(x,y) \in sSet$ are [[Kan complex]]es, then the homotopy coherent nerve $N(C)$ is a [[weak Kan complex]]/[[quasi-category]].

  If $f : C \to D$ is a morphism of such Kan-complex enriched categories which is a weak equivalence (in the [[model structure on sSet-categories]]) in that

  * the induced functor 

    $$
      Ho(f) : Ho(C) \to H(D)
    $$
     
    on the ordinary underlying [[homotopy category of an (infinity,1)-category|homotopy categories]] (obtained by taking hom-wise connected component sets) is [[essentially surjective functor|essentially surjective]] 

  * its component on each hom-object

    $$
      f_{x,y} : C(x,y) \to D(f(x),f(y))
    $$

    is a [[homotopy equivalence]],

  then its homotopy coherent nerve

  $$
    N(f) : N(C) \to N(C)
  $$

  is a [[model structure for quasi-categories|weak equivalence of]] [[quasi-categories]].

  We may think of [[category]] $\Delta[n]$ trivially as a simplicially enriched category. In the [[model structure on sSet-categories]] the object $S[n]$ is a cofibrant replacement of $\Delta[n]$. And Kan-complex enriched categories are fibrant. So on these the homotopy coherent nerve is given by the [[derived hom-space]] functor

  $$
    N(C) = \mathbb{R}Hom(\Delta[\bullet], C)
    \,.
  $$

## Related concepts

### Comonadic resolution
(To be edited)

The use of $S[A]$, above, extends that given at the start of this page. Here $S$ is related  to the [[left adjoint]] of the homotopy coherent nerve, but is defined using a [[comonadic resolution]].  The [[comonad]] comes from the adjunction between small categories and directed graphs with distinguished 'unit' loops. The 'forgetful' part of the adjunction forgets the composition in the category, but remembers that the identity arrows are special. The left adjoint /  'free' part of the adjunction takes a directed graph (with distinguished 'identity' loops, and forms the free category on the non-identity arrows. As usual, we can form a [[comonad]] from this  and hence form a functorial [[simplicial resolution]] of any small category, $A$.  

This can also be seen to be a case of a [[bar resolution]] construction, related to the [[bar construction]]. Here the adjoint pair also give a [[monad]] on   directed graphs with distinguished 'unit' loops and the small category $A$ is an algebra for this monad. 

Since the functors involved preserve the identities on the objects of $A$, the resulting simplicial category  is a simplicially enriched category, and this is $S[A]$.  The $n$-dimensional arrows between objects, $a$ and $b$ in $S[A]$ correspond to a  path from $a$ to $b$ in $A$ containing no identity arrows, together with a bracketting of the 
resulting string having depth $n$. 

### $W$-Construction of topological operads {#WConstruction}

By hom-wise precomposition with the singular complex functor

$$
  Sing : Top \to sSet
  \,,
$$

which is a [[monoidal functor]], the homotopy coherent nerve extends to a nerve of [[Top]]-[[enriched category|categories]]

$$
  N : Top Cat \to sSet
  \,.
$$

As such, it is a special case of the [[Michael Boardman|Boardman]]-[[Rainer Vogt|Vogt]] [[W-construction]] for [[model structure on operads|cofibrant replacement of]] topological [[operads]]. See also _[[dendroidal homotopy coherent nerve]]_.

In this construction, roughly, for $T$ a [[tree]] in an operad $O$, the tree is replaced with the topological space $e(T) \to [0,1]$ of maps from the set of edges of $T$ to the topological unit interval.

We may restrict this construction to the $n$-[[simplex]] $\Delta[n]$, regarded as a [[category]] and then trivially regarded as a $Top$-category. Then a tree in $\Delta[n]$ is necessarily a linear tree $\to \to \cdots \to$ of some length $k$ and is hence mapped to the topological space of functions $k \to [0,1]$, i.e. to the space $[0,1]^k$. This is the [[geometric realization]] of the simplicial cubes $(\Delta[1])^k$ that we saw above.

 
### Relation to quasi-categories

As mentioned above, the simplicial or h.c. nerve, together with its [[adjoint functor|left adjoint]], serves to relate the two models of [[(∞,1)-category|(∞,1)-categories]] given by [[quasi-category|quasi-categories]] and [[simplicially enriched category|simplicially enriched categories]]. 

The homotopy coherent nerve extends to a [[Quillen equivalence]] between the [[Joyal model structure]] $SSet_{Joyal}$ that models [[quasi-categories]] and the [[model structure on SSet-categories]].

See 

* [[relation between quasi-categories and simplicial categories]] 

for details.

### Models for $(\infty,1)$-categories

[[!include table - models for (infinity,1)-operads]]

### Other kinds of nerves

* [[nerve]]

* [[Duskin nerve]]

* [[∞-nerve]]

* **homotopy coherent nerve**

* [[dg-nerve]]


## History

The original motivation for the introduction of the homotopy coherent nerve is that it provides a neat simplicial formulation of idea of [[homotopy coherent diagram|homotopy coherent diagrams]]. Homotopy coherent algebraic structures were studied in the 1970s by [[Michael Boardman|Boardman]] and [[Rainer Vogt|Vogt]] in joint work,  and then Vogt individually looked at homotopy coherent diagrams.  The  homotopy coherent nerve was first explicitly defined by [[Jean-Marc Cordier|Cordier]] (reference below). 
He  realised that, with a slight modification in the definition, Vogt's definition of homotopy coherent diagram, indexed by a small category $A$, say, corresponded exactly to a simplicially enriched functor from the $SSet$-category $S[A]$ to the $SSet$-category $Top$. They thus also corresponded to simplicial maps from the [[nerve]] of $A$ to $N(Top)$, (although that latter object was 'too large' to be a simplicial 'set'). This allowed a good definition of homotopy coherent diagrams in arbitrary simplicially enriched categories to be given. 

This definition works best when the simplicially enriched category is 'locally Kan', in other words it is enriched in the category of [[Kan complex|Kan complexes]]. These locally Kan $SSet$-categories are the fibrant ones in the [[model structure on sSet-categories]]. 

Cordier and [[Tim Porter|Porter]] (1986) proved that if $C$ is a locally Kan simplicially enriched category then $N(C)$ is a '[[weak Kan complex]]', in other words, a [[quasi-category]].  Some of the main ideas behind this result can be traced to [[Rainer Vogt|Vogt]]'s paper of 1973. 

In more modern terminology as [[Kan complex]]es can be considered as [[∞-groupoid]]s, these locally Kan simplicially enriched categories are one particularly nice model for an [[(infinity,1)-category]], and so this result is one of the earliest giving the transition from one model for [[(infinity,1)-categories]] to another, the 'weak Kan complexes' or [[quasi-categories]].





## References and Literature.

The homotopy coherent nerve operation was introduced, explicitly, in

* {#Cordier82} [[Jean-Marc Cordier]], _Sur la notion  de diagramme homotopiquement coh&#233;rent_, Cahier Top. et Geom. Diff. XXIII 1 (1982) 93-112 &lbrack;[numdam:CTGDC_1982__23_1](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_1982__23_1)&rbrack;

making a link with earlier work in

* R. D. Leitch, _The homotopy commutative cube_, J. London Math. Soc. **2** 9 (1974) 23-29 &lbrack;[doi:10.1112/jlms/s2-9.1.23](https://doi.org/10.1112/jlms/s2-9.1.23)&rbrack;

as well as with [Vogt (1973)](#Vogt73) and with

* [[Michael Boardman]], [[Rainer Vogt]], *Homotopy invariant algebraic structures on topological spaces*, Lec. Notes in Math. __347__ Springer (1973) &lbrack;[doi:10.1007/BFb0068547](https://doi.org/10.1007/BFb0068547)&rbrack;

Poof of an [[equivalence of categories|equivalence]] between the category obtained by inverting the 'levelwise' homotopy equivalence in a category of diagrams, and the [[homotopy category]] of [[homotopy coherent diagrams]]:

* {#Vogt73} [[Rainer Vogt]], *Homotopy limits and colimits*, Math. Z. __134__ (1973) 11-52 &lbrack;[eudml:171965](https://eudml.org/doc/171965), [doi:10.1007/BF01219090](https://doi.org/10.1007/BF01219090)&rbrack;

and explicit proof that the homotopy coherent nerve of a locally Kan simplicially enriched category is a [[quasicategory]], as well as the harder result on when [[outer horns]] in this quasicategory can be filled:

* {#CordierPorter86} [[Jean-Marc Cordier]], [[Tim Porter]], *Vogt's theorem on categories of homotopy coherent diagrams*, Math. Proc. Cambridge Philos. Soc. __100__ (1986) 65-90 &lbrack;[doi:10.1017/S0305004100065877](https://doi.org/10.1017/S0305004100065877), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/Cordier-Porter.pdf)&rbrack;

 
Two other papers are relevant to this:

*  [[Jean-Marc Cordier]], [[Tim Porter]], _Maps between homotopy coherent diagrams_, Top. and its Appl. __28__, (1988), 255 &#8211; 275. 

* [[Jean-Marc Cordier]], [[Tim Porter]], _Fibrant diagrams, rectifications and a construction of Loday_, J. Pure. Applied Alg. __67__, (1990), 111 &#8211; 124.

An elementary discussion of the concept of homotopy coherence forms Chapter V of

*  [[K. H. Kamps]], [[Tim Porter]], _Abstract homotopy and simple homotopy theory_, World Scientific 1997. 


For the role played by Cordier's simplicial nerve in the context of relating quasi-categories to simplicially enriched categories as models for $(\infty,1)$-categories see 


* [[André Joyal]], *[[The Theory of Quasi-Categories and its Applications]]*, lectures at *[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)*, CRM (2008) &lbrack;[pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern45-2.pdf), [[JoyalTheoryOfQuasiCategories.pdf:file]]&rbrack;

* [[André Joyal]], *Notes on quasi-categories* (2008) &lbrack;[pdf](http://www.math.uchicago.edu/~may/IMA/Joyal.pdf), [[JoyalNotesOnQuasiCategories.pdf:file]]&rbrack;

* [[Jacob Lurie]], section 1.1.5 in: *[[Higher Topos Theory]]* (2009) 

This emphasizes the [[adjoint functor|adjunction]] corresponding to the homotopy coherent ("simplicial") nerve construction. 


A review of this latter aspect is also in

* {#Dhand} Vivek Dhand, _The simplicial nerve of a simplicial category_ ([pdf](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=374dc56d9a4352b8f9f71cc12dd7331e9285bb0c), [[Dhand-SimplicialNerve.pdf:file]])

* Mitya Boyarchenko, _Notes and exercise on $\infty$-categories_ ([pdf](http://math.uchicago.edu/~mitya/langlands/quasicategories.pdf))

* [[Vladimir Hinich]], _Simplicial nerve in Deformation theory_ ([arXiv:0704.2503](http://arxiv.org/abs/0704.2503))

* [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _Dendroidal sets and simplicial operads_, [arxiv/1109.1004](http://arxiv.org/abs/1109.1004) (a Quillen equivalence for Segal vs. simplicial operads using coherent nerve)

* [[Emily Riehl]], _On the structure of simplicial categories associated to quasi-categories, Math. Proc. Camb. Phil. Soc. 150 (2011), 489 - 504.

For more references see [[relation between quasi-categories and simplicial categories]].

Two query-discussions on terminology and concrete description of the coherent/"simplicial" nerve are archived at nForum [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=754&Focus=20607#Comment_20607).  For an overview of the 2009 paper by Dugger and Spivak, see also:

* [[Emily Riehl]], [Understanding the homotopy coherent nerve](https://golem.ph.utexas.edu/category/2010/04/understanding_the_homotopy_coh.html), n-Category Caf&#233;, 29 April 2010.

Relating the [[Dwyer-Kan loop groupoid]]-construction to the homotopy coherent nerve-construction:

* {#MinichielloRiveraZeinalian23} [[Emilio Minichiello]], [[Manuel Rivera]], [[Mahmoud Zeinalian]], *Categorical models for path spaces*, Advances in Mathematics **415** (2023) 108898 &lbrack;[arXiv:2201.03046](https://arxiv.org/abs/2201.03046), [doi:10.1016/j.aim.2023.108898](https://doi.org/10.1016/j.aim.2023.108898)&rbrack;


[[!redirects homotopy coherent nerves]]
[[!redirects homotopy-coherent nerve]]
[[!redirects homotopy-coherent nerves]]
[[!redirects coherent nerve]]
[[!redirects coherent nerves]]
[[!redirects nerve of a simplicial category]]
[[!redirects simplicial nerve of simplicial categories]]