
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
* automatic table of contents goes here
{:toc}

## Idea

The _homotopy coherent nerve_ (also called _simplicial nerve_) of a [[simplicially enriched category]] is a [[simplicial set]] which includes information about all the higher homotopies present in the hom-spaces.  It generalizes the ordinary [[nerve]] of an ordinary [[category]].

The homotopy coherent nerve operation

$$
  N : SSet\text{-}Cat \to SSet
  \,.
$$

is induced, by the general machinery of [[nerve and realization]], by a 
[[simplicial object|cosimplicial]] [[simplicially enriched category]], namely a [[functor]]

$$
  \Delta \to SSet\text{-}Cat
$$

from the [[simplex category]] to the category of 
[[simplicially enriched categories]] which regards each
$n$-[[simplex]] as a [[SSet]]-[[enriched category]]
with $n$ objects analogous to how the [[oriental]]s
regard the $n$-simplex as an [[strict omega-category|n-category]].



## Definition


### The cosimplicial $sSet$-category

We start by describing the cosimplicial [[sSet]]-[[enriched category]] 

$$
  S : \Delta \to sSet Cat
$$

that induces the homotopy coherent nerve.

For $[n]$ the finite [[ordinal number|ordinal]] $[n] := \{0 \lt 1 \lt  \cdots \lt n\}$ and for $\Delta[n]$ be  standard [[simplicial set|simplicial]] $n$-[[simplex]], define the $sSet$-category $S[n]$ as follows:

* the [[object]]s of $S[n]$ are $\{0,1, \cdots, n\}$;

* the [[hom-object]]s $S[n]_{i,j} \in sSet$ for $i, j \in \{0,1,\cdots, n\}$ are the [[nerve]]s 

  $$
    S[n](i,j) = N(P_{i,j})
  $$ 

  of the [[poset]] $P_{i,j}$ which is equivalently

  1. the [[poset]] of [[subset]]s of $[i,j]$ that contain both $i$ and $j$ (so in particular if $i\gt j$ then $P(i,j)$ is empty and hence so is its nerve) with the partial order is given by inclusion.

   1. the poset of [[path category|path]]s in $[n]$ that start at $i$ and finish at $j$ (hence is empty if $i\gt j$), the order relation is given by 'subdivision', i.e. path $a$ is less than path $b$ in $P(i,j)$ if $b$ visits all the vertices that $i$ does ... and perhaps some others as well.

      Of course, the way you go between the two descriptions is that a path corresponds to the set of vertices it visits and _vice versa_.


Notice that the simplicial set $N(P_{i,j})$ is [[isomorphism|isomorphic]] to the $j-i-1$ cube in $sSet$:

$$
  N(P_{i,j}) = (\Delta[1])^{\times (j-i-1)}
  \,.
$$ 

Under this isomorphism for instance the vertex $(0,0,1,0,1) \in (\Delta[1])^{\times (j-i-1)}$ corresponds to the subset $\{i+3,i+5\} \subset [i,j]$ and to the path $i \to i+3 \to i+5 \to j=i+6$. 

(We will look at an example after this definition.)

* the [[composition]] operation on hom-objects

  $$
    \circ_{i,j,k} : S[n]_{i,j} \times S[n]_{j,k} \to S[n]_{i,k}
  $$

  is induced by 'concatenation of the corresponding paths' and thus essentially by union of the sets involved.

### The homotopy coherent nerve

The **homotopy coherent nerve** functor

$$
  N := Hom_{sSet Cat}(S[\bullet],-) : sSet Cat \to sSet
$$

is the [[nerve]] defined by the cosimplicial $sSet$-category $S : \Delta \to sSet Cat$ defined above.

For $C \in sSet Cat$ a [[simplicially enriched category]], the homotopy coherent nerve  $N(C)$ is the [[simplicial set]] uniquely characterized by the formula 

$$ 
  Hom_{SSet}(\Delta[n], N(C)) = Hom_{SSet Cat}(S[n], C)
  \,.
$$

By the general logic of [[nerve and realization]], this functor has a [[left adjoint]]

$$
  S(-) : SSet \to SSet Cat
$$

the **realization** functor given by the [[coend]] formula

$$
  S(X) := \int^{[n] \in \Delta} X_n \cdot S[n]
  \,.
$$

This functor does extend the functor $S : \Delta \to sSet Cat$ 
in that there is a canonical isomorphism

$$
  S(\Delta[n]) \cong S[n]
$$

and hence may consistently be named $S$.



## Examples and illustration

### For the cosimplicial $sSet$-category {#IllustratOfCosimpSSetCat}

We illustrate here the nature of the cosimplicial $sSet$-category $S : [n] \mapsto S[n]$.

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
    (0,2) \to (0,1,2)
  \right\}
  = 
  \Delta[1]
  \,.
$$

So in $S[2](0,2)$, there is a 1-simplex $k$ starting at $\{0,2\}$ and ending at $\{0,1,2\}$.  

$$
    \array{
      & \nearrow\searrow^{\{0,1,2\}}
      \\
      0 &\Uparrow^{{k}}& 2
      \\
      & \searrow \nearrow_{\{0,2\}}
    }
$$


Everything else, in higher dimensions, is degenerate, so $S[2](0,2)\cong \Delta[1]$. Sometimes it is useful to think of this 1-simplex as 'rewriting' the direct path to that via 1, all this happening in the free category on the underlying graph of the poset $[2]$. (The construction of $S[n]$ in general has a nice interpretation in terms of higher dimensional [[rewriting]]. This can be given using the language of [[polygraph]]s or [[computad]]s.)

In this example there are no significant compositions. To see examples of those, you need to look at $n = 3$. In $S[3]$, the simplicial hom-sets $S[3](i,j)$ for $(i,j) \neq (0,3)$, can all be analysed by the same sort of argument to the above.  The new features occur in $S[3](0,3)$.  The vertices of this simplicial set are the subsets 
corresponding to the direct path $0\to 3$ and then the three others. Rewriting the direct path can be done in two immediate ways, to go via the left or via the right route. Each of these can be 'rewritten' to give the longest path /  largest subset.  There is also, of course, an inclusion of the smallest to the largest of these, so that in total the poset here looks like:

$$
  P_{0,3}
  =
  \left\{
    \array{
       \{0,3\}&\rightarrow & \{0,1,3\}
       \\  
       \downarrow & \searrow &\downarrow\\
       \{0,2,3\}&\rightarrow &\{0,1,2,3\}
     }
  \right\}
  =
  \Delta[1]^{\times 2}
  \,.
$$

In addition, there will be 2-simplexes filling the two triangles, coming from the chains $\{0,3\}\subset \{0,1,3\}\subset \{0,1,2,3\}$ and $\{0,3\}\subset \{0,2,3\}\subset \{0,1,2,3\}$ in the poset. 

$$
  \array{
    & \nearrow && \searrow^{\mathrlap{\{0,1,2,3\}}}
    \\
    & & \Uparrow
    \\
    0  &&\stackrel{\{0,1,3\}}{\to}&& 3
    \\
    && \Uparrow
    \\
    & \searrow && \nearrow_{\mathrlap{\{0,2\}}}
  }
  \;\;\;\;\;
  \;\;\;\;\;
  \;\;\;\;\;
  \,,
  \;\;\;\;\;
  \;\;\;\;\;
  \;\;\;\;\;
  \array{
    & \nearrow && \searrow^{\mathrlap{\{0,1,2,3\}}}
    \\
    & & \Uparrow
    \\
    0  &&\stackrel{\{0,2,3\}}{\to}&& 3
    \\
    && \Uparrow
    \\
    & \searrow && \nearrow_{\mathrlap{\{0,2\}}}
  }
  \,.
$$



We thus get $S[3](0,3) \cong \Delta[1]^2$, a square. 

The composition maps

$$S[3](1,3)\times S[3](0,1)\to S[3](0,3)$$

and similarly for the one with 1 replaced by 2, *are* now fairly obvious.  



For $n = 4$, the corresponding diagram for $S[4](0,4)$ gives a cube 
but here there is an interesting feature.  

Five of the six faces of the cube $|N(P_{0,4})|$ correspond to the the associativity of composition of triples of composable morphisms in $[4]$. These correspond to the 5 faces of the 4-simplex $\Delta[4]$, as depicted for instance at [[oriental]] and at [[monoidal category]].

But the cube has one more face

$$
  \array{
    (0,2,4) &\to& (0,1,2,4)
    \\
    \downarrow &\searrow& \downarrow
    \\
    (0,2,3,4) &\to& (0,1,2,3,4)
  }
$$

which does not correspond to associativity: instead, this encodes the [[exchange law]]


$$
  \array{
    && 1 &&&& 3
    \\
    & \nearrow &\Uparrow& \searrow && \nearrow && \searrow
    \\
    0 &&\to&& 2 &&  && 4
    \\
    &&  &&&& 3
    \\
    & && && \nearrow &\Uparrow& \searrow
    \\
    0 &&\to&& 2 && \to && 4  
  }
  \;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;
  \array{
    && 1 &&&& 3
    \\
    & \nearrow && \searrow && \nearrow &\Uparrow& \searrow
    \\
    0 &&&& 2 && \to && 4
    \\
    && 1 &&&& 
    \\
    & \nearrow &\Uparrow& \searrow &&  && 
    \\
    0 &&\to && 2 && \to && 4  
  }
$$

or, if preferred, to the fact that

$$S[4](2,4)\times S[4](0,2)\to S[4](0,4)$$

is to be a simplicial map.




A similar phenomenon occurs in higher dimensions.  There are two 'extra faces' in $S[5](0,5)$, and so on.

### For the homotopy coherent nerve

*  Any [[2-category]] gives a simplcially enriched category using the embedding of [[Cat]] into [[sSet]] via the usual [[nerve]] functor. The homotopy coherent nerve of a 2-category consideed in this way is, sometimes, called the [[geometric nerve]] of the 2-category. The [[Duskin nerve]] of a [[bicategory]] is an extension of this construction. 

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
      f_{x,y} : C(x,y) \to C(f(x),f(y))
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

As such, it is a special case of the [[Michael Boardman|Boardman]]-[[Rainer Vogt|Vogt]] [[W-construction]] for [[model structure on operads|cofibrant replacement of]] topological [[operad]]s.

In this construction, rouhgly, for $T$ a [[tree]] in an operad $O$, the tree is replaced with the topological space $e(T) \to [0,1]$ of maps from the set of edges of $T$ to the topological unit interval.

We may restrict this construction to the $n$-[[simplex]] $\Delta[n]$, regarded as a [[category]] and then trivially regarded as a $Top$-category. Then a tree in $\Delta[n]$ is necessarily a linear tree $\to \to \cdots \to$ of some length $k$ and is hence mapped to the topological space of functions $k \to [0,1]$, i.e. to the space $[0,1]^k$. This is the [[geometric realization]] of the simplicial cubes $(\Delta[1])^k$ that we saw above.

 
### Relation to quasi-categories

As mentioned above, the simplicial or h.c. nerve, together with its [[adjoint functor|left adjoint]], serves to relate the two models of [[(∞,1)-category|(∞,1)-categories]] given by [[quasi-category|quasi-categories]] and [[simplicially enriched category|simplicially enriched categories]]. 

The homotopy coherent nerve extends to a [[Quillen equivalence]] between the [[Joyal model structure]] $SSet_{Joyal}$ that models [[quasi-categories]] and the [[model structure on SSet-categories]].

See 

* [[relation between quasi-categories and simplicial categories]] 

for details.

## History

The original motivation for the introduction of the homotopy coherent nerve is that it provides a neat simplicial formulation of idea of [[homotopy coherent diagram|homotopy coherent diagrams]]. These were studied in the 1970s, by [[Michael Boardman|Boardman]] and [[Rainer Vogt|Vogt]] in joint work,  and Vogt individually,  and [[Jean-Marc Cordier|Cordier]] (reference below). 

[[Jean-Marc Cordier|Cordier]] realised that, with a slight modification in the definition, Vogt's definition of homotopy coherent diagram, indexed by a small category $A$, say, corresponded exactly to a simplicially enriched functor from the $SSet$-category $S[A]$ to the $SSet$-category $Top$. They thus also corresponded to simplicial maps from the [[nerve]] of $A$ to $N(Top)$, (although that latter object was 'too large' to be a simplicial 'set'). This allowed a good definition of homotopy coherent diagrams in arbitrary simplicially enriched categories to be given. 

This definition works best when the simplicially enriched category is 'locally Kan', in other words it is enriched in the category of [[Kan complex|Kan complexes]]. These locally Kan $SSet$-categories are the fibrant ones in the [[model structure on sSet-categories]]. 

Cordier and [[Tim Porter|Porter]] (1986) proved that if $C$ is a locally Kan simplicially enriched category then $N(C)$ is a '[[weak Kan complex]]', in other words, a [[quasi-category]].  Many of the ideas behind this result can be traced to [[Rainer Vogt|Vogt]]'s paper of 1973. 

In more modern terminology as [[Kan complex]]es can be considered as [[∞-groupoid]]s, these locally Kan simplicially enriched categories are one particularly nice model for a [[(infinity,1)-category]], and so this result is one of the earliest giving the transition from one model for [[(infinity,1)-category]]s to another, the 'weak kan complexes' or [[quasi-categories]].



## References

The homotopy coherent nerve operation was introduced, explicitly, in

* [[Jean-Marc Cordier]], _Sur la notion  de diagramme homotopiquement coh&#233;rent_, Cahier Top. et Geom. Diff. XXIII 1, 1982, 93-112, available from [numdam](http://www.numdam.org/numdam-bin/feuilleter?id=CTGDC_1982__23_1)

Cordier made the link with earlier work by R.D. Leitch.

* R. D. Leitch, _The Homotopy Commutative Cube_, J. London Math. Soc., (2) 9, (1974), 23 &#8211; 
29.

as well as the paper by [[Vogt]] (see below) and earlier work of [[Michael Boardman|Boardman]] and [[Rainer Vogt|Vogt]],

* [[Michael Boardman] and [[Rainer Vogt]], 1973, _Homotopy Invariant algebraic structures on topological 
spaces_, number 347, Lecture Notes in Maths, Springer-Verlag.

With [[Tim Porter]], Cordier proved the simplicial generalisation of a theorem of [[Rainer Vogt|Vogt]], in

*  [[Jean-Marc Cordier]] and [[Tim Porter]], _Vogt's theorem on categories of homotopy coherent diagrams_, 
Math. Proc. Cambridge Philos. Soc., 100, (1986), 65 &#8211; 90.

This theorem describes an equivalence between the category obtained by inverting the 'levelwise' homotopy equivalence in a category of diagrams, and the homotopy category of [[homotopy coherent diagram]]s in the sense of Vogt. This paper includes an explicit proof that the homotopy coherent nerve of a locally Kan simplicially enriched category is a quasicategory. As well as the harder result on when [[outer horn]]s in this quasicategory can be filled.

Vogt's original version of the theorem is in 

* [[Rainer Vogt]], _Homotopy limits and colimits_, Math. Z., 134, (1973), 11 &#8211; 52.  
 
Two other papers are relevant to this:

*  [[Jean-Marc Cordier]] and [[Tim Porter]], _Maps between homotopy coherent diagrams_, Top. and its Appls., 
28, (1988), 255 &#8211; 275. 

and 

* [[Jean-Marc Cordier]] and [[Tim Porter]], _Fibrant diagrams, rectifications and a construction of Loday_, J. 
Pure. Applied Alg., 67, (1990), 111 &#8211; 124.

An elementary discussion of the concept of homotopy coherence forms Chapter V of

*  K. H. Kamps and [[Tim Porter]], 1997, _Abstract Homotopy and Simple Homotopy Theory_, World 
Scientific Publishing Co. Inc., River Edge, NJ. 

The construction has been rediscovered several times more recently, for instance, for the role played by the simplicial nerve in the context of relating quasi-categories to simplicially enriched categories as models for $(\infty,1)$-categories see section 1.1.5 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

This emphasises the adjunction induced by the h.c. / simplicial nerve construction. 

A review of this latter aspect is also in

* Vivek Dhand, _The simplicial nerve of a simplicial category_ ([pdf](http://www.math.msu.edu/~dhand/sSet.pdf))


and 

* Mitya Borachenko, Notes and exercise on $\infty$-cateogires([pdf](http://math.uchicago.edu/~mitya/langlands/quasicategories.pdf))


For more references see [[relation between quasi-categories and simplicial categories]].

## Discussion ##

> The following discussion was at [[simplicial nerve]] when this page was at [[simplicial nerve of simplicial categories]].


+-- {: .query}
Is there a simplicial nerve that\'s not of simplicial categories?  If not, I\'d put the article here instead of there.  ---Toby

[[Urs Schreiber|Urs]]: yes, it seems to be called just "simplicial nerve" in the literature, but I found that a bit undescriptive, since every nerve is "simplicial" and here the point is really that we take the nerve _of_ a simplicial category. I also seem to recall that [[Tim Porter|Tim]] said he doesn't like the term "simplicial nerve". Maybe Tim should decide, he is probably the one among us who has thought about this notion the most.

_Toby_:  Ah, I see how 'simplicial nerve' is confusing; so how about just [[nerve of a simplicial category]]?

[[Urs Schreiber|Urs]]: right, that might be the best option -- I have to run now, maybe you can implement that?

_Toby_:  I\'ll wait to hear from Tim.

[[Mike Shulman|Mike]]: Not all nerves are simplicial; it depends on what you are taking the nerve of.  The nerve of a multicategory is a dendroidal set (a presheaf on the category of trees).  The nerve of a compact symmetric multicategory is a presheaf on the category of Feynman graphs.  And an $n$-category has a nerve that is a simplicial set, but also one that is a $\Theta_n$-set and one that is an $n$-fold simplicial set.

FWIW, I have sometimes seen the "simplicial nerve of simplicial categories" called the "homotopy coherent nerve," which to me captures the intuition better.

[[Urs Schreiber|Urs]]: true, I actually know that not every notion of nerve is simplicial, should have thought before typing. 

Now that you mention it, maybe [[Tim Porter]] also said he favored "homotopy coherent nerve"? I'll send him an email.

[[Tim Porter|Tim]]:  Back from a short absence: the term 'homotopy coherent nerve' is probably a good one only when it fairly directly relates to homotopy coherence. 

Any 2-category can be thought of as a simplicially enriched category and the Duskin nerve of a bicategory specialises to the same construction on 2-categories. Various people use the term 'geometric nerve' for this. (It is interesting to compare the 'simplicial nerve' of a simplicial group (as SSet-enriched category) with Wbar of the same thing.) I am trying to write something for the Menagerie that looks at the h.c. nerve with these aspects accentuated and also with links with Behrang Noohi's weak maps of crossed modules. I may put some of this on nLab when I see more clearly how it all fits together.  

In the meantime, I suggest we keep the term h.c. nerve although it is probably not 'best possible'.
I agree that 'simplicial nerve'  is probably not a good term.
=--

Here is another old discussion that seems to have been resolved

+--{.query}
[[Todd Trimble|Todd]]: I am learning this for the first time, and I had some difficulty with how the definition of $P_{i,j}$ reads. From the ensuing discussion, it seems you want the elements of the poset to be $I \subseteq [i, j]: i, j \in I$, ordered by inclusion. But in the definition, it's not clear what sort of thing $J$ is supposed to be, and it looks like the elements of the poset are instances of inclusions. (Another minor thing I don't understand is why $\subset$ is being used instead of $\subseteq$, since for many mathematicians $\subset$ means strict inclusion. I see this preference for $\subset$ all over the nLab in fact; has this been discussed somewhere?)

[[Tim Porter|Tim]]:  I did not originate the poset based description as I always think of things as being paths through the $N$-simplex from $i$ to $j$ and then use a rewrite idea for the link.  I will try to clean up the poset definition a bit and see if it helps, otherwise we can switch to the path based description and use the poset as a second way. I'm not bothered either way.

Some minutes later!  Does this read well now?

[[Todd Trimble|Todd]]: Thank you! Yes, me happy now. 
=--



[[!redirects homotopy coherent nerves]]
[[!redirects homotopy-coherent nerve]]
[[!redirects homotopy-coherent nerves]]
[[!redirects nerve of a simplicial category]]
[[!redirects simplicial nerve of simplicial categories]]