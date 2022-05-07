
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $\Gamma \;\colon\; \mathcal{E} \to \mathcal{B}$ a [[functor]] we say that it _has [[codiscrete object]]s_ if it has a  [[full and faithful functor|full and faithful]] [[right adjoint]] $coDisc \,\colon\, \mathcal{B} \hookrightarrow \mathcal{E}$. 

This is for instance the case for the [[global section]] [[geometric morphism]] of a [[local topos]] $ (Disc \dashv \Gamma \dashv coDisc) \;\colon\; \mathcal{E} \to \mathcal{B}$. 

In this situation, we say that a  **concrete object** $X \in \mathcal{E}$ is one for which the $(\Gamma \dashv coDisc)$-[[unit of an adjunction]] is a [[monomorphism]].

If $\mathcal{E}$ is a [[sheaf topos]], this is called a [[concrete sheaf]].

If $\mathcal{E}$ is a [[cohesive (∞,1)-topos]] then this is called a [[concrete (∞,1)-sheaf]] or the like.

The dual notion is that of a [[co-concrete object]].

## Properties

$\Gamma$ is a [[faithful functor]] on [[morphisms]] whose [[codomain]] is concrete. 

### Concretification factorization

+-- {: .num_prop #ConcretificationFactorization}
###### Proposition

For $\mathbf{H}$ a [[local topos]], write

$$
  \mathbf{H}_{conc} 
  \overset{ \phantom{AAAA} }{\hookrightarrow}
  \mathbf{H}
$$

for its [[full subcategory]] of [[concrete objects]].

Then there is a sequence of [[reflective subcategory]]-inclusions that factor the $(\Gamma \dashv coDisc)$-adjunction as

$$
  \Gamma \;\dashv\; coDisc
  \;\;\colon\;\;
  \mathbf{H}
  \array{
    \overset{\phantom{AA} conc \phantom{AA}}{\longrightarrow}
    \\
    \overset{\phantom{AA} \iota_{conc} \phantom{AA}}{\hookleftarrow}
  }
  \mathbf{H}_{conc}
  \array{
    \overset{\phantom{AAA}}{\longrightarrow}
    \\
    \overset{\phantom{AAA}}{\hookleftarrow}
  }
  Set
$$

Here morphisms on top are left adjoint to morphisms below, hence

$$
  conc \dashv \iota_{conc}
$$

exhibits the concrete objects as a [[reflective subcategory]], the reflector $conc$ being "[[concretification]]".

=--


+-- {: .proof}
###### Proof

For the adjunction on the right, we just need to observe that for every [[set]] $S \in Set$, the [[codiscrete object]] $coDisc(S)$ is [[concrete object|concrete]], which is immediate by [[idempotent monad|idempotency]] of $\sharp$ and the fact that every [[isomorphism]] is also a [[monomorphism]].

For the adjunction on the left we claim that the [[left adjoint]] $conc$ ([[concretification]]), is given by sending each [[object]] to the [[image]] of its $(\Gamma \dashv coDisc)$ [[adjunction unit]] $\eta^\sharp$:

$$
  conc \;\colon\; X \mapsto im(\eta^\sharp_X)
$$

hence to the object which exhibits the [[(epi, mono) factorization system|epi/mono-factorization]] of $\eta^\sharp_X$

\[
  \label{ConcretificationUnitFromEpiMonoFactorization}
  \eta^\sharp_X
  \;\colon\;
  X 
    \underoverset{epi}{ \eta^{conc}_X }{\longrightarrow}
  conc X
    \underoverset{mono}{}{\longrightarrow}
  \sharp X
  \,.
\]

First we need to show that $conc X$, thus defined, is indeed concrete, hence that $\eta^\sharp_{im(\eta^\sharp_X)}$ is a monomorphism. For this, consider the following [[naturality square]] of the $\Gamma \dashv coDisc$-adjunction hom-isomorphism

\[
  \label{ConcNatur}
  \array{
    {\phantom{A}}
    \\
    Hom_{Set}( \Gamma im(\eta^\sharp_X), \Gamma im(\eta^\sharp_X) )
    &\simeq&
    Hom_{\mathbf{H}}( im(\eta^\sharp_X), \sharp im(\eta^\sharp_X) )
    \\
    {}^{ \mathllap{ (-) \circ \Gamma(\eta^{conc}_X) } }\big\downarrow      
      &&
    \big\downarrow^{
      \mathrlap{ (-) \circ \eta^{conc}_X }
    }
    \\
    Hom_{Set}( \Gamma X, \Gamma im(\eta^\sharp_X) )
    &\simeq&
    Hom_{\mathbf{H}}( X, \sharp im(\eta^\sharp_X) )    
  }
  \phantom{AAAA}
  \array{
    {\phantom{A}}
    \\
    \left\{ id_{\Gamma im(\eta^\sharp_X)} \right\}
      &\longrightarrow&
    \phantom{\sharp(\eta^{conc}_X) \circ \eta^\sharp_{ X }}
    \left\{ \eta^{\sharp}_{im(\eta^\sharp_X)} \right\}
    \\
    \big\downarrow 
      && 
    \phantom{\sharp(\eta^{conc}_X) \circ \eta^\sharp_{ X }}
    \big\downarrow
    \\
    \left\{ \Gamma(\eta^{conc}_X) \right\}
      &\longrightarrow& 
    \left\{
      \underset{
        iso
      }{ 
      \underbrace{
         \sharp(\eta^{conc}_X)
      }}
      \circ \eta^\sharp_{ X }
      \;=\;
    \eta^{\sharp}_{ im(\eta^\sharp_X) } \circ \eta^{conc}_X 
    \right\}
  }
\]

By chasing the [[identity morphism]] on $\Gamma im(\eta^\sharp_X)$ through this diagram, as shown by the diagram on the right, we obtain the equality displayed in the bottom right entry, where we used the general formula for [[adjuncts]] and the definition $\sharp \coloneqq coDisc \circ \Gamma$.

But observe that $\Gamma (\eta^{conc}_X)$, and hence also $\sharp(\eta^{conc}_X)$, is an [[isomorphism]], as indicated above: Since $\Gamma$ is both a [[left adjoint]] as well as a [[right adjoint]], it preserves both [[epimorphisms]] as well as [[monomorphisms]], hence it preserves [[image]] factorizations. This implies that $\Gamma \eta^{conc}_X$ is the epimorphism onto the image of $\Gamma( \eta^\sharp_X )$. But by [[idempotent monad|idempotency]] of $\sharp$, the latter is an [[isomorphism]], and hence so is the epimorphism in its image factorization.

Therefore the equality in (eq:ConcNatur) says that 

$$
  \begin{aligned}
    \eta^\sharp_{ X } 
      & =
    \left( 
      iso \circ \eta^{\sharp}_{ im(\eta^\sharp_X)} 
    \right)
      \circ 
    \eta^{conc}_X
    \\
    & =
    mono \circ \eta^{conc}_X 
    \,,
  \end{aligned}
$$

where in the second line we remembered that $\eta^{conc}_X$ is, by definition, the epimorphism in the epi/mono-factorization of $\eta^\sharp_X$.

Now the defining property of epimorphisms allows to cancel this commmon factor on both sides, which yields

$$
  \eta^{\sharp}_{ im(\eta^\sharp_X) }
  \;=\;
  iso \circ mono
  \;=\;
  mono.
$$

This shows that $conc X \coloneqq im(\eta^\sharp_X)$ is indeed concrete.

It remains to show that this construction is [[left adjoint]] to the inclusion.
We claim that the [[adjunction unit]] of $(conc \dashv \iota_{conc})$ is provided by $\eta^{conc}$ (eq:ConcretificationUnitFromEpiMonoFactorization). 

To see this, first notice that, since the [[(epi, mono) factorization system|epi/mono-factorization]] is [[orthogonal factorization system|orthogonal]] and hence [[functorial factorization|functorial]], we have [[commuting diagrams]] of the form

\[
  \label{NaturalitySquareForConcretificationUnit}
  \array{
    X_1 
      &\underoverset{epi}{\eta^{conc}_{X_1}}{\longrightarrow}& 
    im(\eta^\sharp_{X_1})
      &\underset{mono}{\longrightarrow}&
    \sharp X_1
    \\
    \big\downarrow && \big\downarrow && \big\downarrow
    \\
    X_2 
      &\underoverset{epi}{\eta^{conc}_{X_2}}{\longrightarrow}& 
    im(\eta^\sharp_{X_2})
      &\underset{mono}{\longrightarrow}&
    \sharp X_2
  }
\]

Now to demonstrate the adjunction, it is sufficient, to show that $\eta^{conc}$ is a [[universal morphism]] in the sense discussed at _[[adjoint functors]]_. Hence consider any morphism $f \;\colon\; X_1 \to X_2$ with $X_2 \in \mathbf{H}_{conc} \hookrightarrow \mathbf{H}$. Then we need to show that there is a unique diagonal morphism as below, that makes the following _top left triangle_ [[commuting diagram|commute]]:

$$
  \array{
    X_1 
      &\overset{\phantom{AA} f \phantom{AA}}{\longrightarrow}& 
    X_2
    \\
    {}^{\mathllap{epi}}\big\downarrow^{\mathrlap{\eta^{conc}_{X_1}}} 
      &{}^{\mathllap{\exists !}}\nearrow& 
    \big\downarrow^{\mathrlap{mono}}
    \\
    im(\eta^\sharp_{X_1}) 
      &\underset{}{\longrightarrow}& 
    \sharp X_2
  }
$$

Now, from (eq:NaturalitySquareForConcretificationUnit), we have a [[commuting square]] as shown. Here the left morphism is an [[epimorphism]] by construction, while the right morphism is a [[monomorphism]] by assumption on $X_2$. With this, the [[(epi, mono) factorization system|epi/mono-factorization]] says that there is a diagonal [[lift]] which makes _both_ triangles [[commuting diagram|commute]].

It remains to see that the lift is unique with just the property of making the top left triangle commute. But this is equivalently the statement that the left morphism is an [[epimorphism]].

=--

### Further properties
 {#FurtherProperties} 


\begin{proposition}\label{CohesiveMapsToConcreteObjectsGlue}
**(cohesive maps to concrete objects glue)**
\linebreak
  Let $\mathbf{H}$ be a [[cohesive (infinity,1)-topos|cohesive $\infty$-topos]], and consider $Y \,\in\, \mathbf{H}_{\sharp_1} \xhookrightarrow{\;} \mathbf{H}$ a [[concrete object]], in that its [[sharp modality]] [[unit of a monad|unit]] is [[n-truncated object of an (infinity,1)-category|(-1)-truncated]]/[[monomorphism in an (infinity,1)-category|monomorphic]]: $Y \xhookrightarrow{ \;\;\eta^\sharp_Y\;\; } \sharp Y$.  Then *cohesive maps to $X$ glue* (satisfy the respective sheaf property): 

For any $Y \,\in\, \mathbf{H}$ and any open cover, namely any [[n-connected object of an (infinity,1)-topos|(-1)-connected]]/[[effective epimorphism in an (infinity,1)-category|effective epi-morphism]] $U \twoheadrightarrow X$, cohesive maps $U \xrightarrow{\;} X$ whose maps of [[underlying]] $\infty$-groupoids descend/extend to $Y$, then they also descend/extend to $Y$ as cohesive maps, in an essentially unique way, in that all solid [[homotopy]]-[[commutative square]] as follows have essentially unique dashed lifts:

\begin{tikzcd}[row sep=22pt, column sep=22pt]
  U
  \ar[
    rr,
    "{ \forall }"{above}
  ]
  \ar[
    dd,
    ->>
  ]
  &&
  X
  \ar[
    dd,
    hook,
    "{ \eta^\sharp_X }"
  ]
  \\
  \\
  Y
  \ar[
    rr,
    "{ \forall }"{below}
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists ! }"{description}
  ]
  &&
  \sharp X
\end{tikzcd}

\end{proposition}
The point here is the given interpretation of this [[lifting problem]], but the proof of the latter is immediate:
\begin{proof}
Under the given assumptions, the essentially unique existence of the lift is an instance of the [[(n-connected, n-truncated) factorization system]] for $n = (-1)$.
\end{proof}



## Related concepts

* [[concretification]]

[[!include cohesion - table]]


## References

* {#Shulman} [[Mike Shulman]], _Discreteness, Concreteness, Fibrations, and Scones_ ([blog post](http://golem.ph.utexas.edu/category/2011/11/discreteness_concreteness_fibr.html))

* [[Urs Schreiber]], Section 3.7.2 in *[[schreiber:differential cohomology in a cohesive topos|Differential cohomology in a cohesive $\infty$-topos]]* ([arXiv:1310.7930](https://arxiv.org/abs/1310.7930))
 

[[!redirects concrete objects]]

