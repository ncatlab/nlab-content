
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $X$ a ([[spacetime]]) [[manifold]] and $E \to X$ a [[bundle]] (in [[physics]] called the _[[field bundle]]_) with [[jet bundle]] $j_\infty E \to X$, the **variational bicomplex** is essentially the [[de Rham complex]] $(\Omega^\bullet(j_\infty E),\mathbf{d})$ of $j_\infty E$ with [[differential forms]] $\Omega^n(j_\infty E) = \bigoplus_{h+v=n} \Omega^{h,v}(E)$ bigraded by [[horizontal differential form|horizontal]] degree $h$ (with respect to $X$) and vertical degree $v$ (along the [[fiber]]s of $j_\infty E$)). Accordingly the [[differential]] decomposes as

$$
  \mathbf{d} = d + \delta
  \,,
$$

where $\mathbf{d}$ is the [[de Rham differential]] on $j_\infty E$, $d$ is called the **horizontal differential** and $\delta$ is called the **vertical differential**.

Vector fields on $J^\infty E$ also split into a direct sum of **vertical** and **horizontal** ones, respectively being annihilated by contraction with any horizontal $1$-forms or with any vertical $1$-forms, $\mathfrak{X}(J^\infty E) = \mathfrak{X}_H(J^\infty E) \oplus \mathfrak{X}_V(J^\infty E)$. A special kind of vertical vector field $v \in \mathfrak{X}_V(J^\infty E)$ is called **evolutionary** provided it satisfies $\mathcal{L}_v d = d \mathcal{L}_v$ and $\mathcal{L}_v = \iota_v \delta + \delta \iota_v$, we denote the subspace of evolutionary vector fields as $\mathfrak{X}_{ev}(J^\infty E) \subset \mathfrak{X}_V(J^\infty E)$.

Much of [[classical mechanics]] and [[classical field theory]] on $X$ is formalized in terms of the variational bicomplex. For instance 

* a field configuration is a [[section]] of $E$;

* a [[Lagrangian]] is an element $L \in \Omega^{n,0}(E)$;

* a [[local action functional]] is a map

  $$
    S : \Gamma(E) \to \mathbb{R}
  $$

  of the form

  $$
    S(\phi) = \int_X L(j_\infty \phi)
    \,,
  $$

* the [[Euler-Lagrange equation]] is 

  $$
    E(L) := \delta L \mod im d = 0
  $$

* the [[covariant phase space]] is the locus 

  $$
    \{
     \phi \in \Gamma(E) | E(L)(j_\infty \phi) = 0
   \}
  $$

* a [[conserved current]] is an element $\eta\in \Omega^{n-1,0}(E)$ that is  horizontally closed on the covariant phase space

  $$
    d \eta = 0 \mod E(L)
  $$

* a [[symmetry]] is an evolutionary vector field $v$ such that
  
  $$
    v(L) = 0 \mod im d
  $$

* [[Noether's theorem]] asserts that every [[symmetry]] induces a [[conserved current]].


## Definition

Let $X$ be a [[smooth manifold]] and $p : E \to X$ some smooth [[bundle]] over $X$. Write $j_\infty E \to X$ for the corresponding [[jet bundle]].

The spaces of [[section]]s $\Gamma(E)$ and $\Gamma(j_\infty E)$ canonically inherit a generalized smooth structure that makes them [[diffeological space]]s: we have a [[pullback]] [[diagram]] of diffeological spaces

$$
  \array{
     \Gamma(E) &\to& *
     \\
     \downarrow && \downarrow^{id}
     \\
     [X,E] &\stackrel{p_*}{\to}& [X,X]
  }
  \,.
$$

This induces the [[evaluation map]]

$$
  X \times \Gamma(E) \to E
  \,.
$$

and composed with the jet prolongation

$$
  j_\infty : \Gamma(E)  \to \Gamma(j_\infty E)
$$

it yields a smooth map ([[homomorphism]] of [[diffeological space]]s) 

\[
  \label{EProlongation}
  e_\infty : X \times \Gamma(E) \stackrel{(id,j_\infty)}{\to}
   X \times \Gamma(j_\infty E)
   \stackrel{ev}{\to}
  j_\infty E
  \,.
\]

Write 

$$
  \Omega^{\bullet, \bullet}(X \times \Gamma(E))
$$

for the [[cochain complex]] of smooth differential forms on the [[product]] $X \times \Gamma(E)$, bigraded with respect to the differentials on the two factors

$$
  \mathbf{d} \coloneqq d + \delta
  \,,
$$

where the $\mathbf{d}$, $d$ and $\delta$, are the [[de Rham differential]]s of $X\times\Gamma(E)$, $X$ and $\Gamma(E)$, respectively.


+-- {: .num_defn }
###### Definition

The **variational bicomplex** of $E \to X$ is the sub--bi-complex of $\Omega^{\bullet, \bullet}(X \times \Gamma(E))$ that is the [[image]] of the pullback of forms along the map $e_\infty$ (eq:EProlongation):

$$
  e_\infty^* : \Omega^{\bullet}(j_\infty E) \to 
   \Omega^\bullet(X \times \Gamma(E))
  \,.
$$

We write 

$$
  \Omega^{\bullet, \bullet}_{loc}
  \coloneqq
  im (e_\infty^*)
$$

and speak of the bicomplex of **local forms** on sections on $E$.

=--

The bicomplex structure on $\Omega^{\bullet, \bullet}_{loc}$ is attributed in ([Olver 86](#Olver86)) to ([Takens](#Takens)). The above formulation as the image of the evident bicomplex of forms on $X \times \Gamma(E)$ is due to ([Zuckerman, p. 5](#Zuckerman)).

+-- {: .num_remark #CharacterizationOfHorizontalDifferential}
###### Remark

In terms of a [[coordinate chart]] $(x^i, u^\alpha,u^\alpha_i,u^\alpha_{i j},\cdots)$ of $E$ covering a coordinate chart $(X^i)$ of $X$, the action of the horizontal differential on functions $f \in C^\infty(j_\infty E)$ is given by the formula for the total derivative operation, but with concrete differentials substituted by the respective jet coordinates:

$$
  d f = 
  \sum_i
  \left(
    \frac{\partial f}{\partial x^i}
    + 
    \frac{\partial f}{\partial u^\alpha}u^\alpha_i
    +
    \sum_j \frac{\partial f}{\partial u^\alpha_j} u^\alpha_{j i}
    +
    \cdots
  \right)
  d x^i
  \,.
$$

(For instance ([Anderson 89, p. 10](#Anderson89)).)

More abstractly, the horizontal differential is characterized by the fact that it takes horizontal forms to horizontal forms, and that for all sections $\phi \in \Gamma(E)$ it respects [[pullback of differential forms]] along the jet prolongation $j_\infty \phi \in \Gamma(j_\infty E)$

$$
  (j_\infty \phi)^\ast \circ d = d \circ (j_\infty \phi)^\ast
$$

(where on the right we have the ordinary de Rham differential on the base space).



=--


## Properties

### Horizontal, vertical, and total cohomology

Let $E \to X$ be a smooth [[fiber bundle]] over a base [[smooth manifold]] $X$ of [[dimension]] $n.$ Write $J^\infty E \to X$ for the [[jet bundle]] of $E\to X$. 

Write 

$$
  \mathcal{F}^s(J^\infty E) \coloneqq I (\Omega^{n,s}(J^\infty E))
$$ 

for the projection of $(n,s)$-forms to the image of the "interior Euler operator" ([Anderson 89, p. 21 (50/318)](#Anderson89)).

+-- {: .num_prop #ELComplexHasSameCohomologyAsDeRhamComplex}
###### Proposition

The [[cochain cohomology]] of the Euler-Lagrange complex

$$
 0 \to \mathbb{R}
 \to
  \Omega^{0,0}(J^\infty E)
  \stackrel{d_H}{\to}
  \Omega^{1,0}(J^\infty E)
  \stackrel{d_H}{\to}
  \cdots 
  \stackrel{d_H}{\to}
  \Omega^{n,0}(J^\infty E)
  \stackrel{E}{\to}
  \mathcal{F}^1(J^\infty E)
  \stackrel{\delta_V}{\to}
  \mathcal{F}^2(J^\infty E)
  \stackrel{\delta_V}{\to}
  \cdots
$$

is [[isomorphism|isomorphic]] to the [[de Rham cohomology]] of the total space $E$ of the given fiber bundle.

=--

([Anderson 89, theorem 5.9](#Anderson89)).

### The fundamental variational formula

+-- {: .num_defn }
###### Definition {#BicomplexDefinition}

A **source form** is an element $\alpha$ in $\Omega^{n,1}_{loc}$ such that

$$
  \alpha_\phi(\delta \phi)
$$

depends only on the 0-jet of $\delta \phi$.


=--

+-- {: .num_prop #VariationOfLagrangian}
###### Proposition

Let $L \in \Omega^{n,0}_{loc}$.

Then there is a unique source form $E(L) $ such that

$$
  \delta L = E(L) - d \Theta
  \,.
$$

Moreover

* $E(L)$ is independent of changes of $L$ by $d$-exact terms:

  $$
    E(L) = E(L + d K)
    \,.
  $$

* $\Theta$ is unique up to $d$-exact terms.

=--

This is ([Zuckerman, theorem 3](#Zuckerman)).

Here $E$ is the _[[Euler-Lagrange equations|Euler-Lagrange operator]]_ .

+-- {: .num_defn }
###### Definition

Write

$$
  \Omega = \delta \Theta
  \,.
$$

=--

+-- {: .num_remark #HorizontalDOfOmega}
###### Remark

By prop. \ref{VariationOfLagrangian} have

$$
  d \Omega = -\delta E(L)
  \,.
$$

=--

+-- {: .num_prop #SecondOrderVariationVanishesOnShell}
###### Proposition

$\delta E$ vanishes when restricted to vertical tangent vectors based in [[covariant phase space]] (but not necessarily tangential to it).

$$
  \delta E(L) |_{T_{E(L) = 0} \Gamma(E)} = 0
  \,.
$$

=--

This is ([Zuckerman, lemma 8]{#Zuckerman}).

### Presymplectic covariant phase space

+-- {: .num_cor }
###### Corollary

The form $\Omega$ is a [[conserved current]].

=--

+-- {: .proof}
###### Proof

By remark \ref{HorizontalDOfOmega} and 
prop. \ref{SecondOrderVariationVanishesOnShell}.

=--

+-- {: .num_defn #ThePresymplecticForm}
###### Definition

For $\Sigma \subset X$ a [[compact space|compact]] [[closed manifold|closed]] submanifold of [[dimension]] $n-1$, one says that 

$$
  \omega := \int_\Sigma \Omega \in \Omega^{0,2}_{loc}
$$

is the [[presymplectic structure]] on [[covariant phase space]] relative to $\Sigma$.


=--

+-- {: .num_prop }
###### Proposition

The 2-form $\omega$ is indeed closed

$$
  \delta \omega = 0
$$

and in fact exact: 

$$
  \theta := \int_\Sigma \Theta
$$

is its _presymplectic potential_ .

$$
  \delta \theta  = \omega
  \,.
$$

=--

### Symmetries

Let $L \in \Omega^{n,0}_{loc}$.

+-- {: .num_defn }
###### Definition

An evolutionary vertical vector field $v \in \mathfrak{X}_{ev}(J^\infty E)$ is a **[[symmetry]]** if

$$
  v(L) = 0 \mod im d
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The presymplectic form $\omega$ from def. \ref{ThePresymplecticForm} is annihilated by the Lie derivative of the vector field on $\Gamma(E)$ induced by a symmetry.

=--

This appears as ([Zuckerman, theorem 13](#Zuckerman)).

## References

The variational bicomplex was introduced independently in

* W.M. Tulczyjew, _The Euler-Lagrange resolution_ , in Lecture Notes in Mathematics 836 22&#8211;48 (Springer-Verlag, New York 1980).

* A.M. Vinogradov, _A spectral sequence associated with a non-linear differential equation, and the algebro-geometric foundations of Lagrangian field theory with constraints_ , Sov.
Math. Dokl. 19 (1978) 144&#8211;148.

* A.M. Vinogradov, _The $C$-spectral sequence, Lagrangian formalism and conservation laws_ I, II, J. Math. Anal. Appl. 100 (1984) 1&#8211;129.

Also 

* {#Takens} F. Takens, _A global version of the inverse problem of the calculus of variations_ J. Diff. Geom. 14 (1979) 543-562

An introduction is in 

* Ian Anderson, _Introduction to the variational bicomplex_ in Mathematical aspects of classical field theory, Contemp. Math. 132 (1992) 51&#8211;73, [gBooks](http://books.google.com/books?id=NuiJ0c72_gQC&lpg=PA51&ots=-zAVQLViUn&dq=Zuckerman%20variational%20problems)
 
Textbook accounts include  

* {#Olver86} [[Peter Olver]], section 5.4 of _Applications of Lie groups to differential equations_, Springer Graduate Texts in Mathematics 107 (1986)

* {#Anderson89} Ian Anderson, _The variational bicomplex_, Utah State University 1989 ([pdf]( http://math.uni.lu/~jubin/seminar/bicomplex.pdf)) 
 

An early discussion with application to [[covariant phase spaces]] and their [[presymplectic structure]] is in

* {#Zuckerman} [[Gregg Zuckerman|G. J. Zuckerman]], _Action principles and global geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259&#8364;284. ([[ZuckermanVariation.pdf:file]])


An invariant version (under group action) is in

* Irina A. Kogan, Peter J. Olver, _The invariant variational bicomplex_, [pdf](http://www4.ncsu.edu/~iakogan/papersPDF/sivKoganOlver.pdf)

See also 

* [[Victor Kac]], _An explicit construction of the complex of variational calculus and Lie conformal algebra cohomology_, talk at Algebraic Lie Theory, Newton Institute 2009, [video](http://sms.cam.ac.uk/media/538761)

An application to [[multisymplectic geometry]] is discussed in

* Thomas Bridges, Peter Hydon, Jeffrey Lawson, _Multisymplectic structures and the variational bicomplex_  ([pdf](http://personal.maths.surrey.ac.uk/st/T.Bridges/PAPERS/MPCPS-Paper-09024.pdf))