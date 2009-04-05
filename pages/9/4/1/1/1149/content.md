
The following is (supposed to be) a pedagogical motivation of the 
concepts [[sheaf]], [[stack]], [[infinity-stack]] and
[[Higher Topos Theory|higher topos theory]]. It assumes 
only that the reader has a heuristic knowledge of [[topological space]]s
and aims to provide from that a heuristic but useful idea of 
the relevance of the circle of ideas of [[Categories and Sheaves|categories and sheaves]],
[[nonabelian cohomology]],
[[sheaf cohomology]] and a bit of [[Higher Topos Theory|higher topos theory]].


## Motivation: maps between topological spaces ##

It is a familiar fact that classes of maps between [[topological space]]s encode interesting information.

To pick just one simple but important example: there is a [[topological space]]  that goes by the name
$K(\mathbb{Z},2)$ or $B U(1)$. 
Whatever the name of this space, it is that space which has the  peculiar property that for any other space $X$,
the homotopy classes $[X, B U(1)]$ of continuous maps
from $X$ to this space $B U(1)$ characterize the following useful information:

* they correspond to equivalence classes of circle [[bundle]]s over $X$: that is, to spaces $P$ equipped with a map to $X$ such that over 
a contractible open subset $U \subset X$ the space $P$ looks like
the [[product]] of $U$ with the circle, $P|_U \simeq U \times S^1$. One says that $B U(1)$ is the [[classifying space]] for circle [[bundle]]s.

  * A famous such circle bundle you may have seen is the [Hopf bundle](http://en.wikipedia.org/wiki/Hopf_bundle), which is a way to map the 3-dimensional sphere $S^3$ to the familiar 2-dimensional sphere $S^2$, such that over small parts $U \subset S^2$ of the 2-sphere the 3-sphere looks like the product space $U \times S^1$.

  * This circle bundle corresponds to a very special class of maps $X \to B U(1)$: 
  namely the collection of maps $[S^2, B U(1)]$ happens to have the structure
  of the abelian group $\mathbb{Z}$ of integers under addition, 
  and the Hopf fibration corresponds to the 
  the generating element $1$ of this group;
  
  * generally, this abelian group formed by $[X, B U(1)]$ 
  is famous under another name: it is called the second integral
  [[cohomology]] group of $X$, denoted $H^2(X, \mathbb{Z})$.
  
* There is a similar such cohomology group $H^n(X,\mathbb{Z})$ 
of $X$ for every natural number $n$: the $n$th [[integral cohomology]]
group of $X$ -- and all these groups are naturally
realized in terms of homotopy classes of maps from $X$ into 
some topological space (called $B^{n-1} U(1)$).

* These cohomology groups encode a lot of interesting information about
topological spaces; but there is some useful information about a space, which is not
encoded in maps from this to another topological space: 

* for instance if the space $X$ is not just a topological 
space but actually a smooth manifold, then one is interested 
in smooth circle bundles
over $X$ which are equipped with a [[connection]]: a good rule which assigns 
to each smooth path in $X$ an identification between the two circles
over its endpoints;

 * it would be nice if generalized cohomological information
 about spaces such as the classes of circle bundles with connection over them,
 could also be understood in terms of classes of maps between 
 something akin to topological spaces: maybe we just need a slightly more
 flexible notion of what "space" should mean.
 
* the generalization of the notion of _space_ which does
 accomplish this: the notion of a [[sheaf]] in proper interpretation in the general context of [[space and quantity]]:


## the basic idea of sheaves ##

 
* To understand what a [[sheaf]] is, recall which aspect of the notion of
 [[topological space]] was relevant in the above
 examples $B^{n-1} U(1)$: these spaces were
 entirely characterized by how one can _map_ other spaces _into_ them.

* this is a general strategy that one can adopt: suppose I dream up a space but don't tell you which one it is, but I give you hints: for each other space $U$ that you can dream up, I tell you how you can _probe_ my space by mapping your space $U$ into it.
 
 * Let's call the space which I dreamed up $X$. For every space $U$ that you come up with, I do some secret computation and then present you with the result: I hand you a set, let's call it $X(U)$, and tell you  that this is the set of ways that $U$ can be mapped into $X$.
 
 * will you be able, in general, to guess my space $X$ from this information? Hardly. So, to be fair, I should provide a bit more of information: what you
 need to know to actually get a feeling for what my space $X$ is like is an idea about how different ways of probing my space relate to each other
 
 * Okay, so we'll do this: for every pair $U$ and $V$ of test spaces that 
 you come up with, and for every way $f : U \to V$ of mapping these into each other,
 I inform you not only about the set of ways $X(U)$ that $U$ can be mapped 
 into my secret space $X$, and the set of ways $X(V)$ that $V$ can be mapped
 into my secret space, but I also tell you how these are related when you first map $V$ into $X$ by a map $p : V \to X$ and then map $U$ into $X$
 by first mapping it to $V$: $U \stackrel{f}{\to}  V \stackrel{p}{\to}  X$.
 This transforms every element in $X(V)$ into an element in $X(U)$. To be fair,
 I should tell you at least what this transformation is!
 
 * So I'll do that: for every map of test space $f : U \to V$
 that you hand me, I return you a map of sets that I denote 
 $X(f) : X(V) \to X(U)$.
 
 * Do you need still more information to guess my space $X$? It turns out that: no, this information is enough!
This somewhat remarkable fact is closely related to a 
fundamental statement of [[category theory]]: the [[Yoneda lemma]] and its implication on [[representable functor]]s.
 
 * But, on the other hand, you need to be sure that even if I  won't reveal my space $X$ to you directly, the little information about it which I do provide I should provide honestly and consistently. Some consistency checks to assure that I am not just making things up
 but am giving you consistent information about my secret space $X$ are the following:
 
   * it must be true that if you hand me the identity map $Id_U : U \to U$
   on a test space, that then then I return you the identity map 
   $Id_{X(U)} : X(U) \to X(U)$ on the set of probes of $X$ by $U$. 
   
   * also, it must be true that if you first hand me two consecutive maps of test
   spaces, $f : U \to V$ and $g : V \to W$, and then hand me their composite
   $g \circ f : U \to W$, that my reply $X(g \circ f) : X(W) \to X(U)$ to the latter
   is the result of composing my two replies about the former:
   $X(g \circ f) = X(W) \stackrel{X(g)}{\to} X(V) \stackrel{X(f)}{\to} X(U)$.
   
   * so far, an assignment $U \mapsto X(U)$ of sets to spaces which satisfies the above two properties is what is called a [[presheaf]]: this, in turn, is nothing but what is called a [[functor]] on a [[category]].

   * But there is one further, more nontrivial consistency check on my information which you should do: it must be true that you can piece together the information which I give for small test spaces to deduce information about probes by bigger test spaces. More precisely, if I tell you the set $X(U)$ of probes of my secret space $X$ by the test space $U$, and if you then chop up $U$ into two pieces $V_1$ and $V_2$  sitting inside $U$ by inclusion maps $p_i : V_i \hookrightarrow U$, with a bit of overlap $V_1 \cap V_2$, then it ought
   to be true all the probes by $U$ in $X(U)$ can be entirely and exactly reconstructed
   from taking probes by $V_1$ in $X(V_1)$ and by $V_2$ in $X(V_2)$ and see if they match
   over the overlap $V_1 \cap V_2$ of the two small probes: 
   in symbols, the collection of
   pairs in $\{matching maps from V_1 and V_2\} \hookrightarrow
   X(V_1) \times X(V_2)$ whose elements coincide when restricted to the overlap
   $X(V_1) \times X(V_2) \stackrel{\to}{\to} X(V_1 \cap V_2)$ should be exactly all the possible maps in $X(U)$
   $$
     \{matching maps on V_1 and V_2\} \simeq X(U)
     \,.
   $$
   
* this is a sensible game to play: I don't tell you directly
which space $X$ I am thinking of, but I give you all the information
about its probes $U \mapsto X(U)$ by test spaces, subject to these three 
consistency conditions. Such a collection of information (the sets $X(U)$)
subject to these consistency conditions is called a **[[sheaf]]**
on the collection (being a [[category]]) $S$ of test spaces. 

  * More generally, this notion of sheaf easily makes sense on every other category $S$ for which there is an agreement about how some of its elements $U$, can be covered by other elements, such as the $V_1$ and $V_2$ above. Such an agreement of what counts as a [[cover]] in a [[category]] is called a [[coverage]], and a [[category]] equipped with such an information is called a [[site]].

* and it turns out that, indeed, if I am sticking to these rules of sheaves, then you can reconstruct the space $X$ that I am thinking of from just the information about how to probe it by other spaces.


## sheaves more general than spaces ##

* So far this just reformulates the familar notion of space in a somewhat more indirect form: a rule for how to probe a space. But now something nice happens: it turns out that there are collections of this probe information $U \mapsto X(U)$ which do obey the rules 
(satisfies the three conditions above) but for which there is nevertheless _no_ _ordinary_ space $X$ that it describes probes into;

* on the other hand, maybe this just means that our notion of "ordinary space" was a bit too restrictive: after all, we noticed that all that really matters usually are the 
ways we can probe a given space by other spaces; and
that the information about such probes is useful if only
it obeys the above three consistency rules;

* so we regard sheaves in general then as generalized spaces; or more precisely: we regard sheaves as rules for how to  probe generalized spaces, and we take these generalized spaces to be entirely specified by their possible probes.

* it turns out that every important type of operation on spaces has its analogs as an operation on sheaves: one says that  sheaves form a [[topos]]: a place where we can go 
to study generalized [[homotopy theory]], 
more general than the place of topological spaces, but where
still all the crucial constructions familiar from topological spaces makes sense;

## higher sheaves: $\infty$-stacks ##

* But once we are at this point, we should go even a bit further: we have been talking about _sets_ of probes $X(U)$. But of course 
for $X$ a true [[topological space]] and $U$ a [[topological space]], there
is not just a set, but a [[topological space]] of maps $U \to X$. 
So we should be looking at sheaves with values in topological spaces.

* There is only one thing we need to take care of, then: since a 
topological spaces ia a bit more flexible than a plain set, 
we should be a bit careful about when two sheaves $U \mapsto X(U)$
with values in topological spaces are to be regarded as
equal for all practical purposes: recall that $X(U)$ is
to be thought of as the space of all ways of mapping a probe
space $U$ into a space $X$. Its not the single points (maps) in this
space which matter so much, but they way they hang together. 

  * All "ways of hanging together" in a topological space $X(U)$
  are measured by a collection of groups called the 
  [[homotopy group]]s $\pi_n(X(U))$, one for each natural number $n$.
  
  * So if we are being careful, we should recognize that two sheaves
  $X : U \mapsto X(U)$ and $Y : Y \mapsto Y(U)$ must characterize
  essentially the same generalized space if there is a rule
  $f : X \to Y$ for turning for each test space $U$, probes of $X$ into 
  probes of $Y$, $f_U : X(U) \to Y(U)$
  such that for _sufficiently small_ $U$ this comparison map of
  probe spaces does not change the homotopy groups, i.e. so that
  all homomorphism $\pi_n(f_U) : \pi_n(X(U)) \to \pi_n(X(V))$
  are isomorphisms of groups. One says that such $f_U$ is a [[weak homotopy equivalence]].
  
  * If a comparison map $f : X \to Y$ exists with these properties, then one says that our
  generalized spaces $X$ and $Y$ defined by these sheaves are
  _weakly equivalent_ or [[quasi-isomorphism|quasi-isomorphic]] 
  
* There are several ways to deal with this complication that 
sheaves with values in topological spaces are very flexible, so flexible
that it may require a bit of effort to determine if two of them 
determine the same generalized space, for all practical purposes. 


  * One nice way to deal with it is to again go back to our attitude that everything 
should be determined by how we map other things into it: if 
$f : X \to Y$ is a weak equivalence of sheaves, as above, then we
we would expect that for $Z$ any other sheaf, the induced map 
of spaces of probes $Z(f) : Z(Y) \to Z(X)$
of $Z$ by $X$ and $Y$ is a [[weak homotopy equivalence]].
Now, that may fail to be true, simply because we are using
an awkward realization of the sheaf $Z$. It may be that we have
to straighten out $Z$ a bit, without really changing it, for the above
to be true. Indeed, there is always a sheaf of topological spaces
$Z'$ which is equivalent to $Z$, but for which the above consistency condition
is true: the map $Z'(f) : Z'(Y) \to Z'(X)$ between spaces of probes
of $Z'$ by $X$ and by $Y$ is a homotopy equivalence.

  * The sheaves with this niceness property are called [[infinity-stack]]s
  of [[(infinity,1)-sheaf|(infinity,1)-sheaves]]. Recall that despite the
  fancy terminology, these things are nothing but consistent rules 
  for something that may be probed with test spaces $U$, $V$,...


## generalized cohomology ##

* We come back to our original motivation. Recall that we were looking
at cohomology groups of spaces $X$ by mapping $X$ into other spaces.
We noticed that there is in general interesting information about
$X$ which cannot be gained by mapping it into an ordinary topological
spaces. Starting from this we have now arrived at a more general notion 
of space, called a higher sheaf or an $\infty$-stack.

* So let's state for the record that we succeeded: we will say now for 
$X$ and $A$ generalized spaces, $\infty$-stacks, that the 
collection of maps
$$
  H(X,A) := [X,A]
$$
from $X$ to $A$ is the [[cohomology]] of $X$ with coefficients in $A$.

* Indeed, one finds that despite their enlarged generality, these $\infty$-stacks
behave in all relevant aspects just like ordinary sheaves and ordinary
topological spaces do. So one says that $\infty$-stacks form an [[infinity-topos]]
(more precisely: an [[(infinity,1)-topos]]): a place where we can go in order
to do the familiar [[homotopy theory]} of topological spaces in a more
general context.


  
##  complexes of sheaves: abelian $\infty$-stacks  ##

* Another term for this [[generalized cohomology]] theory thus obtained is
[[nonabelian cohomology]]. The reason for that terms is a historic
one: before arriving at the full picture of higher topos theory as 
described here, people had a pretty good guess about some aspects of
this story, and this aspect they called 
[[abelian sheaf cohomolohy|sheaf cohomology]]. It turns out that 
sheaf cohomology is precisely the _abelian_ part of general cohomology.
So now general cohomology is sometimes called [[nonabelian cohomolohy]]
to distinguish it from the more traditional cohomology theory. 

* Here is what "abelian part of general cohomology" means:

  * For many sheaves that appear in practice, the topological space
  $X(U)$ assigned to any test space $U$ is not just a topological space,
  but happens to have the structure of an abelian group, too. 
  
  * In this case a cascade of simplifications kicks is: first of all,
  such topological spaces, by a special case of something called the 
  [[homotopy hypothesis]] (which is really a precise theorem) 
  can be identified with simplicial abelian groups. 
  
  * Second, by another theorem called the [[Dold-Kan correspondence]],
  simplicial abelian groups are equivalently encoded more simply
  in the collection of data given by
  (non-positively graded) chain complexes in abelian groups.
  
* By an [[abelian sheaf]] one means a sheaf $U \mapsto X(U)$ which
takes values in [[chain complex]]es of abelian groups
(or,  more generally,, in [[complex]]es in another [[abelian category]]).
Under the above correspondences, we understand this as a special case
of a sheaf with values in topological spaces. 

* By [[abelian sheaf cohomology]] one means nothing but the above
general [[Higher Topos Theory|higher topos theoretic]] notion of
cohomology given by the simple idea of collections of maps from 
one generalized space to another. Only that in the special
case of abelian sheaves a wealth of particular computational
techniques are used to compute these mapping spaces
(such as [[derived category|derived categories]] and 
[[derived functor|derived functors]]) which are not available in the
fully general case. This whealth of computational machinery
employed, useful as it is, sometimes hides the simple conceptual
reasoning underlying everything.
  
## Examples ##

* Recall that we started the search for a generalized notion of space
motivated by the fact that a circle bundle on a space $X$ may be
encoded by a map from $X$ to some topological space $B U(1)$, but
that the same was not true for circle bundles _with connection_.
We had wanted to obtain a generalized notion of space such that 
this is remedied.

  * Indeed, this is now the case. There is a famous 
  abelian sheaf, called the second [[Deligne complex]], which has precisely
  the property that maps from a manifold $X$ into it classify circle bundles
  with connection on $X$.
  
  * more....
  
  
  ...