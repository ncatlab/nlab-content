[[!redirects augmented simplex category]]

#Contents#
* automatic table of contents goes here
{:toc}

##Idea##

The **simplex category** $\Delta$ encodes one of the main [[geometric shapes for higher structures]]. Its objects are the standard cellular $n$-[[simplex|simplices]]. It is also called the [[simplicial category]], but that term is ambiguous.

##Definition##

* The **augmented simplex category** $\Delta_a$ is the [[full subcategory]] of [[Cat]] consisting of the [[finite set|finite]] linear [[quivers]], or equivalently the category of finite [[total order|totally ordered sets]], or finite ordinals, and order-preserving functions between them:
$$
  \{c_0 \to c_1 \to \cdots \to c_n\}
  \,.
$$

* The **simplex category** $\Delta$ is the [[full subcategory]] of $\Delta_a$ (and hence of $Cat$) consisting of the finite **[[inhabited set|inhabited]]** linear quivers, non-empty linear orders or non-zero ordinals.

### Details ###

First of all, it is common, convenient and without risk to use a [[skeleton]] of $\Delta$ or $\Delta_a$, where we pick a fixed representative in each isomorphism class of objects. Since isomorphisms of totally ordered sets are _unique_ this step is so trivial that it is often not even mentioned explicitly.

#### The augmented simplex category $\Delta_a$

With the above in mind, the augmented simplex category $\Delta_a$ can be presented as follows:

* objects are the finite totally ordered sets $[n] := \{0 \lt 1 \lt  \cdots \lt n-1\}$ for all $n \in \mathbb{N}$;

* morphisms are order-preserving functions $[n] \to [m]$ -- these are _generated_ by (are all expressible as finite compositions of) the following two elementary kinds of maps

  * **face maps**: $\delta_i := \delta_i^n : [n-1] \hookrightarrow [n]$ is the injection whose image leaves out $i \in [n]$;

  * **degeneracy maps**: $\sigma_i := \sigma_i^n : [n+1] \to  [n]$ is the surjection such that $\sigma_i(i) = \sigma_i(i+1) = i$.

These morphisms generate $\Delta_a$ subject to the following relations, called the **simplicial relations** or **simplicial identities**:

$$
  \array{
     \delta_j^{n+1} \circ \delta_i^n
     =
     \delta_i^{n+1}\circ \delta_{j-1}^n
     &
     for i \lt j
     \\
     \sigma_j^n \circ \sigma_i^{n+1}
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


#### The unaugmented simplex category $\Delta$

The category $\Delta$ is given by the full subcategory of $\Delta_a$ that leaves out $[0]$.  Usually the objects are reindexed to start from 0, so that $[n] \in \Delta = [n+1] \in \Delta_a$.  Authors who use the unaugmented category then often retain this numbering for $\Delta_a$, writing $[-1]$ for its initial object $\{\,\}$.

## Monoidal structure ##

The addition of natural numbers extends to a [[tensor product]]-type functor on both $\Delta$ and $\Delta_a$. If we visualise an object, $[n]$ of $\Delta_a$, as above, as a totally ordered set
$\{0 \lt 1 \lt  \cdots \lt n-1\}$, then from two such $[m]$ and $[n]$, we can form a new one by making all the elements of $[n]$ strictly greater than those in $[m]$.  Thus
$$
[m] \oplus [n] = \{0 \lt 1 \lt  \cdots \lt m-1 \lt 0^*\lt 1^* \lt \cdots \lt (n-1)^*\}
$$
where $k^*$ denotes $k$ considered as an element of $[n]$.

Clearly $\oplus : \Delta \times \Delta \to \Delta$ acts on objects as
$$
  [n] \oplus [m] = [n + m],
$$
On morphisms, given $f : [m] \to [m']$ and $g : [n] \to [n']$, we have 
$$
  (f\oplus g)(i) = \left\lbrace
     \array{
       f(i) & if 0 \leq i  \leq m - 1
       \\
       m' + g(i-m) & if m \lt i \leq (m+n-1)
     }
  \right.
  \,.
$$
so that $f \oplus g$ can be visualised as $f$ and $g$ placed side by side.

It is easy to see now that $(\Delta_a,\oplus,[0])$ is a [[strict monoidal category]].

It is important to note that this tensor does _not_ give a monoidal structure to $\Delta$, as it does not have a unit.  The unit that would be needed would be the empty ordinal, and, as that _is_ there in $\Delta_a$, that does become a monoidal category.

Under [[Day convolution]] this monoidal structure induces the [[join of simplicial sets]].

## $\Delta$ and $\Delta_a$ as 2-categories ##

Being full subcategories of the [[2-category]] $Cat$, $\Delta$ and $\Delta_a$ are themselves 2-categories: their [[2-cells]] $f \Rightarrow g$ are given by the pointwise order on monotone functions.  Equivalently, they are generated under (vertical and [[horizontal composition|horizontal]]) composition by the inequalities
$$ \delta^n_{i+1} \leq \delta^n_i \qquad \qquad \sigma^n_i \leq \sigma^n_{i+1} \, .$$
Of course, the ordinal sum functor $\oplus$ extends to a [[2-functor]] in the obvious way.

For each $n$ there is a string of [[adjunctions]]
$$
  \delta^n_{n-1} \dashv \sigma^n_{n-2} \dashv \delta^n_{n-2} \dashv
  \cdots \dashv \delta^n_1 \dashv \sigma^n_0 \dashv \delta^n_0
$$
where the counit of $\sigma_i \dashv \delta_i$ and the unit of $\delta_{i+1} \dashv \sigma_i$ are identities.

For each $n \geq 2$, the object $[n+1]$ is given by the [[pushout]]
$$
\array{
[n-1] & \overset{\delta_0}{\to} & [n] \\
\mathllap{\scriptsize{\delta_{n-1}}} \downarrow & & \downarrow \mathrlap{\scriptsize{\delta_0}} \\
[n] & \underset{\delta_0}{\to} & [n+1]
}
$$

This means that $\Delta_a$ is generated as a 2-category by these pushouts and by taking adjoints of morphisms.

## Remarks ##

### Simplicial sets ###

[[presheaf|Presheaves]] on $\Delta$ are [[simplicial set|simplicial sets]], and presheaves on $\Delta_a$ are **augmented** simplicial sets.

Under the [[Yoneda embedding]] $Y : \Delta \to $ [[SSet]] the object $[n]$ induces the standard simplicial $n$-[[simplex]] $Y([n]) =: \Delta^n$.

The face and degeneracy maps and the relation they satisfy are geometrically best understood in terms of the [[full and faithful functor|full and faithful]] image under $Y$ in [[SSet]]: 

* the face map $Y(\delta_i) : \Delta^{n-1} \to \Delta^{n}$ injects the standard simplicial $(n-1)$-simplex as the $i$th face into the standard simplicial $n$-simplex;

* the degeneracy map $Y(\sigma_i) : \Delta^{n+1} \to \Delta^{n}$ projects the standard simplicial $(n+1)$-simplex onto the standard simplicial $n$-simplex by collapsing its vertex number $i$ onto the face opposite to it.


#### realization and nerve ####

There are important standard functors from $\Delta$ to other categories which _realize_ $[n]$ as a concrete model of the standard $n$-[[simplex]].

* The functor
$$
  |\cdot| : \Delta \to Top
$$
sends $[n]$ to the standard topological $n$-simplex $[n] \mapsto \{x_0 \leq x_1 \leq \cdots \leq x_n \leq 1\}\subset \mathbb{R}^{n}$. This functor induced [[geometric realization]] of [[simplicial sets]].

* The functor
$$
  O : \Delta \to Str\omega Cat  
$$
sends $[n]$ to the $n$th [[oriental]]. This induces simplicial [[nerves]] of [[omega-category|omega-categories]].

Under the functor $Str \omega Cat \to Cat$ which discards all higher morphisms and identifies all 1-morphisms that are connected by a 2-morphisms, this becomes again the identification of $\Delta$ with the full subbcategory of $Cat$ on linear [[quivers]] that we started the above definition with

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