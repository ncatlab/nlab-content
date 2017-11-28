
We discuss this for the purely bosonic case. The fermionic case follows by parameterizing over superpoints

By def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} a field history
$\Phi \in \Gamma_\Sigma(E)$ is [[on-shell]] precisely if for all smooth collections $\Phi_{(-)} \colon U \to \Gamma_\Sigma(E)$
with $\Phi_{u = 0} = \Phi$ we have

$$
  j^\infty_\Sigma(\Phi_{(-)})^\ast(\delta_{EL}\mathbf{L})\vert_{u = 0} = 0
  \,.
$$

This is the case precisely if for
all [[bump functions]] $b \in C^\infty_{cp}(\Sigma)$ the [[integration of differential forms|integral]]
over $\Sigma$ of the product with $b$ vanishes:


$$
  \int_\Sigma 
    b \, j^\infty_\Sigma(\Phi_{(-)})^\ast(\delta_{EL}\mathbf{L})  \vert_{u = 0}
  \;=\;
  0
  \;\in\;
  T^\ast_0 U
  \,.
$$

Hence we need to show that this holds true also for all values $t$ of the flow parameter
if it holds at $t = 0$, hence that the above implies for  all bump functions $b$ that

$$
  \begin{aligned}
    \int_\Sigma
    b
    \left(
      \exp(t \hat v)
        \circ
      j^\infty_\Sigma(\Phi_{(-)})
    \right)^\ast (\delta_{EL}\mathbf{L})
    \vert_{u = 0}
    & =
    \int_\Sigma
      b
      (j^\infty_\Sigma(\Phi(-)))^\ast
      \exp(t \hat v)^\ast
      (\delta_{EL}\mathbf{L})
      \vert_{u = 0}
    \\
    & =
    0
    \,,
  \end{aligned}
$$

where we used (eq:PullbackOfDifferentialFormsCompatibleWithComposition).

for all $t \in \mathbb{R}^1$. But since we know it holds true at one point $t = 0$,
it is in fact sufficient to show that the [[derivative]] of this smooth family of
differential forms with respect to $t$ vanishes at all $t$. This argument in turn is
the same at $t = 0$ as at any other value, so we consider the derivative at $t = 0$.

Now by definition of [[Lie derivatives]], the derivative of the above expression with respect to $t$ at $t = 0$ is given
by the Lie derivative $\mathcal{L}_{\hat v}$ via

$$
    \frac{d}{d t }
    \int_\Sigma
    \left(
        (j^\infty_\Sigma(\Phi_{(-)}))^\ast
        \exp(t \hat v)^\ast
        (\delta_{EL}\mathbf{L})
    \right)
    \vert_{ {u = 0} \atop { t = 0 } }
    =
    \int_\Sigma
    (j^\infty_\Sigma(\Phi(-)))^\ast
    \underset{= d (\iota_{\hat v}\Omega_{BFV} -\delta J_v)  }{
    \underbrace{
     \mathcal{L}_{\hat v}
     \delta_{EL}\mathbf{L}
     }}
     \vert_{u = 0}
  \,.
$$

We compute that the Lie derivative has the value indicated under the braces as follows:

$$
  \begin{aligned}
     \mathcal{L}_{\hat v} \delta_{EL}\mathbf{L}
     & =
     \iota_{\hat v}
       \underset{ = - d\Omega_{BFV} }{\underbrace{\delta \delta_{EL} \mathbf{L}} }
     + \delta \,\underset{= d J_v}{\underbrace{\iota_{\hat v} \delta_{EL}\mathbf{L}}}
     \\
     & =
     - \iota_{\hat v} d\Omega_{BFV}  + \delta d J_v
     \\
     & =
     d \left(\iota_{\hat v} \Omega_{BFV} - \delta J_v \right)
  \end{aligned}
$$

Here we first used [[Cartan's homotopy formula]] for evolutionary vector fields (eq:HomotopyFormulaForLieDerivativeAlongProlongationOfEvolutionaryVectorField),
then, under the braces,
the [[conserved current]] property of the presymplectic current (prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}) as well as [[Noether's theorem|Noether's theorem I]] (prop. \ref{NoethersFirstTheorem}),
and finally
the defining verticality condition of prolongations of evolutionary vector fields (prop. \ref{EvolutionaryVectorFieldProlongation})
as well as the anti-commutativity of $\delta$ and $d$.

Hence continuing the computation of the derivative above we have

$$
  \begin{aligned}
    \frac{d}{d t }
    \int_\Sigma
    \left(
        (j^\infty_\Sigma(\Phi(-)))^\ast
        \exp(t \hat v)^\ast
        (\delta_{EL}\mathbf{L})
    \right)
    \vert_{ { u = 0} \atop  { t = 0 } }
    & =
    -
    \int_\Sigma
    (j^\infty_\Sigma(\Phi(-)))^\ast
    d (\iota_{\hat v} \Omega_{BFV} - \delta J_v) \vert_{u = 0}
    \\
    & =
    - \int_\Sigma d j^\infty_\Sigma(\Phi(-))^\ast (\iota_{\hat v}\Omega_{BFV} -  \delta J_v) \vert_{u = 0}
    \\
    & = 0
  \end{aligned}
$$

by prop. \ref{PullbackAlongJetProlongationIntertwinesHorizontalDerivative}.


=--
