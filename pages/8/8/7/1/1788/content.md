
#Contents#
* table of contents
{:toc}

## Idea

In [[computer science]], a _monad_ is a kind of [[data type]]-structure which describes "notions of computations which may cause or be subject to *side effects*" -- such as involving [[IO-monad|input/output]], [[exception monad|exception handling]], [[writer monad|writing to]] or [[reader monad|reading from]] global variables,  etc. -- as familiar from [[imperative programming]] but cast as "pure functions" with deterministic and [[verified programming|verifiable behaviour]], in the style of [[functional programming]].

In short, a (Kleisli-style) monad in a given [[programming language]] consists of *assignments* (but see [below](#RefinedIdea)):

1. to any [[data type|data]] [[type]] $D$ of a new data type $T(D)$ of "$D$-data with $T$-effects",

1. to any [[pair]] of [[functions]] (programs) of the form $prog_{12} \colon D_1 \to T(D_2)$ and $prog_{23} \colon D_2 \to T(D_3)$ of a function $prog_{23}\big[prog_{12}(-)\big] : D_1 \to T (D_3)$ (their *binding* or *[[Kleisli composition]]*);

1. to any [[data type|data]] [[type]] $D$ of a function $ret_D \;\colon\; D \to T(D)$ assigning "trivial $T$-effects",

such that the binding is [[associativity|associative]] and also [[unitality|unital]] with respect to the return operation.



### Basic idea: External monads
 {#BasicIdea}

In [[programming language|programming]] it frequently happens that a [[program]] with "nominal" output [[data type]] $D$ *de facto* outputs data of some modified type $T(D)$ which accounts for "external effects" caused by or affecting the program, where 
\[
  \label{MonadMapInIntroduction}
  D \;\mapsto\; T(D)
\]
is some general operation sending [[data types]] $D$ to new data types $T(D)$.

> For example, if alongside the computation of its nominal output data $d \colon D$ a program also writes a log message $msg \,\colon\,$ [[String (computer science)|String]], then its actual output data is the [[pair]] $(d, msg)$ of [[product type]] $T(D) \,=\, D \times String$.

> Or, dually, if the program may fail and instead "throw an [[exception]] message" $msg \,\colon\,$ [[String (computer science)|String]], then its actual output data is *either* $d \colon D$ *or* $msg \colon String$, hence is of [[coproduct type]] $T(D) \,=\, D \sqcup String$.

Given such a $T$-effectful program $prog_{12} \;\colon\; D_1 \to T(D_2)$ and given a subsequent program $prog_{23} \,\colon\, D_2 \to T(D_3)$ accepting nominal input data of type $D_2$ and itself possibly involved in further effects of type $T(-)$, then the *naïve* [[composition]] of the two programs makes no sense (unless $T(D) = D$ is actually the trivial sort of effect), but their evident *intended* composition is, clearly, obtained by: 

1. first adjusting $prog_{23}$ via a given prescription

   \[
     \label{BindingLawInIntroduction}
     prog \;\mapsto\; prog[-]
     \,,
   \]

   such that $prog_{23}[-] \,\colon\, T D_2 \to T D_3$:

   1. does accept data of type $T(D_2)$ and 

   1. "acts as $prog_{12}$ while carrying any previous $T(-)$-effects along";

1. then forming the naive [[composition]] $prog_{23}\big[prog_{12}(-)\big]$

as follows:

\begin{imagefromfile}
    "file_name": "KleisliCompositionOfEffectfulPrograms-221031.jpg",
    "width": "700",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

> (Beware that we are denoting by square brackets "$prog[-]$" what in [[programming languages]] like [[Haskell]] [is denoted by](https://wiki.haskell.org/Monad#The_Monad_class) "`(-) >>= prog`"  aka "fish notation", eg. [Milewski (2019)](#Milewski19), and which other authors denote by "$prog^\ast$" or similar, e.g. [Uustalu (2021), lecture 1](#Uustalu21), [p. 12](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf#page=12) .)

According to the intended behaviour of these programs, it remains to specify how exactly $prog_{23}[-]$ "carries $T(-)$-effects along", hence what the "bind" operation really is. 

> For instance, in the above example of a logging-effect, where $T(D_2) = D_2 \times String$, the evident way is to use the [[concatenation]]  $String \times String \xrightarrow{\; concat \;} String$ and set:

> $ prog_{23}\big[-\big]\;\coloneqq\; D_2 \times String \xrightarrow{ prog_{23} \times Id_{String} } D_3 \times String \times String \xrightarrow{ Id_{D_3} \times concat } D_3 \times String \,. $

> In the other example above, where the effect is the possible throwing of an exception message, the evident way to carry this kind of effect along is to use the [[codiagonal]] $\nabla \;\colon\; String \sqcup String \to String$, which amounts to keep forwarding the exception that has already been thrown, if any:

> $prog_{23}big[-\big] \;\coloneqq\; D_2 \sqcup String \xrightarrow{ prog_{23} \sqcup Id_{String} } D_3 \sqcup String \sqcup String \xrightarrow{ id_{D_3} \sqcup \nabla } D_3 \sqcup String \,.$

Whatever design choice one makes for how to "carry along effects", it must be consistent in that applying the method to a [[triple]] of $T(-)$-effectful programs which are nominally composable, then their effectful composition should be unambiguously defined in that it is [[associative]], satisfying the following "law" ([[equation]]):

\[
  \label{AssociativityConditionInIntroduction}
  prog_{34}\Big[
    prog_{23}\big[
      prog_{12}(-)
    \big]
  \Big]
  \;\;\;=\;\;\;
  \Big(
    prog_{34}\big[
      prog_{23}(-)
    \big]
  \Big)
  \big[
    prog_{12}(-)
  \big]
  \,.
\]

Finally, for such a notion of effectful programs to be usefully connected to "pure" programs without effects,  it ought to be the case that for any program $prog_{01} \,\colon\, D_0 \xrightarrow{\;} D_1$ that happens to have no $T(-)$-effects, we have a prescription for how to regard it as a  $T(-)$-effectful program in a trivial way. For that purpose there should be defined an operation

\[  
  \label{ReturnMapInIntroduction}
  ret_{D} \;\colon\; D \xrightarrow{\;}  T(D)
\]

which does nothing but "return" data of type $D$, but re-regarded as effectful $T(D)$-data in a trivial way; so that we may construct the trivially effectful program $ret_{D_1}\big(prog_{01}(-)\big) \;\colon\; D_0 \xrightarrow{\;} T(D_1)$.

> For instance, in the above example of log-message effects this would be the operation $D \to D \times String$ which assigns the [[empty set|emtpty]] [[string (computer science)|string]] $d \mapsto (d, \varnothing)$.

> In the other example above, of exception handling, the trivial effect $D \to D \sqcup String$ is just not to throw an exception, which is just $d \maspto d$ (the right [[coprojection]] into the [[coproduct]]).

The final consistency condition then is that "carrying along trivial effects is indeed the trivial operation", i.e. that 

\[
  \label{UnitalityInIntroduction}
  prog_{01}
  \big[
    ret_{D_0}(-)
  \big]
  \;=\;
  prog_{01}
  \;\;\;\;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;\;\;\;
  ret_{D_1}\big[
    prog_{01}(-)
  \big]
  \;=\;
  prog_{01}
  \,.
\]

Notice that the [[associativity]] condition (eq:AssociativityConditionInIntroduction) and the [[unitality]] condition (eq:UnitalityInIntroduction) are jointly equivalent to saying that [[data types]] with [[hom-sets]] of $T(-)$-effectful programs between them, in the above sense, form a *[[category]]*. In [[category theory]] this is known as the *[[Kleisli category]]* of a *[[monad]]* $T$.

> Traditionally in [[category theory]], the [[axioms]] on [[monads]] are presented in a somewhat different way, invoking a monad "product" [[natural transformation]] $T \circ T \xrightarrow{ \mu } T$ instead of the "binding" operation. One readily checks that these two axiomatic presentations of monads are in fact equal -- see (eq:TransformBetweenBindAndJoinInIntroduction) below --, but the above "[[Kleisli triple]]"-presentation is typically more relevant in the practice of [[functional programming]].

In summary, a choice of *assignments* (but see [below](#RefinedIdea)) to [[data types]] $D_i$ of

1. $T(D) \;\colon\; Type$,

   namely of types of effectful data of nominal type $D$ (eq:MonadMapInIntroduction);

2. $\array{\\ bind_{D_1, D_2} \colon & Hom\big(D_1,\, T D_2\big) &\longrightarrow& Hom\big(T D_1,\,T D_2\big) \\ & prog &\mapsto& prog[-]}$,

   namely of how to execute a prog while carrying along any previous effects (eq:BindingLawInIntroduction);

3. $ret_D \;\colon\; D \to T D$,

   namely of how to regard plain $D$-data as trivially effectful (eq:ReturnMapInIntroduction)

subject to:

1. the [[associativity]] condition (eq:AssociativityConditionInIntroduction) 

1. the [[unitality]] condition (eq:UnitalityInIntroduction) 

is called a *[[monad in computer science]]* (also: "[[Kleisli triple]]" in [[functional programming]]) and serves to encode the notion that all programs may be subject to certain *external effects* of a kind that is specified by the above choices of monad operations.

Here, for the time being (but see [below](#RefinedIdea)), we write $Hom(D_1, D_2)$ for the *[[set]]* of programs/functions taking data of type $D_1$ to data of $D_2$ (the *[[hom set]]* in the plain [[category]] of [[types]]).

> The first running example above is known as the *[[writer monad]]*, since it encodes the situation where programs may have the additional effect of writing a message string into a given buffer.

> The other running example above is naturally called the *[[exception monad]]*.

The above structure making such a [[Kleisli category|Kleisli-style]] [[monad in computer science]] may and often is encoded in different equivalent ways: Alternatively postulating operations

1. $D \mapsto T D$ (as before)

1. $fmap_{D_1, D_2} \;\colon\; Hom\big(D_1 \to D_2\big) \longrightarrow Hom\big(T D_1, T D_2\big)$ 

1. $ret_D \;\colon\; D \to T D$

1. $join_D \;\colon\; T\big( T D\big) \to T D$

such that 

1. $fmap$ is *[[functor|functorial]]* on [[data types]] 

1. $join$ is [[associativity|associative]] and [[unitality|unital]] (with respect to $ret$) as a [[natural transformation]],

yields the definition of *[[monad]]* traditionally used in [[category theory]] (namely as a [[monoid object]] [[internalization|in]] [[endofunctors]], here  on the plain  [[category]] of [[data types]]).

Direct inspection shows that one may [[bijection|bijectively]] transmute such $bind$- and $join$-operators into each other by expressing them as the following composites (using [[category theory]]-notation, for instance "ev" denotes the [[evaluation map]]):

\[
  \label{TransformBetweenBindAndJoinInIntroduction}
  \begin{array}{ll}
  &
  fmap_{D_1, D_2}
  \;\colon\;
  Hom\big(D_1, D_2\big)
  \xrightarrow{ ret \circ (-) }
  Hom\big(D_1,\, T D_2\big)
  \xrightarrow{ bind }
  Hom\big(T D_1,\, T D_2\big)
  \\
  &
  join_D
  \;\colon\;
  T\big( T (D) \big)
  \xrightarrow{
    \big( 
      id_{T T D}, 
      name(id_{T D})  
    \big)
  }
  T T D \times Hom( T D,\, T D )
  \xrightarrow{ bind }
  T D
  \\
  \text{and conversely:}
  \\
  &
  bind_{D, D'}
  \;\colon\;
  T D \times Hom\big( D,\, T D'  \big)
  \xrightarrow{
    \big(
      id_{T D}, fmap_{D, T D'}
    \big)
  }
  T D \times Hom\big( T D , T T D' \big)
  \xrightarrow{\;
    ev
  \;}
  T T D'
  \xrightarrow{\; join \;}
  D'
  \,.
  \end{array}
\]


### Refined idea: Internal monads
 {#RefinedIdea}

But in fact, in [[functional programming]]-[[programming language|languages]] one typically considers an enhanced version of the above situation: 

In these higher-order languages one has, besides the ([[hom-set|hom-]])*[[set]]* of programs/functionw $Hom\big(D_1, \, D_2\big)$ also the actual *[[data type]]* of functions, namely the *[[function type]]* $D_1 \to D_2$, which in terms of [[categorical semantics]] is the *[[internal hom]]-[[hom object|object]]* $Map(D_1, \, D_2)$ in the [[cartesian closed category]] of [[data types]]. Therefore, in such languages (like [[Haskell]]) the [[type]] of the binding operation for given [[data types]] $D_1$, $D_2$ is actually taken to be the [[function type]]/[[internal hom]]

$$
  \begin{array}{ll}
  bind_{D_1, D_2}
  \;\colon\;
  &&
  \big(
     D_1 \to T D_2
  \big)
  \to
  \big(
    T D_1
    \to
    T D_2
  \big)
  \\
  &\simeq &
  T D_1 
  \times
  \big(
     D_1 \to T D_2
  \big)
  \to
    T D_2
  \\
  & \simeq &
  T D_1 
  \to 
  \Big(
    \big(
       D_1 \to T D_2
    \big)
    \to
      T D_2
  \Big)
  \end{array}
$$

(where we used the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the [[product]]$\dashv$[[internal hom]]-[[adjoint functors|adjunction]] to re-identify the [[types]] on the right)

which (beware) is traditionally written without some of the parenthesis, as follows:

$$
  bind_{D_1, D_2}
  \;\colon\;
  T D_1 
    \to 
  \big(
    D_1
    \to
    T D_2
  \big)
  \to
  T D_2
  \,.
$$

In general (except in the [[base topos]] of [[Sets]]), such an iterated [[function type]]/[[internal hom]] is richer than (certainly different from) the corresponding plain [[hom set]], and accordingly a "Kleisli triple" defined as above but with the binding operation typed in this [[internalization|internal]] way is *more* information than a plain [[monad]] on the underlying category of types: namely what is called a *[[strong monad]]* (eg. [McDermott & Uustalu (2022)](#McDermottUustalu22)).

On such a [[strong monad]], the bind operation is defined as the composite

$$
  T(D_1) \times T Map(D_1,\,D_2)
    \xrightarrow{\; strength_T \;}
  T\big(D_1 \times T Map(D_1, \, D_2) \big) 
    \xrightarrow{
      T eval_{D_1, T D_2}
    } 
  T T D_2 
    \xrightarrow{\;
      \mu_{D_2}
    \;} 
  T D_2
  \,.
$$ 

This makes the monads be [[enriched monads]] in the self-enrichment given by the [[function type]]/[[internal hom]]. 

In particular, monads as used in [[Haskell]] are really strong/enriched monads, in this way.

\linebreak

Yet more structure on effect-monads is available in [[dependent type theories]] with [[type universes]], where one may demand that the monad operation $D \mapsto T(D)$ is not just an [[endofunction]] on the [[set]] of [[types]], but an [[endomorphism]] of the [[type universe]]. At least for [[idempotent monads]] this case is further discussed at *[[reflective subuniverse]]* and *[[modal type theory]]* and maybe elsewhere.


