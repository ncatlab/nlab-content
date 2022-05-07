+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea##

The **simplex category** $\Delta$ encodes one of the main [[geometric shapes for higher structures]]. Its objects are the standard cellular $n$-[[simplices]]. It is also called the _[[simplicial category]]_, but that term is ambiguous.

## Definition ##
 {#Definition}

+-- {: .num_defn }
###### Definition

The **augmented simplex category** $\Delta_a$ is the [[full subcategory]] of [[Cat]] on the [[free categories]] of [[finite set|finite]] linear [[directed graphs]]

$$
  \{c_0 \to c_1 \to \cdots \to c_n\}
  \,.
$$

Equivalently, this is the category whose [[objects]] are finite [[total order|totally ordered sets]], or finite ordinals, and whose [[morphisms]] are order-preserving functions between them. 

=--

\begin{rmk} As a consequence of the equivalent description, $\Delta_a$ can be viewed as a full sub-[[2-poset]] of [[Pos]]. \end{rmk}

+-- {: .num_defn }
###### Definition

The **simplex category** $\Delta$ is the [[full subcategory]] of $\Delta_a$ (and hence of $Cat$) consisting of the free categories on finite and **[[inhabited set|inhabited]]** linear directed graphs, hence of  _non-empty_ finite linear orders or _non-zero_ ordinals.

=--

+-- {: .num_remark }
###### Remark

It is common, convenient and without risk to use a [[skeleton]] of $\Delta$ or $\Delta_a$, where we pick a fixed representative in each [[isomorphism class]] of objects. Since isomorphisms of finite linearly ordered sets are _unique_ this step is so trivial that it is often not even mentioned explicitly.

With this the objects of $\Delta$ are in bijection with [[natural numbers]] $n \in \mathbb{N}$ and one usually writes 

$$
  [n] = \{0 \to 1 \to \cdots \to n\}
$$

for the object of $\Delta$ given by the category with $(n+1)$ [[object]]s. Geometrically one may think of this as the [[spine]] of the standard cellular $n$-[[simplex]], see the discussion of [simplicial sets](#SimplicialSets) below. In this context one also writes $\Delta[n]$ or $\Delta^n$ for the [[simplicial set]] [[representable functor|represented]] by the object $[n]$: the simplicial $n$-[[simplex]]. By the [[Yoneda lemma]] one may identify the subcategory of simplicial sets on the $\Delta[n]$ with $\Delta$.

With this convention the first few objects of $\Delta$ are

$$
  [0] = \{0\}
$$

$$
  [1] = \{0 \to 1\}
$$

$$
  [2] = \{0 \to 1 \to 2\}
$$

etc.

The category $\Delta_a$ contains one more object, corresponding to the empty category $\emptyset$. When sticking to the above standard notation for the objects of $\Delta$, that extra object is naturally often denoted 

$$
  [-1] = \emptyset
  \,.
$$ 

However, in contexts where only $\Delta_a$ and not $\Delta$ plays a role, some authors prefer to start counting with 0 instead of with $-1$. Then for instance the notation

$$
  \mathbf{0} = \emptyset
$$

$$
  \mathbf{1} = [0] =  \{0\}
$$

$$
  \mathbf{2} = [1]  = \{0 \to 1\}
$$

and generally

$$
  \mathbf{n} = [n-1]
$$

may be used.

=--

+-- {: .num_prop }
###### Proposition

The [[skeleton|skeletal]] version of the **augmented simplex category** $\Delta_a$ can be presented as follows:

* objects are the finite totally ordered sets $\mathbf{n} \coloneqq \{0 \lt 1 \lt  \cdots \lt n-1\}$ for all $n \in \mathbb{N}$;

* morphisms  _generated_ by (are all expressible as finite compositions of) the following two elementary kinds of maps

  1. **face maps**: $\;\delta_i^n :\: \mathbf{n-1} \hookrightarrow \mathbf{n}\;$ is the injection whose image leaves out $i \in [n]\quad $ ($n \gt 0$ and $0 \leq i \lt n$);

  1. **degeneracy maps**: $\;\sigma_i^n :\: \mathbf{n+1} \to  \mathbf{n}\;$ is the surjection such that $\sigma_i(i) = \sigma_i(i+1) = i\quad $ ($n \gt 0$ and $0 \leq i \lt n$);

subject to the following relations, called the **simplicial relations** or **[[simplicial identities]]**:

$$
  \array{
     \delta_i^{n+1} \circ \delta_j^n
     =
     \delta_{j+1}^{n+1}\circ \delta_i^n
     &
     \qquad i \leq j
     \\
     \sigma_j^n \circ \sigma_i^{n+1}
     =
     \sigma_i^n \circ \sigma_{j+1}^{n+1}
     &
     \qquad i \leq j
  }
$$
$$
  \sigma_j^n \circ \delta_i^{n+1}
  =
  \left\lbrace
    \array{
      \delta_i^n \circ \sigma_{j-1}^{n-1}
      &
      \qquad i \lt j 
      \\
      Id_n
      &
      \qquad i = j \;or\; i = j+1
      \\
      \delta^n_{i-1} \circ \sigma_{j}^{n-1}
      &
      \qquad j+1 \lt i
    }
  \right.
$$
whenever $i, j$ are chosen so that the maps are defined. For example, in 
$$\delta_i^{n+1} \circ \delta_j^n
     =
     \delta_{j+1}^{n+1}\circ \delta_i^n
$$
we implicitly require      $0 \leq i, j \leq n$.

=--

## Properties

### Monoidal structure 
 {#ordinal sum}

The addition of [[natural number]]s extends to a [[functor]] $\oplus : \Delta_a \times \Delta_a \to \Delta_a$  and $\oplus : \Delta \times \Delta \to \Delta$, by taking $\mathbf{m} \oplus \mathbf{n}$ to be the [[disjoint union]] of the underlying sets of $\mathbf{m}$ and $\mathbf{n}$, with the linear order that extends those on $\mathbf{m}$ and $\mathbf{n}$ by putting every element of $\mathbf{m}$ below every element of $\mathbf{n}$. This is called the _[[ordinal sum]]_ functor. If we visualise $\mathbf{n}$ as a totally ordered set $\{0 \lt 1 \lt \cdots \lt n-1\}$, and similarly for $\mathbf{m}$, then $\mathbf{m} \oplus \mathbf{n}$ looks like

$$
\mathbf{m} \oplus \mathbf{n} = \{0 \lt 1 \lt  \cdots \lt m-1 \lt 0^*\lt 1^* \lt \cdots \lt (n-1)^*\}
$$

where $k^*$ denotes $k$ considered as an element of $\mathbf{n}$.

Clearly $\oplus : \Delta_a \times \Delta_a \to \Delta_a$ acts on objects as
$$
  \mathbf{n} \oplus \mathbf{m} = \mathbf{n+m},
$$

On morphisms, given $f : \mathbf{m} \to \mathbf{m}'$ and $g : \mathbf{n} \to \mathbf{n}'$, we have 
$$
  (f\oplus g)(i) = \left\lbrace
     \array{
       f(i) & if \; 0 \leq i  \leq m - 1
       \\
       m' + g(i-m) & if \; m \leq i \leq (m+n-1)
     }
  \right.
  \,.
$$
so that $f \oplus g$ can be visualised as $f$ and $g$ placed side by side.

It is easy to see now that $(\Delta_a,\oplus,\mathbf{0})$ is a [[strict monoidal category]].

It is important to note that this tensor does _not_ give a monoidal structure to $\Delta$, as that category does not contain the unit $\mathbf{0} = [-1] = \emptyset$.

Also note that this [[monoidal structure]] is _not_ [[braided monoidal category|braided]]!  One does have isomorphisms $\mathbf{m} \oplus \mathbf{n} \simeq \mathbf{n+m} \simeq \mathbf{n} \oplus \mathbf{m}$ for all $m,n$, but it has to be the identity on $\mathbf{n+m}$, and that is not [[bifunctorial]].

Under [[Day convolution]] this monoidal structure induces the [[join of simplicial sets]].

### $\Delta$ and $\Delta_a$ as 2-categories 
 {#As2Categories}

Being full subcategories of the [[2-category]] $Cat$, $\Delta$ and $\Delta_a$ are themselves 2-categories: their [[2-cell|2-cells]] $f \Rightarrow g$ are given by the pointwise order on monotone functions.  Equivalently, they are generated under (vertical and [[horizontal composition|horizontal]]) composition by the inequalities
$$ \delta^n_{i+1} \leq \delta^n_i \qquad \qquad \sigma^n_i \leq \sigma^n_{i+1} \, .$$
Of course, the ordinal sum functor $\oplus$ extends to a [[2-functor]] in the obvious way.

For each $n$ there is [a string of adjunctions](https://ncatlab.org/nlab/show/adjoint+string)
$$
  \delta^n_{n-1} \dashv \sigma^n_{n-2} \dashv \delta^n_{n-2} \dashv
  \cdots \dashv \delta^n_1 \dashv \sigma^n_0 \dashv \delta^n_0
$$
where the counit of $\sigma_i \dashv \delta_i$ and the unit of $\delta_{i+1} \dashv \sigma_i$ are identities.

For each $n \geq 2$, the object $\mathbf{n+1}$ is given by the [[pushout]]
$$
\array{
\mathbf{n-1} & \overset{\delta_0}{\to} & \mathbf{n} \\
\mathllap{\scriptsize{\delta_{n-1}}} \downarrow & & \downarrow \mathrlap{\scriptsize{\delta_n}} \\
\mathbf{n} & \underset{\delta_0}{\to} & \mathbf{n+1}
}
$$

This means that $\Delta_a$ is generated as a 2-category by these pushouts and by taking adjoints of morphisms.  Its monoidal structure is also determined in this way: for each $n$, write $\bot_n = \delta_{n-1}\cdots\delta_2\delta_1$ for the (morphism $\mathbf{1} \to \mathbf{n}$ corresponding to the) least element $0$ of $\mathbf{n}$, and $\top_n = \delta_0\cdots\delta_0\delta_0$ for the greatest.  Then there are [[cospans]] $\mathbf{1} \to \mathbf{n} \leftarrow \mathbf{1}$ given by $\top_n$ and $\bot_n$, and each such is equivalent to the $(n-1)$ fold cospan composite (i.e. pushout) of $\mathbf{1} \to \mathbf{2} \leftarrow \mathbf{1}$ with itself.  The ordinal sum $\mathbf{n} \oplus \mathbf{m}$ is given by the composite
$$
\array{
  & & & & \mathbf{n} \oplus \mathbf{m} & & & & \\
  & & & \nearrow & & \nwarrow & & & \\
  & & \mathbf{n} & & & & \mathbf{m} & & \\
  & \nearrow & & \nwarrow & & \nearrow & & \nwarrow & \\
  \mathbf{1} & & & & \mathbf{1} & & & & \mathbf{1}
}
$$
The universal property of pushouts, together with those of the initial and terminal objects $\mathbf{0},\mathbf{1}$, then suffices to define $\oplus$ as a 2-functor.

### Universal properties 

The morphisms $\mathbf{0} \overset{\delta_0}{\to} \mathbf{1} \overset{\sigma_0}{\leftarrow} \mathbf{2}$ in $\Delta_a$ make $\mathbf{1}$ into a [[monoid object]].  Indeed, it is easy to see that
$$
\begin{aligned}
\delta^n_i & = \mathbf{i} \oplus \delta^0_0 \oplus \mathbf{n-i} \\
\sigma^n_i & = \mathbf{i} \oplus \sigma^1_0 \oplus \mathbf{n-i-1}
\end{aligned}
$$
so that the morphisms of $\Delta_a$ are generated under $\circ$ and $\oplus$ by $\delta^0_0$ and $\sigma^1_0$, together with exactly the equations needed to make them the structure maps of the monoid $[1]$.  The objects of $\Delta_a$ are the elements of the free monoid generated by $\mathbf{1}$ and $\oplus$.

$\Delta_a$ thus becomes the universal category-equipped-with-a-monoid, in the sense that for any strict monoidal category $B$, there is a bijection between monoids $(M,m,e)$ in $B$ and strict [[monoidal functors]] $\Delta_a \to B$ such that $\mathbf{1} \mapsto M$, $\sigma_0 \mapsto m$ and $\delta_0 \mapsto e$.

In particular, for $K$ a 2-category, [[monads]] in $K$ correspond to 2-functors $\mathbf{B}\Delta_a \to K$, where $\mathbf{B}\Delta_a$ is $\Delta_a$ considered as a one-object 2-category.  Because monads in $K$ are also the same as [[lax functors]] $1 \to K$, this correspondence exhibits $\mathbf{B}\Delta_a$ as the [[lax morphism classifier]] for the terminal category $1$.

When $\Delta_a$ is considered as a 2-category, a similar argument to the above shows that the one-object [[3-category]] $\mathbf{B}\Delta_a$ classifies [[lax-idempotent monads]]: given a 3-category $M$ and a lax-idempotent monad $t$ therein, there is a unique 3-functor $\mathbf{B}\Delta_a \to M$ sending $[1]$ to $t$, essentially because $\sigma^1_0 \dashv \delta^1_0 = \delta^0_0 \oplus \mathbf{1}$ with identity counit.


### Duality with intervals  
 {#DualityWithIntervals}

Recall that an [[interval]] is a [[linearly ordered set]] with a top and bottom element; interval maps are [[monotone functions]] which preserve top and bottom. 

Parallel to the categories $\Delta$ and $\Delta_a$, let $\nabla$ denote the category of finite intervals where the top and bottom elements are _distinct_, and let $\nabla_a$ denote the category of all finite intervals, including the terminal one where top and bottom coincide. Then we have [[duality|concrete dualities]], or equivalences of the form  

$$\Delta_a^{op} \simeq \nabla_a; \qquad \Delta^{op} \simeq \nabla,$$ 

both induced by the [[duality|ambimorphic object]] $\mathbf{2}$, seen as both an ordinal and an interval. In other words, we have in each case an adjoint equivalence 

$$Int(-, \mathbf{2})^{op} \dashv Ord(-, \mathbf{2})$$ 

inducing the first equivalence $Ord(-, \mathbf{2}): \Delta_a^{op} \to \nabla_a$, and the second equivalence by restriction. 

This fact is mentioned in ([Joyal](#Joyal)), to help give some intuition for his [[Theta category|category]] $\Theta$ as dual to a category of disks. See also _[Interval -- Relation to simplices](interval#RelationToSimplices)_, and the section on dualities in ([Wraith](#Wraith)).

### Combinatorics

The homogenous symmetric function $h_m(x_1,x_2,{\dots},x_n)$ is the generating function for the set of all morphisms from $[m-1]$ to $[n-1]$.

As an order-preserving function between finite ordinals, any morphism $f : \mathbf{m} \to \mathbf{n}$ in $\Delta_a$ is completely specified by fixing $k$ elements of $\mathbf{n}$ as the [[image]] of $f$, together with a [[partition#of_numbers|composition]] of $\mathbf{m}$ into $k$ parts, each part denoting a non-empty, contiguous subset of elements of $\mathbf{m}$ sharing their value of $f$. That is, each such composition is given by a collection of $k$ interval parts $[0,i_1], [i_1 + 1, i_2], \ldots, [i_{k-1}+1, m-1]$, determined by a $(k-1)$-element subset $\{i_1, \ldots, i_{k-1}\}$ of an $(m-1)$-element set $\{0, \ldots, m-2\}$. Hence, there are a total of

$$
\sum_k \binom{n}{k} \binom{m-1}{k-1} = \sum_k \binom{n}{k} \binom{m-1}{m-k} = \binom{n+m-1}{m}
$$

different morphisms of type $\mathbf{m} \to \mathbf{n}$ in $\Delta_a$, where we obtain the expression on the right by applying the [[Chu–Vandermonde identity]].  For example, there are 

$$
\binom{2}{1}\binom{2}{0} + \binom{2}{2}\binom{2}{1} = 2+2 = 4 = \binom{4}{3}
$$

different morphisms $\mathbf{3} \to \mathbf{2}$, corresponding to the four functions

1. $f(0) = f(1) = 0, f(2) = 1$
1. $f(0) = 0, f(1) = f(2) = 1$
1. $f(0) = f(1) = f(2) = 0$
1. $f(0) = f(1) = f(2) = 1$

The [stars and bars argument](https://en.wikipedia.org/wiki/Stars_and_bars_%28combinatorics%29) gives a direct [[bijective proof]] of the identity $|\Delta_a(\mathbf{m},\mathbf{n})| = \binom{n+m-1}{m}$: see [this comment](http://nforum.ncatlab.org/discussion/3636/number-of-morphisms-in-the-simplex-category/?Focus=29835#Comment_29835) on the nForum.

As some interesting special cases, taking $m=n$ gives the number of monotone endofunctions on $\mathbf{n}$ (OEIS sequence [A088218](https://oeis.org/A088218), or [A001700](https://oeis.org/A001700) if we consider endomorphisms $[n] \to [n] \in \Delta$), while taking $m=2$ gives the triangular numbers (OEIS sequence [A000217](https://oeis.org/A000217)).

### Extra Degeneracies

In some applications, in addition to the usual maps in the simplex category, one has "extra degeneracies" whose key property can be described as constructing an [[absolute limit]] of shape $\Delta$.

Let $\Delta_\bot \subseteq \Delta$ be the [[wide subcategory]] spanned by the functors that preserve minima. Equivalently, $\Delta_\bot \subseteq \Delta_*$ is the full subcategory of pointed objects of the form $(S, \bot_S)$ where $\bot_S$ is the minimum of $S$.

+-- {: .num_prop }
###### Proposition

$1 \oplus - : \Delta_a \to \Delta_\bot$ is an [[absolute limit]] cone in the sense of [[(∞,1)-categories]] (and thus in the sense of ordinary categories).

=--

+-- {: .proof}
###### Proof

By the characterization of absolute limits by representable functors, we need to show every $\Delta_\bot(1 \oplus -, m) : \Delta_a^{\op} \to \infty Grpd$ is a colimit cocone. Observe $\Delta_\bot(1 \oplus -, m) \cong \Delta_a(-, m)$. Since the cone point is $\Delta_a(0, m) = *$, we need to show that the colimit of the simplicial [[∞-gropuoid]] $\Delta(-, m)$ is contractible. Since the colimit (in simplicial ∞-gropuoids) of a simplicial set  is the precisely its homotopy type, the theorem follows from the fact that $\Delta^{m-1}$ is a contractible simplicial set.

=--

Since the retract of an absolute limit is again an absolute limit, we can generalize. Define $\Delta_x$ by the pushout in $(\infty,1)Cat$:

$$
\begin{matrix}
\Delta_a^{\leq 0} \times \Delta_a &\xrightarrow{\oplus}& \Delta_a
\\ \!\!\!\!\!\!\!\!\!\!\!\!(1 \oplus -) \times id \downarrow
& & \downarrow \iota\!
\\ \Delta_\bot^{\leq 1} \times \Delta_a &\xrightarrow{\rho}& \Delta_x
\end{matrix}
$$

+-- {: .num_prop }
###### Proposition

$\iota : \Delta_a \to \Delta_x$ is an [[absolute limit]] cone in the sense of [[(∞,1)-categories]] (and thus in the sense of ordinary categories).

=--

+-- {: .proof}
###### Proof

$\rho$ transposes to a retraction diagram in the category of augmented simplicial objects of $\Delta_x$. This retraction expresses $\iota$ as a retract of the functor $\Delta_a \xrightarrow{1 \oplus -} \Delta_\bot \subseteq \Delta_a \xrightarrow{\iota} \Delta_x$. Since the first map is an absolute limit, so is the composite.

=--

The homotopy category $h \Delta_x$ has a similar property.

To mesh with the usual description of extra degeneracies, the categories $\Delta_\bot$ and $h \Delta_x$ can be given by


+-- {: .num_prop }
###### Proposition

Let $\mathbf{C}$ be the category constructed from $\Delta_a$ by adjoining arrows $s_{-1} : m \to (m+1)$ for all $m \geq 0$, and by imposing the cosimplicial identities

* $s_{-1} d_0 = 1$
* $s_{-1} d_{k+1} = d_k s_{-1}$ for $k \geq 0$
* $s_{-1} s_{k+1} = s_k s_{-1}$ for $k \geq 0$

Then the monomorphism $1 \oplus - : \Delta_a \to h \Delta_x$ extends to an equivalence $\mathbf{C} \to h \Delta_x$.

Let $\mathbf{C}'$ be constructed by imposing the remaining cosimplicial identity
$s_{-1} s_0 = s_{-1} s_{-1}$. Then $1 \oplus - : \Delta_a \to \Delta_\bot$
extends to an equivalence $\mathbf{C}' \to \Delta_\bot$.

=--

+-- {: .proof }
###### Proof idea

The case of $\mathbf{C}'$ follows by the same argument showing that $\Delta$ is presented by the face and degeneracy maps modulo the cosimplicial identities by an algorithm reducing arrows to a normal form. The key observation is that a map of $\Delta$ is contained in $\Delta_\bot$ iff its normal form does not contain any copies of $d_0$.

The case of $\mathbf{C}$ can be determined by working through the construction of $h \Delta_x$ as a pushout of ordinary categories.

=--

The construction of $h \Delta_x$ from $\Delta_a$ consists of the usual definition of "extra degeneracies". The construction of $\Delta_\bot$ from $\Delta_a$ can be described as having "strong extra degeneracies".


## Related constructions ##

### Simplicial sets 
 {#SimplicialSets}

[[presheaf|Presheaves]] on $\Delta$ are [[simplicial set|simplicial sets]]. Presheaves on $\Delta_a$ are **[[augmented simplicial sets]]. 

Under the [[Yoneda embedding]] $Y : \Delta \to $ [[SSet]] the object $[n]$ induces the standard simplicial $n$-[[simplex]] $Y([n]) =: \Delta^n$. So 
in particular we have $(\Delta^n)[m] = Hom_{\Delta}([m],[n])$ and hence 
$\Delta^n[m]$ is a finite set with $\binom{n+m+1}{n}$ elements. 

The face and degeneracy maps and the relation they satisfy are geometrically best understood in terms of the [[full and faithful functor|full and faithful]] image under $Y$ in [[SSet]]: 

* the face map $Y(\delta_i) : \Delta^{n-1} \to \Delta^{n}$ injects the standard simplicial $(n-1)$-simplex as the $i$th face into the standard simplicial $n$-simplex;

* the degeneracy map $Y(\sigma_i) : \Delta^{n+1} \to \Delta^{n}$ projects the standard simplicial $(n+1)$-simplex onto the standard simplicial $n$-simplex by collapsing its vertex number $i$ onto the face opposite to it.

#### Extra degeneracies

Presheaves on $\Delta_x$ are _(augmented) simplicial sets with extra degeneracies_,
and presheaves on $\Delta_a$ are _(augmented) simplicial sets with strong extra degeneracies_. The key feature is

+-- {: .num_prop }
###### Proposition

If an augmented simplicial object $P : \Delta_a^{op} \to C$ can be extended to $\Delta_x^{op} \to C$, then $P$ is a colimit diagram.

=--

### Realization and nerve
 {#RealizationAndNerve}

There are important standard functors from $\Delta$ to other categories which _[[nerve and realization|realize]]_ $[n]$ as a concrete model of the standard $n$-[[simplex]]. 

* The functor $\Delta[-] : \Delta \to $ [[sSet]] (the [[Yoneda embedding]]) realizes $[n]$ as a [[simplicial set]].


* The functor $|\cdot| : \Delta \to $ [[Top]]

  sends $[n]$ to the standard topological $n$-simplex $[n] \mapsto \{(x_0, ... x_n) : 0 \leq x_0 \leq x_1 \leq \cdots \leq x_n \leq 1\}\subset \mathbb{R}^{n}$. This functor induced [[geometric realization]] of [[simplicial sets]].

* The functor $O : \Delta \to Str\omega Cat $
  sends $[n]$ to the $n$th [[oriental]]. This induces simplicial [[nerves]] of [[omega-category|omega-categories]].

  Under the functor $Str \omega Cat \to Cat$ which discards all higher morphisms and identifies all 1-morphisms that are connected by a 2-morphisms, this becomes again the identification of $\Delta$ with the full subbcategory of $Cat$ on linear [[quivers]] that we started the above definition with

  $$
    [n] \mapsto \{0 \to 1 \to \cdots \to n\}
    \,.
  $$

## Related concepts

* [[geometric shapes for higher structures]]

  * **simplex category**

  * [[cube category]]

  * [[globe category]]

  * [[cell category]]

  * [[Segal's category]]

* [[simplicial set]]

* [[augmented simplicial set]]

* [[join of simplicial sets]]

## References

An early description of the simplex category is in

* {#Grothendieck61} [[Alexander Grothendieck]], p. 107 (10 of 21) in: _Techniques de construction et théorèmes d'existence en géométrie algébrique III : préschémas quotients_, Séminaire Bourbaki : années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf))

See also the references at [[simplicial set]].

See also:

* Section VII.5 of [[Categories Work|Categories for the Working Mathematician]]

* Section II.2 of P. Gabriel and M. Zisman, _Calculus of Fractions and Homotopy Theory_. Springer, 1967

* Section 2, Doctrines, of [[Ross Street]], [_Fibrations in Bicategories_](http://www.numdam.org/item?id=CTGDC_1980__21_2_111_0), 1980 

The relation to [[intervals]] and the generalization to the [[cell category]] is due to

* [[André Joyal]], _Disks, duality and $\Theta$-categories_, preprint, 1997 ([pdf](http://ncatlab.org/nlab/files/JoyalThetaCategories.pdf))
 {#Joyal}

A discussion of the opposite categories of $\Delta, \Delta_a$ and related categories can be found here:

* [[Gavin C. Wraith]], _Using the generic interval_, Cah. Top. G&#233;om. Diff. Cat. **XXXIV** 4 (1993) pp.259-266. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1993__34_4/CTGDC_1993__34_4_259_0/CTGDC_1993__34_4_259_0.pdf))
 {#Wraith}

[[!redirects augmented simplex category]]


category: category