
The traditional concept of [[integration of differential forms]] over a [[compact space|compact]] [[smooth manifold]] $\Sigma$ applies in smooth families of differential forms and hence constitutes in fact a [[smooth function]] from the [[smooth set|smooth]] [[moduli space]] of [[differential forms]] on the given manifold, this is Def. \ref{ParameterizedIntegrationOfDifferentialForms} below.

Using this, [[transgression of differential forms]] may be defines as the application of the [[mapping space]]-[[functor]] out of $\Sigma$ to the [[modulating morphisms]] of [[differential forms]] and applying [[integration of differential forms]] to the result (Def. \ref{TransgressionOfDifferentialFormsToMappingSpaces} below). This simple construction turns out to be equivalent to the traditional definition (Prop. \ref{EquivalenceOfTransgressionOfDifferentialFormsToMappingSpaces} below).


+-- {: .num_defn #ParameterizedIntegrationOfDifferentialForms}
###### Definition
**(parameterized [[integration of differential forms]])

Let 

1. $X$ be a [[smooth set]];

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$, regarded as a [[smooth set]] via Example \ref{CartesianSpaceAsSmoothSpace}.

1. $n \geq k \in \mathbb{N}$ a [[natural number]];

Consider the [[smooth set|smooth]] [[mapping space]] $[\Sigma_k, \mathbf{\Omega}^n]$ (Def. \ref{SmoothFunctionSpace}) out of $\Sigma_k$ into the universal [[smooth set|smooth]] [[moduli space]] $\mathbf{\Omega}^n$ of [[differential n-forms]] (Prop. \ref{SmoothModuliSpaceOfnForms}).

Then we write

$$
  \int_{\Sigma}
    \;\colon\;
  [\Sigma_k, \mathbf{\Omega}^n]
    \longrightarrow
  \mathbf{\Omega}^{n-k}
$$

for the [[smooth function]] (Def. \ref{HomomorphismOfSmoothSpaces}) which takes a plot $\omega_{(-)} \colon U \to [\Sigma, \mathbf{\Omega}^k]$, hence equivalently a differential $n$-form $\omega_{(-)}(-)$ on $U \times \Sigma$, to the result of [[integration of differential forms]] over $\Sigma$:


$$
  \int_{\Sigma} \omega_{(-)}(-) \coloneqq \int_\Sigma \omega_{(-)}
  \,.
$$


=--


+-- {: .num_defn #TransgressionOfDifferentialFormsToMappingSpaces}
###### Definition
**([[transgression of differential forms]] to [[mapping spaces]])

Let 

1. $X$ be a [[smooth set]];

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$, regarded as a [[smooth set]] via Example \ref{CartesianSpaceAsSmoothSpace}.

1. $n \geq k \in \mathbb{N}$ a [[natural number]];

Consider the [[smooth set|smooth]] [[mapping space]] $[\Sigma_k, \mathbf{\Omega}^n]$ (Def. \ref{SmoothFunctionSpace}) out of $\Sigma_k$ into the universal [[smooth set|smooth]] [[moduli space]] $\mathbf{\Omega}^n$ of [[differential n-forms]] (Prop. \ref{SmoothModuliSpaceOfnForms}).


Then the operation of _[[transgression of differential n-forms]]_ on $X$ with respect to $\Sigma_k$ is the [[function]]

$$
  \tau_\Sigma
   \;\coloneqq\;
  \int_\Sigma [\Sigma,-]
   \;\colon\;
  \Omega^n(X) \to \Omega^{n-k}([\Sigma,X])
$$

from [[differential n-forms]] on $X$ to differential $n-k$-forms on the [[smooth set|smooth]] [[mapping space]] $[\Sigma_k,X]$ spring  which takes the differential form corresponding to the smooth function

$$
  (X \stackrel{\omega}{\to} \Omega^n) \in \Omega^n(X)
$$

to the differential form corresponding to the following composite smooth function:

$$
  \tau_\Sigma \omega
   \coloneqq
  \int_{\Sigma} [\Sigma,\omega]
   \;\colon\;
  [\Sigma, X] 
    \stackrel{[\Sigma, \omega]}{\longrightarrow}  
  [\Sigma, \Omega^n]
    \stackrel{\int_{\Sigma}}{\longrightarrow}
  \Omega^{n-k}
  \,,
$$

where $[\Sigma,\omega]$ is the [[mapping space]] [[functor]] on [[morphisms]] and $\int_{\Sigma}$ is the parameterized integration of differential forms from def. \ref{ParameterizedIntegrationOfDifferentialForms}.

More explicitly in terms of plots this means equivalently the following 

A plot of the [[mapping space]]

$$
  \phi_{(-)} \;\colon\; U \to [\Sigma, X] 
$$

is equivalently a [[smooth function]] of the form

$$
  \phi_{(-)}(-) \;\colon\; U \times \Sigma \to X
  \,.
$$

The smooth function $[\Sigma,\omega]$ takes this smooth function to the plot

$$
  U \times \Sigma \to X
   \overset{\phi_{(-)}(-)}{\longrightarrow}
  X 
   \overset{\omega}{\longrightarrow}
  \mathbf{\Omega}^{n}
$$

which is equivalently a differential form

$$
  (\phi_{(-)}(-))^\ast \omega \in \Omega^n(U \times \Sigma)
  \,.
$$

Finally the smooth function $\int_\Sigma$ takes this to the result of [[integration of differential forms]] over $\Sigma$:

$$
  \tau_{\Sigma}\omega\vert_{\phi_{(-)}}
  \;=\;
  \int_\Sigma (\phi_{(-)}(-))^\ast \omega
  \;\in\;
  \Omega^{n-k}(U)
  \,.
$$


=--


+-- {: .num_defn #TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap}
###### Definition
**([[transgression of differential forms]] to [[mapping space]] via [[evaluation map]])**

Let 

1. $X$ be a [[smooth set]];

1. $n \geq k \in \mathbb{N}$;

1. $\Sigma_k$ be a [[compact topological space|compact]] [[smooth manifold]] of [[dimension]] $k$.

Then the operation of _transgression of differential $n$-forms_ on $X$ with respect to $\Sigma$ is the [[function]]

$$
  \tau_\Sigma
   \coloneqq
  \int_\Sigma ev^\ast
   \;\colon\;
  \Omega^n(X)
    \overset{ev^\ast}{\longrightarrow} 
  \Omega^n(\Sigma \times [\Sigma, X])
    \overset{\int_\Sigma}{\longrightarrow}
  \Omega^{n-k}([\Sigma,X])
$$

from differential $n$-forms on $X$ to differential $n-k$-forms on the [[mapping space]] $[\Sigma,X]$ (Def. \ref{SmoothFunctionSpace}) which is the [[composition|composite]] of forming the [[pullback of differential forms]] along the [[evaluation map]] $ev \colon  [\Sigma, X] \times \Sigma \to X$ with [[integration of differential forms]] over $\Sigma$.

This construction manifestly extends to the [[smooth set]] of [[differential forms]]

=--



+-- {: .num_prop #EquivalenceOfTransgressionOfDifferentialFormsToMappingSpaces}
###### Proposition

The two definitions of [[transgression of differential forms]] to mapping spaces from def. \ref{TransgressionOfDifferentialFormsToMappingSpaces} and def. \ref{TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap} are equivalent.


=--

+-- {: .proof}
###### Proof


We need to check that for all plots $\gamma \colon U \to [\Sigma, X]$
the pullbacks of the two forms to $U$ coincide.

For def. \ref{TransgressionOfDifferentialFormsToMappingSpacesViaEvaluationMap} we get

$$
  \gamma^\ast \int_\Sigma \mathrm{ev}^\ast A
  =
  \int_\Sigma (\gamma,\mathrm{id}_\Sigma)^\ast \mathrm{ev}^\ast A
  \;
  \in \Omega^n(U)
$$

Here we recognize in the integrand the pullback along
the $( (-)\times \Sigma \dashv [\Sigma,-])$-[[adjunct]] $\tilde \gamma : U \times \Sigma \to \Sigma$ of $\gamma$,
which is given by applying the [[left adjoint]] $(-)\times \Sigma$ and then postcomposing with the adjunction counit $\mathrm{ev}$:

$$
  \array{
    U \times \Sigma
    &
     \overset{(\gamma, \mathrm{id}_\Sigma)}{\longrightarrow}
    &
    [\Sigma,X] \times \Sigma
    &
      \overset{\mathrm{ev}}{\longrightarrow}
    &
    X
  }
  \,.
$$
 
Hence the integral is now

$$
  \cdots = \int_{\Sigma} \tilde \gamma^\ast A
  \,.
$$

This is the operation of the top horizontal composite in the following
[[natural transformation|naturality square]] for [[adjuncts]], and so the claim follows by its [[commuting diagram|commutativity]]:

$$
  \array{
    \tilde \gamma \in 
    & 
    Hom(U \times\Sigma, X)
    &
      \overset{Hom(U \times \Sigma,A)}{\longrightarrow}
    &    
    Hom(U \times \Sigma, \mathbf{\Omega}^{n+k})
    &
      \overset{\int_\Sigma(U)}{\longrightarrow}
    &
    \Omega^n(U)
    \\
    &
    {}^{\mathllap{\simeq}}\big\downarrow
      &&
    {}^{\mathllap{\simeq}}\big\downarrow
      &&
    {}^{\mathllap{\simeq}}\big\downarrow
    \\
    \gamma \in 
    & 
    Hom(U,[\Sigma,X])
    &
      \overset{Hom(U,[\Sigma,A])}{\longrightarrow}
    &
    Hom(U,[\Sigma,\mathbf{\Omega}^{n+k}])
    &
      \overset{Hom(U,\int_\Sigma)}{\longrightarrow}
    & 
    Hom(U,\mathbf{\Omega}^n)
  }
$$

(here we write $Hom(-,-) \coloneqq Hom_{SmoothSet}(-,-)$ for the [[hom functor]] of [[smooth sets]]).

=--
