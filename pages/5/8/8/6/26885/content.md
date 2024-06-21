
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


\tableofcontents

## Idea

Given a [[differentiable map]] $\phi \colon X_1 \xrightarrow{\;} X_2$ between [[differentiable manifolds]] (e.g. a [[smooth map]] between [[smooth manifolds]]) and thinking of [[vector fields]] as infinitesimal approximations to differentiable [[curves]] 

$$
  T_x X
    \;\simeq\;
  \big\{
    \gamma \in C^\infty\big(\mathbb{R},\, X\big)
    \,\big\vert\,
    \gamma(0) = x
  \big\}
    \Big/
  \big(
    \gamma_1 \sim \gamma_2 
      \;\Leftrightarrow\;
    \mathrm{d}\gamma_1(0) = \mathrm{d}\gamma_2(0)
  \big)
$$

then the [[postcomposition]] of these curves with $\phi$ induces maps of [[equivalence classes]]

$$
  \begin{array}{ccc}
    T_x X_1 &\xrightarrow{\phantom{--}}& T_{\phi(x)} X_2
    \\
    [\gamma] &\mapsto& [\phi \circ \gamma]
  \end{array}
$$

alternatively denoted "$\phi_\ast$" or "$\mathrm{d}\phi$" (cf. *[differentiation as a functor](differentiation#AsAFunctor)*) and called the *pushforward* of vector fields along $\phi$.

## Related concept

* The [[duality|dual]] notion is that of *[[pullback of differential forms]]*.

## Literature

Most texts on [[differential geometry]] will discuss pushforward of vector fields.

See also

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Pushforward_(differential)">Pushforward_(differential)</a>*

[[!redirects pushforward of vector fields]]

[[!redirects pushforward of a vector field]]
[[!redirects pushforwards of a vector field]]



