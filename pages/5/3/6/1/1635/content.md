#Contents#
* automatic table of contents goes here
{:toc}

# Idea #

Recall that a [[Kan complex]] is a special [[simplicial set]] that [[homotopy hypothesis|behaves like]] a combinatorial model for a [[topological space]].


The _simplicial homotopy groups_ of a Kan complex (actually a *[[pointed object|pointed]]* Kan complex) are accordingly the combinatorial analog of the [[homotopy groups]] of [[topological spaces]]: instead of being maps from topological spheres modulo maps from topological disks, they are maps from the [[boundary of a simplex]] modulo those from the [[simplex]] itself. Of course, they only tell you something about the connected component of the Kan complex that contains the base vertex, so sometimes it is assumed that $X$ is connected, but see below!

Accordingly, the definition of the discussion of simplicial homotopy groups is essentially literally the same as that of ordinary [[homotopy groups]].  One technical difference is for instance that the definition of the group structure is slightly more non-immediate for simplicial homotopy groups than for topological homotopy groups (see below).

As for ordinary homotopy groups, an $n$th simplicial homotopy 'group' is really an $n$-[[k-tuply groupal n-groupoid|tuply groupal]] $0$-[[0-groupoid|groupoid]].  That is, for $n = 0$, it is not a group at all but rather a [[pointed set]]; for $n = 1$, it is a [[group]]; and for $n \geq 2$, it is an [[abelian group]].  On the other hand, we could drop the base vertex and move to the $n$th simplicial homotopy 'groupoid', which is really an $n$-[[n-groupoid|groupoid]].  

+-- {: .query}

[[Urs Schreiber|Urs]]: This statement is important and useful for the analogous situation with homotopy groups of topological spaces. Here for Kan complexes it has a different flavor, and I find it more subtle in that it becomes more tautological: For notice that in a sensible sense the fundamental $\infty$-groupoid of a Kan complex is nothing but the Kan complex itself! In fact, every Kan complex arises up to equivalence as the fundamental $\infty$-groupoid of a topological space. And one nice way to think of the homotopy groups of topological spaces is as the homotopy groups of their fundamental $\infty$-groupoids. 

So if one were to strictly follow the perspective of the above paragraph, the concept would become a bit empty.

In contrast to that I think that for simplicial homotopy groups the point really is to have them as groups and not as groupoids, for here they are a tool and means to characterize $\infty$-groupoids and in particular their weak equivalence classes.\

[[Tim Porter|Tim]]:  I sort of agree. The point may be that the Kan complex $\infty$-groupoid is quite difficult to analyse and the homotopy groups provide a good first step in that process.  Here we are at the interface between the interests of infinity category theory and homotopy theory. The tools of algebraic topology such as the homotopy groups tell us only a tiny bit about the overall infinity category structure, but they do tell us something, and I believe one good thing to come out of the Lab may be to provide some ways of interpreting between the two areas. I disagree however that the homotopy groups are somehow better than groupoids except that the *family* of all n-th homotopy groups of $X$ can either be thought of as a family or as the disjoint union groupoid of its members! I am thinking ahead to the operation of the fundamental groupoid on that family. WHich should be prefered, homotopy groups as family, homotopy groups as groupoids or homotopy groups as modules over the fundamental groupoid!  I do not know.

Eventually I have wanted to bridge the gap between simplicial groups / inifity groupoids etc., and the Pi algebras studied by David Blanc and others.  These consist of the homotopy groups plus the actions of the fundamental group(oid) and the primary homotopy operations. I do not yet know how to link up each of those structures with the infinity cat viewpoint.

=--

By a special case of the [[delooping hypothesis]] (a case known to be true for many if not all practical definitions of $n$-groupoid), every pointed (that is, $0$-tuply groupal) $n$-groupoid has an $n$-tuply groupal $0$-groupoid, which gives the connection between these.

If we restrict to $X$ being connected (and pointed), then $\pi_0(X)$ will be just a single point. If we allow a pointed $X$ which is not connected, then $\pi_0$ will tell us how many connected components there are, but $\pi_n$ for $n \gt 0$ will only give information about the connected component of the base vertex. There are various ways out of this dilemma, and going towards a groupoid-based definition is a good one in our context. Most basically, we can chose a base vertex in each component and obtain (for every $n$, even $n = 0$) a [[groupoid]] which is a disjoint union of groups. Or we could choose all vertices at once and include the [[fundamental groupoid]] information on change of base vertices along edges ($1$-simplices), and there are various intermediate and other alternative forms. Few give us groups, but we will still, perhaps, stubbornly use the terminology of homotopy 'groups', so as not to confuse things too much. Which version you need, depends on the use it is being put to.


#Definition# 

Recall the classical [[model structure on simplicial sets]]. Let $X$ be a fibrant simplicial set, i.e. a [[Kan complex]].  

Define


* the **$0$th simplicial homotopy groupoid** $\Pi_0(X)$ to be the [[discrete category|discrete groupoid]] on the _set_ $(X_0/X_1)$ of connected components of $X$, i.e. on the set of equivalence classes of 0-cells under [[simplicial homotopy]];

  * for each vertex, $x \in X_0$, the [[pointed set]] $\pi(X,x)$ to be the set $(X_0/X_1)$ with point the connected component $[x]$ of $x \in X_0$; this is actually a special case of the following definition, until the group structure.

+-- {: .query}
  I would like the set of connnected components to be the simplicial homotopy $0$-group*oid* $\Pi_0(X)$, while the $0$th simplicial homotopy 'group' itself is (like the following) a property of a *pointed* space: $\pi_0(X,x)$ is the [[pointed set]] $\Pi_0(X)$ equipped with the component of $x$ as point.  That way, the $n$th simplicial homotopy group is really an $n$-[[k-tuply groupal n-groupoid|tuply groupal]] set, as I\'ve done at [[homotopy group]].  (This also becomes strictly a special case of the general definition below, not an exception.)  ---Toby

*  [[Tim Porter|Tim]]: Good point.  In fact the simplicial homotopy groups are defined for _pointed_ simplicial sets, not for arbitrary ones. The traditional terminology is sloppy, since there is usually a caveat that everything is connected, except when it is not, that is.
 
   On the other hand, the idea of a 0th simplicial homotopy *group* is incorrect as it is not a group. Perhaps the trick of putting inverted commas to indicate that it is 'as if but not really' could be used.  

   Of course, there are really two homotopy theories, the pointed one and the non-pointed one.  The first leads to groups, the second to groupoids.

[[Urs Schreiber|Urs]]: I have now tried to implement Toby's comment, as far as it applies to the above. I am not sure though precisely what [[Tim Porter|Tim]]'s comment about pointed simplicial sets is aiming at: if we have a pointed simplicial set we can just talk about $\pi_n(X)$, true, but here we are being more general and talk about $\pi_n(X,x)$ for all $x  \in X$. No? 

*  [[Tim Porter|Tim]]: My point is that the intro refers to the _homotopy groups_ of a Kan complex.  The body of the entry makes it clear that there is one such for each vertex of the Kan complex, which is what Toby is considering. *Homotopy group of $X$* is thus a misnomer. (I am being pedantic in other words!) Saying the n-th homotopy group of $X$ at $x$ does not get around the difficulty, since then one is specifying a pointed complex not just the complex itself.

   I think that Toby's viewpoint is excellent. Perhaps the homotopy group(oids)s are really 'relative' concepts, i.e.  defined for $X$ and a cofibration, $A\to X$, and the usual ones just have $A$ a point. (If I remember rightly this viewpoint was the one adopted by Baues at least to some extent.) The usual groupoidal case is with the terminal cofibration.  I think that this idea is linked to the fact that SSet is monadic over SplitAugSSet, but that can be a very stark but useful viewpoint to adopt. (It would not be favoured by most algebraic topologists however!) 
 
[[Urs Schreiber|Urs]]: I see. Sure, sounds good. Do you want to go ahead and change the terminology as you deem appropriate?

I might have just one minor quibble: while I'd be fine with it, I have to say that it seems that of the following two equivalent sentences, the former is less awkward:

* a morphism $f : X \to Y$ of fibrant simplicial sets is a weak equivalences precisely if it induces an isomorphism on all homotopy groups based at all points of $X$

* a morphism $f : X \to Y$ of fibrant simplicial sets is a weak equivalences precisely if for all  possible ways to interpret $X$ as a pointed simplicial space and for the corresponding structure of a pointed simplicial space induced by $f$ on $Y$, the morphism induces an isomorphism of homotopy groups.

But okay, I am not dogmatic about issues at that fine-grained level of pedantery.

=--

* for every $n \geq 1$ and $x \in X_0$ the **$n$th simplicial homotopy group** of $X$ at $x$ to be the set 

  * of equivalence classes of morphisms
  $$
    \alpha : \Delta^n \to X
  $$ 
  from the simplicial $n$-[[simplex]] $\Delta^n$ to $X$, 

    * such that they fit into the diagram
    $$
      \array{
        \partial \Delta^n &\to&  \Delta^0
        \\
        \downarrow && \downarrow
        \\
        \Delta^n &\stackrel{\alpha}{\to}& X
      };
    $$
    meaning that all of the boundary of $\Delta^n$ maps to the single point $x$;

  * where two such maps $\alpha, \alpha'$ are taken to be equivalent is they are related by a [[simplicial homotopy]] $\eta$
    $$
      \array{
        \Delta^n
        \\
        \downarrow^{i_0} & \searrow^{\alpha}
        \\
        \Delta^n \times \Delta^1
        &\stackrel{\eta}{\to}&
        X
        \\
        \uparrow^{i_1} & \nearrow_{\alpha'}
        \\
        \Delta^n 
      }
    $$

   * that fixes the boundary
     $$
       \array{
         \partial \Delta^n \times \Delta^1 
         &\to&
         \Delta^0
         \\
         \downarrow && \downarrow
         \\
         \Delta^n  \times \Delta^1
         &\stackrel{\eta}{\to}&
         X
       }
       \,.
     $$

These pointed sets are taken to be equipped with the following group structure.

+-- {: .un_defn}
###### Definition (group structure on $\pi_n(X,x)$)
  
Let $n \geq 1$. For 
$f,g : \Delta^n \to X$ two representatives
of $\pi_n(X,x)$, define the following $n$-simplices in $X_n$:

$$
  v_i =
  \left\{
    \array{
      s_0 \circ s_0 \circ \cdots \circ s_0 (x) & for 0 \leq i \leq  n-2
      \\
      f & for i = n-1
      \\
      g & for i = n+1
    }
  \right.
$$

This is designed such that it yields a morphism $\Lambda^{n+1}_n \to X$ from a [[horn]] of the $(n+1)$-[[simplex]] into $X$. By the [[Kan complex]] property of $X$ this morphism has an extension $\theta$ through the $(n+1)$-[[simplex]] $\Delta^n$
$$
  \array{
     \Lambda^{n+1}_n &\to& X
     \\
     \downarrow & \nearrow_{\theta}
     \\
     \Delta^{n+1}
  }
$$
From the [[simplicial identities]] one finds that the boundary of the $n$-simplex arising as the $n$th boundary piece $d_n \theta$ of $\theta$ is constant on $x$
$$
  d_i d_{n} \theta = d_{n-1} d_i \theta = x
$$

So $d_n \theta$ represents an element in $\pi_n(X,x)$ and we define the product operation by

$$
  [f]\cdot [g] := [d_n \theta]
  \,.
$$

=--

*Remark*: All the degenerate $n$-simplices $v_{0 \leq i \leq n-2}$ above are just there so that the gluing of the two $n$-cells $f$ and $g$ to each other can be regarded as forming the boundary of an $(n+1)$-simplex except for one face. BY the Kan extension property that missing face exists, namely $d_n \theta$.  This is a choice of gluing composite of $f$ with $g$.

+-- {: un_lemma}
###### Lemma

The above product on homotopy group elements is
indeed well defined, in that it is independent of the
choice of representatives $f$, $g$ and of the extension $\theta$.

=--



+-- {: un_lemma}
###### Lemma

For $n \geq 2$ all the groups $\pi_n(X,x)$ are abelian.
=--




# Weak homotopy equivalences of Kan simplicial sets#

For $X$ and $Y$ [[model structure on simplicial sets|fibrant]] simplicial sets, i.e. [[Kan complexes]], a morphism $f : X \to Y$ is a weak equivalence with respect to the classical [[model structure on simplicial sets]] if 

$$
  f_* : \pi_0(X) \to \pi_0(Y)
$$

and

$$
  f_* : \pi_n(X,x) \to \pi_n(Y,f(x))
$$

are [[isomorphisms]] for all choices of base vertex $x \in X_0$.



#Homotopy groups via Kan's loop group construction#

Another way to get the group structure on the homotopy groups of  a Kan complex, $X$, is via its [[Dwyer-Kan loop groupoid]] and the [[Moore complex]]. This gives a [[simplicial groupoid|simplicially enriched groupoid]] $G(X)$, or if we restricted to the pointed case, and just look at the loops at the base vertex, a simplicial group. (We will assume for the sake of simplicity that $X$ is _reduced_, that is to say, $X_0$ is a singleton, and thus that $G(X)$ is a simplicial group.)

The construction of $G(X)$ is then given by  the free group functor on the various levels, shifted by 1, and with a twist in the zeroth face map (see [[Dwyer-Kan loop groupoid]] and simplify to the reduced case.) 



+-- {: .un_prop}
###### Proposition

There is an isomorphism between $\pi_n(X)$ as defined above and $H_{n-1}(N G(X))$, the $(n-1)$th homology group of the [[Moore complex]] of the simplicial group, $G(X)$.
=--

+-- {: .query}
The fact that the n-1th homology of $NG(X)$ is $\pi_n(X)$ in the reduced case is, for me, a strong argument to **define** the type of object that should be studied to be $H_{n-1}(NG(X))$ in general, that is to take ALL the base points at once and to consider the result as a groupoid which is the disjoint union of the homotopy groups at the various base points. That leads to a neat theory when you look for models of homotopy n-types.  If 'properly' done the $\pi_1$ is then the fundamental groupoid, and you get all the change of base point actions in the same set of machinery. What do you all think?  _ Tim

[[Urs Schreiber|Urs]]: Sounds very good. Maybe you can eventually rearrange the entry to make that the viewpoint to start with and derive the more traditional description from that.

[[Tim Porter|Tim]]: The thing I like about that approach is that it combines the idea of algebraic processes (concatenation of the strings in the free groupoids) and the recombination via geometric simplices in higher dimensions giving rewrites.  That is a good neat elegant combination.
=--


# Examples #

+-- {: .un_lemma }
###### Lemma

Let $C$ be a [[groupoid]] and $\mathcal{N}(C)$ its [[nerve]].

Then 

* $\pi_0 \mathcal{N}(C,c)$ is the set of isomorphism classes of $C$ with the class of $c$ as base point

* $\pi_1 \mathcal{N}(C,c)$ is the [[automorphism group]] $Aut_C(c)$ of $c$

* $\pi_{n \geq 2} \mathcal{N}(C,c)$ is trivial

=--

In particular a [[functor]]
$f : C \to D$ of [[groupoids]] is a [[equivalence of categories]] if under the nerve it induces a weak equivalence $\mathcal{N}(f) : \mathcal{N}(C) \to \mathcal{N}(D)$ of [[Kan complexes]]:

* that $\pi_0 \mathcal{N}(f,c) : \pi_0(C,c) \to \pi_0(D,f(c))$ is an isomorphism implies that $f$ is an [[essentially surjective functor]] and is implied by $f$\'s being a [[full functor]];
* that $\pi_1 \mathcal{N}(f,c) : \pi_1(C,c) \to \pi_1(D,f(c))$ is an isomorphism is equivalent to $f$\'s being a [[full and faithful functor]].


#References#

A standard textbook reference is

[chapter 1](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi) of 

* **GoerJard**, Goerss, Jardine, _Simplicial homotopy theory_ 

Originally homotopy groups of simplicial sets had been defined in terms of the ordinary [[homotopy groups]] of the [[topological spaces]] [[geometric realization|realizing]] them. Apparently the first or one of the first discussions of the purely combinatorial definition is 

* D. Kan, _A combinatorial definition of homotopy groups_ ([jstor](http://www.jstor.org/stable/1970006?seq=8))

[[!redirects simplicial homotopy groups]]