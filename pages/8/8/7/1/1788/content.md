### Basic idea: Monadic effects
 {#BasicIdea}

In [[programming language|programming]] it frequently happens that a [[program]] with "nominal" output [[data type]] $D$ *de facto* outputs data of some modified type $T(D)$ which accounts for "external effects" caused by the program, where 
\[
  \label{MonadMapInIntroduction}
  D \;\mapsto\; \mathcal{E}(D)
\]
is some general operation sending [[data types]] $D$ to new data types $\mathcal{E}(D)$.

> For example, if alongside the computation of its nominal output data $d \colon D$ a program also writes a log message $msg \,\colon\,$ [[String (computer science)|String]], then its actual output data is the [[pair]] $(d, msg)$ of [[product type]] $\mathcal{E}(D) \,\coloneqq\, D \times String$.

> Or, dually, if the program may fail and instead "throw an [[exception]] message" $msg \,\colon\,$ [[String (computer science)|String]], then its actual output data is *either* $d \colon D$ *or* $msg \colon String$, hence is of [[coproduct type]] $\mathcal{E}(D) \,\coloneqq\, D \sqcup String$.

Given such an $\mathcal{E}$-effectful program $prog_{12} \;\colon\; D_1 \to \mathcal{E}(D_2)$ and given a subsequent program $prog_{23} \,\colon\, D_2 \to \mathcal{E}(D_3)$ accepting nominal input data of type $D_2$ and itself possibly involved in further effects of type $\mathcal{E}(-)$, then the *naïve* [[composition]] of the two programs makes no sense (unless $\mathcal{E}(D) = D$ is actually the trivial sort of effect), but their evident *intended* composition is, clearly, obtained by: 

1. first adjusting $prog_{23}$ via a given prescription

   \[
     \label{BindingLawInIntroduction}
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

[[KleisliCompositionOfEffectfulPrograms-221105.jpg:file]]

> (Beware that we are denoting by square brackets "$prog[-]$" what in [[programming languages]] like [[Haskell]] [is denoted by](https://wiki.haskell.org/Monad#The_Monad_class) "`(-) >>= prog`"  aka "fish notation", eg. [Milewski (2019)](#Milewski19), and which other authors denote by "$\,(-)^\ast\,$", e.g.  [Moggi (1991)](#Moggi91); [Uustalu (2021), lecture 1](#Uustalu21Lecture1), [p. 12](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf#page=12).)

Depending on the intended behaviour of these programs, it remains to specify how exactly $prog_{23}[-]$ "carries $T(-)$-effects along", hence what the "bind" operation (eq:BindingLawInIntroduction) does concretely. 

> For instance, in the above example of a logging-effect, where $\mathcal{E}(D_2) \,\coloneqq\, D_2 \times String$, the evident way is to use the [[concatenation]]  $String \times String \xrightarrow{\; concat \;} String$ and set:

> $ prog_{23}\big[-\big]\;\coloneqq\; D_2 \times String \xrightarrow{ prog_{23} \times Id_{String} } D_3 \times String \times String \xrightarrow{ Id_{D_3} \times concat } D_3 \times String \,. $

> In the other example above, where the effect is the possible throwing of an exception message, the evident way to carry this kind of effect along is to use the [[codiagonal]] $\nabla \,\colon\, String \sqcup String \to String$, which amounts to keep forwarding the exception that has already been thrown, if any:

> $prog_{23}big[-\big] \;\coloneqq\; D_2 \sqcup String \xrightarrow{ prog_{23} \sqcup Id_{String} } D_3 \sqcup String \sqcup String \xrightarrow{ id_{D_3} \sqcup \nabla } D_3 \sqcup String \,.$

Whatever design choice one makes for how to "carry along effects", it must be consistent in that applying the method to a [[triple]] of $\mathcal{E}$-effectful programs which are nominally composable, then their effectful composition should be unambiguously defined in that it is [[associative]], satisfying the following [[equation]] -- here called the the first "monad law":

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

Finally, for such a notion of effectful programs to be usefully connected to "pure" programs without effects,  it ought to be the case that for any program $prog_{01} \,\colon\, D_0 \xrightarrow{\;} D_1$ that happens to have no $\mathcal{E}$-effects, we have a prescription for how to regard it as an $\mathcal{E}$-effectful program in a trivial way. For that purpose there should be defined an operation

\[  
  \label{ReturnMapInIntroduction}
  ret_{D} \;\colon\; D \xrightarrow{\;} \mathcal{E}(D)
\]

which does nothing but "return" data of type $D$, but re-regarded as effectful $\mathcal{E}(D)$-data in a trivial way; so that we may construct the trivially effectful program $ret_{D_1}\big(prog_{01}(-)\big) \;\colon\; D_0 \xrightarrow{\;} \mathcal{E}(D_1)$.

> For instance, in the above example of log-message effects this would be the operation $D \to D \times String$ which assigns the [[empty set|emtpty]] [[string (computer science)|string]] $d \mapsto (d, \varnothing)$.

