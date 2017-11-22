

+-- {: .num_prop #WaveFronSetsForKGPropagatorsOnMinkowski}
###### Proposition
**([[wave front sets]] of [[propagators]] of [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The [[wave front set]] of the various [[propagators]] for the [[Klein-Gordon equation]] on [[Minkowski spacetime]], regarded, via [[translation]] [[invariant|invariance]], as [[distributions]] in a single variable, are as follows:

* the [[causal propagator]] $\Delta_S$ (prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}) has wave front set all pairs $(x,k)$ with $x$ and $k$ both on the lightcone:

  $$
     WF(\Delta_S) = \left\{ (x,k) \,\vert\, {\vert x\vert}^2_\eta = 0 \;\text{and} \; {\vert k\vert}^2_\eta = 0 \; \text{and} \, k \neq 0  \right\}
  $$

* the [[Hadamard propagator]] $\Delta_H$ (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime}) has wave front set all pairs $(x,k)$ with $x$ on the light cone and $k^0 \gt 0$:


  $$
    WF(\Delta_H) = \left\{ (x,k) \,\vert\, {\vert x\vert}^2_\eta = 0 \;\text{and} \; {\vert k\vert}^2_\eta = 0 \; \text{and} \; k^0 \gt 0   \right\}
  $$


=--


+-- {: .proof}
###### Proof idea

Regarding the causal propagator:

By prop. \ref{SingularSupportOfCausalPropagatorForKleinGordonEquationOnMinkowskiSpacetimeIsTheLightCone} the [[singular support]] of $\Delta_S$ is the [[light cone]].  

Let $b \in C^\infty_{cp}(\mathbb{R}^{p,1})$ be a [[bump function]] whose [[compact support]] includes the origin.

For $a \in \mathbb{R}^{p,1}$ a point on the light cone, we need to determine the decay property of the Fourier transform of $x \mapsto b(x-a)\Delta_S(x)$. This is the [[convolution of distributions]] of $\hat b(k)e^{i k_\mu a^\mu}$ with $\widehat \Delta_S(k)$. By prop. \ref{CausalPropagatorAsFourierTransformOfDeltaDistributionOnTransformedKGOperator} we have

$$
  \widehat \Delta_{S}(k)
  \;\propto\;
  \delta\left( -k_\mu k^\mu - \left( \tfrac{m c}{\hbar} \right)^2 \right)
  sgn(k_0)
  \,.
$$

This means that the convolution product is the smearing of the mass shell by $\widehat b(k)e^{i k_\u a^\mu}$.

Since the mass shell asymptotes to the light cone, and since $e^{i k_\mu a^\mu} = 1$ for $k$ on the light cone (given that $a$ is on the light cone), this implies immediately that all $k$ on the light cone are in the wave front set at the point $a$.

It remains to see that no other wave vctors $k$ are in the wave front set. But if $k$ is not on the light cone, the for large constants $c$ the product $c k$ has arbitrary large distance form the light cone. Since $\widehat b$ is a [[rapidly decreasing function]], it fllows (..?..) that the convolution of the mass shell with $\widehat b$ is rapidly decreasing with distance from the light cone, hence rapidly decreasing along all $k$ not on the light cone.


Now for the [[Hadamard propagator]]:

By def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} its Fourier transform is of the form

$$
  \widehat \Delta_H(k)
  \;\propto\;
  \delta\left( k_\mu k^\mu + m^2 \right) \Theta( -k_0 )
$$

First of all it follows that the singular support is still the light cone, because this means that $\Delta_H$ is a [[convolution of distributions]] of $\Delta_S$ with $\widehat {\Theta} \propto \delta'$, and this convolution does not increase the singular support (...).

Therefore now same argument as before says that the wave front set consists of wave vectors $k$ on the light cone, but now due to the [[step function]] factor $\Theta(-k_0)$ now they must be in only one of the two branches.

=--








