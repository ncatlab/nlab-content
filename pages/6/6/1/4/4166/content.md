
> under construction

> for the time being this here are nothing but [references](#References) and rough notes taken in a talk long ago...


_BDR 2-vector bundles_ are a notion of [[categorified]] [[vector bundle]] motivated by the concept of [Kapranov-Voevodsy's 2-vector spaces](http://ncatlab.org/nlab/show/2-vector+space#KV2VectorSpace).

See also at _[[iterated algebraic K-theory]]_.

#Contents#
* table of contents
{:toc}


## 2-Vector bundles following Baas-Dundas-Rognes

We are looking for a generalization of the notion of [[vector bundle]] in 
[[higher category theory]].

Let $X$ be a [[topological space]] and $\{U_\alpha \to X\}_{\alpha \in A}$ an [[open cover]],
where the index set $A$ is assumed to be a [[poset]].

Defition. A **charted 2-vector bundle** (i.e. a [[cocycle]] for a BDR 2-vector bundle) 
of rank $n$ is

* for $\alpha \lt \beta \in A$ on $U_\alpha \cap U_\beta =: U_{\alpha\beta}$
  a matrix $(E^{\alpha\beta}_{i j})_{i,j = 1}^{n}$ of [[vector bundle]]s 
  $E^{\alpha \beta}_{i j} \to U_{\alpha \beta}$
  such that the determinant of the underlying matrix of dimensions
  is $det(dim(E^{\alpha \beta}_{i j})) = \pm 1$.
  
* on triple overlaps $U_{\alpha \beta \gamma}$
  for  $\alpha \lt \beta \lt \gamma \in A$ we have
  [[isomorphism]]s 
  
  $$
    \phi^{\alpha \beta \gamma}
    : 
    \oplus_{j} E^{\alpha \beta}_{i j} \otimes E^{\beta \gamma}_{j k}
      \stackrel{\simeq}{\to}
      E^{\alpha \gamma}_{i k}
  $$ 

* such that the $\phi$ satisfy  on quadruple overlaps the evident cocycle condition
  (as described at [[gerbe]] and [[principal 2-bundle]]).
  
Next we need to define morphisms of such charted 2-vector bundles. These involve the 
evident refinements of covers and fiberwise transformations.

Write $2Vect(X)$ for the equivalence classes of charted 2-vector bundles under these morphisms. 

**Remark** If we restrict attention to $n = 1$ then this gives the same as
$U(1)$-gerbes/[[bundle gerbe]]s.

**Theorem** (Baas-Dundas-Rognes)

There exists a [[classifying space]] $\mathcal{K}(V)$
such that  for $X$ a finite [[CW-complex]] there is an [[isomorphism]]

$$
  [X, \mathcal{K}(V)] = 
  {\lim_\to}_{a : Y \to X}
    Gr(2Vect(Y))
$$

between [[homotopy]] classes of continuous maps $X \to \mathcal{K}(V)$
and equivalence classes of the group completed [[infinity-stackification|stackification]] of
2-vector bundles,

where the [[colimit]] is over acyclic [[Serre fibration]]s (Note: these are not acyclic fibrations in the usual sense, rather their fibres have trivial integral [[homology]]) and $Gr(-)$ indicates
the [[Grothendieck group]] completion using the monoid structure arising from the direct sum of 2-vector bundles.

**Proof** In BDR, Segal Birthday Proceedings 

**Note** $2Vect_n(X) = [X, |B Gl_n (V)| ]$.

BDR called $\mathcal{K}(V)$ the **2-K-theory** of the [[bimonoidal category]]
of [[Kapranov-Voevodsky 2-vector space]]s.

## The homotopy type of the classifying space

**Theorem** (Baas-Dundas-Rognes-Richter)

The K-theory of BDR 2-vector bundles is the [[algebraic K-theory]] of [[ku]] (see at _[[iterated algebraic K-theory]]_)

$\mathcal{K}(V) \simeq K(ku)$

Here:

* $ku$ is the connected version of the [[spectrum]] of  complex [[topological K-theory]];

* $K(-)$ denotes forming the [[algebraic K-theory]] spectrum of [[ring spectrum|ring spectra]].

So by the general formula for [[algebraic K-theory]] for [[ring spectrum|ring spectra]], this is 

$$
 K(ku) \simeq \mathbb{Z} \times B Gl(ku)^+
 \,
$$

Some flavor of $\mathcal{K}(V)$.

* $V$ is the (a [[skeleton]] of the [[core]] of) of [[category]] of complex [[vector space]]s.

  * [[object]]s are [[natural number]]s, $n$ corresponding to $\mathbb{C}^n$;
  
  * [[morphism]]s are $Hom(k,k)  = GL(k)$ and there are no morphisms between different
    $k,l$.
    
This category $V$ is naturally a [[bimonoidal category]] under [[coproduct]] and 
[[tensor product]] of [[vector space]]s.

K-theory is about understanding linear algebra on a ring, so we want to understand the
linear algebra of this [[monoidal category]].

We write $Mat_n(V) $ for the $n \times n$ matrices of linear isomorphisms between 
finite dimensional vector spaces.

Such matrices can be multiplied using the usual formula for matrix products 
on the [[tensor product]] and [[direct sum]] of vector space and linear maps.

Write $Gl_n(V)$ for the subcollection of those matrices for which the 
determinant of their matrix of dimensions is $\pm 1$.

Now define

$$
  \mathcal{K}(V) = \Omega B (\coprod_{n \geq 0} B Gl_n (V))
  \,.
$$

Notice that this is a direct generalization of the corresponding formula
for the algebraic K-theory of a ring $R$,

$$
  K(R) = \Omega B (\coprod_{n \geq 0} B Gl_n(R))
  \,.
$$

## $K(ku)$ as a form of elliptic cohomology

Ausoni and Rognes compute the [[homology]] groups 
(for a certain sense of homology) of $K(ku)$.

take rational homotopy

* $H^*(-, \mathbb{Q})$

  for $p$ a [[prime]], multiplying by $p$ gives an isomorphism on this.

  p = $\nu_0$

* Let $KU^*(-)$ be complex oriented [[topological K-theory]], then

  $$
    KU_* = \mathbb{Z}[u^{\pm 1}]
  $$
  
  for $|u| = 2$ (the [[Bott class]]) we have that multiplying by $u$ is an 
  isomorphism and $u^{p-1} = \nu_1$
  
The $\nu_i$ come from the [[Brown-Peterson spectrum]] $B P$ and 
$\pi_* BP = \mathbb{Z}_{(p)}[\nu_1, \nu_2, \cdots]$
  
motto: the higher the $\nu_i$ the more you detect.

Christian Ausoni figured out something that implies that

"$K(ku)$ detects as much in the [[stable homotopy category]] as
any other form of [[elliptic cohomology]]."

## From gerbes to 2-vector bundles

It is hard to directly construct charted 2-vector bundles. We have more examples
of [[gerbe]]s. So we want to get one from the other.

**Example** 
We have 

$$
  \mathbb{S}^1 = \mathbb{C}P^1 \subset \mathbb{C}P^\infty = B U(1) = K(\mathbb{Z},2)
$$

(see [[Eilenberg-MacLane space]] and [[classifying space]])

$$
  \mathbb{S}^3 = \Sigma \mathbb{S}^2 \to \Sigma B U(1) \subset 
  \Sigma B U \to B B U_{\otimes}
  \subset units(ku)
  \to B GL(ku)
$$

using $\Sigma B U(1) \to B BU(1) \to B B U_{\otimes}$
we can take a $U(1)$-[[gerbe]] classified by maps into $B^2 U(1)$ and
induce from it the associated 2-vector bundle.

the canonical map

$$
  \mathbb{S}^3 \to K(\mathbb{Z},3)
$$

may be thought of as classifying the gerbe called the [[magnetic monopole]]-gerbe

Postcomposing with $\mu : K(\mathbb{Z},3) \to K(ku)$
we have

Fact: $\mu$ gives a generator in $\pi_3 K(\mathbb{Z},3) = H^3(\mathbb{S}^3)$

**Theorem** (Ausoni-Dundas-Rognes)

$$
  j(\mu) = 2 \zeta - \nu
$$

in $\pi_3(K(ku))$

so regarded as a 2-vector bundle $\mu$ is not a generator.

ADR: $\zeta$ is "half a monopole".

$$
  \pi_3(K(ku))  = \mathbb{Z} \oplus \mathbb{Z}/24 \mathbb{Z}
$$

(the first summand is $\zeta$, the second $\nu$).


Thomas Krogh has an [[orientation]] theory for 2-vector bundles which says that $j(\nu)$
is not orientable.


## 2K-theory of bimonoidal categories {#2K-theory}

Let $(R, \oplus, \otimes, 0,1, c_{\oplus})$
 be a [[bimonoidal category]], i.e. a [[categorification|categorified]] [[rig]].


This can be broken down as

1. $(R, \oplus, 0 , c_{\oplus})$ a permutative category, a categorified abelian [[monoid]];


1. $(R , \otimes, 1)$ is a  [[monoidal category]], assumed to be _strict_ monidal in the following;

1. a distributivity law.

**Examples**

1. $E = Core$[[FinSet]], 
   the [[core]] of the 
   category of finite sets and morphisms only between sets of the
   same cardinality.

   In the [[skeleton]], objects are [[natural number]]s $n \in \mathb{N}$,
   $\oplus$ and $\otimes$ is addition and multiplication on $\mathbb{N}$,
   respectively. Here $c_{\oplus}$ is the evident natural [[isomorphism]]
   between direct sums of finite sets.

1. $V = Core$[[Vect]] the [[core]]
   of the category of finite dim vector spaces, with morphisms only between
   those of the same dimension. 

1. ...

**Definition** For $R$ a bimonoidal category, write $Mat_n(R)$
for the $n \times n$ matrices with entries morphisms in $R$. Then matrix multiplication is defined using the bimonoidal structure on $R$. This gives a weak [[monoid]] structure.


Let $Gl_n(R)$ be the category of weakly invertible such matrices. This is the [[full subcategory]] of $Mat_n(R)$. We get a diagram of [[pullback]] squares

$$
  \array{
    Gl_n(R) &\hookrightarrow& Mat_n(R)
    \\
    \downarrow && \downarrow
    \\
    Gl_n(\pi_0(R))&\to& Mat_n(\pi_0(R))
    \\
    \downarrow && \downarrow
    \\
    Gl_n(Gr(\pi_0(R)))&\to& Mat_n(Gr(\pi_0(R)))
  }
  \,,
$$

where $Gr(-)$ denotes [[Grothendieck group]]-completion.

**Definition** (Baas-Dundas-Rognes, 2004)

For $R$ a [[bimonoidal category]], the **2K-theory** of $R$ is 

$$
  \mathcal{K}(R) :=  \Omega B \coprod_{n \geq 0} | B Gl_n(R) |
$$

where the $\Omega$ is forming [[loop space]], the leftmost $B$ is forming classifying space of a category and the inner $B$ is a flabby version of classifying space of a category.

This can also be written

$$
  \cdots \simeq \mathbb{Z} \times |B Gl_n(R)|^+
  \,.
$$

Here $B_q Gl_n(R)$ is a [[simplicial category]]

...


**Theorem** (Baas-Dundas-Rognes)

Let $R$ be a [[small category|small]] [[Top]]-[[enriched category|enriched]] [[bimonoidal category]]
 such that 

1. $R$ is a [[groupoid]];

1. for all $X \in R$ we have that $X \oplus (-)$ is [[faithful functor|faithful]].

Then $\mathcal{K}(R) \simeq K(H R)$ is the ordinary [[algebraic K-theory]] of the [[ring spectrum]] $H R$.

Notice that for $H R$ to be a spectrum we only need the additive structure $(R, \oplus, 0, c_{\oplus})$.  The point is that the other monoidal structure $\otimes$ indeed makes this a [[ring spectrum]]. This is a not completely trivial statement due to a bunch of people, involving [[Peter May]] and Elmendorf-Mandell (2006).

**Examples**

1. For the category $R := E = Core(FinSet)$ 
   of finite sets as above we have that $H E$ is 
   the [[sphere spectrum]].

1. For $R := V = Core(FinDimVect)$ the [[core]] of [[complex vector spaces|complex]] [[finite dimensional vector spaces]] we have $H V$ is the complex [[K-theory spectrum]].

1. For $V_{\mathbb{R}}$ analogously we get the real K-theory spectrum.

So by the above theorem

1. $\mathcal{K}(E) \simeq K(S) \simeq A(*)$

1. $\mathcal{K}(V) \simeq K(ku)$;

1. etc.


**Remarks** 

1. A. Osono: The equivalence $\mathcal{K}(R) \simeq K(H R)$ of [[topological space]]s is even an equivalence of [[infinity loop space]]s;

1. Application of that: 

   a) for $E$ a [[ring spectrum]]: find a model 

   $$
     E \simeq H R(R)
   $$

   and use the equivalence $\mathbb{K}(R) \simeq K(H R E)$ to understand
   _arithmetic_ properties of $E$.

   b) Often one knows $K(H(R))$ via calculations. here $\mathcal{K}(R)$ might
   help to get some deeper understanding.

   c) Theorem ([[Birgit Richter]]): for $R$ a bimonoidal category with
   anti-involution, then you get an involution of $\mathcal{K}(R)$.


## Related concepts

* [[red-shift conjecture]]


## References
 {#References}

The original articles on BDR 2-vector bundles are

* [[Nils Baas]], [[Ian Dundas]],  [[John Rognes]], _Two-vector bundles and forms of elliptic cohomology_, in: _Topology, geometry and quantum field theory_, volume 308 of London Math. Soc. Lecture Note Ser., pages 18&#8211;45.
Cambridge Univ. Press, Cambridge, (2004).

Their [[classifying spaces]] are discussed in

* [[Nils Baas]], [[Ian Dundas]], [[Birgit Richter]], [[John Rognes]], _Ring completion of rig categories_ ([arXiv:0706.0531](http://arxiv.org/abs/0706.0531))

  (a previous version of this carried the title _Two-vector bundles define a form of elliptic cohomology_)

* [[Nils Baas]], M. B&#246;ckstedt, [[Tore Kro]], _Two-Categorical Bundles and Their Classifying Spaces_ (2008) ([arXiv:math/0612549](http://arxiv.org/abs/math/0612549)), .

Divisibility of the gerbe on the 3-sphere, seen as a 2-vector bundle is in

* [[Christian Ausoni]], [[Bjørn Ian Dundas]] and [[John Rognes]],  _Divisibility of the Dirac magnetic monopole as a two-vector bundle over the three-sphere_, Doc. Math. 13, 795-801 (2008). ([dml:45387](https://eudml.org/doc/45387), [pdf](http://www.math.univ-paris13.fr/~ausoni/papers/ADR08.pdf))

Orientation of BDR 2-vector bundles is discussed in 

* Thomas Kragh, _Orientations and Connective Structures on 2-vector Bundles_ Mathematica Scandinavica, 113 (2013) no 1, ([journal](http://www.mscand.dk/article/view/15482)), ([arXiv:0910.0131](http://arxiv.org/abs/0910.0131))

[[!redirects BDR 2-vector bundles]]