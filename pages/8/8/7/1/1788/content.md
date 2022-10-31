test

## Idea

In [[programming language|programming]] it frequently happens that a [[program]] (say $prog_{12}$) with *nominal* output [[data type]] $D_2$ *de facto* outputs data of some modified type $T(D)$ due to "external effects", where 
\[
  \label{MonadMapInIntroduction}
  D \;\mapsto\; T(D)
\]
is some general operation sending [[data types]] $D$ to new data types $T(D)$.

> For example, if alongside the computation of its nominal output data $d_2 \colon D_2$ the program also writes a log message $msg$, then its actual output data is the [[pair]] $(d_2, msg)$ of [[product type]] $T(D_2) \,=\, D_2 \times String$ (where $String$ is the [[free monoid]] on the given [[alphabet]]).

In such a case, given a subsequent program $prog_{23}$ accepting input data of type $D_2$ and itself possibly involved in further effects of type $T(-)$, then the *na&iuml;ve* [[composition]] of the two programs makes no sense (unless $T(D) = D$ is actually the trivial sort of effect), but their evident *intended* composition is obtained by: 

1. first adjusting $prog_{23}$ via some general prescription

   \[
     \label{BindingLawInIntroduction}
     prog \;\mapsto\; prog[-]
     \,,
   \]

   such that $prog_{23}[-]$:

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

> (Beware that we are denoting by square brackets "$prog[-]$" what in [[programming languages]] like [[Haskell]] [is denoted by](https://wiki.haskell.org/Monad#The_Monad_class) "`(-) >>= prog`" (.)

According to the intended behaviour of these programs, it remains to specify how exactly $prog_{23}[-]$ "carries $T(-)$-effects along", hence what the "bind" operation really is. 

> For instance, in the above example where $T(D_2) = D_2 \times String$, the evident way is to use the [[concatenation]]  $String \times String \xrightarrow{\; concat \;} String$ and set:

> $ prog_{23}\big[-\big]\;\coloneqq\; D_2 \times String \xrightarrow{ prog_{12} \times Id_{String} } D_3 \times String \times String \xrightarrow{ Id_{D_3} \times concat } D_3 \times String \,. $

But whatever design choice one makes for how to "carry along effects", it must be consistent in that applying the method to a [[triple]] of $T(-)$-effectful programs which are nominally composable, then their effectful composition should be unambiguously defined in that it is [[associative]], satisfying the following "law" ([[equation]]):

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

Finally, for such a notion of effectful programs to be usefully connected to "pure" programs without effects,  it ought to be the case that for any program $prog \,\colon\, D_0 \xrightarrow{\;} D_1$ that happens to have no $T(-)$-effects, we have a prescription for how to regard it as a  $T(-)$-effectful program in a trivial way. For that purpose there should be defined an operation

\[  
  \label{ReturnMapInIntroduction}
  ret_{D_1} \;\colon\; D_1 \xrightarrow{\;}  T(D_1)
\]

which does nothing but "return" data of type $D_1$, but re-regarded as effectful $T(D_1)$-data in a trivial way; so that we may construct the trivially effectful program $ret_{D_1}\big(prog_{01}(-)\big) \;\colon\; D_0 \xrightarrow{\;} T(D_1)$.

> For instance, in the above example of log-message effects this would be the operation $D \to D \times String$ which assigns the emtpty string $d \mapsto (d, \varnothing)$.

The final consistency condition then is that "carrying along trivial effects is indeed trivial", i.e. that 

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

Notice that the [[associativity]] condition (eq:AssociativityConditionInIntroduction) and the [[unitality]] condition (eq:UnitalityInIntroduction) jointly say that [[data types]] with $T(-)$-effectful programs between them, in the above sense, form a *[[category]]*. In [[category theory]] this is known as the *[[Kleisli category]]* of a *[[monad]]* $T$.

> Traditionally in [[category theory]], the [[axioms]] on [[monads]] are presented in a slightly different way, invoking a monad "product" [[natural transformation]] $T \circ T \xrightarrow{ \mu } T$ instead of the "binding" operation. One readily checks that these two axiomatic presentations of monads are in fact equal.

In summary, a choice of assignments

1. $D \;\mapsto\; T(D)$  $\;$---$\;$ of types of effectful data of nominal type $D$ (eq:MonadMapInIntroduction),

1. $D \;\mapsto\; ret_D$ $\;$---$\;$ regarding plain $D$-data as trivially effectful (eq:ReturnMapInIntroduction),

1. $prog \;\mapsto\; prog[-]$ $\;$---$\;$ specifying how to execute a given $prog$ while carrying along any previous $T(-)$-effects (eq:BindingLawInIntroduction)

subject to 

1. the [[associativity]] condition (eq:AssociativityConditionInIntroduction) 

1. the [[unitality]] condition (eq:UnitalityInIntroduction) 

is called a *[[monad in computer science]]* and serves to encode the notion that all programs may be subject to certain *external effects*.

> The running example above is known as the *[[writer monad]]*, since it encodes the situation where programs may have the additional effect of writing a message string into a given buffer.



(... dually for comonads ...)



