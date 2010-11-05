
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

This page describes aspects of the combinatorics of [[product]]s of [[simplicial set]]s.

## Properties

+-- {: .un_definition}
###### Notation

For $X$ some [[simplicial set]] $x \in X_p$ some $p$-cell and 
for $\mu = (\mu_1 \lt  \mu_2, \lt \cdots \lt \mu_q)$ a sequence of natural numbers in $\{0, \cdots p+q\}$, write

$$
  s_\mu : X_p \to X_{p+q}
$$

for the map dual to the sequence 

$$
  [p+q] 
    \stackrel{\sigma_{\mu_q}}{\to}
  [p+q-1]
    \stackrel{\sigma_{\mu_{q-1}}}{\to}
  \cdots
   \stackrel{\sigma_{\mu_1}}{\to}
   [p]
  \,,
$$

where $\sigma_i$ is the surjective monotone map that repeats the index $i$.

=--

+-- {: .un_prop}
###### Proposition
The non-degenerate simplices in the [[product]] 
$$
  \Delta[p] \times\Delta[q]
$$ 

of [[simplices]] in [[sSet]] are precisely those of the form 

$$
  (s_\mu x , s_\nu y) \in (\Delta[p] \times \Delta[q])_{p+q}
$$ 

for $(\mu,\nu)$ a $(p,q)$-[[shuffle]] and $x, y$ non-degenerate simplices in $\Delta[p]$ and $\Delta[q]$, respectively.

=--



## Shuffles and products of simplices

[[shuffle|Shuffles]] are interesting combinatorial structures but the reason why they come into many constructions in [[homotopy theory]] and [[higher category theory]] is because of their relationship with the structure of [[product]]s.

The definition of the product, $K\times L$, of [[simplicial set]]s $K$ and $L$ gives that $(K\times L)_k$ is defined to be $K_k\times L_k$ with face and degeneracy maps defined 'componentwise' so, for instance, $d_i(x,y) = (d_i x,d_i y)$.  This means that a [[simplex]] $(s_\alpha x, s_\beta y)$ can be non-degenerate even though its two components are degenerate.  Of course, this happens exactly when $\alpha \cap \beta = \emptyset$.  (Here we mean by $s_\alpha$ the composite, in order,  of the $s_i$ for $i \in \alpha$.)

In particular, take $K = \Delta[p]$ and $L= \Delta[q]$ with $x_p \in \Delta[p]_p$, $y_q \in \Delta[q]_q$, the 'identity' simplices that generate them.  (We will use an _ad hoc_ notation here, since the more obvious, $\iota_p$, and  $\iota_q$, would not distinguish the two simplices sufficiently in some formulae.)  There are, then,  non-degenerate simplices of dimension $p+q$, but none of higher dimension in $\Delta[p]\times \Delta[q]$.  These are of the form $(s_\alpha x_p,s_\beta y_q)$, where $\#\alpha = q$, $\#\beta = p$.



### Non-degenerate simplices in a product 
If we represent a vertex of a product by a 'column vector' rather than the more usual 'row vector' for the moment, then any non-degenerate $(p+q)$-simplex of $\Delta[p]\times \Delta[q]$ can be represented in the form of an ordered list of vertices,

$$\left(\begin{array}{ccccccccc}
0& \ldots & 0 & 1 & \ldots & 1 & 2 & \ldots & p\\
0& \ldots & i & i & \ldots & j & j & \ldots & q
\end{array}\right),$$

with $p + q + 1 $ columns.  The top row, which is a simplex  in $\Delta[p]$, changes at exactly those positions at which the bottom row repeats.  The top row gives a degenerate $p+q$ simplex of $\Delta[p]$, whilst the bottom row one of $\Delta[q]$, i.e., the array gives $(s_\alpha x_p, s_\beta y_q)$ for some $(\alpha, \beta)$  as above.

### Illustrative example 

The usual illustrative example is of the three 3-simplices of $\Delta[2]\times \Delta[1]$:

1. $\left(\begin{array}{cccc}0&1&2&2\\0&0&0&1\end{array}\right)$, 

1. $\left(\begin{array}{cccc}0&1&1&2\\0&0&1&1\end{array}\right)$, 

1. $\left(\begin{array}{cccc}0&0&1&2\\0&1&1&1\end{array}\right)$

with, for 1), $\alpha = (2)$, $\beta = (1,0)$; for 2) $\alpha = (1)$, $\beta = (2,0)$; and, for 3), $\alpha = (0)$, $\beta = (2,1)$.


### Simplices of the product and partitions

Each such simplex yields a partition of $\{0, \ldots, p+q-1\}$ into two disjoint sets,
 $\mu_1\lt\ldots \lt\mu_p$, and $\nu_1 \lt \ldots \lt \nu_q$, and vice versa. Suppose that we have an array, as above, written

 $$\left(\begin{array}{cccc}
i_0& i_1&\ldots & i_{p+q}\\
j_0& j_1 & \ldots & j_{p+q}
\end{array}\right),$$

with $0= i_0 \leq i_1 \leq \ldots \leq i_{p+q}= p$, then if $i_k = i_{k+1}$, we put $k$ into the second set, otherwise $k$ is put in the first set.  This, of course, leads to an operation that preserves order. For instance, in the above example 2., the $i$-sequence is $(0,1,1,2)$, so there is the single repeat with $k = 1$, and $\nu = \{1\}$. 

We likewise require $0= j_0 \leq j_1 \leq \ldots \leq j_{p+q}= p$, and put $k$ into the first set if  $j_k = j_{k+1}$.  For the example, we have the $j$-sequence is $(0,0,1,1)$, so $\mu = \{ 0,2\}$.  Of course, from the partition you can get the sequences and conversely. The attentive reader will, of course, have noted that, for example 2., the $\alpha$, we specified was exactly the $\nu$, and the $\beta$ was the $\mu$.  This is general with the simplex corresponding to a partition, $(\mu,\nu)$,  being given by $(s_{\nu_q}\ldots s_{\nu_1}x_p,s_{\mu_p}\ldots s_{\mu_1}y_q)$.

Each such partition defines a permutation of $\{0,\ldots, p+q-1 \}$.  Let us write $\iota_0 : \{ 0, \ldots, q-1\}\to \{0, \ldots, p+q-1\}$ for the order preserving function $\iota_0 (r)= p+r$, whilst $\iota_1 : \{ 0, \ldots, p-1\}\to \{0, \ldots, p+q-1\}$ will denote the inclusion, so $\iota_1(r) = r$. There will be a permutation  $\sigma$ of $\{0,\ldots, p+q-1 \}$ such that $\sigma \iota_0(r) = \nu_{r+1}$ and $\sigma\iota_1(r) = \mu_{r+1}$. This means that the permutation looks like  

$$\sigma =\left(\begin{array}{ccccccccc}0&1&2& \ldots & p-1&p&p+1& \ldots & p+q-1\\
\mu_1&\mu_2&\mu_3&\ldots & \mu_p&\nu_1&\nu_2&\ldots &\nu_q\end{array}\right).$$




We can thus assign  a sign, $sgn(\sigma)$, to each such shuffle, namely the sign of the corresponding permutation.  

For our standard examples, we have : 1) $\sigma$ is the identity, 2) $\sigma = \left(\begin{array}{ccc}0&1&2\\0&2&1\end{array}\right)$, i.e. the transposition exchanging 1 and 2,  and for 3) $\sigma = \left(\begin{array}{ccc}0&1&2\\1&2&0\end{array}\right)$, a 3-cycle. 
We thus have, in this case, the signs are +1, -1, and  + 1, respectively.


### Paths in the product 


A final useful interpretation of $(p,q)$ shuffles is of ascending paths through a $p$ by $q$ integer lattice from $(0,0)$ to $(p,q)$.  This is quite well illustrated by our example.  The vertices are the integer pairs, $(i,j)$ with $0\leq i\leq p$ and $0\leq j\leq q$, so in our case we get

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{(0,1)\ar@{-}[r]\ar@{-}[d]%26(1,1)\ar@{-}[r]\ar@{-}[d]%26(2,1)\ar@{-}[d]\\(0,0)\ar@{-}[r]%26(1,0)\ar@{-}[r]%26(2,0)}"/>

The path corresponding to a $(p,q)$-shuffle just follows the list of (transposed pairs of) vertices, so, for instance, 2) goes  

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26(1,1)\ar@{-}[r]\ar@{-}[d]%26(2,1)\\	(0,0)\ar@{-}[r]%26(1,0)%26}"/>

###The poset of $(p,q)$-shuffles###

Any pair $(p,q)$ yields a [[poset]] relating the various $(p,q)$-shuffles.  

####Easy examples

For the sake of the will give some elementary examples. (This section can be skipped if you want to move on to the more theoretical analysis of these posets.)

Our $(2,1)$-example is really too simple and small to illustrate this well, but the two cases $(3,1)$ and $(2,2)$ do a much better job, but, even so, we first look at the (2,1) example:


<img src="http://latex.codecogs.com/gif.latex?\xymatrix{(0%3C 1)\ar@{-}[r]%26(0%3C 2)\ar@{-}[r]%26(1%3C 2).}"/>

(This [[Hasse diagram]] has been laid out horizontally to save space.  The bottom is to the left. The vertex $(0\lt 1)$ corresponds to the shuffle with $\mu_1 = 0, \mu_1 = 1$, and so on.)
 
We need here to explain the partial order.  We take the $\mu$-signature' of the shuffle, that is, the ordered set $\mu_1\lt\ldots \lt \mu_p$. (Of course, this determines the $\nu$-signature as that is the complement of $\mu$.)

+--{: .un_defn}
######Definition######
Given two $(p,q)$-shuffles, represented by $(\mu, \nu)$ and $(\mu\prime,\nu\prime)$, we set 

$$(\mu, \nu) \leq (\mu\prime,\nu\prime)$$

if, for each $i$ in the range $1\leq i\leq p$, $\mu_i \leq \mu_i\prime.$  We refer to this poset as $(Shuff_{(p,q)},\leq)$.
=--

Going to $(3,1)$,  the fact that $q = 1$ will mean that the poset is linear:

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{(0%3C 1%3C 2)\ar@{-}[r]%26(0%3C 1%3C 3)\ar@{-}[r]%26(0%3C 2%3C 3)\ar@{-}[r]%26(1%3C 2%3C 3).}"/> 

This is general:

+--{: .un_lemma}
######Lemma
If $p = 1$ or $q = 1$, then  $(Shuff_{(p,q)},\leq)$ is a linear poset.
=--

+-- {: .proof}
######Proof######
If $p = 1$, $\mu = (\mu_1)$ is a singleton, and the poset will be:

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{(0)\ar@{-}[r]%26(1)\ar@{-}[r]%26\quad\ldots\quad\ar@{-}[r]%26(q)}."/>

For $q = 1$, $\nu = (\nu_1)$, and the poset is 

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{(0%3C 1%3C \ldots%3C p-1)\ar@{-}[r]%26 (0%3C 1%3C  \ldots %3C  p-2%3C p)\ar@{-}[r]%26\quad \ldots\quad\ar@{-}[r]%26(1%3C \ldots %3C p),}"/>
where at each stage one misses out the single $\nu$-value.
=--

In all cases, each position is obtained from the one immediately to its 'left' by increasing _one_ value, yet remaining with a shuffle.  This is more clearly seen in the (2,2) example, which is no longer linear.  First we display the grid in which things are happening.

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{(0,2)\ar@{-}[r]\ar@{-}[d] %26 (1,2)\ar@{-}[r]\ar@{-}[d] %26 (2,2)\ar@{-}[d]\\(0,1)\ar@{-}[r]\ar@{-}[d] %26 (1,1)\ar@{-}[r]\ar@{-}[d] %26 (2,1)\ar@{-}[d]\\(0,0)\ar@{-}[r]%26(1,0)\ar@{-}[r]%26(2,0)}"/>

We can then look at the shuffle poset, noting again that it is not linear:

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26%26(1%3C 2)\ar@{-}[dr]%26%26\\(0%3C 1)\ar@{-}[r]%26(0%3C 2)\ar@{-}[ur]\ar@{-}[dr]%26%26(1%3C 3)\ar@{-}[r]%26(2%3C 3)\\%26%26(0%3C 3)\ar@{-}[ur]%26%26}"/>

The left hand shuffle, labelled $(0\lt1)$, corresponds to $\left(\begin{array}{ccccc}0&1&2&2&2\\0&0&0&1&2\end{array}\right)$, so gives the path along the bottom of the square and then up the right hand side. 

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26%26 (2,2)\ar@{-}[d]\\
%26%26 (2,1)\ar@{-}[d]\\
(0,0)\ar@{-}[r]%26(1,0)\ar@{-}[r]%26(2,0)}"/>


The first change goes to $(0\lt 2)$ and gives a path with 2 steps,

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26 %26 (2,2)\ar@{-}[d]\\
%26(1,1)\ar@{-}[r]\ar@{-}[d] %26 (2,1)\\
(0,0)\ar@{-}[r]%26(1,0)%26}"/> 

and corresponds to the shuffle, $\left(\begin{array}{ccccc}0&1&1&2&2\\0&0&1&1&2\end{array}\right)$,
so at this position, $(0\lt2)$, there is a choice, either increase 0 by 1 to get $(1\lt2)$ or increase 2 by 1 to get $(0\lt3)$. In the first case, we get the path shuffle 

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26 %26 (2,2)\ar@{-}[d]\\
(0,1)\ar@{-}[r]\ar@{-}[d]%26(1,1)\ar@{-}[r]%26 (2,1)\\
(0,0)%26%26}"/> 

and the shuffle, $\left(\begin{array}{ccccc}0&0&1&2&2\\0&1&1&1&2\end{array}\right)$, so at this position, there is a choice, either increase 0 by 1 to get $(1 \lt 2)$:

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26 %26 (2,2)\ar@{-}[d]\\
(0,1)\ar@{-}[d] \ar@{-}[r]%26(1,1)\ar@{-}[r]%26 (2,1)\\
(0,0)%26%26}"/>

or increase 2 to 3 to get $(0 \lt 3)$, the shuffle:
 $\left(\begin{array}{ccccc}0&1&1&1&2\\0&0&1&2&2\end{array}\right)$, and the obvious path up the middle of the square:

<img src="http://latex.codecogs.com/gif.latex?\xymatrix{%26(1,2)\ar@{-}[d]\ar@{-}[r] %26 (2,2)\\
%26(1,1)\ar@{-}[d] %26\\
(0,0)\ar@{-}[r]%26(1,0)%26}"/>

From $(1 \lt 2)$ or $(0\lt3)$, there is only on way to go, namely to $(1 \lt 3)$ and a 2-step path (left to you), and, finally it is just one step from  $(1 \lt 3)$ to $(2 \lt 3)$ and the other extremal path.
####Summary####

Each path corresponds to a simplex of maximal dimension in the product. The poset encodes the simplest relationships between those paths with the links in the Hasse diagram corresponding to simple changes in the path, and adjacency of the two simplices in the product, but note that the poset is usually not linear.

[[!redirects product of simplices]]
[[!redirects products of simplices]]
