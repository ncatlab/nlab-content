
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

## Definition

### Invariant differential form

A [[differential form]] $\omega \in \Omega_{dR}^p(G)$ on a [[Lie group]] $G$ is called **left invariant** if for every $g \in G$ it is [[invariant]] under the [[pullback of differential forms]] 

\[
  \label{PullbackOfDifferentialFormIsDifferentialForm}
  (L_g)^* \omega = \omega
\]

along the left multiplication action 

$$
  \array{
    L_g \colon & G &\longrightarrow& G
    \\
    & x &\mapsto& g \cdot x
  }
$$

Analogously a form is **right invariant** if it is invariant under the pullback by right translations $R_g$. 

More generally, given a [[differentiable function|differentiable]] (e.g. [[smooth function|smooth]]) [[group action]] of $G$ on a [[differentiable manifold|differentiable]] (e.g. [[smooth manifold|smooth]]) manifold $M$

$$
  \array{
    G \times M 
    &
      \overset{\rho}{\longrightarrow}
    &
    M
    \\
    (g,x) &\mapsto& g \cdot x
  }
$$

then a [[differential form]] $\omega \in \Omega^p_{dR}(M)$ is called invariant if for all $g \in G$

$$
  \rho(g)^\ast(\omega) \;=\; \omega
  \,.
$$

This reduces to the left invariance (eq:PullbackOfDifferentialFormIsDifferentialForm) for $M = G$ and $\rho$ being the left multiplication action of $G$ on itself.


### Invariant vector field

For a vector field $X$ one instead typically defines the invariance via the pushforward $(T L_g) X = (L_g)_* X$.
Regarding that $L_g$ and $T_g$ are diffeomorphisms, both pullbacks and pushfowards (hence invariance as well) are defined for every tensor field;
and the two requirements are equivalent. 

## Related concepts

* [[invariant metric]]

* [[Maurer-Cartan form]]

* [[tangent Lie algebra]]



## References

See most textbooks on on [[Lie theory]], e.g.:

* [[Sigurdur Helgason]], *Differential geometry, Lie groups and symmetric spaces*, Graduate Studies in Mathematics **34** (2001) &lbrack;[ams:gsm-34](https://bookstore.ams.org/gsm-34)&rbrack;

* [[François Bruhat]] (notes by S. Ramanan): *Lectures on Lie groups and representations of locally compact groups*, Tata Institute Bombay (1958, 1968) &lbrack;[pdf](https://mathweb.tifr.res.in/sites/default/files/publications/ln/tifr14.pdf), [[Bruhat-LecturesOnLie.pdf:file]]&rbrack;

See also:

* page 89 (20 of 49) at *MIT course on Lie groups* ([pdf 2](http://ocw.mit.edu/courses/mathematics/18-755-introduction-to-lie-groups-fall-2004/lecture-notes/chap2_topic8to14.pdf))

* MathOverflow: *Construction of the Lie functor: left vs. right invariant vector fields on Lie groups and Lie groupoids* &lbrack;[MO:q/178528](https://mathoverflow.net/q/178528/381)&rbrack;



[[!redirects invariant differential forms]]

[[!redirects left invariant form]]
[[!redirects right invariant form]]
[[!redirects invariant vector field]]
[[!redirects invariant vector fields]]
[[!redirects left invariant vector field]]
[[!redirects right invariant vector field]]

[[!redirects left invariant differential form]]
[[!redirects left invariant differential forms]]
[[!redirects left-invariant differential form]]
[[!redirects left-invariant differential forms]]

[[!redirects left invariant form]]
[[!redirects left invariant forms]]

[[!redirects left-invariant differential 1-form]]
[[!redirects left-invariant differential 1-forms]]


[[!redirects left-invariant 1-form]]
[[!redirects left-invariant 1-forms]]
[[!redirects left invariant 1-form]]
[[!redirects left invariant 1-forms]]
[[!redirects left-invariant differential 1-form]]
[[!redirects left-invariant differential 1-forms]]
[[!redirects left invariant differential 1-form]]
[[!redirects left invariant differential 1-forms]]


[[!redirects left-invariant 2-form]]
[[!redirects left-invariant 2-forms]]
[[!redirects left invariant 2-form]]
[[!redirects left invariant 2-forms]]
[[!redirects left-invariant differential 2-form]]
[[!redirects left-invariant differential 2-forms]]
[[!redirects left invariant differential 2-form]]
[[!redirects left invariant differential 2-forms]]


