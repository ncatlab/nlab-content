
> This entry is about [[monads]] as known from [[categorical algebra]] but in their application to [[computer science]]. See also at *[[monad (disambiguation)]]*.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}


## Idea
 {#Idea}

In [[computer science]], a *([[comonad|co-]])[[monad]]* (or *([[co-Kleisli category|co-]])[[Kleisli triple]]*, or *(co-)[[extension system]]*) is a kind of [[data type]]-structure which describes "notions of computations" &lbrack;[Moggi (1989)](#Moggi89), [Moggi (1991)](#Moggi91)&rbrack; that may "have external effects or be subject to external contexts/causes" --- such as involving [[random access memory]], [[IO-monad|input/output]], [[exception monad|exception handling]], [[writer monad|writing to]] or [[reader monad|reading from]] global variables,  etc. --- as familiar from [[imperative programming]] but cast as "pure functions" with deterministic and [[verified programming|verifiable behaviour]], in the style of [[functional programming]].

In short, a ("[[extension system]]-style" &lbrack;[Manes (1976), Ex. 3.12](#Manes76)&rbrack; or "[[Kleisli triple]]-style" &lbrack;[Moggi (1991), Def. 1.2](#Moggi91)&rbrack;) *[[monad]]* in a given [[programming language]] consists of *assignments* (but see [below](#RefinedIdea)):

1. to any [[data type|data]] [[type]] $D$ of a new data type $\mathcal{E}(D)$ of "$D$-data with $\mathcal{E}$-effects",

1. to any [[pair]] of $\mathcal{E}$-effectful [[functions]] (programs) of the form $prog_{12} \,\colon\, D_1 \to \mathcal{E}(D_2)$ and $prog_{23} \,\colon\, D_2 \to \mathcal{E}(D_3)$ of an effective-composite function $bind^{\mathcal{E}} prog_{23} \;\circ\; prog_{12}(-) \,\colon\, D_1 \to \mathcal{E}(D_3)$ (their *binding* or *[[Kleisli composition]]*),

1. to any [[data type|data]] [[type]] $D$ of a function $ret^{\mathcal{E}}_D \;\colon\; D \to \mathcal{E}(D)$ assigning "trivial $\mathcal{E}$-effects",

such that the binding is [[associativity|associative]] and also [[unitality|unital]] with respect to the return operation, hence such that [[data types]] with $\mathcal{E}$-effectful programs between them constitute a [[category]] (the *[[Kleisli category]]* of the given effect/monad $\mathcal{E}$).

We now explain in more detail what this means and what it is good for.




### Basic idea: Monadic effects
 {#BasicIdea}

In [[programming language|programming]] it frequently happens that a [[program]] with "nominal" output [[data type]] $D$ *de facto* outputs data of some modified type $T(D)$ which accounts for "external effects" caused by the program, where 
\[
  \label{MonadMapInIntroduction}
  D \;\mapsto\; \mathcal{E}(D)
\]
is some general operation sending [[data types]] $D$ to new data types $\mathcal{E}(D)$.

> For example, if alongside the computation of its nominal output data $d \colon D$ a program also writes a log message $msg \,\colon\,$ [[String (computer science)|String]], then its actual output data is the [[pair]] $(d, msg)$ of [[product type]] $Write(D) \,\coloneqq\, D \times String$.

> Or, dually, if the program may fail and instead "throw an [[exception]] message" $msg \,\colon\,$ [[String (computer science)|String]], then its actual output data is *either* $d \colon D$ *or* $msg \colon String$, hence is of [[coproduct type]] $Excep(D) \,\coloneqq\, D \sqcup String$.

Given such an $\mathcal{E}$-effectful program $prog_{12} \;\colon\; D_1 \to \mathcal{E}(D_2)$ and given a subsequent program $prog_{23} \,\colon\, D_2 \to \mathcal{E}(D_3)$ accepting nominal input data of type $D_2$ and itself possibly involved in further effects of type $\mathcal{E}(-)$, then the *naïve* [[composition]] of the two programs makes no sense (unless $\mathcal{E}(D) = D$ is actually the trivial sort of effect), but their evident *intended* composition is, clearly, obtained by: 

1. first adjusting $prog_{23}$ via a given prescription

   \[
     \label{BindingLawInIntroduction}
     \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
     prog \;\mapsto\; bind^{\mathcal{E}} prog
     \,,
   \]

   such that $bind^{\mathcal{E}} prog_{23} \,\colon\, \mathcal{E}(D_2) \to \mathcal{E}(D_3)$:

   1. does accept data of type $\mathcal{E}(D_2)$ and 

   1. "acts as $prog_{23}$ while *carrying* any previous $\mathcal{E}$-effects along" (this intuition becomes a formal fact below in (eq:FreeEffectHandlingIsBinding));

1. then forming the naive [[composition]] $bind^{\mathcal{E}} prog_{23} \;\circ\;  prog_{12}$

{#BindAndReturnGraphics} as follows:

\begin{imagefromfile}
    "file_name": "KleisliCompositionOfEffectfulPrograms-230927.jpg",
    "width": "840",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


> (Beware that we are denoting by "$bind^{\mathcal{E}} prog (-)$" what in [[programming languages]] like [[Haskell]] [is denoted by](https://wiki.haskell.org/Monad#The_Monad_class) "`(-) >>= prog`"  aka "fish notation", eg. [Milewski 2019 p. 321](#Milewski19), and which some authors denote by an upper-star, "$prog^\ast\,$", e.g.  [Moggi (1991)](#Moggi91); [Uustalu (2021), lecture 1](#Uustalu21Lecture1), [p. 12](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf#page=12).)

Depending on the intended behaviour of these programs, it remains to specify how exactly $bind^{\mathcal{E}} prog_{23}$ "carries $\mathcal{E}(-)$-effects along", hence what the "bind" operation (eq:BindingLawInIntroduction) does concretely. 

> For instance, in the above example of a logging-effect, where $Write(D_2) \,\coloneqq\, D_2 \times String$, the evident way is to use the [[concatenation]]  $String \times String \xrightarrow{\; concat \;} String$ and set:

> $ bind^{Write} prog_{23}\;\coloneqq\; D_2 \times String \xrightarrow{ prog_{23} \times Id_{String} } D_3 \times String \times String \xrightarrow{ Id_{D_3} \times concat } D_3 \times String \,. $

> In the other example above, where the effect is the possible throwing of an [[exception]] message, the evident way to carry this kind of effect along is to use the [[codiagonal]] $\nabla \,\colon\, String \sqcup String \to String$, which amounts to keep forwarding the exception that has already been thrown, if any:

> $bind^{Excep} prog_{23} \;\coloneqq\; D_2 \sqcup String \xrightarrow{ prog_{23} \sqcup Id_{String} } D_3 \sqcup String \sqcup String \xrightarrow{ id_{D_3} \sqcup \nabla } D_3 \sqcup String \,.$

Whatever design choice one makes for how to "carry along effects", it must be consistent in that applying the method to a [[triple]] of $\mathcal{E}$-effectful programs which are nominally composable, then their effectful composition should be unambiguously defined in that it is [[associative]], satisfying the following [[equation]] -- here called the the first "monad law":

\[
  \label{AssociativityConditionInIntroduction}
  bind^{\mathcal{E}} prog_{34}
  \;\circ\;
  \Big(
    bind^{\mathcal{E}}
    prog_{23}
    \;\circ\;
    prog_{12}
  \Big)
  \;\;\;=\;\;\;
  bind^{\mathcal{E}}
  \Big(
    bind^{\mathcal{E}}
    prog_{34}
    \;\circ\;
    prog_{23}
  \Big)
  \;\circ\;
  prog_{12}
  \,.
\]

Finally, for such a notion of effectful programs to be usefully connected to "pure" programs without effects,  it ought to be the case that for any program $prog_{01} \,\colon\, D_0 \xrightarrow{\;} D_1$ that happens to have no $\mathcal{E}$-effects, we have a prescription for how to regard it as an $\mathcal{E}$-effectful program in a trivial way. For that purpose there should be defined an operation

\[  
  \label{ReturnMapInIntroduction}
  ret_{D} \;\colon\; D \xrightarrow{\;} \mathcal{E}(D)
\]

which does nothing but "return" data of type $D$, but re-regarded as effectful $\mathcal{E}(D)$-data in a trivial way; so that we may construct the trivially effectful program $ret^{\mathcal{D}}_{D_1} prog_{01} \;\colon\; D_0 \xrightarrow{\;} \mathcal{E}(D_1)$.

> For instance, in the above example of log-message effects this would be the operation $D \to D \times String$ which assigns the [[empty set|empty]] [[string (computer science)|string]] $ret^{Write} \;\colon\; d \mapsto (d, \varnothing)$.

> In the other example above, of [[exception handling]], the trivial effect $D \to D \sqcup String$ is just not to throw an exception, which is just $ret^{Excep} \;\colon\; d \mapsto d$ (the right [[coprojection]] into the [[coproduct]]).

The final consistency condition (i.e. the remaining "monad law") then is that "carrying along trivial effects is indeed the trivial operation", i.e. that 

\[
  \label{UnitalityInIntroduction}
  bind^{\mathcal{E}}
  prog_{01}
  \;\circ\;
  ret_{D_0}(-)
  \;=\;
  prog_{01}
  \;\;\;\;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;\;\;\;
  bind^{\mathcal{E}}
  ret_{D_1}
  \;\circ\;
  prog_{01}(-)
  \;=\;
  prog_{01}
  \,.
\]

Notice that the [[associativity]] condition (eq:AssociativityConditionInIntroduction) and the [[unitality]] condition (eq:UnitalityInIntroduction) are jointly equivalent to saying that [[data types]] with [[hom-sets]] of $\mathcal{E}$-effectful programs between them, in the above sense, form a *[[category]]*. In [[category theory]] this is known as the *[[Kleisli category]]* $Kl(\mathcal{E})$ of a *[[monad]]* $\mathcal{E}$ on the [[category]] $Type$ of [[data types]] with programs between them:

\[
  \label{TheKleisliCategory}
  \begin{array}{rcl}
    Obj\Big( Kl(\mathcal{E}) \Big)
    &\;\;=\;\;&
    Obj\Big(
      Type
    \Big)
    \\
    Hom\Big( Kl(\mathcal{E}) \Big)\big(D_1,\, D_2\big)
    &\;\;=\;\;&
    Hom\Big(
      Type
    \Big)
    \big(
      D_1, 
      \,
      \mathcal{E}(D_2)  
    \big)
    \\
    (-) \circ_{\mathrm{Kl}(\mathcal{E})} (-)
    &\;\;=\;\;&
    (-) \circ_{Type} bind^{\mathcal{E}}(-)
    \,.
  \end{array}
\]

> Traditionally in [[category theory]], the [[axioms]] on [[monads]] are presented in a somewhat different way, invoking a monad "product" [[natural transformation]] $\mathcal{E} \circ \mathcal{E} \xrightarrow{ \mu } \mathcal{E}$ instead of the "binding" operation. One readily checks that these two axiomatic presentations of monads are in fact equal -- see (eq:TransformBetweenBindAndJoinInIntroduction) below --, but the above "[[Kleisli triple]]/[[extension system]]"-presentation is typically more relevant in the practice of [[functional programming]].

In summary, a choice of *assignments* (but see [below](#RefinedIdea)) to [[data types]] $D_i$ of

1. $\mathcal{E}(D) \;\colon\; Type$,

   namely of types of $\mathcal{E}$-effectful data of nominal type $D$ (eq:MonadMapInIntroduction);

2. $bind^{\mathcal{E}}_{D_1, D_2} \;\colon\;  Hom\big(D_1,\, \mathcal{E}(D_2)\big) \longrightarrow Hom\big(\mathcal{E}(D_1),\,\mathcal{E}(D_2)\big)$,

   namely of how to execute a prog while carrying along any previous effects (eq:BindingLawInIntroduction);

3. $ret^{\mathcal{E}}_D \;\colon\; D \to \mathcal{E}(D)$,

   namely of how to regard plain $D$-data as trivially effectful (eq:ReturnMapInIntroduction)

subject to:

1. the [[associativity]] condition (eq:AssociativityConditionInIntroduction) 

1. the [[unitality]] condition (eq:UnitalityInIntroduction) 

is called a *[[monad in computer science]]* (also: "[[Kleisli triple]]" in [[functional programming]]) and serves to encode the notion that all programs may be subject to certain *external effects* of a kind $\mathcal{E}$ that is specified by the above choices of monad operations.

Here, for the time being (but see [below](#RefinedIdea)), we write $Hom(D_1, D_2)$ for the *[[set]]* of programs/functions taking data of type $D_1$ to data of $D_2$ (the *[[hom set]]* in the plain [[category]] of [[types]]).

> The first running example above is known as the *[[writer monad]]*, since it encodes the situation where programs may have the additional effect of writing a message string into a given buffer.

> The other running example above is naturally called the *[[exception monad]]*.

\linebreak

**Relation to other familiar axioms for monads.**
The above Kleisli/extension-structure, making a [[Kleisli category|Kleisli-style]] [[monad in computer science]], may and often is encoded in different equivalent ways: 

Alternatively postulating operations

1. $D \mapsto \mathcal{E}(D)$ (as before)

1. $fmap^{\mathcal{E}}_{D_1, D_2} \;\colon\; Hom\big(D_1 \to D_2\big) \longrightarrow Hom\big(\mathcal{E}(D_1), \mathcal{E}(D_2)\big)$ 

1. $ret^{\mathcal{E}}_D \;\colon\; D \to \mathcal{E}(D)$

1. $join^{\mathcal{E}}_D \;\colon\; \mathcal{E}\big( \mathcal{E}(D) \big) \to \mathcal{E}(D)$

such that 

1. $fmap^{\mathcal{E}}$ is *[[functor|functorial]]* on [[data types]],

1. $join^{\mathcal{E}}$ is [[associativity|associative]] and [[unitality|unital]] (with respect to $ret$) as a [[natural transformation]],

yields the definition of *[[monad]]* more traditionally used in [[category theory]] (namely as a [[monoid object]] [[internalization|in]] [[endofunctors]], here  on the plain  [[category]] of [[data types]]).

Direct inspection shows that one may [[bijection|bijectively]] transmute such $bind$- and $join$-operators into each other by expressing them as the following composites (using [[category theory]]-notation, for instance "ev" denotes the [[evaluation map]]):

\[
  \label{TransformBetweenBindAndJoinInIntroduction}
  \begin{array}{ll}
  &
  fmap^{\mathcal{E}}_{D_1, D_2}
  \;\colon\;
  Hom\big(D_1, D_2\big)
  \xrightarrow{ ret \circ (-) }
  Hom\big(D_1,\, \mathcal{E}(D_2) \big)
  \xrightarrow{ bind }
  Hom\big( \mathcal{E}(D_1),\, \mathcal{E}(D_2) \big)
  \\
  &
  join^{\mathcal{E}}_D
  \;\colon\;
  \mathcal{E}\big( \mathcal{E}(D) \big)
  \xrightarrow{
    \big( 
      id_{ \mathcal{E} \mathcal{E}(D) }, 
      name(id_{ \mathcal{E} D })  
    \big)
  }
  \mathcal{E} \mathcal{E} D \times Hom\big( \mathcal{E}(D),\, \mathcal{E}(D) \big)
  \xrightarrow{ bind }
  \mathcal{E}(D)
  \\
  \text{and conversely:}
  \\
  &
  bind^{\mathcal{E}}_{D, D'}
  \;\colon\;
  \mathcal{E}(D) \times Hom\big( \mathcal{E}(D),\, \mathcal{E}(D')  \big)
  \xrightarrow{
    \big(
      id_{\mathcal{E} D}, fmap_{D, \mathcal{E} D'}
    \big)
  }
  \mathcal{E} (D) \times Hom\big( \mathcal{E}(D) , \mathcal{E}\mathcal{E}(D') \big)
  \xrightarrow{\;
    ev
  \;}
  \mathcal{E} \mathcal{E}(D')
  \xrightarrow{\; join \;}
  D'
  \,.
  \end{array}
\]


### Refined idea: Strong monads
 {#RefinedIdea}

But in fact, in [[functional programming]]-[[programming language|languages]] one typically considers an enhanced version of the above situation: 

In these higher-order languages one has, besides the ([[hom-set|hom-]])*[[set]]* of programs/functions $Hom\big(D_1, \, D_2\big)$ also the actual *[[data type]]* of functions, namely the *[[function type]]* $D_1 \to D_2$, which in terms of [[relation between type theory and category theory|categorical semantics]] is the *[[internal hom]]-[[hom object|object]]* $Map(D_1, \, D_2)$ in the [[cartesian closed category]] of [[data types]]. Therefore, in such languages (like [[Haskell]]) the [[type]] of the binding operation for given [[data types]] $D_1$, $D_2$ is actually taken to be the [[function type]]/[[internal hom]]

$$
  \begin{array}{ll}
  bind^{\mathcal{E}}_{D_1, D_2}
  \;\colon\;
  &&
  \big(
     D_1 \to \mathcal{E}(D_2)
  \big)
  \to
  \big(
    \mathcal{E}(D_1)
    \to
    \mathcal{E}(D_2)
  \big)
  \\
  &\simeq &
  \mathcal{E}(D_1) 
  \times
  \big(
     D_1 \to \mathcal{E}(D_2)
  \big)
  \to
    \mathcal{E}(D_2)
  \\
  & \simeq &
  \mathcal{E}(D_1) 
  \to 
  \Big(
    \big(
       D_1 \to \mathcal{E}(D_2)
    \big)
    \to
      \mathcal{E}(D_2)
  \Big)
  \end{array}
$$

> (where we used the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of the [[product]]$\dashv$[[internal hom]]-[[adjoint functors|adjunction]] to re-identify the [[types]] on the right)

which (beware) is traditionally written without many of the parenthesis, as follows:

$$
  bind^{\mathcal{E}}_{D_1, D_2}
  \;\colon\;
  \mathcal{E} D_1
    \to 
  \big(
    D_1
    \to
    \mathcal{E} D_2
  \big)
  \to
  \mathcal{E} D_2
  \,.
$$

In general (except in the [[base topos]] of [[Sets]]), such an iterated [[function type]]/[[internal hom]] is richer than (certainly different from) the corresponding plain [[hom set]], and accordingly a "Kleisli triple" defined as above but with the binding operation typed in this [[internalization|internal]] way is *richer* or *stronger* [[structure]] than that of a plain [[monad]] on the underlying category of types: namely it is an *[[enriched monad]]* or [equivalently](enriched+monad#RelationToStrongMonads) a *[[strong monad]]*  with respect to the self-[[enriched category|enrichment]] of the [[symmetric monoidal closed category]] of types ([Moggi 1991 §3](#Moggi91), cf. [Goubault-Larrecq, Lasota & Nowak 2002](#GLLN08), [McDermott & Uustalu (2022)](#McDermottUustalu22)).

On such an [[enriched monad|enriched]]/[[strong monad]], the bind operation is defined as the following composite:

$$
  \mathcal{E}(D_1) \times \mathcal{E} Map(D_1,\,D_2)
    \xrightarrow{\; strength_{\mathcal{E}} \;}
  \mathcal{E}\big(D_1 \times Map(D_1, \, \mathcal{E} D_2) \big) 
    \xrightarrow{
      \mathcal{E} eval_{D_1, \mathcal{E} D_2}
    } 
  \mathcal{E} \mathcal{E} D_2 
    \xrightarrow{\;
      \mu_{D_2}
    \;} 
  \mathcal{E} D_2
  \,.
$$ 

In particular, monads as used in [[functional programming languages]] like [[Haskell]] are really strong/enriched monads, in this way.

In this case -- and in most discussions by default -- the [[symmetric monoidal closed category]] of types is assumed to be [[cartesian closed category|cartesian closed]] ("classical types") but in contexts of [[linear type theory]] (such as [[quantum computation]]) it may be non-cartesian (or both: cf. [[doubly closed monoidal category]]).


\linebreak

Yet more structure on effect-monads is available in [[dependent type theories]] with [[type universes]], where one may demand that the monad operation $D \mapsto T(D)$ is not just an [[endofunction]] on the [[set]] of [[types]], but an [[endomorphism]] of the [[type universe]]. At least for [[idempotent monads]] this case is further discussed at *[[reflective subuniverse]]* and *[[modal type theory]]* and maybe elsewhere.


### Further idea: Monad modules
 {#MonadModulesInIdeaSection}

Further in the practice of [[programming language|programming]]: if programs may cause external effects, as [above](#BasicIdea), then one will often want to have some of them *handle* these effects.

> This is particularly evident in the [above](#BasicIdea) running examples of *[[exceptions]]* whose whole design purpose typically is to be handled when they arise.

Since a "handling" of $\mathcal{E}$-effects should mean that these be done with and turned into pure data of some actual [[type]] $D$, an $\mathcal{E}$-effect handler on(to) a data type $D$ should primarily consist of a program of the form

$$
  \mathcal{E}(D) \to D
  \,.
$$

that handles effects produced by $\mathcal{E}$-effectful programs $D' \to \mathcal{E}(D)$, turning them into pure computations $D' \to D$. 

But in addition, such a handler needs to handle effects that have been "carried along" (eq:BindingLawInIntroduction) from previous computations, even along otherwise in-effectful computations $prog_{0,1} \;\colon\; D_{0} \to D_{1}$; therefore all these need to be assigned handlers:

$$
  hndl^{\mathcal{E}}_{D_2} prog_{1,2} 
  \;\colon\; 
  \mathcal{E}(D_1) \to D_2
  \,.
$$

Of such choice of effect handling, consistency demands that:

1. first handling all previous effects carried along (eq:BindingLawInIntroduction) and then the newly produced effects by a given $prog \,\colon\, D \to \mathcal{E}(D')$ has the same result as letting $prog$ take care of carrying along previous effects by passing to $prog[-]$ and then handling the resulting accumulation at once:

1. handling the trivial effect ought to be no extra operation:

\[
  \label{AxiomsForEffectHandlers}
\]
\begin{imagefromfile}
    "file_name": "MonadicEffectHandlerConditions-221105b.jpg",
    "width": "560",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


A data structure consisting of such assignments $hndl^{\mathcal{E}}$ subject to these "laws" is known as an *Kleisli triple algebra* (e.g. [Uustalu (2021), Lec. 2](#Uustalu21Lecture2)) or *algebra over an extension system* (see [here](algebra+over+a+monad#ReferencesKleisliStyle)) for $\mathcal{E}$ and is bijectively the same as what in traditional [[category theory]] is known as an *[[algebra over a monad|algebra over $\mathcal{E}$]]* or *$\mathcal{E}$-algebra* or, maybe best: an *$\mathcal{E}$-module* or *$\mathcal{E}$-[[modal type]]*.

Given a [[pair]] of such $\mathcal{E}$-[[modal types]] $\big(D_1, hndl^{\mathcal{E}}_{D_1} \big)$, $\big(D_2, hndl^{\mathcal{E}}_{D_2} \big)$, a function $\phi \,\colon\, D_1 \to D_2$ is a *[[homomorphism]]* between them if the result of handling $\mathcal{E}$-effects before or after applying $\phi$ is the same, hence
if for all functions $f \,\colon\, D_0 \to D_1$ the following [[commuting diagram|diagram commutes]]:


\begin{imagefromfile}
    "file_name": "HomomorphismOfMonadiEffectHandlers-221105.jpg",
    "width": "350",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\linebreak

{#FreeModales} **Free $\mathcal{E}$-effect handlers.** Notice that [above](#BasicIdea) we motivated already the binding operation (eq:BindingLawInIntroduction) as a kind of $\mathcal{E}$-effect handling: namely as the "carrying along" of previous $\mathcal{E}$-effects. This intuition now becomes a precise statement: 

For any $D_2 \;\colon\; Type$ we may tautologically handle (eq:AxiomsForEffectHandlers) $\mathcal{E}$-effects by absorbing them into the data type $\mathcal{E}(D_2)$, with the effect-handler simply being the effect-binding operation (eq:BindingLawInIntroduction):

\[
  \label{FreeEffectHandlingIsBinding}
  hndl^{\mathcal{E}}_{\mathcal{E}(D_2)}
  \Big(
     D_1 
     \xrightarrow{ prog }
     \mathcal{E}(D_2)
  \Big)
  \;\coloneqq\;
  bind^{\mathcal{E}}
  prog
  \;\colon\;
  \mathcal{E}(D_1)
  \to
  \mathcal{E}(D_2)
  \,.
\]

The $\mathcal{E}$-effect-handlers (eq:AxiomsForEffectHandlers) arising this way are called *[free](algebra+over+a+monad#FreeAlgebras)*. 

The [[full subcategory]] of free $\mathcal{E}$-effect handlers among [[Eilenberg-Moore category|all]] $\mathcal{E}$-[[modal types]] is known as the *[[Kleisli category]]*. By the [Kleisli equivalence](Kleisli+category#KleisliEquivalence), this is [[equivalence of categories|equivalent]] to the (plain) category (eq:TheKleisliCategory) of $\mathcal{E}$-effectful programs that we started with. Here this means that:

* *Plain data types with $\mathcal{E}$-effectful programs betweem them are equivalently data types freely equipped with the structure of $\mathcal{E}$-effect handlers.*

which makes a lot of sense.

\linebreak


### Dual idea: Comonadic contexts
 {#DualIdeaComonadicCauses}

\begin{imagefromfile}
    "file_name": "Overton-CoMonadHaskell.jpg",
    "float": "right",
    "width": 550,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 30
    },
    "caption": "(from [Overton 2014](#Overton14))"
\end{imagefromfile}


By [[formal duality]], all of the above discussion has a dual version, where now (e.g. [Uustalu & Vene (2008)](#UustaluVene08), [POM13](#POM13), [GKOBU16](#GKOBU16), [KRU20](#KRU20)):

* [[comonads]] encode *computational contexts* (*co-effects*),

* their [[coproduct]] operation is the *duplication* (*co-join*) of contexts  which serves to *extend* (*co-bind*) contexts over consecutive programs,

* [[comodules over comonads]] are data structures that *provide* (*co-handle*) such context.


In more detail:


* Above we had that:

  * A [[Kleisli map]] for a [[monad]] $\mathcal{E}$ is a program 

    $$ 
      prog \;\colon\; D \to \mathcal{E}(D')
    $$

    *causing* an external $\mathcal{E}$-effect.

  * A Kleisli-module for a [[monad]] $\mathcal{E}T$ is a prescription 

    $$
      hdl^{\mathcal{E}}_D id_D \;\colon\; \mathcal{E}(D) \to D
    $$
  
    for *handling* such $\mathcal{E}$-effects.

* Now dually:

  * A [[co-Kleisli map]] for a [[comonad]] $\mathcal{C}$ is a program 

    $$
      prog \;\colon\; \mathcal{C}(D) \to D'
    $$

    *subject to* an external $\mathcal{C}$-"*context*" ([Uustalu & Vene (2008)](#UustaluVene08), [POM13](#POM13))

    (a $\mathcal{C}$-*cause*).

  * A co-Kleisli co-module for a comonad $\mathcal{C}$ is a program 

    $$
      prvd^{\mathcal{C}}_D id_D \;\colon\; D \to \mathcal{C}(D)
    $$

    *producing* or *providing* such $\mathcal{C}$-contexts.

     (cf. &lbrack;[Uustalu (2021), Lect. 3, slide 9](#Uustalu21Lecture3)&rbrack;)


\begin{imagefromfile}
    "file_name": "CoKleisliCompOfContextfulPrograms-230815.jpg",
    "width": "800",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}
 
\linebreak


### Syntactic idea: Do-notation
 {#DoNotation}

Finally, to turn all this into an efficient [[programming language]] one just has to declare a convenient [[syntax]] for denoting [[Kleisli composition]]. 

One such syntax is known as "*do notation*" (introduced with "`{...}`" instead of "`do`" by [Launchbury 1993 §3.3](#Launchbury93), then promoted by [[Mark Jones]] in the 1990s &lbrack;[HHPW07, p. 25](Haskell#HHPW07)&rbrack; and adopted by [[Haskell]] in [version 1.3](https://www.haskell.org/definition/from12to13.html#do), for review see [Benton, Hughes & Moggi 2002 p. 70](#BentonHughesMoggi02), [Milewski 2019 §20.3](#Milewski19)), which aims to jointly express: 

1. successive Kleisli composition in words like "do this, do that, and return the result",

1. any intermediate bind-operation as "extracting" a $D$-datum $d$ out of an $\mathcal{E}(D)$-datum $E$ with notation `d <- E`

Syntactically, do-notation is the following [[syntactic sugar]] for combined [[Kleisli composition]] and [[bound variable|variable binding]]:

1. `do prog` $\;\;\equiv\;\;$ `prog`

2. `do prog1 prog2` $\;\;\equiv\;\;$ `prog1 bind (\_ -> prog2)`

3. `do (x <- prog1) prog2` $\;\;\equiv\;\;$ `prog1 bind (\x -> prog2)`
 
This is, first of all, a suggestive notation (in fact a "[[domain specific embedded programming language]]", see [there](domain+specific+embedded+programming+language#RelationToMonadicEffects)) for expressing effect-binding:

\begin{imagefromfile}
    "file_name": "EffectBindingViaDoNotation-230828.jpg",
    "width": "350",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

but thereby it furthermore provides a convenient means of expressing successive Kleisli-composition simply by successivley "calling" the separate procedures, much in the style of [[imperative programming]] (which thereby is emulated/encapsulated by pure [[functional programming]]): 

\begin{imagefromfile}
    "file_name": "KleisliCompositeInDoNotation-230826.jpg",
    "width": "520",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

but the notation becomes more suggestive with the rule that the "`<-`"-symbols may notationally be suppressed for functions with trivial in- or out-put (ie. of [[unit type]] $\ast$) besides their $\mathcal{E}$-effect, as in this example:

\begin{imagefromfile}
    "file_name": "PureEffectKleisliCompositeInDoNotation-230826.jpg",
    "width": "520",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This case brings out clearly how the ambient "`do`...`return`"-syntax block expresses the (Kleisli-)composition of any number of $\mathcal{E}$-effectful procedures.

On top of that the "`<-`"-syntax is meant to be suggestive of *reading out* a value. This is accurate imagery for the [[state monad]] (and its abstraction to the [[IO-monad]]), where from the two pasic operations of reading/writng a global variable 
$$
  \array{
    read &\colon& W State(W)
    \\
    read &\equiv& w \mapsto (w,w)
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \array{
    write &\colon& W \to W State(\ast)
    \\
    write &\equiv& w \mapsto (w' \mapsto w)
  }
$$
any $W$-stateful program, such as the simple example
$$
  \array{
    inc &\colon& \mathbb{N}State(\ast)
    \\
    inc &\equiv& n \mapsto n+1 
  }
$$
may be constucted in do-notation, such as:

\begin{imagefromfile}
    "file_name": "StatefulNumberIncrementInDONotation-230828.jpg",
    "width": 560,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

For a similar effect monad such as the [[list monad]] the analogous `do`-code for incrementing all entries in a list of numbers looks as follows:

\begin{imagefromfile}
    "file_name": "ListReadKleisliCompositeInDoNotation-230826.jpg",
    "width": "520",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Here The `do`-notation on the right evokes the idea that in *each step* a number $n \colon \mathbb{N}$ is "read out" from MyList and then its increment returned --- but leaves linguistically implicit the idea that this operation is to be performed *for all elements* of the list and all results re-compiled into an output list.

Indeed, in general it is misleading to think of Kleisli composition as being about "reading out" data. What Kleisli composition is really about is acting on data that has *generators* and defining a program by what it does *on generators*, hence *for* a given generating datum:

\begin{imagefromfile}
    "file_name": "KleisliMapsActOnGeneratingData-23-828.jpg",
    "width": 560,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Therefore the conceptually more accurate (if maybe less concise) program-linguistic reflection of the monadic effect-binding operation would be a "`for`...`do`"-block:

\begin{imagefromfile}
    "file_name": "ForDoNotation-230827c.jpg",
    "width": "420",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

In terms of such for-do-notation, the generic case that we started with above has the following syntactic rendering:


\begin{imagefromfile}
    "file_name": "KleisliCompositeInForDoNotation-230826.jpg",
    "width": "670",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This syntax may be notationally less concise but it evokes rather closely what is actually going on in programming with monadic effects. 

For example, the above operation of icrementing all numbers in a given list reads in `for`...`do`-notation as follows:

\begin{imagefromfile}
    "file_name": "ListIncrementViaForDo-280827b.jpg",
    "width": "750",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

neatly indicative of how the operation $+1$ is applied *for* every number $n$ found *in* the list.

(NB.: There is no clash with `for`...`do`-notation as used for loops in [[imperative programming]], since [[functional programming|functionally]] these are instead expressed by [[recursion]].) 

The appropriateness of rendering effect binding as a `for`...`do`-expression becomes yet more pronounced in contexts of [[substructural logic|substructural]] [[type theory|typing contexts]] such as in [[linear type theory]], where the idea of "reading out" of monadic types via "`<-`"-notation becomes yet more dubious.

For example, consider the [[relative monad]] ([this example](relative+monad#LinearSpan)) which sends [[sets]] to the [[vector spaces]] that are their [[linear spans]]:

$$
  \array{
    \mathllap{\mathrm{Q} \;\;\colon\;\;}
    Set &\longrightarrow& Vect
    \\
    W &\mapsto& \underset{W}{\oplus} \mathbb{1}
  } 
$$

with
$$
  \array{
    \mathllap{bind^{\mathrm{Q}} \;\;\colon\;\;}
    (W  \to \mathrm{Q}W') 
    &\longrightarrow& 
    (\mathrm{Q}W \to \mathrm{Q}W')
    \\
    \left(
      w
      \mapsto
      \left\vert \psi_w \right\rangle
    \right)
    &\mapsto&
    \left(
      \sum_w q_{{}_W} \left\vert w \right\rangle
      \,\mapsto\,
      \sum_w q_{{}_w} \left\vert \psi_w \right\rangle
    \right)
  } 
$$

In this case the traditional `do`-notation would suggest that given a vector one may "read out" a basis element from it -- which does not make conceptual sense. 

Instead, what's really happening is that to define a linear map $G \colon \mathrm{Q}W \to \mathscr{H}$ on a vector space equipped with a [[basis of a vector space|linear basis]] $W$ (literally: a set of free [generators](basis+of+a+vector+space#GeneratedVectorSpace)) it is sufficient to define this map *for* each basis-vector $\left\vert w \right\rangle$ --- and this is just what the `for`...`do`-notation for the $\mathrm{Q}$-monad expresses:

\begin{imagefromfile}
    "file_name": "LinearMapInForDoNotation-230828.jpg",
    "width": "150",
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}








\linebreak

## Examples
 {#Examples}


### Definable monads

Various monads are _definable_ in terms of standard [[type formation|type-forming operations]] (such as [[product types]], [[function types]], etc.). These include the following (cf. [Moggi 1991, Exp. 1.1](#Moggi91)):

* The *[[maybe monad]]* encodes possible controlled failure of a program to execute.

* An *[[exception monad]]*, more generally, encodes possible controlled failure together with the output of an error "message" in the general form of data of some type.

* The *[[reader monad]]* and *[[coreader comonad]]* both encode reading out a global parameter.

* The *[[writer monad]]* and *[[cowriter comonad]]* both encode writing *consecutively* into a global resource, such as for a [[stream]].

* The *[[state monad]]* encodes the possibility of *consecutive reading and re-setting* a global parameter  -- this provides a notion of *[[random access memory]]*.

* The *[[costate comonad]]* encodes a way (a "[[lens in computer science|lens]]") to read and write fields in [[databases]].

* The *[[continuation monad]]* encodes [[continuation-passing style]] of program execution.

* The *[[selection monad]]* encodes selecting a value of a type depending on the values of some function on it.

#### State monad and Random access memory
 {#StateMonad}

A [[functional program]] with input of [[type]] $D$, output of [[type]] $D'$ and *mutable state $W$* is a [[function]] ([[morphism]]) of [[type]] $D \times W \longrightarrow D' \times W$ -- also called a *[[Mealy machine]]* (see [there](Mealy+machine#MealyMachinesAsEffectfulMaps)). 

Under the ([[Cartesian product]] $\dashv$ [[internal hom]])-[[adjunction]] ([[currying]]) this is equivalently given by its [[adjunct]], which is a function of type $D \longrightarrow [W, W \times D' ]$. Here the operation $[W, W\times (-)]$ is the [[monad]] induced by the above adjunction and this latter function is naturally regarded as a morphism in the [[Kleisli category]] of this monad. This monad $[W, W\times (-)]$ is called the _[[state monad]]_ for mutable states of type $W$:

<center>
<img src="/nlab/files/State-Effectful-Program-230804.jpg" width="600">
</center>



#### Maybe monad and Controlled failure

The **[[maybe monad]]** is the operation $X \mapsto X \coprod \ast$. The idea here is that a function $X \longrightarrow Y$ in its [[Kleisli category]] is in the original category a function of the form $X \longrightarrow Y \coprod \ast $ so either returns indeed a value in $Y$ or else returns the unique element of the [[unit type]]/[[terminal object]] $\ast$. This is then naturally interpreted as "no value returned", hence as indicating a "failure in computation".

#### Exception monad and Exception handling

(...) [[exception monad]] (...)

#### Continuation monad and Continuation-passing

The [[continuation monad]] on a given type $S$ acts by $X \mapsto [[X,S],S]$.

(...)



### Axiomatic monads

Other monads may be supplied "axiomatically" by the programming language, meaning that they are data structures [[type|typed]] as monads, but whose actual type formation, binding- and return-operations are special purpose operations provided by the programming environment.

This includes:

* the *[[IO monad]]* in [[Haskell]],

* the *[[completion monad]]*, as in [[constructive analysis]], used for dealing for instance with [[real numbers]].

In this vein:

* Equipping [[homotopy type theory]] (say implemented as a programming language concretely in [[Coq]] or [[Agda]]) with two axiomatic [[idempotent monads]], denoted $\sharp$ and $\Pi$, with some additional data and relations, turns it into _[[cohesive homotopy type theory]]_. See also at *[Agda flat](Agda#AgdaFlat)* and at *[[modal type theory]]*.


## Related concepts

* [[extension system]]

  * [[relative monad]]

  * [[polynomand]]

* [[relation between type theory and category theory]], [[categorical semantics]], [[categorical logic]]

* Examples of (co)monads in ([[homotopy type theory|homotopy]]) [[type theory]] involve in particular _[[modal operators]]_ as they  appear in 

  * [[modal logic]]/[[modal type theory]]/[[computational type theory]].

  See also:

  * [[adjoint modality]].

* For an approach to composing monads, see

  * [[monad transformer]]

* Another approach to modelling side effects in [[functional programming languages]] are 

  [[algebraic side effects]]

* [[free monad|Free monads]] in computer science appear in the concepts of 

  * [[initial algebra for an endofunctor]]

  * [[terminal coalgebra for an endofunctor]]

* Other generalizations are:

  * [[arrow (in computer science)]]

  * [[applicative functor]]

* There is also: [[monad (in linguistics)]]


## References

### General
 {#ReferencesGeneral}

The [[extension system]]-style presentation of monads as used in computer science is briefly mentioned in:

* {#Manes76} [[Ernest G. Manes]], Sec 3, Ex. 12 (p. 32) of: *Algebraic Theories*, Springer (1976) &lbrack;[doi:10.1007/978-1-4612-9860-1](https://doi.org/10.1007/978-1-4612-9860-1)&rbrack;

and expanded on in

* {#MarmolejoWood10} [[Francisco Marmolejo]], [[Richard J. Wood]], *Monads as extension systems -- no iteration is necessary*, [[TAC]] **24** 4 (2010) 84-113 &lbrack;[tac:24-04](http://www.tac.mta.ca/tac/volumes/24/4/24-04abs.html)&rbrack;

but not related there to computation.

The original observation of monads as "notions of computation" is:

* {#Moggi89} [[Eugenio Moggi]], *Computational lambda-calculus and monads*, in: *Proceedings of the Fourth Annual Symposium on Logic in Computer Science* (1989) 14-23 &lbrack;[doi:10.1109/LICS.1989.39155](https://doi.org/10.1109/LICS.1989.39155)&rbrack;

* {#Moggi89Abstract} [[Eugenio Moggi]], *An abstract View of Programming Languages*, LFCS report ECS-LFCS-90-113 (1989) &lbrack;[web](http://www.lfcs.inf.ed.ac.uk/reports/90/ECS-LFCS-90-113), [[Moggi-AbstractView.pdf:file]]&rbrack;

  > (considers also [transformations of monads](monad#BicategoryOfMonads) in Def. 4.0.8)

* [[Philip Wadler]], *Comprehending Monads*, in _Conference on Lisp and functional programming_, ACM Press (1990) &lbrack;[[WadlerMonads.pdf:file]], [doi:10.1145/91556.91592](https://doi.org/10.1145/91556.91592)&rbrack;

* {#Moggi91} [[Eugenio Moggi]], *Notions of computation and monads*, Information and Computation, **93** 1 (1991) &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90052-4">doi:10.1016/0890-5401(91)90052-4</a>, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf)&rbrack;

* [[Philip Wadler]], *The essence of functional programming*, *POPL '92: Principles of programming languages* (1992) 1-14 &lbrack;[doi:10.1145/143165.143169](https://doi.org/10.1145/143165.143169), [pdf](https://jgbm.github.io/eecs762f19/papers/wadler-monads.pdf)&rbrack;

Further discussion:

* [[Gordon Plotkin]], [[John Power]], *Notions of Computation Determine Monads*, in: *Foundations of Software Science and Computation Structures* FoSSaCS 2002, Lecture Notes in Computer Science **2303**, Springer (2002) &lbrack;[doi:10.1007/3-540-45931-6_24](https://doi.org/10.1007/3-540-45931-6_24), [era:1842/196](https://era.ed.ac.uk/handle/1842/196)&rbrack; 

On the impact of [Moggi (1991)](#Moggi91):

* [[Martin Hyland]], [[John Power]], §6 of: *The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads*, Electronic Notes in Theor. Comp. Sci. **172** (2007) 437-458 &lbrack;[doi:10.1016/j.entcs.2007.02.019](https://doi.org/10.1016/j.entcs.2007.02.019), [preprint](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf)&rbrack;

Origin of the [[do-notation]] for [[Kleisli composition]] of effectful programs:

* {#Launchbury93} [[John Launchbury]], §3.3 in: *Lazy imperative programming*, Proceedings of *ACM Sigplan Workshop on State in Programming Languages*, Copenhagen (1993) &lbrack;[pdf](https://launchbury.files.wordpress.com/2019/01/lazy-imperative-programming.pdf), [[Launchbury-LazyImperative.pdf:file]]&rbrack;

Introducing the notion of [[monad transformers]]:

* {#Espinosa94} [[David A. Espinosa]], §3.2 in: *Building Interpreters by Transforming Stratified Monads* (1994) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-StratifiedMonads.pdf:file]]&rbrack;

* {#Espinosa95} [[David A. Espinosa]], §2.6 in: *Semantic Lego*, PhD thesis, Columbia University (1995) &lbrack;[pdf](https://github.com/davidespinosa01/papers/blob/master/E/Espinosa%20David/espinosa-stratified-monads.pdf), [[Espinosa-SemanticLego.pdf:file]], slides:[pdf](https://github.com/davidespinosa01/papers/blob/346c2ded6af78805701106d51daee8f7a756c948/E/Espinosa%20David/espinosa-thesis-slides.pdf), [[Espinosa-SemanticLego-slides.pdf:file]]&rbrack;

* {#LiangHudakJones95} Sheng Liang, [[Paul Hudak]], [[Mark Jones]], *Monad transformers and modular interpreters*, POPL '95 (1995) 333–343 &lbrack;[doi:10.1145/199448.199528](https://doi.org/10.1145/199448.199528)&rbrack;


More (early) literature is listed here:

* [[David A. Espinosa]], *[Effects bibliography](https://github.com/davidespinosa01/effects-bibliography)*   

In the generality of [[relative monads]]:

* [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], Section 2 of: *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;


The dual notion of [[comonads in computer science]] as modelling *contexts*: 

* {#UustaluVene08}  [[Tarmo Uustalu]], [[Varmo Vene]], *Comonadic Notions of Computation*, Electronic Notes in Theoretical Computer Science **203** 5 (2008) 263-284 &lbrack;[doi:10.1016/j.entcs.2008.05.029](https://doi.org/10.1016/j.entcs.2008.05.029)&rbrack;

* {#POM13} [[Tomas Petricek]], [[Dominic Orchard]], [[Alan Mycroft]], *Coeffects: Unified Static Analysis of Context-Dependence*, in: *Automata, Languages, and Programming. ICALP 2013*, Lecture Notes in Computer Science **7966** Springer (2013) &lbrack;[doi:10.1007/978-3-642-39212-2_35](https://doi.org/10.1007/978-3-642-39212-2_35)&rbrack;

* {#Overton14} David Overton, *Comonads in Haskell* (2014) &lbrack;[web](https://speakerdeck.com/dmoverton/comonads-in-haskell), [[Overton-ComonadsHaskell.pdf:file]]&rbrack;

  > (in [[Haskell]])
   

on codo-notation for comonadic contexts:

* [[Dominic Orchard]], [[Alan Mycroft]], *A Notation for Comonads*, in: *Implementation and Application of Functional Languages. IFL 2012*, Lecture Notes in Computer Science **8241** &lbrack;[doi:10.1007/978-3-642-41582-1_1](https://doi.org/10.1007/978-3-642-41582-1_1)&rbrack;


and emphasis on the combination of [[monads]], [[comonads]] and [[graded modalities]]:

* {#GKOBU16} Marco Gaboardi, [[Shin-ya Katsumata]], [[Dominic Orchard]], Flavien Breuvart, [[Tarmo Uustalu]], *Combining effects and coeffects via grading*, ICFP 2016: Proceedings of the 21st ACM SIGPLAN International Conference on Functional Programming (2016) 476–489 &lbrack;[doi:10.1145/2951913.2951939](https://doi.org/10.1145/2951913.2951939), [talk abstract](https://icfp16.sigplan.org/details/icfp-2016-papers/31/Combining-Effects-and-Coeffects-via-Grading), [video rec](https://www.youtube.com/watch?v=l1ZNMT3fQCo)&rbrack;

* {#KRU20} [[Shin-ya Katsumata]], Exequiel Rivas, [[Tarmo Uustalu]], LICS (2020) 604-618 *Interaction laws of monads and comonads* &lbrack;[arXiv:1912.13477](https://arxiv.org/abs/1912.13477), [doi:10.1145/3373718.3394808](https://doi.org/10.1145/3373718.3394808)&rbrack;

The identification of (co)effect handling with ([[comodule over a comonad|co]])[[modules over a monad|modales]] over the given (co)monad:

* [[Gordon D. Plotkin ]], [[Matija Pretnar]], *Handling Algebraic Effects*, Logical Methods in Computer Science, **9** 4 (2013) lmcs:705 &lbrack;[arXiv:1312.1399](https://arxiv.org/abs/1312.1399), <a href=" https://doi.org/10.2168/LMCS-9(4:23)2013">doi:10.2168/LMCS-9(4:23)2013</a>&rbrack;

* Ohad Kammar, Sam Lindley, Nicolas Oury, *Handlers in action*, ACM SIGPLAN Notices **48** 9 (2013) 145–158 &lbrack;[doi:10.1145/2544174.2500590](https://doi.org/10.1145/2544174.2500590)&rbrack;

{#ReferencesInActualPorgrammingLanguages} Discussion in actual [[programming languages]] such as [[Haskell]]:

* {#BentonHughesMoggi02} [[Nick Benton]], [[John Hughes]], [[Eugenio Moggi]], *Monads and Effects*, in: *Applied Semantics*, Lecture Notes in Computer Science **2395**, Springer (2002) 42-122 &lbrack;[doi:10.1007/3-540-45699-6_2](https://doi.org/10.1007/3-540-45699-6_2)&rbrack;

* {#Milewski19} [[Bartosz Milewski]] (compiled by Igal Tabachnik), "Monads: Programmer's Definition", §20 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;

* {#Milewski23} [[Bartosz Milewski]], §14 in: *The Dao of Functional Programming* (2023) &lbrack;[pdf](https://github.com/BartoszMilewski/Publications/blob/master/TheDaoOfFP/DaoFP.pdf), [github](https://github.com/BartoszMilewski/Publications/tree/master/TheDaoOfFP)&rbrack;

and [[Scala]]:

* {#Winitzki22} [[Sergei Winitzki]], Section 10 of: *The Science of Functional Programming -- A tutorial, with examples in Scala* (2022) &lbrack;[leanpub:sofp](https://leanpub.com/sofp), [github:sofp](https://github.com/winitzki/sofp)&rbrack;



Further discussion/exposition of the notion and application of (co)monads in computer science:
 
* {#BrookesGeva91} [[Stephen Brookes]], Shai Geva, *Computational Comonads and Intensional Semantics*, CMU-CS-91-190 (1991) &lbrack;[[BrookersGeva-ComputationalComonads.pdf:file]]&rbrack;

* [[Philip Wadler]], *Monads for functional programming*, in M. Broy (eds.) *Program Design Calculi* NATO ASI Series, **118** Springer (1992) &lbrack;[doi;10.1007/978-3-662-02880-3_8](https://doi.org/10.1007/978-3-662-02880-3_8), [pdf](https://homepages.inf.ed.ac.uk/wadler/papers/marktoberdorf/baastad.pdf)&rbrack;
* Philip Mulry, _Monads in semantics_ , ENTCS **14** (1998) pp.275-286.

* {#BrookesVanStone93} [[Stephen Brookes]],  [[Kathryn Van Stone]], *Monads and Comonads in Intensional Semantics* (1993) &lbrack;[dtic:ADA266522](https://apps.dtic.mil/sti/citations/ADA266522), [pdf](https://www.cs.cmu.edu/~brookes/papers/MonadsComonads.pdf), [[BrookesVanStone-CoMonads.pdf:file]]&rbrack;

  > (with [[distributive law]] of comonad over monad)

* [[John Hughes]], section 2 of: _Generalising Monads to Arrows_, Science of Computer Programming (Elsevier) 37 (1-3): 67&#8211;111. (2000) ([pdf](http://pdn.sciencedirect.com/science?_ob=MiamiImageURL&_cid=271600&_user=10&_pii=S0167642399000234&_check=y&_origin=search&_zone=rslt_list_item&_coverDate=2000-05-31&wchp=dGLzVlk-zSkWb&md5=fa91ab4ffc136b0cedc52318c7c249be&pid=1-s2.0-S0167642399000234-main.pdf))

* {#Harper} [[Robert Harper]], _Of course ML Has Monads!_ (2011) ([web](http://existentialtype.wordpress.com/2011/05/01/of-course-ml-has-monads/))

* {#Benton15} [[Nick Benton]], _Categorical Monads and Computer Programming_, in: *[Impact150: stories of the impact of mathematics](https://www.lms.ac.uk/2015/impact150-stories-impact-mathematics)*. London Mathematical Society (2015)  &lbrack;[pdf](https://www.lms.ac.uk/sites/lms.ac.uk/files/2.%20Benton%20-%20Categorical%20Monads%20and%20Computer%20Programming.pdf), [[Benton-CategoricalMonads.pdf:file]], [doi:10.1112/i150lms/t.0002](https://www.lms.ac.uk/2015/impact150-stories-impact-mathematics)&rbrack;

* {#Riehl17} [[Emily Riehl]], *A categorical view of computational effects*, talk at *[C$\circ$mp$\circ$se$\colon\!\colon$Conference](https://www.composeconference.org/2017/)* (2017) &lbrack;[pdf](http://www.math.jhu.edu/~eriehl/compose.pdf), [[Riehl-ComputationalEffects.pdf:file]]&rbrack;

* Rob Norris, *Functional Programming with Effects*, talk at 
*Scala Days 2018* &lbrack;video: [YT](https://youtu.be/30q6BkBv5MY)&rbrack;

* {#Uustalu21} [[Tarmo Uustalu]], lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021):

  {#Uustalu21Lecture1} *Monads and Interaction Lecture 1* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf), [[Uustalu-Monads1.pdf:file]]&rbrack;

  {#Uustalu21Lecture2} *Monads and Interaction Lecture 2* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs2.pdf), [[Uustalu-Monads2.pdf:file]]&rbrack;

  {#Uustalu21Lecture3} *Monads and Interaction Lecture 3* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs3.pdf), [[Uustalu-Monads3.pdf:file]]&rbrack;

  {#Uustalu21Lecture4} *Monads and Interaction Lecture 4* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs4.pdf), [[Uustalu-Monads4.pdf:file]]&rbrack;

* Christina Kohl, Christina Schwaiger, *Monads in Computer Science* (2021) &lbrack;[pdf](https://www.uibk.ac.at/mathematik/algebra/staff/fritz-tobias/ct2021_course_projects/category_theory.pdf), [[KohlSchwaiger-Monads.pdf:file]]&rbrack;

See also:

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Monad_(functional_programming)">Monad (functional programming)</a>_

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Side_effect_(computer_science)">Side_effect_(computer_science)</a>*

The specification of [[monads]] in [[Haskell]] is at:

* [The Haskell programming language](http://www.haskell.org/haskellwiki/Haskell), 

  * *[Monad](https://wiki.haskell.org/Monad)*

  * *[Monad laws](http://www.haskell.org/haskellwiki/Monad_laws)*

and an exposition of [[category theory]] and monads in terms of Haskell is in 

* WikiBooks, _[Haskell/Category](http://en.wikibooks.org/wiki/Haskell/Category_theory)_

Further on the issue of the CS-style monads really being [[strong monads]]:

* {#GLLN08} [[Jean Goubault-Larrecq]], [[Slawomir Lasota]], [[David Nowak]], *Logical Relations for Monadic Types*, Mathematical Structures in Computer Science, **18** 6 (2008) 1169-1217 &lbrack;[arXiv:cs/0511006](https://arxiv.org/abs/cs/0511006), [doi:10.1017/S0960129508007172](https://doi.org/10.1017/S0960129508007172)&rbrack;

* {#McDermottUustalu22} [[Dylan McDermott]], [[Tarmo Uustalu]], *What Makes a Strong Monad?*, EPTCS **360** (2022) 113-133 &lbrack;[arXiv:2207.00851](https://arxiv.org/abs/2207.00851), [doi:10.4204/EPTCS.360.6](https://doi.org/10.4204/EPTCS.360.6)&rbrack;

A comparison of monads with [[applicative functors]] (also known as idioms)
and with [[arrows (in computer science)]] is in 

* Exequiel Rivas, _Relating Idioms, Arrows and Monads from Monoidal Adjunctions_, ([arXiv:1807.04084](https://arxiv.org/abs/1807.04084))




### In quantum computation


Discussion of aspects of [[quantum computing]] in terms of monads:

* J. K. Vizzotto, [[Thorsten Altenkirch]], A. Sabry, *Structuring quantum effects: superoperators as arrows*, Mathematical Structures in Computer Science **16** 3 (2006)  453-468 &lbrack;[arXiv:quant-ph/0501151](https://arxiv.org/abs/quant-ph/0501151), [doi:10.1017/S0960129506005287](https://doi.org/10.1017/S0960129506005287)&rbrack;

  > ([[superoperators]] as [[arrows in computer science]])


The [[quantum IO monad]]:

* [[Thorsten Altenkirch]], [[Alexander Green]], *The quantum IO monad*, Ch. 5 of: Simon Gay, Ian Mackie (eds.): *Semantic Techniques in Quantum Computation* (2010) 173-205 &lbrack;[pdf](http://www.cs.nott.ac.uk/~txa/publ/qio-chapter.pdf), [talk slides](http://www.cs.nott.ac.uk/~txa/talks/qnet06.pdf), [doi:10.1017/CBO9781139193313.006](https://doi.org/10.1017/CBO9781139193313.006)&rbrack;

Exposition:

* [[Alexander Green]], *The Quantum IO Monad*, Nottingham  (2007) &lbrack;[pdf](http://drinkupthyzider.co.uk/asg/pdfs/bctcs07.pdf), [[Green-QIOMonad.pdf:file]] &rbrack;

Implementation in [[Haskell]]:

* [[Alexander Green]], *[hackage.haskell.org/package/QIO](https://hackage.haskell.org/package/QIO)*


Much of the text and the diagrams in the entry above follow

* [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:The Quantum Monadology|The Quantum Monadology]]* &lbrack;[arXiv:2310.15735](https://arxiv.org/abs/2310.15735)&rbrack;


[[!redirects monad (computer science)]]
[[!redirects monads (computer science)]]

[[!redirects monad (in computer science)]]
[[!redirects monads (in computer science)]]

[[!redirects monad (in programming theory)]]
[[!redirects monads (in programming theory)]]

[[!redirects monad in computer science]]
[[!redirects monads in computer science]]

[[!redirects computational effect]]
[[!redirects computational effects]]

[[!redirects monadic effect]]
[[!redirects monadic effects]]

[[!redirects monadic computational effect]]
[[!redirects monadic computational effects]]

[[!redirects comonads in computer science]]

[[!redirects comonadic context]]
[[!redirects comonadic contexts]]

[[!redirects monadic bind operation]]
[[!redirects monadic bind operations]]

[[!redirects comonadic extend operation]]
[[!redirects comonadic extend operations]]


[[!redirects do-notation]]
[[!redirects do notation]]

[[!redirects codo-notation]]
[[!redirects codo notation]]

