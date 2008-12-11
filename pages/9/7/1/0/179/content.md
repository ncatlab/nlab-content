#Idea#

**$L_\infty$-algebroid**s or **Lie $\infty$-algebroid**s or are to [[Lie infinity-groupoid]]s as Lie algebras are to Lie groups. Hence $L_\infty$-algebroids are a [[horizontal categorification]] and [[vertical categorification]] of Lie algebras: they encompass [[L-infinity-algebra]]s as well as [[Lie algebroid]]s.

#Definition in terms of codifferential coalgebra#


A **Lie $\infty$-algebroid** is

* a smooth space $X \in$ [[Diff]];

* an $\mathbb{N}$-graded smooth vector bundle $E \to X$, not necessarily of finite rank;

  * the $C^\infty$-module of sections of $E$ is denoted in the following by $\mathfrak{g} := \Gamma(E)$;

* a coderivation $D$ (over $\mathbb{R}$) of degree -1 on the [[free graded co-commutative coalgebra]] $\vee^\bullet_{C^\infty(X)} \mathfrak{g}$ 

* such that

  * $D^2 = 0$.

Morphisms of Lie $\infty$-algebroids are morphisms of the underlying coalgebras which respect the differential. The resulting category of Lie $\infty$-algebroids we call $L_\infty Algebroids$.


#Definition in terms of differential algebra#

In the case that the vector bundle $E$ is of finite rank in each degree, so that the dual $\mathfrak{g}^*$ of the module $\mathfrak{g}$ over $C^\infty(X)$ exists, this definition is equivalent to the following:

+-- {: .un_defn}
###### Definition
**(quasi-free differential graded-commutative algebras)**

A _quasi-free differential graded commutative algebra_
(**qDGCA**) is 

* an algebra of smooth functions $A := C^\infty(X)$ on a smooth manifold $X$;

* a non-positively graded complex $g$ of finitely generated projective $A$-modules;

* together with a degree +1 graded derivation $d$ on the free (over $A$) graded-(anti-)commutative algebra
$
  \wedge^\bullet_{A} g^* = S^\bullet g^*[1]
$
on the dual (over $A$) of $g$;

* such that $d^2 = 0$.

A morphism of qDGCAs is a linear map of the underlying graded-(anti-)commuting algebras respecting the differential.
=--

Notice that the first few terms of $\wedge^\bullet g^*$ in degree 0, 1 and 2, respectively, are
$$
  \wedge^\bullet g^*
  =
  A \oplus g_0^*[1] \oplus  (g_0^*[1]\wedge g_0^*[1])
  \oplus g_{-1}^*[1] \oplus \cdots
  \,.
$$

**Example:** Take $g = \Gamma(T X)$ to be the $C^\infty(X)$-module of vector fields on $X$, then 
$\wedge^\bullet_{C^\infty(X)} g^* = \wedge^\bullet_{C^\infty(X)} \Omega^1(X) = \Omega^\bullet(X)$. 


**Remark:** There is plenty of room to fuss about the grading conventions. 

**Remark:** This is equivalent to the definition of the algebra of functions on an [[NQ-supermanifold]].


We write 

$$
  L_\infty Algebroids_{fin} \stackrel{CE(-)}{\to} qDGCAs
$$

for the corresponding contravariant functor 
which sends a finite rank Lie $\infty$-algebroid 
$(\vee^\bullet_{C^\infty(X)} \mathfrak{g}, D)$
to the corresponding dual qDGCA

$$
  CE(\mathfrak{g})
  :=
  (\wedge^\bullet_{C^\infty(X)} 
    \mathfrak{g}^*, d : \omega \mapsto -\omega(D(-))
  )
$$

and address the qDGCA $CE(g)$ as the (generalized) [[Chevalley–Eilenberg algebra]] of $g$.

**Remark** In the physics literature $CE(g)$ is called a 
[[Chevalley–Eilenberg algebra|BRST complex]].


##Special Cases##

* an $L_\infty$-algebroid over a point, $X = pt$ is an **$L_\infty$-[[L-infinity-algebra|algebra]]**;

* an $L_\infty$-algebroid with generators concentrated in the first $n$ degrees is a **Lie $n$-algebroid**;

* an $L_\infty$-algebroid the differential of whose CE-algebra is "co-binary", i.e. $d : \mathfrak{g}^* \to g^* \oplus g^* \wedge g^*$, is **strict**.

So in particular

* a Lie 1-algebroid is a **[[Lie algebroid]]**;

* a Lie 1-algebroid over the point is a **Lie algebra**;

* a Lie $n$-algebroid over a point is a 
**[[L-infinity-algebra|Lie n-algebra]]**.

#Further resources#

There should be an [[internalization]] of this into the context of [[generalized smooth spaces]] and [[generalized smooth algebras]]. This is discussed at [[schreiber:generalized smooth L-infinity algebroid]].

#References#

The term "Lie $\infty$-algebroid" or "$L_\infty$-algebroid" as such is not as yet established in the literature, as most authors working with these objects think of them entirely in terms of [[NQ-supermanifold]]s and either ignore the relation to [[Lie theory]] or take it more or less for granted. 

Possibly the first explicit appearance of the idea of $\infty$-Lie-algebroids recognized in their full [[Lie theory|Lie theoretic]] meaning is

* Pavol &#352;evera, _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv](http://arxiv.org/abs/math.SG/0105080))

which uses "[[NQ-supermanifold]]s". Of course, as this article also points out, in hindsight one finds that much of this is already implicit in the much older theory of [[Sullivan model]]s in [[rational homotopy theory]], which is concerned with modelling _spaces_ by qDGCAs. That these spaces can be regarded as [[infinity-groupoid]]s and as [[Lie-infinity-groupoid]]s in particular is clear in hindsight, but was possibly first explicitly realized in the above reference. See also [[Lie integration]].