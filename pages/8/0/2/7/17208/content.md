
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Complex projective space $\mathbb{C}P^n$ is the [[projective space]] $\mathbb{A}P^n$ for $\mathbb{A} = \mathbb{C}$ being the [[complex numbers]] (and for $n \in \mathbb{N}$), a [[complex manifold]] of complex [[dimension]] $n$ (real dimension $2n$). Equivalently, this is the complex [[Grassmannian]] $Gr_1(\mathbb{C}^{n+1})$. For the special case $n = 1$ then $\mathbb{C}P^1 \simeq S^2$ is the [[Riemann sphere]].

As $n$ ranges, there are natural inclusions

$$
  \ast = \mathbb{C}P^0 
    \hookrightarrow 
  \mathbb{C}P^1 
    \hookrightarrow 
  \mathbb{C}P^2
    \hookrightarrow
  \mathbb{C}P^3
    \hookrightarrow
  \cdots
  \,.
$$

The [[sequential colimit]] over this sequence is the infinite complex projective space $\mathbb{C}P^\infty$. This is a model for the [[classifying space]] $B U(1)$ of [[circle principal bundles]]/[[complex line bundles]] (an [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$).

## Definition

+-- {: .num_defn #ComplexProjectiveSpace}
###### Definition

For $n \in \mathbb{N}$, then **complex $n$-dimensional complex projective space** is the [[complex manifold]] (often just regarded as its underlying [[topological space]]) defined as the [[quotient]]

$$
  \mathbb{C}P^n \coloneqq (\mathbb{C}^{n+1}-\{0\})/_\sim
$$ 

of the [[Cartesian product]] of $(n+1)$-copies of the [[complex plane]], with the origin removed, by the [[equivalence relation]]

$$
  (z \sim w) \Leftrightarrow (z = \kappa \cdot w)
$$

for some $\kappa \in \mathbb{C} - \{0\}$ and using the canonical multiplicative [[action]] of $\mathbb{C}$ on $\mathbb{C}^{n+1}$.

The canonical inclusions

$$
  \mathbb{C}^{n+1} \hookrightarrow \mathbb{C}^{n+2}
$$

induce canonical inclusions

$$
  \mathbb{C}P^n \hookrightarrow \mathbb{C}P^{n+1}
  \,.
$$

The [[sequential colimit]] over this sequence of inclusions is the _infinite complex projective space_

$$
  \mathbb{C}P^\infty
    \coloneqq
  \underset{\longleftarrow}{\lim}_n \mathbb{C}P^n
  \,.
$$
=--

The following equivalent characterizations are immediate but useful:

+-- {: .num_prop #ComplexProjectiveSpaceAsGrassmannian}
###### Proposition

For $n \in \mathbb{N}$ then complex projective space, def. \ref{ComplexProjectiveSpace}, is equivalently the complex [[Grassmannian]]

$$
  \mathbb{C}P^n \simeq Gr_1(\mathbb{C}^{n+1})
  \,.
$$

=--

+-- {: .num_prop #ComplexProjectiveSpaceAsS1Quotient}
###### Proposition

For $n \in \mathbb{N}$ then complex projective space, def. \ref{ComplexProjectiveSpace}, is equivalently 

1. the [[coset]] 

   $$
     \mathbb{C}P^n \simeq U(n+1)/(U(n) \times U(1))
     \,,
   $$

1. the quotient of the [[n-sphere|(2n+1)-sphere]] by the [[circle group]] $S^1 \simeq \{ \kappa  \in \mathbb{C}| {\vert \kappa \vert} = 1\}$

  $$
    \mathbb{C}P^n \simeq S^{2n+1}/S^1
    \,.
  $$

=--

+-- {: .proof}
###### Proof

To see the second characterization from def. \ref{ComplexProjectiveSpace}:

With ${\vert -\vert} \colon \mathbb{C}^{n} \longrightarrow \mathbb{R}$ the standard [[norm]], then every element $\vec z \in \mathbb{C}^{n+1}$ is identified under the defining equivalence relation with 

$$
  \frac{1}{\vert \vec z\vert}\vec z \in S^{2n-1} \hookrightarrow \mathbb{C}^{n+1}
$$

lying on the unit $(2n-1)$-sphere. This fixes the action of $\mathbb{C}-0$ up to a remaining action of complex numbers of unit [[absolute value]]. These form the [[circle group]] $S^1$.

The first characterization follows via prop. \ref{ComplexProjectiveSpaceAsGrassmannian} from the general discusion at _[[Grassmannian]]_. With this the second characterization follows also with the [[coset]] identification of the $(2n+1)$-sphere: $S^{2n+1} \simeq U(n+1)/U(n)$ ([exmpl.](unitary+group#nSphereAsUnitaryCosetSpace)).

=--


## Properties

### Cell structure

+-- {: .num_prop #CellComplexStructureOnComplexProjectiveSpace}
###### Proposition

There is a [[CW-complex]] structure on complex projective space $\mathbb{C}P^n$ (def. \ref{ComplexProjectiveSpace}) for $n \in \mathbb{N}$, given by [[induction]], where $\mathbb{C}P^{n+1}$ arises from $\mathbb{C}P^n$ by attaching a single cell of dimension $2(n+1)$ with attaching map the [[projection]] $S^{2n+1} \longrightarrow \mathbb{C}P^n$ from prop. \ref{ComplexProjectiveSpaceAsS1Quotient}:

$$
  \array{
     S^{2n+1} &\longrightarrow& S^{2n+1}/S^1 \simeq \mathbb{C}P^n
     \\
     {}^{\mathllap{\iota_{2n+2}}}\downarrow 
       &(po)& \downarrow
     \\
     D^{2n+2} &\longrightarrow& \mathbb{C}P^{n+1}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

Given homogenous coordinates $(z_0, z_1, \cdots, z_n, z_{n+1}, z_{n+2}) \in \mathbb{C}^{n+2}$ for $\mathbb{C}P^{n+1}$, let 

$$
  \phi \coloneqq -arg(z_{n+2})
$$ 

be the [[phase]] of $z_{n+2}$. Then under the equivalence relation defining $\mathbb{C}P^{n+1}$ these coordinates represent the same element as

$$
  \frac{1}{\vert \vec z\vert}(e^{i \phi} z_0, e^{i \phi}z_1,\cdots, e^{i \phi}z_{n+1}, r)
  \,,
$$ 

where 

$$
  r = {\vert z_{n+2}\vert}\in [0,1) \subset \mathbb{C}
$$ 

is the [[absolute value]] of $z_{n+2}$. Representatives $\vec z'$ of this form (${\vert \vec z' \vert = 1}$ and $z'_{n+2} \in [0,1]$) parameterize the [[n-disk|2n+2-disk]] $D^{2n+2}$ ($2n+3$ real parameters subject to the one condition that the sum of their norm squares is unity) with [[boundary]] the $(2n+1)$-sphere at $r = 0$. The only remaining part of the action of $\mathbb{C}-\{0\}$ which fixes the form of these representatives is $S^1$ acting on the elements with $r = 0$ by phase shifts on the $z_0, \cdots, z_{n+1}$. The quotient of this remaining action on $D^{2(n+1)}$ identifies its boundary $S^{2n+1}$-sphere with $\mathbb{C}P^{n}$, by prop. \ref{ComplexProjectiveSpaceAsS1Quotient}.

=--

### Homology and Cohomology 
 {#Cohomology}

#### Ordinary

+-- {: .num_prop #OrdinaryCohomologyOfComplexProjectiveSpace}
###### Proposition

For $A \in $ [[Ab]] any [[abelian group]], then the [[ordinary homology]] [[homology groups|groups]] of complex projective space $\mathbb{C}P^n$ with [[coefficients]] in $A$ are

$$
  H_k(\mathbb{C}P^n,A)\simeq
  \left\{
    \array{
       A & for \; k \;even\; and \; k \leq 2n 
       \\
       0 & otherwise
    }
  \right.
  \,.
$$

Similarly the [[ordinary cohomology]] [[cohomology groups|groups]] of $\mathbb{C}P^n$ is 

$$
  H^k(\mathbb{C}P^n,A)
   \simeq
  \left\{
    \array{
       A & for \; k \;even\; and \; k \leq 2n 
       \\
       0 & otherwise
    }
  \right.
  \,.
$$

Moreover, if $A$ carries the structure of a [[ring]] $R = (A, \cdot)$, then under the [[cup product]] the [[cohomology ring]] of $\mathbb{C}P^n$ is the the [[graded ring]]

$$
  H^\bullet(\mathbb{C}P^n, R)
   \simeq
  R[c_1] / (c_1^{n+1})
$$

which is the [[quotient]] of the [[polynomial ring]] on a single generator $c_1$ in degree 2, by the relation that identifies [[cup products]] of more than $n$-copies of the generator $c_1$ with zero.

Finally, the [[cohomology ring]] of the infinite-dimensional complex projective space is the [[formal power series ring]] in one generator:

$$
  H^\bullet(\mathbb{C}P^\infty, R)
   \simeq
  R[ [ c_1 ] ]
  \,.
$$

(Or else the [[polynomial ring]] $R[c_1]$, depending on how one chooses to extract a ring from a graded ring, see remark \ref{ChoiceOfRingStructureOnGradedCohomologyGroupOfMultiplicativeCohomologyTheory}.)

=--

+-- {: .proof}
###### Proof

First consider the case that the coefficients are the [[integers]] $A = \mathbb{Z}$. 

Since $\mathbb{C}P^n$ admits the structure of a [[CW-complex]] by prop. \ref{CellComplexStructureOnComplexProjectiveSpace}, we may compute its [[ordinary homology]] equivalently as its [[cellular homology]] ([thm.](Introduction+to+Stable+homotopy+theory+--+I#CelluarEquivalentToSingularFromSpectralSequence)). By definition ([defn.](cellular+homology#CellularChainComplex)) this is the [[chain homology]] of the chain complex of [[relative homology]] groups

$$
  \cdots
    \overset{\partial_{cell}}{\longrightarrow}   
  H_{q+2}((\mathbb{C}P^n)_{q+2}, (\mathbb{C}P^n)_{q+1})
   \overset{\partial_{cell}}{\longrightarrow}   
  H_{q+1}((\mathbb{C}P^n)_{q+1}, (\mathbb{C}P^n)_{q})
   \overset{\partial_{cell}}{\longrightarrow}
  H_{q}((\mathbb{C}P^n)_{q}, (\mathbb{C}P^n)_{q-1})
    \overset{\partial_{cell}}{\longrightarrow}   
  \cdots  
  \,,
$$

where $(-)_q$ denotes the $q$th stage of the [[CW-complex]]-structure. Using the CW-complex structure provided by prop. \ref{CellComplexStructureOnComplexProjectiveSpace}, then there are cells only in every second degree, so that 

$$
  (\mathbb{C}P^n)_{2k+1} = (\mathbb{C}P)_{2k}
$$

for all $k \in \mathbb{N}$. It follows that the cellular chain complex has a zero group in every second degree, so that all differentials vanish. Finally, since prop. \ref{CellComplexStructureOnComplexProjectiveSpace} says that $(\mathbb{C}P^n)_{2k+2}$ arises from $(\mathbb{C}P^n)_{2k+1} = (\mathbb{C}P^n)_{2k}$ by attaching a single $2k+2$-cell it follows that (by passage to [[reduced homology]])

$$
  H_{2k}(\mathbb{C}P^n, \mathbb{Z})
    \simeq
  \tilde H_{2k}(S^{2k})((\mathbb{C}P^n)_{2k}/(\mathbb{C}P^n)_{2k-1})
   \simeq
  \tilde H_{2k}(S^{2k})
    \simeq
  \mathbb{Z}
  \,.
$$

This establishes the claim for ordinary homology with integer coefficients.

In particular this means that $H_q(\mathbb{C}P^n, \mathbb{Z})$ is a [[free abelian group]] for all $q$. Since free abelian groups are the [[projective objects]] in [[Ab]] ([prop.](projective+object#ProjectiveObjectsInAbAreFreeGroups)) it follows (with the discussion at _[[derived functors in homological algebra]]_) that the [[Ext]]-groups vanishe:

$$
  Ext^1(H_q(\mathbb{C}P^n, \mathbb{Z}),A) = 0
$$

and the [[Tor]]-groups vanishes:

$$
 Tor_1(H_q(\mathbb{C}P^n), A) = 0
  \,.
$$

With this, the statement about homology and cohomology groups with general coefficients follows with the [[universal coefficient theorem]] for ordinary homology ([thm.](universal+coefficient+theorem#TheoremInOrdinaryHomology)) and for ordinary cohomology ([thm.](universal+coefficient+theorem#OrdinaryStatementInCohomology)).

Finally to see the action of the [[cup product]]: by definition this is the composite

$$
  \cup
  \;\colon\;
  H^\bullet(\mathbb{C}P^n, R)
  \otimes
  H^\bullet(\mathbb{C}P^n, R)
    \longrightarrow
  H^\bullet(\mathbb{C}P^n \times \mathbb{C}P^n , R)
    \overset{\Delta^\ast}{\longrightarrow}
  H^\bullet(\mathbb{C}P^n,R)
$$

of the "cross-product" map that appears in the [[Kunneth theorem]], and the pullback along the [[diagonal]] $\Delta\colon \mathbb{C}P^n \to \mathbb{C}P^n \times \mathbb{C}P^n$.

Since, by the above, the groups $H^{2k}(\mathbb{C}P^n,R) \simeq R[2k]$ and $H^{2k+1}(\mathbb{C}P^n,R) = 0$ are free and finitely generated, the [[Kunneth theorem]] in ordinary cohomology applies ([prop.](K&#252;nneth+theorem#KunnethInOrdinaryCohomology)) and says that the cross-product map above is an isomorphism. This shows that under cup product pairs of generators are sent to a generator, and so the statement $H^\bullet(\mathbb{C}P^n , R)\simeq R[c_1](c_1^{n+1})$ follows.

This also implies that the projection maps

$$
  H^\bullet((\mathbb{C}P^\infty)_{2n+2}, R)
  = 
  H^\bullet(\mathbb{C}P^{n+1}, R) 
  \to 
  H^\bullet(\mathbb{C}P^{n+}, R) 
  =
  H^\bullet((\mathbb{C}P^\infty)_{2n}, R)
$$

are all [[epimorphisms]]. Therefore this sequence satisfies the [[Mittag-Leffler condition]] ([def.](lim1#MittagLefflerCondition), [exmpl.](lim1#MittagLefflerSatisfiedInParticularForTowerOfSurjections)) and therefore the [[Milnor exact sequence]] for cohomology ([prop.](lim1#MilorSequenceForReducedCohomologyOnCWComplex)) implies the last claim to be proven:

$$
  \begin{aligned}
    H^\bullet(\mathbb{C}P^\infty, R)
    \\
    & 
     \simeq 
    H^\bullet( \underset{\longleftarrow}{\lim}_n \mathbb{C}P^n , R)
   \\
    &\simeq \underset{\longrightarrow}{\lim}_n H^\bullet(\mathbb{C}P^n, R)
   \\
   &\simeq \underset{\longrightarrow}{\lim}_n ( R [c_1^E] / ((c_1)^{n+1})  )
   \\
   & \simeq R[ [ c_1 ] ]
   \,,
  \end{aligned}
$$

where the last step is [this prop.](formal+scheme#FormalPowerSeries).

=--

+-- {: .num_remark #ChoiceOfRingStructureOnGradedCohomologyGroupOfMultiplicativeCohomologyTheory}
###### Remark

There is in general a choice to be made in interpreting the [[cohomology groups]] of a [[multiplicative cohomology theory]] $E$ as a [[ring]]:

a priori $E^\bullet(X)$ is a sequence 

$$
  \{E^n(X)\}_{n \in \mathbb{Z}}
$$

of [[abelian groups]], together with a system of group homomorphisms

$$
  E^{n_1}(X) \otimes E^{n_2}(X)
    \longrightarrow
  E^{n_1 + n_2}(X)
  \,,
$$

one for each pair $(n_1,n_2) \in \mathbb{Z}\times\mathbb{Z}$.

In turning this into a single [[ring]] by forming [[formal sums]] of elements in the groups $E^n(X)$, there is in general the choice of whether allowing formal sums of only finitely many elements, or allowing arbitrary formal sums.

In the former case the ring obtained is the [[direct sum]]

$$
  \oplus_{n \in \mathbb{N}} E^n(X)
$$

while in the latter case it is the [[Cartesian product]]

$$
  \prod_{n \in \mathbb{N}} E^n (X)
  \,.
$$

These differ in general. For instance if $E$ is [[ordinary cohomology]] with [[integer]] [[coefficients]] and $X$ is complex projective space $\mathbb{C}P^\infty$, then (prop. \ref{OrdinaryCohomologyOfComplexProjectiveSpace})

$$
  E^n(X)
  =
  \left\{
    \array{
      \mathbb{Z} & n \; even
      \\
      0 & otherwise
    }
  \right.
$$

and the product operation is given by

$$
  E^{2{n_1}}(X)\otimes E^{2 n_2}(X)
    \longrightarrow
  E^{2(n_1 + n_2)}(X)
$$

for all $n_1, n_2$ (and zero in odd degrees, necessarily).  Now taking the [[direct sum]] of these, this is the [[polynomial ring]] on one generator (in degree 2)

$$
  \oplus_{n \in \mathbb{N}} E^n(X) \;\simeq\; \mathbb{Z}[c_1]
  \,.
$$

But taking the [[Cartesian product]], then this is the [[formal power series ring]]

$$
  \prod_{n \in \mathbb{N}} E^n(X) \;\simeq\; \mathbb{Z} [ [ c_1 ] ]
  \,.
$$

A priori both of these are sensible choices. The former is the usual choice in traditional [[algebraic topology]]. However, from the point of view of regarding [[ordinary cohomology]] theory as a [[multiplicative cohomology theory]] right away, then the second perspective tends to be more natural: 

The cohomology of $\mathbb{C}P^\infty$ is naturally computed as the [[inverse limit]] of the cohomolgies of the $\mathbb{C}P^n$, each of which unambiguously has the ring structure $\mathbb{Z}[c_1]/((c_1)^{n+1})$. So we may naturally take the limit in the [[category]] of [[commutative rings]] right away, instead of first taking it in $\mathbb{Z}$-indexed sequences of abelian groups, and then looking for ring structure on the result. But the limit taken in the category of rings gives the [[formal power series ring]] (see [here](formal+scheme#FormalPowerSeries)).

Incidentally, this is the default choice of ring structure for [[generalized (Eilenberg-Steenrod) cohomology|generalized]] [[multiplicative cohomology theories]] evaluated on $\mathbb{C}P^\infty$. In particular in [[complex oriented cohomology]] (see there) this choice is of paramount importance.

See also for instance remark 1.1. in [[Jacob Lurie]]: _[[A Survey of Elliptic Cohomology]]_.


=--


#### Complex-oriented

+-- {: .num_prop #CohomologyRingOfBU1ForComplexOrientedCohomologyTheory}
###### Proposition

Given a [[complex oriented cohomology theory]] $(E^\bullet, c^E_1)$ ([defn.](complex+oriented+cohomology+theory#ComplexOrientedCohomologyTheory)), then there is an [[isomorphism]] of [[graded rings]] 

$$
  E^\bullet(\mathbb{C}P^\infty) \simeq E^\bullet(\ast)[ [ c_1^E ] ]
$$

between the $E$-[[cohomology ring]] of infinite-dimensional complex projective space and the [[formal power series]] in one generator of even degree over the $E$-[[cohomology ring]] of the point.


=--

+-- {: .proof}
###### Proof

Using the [[CW-complex]]-structure on $\mathbb{C}P^\infty$ from prop. \ref{CellComplexStructureOnComplexProjectiveSpace}, given by inductively identifying $\mathbb{C}P^{n+1}$ with the result of attaching a single $2n$-cell to $\mathbb{C}P^n$. With this structure, the unique 2-cell inclusion $i \;\colon\; S^2 \hookrightarrow \mathbb{C}P^\infty$ is identified with the canonical map $S^2 \to B U(1)$.

Then consider the [[Atiyah-Hirzebruch spectral sequence]] for the $E$-cohomology of $\mathbb{C}P^n$. 

$$
  H^\bullet(\mathbb{C}P^n, E^\bullet(\ast))
  \;\Rightarrow\;
  E^\bullet(\mathbb{C}P^n)
  \,.
$$

Since, by prop. \ref{OrdinaryCohomologyOfComplexProjectiveSpace}, the [[ordinary cohomology]] with [[integer]] [[coefficients]] of projective space is 

$$
  H^\bullet(\mathbb{C}P^n, \mathbb{Z}) \simeq \mathbb{Z}[c_1]/((c_1)^{n+1})
  \,,
$$

where $c_1$ represents a unit in $H^2(S^2, \mathbb{Z})\simeq \mathbb{Z}$, and since similarly the [[ordinary homology]] of $\mathbb{C}P^n$ is a [[free abelian group]], hence a [[projective object]] in abelian groups ([prop.](projective+object#ProjectiveObjectsInAbAreFreeGroups)), the [[Ext]]-group vanishes in each degree ($Ext^1(H_n(\mathbb{C}P^n), E^\bullet(\ast)) = 0$) and so the [[universal coefficient theorem]] ([prop.](universal+coefficient+theorem#OrdinaryStatementInCohomology)) gives that the second page of the spectral sequence is

$$
  H^\bullet(\mathbb{C}P^n, E^\bullet(\ast))
  \simeq
  E^\bullet(\ast)[ c_1 ] / (c_1^{n+1})
  \,.
$$

By the standard construction of the [[Atiyah-Hirzebruch spectral sequence]] ([here](Atiyah&#8211;Hirzebruch+spectral+sequence#ConstructionByFilteringTheBaseSpace)) in this identification the element $c_1$ is identified with a generator of the [[relative cohomology]]

$$
  E^2((\mathbb{C}P^n)_2, (\mathbb{C}P^n)_1)
  \simeq
  \tilde E^2(S^2)
$$

(using, by the above, that this $S^2$ is the unique 2-cell of $\mathbb{C}P^n$ in the standard cell model).

This means that $c_1$ is a permanent cocycle of the spectral sequence (in the kernel of all differentials) precisely if it arises via restriction from an element in $E^2(\mathbb{C}P^n)$ and hence precisely if there exists a complex orientation $c_1^E$ on $E$. Since this is the case by assumption on $E$, $c_1$ is a permanent cocycle. (For the fully detailed argument see ([Pedrotti 16](#Pedrotti16)).)

The same argument applied to all elements in $E^\bullet(\ast)[c]$, or else the $E^\bullet(\ast)$-linearity of the differentials ([prop.](multiplicative+cohomology+theory#LinearityOfDifferentialsInSerreAHSSForMultiplicativeCohomologyTheory)), implies that all these elements are permanent cocycles.

Since the AHSS of a multiplicative cohomology theory is a [[multiplicative spectral sequence]] ([prop.](multiplicative+cohomology+theory#AHSSForMultiplicativeCohomologyTheoryIsMultiplicative)) this implies that the differentials in fact vanish on all elements of $E^\bullet(\ast) [c_1] / (c_1^{n+1})$, hence that the given AHSS collapses on the second page to give

$$
  \mathcal{E}_\infty^{\bullet,\bullet}
  \simeq
  E^\bullet(\ast)[ c_1^{E} ] / ((c_1^E)^{n+1})
$$

or in more detail:

$$
  \mathcal{E}_\infty^{p,\bullet}
  \simeq
  \left\{
    \array{
      E^\bullet(\ast) & \text{if}\; p \leq  2n \; and\; even
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

Moreover, since therefore all $\mathcal{E}_\infty^{p,\bullet}$ are [[free modules]] over $E^\bullet(\ast)$, and since the filter stage inclusions $F^{p+1} E^\bullet(X) \hookrightarrow F^{p}E^\bullet(X)$ are $E^\bullet(\ast)$-[[module]] homomorphisms ([prop.](multiplicative+cohomology+theory#RingAndModuleStructureOnCohomologyGroupsOfMultiplicativeCohomplogyTheory)) the [extension problem](spectral+sequence#ExtensionProblem) trivializes, in that all the [[short exact sequences]]

$$
  0 \to F^{p+1}E^{p+\bullet}(X) \longrightarrow F^{p}E^{p+\bullet}(X) \longrightarrow \mathcal{E}_\infty^{p,\bullet} \to 0
$$

[[split exact sequence|split]] (since the [[Ext]]-group $Ext^1_{E^\bullet(\ast)}(\mathcal{E}_\infty^{p,\bullet},-) = 0$ vanishes on the [[free module]], hence [[projective module]] $\mathcal{E}_\infty^{p,\bullet}$).

In conclusion, this gives an isomorphism of graded rings

$$
  E^\bullet(\mathbb{C}P^n)
  \simeq
  \underset{p}{\oplus} \mathcal{E}_\infty^{p,\bullet}
  \simeq
  E^\bullet(\ast)[ c_1 ] / ((c_1^{E})^{n+1})
  \,.
$$

A first consequence is that the projection maps

$$
  E^\bullet((\mathbb{C}P^\infty)_{2n+2})
  = 
  E^\bullet(\mathbb{C}P^{n+1}) 
  \to 
  E^\bullet(\mathbb{C}P^{n+}) 
  =
  E^\bullet((\mathbb{C}P^\infty)_{2n})
$$

are all [[epimorphisms]]. Therefore this sequence satisfies the [[Mittag-Leffler condition]] ([def.](lim1#MittagLefflerCondition), [exmpl.](lim1#MittagLefflerSatisfiedInParticularForTowerOfSurjections)) and therefore the [[Milnor exact sequence]] for generalized cohomology ([prop.](lim1#MilorSequenceForReducedCohomologyOnCWComplex)) finally implies the claim:

$$
  \begin{aligned}
    E^\bullet(B U(1))
     & \simeq
    E^\bullet(\mathbb{C}P^\infty)
    \\
    & \simeq 
    E^\bullet( \underset{\longleftarrow}{\lim}_n \mathbb{C}P^n )
   \\
    &\simeq \underset{\longrightarrow}{\lim}_n E^\bullet(\mathbb{C}P^n)
   \\
   &\simeq \underset{\longrightarrow}{\lim}_n ( E^\bullet(\ast) [c_1^E] / ((c_1^E)^{n+1})  )
   \\
   & \simeq E^\bullet(\ast)[ [ c_1^E ] ]
   \,,
  \end{aligned}
$$

where the last step is [this prop.](formal+scheme#FormalPowerSeries).


=--


## References

* [[Topospaces]], _[Complex projective space](http://topospaces.subwiki.org/wiki/Complex_projective_space)_

* Wikipedia, _[Complex projective space](https://en.wikipedia.org
/wiki/Complex_projective_space)_

For the [[Atiyah-Hirzebruch spectral sequence]] for [[complex oriented cohomology]] of complex projective space see

* {#Pedrotti16} [[Riccardo Pedrotti]], _Complex oriented cohomology -- Orientation in generalized cohomology_, 2016 ([[PedrotticECohomology2016.pdf:file]])


[[!redirects complex projective spaces]]
