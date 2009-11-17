#Contents#
* automatic table of contents goes here
{:toc}

##Idea##

The _homotopy coherent nerve_ (also called _simplicial nerve_) of a [[simplicially enriched category]] is a [[simplicial set]] which includes information about all the higher homotopies present in the hom-spaces.  It generalizes the ordinary [[nerve]] of an ordinary [[category]].

The homotopy coherent nerve operation

$$
  N : SSet\text{-}Cat \to SSet
  \,.
$$

is induced, by the general nonsense of [[nerve and realization]] by a 
[[simplicial object|cosimplicial]] [[simplicially enriched category]], namely a [[functor]]

$$
  \Delta \to SSet\text{-}Cat
$$

from the [[simplex category]] to the category of 
[[simplicially enriched categories]] which regards each
$n$-[[simplex]] as a [[SSet]]-[[enriched category]]
with $n$ objects analogous to how the [[oriental]]s
regard the $n$-simplex as an [[strict omega-category|n-category]].






##Preliminary definitions##

For $\Delta^n$ the standard [[simplicial set|simplicial]] $n$-[[simplex]], define the [[simplicially enriched category]] $S[\Delta^n]$ as follows:

* the objects of $S[\Delta^n]$ are $\{0,1, \cdots, n\}$;

* for $i, j \in \{0,1,\cdots, n\}$ define  $S[\Delta^n](i,j) = N(P_{i,j}),$ the nerve of the poset $P(i,j)$ defined in either of the two equivalent ways:     
   1. $P_{i,j}$ is the [[poset]] whose  elements are the subsets of $[i,j]$ that contain both $i$ and $j$ (so in particular is $i\gt j$ then $P(i,j)$ is empty and hence so is its nerve), the partial order is given by inclusion.
   1. $P(i,j)$ is the set of paths in $[n]$ that start at $i$ and finish at $j$ (hence is empty if $i\gt j$), the order relation is given by 'subdivision', i.e. path $a$ is less than path $b$ in $P(i,j)$ if $b$ visits all the vertices that $i$ does ... and perhaps some others as well.

Of course, the way you go between the two descriptions is that a path corresponds to the set of vertices it visits and _vice versa_.

+--{.query}
[[Todd Trimble|Todd]]: I am learning this for the first time, and I had some difficulty with how the definition of $P_{i,j}$ reads. From the ensuing discussion, it seems you want the elements of the poset to be $I \subseteq [i, j]: i, j \in I$, ordered by inclusion. But in the definition, it's not clear what sort of thing $J$ is supposed to be, and it looks like the elements of the poset are instances of inclusions. (Another minor thing I don't understand is why $\subset$ is being used instead of $\subseteq$, since for many mathematicians $\subset$ means strict inclusion. I see this preference for $\subset$ all over the nLab in fact; has this been discussed somewhere?)

[[Tim Porter|Tim]]:  I did not originate the poset based description as I always think of things as being paths through the $N$-simplex from $i$ to $j$ and then use a rewrite idea for the link.  I will try to clean up the poset definition a bit and see if it helps, otherwise we can switch to the path based description and use the poset as a second way. I'm not bothered either way.

Some minutes later!  Does this read well now?

[[Todd Trimble|Todd]]: Thank you! Yes, me happy now. 
=--

 The simplicial set $N(P_{i,j})$ is isomorphic to the $j-i-1$ cube $\Delta[1]^{j-i-1}$. (We will look at an example after this definition.)

* the composition operation is induced by 'composition of the corresponding paths' and thus essentially by union of the sets involved.

##Remark:## 

in case you are wondering why we did not just say $P(i,j)$ was the poset of subsets of the set of elements between $i$ and $j$, it is because of the composition.  Of course, it can be done but looks more messy.

##Example and (hopefully) explanation##

We will examine the lowest dimensional cases. For $n = 0,1$, there is nothing of note.

For $n = 2$, there are unique paths in $[2]$ from $[0]$ to $[1]$, and $[1]$ to $[2]$, so the corresponding homs in $S[2]$ are copies of $\Delta[0]$ (or, if you prefer, of $\Delta[1]^0$!). Things are slightly more interesting for $S[2](0,2)$. Looking at this from the 'subsets' viewpoint, as above, there clearly are two subsets of $\{0,1,2\}$ containing both $0$ and $2$, one corresponds to the direct route in $[2]$ from $0$ to $2$, the other goes via $1$ so is $0\to 1\to 2$. In $S[2](0,2)$, there is a 1-simplex starting at $\{0,2\}$ and ending at $\{0,1,2\}$.  
 Everything else, in higher dimensions, is degenerate, so $S[2](0,2)\cong \Delta[1]$. Sometimes it is useful to think of this 1-simplex as 'rewriting' the direct path to that via 1, all this happening in the free category on the underlying graph of the poset $[2]$. 

In this example there are no significant compositions. To see examples of those, you need to look at $n = 3$. In $S[3]$, the simplicial hom-sets $S[3](i,j)$ for $(i,j) \neq (0,3)$, can all be analysed by the same sort of argument to the above.  The new features occur in $S[3](0,3)$.  The vertices of this simplicial set are the subsets $\{ 0.3\}$, $\{0,1,3\}$, $\{0,2,3\}$, and  $\{0,1,2,3\}$, corresponding to the direct path $0\to 3$ and then the three others. Rewriting the direct path can be done in two immediate ways, to go via 1 or via 2. Each of these can be 'rewritten' to give the longest path /  largest subset. There is also, of course, an inclusion of the smalles to the largest of these:
$$
  \array{
     \{0,3\}&\rightarrow & \{0,1,3\}
     \\
     \downarrow & \searrow &\downarrow\\
     \{0,2,3\}&\rightarrow &\{0,1,2,3\}
   }
$$
In addition, there will be 2-simplexes filling the two triangles, coming from the chains $\{0,3\}\subset \{0,1,3\}\subset \{0,1,2,3\}$ and $\{0,3\}\subset \{0,2,3\}\subset \{0,1,2,3\}$ in the poset. We thus get $S[3](0,3) \cong \Delta[1]^2$, a square. 

The composition maps

$$S[3](1,3)\times S[3](0,1)\to S[3](0,3)$$

and similarly for the one with 1 replaced by 2, *are* now fairly obvious.  



For $n = 4$, the corresponding diagram for $S[4](0,4)$ gives a cube (left to the reader), but here there is an interesting feature.  The 4-simplex has five 3-dimensional faces and each will give one 2-dimensional face of that cube.  A cube has six 2-dimensional faces. The 'extra' sixth face corresponds to the interchange law, or, if preferred, to the fact that

$$S[4](2,4)\times S[4](0,2)\to S[4](0,4)$$

is to be a simplicial map.

A similar phenomenon occurs in higher dimensions.  There are two 'extra faces' in $S[5](0,5)$, and so on.


###Remark###

We will return to other thoughts on this $S$ construction later in the entry.


One of the reasons for discussing the above is the following:

##Definition##

For $C$ a [[simplicially enriched category]], the **homotopy coherent nerve**  $N(C)$ is the [[simplicial set]] uniquely characterized by the formula $ Hom_{SSet}(\Delta^n, N(C)) = Hom_{SSet-Cat}(S[\Delta^n], C)$.


##Remarks##

* The original motivation for the introduction of the homotopy coherent nerve is that it provides a neat simplicial formulation of idea of [[homotopy coherent diagram|homotopy coherent diagrams]]. These were studied in the 1970s, by Boardman and Vogt in joint work,  and Vogt individually,  and Cordier (reference below). Cordier realised that, with a slight modification in the definition, Vogt's definition of homotopy coherent diagram, indexed by a small category $A$, say, corresponded exactly to a simplicially enriched functor from the $SSet$-category $S[A]$ to the $SSet$-category $Top$. They thus also corresponded to simplicial maps from the [[nerve]] of $A$ to $N(Top)$, (although that latter object was 'too large' to be a simplicial 'set'). This allowed a good definition of homotopy coherent diagrams in arbitrary simplicially enriched categories to be given. This definition works best when the simplicially enriched category is 'locally Kan', in other words it is enriched in the category of [[Kan complex|Kan complexes]]. These locally Kan $SSet$-categories are the fibrant ones in a model category structure on the category of $SSet$-categories. Cordier and Porter (1986) proved that if $C$ is a locally Kan simplicially enriched category then $N(C)$ is a '[[weak Kan complex]]', in other words, a [[quasi-category]].  Many of the ideas behind this result can be traced to Vogt's paper of 1973.

*   The use of $S[A]$, above, extends that given at the start of this page. Here $S$ is related  to the left adjoint of the homotopy coherent nerve, but is defined using a [[comonadic resolution]].  The comonad is that between small categories and directed graphs with distinguished 'unit' loops. The 'forgetful' part of the adjunction forgets the composition in the category, but remembers that the identity arrows are special. The left adjoint /  'free' part of the adjunction takes a directed graph (with distinguished 'identity' loops, and forms the free category on the non-identity arrows. As usual, we can form a [[comonad]] from this  and hence form a functorial [[simplicial resolution]] of any small category, $A$.  (This is one of the many variants of a [[bar resolution]] construction, related to the [[bar construction]].) Since the functors involved preserve the identities on the objects of $A$, the resulting simplicial category  is a simplicially enriched category, and this is $S[A]$.  The $n$-dimensional arrows between objects, $a$ and $b$ in $S[A]$ correspond to a  path from $a$ to $b$ in $A$ containing no identity arrows, together with a bracketting of the resulting string having depth $n$. 
  

* The simplicial nerve, together with its [[adjoint functor|left adjoint]], serves to relate the two models of [[(infinity,1)-category|(infinity,1)-categories]] given by [[quasi-category|quasi-categories]] and [[simplicially enriched category|simplicially enriched categories]].


*  Any 2-category gives a simplcially enriched category using the embedding of $Cat$ into $SSet$ via the usual nerve functor. The homotopy coherent nerve of a 2-category consideed in this way is, sometimes, called the [[geometric nerve]] of the 2-category. The [[Duskin nerve]] of a bicategory is an extension of this construction. 

   A particular case of this nerve is the nerve of a [[2-group]] considered as a 2-category.

##References##

The homotopy coherent nerve operation was introduced in

* J.-M. Cordier, _Sur la notion  de diagramme homotopiquement coh&#233;rent_, Cahier Top. et Geom. Diff. XXIII 1, 1982, 93-112

For the role played by the simplicial nerve in the context for relating quasi-categories to simplicially enriched categories as models for $(\infty,1)$-categories see section 1.1.5 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

A review is also in

* Vivek Dhand, _The simplicial nerve of a simplicial category_ ([pdf](http://www.math.msu.edu/~dhand/sSet.pdf))

## Discussion ##

The following discussion was at [[simplicial nerve]] when this page was at [[simplicial nerve of simplicial categories]].
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


[[!redirects homotopy coherent nerves]]
[[!redirects homotopy-coherent nerve]]
[[!redirects homotopy-coherent nerves]]
[[!redirects nerve of a simplicial category]]
[[!redirects simplicial nerve of simplicial categories]]