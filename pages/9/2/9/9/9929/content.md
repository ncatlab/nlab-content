
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--



#Contents#
* table of contents$X$ 
{:toc}

## Idea

A _complex oriented cohomology theory_ is a [[generalized (Eilenberg-Steenrod) cohomology theory]] which is [[orientation in generalized cohomology|oriented]] on all [[complex vector bundles]]. Examples include [[ordinary cohomology]], complex [[topological K-theory]], [[elliptic cohomology]] and [[cobordism cohomology]].

The collection of all complex oriented cohomology theories turns out to be parameterized over the [[moduli stack of formal group laws]]. The [[stratification]] of this stack by the [[height of a formal group|height of formal group]] leads to the stratification of complex oriented cohomology theory by "[[chromatic level]]", a perspective also known as _[[chromatic homotopy theory]]_.

For more detailed introduction see at _[[Introduction to Cobordism and Complex Oriented Cohomology]]_.


## Definition
 {#Definition}

### In terms of generalized first Chern classes
 {#DefInTermsOfGeneralizedFirstChernClass}

Write $\mathbb{C}P^\infty \simeq B U(1) \simeq K(\mathbb{Z},2)$ for the inifinite [[complex projective space]], equivalently the [[classifying space]] for [[circle group]]-[[principal bundles]] (an [[Eilenberg-MacLane space]]); write $S^2$ for the [[2-sphere]] and write

$$
  i \;\colon\; S^2 \longrightarrow B U(1)
$$

for a representative of $1 \in \mathbb{Z} \simeq  \pi_2(B U(1))$, classifying the [[universal complex line bundle]]. Regard both $S^2$ and $B U(1)$ as [[pointed homotopy types]] and take $i$ to be a pointed morphism.

Let $E^\bullet$ be a [[multiplicative cohomology theory]], i.e. a [[functor]] $X \mapsto \pi_\bullet[X,E]$ for $E$ a [[ring spectrum]]. Write $\tilde E^\bullet$ for the corresponding [[reduced cohomology]] on [[pointed topological spaces]], such that for any pointed space $X$ there is a canonical [[direct sum]] decomposition ([this prop.](generalized+%28Eilenberg-Steenrod%29+cohomology#UnreducedCohomologyIsReducedPlusPointValue))

$$
  E^\bullet(X) \simeq \tilde E^\bullet(X) \oplus E^\bullet(\ast)
  \,.
$$

By the [[suspension isomorphism]] there is an identification

$$
  \tilde E^2(S^2) \simeq \tilde E^0(S^0) \simeq E^0(\ast) \simeq \pi_0(E)
$$

with the [[commutative ring]] underlying $E$. Write $1 \in \pi_0(E)$ for the multiplicative identity element in this ring.


+-- {: .num_defn #ComplexOrientedCohomologyTheory}
###### Definition
**(complex oriented cohomology theory)**

A [[multiplicative cohomology theory]] $E$ is _complex orientable_ if the following equivalent conditions hold:

1. The morphism

   $$
     i^\ast \;\colon\; E^2(B U(1)) \longrightarrow E^2(S^2)
   $$

   is [[surjection|surjective]].

1. The morphism on [[reduced cohomology]]

   $$
     \tilde i^\ast 
     \;\colon\; 
     \tilde E^2(B U(1)) \longrightarrow \tilde E^2(S^2)
     \simeq \pi_0(E)
   $$

   is [[surjection|surjective]].

1. The [[ring unit]] $1 \in \pi_0(E)$ is in the [[image]] of the morphism $\tilde i^\ast$.

A **complex orientation** on a [[multiplicative cohomology theory]] $E^\bullet$ is an element 

$$
  c_1^E \in \tilde E^2(B U(1))
$$

(the "first [[generalized Chern class]]") such that 

$$
  i^\ast c^E_1 = 1 \in \pi_0(E)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Since $B U(1) \simeq K(\mathbb{Z},2)$ is the [[classifying space]] for [[complex line bundles]], it follows that a complex orientation on $E^\bullet$ induces an $E$-[[generalized Chern class|generalization]] of the [[first Chern class]] which to a [[complex line bundle]] $\mathcal{L}$ on $X$, classified by $\phi \colon X \to B U(1)$  assigns the class $c_1(\mathcal{L}) \coloneqq \phi^\ast c_1^E$. This construction extends to a general construction of $E$-[[Chern classes]] ([[Conner-Floyd Chern classes]]). 

=--

+-- {: .num_remark #ComplexOrientationByExtensionsAndTheirObstructions}
###### Remark
**(complex $E$-orientation by [[extensions]] and their [[obstructions]])**


In terms of [[Brown representability theorem|classifying maps]], Def. \ref{ComplexOrientedCohomologyTheory} means that a complex orientation $c_1^E$ in $E$-cohomology theory is equivalently an [[extension]] (in the [[classical homotopy category]]) of the map $\Sigma^2 1 \,\colon\, \mathbb{C}P^1 \longrightarrow \Omega^{\infty-2} E$ (which classifies the suspended identity in the cohomology ring) along the canonical inclusion of [[complex projective spaces]] 

\[
  \label{ComplexOrientationAsExtension}
  \array{
     \mathbb{C}P^1
     &
     \overset{
       \Sigma^2 1_E
     }{
       \longrightarrow
     }
     &
     \Omega^{\infty - 2} E
     \\
     \big\downarrow
     &
     \nearrow \mathrlap{ {}_{c_1^E} }
     \\
     \mathbb{C}P^\infty
  }
\]

Notice that the [[complex projective spaces]] form a [[cotower]]

$$
  \ast 
  \,=\,
  \mathbb{C}P^0
  \hookrightarrow
  \mathbb{C}P^1
  \hookrightarrow
  \mathbb{C}P^2
  \hookrightarrow
  \mathbb{C}P^3
  \hookrightarrow
  \cdots
  \hookrightarrow
  \mathbb{C}P^\infty
  \,=\,
  \underset{\longrightarrow}{\lim}
  \mathbb{C}P^\bullet
$$

where each inclusion stage is (by [this Prop.](complex+projective+space#CellComplexStructureOnComplexProjectiveSpace), see at _[[cell structure of projective spaces]]_) the coprojection of a [[pushout]] [of topological spaces](Top#UniversalConstructions) (or rather: of [[pointed topological spaces]]) of the form

$$
  \array{
    D^{2n+2}
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{C}P^{n+1}
    \\
    \big\uparrow
    &\mathclap{^{_{(po)}}}&
    \big\uparrow
    \\
    S^{2n+1}
    &\underset{h^{2n+1}_{\mathbb{C}}}{\longrightarrow}&
    \mathbb{C}P^n
  }
$$

(where $h^{2n+1}_{\mathbb{C}}$ is the [[complex Hopf fibration]] in dimension $2n+1$) hence of a [[homotopy pushout]] of [[classical model structure on topological spaces|underlying homotopy types]] (rather: [[classical model structure on pointed topological spaces|of pointed homotopy types]]) of this form:

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{C}P^{n+1}
    \\
    \big\uparrow
    &\mathclap{^{_{(hpo)}}}&
    \big\uparrow
    \\
    S^{2n+1}
    &\underset{h^{2n+1}_{\mathbb{C}}}{\longrightarrow}&
    \mathbb{C}P^n
  }
$$

Therefore, a complex orientation by extension (eq:ComplexOrientationAsExtension) is equivalently the homotopy colimiting map of a sequence

$$
  \big(
    \Sigma^2 1 
      \,=\, 
    c_1^{E,0}
    ,\,
    c_1^{E,1}
    ,\,
    c_1^{E,2}
    ,\,
    \cdots
  \big)
$$

of finite-stage extensions

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{C}P^{n+1}
    &
    \overset{ c_1^{E,n+1} }{\longrightarrow}
    &
    \Omega^{\infty -2} E
    \\
    \big\uparrow
    &\mathclap{^{_{(hpo)}}}&
    \big\uparrow
    & 
    \nearrow \mathrlap{ {}_{c_1^{E,n}} }
    \\
    S^{2n+1}
    &\underset{h^{2n+1}_{\mathbb{C}}}{\longrightarrow}&
    \mathbb{C}P^n
    \,.
  }
$$

Moreover, by the defining [[universal property]] of the [[homotopy pushout]], the extension $c_1^{E,n+1}$ of $c_1^{E,n}$ is equivalently a choice of [[homotopy]] which trivializes the pullback of $c_1^{E,n}$ to the [[n-sphere|2n+1-sphere]]:

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \Omega^{\infty - 2} E
    \\
    \big\uparrow
    &
    {}_{  c_1^{E,n+1}  }
    \seArrow
    &
    \big\uparrow \mathrlap{ ^{_{ c_1^{E,n} }} }
    \\
    S^{2n+1}
    &\underset{ h^{2n+1}_{\mathbb{C}} }{\longrightarrow}&
    \mathbb{C}P^n
    \,.
  }
$$

This means, first of all, that the non-triviality of the pullback class

$$
  \big( 
    h^{2n+1}_{\mathbb{C}}
  \big)^\ast 
  ( c_1^{E,n} )
  \;\in\;
  \widetilde E^2
  \big(
    S^{2n+1}
  \big)
  \;\simeq\;
  E_{2n-1}
$$

is the [[obstruction]] to the existence of the extension/orientation at this stage. 

It follows that if these obstructions all vanish, then a complex $E$-orientation does exist.  A sufficient condition for this is, evidently, that the reduced $E$-cohomology of all odd-dimensional spheres vanishes, hence, that the [[graded-commutative ring|graded]] $E$-[[cohomology ring]] $E_\bullet$ is trivial in odd degrees.

=--

(see also [Lurie, Lecture 6, Remark 4](#LurieLecture))



### In terms of orientations of fibers of complex vector bundles
 {#InTermsOfOrientations}


\begin{remark}
  \label{ComplexEOrientationsFromFirstEChernClass}
  **(complex $E$-orientations from first $E$-Chern class)**

To see that a generalized Chern class $c^E_1$ in the [above sense](#DefInTermsOfGeneralizedFirstChernClass) indeed has to do with _complex orientations_, namely of, first of all, [[fibers]] of [[complex line bundles]], notice that any [[complex projective space]] is equivalently the [[Thom space]] of the [[dual vector bundle|dual]] [[tautological line bundle]] (see [there](tautological+line+bundle#DualTautologicalLineBundle)) on the [[complex projective space]] of one complex dimension lower:

\begin{xymatrix@R=20pt@C=30pt}
    \mathllap{
      S^{2}
      =
      \;\;
    }
    \mathbb{C}P^1
    \ar@{^{(}->}[r]
    &
    \mathbb{C}P^2
    \ar@{=}[d]
    \ar@{^{(}->}[r]
    &
    \;\;
    \cdots
    \;\;
    \ar@{^{(}->}[r]
    &
    \mathbb{C}P^{n+1}
    \ar@{=}[d]
    \;
    \ar@{^{(}->}[rr]
      |-{
        \;
        \scalebox{.76}{
        \raisebox{-5pt}{$
          \cdots
        $}
        }
      \;}
    &
    &
    \mathbb{C}P^{\infty}
    \ar@{=}[d]
    \\
    &
    \mathrm{Th}
    \big(
      \mathcal{L}^\ast_{\mathbb{C}P^1}
    \big)
    \ar@{^{(}->}[r]
    &
    \;\;
    \cdots
    \;\;
    \ar@{^{(}->}[r]
    &
    \mathrm{Th}
    \big(
      \mathcal{L}^\ast_{\mathbb{C}P^n}
    \big)
    \;
    \ar@{^{(}->}[rr]
      |-{
        \;
        \scalebox{.76}{
        \raisebox{-5pt}{$
          \cdots
        $}
        }
      \;}
    &
    &
    \mathrm{Th}
    \big(
      \mathcal{L}^\ast_{\mathbb{C}P^\infty}
    \big)
    \ar@{=}[r]
    &
    \mathrm{Th}
    \big(
      E \mathrm{U}(1)
        \!\!
        \underset{\scalebox{.63}{$\mathrm{U}(1)$}}{\times}
        \!\!
      \mathbb{C}
    \big)
    \\
    \\
    &
    \mathllap{
      S^{2}
      =
      \;\;
    }
    \mathbb{C}P^1
    \ar@{^{(}->}[r]
    \ar[uu]
     |-{
       0_{{}_{
         \mathrm{Th}
         (
           \mathcal{L}^\ast_{\mathbb{C}P^1}
         )
       }}
       \mathclap{\phantom{\vert_{\vert_{\vert_{\vert}}}}}
     }
    &
    \;\;\cdots\;\;
    \ar@{^{(}->}[r]
    &
    \mathbb{C}P^{n}
    \ar[uu]
     |-{
       0_{{}_{
         \mathrm{Th}
         (
           \mathcal{L}^\ast_{\mathbb{C}P^n}
         )
       }}
       \mathclap{\phantom{\vert_{\vert_{\vert_{\vert}}}}}
     }
    \;
    \ar@{^{(}->}[rr]
      |-{
        \;
        \scalebox{.76}{
        \raisebox{-5pt}{$
          \cdots
        $}
        }
      \;}
    &
    &
    \mathbb{C}P^{\infty}
    \ar[uu]
     |-{
       0_{{}_{
         \mathrm{Th}
         (
           \mathcal{L}^\ast_{\mathbb{C}P^\infty}
         )
       }}
       \mathclap{\phantom{\vert_{\vert_{\vert_{\vert}}}}}
     }
     \ar@{=}[r]
     &
     B \mathrm{U}(1)
     \ar[uu]
     |-{
       \hspace{3pt}
       \scalebox{.7}{
         \rotatebox{-90}{$
           \;\simeq\;
         $}
       }
     }
\end{xymatrix}

The morphism of [E-cohomology Milnor sequences](lim1+and+Milnor+sequences#MilnorSequenceForGeneralizedCohomology) that this transformation induces shows (see the proof of Prop. \ref{CohomologyRingOfBU1ForComplexOrientedCohomologyTheory} for details) that [[pullback in cohomology|pullback]] along the [[zero section]] identifies the $E$-cohomology of the [[Thom space]] of the [[universal complex line bundle]] with that of the base [[classifying space]]:


\begin{xymatrix@R=26pt@C=30pt}
    \widetilde E {}^\bullet
    \big(
      S^2
    \big)
    \ar@{=}[d]
    \ar@{<-}[rr]^-{
      \mbox{
        \tiny
        \color{blue}
        \bf
        restriction to fiber
      }
    }
    &&
    \widetilde E {}^\bullet
    \Big(
      \mathrm{Th}
      \big(
        E \mathrm{U}(1)
          \underset{\scalebox{.6}{$\mathrm{U}(1)$}}{\times}
        \mathbb{C}
      \big)
    \Big)
    \ar[d]
     |-{
       \hspace{3pt}
       \scalebox{.7}{
         \rotatebox{-90}{$
           \;\simeq\;
         $}
       }
     }
    &
    \mathrm{th}^E_1
    \ar@{|->}[d]
    \\
    \widetilde E^{\bullet}
    \big(
      S^2
    \big)
    \ar@{<-}[rr]_-{
      \mbox{
        \tiny
        \color{blue}
        \bf
        restriction to $\mathbb{C}P^1 \subset \mathbb{C}P^\infty$
      }
    }
    &&
    \widetilde E {}^{\bullet}
    \big(
      B\mathrm{U}(1)
    \big)
    &
    c^E_1
\end{xymatrix}

(In fact the [[zero-section]] of the [[Thom space]] of the [[universal complex line bundle]] is itself a [[weak homotopy equivalence]], see [this Lemma](universal+complex+orientation+on+MU#UniversalComplexLineBundleThomSpace).)

But this means that the $E$-Chern class $c^E_1$ has a unique pre-image which is an $E$-[[Thom class]] $th^E_1$ on the [[universal complex line bundle]], and hence [[pullback in cohomology|pulls back]] to an $E$-[[Thom class]] on any [[complex line bundle]].

In fact more is true: The choice of $c^E_1$ induces a sequence of [[universal characteristic class|universal]] [[Conner-Floyd Chern classes]] $c^E_n$ for all $n \in \mathbb{N}$, and by an elaboration of the previous argument these are [[pullback in cohomology|pullbacks]] along the [[zero-section]] of universal $E$-[[Thom classes]] on the [[universal complex vector bundle]] of any [[rank]] $n$ (see [this Lemma](universal+complex+orientation+on+MU#UniversalComplexVectorBundleThomSpace)).

\end{remark}



### In terms of genera 
 {#InTermsOfGenera}

Complex orientation in the [above](#Definition) sense is indeed universal [[MU]]-[[orientation in generalized cohomology]]:

+-- {: .num_prop #ComplexOrientationIsMUAlgebraStructure}
###### Proposition

For $E$ a  [[homotopy commutative ring spectrum]], there is a [[bijection]] between complex orientations of $E$-cohomology and  [[homotopy commutative ring spectrum]]-[[homomorphisms]] $MU \longrightarrow E$ out of [[MU]].

=--

([Hopkins 99, section 4](#Hopkins99), [Lurie, lecture 6, theorem 8](#LurieLecture)) 

See at _[[universal complex orientation on MU]]_.



+-- {: .num_remark}
###### Remark

One might hope that the above universal property can be refined to say that that if $E$ is an $E_\infty$-ring spectrum, then complex orientations of $E$ are in bijection with $E_\infty$ ring maps $MU \to E$. This is not the case; Ando classified $H_\infty$ ring maps $MU \to E$ in [his thesis](#Ando92) and in particular showed that not every complex orientation gives rise to an $H_\infty$ ring map out of $MU$. More recently, [Hopkins and Lawson](#HopkinsLawson16) have classified the further structure constituting an $E_\infty$ ring map out of $MU$.

=--

## Examples

Examples of complex orientable cohomology theories:


+-- {: .num_example }
###### Example
**([[ordinary cohomology]])**

For $E = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]], the ordinary [[first Chern class]]

$$
  c_1 \in H^2(B U(1), \mathbb{Z})
$$

defines a complex orientation of $H\mathbb{Z}$.
=--

+-- {: .num_example }
###### Example
**([[topological K-theory]])**

For $E = KU$ complex [[topological K-theory]], then the class of the image of the [[universal complex line bundle]] $\mathcal{O}(1)$ in [[reduced K-theory]] is a complex orientation.

The induced [[formal group law]] (by prop. \ref{ComplexOrientedCohomologyTheoryFormalGroupLaw}) is the [[multiplicative formal group law]]. 

For details see at _[[topological K-theory]]_ the section _[Complex orientation and Formal group law](topological+K-theory#ComplexOrientationAndFormalGroupLaw)_.

=--

+-- {: .num_example #ComplexCobordism}
###### Example
**(complex cobordism)**

For $E = MU$ [[complex cobordism cohomology theory]], the canonical map

$$
  B U(1) \stackrel{\simeq}{\to} MU(1) \to MU
$$ 

defines a complex orientation. 

=--

+-- {: .num_example #BrownPeterson}
###### Example

[[Brown-Peterson cohomology]] $E = B P^\bullet$.

=--



## Properties

### Cohomology ring of $B U(1)$ 
 {#CohomologyRingOfBU1}

+-- {: .num_prop #CohomologyRingOfBU1ForComplexOrientedCohomologyTheory}
###### Proposition

Given a complex oriented cohomology theory $(E^\bullet, c^E_1)$ according to def. \ref{ComplexOrientedCohomologyTheory}, then there are [[isomorphisms]] of [[graded rings]] 

1. $E^\bullet(B U(1)) \simeq E^\bullet(\ast)[ [ c_1^E ] ]$

   (between the $E$-[[cohomology ring]] of $B U(1)$ and the [[formal power series]] (but see remark \ref{ChoiceOfRingStructureOnGradedCohomologyGroupOfMultiplicativeCohomologyTheory}) in one generator of even degree over the $E$-[[cohomology ring]] of the point);

1. $E^\bullet(B U(1) \times B U(1)) \simeq E^\bullet(\ast)[ [ c_1^E \otimes 1 , 1 \otimes c_1^E ] ]$.

=--

+-- {: .proof}
###### Proof

We may realize the [[classifying space]] $B U(1)$ as the infinite [[complex projective space]] $\mathbb{C}P^\infty = \underset{\longleftarrow}{\lim}_n \mathbb{C}P^n$ ([exmpl.](classifying+space#RealComplexProjectiveSpaceAsGrassmannian)).
There is a standard [[CW-complex]]-structure on the [[classifying space]] $\mathbb{C}P^\infty$, given by inductively identifying $\mathbb{C}P^{n+1}$ with the result of attaching a single $2n$-cell to $\mathbb{C}P^n$ ([prop.](complex+projective+space#CellComplexStructureOnComplexProjectiveSpace)). With this structure, the unique 2-cell inclusion $i \;\colon\; S^2 \hookrightarrow \mathbb{C}P^\infty$ is identified with the canonical map $S^2 \to B U(1)$.

Then consider the [[Atiyah-Hirzebruch spectral sequence]] for the $E$-cohomology of $\mathbb{C}P^n$. 

$$
  H^\bullet(\mathbb{C}P^n, E^\bullet(\ast))
  \;\Rightarrow\;
  E^\bullet(\mathbb{C}P^n)
  \,.
$$

Since ([prop.](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace)) the [[ordinary cohomology]] with [[integer]] [[coefficients]] of projective space is 

$$
  H^\bullet(\mathbb{C}P^n, \mathbb{Z}) \simeq \mathbb{Z}[c_1]/((c_1)^{n-1})
  \,,
$$

where $c_1$ represents a unit in $H^2(S^2, \mathbb{Z})\simeq \mathbb{Z}$, and since similarly the [[ordinary homology]] of $\mathbb{C}P^n$ is a [[free abelian group]] ([prop.](complex+projective+space#OrdinaryCohomologyOfComplexProjectiveSpace)), hence a [[projective object]] in abelian groups ([prop.](projective+object#ProjectiveObjectsInAbAreFreeGroups)), the [[Ext]]-group vanishes in each degree ($Ext^1(H_n(\mathbb{C}P^n), E^\bullet(\ast)) = 0$) and so the [[universal coefficient theorem]] ([prop.](universal+coefficient+theorem#OrdinaryStatementInCohomology)) gives that the second page of the spectral sequence is

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

This means that $c_1$ is a permanent cocycle of the spectral sequence (in the kernel of all differentials) precisely if it arises via restriction from an element in $E^2(\mathbb{C}P^n)$ and hence precisely if there exists a complex orientation $c_1^E$ on $E$. Since this is the case by assumption on $E$, $c_1$ is a permanent cocycle. (For the fully detailed argument, see ([Pedrotti 16](#Pedrotti16))).

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
  0 \to F^{p+1}E^{p+\bullet}(X) 
  \longrightarrow F^{p}E^{p+\bullet}(X) \longrightarrow \mathcal{E}_\infty^{p,\bullet} \to 0
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
    E^\bullet( \underset{\longrightarrow}{\lim}_n \mathbb{C}P^n )
   \\
    &\simeq \underset{\longleftarrow}{\lim}_n E^\bullet(\mathbb{C}P^n)
   \\
   &\simeq \underset{\longleftarrow}{\lim}_n ( E^\bullet(\ast) [c_1^E] / ((c_1^E)^{n+1})  )
   \\
   & \simeq E^\bullet(\ast)[ [ c_1^E ] ]
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

These differ in general. For instance if $E$ is [[ordinary cohomology]] with [[integer]] [[coefficients]] and $X$ is infinite [[complex projective space]] $\mathbb{C}P^\infty$, then ([prop.](complex+projective+space+OrdinaryCohomologyOfComplexProjectiveSpace))

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

A priori both of these are sensible choices. The former is the usual choice in traditional [[algebraic topology]]. However, from the point of view of regarding [[ordinary cohomology]] theory as a [[multiplicative cohomology theory]] right away, then the second perspective tends to be more natural;

The cohomology of $\mathbb{C}P^\infty$ is naturally computed as the [[inverse limit]] of the cohomolgies of the $\mathbb{C}P^n$, each of which unambiguously has the ring structure $\mathbb{Z}[c_1]/((c_1)^{n+1})$. So we may naturally take the limit in the [[category]] of [[commutative rings]] right away, instead of first taking it in $\mathbb{Z}$-indexed sequences of abelian groups, and then looking for ring structure on the result. But the limit taken in the category of rings gives the [[formal power series ring]] (see [here](formal+scheme#FormalPowerSeries)).

See also for instance remark 1.1. in [[Jacob Lurie]]: _[[A Survey of Elliptic Cohomology]]_.

=--

\begin{example}\label{ComplexKTheoryOfClassifyingSpaceOfCircleGroup}
**([[topological K-theory]] of [[classifying space]] of [[circle group]])**
  For the case of [[topological K-theory]] $E = $ [[KU]], the cohomology ring $KU^\bullet(B U(1)) \;\simeq\; \mathbb{Z}[ [ c_1^{KU}] ]$ (Prop. \ref{CohomologyRingOfBU1ForComplexOrientedCohomologyTheory}) may also be computed via the [[Atiyah-Segal completion theorem]], see the [Example there](Atiyah-Segal+completion+theorem#ComplexTopologicalKTheoryOfBS1).
\end{example}


### Formal group law
 {#FormalGroupLaw}

Let again $B U(1)$ be the [[classifying space]] for [[complex line bundles]], modeled, in particular, by infinite [[complex projective space]] $\mathbb{C}P^\infty)$.


+-- {: .num_lemma #BU1HomotopyGroupStructure}
###### Lemma

There is a [[continuous function]]

$$
  \mu
    \;\colon\;
  \mathbb{C}P^\infty \times \mathbb{C}P
    \longrightarrow
  \mathbb{C}P^\infty
$$

which represents the [[tensor product of line bundles]] in that under the defining equivalence, and for $X$ any [[paracompact Hausdorff space]] (notably a [[CW-complex]], since all [[CW-complexes are paracompact Hausdorff spaces]]), then

$$
  \array{
     [X, \mathbb{C}P^\infty \times \mathbb{C}P^\infty]
     &\simeq&
     \mathbb{C}LineBund(X)_{/\sim} \times \mathbb{C}LineBund(X)_{/\sim}
     \\
     {}^{\mathllap{[X,\mu]}}\downarrow
       &&
     \downarrow^{\mathrlap{\otimes}}
     \\
     [X,\mathbb{C}P^\infty]
       &\simeq&
     \mathbb{C}LineBund(X)_{/\sim}
  }
  \,,
$$

where $[-,-]$ denotes the [[hom-sets]] in the (Serre-Quillen-)[[classical homotopy category]] and $\mathbb{C}LineBund(X)_{/\sim}$ denotes the set of [[isomorphism classes]] of [[complex line bundles]] on $X$.

Together with the canonical point inclusion $\ast \to \mathbb{C}P^\infty$, this makes $\mathbb{C}P^\infty$ an [[abelian group|abelian]] [[group object]] in the [[classical homotopy category]] (an abelian [[H-group]]).

=--

+-- {: .proof}
###### Proof

By the [[Yoneda lemma]] (the [[fully faithful functor|fully faithfulness]] of the [[Yoneda embedding]]) there exists such a morphism $\mathbb{C}P^\infty \times \mathbb{C}P^\infty \longrightarrow \mathbb{C}P^\infty$ in the [[classical homotopy category]]. But since $\mathbb{C}P^\infty$ admits the structure of a [[CW-complex]] ([prop.](complex+projective+space#CellComplexStructureOnComplexProjectiveSpace)) it is cofibrant in the [[standard model structure on topological spaces]], as is its [[Cartesian product]] with itself ([prop.](CW+complex#ClosureOfCWComplexesUnderCartesianProduct)). Since moreover all spaces are fibrant in the [[classical model structure on topological spaces]], it follows (by [this lemma](Introduction+to+Stable+homotopy+theory+--+P#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)) that there is an actual [[continuous function]] representing that morphism in the homotopy category.

That this gives the structure of an [[abelian group|abelian]] [[group object]] now follows via the [[Yoneda lemma]] from the fact that each $\mathbb{C}LineBund(X)_{/\sim}$ has the structure of an [[abelian group]] under [[tensor product of line bundles]], with the [[trivial bundle|trivial]] line bundle (wich is classified by maps factoring through $\ast \to \mathbb{C}P^\infty$) being the neutral element, and that this group structure is [[natural transformation|natural]] in $X$.

=--

+-- {: .num_remark}
###### Remark

The space $B U(1) \simeq \mathbb{C}P^\infty$ has in fact more structure than that of an [[H-group]] from lemma \ref{BU1HomotopyGroupStructure}. As an object of the [[homotopy theory]] represented by the [[classical model structure on topological spaces]], it is a _[[2-group]]_, a [[truncated object in an (infinity,1)-category|1-truncated]] [[infinity-group]].

=--

+-- {: .num_prop #ComplexOrientedCohomologyTheoryFormalGroupLaw}
###### Proposition

Let $(E, c_1^E)$ be a [[complex oriented cohomology theory]]. Under the identification

$$
  E^\bullet(\mathbb{C}P^\infty)
   \simeq
  \pi_\bullet(E)[ [ c^E_1 ] ]
  \;\;\;\,,
  \;\;\;
  E^\bullet(\mathbb{C}P^\infty \times \mathbb{C}P^\infty)
   \simeq
  \pi_\bullet(E)[ [ c^E_1 \otimes 1 , \, 1 \otimes c^E_1 ] ]
$$

from prop. \ref{CohomologyRingOfBU1ForComplexOrientedCohomologyTheory}, the operation 

$$
  \pi_\bullet(E)
  [ [ c^E_1 ] ]
    \simeq
  E^\bullet(\mathbb{C}P^\infty)
    \longrightarrow
  E^\bullet( \mathbb{C}P^\infty \times \mathbb{C}P^\infty )
    \simeq
  \pi_\bullet(E)[ [ c_1^E \otimes 1, 1 \otimes c_1^E ] ]
$$

of pullback in $E$-cohomology along the maps from lemma \ref{BU1HomotopyGroupStructure} constitutes a 1-dimensional
graded-commutative [[formal group law]] ([exmpl.](formal+group#Commutative1DimFormalGroupLaw)) over the [[graded commutative ring]] $\pi_\bullet(E)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyGroupsOfHomotopyCommutativeRingSpectrum)). If we consider $c_1^E$ to be in degree 2, then this formal group law is compatibly graded.

=--

+-- {: .proof}
###### Proof

The associativity and commutativity conditions follow directly from the respective properties of the map $\mu$ in lemma \ref{BU1HomotopyGroupStructure}. The grading follows from the nature of the identifications in prop. \ref{CohomologyRingOfBU1ForComplexOrientedCohomologyTheory}.

=--

+-- {: .num_remark}
###### Remark

That the grading of $c_1^E$ in prop. \ref{ComplexOrientedCohomologyTheoryFormalGroupLaw} is in negative degree is because by definition

$$
  \pi_\bullet(E) = E_\bullet = E^{-\bullet}
$$

([rmk.](Introduction+to+Stable+homotopy+theory+--+1-2#EMHomology)).

Under different choices of orientation, one obtains different but isomorphic formal group laws. 


=--




+-- {: .num_example}
###### Example

The [[formal group law]] of [[complex cobordism cohomology theory]], example \ref{ComplexCobordism} is [[universal property|universal]] in that for every [[commutative ring]] $R$ there is a [[natural bijection]]

$$
  CRing(MU^\bullet, R)
  \simeq
  FormalGroupLaws_{/R}
  \,.
$$

$MU^\bullet$ is the _[[Lazard ring]]_.

This is _[[Milnor-Quillen's theorem on MU]]_ (involving [[Lazard's theorem]]).


=--


+-- {: .num_example}
###### Example

The [[formal group law]] of [[Brown-Peterson cohomology theory]], example \ref{BrownPeterson} is [[universal property|universal]] for $p$-local cohomology theories in that $\mathbb{G}_{B P}$ is universal among $p$-local, [[p-typical formal group laws]].

=--

### Cohomology ring of $B U(n)$
 {#TheCohomologyRingOfBUn}

+-- {: .num_prop #CohomologyRingOfBUn}
###### Proposition

For $E$ a complex oriented cohomology theory and $n \in \mathbb{N}$, restriction along the canonical map

$$
  (B U(1))^n  \longrightarrow B U(n)
$$

induces an [[isomorphism]]

$$
  E^\bullet(B U(n))
    \stackrel{\simeq}{\longrightarrow}
  (\pi_\bullet E)[ [ c^E_1, \cdots, c^E_n ] ]
  \simeq
  E^\bullet((B U(1))^n)^{\Sigma_n}
  \hookrightarrow
  E^\bullet((B U(1))^n)
  \simeq
  (\pi_\bullet E)[ [(c_1^E)_1, \cdots (c_1^E)_n ] ]  
  \,,
$$

of $E^\bullet(B U(n))$ with the [[cyclic group]]-[[invariants]] in $E^\bullet((B U(1))^n)$, hence with the [[power series]] ring in the [[elementary symmetric polynomials]] $c_i^E$ (the [[generalized Chern classes]]) in the $c_1^E$-s (the generalized first Chern classes of prop. \ref{CohomologyRingOfBU1ForComplexOrientedCohomologyTheory}).

=--

Use [this proposition](ordinary+homology+spectra+split#WhenGeneralizedHomologySpectraSplit) to reduce to the situation for ordinary [[Chern classes]]. (e.g. [Lurie 10, lecture 4](#LurieLecture))

### Canonical orientation on complex vector bundles

The follows says that complex oriented cohomology theories in the sense of def. \ref{ComplexOrientedCohomologyTheory}, indeed canonically have an [[orientation in generalized cohomology]] for the ([[spherical fibration]] of) any [[complex vector bundle]].

For more details see at _[[universal complex orientation on MU]]_.

+-- {: .num_prop #ThomSpaceOfZetan}
###### Proposition

For $E$ any [[cohomology theory]] and $n \in \mathbb{N}$, $n \geq 1$, there is a canonical [[isomorphism]] of [[relative cohomology]]

$$
  E^\bullet(B U(n), B U(n-1))
  \simeq
  E^\bullet( B( \zeta_n), S( \zeta_n) )
  \,,
$$

where $\zeta_n \coloneqq E U(n) \underset{U(n)}{\times} \mathbb{R}^{2n}$ is the [[universal complex vector bundle]].

=--

+-- {: .proof}
###### Proof

Observe that the [[sphere bundle]] $S(\zeta_n) \to B U(n)$ of the [[universal complex vector bundle]] is equivalently the canonical map $B U(n-1) \to B U(n)$. 

This follows form the fact that $S^{2n-1} \simeq U(n)/U(n-1)$ and that hence the [[unit sphere]] bundle is equivalently the quotient of the $U(n)$-[[universal principal bundle]] by $U(n-1)$

$$
  \array{
    U(n) &\longrightarrow& \ast
    \\
    && \downarrow
    \\
    && B U(n)
  }
  \;\;\;\; \stackrel{}{\mapsto}\;\;\;\;
  \array{
     S^{2n-1} \simeq & U(n)/U(n-1) &\longrightarrow& B U(n-1) 
     \\
     & && \downarrow 
     \\
     & &&  B U(n)
  }
  \,.
$$

The unit ball bundle $B(\zeta_n)$ is weakly equivalent to $B U(n)$, and under this identification the map $S(\zeta_n) \to B(\zeta_n)$ is equivalent to $B U(n-1) \to B U(n)$.

=--

+-- {: .num_prop }
###### Proposition

For $E$ a complex oriented cohomology theory,
its $n$th [[generalized Chern class]] $c^E_n$, prop. \ref{CohomologyRingOfBUn}, identified as an element of 
$E^\bullet(B(\zeta_n), S(\zeta_n))$ via prop. \ref{ThomSpaceOfZetan},
is a [[Thom class]].

=--

(e.g. [Lurie 10, lecture 5, prop. 6](#LurieLecture))

## Related concepts

* [[real oriented cohomology theory]]

* [[quaternionic oriented cohomology theory]]

* [[equivariant complex oriented cohomology theory]]

* [[generalized (Eilenberg-Steenrod) cohomology theory]]

* [[multiplicative cohomology theory]]

* [[orientation in generalized cohomology]]

* [[complex cobordism cohomology theory]]

* [[Landweber exact functor theorem]]

* [[chromatic homotopy theory]]

[[!include chromatic tower examples - table]]

## References

### General

Textbook accounts:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], around Theorem 7.6 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))


* [[Frank Adams]], part II, section 2 of: _[[Stable homotopy and generalised homology]]_, 1974

* [[John Michael Boardman]], Section 5 of: _Stable Operations in Generalized Cohomology_ ([pdf](https://hopf.math.purdue.edu/Boardman/stabop.pdf)) in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))


* {#Kochmann96} [[Stanley Kochmann]], section 4.3 of: _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* [[Doug Ravenel]], Section 4.1 of: _[[Complex cobordism and stable homotopy groups of spheres]]_

* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], Section 3.2 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))

Introduction includes

* _[[Introduction to Cobordism and Complex Oriented Cohomology]]_

* {#Pedrotti16} [[Riccardo Pedrotti]], _Complex oriented cohomology, generalized orientation and Thom isomorphism_, 2016, 2018 ([[PedrotticECohomology2018.pdf:file]])


The perspective of [[chromatic homotopy theory]] originates in

* {#Hopkins99} [[Mike Hopkins]], _[[Complex oriented cohomology theories and the language of stacks]]_, 1999 course notes ([[HopkinsComplexOrientedCohomology.pdf:file]])

and is further developed in

* {#LurieLecture} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture notes, 2010 ([web](http://www.math.harvard.edu/~lurie/252x.html))

  Lecture 4 _Complex-oriented cohomology theories_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture4.pdf))

  Lecture 6 _MU and complex orientations_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture6.pdf))

See also the references at _[equivariant cohomology -- References -- Complex oriented cohomology](equivariant+cohomology#InComplexOrientedGeneralizedCohomologyTheory)_-.

A comparison between complex orientations and $H_\infty$ ring maps out of $MU$ was given in

* {#Ando92} [[Matthew Ando]], _Operations in complex-oriented cohomology theories related to subgroups of formal groups_ ([PhD Thesis](https://dspace.mit.edu/bitstream/handle/1721.1/13230/26903638-MIT.pdf?sequence=2))


More recent developments include

* {#HopkinsLawson16} [[Michael Hopkins]], [[Tyler Lawson]], _Strictly commutative complex orientation theory_ ([arXiv:1603.00047](http://arxiv.org/abs/1603.00047))

Refinement to [[equivariant complex oriented cohomology theory]]:

* [[John Greenlees]], _Equivariant formal group laws and complex oriented cohomology theories_, Homology Homotopy Appl. Volume 3, Number 2 (2001), 225-263 ([euclid:hha/1139840255](https://projecteuclid.org/euclid.hha/1139840255))

* [[Michael Cole]], [[John Greenlees]], [[Igor Kriz]], _The universality of equivariant complex bordism_, Math Z 239, 455–475 (2002) ([doi:10.1007/s002090100315](https://doi.org/10.1007/s002090100315))



[[!include finite-rank complex orientation and MΩSUn -- references]]





[[!redirects complex oriented cohomology theories]]

[[!redirects complex oriented cohomology]]
[[!redirects complex-oriented cohomology]]

[[!redirects complex-oriented cohomology theory]]
[[!redirects complex-oriented cohomology theories]]

[[!redirects complex orientable cohomology theory]]
[[!redirects complex orientable cohomology theories]]

