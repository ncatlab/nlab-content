
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

While every [[functor]] might be understood as constituting a "comparison" between its [[domain]] and [[codomain]]-[[categories]], the term "comparison functor" is often understood by default as referring, in [[categorical algebra]], to the unique functor that relates any [[adjoint functors|adjunction]] to its [[monadic adjunction]] -- this is the case we discuss here.

But other instances of functorial "comparison" are bound to be relevant. For instance, for the "[[comparison lemma]]" in [[topos theory]] see there.

## Statement

\begin{proposition}
**(the [[comparison functor]] from any [[adjoint functors|adjunction]] to its [[monadic adjunction]])**
\linebreak
Every [[pair]] of [[adjoint functors]] $(F \dashv U) \;\colon\; \mathbf{C}' \leftrightarrow \mathbf{C}$ (with [[unit of an adjunction|unit]] $\eta^{U F}$ and [[counit of an adjunction|counit]] $\epsilon^{F U}$) between [[categories]] $\mathbf{C}$, $\mathbf{C}'$ fits into a [[commuting diagram]] in [[Cat]] of the following form:

\begin{imagefromfile}
    "file_name": "AdjunctionsAndMonadicity-221108.jpg",
    "width": "470",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Here:

* $\mathcal{E} \;\coloneqq\; U F \;\coloneqq\; U \circ F$ denotes the induced [[endofunctor]] on $\mathbf{C}$

  which carries the [[structure]] of a [[monad]] with 

  * [[unit of a monad|unit]] given by 

    $$
      \eta^{\mathcal{E}}
      \;\;
      \colon
      \;\;
      id_{\mathbf{C}}
      \xrightarrow{\;\;
        \eta^{U F}
      \;\;}
      U F
      \;=\;
      \mathcal{E}
    $$ 

  * product given by

    $$
      \mu^{\mathcal{E}}
      \;\;
      \colon
      \;\;
      \mathcal{E} \mathcal{E}
      \;=\;
      U F U F
      \xrightarrow{\;\; 
        U ( \epsilon^{F U} ) F  
      \;\;}
      U F
      \;=\;
      \mathcal{E}
    $$

* $\mathbf{C}^{\mathcal{E}}$ denotes the ("[[Eilenberg-Moore category|Eilenberg-Moore]]"-)[[category]] of $\mathcal{E}$-[[algebras over a monad|algebras]] in $\mathbf{C}$ 

  $$
    A 
    \;=\;
    \Big(
      \mathcal{E}
      U^{\mathcal{E}}(A)
      \xrightarrow{\;\; \rho_A  \;\;}
      U^{\mathcal{E}}(A)
    \Big) 
  $$

   in $\mathbf{C}$ with [[homomorphisms]] between them,

* $K^{U F}$ denotes the "[[comparison functor]]" given by

  $$
    \array{
      \mathbf{C}'
      &
      \xrightarrow{\;\;\;\;\;\;\;\;\;\;
         K^{U F}
      \;\;\;\;\;\;\;\;\;\;}
      &
      \!\!\!\!\!\!\!\!\!\!\!\!\!\!
      \mathbf{C}^{\mathcal{E}}
      \\
      C' 
      &\mapsto&
      {
        \Big(
          \mathcal{E}
          U(C')
          \,=\,
          U F U (C')
          \xrightarrow{\; 
            U \epsilon^{F U}_{C'}  
          \;}
          U (C')
        \Big)
      }
    }
  $$

* $\mathbf{C}_{\mathcal{E}}$ denotes the ("[[Kleisli category|Kleisli]]"-)[[category]] of *[free](algebra+over+a+monad#FreeAlgebras)* $\mathcal{E}$-[[algebras over a monad|algebras]]

  $$
    \begin{array}{rl}
    F^{\mathcal{E}}(C)
    &
    \;=\;
    \Big(
      \mathcal{E}
      \mathcal{E}
      (C)
      \xrightarrow{\;\; 
        \mu^{\mathcal{E}}_C  
      \;\;}
      \mathcal{E}(C)
    \Big) 
    \\
    \;=\;
    K^{U F} F(C)
    &
    \;=\;
    \Big(
      \mathcal{E}
      U
      F 
      (C)
      \xrightarrow{\;\; 
        U \epsilon^{ F U }_{F(C)}
      \;\;}
      U
      F 
      (C)
    \Big) 
    \,.
    \end{array}
  $$

* Here the last line makes explicit that

  $$
    U^{\mathcal{E}} F^{\mathcal{E}}
    \;=\;
    U F
    \;=\;
    \mathcal{E}
    \,.
  $$ 

  In fact, $F^{\mathcal{E}} \dashv U^{\mathcal{E}}$ and this realizes the [[monadic adjunction]] whose induced monad is $\mathcal{E}$.

  Hence the original $F \dashv U$ is [[monadic adjunction|monadic]] iff the [[comparison functor]] $K^{U F}$ is an [[equivalence of categories]].

\end{proposition}

(See for instance [MacLane (1971), §VI.3](#MacLane71))


## Properties

* $K^{UF}$ is [[fully faithful]] if and only if $U$ is of [[descent type]]. In this case, $K^{UF}$ has a [[right adjoint]] if and only if it is an [[equivalence of categories]], since [[coreflective category|coreflections]] create colimits, and every algebra is a colimit of a free algebra.

* When $F \dashv U$ is the adjunction associated to the [[Kleisli category]] of a monad, $K^{UF}$ is [[dense]] and [[fully faithful]].


## Related concepts

* [[monadic functor]], [[monadicity theorem]]


## References

* {#MacLane71} [[Saunders MacLane]], §VI.3 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5**  Springer (1971) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

[[!redirects comparison functors]]
