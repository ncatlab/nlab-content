
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

For $G$ a [[compact Lie group]] and $\Gamma$ any [[Lie group]], every [[group homomorphisms]] $\phi \,\colon\, G \xrightarrow{\;} \Gamma$ (as [[topological groups]], [[continuous homomorphisms of Lie groups are smooth|hence]] as [[Lie groups]]) has a [[neighbourhood]] $U_\phi$ (in the homomorphism-[[subspace]] of the [[compact open topology]]) all whose elements $\phi'$ are [[conjugation|conjugate]] to $\phi$, in that 

\[
  \label{ExistenceOfConjugationsForNearbyHomomorphisms}  
  \underset{
    \phi' \in U_{\phi}
  }{\forall}
  \;\;\;
  \underset{
    \gamma \in \Gamma
  }{\exists}
  \;\;\;\;\;\;\;
  \phi'(-) 
    \,=\,   
  \gamma^{-1} \cdot \phi(-) \cdot \gamma
  \,.
\]

([Conner & Floyd 1964, Lem. 31.8](#ConnerFloyd64), [Rezk  et al. 2013](#Rezk13)).

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

and that the homomorphism space itself decomposes, as a [[topological G-space|$\Gamma$-space]] via the [[adjoint action]], into the [[disjoint union]], [[indexed set|indexed]] by (eq:DiscreteQuotientSpace), of the [[coset spaces]] of $\Gamma$ by the corresponding [[stabilizer subgroups]] ("[[centralizer subgroups]]") $C_\Gamma(\phi) \subset \Gamma$:


\[
  \label{DisjointUnionOfOrbits}
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
  \Gamma Act(TopSp)
  \,.
\]


## Examples

\begin{example}\label{Pontrjagin duality}
**([[Pontrjagin duality]])**
\linebreak
  In the special case that $\Gamma = S^1$ is the [[circle group]] and $G$ is an [[abelian group]], the homomorphism space $\widehat G \,\coloneqq\, Hom(G,S^1)$ is the [[Pontrjagin dual]] of $G$.

In this case, since $S^1$ is [[abelian group|abelian]] so that the [[conjugation action]] on $Hom(G,S^1)$ is [[trivial action|trivial]], the statement (eq:DiscreteQuotientSpace) is a special case of the classical fact that the [[Pontrjagin dual]] of a [[compact topological group]] is [[discrete group|discrete]] (see [there](Pontrjagin+dual#BasicPropertiesOfDualGroups)).
\end{example}

## Variants

### For crossed homomorphisms
 {#ForCrossedHomomorphisms}

Let 

$$
  \alpha 
    \;\colon\; 
  G 
    \xrightarrow{\;}
  Aut_{Grp}(\Gamma)
$$

be a [[group action]] by [[group homomorphism|group]] [[automorphisms]], with the special property that its restriction to the [[center of a group|center]] $C(G) \subset G$ is [[trivial action|trivial]] (for example when $G$ has [[trivial group|trivial]] center to start with):

$$
  \alpha_{\vert C(G)}
  \;=\;
  id_{\Gamma}
  \,.
$$

In that case the above statement (eq:ExistenceOfConjugationsForNearbyHomomorphisms) generalizes to say that *nearby [[crossed homomorphisms]] are [crossed conjugate](crossed+homomorphism#AdjointActionOnCrossedHomomorphisms).


More precisely, notice ([this Prop.](crossed+homomorphism#CrossedHomomorphismsAreSplittingsOfTheSemidirectProductGroup)) that  a [[crossed homomorphism]] $\phi \;\colon\; G \xrightarrow{\;} \Gamma$ is equivalently 
a plain [[group homomorphism]] $(\phi(-),\,(-)) \,\colon\, G \xrightarrow{\;} \Gamma \rtimes G$ to the [[semidirect product group]], subject to the constraint that its projection to $G$ is the [[identity morphism]].
Now say that another crossed homomorphism $\phi'$ is nearby if it is so as a plain homomorphism $(\phi'(-),(-))$ to the semidirect product group (i.e. we consider [[neighbourhoods]] of crossed homomorphism in the sense of neighbourhoods of the points which they represent in $Hom(G,\Gamma \rtimes G))$.


Then the above statement (eq:ExistenceOfConjugationsForNearbyHomomorphisms) says that there is an element $(\gamma,\,h) \,\in\, \Gamma \rtimes G$ such that

\[
  \label{ConjugationOfHomomorphismsToSemidirectProductGroup}
  \underset{g \in G}{\forall}
  \;\;\;\;\;
  \big(
    \phi'(g),\,g
  \big)
  \;\;
  =
  \;\;
  \big(
    \gamma, \, h
  \big)^{-1}
  \cdot
  \big(
    \phi(g),\,g
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)
  \,.
\]

In order for such a conjugation to be a [crossed conjugation](crossed+homomorphism#AdjointActionOnCrossedHomomorphisms) of $\phi$ to $\phi'$, we need its $G$-component to be the [[neutral element]]: $h = \mathrm{e} \,\in\, G$.

Now, the further conjugation of (eq:ConjugationOfHomomorphismsToSemidirectProductGroup) by $\big(\mathrm{e},\,h^{-1}\big)$ yields:

$$
  \Big(
    \alpha(h^{-1})
    \big(
      \phi'(g)
    \big)
    ,\, g
  \Big)
  \;\;
  =
  \;\;
  \big(
    \mathrm{e},\, h 
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)^{-1}
  \cdot
  \big(
    \phi(g),\,g
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)
  \cdot
  \big(
    \mathrm{e},\, h^{-1} 
  \big)
  \,.
$$

But we know that $h \in C(G)$ is in the [[center of a group|center]] of $G$, since the projection of both sides of (eq:ConjugationOfHomomorphismsToSemidirectProductGroup) to $G$ must be the identity, by construction of crossed homomorphisms. 

Therefore, by the assumption that the action of $G$ on $\Gamma$ restricts along the inclusion $C(G) \xhookrightarrow{\;} G$ to the [[trivial action]],
we have $\alpha(h^{-1})\big( \phi(g) \big) \,=\, \phi(g)$ and it follows that

$$
  \big(
    \gamma, \, h
  \big)
  \cdot
  \big(
    \mathrm{e},\, h^{-1} 
  \big)
  \;\;
  =
  \;\;
  \big(
    \gamma, \, \mathrm{e}
  \big)  
$$

exhibits the required crossed conjugation:

$$
  \phi'(-) \;=\;  \gamma^{-1} \cdot \phi(-) \cdot \alpha(-)(\gamma)
  \,.
$$

### For non-Lie groups
 {#ForNonCompactGroups}

* While the [[projective unitary group]] $\Gamma \,\coloneqq\,$ [[PU(ℋ)]] on a [[separable Hilbert space]] $\mathcal{H}$ is not a (finite-dimensional) [[Lie group]] and hence outside the scope of assumption for the above general theorem, the conclusion still holds, at least for $G$ [[discrete group|discrete]], hence [[finite group|finite]]:

  The [[PU(ℋ)]][[G-space|-space]] of homomorphisms $Hom\big(G,\, PU(\mathcal{H})\big)$ is a [[disjoint union]] (eq:DisjointUnionOfOrbits) of [[orbits]] of the [[conjugation action]].

  This is established in [Uribe & Lück 2013, Sec. 15](universal+equivariant+PUH-bundle#UribeLueck13), [p. 38](https://arxiv.org/pdf/1304.4862.pdf#page=38).

## Related concepts

* [[Hilbert's fifth problem]]


## References

* {#ConnerFloyd64} [[Pierre Conner]], [[Edwin Floyd]], Ch. III, Lem. 38.1 in: _Differentiable periodic maps_, Ergebnisse der Mathematik und ihrer Grenzgebiete **33**, Springer 1964 ([doi:10.1007/978-3-662-41633-4](https://link.springer.com/book/10.1007/978-3-662-41633-4))

* {#Rezk13} [[Charles Rezk]], *Nearby homomorphisms from compact Lie groups are conjugate*, 2013 ([MO:q/123624](https://mathoverflow.net/q/123624/381))

* {#Rezk14} [[Charles Rezk]], Rem. 2.2.1 in: *[[Global Homotopy Theory and Cohesion]]*, 2014 ([pdf](http://www.math.uiuc.edu/~rezk/global-cohesion.pdf), [[Rezk14.pdf:file]])

See also:

* [[Alejandro Adem]], [[Frederick R. Cohen]], Lemma 2.5 in: *Commuting Elements and Spaces of Homomorphisms*, Math. Ann. **338** (2007) 587–626 ([arXiv:math/0603197](https://arxiv.org/abs/math/0603197), [doi:10.1007/s00208-007-0089-z](https://doi.org/10.1007/s00208-007-0089-z))


* [[Charles Rezk]], *Classifying spaces for 1-truncated compact Lie groups*, Algebr. Geom. Topol. 18 (2018) 525-546 ([arXiv:1608.02999](https://arxiv.org/abs/1608.02999), [doi:10.2140/agt.2018.18.525](https://doi.org/10.2140/agt.2018.18.525))



[[!redirects nearby homomorphisms are conjugate]]

