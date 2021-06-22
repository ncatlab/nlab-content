
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

This page describes aspects of the combinatorics of [[Cartesian products]] of [[simplicial sets]].

## Properties

+-- {: .un_definition}
###### Notation

For $X$ some [[simplicial set]] $x \in X_p$ some $p$-cell and 
for $\mu = (\mu_1 \lt  \mu_2, \lt \cdots \lt \mu_q)$ a sequence of [[natural numbers]] in $\{0, \cdots p+q\}$, write

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
 $\mu_1\lt\ldots \lt\mu_p$, and $\nu_1 \lt \ldots \lt \nu_q$, and vice versa, any such partition yields a simplex. Suppose that we have an array, as above, written

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

$$\begin{matrix}
(0,1) & - & (1,1) & - & (2,1) \\
| & & | & & | \\
(0,0) & - & (1,0) & - & (2,0)
\end{matrix}$$


The path corresponding to a $(p,q)$-shuffle just follows the list of (transposed pairs of) vertices, so, for instance, 2) goes  
$$\begin{matrix}
 &  & (1,1) & - & (2,1) \\
 & & | & &  \\
(0,0) & - & (1,0) && 
\end{matrix}$$

###The poset of $(p,q)$-shuffles###

Any pair $(p,q)$ yields a [[poset]] relating the various $(p,q)$-shuffles.  

####Easy examples

We will start by giving some elementary examples. (This section can be skipped if you want to move on to the more theoretical analysis of these posets.)

Our $(2,1)$-example is really too simple and small to illustrate this well, but the two cases $(3,1)$ and $(2,2)$ do a much better job, but, even so, we first look at the (2,1) example:
$$\begin{matrix} (0\lt 1)&-&(0\lt 2)&-&(1\lt 2)\end{matrix}$$



(This [[Hasse diagram]] has been laid out horizontally to save space.  The bottom is to the left. The vertex $(0\lt 1)$ corresponds to the shuffle with $\mu_1 = 0, \mu_1 = 1$, and so on.)
 
We need here to explain the partial order.  We take the '$\mu$-signature' of the shuffle, that is, the ordered set $\mu_1\lt\ldots \lt \mu_p$. (Of course, this determines the $\nu$-signature as that is the complement of $\mu$.)

+--{: .un_defn}
######Definition######
Given two $(p,q)$-shuffles, represented by $(\mu, \nu)$ and $(\mu\prime,\nu\prime)$, we set 

$$(\mu, \nu) \leq (\mu\prime,\nu\prime)$$

if, for each $i$ in the range $1\leq i\leq p$, $\mu_i \leq \mu_i\prime.$  We refer to this poset as $(Shuff(p,q),\leq)$.
=--

Going to  $(Shuff(3,1),\leq)$, the poset for $(3,1)$-shuffles,  the fact that $q = 1$ will mean that this poset is again linear:
$$\begin{matrix}
(0 \lt 1 \lt 2) &-& (0 \lt 1 \lt 3)& - &(0 \lt 2 \lt 3)& - &(1 \lt 2 \lt 3)
\end{matrix}$$

This is true in general:

+--{: .un_lemma}
######Lemma
If $p = 1$ or $q = 1$, then  $(Shuff(p,q),\leq)$ is a linear poset.
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

In all cases, each position is obtained from the one immediately to its 'left' by increasing _one_ value, yet remaining with a shuffle.  This is more clearly seen in the (2,2) example, which is no longer linear.  First we display the grid in which things are happening.
$$\begin{matrix}
(0,2) & - & (1,2) & - & (2,2) \\
| & & | & & | \\
(0,1) & - & (1,1) & - & (2,1) \\
| & & | & & | \\
(0,0) & - & (1,0) & - & (2,0)
\end{matrix}$$

We can then look at the shuffle poset, noting again that it is not linear:
$$\begin{matrix}
&&&&(1\lt 2)&&&&\\
&&& \nearrow &&\searrow &&&\\
(0\lt 1)&-&(0\lt 2)&&&&(1\lt 3)&-&(2\lt 3)\\
&&& \searrow && \nearrow &&&\\
&&&&(0\lt 3)&&&&\\
\end{matrix}$$
(Arrows have been used where itex does not seem to have an `headless arrow'! What follows is produced via presheaf.com.)
           
<img src="http://presheaf.com/cache/d2u2r4t67211k1v3i6u4a2403c50323b.png" title="click to go to presheaf.com for editing"/>}


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

####Summary####

Each path corresponds to a simplex of maximal dimension in the product. The poset encodes the simplest relationships between those paths with the links in the Hasse diagram corresponding to simple changes in the path, and adjacency of the two simplices in the product, but note that the poset is usually not linear.

##The Anti-Lex order

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


## References

Exposition in:

* {#Friedman08} [[Greg Friedman]], Section 5 of: _An elementary illustrated introduction to simplicial sets_, Rocky Mountain J. Math. 42(2): 353-423 (2012) ([arXiv:0809.4221](http://arxiv.org/abs/0809.4221), [doi:10.1216/RMJ-2012-42-2-353](https://projecteuclid.org/journals/rocky-mountain-journal-of-mathematics/volume-42/issue-2/Survey-Article-An-elementary-illustrated-introduction-to-simplicial-sets/10.1216/RMJ-2012-42-2-353.full))




[[!redirects product of simplices]]
[[!redirects products of simplices]]
