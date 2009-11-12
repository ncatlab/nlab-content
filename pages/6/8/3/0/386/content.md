[[!redirects augmented simplex category]]

#Contents#
* automatic table of contents goes here
{:toc}

##Idea##

The **simplex category** $\Delta$ encodes one of the main [[geometric shapes for higher structures]]. Its objects are the standard cellular $n$-[[simplex|simplices]]. It is also called the [[simplicial category]], but that term is ambiguous.

##Definition##

* The __simplex category__ $\Delta$ is the [[full subcategory]] of [[Cat]] consisting of the [[finite set|finite]] [[inhabited set|inhabited]] linear [[quiver]]s.
$$
  \{c_0 \to c_1 \to \cdots \to c_n\}
  \,.
$$


* Equivalently: $\Delta$ is the category of finite inhabited [[total order|totally ordered set]]s and order-preserving functions between them.

### Detailed description ###

In more details, $\Delta$ looks as follows.

First of all, it is common, convenient and without risk to use a [[skeleton]] of $\Delta$, where we pick a fixed representative in each isomorphism class of objects. Since isomorphisms of totally ordered sets are _unique_ this step is so trivial that it is often not even mentioned explicitly.

Often the _simplex category_ is defined to be the following [[skeleton]]:

* objects are the finite totally ordered sets $[n] := \{0 \lt 1 \lt  \cdots \lt n\}$ for all $n \in \mathbb{N}$;

* morphisms are order-preserving functions $[n] \to [m]$ -- these are _generated_ by (are all expressible as finite compositions of) the following two elementary kinds of maps

  * **face maps**: $\delta_i := \delta_i^n : [n-1] \hookrightarrow [n]$ is the injection missing $i \in [n]$;

  * **degeneracy maps**: $\sigma_i := \sigma_i^n : [n+1] \to  [n]$ is the surjection such that $\sigma_i(i) = \sigma_i(i+1) = i$.

These morphism generate $\Delta$ subject to the following relations, called the **simplicial relations**

$$
  \array{
     \delta_j^{n+1} \circ \delta_i^n
     =
     \delta_i^{n+1}\circ \delta_{j-1}^n
     &
     for i \lt j
     \\
     \sigma_j^n \circ \delta_i^{n+1}
     =
     \sigma_i^{n-1} \circ \sigma_{j+1}^n
     &
     for i \leq j
  }
$$
$$
  \sigma_j^n \circ \delta_i^{n+1}
  =
  \left\lbrace
    \array{
      \delta_i^n \circ \sigma_{j-1}^{n-1}
      &
      if i \lt j
      \\
      Id_n & if i = j or i = j+1
      \\
      \delta^n_{i-1} \circ \sigma_{j}^{n-1}
      &
      if i \gt j +1
    }
  \right.
$$


##Remarks##

### simplicial sets ###

[[presheaf|Presheaves]] on $\Delta$ are [[simplicial set|simplicial sets]]. 

Under the [[Yoneda embedding]] $Y : \Delta \to $ [[SSet]] the object $[n]$ induces the standard simplicial $n$-[[simplex]] $Y([n]) =: \Delta^n$.

The face and degeneracy maps and the relation they satisfy are geometrically best understood in terms of the [[full and faithful functor|full and faithful]] image under $Y$ in [[SSet]]: 

* the face map $Y(\delta_i) : \Delta^{n-1} \to \Delta^{n}$ injects the standard simplicial $(n-1)$-simplex as the $i$th face into the standard simplicial $n$-simplex;

* the degeneracy map $Y(\sigma_i) : \Delta^{n+1} \to \Delta^{n}$ projects the standard simplicial $(n+1)$-simplex onto the standard simplicial $n$-simplex by collapsing its vertex number $i$ onto the face opposite to it.



### augmented simplex category ###

* Often, it is highly convenient to extend the category $\Delta$ to contain also the empty totally ordered set $[-1] := \emptyset$. This is called the _augmented_ simplex category $\Delta_a$, and presheaves on it are **augmented simplicial sets**. The category $\Delta_a$ may be characterized as the initial strict monoidal category equipped with a monoid; the monoidal product is **ordinal sum**, and the monoidal unit is the empty ordinal. This style of definition also opens up the possibility of using string diagrams to visualize the structure of $\Delta_a$ and of the [[cube category]] $\Box$. 


## monoidal structure ##

The idea of addition of natural numbers extends, and adapts, to give a [[tensor product]]-type functor on both $\Delta$ and $\Delta_a$. If we visualise an object, $[n]$ of $\Delta$, as above, as a totally ordered set
$\{0 \lt 1 \lt  \cdots \lt n\}$, then from two such $[m]$ and $[n]$, we can form a new one by making all the elements of $[n]$, strictly greater than those in $[m]$. (It can be convenient to adopt the following notational device here. Add an ${}^*$ to each element of $[n]$ just as a label (a different font would serve the same purpose), so we form a new ordinal $[m]+[n] = \{0 \lt 1 \lt  \cdots \lt m \lt 0^*\lt 1^* \lt  \cdots \lt n^*\}$.) Clearly we have 
$$
  + : \Delta \times \Delta \to \Delta
$$

acts on objects 

$$
  [n] + [m] = [n + m + 1],
$$

but that is not really where the subtleties  are apparent, they are clearer with the morphisms. On morphisms given $f : [m] \to [m']$ and $g : [n] \to [n']$, we have 

$$
  (f+g)(i) = \left\lbrace
     \array{
       f(i) & if 0 \leq i  \leq m
       \\
       g(i-m-1) + m' + 1 & if m \lt i \leq (m+n+1)
     }
  \right.
  \,.
$$

It is important to note that this tensor does _not_ give a monoidal structure to $\Delta$, as it does not have a unit.  The unit that would be needed would be the empty ordinal, and, as that _is_ there in $\Delta_a$, that does become a monoidal category.


Under [[Day convolution]] this monoidal structure induces the [[join of simplicial sets]].

+--{.query}
[[Tim Porter|Tim]]: a neat notation for the ordinal sum is $\oplus$ read as 'o plus' with 'o' recalling 'ordinal' and 'plus .... . In editing the above I did not change the pre-existing notation, but would have liked to!
=--


#### realization and nerve ####

There are important standard functors from $\Delta$ to other categories which _realize_ $[n]$ as a concrete model of the standard $n$-[[simplex]].

* The functor
$$
  |\cdot| : \Delta \to Top
$$
sends $[n]$ to the standard topological $n$-simplex $[n] \mapsto \{x_0 \leq x_1 \leq \cdots \leq x_n \leq 1\}\subset \mathbb{R}^{n}$. This functor induced [[geometric realization]] of [[simplicial set]]s.

* The functor
$$
  O : \Delta \to Str\omega Cat  
$$
sends $[n]$ to the $n$th [[oriental]]. This induces simplicial [[nerve]]s of [[omega-category|omega-categories]].

Under the functor $Str \omega Cat \to Cat$ which discards all higher morphisms and identifies all 1-morphisms that are connected by a 2-morphisms, this becomes again the identification of $\Delta$ with the full subbcategory of $Cat$ on linear [[quiver]]s that we started the above definition with

$$
  [n] \mapsto \{0 \to 1 \to \cdots \to n\}
  \,.
$$

##References##

see the references at [[simplicial set]].

***

##Discussion##

An earlier version of this entry started the following discussion:

[[Todd Trimble|Todd]] _says_: Historically, and especially for algebraic topologists, $\Delta$ refers to the category of nonempty totally ordered sets and order-preserving maps; an adjective like "augmented" would be attached to "simplicial object" if they wanted to refer to a contravariant functor coming out of what is being defined here as $\Delta$. While I understand arguments why one might wish to redefine $\Delta$ this way, there are also countervailing arguments (cf. Tom's Caf&#233; post How I Came to Love the Nerve Construction); in any event, given the weight of history, the "sometimes" strikes me as inappropriate understatement. I think more discussion is called for before we appropriate $\Delta$ for the lesser-used concept, and rename the more commonly used one as $\Delta$ with a dot over it (do other people use that notation?). 

_[[Urs Schreiber|Urs]]:_ I have tried to change the entry accordingly now. 

_[[Todd Trimble|Todd]]:_ Having said all of the above, I myself prefer (on conceptual grounds) to treat the category of all finite ordinals (Ross Street used to call it "algebraists' $\Delta$") as the primary concept, and the category of finite nonempty ordinals ("topologists' $\Delta$") as secondary. It's just that I worried about introducing confusion, since my own opinion may well be a minority opinion. 

_[[Mike Shulman|Mike]]_: I think there are many good reasons, including but not limited to tradition, to give the unadorned name to the topologists' $\Delta$.  In my experience, in most applications to [[homotopy theory]], the topologists' $\Delta$ is the important object, both conceptually and mathematically, with its augmented version playing at most a technical role occasionally.  And while the augmented $\Delta$ does have a cute universal property as a monoidal category, the category of simplicial sets (presheaves on the unaugmented $\Delta$) also has a good universal property: it is the [[classifying topos]] for linear orders.

_[[Todd Trimble|Todd]]_: Not meaning to nitpick, Mike, since you raise good points, but I believe "linear order" in your sense should mean "linear order with distinct top and bottom". (See for instance the discussion in Mac Lane-Moerdijk.) Presheaves on the augmented $\Delta$ would give the classifying topos for "linear orders with top and bottom" (not necessarily distinct). (If you want just plain linear orders, I think you'd use presheaves on $\Delta_a^{op}$.) 

_Mike_: Yes, of course.

_Toby_: I certainly prefer the algebraists\' $\Delta$; it\'s part of my general preference for not ignoring the [[empty set]]. (Mike\'s example, with Todd\'s correction, only serves to confirm my opinion.) Seeing the universal construction of $\Delta$, I made the article consistent by picking my favourite, which fit that construction.

I didn\'t know a good notation for the topologists\' unaugmented $\Delta$, so I just used a dot as my standard notation for deleting the basepoint: if $X$ is a [[pointed set]] with point $x$, then $\dot X := X \setminus \{x\}$. (I think that I first saw this in point-set topology to turn a neighbourhood of a point into a deleted neighbourhood.) It is by no means sacred.

category: category