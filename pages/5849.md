

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An **adjoint quadruple** is a sequence of three [[adjunctions]]

$$
  f_! \dashv f^* \dashv f_* \dashv f^!
$$

between a [[quadruple]] of [[morphisms]].  That is, it is an [[adjoint string]] of length 4.

## Properties

### General

Every adjoint quadruple 

$$
  (f_! \dashv f^* \dashv f_* \dashv f^!)
  :
  C 
    \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\stackrel{\overset{f_*}{\to}}{\underset{f^!}{\leftarrow}}}}
  D
$$ 

induces an [[adjoint triple]] on $C$


$$
  (f^* f_! \dashv f^* f_* \dashv f^! f_*)
  :
  C \to C
  \,,
$$

(hence a [[monad]] [[left adjoint]] to a [[comonad]] left adjoint to a monad) and an adjoint triple

$$
  (f_! f^* \dashv f_* f^* \dashv f_* f^!) : D \to D
$$

on $D$.

Since moreover every [[adjoint triple]] $(F \dashv G \dashv H)$ induces an [[adjoint functor|adjoint pair]] $(G F \dashv G H)$ and an adjoint pair $(F G \dashv H G)$, the adjoint quadruple above induces four adjoint pairs, such as 

$$
  (f^* f_* f^* f_! \dashv f^* f_* f^! f_*) : C \to C
  \,.
$$

### Canonical natural transformations

Let $(p_! \dashv p^* \dashv p_*\dashv p^!) : \mathcal{E} \to \mathcal{S}$ be an  [[adjoint quadruple]] of [[adjoint functor]]s such that $p^*$ and $p^!$ are [[full and faithful functor]]s. We record some general properties of such a setup.

We write 

$$
  \iota : id \to p^* p_!
$$

etc. for [[unit of an adjunction|units]] and

$$
  \eta : p_! p^* \to id
$$

etc. for counits.

+-- {: .num_prop #TheCanonicalMorphisms}
###### Proposition/Definition

We have [[commuting diagram]]s, [[natural transformation|natural]] in $X \in \mathcal{E}$, $S \in \mathcal{S}$

$$
  \array{
    p_*X  &\stackrel{\eta_{p^* X}^{-1}}{\to}& p_! p^* p_*X
    \\
    {}^{\mathllap{p_*(i_X)}}\downarrow 
    &\searrow^{\mathrlap{\theta_X}}& 
    \downarrow^{\mathrlap{p_!(\eta_X)}}
    \\
    p_* p^* p_! X &\stackrel{\iota_{p_!X}^{-1}}{\to}& p_! X
  }
$$

and

$$
  \array{
    p^* S &\stackrel{\iota_{p^* S}}{\to}& p^! p_* p^* S
    \\
    {}^{\mathllap{p^* \epsilon_S^{-1}}}\downarrow 
    &\searrow^{\mathrlap{\phi_X}}& \downarrow^{\mathrlap{p^!(\iota_S^{-1})}}
    \\
    p^* p_* p^!S  &\stackrel{{\epsilon}_{p_!S }}{\to}& p^!S
  }
  \,.
$$

where the diagonal morphisms

$$
  \theta_X : p_* X \to p_! X
$$

and 

$$
  \phi_S : p^* S \to p^! S
$$

are defined to be the equal composites of the sides of these diagrams.

=--

This appears as ([Johnstone, lemma 2.1, corollary 2.2](#Johnstone)).

+-- {: .un_prop #TheEpiAndTheMono}
###### Proposition

The following conditions are equivalent:


* for all $X \in \mathcal{E}$ the morphism $\theta_X : p_*X \to p_! X$ is an [[epimorphism]];

* for all $S \in \mathcal{S}$, the morphism $\phi_S : p^*S \to p^! S$ 
  is a [[monomorphism]];

* $p_*$ is [[faithful functor|faithful]] on morphisms of the form $A \to p^* S$.

=--

This appears as ([Johnstone, lemma 2.3](#Johnstone)).



+-- {: .proof}
###### Proof

By the above definition, $\phi_S$ is a [[monomorphism]] precisely if $\iota_{p^* S} : p^* S \to p^! p_* p^* S$ is. This in turn is so (see [[monomorphism]]) precisely if the first [[function]] in

$$  
    \mathcal{E}(A,p^* X) 
     \stackrel{(\iota_{p^* X}) \circ (-)}{\to} 
    \mathcal{E}(A, p^! p_* p^* S)
     \stackrel{\simeq}{\to}
    \mathcal{S}(p_* A, p_* p^* S)
$$

and hence the composite is a monomorphism in [[Set]].

By definition of [[adjunct]] and using the $(p_* \dashv p^!)$-[[zig-zag identity]], this is equal to the action of $p_*$ on morphisms

$$
  (\iota_{p^* X}) \circ (-)  : 
  (A \to p^* S) \mapsto p_*(A \to p^* S)  
  \,.
$$

Similarly, by the above definition the morphism $\theta_X$ is an epimorphism precisely if $p_!(\eta_X) : p_! p^* p_* X \to p_! X$ is so, which is the case precisely if the top morphism in

$$
  \array{
    \mathcal{S}(p_! X, S) 
      &\stackrel{(-) \circ p_!(\eta_X)}{\to} &
    \mathcal{S}(p_! p^* p_* X, S)
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    && \mathcal{E}(p^* p_* X, p^* S)
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    \mathcal{E}(X, p^* S) &\stackrel{p_*}{\to}& \mathcal{S}(p_* X, p_* p^* S)
  }
$$

and hence the bottom morphism is a monomorphism in [[Set]],
where again the commutativity of this diagram follows from the 
definition of [[adjunct]] and the 
$(p_! \dashv p^*)$-[[zig-zag identity]].

=--

## Examples


+-- {: .num_example #KanExtensionOfAdjointPairIsAdjointQuadruple}
###### Example
**([[Kan extension]] of [[adjoint pair]] is [[adjoint quadruple]])**

For $\mathcal{V}$ a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] with all [[limits]] and [[colimits]], let $\mathcal{C}$, $\mathcal{D}$ be two [[small category|small]] $\mathcal{V}$-[[enriched categories]]and let

$$
  \mathcal{C}
    \underoverset
      {\underset{p}{\longrightarrow}}
      {\overset{q}{\longleftarrow}}
      {\bot}
  \mathcal{D}
$$

be a $\mathcal{V}$-[[enriched adjunction]]. Then there are $\mathcal{V}$-[[enriched natural isomorphisms]]


$$
  (q^{op})^\ast \;\simeq\; Lan_{p^{op}}
  \;\colon\;
  [\mathcal{C}^{op},\mathcal{V}]
    \longrightarrow
  [\mathcal{D}^{op},\mathcal{V}]  
$$

$$
  (p^{op})^\ast \;\simeq\; Ran_{q^{op}}
  \;\colon\;
  [\mathcal{D}^{op},\mathcal{V}]
    \longrightarrow
  [\mathcal{V}^{op},\mathcal{V}]  
$$

between the precomposition on [[enriched presheaves]] with one functor and the left/right [[Kan extension]] of the other.

By essential uniqueness of [[adjoint functors]], this means that the two [[Kan extension]] [[adjoint triples]] of $q$ and $p$ 

$$
  \array{
    Lan_{q^{op}} &\dashv& (q^{op})^\ast &\dashv& Ran_{q^{op}}
    \\
    && Lan_{p^{op}} &\dashv& (p^{op})^\ast &\dashv& Ran_{p^{op}}
  }
$$

merge into an [[adjoint quadruple]]

$$
  \array{
    Lan_{q^{op}} &\dashv& (q^{op})^\ast &\dashv& (p^{op})^\ast &\dashv& Ran_{p^{op}}
  }
  \;\colon\;
  [\mathcal{C}^{op},\mathcal{V}]
    \leftrightarrow
  [\mathcal{D}^{op}, \mathcal{V}]
$$

=--

+-- {: .proof}
###### Proof

For every [[enriched presheaf]] $F \;\colon\; \mathcal{C}^{op} \to \mathcal{V}$ we have a sequence of $\mathcal{V}$-[[enriched natural isomorphism]] as follows

$$
  \begin{aligned}
    (Lan_{p^{op}} F)(d)
      & \simeq
    \int^{ c \in \mathcal{C} } \mathcal{D}(d,p(c)) \otimes F(c)
    \\
    & \simeq
    \int^{ c \in \mathcal{C} } \mathcal{C}(q(d),c) \otimes F(c)
    \\
    & \simeq
    F(q(d))
    \\
    & = \left( (q^{op})^\ast F\right) (d)
    \,.    
  \end{aligned}
$$

Here the first step is the [[coend]]-formula for [[left Kan extension]] ([here](Kan+extension#PointwiseByCoEnds)), the second step if the [[enriched adjunction]]-isomorphism for $q \dashv p$ and the third step is the [[co-Yoneda lemma]].

This shows the first statement, which, by essential uniqueness of adjoints, implies the following statements.


=--


* For [[cohesive topos]] by definition the terminal [[geometric morphism]] extends to an adjoint quadruple.

## Related concepts

* [[adjunction]], [[adjoint functor]]

* [[adjoint triple]], [[adjoint string]]


## References

* [[Peter Johnstone]], _Remarks on punctual local connectedness_ ([tac](http://www.tac.mta.ca/tac/volumes/25/3/25-03abs.html))
{#Johnstone}


[[!redirects adjoint quadruples]]