
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### General

Suppose we are given a commutative unital [[ring]] $k$ and a [[module]] $V$ over $k$ equipped with a skew-symmetric [[bilinear form]] 

$$
  \omega: V\otimes_k V\to k
  \,.
$$ 

(Typically, one requires $\omega$ to be non-degenerate, see [below](InSymplecticGeometry), but this is not needed for the following definition). 

The __Heisenberg Lie algebra__ $Heis(V, \omega)$ corresponding to $(V,\omega)$ is the [[Lie algebra]] given by the $k$-module $V\oplus k$ together with the unit $k \hookrightarrow V\oplus k$, $s\mapsto (0,s) =: s 1$ and Lie $k$-algebra bracket

$$
  [(m,s),(m',s')] := (0, \omega(m,m')1)
  \,.
$$


### In symplectic geometry
 {#InSymplecticGeometry}

The notion of Heisenberg algebra arose in the study of [[quantization]] by tools of [[symplectic geometry]]:

A special case of the above definition is that where $(V,\omega)$ a [[symplectic vector space]] (hence $k$ a [[field]] and $\omega$ non-degenerate).

In this case the Heisenberg algebra is a sub-Lie algebra of the Lie algebra underlying the [[Poisson algebra]] of $(V,\omega)$. For more on this see [below](#RelationToPoissonAlgebra).

### Heisenberg Lie $n$-algebras in $n$-plectic geometry
 {#InnplecticGeometry}

We discuss a generalization of the notion of Heisenberg Lie algebra from ordinary [[symplectic geometry]] to a notion of _Heisenberg [[Lie n-algebra]]_  in [[higher geometric quantization]] of [[n-plectic geometry]]. See
at _[[Heisenberg Lie n-algebra]]_ for more.

The following definition is naturally motivated from the fact that:

1. The ordinary Heisenberg Lie algebra is the sub-Lie algebra of the 
[[Poisson bracket]] Lie algebra, the one underlying the corresponding [[Poisson algebra]] (see [below](#RelationToPoissonAlgebra)) on the constant and linear functions.

1. The generalization of [[Poisson bracket|Poisson brackets]] to [[Poisson Lie n-algebras]] in [[n-plectic geometry]] for all $n$ is established (see there).

In view of this, the following definition takes the Heisenberg Lie $n$-algebra to be the sub-Lie $n$-algebra of the [[Poisson Lie n-algebra]] on the linear and constant differential forms.

First we need the following definition, which is elementary, but nevertheless worth making explicit once.

+-- {: .num_defn}
###### Definition

Let $n \in \mathbb{N}$, let $(V, \omega)$ be an [[n-plectic vector space]]. 

The **corresponding $n$-plectic manifold** is the [[n-plectic manifold]] $(V, \mathbf{\omega})$, with $V$ now the canonical [[smooth manifold]] structure on the given vector space, and with 

$$
  \mathbf{\omega} \in \Omega^{n+1}(V)
$$

the [[differential form]] obtained by left (right) translating $\omega$ along $V$.

Explicitly, for all [[vector fields]] $\{v_i \in \Gamma(T V)\}_{i = 1}^n$ and all points $x \in V$ we set

$$
  \mathbf{\omega}_x(v_1, \cdots, v_n)
  :=
  \omega(v_1(x), \cdots, v_n(x))
  \,.
$$

Here on the right --  and in all of the following -- we are using that every [[tangent space]] $T_x V$ of $V$ is naturally identified with $V$ itself

$$
  T_x V \stackrel{\simeq}{\to} V
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

Let $n \in \mathbb{N}$, 
let $(V, \omega)$ be an [[n-plectic vector space]]
and let $(V, \mathbf{\omega})$ be the corresponding
[[n-plectic manifold]].

The **Heisenberg Lie $n$-algebra** $Heis(V,\omega)$ is the sub-[[Lie n-algebra]] of the [[Poisson Lie n-algebra]] $\mathcal{P}(V, \omega)$ on those [[differential forms]] which are either linear or constant (with respect to left/right translation on $V$).

=--

All one has to observe is:

+-- {: .num_prop}
###### Proposition

This is indeed a sub-Lie $n$-algebra.

=--

+-- {: .proof}
###### Proof

We need to check that the linear and constant forms are closed under the [[L-infinity algebra]] brackets of $\mathcal{P}(V, \omega)$. 

The only non-trivial such brackets are the unary one, and the ones on elements all of degree 0. 

The unary bracket is given by the de Rham differential. Since this sends a linear form to a constant form and a constant form to 0, our sub-complex is closed under this.

Similarly, the brackets on elements all in degree 0 is given by contraction of $\mathbf{\omega}$ with the Hamiltonian vector fields of linear or constant forms. Since $\mathbf{\omega}$ is a constant form, and since the de Rham differential of a linear or constant form is constant (or even 0), these Hamiltonian vector fields are necessarily constant. Hence their contraction with $\mathbf{\omega}$ gives a constant form.

=--

## Properties


### Relation to Poisson algebra
 {#RelationToPoissonAlgebra}

We discuss how the notion of Heisenberg Lie algebra relates to that of _[[Poisson algebra]]_.

+-- {: .num_prop}
###### Proposition

For $(X, \omega)$ a [[symplectic vector space]], there is a [[natural transformation|natural]]
[[Lie algebra]] [[homomorphism]]

$$
  Heis(V, \omega) \hookrightarrow \mathcal{P}(V,\omega)
$$

exhibiting the Heisenberg Lie algebra as a [[subobject|sub]]-Lie algebra of that underlying the [[Poisson algebra]] $\mathcal{P}(V,\omega)$ of $V$.

=--

Namely, it is the sub-Lie algebra on the [[linear functions]] and the constant functions.

+-- {: .proof}
###### Proof

Let $(V, \omega)$ be a [[symplectic vector space]] over the [[real numbers]]. Using the canonical [[isomorphism]]
$\phi : T V \simeq V \times V$ of the [[tangent bundle]] of $V$ with the [[projection]] $p_1 : V \times V \to V$, we obtain from the [[bilinear form]] $\omega$ a [[differential form|differential 2-form]] $\mathbf{\omega} \in \Omega^2(V)$ by the assignment

$$
  \mathbf{\omega}(\mathbf{v}, \mathbf{w}) 
   := 
  \omega(p_2 \phi(\mathbf{v}), p_2 \phi(\mathbf{w}))
$$

for all $\mathbf{v}, \mathbf{w} \in \Gamma(T V)$.


This way $(V, \mathbf{\omega})$ is a [[symplectic manifold]] and thus comes with a [[Poisson algebra]].
Write $\mathcal{P}(V,\mathbf{\omega})$ for the [[Lie algebra]] underlying the [[Poisson algebra]] of $(V, \mathbf{\omega})$.

Its underlying [[vector space]] is the space $C^\infty(V)$ of [[smooth functions]] $V \to \mathbb{R}$. To every element $f \in C^\infty(V)$ is associated its _[[Hamiltonian vector field]]_ $\mathbf{v}_f \in \Gamma(T X)$, defined (uniquely, due to the non-degeneracy of $\omega$) by the equation

$$
  d_{dR} f = \mathbf{\omega}(\mathbf{v}_f, -)  
  \,.
$$

In terms of this, the [[Lie bracket]] of the Poisson algebra is defined to be

$$
  [f,g] := \mathbf{\omega}(\mathbf{v}_f, \mathbf{v}_g)
  \,.
$$

Inside all smooth functions sit the [[linear functions]] $V \to \mathbb{R}$, which form the [[dual vector space]] to $V$:

$$
  V^* \hookrightarrow C^\infty(V)
$$
$$
  \alpha \mapsto \alpha(-)
  \,.
$$


By the non-degeneracy of $\omega$, for every $f \in V^*$ there is an element $v_f \in V$ such that

$$
  f = \omega(v_f,-) \in C^\infty(V)
  \,.
$$

Moreover, the canonical extension $\mathbf{v}_f$ of $v_f$ to a vector field on $V$ is a [[Hamiltonian vector field]] for $f$

$$
  d_{dR} f = \mathbf{\omega}(\mathbf{v}_f,-) 
  \,.
$$


It follows that the Lie bracket of two [[linear functions]] $f,g$ in the Poisson algebra is

$$
  \begin{aligned} 
    [f,g]
      & = 
    \mathbf{\omega}(\mathbf{v}_f, \mathbf{v}_g)
     \\
    & =
     \omega(v_f, v_g)
  \end{aligned}
  \,.
$$

Notice that on the right we have a _constant_ function on $V$.

Write $\rho_2 : \mathbb{R} \hookrightarrow C^\infty(V)$ for the inclusion of the constant functions, and write

$$
  \rho_1
  :
  V 
    \stackrel{\omega}{\to} 
  V^* 
    \hookrightarrow 
  C^\infty(V)
  \,.
$$

Then, by the above, the inclusion

$$
  \rho : V \oplus \mathbb{R} \stackrel{(\rho_1, \rho_2)}{\to} C^\infty(V)
$$

induces a Lie algebra [[homomorphism]]

$$
  \rho 
  :
  Heis(V,\omega) 
    \hookrightarrow 
  \mathcal{P}(V, \mathbf{\omega})
$$

which exhibits the Heisenberg Lie algebra as a [[subobject|sub]]-Lie algebra of that underlying the Poisson algebra.

=--

### Integration to Heisenberg group

As for any [[Lie algebra]] one has [[Lie integration]] of the Heisenberg Lie algebra to a [[Lie group]]. This is called the _[[Heisenberg group]]_ (of the given [[symplectic vector space]]). 

### Relation to the Weyl algebra
 {#RelationToTheWeylAlgebra}

In the case of standard [[symplectic form]] on the [[Cartesian space]] $\mathbb{R}^{2n}$, the 
[[universal enveloping algebra]] of the Heisenberg Lie algebra is an [[associative algebra]] $\mathcal{U}\big(Heis(\mathbb{R}^{2n})\big)$. Depending on conventions, this either already is the [[Weyl algebra]] on $2n$ generators or else it becomes so after after forming the [[quotient algebra]] in which the central generator is identified with the [[unit element]] of the [[ground field]] -- whereas in the former case (considered eg. in [Kravchenko 2000, Def. 2.1](#Kravchenko00); [Bekaert 2005, p. 9](#Bekaert05)) the central generator plays the role of the formal [[Planck constant]] $\hbar$ with the Weyl algebra regarded as a [[formal deformation quantization]] of the [[symplectic manifold]] $\mathbb{R}^{2m}$.

Accordingly, given a [[Heisenberg Lie n-algebra|Heisenberg Lie $n$-algebra]] it makes sense to call its [[universal enveloping E-n algebra|universal enveloping $E_n$-algebra]] a _[[Weyl n-algebra|Weyl $n$-algebra]]_.


### Relation to the Heisenberg double

Given any [[Hopf algebra]], one can define its [[Heisenberg double]], which generalized the Heisenberg-Weyl algebra, which corresponds to the case when the Hopf algebra is the polynomial 
algebra. 

## References

Monograph:

* [[Ernst Binz]], Sonja Pods, *The geometry of Heisenberg groups --- With Applications in Signal Theory, Optics, Quantization, and Field Quantization*, Mathematical Surveys and Monographs **151**, American Mathematical Society (2008) &lbrack;[ams:surv-151](https://bookstore.ams.org/surv-151)&rbrack; 


Lecture notes:

* (section 4 in) Gordon, _Infinite-dimensional Lie algebras_, Lecture notes, Edinburgh (2008) ([pdf](http://www.maths.ed.ac.uk/~igordon/LA1.pdf))

* Teruji Thomas, _Geometric quantization II: Prequantization and the Heisenberg group_ ([pdf](http://www.maths.ed.ac.uk/~jthomas7/GeomQuant/Lecture2.pdf)), section 4 (relating to [[geometric quantization]])

Relation to the [[Weyl algebra]]:

* {#Kravchenko00} Olga Kravchenko, *Deformation Quantization of Symplectic Fibrations*, Compositio Mathematica **123** (2000) 131–165 &lbrack;[arXiv:math/9802070](https://arxiv.org/abs/math/9802070), [doi:10.1023/A:1002452002677](https://doi.org/10.1023/A:1002452002677)&rbrack;

* {#Bekaert05} [[Xavier Bekaert]], *Universal enveloping algebras and some applications in physics* (2005) &lbrack;[cds:904799](https://cds.cern.ch/record/904799), [pdf](https://cds.cern.ch/record/904799/files/cer-002575006.pdf)&rbrack;


A [[categorification]] of the Heisenberg algebra:

* [[Mikhail Khovanov]], _Heisenberg algebra and a graphical calculus_ ([arXiv:1009.3295](http://arxiv.org/abs/1009.3295))

* [[Owen Gwilliam]], [[Rune Haugseng]], _Linear Batalin-Vilkovisky quantization as a functor of ∞-categories_ ([arXiv:1608.01290](https://arxiv.org/abs/1608.01290))

An $n$-fold categorification of the Lie algebra underlying the [[Poisson algebra]] (and hence including the Weil algebra) for all $n$ to a [[Lie n-algebra]] is considered in [[n-plectic geometry]],

* [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis (2011) ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068))

[[!redirects Heisenberg Lie algebras]]

[[!redirects Heisenberg algebra]]
[[!redirects Heisenberg algebras]]

