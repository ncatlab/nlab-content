
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
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

### 2-Congruences

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

It is easy to check that taking kernels of objects defines a functor $\Phi:K \to HDC(K)$; this might first have been noticed by [Street](http://www.springerlink.com/content/407n62422140864p/). See prop. \ref{InclusionOfKernelsInCongruences} below.

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

### The 2-category of 2-conguences
 {#2CategoryOf2Congruences}

There is an evident but naive [[2-category]] of 2-congruences in 
any 2-category. And there is a refined version where internal [[functors]]
are replaced by internal [[anafunctors]].

+--{: .num_defn #2CongWithOrdinaryFunctors}
###### Definition

For $K$ a [[2-category]], write $2Cong_s(K)$ for the [[full sub-2-category]]
of that of hom-wise discrete internal categories, def. \ref{HomWiseDiscreteInternalCategory} on the 2-congruences, def. \ref{2Congruence}

$$
  2 Cong_s(K) \hookrightarrow HDC(K)
  \,.
$$

=--

+--{: .num_prop #InclusionOfKernelsInCongruences}
###### Proposition

There is a [[2-functor]] 

$$
   \Phi : K\to 2Cong_s(K)
$$ 

sending each object to its kernel, def. \ref{Kernel}.

=-- 


+--{: .num_defn #2CongWithAnafunctors}
###### Definition

Let the 2-category $K$ be equipped with the structure of a [[2-site]]. 
With this understood, write

$$
  2 Cong(K)
$$

for the [[2-category]] of 2-congruences with morphisms the [[anafunctors]] between them.

=--

+--{: .num_remark }
###### Remark


The evident inclusion

$$
  2 Cong_s(K) \hookrightarrow 2 Cong(K)
$$ 

is a homwise-full sub-2-category closed under finite limits.

=--

## Properties

### Opposites 

The opposite of a homwise-discrete category is again a homwise-discrete category.  However, the opposite of a 2-congruence in $K$ is a 2-congruence in $K^{co}$, since [[nLab:opposite 2-category|2-cell duals]] interchange fibrations and opfibrations.  Likewise, passage to opposites takes 2-forks in $K$ to 2-forks in $K^{co}$, and preserves and reflects kernels, quotients, and exactness.

### Regularity
 {#Regularity}

We discuss that when the ambient 2-category $K$ has finite [[2-limits]], 
then its 2-category $2 Cong_s(K)$ of 2-congruences, def. \ref{2CongWithOrdinaryFunctors} is a _[[regular 2-category]]_. This is theorem \ref{regex} below. A sub-2-category of $Cong_s(K)$ is the _regular completion_ of $K$.

In the following and throughout, "$n$" denotes either of (see [[(n,r)-category]])

$$
  n = (0,1), (1,1), (2,1), (2,2)
  \,.
$$

+--{: .num_lemma}
###### Lemma
Suppose that $K$ has finite [[2-limits]].  Then:

1. $HDC(K)$ (def. \ref{HomWiseDiscreteInternalCategory}) has finite limits.

1. $n Cong_s(K)$ is closed under finite limits in $HDC(K)$.

1. The 2-functor $\Phi : K \to 2 Cong_s(K)$, prop. \ref{InclusionOfKernelsInCongruences}, is [[full and faithful 2-functor|2-fully-faithful]] (that is, an equivalence on hom-categories) and preserves finite limits.

=-- 
+--{: .proof}
###### Proof
It suffices to deal with finite products, inserters, and equifiers.  Evidently $\Phi(1)$ is a terminal object.  If $D$ and $E$ are homwise-discrete categories, define $P_0 = D_0\times E_0$ and $P_1 = D_1\times E_1$; it is easy to check that then $P_1 \;\rightrightarrows\; P_0$ is a homwise-discrete category that is the product $D\times E$ in $HDC(K)$.  Since $(D_0\times E_0) ^{\mathbf{2}} \simeq (D_0) ^{\mathbf{2}} \times (E_0) ^{\mathbf{2}}$, and products preserve ffs, we see that $P$ is an $n$-congruence if $D$ and $E$ are and that $\Phi$ preserves products.

For inserters, let $f,g:C \;\rightrightarrows\; D$ be functors in $HDC(K)$, define $i_0:I_0\to C_0$ by the pullback
$$\array{I_0 & \to & D_1\\ i_0 \downarrow && \downarrow \\
  C_0 & \overset{(f_0,g_0)}{\to} & D_0\times D_0,}$$
and define $i_1:I_1 \to C_1$ by the pullback
$$\array{I_1 & \to & X\\
  i_1\downarrow && \downarrow\\
  C_1 & \overset{(f_1,g_1)}{\to} & D_1\times D_1}$$
where $X$ is the "object of commutative squares in $D$."  Then $I_1 \;\rightrightarrows\; I_0$ is a homwise-discrete category and $i:I\to C$ is an inserter of $f,g$.  Also, $I$ is an $n$-congruence if $C$ is, and $\Phi$ preserves inserters.

Finally, for equifiers, suppose we have functors $f,g:C \;\rightrightarrows\; D$ and 2-cells $\alpha,\beta:f \;\rightrightarrows\; g$ in $HDC(K)$, represented by morphisms $a,b:C_0 \;\rightrightarrows\; D_1$ such that $(s,t) a \cong (f_0,g_0)\cong (s,t) b$.  Let $e_0:E_0\to C_0$ be the universal morphism equipped with an isomorphism $\phi:a e_0 \cong b e_0$ such that $(s,t)\phi$ is the given isomorphism $(s,t) a\cong (s,t) b$ (this is a finite limit in $K$.)  Note that since $(s,t):D_1\to D_0\times D_0$ is discrete, $e_0$ is ff.  Now let $E_1 = (e_0\times e_0)^*C_1$; then $E_1 \;\rightrightarrows\; E_0$ is a homwise-discrete category and $e:E\to C$ is an equifier of $\alpha$ and $\beta$ in $HDC(K)$. Also $E$ is an $n$-congruence if $C$ is, and $\Phi$ preserves equifiers.

For any morphism $f:A\to B$ in $K$, $\Phi(f)$ is the functor $ker(A)\to ker(B)$ that consists of $f:A\to B$ and $f^{\mathbf{2}}: A^{\mathbf{2}} \to B^{\mathbf{2}}$.  A transformation between $\Phi(f)$ and $\Phi(g)$ is a morphism $A\to B ^{\mathbf{2}}$ whose composites $A\to B ^{\mathbf{2}} \;\rightrightarrows\; B$  are $f$ and $g$; but this is just a transformation $f\to g$ in $K$.  Thus, $\Phi$ is homwise fully faithful.  And homwise essential-surjectivity follows from the essential uniqueness of thin structures, or equivalently a version of Prop 6.4 in [FBMF][].
=--

Moreover, we have:

+--{: .num_theorem #regex}
###### Theorem

If $K$ is an $n$-category with finite limits, then $n Cong_s(K)$ is [[regular 2-category|regular]].

=--
+--{: .proof}
###### Proof

It is easy to see that a functor $f:C\to D$ between $n$-congruences is ff in $n Cong_s(K)$ iff the square
$$\array{C_1 & \to & D_1\\ \downarrow && \downarrow\\
  C_0\times C_0 & \to & D_0\times D_0}$$
is a pullback in $K$.

We claim that if $e:E\to D$ is a functor such that $e_0:E_0\to D_0$ is split (that is, $e_0 s\cong 1_{D_0}$ for some $s:D_0\to E_0$), then $e$ is eso in $n Cong_s(K)$.  For if $e\cong f g$ for some ff $f:C\to D$ as above, then we have $g_0 s:D_0 \to C_0$ with $f_0 g_0 s \cong e_0 s \cong 1_{D_0}$, and so the fact that $C_1$ is a pullback induces a functor $h:D\to C$ with $h_0=g_0 s$ and $f h\cong 1_D$.  But this implies $f$ is an equivalence; thus $e$ is eso.

Moreover, if $e_0:E_0\to D_0$ is split, then the same is true for any pullback of $e$.  For the pullback of $e:E\to D$ along some $k:C\to D$ is given by a $P$ where $P_0 = E_0 \times_{D_0} D_{iso} \times_{D_0} C_0$; here $D_{iso}\hookrightarrow D_1$ is the "object of isomorphisms" in $D$.  What matters is that the projection $P_0\to C_0$ has a splitting given by combining the splitting of $e_0$ with the "identities" morphism $D_0\to D_{iso}$.

Now suppose that $f:D\to E$ is any functor in $n Cong_s(K)$.  It is easy to see that if we define $Q_0=D_0$ and let $Q_1$ be the pullback
$$\array{ Q_1 & \to & E_1 \\ \downarrow && \downarrow\\
  Q_0 \times Q_0 & \overset{f_0\times f_0}{\to} & E_0\times E_0}$$
then $f \cong m e$ where $e:D \to Q$ and $m:Q\to E$ are the obvious functors.  Moreover, clearly $m$ is ff, and $e$ satisfies the condition above, so any pullback of it is eso.  It follows that if $f$ itself were eso, then it would be equivalent to $e$, and thus any pullback of it would also be eso; hence esos are stable under pullback.

Since $m$ is ff, the kernel of $f$ is the same as the kernel of $e$, so to prove $K$ regular it remains only to show that $e$ is a quotient of that kernel.  If $C \;\rightrightarrows\; D$ denotes $ker(f)$, then $C$ is the comma object $(f/f)$ and thus we can calculate
$$C_0 = D_0\times_{E_0} E_1 \times_{E_0} D_0 \cong Q_1.$$
Therefore, if $g:D\to X$ is equipped with an action by $ker(f)$, then the action 2-cell is given by a morphism $Q_1=C_0\to X_1$, and the action axioms evidently make this into a functor $Q\to X$.  Thus, $Q$ is a quotient of $ker(f)$, as desired.
=--

+--{: .num_remark }
###### Remark

There are three "problems" with the 2-category $n Cong_s(K)$.

1. It is too big.  It is not necessary to include every $n$-congruence in order to get a regular category containing $K$, only those that occur as kernels of morphisms in $K$.
1. It is too small.  While it is regular, it is not [[exact 2-category|exact]].
1. It doesn't remember information about $K$.  If $K$ is already regular, then passing to $n Cong_s(K)$ destroys most of the esos and quotients already present in $K$.

=--

The solution to the first problem is straightforward.  

+--{: .num_defn }
###### Definition

If $K$ is a 2-category with finite limits, define 

$$
  K_{reg/lex} \hookrightarrow 2 Cong_s(K)
$$ 

to be the sub-2-category of $2 Cong_s(K)$ spanned by the 2-congruences which occur as kernels of morphisms in $K$.  

=--

+--{: .num_remark }
###### Remark

If $K$ is an $n$-category then any such kernel is an $n$-congruence, so in this case $K_{reg/lex}$ is contained in $n Cong_s(K)$ and is an $n$-category.  Also, clearly $\Phi$ factors through $K_{reg/lex}$.

=--

+--{: .num_theorem}
###### Theorem

For any finitely complete 2-category $K$, the 2-category $K_{reg/lex}$ is [[refular 2-category|regular]], and the functor $\Phi:K\to K_{reg/lex}$ induces an equivalence
$$Reg(K_{reg/lex},L) \simeq Lex(K,L)$$
for any regular 2-category $K$.

=--

Here $Reg(-,-)$ denotes the 2-category of regular functors, transformations, and modifications between two regular 2-categories, and likewise $Lex(-,-)$ denotes the 2-category of finite-limit-preserving functors, transformations, and modifications between two finitely complete 2-categories.

+--{: .proof}
###### Proof
It is easy to verify that $K_{reg/lex}$ is closed under finite limits in $2 Cong_s(K)$, and also under the eso-ff factorization constructed in Theorem \ref{regex}; thus it is regular.  If $F:K\to L$ is a lex functor where $L$ is regular, we extend it to $K_{reg/lex}$ by sending $ker(f)$ to the quotient in $L$ of $ker(F f)$, which exists since $L$ is regular.  It is easy to verify that this is regular and is the unique regular extension of $F$.
=--

In particular, if $K$ is a [[nlab:regular category|regular 1-category]], $K_{reg/lex}$ is the ordinary regular completion of $K$.  In this case our construction reduces to one of the usual constructions (see, for example, the [[nlab:Elephant|Elephant]]).

To solve the second and third problems with $n Cong_s(K)$, we need to modify its morphisms.


### Exactness
 {#Exactness}

Let now the ambient [[2-category]] $K$ be equipped with the  structure of a [[2-site]]. Recall from def. \ref{2CongWithAnafunctors} the 2-category $2Cong(K)$ whose objects are 2-congruences in $K$, and whose morpisms are internal [[anafunctors]] between these, with respect to the given 2-site structure.

Notice that when $K$ is a [[regular 2-category]] it comes with a canonical structure of a 2-site: its [[regular coverage]].

+--{: .num_theorem}
###### Theorem

For any [[subcanonical topology|subcanonical]] and finitely complete [[2-site]] $K$ (such as a [[regular coverage]]), the 2-category $2Cong(K)$ from 
def. \ref{2CongWithAnafunctors} 

* is finitely complete;

* contains $2Cong_s(K)$, def. \ref{2CongWithOrdinaryFunctors} as a homwise-full sub-2-category (that is, $2Cong_s(K)(D,E)\hookrightarrow 2Cong(K)(D,E)$ is ff) closed under finite limits.

=--
+--{: .proof}
###### Proof

It is easy to see that products in $2 Cong_S(K)$ remain [[products]] in $n Cong(K)$.  Before dealing with [[inserters]] and [[equifiers]], we observe that if $A\leftarrow F \to B$ is an anafunctor in $2 Cong(K)$ and $e:X_0\to F_0$ is any eso, then pulling back $F_1$ to $X_0\times X_0$ defines a new congruence $X$ and an anafunctor $A \leftarrow X \to B$ which is isomorphic to the original in $2 Cong(K)(A,B)$.  Thus, if $A\leftarrow F\to B$ and $A\leftarrow G\to B$ are parallel anafunctors in $2 Cong(K)$, by pulling them both back to $F\times_A G$ we may assume that they are defined by spans with the same first leg, i.e. we have $A\leftarrow X \;\rightrightarrows\; B$.

Now, for the inserter of $F$ and $G$ as above, let $E\to X$ be the inserter of $X \;\rightrightarrows\; B$ in $2 Cong_s(K)$.  It is easy to check that the composite $E\to X \to A$ is an inserter of $F,G$ in $2 Cong(K)$.  Likewise, given $\alpha,\beta: F \;\rightrightarrows\; G$ with $F$ and $G$ as above, we have transformations between the two functors $X \;\rightrightarrows\; B$ in $2 Cong_s(K)$, and it is again easy to check that their equifier in $2 Cong_s(K)$ is again the equifier in $2 Cong(K)$ of the original 2-cells $\alpha,\beta$.  Thus, $2 Cong(K)$ has finite limits.  Finally, by construction clearly the inclusion of $2 Cong_s(K)$ preserves finite limits.
=--


+--{: .num_theorem #nCongExidempotent}
###### Theorem

If $K$ is a [[subcanonical coverage|subcanonical]] finitely complete $n$-site, then the functor $\Phi:K\to n Cong(K)$, prop. \ref{InclusionOfKernelsInCongruences}, 
is [[full and faithful 2-functor|2-fully-faithful]].  
If $K$ is an $n$-[[exact 2-category|exact]] $n$-category equipped with its [[regular coverage]], then 

$$
  \Phi : K \to n Cong(K)
$$ 

is an [[equivalence of 2-categories]].

=--
+--{: .proof}
###### Proof
Since $\Phi:K \to n Cong_s(K)$ is 2-fully-faithful and $n Cong_s(K)\to n Cong(K)$ is homwise fully faithful, $\Phi:K \to n Cong(K)$ is homwise fully faithful.  For homwise essential-surjectivity, suppose that $ker(A) \leftarrow F \to ker(B)$ is an anafunctor. Then $h:F_0 \to A$ is a cover and $F_1$ is the pullback of $A ^{\mathbf{2}}$ along it; but this just says that $F_1 = (h/h)$.  The functor $F\to B$ consists of morphisms $g:F_0\to B$ and $F_1 = (h/h) \to B ^{\mathbf{2}}$, and functoriality says precisely that the resulting 2-cell equips $g$ with an action by the congruence $F$.  But since $F$ is precisely the kernel of $h:F_0\to A$, which is a cover in a subcanonical 2-site and hence the quotient of this kernel, we have an induced morphism $f:A\to B$ in $K$.  It is then easy to check that $f$ is isomorphic, as an anafunctor, to $F$.  Thus, $\Phi$ is homwise an equivalence.

Now suppose that $K$ is an $n$-exact $n$-category and that $D$ is an $n$-congruence.  Since $K$ is $n$-exact, $D$ has a quotient $q:D_0\to Q$, and since $D$ is the kernel of $q$, we have a functor $D \to ker(Q)$ which is a weak equivalence.  Thus, we can regard it either as an anafunctor $D\to ker(Q)$ or $ker(Q)\to D$, and it is easy to see that these are inverse equivalences in $n Cong(K)$.  Thus, $\Phi$ is essentially surjective, and hence an equivalence.
=--

Note that by working in the generality of 2-sites, this construction includes the previous one.  

+--{: .num_remark}
###### Remark

If $K$ is a finitely complete 2-category equipped with its minimal coverage, in which the covering families are those that contain a [[split epimorphism]], then 

$$
  n Cong(K) \simeq n Cong_s(K)
  \,.
$$ 

=--

+--{: .proof}
###### Proof

 This is immediate from the proof of Theorem \ref{regex}, which implies that the first leg of any anafunctor relative to this coverage is both eso and ff in $n Cong_s(K)$, and hence an equivalence.

=--

+--{: .num_theorem #nCongOnGroupoidsAndDiscretes}
###### Theorem

If $K$ is a 2-exact 2-category with [[core in a 2-category|enough groupoids]], then 

$$
  K\simeq 2 Cong(gpd(K))
  \,.
$$  

Likewise, if $K$ is 2-exact and has enough discretes, then 

$$
  K\simeq 2 Cong(disc(K))
  \,.
$$

=--
+--{: .proof}
###### Proof

Define a functor $K\to 2Cong(gpd(K))$ by taking each object $A$ to the kernel of $j:J\to A$ where $j$ is eso and $J$ is groupoidal (for example, it might be the [[core]] of $A$).  Note that this kernel lives in $2Cong(gpd(K))$ since $(j/j)\to J\times J$ is discrete, hence $(j/j)$ is also groupoidal.  The same argument as in Theorem \ref{nCongExidempotent} shows that this functor is 2-fully-faithful for any regular 2-category $K$ with enough groupoids, and essentially-surjective when $K$ is 2-exact; thus it is an equivalence.  The same argument works for discrete objects.
=--

In particular, the 2-exact 2-categories having enough discretes are precisely the 2-categories of internal categories and anafunctors in 1-exact 1-categories.

Our final goal is to construct the $n$-exact completion of a regular $n$-category, and a first step towards that is the following.

+--{: .num_theorem #almostExreg}
###### Theorem
If $K$ is a regular $n$-category, so is $n Cong(K)$.  The functor $\Phi:K\to n Cong(K)$ is regular, and moreover for any $n$-exact 2-category $L$ it induces an equivalence
$$Reg(n Cong(K), L) \to Reg(K,L).$$
=--
+--{: .proof}
###### Proof

We already know that $n Cong(K)$ has finite limits and $\Phi$ preserves finite limits.  The rest is very similar to Theorem \ref{regex}.  We first observe that an anafunctor $A \leftarrow F \to B$ is an equivalence as soon as $F\to B$ is also a weak equivalence (its reverse span $B\leftarrow F \to A$ then provides an inverse.)  Also, $A \leftarrow F \to B$ is ff if and only if
$$\array{F_1 & \to & B_1\\ \downarrow && \downarrow \\
  F_0\times F_0 & \to & B_0\times B_0}$$
is a pullback.

Now we claim that if $A\leftarrow F \to B$ is an anafunctor such that $F_0\to B_0$ is eso, then $F$ is eso.  For if we have a composition 
$$\array{ &&&& F \\
  &&& \swarrow && \searrow\\
  && G &&&& M\\
  & \swarrow && \searrow && \swarrow && \searrow\\
  A &&&& C &&&& B}$$
such that $M$ is ff, then $F_0\to B_0$ being eso implies that $M_0\to B_0$ is also eso; thus $M\to B$ is a weak equivalence and so $M$ is an equivalence.  Moreover, by the construction of pullbacks in $n Cong(K)$, anafunctors with this property are stable under pullback.

Now suppose that $A \leftarrow F \to B$ is any anafunctor, and define $C_0=F_0$ and let $C_1$ be the pullback of $B_1$ to $C_0\times C_0$ along $C_0 = F_0 to B_0$.  Then $C$ is an $n$-congruence, $C\to B$ is ff in $n Cong_s(K)$ and thus also in $n Cong(K)$, and $A \leftarrow F \to B$ factors through $C$.  (In fact, $C$ is the image of $F\to B$ in $n Cong_s(K)$.)  The kernel of $A\leftarrow F\to B$ can equally well be calculated as the kernel of $F\to B$, which is the same as the kernel of $F\to C$.

Finally, given any $A\leftarrow G \to D$ with an action by this kernel, we may as well assume (by pullbacks) that $F=G$ (which leaves $C$ unchanged up to equivalence).  Then since the kernel acting is the same as the kernel of $F\to C$, regularity of $n Cong_s(K)$ gives a descended functor $C\to D$.  Thus, $A\leftarrow F \to C$ is the quotient of its kernel; so $n Cong(K)$ is regular.

Finally, if $L$ is $n$-exact, then any functor $K\to L$ induces one $n Cong(K) \to n Cong(L)$, but $n Cong(L)\simeq L$, so we have our extension, which it can be shown is unique up to equivalence.

=--

When $K$ is a regular 1-category, it is well-known that $1 Cong(K)$ (which, in that case, is the category of internal equivalence relations and functional relations) is the 1-exact completion of $K$ (the reflection of $K$ from regular 1-categories into 1-exact 1-categories).  Theorem \ref{almostExreg} shows that in general, $n Cong(K)$ will be the $n$-exact completion of $K$ whenver it is $n$-exact.  However, in general for $n\gt 1$ we need to "build up exactness" in stages by iterating this construction.

It is possible that the iteration will converge at some finite stage, but for now, define $n Cong^r(K) = n Cong(n Cong^{r-1}(K))$ and let $K_{n ex/reg} = colim_r n Cong^r(K)$.

+--{: .num_theorem}
###### Theorem
For any regular $n$-category $K$, $K_{n ex/reg}$ is an $n$-exact $n$-category and there is a 2-fully-faithful regular functor $\Phi:K\to K_{n ex/reg}$ that induces an equivalence
$$Reg(K_{n ex/reg},L) \simeq Reg(K,L)$$
for any $n$-exact 2-category $L$.
=--
+--{: .proof}
###### Proof
Sequential colimits preserve 2-fully-faithful functors as well as functors that preserve finite limits and quotients, and the final statement follows easily from Theorem \ref{almostExreg}.  Thus it remains only to show that $K_{n ex/reg}$ is $n$-exact.  But for any $n$-congruence $D_1 \;\rightrightarrows\; D_0$ in $K_{n ex/reg}$, there is some $r$ such that $D_0$ and $D_1$  both live in $n Cong^r(K)$, and thus so does the congruence since $n Cong^r(K)$ sits 2-fully-faithfully in $K_{n ex/reg}$ preserving finite limits.  This congruence in $n Cong^r(K)$ is then an object of $n Cong^{r+1}(K)$ which supplies a quotient there, and thus also in $K_{n ex/reg}$.
=--

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

## Related concepts

* [[congruence]]

* [[n-congruence]]

## References


The above material is taken from 

* [[Mike Shulman]], _[[michaelshulman:2-congruence]]_

and

* [[Mike Shulman]], _[[michaelshulman:exact completion of a 2-category]]_

Some lemmas are taken from

* [[Mike Shulman]], _Framed bicategories and monoidal fibrations_ ([arXiv:0706.1286](http://arxiv.org/abs/0706.1286))
 {#Shulman07}
 
and

* [[Thomas Fiore]], _Pseudo Algebras and Pseudo Double Categories_ ([arXiv:0608760](http://arxiv.org/abs/math/0608760))
 {#Fiore06}



[[!redirects 2-congruences]]


[[!redirects 2-fork]]
[[!redirects 2-forks]]

