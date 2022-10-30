
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

* a [[local action functional]] is a maps

  $$
    S : \Gamma(E) \to \marthbb{R}
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


## Properties

### The fundamental variational formula

+-- {: .num_defn }
###### Definition

A **source form** is an element $\alpha$ in $\Omega^{n,1}$ such that

$$
  \alpha_\phi(\delta \phi)
$$

depends only on the 0-jet of $\delta \phi$.


=--

+-- {: .num_prop #VariationOfLagrangian}
###### Proposition

Let $L \in \Omega^{n,0}(j_\infty E)$.

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
  \omega := \int_\Sigma \Omega \in \Omega^{0,2}
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

Let $L \in \Omega^{n,0}$.

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

An early discussion with application to [[covariant phase space]]s and their [[presymplectic structure]] is in

* [[Gregg Zuckerman|G. J. Zuckerman]], _Action Principles and Global Geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scientific, Singapore, 1987, pp. 259&#8364;284. ([[ZuckermanVariation.pdf:file]])
 {#Zuckerman}

An introduction is in 

* Ian Anderson, _Introduction to the variational bicomplex_ in Mathematical aspects of classical field theory, Contemp. Math. 132 (1992) 51&#8211;73.

A textbook account is in 

* Ian Anderson, _The variational bicomplex_ Utah State University (1989) ([pdf](http://www.math.usu.edu/~fg_mp/Publications/VB/vb.pdf))


A generalization to [[multisymplectic geometry]] is discussed in

* Thomas Bridges, Peter Hydon, Jeffrey Lawson, _Multisymplectic structures and the variational bicomplex_  ([pdf](http://personal.maths.surrey.ac.uk/st/T.Bridges/PAPERS/MPCPS-Paper-09024.pdf))

See also 

* Peter Olver, _Applications of Lie groups to differential equations_, Springer
