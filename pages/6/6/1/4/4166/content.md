

#Contents#
* automatic table of contents goes here
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

Write $2Vect(X)$ for the equivalence classes of charted 2-vector bundles under these
morphisms. 

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

where the [[colimit]] is over acyclic [[Serre fibration]]s and $Gr(-)$ indicates
the [[Grothendieck group]] completion of the tensor product of 2-vector bundles.

**Proof** In BDR, Segal Birthday Proceedings 

**Note** $2Vect_n(X) = [X, |B Gl_n (V)| ]$.

BDR called $\mathcal{K}(V)$ the **2-K-theory** of the [[bimonoidal category]]
of [[Kapranov-Voevodsky 2-vector space]]s.

## The homotopy type of the classifying space

**Theorem** (Baas-Dundas-Rognes-Richter)

$\mathcal{K}(V) \simeq K(ku)$

Here:

* $ku$ is the connected version of the [[spectrum]] of  complex [[topological K-theory]];

* $K(-)$ denotes forming the [[algebraic K-theory]] spectrum of [[ring spectrum|ring spectra]].

So by the general formula for algebraic K-theory for ring spectra, this is 

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
  K(R) = \Omega B (\coprod_{n \geq 0} B Gl(R))
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
any other form of [[elliptic cohomology]]"

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

may be thought of as classifying the gerbe called the [[magnetic monopole]]-gerber

Postcomposing with $\mu : K(\mathbb{Z},3) \to K(ku)$

we have

Fact: $\mu$ gives a generator in $\pi_3 K(\mathbb{Z},3) = H^3(\mathbb{S}^3)$

**Theorem** (Ausoni-Dundas-Rognes)

$$
  j(\mu) = 2 \zeta - \nu
$$

in $\pi_3(K(ku))$

so regarded as a 2-vector bundle $\mu$ is not a generator

ADR: $\zeta$ is "half a monopole".

$$
  \pi_3(K(ku))  = \mathbb{Z} \oplus \mathbb{Z}/24 \mathbb{Z}
$$

(the first summand is $\zeta$, the second $\nu$).


Th: Krogh has an [[orientation]] theory for 2-vector bundles which says that $j(\nu)$
is not orientable.