Here are notes by [[Urs Schreiber]] for Thursday, June 11, from [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Oberwolfach]].


## Henriques: Invertible conformal nets ##

Andr&#233; Henriques has notes on this work available on [his website](http://www.math.uu.nl/people/henrique/);

* Chris Douglas, Andr&#233; Henriques, Michael Hill, _Geometric String structures -- notes on $\mathbb{Z}_2$-graded conformal nets_ ([ps](http://www.math.uu.nl/people/henrique/TringWP.ps))

today: classification of invertible objects in a 3-category

**theorem** (Andr&#233; Henriques, Arthur Bartels, Chris Douglas):
_Conformal nets form the objects of a symmetric monoidal 
3-category CN3_ .

* there is something about this written up to be found on Henriques' webpage.


**definition** A conformal net is a [[factorization algebra]] on the
category of 1-dimensional balls with values in
von Neumann algebras.

* 1-dim ball is just an interval, of course

* so a conformal net associates to each interval a vN algebra, and for each 
inclusion of intervals there is an inclusion of vN algebras

for $I, J$ two intervals equipped with an embedding into interval $K$
the net assigns

$$
  A : (J,K \subset I) \mapsto (A(J) \otimes A(K) \to A(I))
$$

>Freed: why do you call this conformal ?

> Andr&#233;: (as far as I understand the reply he gives after my question) the usual covariance condition under Moebius group imposed on conformal nets is taken care of here by havin not intervals in the
real line on the line but abstract intervals with maps between them being  embeddings. The claim is that this automatically implies the right kind of covariance that is otherwise imposed by hand.


**claim**

$$
  \{unitary full CFTs\} \simeq \{conformal nets\}
$$

>question: do you really mean _full_ instead of _chiral_ CFTs on the right?

>answer: yes

symmetric monoidal structure is objectwise the tensor product

**theorem** aa conformal net $A$ is invertible  in CN3 iff its
$\mu$-index $\mu(A)$ equals 1.

It is fully dualizable iff $\mu(A) \lt \infty$

in general $\mu(A) \in \{0\} \cup [1, \infty]$

### von Neumann algebras ###

in the 2-category of vN algebras, a morphism

$$
  A \to B
$$

is a bimodule ${}_A H_B$ where $H$ is a Hilbert space 

the unit
$$
   Id_A : A \to A
$$

is given by the bimodule called $L^2(A)$

this comes from the following: if $X$ is a measure space and $A$ arises as 
$L^\infty(X)$ then $L^2(A)$ is $L^2(X)$.

the general $L^2(A)$ is a non-commutative analog of this construction, for
$A$ which are not of the form "measurable functions on a measure space".

One word about composition, if 
$$
  A \stackrel{H}{\to} B  \stackrel{K}{\to} C
$$

given by $H \otimes_{Connes} K$ is the Connes-Fusion operation

associated to ${}_A H_B$ is

$$
  dim({}_A H_B) \in \{0\} \cup [1,\infty]
$$

$$
  dim = \left\{
    \array{
      0 & iff H=0
      \\
      1 & iff H is invertible
      \\
      \lt \infty & iff H has a dual
    }
  \right.
$$

**fact** think of an interval $I$ as the upper semicircle.
The two actions of $A(I)$ on 
$H_0 = L^2(A(I))$ can be used to define an
action of $A(J)$ on $H_0$ for every $J \usbset S^1$.

Because if $J$ is in the upper semicircle, use the left action,
if in the lowwer semicircle use the right action, if it is neither,
do something else (not explained here)

so $H_0$ has an action of $A(S^1)$.

so now everything is invariant projectively 
with respect to diffeomorphism group

**definition** 

given two circles $S_a, S_b$, let $nw(S_a)$ be north west quarter cicle, etc

consider $H_0$ as a bimodule over

$$
  A(sw(S_a)) \otimes A(ne(S_a))
$$

and

$$
  A(nw(S_b)) \otimes A(se(S_b))
$$


claim: $\mu(A) = dim(H_0)$


now some ideas on the proof of the first theorem

define always 

$$
  \bar A(I) = A(I)^{op} = A(\bar I)
$$

* if $A$ is dualizable, then $\bar A$ is its dual

* if $A$ is invertible, then $\bar A$ is its inverse

a 1-morphism in CN3, to be called a _defect_ is

consider the category of 
bi-colored 1-dimensional manifold is a 1-d manifolds 
(decomposition into intervals labeled by two things)
with morphisms being color-preserving maps

sufficient to look at intervals

* completely blue

* half blue, half orange

* completely orange

now a defect/1-morphism is a conformal net as above on bi-colored 1d manifolds

so suppose three nets and two defects

$$
  A \stackrel{D}{\to} B \stackrel{E}{\to} C
$$

then define the composition defect net by

$$
  D \otimes E ( blue-interval glued to yellow interval)
  =
  insert orange interval in the middle and average over all local evaluations
$$

the diffeomorphism group of the orange interval does act on the space
of all possible compositions here, which one shows to all be coherently isomorphic

now construct a defect

$$
 D:  A \otimes \bar A \to 1
$$
 by setting 
 
$$
  D(interval)
  := A(bent-around interval)
$$

(whatever that means)



## Henriques: informal evening session ##

things we could talk aout:

* composition of defects

* examples of conformal nets

* $\mathbb{Z}_2$-graded version of all that

>Mike Hopkins: could we talk about relation full CFT to chiral CFT?

### examples for conformal nets ###

* from the standard chiral positive energy nets that are usually
called "conformal nets" in the literature we get the more
general considered here by tensoring two chiral bits ("left" and "right")
and choosing an extension 

examples can be obtained as follows

* loop group nets ($S^1 \to \tilde {L G} \to L G$)

* integral lattice

  * moonshine net: take the Leech lattice and do some orbifolding
  
    * its full automorphism group is isomorphic to the Monster

* free fermion

* minimal model = Virasoro 


general remarks:

* recall the Hillber space $H_0$ obtained from the full cnformal net as the
algebra of the upper semi circle

* but in practice one first constructs $H_0$ and then from that the net

* a functor 
  $$
    \left\{
      subintervals of S^1,
      diffeos between them
    \right\}
    \to V N
  $$
  is already the same as a functor on all abstract 
  intervals, since that category
  is equivalent to intervals in the circle

so given an interval $I$, construc the set of maps

$$
  I \mapsto Maps((I, \partial I), (G, \{e\}))
$$

if $I$ happens to be thought of as embedded in the circle, then
this group could be identified with the subgroup of the loop group
whose elements send the complement of $I$ to $e$.

but the point is there is way to get a conformal net here without assuming
embedding into $S^1$

so the algebra we will assign to $I$ is just the group algebra

$$
  I \mapsto \mathcal{C}(Maps((I, \partial I), (G, \{e\}))]
$$

forgetting all topology, but this still depends on the central extension
and it sits densely in the vN algebra obtained by taking the group,
letting it act on the vacuum in the Hilbert space $H_0$ through a rep of
$\tilde {L G}$

so $A(I)$ is now defined to be the completion of that algebra in $B(H_0)$

this here gives a chiral theory


>audience: one should think of intervals here as thickened points and of the vN algebras as what is assigned to the point in an extended CFT



### algebra assigned to the circle ###

here is how to get the algebra assigned to the circle:

puff up the circle to an annulus, cut this vertically in two pieces;
call the two intervals where the cut goes $I$ and $J$,

let $H_0$ be the Hilbert space assigned to the boundary circles of the
two pieces of the cut annulus. Then the algebra in question is the 
Connes fusion product of $H_0$ with itself over $A(I) \otimes A(J)$

$$
  A(circle) := H_0 \otimes^{Connes}_{A(I) \otimes A(J)} H_0
$$

>audience: so the circle doesn't really appear in this formula, it's just a thing to help us think about this

>answer: yes

now recall the definition of tensor product of nets

$$
  \left(
    A \otimes A^{op}
  \right)(I)
  :=
  A(I) \otimes A(I)^{op}
$$

then consider extensions $B$ of nets of the following form 

$$
  A \otimes A^{op} \hookrightarrow B
$$

such is cooked up from every Frobenius algebra object $Q$ in $Rep(A \otimes A^{op})$
(in vN theorists jargon this is a "$Q$-system")

in the 3-category VN3 this $Rep(A)$ can be written as

$$
  Rep(A) 
  =
  End_{VN3}(Id_A)
  =
  \left\{
    \array{
        & \nearrow \searrow
       \\
       A &\Downarrow^{\rho}& A
       \\
       & \searrow \nearrow
    }
  \right\}
$$

to the circle $B$ assigns $Q$



##Schreiber##

detailed notes with further links and backgeound information are here:

* [[schreiber:Background fields in twisted differential nonabelian cohomology]]

The point of this is to define a notion of twisted differential nonabelian cohomology for every fibration sequence of smooth $\infty$-groupoids and then establish from that the following list of examples.

We now 

* list fibration sequence of smooth $\infty$-groupoids 

* and indicate properties of the corresponding differential twisted nonabelian cohomology

**Examples / Claim**

* fibration sequence: $\mathbf{B}U(n) \to \mathbf{B} PU(n) \to \mathbf{B}^2 U(1)$

  * twisting cocycle: lifting gerbe;

  * twisted cocycle: twisted bundles / gerbe modules

  * twisted Bianchi identity: $d F_\nabla = H_3$

  * occurence: Freed-Witten anomaly cancellation on [[nLab:brane|D-brane]]

* fibration sequence: $\mathbf{B}String(n) \to \mathbf{B} Spin(n) \stackrel{\frac{1}{2}p_1}{\to} \mathbf{B}^3 U(1)$

  * twisting cocycle: Chern-Simons 2-gerbe;

  * twisted cocycle: twisted nonabelian String-gerbe with conection

  * twisted Bianchi identity: 
    $d H_3 \propto \langle F_\nabla \wedge F_\nabla \rangle$

  * occurence: [[nLab:Green-Schwarz mechanism|Green-Schwarz anomaly cancellation]]

  * Proof. 
  
    * (with Danny Stevenson and Christoph Wockel: ([SSSS](http://www.math.uni-hamburg.de/home/schreiber/nactwist.pdf))) use BCSS model ([BCSS](http://arxiv.org/abs/math/0504123)) of $String(n)$ with [Brylinski-McLaughlin construction](http://golem.ph.utexas.edu/category/2008/02/construction_of_cocycles_for_c.html) of $\frac{1}{2}p_1$ 

    * (using ([SaScSt I](http://arxiv.org/abs/0801.3480), [SaScSt III](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf)):) compute local differential form data after differentiating smooth $\infty$-groupoids to  [[nLab:Lie infinity-algebroid|L-infinity algebroids]] using the formalism of ([SaScSt I](http://arxiv.org/abs/0801.3480))

  * for aspects of the twisted case see also

    * [AsJu](http://arxiv.org/abs/hep-th/0409200)

    * for aspects of the untwisted case see also ([Wa](http://arxiv.org/abs/0906.0117))

* fibration sequence: $\mathbf{B}Fivebrane(n) \to \mathbf{B} String(n) \stackrel{\frac{1}{6}p_2}{\to} \mathbf{B}^7 U(1)$

  * twisting cocycle: Chern-Simons 6-gerbe;

  * twisted cocycle: twisted nonabelian Fivebrane-gerbe with connection

  * occurence: dual [[nLab:Green-Schwarz mechanism|Green-Schwarz anomaly cancellation]] for NS 5-brane magnetic dual to string

  * ([SaScSt II](http://arxiv.org/abs/0805.0564) [SaScSt III](http://www.math.uni-hamburg.de/home/schreiber/5twist.pdf))
  

* fibration sequence: $\mathbf{B}^2 U(1) \to \mathbf{B} (U(1) \to \mathbb{Z}_2) \stackrel{}{\to} \mathbf{B} \mathbb{Z}_2$

  * twisting cocycle: $\mathbb{Z}_2$-orbifold;

  * twisted cocycle: [[nLab:orientifold|orientifold gerbe]] / Jandl gerbe with connection

  * occurence: unoriented string

  * unwrap the above abstract nonsense and use the above results to find [SchrSchwWal](http://arxiv.org/abs/hep-th/0512283) and the bosonic part of [DiFrMo](http://arxiv.org/abs/0906.0795)

***

[[Oberwolfach Workshop, June 2009 -- Wednesday, June 10|Previous day]] --- [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Main workshop page]] --- [[Oberwolfach Workshop, June 2009 -- Friday, June 12|Next day]]