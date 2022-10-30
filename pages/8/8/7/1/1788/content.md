

$$
  \array{
    \big(Grpd_\infty\big)_{/\mathbf{B}\mathcal{G}}
    \,\simeq\,
    \big(
      PSh_\infty(\ast)
    \big)_{/\mathbf{B}\mathcal{G}}
    &
    \underoverset
      {\phantom{--}\sim\phantom{--}}
      {\Gamma}
      {\longrightarrow}
    &
    PSh_\infty
    \big(
      \ast_{/\mathbf{B}\mathcal{G}}
    \big)
    \;\simeq\;
    PSh_\infty(
      \mathbf{B}\mathcal{G}
    \big)
    \;\simeq\;
    \mathcal{G} Act
    \big(
      Grpd_\infty
    \big)
    \,.
  }
$$


\linebreak


### Čech localization at a coverage {#LocalizationAtCoverage}


In the literature localization of categories of simplicial presheaves is typically discussed with respect to a [[Grothendieck topology]] or a [[basis for a topology]]. Here we discuss aspects of localization at a  [[coverage]].


Let $C$ be a category equipped with a [[coverage]], i.e. a collection of families of morphisms $\{U_i \to U\}$ for each object $U$ in $C$, called _covering families_ such that for any morphism $f : V \to U$ there exist diagrams

$$
  \array{
    V_j &\to& U_{i(j)}
    \\
    \downarrow && \downarrow
    \\
    V &\stackrel{f}{\to}& U
  }
$$ 

such that $\{V_i \to V\}$ is itself a covering family.

Write $S(\{U_i\}) \to j(U)$ for the [[sieve]] corresponding to a covering family, regarded as a [[subfunctor]] of the [[representable functor]] $j(U)$, which we both regard as simplicially discrete objects in $sPSh(C)$.

Write $sPSh(C)_{inj,cov}$ for the left [[Bousfield localization of model categories|Bousfield localization]] of $sPSh(C)_{inj}$ at these morphisms $S(\{U_i\}) \to j(U)$ corresponding to covering families.

+-- {: .num_prop}
###### Proposition

A subfunctor inclusion 
$$
  S
  \big(
    \{U_i\}_{i \in I}
    \cup
    \{V\}
  \big)
  \overset{
    \phantom{---}
  }{\hookrightarrow}
  y(U)
$$ 

corresponding to a sieve that is generated from 

* a covering $\big\{ U_i \to U \big\}_{i \in I}$ 

together with

* one further morphism $V \longrightarrow U$

  such that the pullback of the cover to $V$ exists and is still covering

is a weak equivalence in $sPSh(C)_{inj,cov}$
 
=--

+-- {: .proof}
###### Proof


The assumption means that we have covering family 
$\big\{ V_i \to V \}_{i \in I}$

$$
  \array{
    \mathllap{
      V_{i} 
      \,\coloneqq\;
    }
    V \times_U U_i
    &\longrightarrow& 
    U_{i}
    \\
    \big\downarrow 
    &{}^{{}_{(pb)}}& 
    \big\downarrow
    \\
    V
    &
    \underset{
      \phantom{-}
      f
      \phantom{-}
    }
    {
      \longrightarrow
    }
    & 
    U
    \mathrlap{\,.}
  }
$$ 

Consider then the commuting diagram:

$$
  \array{
    S\big(
      \{V_{i}\}_{i \in I}
    \big) 
    &\overset{
      \phantom{-}
      f_\ast
      \phantom{-}
    }{\hookrightarrow}& 
    S
    \big(
      \{U_i\}_{i \in I}
    \big)
    \\
    {}^{\mathllap{\simeq}}
    \big\downarrow 
    && 
    \big\downarrow
    \\
    y(V) 
    &\overset{\phantom{---}}{\longrightarrow}& 
    S\big(
      \{U_i\}_{i \in I} 
        \cup 
      \{V\}
    \big)
    \mathrlap{\,.}
  }
$$

Observe that:

1. this is a [[pushout]] in $sPSh(C)$:

   a map which factors through any of $U_i$ or $V$ (bottom right) is a factorization through some $V$ (bottom left) or through some $U_i$ (top right) and the pushout identifies those that are both (by the [[universal property]] of the [[pullback]]).

1. the top morphism is a cofibration in $sPSh(C)_{inj}$: 

   it injects into the set of morphisms that factor through the cover $\{U_i\}_{i \in I}$ those that factor even through the pullback cover.     

1. the left morphism is a weak equivalence in $sPSh(C)_{inj,cov}$:

   since it is a covering sieve map for $V$, by assumption.

1. by general properties of [[Bousfield localization of model categories|left Bousfield localization]] the localization $sPSh(C)_{inj,cov}$ is [[proper model category|left proper]]. 

Therefore the morphism on the right is a weak equivalence. The statement follows by [[2-out-of-3]] applied to the composite

$$
  S
  \big(
    \{U_i\}_{i \in I}
  \big)
  \xrightarrow{\phantom{--}}
  S
  \big(
    \{U_i\}_{i \in I}
    \cup
    V
  \big)
  \xrightarrow{\phantom{--}}
  y(U)
  \,.
$$


=--

+-- {: .num_cor}
###### Corollary

For $S(\{U_i\}) \to j(U)$ a covering sieve, its [[pullback]] $f^*S(\{U_i\}) \to j(V)$ in $sPSh(C)$ along any morphism $j(f) : j(V) \to j(U)$ 

$$
  \array{
    f^* S(\{U_i\}) &\to& S(\{U_i\})
    \\
    \downarrow && \downarrow
    \\
    j(V) &\stackrel{j(f)}{\to}& j(U)
  }
$$

is also a weak equivalence.
 
=--

+-- {: .num_lemma}
###### Lemma

If $S(\{U_i\}) \to j(U)$ is the sieve of a covering family and $\tilde S \hookrightarrow j(U)$ is any sieve such that for every $f_i : U_i \to U$ the pullback $f_i^* \tilde S$ is a weak equivalence, then $\tilde S \to j(U)$ becomes an [[isomorphism]] in the [[homotopy category]].

=--


+-- {: .proof}
###### Proof


First notice that if $f_i^* \tilde S$ is a weak equivalence for all $i$, then the pullback of $\tilde S$ to any element of the sieve $S(\{U_i\})$ is a weak equivalence. 
Use the [[co-Yoneda lemma]] to write 

$$
  S(\{U_i\}) = \lim_{\underset{V \to U_i \to U}{\to}} j(V)
  \,.
$$

Now consider these objects in the [[(∞,1)-category of (∞,1)-presheaves]] that is presented by $sPSh(C)_{inj}$.

Since that has [[universal colimits]] we have the pullback square

$$
  \array{
    i^* \lim_\to j(V)
    &\simeq& \lim_{\to} f_V^* \tilde S
    &\to& \tilde S
    \\
    && \downarrow && \downarrow^{\mathrlap{i}}
    \\
    S(\{U_i\}) &=& 
    \lim_{\underset{f_V : V \to U_i \to U}{\to}} j(V)
    &\stackrel{(f_V)}{\to}&
    j(U)
  }
$$

and the left vertical morphism is a colimit over morphisms that are weak equivalences in $sPSh(C)_{inj,loc}$. By the general properties of [[reflective sub-(∞,1)-categories]] this means that the total left vertical morphism becomes an isomorphism in the homotopy category of $sPSh(C)_{inj,cov}$. Also the bottom morphism is an isomorphism there, and hence the right vertical one is.


=--


+-- {: .num_lemma}
###### Conclusion

In total this shows that the localization at the [[coverage]] produces the [[topological localization]] at the [[Grothendieck topology]] generated by that coverage.


=--

$$
\begin{array}{l l}
recnat &: \forall A. A \rightarrow (A \rightarrow A) \rightarrow \mathbb{N} \rightarrow A \\
recnat & A z s = cata (\phi \circ out) where \\
& \phi (inl \ast) = z \\
& \phi (inr n) = s n
\end{array}
$$