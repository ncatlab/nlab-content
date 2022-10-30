
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $X$ a ([[spacetime]]) [[manifold]] and $E \to X$ a [[bundle]] with [[jet bundle]] $j_\infty E \to X$, the **variarional bicomplex** is essentially the [[de Rham complex]] of $j_\infty E$ with [[differential form]]s bigraded by horizontal degree (with respect to $X$) and vertical degree (along the [[fiber]]s of $j_\infty E$)). Accordingly the [[differential]] decomposes as

$$
  D = d + \delta
  \,,
$$

where $d$ is the [[de Rham differential]] on $X$ and $\delta$ is the variational differential.

Much of [[classical mechanics]] and [[classical field theory]] on $X$ is formalized in terms of the variational bicomplex. For instance 

* a field configuration is a [[section]] of $E$;

* a [[Lagrangian]] is an element $L \in \Omega^{n,0}(j_\infty E)$;

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
    E(L) := \delta L mod im(d) = 0
  $$

* the [[covariant phase space]] is the locus 

  $$
    \{
     \phi \in \Gamma(E) | E(L)(j_\infty \phi) = 0
   \}
  $$

* a [[conserved current]] is an element in $\Omega^{n-1,0}(j_\infty E)$ that is $d$-closed on covariant phase space;

* a [[symmetry]] is a vertical vector field $v$ such that
  
  $$
    v(L) = 0 mod im(d)
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
  D := d + \delta
  \,,
$$

where the first $d = d_{dR}$ is the [[de Rham differential]] on $X$.


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
  :=
  im (e_\infty^*)
$$

and speak of the bicomplex of **local forms** on sections on $E$.

=--

The bicomplex structure on $\Omega^{\bullet, \bullet}_{loc}$ is attributed in ([Olver](#Olver)) to ([Takens](#Takens)). The above formulation as the image of the evident bicomplex of forms on $X \times \Gamma(E)$ is due to ([Zuckerman, p. 5](#Zuckerman)).

## Properties

### The fundamental variational formula

+-- {: .num_defn }
###### Definition

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
  \delta L = E(L) + d \Theta
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
  d \Omega = \delta E(L)
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

For $\Sigma \subset X$ a [[compact space|compact]] [[closed space|closed]] submanifold of [[dimension]] $n-1$, one says that 

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

A vertical vector fields $v \in T_v E \subset T_v j_\infty E$ is a **[[symmetry]]** if

$$
  v(L) = 0 mod im(d)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The presymplectic form $\omega$ from def. \ref{ThePresymplecticForm} is degenerate on symmetries.

=--

This appears as ([Zuckerman, theorem 13](#Zuckerman)).

## References

The variational bicomplex was introduced independently in

* W.M. Tulczyjew, _The Euler-Lagrange resolution_ , in Lecture Notes in Mathematics 836 22&#8211;48 (Springer-Verlag, New York 1980).

* A.M. Vinogradov, _A spectral sequence associated with a non-linear differential equation, and the algebro-geometric foundations of Lagrangian field theory with constraints_ , Sov.
Math. Dokl. 19 (1978) 144&#8211;148.

* A.M. Vinogradov, _The $C$-spectral sequence, Lagrangian formalism and conservation laws_ I, II, J. Math. Anal. Appl. 100 (1984) 1&#8211;129.

Also 

* F. Takens, _A global version of the inverse problem of the calculus of variations_ J. Diff. Geom. 14 (1979) 543-562
 {#Takens}

An textbook account is in section 5.4 of 

* Peter Olver, _Applications of Lie groups to differential equations_, Springer Graduate Texts in Mathematics 107 (1986)
 {#Olver}

An invariant version (under group action) is in

* Irina A. Kogan, Peter J. Olver, _The Invariant Variational Bicomplex_, [pdf](http://www4.ncsu.edu/~iakogan/papersPDF/sivKoganOlver.pdf)

An early discussion with application to [[covariant phase space]]s and their [[presymplectic structure]] is in

* [[Gregg Zuckerman|G. J. Zuckerman]], _Action Principles and Global Geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259&#8364;284. ([[ZuckermanVariation.pdf:file]])
 {#Zuckerman}

An introduction is in 

* Ian Anderson, _Introduction to the variational bicomplex_ in Mathematical aspects of classical field theory, Contemp. Math. 132 (1992) 51&#8211;73, [gBooks](http://books.google.com/books?id=NuiJ0c72_gQC&lpg=PA51&ots=-zAVQLViUn&dq=Zuckerman%20variational%20problems)

A textbook account is in 

* Ian Anderson, _The variational bicomplex_ Utah State University (1989) ([pdf](http://www.math.usu.edu/~fg_mp/Publications/VB/vb.pdf))


A generalization to [[multisymplectic geometry]] is discussed in

* Thomas Bridges, Peter Hydon, Jeffrey Lawson, _Multisymplectic structures and the variational bicomplex_  ([pdf](http://personal.maths.surrey.ac.uk/st/T.Bridges/PAPERS/MPCPS-Paper-09024.pdf))


