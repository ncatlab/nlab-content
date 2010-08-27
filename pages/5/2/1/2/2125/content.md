#Contents#
* automatic table of contents
{:toc}


## Idea

The plain [[Dold-Kan correspondence]] establishes an equivalence between (co)[[simplicial group]]s and (co)[[chain complex]]es.

Both these categories carry natural [[monoidal category]] structures. It turns out that the Dold-Kan correspondence does respect this monoidal structure, to some extent strictly, but generally in the sense of [[homotopy theory]] and  [[higher category theory]].

This way it extends to a [[Quillen equivalence]] between [[model categories]] of _[[monoids]]_ in simplicial groups -- [[simplicial ring]]s -- and monoids in chain complexes -- [[dg-algebra]]s. 


## General discussion 

Notice that 

* monoids in the [[category of chain complexes]] are [[differential graded ring]]s

* monoids in the category of simplicial abelian groups are [[simplicial object|simplicial]] [[ring]]s.

If instead we look at chain complexes and [[simplicial object]]s not in [[Ab]] but in [[Vect]] then

* monoids in the [[category of chain complexes]] of vector spaces are [[differential graded algebra]]s

* monoids in the category of simplicial vector spaces are simplicial algebras.

Analogous statements apply to the dual Dod-Kan correspondence, where the monoids in question are accordingly cosimplicial rings and [[differential graded algebras]] with differential of positive degree.

A crucial fact about the [[Dold-Kan correspondence]] is that

* The two functors in the Dold-Kan correspondence respects these monoidal structures, the are (lax) [[monoidal functor]]s.

But their [[adjunction]] fails to be a [[monoidal adjunction]]. As a result, thesy do not induce an [[equivalence of categories]] or even an adjunction between (co)simplicial rings and (co)chain complexes.


There are two different versions of the monoidal Dold-Kan corespondence, which are almost but apparently not entirely formal duals of each other (at least not in the detailed constructions):

* the **simplicial version** that relates [[monoid]]s in abelian [[simplicial group]]s (simplicial rings)  to monoids in [[chain complex]]es (chain [[dg-algebra]]s),

* the **cosimplicial version** that relates monoids in cosimplicial groups ([[cosimplicial algebra|cosimplicial ring]]) to monoidal in co-chain complexes (cochain [[dg-algebra]]s).

The cosimplicial version is made monoidal by replacing the the Moore complex functor by something else, to obtain a [[Quillen equivalence]].
The simplicial version is made monoidal by replacing the other functor by something else.

## Simplicial rings and chain dg-algebras {#simplicial}


The Dold-Kan correspondence (using the normalized chain complex functor) is in one direction [[monoidal category|monoidal]] in the naive (strict, 1-categorical) way, whereas in the other direction it is monoidal only in the expect homotopical sense.

+-- {: .un_lemma }
###### Lemma

The [[Moore complex]] functor

$$
  C_\bullet : sAb \to Ch_+
$$

as well as the normalized [[Moore complex]] functor

$$
  N_\bullet : sAb \to Ch_+
$$

is a [[monoidal functor|symmetric lax monoidal]] as well as [[lax comonoidal functor|lax comonoidal]]. And in a compatible way: it is actually a _Frobenius monoidal functor_ .


=--

+-- {: .proof}
###### Proof

The proof of symmetric lax monoidalness can be found for instance in 

* Weibel, _An introduction to homological algebra_, section 8.5.4

The lax monoidal transformation that exhibits the lax-monoidalness of the Moore chain complex functor is the [[shuffle map]]. Its component 

$$
  \nabla_{A,B} : (N_\bullet A) \otimes (N_\bullet B))
  \to N_\bullet (A \otimes B)
$$

on a pair $A,B$ of simplicial abelian groups is the morphism of [[chain complex]]es that sends homogeneous elements $a_p\otimes b_q \in A_p \otimes B_q =: C_p(A) \otimes C_q(B)$ to

$$
  \nabla_{A,B}(a \otimes B)
  =
  \sum_{(\mu,\nu)}  sign(\mu,\nu) (s_\nu a) \otimes s_\mu(b) 
  \in
  C_{p+q}(A \otimes B) = A_{p+q}\otimes B_{p+q}  
  \,.
$$

Here the sum is over all $(p,q)$-shuffles, i.e. permutation $\{\mu_1, \dots, \mu_p, \nu_1, \cdots, \nu_q\}$ of the set $\{0,1,\cdots,p+q-1\}$ that leave the first $p$ and the last $q$ elements in their natural order.

The sign in the above sum is the corresponding sign of this permutation and the degeneracy maps $s_\mu$ and $s_\nu$ denote the maps

$$
  s_\mu := s_{\mu_p} \cdots \circ s_{\mu_1}
$$

and similarly for $s_\nu$

>(Hm, is that consistent?)

For more on this see also section 2.3 of [SchwedeSchipley](http://arxiv.org/abs/math.AT/0209342)

The comonoidalness and Frobenius monoidalness of the normalized Moore functor is discussed in

* Marcelo Aguiar, Swapneel Mahajan, _Coxeter Groups and Hopf Algebras_ Fields Institute Monographs, vol. 23 [pdf](http://www.math.tamu.edu/~maguiar/monograph.pdf)

and with more details in

* Marcelo Aguiar, Swapneel Mahajan, _Monoidal functors, species and Hopf algebras_, [pdf, over 6 Mb](http://www.math.tamu.edu/~maguiar/a.pdf) version June 18, 2009, 672 pages.

=--

Since the normalized Moore complex functor $N_\bullet$ is an equivalence of categories, by [[doctrinal adjunction]] its inverse nerve functor $\Xi : Ch_+ \to sAb$ also acquires a monoidal and an opmonoidal structure.  (See te formula on the top of page 296 of Schwede-Shipley.) This monoidal structure can also be given in a [[higher category theory|higher categorical]], i.e. [[homotopy theory|homotopical]] way.
This is the content of the following statements.

In **characteristic zero** there is also a Dold--Kan correspondence between simplicial algebras and $\mathbb{N}$-graded chain [[dg-algebra]]s 

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))


Further work along such lines is

* Birgit Richter, _Symmetry properties of the Dold-Kan correspondence_ ([pdf](http://www.math.uni-hamburg.de/home/richter/doldkan.pdf))

This shows that the Dold-Kan map from Chain complexes to simplicial abelian groups is, while not a [[monoidal category|monoidal functor]], an [[E-k-operad|E-infinity monoidal functor]].

This implies that generalized [[Eilenberg?Mac Lane spectra]] on [[differential graded algebra|differential graded commutative algebras]] are [[E-k operad|E-infinity monoids]] in the category of $H \mathbb{Z}$-[[module]] [[spectrum|spectra]].

* Birgit Richter, _Homotopy algebras and the inverse of the normalization functor_ ([pdf](http://www.math.uni-hamburg.de/home/richter/invjpaa.pdf))

This article shows that the inverse $\Xi$ from chain complexes to simplicial abelian groups sends algebras over arbitrary differential graded [[E-k operad|E-infinity-operad]] to [[E-k-operad|E-infinity-algebra]] in simplicial modules, and is part of a [[Quillen adjunction]] for these.


## Cosimplicial rings and cochain dg-algebras {#cosimplicial}

The monoidal Dold-Kan correspondence relating cosimplicial algebras to cochain dg-algebras is considered less prominently explicitly in the literature, but does appear implicitly in much classical work. For instance the classical statement that the [[cochains on simplicial sets]] form a [[dg-algebra]] that is commutative up to coherent higher homotopy, i.e. that is an [[E-k-operad|E-infinity algebra]], is really the statement that the Moore cochain complex functor on cosimplicial algebras of functions on [[simplicial set]]s is an $\infty$-monoidal functor in a suitable sense.

One article that does make a cosimplicial/cochain monoidal Dold-Kan correspondence explicit is


* J.L. Castiglioni, G. Corti&#241;as, 
Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence, J. Pure Appl. Algebra  191  (2004),  no. 1-2, 119--142, [arXiv:math.KT/0306289](http://arxiv.org/abs/math/0306289).

This establishes not quite a [[Quillen equivalence]], but shows that the [[Dold-Kan correspondence]] induces an [[equivalence]] of [[homotopy category|homotopy categories]] for the [[model structure on cosimplicial rings]] and the [[model structure on dg-algebras|model structure on dg-rings]].

However, this article explicitly constructs the (derived) [[adjoint functor]] to the Moore cochain complex functor. 

Explicit discussion of the Moore co-chain complex functor as inducing an $\infty$-monoidal functor seems not to be in the literature explicitly at time of this writing (?), even though various of its aspects are implicit, partly classical, statements. The following tries to make some aspects explicit.

### Alexander--Whitney and shuffle morphisms {#AlexWhitneyShuffle}

A central ingredient in the monoidal Dold-Kan correspondence are the Alexander--Whitney and the shuffle morphisms.

See chapter VI, paragraph 12 of

* A. Dold, _Lectures on algebraic topology_, Grundlehren Math. Wiss. vol 200, Springer-Verlag, New-York-Berlin, 1972

or chapter VIII, paragraph 8 of

* [[Saunders MacLane]], _Homology_ , Grundlehren Math. Wiss. vol 114, Springer-Verlag, Berlin-G&#246;ttingen-Heidelberg, 1963 .

For $A, B$ cosimplicial abelian groups, $C A$ and $C B$ their [[Moore complex|Moore cochain complex]]es, 

the **Alexander--Whitney morphism** is the morphism

$$  
  N A \otimes N B \to N(A \otimes B)
$$

that is given on homogeneous elements $x, y$ of degree $p,q$, respectively, by

$$
  x \otimes y \mapsto  
  \delta^n \circ \cdots \circ \delta^{p+1}(x)
  \;\;\otimes
  \;\;
  \delta^0 \circ \cdots \circ \delta^0
  (y)
  \,.
$$

Notice that for $A = B$ a cosimplicial algebra, further composing this with the product yields the [[cup product]] induced on dg-algebras of cosimplicial algebras. This is spelled out in detail below.

The **shuffle morphism** goes the other way

$$
  C(A \otimes B) \to C A \otimes C B
$$

and is given on homogeneous elements as above by

$$
  x  \otimes y 
  \mapsto
  \sum_{(\mu,\nu)}  
  \epsilon(\mu,\nu)
  \sigma^{\nu_1 - 1}
  \circ \cdots
  \circ
  \sigma^{\nu_q - 1}
  (x)
  \;\; \otimes
  \;\;
  \sigma^{\mu_1 - 1} \circ \cdots \circ
  \sigma^{\mu_p - 1}(y)
$$

where the sum is over all $(p,q)$ [[shuffle]]s $(\mu,\nu)$ and $\epsilon(\mu,\nu)$ is the sign of the shuffle.

Both the Alexander--Whitney morphism as well as the shuffle morphism respect the passage to the normalized [[Moore complex]] $N A$ of $C A$ and hence induce also morphisms

$$
  AW : N A \otimes N B \to N(A \otimes B)
$$

and 

$$
  S : N(A \otimes B) \to N A \otimes N B
  \,.
$$


In this form they satisfy

$$
  S \circ AW  = Id
  \,.
$$ 

See for instance theorem 2.1.a in 

* [[Samuel Eilenberg]], [[Saunders MacLane]], _On the groups $H(\Pi, n)$ II. Methods of computation_ , Ann. Math. (2) 60 (1954), 49 - 139

A quick summary of all this is in section 7 of

* Jos&#233; Burgos Gil, _The regulators of Beilinson and Borel_ ([pdf](http://atlas.mat.ub.es/personals/burgos/files/brbr.pdf))



### Lax monoidalness of the Moore co-chain complex functor 





+-- {: .standout}

[[Urs Schreiber]]:

We claim to show that the [[Moore complex|Moore cochain complex functor]]

$$
  C : CoS(Ab) \to Ch_+^\bullet(Ab)
$$

from cosimplicial abelian groups to cochain complexes is a  [[lax monoidal functor]] with respect to the standard monoidal structures on $CoS(Ab)$ and $Ch_+^\bullet(Ab)$.

This should be old and standard, but somehow explicit statements in the literature to this extent are hard to find.(?) Some central aspects are recalled in [section 7](http://atlas.mat.ub.es/personals/burgos/files/brbr.pdf#page=63) of

* Jos&#233; Burgos Gil, _The regulators of Beilinson and Borel_ ([pdf](http://atlas.mat.ub.es/personals/burgos/files/brbr.pdf))



=--


Every [[monoid]] $K$ in $CoS(An)$ -- a  cosimplicial ring --  the Moore cochain complex $C(K)$ is naturally equipped with the structure of a [[monoid]] in $Ch_+^\bullet(Ab)$ -- a [[differential graded algebra]] -- by letting the product $\smile : C(K)\otimes C(K) \to C(K)$ be given by the composite

$$
  \smile : C(K)\otimes C(K) \stackrel{\mu_{K,K}}{\to} C(K \otimes K) \stackrel{C(-\cdot -)}{\to} C(K)
$$

where 

* $\mu_{K,K}$ is the component of the [[lax monoidal transformation]] that exhibits the lax monoidal structure (the "compositor"); 

* The operation $-\cdot - : K \otimes K \to K$ is the product on $K$.

+-- {: .standout}


This monoidal structure induced from a cosimplicial ring $K$ on its Moore cochain complex on $C(K)$ is the [[cup product]]. 

=--


More precisely, for $X$ a [[topological space]] and $X^{\Delta^n_{Top}}$ the set of $n$-[[simplex|simplices]] in $X$, arranging themselves into the [[simplicial set]] $\Pi(X) = X^{\Delta^\bullet_{Top}}$ -- the [[fundamental ∞-groupoid]] of $X$ -- and for $R$ some [[ring]] let $Maps(\Pi(X),R)$ be the cosimplicial ring of maps $X^{\Delta^n_{Top}} \to R$. 

Then 

* the Moore cochain complex $C(Maps(\Pi(X),R))$ is the cochain complex that computes the [[singular cohomology]] of $X$;

* the monoid structure induced on $C(Maps(\Pi(X),R))$ by the lax monoidalness of the Moore cochain complex functor is the familiar [[cup product]] on [[singular cohomology]].

We now derive this in detail.

+-- {: .standout}

Check.

=--


For $A$ some [[abelian category]] write
$CoS(A)$ for the category of [[simplicial object|cosimplicial object]]s
in $A$ and $Ch_+^\bullet(Ab)$ for the 
[[category of chain complexes|category of cochain complexes]] in $A$
concentrated in non-negative degree -- called connective or $\mathbb{N}$-graded 
cochain complexes.

Recall that the [[Moore complex|Moore cochain complex]] functor

$$
  C : CoS(A) \to Ch_+^\bullet(A)
$$

is an [[equivalence of categories]]. This is the [[Dold-Kan correspondence]].

For $A = $ [[Ab]] with its standard [[monoidal category]] structure $(A,\otimes)$,
there are standard [[monoidal category]]
structures $(CoS(A), \otimes)$ and $(Ch_+^\bullet(X), \otimes)$:

* for $K,L \in CoS(A)$ their [[tensor product]] $K \otimes L$ is the
_degreewise tensor product_, i.e. the cosimplicial object with 
$(K \otimes L)^n = K^n \otimes L^n$ and with cosimplicial maps the
tensor product of the cosimplicial maps in $K$ and $L$.

* for $V,W \in Ch_+^\bullet(A)$ their [[tensor product]] $V \otimes W$
the _graded tensor product_, i.e. the cochain complex with
$(V \otimes W)^n = \oplus_{p+q = n} V^p \otimes W^q$ whose
coboundary map is given on homogeneous elements 
$\nu \otimes \omega\in V^p \otimes W^q$ by
  $$
    d (\nu \otimes \omega) = (d_V \nu) \otimes \omega + (-)^{p} \vu \otimes d_W \omega
    \,.
  $$

With respect to these standard monoidal  structures
the [[Moore complex|Moore cochain complex]] functor $C : CoS(A) \to Ch_+^\bullet(A)$
becomes a [[lax monoidal functor]] with the following lax monoidal 
[[natural transformation]] map 
$\mu : C(-) \otimes C(-) \to C(-\otimes -) : CoS(A) \times CoS(A) \to Ch_+^\bullet(A)$ .

+-- {: .un_defn}
###### Definition (lax monoidal structure on Moore cochain complex functor)

For $K,L \in CoS(A)$ define the component map

$$
  \mu_{K,L} : C(K)\otimes C(L) \to C(K \otimes L)
$$
 
by defining it on homogeneous elements 

$a\otimes b \in C^p(K)\otimes C^q(L) \subset (C(K)\otimes C(L))^{p+k}$ by

$$
  \mu_{K,L} : a\otimes b \mapsto (d_{p+1})^p a) \otimes 
   ((d_0)^q b) =: a \smile b
  \,.
$$

=--


+-- {: .un_remark }
###### Remark

The iterated application of cosimplicial face maps on the right is to be thought of as producing a $(p+q)$-cosimplex in  $C(K \otimes L)^{p+q} = K^{p+q}\otimes L^{p+q}$ by 
evaluating the $p$-cosimplex $a$ on "leftmost" simplicial $p$-faces 
and the $q$-simplex $b$ on "rightmost" simplicial $q$-faces and then 
tensoring the resulting group elements.

=--


+-- {: .un_prop }
###### Proposition

The $\mu_{K,L}$ defined this is indeed a cochain map.

=--

+-- {: .proof}
###### Proof

We have to check that $\mu$ respect the coboundary maps in that for all $a,b$ as above we have

$$
  d \circ \mu (a \otimes b) = \mu \circ d (a \otimes b)
  \,.
$$

By definition of the cup product and the differential on the 
Moore cochain complex we have
$$
  \begin{aligned}
    d \circ \mu (a \otimes b)
    &=
    d (a \smile b) 
    \\
    &= d ( ((d_{p+1})^q a) \otimes ((d_0)^p b) )
    \\
    &=
    \sum_{i=0}^{p+q+1}
    (-1)^i  d_i((d_{p+1})^q a) \otimes ((d_0)^p b)     
  \end{aligned}
$$

By definition the face maps on the tensor product $K \otimes L$
are just the tensor products of the face maps of $K$ and $L$, so that this is

$$  
    \cdots
    =
    \sum_{i=0}^{p+q+1}
    (-1)^i  (d_i (d_{p+1})^q a) \otimes (d_i (d_0)^p b) 
    \,.
$$

Break up this sum in three parts

$$
    \cdots 
    =
    \sum_{i=0}^{p}
    (-1)^i  (d_i (d_{p+1})^q a) \otimes (d_i (d_0)^p b)     
    +
    (-1)^{p+1}  (d_{p+1} (d_{p+1})^q a) \otimes (d_{p+1} (d_0)^p b)     
    +
    \sum_{i=p+2}^{p+q+1}
    (-1)^i  (d_i (d_{p+1})^q a) \otimes (d_i (d_0)^p b)     
$$

Now repeatedly use the [[simplicial identities]] for face maps

$$
   (i \lt j) \;\;\Rightarrow \;\; d_i \circ d_j = d_j \circ d_{i-1}
$$

to pass face maps from the left to the right. This yields

$$
    \cdots 
    =
    \sum_{i=0}^{p}
    (-1)^i  ( (d_{p+2})^q d_i a) \otimes ( (d_0)^{p+1} b)     
    +
    (-1)^{p+1}  ((d_{p+1})^{q+1} a) \otimes ((d_0)^p d_1 b)     
    +
    \sum_{i=p+2}^{p+q+1}
    (-1)^i  ((d_{p+1})^{q+1} a) \otimes ((d_0)^p d_{i-p}b)         
    \,.
$$
Observe that the second term may now be naturally included in the
sum in the third term, leaving two sums

$$
  \cdots =
    \sum_{i=0}^{p}
    (-1)^i  ( (d_{p+2})^q d_i a) \otimes ( (d_0)^{p+1} b)     
    +
    \sum_{i=p+1}^{p+q+1}
    (-1)^i  ((d_{p+1})^{q+1} a) \otimes ((d_0)^p d_{i-p}b)             
    \,.
$$

Reduce the summation index on the second sum by $p$ to obtain

$$
  \cdots =
    \sum_{i=0}^{p}
    (-1)^i  ( (d_{p+2})^q d_i a) \otimes ( (d_0)^{p+1} b)     
    +
    (-1)^p
    \sum_{i=1}^{q+1}
    (-1)^i  ((d_{p+1})^{q+1} a) \otimes ((d_0)^p d_{i}b)             
    \,.
$$

Each sum seperately is now almost the alternating sum expression of an application
of the Moore complex coboundary map, except for one missing term in each sum.
But the two missing terms are equal and of opposite sign, so we can add them in

$$
 \begin{aligned}
  \cdots 
  =&
    \sum_{i=0}^{p}
    (-1)^i  ( (d_{p+2})^q d_i a) \otimes ( (d_0)^{p+1} b)     
    +
    (-1)^{p+1}  ( (d_{p+2})^q d_{p+1} a) \otimes ( (d_0)^{p+1} b)     
    \\
    &
    +
    (-1)^{p}  ( (d_{p+2})^q d_{p+1} a) \otimes ( (d_0)^{p+1} b)     
    +
    (-1)^p
    \sum_{i=1}^{q+1}
    (-1)^i  ((d_{p+1})^{q+1} a) \otimes ((d_0)^p d_{i}b)             
  \end{aligned}
  \,.
$$

One last application of the simplicial identities in the third tirm shows that
indeed this is the missing term in the sum in the fourth term. 
Comparing the result with the definition of coboundary map and cup product
we find finally

$$
  \begin{aligned}
    \cdots &= (d a) \smile b + (-1)^p a \smile (d b) 
    \\
    &=
    \mu \circ d (a \otimes b)
   \end{aligned}
    \,.
$$

=--

+-- {: .un_prop}
###### Proposition

This $\mu$ is indeed natural in $K,L$. For every $f : K \to K'$ and $g : L\to L'$ we have

$$
  \array{
    C(K) \otimes C(L) &\stackrel{\mu_{K,L}}{\to}& C(K \otimes L)
    \\
    \;\;\;\downarrow^{C(f)\otimes C(g)} && \;\;\;\downarrow^{C(f \otimes g)}
    \\
    C(K') \otimes C(L') &\stackrel{\mu_{K',L'}}{\to}& C(K' \otimes L')    
  }
$$

=--

+-- {: .proof}
###### Proof


This is immediate from the fact that the morphisms $f, g$ of cosimplicial objects respect the face maps.

=--


+-- {: .un_prop}
###### Proposition

The natural transformation $\mu$ is indeed a lax monoidal transformation
in that it is associative and unital in the required sense.

=--


+-- {: .proof}
###### Proof

We need to show that for all $J,K,L \in CoS(A)$ we have

$$
 \array{
  C(J) \otimes C(K) \otimes C(L) &\stackrel{Id_{C(J)} \otimes \mu_{K,L}}{\to}&
  C(J)\otimes C(K \otimes L)
  \\
  \downarrow && \downarrow
  \\
  C(J \otimes K) \otimes C(L)
  &\stackrel{\mu_{J,K} \otimes Id_{C(L)}}{\to}&
  C(J\otimes K \otimes L)
 }
  \,.
$$

it is sufficient to check this on all homogeneous elements
$a \otimes b \otimes c \in C^o(J)\otimes C^p(K) \otimes C^q(L)$.
There it is straightforward to check by using simplicial identities.

=--

+-- {: .un_remark }
###### Remark


The above statement is obvious when one observes the geometric  interpretation of the above remark: the image of $a \otimes b \otimes c$
along both ways around the above square is the $o+p+q$-dimensional
cosimplex that is obtained by evaluating $a$ on the leftmost $o$-face,
$p$ on the middle $p$-face and $q$ on the rightmost $q$-face and then
tensoring the resulting group elements.

=--



+-- {: .un_cor }
###### Corollary

The Moore cochain complex functor 

$$
  C : CoS(Ab) \to Ch_+^\bullet(Ab)
$$

can be equipped with a lax monoidal 
structure with respect to the standard monoidal structure on cosimplicial abelian groups and on connective cochain complexes of abelian groups.

=--


### $E_\infty$-cup product on cochains on simplicial sets {#EooCup}

At least for those [[cosimplicial algebra]]s $A$ that are algebras of [[cochains on simplicial sets]] $S^\bullet \in SSet$, i.e. $A = C(S^\bullet, R)$ it is known that the Moore complex [[dg-algebra]] $N^\bullet(A)$ equipped with the [[cup product]] is an [[E-k-operad|E-∞]]-[[algebra over an operad|algebra]]. See [[cochains on simplicial sets]] for details on this.


## References ##

On top of the references already listed, here are some more.

The Alexander--Whitney/Eilenberg--Zilber equivalences for the normalized chains functor are a special case of the strong [[deformation retract]] of chain complexes that was constructed 

* [[Samuel Eilenberg]], [[Saunders MacLane]], _On the groups $H(\pi, n)$. II_  Annals of Mathematics (1954 ) 

For any commutative ring $R$, they defined chain equivalences between the tensor product of the normalized chains on two simplicial R-modules and the normalized chains on their levelwise tensor product.

See also the appendix in

* Pavol &#352;evera, Thomas Willwacher, _Equivalence of formalities of the little discs operad_, [arXiv:0905.1789](http://arxiv.org/abs/0905.1789)


[[!redirects monoidal Dold?Kan correspondence]]
[[!redirects monoidal Dold--Kan correspondence]]
[[!redirects monoidal Dold-kan correspondence]]