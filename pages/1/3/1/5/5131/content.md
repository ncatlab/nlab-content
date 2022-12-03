
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

This page describes aspects of the [[combinatorics]] of [[Cartesian products]] of [[simplicial sets]], mostly by describing (Prop. \ref{NonDegenerateSimplicesInProductOfSimplices}) the non-degenerate simplicices inside a [[Cartesian product]] $\Delta[p] \times \Delta[q]$ of basic [[n-simplices]] for $n = p,q$. These are enumerate by the $(p,q)$ (un-)[[shuffles]] in a manner that for [[simplicial abelian groups]] is originally known from the [[Eilenberg-Zilber map]].


## Products of simplicial sets
 {#ProductsOfSimplicialSets}

\begin{proposition}\label{CartesianProductOfSimplicialSetsIsComponentwise}
**([[cartesian product]] of [[simplicial sets]])**\linebreak
For $K, L \,\in\,$ [[SimplicialSets]], their [[Cartesian product]], 

$$
  K \times L
  \;\in\;
  SimplicialSets
$$

is the simplicial set whose $k$th component [[set]] is the [[Cartesian product]] of [[Sets]] of the components of the two factors

\[
  \label{ComponentSetsOfProductSimplicialSet}
  (K\times L)_k
  \;=\;
  K_k \times L_k
  \,,
\]

and whose face- and degeneracy maps are, similarly, the image under the Cartesian product-[[functor]] of the face- and degeneracy maps of the factors:

\[
  \label{StructureMapsOfProductSimpliciaSet}
  d^{K \times L}_i(x,y) 
  \;=\; 
  \big(
    d^K_i(x), \, d^L_i(y)
  \big)
  \,,
  \;\;\;\;\;
  s^{K \times L}_i(x,y) 
  \;=\; 
  \big(
    s^K_i(x), \, s^L_i(y)
  \big)
\]

\end{proposition}
\begin{proof}  
Since [[SimplicialSets]] is a [[category of presheaves]], namely over the [[simplex category]], this is a special case of the general fact that [[limits of presheaves are computed objectwise]].

But it is also immediate to check that
(eq:StructureMapsOfProductSimpliciaSet) with (eq:ComponentSetsOfProductSimplicialSet)
satisfies the defining [[universal property]] of the [[Cartesian product]].
\end{proof}

\begin{remark}\label{DegenerateSimplicesInProductOfSimplicialSets}
**(degenerate simplices in product of simplicial sets)**
Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise} 
means in particular that a [[simplex]] 
of the form $\big(s_\alpha(x),\, s_\beta(y)\big) \,\in\, K \times L$  may be non-degenerate even though its two components are each degenerate (see the archetypical Example \ref{NonDegenerateSimplicesInSimplicialSquare} below).

Indeed, the proposition says that the degenerate simplices in $K \times L$ are precisely those such that their two simplex-components in $K$ and $L$, respectively, are in the image of the *same* degeneracy map $\alpha = \beta$.
\end{remark}



## Non-degenerate cells in a product of simplices
 {#NonDegenerateCellsInAProductOfSimplices}

### Characterization

\begin{proposition}\label{NonDegenerateSimplicesInProductOfSimplices}
**(non-degenerate $(p+q)$-simplices in $\Delta[p] \times \Delta[q]$)**
\linebreak
For $p,q \,\in\, \mathbb{N}$,
the non-degenerate simplices in the [[Cartesian product]] (Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise})

$$
  \Delta[p] \times \Delta[q]
$$ 

of standard [[simplices]] in [[sSet]] correspond, under the [[Yoneda lemma]], to precisely those [[morphisms]] of [[simplicial sets]]

\[
  \label{GenericSimplexInProductOfSimplices}
  \Delta[p+q]
  \xrightarrow{\;\; \sigma \;\;}
  \Delta[p] \times \Delta[q]
\]

which satisfy the following equivalent conditions:

* as morphisms of [[posets]] they are [[strictly monotone]];

* as [[permutations]] of $(p+q)$ elements they are $(p,q)$-[[shuffles]];

* as morphisms of [[finitely generated object|finitely generated]] [[categories]] they take generating morphisms to generating morphisms;

\end{proposition}

(e.g. [Kerodon 2.5.7.2](#Kerodon): [00RH](https://kerodon.net/tag/00RH))

Such morphisms may hence be represented by [[paths]]

* on a $(p+1)\times(q+1)$-lattice,

* from one corner to its opposite corner,

* consisting of $p+q$ unit steps, 

* each either horizontally or vertically:

\begin{tikzcd}
  [
    row sep=large
  ]
    {(0,0)}
    \ar[r]
    \ar[d]
    \ar[
      r,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    %
    {(1,0)}
    \ar[r]
    \ar[d]
    \ar[
      d,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,0)}
    \ar[rr,dotted]
    \ar[d]
    &
    &
    {(p,0)}
    \ar[d]
    \\
    {(0,1)}
    \ar[r]
    \ar[d]
    &
    {(1,1)}
    \ar[r]
    \ar[d]
    \ar[
      d,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,1)}
    \ar[rr, dotted]
    \ar[d]
    &
    \cdots
    &
    {(p,1)}    
    \ar[d]
    \\
    {(0,2)}
    \ar[r]
    \ar[dd, dotted]
    &
    {(1,2)}
    \ar[r]
    \ar[dd, dotted]
    \ar[
      r,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,2)}
    \ar[rr, dotted]
    \ar[dd, dotted]
    \ar[ddrr, dotted]
    \ar[
      ddrr,-,
      color=blue,
      opacity=.25,
      line width=6pt,
      dotted
    ]
    &
    &
    {(p,2)}
    \ar[dd, dotted]
    \\
    &
    &
    &&
    \\
    {(0,q)}
    \ar[r]
    &
    {(1,q)}
    \ar[r]
    &
    {(2,q)}
    \ar[rr, dotted]
    &
    &
    {(p,q)}
\end{tikzcd}


\begin{proof}
From Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise} 
it is clear (Rem. \ref{DegenerateSimplicesInProductOfSimplicialSets}) that a 
simplex $\sigma$ (eq:GenericSimplexInProductOfSimplices) is degenerate 
precisely if, when regarded as a path as above, it contains a [[constant function|constant]] step, i.e. one which moves neither horizontally nor vertically. But then -- by degree reasons, since we are looking at paths of $p + q$ steps in a lattice of side length $p$ and $q$ -- it must be that the path proceeds by $p + q$ unit steps. 
\end{proof}

\begin{remark}\label{NotationForSimplicesInAProductOfSimplices}
**(sequence-notation for simplices in a product of simplices)** \linebreak
Written as a [[pair]] of $(p+q)$-simplices, one in $\Delta[p]$ and one in $\Delta[q]$, the non-degenerate simplex (eq:GenericSimplexInProductOfSimplices) is a [[pair]] of [[monotone]] lists of [[natural numbers]]

$$
  \left(
    \begin{array}{ccccccccc}
      0& \ldots & 0 & 1 & \ldots & 1 & 2 & \ldots & p
      \\
      0& \ldots & i & i & \ldots & j & j & \ldots & q
    \end{array}
  \right)
  \,,
$$

such that one row has a constant step precisely where the other has not.
\end{remark}


Here is a slightly alternative way to think of these non-degenerate simplices:

\begin{definition}
For $X$ some [[simplicial set]] $x \in X_p$ some $p$-cell and 
for $\mu = (\mu_1 \lt  \mu_2, \lt \cdots \lt \mu_q)$ a sequence of [[natural numbers]] in $\{0, \cdots p+q\}$, write

$$
  s_\mu \colon X_p \to X_{p+q}
$$

for the map dual to the sequence 

$$
  [p+q] 
    \overset{\;\; \sigma_{\mu_q} \;\;}{\longrightarrow}
  [p+q-1]
    \overset{\;\; \sigma_{\mu_{q-1}} \;\;}{\longrightarrow}
  \cdots
   \overset{\;\; \sigma_{\mu_1} \;\;}{\longrightarrow}
   [p]
  \,,
$$

where $\sigma_i$ is the surjective monotone map that repeats the index $i$.

\end{definition}

\begin{proposition}
The non-degenerate simplices in the [[Cartesian product]] (Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise})

$$
  \Delta[p] \times \Delta[q]
$$ 

of [[simplices]] in [[sSet]] are precisely those of the form 

$$
  (s_\mu x , s_\nu y) \in (\Delta[p] \times \Delta[q])_{p+q}
$$ 

for $(\mu,\nu)$ a $(p,q)$-[[shuffle]] and $x, y$ non-degenerate simplices in $\Delta[p]$ and $\Delta[q]$, respectively.

\end{proposition}


### Examples
 {#Examples}

\begin{example}\label{CylindersOfSimplices}
**([[cylinders]] of [[simplices]])**

The non-degenerate (n+1)-simplices in the [[cylinder]] of the [[n-simplex]]
$$
  \begin{aligned} & \Delta[1] \\ \times & \Delta[n] \end{aligned}
  \;\in\;
  sSet
$$ 

are, according to Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise}
 and in the notation of Remark \ref{NotationForSimplicesInAProductOfSimplices}, as follows:

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 1 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 1 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
  \,,
$$

\linebreak

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 1 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 1 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$

\linebreak

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
  \,,
$$

\linebreak

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 0 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 3 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
  \,,
$$

and so on.

\end{example}




\begin{example}
\label{NonDegenerateSimplicesInSimplicialSquare}
**(non-degenerate simplices in [[simplicial set|simplicial]] [[square]])**
\linebreak
The complete set of non-degenerate simplices in 
$\Delta[1] \times \Delta[1]$
is, in specialization of Example \ref{CylindersOfSimplices}, 
according to Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise}
and in the notation of Remark \ref{NotationForSimplicesInAProductOfSimplices}, 
the following:

  \begin{tikzcd}
    \scalebox{.8}{$
      \left( {[0]} \atop {[0]} \right)
    $}
    \ar[
      rr,
      "{
        \left(
        {[0,0]}
        \atop
        {[0,1]}
        \right)
      }"{above, scale=.8}
    ]
    \ar[
      dd,
      "{
        \left(
        {[0,1]}
        \atop
        {[0,0]}
        \right)
      }"{left, scale=.8}
    ]
    \ar[
      ddrr,
      "{
        \left(
        { [0,1] }
        \atop
        { [0,1] }
        \right)
      }"{description, scale=.8}
    ]
    &&
    \scalebox{.8}{$
      \left( {[0]} \atop {[1]} \right)
    $}
    \ar[
      dd,
      "{
        \left(
        {[0,1]}
        \atop
        {[1,1]}
        \right)
      }"{right, scale=.8}
    ]
    \ar[
      ddll,
      phantom,
      "{
        \left(
        { [0,0,1] }
        \atop
        { [0,1,1] }
        \right)
      }"{pos=.15, scale=.8}
    ]
    \ar[
      ddll,
      phantom,
      "{
        \left(
        { [0,1,1] }
        \atop
        { [0,0,1] }
        \right)
      }"{pos=.85, scale=.8}
    ]
    \\
    \\
    \scalebox{.8}{$
      \left( {[1]} \atop {[0]} \right)
    $}
    \ar[
      rr,
      "{
        \left(
        {[1,1]}
        \atop
        {[0,1]}
        \right)
      }"{below, scale=.8}
    ]
    &&
    \scalebox{.8}{$
      \left( {[1]} \atop {[1]} \right)    
    $}
  \end{tikzcd}

See also [Friedman 2008, Fig. 20](#Friedman08).
\end{example}





\begin{example}
  The non-degenerate simplices in 
  $$
    \begin{aligned}
      & \Delta[2]
      \\
      \times & \Delta[1]
    \end{aligned}
  $$
  are, in specialization of Example \ref{CylindersOfSimplices}, 
  according to Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise}
  and in the notation of Remark \ref{NotationForSimplicesInAProductOfSimplices}, 
  the following three:

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 2 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 0 & 1 
    \mathrlap]
  }
  \;\,
  \right)
  \,,
  \;\;\;\;\;\;\;
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 1 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 1 & 1 
    \mathrlap]
  }
  \;\,
  \right)
  \,,
  \;\;\;\;\;\;\;
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 1 & 2
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 1 & 1 
    \mathrlap]
  }
  \;\,
  \right)
$$  

\end{example}



### In terms of shuffles

Each such simplex yields a [[partition]] of $\{0, \ldots, p+q-1\}$ into two disjoint sets,
$\mu_1\lt\ldots \lt\mu_p$, and $\nu_1 \lt \ldots \lt \nu_q$, and vice versa, any such partition yields a simplex. Suppose that we have an array, as above, written

$$
  \left(
    \begin{array}{cccc}
      i_0& i_1&\ldots & i_{p+q}
      \\
      j_0& j_1 & \ldots & j_{p+q}
     \end{array}
  \right)
  \,,
$$

with $0= i_0 \leq i_1 \leq \ldots \leq i_{p+q}= p$, then if $i_k = i_{k+1}$, we put $k$ into the second set, otherwise $k$ is put in the first set.  This, of course, leads to an operation that preserves order. For instance, in the above example 2., the $i$-sequence is $(0,1,1,2)$, so there is the single repeat with $k = 1$, and $\nu = \{1\}$. 

We likewise require $0= j_0 \leq j_1 \leq \ldots \leq j_{p+q}= p$, and put $k$ into the first set if  $j_k = j_{k+1}$.  For the example, we have the $j$-sequence is $(0,0,1,1)$, so $\mu = \{ 0,2\}$.  Of course, from the partition you can get the sequences and conversely. The attentive reader will, of course, have noted that, for example 2., the $\alpha$, we specified was exactly the $\nu$, and the $\beta$ was the $\mu$.  This is general with the simplex corresponding to a partition, $(\mu,\nu)$,  being given by $(s_{\nu_q}\ldots s_{\nu_1}x_p,s_{\mu_p}\ldots s_{\mu_1}y_q)$.

Each such partition defines a [[permutation]] of $\{0,\ldots, p+q-1 \}$.  Let us write $\iota_0 : \{ 0, \ldots, q-1\}\to \{0, \ldots, p+q-1\}$ for the order preserving function $\iota_0 (r)= p+r$, whilst $\iota_1 : \{ 0, \ldots, p-1\}\to \{0, \ldots, p+q-1\}$ will denote the inclusion, so $\iota_1(r) = r$. There will be a permutation  $\sigma$ of $\{0,\ldots, p+q-1 \}$ such that $\sigma \iota_0(r) = \nu_{r+1}$ and $\sigma\iota_1(r) = \mu_{r+1}$. This means that the permutation looks like  

$$\sigma =\left(\begin{array}{ccccccccc}0&1&2& \ldots & p-1&p&p+1& \ldots & p+q-1\\
\mu_1&\mu_2&\mu_3&\ldots & \mu_p&\nu_1&\nu_2&\ldots &\nu_q\end{array}\right).$$




We can thus assign  a sign, $sgn(\sigma)$, to each such shuffle, namely the sign of the corresponding permutation.  

For our standard examples, we have : 1) $\sigma$ is the identity, 2) $\sigma = \left(\begin{array}{ccc}0&1&2\\0&2&1\end{array}\right)$, i.e. the transposition exchanging 1 and 2,  and for 3) $\sigma = \left(\begin{array}{ccc}0&1&2\\1&2&0\end{array}\right)$, a 3-cycle. 
We thus have, in this case, the signs are +1, -1, and  + 1, respectively.



## The poset of $(p,q)$-shuffles###

Any pair $(p,q)$ yields a [[poset]] relating the various $(p,q)$-[[shuffles]].  


Our $(2,1)$-example is really too simple and small to illustrate this well, but the two cases $(3,1)$ and $(2,2)$ do a much better job, but, even so, we first look at the (2,1) example:
$$\begin{matrix} (0\lt 1)&-&(0\lt 2)&-&(1\lt 2)\end{matrix}$$


(This [[Hasse diagram]] has been laid out horizontally to save space.  The bottom is to the left. The vertex $(0\lt 1)$ corresponds to the shuffle with $\mu_1 = 0, \mu_1 = 1$, and so on.)
 
We need here to explain the partial order.  We take the '$\mu$-signature' of the shuffle, that is, the ordered set $\mu_1\lt\ldots \lt \mu_p$. (Of course, this determines the $\nu$-signature as that is the complement of $\mu$.)

+--{: .num_defn}
######Definition######
Given two $(p,q)$-shuffles, represented by $(\mu, \nu)$ and $(\mu\prime,\nu\prime)$, we set 

$$(\mu, \nu) \leq (\mu\prime,\nu\prime)$$

if, for each $i$ in the range $1\leq i\leq p$, $\mu_i \leq \mu_i\prime.$  We refer to this poset as $(Shuff(p,q),\leq)$.
=--

Going to  $(Shuff(3,1),\leq)$, the poset for $(3,1)$-shuffles,  the fact that $q = 1$ will mean that this poset is again [[linear order|linear]]:
$$\begin{matrix}
(0 \lt 1 \lt 2) &-& (0 \lt 1 \lt 3)& - &(0 \lt 2 \lt 3)& - &(1 \lt 2 \lt 3)
\end{matrix}$$

This is true in general:

+--{: .num_lemma}
######Lemma
If $p = 1$ or $q = 1$, then  $(Shuff(p,q),\leq)$ is a [[linear order|linear poset]].
=--

+-- {: .proof}
######Proof######
If $p = 1$, $\mu = (\mu_1)$ is a singleton, and the poset will be:

$$\begin{matrix}
(0) & - & (1) & - & \ldots & - & (q).
\end{matrix}$$

For $q = 1$, $\nu = (\nu_1)$, and the poset is 

$$\begin{matrix}
(0 \lt 1 \lt \ldots \lt p-1) & - & (0 \lt 1 \lt \ldots \lt p-2 \lt p) & - & \ldots & - & (1 \lt \ldots \lt p),
\end{matrix}$$
where at each stage one misses out the single $\nu$-value.
=--

In all cases, each position is obtained from the one immediately to its 'left' by increasing _one_ value, yet remaining with a shuffle.  This is more clearly seen in the (2,2) example, which is no longer [[linear order|linear]].  First we display the grid in which things are happening.
$$\begin{matrix}
(0,2) & - & (1,2) & - & (2,2) \\
| & & | & & | \\
(0,1) & - & (1,1) & - & (2,1) \\
| & & | & & | \\
(0,0) & - & (1,0) & - & (2,0)
\end{matrix}$$

We can then look at the shuffle poset, noting again that it is not [[linear order|linear]]:


\begin{xymatrix@=1.5em}&&(1<2)\ar@{-}[dr]&&\\
(0<1)\ar@{-}[r]&(0<2)\ar@{-}[ur]\ar@{-}[dr]&&(1<3)\ar@{-}[r]&(2<3)\\
&&(0<3)\ar@{-}[ur]&&\end{xymatrix}


The left hand shuffle, labelled $(0\lt1)$, corresponds to $\left(\begin{array}{ccccc}0&1&2&2&2\\0&0&0&1&2\end{array}\right)$, so gives the path along the bottom of the square and then up the right hand side. 

<img src="http://presheaf.com/cache/d235j2o1r1a66p292a442r4w4p3q3l5k.png" title="click to go to presheaf.com for editing"/>


The first change goes to $(0\lt 2)$ and gives a path with 2 steps,

<img src="http://presheaf.com/cache/d3r3h4z7142561t5j3q67396h2x74gn.png" title="click to go to presheaf.com for editing"/> 

and corresponds to the shuffle, $\left(\begin{array}{ccccc}0&1&1&2&2\\0&0&1&1&2\end{array}\right)$,
so at this position, $(0\lt2)$, there is a choice, either increase 0 by 1 to get $(1\lt 2)$ or increase 2 by 1 to get $(0\lt3)$. In the first case, we get the path  

<img src="http://presheaf.com/cache/d3h5a353o3oc3d1wm1k3020585o476t.png" title="click to go to presheaf.com for editing"/> 
going horizontally across the square,
and the shuffle, $\left(\begin{array}{ccccc}0&0&1&2&2\\0&1&1&1&2\end{array}\right)$, 
and in the second case, we get the shuffle:
 $\left(\begin{array}{ccccc}0&1&1&1&2\\0&0&1&2&2\end{array}\right)$, and the obvious path up the middle of the square:


<img src="http://presheaf.com/cache/d521h5c205h93p274p3f1w5v563776v.png" title="click to go to presheaf.com for editing"/>

From $(1 \lt 2)$ or $(0\lt3)$, there is only one way to go, namely to $(1 \lt 3)$ and a 2-step path (left to you), and, finally it is just one step from  $(1 \lt 3)$ to $(2 \lt 3)$ and the other extremal path.


\linebreak

In summary, each path corresponds to a simplex of maximal dimension in the product. The poset encodes the simplest relationships between those paths with the links in the Hasse diagram corresponding to simple changes in the path, and adjacency of the two simplices in the product, but note that the poset is usually not linear.

## The Anti-Lex order

There is a total order on $Shuff(p,q)$ related to the above partial order and which is useful when checking cancellation of terms in non-commutative contexts, as occurs in the Whitehead product formula given by Curtis and attributed to Kan.  This is the **anti-lexicographic order.


We  represent   a $(p,q)$-shuffle $(\mu,\nu)$ by an increasing $\mu$-sequence $\mu_1\lt \ldots \lt \mu_p$, (so with complementary $\nu$-sequence $\nu_1\lt \ldots \lt \nu_q$). 

We order the $(\mu,\nu)$ using just the $\mu$-sequence as, of course, that determines the $\nu$-sequence completely.  Inductively in $p$, we set 


$$\mu = (\mu_1,\ldots, \mu_p)\prec \mu\prime = (\mu\prime_1,\ldots, \mu\prime_p),$$

(i) if $\mu_p\lt \mu\prime_p$,

or

(ii) if $\mu_p = \mu\prime_p$ and $\mu_p$ is odd, 

$$(\mu_1,\ldots, \mu_{p-1})\prec (\mu\prime_1,\ldots, \mu\prime_{p-1}),$$

whilst if $\mu_p = \mu\prime_p$ and $\mu_p$ is even, 

$$(\mu_1,\ldots, \mu_{p-1})\succ (\mu\prime_1,\ldots, \mu\prime_{p-1}),$$ 

where we adopt the notation $(\mu_1,\ldots, \mu_p)$ instead of $(\mu_1\lt\ldots \lt \mu_p)$.

For example, on our (2,2)-shuffles, the total order is 

$$(0,1) - (1,2) - (0,2) - (0,3) - (1,3) - (2,3). $$

We note the lexicographic order on the sector with $\mu_2 = 2$ is reversed.

For illustrative purposes, we will look at two other examples. 

 First a generic $(p,1)$ case:  the shuffle poset for $(p,1)$ is, more or less, 

$$(0,\ldots , p-2) - (0,\ldots, p-4,p-3,p-1) - (0, \ldots, p-4,p-2,p-1) - 
 \ldots  -  (1, \ldots , p-1)$$

as, at each position, there is only one transposition that can be applied.  The anti-lex total order will correspond _exactly_ to this if $p-1$ is odd, but, if $p-1$ is even, it will reverse the order on the last $p-1$ positions giving 

$$(0,\ldots , p-2) - (1, \ldots , p-1) - (0,2, \ldots, p-1) -  \ldots  - (0,\ldots, p-3,p-1).$$

There are various points to note.  Firstly that if $p$ is even, the permutation corresponding to $(1, \ldots , p-1)$ is odd.  Secondly, the geometric picture is simply a prism, $\Delta[p]\times \Delta[1]$, and we can easily interpret the above order as a filling scheme for the simplices of $(\Delta[p]\times \Delta[1])\times \Delta[1]$, starting with the empty shell of 

$$(\Delta[p]\times \Delta[1])\times \{0\} \cup \partial(\Delta[p]\times \Delta[1])\times \Delta[1],$$ 

together with part of the top of the 'canister'.  (In general the total order seems to correspond to some sort of filling scheme although this is not always as clear as here.)

Our second case will be (3,2).  Again we will write $(i,j,k)$ instead of $i\lt j\ltk$ in order to save confusion over the various different orders being considered.  The shuffle poset, $\mathrm{Shuff}(3,2)$, has Hasse diagram given below:

<a href="http://presheaf.com/?d=d6h6o5y2s5an2i2l694co21381e385u"><img src="http://presheaf.com/cache/d6h6o5y2s5an2i2l694co21381e385u.png" title="click to go to presheaf.com for editing"/></a>

The subgraph of those with $\mu_3 = 4$, of course, is a copy of our earlier $(2,2)$-example, whilst that with $\mu_3 = 3$, is a copy of $Shuff(3,1)$.  Within that we have, on deleting the 3s from the final positions, a copy of $Shuff(2,1)$ and so on.  Taking $Shuff(2,1) \times \{3\}$, we can match it with a $Shuff(2,1) \times \{4\}$ within the $\mu_3 = 4$ block, the matching being given by, for instance, $(0,1,3)\leftrightarrow(0,1,4)$, etc.  The anti-lex order gives
\[
(0,1,2)-(0,1,3) - (1,2,3)-(0,2,3)-(2,3,4)-(1,3,4)-(0,3,4) - (0,2,4) - (1,2,4) - (0,1,4),\]

which is 
$$Shuff(3,1)\oplus Shuff(2,2)^{op}\times \{4\},$$
the ordinal sum, or join, of the anti-lex ordered shuffle sets.  This sort of decomposition is quite general.

## Related concepts

* [[Eilenberg-Zilber map]]

## References

The shuffle-formula is due (in terms of [[simplicial abelian groups]] of [[cochain on a simplicial set|chains on a simplicial set]], see at *[[Eilenberg-Zilber map]]*) to:

* [[Samuel Eilenberg]], [[Saunders MacLane]], (5.3) in: *On the groups $H(\Pi,n)$*, I, Ann. of Math. (2) 58, (1953), 55&#8211;106. ([jstor:1969820](https://www.jstor.org/stable/1969820))

following:

* [[Samuel Eilenberg]], [[Joseph A. Zilber]], American Journal of Mathematics Vol. 75, No. 1 (Jan., 1953), pp. 200-204 ([jstor:2372629](https://www.jstor.org/stable/2372629), [doi:10.2307/2372629](https://doi.org/10.2307/2372629))

The streamlined perspective of strictly monotonic morphisms $\Delta[p+q] \to \Delta[p] \times \Delta[q]$ is highlighted in 

* {#Kerodon} [[Kerodon]], 2.5.7.2 *$(p,q)$-Shuffles* ([00RH](https://kerodon.net/tag/00RH))


Exposition:

* {#Friedman08} [[Greg Friedman]], Section 5 of: _An elementary illustrated introduction to simplicial sets_, Rocky Mountain J. Math. 42(2): 353-423 (2012) ([arXiv:0809.4221](http://arxiv.org/abs/0809.4221), [doi:10.1216/RMJ-2012-42-2-353](https://projecteuclid.org/journals/rocky-mountain-journal-of-mathematics/volume-42/issue-2/Survey-Article-An-elementary-illustrated-introduction-to-simplicial-sets/10.1216/RMJ-2012-42-2-353.full))

Textbook accounts:

* {#Friedman20} [[Greg Friedman]], Appendix B.6 in: *Singular Intersection Homology*,  Cambridge University Press 2020 ([doi:10.1017/9781316584446](https://doi.org/10.1017/9781316584446), [pdf](http://faculty.tcu.edu/gfriedman/IHbook.pdf))


[[!redirects products of simplices]]

[[!redirects product of simplicial sets]]
[[!redirects products of simplicial sets]]

[[!redirects Cartesian product of simplices]]
[[!redirects Cartesian products of simplices]]

