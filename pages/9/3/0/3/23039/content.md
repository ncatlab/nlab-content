
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Mapping spaces
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[compact Lie group]] and $\Gamma$ any [[Lie group]], every [[group homomorphisms]] $\phi \,\colon\, G \xrightarrow{\;} \Gamma$ (as [[topological groups]], [[continuous homomorphisms of Lie groups are smooth|hence]] as [[Lie groups]]) has a [[neighbourhood]] (in the homomorphism-[[subspace]] of the [[compact open topology]]) all whose elements $\phi'$ are [[conjugation|conjugate]] to $\phi$, in that for each there exists $\gamma \,\in\, \Gamma$ such that $\phi'(-) \,=\,   \gamma^{-1} \cdot \phi(-) \cdot \gamma$ ([Conner & Floyd 1964, Lem. 31.8](#ConnerFloyd64), [Rezk  et al. 2013](#Rezk13)).

It follows (highlighted in [Rezk 2014, Rem. 2.2.1](#Rezk14)) that the [[quotient space]] of the homomorphism space $Hom(G,\Gamma) \,\subset\, Maps(G,\Gamma)$ under the [[adjoint action]] by $\Gamma$ is [[discrete topological space|discrete]]:

\[
  \label{DiscreteQuotientSpace}
  Hom(G,\Gamma)/_{\!\!ad} \Gamma
  \;\;\;
  \in
  Set
  \xhookrightarrow{\;}
  TopSp
  \,,
\]

and that the homomorphism space itself decomposes, as a [[topological G-space|$\Gamma$-space]] via the [[adjoint action]], into the [[disjoint union]], [[indexed set|indexed]] by (eq:DiscreteQuotientSpace), of the [[coset spaces]] of $\Gamma$ by the corresponding [[centralizer subgroups]] $C_\Gamma(\phi) \subset \Gamma$:


\[
  Hom(G,\Gamma)
  \;\simeq\;
  \underset{ 
    {[\phi] \, \in }
    \atop
    \mathclap{ Hom(G,\Gamma)/\Gamma }
  }{\bigsqcup}
  \Gamma/C_{{}_{\Gamma}}(\phi)
  \;\;\;
  \in
  \;
  G Act(TopSp)
  \,.
\]

## Examples

\begin{example}\label{Pontrjagin duality}
**([[Pontrjagin duality]])**
\linebreak
  In the special case that $\Gamma = S^1$ is the [[circle group]] and $G$ is an [[abelian group]], the homomorphism space $\widehat G \,\coloneqq\, Hom(G,S^1)$ is the [[Pontrjagin dual]] of $G$.

In this case, since $S^1$ is [[abelian group|abelian]] so that the [[conjugation action]] on $Hom(G,S^1)$ is [[trivial action|trivial]], the statement (eq:DiscreteQuotientSpace) is a special case of the classical fact that the [[Pontrjagin dual]] of a [[compact topological group]] is [[discrete group|discrete]] (see [there](Pontrjagin+dual#BasicPropertiesOfDualGroups)).
\end{example}


## Related concepts

* [[Hilbert's fifth problem]]


## References

* {#ConnerFloyd64} [[Pierre Conner]], [[Edwin Floyd]], Ch. III, Lem. 38.1 in: _Differentiable periodic maps_, Ergebnisse der Mathematik und ihrer Grenzgebiete **33**, Springer 1964 ([doi:10.1007/978-3-662-41633-4](https://link.springer.com/book/10.1007/978-3-662-41633-4))

* {#Rezk13} [[Charles Rezk]], *Nearby homomorphisms from compact Lie groups are conjugate*, 2013 ([MO:q/123624](https://mathoverflow.net/q/123624/381))

* {#Rezk14} [[Charles Rezk]], Rem. 2.2.1 in: *[[Global Homotopy Theory and Cohesion]]*, 2014 ([pdf](http://www.math.uiuc.edu/~rezk/global-cohesion.pdf), [[Rezk14.pdf:file]])




