
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A bisimplicial set is a [[bisimplicial object]] in [[Set]].


## Properties

### Diagonal
 {#Diagonal}

+-- {: .num_defn }
###### Definition
**(diagonal)**

For $X_{\bullet,\bullet}$ a bisimplicial set, its **diagonal** is the simplicial set that is the precomposition with $(Id, Id) : \Delta^{op} \to \Delta^{op} \times \Delta^{op}$, i.e. the simplicial set with components

$$
  d(X)_n = X_{n,n}
  \,.
$$

=--


+-- {: .num_defn }
###### Definition
**(realization)**

The **realization** $|X|$ of a bisimplicial set $X_{\bullet,\bullet}$ is the [[simplicial set]] that is given by the [[coend]]

$$
  |X| =  \int^{[n] \in \Delta} X_{n, *} \times \Delta[n]
$$

in [[sSet]].

=--

+-- {: .num_prop }
###### Proposition
**(diagonal is realization)**

For $X$ a bisimplicial set, its diagonal $d(X)$ is (isomorphic to) its realization $|X|$:

$$
  |X| \simeq d(X)
  \,.
$$


=--


This is for instance exercise 1.6 in  in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) [Goerss-Jardine](#GoerssJardine). For a derivation see the examples at _[[homotopy colimit]]_.



+-- {: .num_prop }
###### Proposition
**(diagonal is homotopy colimit)**

The diagonal of a bisimplicial set $X_{\bullet,\bullet}$ is also (up to weak equivalence) the [[homotopy colimit]] of $X$ regarded as a simplicial diagram in the [[model structure on simplicial sets]]

$$  
  diag X \simeq hocolim (X : \Delta^{op} \to sSet_{Quillen})
  \,.
$$

=--

This appears for instance as theorem 3.6 in ([Isaacson](#Isaacson)).

+-- {: .proof}
###### Proof

This follows with the above equivalence to the [[coend]] $diag X \simeq \int^{[k] \in \Delta} \Delta[k] \cdot X_k$ and general expression of  [[homotopy colimit]]s by coends (as discussed there) in terms of the [[Quillen bifunctor]]

$$
  \int^\Delta (-) \cdot (-)
    :
   [\Delta, sSet_{Quillen}]_{Reedy} \times
   [\Delta, sSet_{Quillen}]_{Reedy}  
  \to 
    sSet_{Quillen}
$$

in [[Reedy model structure]]s (as discussed there) by using that $\Delta[-] : \Delta \to sSet_{Quillen}$ is a Reedy cofibrant resultion of the point in $[\Delta, sSet_{Quillen}]$ and that every object in $[\Delta^{op}, sSet_{Quillen}]_{Reedy}$ is cofibrant.
=--

+-- {: .num_prop }
###### Proposition
**(degreewise weak equivalences)**

Let $X,Y : \Delta^{op} \times \Delta^{op} \to Set$ be bisimplicial sets.
A morphism $f : X \to Y$ which is degreewise in one argument a weak equivalence
$f_{n,\bullet} : X(n,\bullet) \to Y(n,\bullet)$ induces a weak equivalence 
$d(f) : d(X) \to d(Y)$ of the associated diagonal simplicial sets
(with respect to the standard [[model structure on simplicial sets]]).

=--


+-- {: .proof}
###### Proof

This is prop 1.9 in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* Goerss-Jardine, _Simplicial Homotopy Theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)) 

=--

### Total d&#233;calage and total simplicial sets
 {#TotalSimplicialSets}

There is a [[functor]] called _[[ordinal sum]]_ (see also at [[simplex category]])

$$
  + : \Delta^\op \times \Delta^{op} \to \Delta^{op}
  \,.
$$

$$
  + : [k], [l] \mapsto [k+l+1]
  \,.
$$

This induces an [[adjoint triple]]

$$
  ssSet
   \stackrel{\overset{+_!}{\longrightarrow}}{\stackrel{\overset{+^*}{\longleftarrow}}{\underset{+_*}{\longrightarrow}}}
  sSet
  \,.
$$

+-- {: .num_defn }
###### Definition

Here 

* $T \coloneqq +_*$ is called the **total simplicial set** functor or **Artin-Mazur codiagonal** (we will use the first of these as codiagonal also has another accepted meaning, see [[codiagonal]]);

* $Dec \coloneqq +^*$ is called the [[total décalage]] functor (inside which is plain [[décalage]]);

=--

+-- {: .num_prop }
###### Proposition

$T$ preserves degreewise [[weak equivalences]] of [[simplicial sets]].

=--

+-- {: .num_prop #TotalAndDiagonal}
###### Proposition

For $X$ any bisimplicial set 

* the canonical morphism
 
  $$
    diag X \to T X
  $$

  from the [[diagonal]] to the total simplicial set is a [[weak equivalence]] in the [[model structure on simplicial sets]];

* the [[unit of an adjunction|adjunction unit]]

  $$
    X \to T Dec X
  $$

  is a weak equivalence.

=--

These statements are for instance in ([CegarraRemedios](#CegarraRemedios)) and ([Stevenson](#Stevenson)). They may be considered as a non-additive versions of the [[Eilenberg-Zilber theorem]]. 

+-- {: .num_remark }
###### Remark

By prop. \ref{TotalAndDiagonal} and the  usual _[[Eilenberg-Zilber theorem]]_ it follows
that under forming chain complexes for [[simplicial homology]], total simplicial sets correspond to [[total complexes]] of [[double complexes]].

=--


+-- {: .num_remark }
###### Remark

After [[geometric realization]] these spaces are even related by a [[homeomorphism]].

=--

(This seems to be due to Berger and H&#252;bschmann, but related results were known to Zisman as they are so mentioned by Cordier in his work on homotopy limits.)


+-- {: .num_remark }
###### Remark

The standard [[delooping]] functor for [[simplicial groups]]

$$
  \bar W : sGrp \to sSet_*
$$

is the composite

$$
  \bar W 
   : 
  sGrp
   \stackrel{\mathbf{B}}{\longrightarrow}
  sGrpd
   \stackrel{N}{\longrightarrow}
  ssSet
   \stackrel{T}{\longrightarrow}
  sSet
  \,.
$$

=--

We have the following explicit formula for $ T X$, attributed to [[John Duskin]]:

+-- {: .num_lemma }
###### Lemma

For $X$ a [[bisimplicial set]] the total simplicial set 
$T X$ is in degree $n$ the [[equalizer]]

$$
  (T X)_n 
  \to
  \prod_{i = 0}^n X_{i, n-i}
  \stackrel{\longrightarrow}{\longrightarrow}
  \prod_{i = 0}^{n-1}
  X_{i, n-i-1}
$$

where the components of the two morphisms on the right are

$$
  \prod_{i = 0}^n X_{i,n-i}
   \stackrel{p_i}{\to}
  X_{i, n-i}
 \stackrel{d_0^v}{\to}
  X_{i, n-i-1}
$$

and

$$
 \prod_{i = 0}^n X_{i,n-i}
  \stackrel{p_{i+1}}{\to}
  X_{i+1,n-i-1}
  \stackrel{d_{i+1}^h}{\to}
  X_{i,n-i-1}
 \,.
$$

The face maps $d_i : (T X)_n \to (T X)_{n-1}$
are given by

$$
  d_i 
    =
  (d_i^v p_0, 
   d_{i-1}^v p_1,
   \cdots,
   d_1^v p_{i-1},
   d_i^h p_{i+1},
   d_i^h p_{i+2},
   \cdots,
   d_i^h p_n
  )
$$

and the degeneracy maps are given by

$$
  s_i 
  =
  (s_i^v p_0, s_{i-1}^v p_1, \cdots, 
   s_0^v p_i, s_i^h p_{i+1}, \cdots, 
   s_i^h p_n)
  \,.
$$

The $(Dec \dashv T)$-[[unit of an adjunction|adjunction unit]] $\eta : X \to T Dec X$ is given in degree $n$ by

$$
  \eta : x \mapsto 
   (s_0(x), s_1(x), \cdots, s_n(x))
  \,.
$$

=--

### Geometric realization

See [[geometric realization of simplicial topological spaces]].

## Model structures

There are various useful [[model category]] structures on the category of bisimplicial sets.

### Induced from the diagonal

There is an [[adjunction]]

$$
  (L \dashv diag)   : 
  ssSet
  \stackrel{\overset{L}{\longleftarrow}}{\underset{diag}{\longrightarrow}}
  sSet 
  \,.
$$

The [[transferred model structure]] along this adjunction of the standard [[model structure on simplicial sets]] exists and with respect to it the above [[Quillen adjunction]] is a [[Quillen equivalence]].

This is due to ([Moerdijk 89](#Moerdijk))

### Induced from codiagonal $T$.

The [[transferred model structure]] on $ssSet$ along the total simplicial set functor $T$ exists. And for it 

$$
  (Dec \dashv T) : ssSet 
    \stackrel{\overset{Dec}{\longleftarrow}}{\underset{T}{\longrightarrow}}
   sSet
$$ 

is a [[Quillen equivalence]].


+-- {: .num_prop }
###### Proposition

Every diag-fibration is also a $T$-fibration.

=--

This is ([CegarraRemedios, theorem 9](#CegarraRemedios)).

#### Remark on notation

There are two uses of $\bar W$ in this area, one is as used in ([CegarraRemedios](#CegarraRemedios)) where it is used for the codiagonal (sometimes denoted "$\nabla$" or $T$ as above), the other is for the [[classifying space]] functor for a [[simplicial group]]. This latter is not only the older of the two uses, but also comes with a related $W$ construction.  The relationship between the two is that given a simplicial group or simplicially enriched groupoid, $G$, applying the [[nerve]] functor in each dimension gives a bisimplicial set and $\bar{W}G = T Ner G$. Because of this, some care is needed when using these sources.

## Bisimplicial abelian groups 


+-- {: .num_prop }
###### Proposition

Let $A,B : \Delta^{op} \times \Delta^{op} \to Ab$ be bisimplicial abelian groups.
A morphism $f : A \to B$ which is degreewise in one argument a weak equivalence
$f_{n,\bullet} : A(n,\bullet) \to B(n,\bullet)$ induces a weak equivalence 
$d(f) : d(A) \to d(B)$ of the associated diagonal complexes.

=--


+-- {: .proof}
###### Proof

This is Lemma 2.7 in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of ([GoerssJardine](#GoerssJardine))


=--

## References

Some standard material is for instance in

* [[Paul Goerss]] and [[Rick Jardine]], _Simplicial Homotopy Theory_
{#GoerssJardine}

* [[Rick Jardine]], Lecture 008 (2010) ([pdf](http://jardine.math.uwo.ca/HomTh/lecture008a.pdf))

* [[Samuel Isaacson]], _Excercises in homotopy colimits_ ([pdf](http://www-math.mit.edu/~mbehrens/TAGS/Isaacson_exer.pdf))
{#Isaacson}

The total simplicial set functor goes back to

* [[M. Artin]], [[B. Mazur]], _On the Van Kampen theorem_ , Topology 5 (1966) 179&#8211;189.

The diagonal, total d&#233;calage and total simplicial set constructions are discussed in

* [[Antonio Cegarra]], [[Josué Remedios]], _The relationship between the diagonal and the bar constructions on a bisimplicial set_, Topology and its applications, volume 153 (1)  (2005) ([pdf](http://www.ugr.es/~acegarra/Paperspdfs/TRBDWC.pdf))

* [[Antonio Cegarra]], [[Josué Remedios]], _The behaviour of the $\bar W$-construction on the homotopy theory of bisimplicial sets_, Manuscripta Mathematica, volume 124 (4) Springer (2007)
 {#CegarraRemedios}

* [[Danny Stevenson]], _D&#233;calage and Kan's simplicial loop group functor_ ([arXiv:1112.0474](http://arxiv.org/abs/1112.0474)){#Stevenson}

* [[Viktoriya Ozornova]], [[Martina Rovelli]], _The unit of the total décalage adjunction_, Journal of Homotopy and Related Structures (2020) 15:333–349, [doi.org/10.1007/s40062-020-00257-1](https://doi.org/10.1007/s40062-020-00257-1)



The diagonal-induced model structure on $ssSet$ is discussed in

* [[Ieke Moerdijk]], _Bisimplicial sets and the group completion theorem_  in _Algebraic K-Theory: Connections with Geometry and Topology_, pp 225&#8211;240. Kluwer, Dordrecht (1989)
 {#Moerdijk}

The behaviour of fibrations under [[geometric realization]] of bisimplicial sets is discussed in

* D. Anderson, _Fibrations and geometric realization_ , 
Bull. Amer. Math. Soc. Volume 84, Number 5 (1978), 765-788. ([ProjEuclid](http://projecteuclid.org/euclid.bams/1183541139))

Discussion of respect of $\bar W$ for fibrant objects is discussed in fact 2.8 of 

* [[Antonio M. Cegarra]], Benjam&#237;n A. Heredia, Josu&#233; Remedios, _Double groupoids and homotopy 2-types_ ([arXiv:1003.3820](http://arxiv.org/abs/1003.3820))


[[!redirects bisimplicial set]]
[[!redirects bisimplicial sets]]

[[!redirects simplicial simplicial set]]
[[!redirects simplicial simplicial sets]]

[[!redirects total simplicial set]]
[[!redirects total simplicial sets]]

[[!redirects total décalage]]