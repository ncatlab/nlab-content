This entry collects material on the Oberwolfach workshop

* Title:      Strings, Fields and Topology

* Organisers: 
  * Dennis Sullivan, New York
  * Stephan Stolz, Notre Dame
   * Peter Teichner, Berkeley

* Date:       June 7th - June 13th, 2009

* ID:         0924

Here are some scanned notes of talks from Bruce (not always complete!):

* Christoph Schweigert, Monday morning 9.15. CFT and algebra in braided tensor categories I. [[talk1.pdf:file]]


#Monday, June 8#

## Schweigert: CFT and algebra in braided tensor categories, I##

### 1. Modular tensor categories and rational CFT ###

#### 1.1 ####

* consider a _rational semisimple conformal vertex algebra_ $V$ 

* $\to$ from this we get a representation category $C$, which is a 
  [[braided monoidal category]]

  * that $V$ is semisimple and rarional makes $C$ in fact a [[modular tensor category]]

* $\to$ this gives rise to conformal blocks

**Definition: modular tensor category**

* abelian, $\mathbb{C}$-linear, semi-simple tensor category

* the tensor unit is a simple object, $I$ 
  a finite set of representatives of isomorphism classes of simple objects

* ribbon category, in particular objects have duals

* a non-degeneracy condition on the braiding given by an isomorphism of algebras
  $$
    K(C) \otimes_{\mathbb{Z}} \stackrel{\simeq}{\to} End(Id_C)
  $$
  where
  $$
    [U] \mapsto \alpha_U
  $$
  where the transformation $\alpha_U$ is given on the simple object $V$ by
  $$
    \alpha_U(V) = straight V-line encircled by U-loop
  $$
  (on the right we use string diagram notation)


#### 1.2 ####

**Fact (Reshitikhin-Turaev)** for any modula tensor category
$C$ there is a monoidal functor
$$
  tft_C : cobord_{3,2}^C \to vect_f(\mathcal{C})
$$ 

* 1) factorization homomorphism: given a surface $\Sigma_{U,U^*}$ with two marked points labeled by $U$ and $U^*$ consider the 3d cobordism from $\Sigma$ to the result of gluing a handle
to $\Sigma$ that connects the two marked points with a $U$-line running inside the handle.
the corresponding linear map given by the tft
$$
 fact_U := tft_C(\Sigma_{U,U^*} \to \Sigma)
$$
we have 
* $$
   \oplus_{i \in I} fact_{U_i} 
   : 
   \oplus_{i \in I} tft_C(\Sigma_{U,U^*})
   \stackrel{\simeq}{\to}
   tft_C(X)
  $$

* a representation of the mapping class group $Map(\Sigma)$ on $tft_C(X)$


### 2. CFT correlator ###

#### 2.1 ####


* $X$ a 2-dimensional conformal manifold, either oriented or unoriented
without boundary

* for the purpose of this talk restrict to the oriented case (but unoriented
case has been dealt with, too)

* also, from now on $X$ regarded just as a topological surface, no longer a
conformal one

#### 2.2 ####


strategy

* decorate $X$

* appropriate spaces of "functions" for correlators

**holomorphic factorization**

* pass from $X$ to its $\mathbb{Z}_2$ _orientation bundle_ $\hat X$,
the _orientation double cover_ (identifying points on the boundary, though) 
(an orientation twisted version of what is called the __double__ )

* double accounts for what physicists call left- and rightmoving
degrees of freedom

**goal**

* 1) find a decoration for $X$ such that $\hat X \in cobord_{3,2}^C$

* 2) specify the correlator $Cor(X) \in tft_C(\hatt X)$

  * a) $Cor(X)$ invariant under $Map(\hat X)^{\mathbb{Z}_2}$
    **modular invariance**
    
  * b) compatibility with factorization homomorphism (technical to state, dropped here)


#### 2.3 ####

**Insight.** decoration bicategory of special symmetric Frobenius algebras in $C$

* Frobenius algebra in $C$: an object
  $$
    (A \in Obj(C), \eta : 1 \to A,\epsilon : A \to 1,  
    m : A \otimes A \to A, \Delta : A \to A \otimes A)
  $$
  which is a unital associative algebra and counital coassociative coalgebra 
  in $C$ 

* being Frobenius means that the coproduct 
  $\Delta : A \to A \otimes A$ is a homomorphism of $A$-bimodules

* being _symmetric_ means that the two obvious nontriviall morphisms $A \to A^*$
  that one can build using unit and counit are equal

* being special means that $m \circ \Delta = Id_A$ and $\epsilon \circ \eta = dim(A) Id_1$


#### 2.4 ####

A typical worldsheet $X$: higher genus surface with defect lines and
marked points drawn on it

**decoration**

* to 2-dimensional cells assign special symmetric Frobenius algebras $A$;

* to 1-dimensional cells

  * to boundary lines a left or right module over the respective Frobenius algebra 
    (boundary is oriented);
  
  * to a defect line: a bimodule over the respective Frobenius algebras

* to 0-dimensional cells

  * to a junction of three defect lines labeled by three bimodules $D_i$, associate
    an element in $Hom_{A_1| A_3}(D_1 \otimes_{A_2} D_2, D_3)$
    
  * boundary field insertions: 
    for marked point on the boundary $x \in \partial X$ 
    attach a simple object $U \in Obj(C)$ to a marked point
    on a given defect line (or rather, on a junction of two defect lines) and an 
    element in $Hom_A(D_1 \otimes U, D_2)$

  * bulk field insertion: for $x$ not in the boundary but in the inside of $X$,
    consider the two preimages in $\hat X$, assign simple objects $U, V$ to these,
    respectively and assign an element in
    $$
      Hom_{A_1|A_2}(U \otimes A_1 \otimes V, A_2)
    $$

  * here the bimodule structure on these tensor products are given by over- and
    underbraiding, respectively (depending on orientation)


#### 2.5 ####

correlators from cobordisms

given $X$ consider the cobordism from the empty surface

$$
  \emptyset \stackrel{M_X}{\to} \hat X
$$
given by
$$
  M_X = (\hat X \times [-1,1])/_{\sigma t \sim -t}
$$
and set
$$
  Cor(X) = tft_C(M_X) 1  \in tft_C(\hat H)
$$

**Example** 

$X$ the disk with a defect line running across it from boundary to boundary.

then

* $\hat X$ is the sphere

* $M_X$ is the 3-ball

* $X$ sits inside the equatorial plane of $M_X$: one copy of $[-1,1]$ over each of
  its interior points connectint its two preimages in $\hat X$, in addtion one copy of 
  the interval connecting each boundary point to its unique preimage in $\hat X$


>long discussion with audience ensues: audience wants to better understand why
all these constructions are being undertaken. The answer is in the theorem to come:
every assignment of correlators as above (compatible with factorization morphism and
invariant in the above sense under mapping class group (preserving defect decoration))
is obtained by the recipe presented here


## Runkel: CFT and modular tensor categories, II##

* Ingo Runkel, Monday morning 11.15. CFT and algebra in braided tensor categories II; notes by [[Bruce Bartlett]]: [[talk2.pdf:file]]


## Freed ##

joint work with [[Jacques Distler]] and Greg Moore.

(on [[differential cohomology]] of background fields in type II [[string theory]])

* $\Sigma$ in this talk a compact 2-dimensional manifold: the _worldsheet_

  * (called $X$ in the morning talks)

* $X$ smooth 10-dimensional manifold: _spacetime_

* fields $\Sigma \stackrel{\phi}{\to} X$ (see [[sigma-model]] )

* 2-dimensional theory $\to$ 10-dimensional theory 

* more generally: $X$ is an [[orbifold]]

* today: a variation of this called _orientiold_ : $X_W \to X$ is a double cover

  * physicists think of $X_W$ as the spacetime equipped with an involution, 
    but really spacetime is the $\mathbb{Z}_2$-quotient $X$
    
* I) $\sigma \in \mathbb{Z}_2$ acts trivially : _type I string_

* II) section $X_W \stackrel{\leftarrow}{\to} X$ _type II string theory_

this project started when Jacques Distler showed Dan Freed a certain formula, namely

let 
$$
  i : F \hookrightarrow  X_w
$$
be the fixed point

* set 
  $$
    RR-charge = \pm 2^{something} i_*
    ( \sqrt{\frac{L'(F)}{L'(\nu)}} )
  $$
  where
  $$
    L' = \prod \frac{x/4 u}{tanh x/4u}
  $$
  where 
  * $u$ is the Bott generator of K-theory
  * $\nu$ is normal bundle of $F \hookrightarrow X_W$
  * with another factor this would be the Hrizebruch 
      L-function, this way it is not

what is it?

this led to thinking about the following
 
* 1) definition of fields/theory

* 2) derive RR-charge formula over $\mathbb{Z}[1/2]$ from $10 d$

* 3) anomaly cancellation in 2d

* there is paper on arXiv with a summary, but this is still work in progress  

diff geoemtric structures that one needs to make sense of this:

* differential cohomology

* twistings


### differential cohomology ###

suppose $h$ is any cohomology theory

then $h$ with rational coefficients $h(-; \mathbb{Q}) = H(-;h(pt, \mathbb{Q}))^\bullet$

here the coefficient object 

$$
  h_Q := h(pt;\mathbb{Q})
$$

on the right is a graded ring and the bulleted-degree is the
corresponding total degree of that and the cohomology degree


consider the [[homotopy limit]] which gives [[differential cohomology]]

$$
  \array{
    h^{v \bullet} &\to& \Omega(M, h_{\mathbb{R}})_{closed}
    \\
    \downarrow && \downarrow
    \\
    h^\bullet(M) &\to& H(M; h_{\mathbb{R}})
  }
$$

>question from Mike Hopkins: are there choices in the bottom horizontal map; doesn't one 
have to choose a basis of cocycles?
  
we get from this two exact sequences

$$
  0 \to h(M;h_{\mathbb{R}} \otimes \mathbb{R}/\mathbb{Z})^{q-1}
  \stackrel{curv}{\to}\Omega(M;h_{\mathbb{R}})^q_{\mathbb{Z}} \to 0
$$  

$$
  0 \to forms \to h^{v \bullet}(M) \to h^q(M) \to 0
$$

* this was introduced for ordinary cohomology by Cheeger and Simons and generalized by
Hopkins and Singer

* we can think of the cohomology group as components of some space
  $$
    h^q(M) = \pi_0(Map(M, h_q))
  $$
  and
  $$
    h^{v q}(M) = \pi_0(--)
  $$
  
* various people constructed various models for this, such as Bunke and Schick;
  by Gomi for equivariant cohomology, also Szabo and Alessandro
  
**examples**

$$
    H^{v 1}(M) = Map(M, \mathbb{T})
$$
  
$$
    H^{1}(M) = \pi_0 Map(M, \mathbb{T})
$$

$$
    H^{v 2}(M) = \{line bundles with connection\}
$$

$$
    H^{v 3}(M) = \{line bundle gerbes with connection\}
$$

**remarks**

* the application to string theory here will have completely topological flavor

* defining certain terms in an action like Wess-Zumino-Witten  term and chern-Simons term, these are nicely understood in terms of differential cohomology: observation goes back to Gawedzki

* in physics the forms are "currents" which say where charges are located, the class in real cohomology is the total charge

* in quantum physics this total charge has to be quantized (sit on a lattice inside the real cohomology)

* so the above pullback diagram says that classical charges are to be combined with quantization condition in order to give physical fields



### twistings of $KR(X_w)$ ###

so consider again $\pi : X_w \to X$ a double cover

* an object in $KR^0(X_W)$ is represented by 

  * a $\mathbb{Z}_2$-graded complex
vector bundle $E \to X_W$ (in terms of pseudobundles: even part minus odd part)

  * $\tilde \sigma : \sigma^* \bar E \to E$

recall that $\sigma$ may have fixedpoints

special cases

* $\sigma$ acts trivially: we get just $KO^0(X_w)$-theory

* $X_w \to X$ has a section: $K^0(X)$ 

**twisting**

pass to a locally equivalent groupoid

$$
  Y_W \to Y 
$$

$$
  Y : (Y_0  \stackrel{\leftarrow}{\leftarrow} Y_1 \stackrel{\stackrel{\leftarrow}{\leftarrow}}{\leftarrow}
 \cdots)
$$

notation: $V^\phi = $ $V$ if $\phi = 0$ and $\bar V$ otherwise

**definition**

a twsiting of $KR(X_W)$ is an equivalent thing $Y_w \to Y$ as above

where 

$$
  d : Y_0 \to \mathbb{Z}
$$
continuous

$$
  L \to Y_1
$$
hermitian line bundle, $\mathbb{Z}_2$-graded

$$
  \theta: L_g^{\phi(f)} \otimes L_f \to L_{g f}
$$

cocycle condition for $\theta$


recognize these twistings as classified by some cohomology theory

**cohomology group**

For $K(X)$:  $\pi_{\{0,1,2,3\}h \simeq \{\mathbb{Z}, \mathbb{Z}_2, 0 , \mathbb{Z}\}$

for some $h$ that we are not being told about

For $KO(X_W)$: $\pi_{\{0,1,2\}} k_{0 \lt 0..2\gt} \simeq \{\mathbb{Z},  \mathbb{Z}_2, \mathbb{Z}_2\}$

for $KR(X_W)$ the iso classes are

$$
  H^0(X, \mathbb{Z}) \times H^1(X; \mathbb{Z}) \times
   H^{w+3}(X, \mathbb{Z})
$$ 

as a set

$$
  u \in K^2(pt) \in KR^{\tau_1 +2}(pt)
$$

>speaker is running out of time, coherence is being lost a bit... notetaker misses to take notes on some central statement on these twisted cohomology classes, but see the arXiv article


### string backgrounds ###

the differential cocycles are background data for the 2-d theory and 
field data for the 10 d theory (see [[sigma-model]])

**def** an NS-NS superstring background is

* i) a smooth 10d orbifold with metruc and real function (dilaton field)

* ii) $\pi : X_W \to X$ orientifold double cover

* iii) $\beta^v$ a differential twisting of $KR(X_w)$: the $B$-field

* iv) K : $R(\beta) \to \tau^{KO}(T X -2)$ iso of twistings of $KO(X)$: twisted Spin-structure

Bott shift, leading to equivalent theories $\beta^v \to \beta^v + (\tau^v + 2)$

and something else

Stiefel-Whitney classes
$$
  w_1(X) = t w
$$
$$
  w_2(X) =  t w^2 + a w 
$$

aim: mix iii) and iv)

2d theory: A worldsheet  $\Sigma$ with metric,
a spin structure on $\hat \Sigma$: the orientation double cover



$$
  \array{
     \hat \Sigma &\to& X_w
     \\
     \downarrow && \downarrow
    \\
    \Sigma &\to& X
  }
$$

$$
  \phi^* w \simeq \hat w
$$

and spme spinor fields on $\hat \Sigma$

in the [[path integral]]: integrate over all of these pieces of data

$\to$ effective action Pfaffian of Dirac operator 

$$
  Pfaff  D_{\hat \Sigma}(\phi^*T X - 2)
  \cdot
    exp 2 \pi i \int_{\Sigma/S} \phi^* \beta^v
$$

Pfaffian bit is section of a Pfaffian line bundle over $S$

where?


work over some parameter space $S$

both factors above are sections of a line bundle over $S$

**theorem** (in preparation) there is a hopefully canonical
trivialization of $L_\Psi \otimes L_B \to S$

action being section of bundle instead of function: annomaly: 

sources

* 1) integrals over fermions $L_\Psi$: spin structure need not be equivariant under $\mathbb{Z}_2$-action

* 2) simultaneous electric and magnetic current or alternatively self-dual current

interply between 1 and 2 leads to anomaly cancellation

* 3) boundary of topological terms, like WZW, Chern-Simons

what about $L_B$: exotic orientation



## Kevin Costello;  part I ##


### deformation quantization ###

* classical mechanics: $A^{cl}$ commutative algebra with 
Poisson brackets $\{-,-\}$

* this is the classical observable algebra

* to quantize this we need to find some associative algebra
  $A^q$ over the ring $\mathbb{R}[[\hbar]]$

* such that 

  * 1) $A^q/\hbar A^q = A^cl$ 

  * 2) if $a,b \in A^c{l}$, $\tilde a, \tilde b$ are lifts in $A^q$ then
    $$
      \{a,b\} = \frac{1}{\hbar} [\tilde a, \tilde b] mod \hbar
    $$
    
**goal** of these lectures: want to give an analog of ths picture for QFT

* 1) need to explain wha plays the role of commutative, Poisson and 
  associative algebras
  
* 2) explain how classical field theory is encoded in commutative and Poisson

* 3) explain how to quantize

structure that play the role of associative algebras is a 
[[factorization algebra]] 

this is a $C^\infty$-analog (i.e. differential geometric analog) 
of a **chiral algebra** in the sense of
Beilinson and Drinfeld

* let $M$ be a manifold (on which we do QFT)

* Let $B(M) = \{smooth balls in M\}$; this is an $\infty$-dim manifold


>audience: would open balls here form a manifold? does it matter?
  >answer: well, really we don't think of manifolds but of [[diffeological space]]s, of course (sheaves on manifold)

* Let $B_n(M) = \{n disjoint smooth balls embedded in larger ball in M\}$

there are obvious projection maps

$$
  B(M) \stackrel{q}{\leftarrow} B_n(M) \stackrel{p}{\to} B(M)^n
$$

everything now joint work with O. Gwilliam


**def** A **factorization algebra** is

* a [[vector bundle]] $F$ on $B(M)$  

  * equipped with maps $p^*(F^{\times n}) \to q^*(F)$ 
  
    * satisfying some evident compatibility condition
    
    * such that everything is invariant under the obvious $S_n$-action on 
      $B_n(M)$ that exchanges the order of the balls
* concretely: 

  * $F$ assigns a vector space to every ball $B \subset M$
  
  * if we have some configuration of balls, like 2 balls $B_1, B_2$ inside a big one $B_3$
    we get a map $F(B_1)\otimes F(B_2) \to F(B_3)$
    
  * these must vary smoothly as the configuration of the balls varies
 

This is an algebra over the embedded little disk [[operad]], which is a 
"colored operad" (i.e. a [[multicategory]] with more than one object)

* where the colors are $B(M)$

* $n$-ary operations are $B_n(M)$ 

* with extra conditions such that the vector space we assign to each color forms a smooth vector bundle

  * and all operad maps are compatible with this

notice that it happenss that for given in and out colors, there is at least one
morphism in the operad.

* there are several different reductions of this structure that are more familiar

* notion of [[vector bundle]] comes in three natural flavors

  * 1) $C^\infty$
  
  * 2) holomorphic
  
  * 3) locally constant sheaves
  
* definition of factorization algebra can be modified to the case of 2) and 3)


**def** a locally constant factorization algebra is like a factorization algebra,
except that instead of being a vector bundle $F$ is a locally constant sheaf on $B(M)$
of co[[chain complex]]es
and the structure maps of locally constant sheaves

>question: cohomologically locally constant or really locally constant

  > answer: I think cohomologically locally constant
  
let $F$ be a locally constant factorization algebra in $\mathbb{R}^n$, then 
since $B(\mathbb{R}^n)$ is contractible $F$ is quasi-isomorphic to a
trivial sheaf with fiber $V$ a cochain complex

so then for instance the map $V__{B_1} \otimes V_{B_2}  \to V_{B_3}$
depends only on homotopies of the configuration,

so, a locally constant factorization algebra on $\mathbb{R}^n$ is an 
$E_n$-[[algebra over an operad|algebra]]

next specialization: **holomorphic factorization algebras**

Let $\Sigma$ be a Riemannian surface.

We know what it means for a map from a complex manifold to $B(M)$ to be
holomorphic; so we can talk about holomorphic algebras on $B(\Sigma)$

a homomorphic map $U \to B(M)$ is a bundle $M \to U$ all of whose fibers are balls
and a map
$$
  \array{
    M &\to& \Sigma
    \\
    \downarrow
    \\
    U
  }
$$

actually $B(M)$, too, is also not a complex manifold but a sheaf on complex manifold

>Andre Henriquez: but with this definition, won't every map $U \to B(M)$ be holomorphic:
  > answer: oops, right
  
??

let's consider a holomorphic factorization algebra on $\mathcal{C}$, which is
translation invariant and dilation invariant

let $V = F$ (any round disk)

if we have a configuratoin of disks with $B_1$ and $B_2$ in $B_3$ with radii
$\epsilon_i$ with one disk in the center of the big one and the other at
complex parameter $z$, the map
$$
  m_z : V \otimes V \to V
$$
must vary holomorphically with $z$

so $z \mapsto m_z$ is a holomorphic map $Annulus \to Hom(V \otimes V, V)$, so it has 
a Laurent expansion

$$
  m_z \sim \sum_{k \in \mathbb{Z}} Z^k a_k
$$

with $a_k$ in some completion of $Hom(V \otimes V , V)$

>question by Ulrich Bunke: algebraic tensor product or not?
  > answer: no, in examples tensor product will be projective tensor product
  
reminiscent of vertex operator algebra

notice that Beilinson-Drinfeld make the same def in the algebraic setting, in their
case the axioms are equivalent to that of a vertex operator algebra;

they show axioms for chiral algebra on $\mathcal{C}$ are essentially equivalent
to those of a vertex operator algebra


**claim**: structure of factorization algebra: good to encode quantum field theory

notice that factorizations algebras on real line tend to be associativ algebras,
so that fits in with the expectation from quantum mechanics.