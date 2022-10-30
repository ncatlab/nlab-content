
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 

The notion of _[[2-congruence]]_ is the generalization of the notion of _[[congruence]]_ from [[category theory]] to [[2-category theory]]. 

The correct notions of _[[regular 2-category|regularity]] and [[exact 2-category|exactness]]_ for [[2-categories]] is one of the subtler parts of the theory of first-order structure.  In particular, we need a suitable replacement for the 1-categorical notion of _[[equivalence relation]]_.  The (almost) correct definition was probably first written down in [[StreetCBS]].

One way to express the idea is that in an [[n-category]], every [[object]] is [[internal logic|internally]] a $(n-1)$-category; exactness says that conversely every "internal $(n-1)$-category" is represented by an object.  When $n=1$, an "internal 0-category" means an internal _equivalence relation_; thus exactness for 1-categories says that every equivalence relation is a kernel (i.e. is represented by some object).  Thus, we need to find a good notion of "[[internal category|internal 1-category]]" in a 2-category.

Of course, there is an obvious notion of an internal category in a 2-category, as a straightforward generalization of [[internal category|internal categories]] in a 1-category.  But internal categories in [[Cat]] are [[double categories]], so we need to somehow cut down the [[double categories]] to those that really represent honest [[1-categories]].  These are the _2-congruences_.


## Definition 

Before we define 2-congruences below in def. \ref{2Congruence}, we need some preliminaries.

### 2-Congruence

+--{: .num_defn #HomWiseDiscreteInternalCategory}
###### Definition

If $K$ is a finitely complete 2-category, a **homwise-discrete category** in $K$ consists of 

* a [[discrete morphism]] $D_1\to D_0\times D_0$, together 

* with composition and identity maps $D_0\to D_1$ and $D_1\times_{D_0} D_1\to D_1$ in $K/(D_0\times D_0)$, 

which satisfy the usual axioms of an [[internal category]] up to [[isomorphism]].  

Together with the evident notions of **[[internal functor]]** and **internal [[natural transformation]]** there is a [[2-category]] $HDC(K)$ of hom-wise discrete 2-categories in $K$.

=--

+--{: .num_remark}
###### Remark

Since $D_1\to D_0\times D_0$ is discrete, the structural isomorphisms will automatically satisfy any [[coherence]] axioms one might care to impose.

=--

+--{: .num_remark}
###### Remark


The transformations between functors $D\to E$ are a version of the notion for internal categories, thus given by a morphism $D_0\to E_1$ in $K$. The 2-cells in $K(D_0,E_0)$ play no explicit role, but we will recapture them below.  

=--

+--{: .num_remark}
###### Remark


By homwise-discreteness, any "[[modification]]" between transformations is necessarily a unique isomorphism, so (after performing some quotienting, if we want to be pedantic) we really have a 2-category $HDC(K)$ rather than a [[3-category]].

=--

+--{: .num_defn #Kernel}
###### Definition


If $f:A\to B$ is any morphism in $K$, there is a canonical homwise-discrete category $(f/f) \to A\times A$, where $(f/f)$ is the [[comma object]] of $f$ with itself.  We call this the **kernel** $ker(f)$ of $f$ (the "comma [[kernel pair]]" or "comma [[Cech nerve]]" of $f$).  

In particular, if $f=1_A$ then $(1_A/1_A) = A^{\mathbf{2}}$, so we have a canonical homwise-discrete category $A^{\mathbf{2}} \to A\times A$ called the **kernel** $ker(A)$ of $A$.  

=--

+--{: .num_remark}
###### Remark

It is easy to check that taking kernels of objects defines a functor $\Phi:K \to HDC(K)$; this might first have been noticed by [Street](http://www.springerlink.com/content/407n62422140864p/).

=--

+--{: .num_theorem #Folding}
###### Theorem 

If $D_1\,\rightrightarrows\, D_0$ is a homwise-discrete category in $K$, the following are equivalent.

1. $D_0 \leftarrow D_1 \to D_0$ is a [[two-sided fibration]] in $K$.

1. There is a functor $\ker(D_0)\to D$ whose object-map $D_0\to D_0$ is the identity.

=--

Actually, homwise-discreteness is not necessary for this result, but we include it to avoid worrying about [[coherence]] isomorphisms, and since that is the case we are most interested in here.

+--{: .proof}
###### Proof
We consider the case $K=Cat$; the general case follows because all the notions are defined representably.   A homwise-discrete category in $Cat$ is, essentially, a [[double category]] whose horizontal 2-category is homwise-discrete (hence equivalent to a [[1-category]]).  We say "essentially" because the pullbacks and diagrams only commute up to isomorphism, but up to equivalence we may replace $D_1\to D_0\times D_0$ by an [[isofibration]], obtaining a (pseudo) double category in the usual sense.  Now the key is to compare both properties to a third: the existence of a [[companion pair|companion]] for any vertical arrow.

Suppose first that $D_0 \leftarrow D_1 \to D_0$ is a two-sided fibration.  Then for any (vertical) arrow $f:x\to y$ in $D_0$ we have [[cartesian morphism|cartesian]] and [[opcartesian morphisms]] (squares) in $D_1$:

\[
  \array{
     x & \overset{id}{\to} & x 
       & \qquad  &
     x & \overset{f_1}{\to} & y' 
     \\
      {}^{\mathllap{\cong}}\downarrow & opcart &  \downarrow^{\mathrlap{f}} 
       & \qquad  &
     {}^{\mathllap{f}}\downarrow & cart &  \downarrow^{\mathrlap{\cong}}
     \\
     x' & \overset{f_2}{\to} & y 
      & \qquad &
    y & \overset{id}{\to} & y
  }
\]

The vertical arrows marked as isomorphisms are so by one of the axioms for a two-sided fibration.  Moreover, the final compatibility axiom for a 2-sided fibration says that the square
\[
\array{ x & \overset{f_1}{\to} & y'\\
  \cong \downarrow & & \downarrow\cong \\
  x' & \overset{f_2}{\to} & y,}
\]
induced by factoring the horizontal identity square of $f$ through these cartesian and opcartesian squares, must be an isomorphism.  We can then show that $f_1$ (or equivalently $f_2$) is a [[companion pair|companion]] for $f$ just as in ([Shulman 07, theorem 4.1](#Shulman07)).  Conversely, from a [[companion pair]] we can show that $D_0 \leftarrow D_1 \to D_0$ is a two-sided fibration just as as in [loc cit](#Shulman07).

The equivalence between the existence of companions and the existence of a functor from the kernel of $D_0$ is essentially found in ([Fiore 06](#Fiore06)), although stated only for the "edge-symmetric" case.  In their language, a kernel $ker(A)$ is the double category $\Box A$ of commutative squares in $A$, and a functor $ker(D_0)\to D$ which is the identity on $D_0$ is a _thin structure_ on $D$.  In one direction, clearly $ker(D_0)$ has companions, and this property is preserved by any functor $ker(D_0)\to D$.  In the other direction, sending any vertical arrow to its horizontal companion is easily checked to define a functor $ker(D_0)\to D$.

=--

In particular, we conclude that up to isomorphism, there can be at most one functor $ker(D_0)\to D$ which is the identity on objects.

+--{: .num_defn #2Congruence}
###### Definition
A **2-congruence** in a finitely complete [[2-category]] $K$ is a homwise-discrete category, def. \ref{HomWiseDiscreteInternalCategory} in $K$ satisfying the equivalent conditions of Theorem \ref{Folding}.
=--


+--{: .num_example}
###### Example

The kernel $ker(A)$, def. \ref{Kernel} of any object is a 2-congruence.  

More generally, the kernel $ker(f)$ of any morphism is also a 2-congruence.

=--

### 2-Forks and Quotients 

The idea of a 2-fork is to characterize the structure that relates a morphism $f$ to its kernel $ker(f)$.  The kernel then becomes the universal 2-fork on $f$, while the _quotient_ of a 2-congruence is the couniversal 2-fork constructed from it.

+--{: .num_defn}
###### Definition
A **2-fork** in a 2-category consists of a 2-congruence $s,t:D_1\;\rightrightarrows\; D_0$, $i:D_0\to D_1$, $c:D_1\times_{D_0} D_1\to D_1$, and a morphism $f:D_0\to X$, together with a 2-cell $\phi:f s \to f t$ such that $\phi i = f$ and such that
$$\array{
  D_1\times_{D_0} D_1 & \to & D_1 & = & D_1\\
  \downarrow && \downarrow & \Downarrow_\phi & \downarrow\\
  D_1 & \to & D_0 && D_0\\
  || &\Downarrow_\phi && \searrow^f & \downarrow f\\
  D_1 & \to & D_0 & \overset{f}{\to} & X
} \qquad = \qquad 
\array{ D_1\times_{D_0} D_1 \\
  & \searrow^c\\
  && D_1 & \to & D_0\\
  && \downarrow & \Downarrow_\phi & \downarrow f\\
  && D_1 & \overset{f}{\to} & X.
}$$
=--

The comma square in the definition of the kernel of a morphism $f:A\to B$ gives a canonical 2-fork
$$(f/f) \;\rightrightarrows\; A \overset{f}{\to} B.$$
It is easy to see that any other 2-fork
$$D_1 \;\rightrightarrows\; D_0 = A \overset{f}{\to} B$$
factors through the kernel by an essentially unique functor $D \to ker(f)$ that is the identity on $A$.

If $D_1 \;\rightrightarrows\; D_0 \overset{f}{\to} X$ is a 2-fork, we say that it equips $f$ with an **action** by the 2-congruence $D$.  If $g:D_0\to X$ also has an action by $D$, say $\psi:g s \to g t$, a 2-cell $\alpha:f\to g$ is called an **action 2-cell** if $(\alpha t).\phi= \psi . (\alpha s)$.  There is an evident category $Act(D,X)$ of morphisms $D_0\to X$ equipped with actions.

+--{: .num_defn}
###### Definition
A **quotient** for a 2-congruence $D_1\;\rightrightarrows\; D_0$ in a 2-category $K$ is a 2-fork $D_1 \;\rightrightarrows\; D_0 \overset{q}{\to} Q$ such that for any object $X$, composition with $q$ defines an equivalence of categories
$$K(Q,X) \simeq Act(D,X).$$
=--

A quotient can also, of course, be defined as a suitable [[nLab:2-categorical limit|2-categorical limit]].

+-- {: .num_lem}
###### Lemma
The quotient $q$ in any 2-congruence is [[nlab:eso morphism|eso]].
=--
+-- {: .proof}
###### Proof
If $m\colon A\to B$ is ff, then the square we must show to be a pullback is
$$\array{Act(D,A) & \overset{}{\to} & Act(D,B)\\
  \downarrow && \downarrow\\
  K(D_0,A)& \underset{}{\to} & K(D_0,B)}$$
But this just says that an action of $D$ on $A$ is the same as an action of $D$ on $B$ which happens to factor through $m$, and this follows directly from the assumption that $m$ is ff.
=--

+--{: .num_defn}
###### Definition
A 2-fork $D_1 \;\rightrightarrows\; D_0 \overset{f}{\to} X$ is called **exact** if $f$ is a quotient of $D$ _and_ $D$ is a kernel of $f$.
=--

This is the 2-categorical analogue of the notion of exact fork in a 1-category, and plays an analogous role in the definition of a [[regular 2-category]] and an [[exact 2-category]].


## Properties

### Opposites 

The opposite of a homwise-discrete category is again a homwise-discrete category.  However, the opposite of a 2-congruence in $K$ is a 2-congruence in $K^{co}$, since [[nLab:opposite 2-category|2-cell duals]] interchange fibrations and opfibrations.  Likewise, passage to opposites takes 2-forks in $K$ to 2-forks in $K^{co}$, and preserves and reflects kernels, quotients, and exactness.

## Examples
 {#Examples}

### In $Grpd$
 {#ExamplesInGrpd}

> Under construction.

Let $K :=$ [[Grpd]] be the 2-category of [[groupoids]].

We would like to see that the following statement is true:

The [[2-category]] of 2-congruences in $Grpd$ is [[equivalence of 2-categories|equivalent]] to the 2-category [[Cat]] of [[small categories]].

$$
  2Cong(Grpd)
  \simeq
  Cat
  \,.
$$

Let's check:

For $C$ a [[small category]], construct a 2-congruence $\mathbb{C}$ in $Grpd$ as follows.

* let $\mathbb{C}_0 := Core(C) \in Grpd$ be the [[core]] of $C$;

* let $\mathbb{C}_1 := Core(C^{\Delta[1]}) \in Grpd$ be the core of the [[arrow category]] of $C$;

* let $(s,t) : \mathbb{C}_1 \to \mathbb{C}_0$ be image under $Core : Cat \to Grpd$ of the endpoint evaluation [[functor]] 

$$
  C^{\Delta[0] \coprod \Delta[0] \to \Delta[1]} 
  : 
  C^{\Delta[1]} \to C^{\Delta[0] \coprod \Delta[0]}
  =
  C \times C
  \,.
$$

(Here we are using the canonical embedding $\Delta \hookrightarrow Cat$ of the [[simplex category]].)

This is clearly a [[faithful functor]]. Moreover, every morphism in [[Grpd]] is trivially a [[conservative morphism]]. So $\mathbb{C}_1 \to \mathbb{C}_0 \times \mathbb{C}_0$ is a [[discrete morphism]] in [[Grpd]]. 

Since [[Grpd]] is a [[(2,1)-category]], the [[2-pullbacks]] in [[Grpd]] are [[homotopy pullbacks]]. Using that $(s,t)$ is (under the [[right adjoint]] [[nerve]] embedding $N : Grpd \hookrightarrow sSet$) a [[Kan fibration]] (by direct inspection, but also as a special case of standard facts about the [[model structure on simplicial sets]]), the object of composable morphisms is found to be 

$$
  \mathbb{C}_1 \times_{\mathbb{C}_0} \mathbb{C}_1
  \simeq
  Core(C^{\Delta[2]})
  \,.
$$

Accordingly, let the internal composition in $\mathbb{C}$ be induced by the given composition in $C$:

$$
  \mathbb{C}_1 \times_{\mathbb{C}_0} \mathbb{C}_1
  \simeq
  Core(C^{\Delta[2]})  
  \stackrel{}{\to}
  Core(C^{\Delta[1]})  
  \simeq
  \mathbb{C}_1
  \,.
$$

This is clearly [[associativity|associative]] and [[unitality|unital]] and hence makes $\mathbb{C}$ a hom-wise discrete category, def. \ref{HomWiseDiscreteInternalCategory}, internal to $Grpd$.


Observe next (for instance using the discussion and examples at [[homotopy pullback]], see also _[[path object]]_) that 

$$
  ker(\mathbb{C}_0) = 
  ( \mathbb{C}_0^{\Delta[1]} \stackrel{\to}{\to} \mathbb{C}_0)
  \,.
$$

Notice that up to [[equivalence of categories|equivalence of groupoids]], this is just the [[diagonal]] $\Delta : \mathbb{C}_0 \to \mathbb{C}_0 \times \mathbb{C}_0$.

Therefore there is an evident [[internal functor]] $ker(\mathbb{C}_0) \to \mathbb{C}$, which on the first equivalent incarnation of $ker(\mathbb{C}_0)$ given by the inclusion

$$
  ker(\mathbb{C}_0) 
  \simeq
  \mathbb{C}_0^{\Delta[1]}
  \simeq 
  Core(C)^{\Delta[1]} 
  \hookrightarrow 
  Core(C^{\Delta[1]})
  \,,
$$

but which in the second version above simply reproduces the [[identity-assigning morphism]] of the internal category $\mathbb{C}$.

It follows that $\mathbb{C}$ is indeed a 2-congruence, def. \ref{2Congruence}.

Conversely, given a 2-congruence $\mathbb{C}$ in $Grpd$, define a category $C$ as follows:


(...)


+--{: .num_remark}
###### Remark

In the notation of the above proof, we can also form _internally_ the [[core]] of $\mathbb{C}$. This is evidently the internally discrete category $\mathbb{C}_0 \stackrel{\overset{id}{\to}}{\underset{id}{\to}} \mathbb{C}_0$.

This means that the 2-congruences $\mathbb{C}$ in the above proof are [[complete Segal spaces]]

$$
  \mathbb{C} : [n] \mapsto Core(C^{\Delta[n]})
  \,,
$$

hence are [[internal categories in an (∞,1)-category]] in the [[(2,1)-category]] [[Grpd]].

=--

### In a general $(2,1)$-category
 {#ExamplesInA2Comma1Category}

(...)

## References


Much of the above material is taken from 

* [[Mike Shulman]], _[[michaelshulman:2-congruence]]_

using results from

* [[Mike Shulman]], _Framed bicategories and monoidal fibrations_ ([arXiv:0706.1286](http://arxiv.org/abs/0706.1286))
 {#Shulman07}
 
and

* [[Thomas Fiore]], _Pseudo Algebras and Pseudo Double Categories_ ([arXiv:0608760](http://arxiv.org/abs/math/0608760))
 {#Fiore06}



[[!redirects 2-congruences]]


[[!redirects 2-fork]]
[[!redirects 2-forks]]

