
Equivalently this means that a complex orientation $c_1^E$ in $E$-theory is an [[extension]] (in the [[classical homotopy category]]) of the map $\Sigma^2 1 \,\colon\, \mathbb{C}P^1 \longrightarrow \Omega^\infty E$ (which classifies the suspended identity in the cohomology ring) along the canonical inclusion of [[complex projective spaces]] 

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

where each inclusion stage is (by [this Prop.](complex+projective+space#CellComplexStructureOnComplexProjectiveSpace)) the coprojection of a [[pushout]] [of topological spaces](Top#UniversalConstructions) (of [[pointed topological spaces]]) of the form

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

Therefore, a complex orientation by extension (eq:ComplexOrientationAsExtension) is equivalently the homotopy colimiting map out of a sequence

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
    ,\,
    c_1^{E,\infty}
    \,=\,
    c_1^E
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


