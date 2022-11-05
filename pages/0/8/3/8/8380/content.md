
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

In [[computer science]], a *([[comonad|co-]])[[monad]]* (or *([[co-Kleisli category|co-]])[[Kleisli triple]]*, or *(co-)[[extension system]]*) is a kind of [[data type]]-structure which describes "notions of computations" &lbrack;[Moggi (1991)](#Moggi91)&rbrack; that may "have external effects or be subject to external contexts/causes" --- such as involving [[random access memory]], [[IO-monad|input/output]], [[exception monad|exception handling]], [[writer monad|writing to]] or [[reader monad|reading from]] global variables,  etc. --- as familiar from [[imperative programming]] but cast as "pure functions" with deterministic and [[verified programming|verifiable behaviour]], in the style of [[functional programming]].

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

   1. "acts as $prog_{23}$ while *carrying* any previous $\mathcal{E}$-effects along";

1. then forming the naive [[composition]] $bind^{\mathcal{E}} prog_{23} \;\circ\;  prog_{12}$

as follows:

\begin{imagefromfile}
    "file_name": "KleisliCompositionOfEffectfulPrograms-221105.jpg",
    "width": "700",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


> (Beware that we are denoting by "$bind^{\mathcal{E}} prog (-)$" what in [[programming languages]] like [[Haskell]] [is denoted by](https://wiki.haskell.org/Monad#The_Monad_class) "`(-) >>= prog`"  aka "fish notation", eg. [Milewski (2019)](#Milewski19), and which some authors denote by "$prog^\ast\,$", e.g.  [Moggi (1991)](#Moggi91); [Uustalu (2021), lecture 1](#Uustalu21Lecture1), [p. 12](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf#page=12).)

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

> For instance, in the above example of log-message effects this would be the operation $D \to D \times String$ which assigns the [[empty set|emtpty]] [[string (computer science)|string]] $ret^{Write} \;\colon\; d \mapsto (d, \varnothing)$.

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

Notice that the [[associativity]] condition (eq:AssociativityConditionInIntroduction) and the [[unitality]] condition (eq:UnitalityInIntroduction) are jointly equivalent to saying that [[data types]] with [[hom-sets]] of $\mathcal{E}$-effectful programs between them, in the above sense, form a *[[category]]*. In [[category theory]] this is known as the *[[Kleisli category]]* of a *[[monad]]* $\mathcal{E}$.

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


### Refined idea: Internal monads
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

In general (except in the [[base topos]] of [[Sets]]), such an iterated [[function type]]/[[internal hom]] is richer than (certainly different from) the corresponding plain [[hom set]], and accordingly a "Kleisli triple" defined as above but with the binding operation typed in this [[internalization|internal]] way is *more* information than a plain [[monad]] on the underlying category of types: namely what is called a *[[strong monad]]* (eg. [McDermott & Uustalu (2022)](#McDermottUustalu22)).

On such a [[strong monad]], the bind operation is defined as the following composite:

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

This makes the monads be [[enriched monads]] in the self-[[enriched category|enrichment]] of the category of types given by the [[function type]]/[[internal hom]]. 

In particular, monads as used in [[Haskell]] are really strong/enriched monads, in this way.

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

Given a [[pair]] of such $\mathcal{E}$-[[modal types]] $\big(D_1, hndl^{\mathcal{E}}_{D_1} \big)$, $\big(D_2, hndl^{\mathcal{E}}_{D_2} \big)$, a function $\phi \,\colon\, D_1 \to D_2$ is a *[[homomorphism]]* between them if for all functions $f \,\colon\, D_0 \to D_1$ the following [[commuting diagram|diagram commutes]]:


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





### Dual idea: Comonadic contexts
 {#DualIdeaComonadicCauses}

(...)

By [[formal duality]]:

* On the one hand:

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

* Dually:

  * A [[co-Kleisli map]] for a [[comonad]] $\mathcal{C}$ is a program 

    $$
      prog \;\colon\; \mathcal{C}(D) \to D'
    $$

    *subject to* an external $\mathcal{C}$-context (a $\mathcal{C}$-cause).

  * A co-Kleisli co-module for a comonad $\mathcal{C}$ is a program 

    $$
      caus^{\mathcal{C}}_D id_D \;\colon\; D \to \mathcal{C}(D)
    $$

    *causing* such $\mathcal{C}$-contexts.


(...)


## Examples
 {#Examples}


### Definable monads

Various monads are _definable_ in terms of standard [[type formation|type-forming operations]] (such as [[product types]], [[function types]], etc.). These include the following.

* The *[[maybe monad]]* encodes possible controlled failure of a program to execute.

* An *[[exception monad]]*, more generally, encodes possible controlled failure together with the output of an error "message" in the general form of data of some type.

* The *[[reader monad]]* and *[[coreader comonad]]* both encode reading out a global parameter.


* The *[[state monad]]* encodes the possibility of *consecutive reading and re-setting* a global parameter  -- this provides a notion of *[[random access memory]]*.

* The *[[costate comonad]]* encodes a way (a "[[lens in computer science|lens]]") to read and write fields in [[databases]].

* The *[[writer monad]]* encodes writing *consecutively* into a global resource, such as for a [[stream]].

* The *[[continuation monad]]* encodes [[continuation-passing style]] of program execution.



#### State monad and Random access memory

A [[functional program]] with input of [[type]] $X$, output of [[type]] $Y$ and mutable state $S$ is a [[function]] ([[morphism]]) of [[type]] $X \times S \longrightarrow Y \times S$. Under the ([[Cartesian product]] $\dashv$ [[internal hom]])-[[adjunction]] this is equivalently given by its [[adjunct]], which is a function of type $X \longrightarrow [S, S \times Y ]$. Here the operation $[S, S\times (-)]$ is the [[monad]] induced by the above adjunction and this latter function is naturally regarded as a morphism in the [[Kleisli category]] of this monad. This monad $[S, S\times (-)]$ is called the _[[state monad]]_ for mutable states of type S.


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

* Equipping [[homotopy type theory]] (say implemented as a programming language concretely in [[Coq]] or [[Agda]]) with two axiomatic [[idempotent monads]], denoted $\sharp$ and $\Pi$, with some additional data and relations, turns it into _[[cohesive homotopy type theory]]_. See also _[[modal type theory]]_.


## Related concepts

* [[extension system]]

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

* {#MarmolejoWood10} [[F. Marmolejo]], [[Richard J. Wood]], *Monads as extension systems -- no iteration is necessary* [[TAC]] **24** 4 (2010) 84-113 &lbrack;[24-04](http://www.tac.mta.ca/tac/volumes/24/4/24-04abs.html)&rbrack;

but not related there to computation.

The original observation of monads as "notions of computation" is:

* {#Moggi91} [[Eugenio Moggi]], *Notions of computation and monads*, Information and Computation, **93** 1 (1991) &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90052-4">doi:10.1016/0890-5401(91)90052-4</a>, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf)&rbrack;

On the impact of [Moggi (1991)](#Moggi91):

* {#HylandPower07} [[Martin Hyland]], [[John Power]], _The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads_, Electronic Notes in Theoretical Computer Science (ENTCS) archive Volume 172, April, 2007 Pages 437-458  ([pdf](https://www.dpmms.cam.ac.uk/~martin/Research/Publications/2007/hp07.pdf))

In the generality of [[relative monads]]:

* [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], Section 2 of: *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;

Textbook accounts of monads as used in actual [[programming languages]] such as [[Haskell]]:

* {#Milewski19} [[Bartosz Milewski]] (compiled by Igal Tabachnik), "Monads: Programmer's Definition", §20 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;

Further discussion/exposition of the notion and application of (co)monads in computer science:
 
* [[Philip Wadler]], _Comprehending Monads_, in _Conference on Lisp and functional programming_, ACM Press, 1990 ([[WadlerMonads.pdf:file]])

* {#BrookesGeva91} [[Stephen Brookes]], Shai Geva, *Computational Comonads and Intensional Semantics*, CMU-CS-91-190 (1991) &lbrack;[[BrookersGeva-ComputationalComonads.pdf:file]]&rbrack;

* [[Philip Wadler]], *Monads for functional programming*, in M. Broy (eds.) *Program Design Calculi* NATO ASI Series, **118** Springer (1992) &lbrack;[doi;10.1007/978-3-662-02880-3_8](https://doi.org/10.1007/978-3-662-02880-3_8), [pdf](https://homepages.inf.ed.ac.uk/wadler/papers/marktoberdorf/baastad.pdf)&rbrack;

* Philip Mulry, _Monads in semantics_ , ENTCS **14** (1998) pp.275-286.

* John Hughes, section 2 of _Generalising Monads to Arrows_, Science of Computer Programming (Elsevier) 37 (1-3): 67&#8211;111. (2000) ([pdf](http://pdn.sciencedirect.com/science?_ob=MiamiImageURL&_cid=271600&_user=10&_pii=S0167642399000234&_check=y&_origin=search&_zone=rslt_list_item&_coverDate=2000-05-31&wchp=dGLzVlk-zSkWb&md5=fa91ab4ffc136b0cedc52318c7c249be&pid=1-s2.0-S0167642399000234-main.pdf))

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

On the issue of the CS-style monads really being [[strong monads]]:

* {#McDermottUustalu22} [[Dylan McDermott]], [[Tarmo Uustalu]], *What Makes a Strong Monad?*, EPTCS **360** (2022) 113-133 &lbrack;[arXiv:2207.00851](https://arxiv.org/abs/2207.00851), [doi:10.4204/EPTCS.360.6](https://doi.org/10.4204/EPTCS.360.6)&rbrack;

A comparison of monads with [[applicative functors]] (also known as idioms)
and with [[arrows (in computer science)]] is in 

* Exequiel Rivas, _Relating Idioms, Arrows and Monads from Monoidal Adjunctions_, ([arXiv:1807.04084](https://arxiv.org/abs/1807.04084))


Discussion of [[comonads]] in this context includes


* {#Overton14} David Overton, _Comonads in Haskell_, 2014 ([web](https://speakerdeck.com/dmoverton/comonads-in-haskell))

### In quantum computation


Discussion of aspects of [[quantum computing]] in terms of monads:

* [[Thorsten Altenkirch]], Alexander Green, _The quantum IO monad_, in _Semantic Techniques in Quantum Computation_, January 2009, appeared in 2010 ([pdf](http://www.cs.nott.ac.uk/~txa/publ/qio-chapter.pdf), [talk slides](http://www.cs.nott.ac.uk/~txa/talks/qnet06.pdf))

* J. K. Vizzotto, [[Thorsten Altenkirch]], A. Sabry, _Structuring quantum effects: superoperators as arrows_ ([arXiv:quant-ph/0501151](http://arxiv.org/abs/quant-ph/0501151))



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

