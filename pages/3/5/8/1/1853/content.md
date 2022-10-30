
# Idea #

The cup product on [[cohomology]] is an operation on cocycles with coefficients in $A$ induced from a pairing morphism

$$
  A_1 \times A_2 \to A_3
$$

If $g_1 : X \to A_1$ and $g_2 : X \to A_2$ are two cocycles in $\mathbf{H}(X,A_1)$ and $\mathbf{H}(X,A_2)$, respectively, then their cup product with respect to this pairing is the cocycle

$$
  g_1 \cdot g_2 : X \stackrel{Id \times Id}{\to}
  X \times X
  \stackrel{g_1 \times g_2}{\to}
  A_1 \times A_2
  \to
  A_3
$$

in $\mathbf{H}(X,A_3)$.

# On singular cohomology #

Often in the literature by _cup product_ is meant specifically the realization of the cup product on [[singular cohomology]].

For $X$ a [[topological space]], let $\Pi(X)_\bullet := X^{\Delta_{Top}^\bullet}$ be the [[simplicial set]] of $n$-[[simplex|simplices]] in $X$ -- the [[fundamental ∞-groupoid]] of $X$.

For $R$ some [[ring]], let $Maps(\Pi(X),R)^{\bullet}$ be the [[simplicial object|simplicial ring]] of $R$-valued functions on the spaces of $n$-simplices. The corresponding [[Moore complex|Moore cochain complex]] $C^\bullet(X)$ is the cochain complex whose [[chain homology and cohomology|cochain cohomology]] is the [[singular cohomology]] of the space $X$: a homogeneous element $\omega_p \in C^p(X)$ is a function on $p$-simplices in $X$.

Write, as usual, for $p \in \mathbb{N}$, $[p] = \{0 \lt 1 \lt \cdots \lt p\}$ for the [[poset|totally ordered set]] with $p+1$ elements. For $\mu : [p] \to [p+q]$ an injective order preserving map and $K$ some [[simplicial object|cosimplicial object]], write $d_\mu^* K : K^p \to K^{p+q}$ for the image of this map under $K$.

Specifically, for $p,q \in \mathbb{N}$ let $L : [p] \to [p+q]$ be the map that sends $i \in [p]$ to $i \in [p+q]$ and let $R : [q] \to [p+q]$ be the map that sends $i \in [q]$ to $i+q \in [p+q]$. 

Then the **cup product** 

$$
  \smile : C^\bullet(X) \otimes C^\bullet(X)
   \to C^\bullet(X)
$$

is the cochain map that on homogeneous elements $a \otimes b \in C^p(X) \otimes C^q(X) \subset C^\bullet(X) \otimes C^\bullet(X)$ is defined by the formula

$$
  a \smile b = (d_L^* a) \cdot (d_R^* b)
  \,.
$$

This means that $(a \smile b)_{i_0, \cdots, i_{p+q}} = a_{i_0, \cdots, i_p} \cdot b_{i_p, \cdots, i_{p+q}}$.

+-- {: .un_prop }
###### Proposition

This cup product enjoys the following properties:

* it is indeed a cochain complex morphism as claimed, in that it respects the differential: for any homogeneosu $a\otimes b \in C^p(X) \otimes C^q(X)$ as above we have
  
  $$
    d(a \smile b) = (d a) \smile b + (-1)^p a \smile (d b)
    \,.
  $$
 
* the image of the cup product on [[chain homology and cohomology|cochain cohomology]]

  $$
     \smile :  H^\bullet(C^\bullet(X))\otimes H^\bullet(C^\bullet(X)) \to H^\bullet(C^\bullet(X))
  $$

  is associative and distributes over the additon in $H^\bullet(C^\bullet(X))$.

=--


Accordingly, the cup product makes $H^\bullet(C^\bullet(X)) = H^\bullet(X,R)$ into a [[ring]]: the **cohomology ring** on the [[Eilenberg-MacLane spectrum|ordinary cohomology]] of $X$.


See for instance section 3.2 of 

* Hatcher, _Algebraic Topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html) [pdf](http://www.math.cornell.edu/~hatcher/AT/AT.pdf))


# In abelian sheaf cohomology #

Traditionally the cup product is considered for 
abelian cohomology, such as [[generalized (Eilenberg-Steenrod) cohomology]] and more generally [[abelian sheaf cohomology]].

In that case all coefficient objects $A_i$ are complexes $(A_i)_\bullet$ of sheaves and the pairing that one usually considers is the [[tensor product]] of [[chain complex]]es

$$
  (A_1)_\bullet \times (A_2)_\bullet \to (A_1 \otimes A_2)_\bullet
$$

where

$$
  (A_1 \otimes A_2)_n = \oplus_p (A_1)_p \otimes (A_2)_{n-p}
  \,.
$$

with differential 

$$
  d (a_1 \otimes a_2) = (d a_1) \otimes a_2 + (-1)^{|a_1|} a_1 \otimes d a_2
  \,.
$$

## In abelian &#268;ech cohomology ##

The cup product has a simple expression in abelian [[?ech cohomology]].

For $\alpha \in C(U,A_1)_\bullet$ and $\beta \in C(U,A_2)_\bullet$ two &#268;ech cocycles with respect to the same cover $\{U_i \to X\}$ of $X$, their cup product is simply the cocycle in $C(U, A_1 \otimes A_2)$ given by

$$
  (\alpha \cdot \beta)_{i_0, \cdots , i_{p + q}}
  \;:=\;
  \alpha_{i_0, \cdots, i_p} \otimes \beta_{i_p, \cdots i_{p+q}}
  \,.
$$