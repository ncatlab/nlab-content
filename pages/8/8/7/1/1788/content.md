
Where the idea of (non-higher) [[observational type theory]] is to equip all [[type formation]] rules (notably [[dependent functions]], [[dependent pairs]] and [[W-types|inductive constructions]]) with their dedicated notion of *structure preserving* [[definitional equality]] --- namely: component-wise, ie. homo-morphic, hence: "observational" ---; the idea of *higher* observational type theory is to do the same for [[propositional equality]] hence for [[identification types]] used in [[homotopy type theory]] (where [[types]] behave like [[homotopy n-type|*higher* homomotopy types]], whence the qualifier "higher").

Concretely:

* the "observational" principle for identification of [[dependent functions]] is to say that these are dependent functions of identifications of arguments and values (a statement otherwise known as [[function extensionality]])

* the "observational" principle for identifications of [[dependent pairs]] is to say that these are dependent pairs of identifications of factors.

and in ordinary [[univalence axiom|univalent]] [[homotopy type theory]] this form of the "[[structure identity principle]]" follows as a [[type equivalence]] between [[identification types]]:

<img src="/nlab/files/DependentPairExtensionality-230121.jpg" width="660">

<img src="/nlab/files/DependentFunctionExtensionality-230121.jpg" width="660">

The idea of higher observational type theory is to make this and analogous structural characterizations of [[identification types]] be part of their definitional [[inference rules]], thus building the [[structure identity principle]] right into the rewrite rules of the type theory.

In such a higher observational theory, in particular also the [[univalence axiom]] would be a [[definitional equality]] and hence would "compute". 

This most desirable property of any [[homotopy type theory]] has previously has been accomplished only by [[cubical type theories]].  However, cubical type theories achieve this only by adding rewrite rules which encode technical detail that has no nice abstract motivation other than making the univalence axiom compute and which one would rather keep out of the syntactic logic and instead relegate to the construction of [[categorical semantics]]. 

The hope is therefore that higher observational type theory would provide a type system which achieves both:

1. its syntax is as logically clean as that of [[Martin-Löf dependent type theory]] equipped with the [[univalence axiom]];

1. its [[inference rules]] for [[identification types]] make the [[univalence axiom]] be a computable function as it is in [[cubical type theories]].

At the moment this seems to remain a hope, certainly there is currently no [[proof assistant]] implementing the principles of higher observational type theory. Ideally the reference below would elucidate which questions remain open and which problems remain to be solved.



\linebreak

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

