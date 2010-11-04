[[!redirects shuffles]]


#Contents#
* table of contents
{:toc}
 
##Idea

The term 'shuffle' conjures up the idea of shuffling a pack of cards. In fact the mathematical idea is nearer to shuffling two packs of cards one through the other. Suppose we have a pack of $p$ cards and a pack of $q$ cards and we build a pack of $p+q$ cards, whilst retaining the order on the two 'sub-packs'.  The result is a $(p,q)$-shuffle. 

## Definition

+-- {: .un_defn}
###### Definition

For $p,q \in \mathbb{N}$ two [[natural number]]s, a **$(p,q)$-shuffle** is a [[permutation]]

$$
  (\mu_1, \cdots, \mu_p, \nu_1, \cdots, \nu_q)
$$

of $(1,2, \cdots, p+q)$ subject to the condition that

$$  
  \mu_1 \lt \mu_2 \lt \cdots \lt \mu_p
$$

and

$$  
  \nu_1 \lt \nu_2 \lt \cdots \lt \nu_q
  \,.
$$

The **signature** of a $(p,q)$-shuffle is the [[signature of a permutation|signature]] of the corresponding permutation.

=--

## Applications 

### Products of simplices

Shuffles are interesting combinatorial structures but the reason why they come into many constructions in [[homotopy theory]] and [[higher category theory]] is because of their relationship with the structure of [[product]]s.

The definition of the product, $K\times L$, of [[simplicial set]]s $K$ and $L$ gives that $(K\times L)_k$ is defined to be $K_k\times L_k$ with face and degeneracy maps defined 'componentwise' so, for instance, $d_i(x,y) = (d_i x,d_i y)$.  This means that a [[simplex]] $(s_\alpha x, s_\beta y)$ can be non-degenerate even though its two components are degenerate.  Of course, this happens exactly when $\alpha \cap \beta = \emptyset$.  (Here we mean by $s_\alpha$ the composite, in order,  of the $s_i$ for $i \in \alpha$.)

In particular, take $K = \Delta[p]$ and $L= \Delta[q]$ with $x_p \in \Delta[p]_p$, $y_q \in \Delta[q]_q$, the 'identity' simplices that generate them.  (We will use an _ad hoc_ notation here, since the more obvious, $\iota_p$, and  $\iota_q$, would not distinguish the two simplices sufficiently in some formulae.)  There are, then,  non-degenerate simplices of dimension $p+q$, but none of higher dimension in $\Delta[p]\times \Delta[q]$.  These are of the form $(s_\alpha x_p,s_\beta y_q)$, where $\#\alpha = q$, $\#\beta = p$.



#### Non-degenerate simplices in a product 


If we represent a vertex of a product by a 'column vector' rather than the more usual 'row vector' for the moment, then any non-degenerate $(p+q)$-simplex of $\Delta[p]\times \Delta[q]$ can be represented in the form of an ordered list of vertices,

$$\left(\begin{array}{ccccccccc}
0& \ldots & 0 & 1 & \ldots & 1 & 2 & \ldots & p\\
0& \ldots & i & i & \ldots & j & j & \ldots & q
\end{array}\right),$$

with $p + q + 1 $ columns.  The top row, which is a simplex  in $\Delta[p]$, changes at exactly those positions at which the bottom row repeats.  The top row gives a degenerate $p+q$ simplex of $\Delta[p]$, whilst the bottom row one of $\Delta[q]$, i.e., the array gives $(s_\alpha x_p, s_\beta y_q)$ for some $(\alpha, \beta)$  as above.

#### Illustrative example 

The usual illustrative example is of the three 3-simplices of $\Delta[2]\times \Delta[1]$:

1. $\left(\begin{array}{cccc}0&1&2&2\\0&0&0&1\end{array}\right)$, 

1. $\left(\begin{array}{cccc}0&1&1&2\\0&0&1&1\end{array}\right)$, 

1. $\left(\begin{array}{cccc}0&0&1&2\\0&1&1&1\end{array}\right)$

with, for 1), $\alpha = (2)$, $\beta = (1,0)$; for 2) $\alpha = (1)$, $\beta = (2,0)$; and, for 3), $\alpha = (0)$, $\beta = (2,1)$.

#### Simplices of the product and partitions

Each such simplex yields a partition of $\{0, \ldots, p+q-1\}$ into two disjoint sets,
 $\mu_1\lt\ldots \lt\mu_p$, and $\nu_1 \lt \ldots \lt \nu_q$, and vice versa. Suppose that we have an array, as above, written

 $$\left(\begin{array}{cccc}
i_0& i_1&\ldots & i_{p+q}\\
j_0& j_1 & \ldots & j_{p+q}
\end{array}\right),$$

with $0= i_0 \leq i_1 \leq \ldots \leq i_{p+q}= p$, then if $i_k = i_{k+1}$, we put $k$ into the second set, otherwise $k$ is put in the first set.  This, of course, leads to an operation that preserves order. For instance, in the above example 2., the $i$-sequence is $(0,1,1,2)$, so there is the single repeat with $k = 1$, and $\nu = \{1\}$. 

We likewise require $0= j_0 \leq j_1 \leq \ldots \leq j_{p+q}= p$, and put $k$ into the first set if  $j_k = j_{k+1}$.  For the example, we have the $j$-sequence is $(0,0,1,1)$, so $\mu = \{ 0,2\}$.  Of course, from the partition you can get the sequences and conversely. The attentive reader will, of course, have noted that, for example 2., the $\alpha$, we specified was exactly the $\nu$, and the $\beta$ was the $\mu$.  This is general with the simplex corresponding to a partition, $(\mu,\nu)$,  being given by $(s_{\nu_q}\ldots s_{\nu_1}x_p,s_{\mu_p}\ldots s_{\mu_1}y_q)$.

### Eilenberg-Zilber map

Related to the product of simplices: shuffles control the [[Eilenberg-Zilber map]]. See there for details.


[[!redirects shuffles]]