

$$
  \frac{
  \frac{
    D \,\colon\, Type
  }
  {
  \big(
    (x \,\colon\, \varnothing)
    \mapsto
    D
  \big)
  \,\colon\,
  (\varnothing \to Type)
  }
  }{
  ind_{ (x \mapsto D) }
  \,\colon\,
  (x \colon \varnothing) \to D
  }
$$


\[
  \label{SurjectiveModuleMapsAsRightOrthClass}
  \{ 0 \to R \}^{&solb;} 
  \;\;\;=\;\;\; 
  Srjctv
  \,.
\]

The [[injection|injective]] [[homomorphisms]] are those with the [[right lifting property]] against the [[terminal object|terminal]] [[homomorphism]] from the [[ground ring]] 
into the [[zero]] [[module]]:

\[
  \label{InjectiveModuleMapsAsRightOrthClass}
  \{ R \to 0 \}^{&solb;}
  \;\;\;=\;\;\;
  Injctv
  \,.
\]


An $R$-[[module]] $M$ is [[projective module|projective]] iff (by direct unwinding of the definitions of [[projective objects]] and lifts) the [[initial object|initial morphism]] $0 \to R$ (out of the [[zero]] [[module]] into the [[ground ring]]) has the [[left lifting property]] against all surjective homomorphisms.

With the notation of Def. \ref{QuillenNegation} this reads as follows:

  $$
    M\;\text{projective}
    \;\;\;\;\;
      \Leftrightarrow
    \;\;\;\;\;
    \{ 0 \to M \}
    \;&solb;\;
    Srjctv
    \;\;\;\;\;
      \overset{
        \text{(eq:SurjectiveModuleMapsAsRightOrthClass)}
      }{
      \Leftrightarrow
      }
    \;\;\;\;\;
    \{ 0 \to M \}
    \;&solb;\;
    \Big(
      \{ 0 \to R \}^{&solb;}
    \Big)
    \;\;\;\;\;
      \Leftrightarrow
    \;\;\;\;\;
    \{ 0 \to M \}
    \;\in\;
    \multiscripts{^{&solb;}}
    {
    \Big(
      \{ 0 \to R \}^{^&solb;}
    \Big)
    }{}
  $$

