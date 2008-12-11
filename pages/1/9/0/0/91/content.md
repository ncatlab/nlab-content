#Idea#

Globular sets are to [[simplicial set]]s as [[globe]]s are to simplices.

#Definition#


  The **globular category** $G$ is
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

  for all $n \in \mathbb{N}$ subject to the relations

  $$
    \sigma_{n+1}\circ \sigma_n = \tau_{n+1} \circ \sigma_n
  $$
  $$
    \sigma_{n+1}\circ \tau_n = \tau_{n+1} \circ \tau_n
  $$
  $$
    \iota_n \circ \sigma_n = \mathrm{Id}
  $$
  $$
    \iota_n \circ \tau_n = \mathrm{Id}
    \,.
  $$

  A
  **globular object**
  $S$ [[internalization|internal to]] a category $K$
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
  and call $S_n$ the **collection of $n$-cells** of **$n$-[[globe]]s**; $s_n$ the $(n+1)$st **source map** and $t_n$ the    
  $(n+1)$st
  **target map** and $i_n$ the $n$th 
  **identity assigning map**.

  The relations
  $$
    s_n \circ s_{n+1} = s_n \circ t_{n+1}
  $$
  $$
    t_n \circ s_{n+1} = t_n \circ t_{n+1}
  $$
  $$
    s_n \circ i_n = \mathrm{Id}
  $$
  $$
    t_n \circ i_n = \mathrm{Id}
  $$

  which these satisfy by functoriality for all $n \in \mathbb{N}$
  are called the **globular identities**.

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
