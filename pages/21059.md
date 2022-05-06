
### M2-M5 brane bound states in the BMN matrix model
 {#M2M5BraneBoundStatesInTheBMNMatrixModel}

There is the suggestion  ([MSJVR 02](BMN+matrix+model#MSJVR02), checked in [AIST 17](BMN+matrix+models#AIST17)) that, in the [[BMN matrix model]], [[supersymmetry|supersymmetric]] [[M2-M5-brane bound states]] are identified with [[isomorphism classes]] of certain "limit sequences" of longitudinal-[[light cone]]-[[constant function|constant]] $N \times N$-[[matrix]]-[[field (physics)|fields]] constituting [[finite-dimensional vector space|finite-dimensional]] [[complex numbers|complex]] [[Lie algebra representations]] of [[su(2)]].

Concretely, if

$$
  \underset{ i }{\oplus}  
  \big(
    N^{(M2)}_i \cdot \mathbf{N}^{(M5)}_i
  \big)
  \;\;\in\;\;
  \mathfrak{su}(2)Rep^{fin}
$$

denotes [[generalized the|the]] [[Lie algebra representation|representation]] containing 

* $N^{(M2)}_i$ [[direct sum|direct summands]]

of [[generalized the|the]]

* $N^{(M5)}_i$-[[dimension|dimensional]] [[irrep]] $\mathbf{N}^{(M5)}_i \in \mathfrak{su}(2)Rep$

(for $\{N^{(M2)}_i, N^{(M5)}_i\}_{i} \in (\mathbb{N} \times \mathbb{N})^I$ some [[finite set|finitely]] [[indexed set]] of [[pairs]] of [[natural numbers]])

with total [[dimension]]

$$
  N 
    \;\coloneqq\; 
  dim
  \big( 
    \underset{ i }{\oplus}  
    \big(
      N^{(M2)}_i \cdot \mathbf{N}^{(M5)}_i
    \big)    
  \big)
$$

then:

1. an [[M5-brane]] configuration corresponds to a [[sequence]] of such representations for which 
 
   $N^{(M2)}_i \to \infty$ 

   for fixed $N^{(M5)}_i$

   and fixed [[ratios]] $N^{(M2)}_i/N$;

1. an [[M2-brane]] configuration corresponds to a [[sequence]] of such representations for which 
 
   $N^{(M5)}_i \to \infty$ 

   for fixed $N^{(M2)}_i$

   and fixed [[ratios]] $N^{(M5)}_i/N$ 

for all $i \in I$.

Hence, by extension, any other sequence of finite-dimensional $\mathfrak{su}(2)$-representations is a kind of mixture of these two cases, interpreted as an [[M2-M5 brane bound state]] of sorts.


To make this precise, let 

$$
  \mathfrak{sl}(2,\mathbb{C})MetMod_{/\sim}
  \;\in\;
  Set
$$

be the [[set]] of [[isomorphism classes]] of [[complex numbers|complex]] [[metric Lie representations]] (hence [[finite-dimensional vector space|finite-dimensional representations]]) of [[su(2)]] (of $\mathfrak{sl}(2,C)$) and write 

$$
  Span
  \big(
    \mathfrak{sl}(2,\mathbb{C})MetMod_{/\sim}
  \big)
  \;\in\;
  Vect_{\mathbb{C}}
$$

for its [[linear span]] (the [[complex vector space]] of [[formal linear combinations]] of [[isomorphism classes]] of [[metric Lie representations]]).

Finally, write 
 
$$
  \array{
    Span
    \big(
      \mathfrak{sl}(2,\mathbb{C})MetMod_{/\sim}
    \big)
    &
      \longrightarrow
    &
    \big(
      \mathcal{W}^{{}^{s}}
    \big)^n
    \\
    c_1 \cdot V_1
    +
    c_2 \cdot V_2
    \\
    &\mapsto&
    c_1 \cdot Tr_{V_1}\big( - \big)
    +
    c_2 \cdot Tr_{V_2}\big( - \big)
  }
$$

for the [[linear map]] which sends a [[formal linear combination]] or representations to the [[weight system]] on [[Sullivan chord diagrams]] with $n \in \mathbb{N}$ chords which is given by [[trace|tracing]] in the given representation.

Then the normalization  


