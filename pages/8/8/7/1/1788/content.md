
* Gilles Barthe, Olivier Pons, *Type Isomorphisms and Proof Reuse in Dependent Type Theory*, in *Foundations of Software Science and Computation Structures. FoSSaCS 2001*, Lecture Notes in Computer Science **2030**, Springer (2001) &lbrack;[doi:10.1007/3-540-45315-6_4](https://doi.org/10.1007/3-540-45315-6_4)&rbrack;

* Roberto di Cosmo, *A short survey of Isomorphisms of Types* &lbrack;[pdf](https://www.dicosmo.org/Articles/mscs-survey.pdf)&rbrack;

* Sergei Soloviev, *On Isomorphism of Dependent Products in a
Typed Logical Framework* &lbrack;[pdf](https://drops.dagstuhl.de/opus/volltexte/2015/5501/pdf/15.pdf)&rbrack;

* [arXiv:2104.08958](https://arxiv.org/abs/2104.08958)

    


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

