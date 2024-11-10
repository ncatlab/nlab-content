+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _super Lie algebra_ is the analog of a [[Lie algebra]] in [[superalgebra]]/[[supergeometry]]. 

See also at *[[supersymmetry]]*.

## Definition

There are various equivalent ways to state the definition of super Lie algebras. Here are a few (for more discussion see at _[[geometry of physics -- superalgebra]]_):

### As Lie algebras internal to super vector spaces
 {#AsLieAlgebrasInternalToSuperVectorSpaces}

+-- {: .num_defn #SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}
###### Definition

A _[[super Lie algebra]]_ is a [[Lie algebra object]] [[internalization|internal]] to the [[symmetric monoidal category]] $sVect = (Vect^{\mathbb{Z}/2}, \otimes_k, \tau^{super} )$ of [[super vector spaces]] (a _[[Lie algebra object]] in [[super vector spaces]]_).
Hence this is

1. a [[super vector space]] $\mathfrak{g}$;

1. a homomorphism

   $$
     [-,-] \;\colon\; \mathfrak{g} \otimes_k \mathfrak{g} \longrightarrow \mathfrak{g}
   $$

   of super vector spaces (the _super Lie bracket_)

such that

1. the bracket is skew-symmetric in that the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       \mathfrak{g} \otimes_k \mathfrak{g}
         &
           \overset{\tau^{super}_{\mathfrak{g},\mathfrak{g}}}{\longrightarrow}
         &
       \mathfrak{g} \otimes_k \mathfrak{g}
       \\
       {}^{\mathllap{[-,-]}}\downarrow && \downarrow^{\mathrlap{[-,-]}}
       \\
       \mathfrak{g} &\underset{-1}{\longrightarrow}& \mathfrak{g}
     }
   $$

   (here $\tau^{super}$ is the [[braiding]] [[natural isomorphism]] in the category of [[super vector spaces]])

1. the [[Jacobi identity]] holds in that the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       \mathfrak{g} \otimes_k \mathfrak{g} \otimes_k \mathfrak{g}
       &&
         \overset{\tau^{super}_{\mathfrak{g}, \mathfrak{g}} \otimes_k id }{\longrightarrow}
       &&
       \mathfrak{g} \otimes_k \mathfrak{g} \otimes_k \mathfrak{g}
       \\
       & {}_{\mathllap{\left[-,\left[-,-\right]\right]} - \left[\left[-,-\right],-\right] }\searrow && \swarrow_{\mathrlap{\left[-,\left[-,-\right]\right]}}
       \\
       && \mathfrak{g}
     }
     \,.
   $$

=--




### As super-graded Lie algebras


Externally this means the following:

+-- {: .num_prop #SuperLieAlgebraTraditional}
###### Proposition

A [[super Lie algebra]] according to def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces} is equivalently

1. a $\mathbb{Z}/2$-[[graded vector space]] $\mathfrak{g}_{even} \oplus \mathfrak{g}_{odd}$;

1. equipped with a [[bilinear map]] (the _super Lie bracket_)

   $$
     [-,-] : \mathfrak{g}\otimes_k \mathfrak{g} \to \mathfrak{g}
   $$

   which is _graded_ skew-symmetric: for $x,y \in \mathfrak{g}$ two elements of homogeneous degree $\sigma_x$, $\sigma_y$, respectively, then

   $$
     [x,y] = -(-1)^{\sigma_x \sigma_y} [y,x]
     \,,
   $$

1. that satisfies the $\mathbb{Z}/2$-graded [[Jacobi identity]] in that
for any three elements $x,y,z \in \mathfrak{g}$ of homogeneous super-degree $\sigma_x,\sigma_y,\sigma_z\in \mathbb{Z}_2$ then

   \[
     \label{GradedJacobiIdentity}
     [x, [y, z] ] = [ [x,y],z] + (-1)^{\sigma_x \cdot \sigma_y} [y, [x,z] ]
     \,.
   \]

A [[homomorphism]] of super Lie algebras is a homomorphisms of the underlying [[super vector spaces]]
which preserves the Lie bracket. We write

$$
  sLieAlg
$$

for the resulting [[category]] of super Lie algebras.

=--


### As formal duals of a Chevalley-Eilenberg super-algebras

+-- {: .num_defn #CEAlgebraofSuperLieAlgebra}
###### Definition

For $\mathfrak{g}$ a [[super Lie algebra]] of [[finite number|finite]] [[dimension]], then its _[[Chevalley-Eilenberg algebra]]_ $CE(\mathfrak{g})$ is the super-[[Grassmann algebra]] on the [[dual vector space|dual]] super vector space

$$
  \wedge^\bullet  \mathfrak{g}^\ast
$$

equipped with a [[differential]] $d_{\mathfrak{g}}$ that on generators is the linear dual of the super Lie bracket

$$
  d_{\mathfrak{g}} \;\coloneqq\; [-,-]^\ast \;\colon\; \mathfrak{g}^\ast \to \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
$$

and which is extended to $\wedge^\bullet \mathfrak{g}^\ast$ by the graded Leibniz rule (i.e. as a graded [[derivation]]).

$\,$

Here all elements are $(\mathbb{Z} \times \mathbb{Z}/2)$-bigraded, the first being the _cohomological grading_ $n$ in $\wedge^\n \mathfrak{g}^\ast$, the second being the _super-grading_ $\sigma$ (even/odd).

For $\alpha_i \in CE(\mathfrak{g})$ two elements of homogeneous bi-degree $(n_i, \sigma_i)$, respectively,
the [[signs in supergeometry|sign rule]] is

$$
  \alpha_1 \wedge \alpha_2 = (-1)^{n_1 n_2} (-1)^{\sigma_1 \sigma_2}\; \alpha_2 \wedge \alpha_1
  \,.
$$

(See at _[[signs in supergeometry]]_ for discussion of this sign rule and of an alternative sign rule that is also in use. )

=--

We may think of $CE(\mathfrak{g})$ equivalently as the [[dg-algebra]] of [[invariant differential form|left-invariant]]
[[super differential forms]] on the [[Lie theory|corresponding]] simply connected [[super Lie group]] .


The concept of [[Chevalley-Eilenberg algebras]] is traditionally introduced as a means to define
[[Lie algebra cohomology]]:

+-- {: .num_defn #SuperLieAlgebraCohomology}
###### Definition

Given a [[super Lie algebra]] $\mathfrak{g}$, then

1. an _$n$-cocycle_ on $\mathfrak{g}$ (with [[coefficients]] in $\mathbb{R}$) is an element of degree $(n,even)$ in its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ (def. \ref{CEAlgebraofSuperLieAlgebra}) which is $d_{\mathbb{g}}$ closed.

1. the cocycle is non-trivial if it is not $d_{\mathfrak{g}}$-exact

1. hene the _super-[[Lie algebra cohomology]]_ of $\mathfrak{g}$ (with [[coefficients]] in $\mathbb{R}$) is the [[cochain cohomology]] of its [[Chevalley-Eilenberg algebra]]

   $$
     H^\bullet(\mathfrak{g}, \mathbb{R}) = H^\bullet(CE(\mathfrak{g}))
     \,.
   $$

=--



The following says that the [[Chevalley-Eilenberg algebra]] is an equivalent incarnation of the [[super Lie algebra]]:

+-- {: .num_prop}
###### Proposition

The functor

$$
  CE \;\colon\; sLieAlg^{fin}  \hookrightarrow dgAlg^{op}
$$

that sends a finite dimensional [[super Lie algebra]] $\mathfrak{g}$ to its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$
(def. \ref{CEAlgebraofSuperLieAlgebra}) is a [[fully faithful functor]] which hence exibits [[super Lie algebras]]
as a [[full subcategory]] of the [[opposite category]] of [[differential-graded algebras]].

=--


### As super-representable Lie algebras in the topos over superpoints
 {#AsSuperRepresentableLieAlgebrasOverSuperpoints}



Equivalently, a super Lie algebra is a "super-representable" [[Lie algebra object]] [[internalization|internal]] to the [[cohesive (∞,1)-topos]] [[Super∞Grpd]] over the site of [[super points]] ([Sachse 08, Section 3.2, towards cor. 3.3](#Sachse08)). 

See the discussion at [[superalgebra]] for details on this.



## Properties

### Classification
 {#Classification}

([Kac 77a](Kac77a), [Kac 77b](#Kac77b)) states a classification of super Lie algebras which are

1. finite dimensional

1. simple

1. over a [[field]] of [[characteristic zero]].

Such an algebra is called of _classical type_ if the [[action]] of its even-degree part on the odd-degree part is completely reducible. Those simple finite dimensional algebras not of classical type are of _Cartan type_.

1. classical type

   1. four infinite series
 
      1. $A(m,n)$

      1. $B(m,n) = $ [[osp]]$(2m+1,2n)$ $m\geq 0$, $n \gt 0$

      1. $C(n)$

      1. $D(m,n) = $[[osp]]$(2m,2n)$ $m \geq 2$, $n \gt 0$

   1. two exceptional ones

      1. $F(4)$

      1. [[G(3)]]

   1. a family $D(2,1;\alpha)$ of deformations of $D(2,1)$

   1. two "strange" series

      1. $P(n)$

      1. $Q(n)$

1. Cartan type

   (...)


The underlying even-graded [[Lie algebra]] for type 2 is as follows

| $\mathfrak{g}$ |  $\mathfrak{g}_{even}$  |  $\mathfrak{g}_{even}$ rep on $\mathfrak{g}_{odd}$ |
|----------------|-------------------------|------------------|
| $B(m,n)$  | $B_m \oplus C_n$  | vector $\otimes$ vector |
| $D(m,n)$  | $D_m \oplus C_n$  | vector $\otimes$ vector |
| $D(2,1,\alpha)$ |  $A_1 \oplus A_1 \oplus A_1$ | vector $\otimes$ vector $\otimes$ vector |
| $F(4)$ | $B_3\otimes A_1$ | spinor $\otimes$ vector |
| $G(3)$ | $G_2\oplus A_1$ | spinor $\otimes$ vector |
| $Q(n)$ | $A_n$ | adjoint |


For type 1 the $\mathbb{Z}/2\mathbb{Z}$-grading lifts to an $\mathbb{Z}$-grading with $\mathfrak{g} = \mathfrak{g}_{-1}\oplus \mathfrak{g}_0 \oplus \mathfrak{g}_1$. 

| $\mathfrak{g}$ |  $\mathfrak{g}_{even}$  |  $\mathfrak{g}_{even}$ rep on $\mathfrak{g}_{{-1}}$ |
|----------------|-------------------------|------------------|
| $A(m,n)$ |  $A_m \oplus A_n \oplus \mathbb{C}$ | vector $\otimes$ vector $\otimes$ $\mathbb{C}$ |
| $A(m,m)$ | $A_m \oplus A_m$ | vector $\otimes$ vector |
| $C(n)$ | $C_{n-1} \oplus \mathbb{C}$ | vector $\otimes$ $\mathbb{C}$ |

reviewed e.g. in ([Farmer 84, p. 25,26](#Farmer84), [Minwalla 98, section 4.1](#Minwalla98)).


### Relation to dg-Lie algebras
 {#RelationToDGLieAlgebras}

A [[dg-Lie algebra]] $(\mathfrak{g}, \partial, [-,-])$ may be understood equivalently as a [[super Lie algebra]] 

$$
  (\mathfrak{g} = \mathfrak{g}_{even} \oplus \mathfrak{g}_{odd}, [-,-,])
$$ 

equipped with 

1. a [[lift]] of the $\mathbb{Z}_2$-[[graded vector space|grading]] of the underlying [[vector space]] to a $\mathbb{Z}$[-graded vector space](graded+vector+space#SpecialCaseOfZGradedVectorSpaces) through the projection $\mathbb{Z} \to \mathbb{Z}/2\mathbb{Z} = \mathbb{Z}_2$, hence

   $$
     \mathfrak{g}_{even}
     \;\simeq\;
     \underset{n }{\oplus} \mathfrak{g}_{2n}
     \,,
     \phantom{AAA}
     \mathfrak{g}_{odd}
     \;\simeq\;
     \underset{n }{\oplus} \mathfrak{g}_{2n+1}
   $$

   such that 

   $$
     [-,-] \;\colon\; \mathfrak{g}_{n_1} \otimes \mathfrak{g}_{n_2} \longrightarrow \mathfrak{g}_{n_1 + n_2}
   $$

1. an element $Q \in \mathfrak{g}_{-1}$  

   such that 

   \[
     \label{NilpotencyOfQ}
      [Q,Q] = 0
   \]

(See also at "[[NQ-supermanifold]]".)

Given this, define the [[differential]] to be the [[adjoint action]] by $Q$:

$$
  \partial \;\coloneqq\; [Q,-]
  \,.
$$

That this differential squares to 0 follows by the super-Jacobi identity (eq:GradedJacobiIdentity) and by the nilpotency (eq:NilpotencyOfQ):

$$
  [Q,[Q,-] ]
  \;=\;
  [ \underset{= 0}{\underbrace{[Q,Q]}}, -  ] - [  Q, [Q, -]  ]
  \phantom{AA}
  \Rightarrow
  \phantom{AA}
  [ Q,[Q,-] ] = 0
$$

and the [[derivation]]-property of the differential over the bracket follows again with the super Jacobi identity (eq:GradedJacobiIdentity):

$$
  [Q,[x,y] ]
  \;=\;
  [ [Q,x],y]
  + (-1)^{deg(x)} [x, [Q,y] ]
  \,.
$$






## Examples
 {#Examples}

### Basic examples

Some obvious but important classes of examples are the following:

+-- {: .num_example #SuperVectorSpaceAsAbelianSuperLieAlgebra}
###### Example

every $\mathbb{Z}/2$-[[graded vector space]] $V$ becomes a
[[super Lie algebra]]
(def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}, prop. \ref{SuperLieAlgebraTraditional})
by taking the super Lie bracket to be the [[zero morphism|zero map]]

$$
  [-,-] = 0
  \,.
$$

These may be called the "abelian" super Lie algebras.

=--


+-- {: .num_example #OrdinaryLieAlgebraAsSuperLieAlgebra}
###### Example

Every ordinary [[Lie algebras]] becomes a [[super Lie algebra]]
(def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}, prop. \ref{SuperLieAlgebraTraditional})
concentrated in even degrees. This constitutes a [[fully faithful functor]]

$$
  LieAlg \hookrightarrow sLieAlg
  \,.
$$

which is a  [[coreflective subcategory]] inclusion in that it has a [[left adjoint]]

$$
  LieAlg
    \underoverset
     {\underset{ \overset{ \rightsquigarrow}{(-)} }{\longleftarrow}}
     {\hookrightarrow}
     {\bot}
  sLieAlg
$$

given on the underlying super vector spaces by restriction to the even graded part

$$
  \overset{\rightsquigarrow}{\mathfrak{s}} = \mathfrak{s}_{even}
  \,.
$$

=--


### Super-Poincaré super Lie algebras (supersymmetry)

* The [[super Poincaré Lie algebra]] and various of its polyvector extension are super-extension of the ordinary [[Poincare Lie algebra]]. These are the [[supersymmetry algebras]] in the strict original sense of the word.  For more on this see at _[[geometry of physics -- supersymmetry]]_.

* [[super q-Schur algebra]]

* For every [[connected topological space]], the [[Whitehead product]] makes its [[homotopy groups]] into a super Lie algebra over the [[ring]] of [[integers]] -- the [Whitehead super Lie algebra](Whitehead+product#SuperLieAlgebraStructure).

* higher super Lie algebras

  Just as [[Lie algebras]] are [[vertical categorification|categorified]] to [[L-infinity algebra]]s and [[L-infinity algebroid]]s, so super Lie algebras categorifie to [[super L-infinity algebra]]s.  A secretly famous example is the

  * [[supergravity Lie 3-algebra]], [[supergravity Lie 6-algebra]]



### Embedding tensors and tensor hierarchy
 {#SuperLieAlgebraInducedFromVectorSpace}

The following example is highlighted in [Palmkvist 13, 3.1](tensor+hierarchy#Palmkvist13) (reviewed more clearly in [Lavau-Palmkvist 19, 2.4](tensor+hierarchy#LavauPalmkvist19)) where it is attributed to I. L. Kantor (1970).

+-- {: .num_defn #TheSuperLieAlgebraInducedFromVectorSpace}
###### Definition

Let $V$ be a [[finite-dimensional vector space]] over some [[ground field]] $k$.

Define a $\mathbb{Z}$-[[graded vector space]] 

$$
  \widehat V \;\in \; Vect_k^{\mathbb{Z}}
  \,,
$$

concentrated in degrees $\leq 1$, [[recursion|recursively]] as follows:

For $n =1$ we set

$$
  \widehat V_{1}
  \;\coloneqq\;
  V
  \,.
$$

For $n \leq 0 \in \mathbb{Z}$, the component space in degree $n-1$ is taken to be the vector space of [[linear maps]] from $V$ to the component space in degree $n$:

$$
  \widehat V_{n-1}
  \;\coloneqq\;
  Hom_k( V, \widehat V_n )
  \,.
$$

Hence:

\[
  \label{ExplicitComponentSpacesOfSuperLieAlgebraInducedFromVectorSpace}
  \begin{aligned}
    \widehat V_1 & = V
    \\
    \widehat V_0 & = Hom_k(V,V) = \mathfrak{gl}(V)
    \\
    \widehat V_{-1} & =  Hom_k(V, Hom_k(V,V)) \simeq  Hom_k(V \otimes V, V)
    \\
    \widehat V_{-2} & = Hom_k(V, Hom_k(V, Hom_k(V,V))) \simeq  Hom_k(V \otimes V \otimes V, V)
    \\
    \vdots
  \end{aligned}
\]

Consider then the [[direct sum]] of these component spaces as a [[super vector space]] with the [[even number]]/[[odd number]]-degrees being in super-even/super-odd degree, respectively.

On this [[super vector  space]] consider a [[super Lie bracket]] defined [[recursion|recusively]] as follows:

For all $v_1, v_2 \in \widehat V_1 = V$ we set

$$
  [v_1, v_2] \;=\; 0
  \,.
$$

For $f \in \widehat V_{n \leq 0}$ and $v \in \widehat V_1 = V$ we set

\[
  \label{SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace}
  [f, v]
  \;\coloneqq\;
  f(v)
\]

Finally, for $f\in \widehat V_{ deg(f) \leq 0 }$ and $g\in \widehat V_{deg(g) \leq 0}$ we set

\[
  \label{SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace}
  \begin{aligned}
  [f, g]
  &
  \colon\;
  v 
  \;\mapsto\;
  [f, g(v)]
  -
  (-1)^{
    deg(f) deg(g)
  }
  [ g, f(v) ]
  \\
  \end{aligned}
\]

=--

+-- {: .num_remark #ConstraintsOnBracketInSuperLieAlgebraInducedByVectorSpace}
###### Remark

By (eq:SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace) the definition (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) is equivalent to

$$
  [ [f,g],v ]
  \;=\;
  [f, [g,v] ]
  -
  (-1)^{
    deg(f) deg(g)
  }
  [ g, [f,v] ]
$$


Hence (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) is already implied by (eq:SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace) if the bracket is to satisfy the super Jacobi identity (eq:GradedJacobiIdentity).

=--

It remains to show that:

+-- {: .num_prop #SuperJacobiForSuperLieAlgebraInducedFromVectorSpace}
###### Proposition

Def. \ref{TheSuperLieAlgebraInducedFromVectorSpace} indeed gives a [[super Lie algebra]] in that the bracket (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) satisfies the super Jacobi identity (eq:GradedJacobiIdentity).

=--

+-- {: .proof}
###### Proof

We proceed by [[induction]]:

By Remark \ref{ConstraintsOnBracketInSuperLieAlgebraInducedByVectorSpace} we have that the super Jacobi identity holds for for all [[triples]] $f_1, f_2, f_3 \in \widehat{V}$ with $deg(f_3) \geq 0$.

Now assume that the super Jacobi identity has been shown for triples $(f_1, f_2, f_3(v))$ and $(f_1, f_3, f_2(v))$, for any $v \in V$. The following computation shows that then it holds for $(f_1, f_2, f_3)$:

$$
  \begin{aligned}
    [f_1, [f_2, f_3] ] (v)
    & 
    =
    [ f_1,  [f_2, f_3](v) ] 
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    [  [ f_2, f_3 ], f_1(v)  ]
    \\
    & =
    [ f_1,  [  f_2, f_3(v) ] ] 
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_2)deg(f_3)}
    [ f_1,  [  f_3, f_2(v) ] ] 
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    [  f_2,  [ f_3,  f_1(v) ] ]
    \\
    & \phantom{=}
    +    
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3)) + deg(f_2)deg(f_3)}
    [  f_3,  [ f_2,  f_1(v) ] ]
    \\
    & = 
    [ f_1,  [  f_2, f_3(v) ] ] 
    -
    (-1)^{deg(f_1) deg(f_2)}
    {
    \color{green}
    [ f_2,  [  f_1, f_3(v) ] ] 
    }
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_2) deg(f_3)}
    \big(
    [ f_1,  [  f_3, f_2(v) ] ] 
    -
    (-1)^{deg(f_1) deg(f_3)}
    {
    \color{orange}
    [ f_3,  [  f_1, f_2(v) ] ] 
    }
    \big)
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    \big(
    [  f_2,  [ f_3,  f_1(v) ] ]
    -
    (-1)^{deg(f_1)deg(f_3)}
    {
    \color{blue}
    [  f_2,  [ f_1,  f_3(v) ] ]   
    }
    \big)
    \\
    & \phantom{=}
    +    
    (-1)^{deg(f_1) deg(f_2 ) + deg(f_1) deg(f_3) + deg(f_2) deg(f_3)}
    \big(
    [  f_3,  [ f_2,  f_1(v) ] ]
    -
    (-1)^{deg(f_1) deg(f_2)}
    {
    \color{cyan}
    [  f_3,  [ f_1,  f_2(c) ] ]
    }
    \big)
    \\
    & \phantom{=}
    +
    (-1)^{deg(f_1) deg(f_2)}
    \big(
    \underset{
      = 0
    }{
    \underbrace{
    +
    {
    \color{green}
    [ f_2,  [  f_1, f_3(v) ] ] 
    }
    -
    {
    \color{blue}
    [  f_2,  [ f_1,  f_3(v) ] ]
    }
    }
    }
    \big)
    \\
    & \phantom{=}
    +
    (-1)^{deg(f_1) deg(f_3) + deg(f_2) deg(f_3)}
    \big(
    \underset{
      = 0
    }{
    \underbrace{
    {
    \color{orange}
    [  f_3,  [ f_1,  f_2(v) ] ]
    }
    -
    {
    \color{cyan}
    [ f_3,  [  f_1, f_2(v) ] ] 
    }
    }
    }
    \big)
    \\
    & =
    \big[
      [f_1, f_2], f_3(v)
    \big]   
    \\
    & \phantom{=}
    -
    (-1)^{ deg(f_2) deg(f_3) } 
    \big[
      [f_1, f_3], f_2(c) 
    \big]
    \\
    & \phantom{=}
    +
    (-1)^{ deg(f_1) deg(f_2)  }
    \big[
      f_2, [f_1, f_3](v)
    \big]
    \\
    & \phantom{=}
    -
    (-1)^{ deg(f_3)( deg(f_1) + deg(f_2) ) } 
    \big[
      f_3, [f_1, f_2](v) 
    \big]
    \\
    & =
    \big[
     [f_1, f_2], f_3
    \big](v)
    +
    (-1)^{deg(f_1)deg(f_2))}
    \big[
      f_2, [f_1, f_3]
    \big](v)
  \end{aligned}
$$

> (Fine, but is this sufficient to induct over the full range of all three degrees?)

=--


+-- {: .num_example #LieBracketOnglInsideSuperLieAlgebraInducedFromVectorSpace}
###### Example

For $f,g \in \widehat V_0 = Hom_k(V,V)$ (eq:ExplicitComponentSpacesOfSuperLieAlgebraInducedFromVectorSpace) we have that the bracket on $\widehat V$ in Def. \ref{SuperLieAlgebraInducedFromVectorSpace} restricts to

$$
  [f,g](v)
  \;=\;
  [f,g(v)] - [g,f(v)]
  \;=\;
  f(g(v)) - g(f(v))
$$

(by combining (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) with (eq:SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace)).

This is the [[Lie bracket]] of the [[general linear Lie algebra]] $\mathfrak{gl}(V)$, as indicated on the right in (eq:ExplicitComponentSpacesOfSuperLieAlgebraInducedFromVectorSpace).

=--

+-- {: .num_prop #EmbeddingTensorViaSuperLieAlgebraInducedFromVectorSpace}
###### Proposition
**([[embedding tensors]] are square-0 elements in $\widehat{V}$)**

Let $k$ be a [[ground field]] of [[characteristic zero]].

An element in degree -1 of the [[super Lie algebra]] $\widehat V$ from Def. \ref{SuperLieAlgebraInducedFromVectorSpace}, 

$$
  \Theta \in \widehat V_{-1} \simeq Hom_{k}(V, \mathfrak{gl}(V))
  \,,
$$

which by Example \ref{LieBracketOnglInsideSuperLieAlgebraInducedFromVectorSpace} is identified with a [[linear map]] 

$$
  \Theta \;\colon\; V \longrightarrow \mathfrak{g} \coloneqq \mathfrak{gl}(V)
$$

from $V$ to the [[general linear Lie algebra]] on $V$, is square-0 (eq:NilpotencyOfQ) precisely if it is an _[[embedding tensor]]_, in that:

$$
  [\Theta, \Theta]
  \;=\;
  0
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  [\Theta(v_1), \Theta(v_2) ]
  \;=\;
  \Theta( \rho_{\Theta(v)1)}(v_2) )
  \,.
$$

Here on the right, $[-,-]$ denotes the [[Lie bracket]] in $\mathfrak{gl}(V)$, while $\rho$ denotes the canonical [[Lie algebra action]] of $\mathfrak{gl}(V)$ on $V$.

=--

+-- {: .proof}
###### Proof

By unwinding of the definition (eq:SuperLieBracketOnDegree0InSuperLieAlgebraInducedFromVectorSpace) and (eq:SuperLieBracketInSuperLieAlgebraInducedFromVectorSpace) and using again Example \ref{LieBracketOnglInsideSuperLieAlgebraInducedFromVectorSpace} we compute as follows:

$$
  \begin{aligned}
    \big( \tfrac{1}{2} [Q,Q](v_1) \big)(v_2)
    & =
    [Q, Q(v_1)](v_2)
    \\
    & =
    [Q, 
      \underset{
        \mathclap{
          = \rho_{\Theta(v_1)}(v_2)   
        }
      }
      {
        \underbrace{
          (Q(v_1))(v_2)
        }
      }
    ] 
    - 
    [Q(v_1), Q(v_2)]
    \\
    & =
    \Theta( \rho_{\Theta(v_1)}(v_2) )
    -
    [ \Theta(v_1), \Theta(v) ]
  \end{aligned}
$$


=--

+-- {: .num_prop #EmbeddingTensorsInduceTensorHierarchies}
###### Remark
**([[embedding tensors]] induce [[tensor hierarchies]])**

In view of the relation between [[super Lie algebras]] and [[dg-Lie algebras]] ([above](#RelationToDGLieAlgebras)), Prop. \ref{EmbeddingTensorViaSuperLieAlgebraInducedFromVectorSpace} says that every choice of an [[embedding tensor]] for a [[faithful representation]] on a [[vector space]] $V$ induces a [[dg-Lie algebra]] 
$(\widehat V, [-,-], \partial \coloneqq [\Theta, -])$.

According to [Palmkvist 13, 3.1](tensor+hierarchy#Palmkvist13), [Lavau-Palmkvist 19, 2.4](tensor+hierarchy#LavauPalmkvist19) this [[dg-Lie algebra]] (or some extension of some sub-algebra of it) is the _[[tensor hierarchy]]_ associated with the embedding tensor.

=--

## Related entries

* [[Haag–Łopuszański–Sohnius theorem]]

* [[geometry of physics -- supersymmetry]]

## References

According to [V. Kac 1977b](#Kac77b) the definition of super Lie algebra is originally due to:

* [[Felix Berezin]], G. I. Kac, Math. Sbornik **82** (1970) 343-351 
  > (in Russian)

See also:

* {#Kantor70} [[Isaiah Kantor]], _Graded Lie algebras_, Trudy Sem. Vektor. Tenzor. Anal 15 (1970): 227-266.

* [[Felix A. Berezin]] (edited by [[Alexandre A. Kirillov]]): *Lie Superalgebras*, chapters I.5 and II.1 in: *Introduction to Superanalysis*, Mathematical Physics and Applied Mathematics **9**, Springer (1987) &lbrack;[doi:10.1007/978-94-017-1963-6_6](https://doi.org/10.1007/978-94-017-1963-6_6), [doi:10.1007/978-94-017-1963-6_7](https://doi.org/10.1007/978-94-017-1963-6_7)&rbrack; 


The original references on the classification of super Lie algebras:

* {#Kac77a} [[Victor Kac]], _Lie superalgebras_, Advances in Math. **26** 1 (1977) 8-96 &lbrack;<a href="https://doi.org/10.1016/0001-8708(77)90017-2">doi:10.1016/0001-8708(77)90017-2</a>&rbrack;

* {#Kac77b} [[Victor Kac]]: *A sketch of Lie superalgebra theory*, Comm. Math. Phys. **53** 1 (1977) 31-64 &lbrack;[euclid:1103900590](https://projecteuclid.org/euclid.cmp/1103900590), [doi:10.1007/BF01609166](https://doi.org/10.1007/BF01609166)&rbrack;

See also:

* [[Werner Nahm]], [[Vladimir Rittenberg]], [[Manfred Scheunert]], *The classification of graded Lie algebras*, Physics Letters B **61** 4 (1976) 383-384 &lbrack;<a href="https://doi.org/10.1016/0370-2693(76)90594-3">doi:10.1016/0370-2693(76)90594-3</a>&rbrack;

* M. Parker, _Classification Of Real Simple Lie Superalgebras Of Classical Type_, J.Math.Phys. 21 (1980) 689-697 ([spire](http://inspirehep.net/record/157627?ln=en))

Further discussion specifically of [classification of supersymmetry](#supersymmetry#Classification):

* {#Nahm78} [[Werner Nahm]], _[[Supersymmetries and their Representations]]_, Nucl. Phys. B **135** (1978) 149 &lbrack;[spire](https://inspirehep.net/record/120988/), [pdf](http://cds.cern.ch/record/132743/files/197709213.pdf)&rbrack;

* {#Shnider88} [[Steven Shnider]], *The superconformal algebra in higher dimensions*, Letters in Mathematical Physics **16** 4 (1988) 377-383 &lbrack;[doi:10.1007/BF00402046](https://doi.org/10.1007/BF00402046)&rbrack;

* [[Victor Kac]], _Classification of supersymmetries_, Proceedings of the ICM, Beijing 2002, vol. 1, 319--344 ([arXiv:math-ph/0302016](http://arxiv.org/abs/math-ph/0302016))

Introductions and surveys:

* [[Vladimir Rittenberg]]: *A guide to Lie superalgebras*, in P. Kramers, A. Rieckers (eds.): *Group Theoretical Methods in Physics*, Lecture Notes in Physics **79** Springer (1978) 3-21 &lbrack;[doi:10.1007/3-540-08848-2_1](https://doi.org/10.1007/3-540-08848-2_1), [[Rittenberg-GuideToLieSuperalgebras.pdf:file]]&rbrack; 

* [[Manfred Scheunert]], *The theory of Lie superalgebras. An introduction*, Lect. Notes Math. **716** (1979) &lbrack;[doi:10.1007/BFb0070929](https://doi.org/10.1007/BFb0070929)&rbrack;
 
* [[Dimitry A. Leites]], *Lie Superalgebras*, J. Soviet Math. **30** (1985) 2481-2512 &lbrack;[doi:10.1007/BF02249121](http://dx.doi.org/10.1007/BF02249121)&rbrack;

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], section II.2 of: _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), toc: [[CDF91-TOC.pdf:file]], chII.2: [[CastellaniDAuriaFre-ChII2.pdf:file]]&rbrack;
  > (with an eye towards [[supergravity]])

* {#Farmer84} Richard J. Farmer, *Orthosymplectic superalgebras in mathematics and science*, PhD Thesis (1984) &lbrack;[eprints:19542](http://eprints.utas.edu.au/19542), [[Farmer-OSpSuperalgebra.pdf:file]]&rbrack;

* Luc Frappat, Antonio Sciarrino, Paul Sorba: *Structure of basic Lie superalgebras and of their affine extensions*, Comm. Math. Phys. **121** 3 (1989) 457-500 &lbrack;[euclid:cmp/1104178142](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-121/issue-3/Structure-of-basic-Lie-superalgebras-and-of-their-affine-extensions/cmp/1104178142.full)&rbrack;

* Luc Frappat, Antonio Sciarrino, Paul Sorba: _Dictionary on Lie Superalgebras_, Academic Press (2000) &lbrack;[arXiv:hep-th/9607161](http://arxiv.org/abs/hep-th/9607161), ISBN:978-0122653407&rbrack;


* Groeger, _Super Lie groups and super Lie algebras_, lecture notes 2011 ([pdf](http://www.mathematik.hu-berlin.de/~groegerj/teaching_files/lecture12.pdf))


* D. Westra, _Superrings and supergroups_ ([pdf](http://www.mat.univie.ac.at/~michor/westra_diss.pdf))

* {#Minwalla98} [[Shiraz Minwalla]], _Restrictions imposed by superconformal invariance on quantum field theories_, Adv. Theor. Math. Phys. **2** (1998) 781 &lbrack;[arXiv:hep-th/9712074](http://arxiv.org/abs/hep-th/9712074)&rbrack;


Discussion in the [[presheaf topos]] over [[superpoints]]:

* {#Sachse08} [[Christoph Sachse]], Section 3 of: _A Categorical Formulation of Superalgebra and Supergeometry_ &lbrack;[arXiv:0802.4067](http://arxiv.org/abs/0802.4067)&rbrack;


Discussion of  [[Lie algebra extensions]] for super Lie algebras includes

* [[Dmitri Alekseevsky]], [[Peter Michor]], Wolfgang Ruppert, _Extensions of super Lie algebras_, J. Lie Theory **15** 1 (2005) 125-134 &lbrack;[arXiv:math/0101190](http://arxiv.org/abs/math/0101190)&rbrack;

On [[Lie algebra weight systems]] arising from [[super Lie algebras]]:

* {#FFKV97} [[José Figueroa-O’Farrill]], [[Takashi Kimura]], [[Arkady Vaintrob]], _The universal Vassiliev invariant for the Lie superalgebra $\mathfrak{gl}(1\vert1)$_, Commun. Math. Phys. 185 (1997) 93-127 ([arXiv:q-alg/9602014](https://arxiv.org/abs/q-alg/9602014))

On [[Lie algebra cohomology]] of [[super Lie algebras]] (see also the [[Green-Schwarz action functional|brane scan]]) in relation to [[integration over supermanifolds|integrable forms]] of coset [[supermanifolds]]:

* [[Roberto Catenacci]], [[C. A. Cremonini]], [[Pietro Antonio Grassi]], [[Simone Noja]], _Cohomology of Lie Superalgebras: Forms, Integral Forms and Coset Superspaces_ ([arXiv:2012.05246](https://arxiv.org/abs/2012.05246))


[[!redirects super Lie algebras]]

[[!redirects Lie superalgebra]]
[[!redirects Lie superalgebras]]

[[!redirects super Lie bracket]]
[[!redirects super Lie brackets]]

[[!redirects super-Lie algebra]]
[[!redirects super-Lie algebras]]



