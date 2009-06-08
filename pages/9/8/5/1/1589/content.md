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
* Ingo Runkel, Monday morning 11.15. CFT and algebra in braided tensor categories II. [[talk2.pdf:file]]


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
  tft_C : cobord_{3,2}^C \to vect_f(\magthcal{C})
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
