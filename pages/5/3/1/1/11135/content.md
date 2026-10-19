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


\tableofcontents

## Idea

In a [[category]] with [[internal homs]] $[-,-]$, given an [[object]] $S$, the _continuation monad_ is the [[endofunctor]] $X \mapsto \big[ [X, S], S\big]$, together with the [[unit of a monad|unit]]
\[
  \begin{array}{ccl}
    X 
    &\overset{\eta}{\longrightarrow}&
    \big[ [X,S],S \big]
    \\
    x &\mapsto& \lambda\big(k:[X,S]\big).\, k(x)
  \end{array}
\]
and multiplication
\[
  \begin{array}{ccl}
    \big[ \big[ [ [X,S],S ],S \big],S \big] 
    &\overset{\mu}{\longrightarrow}&
    \big[ [X,S],S\big]
    \\
    M &\mapsto& 
    \lambda\big(k:[X,S]\big).\, 
      M\Big(\lambda\big(c: [ [X,S],S]\big). c(k)\Big)
    \mathrlap{\,.}
  \end{array}
\]

In general [[mathematics]] this [[monad]] is ubiquitous as modelling _double dualization_ (cf. Ex. \ref{DoublePowerset}, Ex. \ref{DoubleDualVectorSpaces} and Rem. \ref{StoneCechCompactification} below).

In [[computer science]] this [[monad (in computer science)|monad]] is used to model [[continuation-passing style]] of programming, and therefore this is also called the _continuation monad_. The idea here is that a [[morphism]] $f \colon X \to Y$ in the [[Kleisli category]] of the continuation monad, hence a morphism in the original category of the form $X\longrightarrow [ [Y,S],S]$, is much like a map from $X$ to $Y$ only that instead of "returning" its output directly it instead feeds it into a given function $Y \to S$ which hence _continues_ the computation.


## Definition

### Setting and notation

\begin{remark}\label{SettingAndNotation}
**(setting)**
Throughout, $(\mathcal{C}, \otimes, \mathbb{1})$ denotes a [[symmetric monoidal category|symmetric]] [[closed monoidal category]], with
[[internal hom]] $[-,-] \colon \mathcal{C}^{op} \times \mathcal{C} \to \mathcal{C}$,
[[evaluation map]] $\mathrm{ev}_{A,B} \colon [A,B] \otimes A \to B$,
and [[braiding|symmetry]] $\sigma_{A,B} \colon A \otimes B \overset{\sim}{\longrightarrow} B \otimes A$.
The main example is a [[cartesian closed category]] such as [[Set]], where $\otimes = \times$.

We fix an object
$$
  S \,\in\, \mathcal{C}
$$
and refer to it as the _answer object_ (or _answer type_, or _result type_, in [[computer science]]). Morphisms $k \colon X \to S$, hence (generalized) elements $k : [X,S]$, are called _continuations_ for $X$.
\end{remark}

\begin{remark}\label{LambdaNotation}
**($\lambda$-notation)**
We denote morphisms by terms of the [[simply typed lambda calculus]] (in the cartesian case) or of the [[linear type theory|linear $\lambda$-calculus]] (in the general symmetric monoidal case), interpreted in $\mathcal{C}$ as its [[internal language]]:

* a [[term]] $t$ of [[type]] $B$ in a [[context]] of [[variables]] $x_1 \colon X_1, \cdots, x_n \colon X_n$ denotes a [[morphism]] $X_1 \otimes \cdots \otimes X_n \to B$;

* [[application]] $k(x)$, for $k \colon [X,S]$ and $x : X$, denotes the [[evaluation map]], $\mathrm{ev}(k \otimes x)$;

* abstraction $\lambda (x : X).\, t$ denotes the [[adjunct]] ("[[currying]]") of the morphism denoted by $t$;

* for terms $a : A$ and $x : X$ in disjoint contexts, $a \otimes x$ denotes their [[tensor product]], a term of type $A \otimes X$; and a morphism out of a tensor product $A \otimes X$ is specified by a term $t$ in context $a : A,\, x : X$, written as $a \otimes x \,\mapsto\, t$. (In the cartesian case, $a \otimes x$ is just the pair $(a,x)$.)

By the [[universal property]] of the [[internal hom]], these terms satisfy [[beta reduction|$\beta$-reduction]] $(\lambda x.\, t)(a) = t[a/x]$ and [[eta reduction|$\eta$-reduction]] $\lambda x.\, k(x) = k$.

In the cartesian case this is equivalently the usual notation in terms of [[generalized elements]]. In the general symmetric monoidal case it is legitimate here because all terms below use each [[variable]] --- whether [[bound variable|bound]] or [[free variable|free]] in the context --- exactly once (Rem. \ref{Linearity}).

We also write $k \circ f \,:=\, \lambda x.\, k\big(f(x)\big)$.
\end{remark}


### The dualization adjunction

\begin{proposition}\label{DualizationSelfAdjunction}
**(dualization is self-adjoint on the right)**
The [[functor]] of dualization into $S$,
$$
  [-,S]
    \;\colon\;
  \mathcal{C}^{op} \longrightarrow \mathcal{C}
  \,,
  \;\;\;\;\;\;\;
  \big(
    X \overset{f}{\longrightarrow} Y
  \big)
  \;\;\mapsto\;\;
  \Big(
    [Y,S]
      \overset{[f,S]}{\longrightarrow}
    [X,S]
    \,,
    \;\;
    k \mapsto k \circ f
  \Big)
  \,,
$$
is [[right adjoint]] to its own [[opposite functor]]:
$$
  \mathcal{C}^{op}
  \underoverset
    {\underset{[-,S]}{\longrightarrow}}
    {\overset{[-,S]^{op}}{\longleftarrow}}
    {\bot}
  \mathcal{C}
  \,.
$$
The [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) of this [[adjoint functors|adjunction]] is the [[composition|composite]] of [[natural isomorphisms]]
$$
  \mathcal{C}^{op}\big([X,S],\, A\big)
  \;=\;
  \mathcal{C}\big(A,\, [X,S]\big)
  \;\simeq\;
  \mathcal{C}\big(A \otimes X,\, S\big)
  \underset{
    \mathcal{C}(\sigma_{X,A},\, S)
  }{\simeq}
  \mathcal{C}\big(X \otimes A,\, S\big)
  \;\simeq\;
  \mathcal{C}\big(X,\, [A,S]\big)
  \,,
$$
which in $\lambda$-notation (Rem. \ref{LambdaNotation}) is "swapping the arguments":
$$
  \Big(
    A \overset{\phi}{\longrightarrow} [X,S]
  \Big)
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \Big(
    X \overset{\widetilde{\phi}}{\longrightarrow} [A,S]
  \Big)
  \,,
  \;\;\;\;\;\;
  \widetilde{\phi}
  \;:=\;
  \lambda (x : X).\,
  \lambda (a : A).\,
  \phi(a)(x)
  \,.
$$
This [[bijection]] is its own inverse: $\widetilde{\widetilde{\phi}} = \phi$.
\end{proposition}

\begin{proof}
Each of the displayed [[bijections]] is [[natural bijection|natural]] in $X \in \mathcal{C}$ and in $A \in \mathcal{C}^{op}$; the outer two by the definition of the [[internal hom]], and the middle one by naturality of the symmetry. That the [[composition|composite]] is an [[involution]] follows from $\sigma_{A,X} \circ \sigma_{X,A} = \mathrm{id}$, or directly from the $\lambda$-formula.
\end{proof}

\begin{remark}\label{UnitAndCounit}
**(unit and counit)**
The [[adjunction unit]] of Prop. \ref{DualizationSelfAdjunction} at $X \in \mathcal{C}$ is the image of $\mathrm{id}_{[X,S]}$ under the hom-isomorphism, which is the canonical map into the double dual:
$$
  \eta_X
    \;\colon\;
  X \longrightarrow [ [X,S],S]
  \,,
  \;\;\;\;\;\;\;
  \eta_X
    \;:=\;
  \lambda (x : X).\,
  \lambda (k : [X,S]).\,
  k(x)
  \,,
$$
namely the [[adjunct]] of
$X \otimes [X,S] \overset{\sigma}{\longrightarrow} [X,S] \otimes X \overset{\mathrm{ev}}{\longrightarrow} S$.

Since the hom-isomorphism is its own inverse, the [[adjunction counit]] at $A \in \mathcal{C}^{op}$ is, regarded as a morphism in $\mathcal{C}$, the same kind of map, namely $\eta_A \colon A \to [ [A,S],S]$. Accordingly, both [[triangle identities]] of the adjunction reduce to one and the same identity in $\mathcal{C}$, saying that the single dual is a [[retract]] of the triple dual:
$$
  [\eta_A, S] \circ \eta_{[A,S]}
  \;=\;
  \mathrm{id}_{[A,S]}
  \;\;\;\;\;\;
  \text{for all}\; A \in \mathcal{C}
  \,.
$$
In $\lambda$-notation:
$$
  k
  \;\;\mapsto\;\;
  \lambda (c : [ [A,S],S]).\, c(k)
  \;\;\mapsto\;\;
  \lambda (a : A).\,
  \big(\lambda c.\, c(k)\big)\big(\eta_A(a)\big)
  \;=\;
  \lambda a.\, \eta_A(a)(k)
  \;=\;
  \lambda a.\, k(a)
  \;=\;
  k
  \,.
$$
\end{remark}


### The continuation monad

\begin{definition}\label{TheContinuationMonad}
**(continuation monad)**
The _continuation monad_ (or _double dualization monad_) on $\mathcal{C}$ with answer object $S$ is the [[monad]] $(D, \eta, \mu)$ induced by the [[adjunction]] of Prop. \ref{DualizationSelfAdjunction}, hence with
$$
  D
    \;:=\;
  [-,S] \circ [-,S]^{op}
    \;\colon\;
  \mathcal{C} \longrightarrow \mathcal{C}
  \,,
  \;\;\;\;\;\;\;
  \eta \;:=\; \text{adjunction unit}
  \,,
  \;\;\;\;\;\;\;
  \mu \;:=\; [-,S] \, \epsilon \, [-,S]^{op}
  \,.
$$
Explicitly, the components are as follows:

**The underlying [[endofunctor]]** is
$$
  D(X) \;=\; [ [X,S],S]
  \,,
  \;\;\;\;\;\;\;
  D(f) \;=\; [ [f,S],S]
  \,,
$$
hence for $f \colon X \to Y$:
$$
  D(f)
    \;\colon\;
  [ [X,S],S] \longrightarrow [ [Y,S],S]
  \,,
  \;\;\;\;\;\;\;
  \phi
    \;\mapsto\;
  \lambda (k : [Y,S]).\, \phi(k \circ f)
  \,.
$$

**The unit** is the canonical map into the double dual (Rem. \ref{UnitAndCounit}):
$$
  \eta_X
    \;\colon\;
  X \longrightarrow [ [X,S],S]
  \,,
  \;\;\;\;\;\;\;
  x
    \;\mapsto\;
  \lambda (k : [X,S]).\, k(x)
  \,.
$$

**The multiplication** is the dual of the unit at $[X,S]$:
$$
  \mu_X
    \;:=\;
  [\eta_{[X,S]},\, S]
    \;\colon\;
  [ [ [ [X,S],S],S],S]
    \longrightarrow
  [ [X,S],S]
  \,,
$$
hence it is given by precomposition with $\eta_{[X,S]}$,
$$
  \mu_X(M)
    \;=\;
  M \circ \eta_{[X,S]}
  \,,
$$
which in $\lambda$-notation reads:
$$
  \mu_X(M)
  \;=\;
  \lambda (k : [X,S]).\,
  M\Big(
    \lambda (c : [ [X,S],S]).\, c(k)
  \Big)
  \,.
$$
\end{definition}

\begin{remark}\label{UnwindingTheMultiplication}
**(unwinding the multiplication)**
In the $\lambda$-term for $\mu_X$ in Def. \ref{TheContinuationMonad} the subterms have the following types:
$$
  \array{
    \arrayopts{\colalign{right center left}}
    k
      &:&
    [X,S]
    \\
    c
      &:&
    [ [X,S],S]
    \\
    c(k)
      &:&
    S
    \\
    \lambda c.\, c(k)
      \;=\;
    \eta_{[X,S]}(k)
      &:&
    [ [ [X,S],S],S]
    \\
    M
      &:&
    [ [ [ [X,S],S],S],S]
    \\
    M\big(\lambda c.\, c(k)\big)
      &:&
    S
    \\
    \lambda k.\, M\big(\lambda c.\, c(k)\big)
      &:&
    [ [X,S],S]
  }
$$
In words: $\mu_X(M)$ is the functional on continuations which, given a continuation $k \colon X \to S$, evaluates $M$ on the "evaluation at $k$"-functional
$$
  \eta_{[X,S]}(k)
    \;=\;
  \lambda \big(c : [ [X,S],S]\big).\, c(k)
  \,,
$$
hence:
$$
  \mu_X(M)(k) \;=\; M\big(\eta_{[X,S]}(k)\big)
  \mathrlap{\,.}
$$
\end{remark}

\begin{proposition}\label{MonadLaws}
**(monad laws)**
The data in Def. \ref{TheContinuationMonad} satisfies the [[monad]] axioms.
\end{proposition}

\begin{proof}
Abstractly, this is a special case of the general fact that every [[adjunction]] $L \dashv R$ induces a monad $(R L, \eta, R \epsilon L)$.

Concretely, in terms of the one triangle identity from Rem. \ref{UnitAndCounit}, of the contravariant functoriality $[g,S] \circ [h,S] = [h \circ g, S]$ and of [[natural transformation|naturality]] of $\eta$:

*Left unit law.* By the triangle identity for $A = [X,S]$:
$$
  \mu_X \circ \eta_{D X}
    \;=\;
  [\eta_{[X,S]}, S] \circ \eta_{[ [X,S],S]}
    \;=\;
  \mathrm{id}_{D X}
  \,.
$$

*Right unit law.* By the triangle identity for $A = X$:
$$
  \mu_X \circ D(\eta_X)
    \;=\;
  [\eta_{[X,S]},S] \circ \big[ [\eta_X, S], S\big]
    \;=\;
  \Big[ [\eta_X,S] \circ \eta_{[X,S]},\, S\Big]
    \;=\;
  [\mathrm{id}_{[X,S]}, S]
    \;=\;
  \mathrm{id}_{D X}
  \,.
$$

*Associativity.* We have
$$
  \mu_X \circ \mu_{D X}
    \;=\;
  \big[
    \eta_{[D X,S]} \circ \eta_{[X,S]}
    ,\,
    S
  \big]
  \;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;
  \mu_X \circ D(\mu_X)
    \;=\;
  \big[
    [\mu_X, S] \circ \eta_{[X,S]}
    ,\,
    S
  \big]
  \,,
$$
and these agree: since $[\mu_X,S] = \big[ [\eta_{[X,S]},S],S\big] = D(\eta_{[X,S]})$, the equation $\eta_{[D X,S]} \circ \eta_{[X,S]} = D(\eta_{[X,S]}) \circ \eta_{[X,S]}$ is the naturality square of $\eta$ on the morphism $\eta_{[X,S]} \colon [X,S] \to [D X, S]$.

Alternatively, in $\lambda$-notation, using only $\beta$- and $\eta$-reduction (for associativity, both sides reduce to the same term):
$$
  \array{
    \arrayopts{\colalign{right center left}}
    \mu_X\big(\eta_{D X}(\phi)\big)
      &=&
    \lambda k.\, \big(\lambda c.\, c(k)\big)(\phi)
    \;=\;
    \lambda k.\, \phi(k)
    \;=\;
    \phi
    \\
    \mu_X\big(D(\eta_X)(\phi)\big)
      &=&
    \lambda k.\, \phi\big(\lambda x.\, \eta_X(x)(k)\big)
    \;=\;
    \lambda k.\, \phi\big(\lambda x.\, k(x)\big)
    \;=\;
    \phi
    \\
    \mu_X\big(\mu_{D X}(\mathcal{M})\big)
      &=&
    \lambda k.\, \mathcal{M}\Big(\lambda C.\, C\big(\lambda c.\, c(k)\big)\Big)
    \\
    \mu_X\big(D(\mu_X)(\mathcal{M})\big)
      &=&
    \lambda k.\, \mathcal{M}\big(\lambda C.\, \mu_X(C)(k)\big)
    \;=\;
    \lambda k.\, \mathcal{M}\Big(\lambda C.\, C\big(\lambda c.\, c(k)\big)\Big)
    \mathrlap{\,.}
  }
$$
This completes the argument.
\end{proof}

\begin{remark}\label{Linearity}
**(linearity and the role of the symmetry)**
In each of the $\lambda$-terms on this page every variable, whether bound or free in the context, occurs exactly once. Therefore these terms make sense in the [[linear type theory|internal linear type theory]] of any symmetric closed monoidal category: they use neither [[diagonal|duplication]] nor [[projection|deletion]] of variables, which is why the definition does not require $\mathcal{C}$ to be [[cartesian monoidal category|cartesian]] (see [Melliès & Tabareau 2007](#MelliesTabareau07)).

On the other hand, the symmetry $\sigma$ is used, if implicitly: it is the exchange rule which allows to form $k(x)$ in the context $x : X,\, k : [X,S]$, as in the definition of $\eta_X$. In a non-symmetric [[biclosed monoidal category]], writing $[X,-]_r$ for the [[right adjoint]] of $(-) \otimes X$ and $[X,-]_l$ for that of $X \otimes (-)$, the hom-isomorphism of Prop. \ref{DualizationSelfAdjunction} is instead
$$
  \mathcal{C}\big(A,\, [X,S]_r\big)
  \;\simeq\;
  \mathcal{C}\big(A \otimes X,\, S\big)
  \;\simeq\;
  \mathcal{C}\big(X,\, [A,S]_l\big)
  \,,
$$
so that one has to alternate between the two one-sided internal homs: $X \mapsto \big[ [X,S]_r, S\big]_l$.
\end{remark}


### Equivalent formulations

\begin{proposition}\label{KleisliExtension}
**(Kleisli triple / bind form)**
In terms of [[extension system|Kleisli extension]], the continuation monad (Def. \ref{TheContinuationMonad}) is given by the unit $\eta$ together with the operation which sends a Kleisli morphism $f \colon X \to [ [Y,S],S]$ to
$$
  f^\ast
    \;:=\;
  \mu_Y \circ D(f)
    \;\colon\;
  [ [X,S],S] \longrightarrow [ [Y,S],S]
  \,,
  \;\;\;\;\;\;\;
  \phi
    \;\mapsto\;
  \lambda (k : [Y,S]).\,
  \phi\big(
    \lambda (x : X).\, f(x)(k)
  \big)
  \,.
$$
Conversely, the multiplication and the functor are recovered as
$$
  \mu_X \;=\; \big(\mathrm{id}_{D X}\big)^\ast
  \,,
  \;\;\;\;\;\;\;
  D(f) \;=\; \big(\eta_Y \circ f\big)^\ast
  \,,
$$
and the composite of Kleisli morphisms $f \colon X \to D Y$ and $g \colon Y \to D Z$ is
$$
  g^\ast \circ f
  \;=\;
  \lambda (x : X).\,
  \lambda (k : [Z,S]).\,
  f(x)\big(
    \lambda (y : Y).\, g(y)(k)
  \big)
  \,.
$$
This is the form in which the continuation monad appears in [Moggi (1991), Ex. 1.1](#Moggi91). In [[Haskell]]-notation (ignoring that the standard libraries define `Cont r` as `ContT r Identity`, with `ContT` a `newtype`):

    type Cont r a = (a -> r) -> r

    return x  = \k -> k x               -- unit
    m >>= f   = \k -> m (\x -> f x k)   -- Kleisli extension
    join mm   = \k -> mm (\m -> m k)    -- multiplication

\end{proposition}

\begin{proposition}\label{ContinuationTransformers}
**(Kleisli morphisms as continuation transformers)**
Under the hom-isomorphism of Prop. \ref{DualizationSelfAdjunction}, Kleisli morphisms $f \colon X \to [ [Y,S],S]$ correspond to morphisms
$$
  \widetilde{f}
    \;\colon\;
  [Y,S] \longrightarrow [X,S]
  \,,
  \;\;\;\;\;\;\;
  k
    \;\mapsto\;
  \lambda (x : X).\, f(x)(k)
  \,,
$$
which turn continuations of the output into continuations of the input. This correspondence is compatible with composition, in that
$$
  \widetilde{\eta_X} \;=\; \mathrm{id}_{[X,S]}
  \,,
  \;\;\;\;\;\;\;
  \widetilde{ g^\ast \circ f } \;=\; \widetilde{f} \circ \widetilde{g}
  \,.
$$
Hence the [[Kleisli category]] of the continuation monad is equivalent to the [[opposite category|opposite]] of the [[full subcategory]] of $\mathcal{C}$ on the objects of the form $[X,S]$, via $X \mapsto [X,S]$ and $f \mapsto \widetilde{f}$. (This is an instance of the general fact that the Kleisli category of the monad induced by an adjunction is equivalent to the full image of the [[left adjoint]].)

In these terms, Kleisli extension and multiplication are just dualization of continuation transformers:
$$
  f^\ast \;=\; [\widetilde{f},\, S]
  \,,
  \;\;\;\;\;\;\;
  \mu_X
    \;=\;
  \big[\widetilde{\mathrm{id}_{D X}},\, S\big]
    \;=\;
  [\eta_{[X,S]},\, S]
  \,.
$$
\end{proposition}

\begin{remark}\label{AsCodensityMonad}
**(as a codensity monad)**
The continuation monad is the ($\mathcal{C}$-[[enriched category theory|enriched]]) [[codensity monad]] of the functor $\mathbb{1} \to \mathcal{C}$ which picks the object $S$, since the [[right Kan extension]] of $S$ along itself is the [[cotensor]]
$$
  \mathrm{Ran}_S S \,(X)
  \;\simeq\;
  \big\{ [X,S],\, S \big\}
  \;=\;
  [ [X,S],S]
  \,.
$$
For $\mathcal{C} = $ [[Set]] this is the familiar $X \mapsto S^{(S^X)}$.

Codensity monads of inclusions of [[full subcategory|full subcategories]] of "small" objects are closely related: the codensity monad of [[FinSet]] $\hookrightarrow$ [[Set]] is the [[ultrafilter monad]], which is a submonad of the continuation monad on $Set$ with $S = \{0,1\}$ (Ex. \ref{DoublePowerset}); and the codensity monad of the inclusion of [[finite-dimensional vector spaces]] into all [[vector spaces]] is the continuation monad of Ex. \ref{DoubleDualVectorSpaces} itself (see [Leinster (2013)](#Leinster13)).
\end{remark}


### Strength

\begin{proposition}\label{Strength}
**(strength)**
The continuation monad is a [[strong monad]], with [[tensorial strength]]
$$
  t_{A,X}
    \;\colon\;
  A \otimes [ [X,S],S]
    \longrightarrow
  [ [A \otimes X, S], S]
  \,,
  \;\;\;\;\;\;\;
  a \otimes \phi
    \;\mapsto\;
  \lambda (k : [A \otimes X, S]).\,
  \phi\big(
    \lambda (x : X).\, k(a \otimes x)
  \big)
  \,;
$$
equivalently ([Kock (1972)](#Kock72)) it is a $\mathcal{C}$-[[enriched monad]], with action on internal homs
$$
  [X,Y] \longrightarrow \big[ D X,\, D Y \big]
  \,,
  \;\;\;\;\;\;\;
  f
    \;\mapsto\;
  \lambda (\phi : D X).\,
  \lambda (k : [Y,S]).\,
  \phi(k \circ f)
  \,.
$$
\end{proposition}

\begin{remark}\label{NonCommutativity}
**(non-commutativity)**
The continuation monad is (in general) _not_ a [[commutative monad]]: The two maps
$D X \otimes D Y \to D(X \otimes Y)$
induced by the strength and its mirror image are
$$
  \phi \otimes \psi
    \;\mapsto\;
  \lambda k.\,
  \phi\Big(\lambda x.\, \psi\big(\lambda y.\, k(x \otimes y)\big)\Big)
  \;\;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;\;
  \phi \otimes \psi
    \;\mapsto\;
  \lambda k.\,
  \psi\Big(\lambda y.\, \phi\big(\lambda x.\, k(x \otimes y)\big)\Big)
  \,,
$$
which differ in the order in which $\phi$ and $\psi$ get to act on the continuation ("evaluation order"). For example, in $\mathcal{C} = $ [[Set]] with $S = \{0,1\}$ and $X = Y = \ast$, let $\phi$ and $\psi$ be the constant functionals with value $0$ and $1$, respectively: then the first map gives the constant functional with value $0$, the second the one with value $1$.
\end{remark}


## Examples

### First examples

\begin{example}\label{DoublePowerset}
**(double powerset)**
For $\mathcal{C} = $ [[Set]] and $S = \{0,1\}$, identify maps $X \to \{0,1\}$ with [[subsets]] $A \subset X$ (via their [[characteristic functions]]). Then $D X \simeq P P X$ is the set of families $\mathcal{A}$ of subsets of $X$, and the structure maps of Def. \ref{TheContinuationMonad} become:
$$
  \array{
    \arrayopts{\colalign{right center left}}
    \eta_X(x)
      &=&
    \big\{
      A \subset X
      \,\big\vert\,
      x \in A
    \big\}
    \\
    D(f)(\mathcal{A})
      &=&
    \big\{
      B \subset Y
      \,\big\vert\,
      f^{-1}(B) \in \mathcal{A}
    \big\}
    \\
    \mu_X(\mathfrak{M})
      &=&
    \Big\{
      A \subset X
      \,\Big\vert\,
      \big\{
        \mathcal{A} \in P P X
        \,\vert\,
        A \in \mathcal{A}
      \big\}
      \in
      \mathfrak{M}
    \Big\}
    \mathrlap{\,.}
  }
$$
Elements of $P P X$ may be thought of as generalized [[quantifiers]] on $X$, for instance $\forall_X = \{X\}$ and $\exists_X = \{ A \subset X \,\vert\, A \neq \varnothing\}$, while $\eta_X(x)$ is the [[principal ultrafilter]] at $x$ ("evaluation at $x$").

Restricting to upward closed families, to [[filters]], or to [[ultrafilters]] yields submonads, the last one being the [[ultrafilter monad]], whose [[algebras over a monad|algebras]] are the [[compact Hausdorff spaces]] (see [Leinster (2013)](#Leinster13) and Rem. \ref{StoneCechCompactification} below).
\end{example}

\begin{example}\label{DoubleDualVectorSpaces}
**(double dual vector spaces)**
For $\mathcal{C} = \mathrm{Vect}_{\mathbb{K}}$ the category of [[vector spaces]] over a [[field]] $\mathbb{K}$, with $\otimes$ the [[tensor product of vector spaces]], and with $S = \mathbb{K}$ the [[ground field]], the continuation monad is
$$
  V \;\mapsto\; V^{\ast\ast}
$$
with $\eta_V \colon V \to V^{\ast\ast}$ the canonical map of a [[vector space]] into its [[dual vector space|double dual]] (which is injective by the existence of [[basis|bases]], invoking the [[axiom of choice]] for infinite-dimensional $V$), and with multiplication
$$
  \mu_V \;=\; [\eta_{V^\ast}, \mathbb{K}] \;\colon\; V^{\ast\ast\ast\ast} \longrightarrow V^{\ast\ast}
$$
the [[dual linear map]] of the canonical inclusion $\eta_{V^\ast} \colon V^\ast \hookrightarrow V^{\ast\ast\ast}$ (as in Def. \ref{TheContinuationMonad}). This is an example where $\mathcal{C}$ is not cartesian (cf. Rem. \ref{Linearity}). On [[finite-dimensional vector spaces]] the unit $\eta$ is an isomorphism.
\end{example}


### Further examples

Not quite an example is the following:

\begin{remark}\label{StoneCechCompactification}
**(Stone-Čech compactification)**

The [[Stone-Čech compactification]] functor $\beta \colon Top \to CpHaus$ is the universal way to map a [[topological space]] into a [[compact Hausdorff space]], and it is a form of double dualization into the unit [[interval]] $[0,1]$, which is a [[cogenerator]] in the [[category]] of [[compact Hausdorff spaces]] (by [[Urysohn's lemma]]): For any topological space $X$, $\beta X$ is [[homeomorphism|homeomorphic]] to the [[closure]] of the [[image]] of the map
$$
  \begin{array}{ccc}
  X &\longrightarrow& [0,1]^{C(X,[0,1])}
  \\
  x &\mapsto& \big(h \mapsto h(x)\big)
  \end{array}
$$
into the [[product topological space]] of copies of $[0,1]$ indexed by the set $C(X,[0,1])$ of [[continuous functions]] --- this map being the evident analog of the unit $\eta_X$ (Def. \ref{TheContinuationMonad}), with the internal hom replaced by the set of continuous functions.

Composing $\beta$ with the inclusion [[functor]] $\iota \colon CpHaus \hookrightarrow Top$ yields a [[monad]] $\iota \circ \beta$ on $Top$. 

Beware that this monad is _not_ an instance of the continuation monad of Def. \ref{TheContinuationMonad}:

* [[Top|$Top$]] is not [[cartesian closed category|cartesian closed]], so that $\big[ [X,[0,1] ],[0,1]\big]$ is not available as an internal hom;

* $\iota \circ \beta$ is an [[idempotent monad]] (since $CpHaus \hookrightarrow Top$ is a [[reflective subcategory]]), while continuation monads are in general not idempotent; for example on $Set$ with $S = \{0,1\}$ (Ex. \ref{DoublePowerset}) the map $\eta_{D X} \colon P P X \to P P P P X$ is not surjective, by [[Cantor's theorem]].

Rather, $\iota \circ \beta$ is the [[codensity monad]] of the inclusion $\iota$ (as for the codensity monad of any [[right adjoint]], see [Leinster (2013)](#Leinster13)), in line with Rem. \ref{AsCodensityMonad}. On [[discrete topological spaces]] $X$, $\beta X$ is the set of [[ultrafilters]] on $X$ (with its Stone topology), and the monad on $Set$ induced by the free/forgetful adjunction between $Set$ and $CpHaus$ is the [[ultrafilter monad]] of Ex. \ref{DoublePowerset}.
\end{remark}

Further examples are discussed at:

* [[double negation monad]]

* [[dualizing object in a closed category]]

* [[extensive quantity]]


## Properties
 
### Algebras

\begin{proposition}\label{MonadicityOfDualization}
**(monadicity of dualization over $Set$)**
On the [[category of sets]], the functor $[-,S] \colon\mathbf{Set}^{op}\to \mathbf{Set}$ is [[monadic]] (with left adjoint $[-, S]^{op} \colon \mathbf{Set} \to \mathbf{Set}^{op}$) whenever ${|S|}\geq 2$. 
\end{proposition} 

(cf. [Hyland, Levy, Plotkin & Power 2007 Prop. 10](#HylandLevyPlotkinPower07))

\begin{proof}
The following argument uses [[classical logic]], for instance in identifying the [[subobject classifier]] of $Set$ with the [[boolean domain]] $2$.

Since $[-,S]$ has the [[left adjoint]] $[-,S]^{op}$ (Prop. \ref{DualizationSelfAdjunction}) and $Set^{op}$ has [[reflexive coequalizers]] (these being the coreflexive [[equalizers]] in $Set$), by Beck's crude [[monadicity theorem]] it suffices to see that $[-,S]$

1. [[preserved colimit|preserves]] reflexive coequalizers, hence takes coreflexive equalizers in $Set$ to [[coequalizers]] in $Set$, 

1. reflects [[isomorphisms]].

> (The alternative argument of [Hyland, Levy, Plotkin & Power 2007, Prop. 10](#HylandLevyPlotkinPower07), shows and uses that the image under $[-,S]$ of a [[coreflexive equalizer]] is a [[split coequalizer]].)

Regarding the first point: Say that $S$ is (internally) *injective* if $[-, S]$ takes coreflexive equalizers in $Set$ to coequalizers in $Set$. (The coreflexivity cannot be dropped here: For example, the equalizer of the identity and of the swap map $\tau$ on $2 = \{0,1\}$ is $\varnothing \hookrightarrow 2$, but the coequalizer of $[\mathrm{id},2]$ and $[\tau,2]$ on the 4-element set $[2,2]$ has 3 elements, while $[\varnothing,2]$ has a single element.)

The [[subobject classifier]] $2$ is injective in this sense, by the proof of Par&eacute;&rsquo;s theorem (for constructing finite colimits in an elementary topos), which shows that the [[power object]] functor takes coreflexive equalizers to (split) coequalizers. Since $S \times (-) \colon Set \to Set$ preserves [[connected limits]] such as equalizers (and, as does any functor, coreflexive pairs), it follows that $[S \times -, 2] \cong [-, 2^S]$ takes coreflexive equalizers to coequalizers, i.e., that $2^S$ is injective, for any $S$. Finally, for $|S| \geq 2$, $S$ is a [[retract]] of $2^S$ --- via the map $s \mapsto \{s\}$ and the map which sends singletons to their element and all other subsets to a fixed element $s_0 \in S$ --- so that the functor $[-,S]$ is a retract of $[-,2^S]$; and since a retract of a coequalizer diagram is again a coequalizer diagram, also $S$ is injective.

Regarding the second point: Since $|S| \geq 2$, the set $2$ is a retract of $S$; and since $2$ is a [[cogenerator]] in $Set$, so is $S$, which means that $[-,S]$ is [[faithful functor|faithful]]. But faithful functors reflect [[monomorphisms]] and [[epimorphisms]], and in $Set$ every morphism which is both is an isomorphism. Hence $[-, S]$ reflects isomorphisms.

\end{proof}


\begin{remark}\label{AlgebrasAsCompleteAtomicBooleanAlgebras}
**(algebras as complete atomic Boolean algebras)**
Thus, for $|S| \geq 2$, the [[Eilenberg-Moore algebras]] of the continuation monad on $Set$ are equivalent to [[complete atomic Boolean algebras]], as the category of these is equivalent to the [[opposite category|opposite]] of the category of sets. (For $|S| \leq 1$ the continuation monad degenerates: For $S = \ast$ it is constant on the point, while for $S = \varnothing$ it sends $\varnothing$ to itself and every other set to the point.)
\end{remark}

\begin{remark}\label{MonadicInMultipleWays}
**(monadic in multiple ways)**
This illustrates the fact that a category can be monadic over $\mathbf{Set}$ in multiple ways. In other words, one should not refer to a *category* $C$ as monadic over $Set$, unless everyone agrees to which "forgetful functor" $U\colon C \to \mathbf{Set}$ is being considered -- better is to refer to a *functor* as monadic. 
\end{remark}




## Related concepts

* [[selection monad]]

* [[continuation-passing style]]

* [[maybe monad]]

* [[state monad]]

## References

As a [[monad]] in [[mathematics]]:

* {#Kock70} [[Anders Kock]]: _On double dualization monads_, Math. Scand. **27** (1970) 151--165 &lbrack;[jstor:24489892](https://www.jstor.org/stable/24489892), [eudml:166154](https://eudml.org/doc/166154), [pdf](https://tildeweb.au.dk/au76680/DD.pdf)&rbrack;

* {#Kock72} [[Anders Kock]], *Strong functors and monoidal monads*, Archiv der Mathematik **23** (1972) 113-120 &lbrack;[doi:10.1007/BF01304852](https://doi.org/10.1007/BF01304852)&rbrack;

As a [[monad in computer science]]:

* {#Moggi91} [[Eugenio Moggi]], Ex. 1.1 in: *Notions of computation and monads*, Information and Computation **93** 1 (1991) 55-92 &lbrack;<a href="https://doi.org/10.1016/0890-5401(91)90052-4">doi:10.1016/0890-5401(91)90052-4</a>, [pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf)&rbrack;

* {#Milewski19} [[Bartosz Milewski]], §21.2.7 in: *Category Theory for Programmers*, Blurb (2019) &lbrack;[pdf](https://github.com/hmemcpy/milewski-ctfp-pdf/releases/download/v1.3.0/category-theory-for-programmers.pdf), [github](https://github.com/hmemcpy/milewski-ctfp-pdf), [webpage](https://bartoszmilewski.com/2014/10/28/category-theory-for-programmers-the-preface/), [ISBN:9780464243878](https://www.blurb.com/b/9621951-category-theory-for-programmers-new-edition-hardco)&rbrack;

* [[Tarmo Uustalu]], p.27 of: *Monads and Interaction Lecture 1* &lbrack;[pdf](https://cs.ioc.ee/~tarmo/mgs21/mgs1.pdf), [[Uustalu-Monads1.pdf:file]]&rbrack;, lecture notes for [MGS 2021](https://staffwww.dcs.shef.ac.uk/people/G.Struth/mgs21.html) (2021)

As a [[codensity monad]]:

* {#Leinster13} [[Tom Leinster]], *Codensity and the ultrafilter monad*, Theory and Applications of Categories **28** 13 (2013) 332-370 &lbrack;[arXiv:1209.3606](https://arxiv.org/abs/1209.3606), [tac:28-13](http://www.tac.mta.ca/tac/volumes/28/13/28-13abs.html)&rbrack;


In the generality of [[linear type theory]] as the linear [[double negation monad]]:

* {#MelliesTabareau07} [[Paul-André Melliès]], Nicolas Tabareau: _Linear continuations and duality_, preprint (2007) &lbrack;[hal:hal-00339156](https://hal.science/hal-00339156), [pdf](http://hal.inria.fr/docs/00/33/91/56/PDF/linear-control.pdf)&rbrack;

* [[Paul-André Melliès]], _The parametric continuation monad_, Mathematical Structures in Computer Science **27** 5 (2017) 651-680, Festschrift in honor of Corrado B&#246;hm for his 90th birthday &lbrack;[doi:10.1017/S0960129515000328](https://doi.org/10.1017/S0960129515000328), [[MelliesContinuation.pdf:file]]&rbrack;


The characterization of algebras over the continuation monad:

* {#HylandLevyPlotkinPower07} [[Martin Hyland]], [[Paul Blain Levy]], [[Gordon Plotkin]], [[John Power]]; Prop. 10 in: _Combining algebraic effects with continuations_, Theoretical Computer Science **375** 1-3 (2007) 20-40 &lbrack;[pdf](https://homepages.inf.ed.ac.uk/gdp/publications/comb_cont_journal.pdf)&rbrack;

A characterisation of ([[enriched monad|enriched]]) monads isomorphic to continuation monads is given in:

* Christopher Townsend, _When are enriched strong monads double exponential monads?_, Bulletin of the Belgian Mathematical Society-Simon Stevin **23.2** (2016) 311--319 &lbrack;[doi:10.36045/bbms/1464710120](http://doi.org/10.36045/bbms/1464710120)&rbrack;

[[!redirects continuation monads]]

[[!redirects double dualization monad]]
[[!redirects double dualization monads]]