
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 
  {#Idea}

The [[cochain cohomology]] of the framed [[knot graph complex]] (sometimes called the "Wilson graph complex") in the bidegree corresponding to trivalent graphs, hence to [[Jacobi diagrams]], coincides with the space of framed [[weight systems]] on [[Jacobi diagrams]], [[chord diagrams modulo 4T are Jacobi diagrams modulo STU|equivalently]] on [[round chord diagrams]]:

$$
  \underset{
    \mathclap{
    {\phantom{a}}
    \atop
    {
      {\color{blue}cohomology\;of\;knot\;graph\;complex}
      \atop
      {\color{blue}spanned\;by\;trivalent\;graphs}
    }
    }
  }{
  H^{\bullet}
  \big(
    GraphCplx_3 
  \big)
  }
  \underoverset{
    \phi
  }{
   \;\;\;\simeq\;\;\;
  }{
    \longleftarrow
  }
  \underset{
    \phantom{a}
    \atop
    {
      {\color{blue}framed\;weight\;systems\;on}
      \atop
      {\color{blue}round\;chord\;diagrams}
    }
  }{
    \mathcal{W}^\bullet
  }
  \;\simeq\;
  \underset{
    \phantom{a}
    \atop
    {
      {\color{blue}\weight\;systems\;on}
      \atop
      {\color{blue}Jacobi\;diagrams}
    }
  }{
    \mathcal{W}^\bullet
  }
$$

This statement is made explicit as [CCRL 02, Prop. 7.6](#CattaneoCottaRamusinoLongoni02), where it is noticed that this is implicit in statement and proof of [AF 96, Theorem 1](#AF96) (where in turn the argument is attributed to [Kohno 94](#Kohno94)!)

Moreover: 

If $w \in \mathcal{W}$ is a [[weight system]] and $D \in \mathcal{D}$ is a [[Jacobi diagram]] such that $w(D) \neq 0$, then $\phi(w) \in Graphs$ contains a non-vanishing multiple of $D$ as a summand.

This is made explicit as [CCRL 02, Remark 7.7](#CattaneoCottaRamusinoLongoni02) and again this is implicit in the statement of [AF 96, Theorem 1](#AF96).

## Ingredients
 {#Ingredients}

Write 

$$
  Graphs^\bullet \;\in\; Set^{\mathbb{N}}
$$

for the [[graded set]] of [[isomorphism classes]] of  framed knot graphs ("Wilson graphs" [AF 96, Section 1](#AF96), slightly differing from the un-framed knot graphs in [CCRL 02](#CattaneoCottaRamusinoLongoni02)). 

By definition, a [[graph]] $\Gamma \in Graphs$ must have [[even number]] of [[vertices]], and its degree is half that number ([AF 96, (2.9)](#AF96))

$$
  \Gamma \;\in\; Graphs^{(\# Vert_\Gamma)/2}
  \,.
$$

Write

$$
  Graphs_3^\bullet \subset Graphs^\bullet
$$

for the [[graded set|graded]] [[subset]] of trivalent graphs.

For any $\Gamma \in Graphs$ write 

$$
  Aut(\Gamma)
  \;\in\;
  Grp
$$

for its [[automorphism group]], a [[finite group]] whose [[order of a group|order]] we denote by

$$
  \left\vert Aut(\Gamma)\right\vert
  \;\in\;
  \mathbb{N}
  \,.
$$


Write 

$$
  GraphCplx^\bullet \;\in\; Ch^\bullet(\mathbb{R})
$$

for the corresponding [[knot graph complex]] and

$$
  GraphCplx_3^\bullet \subset GraphCplx^\bullet
$$

for the sub-vector space spanned by the trivalent graphs (not a subcomplex! as the differential increases the valence of vertices by one).

Write 

$$
  \mathcal{A}_\bullet \in Vect_\bullet(\mathbb{R})
$$

for the [[graded vector space]] of [[Jacobi diagrams]] [[quotient vector space|modulo]] the [[STU-relations]].

This is the graded [[linear dual]] of the space of [[weight systems]] 

$$
  \mathcal{W}^\bullet
  \;\coloneqq\;
  (\mathcal{A}_\bullet)^\ast
$$

Hence if we regard 

$$
  \mathcal{A}_\bullet
  \;=\;
  (\mathcal{A}^{-\bullet}, d= 0)
$$

as a [[cochain complex]] in non-positive degree with vanishing [[differential]], then its [[tensor product of cochain complexes]] with the knot graph complex is the [[cochain complex]] whose closed elements are the graded [[linear maps]] from $\mathcal{W}^\bullet$ to the [[cochain cohomology]] $H^\bullet(GraphCplx)$ of the [[knot graph complex]]:

\[
  \label{TensorCochainsAsMaps}
  Z^0
  \big( 
    \mathcal{A}_\bullet
    \otimes 
    GraphCplx^\bullet
  \big)
  \;\simeq\;
  Hom
  \big(
    \mathcal{W}^\bullet
    ,
    H^\bullet(GraphCplx)
  \big)
\]


Also write

\[
  \array{ 
    && Graphs^\bullet
    \\
    & 
      {}^{\mathllap{ [-]_J }}
      \swarrow 
    && 
     \searrow^{\mathrlap{ [-]_C }}
    \\
    \mathcal{A}_\bullet
    &&
    &&
    GraphCplx^\bullet
  }
\]

for the [[functions]] that send a [[graph]] to the defining [[linear basis|basis]] [[vector]] that it represents in these [[vector spaces]], respectively.



## Statement
  {#Statement}

For all $n \in \mathbb{N}$, the element

$$
  \begin{aligned}
    Z_n
    \;\coloneqq\;
    \underset{
     \Gamma \in Graphs^n 
    }{\sum}
    \left(
      \frac{1}{\left\vert \Gamma\right\vert}
      \,
      [\Gamma]_J \otimes [\Gamma]_C
    \right)
   \;
   & 
    \in
    \;\;
    Z^0
    \big( 
       \mathcal{A}_n \otimes GraphCplx^n
    \big) 
    \\
    & 
    \;\simeq\;
    Hom
    \big(
      \mathcal{W}^n,
      H^n(GraphCplx)
    \big)
  \end{aligned}
$$

takes values in [[cocycles]] of the trivalent knot graph complex ([AF 96, Theorem 1](#AF96)):

$$
  d_{{}_{GraphCplx}} \, Z_n \;=\; 0
$$

hence, by (eq:TensorCochainsAsMaps), defines a graded [[linear function]]

$$
  \mathcal{W}^n
  \overset{
    \;\;\phi\;\;
  }{\longrightarrow}
  H^n(GraphCplx_3)
$$

from [[weight systems]] on [[Jacobi diagrams]] ([[chord diagrams modulo 4T are Jacobi diagrams modulo STU|equivalently]] on [[round chord diagrams]]) to the [[cochain cohomology]] of the framed [[knot graph complex]] spanned by trivalent graphs.


## References

The statement is made explicit in

* {#CattaneoCottaRamusinoLongoni02} [[Alberto Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Configuration spaces and Vassiliev classes in any dimension_, Algebr. Geom. Topol. 2 (2002) 949-1000 ([arXiv:math/9910139](https://arxiv.org/abs/math/9910139))

following

* {#AF96} Daniel Altschuler, Laurent Freidel, _Vassiliev knot invariants and Chern-Simons perturbation theory to all orders_, Commun. Math. Phys. 187 (1997) 261-287 ([arXiv:q-alg/9603010](https://arxiv.org/abs/q-alg/9603010))

See also

* {#Kohno94} [[Toshitake Kohno]], _Vassiliev invariants and de Rham complex on the space of knots_, 
In: Yoshiaki Maeda, Hideki Omori, [[Alan Weinstein]] (eds.), _Symplectic Geometry and Quantization_, Contemporary Mathematics 179 (1994): 123-123 ([doi:10.1090/conm/179](http://dx.doi.org/10.1090/conm/179))

