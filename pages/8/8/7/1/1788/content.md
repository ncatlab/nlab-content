

+-- {: .num_prop #DerivedCriticalLocusOfActionLiAlgebroidBicomplexStructure}
###### Proposition
**([[Chevalley-Eilenberg algebra]] of [[derived critical locus]] is [[total complex]] of [[BV-BRST formalism|BV-BRST]] [[bicomplex]])**

Let $(X/\mathfrak{g})_{d S \simeq 0}$ be a [[derived critical locus]] inside an [[action Lie algebroid]] as in example \ref{ArchetypeOfBVBRSTComplex}. Then its [[Chevalley-Eilenberg differential]] (eq:ExplitiCEDifferentialInCotangentBundleOfActionLieAlgebroid) may be decomposed as the sum of two anti-commuting differential

$$
  d_{CE\left( (X/\mathfrak{g})_{d S \simeq 0}  \right)}
  \;=\;
  s_{BRST} +  s_{BS}
$$

which are defined on the generators of the [[Chevalley-Eilenberg algebra]] as follows:

$$
  \label{ExplitiCEDifferentialInCotangentBundleOfActionLieAlgebroid}
  \array{
    & s_{BV}
    \\
    \phi^a
      &\mapsto&
    0
    \\
    c^\alpha
      & \mapsto&
    0
    \\
    \phi^\ddagger_a
      &\mapsto&
     \frac{\partial S}{\partial \phi^a}
    \\
    c^\ddagger_\alpha
      &\mapsto&
    R_\alpha^a  \phi^\ddagger_a
  }
$$

and

$$
  \label{ExplitiCEDifferentialInCotangentBundleOfActionLieAlgebroid}
  \array{
    & s_{BRST}
    \\
    \phi^a
      &\mapsto&
    c^\alpha R^a_\alpha
    \\
    c^\alpha
      & \mapsto&
    \tfrac{1}{2} \gamma^\alpha{}_{\beta \gamma} c^\beta c^\gamma
    \\
    \phi^\ddagger_a
      &\mapsto&
    -
    c^\alpha \frac{\partial R_\alpha^b}{\partial \phi^a} \phi^\ddagger_b
    \\
    c^\ddagger_\alpha
      &\mapsto&
    \gamma^\beta{}_{\alpha \gamma} c^\gamma c^\ddagger_b
  }
$$

If we moreover decompose the degree of the generators into two degrees

$$
  \array{
    &
    \left(
      c^\ddagger_{\alpha}
    \right)
    &
    \left(
      \phi^\ddagger_a
    \right)
    &
    \left(
      \phi^a
    \right)
    &
    \left(
      c^\alpha
    \right)
    \\
    deg_{gh} = 
    &
    0
    &
    0
    &
    0
    &
    +1
    \\
    deg_{af} = 
    &
    -2
    &
    -1
    &
    0
    &
    0
  }
$$

then these two differentials constitute a [[bicomplex]]

$$
  \array{
     CE^{0,0}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)
       &\overset{s_{BRST}}{\longrightarrow}&
     CE^{1,0}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)     
       &\overset{s_{BRST}}{\longrightarrow}&
     CE^{2,0}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)     
       &\overset{s_{BRST}}{\longrightarrow}&
     \cdots
     \\
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \\
     CE^{0,-1}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)
       &\overset{s_{BRST}}{\longrightarrow}&
     CE^{1,-1}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)     
       &\overset{s_{BRST}}{\longrightarrow}&
     CE^{2,-1}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)     
       &\overset{s_{BRST}}{\longrightarrow}&
     \cdots
     \\
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \\     
     CE^{0,-2}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)
       &\overset{s_{BRST}}{\longrightarrow}&
     CE^{1,-2}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)     
       &\overset{s_{BRST}}{\longrightarrow}&
     CE^{2,-2}\left( (X/\mathfrak{g})_{d S \simeq 0}\right)     
       &\overset{s_{BRST}}{\longrightarrow}&
     \cdots
     \\
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \big\uparrow^{\mathrlap{s_{BV}}}
       &&
     \\
     \vdots && \vdots && \vdots
  }
$$

whose [[total complex]] is the [[Chevalley-Eilenberg dg-algebra]] of the derived critical locus

$$
  \begin{aligned}
    CE\left(
      (X/\mathfrak{g})_{d S \simeq 0}
    \right)
    & =
    \underset{ gh, af }{\bigoplus}
    CE^{gh,af}\left( 
       (X/\mathfrak{g})_{d S \simeq 0}
    \right)
    \\
    d_CE\left( (X/\mathfrak{g})_{d S \simeq 0}  \right){}
    & =
    s_{BV} + s_{BRST}
  \end{aligned}
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is clear from the definition that the graded [[derivations]] $s_{BV}$ and $s_{BRST}$ have (i.e. increase) bidegree as follows:

$$
  \array{
     & s_{BRST} & s_{BV}
    \\
    deg_{gh} = & +1 & 0
    \\
    deg_{af} = & 0 & +1
  }
  \,.
$$

This implies that in

$$
  \begin{aligned}
    0 & =
    \left( d_{CE\left( (X/\mathfrak{g})_{d S \simeq 0} \right)} \right)^2
    \\
    & = 
    \left( s_{BV} +  s_{BRST}\right)^2
    \\
    & =
    \underset{ = 0 }{
    \underbrace{
      \left( s_{BV}\right)^2 
    }}
    + 
    \underset{ = 0 }{
    \underbrace{
      \left( s_{BRST} \right)^2 
    }}
    +
    \underset{ = 0 }{
    \underbrace{
      \left[ s_{BV}, s_{BRST} \right]
    }
    }
  \end{aligned}
$$

all three terms have to vanish separately, as shown, since they each have different bidegree (the last term denotes the graded commutator, hence the [[anticommutator]]). This is the statement to be proven.

Notice that the nilpotency of $s_{BV}$ is also immediately checked explicitly, due to the [[invariant|invariance]] of $S$ (example \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids}).

=--

As a corollary of prop. \refDerivedCriticalLocusOfActionLiAlgebroidBicomplexStructure{} we obtain the generalization of example \ref{OrdinaryCriticalLocusAsCohomologyOfDerivedCriticalLocus} to non-trivial $\mathfrak{g}$-actions:

+-- {: .num_prop}
###### Proposition

Let $(X/\mathfrak{g})_{d S \simeq 0}$ be a [[derived critical locus]] inside an [[action Lie algebroid]] as in example \ref{ArchetypeOfBVBRSTComplex}.

Then if the vertical [[differential]] (prop. \ref{DerivedCriticalLocusOfActionLiAlgebroidBicomplexStructure})

$$
  \array{
    CE^{\bullet, \bullet+1}\left( (X/\mathfrak{g})_{d S \simeq 0} \right)
    \\
    \uparrow^{\mathrlap{s_{BV}}}
    \\
    CE^{\bullet, \bullet}\left( (X/\mathfrak{g})_{d S \simeq 0} \right)
  }
$$

has vanishing [[cochain cohomology]] in [[negative number|negative]] $af$-degree

$$
  \label{VanishingOfNaiveLieAlgebroidBVCohomlogyInNegativeDegree}
  H^{\bullet \leq 1}(s_{BV}) = 0  
$$ 

then the [[cochain cohomology]] of the full [[Chevalley-Eilenberg dg-algebra]] is given by the cochain cohomology of $s_{BRST}$ on $H^0(s_{BV})$:

$$
  H^k\left( 
    CE\left( 
      (X/\mathfrak{g})_{d S \simeq 0}
    \right)
  \right)
  \;\simeq\;
  H^k\left(  H^0(s_{BV}), s_{BRST} \right)
  \,.
$$

Moreover if $X$ is inside the [[infinitesimal neighbourhood]] of a point as in example \ref{OrdinaryCriticalLocusAsCohomologyOfDerivedCriticalLocus} then the full cochain cohomology in degree 0 is the space of those functions on the ordinary [[critical locus]] $X_{d S = 0}$ which are $\mathfrak{g}$-[[invariant]]:

$$
  H^0
  \left(
    CE\left(
      (X/\mathfrak{g})_{d S \simeq 0}
    \right)
  \right)
  \;=\;
  \left\{
    X_{d S = 0}
      \overset{f}{\to}
    \mathbb{R}
     \;\vert\;
     \left(R_\alpha^a \frac{\partial f}{\partial \phi^a} = 0\right)
  \right\}
$$

=--

+-- {: .proof}
###### Proof


The first statement follows from the [[spectral sequence]] [[spectral sequence of a double complex|of the double complex]]

$$
  H^{gh}
  \left(
    H^{af}
    \left(
      CE\left(  (X/\mathfrak{g})_{d S \simeq 0} \right)
    \right)
  \right)
  \;\Rightarrow\;
  H^{gh + af}\left(
      CE\left(  (X/\mathfrak{g})_{d S \simeq 0} \right)  
  \right)
  \,.
$$

Under the given assumption the second page of this [[spectral sequence]] is concentrated on the row $af = 0$. This implies that all differentials on this page vanish, so that the sequence collapses on this page. Moreover, since the spectral sequence consists of [[vector spaces]] ([[modules]] over the [[real numbers]]) the [extension problem](spectral+sequence#ExtensionProblem) is trivial, and hence the claim follows.

Now if $X$ is inside the [[infinitesimal neighbourhood]] of a point, then example \ref{OrdinaryCriticalLocusAsCohomologyOfDerivedCriticalLocus} says that $H^0(s_{BV})$ in $deg_{gh} = 0$ consists of the functions on the ordinary critical locus and hence the abvove result implies that 

$$
  \begin{aligned}
    H^0\left( CE\left( (X/\mathfrak{g})_{d S \simeq 0}\right) \right)
    & =
    ker(s_{BRST})\vert_{C^\infty\left( X_{d S = 0} \right) }
    \,/\,
    \underset{= 0}{
    \underbrace{
      im(s_{BRST})\vert_{C^\infty\left(  X_{d S = 0} \right)}
    }
    }
    \\
    & = ker(s_{BRST})\vert_{C^\infty\left( X_{d S = 0} \right) }    
    \\
    & = 
    \left\{
       X_{d S = 0} \overset{f}{\longrightarrow} \mathbb{R}
       \,\vert\,
       \left( 
         R_\alpha^a \frac{\partial S}{\partial \phi^a}
         = 
         0 
       \right)
    \right\}
  \end{aligned}
$$


=--

This means that under condition (eq:VanishingOfNaiveLieAlgebroidBVCohomlogyInNegativeDegree) the construction of a [[derived critical locus]] inside an [[action Lie algebroid]] provides a [[resolution]] of the space of those functions which are 

1. _[[restriction|restricted]]_ to the [[critical locus]] (a [[homotopy intersection]]);

1. _[[invariant]]_ under the [[Lie algebra action]] (a [[homotopy quotient]]).

We apply this general mechanism [below](#DerivedCriticalLocusOnJetBundle) to [[Lagrangian field theory]], where it serves to provide a [[resolution]] by the _[[BV-BRST complex]]_ of the space of [[observables]] which are

1. [[on-shell]],

1. _[[gauge invariance|gauge invariant]]_.

But in order to control this application, we first establish the tool of the _[[Schouren bracket]]_/_[[antibracket]]_.
