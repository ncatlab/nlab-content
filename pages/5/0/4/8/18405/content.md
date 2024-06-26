
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[tangent vector field]] on a [[differentiable manifold]] $X$ then its _flow_ is the [[group]] of [[diffeomorphisms]] of $X$ that lets the points of the manifold "flow along the vector field" hence which sends them along _flow lines_ (integral curves) that are tangent to the vector field. 

Integral curves generalize to *integral sections* for [[multivector field|multivector fields]]. See there for more.


## Definition

### Traditional definition

Throughout, let $X$ be a [[differentiable manifold]] and let $v \in \Gamma(T X)$ be a continuously differentiable [[vector field]] on $X$ (i.e. of class $C^1$).


+-- {: .num_defn #IntegralCurve}
###### Definition
**(integral curves/flow lines)**


An _integral curve_ or _flow line_ of the vector field $v$ is a [[differentiable function]] of the form

$$
  \gamma
    \;\colon\;
    U
    \longrightarrow
  X    
$$

for $U \subset \mathbb{R}$ an [[open interval]]  with the property that its [[tangent vector]] at any $t \in U$ equals the value of the vector field $v$ at the point $\gamma(t)$:

$$
  \underset{t \in U}{\forall}
  \left(
     d \gamma_t = v_{\gamma(t)}
  \right)
  \,.
$$

=--

+-- {: .num_defn #FlowOfAVectorField}
###### Definition
**(flow of a vector field)**

A _global flow_ of $v$ is a function of the form

$$
  \Phi \;\colon\; X \times \mathbb{R} \longrightarrow X
$$

such that for each $x \in X$ the function $\phi(x,-) \colon \mathbb{R} \to X$ is an integral curve of $v$ (def. \ref{IntegralCurve}).

A _flow domain_ is an open subset $O \subset X \times \mathbb{R}$ such that for all $x \in X$ the intersection $O \cap \{x\} \times \mathbb{R}$ is an [[open interval]] containing $0$. 

A _flow_ of $v$ on a flow domain $O \subset X \times \mathbb{R}$ is a differentiable function 

$$
  X \times \mathbb{R} \supset O \overset{\phi}{\longrightarrow} X
$$ 

such that for all $x \in X$ the function $\phi(x,-)$ is an integral curve of $v$ (def. \ref{IntegralCurve}).


=--

+-- {: .num_defn #CompleteVectorField}
###### Definition
**(complete vector field)

The vector field $v$ is called a _complete vector field_ if it admits a global flow (def. \ref{FlowOfAVectorField}).


=--

### Synthetic definition
 {#SyntheticDefinition}

In [[synthetic differential geometry]] a [[tangent vector field]] is a morphism $v \colon X \to X^D$ such that

$$
  \array{
    && X^D 
    \\
    & {}^{\mathllap{v}}\nearrow & \downarrow^{\mathrlap{X^{\ast \to D}}}
    \\
    X &=& X
  }
$$

The [[internal hom]]-[[adjunct]] of such a morphism is of the form

$$
  \tilde v \;\colon\; D \longrightarrow X^X
  \,.
$$

If $X$ is sufficiently nice (a [[microlinear space]] should be sufficient) then this morphism factors through the internal [[automorphism group]] $\mathbf{Aut}(X)$ inside the internal [[endomorphisms]] $X^X$

$$
  \tilde v \;\colon\; D \longrightarrow \mathbf{Aut}(X) \hookrightarrow X^X
  \,.
$$

Then a group homomorphism 

$$
  \phi_v \;\colon\; (R,+) \longrightarrow \mathbf{Aut}(X)
$$

with the property that restricted along any of the affine inclusions $D \hookrightarrow \mathbb{R}$ it equals $\tilde v$

$$
  \array{
     D &\hookrightarrow& \mathbb{R}
     \\
     & {}_{\mathllap{\tilde v}}\searrow & \downarrow^{\mathrlap{\phi}}
     \\
     && \mathbf{Aut}(X) &\hookrightarrow& X^X
  }
$$

is a _flow_ for $v$.

## Properties

+-- {: .num_prop }
###### Proposition

Let $\phi$ be a global flow of a vector field $v$ (def. \ref{FlowOfAVectorField}). This yields an [[action]] of the additive group $(\mathbb{R},+)$ of [[real numbers]] on the [[differentiable manifold]] $X$ by [[diffeomorphisms]], in that 

* $\phi_v(-,0) = id_X$;

* $\phi_n(-,t_2) \circ \phi_v(-,t_1) = \phi_v(-, t_1 + t_2)$;

* $\phi_v(-,-t) = \phi_v(-,t)^{-1}$.

=--

+-- {: .num_prop}
###### Proposition
**(fundamental theorem of flows)**

Let $X$ be a [[smooth manifold]] and $v \in \Gamma(T X)$ a smooth [[vector field]]. Then $v$ has a unique maximal flow (def. \ref{FlowOfAVectorField}).

This unique flow is often denoted $\phi_v$ or $\exp(v)$ (see also at _[[exponential map]]_).

=--

e.g. [Lee, theorem 12.9](#Lee)

+-- {: .num_prop }
###### Proposition

Let $X$ be a [[compact topological space|compact]] [[smooth manifold]]. Then every smooth [[vector field]] $v \in \Gamma(T X)$ is a complete vector field (def. \ref{CompleteVectorField}) hence has a global flow (def. \ref{FlowOfAVectorField}).

=--

e.g. [Lee, theorem 12.12](#Lee)

## References

* {#Lee} John Lee, chapter 12 "Integral curves and flows" of _Introduction to smooth manifolds_ ([pdf](http://webmath2.unito.it/paginepersonali/sergio.console/lee.pdf))

[[!redirects flows of a vector field]]

[[!redirects flow]]
[[!redirects flows]]
[[!redirects flow line]]
[[!redirects flow lines]]


[[!redirects integral curve]]
[[!redirects integral curves]]

