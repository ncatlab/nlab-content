> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", there is no harm in breaking the lock, as it is just caused by bot traffic. When the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.



***



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
**(λ-notation)**
We denote morphisms by terms of the [[simply typed lambda calculus]] (in the cartesian case) or of the [[linear type theory|linear λ-calculus]] (in the general symmetric monoidal case), interpreted in $\mathcal{C}$ as its [[internal language]]:

* a term $t$ of type $B$ in a context of variables $x_1 : X_1, \cdots, x_n : X_n$ denotes a morphism $X_1 \otimes \cdots \otimes X_n \to B$;

* application $k(x)$, for $k : [X,S]$ and $x : X$, denotes the [[evaluation map]], $\mathrm{ev}(k \otimes x)$;

* abstraction $\lambda (x : X).\, t$ denotes the [[adjunct]] ("currying") of the morphism denoted by $t$.

By the [[universal property]] of the internal hom, these terms satisfy $\beta$-reduction $\big(\lambda x.\, t\big)(a) = t[a/x]$ and $\eta$-reduction $\lambda x.\, k(x) = k$.

In the cartesian case this is equivalently the usual notation in terms of [[generalized elements]]. In the general symmetric monoidal case it is legitimate here because all terms below use each bound variable exactly once (Rem. \ref{Linearity}).

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
The hom-isomorphism of this adjunction is the composite of [[natural isomorphisms]]
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
which in λ-notation (Rem. \ref{LambdaNotation}) is "swapping the arguments":
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
This bijection is its own inverse: $\widetilde{\widetilde{\phi}} = \phi$.
\end{proposition}

\begin{proof}
Each of the displayed bijections is natural in $X \in \mathcal{C}$ and in $A \in \mathcal{C}^{op}$; the outer two by the definition of the internal hom, and the middle one by naturality of the symmetry. That the composite is an [[involution]] follows from $\sigma_{A,X} \circ \sigma_{X,A} = \mathrm{id}$, or directly from the λ-formula.
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
In λ-notation:
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
Explicitly, the components are as follows (we write $D_S$ instead of $D$ where the dependence on $S$ needs to be shown):

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
which in λ-notation reads:
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
In the λ-term for $\mu_X$ in Def. \ref{TheContinuationMonad} the subterms have the following types:
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
In words: $\mu_X(M)$ is the functional on continuations which, given a continuation $k \colon X \to S$, evaluates $M$ on the "evaluation at $k$" functional
$$
  \mathrm{ev}_k
    \;:=\;
  \eta_{[X,S]}(k)
    \;=\;
  \lambda (c : [ [X,S],S]).\, c(k)
  \,,
$$
hence:
$$
  \mu_X(M)(k) \;=\; M(\mathrm{ev}_k)
  \,.
$$
Notice that $M$ is _not_ applied to the bound variable $c$ (which would not be well-typed) but to the λ-abstraction $\lambda c.\, c(k)$ over $c$, whose body $c(k)$ is where the continuation $k$ enters.
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

Alternatively, in λ-notation, using only $\beta$- and $\eta$-reduction:
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
    \;=\;
    \mu_X\big(D(\mu_X)(\mathcal{M})\big)
    \mathrlap{\,.}
  }
$$
\end{proof}

\begin{remark}\label{Linearity}
**(linearity and the role of the symmetry)**
In each of the λ-terms in Def. \ref{TheContinuationMonad} (and in Prop. \ref{KleisliExtension} and Prop. \ref{Strength} below) every bound variable occurs exactly once. Therefore these terms make sense in the [[linear type theory|internal linear type theory]] of any symmetric closed monoidal category: they use neither [[diagonal|duplication]] nor [[projection|deletion]] of variables, which is why the definition does not require $\mathcal{C}$ to be [[cartesian monoidal category|cartesian]] (see [Melliès & Tabareau 2008](#MelliesTabareau08)).

On the other hand, the symmetry $\sigma$ is used, if implicitly: it is the exchange rule which allows to form $k(x)$ in the context $x : X,\, k : [X,S]$, as in the definition of $\eta_X$. In a non-symmetric [[biclosed monoidal category]] one instead has to alternate between the two one-sided internal homs, $X \mapsto [ [X,S]_r, S]_l$.
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
This is the form in which the continuation monad appears in [Moggi (1991), Ex. 1.1](#Moggi91). In [[Haskell]]-notation, ignoring the `newtype`-wrapper of `Cont r a`:

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

Restricting to upward closed families, to [[filters]], or to [[ultrafilters]] yields submonads, the last one being the [[ultrafilter monad]], whose [[algebras over a monad|algebras]] are the [[compact Hausdorff spaces]] (see [Leinster (2013)](#Leinster13) and the discussion of the [[Stone-Čech compactification]] above).
\end{example}

\begin{example}\label{DoubleDualVectorSpaces}
**(double dual vector spaces)**
For $\mathcal{C} = \mathrm{Vect}_k$ the category of [[vector spaces]] over a [[field]] $k$, with $\otimes$ the [[tensor product of vector spaces]], and with $S = k$ the [[ground field]], the continuation monad is
$$
  V \;\mapsto\; V^{\ast\ast}
$$
with $\eta_V \colon V \to V^{\ast\ast}$ the canonical inclusion of a [[vector space]] into its [[dual vector space|double dual]], and with multiplication
$\mu_V = (\eta_{V^\ast})^\ast \colon V^{\ast\ast\ast\ast} \to V^{\ast\ast}$
the [[dual linear map]] of the canonical inclusion $V^\ast \hookrightarrow V^{\ast\ast\ast}$. This is an example where $\mathcal{C}$ is not cartesian (cf. Rem. \ref{Linearity}). On [[finite-dimensional vector spaces]] the unit $\eta$ is an isomorphism.
\end{example}





* {#Kock70} [[Anders Kock]], _On the double dualization monad_, Math. Scand., 27 (1970), p151-165.


* {#Kock72} [[Anders Kock]], *Strong functors and monoidal monads*, Archiv der Mathematik **23** (1972) 113-120 &lbrack;[doi:10.1007/BF01304852](https://doi.org/10.1007/BF01304852)&rbrack;

% -- add anchor to the existing Melliès–Tabareau item:

* {#MelliesTabareau08} [[Paul-André Melliès]], Nicolas Tabareau, _Linear continuation and duality_, 2008 ([pdf](http://hal.inria.fr/docs/00/33/91/56/PDF/linear-control.pdf))

% -- new item, e.g. in a new paragraph "As a codensity monad:"

As a [[codensity monad]]:

* {#Leinster13} [[Tom Leinster]], *Codensity and the ultrafilter monad*, Theory and Applications of Categories **28** 13 (2013) 332-370 &lbrack;[arXiv:1209.3606](https://arxiv.org/abs/1209.3606), [tac:28-13](http://www.tac.mta.ca/tac/volumes/28/13/28-13abs.html)&rbrack;

***

[[JoshuaDuality.pdf:file]]

quantum incrementer:

* *A Class of Efficient Quantum Incrementer Gates for Quantum Circuit Synthesis*, International Journal of Modern Physics B **28** 01 (2014) 1350191 \[<a href="https://doi.org/10.1142/S0217979213501919">doi:10.1142/S0217979213501919</a>\]

* Vivien Vandaele: *Asymptotically Optimal Quantum Circuits for Comparators and Incrementers* \[<a href="https://arxiv.org/abs/2603.12917">arXiv:2603.12917</a>\]

