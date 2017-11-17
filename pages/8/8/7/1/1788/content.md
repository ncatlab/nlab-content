+-- {: .num_remark #PresymplecticCurrentInterpretation}
###### Remark
**([[presymplectic current]] is local version of ([[presymplectic form|pre-]])[[symplectic form]] of [[Hamiltonian mechanics]])**

In the simple but very common situation of example \ref{CanonicalMomentum}
the [[presymplectic current]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) takes the form (eq:CanonicalMomentum)

$$
  \Omega_{BFV}
   \;=\;
  \delta p_a^\mu
  \wedge
  \delta \phi^a
  \wedge
  \iota_{\partial_\mu} dvol_\Sigma
$$

with $\phi^a$ the [[field (physics)|field]] [[coordinates]] ("[[canonical coordinates]]")
and $p_a^\mu$ the "[[canonical momentum]]" (eq:CanonicalMomentumInCoordinates).

Notice that this is of the schematic form "$\delta p_a \wedge \delta q^a \wedge dvol_{\Sigma_p}$",
which is reminiscent of a [[symplectic form]] expressed in [[Darboux coordinates]] times 
a [[volume form]] for a $p$-dimensional [[manifold]]. Indeed, below in _[Phase space](#PhaseSpace)_
we discuss that this [[presymplectic current]]  _[[transgression of variational differential forms|transgresses]]_ (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces} below)
to a [[presymplectic form]] of the schematic form "$d P_a \wedge d Q^a$" on the [[on shell]] [[space of field histories]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime})
by [[integration of differential forms|integrating]] it over a [[Cauchy surface]]. In good situations
this [[presymplectic form]] is in fact a [[symplectic form]] on the [[on-shell]] [[space of field histories]],
in a suitable sense (theorem \ref{PPeierlsBracket} below).

This shows that the [[presymplectic current]] $\Omega_{BFV}$ is the [[local field theory|local]] (i.e. [[jet bundle|jet level]]) avatar of the
[[symplectic form]] familiar from the formulation of [[Hamiltonian mechanics]] in terms of [[symplectic geometry]]:

In fact prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell} may be read as saying that 
the [[presymplectic current]] is a _[[conserved current]]_ (def. \ref{SymmetriesAndConservedCurrents} below),
only that it takes values not in [[smooth functions]] of the field coordinates and jets, but in
[[variational differential form|variational 2-forms]] on fields. There is a [[conserved charge]] associated with
every [[conserved current]] (prop. \ref{ConservedCharge} below) and the conserved charge associated with the
[[presymplectic current]] will be seen to be the ([[presymplectic form|pre-]])[[symplectic form]] on the [[phase space]]
of the field theory (def. \ref{PhaseSpaceAssociatedWithCauchySurface} below).

=--
