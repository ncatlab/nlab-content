#Idea#

Globular sets are to [[simplicial sets]] as [[globes]] are to simplices.

#Definition#

A _globular set_ is a [[presheaf]] on the _globe category_ (described below), one of the [[geometric shapes for higher structures]].

* The presheaf definition is to be understood from the point of view of [[space and quantity]]: a _globular set_ is a space characterized by the fact that and how it may be _probed_ by mapping standard globes into it: the set $S_n$ assigned by a globular set to the standard $n$-globe $[n]$ is the set of $n$-globes in this space, hence the way of mapping a standard $n$-globe into this spaces.



  The **[[globe category]]** $G$ is
  the category whose objects are the integers and
  whose morphisms are generated from

  $$
    \sigma_n : [n] \to [n+1]
  $$
  $$
    \tau_n : [n] \to [n+1]
  $$
  $$
    \iota_n : [n+1] \to [n]
  $$

  for all $n \in \mathbb{N}$ subject to the relations (dropping obvious subscripts)

  $$
    \sigma\circ \sigma = \tau \circ \sigma
  $$
  $$
    \sigma\circ \tau = \tau \circ \tau
  $$
  $$
    \iota \circ \sigma = \mathrm{Id}
  $$
  $$
    \iota \circ \tau = \mathrm{Id}
    \,.
  $$

  A
  **globular object**
  $S$ [[internalization|in]] a category $K$
  is a functor $S : G^{\mathrm{op}} \to K$.
  In particular, for $K = Sets$ we say $S$ is a
  **globular set**.

  For $n \in \mathbb{N}$ we write

  $$
    S_n := S(n) 
  $$
  $$
    s_n := S(\sigma_n) : S_{n+1} \to S_{n}
  $$
  $$
    t_n := S(\tau_n) : S_{n+1} \to S_{n}
  $$
  $$
    i_n := S(\iota_n) : S_{n} \to S_{n+1}
  $$
  and call $S_n$ the **collection of $n$-cells**; $s_n$ the $(n+1)$st **source map** and $t_n$ the    
  $(n+1)$st
  **target map** and $i_n$ the $n$th 
  **identity assigning map**.

  The relations (dropping obvious subscripts)
  $$
    s \circ s = s \circ t
  $$
  $$
    t \circ s = t \circ t
  $$
  $$
    s \circ i = \mathrm{Id}
  $$
  $$
    t \circ i = \mathrm{Id}
  $$

are called the **globular identities**.

 +-- {: .query}
[[Marc Olschok|Marc]]:
Perhaps it would be better, not to require reflexivity
(i.e. the map $i$) in these definitions and use
"reflexive globular set" if reflexivity is required?
The way it is phrased now is in conflict with the 
terminology for directed graphs, where one uses 
"reflexive graphs" if these are meant, but allows
graphs without distinguished loops.
=--

 A morphism of globular objects is a natural transformation
  of the corresponding functors.
For the resulting category of globular objects in $K$
we write 

$$
  GlobularObjects(K) := K^{G^{\mathrm{op}}}
$$ 


##Notation for composite globular maps##

The globular identities ensure that

* two sequences of boundary maps
$$
  f_n \circ \cdots \circ f_{n+m-1} \circ f_{n+m} :
  S_{n+m+1} \to S_n
$$

with $n,m \in \mathbb{N}$ and for $f_k, \in \{s_k, t_k\}$ are
equal if and only if their last term $f_n$ coincides;

* for all $n,m \in \mathbb{N}$ we have

$$
    s_n \cdots s_{n+1} \circ \cdots \circ
    s_{n+m} \circ i_{n+m} \circ \cdots \circ i_{n+1} \circ i_n
    =
    \mathrm{Id}
  $$
  $$
    t_n \cdots t_{n+1} \circ \cdots \circ
    t_{n+m} \circ i_{n+m} \circ \cdots \circ i_{n+1} \circ i_n
    =
    \mathrm{Id}
    \,.
  $$

We therefore write

$$
  s_n, t_n : S_{n+m+1} \to S_n
$$
$$
  i_n : S_n \to S_{n+m+1}  
$$

with $i_n, s_n, t_m$ the sequence of $m$
consecutive identity-assigning, source or target maps, respectively.


#Examples#

* A globular set concentrated in degree 0 is just a set. A globular set concentrated in degrees 0 and 1 is a [[directed graph]]. See also [[directed n-graph]].

* The **globular $n$-globe** $G_n$ is the globular set represented by $n$, i.e. $G_n(-) := Hom_G(-,n)$.

#Remarks#

* Globular sets are also referred to as $\omega$-[[omega-graph|graphs]].

* globular sets are based on one of the three major [[geometric shapes for higher structures]].

[[!redirects globular sets]]