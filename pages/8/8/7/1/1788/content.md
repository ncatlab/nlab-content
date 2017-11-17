+-- {: .num_example #ModuliOfSDifferentialForms}
###### Example
**(universal [[smooth set|smooth]] [[moduli spaces]] of [[super differential forms]])**

For $n \in \mathbf{M}$ write 

$$
  \mathbf{\Omega}^n \;\in\; SuperSmoothSet
$$

for the [[super smooth set]] (def. \ref{SuperSmoothSetSuperCartesianSpaces}) whose set of plots
on a [[super Cartesian space]] $U \in SuperCartSp$ (def. \ref{SuperCartesianSpace})
is the set of [[super differential forms]] (def. \ref{DifferentialFormOnSuperCartesianSpaces})
of cohomolgical degree $n$

$$
  \mathbf{\Omega}^n(U) \;\coloneqq\; \Omega^n(U)
$$ 

and whose maps of plots is given by [[pullback of differential forms|pullback]] of super differential forms.

The [[de Rham differential]] on [[super differential forms]] applied plot-wise yields a morpism
of super smooth sets

$$
  \label{SuperUniversalDeRhamDifferential}
  d \;\colon\; \mathbf{\Omega}^n \longrightarrow \mathbf{\Omega}^{n+1}
  \,.
$$

As before in def. \ref{DifferentialFormsOnDiffeologicalSpaces} we then define 
for any [[super smooth set]] $X \in SuperSmoothSet$ its set of differential $n$-forms to be

$$
  \Omega^n(X)
   \;\coloneqq\;
  Hom_{SuperSmoothSet}(X,\mathbf{\Omega}^n)
$$

and we define the [[de Rham differential]] on these to be given by postcomposition with (eq:SuperUniversalDeRhamDifferential).

=--
